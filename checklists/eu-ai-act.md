# EU AI Act obligations checklist

For systems that came out of [intake triage](intake-triage.md) as high risk, or that trigger Article 50 or the GPAI rules.

Every row names the article, the artefact you have to produce, and who signs. If you cannot name a signer, the obligation has no owner.

**Verified 16 August 2026** against Regulation (EU) 2024/1689 as amended by Regulation (EU) 2026/1744. Dates in [reference/timeline.md](../reference/timeline.md).

---

## A. Provider of a high-risk system

Article 16 lists the twelve duties. The substance is in Section 2. Applies from **2 Dec 2027** (Annex III) or **2 Aug 2028** (Annex I).

### Build

| # | Art. | Obligation | Artefact | Signs |
|---|---|---|---|---|
| A1 | **9** | Risk management system, continuous and iterative across the whole lifecycle. Must cover reasonably foreseeable **misuse**, not just intended use | Living risk register with residual-risk acceptances | Risk owner |
| A2 | **10** | Data governance over training, validation and testing sets: origin, preparation, assumptions, suitability, **bias examination `10(2)(f)` and mitigation `10(2)(g)`**, representativeness, geographic and contextual fit | Data governance record plus a datasheet per dataset | Data lead |
| A3 | **11 + Annex IV** | Technical documentation, drawn up **before** placing on the market and kept current | Annex IV pack | Eng lead |
| A4 | **12** | Automatic logging of events across the system's lifetime, sufficient for risk identification and post-market monitoring | Logging design and retention config | Platform |
| A5 | **13** | Transparency to deployers, plus **instructions for use** carrying the `13(3)` minimum contents, including **declared accuracy metrics** and known limitations | Instructions for use | PM writes, Legal reviews |
| A6 | **14** | Human oversight designed in, so a natural person can effectively oversee it | Oversight design spec | PM and Design |
| A7 | **15** | Accuracy, robustness and cybersecurity appropriate and consistent across the lifecycle. **Accuracy levels and metrics are declared in the instructions for use**, which makes them auditable numbers rather than marketing | Evaluation results pack | Eng lead |
| A8 | **17** | Quality management system, documented. See note on EN 18286 below | QMS documentation | Quality |

> [!NOTE]
> **Article 4a is new.** The Omnibus created a legal basis for processing special category data to detect and correct bias, and extended it beyond high-risk providers. Old Article 10(5) was deleted. The conditions are real: no effective alternative including synthetic or anonymised data, technical limits on reuse, strict access controls. Evidence them, and have the DPO sign.

### Ship

| # | Art. | Obligation | Artefact | Signs |
|---|---|---|---|---|
| A9 | **43** | Conformity assessment. Annex III point 1 (biometrics) allows Annex VI internal control **only where harmonised standards were applied**, otherwise Annex VII notified body. Other Annex III areas use internal control | Conformity assessment record | Quality |
| A10 | **47** | EU declaration of conformity, kept for 10 years | Signed DoC | Authorised signatory |
| A11 | **48** | CE marking, visible, legible and indelible | | Quality |
| A12 | **49** | Registration in the EU database before placing on the market. Also `49(2)` where you claim the Art. 6(3) derogation. `49(4)` gives a secure non-public section for Annex III points 1, 6 and 7 | Registration record | Compliance |

> [!WARNING]
> **No harmonised standard has been cited in the Official Journal.** As of 16 August 2026, nothing gives you the Article 40 presumption of conformity. For Annex III point 1, that pushes you onto the Annex VII notified body route. Notified body capacity is thin. Treat this as a twelve to eighteen month path, and start before you think you need to.

### Run

| # | Art. | Obligation | Artefact | Signs |
|---|---|---|---|---|
| A13 | **18** | Keep technical documentation, QMS records, notified body decisions and the DoC at authorities' disposal for **10 years** | Retention policy | Compliance |
| A14 | **19** | Keep automatically generated logs under your control for **at least 6 months** | Retention config | Platform |
| A15 | **20** | Corrective actions: withdraw, disable or recall, and inform distributors, deployers, authorised representative and importers | Corrective action procedure | Quality |
| A16 | **72** | Post-market monitoring system, proportionate, based on a **plan that forms part of the Annex IV technical documentation**. The Commission template is due 2 Sep 2027, so write yours now | PMM plan | PM and Quality |
| A17 | **73** | Serious incident reporting to the market surveillance authority of the Member State where it occurred | Incident runbook with the clocks pre-wired | Incident commander |

