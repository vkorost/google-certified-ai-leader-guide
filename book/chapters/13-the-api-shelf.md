# Chapter 13: The API Shelf, and Which Studio You Are Standing In

**Summary:** *Google keeps a shelf of pre-built AI APIs that solve specific, narrow problems, and the exam expects you to reach for them before reaching for a foundation model. Most of this objective is a matching exercise, and it is worth treating as one: eight APIs, a handful of places to run code, two studios with confusingly similar names, and one pair that is distinguished by a single word. Learn the shelf and this is among the cheapest sections of the exam.*

## The Same Capability, Two Prices

A team needs to pull the invoice number, date and total out of ten thousand scanned PDFs.

They could prompt a frontier multimodal model to read each one. It would work. Or they could call an API that exists specifically to extract structured fields from documents, which also works, costs less, and needed no prompt engineering.

**The shelf before the model** is the habit: for a problem that has been solved as a product, the product is the answer. The exam tests this repeatedly, because reaching for the most capable model is the modern reflex and it is frequently the wrong call.

## Eight Pre-Built APIs, by the Job They Do

| API | What it does |
|---|---|
| Speech-to-Text | Turns speech into text, and transcribes audio and video content<sup>[2]</sup> |
| Text-to-Speech | Turns text into natural-sounding speech; voice interfaces and personalised audio<sup>[2]</sup> |
| Translation API | Language conversion across text, whole documents, web pages, and audio or video files<sup>[2]</sup> |
| Document Translation API | Translation that **leaves the formatting intact**<sup>[2]</sup> |
| Document AI | Extracts data from varied document formats and automates capture<sup>[2]</sup><sup>[3]</sup> |
| Cloud Vision API | Analyses images: objects, text, faces and landmarks<sup>[2]</sup> |
| Cloud Video Intelligence API | Analyses video and extracts meaning, for search and recommendation<sup>[2]</sup> |
| Natural Language API | Derives insight from unstructured text: sentiment, classification, entity extraction<sup>[2]</sup> |

The blueprint also names the **Google Cloud API Library** as the place these are found, which no question tests and which is worth recognising as the catalogue rather than a product.<sup>[1]</sup>

## The Two Translation APIs Differ by One Word

This pair gets tested, and the distinction is narrow enough to lose by skimming.

Translation API converts the language of content, documents included. Document Translation API does the same job to a **formatted** document and brings the formatting through unchanged.<sup>[2]</sup>

So the deciding word in any scenario is about the **shape** of the output, not the content. A business that needs its contracts, tables and headings to come out looking like contracts, tables and headings is describing document translation. A business that needs the words in another language is describing translation. **The text-translation answer** is the trap: correct about the language, silent about the layout the scenario asked for.

## Combination Questions Want the Pipeline, Not the Best Single API

A particular shape recurs: a scenario describes a capability made of several steps and asks which combination of APIs delivers it.

The method is to decompose the scenario into transformations and name the API for each.

| The scenario step | The API |
|---|---|
| A person speaks to it | Speech-to-Text |
| Work out how they feel, or what they mentioned | Natural Language API |
| It speaks back | Text-to-Speech |

Three steps, three APIs, and the right answer is the set rather than the strongest member. **The single-API answer** is the trap here, and it usually names the most impressive one on the list.

## Where the Code Actually Runs

An agent's tools have to execute somewhere, and the exam names a small set of places.

| Service | What it is for | The cue |
|---|---|---|
| Cloud Run | Runs containers, serverless, scaling to zero when idle<sup>[4]</sup> | A ready-made container image; bursty or unpredictable traffic |
| Cloud Functions | Runs a small piece of code on an event<sup>[1]</sup> | Lightweight, event-driven, triggered by something happening |
| Cloud Storage | Holds files and objects<sup>[1]</sup> | Documents, images, audio, anything unstructured |
| BigQuery | Analysis at scale. **BigQuery ML trains a model from SQL**<sup>[5]</sup> | Analysts who know SQL, data already in the warehouse |

BigQuery ML deserves the bold, because it answers a scenario candidates reliably get wrong: a team of analysts fluent in SQL, data already sitting in the warehouse, and a model to build. They do not need a data science platform or a new skill. They can build the model where the data already is, in the language they already use. *The skills gap was imaginary.* The humans in that room were qualified the whole time, and an answer that sends them on a course is answering a different question.

For the no-code end of the spectrum the blueprint names **Apps Script** and **AppSheet**, which let people build with Gemini without writing an application.<sup>[2]</sup> No question in circulation tests either, and both are the kind of thing a leader is asked about by a function that has no engineers.

## Which Studio You Are Standing In

Two products are both called a studio and the difference between them is the entire question.

Both of them are places to work with the **Gemini API**, which is how Gemini is reached programmatically, and that shared foundation is why the two get confused.<sup>[2]</sup> **Google AI Studio** costs nothing and exists for rapid prototyping. **Agent Studio** is where you build the thing that has to go live and carry real load.<sup>[2]</sup>

