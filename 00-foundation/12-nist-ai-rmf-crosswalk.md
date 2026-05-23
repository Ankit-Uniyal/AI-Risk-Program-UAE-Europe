# 12 - NIST AI RMF 1.0 Crosswalk (incl. Generative AI Profile)

This file maps **NIST AI Risk Management Framework 1.0 (Jan 2023)** plus the **NIST Generative AI Profile (Jul 2024)** to where this program already satisfies them. NIST AI RMF is voluntary; this crosswalk demonstrates methodological alignment for audit, regulator, customer, or partner conversations.

NIST AI RMF organises actions into four functions: **GOVERN, MAP, MEASURE, MANAGE**. The Generative AI Profile adds twelve risk categories on top.

---

## GOVERN - cultivate a culture of risk management

| NIST sub-category | Topic | Where in this repo |
|---|---|---|
| GV-1.1 | Legal and regulatory requirements understood | europe/ (EU AI Act, GDPR, NIS2, DORA); uae/ (CBUAE, DOH, DIFC, PDPL) |
| GV-1.2 | Trustworthiness characteristics integrated | 00-foundation/03-ai-risk-taxonomy.md; toolkit/03-risk-assessment-workbook.md (8 dimensions) |
| GV-1.3 | Risk-tolerance levels set | toolkit/03-risk-assessment-workbook.md (residual bands and approval matrix) |
| GV-1.4 | Risk-management process documented | START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md |
| GV-1.5 | Ongoing monitoring policy | toolkit/03-risk-assessment-workbook.md Section E; toolkit/06-board-report.md |
| GV-1.6 | Inventory of AI systems | toolkit/01-ai-inventory.csv |
| GV-2.1 | Roles, responsibilities and lines of communication | 00-foundation/02-governance-and-raci.md |
| GV-2.2 | Training for AI roles | 00-foundation/10-training-and-awareness.md |
| GV-2.3 | Executive leadership accountability | 00-foundation/01-program-charter.md; toolkit/06-board-report.md |
| GV-3 | Diversity, equity, inclusion in AI teams | 00-foundation/02-governance-and-raci.md (composition guidance) |
| GV-4.1 | Organisational practices for trustworthy AI | 00-foundation/07-policy-stack.md |
| GV-4.2 | Documentation of AI risk-management policies and procedures | The whole repository |
| GV-4.3 | Engagement with AI actors (operators, deployers, providers) | templates/vendor-ai-due-diligence.md; toolkit/02-intake-form.md |
| GV-5 | Engagement with third parties | 00-foundation/08-tooling-and-vendor-evaluation.md; templates/vendor-ai-due-diligence.md |
| GV-6 | Third-party risks addressed | toolkit/03-risk-assessment-workbook.md B8; toolkit/05-treatment-plan.csv vendor controls |

---

## MAP - context recognised and risks identified

| NIST sub-category | Topic | Where in this repo |
|---|---|---|
| MP-1.1 | Intended purpose, beneficial use, context defined | toolkit/02-intake-form.md Sections A–C |
| MP-1.2 | Inter-disciplinary collaboration | 00-foundation/02-governance-and-raci.md (ARC composition) |
| MP-1.3 | Mission and goals understood | 00-foundation/01-program-charter.md |
| MP-1.4 | Business value and risk balance | toolkit/02-intake-form.md Section B |
| MP-1.5 | Organisational risk tolerance documented | toolkit/03-risk-assessment-workbook.md residual bands |
| MP-2.1 | Tasks and methods for AI system documented | templates/model-card.md; templates/data-card.md |
| MP-2.2 | Categorisation of AI systems | toolkit/03-risk-assessment-workbook.md Section A (Tier 1–4) |
| MP-2.3 | AI capabilities, targeted usage, assumptions, limitations documented | templates/model-card.md |
| MP-3.1 | Benefits of intended AI system documented | toolkit/02-intake-form.md Section B |
| MP-3.2 | Potential costs and risks documented | toolkit/03-risk-assessment-workbook.md Sections B–C |
| MP-4.1 | Internal risk controls mapped | 00-foundation/06-control-catalogue.md |
| MP-4.2 | External risks examined | europe/; uae/; toolkit/07-genai-llm-annex.md |
| MP-5 | Impacts to individuals, groups, communities and society characterised | toolkit/03-risk-assessment-workbook.md B1, B3 |

---

## MEASURE - risks analysed, assessed, tracked

