# Chapter 7: Choosing a Model Is Eight Trade-offs, Not One Ranking

**Summary:** *Google publishes eight factors for choosing a foundation model, and the exam tests them by naming one constraint in a scenario and offering you four factors that all sound sensible. There is no ranking among the eight, which is the thing candidates most want there to be. What decides the answer is which single factor the scenario has made impossible to satisfy, and that is a different question from which factor is most important in general.*

## The Meeting Where Everyone Is Right

You are in a review for a project that will read long legal agreements and answer questions about them. Four people speak.

Security says the documents cannot leave a controlled environment. Finance says the per-token cost at the projected volume is the thing that will kill this. Engineering says the agreements run to eighty pages and the model has to hold a whole one at once. The product lead says the output has to use the firm's exact clause terminology or the lawyers will not touch it.

Every one of those is on Google's list of factors. Every one is true. And on a question here, exactly one of them will be the answer, because exactly one will be the thing the scenario has made binding.

## The Binding Constraint, and the Eight Candidates

Google's factors for choosing a foundation model: modality, context window, security, availability and reliability, cost, performance, fine-tuning, and customization.<sup>[1]</sup> The study guide works through four of them in detail, adding that performance means accuracy, speed and efficiency considered against cost, and that availability means uptime, redundancy and recovery under load.<sup>[2]</sup>

**The binding constraint** is the one factor the scenario has pinned. The other seven still matter, and on this exam they are distractors.

| Factor | The question it answers | The scenario phrase that pins it |
|---|---|---|
| Modality | What data types go in and come out? | images, audio, video, a mix of formats |
| Context window | How much can it consider at once? | full document, entire transcript, eighty pages, whole history |
| Security | Where can the data go, and who sees it? | cannot leave, regulated, confidential, residency |
| Availability and reliability | Will it be there under load? | uptime, always on, peak season, disaster recovery |
| Cost | What does it cost at this volume? | per request, at scale, budget, millions of calls |
| Performance | Is it accurate and fast enough? | response time, accuracy threshold, latency budget |
| Fine-tuning | Can it be trained further on our data? | adapt to our domain, improve on our examples |
| Customization | Can its behaviour be shaped to our requirements? | our terminology, our format, our tone, our rules |

Read the last two rows together, because the exam distinguishes them and candidates often do not. **Fine-tuning is additional training on your data to improve performance on your tasks.**<sup>[2]</sup> Customization is the broader question of whether the model's behaviour can be shaped to your requirements at all, by any means available.

That distinction decides a real question. A scenario about a regulated industry needing exact terminology and prescribed formatting is a customization question: what has to change is how the model writes. Security, cost and availability are all genuine concerns in a regulated industry, and none of them changes a single word of the output.

## How to Find the Binding Constraint in One Pass

Three questions, in order, and they resolve most of these.

**What does the scenario say the model cannot currently do?** Not what would be nice. What is stated as a hard requirement that a default choice would fail.

**Would changing that requirement change the answer?** If the answer stays the same when you delete the clause, the clause was not the constraint.

**Is the constraint about the model, or about the project?** A limit on accelerator supply is not a factor in the eight. It is a condition that forces a choice *within* one: limited compute means a smaller, less complex model, so it arrives as a question about which foundation model and what size.

That third question catches a question type worth preparing for. A scenario can spend most of its words on something irrelevant, mention a hardware limit in one clause, and ask what that limit actually bears on. The answer is the model and its size, because larger and more complex models need more capacity to run. *The ethics paragraph in that scenario is scenery.* It is there because it is the kind of thing a reader expects to matter, and the question asked what the stated constraint determines.

## Pre-trained or Custom Is the Decision Everything Else Hangs Off

One choice sits above the eight factors rather than among them, and the exam treats it as the most consequential planning decision in a gen AI project: whether you use a pre-trained model or build a custom one.<sup>[1]</sup><sup>[2]</sup>