| The scenario says | The studio |
|---|---|
| Try an idea, explore what is possible, no setup | Google AI Studio |
| Build it properly, deploy it, run it at scale | Agent Studio |

That is the whole distinction: **exploration against production**. A scenario emphasising speed of first experiment, a small team wanting to see whether something is feasible, or deliberately minimal setup is pointing at Google AI Studio, and an option naming the production tool there is right about the product and wrong about the stage.

## Running AI Where the Work Is

Three terms cover the edge, and none of them is tested by any question in circulation, which makes them precisely the blueprint surface worth ten seconds each.

**AI on the edge** means running the solution on infrastructure close to where things are happening, on a device or a local server rather than in a distant data centre.<sup>[2]</sup> The reasons are the ones chapter 19 lists as needs: latency, and connectivity you cannot rely on.

**LiteRT**, the Lite Runtime, is Google's tooling for deploying models onto edge devices.<sup>[2]</sup> **Gemini Nano** is Google's most compact and efficient model, built specifically to run on devices.<sup>[2]</sup>

So a factory with poor connectivity, a device that must respond instantly, or a situation where data should not leave the premises is an edge scenario, and the three names above are the answer set.

## How Wrong Answers Are Built on This Material

This objective is a matching exercise, so its distractors are other real products from the same shelf. There is nothing implausible to eliminate, which means the only defence is naming the transformation the scenario needs before looking at the options.

- **The frontier-model answer.** A general multimodal model offered for a job a pre-built API does. Everything the option says is achievable. It is the wrong answer because the problem is already solved as a product, and the exam consistently prefers the product.
- **The text-translation answer.** Translation where layout preservation was the requirement.
- **The single-API answer.** One capable API where the scenario described a pipeline of three transformations.
- **The wrong-stage studio answer.** Agent Studio for an exploratory prototype, or Google AI Studio for a production deployment.
- **The new-platform answer.** A machine learning platform offered to SQL analysts whose data is already in the warehouse, where BigQuery ML does it in place.
- **The wrong-execution-shape answer.** Cloud Run where a small event-triggered function was described, or Cloud Functions where a prepared container image was.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Extracts fields from scanned documents or PDFs | Document AI | A multimodal model reading each page |
| Must keep tables and layout after translating | Document Translation API | Translation API |
| Describes speech in, understanding, speech out | The set of three APIs | The single most capable one |
| Has a container image ready to deploy | Cloud Run | Cloud Functions |
| Triggers small logic when an event happens | Cloud Functions | Cloud Run |
| Has SQL analysts and data in the warehouse | BigQuery ML | A separate ML platform and a new skill |
| Wants a quick, low-setup experiment | Google AI Studio | Agent Studio |
| Needs production deployment at scale | Agent Studio | Google AI Studio |
| Names poor connectivity or on-device response | Edge, LiteRT, Gemini Nano | A cloud-hosted frontier model |

The habit: describe the scenario as "X goes in, Y comes out" before reading the options. The shelf is organised by exactly that, so the sentence usually names the product for you.

## What to Remember

- **The shelf before the model.** If the problem is solved as a **pre-built API**, that is the answer, and a frontier model is the expensive way to the same place.
- **Speech-to-Text** transcribes audio and video; **Text-to-Speech** produces natural speech and voice interfaces.
- **Translation API** translates content; **Document Translation API** translates formatted documents and **preserves the layout**. The deciding word is about **shape, not language**.
- **Document AI extracts data from documents** and automates capture and processing. It is the answer for **scanned files and PDFs**.
- **Cloud Vision analyses images**; **Video Intelligence analyses video**; **Natural Language derives sentiment, classification and entities from text**.
- **Combination questions want the pipeline.** Decompose into transformations and name an API for each, rather than picking the strongest one.
- **Cloud Run** runs **containers** and **scales to zero**; **Cloud Functions** runs **small event-driven code**; **Cloud Storage** holds **unstructured files**.
- **BigQuery ML trains a model from SQL**, in place, which is the answer for **analysts who know SQL** and **data already in the warehouse**.
- **Google AI Studio** is **free, for quick prototyping**. **Agent Studio** is for **production at scale**. The distinction is **exploration against production**.
- **Edge means running close to the action**, for **latency and unreliable connectivity**. **LiteRT deploys to devices** and **Gemini Nano is the on-device model**.
- **Apps Script and AppSheet** are the **low-code and no-code** route for functions with no engineers.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Document AI documentation. https://docs.cloud.google.com/document-ai/docs
4. What is Cloud Run. https://docs.cloud.google.com/run/docs/overview/what-is-cloud-run
5. AI in BigQuery. https://docs.cloud.google.com/bigquery/docs/ai-introduction
