# Chapter 15: Prompting: Examples Are Instructions

**Summary:** *Google names eight prompting techniques and the exam tests them by describing a disappointing output and asking which technique fixes it. The techniques are not interchangeable and each one changes something different: how many examples the model has, who it is pretending to be, how many turns it gets, or whether it shows its working. Get the mapping right and this objective is nearly free. Get it wrong and you will reach for the same two techniques every time.*

## The Same Prompt, Twice

A marketing function asks for a product description and gets something bland, generic, and about three times too long.

The first instinct is that the model is not good enough. The second is that it needs training on the company's past descriptions. Both are wrong, and the fix is almost embarrassing: the prompt did not say who the description was for, what tone it should take, or which words had to appear in it.

Add those three things and the output changes completely. Nothing about the model changed. *The model answered the question it was asked.*

That is the first lesson of this objective and it is worth more than the taxonomy: a vague output is usually evidence of a vague prompt, and the remedy is a more specific prompt rather than a different model or a tuning run.

## Prompt Engineering, and the Thing It Is Not

Prompting is how you interact with a foundation model and steer it: you supply instructions or input, and it produces output.<sup>[2]</sup> Prompt engineering is the craft of building those inputs well, so the model's value is maximised and the responses suit the need.<sup>[2]</sup>

One adjacent term gets confused with it and the blueprint lists both, so learn the pair.<sup>[1]</sup> **Prompt engineering** changes what you send. **Prompt tuning** is a tuning technique, which means it adjusts the model side rather than the message side. If a question is about writing better instructions, it is engineering. If it is about adapting the model, it is tuning, and chapter 11's ladder applies.

## How Many Examples, and What That Buys

The first family is counted by examples, and the counting is the whole distinction.<sup>[2]</sup>

| Technique | What you give it | Reach for it when |
|---|---|---|
| **Zero-shot** | The task, no examples | The task is common and the output shape does not matter much |
| **One-shot** | The task plus a single example | There is a pattern to follow and one instance conveys it |
| **Few-shot** | The task plus several examples | The output has to match a shape, a format or a style consistently |

**Examples are instructions.** That is the idea to carry, and it explains why few-shot is the answer to a class of problem that looks like it needs something heavier. When a scenario says responses are inconsistent, badly shaped, or not in the expected form, showing the model several successful instances teaches it the pattern without touching the model at all.

So the cue for few-shot is **consistency and shape**. The cue for zero-shot is a scenario where no examples are available or needed.

## Who the Model Is Pretending to Be

**Role prompting** assigns a persona, and doing that influences the style, the tone and the focus of what comes back.<sup>[2]</sup>

This is the technique candidates most often skip, and it answers a very specific and very common requirement. When a scenario asks for a consistent voice, a professional manner, a particular expertise, or conduct that reflects how a certain kind of person would behave, assigning the role is the answer. Telling a model to respond as an experienced support representative who knows the company's policies does more for tone and conduct than a page of instructions about tone and conduct.

The discrimination that matters: **role prompting changes manner; few-shot changes shape.** A scenario about tone and consistency of voice is role. A scenario about format and structure is few-shot. Both are about consistency, and they are consistency of different things.

## More Than One Turn

**Prompt chaining** means carrying on the conversation, back and forth, so that context builds up rather than being restated.<sup>[2]</sup>

The cue is **context across turns**. A scenario where the assistant keeps losing track of what was said earlier, or where information has to be gathered in stages before anything useful can be produced, is a chaining scenario. It is also the technique behind a practical habit Google recommends: keeping a conversation going in one place so the context stays live.<sup>[2]</sup>

## Making the Reasoning Visible

Two advanced techniques are in the blueprint by name, and both are about the model's process rather than its output.<sup>[1]</sup>

**Chain-of-thought** guides the model through a problem by giving it examples that include the intermediate reasoning steps.<sup>[2]</sup> The defining feature, and the thing a question will describe, is that the prompt lays out the steps of the thinking rather than only the answer. When a scenario shows a prompt prescribing how to work something out, step by step, that is chain-of-thought.

