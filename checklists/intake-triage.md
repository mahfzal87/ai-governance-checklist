# Intake triage

Run this before anyone writes a line of the PRD. It takes about thirty minutes and it decides how much governance work the rest of the quarter is carrying.

Output is four written answers: **what it is, what we are, what tier it lands in, and what that triggers.** Write them down. "We discussed it in a meeting" is not an artefact, and it will not be one later when somebody asks.

---

## Step 0. Is it an AI system at all?

Article 3(1) defines an AI system as a machine-based system designed to operate with varying levels of autonomy, that may exhibit adaptiveness, and that infers from input how to generate outputs such as predictions, content, recommendations or decisions.

The Commission's [guidelines on the definition](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) are non-binding but are what a regulator will read. Two practical notes:

- **Inference is the hinge.** A system that applies rules a human wrote is generally out. A system that derives the rule from data is generally in.
- Do not try to argue your way out at this step. If it is genuinely borderline, running the rest of this checklist anyway costs you half an hour. Being wrong costs considerably more, and later, and in public.

**Write down:** the system, in one sentence, in plain language.

---

## Step 1. Freeze the intended purpose

One sentence. It is the legal hinge for classification, for Article 13 instructions for use, and for the whole Annex III test. It deserves more care than it usually gets.

> Intended purpose: _______________________________________________

Two rules. Write what it **is for**, not what it **can do**, because the second one is marketing. And treat changing it later as a design change with legal consequences, not as a copy edit somebody does on a Friday.

---

## Step 2. What are we?

| Role | Definition | You are here if |
|---|---|---|
| **Provider** | Art. 3(3). Develops, or has developed, an AI system and places it on the market or puts it into service under its own name or trademark | You are shipping it to customers |
| **Deployer** | Art. 3(4). Uses an AI system under its own authority, other than personal non-professional use | You bought it and are running it on your own people or customers |
| **Both** | | You ship a product and also use it internally |
| **Downstream provider** | | You build on someone else's GPAI model |

> [!WARNING]
> **Article 25 flips you.** If you put your name or trademark on a high-risk system, substantially modify one, or change the intended purpose of a system so that it becomes high-risk, **you become the provider** and inherit the full Article 16 obligation set. Re-run this step after any rebrand, fine-tune, or substantial modification.

**Write down:** our role, and the one fact that decides it.

---

## Step 3. Tier it

Work down. Stop at the first match.

### Tier 1: Prohibited (Article 5). If this matches, stop.

Applicable since 2 February 2025, except the last two, which apply from 2 December 2026.

- [ ] Subliminal, purposefully manipulative or deceptive techniques that materially distort behaviour and cause or are likely to cause significant harm `5(1)(a)`
- [ ] Exploiting vulnerabilities due to age, disability, or a specific social or economic situation `5(1)(b)`
- [ ] Social scoring leading to detrimental treatment in unrelated contexts, or disproportionate to the behaviour `5(1)(c)`
- [ ] Predictive policing on individuals based solely on profiling or personality traits `5(1)(d)`
- [ ] Untargeted scraping of internet or CCTV images to build or expand facial recognition databases `5(1)(e)`
- [ ] Emotion inference in the workplace or in education, outside medical or safety reasons `5(1)(f)`
- [ ] Biometric categorisation to deduce race, political opinions, trade union membership, religious or philosophical beliefs, sex life or sexual orientation `5(1)(g)`
- [ ] Real-time remote biometric identification in publicly accessible spaces for law enforcement, outside three narrow authorised exceptions `5(1)(h)`
- [ ] Generating or manipulating realistic non-consensual intimate imagery of an identifiable person `5(1)(ba)`, from 2 Dec 2026
- [ ] Generating or manipulating child sexual abuse material `5(1)(bb)`, from 2 Dec 2026

Penalty tier: **35 million euro or 7 percent of worldwide annual turnover, whichever is higher** (Art. 99(3)). For SMEs, whichever is lower. Note that the small mid-cap cap added by the Omnibus does **not** extend to this tier.

### Tier 2: High risk

**Annex I route (Art. 6(1)).** The AI is a product, or a safety component of a product, covered by listed Union harmonisation legislation, **and** that product requires third-party conformity assessment. Applies from **2 August 2028**.

The Omnibus narrowed this. AI used solely for user assistance, performance optimisation, service efficiency, automation, convenience or quality control is excluded, unless its failure would endanger health and safety.

**Annex III route (Art. 6(2)).** Applies from **2 December 2027**. Eight areas:

| # | Area | Watch for |
|---|---|---|
| 1 | Biometrics | The only Annex III area where a notified body may be required |
| 2 | Critical infrastructure | Excluded from the Art. 27 FRIA duty |
| 3 | Education and vocational training | Admissions, assessment, proctoring |
| 4 | Employment and workers' management | Screening, ranking, task allocation, monitoring, termination |
| 5 | Essential private and public services | Includes **5(b) creditworthiness** and **5(c) life and health insurance pricing**, which carry the FRIA duty even for private deployers |
| 6 | Law enforcement | |
| 7 | Migration, asylum and border control | |
| 8 | Administration of justice and democratic processes | |

**The Article 6(3) derogation.** An Annex III system is not high-risk if it poses no significant risk of harm and it only performs a narrow procedural task, improves the result of a previously completed human activity, detects decision-making patterns without replacing or influencing a prior human assessment, or performs a preparatory task.

> [!CAUTION]
> **Profiling of natural persons always makes it high-risk.** No derogation.
>
> And the derogation is not free. Article 6(4) requires you to **document the assessment before placing on the market**, and Article 49(2) requires you to **register anyway**. Claiming the derogation is a filing obligation, not an exemption from paperwork.

Penalty tier: **15 million euro or 3 percent**, whichever is higher (Art. 99(4)).

### Tier 3: Transparency (Article 50). Live now, since 2 August 2026.

This tier is **independent of the others**. A minimal-risk chatbot still owes Article 50. This is the obligation most teams currently miss, and it is already enforceable.

- [ ] `50(1)` **Provider.** System interacts directly with people, so it must tell them, unless that is obvious
- [ ] `50(2)` **Provider.** Output is synthetic audio, image, video or text, so it must be **marked in a machine-readable format** and detectable as artificially generated or manipulated
- [ ] `50(3)` **Deployer.** Emotion recognition or biometric categorisation, so inform the people exposed to it
- [ ] `50(4)` **Deployer.** Deep fakes must be disclosed. AI-generated or manipulated text published to inform the public on matters of public interest must be disclosed

Penalty tier: **15 million euro or 3 percent**, whichever is higher.

### Tier 4: Minimal risk

Everything else. Article 4 AI literacy still applies, and voluntary codes of conduct are available under Article 95. This is the tier everyone assumes they are in.

---

## Step 4. The GPAI question

Separate axis. Ask it even if you already tiered the system.

- [ ] **Do we place a general-purpose AI model on the market?** If yes, Article 53 applies: technical documentation (Annex XI), documentation for downstream providers (Annex XII), a copyright policy, and a **publicly available sufficiently detailed summary of training content**
- [ ] **Open-source release?** Art. 53(2) exempts (a) and (b) for models under a free and open-source licence with weights, architecture and usage information public. **The exemption does not apply to systemic-risk models**
- [ ] **Training compute greater than 10²⁵ FLOP?** That is the Art. 51(2) presumption of systemic risk. **You must notify the Commission within two weeks** (Art. 52), and Article 55 adds model evaluation with documented adversarial testing, Union-level systemic risk mitigation, serious incident reporting to the AI Office, and cybersecurity for the model and its infrastructure
- [ ] **Are we a downstream provider building on someone else's GPAI?** Then collect their Annex XII documentation. You need it, and you should make it a procurement condition

GPAI obligations have applied since 2 August 2025. Commission enforcement powers, at 3 percent or 15 million euro, began 2 August 2026.

---

## Step 5. What did that trigger?

| If | Then | By when |
|---|---|---|
| Prohibited | Stop. Escalate to legal. There is no compliance route | Now |
| Annex III high risk | Full [EU AI Act checklist](eu-ai-act.md), provider or deployer column | 2 Dec 2027 |
| Annex I high risk | Same, plus your sectoral product legislation | 2 Aug 2028 |
| Art. 6(3) derogation claimed | Documented assessment before market, plus Art. 49(2) registration | Before launch |
| Art. 50 applies | Transparency implementation and evidence | **Already live** |
| GPAI provider | Art. 53 pack. Art. 55 as well if systemic risk | **Already live** |
| Deployer, public body or private provider of public services, or Annex III 5(b) or 5(c) | **Article 27 FRIA** | 2 Dec 2027 |
| Personal data involved | **DPIA** under GDPR Art. 35. Write it so it interlocks with the FRIA, which amended Art. 27(4) now permits | Before processing |
| Anything above | Registry entry, named accountable owner, review date | Now |

---

## The four answers

Paste these into section 11 of the [PRD](../templates/prd-ai-feature.md).

```
System:            
Intended purpose:  
Our role:          Provider / Deployer / Both / Downstream provider
Tier:              Prohibited / High risk (Annex I | Annex III) / Transparency / Minimal
Reasoning:         
Triggered:         
Decided by:                          Date:
Review when:       intended purpose changes, substantial modification, new jurisdiction
```

---

<sub>Article and Annex references are to Regulation (EU) 2024/1689 as amended by Regulation (EU) 2026/1744, verified 16 August 2026. This is a working checklist written by a product manager, not legal advice.</sub>