It is the first decision because it determines the shape of everything after it.

| | Pre-trained model | Custom model |
|---|---|---|
| What you supply | Prompts, and your data for grounding | A training dataset, and the expertise to use it |
| Time to something working | Days | Months |
| Who you need | People who can write and evaluate prompts | Humans with machine learning expertise |
| What you control | The inputs and the surrounding system | The model itself |
| When it is right | The task is well served by a general model | The task genuinely needs behaviour a general model cannot reach |

Google's own guidance pushes harder towards pre-trained than teams expect. Where there is no suitable training dataset, or not enough of one, the recommended path is a generative model with prompt engineering, tuned further later if the work is specialised. And where the business priority is reaching the market sooner, that is also the generative path rather than custom training.<sup>[3]</sup>

**The build-it-ourselves answer** is the named trap here. Custom training reads as the serious, rigorous choice, and the scenario will often include something that sounds like a reason for it: a specialised domain, proprietary data, a competitive requirement. None of those is sufficient on its own. The question is whether a pre-trained model plus grounding and prompting can already do the job, and usually it can.

## How Wrong Answers Are Built on This Material

These questions are built by offering four true statements about four real factors. There is no option you can discard for being wrong, which is why reading quickly is actively harmful: every option passes.

- **The most-important-in-general answer.** Security, or cost, offered because they are the factors a sensible leader worries about most often. They are correct whenever the scenario pins them, and they are the default wrong answer when it pins something else.
- **The same-industry answer.** It names the factor you would expect that industry to care about, rather than the one the stem specified. Healthcare suggests security, retail suggests cost, and the exam uses that expectation against you.
- **The adjacent-factor answer.** Fine-tuning offered where customization is wanted, performance offered where context window is wanted. Each pair is genuinely close and the distinction is specific.
- **The scenery answer.** It latches onto the most emotive detail in the scenario, often an ethical or reputational concern, when the question asked what a stated technical limit determines.
- **The build-it-ourselves answer.** Custom training where a pre-trained model and good prompting would do.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Names a document length the model must hold | Context window | Performance, because speed is also mentioned |
| Requires exact terminology or prescribed format | Customization | Security, because the industry is regulated |
| Names limited accelerator capacity | Model choice and its size | An ethical concern raised earlier in the stem |
| Asks what to decide first in a gen AI project | Pre-trained or custom | A later decision such as which tool or which cloud |
| Lists several data types | Modality | Whichever factor the industry suggests |
| Mentions improving on our own examples | Fine-tuning | Customization, which is the broader term |

The habit: before reading the options, say the constraint out loud in four words. "Must hold whole document." "Must use our terminology." Then find the factor that names it.

## What to Remember

- **Eight factors, no ranking**: **modality, context window, security, availability and reliability, cost, performance, fine-tuning, customization**.
- **The binding constraint** is the one factor the scenario has pinned. **Delete the clause**; if the answer does not change, **that clause was not it**.
- **Context window is how much the model can consider at once.** A stated **document length or full transcript** pins it.
- **Fine-tuning is further training on your data**; **customization is shaping the behaviour** by any means. **Exact terminology and formatting** is **customization**.
- **Performance means accuracy, speed and efficiency**, judged against cost. **Availability means uptime, redundancy and recovery** under load.
- **Limited compute is not one of the eight.** It **forces a smaller, less complex model**, so it arrives as a question about **which model and what size**.
- **Pre-trained or custom is the decision everything else hangs off**, and it is the right answer to "what should we decide first".
- **Google's guidance leans pre-trained.** **No sufficient dataset**, or a need to **reach market sooner**, both point at **a generative model with prompt engineering**.
- **Specialised domain and proprietary data are not reasons to train your own.** Ask first whether **grounding and prompting** already do the job.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. When to use generative AI or traditional AI. https://docs.cloud.google.com/docs/ai-ml/generative-ai/generative-ai-or-traditional-ai
