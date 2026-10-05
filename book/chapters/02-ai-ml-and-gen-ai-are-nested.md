# Chapter 2: AI, ML and Gen AI Are Nested, and the Order Matters

**Summary:** *Several times on this exam you will be shown four definitions, all of them accurate descriptions of something, and asked which one defines generative AI. Three will define a neighbour: a neural network, deep learning, a regression model. The skill being tested is not whether you know roughly what gen AI is. It is whether you can say what sits inside what, and what each layer adds that the layer above it does not have. Learn the nesting and these questions collapse.*

## The Definition Questions Are Boundary Questions

You are going to meet a question that lists four sentences, each of which is true about something in this field, and asks which one defines generative AI.

Here is the thing to understand about that question before you meet it. The wrong options are not wrong. One of them accurately describes a system of interconnected nodes loosely modelled on a brain. One accurately describes fitting a line through observed data to estimate a relationship. One accurately describes a system that improves itself from data using many-layered networks. Every one of those is a real thing with a real name, and none of them is the name on the question.

So the work is not recall. It is placement.

## Everything Here Fits Inside Something Else

**The containment order** is the single most load-bearing fact in this section of the exam, and it is four nested statements.

Artificial intelligence is the outer ring: building machines that do things we would otherwise call thinking, like learning, solving problems and deciding. Machine learning sits inside it, and narrows it with one condition: the machine learns from data rather than being told the rules. Deep learning sits inside machine learning, and narrows it again: the learning happens in neural networks with many layers, which is what lets them pull complex patterns out of messy input. Generative AI is an application of machine learning with a specific output: new content.<sup>[2]</sup>

| Layer | What it adds that its parent does not have | What it does not imply |
|---|---|---|
| Artificial intelligence | Machines doing tasks that need intelligence | Any learning at all; rules can be hand-written |
| Machine learning | The rules are learned from data | Neural networks, or depth |
| Deep learning | Many-layered neural networks | Generating anything |
| Generative AI | New content as the output | A chatbot, or a particular architecture |

Read the right-hand column twice. It is where the exam's distractors come from.

Two more pieces attach to the bottom of that stack rather than extending it. **Foundation models** are large models trained on enormous quantities of unlabelled data, which gives them a broad general grasp of their domain and makes them adaptable to many tasks instead of one. They are what gen AI applications are built on. A **large language model** is a foundation model specialised to human language: understanding it and producing it.<sup>[2]</sup>

That relationship has a direction, and the direction is examinable. Every large language model is a foundation model. Not every foundation model is a large language model, because a model trained on images is still a foundation model.

**Natural language processing** is the odd one out, and candidates trip on it. It is not a layer in the stack. It is a field: getting machines to work with human language. Large language models are currently the most capable technology serving it, and classical NLP long predates them. The exam lists it among the core concepts, so know what it names.<sup>[1]</sup>

## What Separates Generative AI From the AI That Came Before It

Google draws this line in its own documentation, and the line is one sentence long. Traditional AI learns from data that already exists in order to classify it or predict what comes next. Generative AI extends that into producing something new: a summary, an image, a passage of code, a relationship nobody had noticed.<sup>[3]</sup>

The useful consequence is a test you can apply to any option on any question.

**Ask what the system hands back. If the output is a label, a score, a number or a forecast, it is traditional AI. If the output is content that did not exist before, it is generative.**

Which sorts the usual suspects immediately:

| The task | What it hands back | Which kind |
|---|---|---|
| Deciding whether an email is spam | A label from a fixed set | Traditional, classification |
| Predicting a house price | A continuous number | Traditional, regression |
| Forecasting next quarter's demand | A number over time | Traditional, time series |
| Grouping customers by purchase behaviour | Cluster membership | Traditional, clustering |
| Writing the product description | Text that did not exist | Generative |
| Turning a text description into an image | An image | Generative |
| Summarising a thousand support calls | A new, shorter text | Generative |

That table is also a warning about a trap, because clustering is sitting in it. Customer segmentation feels like the most modern thing on the list. *It is the oldest.* Grouping records with no labels is traditional unsupervised machine learning, and it has been running in production for decades.<sup>[3]</sup>

## Diffusion Models Build Content Out of Noise

One architecture gets named specifically in the blueprint, so it gets a paragraph.<sup>[1]</sup>

A diffusion model starts from random noise and repeatedly refines it until structured content emerges. That is the mechanism, and the reason to know it is that Imagen, Google's text-to-image model, is a diffusion model producing high-quality images from written descriptions.<sup>[2]</sup>

Learn it as a one-line pairing: diffusion means noise refined into content, and the Google product attached to it is Imagen.

## Multimodal Means More Than One Kind of Data, Anywhere in the Pipeline

A multimodal model handles more than one type of data: text, images, audio, video, code, in some combination.<sup>[1]</sup>

