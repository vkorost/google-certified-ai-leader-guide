# Chapter 9: The Productivity Surface You Already Own

**Summary:** *Google puts Gemini into half a dozen places, and they are not interchangeable. The exam gives you an employee with a task and asks which surface they should be using, and the options are all real Google products that could all plausibly help. What decides it is where the work lives: in a chat window, in a document, in the cloud console, across the company's internal systems, or inside a specific set of uploaded files. This is a short chapter with a lot of marks in it.*

## The Request That Arrives Six Times

You run a function. Over a month, six people ask you some version of "can AI help with this".

One wants to draft and rework text in a chat window. One wants to stop retyping the same instructions every time. One wants help inside the documents and mail they already live in. One wants to search everything the company knows, across systems that do not talk to each other. One wants to interrogate a specific pile of forty PDFs and trust the answers. One wants help managing cloud infrastructure and writing code.

Those are six different products, and **the surface already in the building** is usually the right answer. The question is which one.

## The Six Surfaces

| Surface | Where the work happens | What it is for |
|---|---|---|
| Gemini app | A chat window | Writing, summarising, translating, creating images<sup>[2]</sup> |
| Gemini Advanced | The same window, with more | Extra capability and enterprise-grade protections, and **Gems**<sup>[2]</sup> |
| Gemini for Google Workspace | Inside Gmail, Docs, Slides, Meet | Composing mail, generating images in slides, summarising a meeting<sup>[2]</sup> |
| Gemini for Google Cloud | The cloud console and developer tools | Code, cloud operations, data queries, security posture<sup>[2]</sup> |
| Gemini Enterprise | Across the company's internal systems | Unified search and agents over scattered internal data<sup>[3]</sup> |
| Gemini Notebook | A set of files you upload | A research assistant grounded in those sources<sup>[2]</sup> |

Two of those names changed in April 2026. The current ones are in the table, and they are the ones the blueprint uses.

## Gems Are Saved Instructions, and That Is the Whole Idea

A Gem is a personalised assistant inside Gemini, carrying instructions you have given it once so that it responds the same way every time, which makes templates, repeated prompts and guided interactions quicker.<sup>[2]</sup>

The scenario cue is **repetition with a fixed shape**. Somebody producing the same kind of output over and over, in the same format, with the same background context: a weekly competitor summary, a standard report structure, an industry they always work in. Saving that context into a Gem is the answer, and it is a better answer than writing a longer prompt each time.

This sits next to a related feature worth knowing by name. **Saved info** in Gemini stores specific details for the model to use consistently, so you do not restate them.<sup>[2]</sup> Gems package instructions; saved info packages facts about you.

## Gemini Notebook Is the One That Stays Inside Your Sources

This is the surface most often answered wrongly, and the reason is that it looks like the weakest option on the list.

Gemini Notebook takes files you upload and acts as a research assistant over them: summarising key points, answering questions, generating ideas, **and staying grounded in the material you gave it**.<sup>[2]</sup> It will also produce an audio summary of them.

That last property is the entire point and it is what the exam tests. When a scenario says the answers must come from a specific set of documents, and must be traceable back to them, no general chat surface satisfies it. A general assistant answers from everything it knows. Gemini Notebook answers from what you handed it, and says where in the sources the answer came from, which is what lets the humans reading the output check it rather than trust it.

So the cue is not "documents". It is **these documents, and point to the line that says it**.

## Gemini Enterprise Is the Answer to Silos

When the problem is that the company's knowledge is scattered across systems that were never meant to talk, the answer is Gemini Enterprise. It brings customised search and conversational agents over data from various internal sources, and surfaces them in internal sites and dashboards.<sup>[2]</sup>

Its structure is worth one paragraph because it explains what the product actually is. You connect **data sources**, which become **data stores**; an **app** sits over one or more of those and serves search results, answers, actions and agents to the people using it. When several data stores feed one app, that is blended search.<sup>[3]</sup>

Which produces the business benefits the exam asks about, and they are about people rather than infrastructure: knowledge gets shared across systems that previously hid it from each other, employees stop re-finding things, and routine research and data entry can be handed to an agent.

One capability gets named separately in the blueprint and is worth holding as its own answer: **multimodal search**, meaning a single search that spans more than one type of data rather than one search per format.<sup>[1]</sup> When a scenario describes needing to find across text, images and video together, that is the term being tested.

