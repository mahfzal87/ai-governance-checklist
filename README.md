# AI governance checklist

**The intake triage, PRD template and launch gate I use to take an AI feature from idea to release.** Structured on the EU AI Act, the NIST AI RMF and ISO/IEC 42001, written for the product manager who has to produce the artefacts rather than the lawyer who reviews them.

I built this because the material available sits at two unhelpful extremes. Law firm briefings tell you the regulation exists and stop. Vendor maturity models tell you to "establish a governance framework." Neither answers the question a PM actually has on a Tuesday: *this feature, this sprint, what do I have to write, and who signs it?*

Every obligation here names an article, an artefact and a signer.

---

## Start here

| | |
|---|---|
| **[Intake triage](checklists/intake-triage.md)** | Thirty minutes, before the PRD. Is it an AI system, what are we, what tier, what does that trigger |
| **[PRD template](templates/prd-ai-feature.md)** | The spec, with the governance sections built in rather than bolted on |
| **[Launch gate](templates/launch-gate.md)** | One page of blocking criteria for the go/no-go |

## Reference

| | |
|---|---|
| **[EU AI Act obligations](checklists/eu-ai-act.md)** | Provider, deployer, Article 50 and GPAI duties, each with the artefact and the signer |
| **[NIST AI RMF](checklists/nist-ai-rmf.md)** | The four functions turned into artefacts, plus the AI 600-1 generative risk taxonomy |
| **[Timeline](reference/timeline.md)** | What applies when, post-Omnibus |
| **[Crosswalk](reference/crosswalk.md)** | EU AI Act to NIST to ISO 42001, with the gaps marked |

---

## Three things this repo gets right that most sources currently do not

**The Digital Omnibus was adopted.** Regulation (EU) 2026/1744 was published on 24 July 2026 and entered into force on **27 July 2026**, amending the AI Act in 43 places. It is not a proposal. A lot of published guidance, including timelines still live on well-known AI Act sites, has not been updated.

**Annex III high-risk obligations now apply from 2 December 2027**, and Annex I from 2 August 2028. The **Article 27 FRIA moved with them**, to December 2027, not August 2026 as many guides still say.

**The Act was not delayed.** Only Chapter III Sections 1 to 3 moved. **Article 50 transparency has been enforceable since 2 August 2026**, at up to 15 million euro or 3 percent of worldwide turnover, and it applies regardless of risk tier. It is the obligation teams are most likely to be breaching right now while they plan for 2027.

---

## How to use it

Fork it and change it. This is the version that fits how I work, and the parts that matter are the questions, not the formatting.

If you take one thing, take the intake triage. Most governance failures I have seen are not failures of controls. They are a system that was never classified, so nobody knew which controls applied, so the question never reached anyone who could answer it.

Two habits underneath all of it:

**Write the eval before the roadmap.** A quality bar you cannot measure is a wish, and a threshold moved after seeing the results is not a threshold.

**Every accepted risk needs a person, not a team.** If nobody will put their name against it, it has not been accepted. It has been ignored.

---

## Accuracy

Every article number, clause reference and date was verified against a primary source on **16 August 2026**: the [consolidated AI Act](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:02024R1689-20260727), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng), [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf), and the ISO Online Browsing Platform.

Where something could not be verified, it is marked as such rather than filled in with a plausible number. Two examples: the crosswalk is labelled inferred throughout, because no standards body publishes a validated three-way mapping. And there is no count of ISO/IEC 42001 certificates anywhere in this repo, because 42001 does not yet appear in the ISO Survey and every circulating figure is a vendor tally.

This ages. If you are reading it well after August 2026, check the timeline against the [AI Act Service Desk](https://ai-act-service-desk.ec.europa.eu/en/ai-act/timeline/timeline-implementation-eu-ai-act) before relying on a date. Corrections by issue or PR are welcome, and citations are appreciated.

> [!IMPORTANT]
> **Not legal advice.** This is a working checklist written by a product manager for product managers. It is not a substitute for advice from a qualified lawyer in your jurisdiction, and it does not create a compliance position. Where this repo and the Regulation disagree, the Regulation wins.

---

## Licence

[CC BY 4.0](LICENSE). Use it, adapt it, ship it in your own company's process. Attribution appreciated, not enforced.

<sub>Maintained by <a href="https://github.com/mahfzal87">Ahmad Afzal</a>, Product Lead for AI platforms in sovereign and regulated environments. More at <a href="https://mahmadafzal.com">mahmadafzal.com</a>.</sub>