**Article 73 clocks.** Immediately, and in any case no later than **15 days** after becoming aware. **2 days** for widespread infringement or Art. 3(49)(b) incidents. **10 days** where a person has died. Incomplete initial reports are permitted, so report on time and complete later. Note Art. 73(6): do not alter the system before informing the authorities.

---

## B. Deployer of a high-risk system

Article 26. Applies from **2 Dec 2027** or **2 Aug 2028**.

| # | Art. | Obligation | Artefact | Signs |
|---|---|---|---|---|
| B1 | **26(1)** | Technical and organisational measures to use the system **in accordance with the instructions for use** | Operating procedure | Business owner |
| B2 | **26(2)** | Assign human oversight to people with the necessary **competence, training and authority, as well as the necessary support** | Named roles, training record | Business owner |
| B3 | **26(4)** | Where you control input data, ensure it is relevant and sufficiently representative | Input data controls | Data lead |
| B4 | **26(5)** | Monitor operation. Suspend and inform the provider and the market surveillance authority where an Art. 79(1) risk arises. On a serious incident, inform the provider first | Monitoring plan, escalation path | Business owner |
| B5 | **26(6)** | Keep logs under your control for **at least 6 months** | Retention config | Platform |
| B6 | **26(7)** | **Inform workers' representatives and affected workers** before putting a high-risk system into use in the workplace | Comms record | HR |
| B7 | **26(8)** | Public authority deployers must comply with Art. 49 registration, and **must not use an unregistered system** | Registration check | Compliance |
| B8 | **26(9)** | Use the Art. 13 information to carry out a **DPIA** under GDPR Art. 35 | DPIA | DPO |
| B9 | **26(10)** | Post remote biometric identification requires judicial or administrative authorisation, in advance or **within 48 hours** | Authorisation record | Legal |
| B10 | **26(11)** | Inform people who are subject to decisions made with an Annex III high-risk system | User-facing notice | PM |

### The FRIA, Article 27

**Who owes it.** Deployers of Annex III high-risk systems, **excluding Annex III point 2 (critical infrastructure)**, that are:

- bodies governed by public law, **or**
- private entities providing public services, **or**
- any deployer of systems under **Annex III 5(b)** creditworthiness and credit scoring, or **Annex III 5(c)** risk assessment and pricing in life and health insurance

That last limb catches ordinary private companies. Lenders and insurers owe a fundamental rights impact assessment whether or not they are public bodies.

**Required contents**, Art. 27(1):

- [ ] (a) The deployer's processes in which the system will be used
- [ ] (b) Period and frequency of intended use
- [ ] (c) Categories of natural persons and groups likely to be affected
- [ ] (d) Specific risks of harm to those groups, informed by the Art. 13 information from the provider
- [ ] (e) How human oversight measures will be implemented
- [ ] (f) Measures to take if the risks materialise, including internal governance and complaint mechanisms

**Two Omnibus changes that save real work.** Art. 27(4) now permits cross-references to, or inclusion of parts of, the **DPIA**. Art. 27(5) requires the AI Office to publish a template with an automated tool. **That template does not exist yet.** Write the DPIA and the FRIA so they interlock, and build your own structure against (a) to (f).

The obligation attaches to **first use**, and a prior FRIA can be relied on for similar cases.

---

## C. Article 50 transparency. Live since 2 August 2026.

Independent of risk tier, and the obligation most teams are currently missing. Enforceable at 15 million euro or 3 percent.

