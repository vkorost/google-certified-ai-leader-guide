# Chapter 12: What an Agent Is Made Of, and What It Can Reach

**Summary:** *An agent is the one concept in this exam that gets defined, taken apart, sorted into types and then tested on all three, which is why the word turns up under eight of the fifteen objectives. The definition is short and you will be held to it precisely: something with a goal, a view of its situation, and the means to change it. Most wrong answers describe a thing with only two of those three, and the part missing is nearly always the ability to do anything.*

## A Chatbot Answers. An Agent Acts.

That is the distinction, and the rest of this chapter elaborates it.

Google's definition has three parts, and you need all three.<sup>[2]</sup> An agent is software pursuing a **goal**. It forms a picture of the situation it is in. And it can change that situation, using whatever tools it has been handed.

**Goal, observe, act.** Drop any one and you are describing something else. A dashboard observes and cannot act. A scheduled script acts and never looks. A person has goals and is not software. All three of those appear as distractors, and the first one appears most, because it describes most of what organisations already own.

The phrasing the exam tends to put in the right answer is the practical version of the same thing: it sizes up what is in front of it, reaches for more than one tool, and gets on with it without someone approving each step.

## Three Parts, and the Cycle That Drives Them

| Part | What it contributes |
|---|---|
| Model | The thinking. Algorithms that learned patterns from data and can produce content<sup>[2]</sup> |
| Tools | The reach. Whatever lets it touch data, systems or hardware outside itself<sup>[2]</sup> |
| Reasoning loop | The motion. It observes, interprets, decides a next step and acts, over and over<sup>[2]</sup> |

The **reasoning loop** is examined by name, so learn it as a cycle rather than a list: notice, interpret, plan, act, and begin again. When a question describes a repeating process of watching, working out, deciding and doing, that cycle is the term being asked for. Prompt engineering is usually what drives each turn of it.

Why it matters beyond the vocabulary: a system that decides its own next step, repeatedly, based on what it just found, has no fixed route for anybody to review in advance. You can review its goal and you can review its tools. You cannot review the path, because the path does not exist until it runs. Chapter 22 comes back to this, because it is where the accountability questions start.

## Three Types, and the One Most Real Systems Turn Out to Be

Google sorts agents three ways.<sup>[2]</sup>

**Deterministic agents**, which Google also calls traditional: the paths and the actions are laid down in advance. Give one the same input and it takes the same route, every time.

**Generative agents**: the behaviour is specified in ordinary language and carried by a large language model, which is what makes a conversation feel like a conversation rather than a phone menu.

**Hybrid agents**: both at once, in one system, and Google is direct about this combination being where the power is.

The hybrid agent is blueprint surface that no question in circulation touches, which makes it worth the thirty seconds. The logic is worth more than the label. The deterministic half holds the steps that must never vary, moving money, checking entitlement, escalating a complaint. The generative half absorbs the part nobody could enumerate in advance, which is whatever the human actually said. *Neither half can do the other's job.*

Agents also get named for the **work** they do rather than how they are built, and the exam uses that vocabulary freely. Something that drives a multi-step business process from end to end is a workflow agent. Something that researches threats and writes detection rules is a security agent. The job names the agent; how it was constructed is a separate question.

## Four Kinds of Tool, and They Are Not Interchangeable

This is the most heavily tested part of the objective, and the four categories sit in the blueprint by name.<sup>[1]</sup><sup>[2]</sup>

| Reach for it when | The category | What the agent gets |
|---|---|---|
| It has to work with a service somebody else runs | **Extensions** | A standard way in, through that service's API |
| A particular piece of your own logic has to run | **Functions** | A named action it can call |
| Something has to be looked up | **Data stores** | A route to information |
| It needs a capability it was not built with | **Plugins** | Extra skills, added on |

Two of those overlap in practice and the exam accepts the pair. Where a scenario has the agent needing something from an outside service, checking a flight, taking a booking, reading today's price, the answer is extensions or functions, because both are ways to call an external API. Where the question forces one and leans on **standardised interaction with somebody else's API**, choose extensions.

