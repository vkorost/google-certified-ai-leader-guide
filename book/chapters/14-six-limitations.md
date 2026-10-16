# Chapter 14: Six Limitations, and the Remedy for Each

**Summary:** *Google names six ways a foundation model falls short, and five recommended ways to deal with them. The exam pairs one limitation with four remedies and asks which one applies, and the mapping is not one-to-one, which is where the marks are lost. Two of the limitations have the same remedy, one of them has no technical remedy at all, and the most popular wrong answer is a remedy that is genuinely useful against a different problem.*

## Five Hundred Correct Answers and One Confident Invention

A summarising tool runs over internal reports for a month. It produces five hundred summaries. Four hundred and ninety-nine are fine.

One contains a figure that appears in none of the source documents, stated with exactly the same assurance as everything else.

That is not a failure rate you can manage with a quality threshold, and it is not an accuracy problem in the ordinary sense. A wrong answer here is well formed, fluent, and indistinguishable from a right one until somebody checks it against the source. Knowing which of the six limitations this is, and which of the five remedies addresses it, is the whole of this objective.

## The Six, and What Each One Looks Like

Google's six: data dependency, knowledge cutoff, bias, fairness, hallucination, edge cases.<sup>[1]</sup>

| Limitation | What it is | How it shows up |
|---|---|---|
| **Data dependency** | Performance rests on the training data, so flaws in it reach the output<sup>[2]</sup> | Consistently poor results across a whole category |
| **Knowledge cutoff** | Training stopped at a date, so the model may know nothing after it<sup>[2]</sup> | Confident answers about a world that has since changed |
| **Bias** | Large training sets carry biases, and a model can amplify even subtle ones<sup>[2]</sup> | Systematically different treatment of comparable cases |
| **Fairness** | Whether outcomes are equitable, which has to be assessed rather than assumed<sup>[2]</sup> | A model that is accurate overall and unequal across groups |
| **Hallucination** | Output that is not accurate and not based on anything real<sup>[2]</sup> | Fluent, confident, fabricated specifics |
| **Edge cases** | Rare, atypical situations that expose weaknesses<sup>[2]</sup> | Reliable on the ordinary, erratic on the unusual |

Two pairs need separating, because the exam separates them.

**Data dependency against hallucination.** Both produce wrong output. Data dependency is a defect inherited from the training set, so it is systematic: the same kind of question is wrong every time, and the cause is upstream. A hallucination is an invention, and it appears in output that is otherwise correct. If a scenario describes consistently weak performance on a category, that is data. If it describes something made up amid good work, that is a hallucination.

**Bias against fairness.** Bias is the property of the data and the model: a skew learned and then amplified. Fairness is the property of the outcome, and it is a judgement somebody has to make. A scenario describing skewed training material is talking about bias. A scenario asking whether the results treat people equitably is talking about fairness.

## The Five Remedies, and What Each One Actually Does

Google recommends five practices against these. Two change where the answer comes from, grounding and retrieval-augmented generation. Two change the request or the model, prompt engineering and fine-tuning. One changes who signs it off, which is keeping humans in the loop.<sup>[1]</sup>

**The limitation-to-remedy map** is the thing to memorise, and the useful version is not a list of five but a table of which problem each one can and cannot touch.

| Remedy | What it changes | The limitation it answers | What it cannot fix |
|---|---|---|---|
| Grounding | Where the answer comes from: a designated source rather than the weights | Hallucination, above all | Nuance, judgement, fairness |
| RAG | The same, by retrieving current passages at question time | Knowledge cutoff, and stale facts | Anything about how the model writes |
| Prompt engineering | What you asked for, and how precisely | Vague or unfocused output | Missing facts the model never had |
| Fine-tuning | How the model behaves, learned from your examples | Format, register, specialised tasks | Freshness, factuality, accountability |
| A person in the loop | Who approves before it counts | Nuance, judgement, consequence, edge cases | Nothing at scale; it costs time per item |

Three pairings carry most of the exam's weight here, and all three are worth holding as reflexes.

**Hallucination is answered by grounding.** Not by lowering the randomness setting, not by filtering, not by fine-tuning. Grounding anchors the output to a source that can be checked, which is the only one of those that makes factuality enforceable.<sup>[4]</sup>

**Knowledge cutoff is answered by retrieval.** The model cannot be taught its way past a date; something has to fetch the current information when the question is asked.<sup>[3]</sup>