| # | Art. | Who | Obligation | Evidence |
|---|---|---|---|---|
| C1 | **50(1)** | Provider | Tell people they are interacting with an AI system, unless it is obvious to a reasonably well-informed person | Screenshot of the disclosure, and its wording |
| C2 | **50(2)** | Provider | Mark synthetic audio, image, video or text **in a machine-readable format**, detectable as artificially generated or manipulated | Technical spec of the marking, plus a verification test |
| C3 | **50(3)** | Deployer | Inform people exposed to emotion recognition or biometric categorisation | Notice, and the consent or notification flow |
| C4 | **50(4)** | Deployer | Disclose deep fakes. Disclose AI-generated or manipulated **text published to inform the public on matters of public interest** | Editorial policy and label |

Legacy systems get until **2 December 2026** for the `50(2)` machine-readable marking, under Art. 111(4).

Guidance: [Commission guidelines on Article 50](https://ai-act-service-desk.ec.europa.eu/en/ai-act), content approved 20 July 2026, and the voluntary Code of Practice on marking and labelling AI-generated content, 10 June 2026.

---

## D. GPAI model providers. Live since 2 August 2025.

| # | Art. | Obligation |
|---|---|---|
| D1 | **53(1)(a)** | Technical documentation of the model, including training and testing process and evaluation results. Annex XI minimum contents. Available to the AI Office and national authorities on request |
| D2 | **53(1)(b)** | Documentation for **downstream providers**. Annex XII minimum contents |
| D3 | **53(1)(c)** | Copyright policy, including identifying and complying with Art. 4(3) DSM Directive rights reservations using state of the art technologies |
| D4 | **53(1)(d)** | **Publicly available, sufficiently detailed summary of training content**, following the AI Office template |
| D5 | **53(2)** | Open-source exemption from (a) and (b) where weights, architecture and usage information are public under a free and open-source licence. **Not available to systemic-risk models** |
| D6 | **52** | Notify the Commission **within two weeks** of meeting, or knowing you will meet, the systemic risk threshold |

**Systemic risk**, Art. 51(2): cumulative training compute greater than **10²⁵ FLOP**. Article 55 then adds:

- [ ] (a) Model evaluation to standardised protocols, including **documented adversarial testing**
- [ ] (b) Assess and mitigate systemic risks at Union level
- [ ] (c) Track, document and report serious incidents to the AI Office without undue delay
- [ ] (d) Adequate cybersecurity for the model and its physical infrastructure

The [GPAI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai), final 10 July 2025, has three chapters: Transparency, Copyright, and Safety and Security, the last applying only to Article 55 providers. It is voluntary, and the Commission and AI Board have confirmed it as an adequate tool. Signing it is the cheapest way to demonstrate good faith.

---

## E. Penalties

| Breach | Ceiling |
|---|---|
| Article 5 prohibited practices | **35m euro or 7%** of worldwide annual turnover, whichever is **higher** |
| Provider, deployer, importer, distributor, authorised representative and notified body duties, and **Article 50** | **15m euro or 3%**, whichever is higher |
| Incorrect, incomplete or misleading information to authorities or notified bodies | **7.5m euro or 1%**, whichever is higher |
| GPAI model providers, imposed by the Commission (Art. 101) | **15m euro or 3%**, whichever is higher |

SMEs and start-ups get whichever is **lower**. The small mid-cap cap added by the Omnibus applies only to the 3 percent and 1 percent tiers, **not** to the Article 5 tier.

Article 4 AI literacy has **no dedicated fine tier**. It falls under the general Member State regime in Art. 99(1), which the Omnibus amended to include warnings and non-monetary measures.

---

## F. On ISO/IEC 42001

Worth being precise, because this gets oversold.

ISO/IEC 42001:2023 is certifiable, and certification is strong evidence of governance maturity. **It confers no presumption of conformity under the AI Act.** EN ISO/IEC 42001:2026 is CEN-CENELEC's identical adoption of the unchanged ISO text, and it is not among the deliverables under standardisation request M/613. For the Article 17 QMS requirement, CEN-CENELEC wrote a purpose-built standard, **EN 18286:2026**, precisely because 42001's scope does not map cleanly onto it.

So: pursue 42001 because it builds the management system you need anyway, and track EN 18286 for the legal route.

---

<sub>Not legal advice. Article references verified 16 August 2026 against the consolidated text. Where this checklist and the Regulation disagree, the Regulation wins.</sub>
