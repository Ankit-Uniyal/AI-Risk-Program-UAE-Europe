# 03 - AI Risk Taxonomy

A comprehensive, industry-neutral taxonomy of AI risks. Each category lists representative scenarios and an indicative risk owner.

## 1. Strategic and business risk
- Misalignment between AI initiatives and corporate strategy.
- Over-reliance on a single foundation-model vendor (concentration risk).
- AI investments failing to deliver measurable value.
- Owner: CAIO, CFO.

## 2. Regulatory and compliance risk
- Breach of EU AI Act prohibitions or High-risk obligations.
- Breach of GDPR / UAE PDPL / DIFC DP Law (automated decision-making, profiling).
- Sector-specific breach: CBUAE model-risk expectations, DOH AI policy, MDR for medical devices.
- Cross-border data transfer breaches.
- Owner: CCO, DPO, General Counsel.

## 3. Model risk
- Model error, instability, drift, concept shift.
- Overfitting / underfitting; poor generalisation to production data.
- Hallucination and confabulation in generative models.
- Inadequate validation, challenger models, back-testing.
- Owner: Model Risk Manager.

## 4. Data risk
- Poor data quality: incomplete, stale, biased, mislabelled.
- Unlawful data sourcing (scraped, unlicensed, copyrighted).
- Sensitive-attribute leakage; re-identification.
- Training-data poisoning.
- Owner: CDO, DPO.

## 5. Bias, fairness and discrimination risk
- Disparate impact on protected groups (gender, age, nationality, disability).
- Proxy discrimination via correlated features.
- Feedback-loop amplification.
- Owner: Head of AI Risk, DEI, Compliance.

## 6. Privacy risk
- Unlawful processing of personal data for training.
- Model memorisation and personal-data extraction attacks.
- Failure to honour data-subject rights (access, erasure, objection).
- Inadequate DPIA / AIIA.
- Owner: DPO.

## 7. Security and cyber risk
- Prompt injection, jailbreak, indirect prompt injection via tools or RAG.
- Model theft, model extraction, model inversion.
- Adversarial examples, evasion, poisoning, backdoors.
- Insecure ML pipelines, exposed model endpoints, supply-chain compromise.
- Owner: CISO.

## 8. Operational and resilience risk
- Inference latency / availability failures.
- Cloud or GPU capacity disruption.
- Vendor outage of foundation model API.
- Inadequate rollback and human fallback.
- DORA-style ICT third-party concentration in the EU.
- Owner: CTO, COO.

## 9. Transparency and explainability risk
- Inability to explain a consequential decision to a customer or regulator.
- Missing model cards, data cards, decision logs.
- Failure to disclose AI interaction or AI-generated content.
- Owner: Head of AI Risk.

## 10. Human-oversight risk
- Automation bias: humans rubber-stamp AI outputs.
- Insufficient training of human reviewers.
- Lack of meaningful override / appeal mechanism.
- Owner: Business Unit head.

## 11. Safety and physical-harm risk
- AI-enabled medical, industrial, robotics, autonomous-vehicle failures.
- Misdiagnosis, mis-triage, dosing error in clinical AI (DOH-relevant).
- Owner: BU head, Safety Officer.

## 12. Ethical and reputational risk
- Use of AI in ways the public would consider unacceptable.
- Sensitive use cases: emotion recognition, social scoring, surveillance.
- Owner: Ethics Panel, CCO, Communications.

## 13. Intellectual-property and copyright risk
- Training-data copyright disputes; output infringement.
- Loss of trade secrets via prompts to third-party LLMs.
- Owner: General Counsel.

## 14. Financial and accounting risk
- Mispriced models in credit, insurance, trading.
- IFRS / IAS implications of capitalised AI assets.
- Owner: CFO.

## 15. Environmental and ESG risk
- Energy / water / carbon footprint of training and inference.
- Owner: Chief Sustainability Officer.

## 16. Generative-AI-specific risk
- Hallucination in customer-facing outputs.
- Unauthorised use of shadow GenAI tools by employees.
- Deepfake misuse (internal and external).
- Output toxicity, bias, defamation.
- Copyright contamination.
- Owner: Head of AI Risk + CISO.

## 17. Agentic-AI-specific risk
- Tool-use chains causing real-world side effects.
- Goal mis-specification, reward hacking.
- Loss of human-in-the-loop.
- Owner: CAIO, CISO.
