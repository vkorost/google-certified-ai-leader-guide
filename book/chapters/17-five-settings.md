# Chapter 17: Five Settings That Change the Output, Not the Model

**Summary:** *Five sampling settings sit between a model and its output, and the exam tests them by describing an unsatisfactory response and asking which one to adjust. The whole objective rests on knowing precisely what each setting touches, because the distractors are the other four and all of them are real. The expensive mistake runs the other way too: reaching for a setting when the scenario described a problem no setting can reach.*

## Two Complaints, One Model, Only One of Them Is a Setting

A team brings two complaints about the same assistant.

The first: the answers wander. Different phrasing each time, occasional odd word choices, nothing you could call wrong but nothing you could rely on either.

The second: the answers are sometimes factually invented.

The first complaint is a setting, and a single one at that. The second is not a setting at all, and no amount of adjustment will touch it, because nothing in this chapter has any opinion about whether a sentence is true. That boundary is the most valuable thing here, and the exam tests both halves of it.

## Dials, Not Training

**Dials, not training** is the frame. Google groups these under **sampling parameters**: settings that influence how the model behaves, letting you shape the result without changing the model at all.<sup>[1]</sup><sup>[2]</sup> Learn the umbrella term as well as the five under it, because a question can ask which sampling parameter to adjust and expect you to know that the phrase means these and nothing else.

| Setting | What it controls | Turn to it when |
|---|---|---|
| **Token count** | Meaningful chunks of text, which is how length and capacity get measured<sup>[2]</sup> | You need to reason about how much text is involved, or what it costs |
| **Temperature** | How adventurous the model's word choices are; its creativity, or its randomness<sup>[2]</sup> | Output is too varied and you want it focused, or too flat and you want range |
| **Top-p** | Also called nucleus sampling. It bounds the pool of candidate tokens by accumulated probability<sup>[2]</sup> | The same purpose as temperature, by a different route |
| **Safety settings** | Screening the output for harmful or inappropriate material<sup>[2]</sup> | The concern is harm rather than error |
| **Output length** | The maximum length of what gets generated<sup>[2]</sup> | Responses are too long, or inconsistently long |

Five of them, and the first thing worth noticing is that **two do the same job as each other**. Temperature and top-p are both ways of controlling randomness. When a question asks which setting to lower for more deterministic, focused output, the expected answer is temperature, because that is the one Google describes as governing creativity and randomness directly.

## Output Length Is the Answer More Often Than It Looks

This setting carries more exam weight than its simplicity suggests, and it is worth understanding why.

Output length caps how much the model produces.<sup>[2]</sup> So it is the answer when responses are too long. It is also the answer, less obviously, when responses are **inconsistently** long: a cap makes every response fit inside the same bound, which is a crude but real kind of consistency.

That second case produces a question shape worth being ready for, and the humans who wrote it did not play entirely fair. A scenario can complain that descriptions are sometimes too short and sometimes too long, and then offer four options of which only one is a parameter at all. A maximum length cap only addresses the second half of the complaint. It is still the answer, because the question asked which **parameter** to adjust and the others on offer are not parameters.

**The not-a-parameter answer** is the trap in that shape, and it is usually a prompting technique: few-shot prompting, role prompting, something from chapter 15. Those are genuinely better fixes for inconsistent output. They are not parameters, and when a question says parameter it means one of these five.

## Safety Settings Filter Harm, Not Error

A clean distinction, tested directly.

Safety settings screen the output for material that is harmful or inappropriate, at whatever strictness you set.<sup>[2]</sup> That is the whole scope. They do not detect falsehood, they do not improve accuracy, and they do not catch a confident invention.

So an option offering safety settings against hallucination is wrong, and it is wrong in the way that catches careful readers: both things sound like protecting the user from bad output. *Harmful and untrue are different categories.* One is about the nature of the content and the other is about its relationship to reality, and only grounding addresses the second.

## What No Setting Can Reach

Worth stating plainly, because half the marks on this objective come from questions where the answer is not a setting at all.

| The complaint | Not a setting. It is |
|---|---|
| Invented facts | Grounding, chapter 16 |
| Does not know recent events | Retrieval, chapter 16 |
| Wrong tone or persona | Role prompting, chapter 15 |
| Wrong format or structure | Few-shot prompting, chapter 15 |
| Misses nuance a person would catch | A review step, chapter 14 |
| Cannot hold the whole document | The context window, chapter 7 |

The last row deserves a note because the vocabulary invites the error. Token count and context window both measure text, and they are not the same thing. Context window is a property of the model, fixed before you choose it. Token count is how you measure what you are sending and what comes back.

## How Wrong Answers Are Built on This Material

Two shapes, and they run in opposite directions.

- **The wrong-setting answer.** One of the other four, each a real setting with a real purpose. The commonest pairing is a randomness setting offered where length was the issue, and the other common one is safety settings offered against inaccuracy.
- **The not-a-parameter answer.** A prompting technique offered where the question asked specifically which parameter to adjust. Often the better engineering advice, and still not an answer to the question asked.
- **The settings-for-everything answer.** The reverse case: a parameter offered where the problem is factuality, freshness, tone or format. If the complaint is about **truth or shape**, no dial reaches it.
- **The two-dials answer.** Top-p where temperature is wanted. Both control randomness, and temperature is the one Google frames as creativity, so it is the expected answer when a question asks for focused and deterministic output.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Wants focused, deterministic output | Lower the temperature | Top-p, which does a similar job |
| Complains responses are too long | Output length | Temperature, because output varies |
| Complains length is inconsistent | Output length | A prompting technique, which is not a parameter |
| Worries about harmful or inappropriate content | Safety settings | Grounding |
| Describes invented facts | Grounding, not a setting | Safety settings, or lower temperature |
| Asks which **parameter** to adjust | One of the five | The best fix, which may not be a parameter |
| Cannot fit the whole document | Context window, a model property | Token count, which measures rather than limits |

The habit: decide first whether the complaint is about **manner** or about **matter**. Manner, meaning length, variety and tone, is reachable by settings and prompts. Matter, meaning truth, currency and provenance, is not.

## What to Remember

- **Dials, not training.** These five **shape the output** without changing the model.
- **Five settings**: **token count**, **temperature**, **top-p**, **safety settings**, **output length**.
- **Temperature controls randomness and creativity.** For **focused, deterministic output, lower the temperature**: it is the expected answer even though **top-p does a similar job**.
- **Output length caps how much is produced.** It is the answer for **too long** and also for **inconsistently long**.
- **Safety settings screen for harmful or inappropriate material**, at a strictness you set. They do **not** detect falsehood: **harmful** and **untrue** are **different categories**.
- **Token count measures text in meaningful chunks.** It is **not the context window**, which is a **fixed property of the model**.
- **When a question says parameter, it means one of the five.** A prompting technique may be better advice and is still not a parameter.
- **No setting reaches truth, currency, provenance, tone or format.** Those are **grounding, retrieval, prompting and review**.
- **Decide whether the complaint is manner or matter.** **Manner** is reachable by **dials**; **matter** is not.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
