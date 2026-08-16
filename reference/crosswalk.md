# Crosswalk: EU AI Act, NIST AI RMF, ISO/IEC 42001

Useful for exactly one purpose: doing a piece of work once and pointing three audiences at it. Not useful for claiming that satisfying one satisfies another, however much everyone would like that to be true.

> [!IMPORTANT]
> **Every mapping below is inferred.** No standards body publishes a validated three-way crosswalk.
>
> NIST's own EU mapping addresses the **proposed** AI Act from January 2023. It predates the enacted Regulation (EU) 2024/1689 and the 2026 amendments, so it should not be presented as current. And the ISO/IEC 42001 crosswalk hosted at `airc.nist.gov` is **authored by Microsoft**, not NIST. NIST's disclaimer says plainly that inclusion "does not imply NIST endorsement."
>
> What follows is a defensible reading of the three texts by a practitioner. Treat it as a work-planning aid, and take advice before relying on it in a filing.

## The table

| EU AI Act | NIST AI RMF | ISO/IEC 42001 |
|---|---|---|
| **Art. 4** AI literacy | `GOVERN 2.2`, `GOVERN 3.2` | **7.2** Competence, **7.3** Awareness |
| **Art. 5** prohibited practices | `GOVERN 1.1` | **4.1**, **6.1.4**, **A.5** |
| **Art. 6 + Annex III** classification, and the 6(3) derogation | `MAP 1.1`, `MAP 1.5`, `MAP 5.1` | **6.1.2**, **A.5** |
| **Art. 9** risk management system | `MAP 1.1`, `MAP 5.1`, `MEASURE 1.1`, `MANAGE 1.2`, `MANAGE 2.1` | **6.1.1** to **6.1.3**, **8.2**, **8.3**, **A.5** |
| **Art. 10** data governance, bias examination and mitigation, and new **Art. 4a** | `MAP 2.3`, `MEASURE 2.11`, `MANAGE 2.2` | **A.7** Data for AI systems, **8.4** |
| **Art. 11 + Annex IV** technical documentation | `MAP 4.1`, `GOVERN 1.6` | **7.5**, **A.6** |
| **Art. 12 / 19** logging and retention | `MEASURE 3.1`, `MANAGE 4.1` | **7.5.3**, **A.6** &nbsp; **gap, see below** |
| **Art. 13** transparency to deployers | `GOVERN 4.2`, `MAP 3.4` | **A.8** Information for interested parties |
| **Art. 14** human oversight | `MAP 3.5`, `MANAGE 4.1` | **A.9** Use of AI systems |
| **Art. 15** accuracy, robustness, cybersecurity | `MEASURE 2.5`, `2.6`, `2.7` | **A.6.2**, and ISO/IEC 25059 for the quality model |
| **Art. 17** quality management system | `GOVERN 1.2`, `GOVERN 1.4` | Clauses **4 to 10** as a whole. The purpose-built route is **EN 18286:2026** |
| **Art. 26** deployer obligations | `GOVERN 6.1`, `MANAGE 3.1`, `MANAGE 4.1` | **A.9**, **A.10** |
| **Art. 27** FRIA | `MAP 1.1`, `MAP 3.3`, `MAP 5.1`, `MAP 5.2` | **6.1.4** and **8.4** AI system impact assessment, **A.5**, and **ISO/IEC 42005:2025** |
| **Art. 43 / 47 / 48** conformity assessment, DoC, CE marking | *no analogue* | **9.2**, **9.3** internal only &nbsp; **gap** |
| **Art. 49 / 71** EU database registration | `GOVERN 1.6` inventory | *no analogue* &nbsp; **gap** |
| **Art. 50** transparency and synthetic content marking | `MEASURE 2.8`, `GOVERN 4.2` | **A.8** |
| **Art. 53** GPAI documentation, copyright, training data summary | `GOVERN 6.1`, `GOVERN 6.2`, `MAP 4.1` | **A.10**, **A.7** |
| **Art. 55** systemic risk GPAI | `MEASURE 2.7`, `MANAGE 4.1`, `MANAGE 4.3` | AI 100-2 E2025 and AI 600-1 are the substantive references, not 42001 |
| **Art. 72** post-market monitoring | `MANAGE 4.1`, `MEASURE 3.1` | **9.1**, **10.1** |
| **Art. 73** serious incident reporting | `MANAGE 4.3` | **10.2** &nbsp; **gap** |

