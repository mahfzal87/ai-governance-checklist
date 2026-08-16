# NIST AI RMF as a working checklist

The AI RMF is voluntary and non-prescriptive, which is its strength and its problem. It tells you what good looks like and leaves you to decide what to produce. This turns the four functions into artefacts a product team can actually be held to.

**Framework:** NIST AI 100-1, AI RMF 1.0, January 2023. [PDF](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) · [DOI](https://doi.org/10.6028/NIST.AI.100-1)

**Structure:** 4 functions, 19 categories, 72 subcategories. GOVERN is cross-cutting and runs through the other three rather than sitting before them.

> [!NOTE]
> **AI RMF 1.0 is under revision** as part of the White House AI Action Plan, which tasked NIST with revising it to remove references to misinformation, DEI and climate change. As of 16 August 2026 there is **no draft, no RFI and no announced date**. AI 100-1 (January 2023) remains the only version and the one to cite. The [Playbook](https://airc.nist.gov/airmf-resources/playbook/) is live but frozen pending the revision.

---

## The seven characteristics of trustworthy AI

Your evaluation plan should say something about each, even if the answer for some is "not applicable, because."

1. Valid and Reliable. Foundational, and the others rest on it
2. Safe
3. Secure and Resilient
4. Accountable and Transparent
5. Explainable and Interpretable
6. Privacy-Enhanced
7. Fair, with Harmful Bias Managed

Three of the seven are paired characteristics, which is why there are seven and not ten.

---

## GOVERN. 6 categories, 19 subcategories.

Organisation-level, mostly not per-feature. Do it once, review it annually, and reference it from every PRD.

| Do | Artefact | Key subcategories |
|---|---|---|
| Know which laws apply to you, and write it down | Regulatory applicability register | `GOVERN 1.1` "Legal and regulatory requirements involving AI are understood, managed, and documented." |
| Put the trustworthiness characteristics into actual policy | AI policy | `GOVERN 1.2` |
| Name who is accountable for what | RACI, with individuals not teams | `GOVERN 2.1` |
| Maintain an inventory of AI systems | AI system registry | `GOVERN 1.6` |
| Build a culture where people can raise concerns | Escalation path, and evidence it was used | `GOVERN 4.1` |
| Govern third-party AI and its IP risk | Vendor assessment, procurement clauses | `GOVERN 6.1` |

If you only do one: **the registry**. Almost every downstream obligation, in every framework, assumes you know what you have.

---

## MAP. 5 categories, 18 subcategories.

Per-system, and this is where product managers do the most work. Everything here should already exist in a good PRD.

| Do | Artefact | Key subcategories |
|---|---|---|
| Document intended purpose, users, context, and both positive and negative impacts | PRD sections 1 to 4 | `MAP 1.1` |
| Tie it to a business goal | PRD section 1 | `MAP 1.3` |
| State the task and method plainly | PRD section 5 | `MAP 2.1` "The specific tasks and methods used to implement the tasks that the AI system will support are defined (e.g., classifiers, generative models, recommenders)." |
| Define human oversight processes | Oversight design spec | `MAP 3.5` |
| Estimate likelihood and magnitude of each impact | Risk register | `MAP 5.1` |

**The question MAP forces that teams skip:** what is the non-AI baseline, and what does it cost you to not use AI here? `MANAGE 2.1` requires considering "viable non-AI alternative systems, approaches, or methods." Answer it in writing before you build.

---

## MEASURE. 4 categories, 22 subcategories.

The largest function, and the one that separates a governed system from a documented one.

| Do | Artefact | Key subcategories |
|---|---|---|
| Choose metrics, and **document what you are not measuring** | Evaluation plan | `MEASURE 1.1` "The risks or trustworthiness characteristics that will not – or cannot – be measured are properly documented." |
| Evaluate validity, safety, security and resilience | Results pack | `MEASURE 2.5` to `2.7` |
| Evaluate fairness and bias | Fairness report with the subgroups named | `MEASURE 2.11` "Fairness and bias – as identified in the MAP function – are evaluated and results are documented." |
| Check that your evaluation approach itself works | Eval retro | `MEASURE 2.13` |
| Track emergent risks after deployment | Monitoring plan | `MEASURE 3.1` |
| Consult domain experts and end users | Research record | `MEASURE 4.1` |

> [!TIP]
> `MEASURE 1.1` is the most useful line in the entire framework, and the least used. Writing down **what you decided not to measure and why** takes twenty minutes, kills the argument about whether a gap was an oversight or a decision, and is the first thing an auditor asks for.

---

## MANAGE. 4 categories, 13 subcategories.

Deciding and acting on what MEASURE found.

| Do | Artefact | Key subcategories |
|---|---|---|
| Prioritise risk treatment by impact, likelihood and available resources | Risk register with dispositions | `MANAGE 1.2` |
| Consider non-AI alternatives when allocating resources | Decision log | `MANAGE 2.1` |
| Monitor third-party risk on an ongoing basis | Vendor review cadence | `MANAGE 3.1` |
| Run post-deployment monitoring with appeal, override, decommissioning, incident response and change management | Monitoring plan and incident runbook | `MANAGE 4.1` |

`MANAGE 4.1` is the closest single subcategory to the EU AI Act's Article 72 post-market monitoring duty. If you build to Article 72, you have largely satisfied it. The reverse is not true: `MANAGE 4.1` carries no regulator notification duty and no statutory clock.

---

## Generative AI: use AI 600-1 for eval scope

[NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf), July 2024, is the Generative AI Profile, and still the only completed AI RMF profile. Its twelve risks are the best public taxonomy for scoping a generative red team. Use it as the coverage checklist and record a disposition for each.

| # | Risk | Covered? | Evidence |
|---|---|---|---|
| 1 | CBRN Information or Capabilities | | |
| 2 | Confabulation | | |
| 3 | Dangerous, Violent, or Hateful Content | | |
| 4 | Data Privacy | | |
| 5 | Environmental Impacts | | |
| 6 | Harmful Bias and Homogenization | | |
| 7 | Human-AI Configuration | | |
| 8 | Information Integrity | | |
| 9 | Information Security | | |
| 10 | Intellectual Property | | |
| 11 | Obscene, Degrading, and/or Abusive Content | | |
| 12 | Value Chain and Component Integration | | |

For adversarial ML specifically, the current NIST reference is **AI 100-2 E2025**, *Adversarial Machine Learning: A Taxonomy and Terminology*, final 24 March 2025.

---

## What the AI RMF does not give you

Be honest about this when someone proposes it as a compliance answer.

- **No conformity assessment, no certification, no CE marking.** It is a framework, not a scheme
- **No registration duty** and no public register
- **No incident notification** to any regulator, and no statutory clock
- **No log retention minimum**

Those four are exactly where the EU AI Act imposes duties that no voluntary framework discharges. See [reference/crosswalk.md](../reference/crosswalk.md).

---

<sub>Subcategory statements quoted verbatim from NIST AI 100-1. NIST uses en dashes inside several statements; those are preserved in the quotations. Verified 16 August 2026.</sub>
