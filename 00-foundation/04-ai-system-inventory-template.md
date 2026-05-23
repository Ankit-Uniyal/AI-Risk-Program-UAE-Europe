# 04 - AI System Inventory Template

The inventory is the single source of truth for every AI system in <ORG>. Without an inventory, no other control is enforceable.

## 1. Inventory scope rules
- Every system that ingests data and produces a prediction, classification, generation, recommendation, score, or autonomous action.
- Every embedded ML component in a vendor product.
- Every internal use of a public LLM (ChatGPT, Claude, Gemini, etc.) that touches business data.
- Every agent / copilot / RAG application.
- Every notebook or pipeline that has been promoted past prototype.

## 2. Mandatory fields

| Field | Description | Example |
|---|---|---|
| AI-ID | Unique identifier (auto-generated). | AI-2026-0142 |
| System name | Friendly name. | Mortgage Pre-screening Model |
| Business owner | Named accountable executive. | Head of Retail Credit |
| Technical owner | Named MLE / data-science lead. | Jane Smith |
| Business unit | BU code. | RB-CRE |
| Purpose | One-paragraph business purpose. | Pre-score mortgage applications. |
| Intended users | Internal staff, customers, public, supervised by professional. | Underwriters |
| Affected persons | Who is impacted by decisions. | Mortgage applicants |
| Decision type | Fully automated / human-in-the-loop / decision-support. | Decision-support |
| Risk tier | Prohibited / High / Limited / Minimal. | High |
| Jurisdictions | List. | EU, UAE (DIFC) |
| Regulatory anchors | EU AI Act Annex III #5(b), GDPR Art 22, CBUAE MRM. | Annex III 5(b) |
| AI technique | ML type, model family, foundation model used. | Gradient-boosted trees |
| Foundation model | Name, version, provider (if used). | GPT-4o via Azure OpenAI |
| Training data sources | Internal datasets, external feeds, licensed corpora. | CRM, bureau A |
| Personal data | Yes / No, categories, lawful basis. | Yes - Art 6(1)(b) |
| Special category data | Yes / No, justification. | No |
| Deployment environment | On-prem, public cloud region, edge. | Azure UAE North |
| Vendor | Build vs buy vs hybrid. | Hybrid |
| Status | Concept / Build / Validation / Production / Retired. | Production |
| Go-live date | yyyy-mm-dd | 2025-09-15 |
| Last validation date | yyyy-mm-dd | 2026-03-01 |
| Next validation due | yyyy-mm-dd | 2026-09-01 |
| Incident history | Count and severity. | 0 |
| Model card link | URL or path. | /cards/AI-2026-0142.md |
| Data card link | URL or path. | /cards/data-0142.md |
| AIIA link | Link to AI Impact Assessment. | /aiia/0142.md |
| DPIA link | Link to DPIA where required. | /dpia/0142.md |
| Residual risk | Score after controls. | Medium |
| ARC approval | Date and reference. | 2025-09-10 ARC-073 |

## 3. Discovery techniques
- Procurement gate: every purchase order with software or SaaS routed through AI keyword screen.
- Cloud spend analytics: tag all GPU and managed-ML SKUs.
- Network egress monitoring: detect calls to known AI APIs.
- Employee self-attestation campaign with anonymous amnesty period.
- CI/CD scanners: detect ML libraries (transformers, torch, sklearn, langchain).
- Survey to BU heads with mandatory sign-off.

## 4. Refresh cadence
- Tier 1 (High-risk): quarterly attestation.
- Tier 2 (Limited): semi-annual.
- Tier 3 (Minimal): annual.
- Trigger-based refresh: model retraining, vendor change, scope change, incident, regulatory change.

## 5. Tooling options
- Lightweight: SharePoint list, Notion database, Airtable, Confluence.
- Mid-tier: ServiceNow IRM AI module, Archer, OneTrust AI Governance, Collibra AI Governance.
- Enterprise: Credo AI, Holistic AI, Fairly AI, IBM watsonx.governance, ModelOp, Saidot.
- Open-source: a Git-backed YAML registry with CI validation against a JSON schema is sufficient for early stages.

## 6. Sample YAML record
```yaml
ai_id: AI-2026-0142
name: Mortgage Pre-screening Model
business_owner: Head of Retail Credit
risk_tier: High
jurisdictions: [EU, UAE-DIFC]
foundation_model: null
personal_data: true
lawful_basis: contract
status: production
next_validation_due: 2026-09-01
residual_risk: medium
arc_approval: ARC-073-2025-09-10
```
