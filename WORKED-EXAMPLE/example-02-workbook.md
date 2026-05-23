# Worked Example 02 — Risk Assessment Workbook (CV-Screening AI)

Filled-in copy of `toolkit/03-risk-assessment-workbook.md` for AI-2026-0001 (CV-Screening AI). Sections, tier labels, and scoring method mirror the toolkit exactly (Tier 1 Prohibited / Tier 2 High-risk / Tier 3 Limited / Tier 4 Minimal; inherent score = sum of 8 dimensions, 8–40 scale).

AI-ID: **AI-2026-0001**  System name: **CV-Screening AI for HR**  Assessor: **Ankit U., AI Risk Lead**  Date: **18 April 2026**

Workshop participants: Head of HR, HR Operations Manager, DPO, IT Security Lead, Legal Counsel (EU + UAE), TalentRank.ai Customer Success Manager.

---

## SECTION A — Tier Classification

**A1. PROHIBITED list** — all N. No subliminal manipulation, no social scoring, no biometric ID, no emotion recognition in workplace (the system does not infer emotion; it scores fit-to-JD).

**A2. HIGH-RISK list** — **Y** on "Employment, worker management, access to self-employment (CV screening, performance, firing)". EU AI Act Annex III §4 applies.

→ **Tier 2 High-risk**. Continue with full assessment.

Recorded Tier: **Tier 2 High-risk**.

---

## SECTION B — Inherent Risk Scoring (8 Dimensions, additive 8–40)

| Dim | Score | Rationale |
|---|---|---|
| B1 Impact | **4** | Affects access to employment for ~18,000 candidates/year. Possible loss of opportunity; dignity impact; some vulnerable applicants. |
| B2 Privacy | **3** | Personal data including nationality, DOB; cross-border EU→US for vendor support (SCCs); UAE PDPL transfer needs assessment. Clear lawful basis. |
| B3 Bias | **4** | Training data is 5 years of hires that historically skewed 68% male in engineering. Vendor has not tested on Arabic-language CVs. Mitigations under development. |
| B4 Security | **3** | Vendor SOC 2 Type II; pen test 8 months old; no customer-managed keys at start. |
| B5 Robustness | **3** | Vendor reports AUC 0.81 on their benchmark; not yet validated on our population; drift monitoring planned. |
| B6 Transparency | **4** | Candidates currently not informed CV is scored by AI; no reason codes shown to recruiters. EU AI Act Art. 13 and GDPR Art. 13/22 require disclosure. |
| B7 Oversight | **2** | Recruiter reviews every shortlist with authority to override. Override rate not yet measured. |
| B8 Vendor | **3** | Series B startup; standard MSA in place; AI addendum pending; concentration risk. |

**Inherent Risk Score = 4 + 3 + 4 + 3 + 3 + 4 + 2 + 3 = 26 / 40 → Medium**

Note: two dimensions at 4 (B1, B3, B6) and no single dimension at 5 — band stays Medium per the workbook, but proximity to the High band (27–32) is noted for ARC.

---

## SECTION C — Controls and Treatment

| Dim ≥ 3 | Control(s) chosen | Owner | Due |
|---|---|---|---|
| B1 Impact | (a) Candidate appeal route (human-only review on request); (b) Recruiter UI shows top-5 features per score; (c) Limited decision autonomy in pilot (shortlist only, no auto-reject) | HR + Product | 15 Aug 2026 |
| B2 Privacy | (a) DPIA signed by DPO; (b) Candidate privacy notice updated to disclose AI scoring; (c) UAE PDPL cross-border transfer assessment; (d) Data minimisation — strip free-text health/family fields before scoring | DPO | 30 Jun 2026 |
| B3 Bias | (a) Pre-deployment disparate-impact test (4/5ths rule) across gender, nationality, age; (b) Exclude photo + DOB from features; (c) Quarterly bias re-test; (d) Fairness-aware retraining trigger when subgroup AUC gap >5% | HR Ops + AI Risk | 15 Jul 2026 |
| B4 Security | (a) Updated pen test (<6 months); (b) Customer-managed KMS keys; (c) Vendor added to continuous monitoring; (d) AI events to SIEM | CISO | 30 Jun 2026 |
| B5 Robustness | (a) Champion-challenger test on 2,000 of our historical CVs; (b) Accept only if AUC ≥ 0.78 on our data; (c) Monthly drift monitor | Data Science | 31 Jul 2026 |
| B6 Transparency | (a) "Your application is reviewed with the help of AI" notice on careers portal; (b) GDPR Art. 22 human-review request route; (c) Model card and data card published internally | DPO + Product | 15 Aug 2026 |
| B8 Vendor | (a) Signed AI addendum (provider obligations, model-change notification, audit rights, escrow, exit); (b) Documented manual fallback shortlisting process | Procurement | 30 Jun 2026 |

All eight rows added to `toolkit/05-treatment-plan.csv` (see WORKED-EXAMPLE/example-04-treatment-plan-extract.csv).

---

## SECTION D — Residual Risk and Approval

| Dimension | Inherent (1–5) | Controls strength | Residual (1–5) |
|---|---|---|---|
| B1 Impact | 4 | High | 2 |
| B2 Privacy | 3 | High | 2 |
| B3 Bias | 4 | High | 2 |
| B4 Security | 3 | Medium | 2 |
| B5 Robustness | 3 | Medium | 2 |
| B6 Transparency | 4 | High | 2 |
| B7 Oversight | 2 | Medium | 2 |
| B8 Vendor | 3 | Medium | 2 |

**Residual Risk Score = 2 + 2 + 2 + 2 + 2 + 2 + 2 + 2 = 16 / 40 → Low-Medium**

### Approval

Required: AI Risk Committee (Tier 2 High-risk; residual Low-Medium still requires ARC because tier is High).

| Approver | Role | Decision | Date | Conditions |
|---|---|---|---|---|
| Chair, AI Risk Committee | Chair | Approve with conditions | 25 Apr 2026 | All Section C controls complete before go-live. Bias re-test result tabled at ARC before launch. |
| DPO | Privacy | Approve | 25 Apr 2026 | DPIA signed; candidate notice live before go-live. |
| CISO | Security | Approve | 25 Apr 2026 | KMS keys + fresh pen test before go-live. |
| Head of HR | Business owner | Accept residual risk | 25 Apr 2026 | — |

Go-live conditional on all controls verified.

---

## SECTION E — Monitoring Plan

| Metric | Cadence | Threshold | Owner |
|---|---|---|---|
| Disparate impact ratio (gender, nationality, age groups) | Quarterly | ≥ 0.80 (4/5ths) | AI Risk + HR |
| Recruiter override rate | Monthly | ≥ 10% | HR Ops |
| Candidate complaints related to AI | Monthly | < 5 / quarter | DPO |
| Model AUC on rolling 90-day window | Monthly | ≥ 0.78 | Data Science |
| Drift indicator (PSI on top features) | Monthly | < 0.2 | Data Science |
| Time-to-shortlist | Monthly | ≤ 3 days | HR Ops |
| Vendor incidents (SOC 2 exceptions, breach) | Continuous | 0 | CISO |
| Guardrail / data-leak events | Real-time | 0 | CISO |

Reassessment triggers: model retrained, prompt or feature change, vendor changes foundation model, new jurisdiction, incident, regulatory change, or 6 months elapsed (Tier 2 cadence).

Next reassessment date: **25 October 2026** (6 months).

---

End of workbook. Inventory updated; risks added to register (R-0001 through R-0005 for this use case); treatments tracked in T-0001 through T-0006.