| NIST sub-category | Topic | Where in this repo |
|---|---|---|
| MS-1.1 | Approaches and metrics identified | toolkit/03-risk-assessment-workbook.md (B1–B8 scoring) |
| MS-1.2 | Effectiveness of existing controls evaluated | toolkit/03-risk-assessment-workbook.md Section D (residual scoring) |
| MS-2.1 | Test sets, metrics, details of test data documented | templates/data-card.md; toolkit/07-genai-llm-annex.md (gold sets) |
| MS-2.2 | Trustworthy characteristics evaluated | toolkit/03-risk-assessment-workbook.md (8 dimensions) |
| MS-2.3 | Validity and reliability examined | toolkit/03-risk-assessment-workbook.md B5; toolkit/07-genai-llm-annex.md |
| MS-2.4 | Bias and fairness examined | toolkit/03-risk-assessment-workbook.md B3; treatments in toolkit/05 |
| MS-2.5 | Safety examined | toolkit/03-risk-assessment-workbook.md B1, B4 |
| MS-2.6 | Privacy examined | toolkit/03-risk-assessment-workbook.md B2; europe/ GDPR overlay |
| MS-2.7 | Security and resilience examined | toolkit/03-risk-assessment-workbook.md B4; toolkit/07 (prompt injection) |
| MS-2.8 | Explainability and interpretability examined | toolkit/03-risk-assessment-workbook.md B6; templates/model-card.md |
| MS-2.9 | Accountability and transparency | toolkit/03-risk-assessment-workbook.md B6, B7 |
| MS-3 | Mechanisms for tracking risks identified during MAP | toolkit/04-risk-register.csv |
| MS-4 | Feedback about efficacy of measurement | toolkit/06-board-report.md (quarterly review) |

---

## MANAGE - risks prioritised and acted upon

| NIST sub-category | Topic | Where in this repo |
|---|---|---|
| MG-1.1 | Highest-priority risks documented | toolkit/04-risk-register.csv; toolkit/06-board-report.md Section 4 |
| MG-1.2 | Treatment of high-priority risks | toolkit/05-treatment-plan.csv |
| MG-1.3 | Responses to AI risks | toolkit/05-treatment-plan.csv (treatment types: Preventive, Detective, etc.) |
| MG-2.1 | Resources to manage risks allocated | roadmap/18-month-master-roadmap.md |
| MG-2.2 | Mechanisms to manage residual risks | toolkit/03-risk-assessment-workbook.md Section D |
| MG-2.3 | Mechanisms to manage emergent risks | toolkit/03-risk-assessment-workbook.md Section E (reassessment triggers); templates/incident-runbook.md |
| MG-3 | AI risks from third-party entities managed | 00-foundation/08-tooling-and-vendor-evaluation.md; templates/vendor-ai-due-diligence.md |
| MG-4.1 | Post-deployment monitoring planned | toolkit/03-risk-assessment-workbook.md Section E; toolkit/07-genai-llm-annex.md G3 |
| MG-4.2 | Measurable continuous improvement activities | toolkit/05-treatment-plan.csv; 00-foundation/12-internal-audit-plan.md |
| MG-4.3 | Incident response and recovery | templates/incident-runbook.md; WORKED-EXAMPLE/example-06-incident-log.md |

---

## NIST Generative AI Profile (July 2024) - 12 risk categories

| Risk category | Where addressed |
|---|---|
| 1. Confabulation (hallucination) | toolkit/07-genai-llm-annex.md G1.1, G2.4 |
| 2. Dangerous, violent or hateful content | toolkit/07-genai-llm-annex.md G2.5, G2.6 |
| 3. Data privacy | toolkit/03-risk-assessment-workbook.md B2; toolkit/07 G1.3 |
| 4. Environmental impacts | toolkit/07-genai-llm-annex.md G2.10 (cost/energy proxy) |
| 5. Harmful bias and homogenisation | toolkit/03-risk-assessment-workbook.md B3; toolkit/07 G2.5 |
| 6. Human-AI configuration | toolkit/03-risk-assessment-workbook.md B7 |
| 7. Information integrity | toolkit/07-genai-llm-annex.md G1.4 (provenance) |
| 8. Information security | toolkit/03-risk-assessment-workbook.md B4; toolkit/07 G1.2 |
| 9. Intellectual property | toolkit/07-genai-llm-annex.md G2.8 |
| 10. Obscene, degrading, abusive content | toolkit/07-genai-llm-annex.md G2.6 |
| 11. Toxicity, harassment | toolkit/07-genai-llm-annex.md G2.6 |
| 12. Value chain and component integration | toolkit/03-risk-assessment-workbook.md B8; toolkit/07 G2.8 |

---

## How to use this crosswalk

When a regulator, auditor, customer, or board asks "Are you aligned to NIST AI RMF?", give them this file plus the named referenced artefacts. The repository contents are the evidence; this file is the map.

For ISO/IEC 42001 see 00-foundation/11-iso-42001-crosswalk.md.
