# Chapter 1: What a Leader Exam Tests, and What It Does Not

**Summary:** *This exam will hand you scenarios where several options are things a competent person would really do, and ask you to pick one. The deciding factor is almost never which option is most capable. It is which option sits at the level the certification says the role operates at: business-level knowledge of the products, strategic influence, conceptual understanding of the technology. Learn that level and a third of the exam stops being a guess. Miss it and you will reason your way, carefully, to the wrong answer.*

## Two Answers to One Scenario, and Only One of Them Is Being Asked For

Suppose a support organisation is slow to reply to customers, and you are asked what to do about it.

Here are two answers.

The first says: take five years of support transcripts, tune a model on them, and measure reply quality before and after. The second says: work out which specific business problem is being solved and what outcome would count as solving it, then pick the approach that serves it.

Both are reasonable. The first is what a good engineer would say, and nothing about it is wrong. On this exam it is still the losing answer, almost every time, and the reason is not that tuning is a bad idea. It is that the question was never about tuning.

That gap is the whole chapter.

## The Certification Tells You What Level an Answer Sits At

Google publishes a description of the role, and it is worth more than its length suggests. The required knowledge sits at business level: what each product is for, rather than how it is built. The holder is expected to spot where gen AI could change how a business function works, and to be equally usable in a room full of engineers and a room full of executives. Then comes the sentence that does the real work. The expertise, Google says, is strategic rather than technical: leadership and influence, not implementation, with the technology understood at the level of concepts.<sup>[1]</sup>

Read the shape of that. It is a claim about which decisions belong to the reader.

Call the thing you are looking for **the business-level answer**: the option pitched at the altitude where a leader actually decides. Not the most thorough option. Not the most technical. The one a person with this job would own.

A caution immediately, because the obvious misreading of that is expensive. **The business-level answer is not the vaguest option on the list.** The second-largest part of this exam, 35% of it, is a products inventory, and a candidate who learned to pick whichever option sounds strategic will lose most of it.<sup>[1]</sup> Google names specific services and expects you to know which one fits.

That gives this book its first named trap. **The executive-summary answer** is the option built from outcome words with no object in it: align stakeholders, drive adoption, ensure success, build a roadmap. It wins no points for sounding like leadership. It loses whenever a different option names the service that would actually do the job. The business-level answer names things. *It just does not configure them.*

## Four Sections, and What Each One Is Really Asking

Google divides the exam into four sections and publishes a weight for each. There are 15 objectives under those four, and **no weight is published for any individual objective.**<sup>[1]</sup>

| Section | The question underneath it | What a right answer looks like | Weight |
|---|---|---|---|
| 1 Fundamentals of gen AI | Can you put a concept in the right box? | A definition that holds at the boundary | 30% |
| 2 Google Cloud's gen AI offerings | Can you name the product that fits? | A specific service, not a category | 35% |
| 3 Techniques to improve output | Can you pick the remedy for the stated failure? | The one that addresses *this* failure | 20% |
| 4 Business strategies | Can you decide what to do first? | Google's published recommendation | 15% |

That last column is the useful one, because the four sections reward four different habits and candidates tend to bring only one.

Note what the missing per-objective weight costs you. Sections 1 and 2 are 65% of the exam between them, and inside section 1 there is no way to know from Google whether the models objective is worth twice the data objective or half of it. **Revising by objective is revising at a granularity Google did not publish.** Revise by section, and treat every objective inside a section as capable of carrying a question.

## Three Question Shapes, and the One That Has a Published Answer

Almost everything on this exam arrives in one of three shapes.

The **definition** shape asks what something is: which option describes a multimodal application, which one defines generative AI. These reward precision at the edge of a concept rather than familiarity with it. Knowing roughly what unsupervised learning is will not separate two options that both sound right.

The **fit** shape gives you a situation and asks which product, model or technique belongs in it. This is most of section 2 and much of section 3. The situation always contains the deciding detail, and the next section is about finding it.

The **practice** shape is the one to notice. It says *according to Google-recommended practices*, or *Google-recommended*, and then asks what to do, or what to do first. That phrasing is not decoration. It means Google has published an answer, and the exam wants Google's answer rather than a defensible one.

So the third named trap: **the defensible-alternative answer.** An option that a thoughtful leader could argue for, that is not what Google recommends. On a practice-shape question your own judgement is the distractor. When you see that phrasing, stop reasoning from first principles and recall the published list.

There is a corollary that catches people who do recall it. Google's recommendations are frequently two-sided, and a wrong option will hand you one side. The published strategy advice combines leadership setting direction with employees finding practical applications, which means an option offering only the first is half an answer dressed as a whole one.<sup>[2]</sup> **Half of Google's recommendation is a wrong answer**, and it is wrong in the most convincing way available: by being correct as far as it goes.

## One Clause in the Scenario Decides It

Fit-shape questions are long. Most of the words are furniture: an industry, a team, a quantity, a sense of urgency. The decision usually rests on a single clause.

**The test is deletion. Find the clause that, if you removed it, would change the answer. That clause is the question.**

The clauses come in recognisable families, and each family points somewhere different:

| The clause says something about | It is asking about |
|---|---|
| Information the model could not have known | Where the answer comes from, not how the model is built |
| Data that must not leave the organisation | Whose data grounds the answer |
| A team with no machine learning background | How much building the solution requires |
| Audio, images or video in the input or output | Which modality the model has to handle |
| A decision with consequences for a person | Whether a human stays in the loop |
| Response time, or a device with poor connectivity | Where the computing happens |
| A reply that has to be traceable to a source | Grounding, and whether the source is citable |

