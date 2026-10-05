# Chapter 6: Four Google Models, and the Question That Picks One

**Summary:** *The blueprint names four Google foundation models, and the exam asks you to choose between them often enough that this is the best return on memorisation anywhere in the first section. The good news is that the choice is nearly always decided by one property. The bad news is that candidates reach for the most capable model by reflex, which is correct often enough to feel like a strategy and wrong in exactly the cases the exam cares about.*

## Two Requests, Two Models, and the Difference Is Not Quality

Two teams ask for help in the same week.

The first wants an assistant that can take a photograph of a damaged part, read the attached service history, and explain what probably happened. The second wants a model running on hardware inside a factory with no reliable network, summarising shift reports into a few lines.

Both are reasonable. Both are well within what Google offers. They get different models, and the deciding factor is not which model is better, because on raw capability one of these answers is clearly the weaker model and it is still the right choice.

## Modality First, Then Where It Has to Run

**Modality first** is the rule. Before anything else, ask what data types have to go in and what has to come out, because that eliminates most of the list immediately.<sup>[1]</sup>

| Model | What it is for | The cue in a scenario |
|---|---|---|
| Gemini | Multimodal understanding, conversation, content creation and question answering | More than one data type; reasoning; a large amount of text to hold at once |
| Gemma | Open and customisable, built for local deployment and specialised applications | Running it yourself, on your own hardware, lightweight, offline, open |
| Imagen | A diffusion model that turns written descriptions into finished images | An image has to be produced from words |
| Veo | Video generated from text descriptions or from still images | A video has to be produced |

Those four descriptions are Google's.<sup>[2]</sup> The catalogue on the platform is larger than the blueprint's four, and includes models for other modalities such as Lyria for music, but the exam asks about these.<sup>[3]</sup>

## Gemini Is the Default, and Knowing When It Is Not Is the Examinable Part

Gemini is Google's multimodal model, and it is the answer to a lot of questions: anything mixing text with images, anything needing reasoning over a long document, anything conversational.<sup>[2]</sup> When a scenario lists several data types and several tasks, Gemini's multimodal breadth is the model-level strength that covers all of them at once, and that is usually what the question is testing.

Two cases turn it into the wrong answer, and both appear on this exam.

**The first is determinism.** A generative model produces plausible output, not identical output, and it does not guarantee the same input will yield the same result. So a scenario demanding strict, rule-governed outcomes, where a given input must always produce exactly one prescribed decision, is describing something a generative model is the wrong shape for. Rules engines are deterministic by construction. Generative models are not, and no amount of capability changes that. **The capable-model answer** is the trap: an option that is right about Gemini's power and wrong about the requirement.

**The second is where the model has to run.** Gemini is served from Google's infrastructure. A scenario that specifies hardware you control, a site with poor connectivity, or a deployment you need to own and modify is pointing at Gemma, which is open and light enough to be served from your own environment, including a cluster you run yourself.<sup>[4]</sup>

## Gemma Is Not a Lesser Gemini

Gemma is the model candidates underuse, because "lightweight" reads as "worse" and the exam does not treat it that way.

Google's framing is that Gemma offers developers a user-friendly, customisable option for local deployments and specialised applications.<sup>[2]</sup> Three words in that sentence do the work. **Customisable**, so you can adapt it. **Local**, so it runs where you put it. **Specialised**, so it is aimed at a defined job rather than at everything.

Which means a scenario about producing competent written output at volume, summaries and first drafts of routine documents, is well served by Gemma: it is lightweight text generation, and the task is the kind of narrow, repeated work that does not need a frontier model. Reaching for the biggest available model there looks like caution. *It is just an invoice.* You are paying for capability the task never touches, on work that humans will skim and approve in seconds.

