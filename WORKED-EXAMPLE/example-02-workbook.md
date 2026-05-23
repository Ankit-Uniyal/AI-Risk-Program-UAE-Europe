# Worked Example 02 — Risk Assessment Workbook (CV-Screening AI)

Filled-in copy of toolkit/03-risk-assessment-workbook.md for AI-2026-0001 (CV-Screening AI).

Assessor: Ankit U. (AI Risk Lead)
Date completed: 18 April 2026
Workshop participants: Head of HR, HR Operations Manager, DPO, IT Security Lead, Legal Counsel (EU + UAE), TalentRank.ai Customer Success Manager.

---

## Section A — Classification (Tier)

| Question | Answer | Notes |
|---|---|---|
| Does the system make or materially influence decisions about people? | Yes | Influences interview shortlists. |
| Is it used in employment, education, credit, health, insurance, law enforcement, biometrics, or critical infrastructure? | Yes — employment | EU AI Act Annex III §4 (employment, workers management, access to self-employment). |
| Does it process personal data at scale? | Yes | ~18,000 candidates/year. |
| Is it a foundation model or general-purpose AI? | No | Classification model. |
| Could a failure cause physical harm, financial loss, or denial of rights? | Yes — denial of access to employment | Discrimination risk. |

**Final tier: Tier 2 — High risk** (EU AI Act high-risk; GDPR Art. 22 automated decision-making with human-in-the-loop; UAE Charter Principle "Fairness".)

Approver of tier: AI Risk Committee, 22 April 2026.

---

## Section B — Risk Scoring (8 dimensions, 1=low … 5=critical)

| # | Dimension | Score | Rationale |
|---|---|---|---|
| 1 | Fairness & bias | 4 | Training data covers 5 years of hires that historically skewed 68% male in engineering roles. Vendor has not tested on Arabic-language CVs. |
| 2 | Privacy & data protection | 3 | Personal data including nationality and DOB. Cross-border transfer EU→US for vendor analytics (SCCs in place). UAE PDPL transfer needs assessment. |
| 3 | Security | 3 | Vendor SOC 2 Type II. Pen test 8 months old. No customer-managed keys. |
| 4 | Robustness & accuracy | 3 | Vendor reports AUC 0.81 on their benchmark. Not validated on our population yet. |
| 5 | Transparency & explainability | 4 | Candidates not informed CV is scored by AI. No reason codes shown to recruiters. EU AI Act Art. 13 + GDPR Art. 13/22 require disclosure. |
| 6 | Human oversight | 2 | Recruiter reviews every shortlist; can override. Override rate not yet measured. |
| 7 | Accountability & governance | 3 | Business owner named. RACI not signed. Vendor DPA signed; AI addendum pending. |
| 8 | Societal & reputational | 3 | Local media has covered AI-hiring discrimination twice in past year. |

Inherent risk total: 25 / 40 → **High inherent risk**.

---

## Section C — Treatment (Controls)

| Risk dimension | Control(s) chosen | Owner | Due |
|---|---|---|---|
| Fairness & bias | (a) Pre-deployment disparate impact testing across gender, nationality, age (4/5ths rule). (b) Quarterly bias re-test. (c) Exclude photo + DOB from features. | HR Ops + AI Risk | 15 Jul 2026 |
| Privacy | (a) DPIA completed and approved by DPO. (b) Candidate privacy notice updated to disclose AI scoring. (c) UAE PDPL cross-border transfer assessment. | DPO | 30 Jun 2026 |
| Security | (a) Require updated pen test (<6 months). (b) Enable customer-managed KMS keys. (c) Add vendor to continuous monitoring. | CISO | 30 Jun 2026 |
| Robustness | (a) Champion-challenger test on 2,000 of our historical CVs with known outcomes. (b) Accept only if AUC ≥ 0.78 on our data. | Data Science | 31 Jul 2026 |
| Transparency | (a) Add notice in careers portal: "Your application is reviewed with the help of AI." (b) Provide candidates a route to request human-only review (GDPR Art. 22). (c) Recruiter UI shows top 5 features driving each score. | HR + Product | 15 Aug 2026 |
| Human oversight | (a) Recruiter training: AI ranking is advisory. (b) Track and report override rate monthly; investigate if <10%. | HR Ops | Ongoing |
| Accountability | (a) Sign RACI. (b) Vendor AI addendum (EU AI Act + ISO 42001 alignment). (c) Add to AI inventory + risk register. | AI Risk Lead | 30 Jun 2026 |
| Societal | (a) Pre-launch comms plan. (b) Candidate FAQ. | Comms | 20 Aug 2026 |

---

## Section D — Approval

Residual risk after controls (target): 12 / 40 → **Moderate**.

Approval required from: AI Risk Committee (Tier 2 requires ARC sign-off; Tier 3+ would require Board).

| Approver | Role | Decision | Date | Conditions |
|---|---|---|---|---|
| Chair, AI Risk Committee | Chair | Approve with conditions | 25 Apr 2026 | All Section C controls complete before go-live. Bias re-test result tabled at ARC before launch. |
| DPO | Privacy | Approve | 25 Apr 2026 | DPIA signed; candidate notice live before go-live. |
| CISO | Security | Approve | 25 Apr 2026 | KMS keys + fresh pen test before go-live. |
| Head of HR | Business owner | Accept residual risk | 25 Apr 2026 | — |

Go-live conditional on all controls verified. Re-assessment trigger: annual, or sooner if model retrained, vendor changes, or override rate <10%.

---

## Section E — Monitoring (post go-live)

| KPI | Target | Frequency | Owner |
|---|---|---|---|
| Disparate impact ratio (gender, nationality, age groups) | ≥ 0.80 (4/5ths rule) | Quarterly | AI Risk + HR |
| Recruiter override rate | ≥ 10% | Monthly | HR Ops |
| Candidate complaints related to AI | < 5 / quarter | Monthly | DPO |
| Model AUC on rolling 90-day window | ≥ 0.78 | Monthly | Data Science |
| Time-to-shortlist | ≤ 3 days | Monthly | HR Ops |
| Vendor incidents (SOC 2 exceptions, breach) | 0 | Continuous | CISO |

Escalation: any KPI breach for 2 consecutive periods → re-open risk assessment; ARC notified within 5 working days.
