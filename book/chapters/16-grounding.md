# Chapter 16: Grounding Changes Where the Answer Comes From

**Summary:** *Grounding is the most consequential idea in this half of the exam and the one candidates half-know. It does not make a model smarter, more careful or better trained. It changes where the answer comes from, and that single change is what makes a response checkable. The exam tests two things about it: that you know which problems it solves, and that you know which of three kinds of data a given scenario needs to be grounded in.*

## The Only Question a Grounded Answer Can Be Asked

An assistant tells a customer their order shipped on Tuesday.

If that answer came out of the model's weights, there is no way to find out whether it is true without going and looking in the order system yourself. If it came from the order system, the answer carries its own receipt, and the humans who have to stand behind it can check it in seconds.

Nothing about the model changed between those two sentences. What changed is where the answer came from, and that is the entire subject of this chapter.

## Grounding Connects Output to Something Verifiable

Google's definition is one line long: grounding ties what the model says to sources somebody can go and verify.<sup>[2]</sup>

**The provenance question** is the one a grounded system can answer and an ungrounded one cannot: *where did that come from?* Hold grounding as the answer to that question rather than as a quality improvement, because the exam's distractors are all quality improvements.

Which means grounding is the right answer to a specific and narrow set of problems:

| The problem | Why grounding addresses it |
|---|---|
| The model invents specifics | The answer has to come from the source, so there is nothing to invent from |
| The model does not know recent events | The source is current even though the training is not |
| The answer has to be traceable | The source can be named and checked |
| The answer must use only our own material | The retrieval set is ours, and only ours |

And wrong for problems that look adjacent. Grounding does not change how the model writes, does not improve its reasoning, does not make it more careful, and does not filter anything. Those are tuning, prompting and safety settings respectively, and each is a distractor here.

## Retrieval-Augmented Generation Is the Mechanism

RAG is how grounding usually happens, and Google sets it out in four steps.<sup>[2]</sup>

1. **Retrieval.** The model pulls relevant material from an external source, using tooling.
2. **Augmentation.** What came back gets folded into the prompt.
3. **Generation.** The model produces its answer from that enlarged prompt.
4. **Iteration**, which is optional. It can go back and retrieve again if it needs to.

Step two explains both why RAG works and why its limits are where they are. The retrieved material arrives **as part of the prompt**. Nothing is being learned and nothing is being stored. The model is simply answering a question that now has the relevant passage attached to it, which is why RAG delivers current information and changes nothing about the model's behaviour.

The benefit to state, and the exam asks for it in these words often enough to matter: retrieval brings in **external, up-to-date information at the moment of the query**, which is what makes the answer accurate and relevant when training data alone would not.<sup>[3]</sup>

It also has a cost profile worth knowing, because one question turns on it. RAG is the **cheap** way to fix missing knowledge. Fine-tuning on the same material costs more, takes longer, and would have to be repeated every time the material changed.

## Three Kinds of Data to Ground In, and the Exam Cares Which

This is the distinction most likely to decide a question on this objective.<sup>[1]</sup>

| Kind | What it is | The scenario cue |
|---|---|---|
| **First-party data** | The organisation's own records and content | Our documents, our customers, their purchase history, our policies |
| **Third-party data** | Data from another organisation, licensed or supplied | Industry data, a partner's catalogue, a bought dataset |
| **World data** | What is publicly known, out on the web | Current events, public facts, anything the organisation does not own |

First-party is the one the exam tests hardest, and the cue is possession. A customer asking about their own recent purchases can only be answered from the company's own records: no public source knows, and no third party has it. That question is a first-party grounding question and nothing else will do.

World data is the blueprint term that no question in circulation uses, which makes it worth the ten seconds. When a scenario needs something true about the world right now, and the organisation has no record of it, that is world data.

## Google's Three Grounding Offerings

The blueprint names three, and they are chosen by which of those kinds of data you need.<sup>[1]</sup>

