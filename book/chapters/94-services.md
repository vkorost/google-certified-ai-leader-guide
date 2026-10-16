# The Services, by Name

The chapters teach each service where its decision lives, which is the right place to meet one and the wrong place to memorise a set. This appendix is the set. **Each entry gives what the thing is, the condition that makes it the answer, and the product it is most often confused with.** The middle one is what the exam tests.

The names here are the current ones. Google renamed most of this surface in April 2026 and the retired names are not listed, because neither of the documents Google publishes for this exam uses one. Where Google’s own two documents give different current names to the same thing, both are given, because that disagreement is live.

## Apps: a person opens them

No deployment, no training, no engineers. A scenario in this family says *quickly*, *no budget*, or *a team wants to*.

**Gemini app.** Google's gen AI chatbot: writing, summarising, translating, creating images. **Cue:** one person doing general work, with no company data involved. **Not:** Gemini Enterprise, which searches company data with permissions applied.

**Gemini Advanced.** The paid tier of the Gemini app, with extra features and enterprise-grade protections. **Cue:** the stem asks for the premium tier specifically. **Not:** Gemini Enterprise. Advanced is a chat tier; Enterprise is a platform.

**Gems.** Personalised assistants inside the Gemini app, built from your own instructions. **Cue:** a repeated task needs a saved persona, built without code. **Not:** an agent. A Gem is a stored prompt: it cannot ingest a document set or cite it.

**Gemini for Google Workspace.** *Also written Google Workspace with Gemini.* Gemini inside Gmail, Docs, Sheets, Slides and Meet. **Cue:** employees want help inside the apps they already use. **Not:** Gemini for Google Cloud, which helps engineers with code, operations and security.

**Gemini for Google Cloud.** The assistant for people doing Google Cloud work: code, cloud management, data and security posture. **Cue:** the person being helped is an engineer or operator, not a customer and not an office worker. **Not:** Gemini for Google Workspace, which helps inside Gmail and Docs instead.

**Gemini Notebook.** A research assistant that answers only from files you upload, citing them. **Cue:** a specific, limited set of documents must be summarised, questioned and cited. **Not:** the Gemini app, which answers from the model’s own knowledge of the world.

**Google Vids.** The Workspace app for making work videos, with AI storyboards, avatars and voiceover. **Cue:** a branded video made by non-specialists with no production budget. **Not:** Veo, which is the model that generates video. Vids is the app a person opens.

## Suites: a department buys them

A capability sold whole, assembled from several products underneath.

**Gemini Enterprise.** Intranet search, an AI assistant and an agent platform over company data, with permissions respected. **Cue:** employees searching and acting across many internal systems at once. **Not:** Gemini Notebook, which is confined to the sources you upload.

**Customer Engagement Suite.** *Also written Gemini Enterprise for Customer Experience.* Google's set of customer-service products: virtual agents, live help, analytics and the contact centre platform. **Cue:** anything covering customer service end to end. **Not:** Gemini Enterprise, which serves employees rather than customers.

## The search and grounding offerings

Five offerings that all find things, separated by **whose data is being searched**. That one question settles every question about them.

**Agent Search.** Google-quality search and recommendation built over your own content, and the prebuilt way to do retrieval without assembling one. **Cue:** a company wants search or grounded answers over **its own** documents, site or knowledge base. **Not:** Grounding with Google Search, which reaches the public web instead. Agent Search grounds in your world; that one grounds in the world.

**Grounding with Google Search.** Grounds a model's answers in current results from Google's public web index. **Cue:** the stem says *current*, *real time*, *breaking*, or *as it emerges*. **Not:** Agent Search, which searches content you control rather than the web.

**Google Search.** The public web index itself, which the blueprint sets against Agent Search as the other external search offering. **Cue:** the contrast being drawn is your content against the whole world. **Not:** Agent Search. The exam guide names both together precisely so the two can be told apart.

**RAG APIs.** Retrieval components you compose into an application you are already building. **Cue:** the stem wants retrieval assembled by its own developers rather than delivered ready-made. **Not:** prebuilt RAG with Agent Search, which is the same job with nothing to assemble.

