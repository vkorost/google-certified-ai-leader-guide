# Chapter 11: Ground, Tune or Train on the Platform

**Summary:** *Agent Platform is the single most heavily tested product on this exam, and the questions are not about what it is. They are about which part of it answers a given need, and the parts are easy to confuse because three of them have similar names and one of them is routinely mistaken for another product entirely. Underneath the naming sits a decision ladder with three rungs, and climbing higher than you need to is the most expensive mistake available on this material.*

## Two Teams, Same Problem, Different Rung

Two teams want a model that knows about their business.

The first team's content changes weekly: prices, policies, stock. The second team needs output in a format and register that no general model produces, and the format is not going to change.

Both say they need a model trained on their data. Only one of them is anywhere near correct, and the difference is not a matter of degree. They need different rungs of the same ladder.

## Ground, Tune, or Train

**Ground, tune, or train** is the ladder, and it runs in that order for a reason: each rung costs more than the one below it, and the lowest rung that works is the answer.

| Rung | What changes | What it is good for | What it costs |
|---|---|---|---|
| **Ground** | Nothing in the model. It retrieves from the organisation's own sources at the moment of the question | Facts that change, anything needing a citable source | Setting up retrieval over that content |
| **Tune** | The model's weights, adjusted on supplied examples | Behaviour: format, register, terminology, a specialised task | Examples, and a tuning run |
| **Train** | Everything. The model itself gets built | Cases a general model genuinely cannot reach | Data, machine learning specialists, months |

So the first team grounds. Their content changes weekly, and a tuned model would be stale by the time it shipped, because tuning teaches behaviour rather than facts. The second team tunes, since what has to change is how the model writes, and that is the one thing tuning does change.

Neither of them trains. *Almost nobody trains.*

## Agent Platform Is One Platform Doing Four Jobs

Agent Platform is the platform layer on Google Cloud. One place covers the whole of machine learning and generative AI work there: the compute underneath, a catalogue of models already trained, the tooling to build with, and the means to put the result into production and keep it running.<sup>[2]</sup><sup>[3]</sup>

The reason the exam asks about it so often is that "unified" is the answer to a specific scenario: an organisation that wants one place to get a model, build with it, put it into production and keep it running, rather than four products stitched together. When a scenario lists all four of those activities, the answer is the platform rather than any one component.

| Part | What it does | What it is NOT |
|---|---|---|
| Model Garden | A catalogue of existing models from Google, partners and open source<sup>[4]</sup> | Not where you train, and not a version registry |
| Model Builder | Where a model of your own gets built, hand-rolled with a machine learning framework<sup>[2]</sup> | Not needed if a pre-trained model will do |
| AutoML | The same training, reachable by people without machine learning skills<sup>[2]</sup> | Not a pre-trained model; it still learns from your data |
| MLOps tooling | Lets teams collaborate to monitor and improve models in production<sup>[2]</sup> | Not a build tool |

**The catalogue-as-registry answer** is the most reliable trap on this objective. Model Garden is where you go to *find and pick* a model; a registry is where you keep track of *versions of yours*. The study guide uses loose language about storing models in Model Garden, so the distinction is worth holding firmly: discovery and selection is Garden, version tracking is Model Registry, and chapter 18 covers the second.

## AutoML Is the Answer to a Skills Gap, Not to a Data Gap

AutoML gets its own section because it solves a problem candidates often mis-diagnose.

A team with its own data, a genuine need to train on it, and nobody who can write training code is not blocked. AutoML gets a model created and trained without much technical knowledge being required.<sup>[2]</sup> The requirement it removes is **expertise**, not data, and the humans it is aimed at are the ones who understand the business problem rather than the mathematics.

So the cue is a scenario naming both halves: data they own, plus a team without machine learning skills. A marketing function wanting predictions from its own campaign history is the standard shape. Where only one half is present, the answer is usually somewhere else: no data means a pre-trained model and prompting, and no expertise with no data means a pre-built API.

## Google's RAG Offerings Come in Two Shapes

Retrieval-augmented generation is the mechanism behind grounding, and chapter 16 covers how it works. What belongs here is which Google product delivers it, because the blueprint names two and they are chosen on a single distinction.<sup>[1]</sup>

**Prebuilt RAG with Agent Search** is the managed route: it is pointed at the organisation's own content and handles retrieval itself. The cue is a scenario about searching and answering over company material, especially material that keeps changing, where nobody wants to build a retrieval pipeline.

