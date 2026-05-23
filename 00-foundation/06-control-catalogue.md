# 06 — Control Catalogue

A control library cross-mapped to **EU AI Act**, **NIST AI RMF 1.0**, and **ISO/IEC 42001:2023**. Use this as the master list when designing controls for any AI system.

## Control families

### A. Governance and accountability
- A1. Documented AI risk appetite and tier criteria.
- A2. AI Risk Charter approved by Board.
- A3. RACI defined and assigned per AI system.
- A4. AI inventory maintained and refreshed.
- A5. Named human owner for every consequential decision.

Mappings: EU AI Act Art. 9, Art. 17 (QMS), Art. 26 (deployers). NIST AI RMF: Govern function. ISO/IEC 42001: clauses 4–10 (management system).

### B. Risk management
- B1. AI risk assessment at intake.
- B2. Inherent and residual risk scoring.
- B3. Risk register entry per AI system.
- B4. Reassessment on triggers and on cadence.
- B5. Risk-acceptance memo signed by authorised approver.

Mappings: EU AI Act Art. 9 (risk management system). NIST: Map, Measure, Manage. ISO/IEC 42001: Annex A.6 (AI risk assessment).

### C. Data governance
- C1. Documented lawful basis for personal data used in training and inference.
- C2. Data minimisation and purpose limitation.
- C3. Data quality SLAs: accuracy, completeness, freshness, representativeness.
- C4. Bias and representativeness testing of training datasets.
- C5. Data lineage and provenance recorded.
- C6. Synthetic-data governance.
- C7. Data card maintained per dataset.

Mappings: EU AI Act Art. 10 (data and data governance). GDPR Arts. 5, 6, 9, 25, 35. ISO/IEC 42001 Annex A.7.

### D. Technical documentation and records
- D1. Technical documentation per EU AI Act Annex IV (for High-risk).
- D2. Model card per system.
- D3. Logging of inputs, outputs, decisions for traceability (Art. 12 logs).
- D4. Retention period defined and enforced.

Mappings: EU AI Act Arts. 11, 12, 18. ISO/IEC 42001 Annex A.8.

### E. Transparency and disclosure
- E1. End users informed they are interacting with AI (chatbots, agents).
- E2. AI-generated content marked machine-readable and visibly labelled (deepfakes, public-interest text).
- E3. Customer-facing explanations for adverse decisions.
- E4. Public model card or impact summary for High-risk.

Mappings: EU AI Act Arts. 13, 50, 52. NIST: Govern 4, Manage 4.

### F. Human oversight
- F1. Designated human reviewer with authority to override.
- F2. Reviewer training and bias awareness.
- F3. Override and appeal mechanism documented and tested.
- F4. Stop / kill-switch for production systems.

Mappings: EU AI Act Art. 14. ISO/IEC 42001 Annex A.9.

### G. Accuracy, robustness and cybersecurity
- G1. Accuracy thresholds defined and monitored.
- G2. Robustness testing: adversarial, perturbation, OOD.
- G3. MLSecOps: model registry, signed artefacts, supply-chain integrity (SBOM/MBOM).
- G4. Threat modelling for AI: prompt injection, jailbreak, data poisoning, model theft, inversion, membership inference.
- G5. Red-teaming pre-deployment and ongoing.
- G6. Secrets, keys and credentials management for AI pipelines.
- G7. Output filtering and guardrails (toxicity, PII leakage, jailbreak detection).

Mappings: EU AI Act Art. 15. NIST AI RMF + NIST SP 800-218A (SSDF for AI). OWASP Top 10 for LLM. MITRE ATLAS.

### H. Privacy
- H1. DPIA where required.
- H2. AI Impact Assessment that includes privacy.
- H3. Data subject rights workflow (access, rectification, erasure, objection, automated-decision rights).
- H4. Cross-border transfer mechanism (SCCs, adequacy, BCRs).
- H5. Privacy-enhancing technologies where proportionate (DP, federated, secure enclaves).

Mappings: GDPR Arts. 22, 25, 35, 44–49. UAE Federal Decree-Law No. 45/2021 (PDPL). DIFC DP Law and Regulation 10.

### I. Conformity, assurance and audit
- I1. Pre-deployment conformity check (self-assessment or third-party where required).
- I2. Independent validation by Model Risk.
- I3. Internal Audit programme covers AI.
- I4. External audit / certification (ISO/IEC 42001) where strategic.
- I5. Post-market monitoring plan.
- I6. Serious-incident reporting workflow to relevant authorities.

Mappings: EU AI Act Arts. 17, 43, 44, 61, 73. ISO/IEC 42001 clause 9.

### J. Third-party and supply chain
- J1. AI vendor due-diligence questionnaire.
- J2. Contractual AI clauses: data use, IP, indemnity, audit rights, security, sub-processors, model-change notification.
- J3. Concentration-risk monitoring (single foundation-model provider).
- J4. Exit and portability plan.

Mappings: EU AI Act Art. 25 (providers along the value chain). DORA Arts. 28–30 (ICT third-party). NIST AI RMF 1.3.

### K. Monitoring and post-market
- K1. Performance and drift monitoring.
- K2. Bias monitoring against protected attributes.
- K3. Incident logging and root-cause analysis.
- K4. Periodic revalidation.
- K5. Decommissioning playbook.

Mappings: EU AI Act Arts. 61, 62, 72. ISO/IEC 42001 Annex A.10.

### L. Generative-AI-specific
- L1. System-prompt management and version control.
- L2. RAG source validation and freshness.
- L3. Output watermarking / provenance (C2PA where applicable).
- L4. Prompt-injection defences and red-team coverage.
- L5. GenAI acceptable-use policy with employee attestation.
- L6. Shadow-GenAI discovery and blocking.

Mappings: EU AI Act Arts. 50, 51–55 (GPAI). NIST AI RMF Generative AI Profile (NIST AI 600-1).