**Nuance and judgement are answered by people.** When a scenario says the output misses something a reader would catch, you are not looking at a parameter, a prompt or a tuning job. You are looking at a review step, and you will have to pay for it in time.

## Humans in the Loop Is Five Different Controls

This is the remedy the exam returns to most often, and Google names five distinct places it belongs.<sup>[2]</sup>

| Where the human sits | Why it belongs there |
|---|---|
| **Content moderation** | Judging user-generated material in context, catching harm an algorithm reads past |
| **Sensitive applications** | Fields like healthcare and finance, where an automated error carries real cost |
| **High-stakes decisions** | Review protecting both accuracy and accountability on consequential calls |
| **Pre-generation review** | Experts validating output before anybody relies on it, catching errors and bias early |
| **Post-generation review** | Continuous feedback after release, so the system keeps adapting |

Three of those five are blueprint surface no question in circulation tests, and the two review positions are the ones most worth knowing, because they answer different scenarios. **Pre-generation review** is the answer when the cost of a wrong output reaching someone is high. **Post-generation review** is the answer when the concern is drift, changing context, or improvement over time.

The decision rule you need out of all this: **a reviewer belongs wherever a wrong output would be acted on before anybody noticed it was wrong.** That sentence covers all five positions and it will carry you into situations Google never listed.

## How Wrong Answers Are Built on This Material

Distractors here are the other four remedies, every one of them a genuine Google-recommended practice. That is what makes this objective difficult despite being purely conceptual: there is no wrong answer in the list, only an inapplicable one.

- **The settings answer.** A sampling parameter offered against hallucination or bias. Lowering randomness makes output more predictable and does nothing about whether it is true. This is the commonest wrong answer on the whole objective.
- **The fine-tuning answer.** Further training offered against a freshness problem or a factuality problem. Tuning changes behaviour; it does not install facts and it does not enforce accuracy.
- **The filtering answer.** Safety settings offered against inaccuracy. Filters remove harmful content, not false content.
- **The automation answer.** More autonomy offered where the scenario described missing judgement. If somebody is catching what the model cannot, removing them is not an improvement, however much it looks like progress.
- **The adjacent-limitation answer.** On diagnosis questions, the limitation next door: data dependency for a hallucination, bias for a fairness question, knowledge cutoff for an edge case.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Describes confident fabrication | Hallucination, remedied by grounding | A randomness or safety setting |
| Describes ignorance of recent events | Knowledge cutoff, remedied by retrieval | Fine-tuning on recent data |
| Describes consistent failure on one category | Data dependency | Hallucination, because the output is wrong |
| Describes success on normal cases, failure on rare ones | Edge cases | Data dependency, or hallucination |
| Asks whether outcomes treat groups equitably | Fairness | Bias, which is the cause rather than the question |
| Says the output misses nuance a person would catch | Humans in the loop | A prompting or tuning change |
| Needs output validated before anyone relies on it | Pre-generation review | Post-generation review |

One habit transfers past the table. For every candidate remedy, say what it changes: the source, the freshness, the request, the behaviour, or the approval. Then ask whether that is what the scenario said was wrong.

## What to Remember

- **Six limitations**: **data dependency, knowledge cutoff, bias, fairness, hallucination, edge cases**.
- **Five recommended remedies**: **grounding, RAG, prompt engineering, fine-tuning, humans in the loop**.
- **Hallucination is answered by grounding**, because grounding **anchors output to a checkable source**. **Not** by a randomness setting, a filter, or tuning.
- **Knowledge cutoff is answered by retrieval.** A model **cannot be taught past a date**; something must **fetch current information at question time**.
- **Data dependency is systematic and upstream**; **hallucination is an invention inside otherwise good output**. Consistent failure on a category means **data**.
- **Bias is the skew in data and model; fairness is whether outcomes are equitable.** Bias is **the cause**, fairness **the question**.
- **Edge cases mean reliable on the ordinary, erratic on the unusual.** The remedy is **human review and monitoring**, not more training on normal cases.
- **Humans in the loop covers five places**: **content moderation, sensitive applications, high-stakes decisions, pre-generation review, post-generation review**.
- **The rule that transfers**: put a reviewer **wherever a wrong output would be acted on before anybody noticed**.
- **Name what each remedy changes** before choosing: **the source, the freshness, the request, the behaviour, or the approval**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. RAG Engine overview. https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/rag-engine/rag-overview
4. Design agents in Agent Studio. https://docs.cloud.google.com/gemini-enterprise-agent-platform/agent-studio/design-agents