The blueprint asks for the business value of this one and not only its name, so hold the value as well.<sup>[1]</sup> It lands on the person doing the searching: they find material they could not have described in words, in formats they would otherwise have had to search one at a time, which turns a set of disconnected repositories into something a person can actually ask a question of. Every benefit further downstream, the hours saved and the decisions made better, follows from that one. An option that pays somebody else, the storage bill or the administrator or the catalogue team, is answering a question about a different capability.

## Picking Between Them in One Question

**Ask where the work already lives.** Not what the task is, where it happens.

| The scenario | The surface |
|---|---|
| In a chat window, general writing help | Gemini app |
| The same, but repeated in a fixed format | A Gem in Gemini Advanced |
| In Gmail, Docs, Slides or Meet | Gemini for Google Workspace |
| In the cloud console, or in code | Gemini for Google Cloud |
| Across internal systems that do not connect | Gemini Enterprise |
| Inside a specific uploaded set of files, with citations | Gemini Notebook |
| Needing a video assembled for internal communication | Google Vids, in Workspace<sup>[4]</sup> |

That last row is not on the blueprint and is worth one line of recognition: Workspace includes a video tool that assembles a branded video with an avatar and voiceover, and it has turned up as the answer to a "we need a short video" scenario.

## How Wrong Answers Are Built on This Material

Every option here is a real Google product that genuinely helps with something. There is no implausible answer to discard, so these questions reward one specific discipline: locating the work before evaluating the tools.

- **The general-assistant answer.** The Gemini app, or Gemini Advanced, offered where the requirement is grounding in specific sources. It is a true statement about a capable product and it fails the stated requirement, because a general assistant draws on everything rather than on your forty files.
- **The wrong-venue answer.** The right capability in the wrong place. Help with code is Gemini for Google Cloud, not Workspace. Help with a slide deck is Workspace, not the console.
- **The build-it answer.** It proposes constructing a custom search application where Gemini Enterprise already does unified internal search with prebuilt agents. The scenario usually signals this by naming several disconnected systems, which is the product's purpose rather than a project brief.
- **The back-office-benefit answer.** On benefit questions, it names internal efficiency where the scenario describes a customer-facing capability. A richer search experience for shoppers improves engagement and discovery; it is not a cost saving in operations.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Says answers must come from these specific files | Gemini Notebook | A general assistant, described accurately |
| Describes the same output repeatedly, same format | A Gem | Writing a longer prompt, or a custom build |
| Names several disconnected internal systems | Gemini Enterprise | Building a search application |
| Puts the work inside mail, documents or meetings | Gemini for Google Workspace | The standalone Gemini app |
| Puts the work in the console or in code | Gemini for Google Cloud | Workspace, because the person is an employee |
| Asks for the benefit of a customer-facing search | Engagement and discovery | Internal efficiency or cost reduction |

The habit is to name the venue before naming the product, because the venue is stated in the scenario and the product never is.

## What to Remember

- **Ask where the work already lives**, not what the task is. The venue picks the product.
- **Gemini app** is the **chat window**: writing, summarising, translating, images. **Gemini Advanced** adds capability, **enterprise-grade protections**, and **Gems**.
- **A Gem is saved instructions** making responses consistent, for work that is **repeated in a fixed shape**. **Saved info stores facts** about you instead.
- **Gemini for Google Workspace** is inside **Gmail, Docs, Slides and Meet**. **Gemini for Google Cloud** is for **code, cloud management, data and security posture**.
- **Gemini Notebook stays grounded in the files you upload** and points back to them. The cue is **"these documents, and point to the line"**.
- **Gemini Enterprise answers silos**: **unified search and agents over scattered internal sources**. Structure: **data sources become data stores; an app serves search, answers, actions and agents**.
- **Multimodal search means one search across several data types**, not one search per format. Its value lands on **the person searching**: they **find what they could not have described**, across formats, in one query.
- **A general assistant cannot satisfy a grounding requirement.** It answers from everything it knows, which is the opposite of the requirement.
- **On customer-facing benefit questions, the benefit is customer-facing**: **engagement and discovery**, not back-office savings.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Gemini Enterprise concepts. https://docs.cloud.google.com/gemini/enterprise/docs/concepts
4. How to create professional work videos with AI avatars in Google Vids. https://workspace.google.com/blog/ai-and-machine-learning/how-to-create-professional-work-videos-with-ai-avatars-in-google-vids
