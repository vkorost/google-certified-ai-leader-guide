# Chapter 19: Needs Before Tools: Nine Questions to Ask First

**Summary:** *This objective has the weakest coverage of anything on the exam and the most judgement in it, which is an awkward combination. Google's position is consistent and simple: the first thing you establish is the business problem and the outcome that would count as solving it, and everything technical comes after. The exam tests that order directly, and it tests the nine questions Google says to ask before starting. Candidates who skip to the technology lose these questions by answering competently.*

## The Meeting That Starts in the Wrong Place

You are in the room where a gen AI initiative gets decided. Somebody has brought a shortlist.

The shortlist compares model families. It has a column for context window, one for cost per request, one for which clouds each option runs on. It is a good piece of work and it took somebody a week.

Nobody in the room can say, in one sentence, what problem this is for.

**Needs before tools** is the whole of this chapter, and the exam is unusually direct about it. When a scenario asks what to settle *first* for a gen AI use case to succeed, the answer names two things: which business problems this is meant to solve, and what outcome would count as having solved them.<sup>[1]</sup><sup>[2]</sup> Not the models available. Not which platforms have the newest features. Not how many people will need training.

Those three are real considerations and all three are distractors on this question. *A shortlist is not a decision.*

## The Nine Questions

Google names two kinds of thing that influence what a gen AI solution needs to be: **business requirements** and **technical constraints**.<sup>[1]</sup> The nine questions below are how those two become answerable. Six are about what the thing has to be, and three are about what you have to build it with.<sup>[2]</sup>

| Question | What it decides |
|---|---|
| **Scale** | How many people will use it, which bears on cost and architecture |
| **Customization** | How specialised this has to be, which picks a rung on chapter 11's ladder |
| **User interaction** | How people will engage with it, which shapes the surface |
| **Privacy** | How sensitive the data is, which constrains where it can go |
| **Latency** | What response time is acceptable, which can rule out remote inference |
| **Connectivity** | What network you can count on, which can force the work to the edge |
| **People** | Whether you have access to AI expertise at all |
| **Money** | What the budget is |
| **Time** | What the timelines are |

Four of those nine appear in no question in circulation, and they are the four most likely to decide a real project: user interaction, connectivity, people and time. The exam's silence is not evidence they do not matter.

Two deserve a note because they get confused with their neighbours.

**Latency is not throughput.** Latency is how long one response takes. Throughput is how many responses you can produce at once. A scenario about a translation app that must feel instant to the person holding the phone is a latency requirement, and an option about handling many simultaneous requests is answering a different question.

**Connectivity and latency often point the same way** but for different reasons: poor connectivity forces work onto the device because the network cannot be relied on, while tight latency forces it there because the round trip is too slow. Both lead to chapter 13's edge answers.

## What Shape of Solution the Problem Wants

Once the problem is named, the kinds of gen AI solution are a short list, and Google names them: text generation, image generation, code generation, video generation, data analysis, and a **personalized user experience** built around what one person needs.<sup>[1]</sup>

Most scenarios map onto one of those immediately. The ones worth rehearsing are the two where candidates reach past the obvious answer.

**Code generation** means suggesting snippets and completing functions for somebody who is writing code. When a team wants to build faster, that is the answer, and it is more useful than it sounds because it also covers generating the tests. The benefit of generated unit tests is **less manual validation effort**, and that phrasing matters: generated tests do not guarantee correct code, do not remove the need for review, and do not simplify the code they test.<sup>[3]</sup>

**Personalised user needs** is the shape to reach for when a scenario describes something doing several things for one person across time: assessing where they are, recommending what comes next, producing material for them, and tracking how they progress. That combination is not a recommendation engine and not a content generator. It is an agent, because only an agent covers all four together.<sup>[1]</sup>

## Where Gen AI Belongs, and Where It Assists

Google draws a line that this exam tests from both sides.

