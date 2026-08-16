# Launch gate

One page. Filled in before the go/no-go, not written up after it.

The point of a gate is that it can say no. If nothing on this page could ever block a launch, you do not have a gate, you have a status update.

---

**System:** &nbsp; **Release:** &nbsp; **Date:** &nbsp; **Chair:**

**Tier from [intake triage](../checklists/intake-triage.md):** Prohibited / High risk (Annex I | Annex III) / Transparency / Minimal
**Our role:** Provider / Deployer / Both / Downstream provider

---

## 1. Blocking criteria

Nothing ships until every applicable row is Yes. A No is a stop, not a risk to be accepted in the meeting.

| # | Criterion | Applies | Status | Evidence |
|---|---|---|---|---|
| 1 | Intake triage completed, tier documented, and legal has signed the classification | Always | ☐ | |
| 2 | Evaluation targets met at the thresholds set in the PRD **before** results were seen | Always | ☐ | |
| 3 | Fairness evaluation run across named subgroups, disparities inside the stated bound | Where people are affected | ☐ | |
| 4 | Adversarial and red team testing complete, with every finding dispositioned | Generative or externally exposed | ☐ | |
| 5 | Human oversight implemented as specified, and the reviewers have the authority to override | High risk | ☐ | |
| 6 | Kill switch tested in production conditions, with a named owner and a measured time to disable | Always | ☐ | |
| 7 | Logging live, retention configured to **at least 6 months** | High risk | ☐ | |
| 8 | Monitoring and alerting live, with a named on-call | Always | ☐ | |
| 9 | Incident runbook written, with the Article 73 clocks pre-wired: 15 days, 2 days, 10 days | High risk | ☐ | |
| 10 | Rollback tested, and the trigger conditions are written down | Always | ☐ | |
| 11 | **Article 50 transparency implemented and evidenced.** Live obligation since 2 Aug 2026 | Any user-facing or generative system | ☐ | |
| 12 | DPIA complete and signed | Personal data | ☐ | |
| 13 | FRIA complete and signed | Art. 27 deployers | ☐ | |
| 14 | Technical documentation complete per Annex IV | High risk provider | ☐ | |
| 15 | Instructions for use published, with **declared accuracy metrics** | High risk provider | ☐ | |
| 16 | Conformity assessment complete, DoC signed, CE marking affixed | High risk provider | ☐ | |
| 17 | Registered in the EU database, including where the Art. 6(3) derogation is claimed | High risk provider, and public authority deployers | ☐ | |
| 18 | Post-market monitoring plan written and part of the technical documentation | High risk provider | ☐ | |
| 19 | Workers' representatives informed | Workplace deployment | ☐ | |

> [!CAUTION]
> **Criterion 2 has a failure mode worth naming.** A threshold moved after seeing the results is not a threshold. If the bar changed, record who changed it, when, and why, and treat the gate as failed unless that reasoning survives scrutiny.

## 2. Residual risks accepted

Every accepted risk needs a person, not a team. If nobody will put their name in the last column, it is not accepted, it is ignored.

| Risk | Impact if it materialises | Why we are accepting it | Accepted by | Review date |
|---|---|---|---|---|
| | | | | |

## 3. Known limitations we are shipping with

What the system cannot do, stated plainly, and where users will be told.

| Limitation | Communicated where |
|---|---|
| | |

## 4. Rollout

| Stage | Audience | Entry criteria | Exit criteria | Rollback trigger |
|---|---|---|---|---|
| Internal | | | | |
| Limited | | | | |
| General | | | | |

## 5. Decision

**Outcome:** Go / Go with conditions / No go

**Conditions, with owners and dates:**

**Reasoning, in two or three sentences.** Write it for someone reading this in eighteen months who was not in the room.

| Role | Name | Decision | Date |
|---|---|---|---|
| Product | | | |
| Engineering | | | |
| Security | | | |
| Legal / Compliance | | | |
| Data protection | | | |
| **Accountable executive** | | | |

## 6. Next review

**Date:** &nbsp; **Owner:**

Triggers that pull the review forward: substantial modification, change of intended purpose, a new jurisdiction, a serious incident, a drift alert, or a change in the applicable law.

---

<sub>Article references are to Regulation (EU) 2024/1689 as amended by Regulation (EU) 2026/1744. Not legal advice.</sub>