None of those is a product name, and that is the point. The scenario describes a constraint; the options offer products; the work is mapping one to the other. Every chapter from here on is a column of that table worked out properly.

Two more traps live in this gap. **The maximalist answer** offers several good practices at once: tune the model, add retrieval, put a human in the loop, monitor for drift. Nothing in it is wrong, which is why it survives a first read. It loses because the scenario named one constraint and another option addresses exactly that one. And **the right answer to a different question** is an option that would win if the deciding clause had said something else. It is the most common wrong answer on this exam, and the most instructive, because the way to see through it is to say out loud which question it answers.

## The Product Names Changed, and Both Names Still Matter

In April 2026 Google renamed most of this surface. The exam guide uses the new names. A great deal of material still in circulation uses the old ones, and Google's own documentation is mid-transition: the Dialogflow CX documentation currently opens by noting that some products and features "are in the process of being renamed."<sup>[3]</sup> The platform release notes write it as Agent Platform, "formerly Vertex AI."<sup>[4]</sup>

| Old name | Current name |
|---|---|
| Vertex AI | Gemini Enterprise Agent Platform, or Agent Platform |
| Vertex AI Search | Agent Search |
| Vertex AI Studio | Agent Studio |
| Vertex AI Agents | Conversational Agents |
| Vertex AI Agent Builder | Agent Platform |
| Agentspace | Gemini Enterprise |
| NotebookLM | Gemini Notebook |

Learn these as pairs rather than as replacements. You may meet either name, and an option naming the old one is not wrong for being old.

Which produces one final trap, and it is the mirror image of the one candidates expect. **The obsolete-name answer** is the assumption that a familiar old name must be the distractor. Two products that sound like they belong to the retired generation were not renamed at all: Dialogflow CX and Contact Center AI both have current documentation.<sup>[3]</sup> Rejecting an option because its name feels dated is not knowledge. It is pattern-matching on vocabulary, and it will take questions off you in the section that carries more weight than any other.

## How Wrong Answers Are Built on This Material

Wrong answers on this exam are not stupid, and this is the single most useful thing to know before you start. Nearly every one describes something a competent leader would really do. Elimination by obvious nonsense, which carries people through a lot of technical exams, does very little here.

They are built in five ways, and all five are about altitude or about scope rather than about facts.

- **The implementer's answer.** Technically the most capable option, and the one an engineer would choose. It is wrong because the question asks what a leader decides, not what a team builds. Tell: it specifies a method where the other options specify an outcome.
- **The executive-summary answer.** Outcome words with no object. Align, drive, ensure, enable. It becomes correct only when the question genuinely asks about organisational behaviour, which section 4 sometimes does.
- **The maximalist answer.** Several correct practices bundled together. It becomes correct only when the scenario names several constraints, which is rare.
- **Half of Google's recommendation.** One side of a two-sided published practice. It becomes correct only if the scenario rules the other half out explicitly.
- **The right answer to a different question.** Correct for a constraint the scenario did not state. It becomes correct the moment you misread which clause is load-bearing, which is why it works.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Names a business problem and asks what comes first | Clarify the problem and the desired outcome | A technique, chosen before the problem is defined |
| Says "Google-recommended" | The published recommendation, in full | Your own defensible alternative, or half of Google's |
| Describes one specific failure | The single remedy aimed at that failure | A bundle of good practices, one of which fits |
| Offers a familiar retired product name | Whichever option fits, old name or new | Rejecting the option because the name looks dated |
| Reads as strategy with no technical content | Still often a named Google service | The option made entirely of outcome words |

One habit transfers past all of it. Before choosing, say which question each remaining option is the right answer to. Two of the four usually answer a question you were not asked.

## What to Remember

- **The business-level answer**: the option at the altitude the role actually decides at, since the certification puts the expertise in **strategic leadership and influence rather than technical implementation**. It **names specific products** and does not configure them.
- **Four sections, four habits**: fundamentals wants **precise definitions**, offerings wants **the right service named**, techniques wants **the remedy for the stated failure**, strategies wants **Google's published recommendation**. Weights are **30, 35, 20, 15**.
- **No per-objective weight exists.** Google publishes weight per section only, across 15 objectives, so **revise by section** and assume any objective can carry a question.
- **"Google-recommended" means a published answer exists**, and your own reasoning becomes the distractor. Recall the list rather than deriving one.
- **Half of a two-sided recommendation is a wrong answer.** The strategy advice pairs **leadership setting direction with employees finding applications**; an option with only one side is incomplete, not partially right.
- **Find the clause you could delete to change the answer.** That clause is the question; the rest of the scenario is furniture.
- **Five ways wrong answers are built**: the **implementer's** answer, the **executive-summary** answer, the **maximalist** answer, **half of Google's** answer, and the **right answer to a different question**. None of them is nonsense, so **elimination by obvious error will not work**.
- **Carry both product names.** Vertex AI is **Agent Platform**, Vertex AI Search is **Agent Search**, Agentspace is **Gemini Enterprise**. But **Dialogflow CX and Contact Center AI were never renamed**, so a dated-sounding name is not evidence of a wrong option.
- The exam is **90 minutes, 50 to 60 multiple choice questions, $99, valid three years, no prerequisites**, delivered online- or onsite-proctored.<sup>[5]</sup>

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Dialogflow CX documentation. https://docs.cloud.google.com/dialogflow/cx/docs
4. Gemini Enterprise Agent Platform release notes. https://docs.cloud.google.com/gemini-enterprise-agent-platform/release-notes
5. Generative AI Leader certification. https://cloud.google.com/learn/certification/generative-ai-leader
