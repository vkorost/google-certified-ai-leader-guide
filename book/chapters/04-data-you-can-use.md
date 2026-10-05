# Chapter 4: Data You Can Use Is Not the Same as Data You Have

**Summary:** *This is the smallest objective in the first section and it carries two distinctions the exam returns to: structured against unstructured, and labelled against unlabelled. They are not the same distinction, and candidates who treat them as one lose questions on both. Underneath sits a quieter idea worth more than either, which is that data can be abundant, clean, and still useless for the thing you are trying to do. Knowing which quality is missing is the whole of this material.*

## A Dataset That Is 99% Complete and Entirely Wrong

Suppose a team reports that the training data for a new drafting assistant is 99% complete, consistent in format, and freshly validated. Those are three real quality properties and all three are satisfied.

The assistant then writes in the wrong voice for the company, every time, and no amount of further training fixes it.

Nothing in that report was false. The data was complete, consistent and clean. It was drawn from a decade of internal technical documentation, and what the company wanted was its public brand voice, which appears nowhere in it. The missing property was never completeness.

**It was relevance**, and relevance is the quality characteristic that an audit of the dataset cannot detect, because the dataset is not where the defect lives. The defect is in the relationship between the data and the goal.

## Quality Is a Short List, and the Exam Expects the Whole List

Google describes quality data as accurate, complete, consistent and relevant.<sup>[2]</sup> The blueprint widens it, adding the practical properties that decide whether data can be used at all: availability, cost and format.<sup>[1]</sup>

| Characteristic | The question it answers | What its absence looks like |
|---|---|---|
| Accuracy | Does it reflect reality? | Values that are simply wrong |
| Completeness | Is any of it missing? | Empty fields, absent records, gaps in time |
| Consistency | Does it agree with itself? | The same customer recorded three ways |
| Relevance | Does it bear on *this* goal? | A clean dataset about the wrong thing |
| Availability | Can you get at it? | It exists, in a system nobody can query |
| Cost | Can you afford to get at it? | Licensed, metered or expensive to move |
| Format | Can the model consume it? | Scanned paper, a proprietary export |

Relevance is the one that carries most of the exam's weight on this objective, because it is the only one that cannot be judged by looking at the data on its own. The other six are properties of the dataset. Relevance is a property of the match.

## Accessible Data Is a Separate Requirement From Good Data

Google treats accessibility as its own idea: data for training has to be readily available, usable, and in a form that can be consumed.<sup>[2]</sup>

Call it **reachable data**. A warehouse holding exactly the right records, in a system that cannot export them, behind a team with no capacity to help, is not an asset for this project. It is a description of an asset.

No question in circulation tests accessibility directly, which is precisely why it is worth holding in mind: it is blueprint surface with nothing to remind you it exists. The business form of it is familiar enough. The data you own, the data you can reach, and the data you can reach in time for the thing you promised are three different quantities, and leaders routinely plan against the first.

## Structured and Unstructured Is About Shape

**Structured data** is organised and easy to search, and lives in things like relational tables.<sup>[2]</sup> Rows, columns, a schema agreed in advance, a query language that works.

**Unstructured data** has no predefined shape and needs more sophisticated handling to get anything out of it.<sup>[2]</sup> Prose, email bodies, photographs, audio recordings, video, scanned documents.

| Example | Which | Why |
|---|---|---|
| A sales table with date, amount, region | Structured | Fixed columns, known types |
| Free-text customer complaints | Unstructured | No schema; the meaning is in the prose |
| Product photographs | Unstructured | Pixels, with no fields |
| Call recordings | Unstructured | Audio, until something transcribes it |
| A transcript in a database column | Structured container, unstructured content | The row is structured; the paragraph inside is not |

That last row is where the exam likes to sit. Putting unstructured content into a structured store does not make it structured. The test is whether the *meaning* is held in defined fields or in free-form content.

## Labelled and Unlabelled Is About Annotation

**Labelled data** carries a tag saying what the example is: a name, a type, a number. Somebody put it there, and on most datasets that somebody was a team of humans working through the records one at a time.<sup>[2]</sup> **Unlabelled data** is raw and untagged, carrying no meaning that a model can learn a target from on its own: a folder of unsorted photographs, a stream of recordings.<sup>[2]</sup>

Now the point of this chapter, which is that shape and annotation are independent. Four combinations exist and all four are ordinary:

| | Labelled | Unlabelled |
|---|---|---|
| **Structured** | A sales table with a churned-or-not column | A sales table with no outcome recorded |
| **Unstructured** | Photographs, each tagged with its product | A folder of photographs nobody has sorted |

**The shape-is-annotation answer** is the trap this builds, and it runs in both directions. An option treating unstructured data as automatically unlabelled is wrong, because tagged images are both. An option treating structured data as automatically labelled is wrong too, and it is the more expensive error, because it is the one that makes a supervised project look ready when it is not. *A schema is not an answer key.*

There is one fact to carry out of here into section 3. Foundation models are trained on enormous quantities of **unlabelled** data, which is what gives them their breadth.<sup>[2]</sup> So the instinct that unlabelled data is the inferior kind is wrong at the scale that matters most in this field.

## How Wrong Answers Are Built on This Material

The distractors on this objective are mostly other members of the same list. Every option names a real data property, and only one of them is the property the scenario is short of. That means the work is diagnosis rather than recall.

- **The visible-defect answer.** It names whatever flaw the scenario mentions in passing, usually completeness or consistency, when the scenario has already told you that the data is clean. If the stem goes out of its way to say the data is accurate and complete, it is eliminating those options for you and pointing at relevance.
- **The shape-is-annotation answer.** Structured read as labelled, or unstructured read as unlabelled. Two distinctions collapsed into one.
- **The container answer.** It classifies data by where it is stored rather than by what it is. A paragraph in a database column is still unstructured content.
- **The volume answer.** It treats having a great deal of data as having good data. Quantity appears nowhere in the quality list.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| States the data is clean, complete and still fails | Relevance | Completeness or accuracy, named in passing |
| Describes free-form prose, images, audio or video | Unstructured | Structured, because it sits in a database |
| Describes tagged or categorised examples | Labelled | Unstructured, treated as a synonym for unlabelled |
| Describes data nobody can export or query in time | An availability or format problem | A quality problem in the data itself |
| Boasts about dataset size | Size is not on the list | Treating volume as quality |

The habit: when a scenario describes a failure, ask what the data would need to have *instead*, not what is wrong with it. That phrasing finds relevance, which the other phrasing never does.

## What to Remember

- **Seven quality characteristics**: **accuracy, completeness, consistency, relevance**, plus the practical three, **availability, cost and format**.
- **Relevance is the only one you cannot see by inspecting the data.** The other six are properties of the dataset; **relevance is a property of the match** between the data and the goal.
- **A stem that says the data is clean and complete is eliminating options for you.** It is pointing at **relevance**.
- **Reachable data**: data for training has to be **available, usable and in a consumable format**. Owning it, reaching it, and reaching it **in time** are three different things.
- **Structured means a predefined schema** and easy searching. **Unstructured means no predefined shape**: prose, images, audio, video.
- **Labelled means carrying a tag** that says what the example is. **Unlabelled** means **raw and untagged**.
- **Shape and annotation are independent.** All four combinations exist, so **structured is not labelled** and **unstructured is not unlabelled**.
- **A paragraph inside a database column is unstructured content** in a structured container. Classify by **where the meaning sits**, not where the bytes sit.
- **Foundation models are trained on unlabelled data at enormous scale.** Unlabelled is not the inferior kind.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
