# 13 — Internal Audit Plan (Third Line of Defence)

This file defines the third-line assurance plan for the AI Risk Program. It sits independently of the first line (business owners) and the second line (AI Risk team, DPO, CISO), reporting through the Audit Committee.

---

## 1. Purpose

Provide independent, objective assurance to the Board Audit Committee that:
- AI risks are identified, assessed, treated, monitored and reported correctly.
- The controls described in this repository are designed effectively and operating as intended.
- The program meets internal policy, applicable regulation (EU AI Act, GDPR, NIS2, DORA, UAE PDPL, CBUAE, DOH, DIFC, ADGM as relevant), and recognised standards (ISO/IEC 42001, NIST AI RMF).

---

## 2. Scope

In scope:
- The AI inventory and its completeness.
- Tiering decisions for all Tier 2 High-risk systems and a sample of Tier 3 Limited and Tier 4 Minimal.
- Risk assessments, treatment plans, approvals, and acceptance memos.
- Evidence vault contents and traceability.
- Vendor due-diligence completeness.
- Monitoring KPIs and their reporting to ARC and the Board.
- Incident response effectiveness.
- Training completion and effectiveness.

Out of scope (handled by other audit streams):
- General IT controls, cloud security baselines (covered by IT/Cyber audit).
- Data protection programme as a whole (covered by Privacy audit).

---

## 3. Audit universe and cadence

| Theme | Frequency | Last | Next |
|---|---|---|---|
| AI Inventory completeness and accuracy | Annual | — | Q4 2026 |
| AI Risk Assessment quality (sample of Tier 2 + 25% of Tier 3) | Annual | — | Q4 2026 |
| Treatment plan execution and evidence | Semi-annual | — | Q4 2026 |
| Vendor AI due diligence | Annual | — | Q1 2027 |
| Incident response (table-top + real-incident review) | Annual | — | Q1 2027 |
| Monitoring KPIs accuracy and ARC reporting | Annual | — | Q2 2027 |
| Standards alignment (ISO 42001, NIST AI RMF) | Biennial | — | Q3 2027 |
| GenAI and agentic AI thematic | Annual | — | Q4 2026 |

---

## 4. Audit methodology

For every theme:
1. **Plan** — confirm scope, obtain inventory snapshot, define sample, agree timetable with auditees.
2. **Walkthrough** — interview first and second line; verify the documented process.
3. **Test of design** — confirm controls are described, owned, and triggered by appropriate events.
4. **Test of operation** — re-perform a sample, inspect evidence in evidence/ vault, recompute KPIs.
5. **Report** — findings rated Critical / High / Medium / Low; agreed actions with owners and dates.
6. **Follow-up** — verify closure of prior findings before next audit cycle.

Sampling rules:
- Tier 2 High-risk systems: 100% reviewed each year.
- Tier 3 Limited: stratified random sample of 25% per year.
- Tier 4 Minimal: 5% per year.
- Every incident in the prior 12 months: 100%.
- Every overdue treatment beyond 30 days: 100%.

---

## 5. Standards used by Internal Audit

- IIA *Global Internal Audit Standards* (2024).
- IIA *AI Auditing Framework* (where applicable).
- ISO/IEC 42001:2023 clause 9.2 (internal audit of an AIMS).
- NIST AI RMF GOVERN function and the Generative AI Profile.
- Sector standards as applicable (CBUAE governance, DOH compliance audit expectations, DORA Art. 6 ICT internal audit).

---

## 6. Reporting

| Audience | Cadence | Content |
|---|---|---|
| Audit Committee of the Board | Semi-annual | Findings, ratings, management responses, closure status |
| AI Risk Committee | Quarterly | Open findings list; thematic observations |
| CRO and CISO | On every report | Full report with management response |
| External regulator | On request only | Filtered for confidentiality |

All Internal Audit reports related to AI are filed in evidence/internal-audit/ and referenced (by ID only) in toolkit/06-board-report.md.

---

## 7. Independence and competence

- The Head of Internal Audit reports administratively to the CEO and functionally to the Audit Committee Chair.
- Internal Audit does not own first or second line AI controls and does not sign off on AI deployments.
- Each AI-related engagement includes at least one auditor with AI/ML competence (in-house or co-source).
- Internal Audit attends ARC as observer but does not vote.

---

## 8. Year-1 thematic audit (Q4 2026)

The first AI audit will cover:
1. Inventory completeness — sweep against procurement, cloud spend, and BU self-attestation.
2. Tiering quality — re-perform tier decision on all Tier 2 and 10 sampled Tier 3 systems.
3. Treatment evidence — for every closed treatment in the Q3 board report, verify the artefact in the evidence vault.
4. CV-Screening AI (AI-2026-0001) deep-dive — pre- and post-go-live controls operation.
5. GenAI/agentic readiness — test that toolkit/07 is applied to every applicable system.

Estimated effort: 45 auditor-days over 8 weeks. Co-source 10 days of specialist AI assurance from external firm for items 4 and 5.

---

End of internal audit plan.