**multimodal search.** One search interface across several data types and source systems at once. **Cue:** documents, images and video must be searched together, in one place. **Not:** Grounding with Google Search, which reaches the public web instead.

**AI Commerce Search.** Personalised search and recommendations for a retail catalogue, across websites and mobile apps. **Cue:** shoppers must find products **and** get personalised recommendations: two requirements, and only this offering meets both. **Not:** Agent Search, which searches your content generally rather than a shop.

## The Customer Engagement Suite, part by part

Four products, separated by **when in the conversation each one acts**. That axis settles every question about them.

**Conversational Agents.** Builds the virtual agents, chat and voice, that talk to customers directly. **Cue:** automated self-service, **before** a human is involved. **Not:** Agent Assist, which helps a human rather than replacing one.

**Agent Assist.** Suggests responses and information to the human agent during a live conversation. **Cue:** **During** the call, and the stem says the humans are staying. **Not:** Conversational Agents. Agent Assist never speaks to the customer.

**Conversational Insights.** *Also written Customer Experience Insights.* Analyses completed conversations for sentiment, topics and trends. **Cue:** **After** the calls, and the stem says nobody wants to listen to recordings. **Not:** Agent Assist, which works live. Insights works on what already happened.

**Contact Center as a Service.** *Also written CCaaS or Contact Center AI Platform.* The contact centre platform itself: it queues and routes every customer contact, by phone or online, and passes it to a person when needed. **Cue:** multiple channels, consistent support and agent empowerment, together. **Not:** any single component. Only the platform carries all three requirements.

## Agent Platform and its components

Where models and agents are built, trained, deployed and governed.

**Agent Platform.** *Also written Gemini Enterprise Agent Platform.* The unified platform for building, training, deploying and governing models and agents. **Cue:** the stem asks which **platform**, and wants one managed place for all of it. **Not:** Gemini for Google Cloud, which assists people doing cloud work rather than hosting what they build.

**Model Garden.** A library of models from Google, its partners and open source, to discover, test, customise and deploy. **Cue:** picking an **existing** model rather than training one. **Not:** Model Registry, which holds your own models and their versions.

**Model Builder.** Training and using your own models, either fully custom or through AutoML. **Cue:** the model has to be trained on the company’s own data. **Not:** Model Garden, which is for choosing a model somebody else trained.

**AutoML.** Trains a model on your data with minimal ML expertise and no training code. **Cue:** your own labelled data, a team with no ML skills, a custom model needed. **Not:** a pre-trained model, which nobody trains on your data.

**Agent Studio.** The console workspace for discovering models, refining prompts and designing agents. **Cue:** building and deploying a **production** application at scale. **Not:** Google AI Studio, which is free and for quick prototyping.

**Google AI Studio.** Free, low-setup prototyping with the Gemini API. **Cue:** experimenting quickly, with no complex setup. **Not:** Agent Studio, which sits inside Google Cloud and targets production.

**Apps Script.** Low-code building inside Google Workspace. **Cue:** a small automation wanted inside Workspace, by someone who is not a developer. **Not:** AppSheet, which needs no code at all.

**AppSheet.** No-code application building, with no programming of any kind. **Cue:** a business function with no engineers needs an application. **Not:** apps Script, which still involves writing some code.

**MLOps.** The tooling and practice that lets teams collaborate to monitor and improve models already in production. **Cue:** the stem is about running and improving models over time, not building one. **Not:** a single product. MLOps is a practice that several tools support.

**Model Registry.** The central repository for your own models, their versions and their metadata, and for deploying a chosen version. **Cue:** the words are *versions*, *metadata*, *track changes*, *organised*. **Not:** Model Garden. **The study guide says Model Garden stores models; the product documentation does not agree, and the registry is the repository for models you own.**

**Feature Store.** Stores and serves the data features a model consumes, so training and serving get the same values. **Cue:** the words are *feature*, *consistency between models*, *training-serving skew*. **Not:** Model Monitoring. Tracking the features is Feature Store; tracking the model’s behaviour is Monitoring.

