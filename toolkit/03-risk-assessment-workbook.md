# 03 — AI Risk Assessment Workbook

> **How to use:** copy this file into a new doc, rename it `assessment-<AI-ID>.md`, and fill in every section. Each section is self-scoring — just answer the questions and add up the scores as instructed.

**AI-ID:** ____________________
**System name:** ____________________
**Assessor:** ____________________
**Date:** ____________________

---

# SECTION A — Tier Classification

Answer each question Y / N. Stop at the first YES.

### A1. Is this AI used for any of the following (PROHIBITED)?
- [ ] Subliminal manipulation that causes harm
- [ ] Exploiting vulnerabilities of children, elderly, or persons with disabilities
- [ ] Social scoring by public authorities
- [ ] Real-time remote biometric identification in public spaces (outside narrow exceptions)
- [ ] Emotion recognition in the workplace or schools
- [ ] Predictive policing based solely on profiling
- [ ] Untargeted scraping of facial images
- [ ] Biometric categorisation to infer race, political opinions, religion, sexual orientation

If ANY ticked → **Tier 1 Prohibited. STOP. Do not deploy. Inform the sponsor.**

### A2. Does the AI fall in any of the following HIGH-RISK categories?
- [ ] Safety component of a regulated product (medical device, vehicle, machinery, toy)
- [ ] Critical infrastructure management (water, energy, traffic, digital)
- [ ] Education or vocational training (admissions, scoring, proctoring)
- [ ] Employment, worker management, access to self-employment (CV screening, performance, firing)
- [ ] Access to essential services (credit scoring, insurance, public benefits, emergency triage)
- [ ] Law enforcement (risk assessment, evidence reliability)
- [ ] Migration, asylum, border control
- [ ] Administration of justice and democratic processes
- [ ] Biometric identification, categorisation, or emotion recognition (where not prohibited)

If ANY ticked → **Tier 2 High-risk**. Continue with full assessment.

### A3. Does the AI do any of the following (LIMITED-risk transparency)?
- [ ] Chatbot / virtual assistant that interacts with people
- [ ] Generates or manipulates content (images, audio, video, text) that could be mistaken for human-made
- [ ] Performs emotion recognition or biometric categorisation outside prohibited domains

If ANY ticked → **Tier 3 Limited**. Lightweight assessment.

### A4. If none of the above → **Tier 4 Minimal**. Light-touch assessment.

**Recorded Tier: ____________________**

---

# SECTION B — Inherent Risk Scoring (8 Dimensions)

For each dimension below, pick the score that best matches the situation. Write the score in the box. At the end, the **Inherent Risk = the highest single score**.

## B1. Impact on individuals
- 1 — No effect on anyone's rights, safety, finances or wellbeing.
- 2 — Inconvenience only.
- 3 — Material inconvenience or minor financial impact.
- 4 — Loss of access to services, financial loss, dignity impact, or affects vulnerable groups.
- 5 — Safety risk, loss of fundamental rights, or irreversible harm.

**Score B1: __**

## B2. Privacy and data
- 1 — No personal data used.
- 2 — Limited personal data, well-known lawful basis, no sensitive categories.
- 3 — Significant personal data, clear lawful basis, some monitoring needed.
- 4 — Special category data (health, biometric, etc.) or children's data; cross-border processing.
- 5 — Mass personal data with weak lawful basis, or special category at scale.

**Score B2: __**

## B3. Bias and fairness
- 1 — No decision affects different groups differently.
- 2 — Outputs are similar across groups; basic testing done.
- 3 — Some risk of disparate impact; mitigations in place.
- 4 — Known risk of disparate impact; mitigations under development.
- 5 — High risk of disparate impact on protected groups; no mitigation yet.

**Score B3: __**

## B4. Security
- 1 — System is closed, no external inputs, well-protected.
- 2 — Standard enterprise controls in place.
- 3 — Exposed to user inputs (e.g. LLM prompts) with guardrails.
- 4 — Exposed to user inputs without robust guardrails; or supply-chain risk.
- 5 — High-value model with no AI-specific threat mitigation (prompt injection, model theft, poisoning).

**Score B4: __**

## B5. Robustness and accuracy
- 1 — Deterministic logic, accuracy not a concern.
- 2 — Accuracy measured, stable, drift unlikely.
- 3 — Accuracy measured; drift possible; monitoring planned.
- 4 — Accuracy varies; drift expected; monitoring not yet in place.
- 5 — Accuracy unknown or unstable; hallucination risk; no monitoring.

**Score B5: __**

## B6. Transparency and explainability
- 1 — Outputs are fully explainable to a layperson.
- 2 — Outputs are explainable to a domain expert.
- 3 — Outputs explainable with effort; instructions for use published.
- 4 — Black-box model; explanations only at aggregate level.
- 5 — No explanation possible; no disclosure to affected persons.

**Score B6: __**

## B7. Human oversight
- 1 — Every decision reviewed by a trained human with authority to override.
- 2 — Sampling-based human review; clear override path.
- 3 — Human review on exception only; override possible.
- 4 — Limited human review; override slow or unclear.
- 5 — Fully automated decisions; no meaningful human review.

**Score B7: __**

