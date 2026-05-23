# AI Risk Program — UAE & Europe

An **industry-neutral, end-to-end AI Risk Management Program** authored from the perspective of a Chief AI Officer / CISO / CRO with 50 years of cumulative risk experience. It is delivered as **two parallel sub-projects** — **UAE** and **Europe** — that share a common foundation and diverge only where regulation and supervisory expectations differ.

This repository is a **ready-to-fork blueprint**. Replace organisation-specific placeholders, choose your geography, and use the templates from day one.

## 1. Why this repository exists

Most organisations buy AI faster than they govern it. Boards now demand the same rigour for AI that they demand for cyber, credit and operational risk. This repository covers, in one place:

- Governance charter, RACI and three-lines-of-defence model.
- Scope, AI inventory and risk taxonomy.
- Risk assessment methodology (impact, likelihood, control, residual).
- Policy stack — Acceptable Use, Model Risk, AI Data, Third-Party AI, GenAI, Incident, Records, Transparency, Human Oversight.
- Process design — intake, triage, assessment, approval, monitoring, retirement.
- Control catalogue mapped to EU AI Act, NIST AI RMF 1.0, ISO/IEC 42001:2023.
- Tooling and vendor evaluation criteria, including UAE-resident options.
- Metrics, KRIs, board reporting pack.
- Phased 18-month roadmap with quarterly deliverables.

## 2. Sub-projects

| Sub-project | Primary regulatory anchors |
|---|---|
| **Europe** | Regulation (EU) 2024/1689 (the AI Act), GDPR, NIS2, DORA, MDR, Product Liability Directive, CRA, ISO/IEC 42001, NIST AI RMF |
| **UAE** | UAE National AI Strategy 2031, the UAE Charter for the Development & Use of AI, UAE PDPL (Federal Decree-Law 45/2021), CBUAE risk-management, technology and outsourcing expectations, DOH Abu Dhabi Policy on Use of AI in the Healthcare Sector, DIFC Data Protection Law and Regulation 10 on Autonomous & Semi-Autonomous Systems, ISO/IEC 42001 |

## 3. Repository structure

```
AI-Risk-Program-UAE-Europe/
README.md
00-foundation/
  01-program-charter.md
  02-governance-and-raci.md
  03-ai-risk-taxonomy.md
  04-ai-system-inventory-template.md
  05-risk-assessment-methodology.md
  06-control-catalogue.md
  07-policy-stack.md
  08-tooling-and-vendor-evaluation.md
  09-metrics-kris-and-board-reporting.md
  10-training-and-awareness.md
europe/
  README.md
  eu-ai-act-mapping.md
  high-risk-conformity-checklist.md
  gpai-obligations.md
  roadmap-europe.md
uae/
  README.md
  uae-regulatory-mapping.md
  cbuae-financial-sector-addendum.md
  doh-healthcare-addendum.md
  difc-data-protection-addendum.md
  roadmap-uae.md
templates/
  ai-intake-form.md
  ai-impact-assessment.md
  model-card.md
  data-card.md
  vendor-ai-due-diligence.md
  incident-runbook.md
roadmap/
  18-month-master-roadmap.md
```

## 4. How to use this repo

1. **Fork it.** Replace organisation-specific placeholders (`<ORG>`, `<JURISDICTION>`, `<BU>`).
2. **Run the foundation sprint** (`00-foundation/`) — 6 to 8 weeks — to stand up governance, taxonomy, inventory and policies.
3. **Choose your geography** — `europe/` or `uae/` — and overlay the regulatory mapping.
4. **Operationalise** — use the `templates/` for every new AI use case from day one.
5. **Report** — adopt the KRIs in `00-foundation/09-metrics-kris-and-board-reporting.md`.
6. **Plan delivery** — follow `roadmap/18-month-master-roadmap.md`.

## 5. Source anchors

- European Commission — AI Act overview and Regulation (EU) 2024/1689.
- NIST AI Risk Management Framework (AI RMF 1.0) and the Generative AI Profile (NIST AI 600-1).
- ISO/IEC 42001:2023 — Information technology — Artificial intelligence — Management system.
- UAE Artificial Intelligence Office — National Strategy for AI 2031, the UAE Charter for the Development & Use of AI, UAE position on AI policy.
- Central Bank of the UAE — risk management, model risk, technology risk and outsourcing supervisory expectations.
- Department of Health — Abu Dhabi — Policy on Use of Artificial Intelligence in the Healthcare Sector of the Emirate of Abu Dhabi.
- DIFC — Data Protection Law (DIFC Law No. 5 of 2020) and Regulation 10 on the Processing of Personal Data through Autonomous and Semi-Autonomous Systems.

## 6. Disclaimer

This repository is a **reference blueprint**, not legal advice. Validate every control with your General Counsel, DPO, supervisor and external auditor before adoption.

---

*Maintainer: Ankit Uniyal — contributions welcome via pull request.*
