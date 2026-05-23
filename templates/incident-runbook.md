# Template — AI Incident Runbook

This runbook is invoked when an AI-related event meets the definition of an incident or near-miss.

## 1. Definitions
- **Event**: anything unexpected detected in AI operation (a drift alert, a complaint, an audit observation).
- **Incident**: an event that has caused or could cause material harm to individuals, the organisation, or third parties. Examples: customer-impact bias, PII exfil via prompt injection, model outage with safety implication, hallucination causing wrong advice.
- **Serious incident** (EU AI Act Art. 73 equivalent): death or serious harm to health; serious disruption of critical infrastructure; serious infringement of fundamental rights; serious harm to property or the environment.
- **Near-miss**: event that could have led to harm but did not, identified before customer impact.

## 2. Roles
- **Incident Commander (IC)**: senior leader on call for AI incidents.
- **AI SME**: data-scientist / MLE owning the affected system.
- **Security IR**: from SOC / CSIRT.
- **Privacy IR**: DPO or delegate.
- **Communications**: internal and external comms.
- **Legal**: regulator notifications.
- **Customer Care**: customer-facing response.

## 3. Severity scale (illustrative)
- Sev-1: Serious incident; immediate executive engagement; regulatory notification likely.
- Sev-2: Material customer impact or significant control failure.
- Sev-3: Limited impact; corrective action within 30 days.
- Sev-4: Near-miss; lessons learned.

## 4. Response phases

### Phase 1 — Detect
- Source: monitoring alert, customer complaint, employee report, regulator notice, media.
- Triage by AI SME and Security IR within 1 hour.
- IC declares incident, sets Sev, opens war room.

### Phase 2 — Contain
- Stop the bleed: take system offline, switch to fallback (rules engine / human-only), disable specific endpoints, revoke API keys.
- Preserve evidence: snapshot logs, model artefacts, prompt history, inference outputs.

### Phase 3 — Investigate
- Determine root cause (data drift, model bug, vendor change, attack, misuse).
- Quantify impact: affected persons, decisions made, monetary exposure.
- Determine notification obligations: regulators (per jurisdiction), data subjects (where required), customers, insurers.

### Phase 4 — Remediate
- Fix root cause; retrain or roll back model; patch pipeline.
- Add detective and preventive controls.
- Update model and data cards.

### Phase 5 — Notify
- EU: serious incident reporting to the relevant authority per Art. 73 timelines (15 days standard; shorter for fatal / widespread).
- UAE: per CBUAE / DOH / DHA / DIFC Commissioner / TDRA expectations; align with operational-risk and DP incident timelines.
- Affected individuals where high risk to rights and freedoms.
- Insurers per policy terms.

### Phase 6 — Close and learn
- Post-incident review (PIR) within 10 working days.
- Lessons learned captured in policy or control updates.
- Risk register updated.
- Tabletop exercise updated with the new scenario.

## 5. Communications templates
- Internal staff comms (do / don't).
- Customer-facing statement (legal-reviewed).
- Regulator notification cover note.
- Board notification one-pager.

## 6. Special incident types

### 6.1 Prompt-injection / jailbreak leading to data exfiltration
- Treat as a privacy and security incident; engage DPO and CSIRT.
- Identify all data potentially exposed.
- Rotate keys and secrets; review guardrail rules.

### 6.2 Generative-AI hallucination causing customer harm
- Withdraw the affected output channel.
- Manual review of recent outputs.
- Communications to affected customers.

### 6.3 Model drift causing systemic bias
- Pause the model; switch to challenger or human review.
- Re-evaluate on protected attributes.
- Engage fairness review board.

### 6.4 Vendor model change without notice
- Treat as a third-party incident; invoke contractual rights.
- Re-validate critical functionality.
- Update vendor scorecard.
