# 02 - Governance and RACI

## 1. Governance bodies

### 1.1 Board Risk Committee (BRC)
- Approves the AI Risk Charter, appetite, and policy stack.
- Receives quarterly AI risk dashboard and material incident reports.
- Approves exceptions above the High-risk threshold.

### 1.2 AI Risk Committee (ARC) - executive
- Chair: Chief AI Officer (or CRO + CISO joint chair).
- Members: CDO, CTO, CIO, CCO, DPO, General Counsel, Head of Internal Audit (observer), Head of Procurement, lead Business Unit risk officers.
- Meets monthly. Approves risk tier classifications, conformity assessments, and remediation plans.

### 1.3 AI Risk Working Group (ARWG)
- Working-level forum. Reviews intake queue, triages new use cases, runs the assessment process, prepares ARC papers.
- Chaired by Head of AI Risk. Includes Model Risk, Privacy, Security, Architecture, Procurement, and BU AI champions.

### 1.4 Ethics Advisory Panel (optional but recommended)
- Independent advisers. Reviews ethically sensitive use cases (vulnerable populations, biometric, public-impact).

## 2. Key roles

| Role | Core responsibility |
|---|---|
| Chief AI Officer (CAIO) | End-to-end accountability for AI strategy, value, and risk. |
| Head of AI Risk | Runs the second-line function: standards, assessments, monitoring. |
| Model Risk Manager | Independent validation of models, ongoing performance challenge. |
| Data Protection Officer (DPO) | GDPR / UAE PDPL alignment, DPIA / AIIA sign-off. |
| CISO | Security of AI systems, MLSecOps, threat modelling (prompt injection, data poisoning, model theft). |
| Chief Compliance Officer | Regulatory mapping and supervisor engagement. |
| AI Product Owner (first line) | Owns the use case, the risk, and the controls. |
| ML Engineer / Data Scientist | Builds models per standards; produces model and data cards. |
| Internal Audit | Independent assurance, third line. |
| Procurement | Enforces vendor AI due-diligence gate. |
| Legal | Contracts (AI clauses), IP, liability, copyright. |

## 3. RACI for the AI lifecycle

Legend: R = Responsible, A = Accountable, C = Consulted, I = Informed.

| Lifecycle stage | AI Product Owner | Data Scientist / ML Eng | Head of AI Risk | Model Risk | Privacy / DPO | Security / CISO | Compliance | Legal | Internal Audit | Board / BRC |
|---|---|---|---|---|---|---|---|---|---|---|
| Use-case intake | A | R | C | I | C | C | C | I | I | I |
| Risk tier classification | R | C | A | C | C | C | C | C | I | I |
| Data sourcing & lawful basis | A | R | C | I | A | C | C | C | I | I |
| Model design & training | A | R | C | C | C | C | I | I | I | I |
| Independent validation | C | C | A | R | C | C | I | I | I | I |
| Pre-deployment risk acceptance | A | C | A | C | C | C | C | C | I | I (High-risk) |
| Production deployment | A | R | C | I | I | C | I | I | I | I |
| Monitoring & drift | A | R | C | C | C | C | I | I | I | I |
| Incident response | A | R | C | C | C | A | C | C | I | I |
| Retirement / decommission | A | R | C | I | C | C | I | I | I | I |
| Vendor AI procurement | C | C | A | C | C | C | C | C | I | I |
| Regulatory reporting | C | I | C | I | C | I | A | C | I | I |
| Board reporting | C | I | A | C | C | C | C | I | C | A |

## 4. Decision rights

- Risk tier classification: ARC approves; Head of AI Risk recommends.
- Go-live for High-risk AI: ARC approves; BRC informed; BRC approves for novel public-facing use cases.
- Prohibited practices: blocked by Head of AI Risk; no override available.
- Material exceptions: BRC approval with documented compensating controls and time-bound remediation.

## 5. Escalation path
First line → Head of AI Risk → ARC → BRC → Board.

Material incident (regulatory reportable, safety-related, or media-attention) follows the Incident Runbook (see `templates/incident-runbook.md`) with parallel notification to CRO, CISO, DPO, General Counsel and CEO.
