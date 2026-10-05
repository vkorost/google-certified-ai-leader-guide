# Chapter 3: Three Ways a Model Learns, and the ML Lifecycle

**Summary:** *Two kinds of question come off this material, and both are nearly mechanical once you know what to look for. The first gives you a business situation and asks which learning approach fits, and the answer is decided by one property of the data. The second gives you an activity and asks which stage of the lifecycle it belongs to, and the answer is decided by one verb in the scenario. Neither rewards depth. Both reward knowing exactly where the boundary falls.*

## Two Datasets, and the Only Difference That Matters

Picture two spreadsheets.

The first holds five years of support tickets. Every row has the problem description, the product, the customer tier, and a final column: how long the ticket actually took to resolve.

The second holds two years of purchase records, with what was bought, when, and for how much. There is no final column, because nobody ever wrote down which kind of customer each row represents and nobody is sure what the kinds are.

Those two spreadsheets need different approaches, and the difference between them is not their size, their subject or their quality. It is that one of them already contains the answer.

## The Label Question Decides It

Before you look at any option, ask **the label question**: does this data already contain the thing you want the model to produce?

That one question has three possible answers, and each one points at a different approach.

**Yes, the answer is in the data.** The resolution-time column is a label, and training on labelled examples to predict a known target is supervised learning.<sup>[2]</sup> It covers both the case where the target is a category and the case where it is a number.

**No, and finding the structure is the point.** The purchase records have no target column, and the task is to discover groupings and patterns nobody specified in advance. That is unsupervised learning.<sup>[2]</sup> Customer segmentation is its standard example, and Google documents clustering for exactly that purpose.<sup>[3]</sup>

**No, and there is no fixed dataset either.** Instead there is an environment, actions you can take in it, and a score that goes up or down depending on what happens. The model learns by trying things and keeping what scores well. That is reinforcement learning, which learns through interaction and feedback, chasing rewards and avoiding penalties.<sup>[2]</sup>

| Approach | What the data has | What it produces | The phrase that gives it away |
|---|---|---|---|
| Supervised | A column holding the known answer | A prediction of that answer for new rows | labelled, historical outcomes, known target, past records of X |
| Unsupervised | No target column at all | Groups, patterns, anomalies | natural groupings, segments, unknown categories, outliers |
| Reinforcement | An environment and a score | A policy for what to do next | reward, penalty, trial and error, learns by interacting |

That right-hand column is worth more than the rest of the table. These questions are written as business scenarios, and the vocabulary in the scenario is the signal.

## Why a Leader Cares Which One It Is

The approach is not a technical detail you can delegate and forget, and the reason is that each one commits you to a different kind of spending before any model exists.

Supervised learning needs labels, and labels are usually made by humans. Somebody has to decide what each example is, example by example, and that work is slow, expensive, and the thing most likely to be quietly skipped under deadline pressure. When a team tells you they have plenty of data for a supervised problem, the question that matters is not how much data. It is who labelled it, how consistently, and whether the labels mean what the model will be asked to predict. A supervised project with cheerful data volumes and nobody assigned to labelling is a project with a hole in it that will not show up until training.

Unsupervised work escapes that cost and buys a different problem. There is nothing to be wrong against, so nobody can tell you the model is accurate. It groups what it is given, the groups come out, and whether they are useful is a judgement a human makes afterwards by looking at them. That sounds like the cheaper option. *It is the harder one to govern.*

Reinforcement learning needs something rarer than either: an environment safe enough to let a learning system act in, and a score that genuinely represents what you want. Both are hard to arrange in a business, which is why it appears far less often in practice than its reputation suggests.

## The Confusion the Exam Keeps Returning To

One pair gets tested repeatedly, and it is supervised prediction against unsupervised grouping. They sound similar in business language and they are opposites in method.

| The scenario says | Approach | Why |
|---|---|---|
| Predict whether a subscription will renew, from past renewal records | Supervised | Past renewals are recorded outcomes. The label exists |
| Group customers by behaviour to find segments nobody defined | Unsupervised | There is nothing to predict, only structure to find |
| Recognise products in photographs, using categorised example images | Supervised | Categorised examples are labels |
| Find the recurring themes in a pile of reviews, with no theme list | Unsupervised | The themes are the output, so they cannot be the input |
| Forecast next quarter's sales from historical figures | Supervised | A historical figure is a recorded answer |
| Spot transactions unlike anything in the normal pattern | Unsupervised | Nobody labelled them as fraud; the model finds the odd ones |

Two tests cut through nearly all of it, and the first is the one to reach for.

**If the output category already exists somewhere in the data, the approach is supervised. If producing those categories is the job, it is unsupervised.**

The second test is blunter and almost as reliable: forecasting and predicting are supervised words, while discovering and grouping are unsupervised ones. The exam is consistent enough about that vocabulary to make it worth trusting.

## The Lifecycle Is Five Stages, and Scenarios Name Them by Their Verbs

Google calls the path a model takes the **machine learning lifecycle**, and sets it out as a sequence: data is ingested and prepared, the model is trained, it is deployed, and then it is managed over time.<sup>[1]</sup><sup>[2]</sup> The blueprint asks you to identify its stages by name, so learn them as a list and not as a vague progression.

