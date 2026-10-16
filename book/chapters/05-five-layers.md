# Chapter 5: Five Layers, and Which One Owns Your Problem

**Summary:** *Google describes the generative AI world as five stacked layers, and the exam asks you to place things in them, repeatedly. The questions are not hard once the layers are clear, and they are nearly impossible when they are not, because the distractors are always the layer above or below. This chapter is also the map the rest of the book runs on: every product in section 2 sits in one of these five, and knowing which one tells you what kind of decision it is.*

## The Stack Is the Answer Sheet for Most of Section 2

You are going to be handed a scenario that describes something concrete, a rack of accelerators, a set of APIs, a chatbot a customer talks to, and asked which layer of the landscape it belongs to.

Google calls the whole picture the **gen AI landscape**, and its layers run from the ground up: infrastructure, models, platforms, agents, applications.<sup>[1]</sup>

| Layer | What it provides | What it means for a business |
|---|---|---|
| Infrastructure | Servers and accelerators, plus the software that stores and runs models and their training data | Capacity and cost. It sets the ceiling on what you can run |
| Model | The trained algorithm itself, holding the patterns learned from data | Capability. It sets what is possible at all |
| Platform | APIs, data management, tuning and deployment tooling over the models | Speed. It removes the infrastructure work between a model and a product |
| Agent | Software that pursues a goal, deciding and acting with the tools it holds | Autonomy. It does work rather than answering questions |
| Application | The user-facing surface sitting over any of the above | Adoption. It decides whether anyone actually uses it |

Each layer rests on the ones under it, and that ordering is examinable in its own right.<sup>[2]</sup>

## The Layer That Owns the Decision

Here is why this is a leader's chapter rather than an architecture diagram.

**The layer that owns the decision** is the layer where your real constraint lives, and it is almost never the layer where the symptom appears. A chatbot giving stale answers looks like an application problem, and it is a model-or-grounding problem. A project that cannot get out of pilot looks like a model problem, and it is usually a platform problem: nobody can deploy the thing. A cost overrun looks like a platform problem, and it is infrastructure.

So the diagnostic habit is to find the layer that will still be a problem after you have fixed the obvious one. *The symptom and the owner are rarely the same layer.*

## Infrastructure Is Hardware, and the Exam Means That Literally

The infrastructure layer supplies the core computing resources: the physical hardware, meaning servers and accelerators such as GPUs and TPUs, along with whatever software is needed to train a model, keep it somewhere and run it.<sup>[2]</sup>

When a question asks for the **hardware components** of this layer, it wants accelerators. TPUs are Google's own custom-designed chips for this work and GPUs are the general-purpose alternative; both are infrastructure, both are named in the blueprint, and neither is anything else.<sup>[1]</sup><sup>[3]</sup>

**The higher-layer answer** is the standard distractor here. A question about hardware components will offer you models, platforms or applications as options, and each of those is a real part of the landscape sitting at the wrong altitude. If the question says hardware, compute, or resources needed to run and train, the answer is infrastructure and the only candidates are chips, servers, networking and storage.

## Platform Is the Layer People Most Often Misplace

The platform layer sits over the models and hands you three things: a way to call them programmatically, somewhere to manage the data they work on, and the machinery to put what you build into production. It closes the distance between a raw model and a working agent, and it keeps infrastructure management out of your way.<sup>[2]</sup>

Read that as three claims, because each one answers a different question on the test. A platform gives you **programmatic access** to models. It gives you somewhere to **manage the data** they use. It gives you a way to **deploy** what you build. The business implication is that AI development, deployment and management get simpler, which buys scalability and speed.

The two confusions, both common:

| Not the platform layer | Why | Which layer it is |
|---|---|---|
| The accelerators the platform runs on | Hardware, however managed | Infrastructure |
| The chat window an employee types into | Where a human interacts | Application |
| The model being served | The algorithm itself | Model |
| The thing that pursues a goal using tools | Autonomous action | Agent |