**Automate** work that is repetitive and rule-governed.<sup>[4]</sup> Chapter 2 covered this.

**Augment** work that needs critical thinking, creativity or strategic judgement. The examinable claim is that gen AI belongs in that work as a contributor to open-ended thinking, analysis and content creation, rather than being kept out of it.<sup>[1]</sup>

Those two look contradictory and are not. The distinction is who holds the decision. Automating a repetitive task means nobody looks at each instance. Augmenting a strategic task means a human is still deciding, with better material in front of them.

Which produces the shape of a right answer on responsible-use questions. When a function asks how to use gen AI to work faster, the answer that wins is usually **assistive**: drafting the communication, surfacing the insight, preparing the material for a person who then does their job. The answers that lose either hand the judgement over, move sensitive data somewhere it should not go, or replace a working system that nobody asked to replace.<sup>[1]</sup><sup>[2]</sup>

## How Wrong Answers Are Built on This Material

This objective has almost no product documentation behind it, which means its questions are about Google's published position rather than about how anything works. The distractors are competent, plausible, and in the wrong order.

- **The technology-first answer.** Available models, platform features, cloud options, or how many people need training, offered where the question asked what to establish first. Every one is a real consideration arriving before the problem has been named.
- **The throughput-for-latency answer.** Capacity where the scenario specified speed of a single response.
- **The nearest-shape answer.** A recommendation system or a content generator where the scenario described something that assesses, recommends, generates and tracks. Each covers one quarter of the requirement.
- **The over-claiming benefit answer.** On benefit questions, an option promising a guarantee, or the removal of human review. Generated output never guarantees anything and never removes the review.
- **The hand-it-over answer.** Automating the judgement where the scenario asked how to support the humans doing it.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Asks what to settle first | The business problems, and the outcome wanted | Models, platforms, or training headcount |
| Needs a single response to feel instant | Latency | Throughput, or simultaneous capacity |
| Names unreliable network or on-device work | Connectivity, pointing at the edge | A more capable hosted model |
| Describes assessing, recommending, generating, tracking | An agent | A recommendation engine, or a tuned model |
| Wants a team to write code faster | Suggesting snippets and completing functions | Generating the whole application |
| Asks the benefit of generated tests | Less manual validation effort | A guarantee of correct code |
| Asks how a function should use gen AI responsibly | Assistive drafting and insight | Replacing the system, or automating the judgement |

The habit: before reading the options, say what the problem is and what would count as solving it. If you cannot, the answer is the option that says the same thing.

## What to Remember

- **Needs before tools.** Asked what to settle **first**, the answer names **the business problems** and **the outcome that would count as solving them**. Models and platforms come after.
- **Nine questions before starting**: **scale, customization, user interaction, privacy, latency, connectivity**, and the resources, **people, money, time**.
- **Four of the nine are tested by nothing**: **user interaction, connectivity, people and time**. They are still the ones most likely to decide a real project.
- **Latency is one response; throughput is many at once.** A requirement that something **feel instant** is latency.
- **Poor connectivity and tight latency both point to the edge**, for different reasons: **the network cannot be trusted** against **the round trip is too slow**.
- **Six solution shapes**: **text, image, code and video generation, data analysis, and personalised user needs**.
- **Code generation means suggesting snippets and completing functions**, and it covers **generating tests**. The benefit of generated tests is **less manual validation effort**, never **a guarantee**.
- **Assess, recommend, generate and track together is an agent.** A recommendation engine covers **one quarter** of it.
- **Automate the repetitive; augment the strategic.** The difference is **who still holds the decision**.
- **On responsible-use questions the winning answer is assistive**: **draft it, surface it, prepare it** for a person who then decides.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. When to keep generative AI adoption simple. https://cloud.google.com/blog/transform/prompt-when-keep-generative-ai-adoption-simple
4. When to use generative AI or traditional AI. https://docs.cloud.google.com/docs/ai-ml/generative-ai/generative-ai-or-traditional-ai