**Model Monitoring.** Watches a deployed model’s data for drift against a baseline and alerts past a threshold. **Cue:** the words are *accuracy over time*, *drift*, *alert*. **Not:** Pipelines. Monitoring detects; Pipelines is where the retraining runs.

**Pipelines.** Automates and governs ML workflow steps as repeatable runs. **Cue:** the words are *automate*, *repeatable*, *retrain on a schedule*. **Not:** Model Monitoring, which observes rather than runs.

## The pre-built APIs: one capability each

No model to train. The exam guide lists these as agent tooling, which is the clue to what they are for: something an agent can reach for.

**Document AI API.** Turns unstructured documents into structured data: classify, extract, enrich, read scanned text. **Cue:** scanned documents, PDFs, varying layouts, forms, invoices. **Not:** Cloud Vision API. A loan application is a document, not an image.

**Cloud Vision API.** Image labelling, face and landmark detection, reading text in images, flagging explicit content. **Cue:** a still image to be described, tagged or moderated. **Not:** document AI, which processes documents rather than pictures.

**Cloud Video Intelligence API.** Annotates video for entities, scene changes and adult content. **Cue:** video analysis with a pre-built API. **Not:** Cloud Vision API, which handles still images.

**Speech-to-Text API.** Audio in, text out. **Cue:** transcripts, captions, or voice as an input. **Not:** Text-to-Speech, which runs the other way.

**Text-to-Speech API.** Text in, spoken audio out. **Cue:** a voice for an agent, or narration. **Not:** Speech-to-Text, which runs the other way.

**Translation API.** Translates text between thousands of language pairs. **Cue:** text has to be translated from code, with no file layout to preserve. **Not:** document Translation, which preserves a formatted file’s layout.

**Document Translation API.** Translates whole formatted documents while keeping their layout. **Cue:** a PDF or DOCX that must still look like itself afterwards. **Not:** the plain Translation API, which handles text rather than files.

**Natural Language API.** Sentiment, entities, classification and syntax over text. **Cue:** analysing text rather than generating it. **Not:** a generative model. This one reads; it does not write.

**Google Cloud API Library.** The catalogue where you find and switch on Google Cloud APIs. **Cue:** finding and enabling an API before calling it. **Not:** Model Garden, which lists models rather than APIs.

## Infrastructure: where things actually run

A **container** is an application packaged with everything it needs. **Serverless** means you never see or pay for an idle server. **Scale to zero** means no copies run, and nothing is charged, when nobody is using it.

**Cloud Run.** Runs a container as a scalable service with a web address, serverless, scaling to zero. **Cue:** **A container image already exists** and must be exposed as an endpoint. **Not:** Cloud Functions. Both are serverless and both scale to zero, so neither property decides anything. The container does.

**Cloud Functions.** *Also written Cloud Run functions.* Runs a small single-purpose piece of code when a request or an event arrives. **Cue:** lightweight event-driven backend logic, such as calling somebody else’s API. **Not:** Cloud Run, which runs a container you already built.

**Cloud Storage.** Keeps files of any kind as objects, in buckets. **Cue:** unstructured files: images, video, logs, training data, backups. **Not:** Cloud SQL, which holds rows in tables rather than files.

**Cloud SQL.** A managed relational database: MySQL, PostgreSQL or SQL Server. **Cue:** ordinary application data in rows and tables. **Not:** BigQuery, which analyses large datasets rather than serving an application.

**BigQuery.** A serverless data warehouse for analysing very large datasets with SQL. **Cue:** analysis at scale, and business intelligence. **Not:** Cloud SQL, which is an application database.

**BigQuery ML.** Builds and runs machine learning models using only SQL, inside BigQuery. **Cue:** analysts who know SQL, data already in the warehouse, and no appetite for moving it or learning a new language. **Not:** Agent Platform, which is a separate place the data would have to travel to.

**Pub/Sub.** Messaging: one application publishes, others receive, neither needing to know about the other. **Cue:** streaming data arriving continuously. **Not:** Cloud Storage, which keeps data rather than carrying it.

