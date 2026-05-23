# 11 - ISO/IEC 42001 Crosswalk

This file maps **ISO/IEC 42001:2023 - Information technology - Artificial intelligence - Management system** clauses to where this program already satisfies them. It is a self-attestation crosswalk, not a certification.

Use this when (a) building the case for management certification, (b) answering an audit or regulator question on standards alignment, or (c) showing a vendor / customer that the program follows a recognised AIMS standard.

---

## Clause coverage

| ISO 42001 clause | Topic | Where in this repo |
|---|---|---|
| **4. Context of the organisation** | | |
| 4.1 Understanding the organisation and its context | External / internal issues affecting AIMS | 00-foundation/01-program-charter.md (scope and context) |
| 4.2 Understanding needs and expectations of interested parties | Stakeholder identification | 00-foundation/01-program-charter.md; 00-foundation/02-governance-and-raci.md |
| 4.3 Determining the scope of the AIMS | Scope statement | 00-foundation/01-program-charter.md |
| 4.4 AI management system | Process approach | 00-foundation/05-risk-assessment-methodology.md; the 8-step process in START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md |
| **5. Leadership** | | |
| 5.1 Leadership and commitment | Top-management ownership | 00-foundation/02-governance-and-raci.md (Board / ARC / CRO accountability) |
| 5.2 AI policy | Policy statement | 00-foundation/07-policy-stack.md (AI Acceptable Use Policy) |
| 5.3 Roles, responsibilities, authorities | RACI | 00-foundation/02-governance-and-raci.md |
| **6. Planning** | | |
| 6.1 Actions to address risks and opportunities | Risk-based planning | toolkit/03-risk-assessment-workbook.md; toolkit/04-risk-register.csv |
| 6.1.2 AI risk assessment | Methodology | 00-foundation/05-risk-assessment-methodology.md; toolkit/03-risk-assessment-workbook.md |
| 6.1.3 AI risk treatment | Treatment plan | toolkit/05-treatment-plan.csv; 00-foundation/06-control-catalogue.md |
| 6.1.4 AI system impact assessment (AIIA) | AIIA / DPIA | templates/ai-impact-assessment.md; toolkit/03-risk-assessment-workbook.md |
| 6.2 AI objectives and planning | Measurable objectives | 00-foundation/09-metrics-kris-and-board-reporting.md |
| 6.3 Planning of changes | Change management | toolkit/03-risk-assessment-workbook.md Section E (reassessment triggers) |
| **7. Support** | | |
| 7.1 Resources | Resourcing the AIMS | roadmap/18-month-master-roadmap.md |
| 7.2 Competence | Skills | 00-foundation/10-training-and-awareness.md |
| 7.3 Awareness | Awareness programme | 00-foundation/10-training-and-awareness.md |
| 7.4 Communication | Internal/external communications | 00-foundation/09-metrics-kris-and-board-reporting.md; toolkit/06-board-report.md |
| 7.5 Documented information | Document control | This repository is the documented-information set; commits provide version history. |
| **8. Operation** | | |
| 8.1 Operational planning and control | Run the process | START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md; toolkit/ |
| 8.2 AI risk assessment | Periodic / triggered | toolkit/03-risk-assessment-workbook.md Section E |
| 8.3 AI risk treatment | Implement controls | toolkit/05-treatment-plan.csv; evidence/ |
| 8.4 AI system impact assessment | Performed before deployment | Worked example: WORKED-EXAMPLE/example-02-workbook.md |
| **9. Performance evaluation** | | |
| 9.1 Monitoring, measurement, analysis, evaluation | KPIs / KRIs | toolkit/06-board-report.md Section 5; toolkit/03-risk-assessment-workbook.md Section E |
| 9.2 Internal audit | Third-line audit | 00-foundation/12-internal-audit-plan.md |
| 9.3 Management review | ARC / Board review | toolkit/06-board-report.md (quarterly) |
| **10. Improvement** | | |
| 10.1 Continual improvement | Corrective actions and improvement | toolkit/05-treatment-plan.csv; toolkit/03-risk-assessment-workbook.md (reassessment loop) |
| 10.2 Nonconformity and corrective action | Incidents and findings | templates/incident-runbook.md; WORKED-EXAMPLE/example-06-incident-log.md |

---

## Annex A controls (ISO 42001 Annex A - reference controls)

ISO 42001 Annex A lists ~38 controls grouped into AI-policy, internal organisation, resources, impact assessment, lifecycle, data, information for interested parties, AI system use, and third-party relationships. The mapping below shows which file in this repo carries the evidence:

| Annex A theme | Where evidenced |
|---|---|
| A.2 Policies | 00-foundation/07-policy-stack.md |
| A.3 Internal organisation | 00-foundation/02-governance-and-raci.md |
| A.4 Resources (data, tooling, system, computing, human) | 00-foundation/08-tooling-and-vendor-evaluation.md; 00-foundation/10-training-and-awareness.md |
| A.5 Impact assessment of AI systems | templates/ai-impact-assessment.md; toolkit/03-risk-assessment-workbook.md |
| A.6 AI system lifecycle | toolkit/ (intake → workbook → treatment → monitor → report) |
| A.7 Data for AI systems | templates/data-card.md |
| A.8 Information for interested parties | templates/model-card.md; user-facing disclosure in worked example (toolkit transparency controls) |
| A.9 Use of AI systems | 00-foundation/07-policy-stack.md (Acceptable Use Policy) |
| A.10 Third-party and customer relationships | templates/vendor-ai-due-diligence.md; toolkit/05-treatment-plan.csv vendor controls |

---

## Gaps to certification

If pursuing third-party ISO 42001 certification, the following still need formal evidence beyond this repository:
- Signed top-management commitment statement.
- Formal AI Policy approval minutes.
- Documented competence records per role.
- Two complete cycles of management review with minutes.
- Internal audit programme executed at least once.
- Records of corrective actions closed and verified.

Targeted timeline to close: 6–9 months from program launch (see roadmap/18-month-master-roadmap.md).
