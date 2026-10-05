# Chapter 10: Customer Experience: Who Is Helped, and When

**Summary:** *Google's customer-experience products divide along two lines, and once you see them the questions on this objective answer themselves. The first line is who is being helped: the customer, or the human agent serving the customer. The second is when: during the conversation, or after it. Four products, two questions, and almost every item on this objective is decided by one of them. This is the most mechanical objective in section 2 and it is worth the ten minutes.*

## Four Products, and the Two Questions That Separate Them

A contact centre comes to you with four complaints in one meeting. Customers wait too long for simple answers. The agents who take the hard calls have to look everything up by hand. Nobody knows why the satisfaction scores dropped last quarter. And the whole telephony estate is ageing and needs replacing anyway.

Those are four products. Here they are, arranged by the only two questions that matter:

| | During the conversation | After the conversation |
|---|---|---|
| **Helping the customer directly** | Conversational Agents | |
| **Helping the person serving them** | Agent Assist | Conversational Insights |

And underneath all three, the platform the whole operation runs on: **Contact Center as a Service**, Google's cloud-native contact centre.<sup>[2]</sup>

**The handoff boundary** is the idea to carry out of this chapter. Every one of these products is defined by where it sits relative to the moment a conversation passes from software to a human, and the exam tests that boundary more than it tests any product's feature list.

## Conversational Agents Talk to the Customer

A conversational agent is the customer-facing virtual agent: it holds the conversation, handles what it can, and escalates to a human when it cannot.<sup>[4]</sup>

The cue is that the **customer** is on the other end. Self-service, deflection, answering routine questions without a person, available outside working hours. And the escalation path matters: a scenario that mentions handing difficult cases to a human is describing a conversational agent working properly rather than a limitation.

Naming, because it is genuinely confusing here. These were **Dialogflow CX** and are also referred to as Vertex AI Agents in older material. Dialogflow CX still has current documentation and was not retired, so an option naming it is not wrong for being old.<sup>[5]</sup>

## Agent Assist Helps the Human, While the Call Is Live

Agent Assist supports the **live agent** in real time, suggesting responses and surfacing the information they would otherwise go looking for.<sup>[3]</sup>

The distinction from a conversational agent is the whole point, and it is clean. A conversational agent takes the calls it can handle instead of a person. Agent Assist never speaks to the customer at all; it speaks to whoever is speaking to the customer.

So the scenario cue is a person doing the talking and needing help doing it: recommended replies, relevant knowledge, real-time suggestions during an interaction. A contact centre that wants to keep its people on the phone and make them faster is describing Agent Assist, and an option offering to automate those conversations instead is answering a question that was not asked.

## Conversational Insights Looks Backwards

Conversational Insights analyses conversational data that has already happened, across both bot and human interactions, to find topics, sentiment and trends.<sup>[3]</sup>

The cue is **past tense**. Why did scores drop. What are customers calling about. Which issues recur. Where agents struggle. The analysis is of completed conversations, which is what separates it from Agent Assist in every question that offers both.

| The scenario asks | Product | The tense |
|---|---|---|
| Answer routine customer questions without a person | Conversational Agents | Present, customer-facing |
| Suggest replies to the agent mid-call | Agent Assist | Present, agent-facing |
| Find out what customers have been calling about | Conversational Insights | Past |
| Replace the telephony and run the whole centre | Contact Center as a Service | All of it |

## Contact Center as a Service Is the Platform, Not a Feature

CCaaS is the enterprise-grade, cloud-native contact centre platform, and the customer-experience tooling is built on top of it.<sup>[2]</sup><sup>[6]</sup>

The cue is **scope**. When the scenario asks for the whole thing in one package, telephony and routing and interactive voice response and virtual agents and agent assistance together, that package is CCaaS. When the scenario asks for one capability, it is one of the three products above.

**The platform-for-a-feature answer** is the trap in both directions. Offering CCaaS where the scenario wants only post-call analysis is oversized. Offering a single product where the scenario wants the whole estate replaced is undersized. The question to ask is how many of the four complaints the scenario is making.

## Agent Search Is for Your Own Content, Not for Your Call Centre

One more product sits in this objective and it is easy to misfile, because it is about search rather than conversation.