On Google Cloud the platform layer is Agent Platform. Chapter 11 is about what it contains.

## Models, Agents and Applications

The **model** layer is the trained algorithm: it has learned patterns and relationships from a great deal of data, and that is what lets it generate content, translate, answer and the rest.<sup>[2]</sup> Chapter 6 covers Google's four.

The **agent** layer is software that sets out to reach a goal: it looks at the situation around it, works out what to do, and does it with whatever tools it has been given.<sup>[2]</sup> The distinguishing property is not intelligence, it is initiative: an agent takes steps. Chapter 12 takes it apart.

Two things to carry now. First, an agent sits **above** the platform, because it is built using one. Second, agents are usually described by the job they do rather than by their technology, which is why a scenario about researching threats and writing detection rules is answered with the agent for security work rather than with a general-purpose assistant. The job names the agent.

The **application** layer is the user-facing part, where a person meets the capability and gets something out of it. Google's term for what sits here is a **gen AI powered application**, and the word that matters in it is *application*: this is the layer people actually touch.<sup>[2]</sup> It is the layer most likely to be dismissed as the thin bit on top, and the layer that decides whether anything underneath it earns a return.

## How Wrong Answers Are Built on This Material

Every distractor on this objective is a genuine layer of the landscape, correctly described, placed one step away from the right one. There is no nonsense to eliminate, which is why these questions catch people who understand the material perfectly well and read quickly.

- **The higher-layer answer.** Platform or application offered for a question about compute. It is seductive because platforms and applications are what people talk about. The cue that rules them out is any mention of hardware, chips, servers, running or training capacity.
- **The lower-layer answer.** Infrastructure offered for a question about tooling and deployment, usually because the stem mentions scale. Scale is a business outcome of the platform layer, not evidence of an infrastructure question.
- **The product-name answer.** It names a Google product that does sit in the landscape, when the question asked for a layer. If the question asks which layer, answer with a layer.
- **The symptom-layer answer.** It names the layer where the problem is visible rather than where it is caused. Stale answers surface in an application and originate in grounding.

| When the question | The answer is usually | The trap is usually |
|---|---|---|
| Asks for hardware or compute resources | Infrastructure, meaning TPUs and GPUs | Platform, which is where that compute is consumed |
| Describes APIs, data management and deployment tooling | Platform | Infrastructure, because scale is mentioned |
| Describes a human typing, asking or clicking | Application | Platform, because a platform is serving it |
| Describes software pursuing a goal with tools | Agent | Application, because a human sees the result |
| Describes a specialised job like threat research | The agent for that job | A general-purpose assistant |

The habit that transfers: say the layer's one-word job out loud before choosing. Capacity, capability, speed, autonomy, adoption. If the scenario is about one of those words, the layer attached to it is the answer.

## What to Remember

- **Five layers, bottom up**: **infrastructure, model, platform, agent, application**. Each rests on the ones below it.
- **Infrastructure is literally hardware**: **servers, GPUs and TPUs**, plus the software to store, train and run. **TPUs** are Google's **custom-designed** chips.
- **Model is the trained algorithm** that holds the learned patterns. It sets **what is possible**.
- **Platform means three things**: **API access to models**, **data management**, and **deployment tooling**, with the infrastructure hidden. Its business implication is **simpler development and faster scaling**.
- **Agent means initiative**: software **pursuing a goal** by **observing and acting** with **tools**. It sits **above** the platform because it is built on one.
- **Application is where humans interact** with the capability, and it is what decides **adoption**.
- **The layer that owns the decision is rarely the layer showing the symptom.** Stale answers appear in the **application** and are caused in **grounding**.
- **Every distractor here is a real layer one step away.** Match the scenario to a layer's **one-word job**: capacity, capability, speed, autonomy, adoption.
- **If a question asks which layer, the answer is a layer**, not a product name.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Generative AI on Google Cloud. https://docs.cloud.google.com/docs/ai-ml/generative-ai