| Offering | What it grounds in | Reach for it when |
|---|---|---|
| **Prebuilt RAG with Agent Search** | The organisation's own content, licensed outside sources, and Google's knowledge graph<sup>[5]</sup> | Search and answers over the organisation's own material, managed rather than built |
| **RAG APIs** | Whatever you point them at | An application already exists and needs retrieval wired into it<sup>[3]</sup> |
| **Grounding with Google Search** | The public web, in real time<sup>[4]</sup> | The answer depends on current world information |

The pairing to memorise is the last two rows against each other. **Agent Search grounds in what the organisation has. Grounding with Google Search grounds in what the world knows.** A scenario wanting answers restricted to proprietary sources must not be answered with Google Search, and a scenario needing today's public information cannot be answered from an internal repository.

Chapter 10 met the same distinction from the product side, as Agent Search against Google Search. It is the same decision: whose content is the model allowed to use.

## How Wrong Answers Are Built on This Material

Almost every distractor here is a real technique that improves something. The failure mode is answering "what would help?" instead of "what does this scenario require?"

- **The quality-improvement answer.** Fine-tuning, a better model, or a longer prompt, offered where provenance was the requirement. Each might make the output better. None of them makes it checkable.
- **The wrong-source answer.** Google Search where the scenario said only our own documents, or an internal repository where the scenario needed current public facts. This is the commonest error on the objective and it is always decided by one clause in the stem.
- **The settings answer.** Lowering randomness, or turning on a filter, offered against fabrication. Neither connects the output to anything.
- **The expensive-fix answer.** Fine-tuning where the scenario asks for a cost-effective way to add missing current knowledge. Retrieval is the cheap one.
- **The learned-it answer.** Any option that describes the model *knowing* the new information rather than *fetching* it. Retrieval does not teach.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Needs answers only from our documents | Retrieval over those documents, first-party | Grounding with Google Search |
| Needs current public information | Grounding with Google Search | An internal knowledge base |
| Asks about a customer's own history | First-party grounding | Third-party or world data |
| Wants fabrication stopped | Grounding | A randomness or safety setting |
| Wants missing knowledge added cheaply | RAG | Fine-tuning on the new material |
| Already has an application needing retrieval | RAG APIs | Prebuilt RAG, which is the managed route |
| Wants search and answers over company content, managed | Prebuilt RAG with Agent Search | Building a retrieval pipeline |

The habit that transfers: before choosing, say whose data the answer has to come from. Ours, somebody else's, or the world's. That sentence picks the offering, and it is nearly always stated outright in the scenario.

## What to Remember

- **Grounding connects output to verifiable sources.** It answers **one question**: where did that come from?
- **Grounding changes the source, not the model.** It does **not** improve writing, reasoning or care, and it **filters nothing**.
- **RAG in four steps**: **retrieval**, **augmentation** into the prompt, **generation**, and optional **iteration**.
- **The retrieved material arrives as part of the prompt.** Nothing is learned and nothing is stored, which is why RAG delivers **current** information and changes **no behaviour**.
- **The benefit to state**: **external, up-to-date information at the moment of the query**.
- **RAG is the cheap fix for missing knowledge.** Fine-tuning the same material costs more and **goes stale again** the moment it changes.
- **Three kinds of data**: **first-party** is ours, **third-party** is somebody else's, **world** is public. The cue for first-party is **possession**.
- **A customer's own purchase history can only be first-party.** No public source knows it.
- **Agent Search grounds in what the organisation has**, plus **licensed outside sources** and **Google's knowledge graph**. **Grounding with Google Search** reaches **what the world knows**, in real time.
- **RAG APIs are for an application that already exists**; **prebuilt RAG with Agent Search is the managed route**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. RAG Engine overview. https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/rag-engine/rag-overview
4. Model interaction capabilities, Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/capabilities/interactions
5. Introduction to enterprise search. https://docs.cloud.google.com/generative-ai-app-builder/docs/enterprise-search-introduction