## B8. Vendor and supply chain
- 1 — Fully in-house, no third-party AI.
- 2 — Single trusted vendor with strong contract.
- 3 — Multiple vendors with standard contracts.
- 4 — Critical vendor with weak contract terms; concentration risk.
- 5 — Vendor will train on our data; no model-change notification; no exit plan.

**Score B8: __**

---

## Inherent Risk = MAX of B1..B8 = __

Map to band:
- 1 = **Low**
- 2 = **Low-Medium**
- 3 = **Medium**
- 4 = **High**
- 5 = **Critical**

**Inherent Risk band: ____________________**

---

# SECTION C — Controls and Treatment

For every dimension that scored **3 or higher**, pick the recommended controls below and commit to implementing them. Add each control to `toolkit/05-treatment-plan.csv`.

### If B1 Impact ≥ 3
- [ ] Define meaningful human-review and appeal mechanism.
- [ ] Publish a plain-language explanation for affected persons.
- [ ] Limit decision autonomy until performance proven.

### If B2 Privacy ≥ 3
- [ ] Complete a DPIA (and DIFC Reg. 10 risk assessment if in DIFC).
- [ ] Confirm lawful basis with DPO; document data flow.
- [ ] Apply data minimisation and retention limits.
- [ ] Configure cross-border transfer safeguards.

### If B3 Bias ≥ 3
- [ ] Run bias / fairness tests on training and live data; document results.
- [ ] Monitor outputs by protected attribute proxies.
- [ ] Define re-training trigger on bias breach.

### If B4 Security ≥ 3
- [ ] Threat-model for AI-specific attacks (prompt injection, poisoning, theft).
- [ ] Add guardrails / output filters.
- [ ] Red-team test before go-live.
- [ ] Add AI events to SIEM monitoring.

### If B5 Robustness ≥ 3
- [ ] Define accuracy and drift KPIs; set alert thresholds.
- [ ] Set retraining cadence and trigger.
- [ ] For GenAI: define hallucination evaluation.

### If B6 Transparency ≥ 3
- [ ] Create a model card and a data card.
- [ ] Disclose AI use to end-users in the UI.
- [ ] For GenAI output: mark with provenance / watermark.

### If B7 Oversight ≥ 3
- [ ] Define HITL design and reviewer competence.
- [ ] Train reviewers on automation bias.
- [ ] Build a tested kill-switch.

### If B8 Vendor ≥ 3
- [ ] Complete `templates/vendor-ai-due-diligence.md` questionnaire.
- [ ] Add AI-specific clauses to contract (data use, model-change, indemnity, audit, exit).
- [ ] Set concentration limits with Procurement.

**For every control added: copy a row into `toolkit/05-treatment-plan.csv`.**

---

# SECTION D — Residual Risk and Approval

After committing to the controls above, **re-score the relevant dimensions** assuming the controls are in place and working.

| Dimension | Inherent | Controls strength (Low / Med / High) | Residual |
|---|---|---|---|
| B1 Impact |  |  |  |
| B2 Privacy |  |  |  |
| B3 Bias |  |  |  |
| B4 Security |  |  |  |
| B5 Robustness |  |  |  |
| B6 Transparency |  |  |  |
| B7 Oversight |  |  |  |
| B8 Vendor |  |  |  |

Residual Risk = MAX of residual column = __ ( Low / Low-Med / Medium / High / Critical )

### Approval authority based on residual
| Residual | Who must approve |
|---|---|
| Low | Business owner + Head of AI Risk |
| Low-Medium | Head of AI Risk |
| Medium | AI Risk Committee |
| High | AI Risk Committee + Board notification |
| Critical | Board approval required; default is do-not-deploy |

### Acceptance memo (fill in)
- I/we accept the residual risk identified above for the named AI system, subject to the controls in Section C and the monitoring in Section E.
- Conditions of acceptance: ____________________
- Reassessment due: ____________________
- Approver name and role: ____________________
- Signature and date: ____________________

---

# SECTION E — Monitoring Plan

Pick the metrics relevant to this system and the cadence. These are what you watch after go-live.

| Metric | Cadence | Threshold | Owner |
|---|---|---|---|
| Model accuracy (or task-relevant equivalent) | daily / weekly / monthly |  |  |
| Drift indicator | daily / weekly / monthly |  |  |
| Bias / fairness check | weekly / monthly / quarterly |  |  |
| Hallucination rate (GenAI) | daily / weekly |  |  |
| Guardrail violations (LLM) | real-time |  |  |
| Customer complaints attributable to AI | monthly |  |  |
| Override rate (human reviewer) | weekly / monthly |  |  |
| Security events on AI endpoints | real-time |  |  |
| Vendor model change notifications | as received |  |  |

**Reassessment triggers** (full re-run of Sections A–D when these happen):
- [ ] Model retrained or prompt template changed materially
- [ ] New data source added
- [ ] New jurisdiction added
- [ ] Vendor changed foundation model
- [ ] Incident or near-miss occurred
- [ ] Regulatory change
- [ ] 12 months elapsed (6 months for High-risk)

**Next reassessment date: ____________________**

---

## End of workbook

Update `toolkit/01-ai-inventory.csv` with the final Tier, residual risk, approver, and next-assessment date.
Roll this system's residual score and any open risks into the next quarterly `toolkit/06-board-report.md`.
