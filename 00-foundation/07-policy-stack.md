# 07 — Policy Stack

The policy stack is the **written set of binding rules** that translate the Charter into day-to-day behaviour. Approve each policy at the appropriate authority level and publish on the enterprise policy portal.

## Layer 1 — Apex policy

### 1. AI Policy (enterprise)
- Statement of principles (lawful, ethical, robust).
- Scope and applicability across BUs and subsidiaries.
- Risk appetite and prohibited practices.
- Governance bodies and authority.
- Reference to all lower-layer policies and standards.
- Owner: CAIO / CRO. Approver: Board.

## Layer 2 — Functional policies

### 2. Acceptable Use of AI (employee-facing)
- Approved enterprise tools (e.g., enterprise GenAI workspace).
- Prohibited inputs: customer PII, financial data, source code without approval, regulated data classes.
- Required disclosures when AI output is reused externally.
- Verification and human review obligations for outputs.
- Disciplinary consequences.
- Owner: CISO + Head of HR. Approver: ExCo.

### 3. Model Risk Management Policy
- Definition of model and AI system.
- Model lifecycle: development, validation, approval, monitoring, retirement.
- Independence requirements for validation.
- Materiality tiers and review cadence.
- Documentation and challenger model requirements.
- Owner: Model Risk Manager. Approver: BRC.
(Mandatory for CBUAE-regulated entities.)

### 4. AI Data Policy
- Lawful basis and data categories.
- Provenance, licensing and copyright clearance.
- Special-category and children's data restrictions.
- Synthetic-data rules.
- Cross-border transfer mechanisms.
- Owner: CDO + DPO. Approver: ExCo.

### 5. Third-Party / Vendor AI Policy
- Procurement gate triggers (AI keyword detection).
- Mandatory due-diligence questionnaire.
- Contract clauses required.
- Concentration and exit planning.
- Owner: CPO + Head of AI Risk. Approver: ExCo.

### 6. Generative AI Policy
- Approved tools and tenancies.
- Prompt hygiene.
- Output validation and disclosure.
- IP and copyright.
- Shadow-GenAI detection and response.
- Owner: CISO + CAIO. Approver: ExCo.

### 7. AI Incident Management Policy
- Definitions: incident, near-miss, serious incident.
- Reporting timelines (internal 24h; regulators per jurisdiction).
- Roles and escalation.
- Owner: Head of AI Risk + CISO. Approver: ExCo.

### 8. AI Records and Retention Policy
- What to retain: technical documentation, logs, model artefacts, training data snapshots, validation evidence.
- Retention periods aligned with EU AI Act Art. 18 (10 years for providers of High-risk).
- Disposal procedures.
- Owner: General Counsel + Head of AI Risk.

### 9. AI Transparency and Disclosure Policy
- When and how to disclose AI use to customers, employees, candidates.
- Deepfake and synthetic-media labelling.
- GenAI marking obligations.
- Owner: CCO + Communications.

### 10. Human Oversight Policy
- Decisions requiring HITL.
- Reviewer competence and training.
- Override and appeal rights.
- Owner: Head of AI Risk + BU heads.

## Layer 3 — Standards and procedures
- AI System Inventory Standard.
- AI Impact Assessment Procedure.
- Model Validation Standard.
- AI Security Standard (aligned to ISO 27001 + AI-specific extensions).
- GenAI Prompt and Output Logging Standard.
- AI Vendor Due-Diligence Procedure.
- AI Incident Runbook.

## Policy lifecycle
- Annual review minimum.
- Out-of-cycle review on regulatory change.
- Version-controlled in a single repository.
- Linked to training modules in `10-training-and-awareness.md`.
