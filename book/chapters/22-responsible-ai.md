# Chapter 22: Responsible AI Is Four Obligations You Can Name

**Summary:** *This is the last objective, the smallest share of the exam, and the one with no product documentation behind it at all. What that means in practice is that the questions test whether you can name the specific obligation a scenario is short of, from a list of four that overlap in ordinary speech and not on this exam. Transparency, privacy, fairness and accountability are different failures with different remedies, and the exam will offer you all four every time.*

## The Letter That Says No and Nothing Else

A system declines a loan application. The letter says the application was unsuccessful.

The applicant asks why. Nobody can tell them, not because the information is withheld but because it was never produced. Complaints arrive. Somebody suggests retraining the model on more data, somebody else suggests testing it for bias, and both of those are reasonable things to do that would not fix this.

What is missing is not accuracy and not fairness. It is an account of the reasoning. **Harm you can name** is the skill this chapter builds, and the harm here has a name: the system is not explainable, so nobody can be accountable for what it decided.<sup>[1]</sup>

## Responsible AI Covers the Whole Lifecycle Too

Responsible AI means making sure your applications do not cause harm and are used ethically.<sup>[2]</sup> Like security, it has to be considered across the entire lifecycle, from data preparation and training through deployment and ongoing monitoring.<sup>[2]</sup>

The two chapters are deliberately adjacent and they are not the same. Chapter 21 is about harm done **to** the system. This one is about harm done **by** it. A question about protecting a model from attackers is secure AI; a question about a model treating people unfairly is responsible AI.

Google also publishes a set of **AI Principles** that this material sits under, and the blueprint names them.<sup>[1]</sup><sup>[3]</sup> The organisational form of those principles is a set of **ethical guidelines**, which the strategy advice in chapter 20 lists as something a gen AI strategy has to establish rather than assume.

## The Four Obligations, and What Each One Fails to Deliver

| Obligation | What it requires | What its absence looks like |
|---|---|---|
| **Transparency** | Being open about how the system is evaluated and what data it uses | Nobody outside the team can tell what the thing does with their information |
| **Privacy** | Managing the risk in personal data, through anonymisation and pseudonymisation | Personal details sitting in training data that nobody needed |
| **Fairness** | Outcomes that do not skew against groups, given data quality and bias | A system accurate overall and unequal in effect |
| **Accountability and explainability** | Decisions that can be explained, so somebody can answer for them | A decision nobody can account for, including the people who built it |

These are the four the blueprint lists, and the exam's technique is to offer all four and let you pick the one the scenario is actually short of.<sup>[1]</sup> They look similar from a distance. They are specific up close.

**Transparency is about being open; explainability is about a particular decision.** A company that publishes how its hiring tool is evaluated and what data it uses is being transparent. A company that can say why *this* applicant was scored as they were is being explainable. A scenario about building trust with candidates by being open about the evaluation logic and the data handling is a transparency question. A scenario about a specific rejection nobody can account for is an explainability question.

**Explainability and accountability travel together** and the exam treats them as a pair, which is correct: you cannot hold anybody answerable for a decision nobody can explain. When complaints are about unexplained outcomes, the answer usually names both.

## Privacy Means Changing the Data, Not Just Guarding It

Two techniques are named in the blueprint and one of them is the answer to a specific common question.<sup>[1]</sup>

**Anonymisation** removes or obscures the personal detail so it is no longer identifying. **Pseudonymisation** replaces identifiers with substitutes, so the data can still be worked with and the link back is held separately.

The exam's shape here is a scenario where personal information is sitting in material a model is going to train on. The answer is **anonymisation**: take the personal detail out of what the model learns from. The trap is an option offering to restrict access to the training data instead, which is a security control and a good one. It does not change what the model absorbs, and once a model has learned from personal data, the access control on the original dataset is beside the point.

Pseudonymisation is blueprint surface no question in circulation tests, which makes it worth the ten seconds: the identifiers are replaced rather than removed, so the data stays useful and the re-identification key is kept apart from it.