| The scenario says | The model | Why |
|---|---|---|
| Analyse an image and the text alongside it | Gemini | More than one modality in the input |
| Summarise long transcripts, holding a lot at once | Gemini | Large context window |
| Deploy on our own hardware, or offline | Gemma | Open and locally deployable |
| Draft and summarise routine documents at volume | Gemma | Lightweight text generation is the fit |
| Create an image from a written description | Imagen | Text to image |
| Produce a short video from a script or a still | Veo | Video generation |
| Every input must produce one prescribed outcome | None of them | Determinism is not a generative property |

## Imagen and Veo Are Decided by the Output Alone

These two are the easiest marks on the objective and the fastest to lose by skimming.

Imagen takes a written description and returns a finished image, and it does it by diffusion, which is why chapter 2 pairs those two names together.<sup>[2]</sup> Veo generates video, either from a text description or from a still image as the starting point.<sup>[2]</sup>

The distinction that matters is only the output. A scenario about *understanding* an image, classifying it, describing it, extracting text from it, is not an Imagen question, because Imagen makes images rather than reading them. Understanding an image is Gemini, or one of the pre-built vision APIs in chapter 13. **The input-output inversion** is the trap: a model named because its modality appears in the scenario, rather than because it produces the thing being asked for.

## How Wrong Answers Are Built on This Material

Model-choice questions are built out of real Google models, correctly described, aimed at the wrong requirement. Nothing here is a fake product, so there is nothing to spot as implausible.

- **The capable-model answer.** Gemini, offered for a problem whose constraint is determinism, deployment location or cost. Everything the option says about Gemini is true. It becomes correct whenever the constraint is actually capability, breadth or context length, which is most of the time, which is what makes it dangerous.
- **The input-output inversion.** A generation model named for an understanding task, or the reverse. Imagen for reading an image, Gemini for making a film.
- **The size-is-quality answer.** It treats the largest model as the safe choice regardless of the stated constraint. Where the scenario names local hardware or routine volume work, the smaller open model is the answer and the larger one is a wrong answer with good manners.
- **The wrong-family answer.** A code-specialised or speech-specialised model offered where the blueprint's four are what is being tested. Know the four, and treat an unfamiliar name as a prompt to check which modality it serves.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Mixes data types, or needs long-context reasoning | Gemini | A single-modality model matching one input type |
| Names your own hardware, offline use, or customisation | Gemma | Gemini, described accurately and deployed impossibly |
| Demands identical output for identical input | A generative model is the wrong tool | The most capable generative model |
| Asks for an image to be produced | Imagen | Gemini, for being generally stronger |
| Asks for an image to be understood | Gemini or a vision API | Imagen, because an image is mentioned |
| Describes routine drafting at volume | Gemma | Gemini, because drafting sounds like writing |

The habit: name the output modality, then name the constraint on where it runs. Two sentences, and the list is down to one.

## What to Remember

- **Modality first.** Decide **what goes in and what comes out** before considering anything else; it eliminates most options at once.
- **Gemini** is the **multimodal** model: several data types, **conversation, content creation, question answering**, and a **large context window** for long inputs.
- **Gemma** is **open, lightweight and customisable**, built for **local deployment** and **specialised applications**. It is **not a lesser Gemini**; it is the answer when you must **run it yourself**.
- **Imagen** is **text to image** and is a **diffusion model**. **Veo** is **video**, from **text or a still image**.
- **Generative models are not deterministic.** A scenario demanding **one prescribed outcome per input** is not a generative problem at all, however capable the model.
- **Generation is not understanding.** Imagen **makes** images and does **not read** them. Reading an image is **Gemini or a vision API**.
- **Routine drafting and summarising at volume fits Gemma.** Choosing the largest model there buys **capability the task never uses**.
- **Match the output, then the deployment location.** Those two sentences decide nearly every question on this objective.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Overview of models on Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/models
4. Serve Gemma on GPUs with TGI. https://docs.cloud.google.com/kubernetes-engine/docs/tutorials/serve-gemma-gpu-tgi