| Stage | What happens | The verbs that mark it |
|---|---|---|
| Data ingestion | Raw data is collected and brought in from its sources | collecting, gathering, bringing in, capturing, streaming in |
| Data preparation | It is cleaned, corrected, reshaped into a usable form | cleaning, filling gaps, deduplicating, reformatting, transforming |
| Model training | The model is built from the prepared data | training, fitting, learning from, building the model |
| Model deployment | The trained model is made available to be used | releasing, serving, putting into production, exposing an endpoint |
| Model management | It is maintained, watched and kept current | monitoring, versioning, retraining, tracking performance |

Ingestion against preparation is the boundary the exam tests, because in ordinary speech both are "getting the data ready". The split is clean once you see it: **ingestion moves data, preparation changes it.** A scenario describing files pulled from several systems into one place is ingestion, even if it mentions that cleaning will follow. A scenario describing missing values being filled and formats being made consistent is preparation, even if it mentions where the data came from.

Management gets its own chapter later, because a deployed model is a running system and the exam treats it as one.

## Which Google Tool Belongs to Which Stage

The blueprint asks for the Google Cloud tools at each stage, not just the stages.<sup>[1]</sup> For ingestion, the choice follows the shape of the data rather than the industry or the volume:

| The data arriving is | Google Cloud service |
|---|---|
| A continuous stream of events or messages | Pub/Sub<sup>[4]</sup> |
| Files and objects with no fixed structure: documents, images, audio | Cloud Storage<sup>[5]</sup> |
| Rows in tables, from a relational database | Cloud SQL<sup>[6]</sup> |
| Large volumes to be queried and analysed where they sit | BigQuery<sup>[3]</sup> |

Training and deployment both live on Agent Platform, formerly Vertex AI, which is where models are built, tuned, deployed and managed. Chapter 11 takes that platform apart service by service.

There is a trap sitting in this table, and it caught enough candidates to be worth naming. **The analysis-tool answer** offers a strong product for the wrong stage. BigQuery is a genuinely excellent place to analyse data at scale, and an option that praises it for that is saying something true. If the scenario is about *gathering* streaming events, true is not the same as correct. Match the stage first, the product second.

## How Wrong Answers Are Built on This Material

The distractors here are rarely nonsense, and are usually the correct response to the question sitting next door to the one asked, which is why slowing down helps and confidence does not.

- **The sophistication answer.** Reinforcement learning, or something that sounds more advanced, offered for a problem that labelled data already solves. It is seductive because it sounds like a better answer to a harder question. It becomes correct only when the scenario describes an agent acting in an environment and a score it is trying to improve.
- **The label-blind answer.** It reads "we have years of data" as "we have labelled data". Volume is not labelling. The question to ask is whether the specific thing being predicted is recorded in the rows, and a scenario that carefully avoids saying so is avoiding it deliberately.
- **The adjacent-stage answer.** It names the lifecycle stage either side of the one the scenario describes, usually by latching onto a mention of what comes next. A scenario often tells you that cleaning will happen afterwards, precisely so that an inattentive reader will answer "preparation".
- **The analysis-tool answer.** A capable Google product named for the wrong stage of the lifecycle.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Names recorded past outcomes | Supervised learning | Unsupervised, because the data sounds unstructured |
| Asks for groups nobody has defined | Unsupervised learning | Supervised, because "identify" sounds like prediction |
| Describes rewards, penalties or trial and error | Reinforcement learning | Supervised, because feedback sounds like labels |
| Describes collecting from several sources | Data ingestion | Preparation, mentioned later in the same sentence |
| Describes fixing, filling or reformatting | Data preparation | Ingestion, because the sources get named |
| Asks which service gathers streaming data | Pub/Sub | An analysis product praised for analysis |

One habit transfers past all of it. For learning-approach questions, find the label or establish that there is not one, before reading the options at all. For lifecycle questions, find the verb.

## What to Remember

- **The label question**: does the data already contain what you want the model to produce? **Yes means supervised, no means unsupervised**, and **no data plus a score to improve means reinforcement**.
- **Supervised learning trains on labelled examples** to predict a **known target**, whether that target is a **category or a number**.
- **Unsupervised learning has no target column.** It produces **groupings, patterns and anomalies**, and **customer segmentation is its standard example**.
- **Reinforcement learning learns by interacting**, keeping what earns **reward** and avoiding **penalty**. Scenario words: **trial and error, reward, penalty**.
- **Volume is not labelling.** "Years of data" tells you nothing about whether the answer is in it.
- **Five lifecycle stages**: **data ingestion, data preparation, model training, model deployment, model management**.
- **Ingestion moves data; preparation changes it.** A scenario mentioning cleaning *to come* is still describing **ingestion**.
- **Ingestion service follows data shape**: **Pub/Sub for streams**, **Cloud Storage for files and objects**, **Cloud SQL for relational rows**, **BigQuery to query at scale**.
- **A true statement about a product is not a correct answer.** Match the **stage** first, then the product.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Introduction to BigQuery ML. https://docs.cloud.google.com/bigquery/docs/bqml-introduction
4. Pub/Sub documentation. https://docs.cloud.google.com/pubsub/docs
5. Cloud Storage documentation. https://docs.cloud.google.com/storage
6. Cloud SQL documentation. https://docs.cloud.google.com/sql