The detail that decides questions is that the mixture can be on either side. A model that reads an image and writes text about it is multimodal. So is one that reads text and produces video. So is one that takes a video and a spreadsheet together and answers a question that needs both.

Which gives the single most common way a multimodal question is answered wrongly. **The one-modality-each-way answer** looks multimodal because two different data types appear in the scenario, but they appear in two separate single-type steps: one tool transcribes the audio, a different tool summarises the transcript. Two systems, each handling one modality, is not one multimodal system. The test is whether a single model is holding more than one type of data at once.

## Four Verbs, and They Are Google's Own Shorthand

Google compresses what gen AI is for into four words: it can **create**, **summarize**, **discover** and **automate**.<sup>[2]</sup>

No question in circulation uses that shorthand directly, which is exactly why it is worth holding. It is a checklist for recognising a use case when the scenario does not announce itself, and the product documentation sets out what each verb covers: generating content and recommending it, running conversational search and assistants, finding insight and relationships buried in documents and data, scaling repetitive workflow, and writing and explaining code.<sup>[3]</sup>

The fourth verb carries a condition that the exam asks about directly. Automation with gen AI fits work that is **repetitive and rule-governed**.<sup>[3]</sup> It does not fit the two cases people reach for first:

- Work that is genuinely creative or needs original strategic thought, where gen AI assists a human rather than replacing the step.
- Work on sensitive material, or any decision that needs to be answerable to someone, which calls for a human in the loop rather than automation.

**The automate-the-hard-part answer** is a reliable trap. An option offering to automate the strategic judgement, the ethical call or the high-stakes decision sounds ambitious and is always wrong on this exam. Google's position is consistent: automate the repetitive, assist the creative, supervise the consequential.

## How Wrong Answers Are Built on This Material

Definition questions on this material are built out of true statements about neighbouring things. That is the entire technique, and it means reading faster makes you worse at them, because every option passes a quick plausibility check.

Three families cover almost all of it.

- **The architecture answer.** It describes the mechanism rather than the output: interconnected nodes modelled on the brain, many-layered networks that learn by themselves. Those describe neural networks and deep learning. They become correct when the question asks how the thing is built. They are wrong when the question asks what it produces.
- **The adjacent-technique answer.** It accurately describes a different technique from the same field: fitting a line to data, classifying into categories, grouping records with no labels. Each one is a real method, correctly described, answering a question nobody asked. The giveaway is that the option never mentions anything being produced.
- **The application answer.** It names a product or an interface where a concept is wanted: a chatbot, an assistant, a tool that answers questions. A chatbot is somewhere generative AI gets used. It is not what generative AI is, and confusing a surface with a technology is the most common error in the whole of this section.

| When the question | The answer is usually | The trap is usually |
|---|---|---|
| Asks what gen AI *is* | The option naming new content as the output | A true description of a neural network or deep learning |
| Asks for an example of gen AI | Something producing text, images, audio, video or code | Classification, prediction, forecasting or segmentation |
| Describes two data types in two steps | Not multimodal | Calling it multimodal because two types appear |
| Asks when to automate with gen AI | Repetitive, rule-governed work | Automating the creative, sensitive or high-stakes step |
| Names a specific architecture | Match the mechanism to the product | A plausible mechanism attached to the wrong product |

The habit that transfers: for every option, name the thing it actually describes. If you can say "that is deep learning" or "that is regression" out loud, you have eliminated it for a reason rather than a feeling.

## What to Remember

- **The containment order**: **AI contains machine learning, which contains deep learning**; **generative AI is an application of machine learning** whose output is new content. Each layer adds **one condition** and implies nothing about the layers below it.
- **Machine learning means the rules come from data**, not from a person writing them. **Deep learning** means **many-layered neural networks**. Neither implies generation.
- **Every large language model is a foundation model; not every foundation model is a large language model.** A foundation model is trained on **huge amounts of unlabelled data**, which is what makes it adaptable to many tasks.
- **Natural language processing is a field, not a layer** in the stack: making machines work with human language. LLMs **serve that field** and are **not identical to it**.
- **The output test**: a **label, score, number or forecast means traditional AI**; **content that did not exist means generative**. It settles almost every "which is an example of" question.
- **Clustering and customer segmentation are traditional unsupervised machine learning**, not gen AI, however modern they sound.
- **Diffusion means refining random noise into structured content**, and Google's diffusion product is **Imagen**, text to image.
- **Multimodal means one model holding more than one data type**, on the input side, the output side or both. **Two single-modality tools in sequence** is not multimodal.
- **Four verbs**: gen AI can **create, summarize, discover and automate**. Automate applies to **repetitive, rule-governed work**; creative work gets **assistance** and consequential decisions get **a human in the loop**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. When to use generative AI or traditional AI. https://docs.cloud.google.com/docs/ai-ml/generative-ai/generative-ai-or-traditional-ai