**LiteRT.** The Lite Runtime: tooling for deploying models onto edge devices. **Cue:** the stem says on-device, at the edge, or names poor connectivity. **Not:** Gemini Nano, which is a model that runs on a device rather than the tooling that puts one there.

**AI Hypercomputer.** *Also written hypercomputer.* The whole AI-optimised system: hardware, open software, ML frameworks and flexible ways to buy capacity. **Cue:** *System-level*, *tightly coupled*, *beyond individual accelerators*, *extreme scale*. **Not:** a TPU or a GPU, which are components inside it rather than the system.

**TPU.** Google's own custom-designed chips for machine learning. **Cue:** the stem stresses Google's custom silicon. **Not:** a GPU, which in Google Cloud is NVIDIA hardware.

**GPU.** NVIDIA accelerator chips, rented in Google Cloud. **Cue:** flexible acceleration, inference and prototyping at moderate scale. **Not:** a TPU, which is Google-designed.

## Security

Three tools with three different jobs, and the exam tests the difference.

**Security Command Center.** Finds and reports weaknesses and threats across the whole cloud estate. **Cue:** *Centralised view*, *security posture*, *identify vulnerabilities across teams*. **Not:** IAM. Listing an over-permissive role is reporting; IAM is where it gets fixed.

**Identity and Access Management.** *Also written IAM.* Controls who may do what on which resource. **Cue:** granting or restricting access. **Not:** Security Command Center, which reports rather than grants.

**Secure AI Framework.** *Also written SAIF.* Google's framework for managing the risks of AI and ML models. **Cue:** the stem asks for the framework rather than a tool. **Not:** a product. SAIF is guidance, not something you switch on.

## Google's foundation models

Google names four. Everything else on an option list is either a specialised sibling or not a foundation model at all.

**Gemini.** Multimodal understanding, conversation, content creation, question answering, and a large context window. **Cue:** text, long documents, or more than one modality at once. **Not:** Imagen, which makes still images and nothing else.

**Gemma.** The lightweight, open, customisable model, for local deployment and specialised applications. **Cue:** *Lightweight*, *local*, *open*, *on-device*, and the task is writing or summarising text. **Not:** Gemini. Gemma is small, so heavy analysis is not its job.

**Imagen.** A text-to-image model: high-quality images generated from a description. **Cue:** still images, and nothing in the stem asks for text or video as well. **Not:** Veo, which makes video. Imagen cannot produce a video by generating frames.

**Veo.** Generates video from a text description or a still image. **Cue:** video has to be generated rather than assembled from existing material. **Not:** Google Vids, which is the app a person opens rather than the model.

**Gemini Nano.** Google's most compact model, designed to run on devices. **Cue:** the stem says on-device. **Not:** Gemma. If a stem says on-device, check whether Nano is on the list first.

## The 5 that Google’s exam documents never name

Everything above is named by the exam guide, the study guide, or both. These 5 are not, and they are here anyway, with the reason stated rather than buried.

**AI Commerce Search.** Named in neither document. Google documents it, and a retail scenario asking for discovery and recommendations together has no other answer.

**BigQuery ML.** Named in neither document, although the study guide names BigQuery itself. This is the feature of it that trains models, and the skills-and-location scenario has no other answer.

**Cloud SQL.** Named in neither document, though the exam guide’s list of agent tooling says *databases*, and this is the managed relational one.

**Google Vids.** Named in neither document. It is Google’s own Workspace video app, and a no-budget video scenario has no other answer.

**Pub/Sub.** Named in neither document. It is how streaming data is gathered on Google Cloud, and the gathering stage of the lifecycle is on the blueprint.

## Where these names come from

| Named by | Services |
|:---|---:|
| Both official documents | 33 |
| The exam guide only | 10 |
| The study guide only | 12 |
| Neither, and said so above | 5 |

**A name carried by only one of the two documents is still examinable**, because the exam is written against both. The column above exists so a reader can see which claims rest on which document, and the reader who checks is the reader this book is for.