The strongest row is **Article 9**, because NIST publishes its own AI RMF to ISO/IEC 23894 crosswalk, which supports the NIST to ISO leg independently. The closest genuine one-to-one in the table is **Article 27 to ISO/IEC 42005**, since 42005 is a dedicated AI system impact assessment standard.

## The four gaps that matter

Where "we are ISO 42001 certified" and "we follow the NIST AI RMF" stop being answers and start being conversation. None of these has a voluntary-framework analogue that discharges the legal duty.

1. **Conformity assessment and CE marking.** Articles 43, 47, 48. Neither NIST nor ISO has a notified body equivalent.
2. **Registration in the EU database.** Articles 49 and 71. A public register duty has no analogue at all.
3. **Serious incident notification with statutory clocks.** Article 73: 15 days, 2 days for widespread infringement, 10 days for a death. ISO 10.2 is internal corrective action, which is a different thing.
4. **Runtime logging with a six month minimum retention.** Articles 19 and 26(6). ISO has no explicit runtime logging control.

## Official crosswalks, and what they actually cover

| Crosswalk | Author | Covers |
|---|---|---|
| [AI RMF to OECD, proposed EU AI Act, EO 13960, AI Bill of Rights](https://www.nist.gov/system/files/documents/2023/01/26/crosswalk_AI_RMF_1_0_OECD_EO_AIA_BoR.pdf) | NIST | The **proposed** AI Act, January 2023. Not current |
| [AI RMF to ISO/IEC FDIS 23894](https://www.nist.gov/system/files/documents/2023/01/26/crosswalk_AI_RMF_1_0_ISO_IEC_23894.pdf) | NIST | Risk management. NIST marks it superseded |
| AI RMF to Singapore IMDA AI Verify | NIST | October 2023 |
| AI RMF to ISO/IEC 42001, hosted on nist.gov | **Microsoft** | Often mistaken for a NIST product |

Index: [airc.nist.gov/AI_RMF_Knowledge_Base/Crosswalks](https://airc.nist.gov/AI_RMF_Knowledge_Base/Crosswalks)

There is **no** NIST crosswalk between the AI RMF and either the NIST CSF or the NIST Privacy Framework.

## ISO/IEC 42001 structure, for reference

Requirements are clauses 4 to 10. Annex A carries **38 controls in 9 groups, numbered A.2 to A.10**. A.1 is the annex introduction, not a control group, which is why counting A.1 to A.10 gives the wrong answer of ten.

| Group | Title |
|---|---|
| A.2 | Policies related to AI |
| A.3 | Internal organization |
| A.4 | Resources for AI systems |
| A.5 | Assessing impacts of AI systems |
| A.6 | AI system life cycle |
| A.7 | Data for AI systems |
| A.8 | Information for interested parties |
| A.9 | Use of AI systems |
| A.10 | Third-party and customer relationships |

Note that **Annex B is normative** in 42001, unlike the ISO 27001 and 27002 split. Several widely read vendor pages say all annexes are informative. They are wrong.

Related standards worth knowing: **ISO/IEC 42005:2025** AI system impact assessment, **ISO/IEC 42006:2025** requirements for certification bodies, and **ISO/IEC 23894:2023** risk management guidance, which is a full International Standard and not a Technical Report.

---

<sub>Verified 16 August 2026. The total of 38 controls and the A.2 to A.10 grouping are taken from the standard's own Annex A. The per-group split is not reproduced here because Table A.1 is copyright ISO. Not legal advice.</sub>
