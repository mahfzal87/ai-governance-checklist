# PRD: [Feature name]

> Delete this line and every instruction in square brackets before circulating.
> If a section does not apply, write "N/A" and one line saying why. Do not delete it.
> Empty sections are how obligations get missed.

| | |
|---|---|
| **Owner** | [name, role] |
| **Status** | Draft / In review / Approved / Shipped |
| **Risk classification** | Prohibited / High risk / Transparency / Minimal &nbsp; (see [intake-triage.md](../checklists/intake-triage.md)) |
| **Last updated** | [YYYY-MM-DD] |
| **Reviewers** | [legal, security, data protection, the accountable exec] |

---

## 1. The problem

[Two paragraphs maximum. Whose problem, how you know it is real, and what it costs them today. Cite the research, ticket volume, or interviews. If the only evidence is that someone senior asked for it, write that down honestly, because it changes how much you should build.]

**Who has this problem:** [the specific user, not the buyer, unless they are the same person]

**How they solve it today:** [the incumbent, even if the incumbent is a spreadsheet or nothing]

**Why now:** [what changed]

## 2. Why AI

[The section most AI PRDs skip. Answer it properly, because every obligation downstream in this document is triggered by this choice.]

- What makes this a problem that deterministic software cannot solve?
- What is the non-AI baseline, and how much of the value does it capture? [If a rules engine gets you 80 percent, say so, and justify the remaining 20 percent against the governance cost.]
- What happens to the user when the model is wrong? [Wrong answer, wrong action, wrong person affected]
- Is there a plausible way this system produces a materially different outcome for one group of people than another? [If yes, section 6 is not optional]

## 3. Users and jobs

| User | Job to be done | Success looks like |
|---|---|---|
| [role] | [when ..., I want to ..., so I can ...] | [observable outcome] |

**Explicitly not building for:** [the users you are declining to serve in v1, and why]

## 4. Scope

**In scope**
- [capability]

**Out of scope for v1**
- [capability, and what would have to be true to bring it in]

**Non-goals**
- [things people will assume you are doing, that you are not]

## 5. How it works

[Describe the system in the terms a reviewer needs. A diagram beats prose.]

- **Inputs:** [what the model sees, where it comes from, whether it contains personal data]
- **Model:** [foundation model, fine-tune, classical ML, retrieval. Name the provider and version]
- **Autonomy:** [recommends / drafts for approval / acts with human review / acts unsupervised. Be exact. This is the single most consequential line in the PRD]
- **Outputs:** [what the user or the system receives, and what it triggers]
- **Fallback:** [behaviour when the model is unavailable, low confidence, or refuses]

## 6. Data

| Question | Answer |
|---|---|
| Training or fine-tuning data sources | |
| Inference-time data sources | |
| Personal data involved? | [if yes: categories, lawful basis, retention] |
| Special category data involved? | |
| Data residency requirement | |
| Provenance and licensing of each source | |
| Known gaps or skew in the data | |
| Who can access the data, and the logs | |

[Representativeness is a product question, not a data science one. If your training data over-represents one population, name the population and the consequence in plain language.]

## 7. Evaluation

> Write this section before you write the roadmap. A quality bar you cannot measure is a wish.

**Offline evaluation**

| Metric | Definition | Target | Measured on |
|---|---|---|---|
| [accuracy, groundedness, refusal rate, ...] | [how it is computed] | [the number that gates launch] | [dataset, size, how it was built] |

**Fairness evaluation**

| Metric | Slices compared | Acceptable disparity | Rationale for that threshold |
|---|---|---|---|
| | | | |

**Adversarial evaluation**

- Prompt injection and jailbreak coverage: [what was tested, by whom, when]
- Red team findings and dispositions: [link]
- Abuse cases considered: [the malicious user, not just the confused one]

**Online metrics**

| Metric | Type | Target |
|---|---|---|
| [the metric that says users got value] | Primary | |
| [the metric that says you did no harm] | Guardrail | |

**Launch gate:** [the specific thresholds that, if unmet, mean this does not ship. Name the person who can override, because someone will ask]

## 8. Human oversight

- **Who reviews what, when:** [not "a human is in the loop", but which human, seeing which information, with how long to decide]
- **What the reviewer sees:** [confidence, sources, the input, the alternative]
- **Can they override, and how:** [and is the override logged]
- **Automation bias mitigation:** [what stops the reviewer from rubber-stamping. If nothing does, say so]
- **Kill switch:** [who can disable this in production, by what mechanism, in how long]

## 9. Transparency

- **Does the user know they are interacting with AI?** [where it says so, in what words]
- **Is AI-generated output labelled or marked?**
- **What explanation does an affected person get?** [and can they contest the outcome, and to whom]
- **Documentation published:** [model card, system card, changelog]

## 10. Risks

| Risk | Likelihood | Impact | Mitigation | Owner | Residual risk accepted by |
|---|---|---|---|---|---|
| | L/M/H | L/M/H | | | |

[Include at least: a wrong-output harm, a misuse case, a data protection risk, a dependency risk, and a reputational risk. If a residual risk is being accepted, a named person accepts it. "The team" is not a person.]

## 11. Compliance position

[Link the obligations, do not restate the law. See [eu-ai-act.md](../checklists/eu-ai-act.md) and [nist-ai-rmf.md](../checklists/nist-ai-rmf.md).]

| Question | Answer |
|---|---|
| Our role for this system | Provider / Deployer / Both / Neither |
| Risk classification and the reasoning | |
| Jurisdictions in scope | |
| Obligations triggered | [link to the completed checklist] |
| Impact assessment required? | [DPIA, FRIA, or both. Link when done] |
| Sign-offs required before launch | |

## 12. Monitoring after launch

- **What is logged:** [enough to reconstruct a decision after a complaint, and for how long]
- **Drift detection:** [what is monitored, what threshold alerts, who it pages]
- **Feedback channel:** [how a user reports a bad output, and where it lands]
- **Incident path:** [severity definitions, who is called, and any regulatory reporting clock that starts]
- **Review cadence:** [when this document gets re-read, and by whom]

## 13. Rollout

| Stage | Audience | Entry criteria | Exit criteria | Rollback trigger |
|---|---|---|---|---|
| Internal | | | | |
| Limited | | | | |
| General | | | | |

## 14. Open questions

| Question | Owner | Needed by | Blocking? |
|---|---|---|---|
| | | | |

## Appendix: decision log

| Date | Decision | Alternatives considered | Why | Decided by |
|---|---|---|---|---|
| | | | | |

[Keep this. In twelve months, when someone asks why the system works this way, this is the only section anyone will read.]