## Bias Comes From the Data, and That Is Where the Exam Puts It

Two question shapes on bias, and both resolve to the training data.

When a scenario describes a model producing a consistent demographic skew from neutral prompts, professional roles rendered as one gender, say, the cause the exam wants is **bias in the training data**.<sup>[2]</sup> Not a prompting defect, not a parameter, not a model-architecture problem. The model learned the pattern from what it was shown.

When a scenario asks which situation is most likely to produce an unfair, biased outcome, the answer is the one describing **skewed representation of groups** in the training set: a recognition system trained mostly on one demographic with little coverage of others.<sup>[2]</sup> The other options usually describe data quality problems, and those matter, and they produce inaccuracy rather than unfairness.

That distinction is the one to carry: **incomplete or messy data makes a model wrong; unrepresentative data makes it unfair.** Both are data problems and only one is a fairness problem.

## How Wrong Answers Are Built on This Material

This objective has no product documentation behind it, so the distractors are the other three obligations plus whatever a sensible manager would suggest. Every option is defensible and only one is on topic.

- **The adjacent-obligation answer.** Fairness where explainability was missing, privacy where transparency was, accountability where the issue was bias. The defence is to name in one word what the scenario's complaint is actually about.
- **The access-control-for-privacy answer.** Restricting who can see the training data where the personal information needed removing from it. A security control answering a privacy requirement.
- **The performance answer.** More data, a better model, higher accuracy, offered where the complaint was that nobody could explain a decision. Accuracy and explainability are independent: a model can be right and inscrutable.
- **The remove-the-human answer.** More automation offered on a responsibility question. On this objective it is always wrong, because every obligation here is ultimately somebody being answerable.
- **The speed-or-reach answer.** Faster processing, broader coverage, or efficiency offered where trust was being asked about. Real benefits, wrong subject.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Says nobody can explain a specific decision | Explainability, and accountability with it | Retraining, or testing for bias |
| Wants to build trust by being open about evaluation and data use | Transparency | Explainability, or fairness |
| Has personal information in the training data | Anonymisation | Restricting access to that data |
| Shows a consistent demographic skew from neutral prompts | Bias in the training data | A prompting or parameter problem |
| Asks which setup produces unfair outcomes | Unrepresentative coverage of groups | Incomplete or noisy data generally |
| Asks what to prioritise for responsible use | The obligation the scenario is short of | Efficiency, speed or reach |

The habit: say what the complaint is in one word. Unexplained. Unequal. Exposed. Opaque. Each of those words maps to exactly one of the four obligations, and the scenario nearly always uses it or something close to it.

## What to Remember

- **Responsible AI means applications that do not cause harm and are used ethically**, considered **across the whole lifecycle**.
- **Chapter 21 is harm done to the system; this is harm done by it.** Attack is **secure AI**; unfair treatment is **responsible AI**.
- **Four obligations**: **transparency, privacy, fairness, and accountability with explainability**.
- **Transparency** is being **open about evaluation and data use**; **explainability** is **accounting for one decision**. Trust-building openness is **transparency**; an unexplained rejection is **explainability**.
- **Explainability and accountability travel together.** Nobody can **answer for** a decision nobody can **explain**.
- **Anonymisation removes or obscures the personal detail**; **pseudonymisation substitutes identifiers** and keeps the link separately.
- **Personal data in a training set needs anonymisation, not access control.** Once a model has **learned** from it, guarding the original dataset is **beside the point**.
- **A consistent demographic skew from neutral prompts means bias in the training data**, not a prompting or parameter fault.
- **Incomplete or messy data makes a model wrong; unrepresentative data makes it unfair.** Only the second is a **fairness** problem.
- **Accuracy and explainability are independent.** A model can be **right and inscrutable**, and on this objective that is still a failure.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Responsible AI. https://docs.cloud.google.com/gemini/docs/discover/responsible-ai