Where it is specifically about a **small piece of backend code firing on an event**, the Google product underneath is Cloud Functions, and chapter 13 puts it on the shelf with the rest.

## Fresh Information Comes From Tools, Never From Training

One scenario shape recurs across the whole exam, and this is the chapter where the reasoning becomes obvious.

An agent needs something that is true at this moment: stock on hand, today's price, the state of an order. The instinct is to get that knowledge into the model. The answer is that the agent **asks a live source through a tool**, at the moment it needs to know.<sup>[2]</sup><sup>[3]</sup>

A model holds a snapshot. A tool reaches the present. **The retrain-for-freshness answer** is the named trap, and it is chapter 11's ladder error wearing different clothes.

## Several Agents, When One Will Not Do

Multi-agent systems exist for complex work that needs **coordinated** specialists, each owning a part, with something organising them.<sup>[3]</sup>

Get the phrasing right, because the exam asks for the benefit specifically. The benefit is **coordination of specialisms on complex tasks**. It is not that several agents are faster, cheaper or more accurate than one. When a scenario spans several genuinely distinct kinds of expertise, that is the cue.

## How Wrong Answers Are Built on This Material

Definition questions are built from things that sit next to an agent, each short of one part of the definition. Tooling questions are built from the other three categories. Both reward precision over recognition.

- **The missing-action answer.** Something that watches and reports and cannot change anything: a dashboard, an analysis, a report. The commonest distractor on agent definitions.
- **The interface answer.** The agent defined as a screen, a window, the place a person types. That is the application layer from chapter 5, sitting above the agent rather than being it.
- **The static-component answer.** A model, a data store or a piece of infrastructure offered as the definition. Each is a part, and a part is not the whole.
- **The retrain-for-freshness answer.** Teaching the model current data instead of giving the agent a way to fetch it.
- **The wrong-tool-category answer.** A data store where an external call was needed, or an extension where a lookup was wanted. Ask whether the agent needs to **read** something or **do** something.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Asks what an agent is | Goal-directed, uses tools, decides without step-by-step approval | Something that observes but cannot act |
| Describes noticing, interpreting, planning, acting, repeating | The reasoning loop | Prompt chaining, or the model itself |
| Needs live data from an outside service | Extensions or functions | Retraining or tuning on that data |
| Stresses a standard way into somebody else's API | Extensions | Data stores, because information is involved |
| Needs to look something up | Data stores | Extensions, because an API is implied |
| Spans several distinct specialisms | A multi-agent system | One larger agent, or a stronger model |
| Automates a multi-step business process | A workflow agent | A conversational agent |

The habit: for any agent question, ask whether the thing described can change something in the world. If it cannot, it is not an agent, whatever else is true of it.

## What to Remember

- **Goal, observe, act.** An agent **pursues a goal**, **forms a picture of its situation**, and **changes that situation with tools**. Missing any one means it is something else.
- **The practical phrasing**: it **sizes up the situation**, **uses several tools**, and **proceeds without approval at every step**.
- **Three parts**: the **model** does the thinking, **tools** give it reach, the **reasoning loop** keeps it moving.
- **The reasoning loop is notice, interpret, plan, act, repeat.** It is why an agent **has no route to review in advance**: you can review the goal and the tools, never the path.
- **Three types**: **deterministic** with paths laid down, **generative** specified in ordinary language on an LLM, and **hybrid**, which Google calls the powerful combination.
- **Four tool categories**: **extensions** for somebody else's service through its API, **functions** for your own logic, **data stores** for looking things up, **plugins** for skills it lacks.
- **A live external call is extensions or functions.** Where a **standard way into another party's API** is stressed, **extensions**.
- **Fresh information comes from tools, never training.** A model holds **a snapshot**; a tool reaches **the present**.
- **Multi-agent systems are for coordinated specialisms** on complex work, **not for speed or cost**.
- **Agents get named for their work**: a **workflow agent** drives a multi-step process, a **security agent** does security.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Agents overview, Gemini Enterprise Agent Platform. https://docs.cloud.google.com/gemini-enterprise-agent-platform/agents/overview
