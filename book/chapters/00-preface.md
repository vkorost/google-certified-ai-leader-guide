# Preface

This book prepares you for Google Cloud's Generative AI Leader exam, and it is arranged in the order the decisions arrive rather than in the order Google lists them.

That choice needs justifying, because the published exam guide is right there and following it would have been easier.

Google divides the exam into four sections and fifteen objectives. The division is sound as a specification and poor as a teaching order, because several single decisions are split across it. The word *agent* appears under eight of the fifteen objectives. Grounding is taught once as a product, under Google Cloud's offerings, and again as a technique, under improving model output. Choosing a model is partly in section 1, where the criteria live, and partly in section 4, where the business need does. A reader working through the blueprint in order meets a third of the agent decision three times and the whole of it never.

So the twenty-two chapters here follow a different sequence: what this technology is, what you are choosing between, what Google sells, how to make the output better, and how to lead the thing. Each chapter settles one decision and says what it costs to get wrong. The coverage map at the back shows which chapters own which objectives, and every objective has at least one.

## What this is built from

Three sources, and nothing else.

Google's own two documents for this certification, the exam guide and the study guide, which are the only authority on what is testable. Google Cloud's product documentation, which is where the products are actually described. And Google's own non-product writing, where the first two are silent.

Every claim about a product comes from one of those, cited by its own URL at the end of each chapter. Where none of them settles a question, this book says so rather than filling the gap, because the alternative is a confident answer with nothing behind it.

**There are no questions in this book.** It is a guide, and a reader who finishes it should be able to answer things they have never seen rather than recognise things they have.

## One disclosure

This book was written by software. Specifically, by a language model working from the documents named above, under direction from a human editor who set its constraints, chose its structure and rejected several versions of it.

That is worth one paragraph and no more. The narrator has no career to draw on, no customers, and no war stories, which is why you will not find an anecdote anywhere in it. What it has is the documentation, read closely. Where you would expect a scene from somebody's working life, you will find a situation described in the second person instead: a meeting you are in, a decision you are holding. Those situations are hypothetical and are meant to be recognisably so. No company, customer, figure or incident in this book is real, because inventing one would have been easier than checking it.

## The names changed in April 2026

At Cloud Next 2026 Google renamed most of the surface this exam covers. Vertex AI became Gemini Enterprise Agent Platform, usually shortened to Agent Platform. Vertex AI Search became Agent Search, Vertex AI Studio became Agent Studio, Agentspace became Gemini Enterprise, and NotebookLM became Gemini Notebook.

The exam guide uses the new names. A great deal of material still in circulation uses the old ones, and Google's own documentation is mid-transition: the Dialogflow CX pages currently open by noting that some products and features are being renamed.

**This book carries both names**, as `Vertex AI Search (now Agent Search)` on first use in a chapter, and the current name after that. Nobody outside Google knows whether the exam's own questions were rewritten with the rebrand, and a guide that bet on one answer would be wrong half the time if it bet wrong. Two products that sound like they belong to the retired generation were not renamed at all, Dialogflow CX and Contact Center AI, and a familiar old name is not evidence of a wrong answer.

## The exam itself

Google publishes the particulars on its certification page: ninety minutes, fifty to sixty multiple-choice questions, ninety-nine dollars plus tax, valid for three years, no prerequisites, delivered either online-proctored or at a test centre, in English, Japanese, Spanish and Portuguese.<sup>[1]</sup>

The four sections carry roughly 30%, 35%, 20% and 15% of the exam. Google publishes no weight for any individual objective, so this book does not estimate one, and you should treat every objective inside a section as capable of carrying a question.

## How to read it

Straight through, if you have the time. The chapters build: the five layers in chapter 5 are the map the whole of section 2 hangs off, and the ground-tune-or-train ladder in chapter 11 settles questions that recur in chapters 14 through 17.

If you are revising, use the coverage map to find the chapter for an objective you are weak on, and read its closing section first. Every chapter ends with two blocks worth more than their length: one on how wrong answers are built on that material, and one of compact rules that are meant to survive with the book closed.

A word about proportion. Sections 3 and 4 are 35% of the exam and get more than a third of the chapters, which is deliberate. Google documents its products thoroughly and its judgement sparsely. For sections 1 and 2 you can always go and read the documentation. For the half of this exam about choosing, leading, securing and taking responsibility, there is much less to go and read, and that is where a guide earns its keep.

## Endnotes for this chapter

1. Generative AI Leader certification. https://cloud.google.com/learn/certification/generative-ai-leader