**RAG APIs** are the assembled route: the retrieval components arrive separately and get composed into an application somebody is already building. The cue is a scenario that already has an application and needs it to fetch current, relevant passages from specific documents at the moment of the query.<sup>[5]</sup>

The benefit to state in either case is the same, and the exam asks for it directly: retrieval brings in **current** information at question time, instead of relying on what a model absorbed during training.<sup>[5]</sup>

## Custom Agents Are Built Here Too, and That Is a Different Decision

Agent Platform is also where custom agents get built, and the exam distinguishes an agent problem from a model problem.<sup>[1]</sup><sup>[6]</sup>

The signal is **integration and rules**. When a scenario describes something that has to talk to several company systems, follow a defined process, and take actions rather than produce text, that is agent behaviour. No amount of model customisation produces it, because the thing missing is not how the model writes. It is what the software is allowed to do.

So: a request that needs answers and summaries from your content, rather than keyword retrieval, points at a custom agent. A request that needs a task-specific assistant wired into several internal systems points at a custom agent. **The model-customisation answer** is the trap, and it is seductive because customisation is a real and relevant capability that happens to be aimed at the wrong layer.

## How Wrong Answers Are Built on This Material

Every option on this objective is a real part of a real platform. The distractors work by naming a component that would be correct for a neighbouring need, so the discipline is to classify the need before reading the component names.

- **The train-it answer.** Custom training, or fine-tuning, offered where grounding is what the scenario described. The tell is content that changes: changing content is a retrieval problem and training cannot keep up with it.
- **The catalogue-as-registry answer.** Model Garden where version tracking was wanted, or Model Registry where model selection was wanted.
- **The model-customisation answer.** Tuning offered where the requirement is integration with systems and a defined process. That is agent work.
- **The component-for-the-platform answer.** One part of Agent Platform named where the scenario asked for an end-to-end place to build, deploy and manage. If the scenario lists all the activities, answer with the platform.
- **The expertise-is-data answer.** A pre-trained model offered to a team that genuinely needs to train on data they own. AutoML exists precisely for that case.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Says the content changes constantly | Grounding, retrieval, prebuilt RAG | Fine-tuning or training on that content |
| Needs a specific format, register or terminology | Tuning or customisation | Grounding, which does not change how it writes |
| Wants one place to build, deploy and manage | Agent Platform itself | A single component of it |
| Wants to find and pick an existing model | Model Garden | Model Registry, or Model Builder |
| Has their own data and no ML specialists | AutoML | A pre-trained model, which cannot learn their data |
| Must integrate with several systems and follow rules | A custom agent | Model customisation or fine-tuning |
| Asks the benefit of retrieval | Current information at query time | Reduced cost, or a smarter model |

The habit that transfers: say which rung of the ladder the scenario is on before you look at the products. Ground, tune, train. Most scenarios are on the first rung and most wrong answers are on the second.

## What to Remember

- **Ground, tune, or train**, in that order, and **take the lowest rung that works**. Each rung costs more than the one below.
- **Grounding changes nothing in the model**; it **retrieves at question time**. **Tuning changes behaviour**: format, register, terminology. **Training builds the model.**
- **Changing facts are a grounding problem.** Tuning teaches **behaviour, not facts**, so a tuned model goes stale.
- **Agent Platform is the unified platform**: **pre-trained models, build tools, deployment and management** in one place. If a scenario lists all of those, **answer with the platform**.
- **Model Garden is a catalogue** for **discovering, customising and deploying existing** Google, partner and open-source models. **It is not a version registry** and **not where you train from scratch**.
- **Model Builder trains your own models**; **AutoML trains them with minimal expertise**. AutoML answers a **skills gap, not a data gap**.
- **Two RAG offerings**: **prebuilt RAG with Agent Search** when you want it managed over your own content, and **RAG APIs** when you are composing your own application.
- **The benefit of retrieval is current information at query time**, rather than knowledge frozen at training.
- **Integration with several systems plus a defined process is agent work**, not model work. Customising a model **cannot change what the software is allowed to do**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Gemini Enterprise Agent Platform documentation. https://docs.cloud.google.com/gemini-enterprise-agent-platform
4. Agents overview, Gemini Enterprise Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/agents/overview
5. RAG Engine overview. https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/rag-engine/rag-overview
6. Build on Gemini Enterprise Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/build
