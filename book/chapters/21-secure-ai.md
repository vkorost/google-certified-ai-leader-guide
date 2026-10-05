# Chapter 21: Secure AI Is a Lifecycle Property, Not a Product

**Summary:** *Three Google security products appear on this objective and the questions matching them are nearly mechanical: who can do what is one product, what the overall posture looks like is another, and what Google builds in underneath is a third. The harder half asks where in the machine learning lifecycle security belongs, and the answer is always the whole of it. An option naming one stage is wrong however sensible that stage sounds.*

## Two Answers to "When Do We Do Security"

A healthcare provider is building a tool to summarise patient records, and asks when the privacy and security work happens.

One answer says: before launch, in review, where these things get checked. That is a real process, run by real humans who are good at it, and as an answer here it is wrong.

The other says: throughout, starting at the moment data is first collected. That is Google's position, and the reason it is the right answer is not diligence. It is that the earlier stages are where the irreversible decisions are made. Data that should never have been ingested is already ingested. A model trained on material it should not have seen cannot unsee it.<sup>[2]</sup>

**Security across the lifecycle** is the examinable claim, and on this objective it is the one that recurs.

## Secure AI, and the Framework Behind It

Secure AI means protecting the AI applications themselves from harm.<sup>[2]</sup> The blueprint names the concern precisely: malicious attack and misuse. That precision is what separates this objective from the next one, because chapter 22 is about harm the system causes and this one is about harm done to the system.

Google's **Secure AI Framework**, SAIF, exists to help organisations manage the risks of AI and machine learning models and keep them secure.<sup>[2]</sup> Underneath it, Google Cloud's **secure-by-design infrastructure** supports security across the whole AI and ML lifecycle, with tooling protecting the data, the models and the applications.<sup>[2]</sup>

Both SAIF and secure AI as a term are blueprint surface that no question in circulation tests. Know the names and what each covers, because the exam can ask and nothing else will remind you they exist.

## Three Tools, Three Questions

| Tool | The question it answers | The scenario words |
|---|---|---|
| **Identity and Access Management** | Who is allowed to use or see which resource? | permissions, who can access, roles, restrict, authorise |
| **Security Command Center** | What does our security posture look like across everything? | central view, overall health, misconfigurations, exposure, threats across projects |
| **Workload monitoring** | Are the running systems behaving as they should? | monitoring workloads, keeping systems secure in operation |

This is as clean a mapping as the exam offers, and it is decided by a single word in the scenario.<sup>[2]</sup>

**IAM is about permission.** When a scenario is about controlling who may reach a resource, enforcing who can see what, or managing access to sensitive material, that is authorisation and that is IAM.<sup>[1]</sup>

**Security Command Center is about visibility.** When a scenario wants one place to see security health, find misconfigurations, or understand exposure and threats across an environment, that is posture management.<sup>[3]</sup><sup>[4]</sup>

The distinction to hold: IAM **prevents** access, Security Command Center **reveals** problems. A scenario asking you to stop somebody reaching the data is IAM. A scenario asking you to find out what is already wrong is Security Command Center. *Prevention and discovery are different purchases.*

**Secure-by-design infrastructure** is the term for what Google builds in rather than what you configure: the protections inherent in the network and hardware. When a question asks what to call those built-in protective measures, that phrase is the answer, and it is a vocabulary question rather than a product one.

## Security Attaches to Each Stage Differently

Saying security covers the whole lifecycle is correct and not yet useful. The useful version names what the risk is at each stage, because scenarios usually sit in one of them.

| Stage | What the security work is there |
|---|---|
| Data ingestion and preparation | Controlling who can reach the data, and protecting whatever sensitive material is inside it |
| Model training | Protecting the training data and the model being produced from exposure or tampering |
| Model deployment | Controlling who may call the model, and what it may reach on their behalf |
| Monitoring and management | Watching the running system, and keeping it patched |

The first row is the one the exam asks about, and it is the stage people skip. When a scenario places itself at data collection and asks what matters, the answer is **access control plus protection of the sensitive data in the training set**.<sup>[2]</sup> Not model hardening, not endpoint security, not output filtering. All three are real controls that belong to later stages.

## How Wrong Answers Are Built on This Material

The distractors here are other genuine security controls, each belonging to a different stage or a different purpose. Nothing is implausible, so the only defence is naming the stage and the purpose before reading the options.

- **The single-stage answer.** Security located at one point in the lifecycle, usually review before launch. It sounds like professional practice and it contradicts the published position, which is that this runs throughout and starts at ingestion.
- **The wrong-purpose tool answer.** Security Command Center where permission was the issue, or IAM where visibility was. **Prevention against discovery** settles it.
- **The later-stage control answer.** Output filtering, endpoint protection or model hardening offered where the scenario is at data collection.
- **The compliance-as-security answer.** A certification, an audit or a policy document offered where a technical control was asked for. Governance matters and is not the same as a control.
- **The product-for-a-term answer.** A product named where the question asked for the **term** describing built-in protections, which is secure-by-design infrastructure.

| When the scenario | The answer is usually | The trap is usually |
|---|---|---|
| Asks when security and privacy apply | Throughout the lifecycle, from ingestion onward | A single stage, usually pre-launch review |
| Is about who may reach a resource | Identity and Access Management | Security Command Center |
| Wants one view of posture and exposure | Security Command Center | IAM, because access is mentioned |
| Sits at data collection | Access control and protecting sensitive training data | A control belonging to a later stage |
| Asks what built-in protections are called | Secure-by-design infrastructure | A named product |
| Describes managing AI and ML model risk | The Secure AI Framework | A general security framework |

The habit: say the stage, then say whether the need is prevention or discovery. Two short phrases, and the product follows.

## What to Remember

- **Secure AI means protecting the AI application from harm**, specifically from **attack and misuse**. Chapter 22 is the other direction: harm the system **causes**.
- **Security covers the entire ML lifecycle and starts at ingestion.** An option naming **one stage** is wrong, however professional it sounds.
- **The Secure AI Framework, SAIF, helps organisations manage AI and ML model risk.** Untested, and on the blueprint.
- **Secure-by-design infrastructure is the term** for the protections Google builds into **network and hardware**, rather than ones you configure.
- **IAM answers who may use or see a resource.** It **prevents** access.
- **Security Command Center answers what the posture looks like** across everything: **misconfigurations, exposure, threats**. It **reveals** problems.
- **Prevention against discovery** settles nearly every tool question on this objective.
- **Workload monitoring** covers whether **running systems behave as they should**.
- **At data collection the control is access control plus protecting sensitive training data.** Output filtering and model hardening belong **later**.
- **A certification is not a control.** Governance matters and answers a different question.

## Endnotes for this chapter

1. Generative AI Leader certification exam guide. https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_english.pdf
2. Generative AI Leader certification exam study guide. https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf
3. Security Command Center documentation. https://docs.cloud.google.com/security-command-center/docs
4. Security Command Center overview. https://docs.cloud.google.com/security-command-center/docs/security-command-center-overview
