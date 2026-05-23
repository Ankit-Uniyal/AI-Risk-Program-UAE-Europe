# Worked Example 05 - Board Report (Q2 2026)

Filled-in copy of `toolkit/06-board-report.md` showing how the CV-Screening AI (AI-2026-0001) and Customer Service Chatbot (AI-2026-0002) appear in quarterly reporting. Tier labels and scoring method match the toolkit (Tier 1 Prohibited / Tier 2 High-risk / Tier 3 Limited / Tier 4 Minimal; inherent/residual scored 8–40 additive).

Period covered: **Q2 / 2026**  Prepared by: **Ankit U., Head of AI Risk**  Date: **5 July 2026**

---

## 1. Headline (3 sentences)

We have 14 AI systems in the inventory; 1 is Tier 2 High-risk (CV-Screening AI), 5 are Tier 3 Limited, 8 are Tier 4 Minimal, and 0 are Tier 1 Prohibited. The CV-Screening AI was approved with conditions by the AI Risk Committee on 25 April 2026 and is on track for 1 September 2026 go-live; residual risk band is Low-Medium after controls (16/40). No material AI incidents this quarter; one regulatory observation (UAE Data Office informal feedback) remains open and is on track for closure in Q3.

---

## 2. Inventory at a glance

| Metric | This quarter | Last quarter | Trend |
|---|---|---|---|
| Total AI systems in inventory | 14 | 9 | ▲ +5 |
| New AI systems this quarter | 5 | 2 | ▲ |
| Retired AI systems this quarter | 0 | 1 | - |
| Tier 1 Prohibited (should always be 0) | 0 | 0 | flat |
| Tier 2 High-risk | 1 | 0 | ▲ +1 |
| Tier 3 Limited | 5 | 3 | ▲ +2 |
| Tier 4 Minimal | 8 | 6 | ▲ +2 |

---

## 3. Residual risk heat-map (count of systems per band)

| Tier | Low (8–14) | Low-Med (15–20) | Medium (21–26) | High (27–32) | Critical (33–40) |
|---|---|---|---|---|---|
| Tier 2 High-risk | 0 | 1 | 0 | 0 | 0 |
| Tier 3 Limited | 3 | 2 | 0 | 0 | 0 |
| Tier 4 Minimal | 8 | 0 | 0 | 0 | 0 |

**Comment:** Portfolio sits in Low / Low-Medium. CV-Screening AI is the only Tier 2 system and is in Low-Medium residual after controls (16/40). No items in Medium or above.

---

## 4. Top 5 residual risks

| # | AI system | Risk | Residual | Owner | Treatment status |
|---|---|---|---|---|---|
| 1 | CV-Screening AI | Lack of candidate transparency (R-0003) | 6 | DPO | In progress - go-live conditional |
| 2 | CV-Screening AI | Disparate impact on female applicants (R-0001) | 8 | Head of HR | In progress - bias test scheduled 15 Jul |
| 3 | Customer Service Chatbot | Hallucinated product details (R-0006) | 6 | Head of CX | Mitigations in production; weekly evals running |
| 4 | CV-Screening AI | Vendor concentration / training-on-customer-data (R-0002) | 6 | Procurement | Addendum signature expected 30 Jun |
| 5 | CV-Screening AI | Low recruiter override rate (R-0005) | 6 | HR Ops Manager | Training scheduled Aug; KPI dashboard build started |

---

## 5. KRIs vs appetite

| KRI | Target | Actual | RAG | Comment |
|---|---|---|---|---|
| % inventory complete | 98% | 100% | 🟢 | Refreshed against procurement and cloud-spend sweep |
| % High-risk with current AIIA | 100% | 100% | 🟢 | CV-Screening AI assessed 18 Apr 2026 |
| % vendors with current AI due-diligence | 95% | 92% | 🟡 | Two minor SaaS vendors with embedded AI features overdue; closure planned Q3 |
| Open material findings (Internal Audit) | 0 | 0 | 🟢 | First thematic audit scheduled Q4 2026 |
| Material AI incidents | 0 | 0 | 🟢 | One minor chatbot incident in Q1 - closed |
| Staff trained in AI literacy | 95% | 84% | 🟡 | AAUP v1.2 training rolled out; completion tracking on |
| % LLM endpoints behind guardrails | 100% | 100% | 🟢 | All four production LLM endpoints fronted by gateway |

---

## 6. Incidents this quarter

| Date | System | Severity | Summary | Root cause | Status |
|---|---|---|---|---|---|
| - | - | - | No material incidents this quarter | - | - |

---

## 7. Regulatory horizon

- EU AI Act: prohibitions in force since 2 Feb 2025; GPAI obligations since 2 Aug 2025; most high-risk obligations apply from 2 Aug 2026. CV-Screening AI go-live (1 Sep 2026) is deliberately scheduled after that date.
- UAE: informal call with UAE Data Office (PDPL) on the CV-Screening AI cross-border transfer. Positive feedback; no requested changes; written confirmation expected Q3.
- DOH Abu Dhabi: no current healthcare AI in the portfolio; monitoring continues.
- CBUAE: no financial-services AI in current scope.
- Standards: ISO/IEC 42001 adoption assessment to begin Q3; NIST AI RMF crosswalk completed and filed under 00-foundation/.

---

## 8. Decisions requested from the Board

| # | Decision needed | Recommendation |
|---|---|---|
| 1 | Note approval of CV-Screening AI (Tier 2) by ARC with conditions | Note and endorse |
| 2 | Note appointment of Internal Audit to perform Q4 2026 thematic review of AI controls | Note |
| 3 | Approve AI Acceptable Use Policy v1.2 (refreshed for GenAI and agentic AI) | Approve |

---

## 9. Forward look (next quarter)

- Verify CV-Screening AI go-live conditions (bias test pass, KMS keys, pen test refresh, candidate notice live, recruiter training 100%).
- Intake and assess Fraud Triage AI (planned Tier 2).
- Publish AI Risk Policy v1.3 with foundation-model / generative-AI annex.
- Kick-off third-line (Internal Audit) AI controls audit.
- Complete UAE Arabic-language safety evaluation for Customer Service Chatbot; UAE launch.

---

Signed: **Ankit U.**, Head of AI Risk  For information: CEO, CRO, CISO, CCO, DPO, General Counsel, Internal Audit

Appendix references (in repo):
- Assessment workbook: WORKED-EXAMPLE/example-02-workbook.md
- Risk register extract: WORKED-EXAMPLE/example-03-risk-register-extract.csv
- Treatment plan extract: WORKED-EXAMPLE/example-04-treatment-plan-extract.csv
- Incident log example: WORKED-EXAMPLE/example-06-incident-log.md