**ReAct**, for reason and act, lets the model reason about a query and then take action on it.<sup>[2]</sup> The reason it sits in this chapter rather than chapter 12 is that it is a prompting pattern, and the reason it matters is that it is the pattern underneath agent behaviour: thinking and doing, alternating.

**Metaprompting** is the third, and no question in circulation tests it. It means using prompting to get the model to produce, modify or interpret other prompts.<sup>[2]</sup> Worth knowing by name for exactly that reason.

## The Habits Google Recommends Around Prompting

Three practical items, none of them tested, all of them blueprint surface.<sup>[2]</sup>

**Reusing prompts** means saving the ones that work as templates instead of rewriting them. **Saved info** in Gemini stores details you would otherwise repeat, so the model holds them consistently. And **Gems**, from chapter 9, package a whole set of instructions into a reusable assistant.

Those three are the same idea at three sizes: stop retyping the context. A leader's version of this is more useful than the exam's: the difference between an organisation where prompting works and one where it does not is usually whether good prompts are kept anywhere. Humans will rewrite a prompt from memory forty times rather than go looking for the one that worked.

## How Wrong Answers Are Built on This Material

The distractors are the other techniques, all real, all recommended by Google. Nothing is eliminable as nonsense, so the discipline is naming what the scenario says is wrong with the output.

- **The heavier-machinery answer.** Fine-tuning, or a different model, offered where a more specific prompt would do. The tell is a scenario complaining that output is generic, vague or off-target, which is a description of the prompt rather than the model.
- **The settings answer.** A sampling parameter offered where a technique was needed. Parameters change how adventurous the wording is, not whether the model understood the task.
- **The wrong-consistency answer.** Few-shot where the problem was tone, or role where the problem was format. Both techniques produce consistency, of different things.
- **The example-count answer.** Zero-shot or one-shot where the scenario stressed matching a shape reliably. If consistency across many outputs matters, several examples is the answer.
- **The chaining-for-everything answer.** Prompt chaining offered where nothing in the scenario is about multiple turns. Chaining fixes lost context, not quality.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Says output is vague or generic | Add specifics to the prompt | Fine-tuning, or a bigger model |
| Needs a consistent format or structure | Few-shot prompting | Role prompting, or a parameter |
| Needs a consistent tone, manner or expertise | Role prompting | Few-shot, because both mean consistency |
| Loses context between turns | Prompt chaining | A larger context window |
| Shows a prompt laying out reasoning steps | Chain-of-thought | Few-shot, because examples are present |
| Describes reasoning then acting on a query | ReAct | Chain-of-thought |
| Describes generating or rewriting prompts | Metaprompting | Prompt chaining |

The habit: say in one short phrase what is wrong with the output. Wrong shape. Wrong tone. Missing context. Too long. Each phrase maps to exactly one technique, and the phrase is nearly always in the scenario already.

## What to Remember

- **A vague output usually means a vague prompt.** The remedy is **a more specific prompt**, naming **audience, tone and required terms**, not a bigger model.
- **Prompt engineering** changes **what you send**; **prompt tuning** adjusts **the model**. The blueprint names both, and they sit at different layers.
- **Zero-shot is no examples, one-shot is one, few-shot is several.** **Examples are instructions**, so **few-shot answers inconsistency of shape and format**.
- **Role prompting assigns a persona** and changes **style, tone and focus**. It is the answer for **consistent voice, manner or expertise**.
- **Role changes manner; few-shot changes shape.** Both produce consistency, **of different things**.
- **Prompt chaining carries context across turns**, and is the answer when the assistant **loses track of what was said**.
- **Chain-of-thought supplies the intermediate reasoning steps** in the prompt. **ReAct is reason then act**, and it is the pattern under agent behaviour.
- **Metaprompting uses prompting to produce or modify other prompts.** Untested, and on the blueprint.
- **Reusing prompts, saved info and Gems are one idea at three sizes**: **stop retyping the context**.
- **Parameters are not techniques.** A sampling setting changes **how adventurous the wording is**, never **whether the task was understood**.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
