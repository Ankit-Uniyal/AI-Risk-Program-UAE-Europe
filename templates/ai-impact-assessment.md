# Template — AI Impact Assessment (AIIA)

The AIIA is the canonical pre-deployment risk artefact. It supersedes intake once a use case is accepted and combines AI-Act-style risk-management documentation, DPIA elements (for personal-data systems), DIFC Reg. 10 risk assessment (for DIFC), and clinical-risk elements (for healthcare). The template below produces a single document that drives all of these.

---

## 1. System overview
- AI-ID:
- Name and version:
- Owners (business, technical):
- Risk tier (provisional → final):
- Jurisdictions:
- Regulatory anchors (EU AI Act Annex, GDPR Art. 22, UAE PDPL Art. X, DIFC Reg. 10, DOH, CBUAE expectations):

## 2. Purpose and context
- Business purpose:
- Intended users:
- Intended affected persons:
- Foreseeable misuse:
- Out-of-scope uses (explicitly forbidden):

## 3. Stakeholder map
- Internal stakeholders:
- External stakeholders:
- Vulnerable populations:
- Affected workers' representatives (if relevant):

## 4. AI characteristics
- Technique and architecture:
- Foundation model used (if any), version, provider:
- Training, fine-tuning, RAG, agentic capability:
- Decision autonomy:

## 5. Data assessment
- Data categories:
- Lawful basis under each applicable jurisdiction:
- Source and provenance:
- Quality and representativeness:
- Bias analysis on training data:
- Data minimisation and retention:

## 6. Risk assessment (per dimension in `../00-foundation/03-ai-risk-taxonomy.md`)
For each risk dimension: inherent score, controls applied (linked to catalogue), control effectiveness rating, residual score.

| Risk dimension | Inherent | Controls (IDs) | Effectiveness | Residual |
|---|---|---|---|---|
| Strategic |  |  |  |  |
| Regulatory |  |  |  |  |
| Model |  |  |  |  |
| Data |  |  |  |  |
| Bias / fairness |  |  |  |  |
| Privacy |  |  |  |  |
| Security |  |  |  |  |
| Operational |  |  |  |  |
| Transparency |  |  |  |  |
| Human oversight |  |  |  |  |
| Safety |  |  |  |  |
| Ethical / reputational |  |  |  |  |
| IP / copyright |  |  |  |  |
| Environmental |  |  |  |  |
| GenAI-specific |  |  |  |  |
| Agentic-specific |  |  |  |  |

## 7. Fundamental rights impact (EU AI Act Art. 27 where applicable)
- Categories of rights potentially affected:
- Categories of persons potentially affected:
- Frequency and duration of use:
- Specific harms anticipated:
- Mitigations:
- Human-oversight measures:

## 8. DIFC Reg. 10 questions (if DIFC)
- Is the system autonomous or semi-autonomous?
- Logic explanation prepared?
- Human-review pathway designed?
- Bias and accuracy monitoring planned?
- Registered with the Commissioner if required?

## 9. Clinical safety (if healthcare)
- Intended clinical use and population:
- Clinical evidence summary:
- Risk classification:
- Clinician oversight design:
- Patient disclosure:
- Adverse-event reporting wiring:

## 10. Security threat model
- Threat actors and motivations:
- Threats identified (prompt injection, data poisoning, model theft, inversion, evasion, supply-chain):
- Controls and validation evidence:
- Red-team plan:

## 11. Acceptance recommendation
- Residual risk level:
- Conditions of acceptance:
- Required monitoring metrics:
- Reassessment date:
- Approver and date:

## 12. Sign-offs
- Business owner:
- Head of AI Risk:
- DPO (if personal data):
- Model Risk (if material):
- CISO (if material):
- Legal:
- ARC chair:
- BRC (where required):