**Agent Search**, previously Vertex AI Search, provides search and recommendation over your own business content.<sup>[2]</sup> A company that wants its website visitors to search its catalogue, documentation and knowledge base and get good answers is describing Agent Search.

The contrast the blueprint draws is between that and **Google Search**: one searches your content, the other searches the world.<sup>[1]</sup> That distinction returns in chapter 16, where it becomes a question about grounding, because what a model is allowed to retrieve from is the same decision seen from the other side.

## The Two Google Documents Disagree About These Names

Worth knowing before you meet it, because it will look like you have misremembered something.

The exam guide names the suite **Customer Engagement Suite**, with Conversational Agents, Agent Assist, Conversational Insights and Contact Center as a Service inside it.<sup>[1]</sup> The study guide calls the same area **Gemini Enterprise for Customer Experience**, and names its pieces Customer Experience Agent Studio, Agent Assist and Customer Experience Insights.<sup>[2]</sup>

Those are Google's own two documents, published for the same exam, naming the same products differently. The rebrand is mid-flight and the documentation says so in places.<sup>[5]</sup> *The disagreement is not yours to resolve.* Learn the functions and recognise both labels: the thing that talks to customers, the thing that helps the agent, the thing that analyses afterwards, the platform underneath.

## How Wrong Answers Are Built on This Material

The distractors here are the other three products in the suite, and each one is a correct description of something in the same room. Reading the product names and matching the one you recognise is exactly the behaviour these items are built to punish.

- **The wrong-beneficiary answer.** A customer-facing product where the agent needed the help, or the reverse. This is the single most common error on the objective, because both options involve a conversation and both improve the same metric.
- **The wrong-tense answer.** Agent Assist where the scenario is about analysing conversations that already happened, or Insights where the need is live help. The giveaway is in the verb: *are* calling against *have been* calling.
- **The platform-for-a-feature answer.** CCaaS offered for a single capability, or a single product offered where the whole estate is being replaced.
- **The misfiled-search answer.** Agent Search offered for a contact centre problem, or a contact centre product offered for a website search problem.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Says customers get answers without a person | Conversational Agents | Agent Assist, which never talks to customers |
| Says live agents need suggestions now | Agent Assist | Conversational Agents, which would replace them |
| Asks what customers have been contacting about | Conversational Insights | Agent Assist, because both help agents |
| Lists telephony, routing, virtual agents and assistance | Contact Center as a Service | One component of it |
| Describes searching the company's own catalogue | Agent Search | A contact centre product |
| Mentions escalating hard cases to a human | Conversational Agents, working correctly | Treating escalation as a failure of the product |

The habit: before reading the options, answer two questions in four words. Who is helped, and when. Customer or agent, during or after.

## What to Remember

- **Two questions decide this objective**: **who is being helped**, the customer or the agent serving them, and **when**, during the conversation or after it.
- **Conversational Agents** are **customer-facing** virtual agents that handle what they can and **escalate to a human**. Escalation is **correct behaviour**, not a shortcoming.
- **Agent Assist helps the live agent in real time** with suggested responses and surfaced knowledge. It **never speaks to the customer**.
- **Conversational Insights is past tense**: analysing **completed conversations**, bot and human, for **topics, sentiment and trends**.
- **Contact Center as a Service is the platform**: **telephony, routing, IVR, virtual agents and agent assistance** in one cloud-native package. The cue is **scope**.
- **Agent Search, formerly Vertex AI Search, searches your own content.** **Google Search** searches **the world**. That pairing returns as a grounding question.
- **Google's two documents name these products differently.** Exam guide: **Customer Engagement Suite**. Study guide: **Gemini Enterprise for Customer Experience**. **Learn the functions**, and **recognise both labels**.
- **Dialogflow CX was not retired** and still has current documentation, so an option naming it is **not wrong for sounding dated**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Agent Assist documentation. https://docs.cloud.google.com/agent-assist/docs
4. Conversational AI documentation. https://docs.cloud.google.com/conversational-ai/docs
5. Dialogflow CX documentation. https://docs.cloud.google.com/dialogflow/cx/docs
6. Contact Center AI Platform documentation. https://docs.cloud.google.com/contact-center/ccai-platform/docs
