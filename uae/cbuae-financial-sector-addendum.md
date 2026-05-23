# CBUAE — Financial Sector Addendum

This addendum sets the additional expectations for AI deployed in **CBUAE-licensed financial institutions** (banks, finance companies, exchange houses, payment service providers, insurance and reinsurance companies under CBUAE supervision since the integration of the Insurance Authority, and stored-value facilities).

## 1. Governing supervisory expectations (non-exhaustive)
- Corporate governance and senior-management responsibility frameworks.
- Risk-management framework expectations covering credit, market, operational, liquidity, conduct and **technology** risks.
- Outsourcing and third-party risk regulations (notification thresholds and pre-approval for material outsourcing).
- Information Security and Information Technology risk regulations.
- Business Continuity Management standards.
- Consumer protection and market conduct regulations.
- Anti-Money Laundering and Combating the Financing of Terrorism (AML/CFT) — relevant for AI in transaction monitoring and customer screening.
- (Where applicable) Sandbox regulations and FinTech licensing.

Note: AI is not yet covered by a single dedicated CBUAE AI regulation as of the knowledge cutoff. AI must therefore be **mapped into the existing regulatory perimeter** — primarily technology risk, outsourcing, model risk, conduct, and AML.

## 2. Model risk management (MRM)
Apply a model-risk discipline aligned to BCBS principles (e.g., BCBS 239) and US SR 11-7-style validation, adapted for ML/AI:
- Independent validation function reporting to CRO.
- Tiering by model materiality.
- Conceptual soundness, data quality, outcomes analysis, ongoing monitoring.
- Challenger models and stress tests.
- Model inventory shared with the AI inventory (`../00-foundation/04-ai-system-inventory-template.md`).

## 3. Outsourcing of AI
- Pre-notify or seek non-objection from CBUAE for **material** outsourcing arrangements (definitions per CBUAE outsourcing regulations).
- Maintain a written outsourcing policy with concentration limits per provider.
- Right-to-audit and right-to-information clauses must extend to cloud and AI-vendor sub-processors.
- Data residency: sensitive customer data of CBUAE-regulated activities should be processed in a manner compliant with CBUAE expectations (often UAE-resident or carefully justified offshore arrangements).

## 4. Customer fair treatment and explainability
- AI used in credit, pricing, claims, dispute resolution and complaints must produce **decisions that can be explained** to the customer.
- Adverse decisions require a meaningful reason code and a route to human review.
- No protected-attribute discrimination (gender, nationality, religion, age, disability).
- Conduct risk metrics must include AI-driven outcomes.

## 5. AML / sanctions AI
- Model validation must include false-positive / false-negative analysis, threshold calibration, and back-testing against known SARs.
- Tuning changes require independent review and audit-trail.
- Vendor lists, sanctions data and screening logic version-controlled.

## 6. Algorithmic and AI-driven trading / advice
- Pre-deployment testing including stress and stress-to-failure.
- Kill-switches and circuit breakers.
- Real-time monitoring with human override.
- Market-abuse surveillance over algorithm behaviour.

## 7. Generative AI for customer engagement
- Bots in customer-facing roles must clearly disclose AI nature.
- Outputs in financial-advice contexts require strict guardrails — no unlicensed advice.
- Logs retained per CBUAE record-keeping expectations and accessible to compliance.

## 8. Reporting and incident management
- Material AI incidents likely reportable under existing operational-risk and IT-incident expectations.
- AI-incident definitions and timelines integrated with the operational-risk policy.

## 9. Programme actions
- Add CBUAE liaison contact and outsourcing pre-approval tracker to ARC.
- Model Risk Manager appointed (or augmented for AI).
- Customer-fair-treatment KRIs for AI-driven decisions.
- AML AI-validation cycle on calendar.
- Update outsourcing register with all AI vendors and concentration view.
- Engage CBUAE early on novel use cases via the appropriate sandbox or notification pathway.
