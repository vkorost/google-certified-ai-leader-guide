# Chapter 18: A Deployed Model Is a Running System

**Summary:** *Deployment is where most organisations think the work ends, and the exam treats it as where a different kind of work starts. Google names a set of practices for keeping a model honest once it is live, and a specific Google product sits behind each one. The questions are product-matching questions, and they are decided by one word in the scenario: whether the thing being managed is the model, its versions, its data, or its accuracy over time.*

## The Model That Got Worse Without Changing

A churn model goes live in March at 88% accuracy, and nobody touches it after that. By November it is running at 71%.

The model is identical, and every weight is exactly where it was in March. What moved is the world it was trained on: new products, a different customer mix, a competitor who changed their pricing without telling anybody. The model is answering a question about a market that no longer exists, and it is answering with the same confidence it had in March.

That is drift, and the reason it belongs in a chapter for you rather than in an operations runbook is that **nothing surfaces it**. There is no error, no alert, no failure. **The model is a running system**, and a running system that nobody watches is a system you will hear about from a customer.

## Six Practices, and the Google Product for Each

Google's recommended practices for continuous monitoring and evaluation name automatic model upgrades, key performance indicators, security patches and updates, versioning, performance tracking, drift monitoring, and feature management.<sup>[1]</sup>

Each has a product behind it, and the exam asks for the product.<sup>[2]</sup>

| The job | The product | What makes it the answer |
|---|---|---|
| Keeping track of versions of a model | **Model Registry** | Versions, their metadata, and getting them deployed, in one place<sup>[3]</sup> |
| Watching accuracy change over time | **Model Monitoring** | Drift is what it exists to detect<sup>[4]</sup> |
| Managing the feature data a model consumes | **Feature Store** | One definition of a feature, served to every model that needs it<sup>[5]</sup> |
| Automating the machine learning steps | **Pipelines** | Repeatable, scheduled, hands-off execution<sup>[2]</sup> |
| Reviewing how the model is performing | **Performance tracking**, on the model's metrics | The measurement, rather than a product |
| Finding and organising available models | **Model Garden** | A catalogue of models to pick from, per chapter 11 |

Two of those collide in a way worth fixing now.

**Model Registry against Model Garden.** The Registry holds *your* models and their versions. The Garden is a catalogue of models *available to you* from Google, partners and open source. A scenario about a central, organised place to keep model versions with their metadata, ready to deploy, is the Registry. A scenario about choosing a model to start from is the Garden. The study guide's language about storing models in Model Garden is loose enough to mislead, so hold the distinction by what the scenario is doing: picking, or keeping track.

**Feature Store against Model Monitoring.** Both involve watching something. Feature Store manages and serves **feature data**, so it is the answer when the scenario is about the data going in, especially when several models need the same feature defined the same way. Model Monitoring watches **the model's accuracy**, so it is the answer when the scenario is about performance decaying.

## Versioning Is the One With the Business Consequence

Worth a paragraph on its own, because the exam asks about it and the reason matters.

A model in production has a version, and so does the one before it, and so does the one somebody is about to replace it with. Without a registry, three things become impossible: knowing what is actually running, going back to what ran last month, and explaining to anyone why a decision made in June came out the way it did.

That third one is not an operations concern at all. It is the accountability requirement from chapter 22 arriving dressed as a technical one, and the humans who ask you about it will be auditors rather than engineers. If you cannot say which version produced a given decision, you cannot explain the decision, and explainability sits on the blueprint.

## Upgrades, Patches and KPIs

Three items on Google's list have no single product attached to them, and are worth knowing as practices rather than as answers to a matching question.<sup>[1]</sup>

**Automatic model upgrades.** Managed models get better underneath you, which is a benefit and a risk at once: the thing you tested is not necessarily the thing running next quarter. No question in circulation tests this, and it is on the blueprint.

**Security patches and updates.** The ordinary software obligation, which does not stop applying because the software contains a model. Also untested, also on the blueprint.

**Key performance indicators.** The one that gets tested, and it gets tested from the business side. When a scenario asks how to tell whether a deployed gen AI tool is actually working, the answer is the operational measures that already mean something in that function: for a contact centre, how long a case takes and whether it is resolved first time. Not model accuracy, not user enthusiasm. **A KPI that only the model team understands is not a measure of business impact.**

## How Wrong Answers Are Built on This Material

Every distractor is a real Google product from the same platform, which makes this a vocabulary-precision objective. There is nothing to eliminate by plausibility.

- **The catalogue-for-registry answer.** Model Garden where version tracking was wanted. The most reliable trap on the objective.
- **The monitoring-for-features answer.** Model Monitoring where the scenario was about managing feature data, or Feature Store where it was about accuracy decaying. Ask whether the scenario is about **the input** or **the outcome**.
- **The retrain-it answer.** Retraining offered where the scenario asked which tool to use for watching. Retraining is a response to drift, not a way of detecting it.
- **The model-metric answer.** On impact questions, accuracy or another internal measure offered where the scenario asked about business impact.
- **The build-it answer.** A custom monitoring or tracking solution where a platform product exists.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Needs versions, metadata, and deployment in one place | Model Registry | Model Garden |
| Wants to choose a model to start from | Model Garden | Model Registry |
| Describes accuracy falling over months | Model Monitoring, detecting drift | Retraining, which is the response |
| Manages feature data used by a model | Feature Store | Model Monitoring |
| Needs one feature definition shared across models | Feature Store | A database, or a data warehouse |
| Automates repeated machine learning steps | Pipelines | A scheduler, or a custom script |
| Asks whether a live tool is delivering value | Operational KPIs for that function | Model accuracy, or usage counts |

The habit is to name the object before naming the product: versions, accuracy, features, steps, value. Each of those words has exactly one answer behind it, and the scenario almost always says one of them outright.

## What to Remember

- **A deployed model is a running system**, and **drift produces no error**. Accuracy can fall for months with **nothing to alert on**.
- **Model Registry holds your models and their versions**, with metadata, ready to deploy. **Model Garden** is a **catalogue to pick from**. The split is **keeping track against choosing**.
- **Model Monitoring watches accuracy over time**, which is **how drift is detected**. **Retraining** is the **response**, not the **detection**.
- **Feature Store manages and serves feature data**, and is the answer when **several models need one feature defined the same way**.
- **Pipelines automate the machine learning steps**, repeatably and on a schedule.
- **Versioning carries the accountability consequence**: without it you cannot say **what is running**, **what ran last month**, or **why a past decision came out as it did**.
- **Automatic model upgrades** mean the thing you tested **may not be the thing running next quarter**. Untested, and on the blueprint.
- **Security patches still apply** to software that happens to contain a model.
- **Business impact is measured in that function's own operational KPIs**, such as **handling time and first-contact resolution**, not in **model accuracy or usage counts**.
- **Name the object before the product**: **versions, accuracy, features, steps, value**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Machine learning on Gemini Enterprise Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning
4. Model Monitoring overview. https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning/model-monitoring/overview
5. Feature Store overview. https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning/featurestore/latest/overview
