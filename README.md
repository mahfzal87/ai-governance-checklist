# AI governance checklist

**The intake triage, PRD template and launch gate I use to get an AI feature from idea to release.** Structured on the EU AI Act, the NIST AI RMF and ISO/IEC 42001, and written for the product manager who has to produce the artefacts rather than the lawyer who reviews them.

I built this because the available material sits at two unhelpful extremes. Law firm briefings tell you the regulation exists, at length, for a fee. Vendor maturity models tell you to "establish a governance framework," which is advice in the same way that "be taller" is advice. Neither answers the question a PM actually has on a Tuesday: *this feature, this sprint, what do I have to write, and who signs it?*

Every obligation here names an article, an artefact and a signer.

## Start here

| | |
|---|---|
| **[Intake triage](checklists/intake-triage.md)** | Thirty minutes, before the PRD. Is it an AI system, what are we, what tier, what does that trigger |
| **[PRD template](templates/prd-ai-feature.md)** | The spec, with the governance sections built in rather than bolted on afterwards by someone annoyed about it |
| **[Launch gate](templates/launch-gate.md)** | One page of blocking criteria for the go/no-go |

## Reference

| | |
|---|---|
| **[EU AI Act obligations](checklists/eu-ai-act.md)** | Provider, deployer, Article 50 and GPAI duties, each with the artefact and the signer |
| **[NIST AI RMF](checklists/nist-ai-rmf.md)** | The four functions turned into things you can actually hand someone, plus the AI 600-1 generative risk list |
| **[Timeline](reference/timeline.md)** | What applies when, post-Omnibus |
| **[Crosswalk](reference/crosswalk.md)** | EU AI Act to NIST to ISO 42001, with the gaps marked, because the gaps are the interesting part |

## Three things this gets right that most sources currently do not

**The Digital Omnibus was adopted.** Regulation (EU) 2026/1744 was published on 24 July 2026 and entered into force on **27 July 2026**, amending the AI Act in a lot of places including the high-risk dates. It is not a proposal. A surprising amount of published guidance, including timelines still sitting live on well-known AI Act sites, has not caught up.

**Annex III high-risk obligations now apply from 2 December 2027**, and Annex I from 2 August 2028. The **Article 27 FRIA moved with them**, to December 2027, not August 2026 as plenty of guides still cheerfully state.

**The Act was not delayed.** Only Chapter III Sections 1 to 3 moved. **Article 50 transparency has been enforceable since 2 August 2026**, at up to 15 million euro or 3 percent of worldwide turnover, whichever is higher, and it applies regardless of risk tier. It is the obligation teams are most likely to be breaching right now while they plan carefully for 2027.

## How to use it

Fork it and change it. This is the version that fits how I work. The questions are the useful part; the formatting is not sacred.

If you take one thing, take the intake triage. Most governance failures I have watched were not failures of controls. They were a system nobody ever classified, so nobody knew which controls applied, so the question never reached anyone who could have answered it. The controls were fine. They were just pointed at a different product.

Two habits sit underneath all of it.

**Write the eval before the roadmap.** A quality bar you cannot measure is a wish, and a threshold moved after seeing the results was never a threshold. If you want the runnable version of this, it is in [ai-governance-evals](https://github.com/mahfzal87/ai-governance-evals).

**Every accepted risk needs a person, not a team.** If nobody will put their name against it, it has not been accepted. It has been left somewhere warm and dark to grow.

## Accuracy

Every article number, clause reference and date was checked against a primary source on **16 August 2026**: the [consolidated AI Act](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:02024R1689-20260727), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng), [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf), and the ISO Online Browsing Platform.

Where something could not be verified it is marked as such rather than filled in with a confident number. Two examples. The crosswalk is labelled inferred throughout, because no standards body publishes a validated three-way mapping and pretending otherwise would be exactly the behaviour this repo is complaining about. And there is no count of ISO/IEC 42001 certificates anywhere in here, because 42001 does not appear in the ISO Survey yet and every figure in circulation is a vendor counting its own customers.

This ages. If you are reading it well after August 2026, check the dates against the [AI Act Service Desk](https://ai-act-service-desk.ec.europa.eu/en/ai-act/timeline/timeline-implementation-eu-ai-act) before you rely on one. Corrections by issue or PR are genuinely welcome, especially the embarrassing kind.

> [!IMPORTANT]
> **Not legal advice.** A working checklist written by a product manager for product managers. It is not a substitute for a qualified lawyer in your jurisdiction and it does not create a compliance position. Where this and the Regulation disagree, the Regulation wins.

## Licence

[CC BY 4.0](LICENSE). Use it, adapt it, put it in your own company's process. Attribution appreciated, not enforced.

<sub>Maintained by <a href="https://github.com/mahfzal87">Ahmad Afzal</a>. More at <a href="https://mahmadafzal.com">mahmadafzal.com</a>.</sub>
