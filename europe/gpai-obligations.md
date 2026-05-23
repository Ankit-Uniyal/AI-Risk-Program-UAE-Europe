# General-Purpose AI (GPAI) - Obligations

GPAI model obligations under the EU AI Act apply from **2 August 2025**. Two tiers: GPAI models, and GPAI models with **systemic risk**.

## 1. Who is a GPAI provider?
A provider that develops a general-purpose AI model and places it on the EU market - directly, via API, via library, embedded in a system, or under another label. Open-source models have specific exemptions but **not** if they pose systemic risk.

## 2. Baseline GPAI obligations (Art. 53)
- Technical documentation of the model (training, evaluation, intended use, integration guidance).
- Information for downstream providers integrating the model (capabilities, limitations, evaluations).
- Copyright policy compliant with EU law; honour text-and-data mining opt-outs.
- Summary of training data using the AI Office template.

## 3. Systemic-risk GPAI (Art. 51, 55)
Threshold trigger: cumulative compute used for training above the level set by the Act (10^25 FLOPs, adjustable by the Commission), or designation by the Commission.

Additional obligations:
- Model evaluations including adversarial testing.
- Assessment and mitigation of systemic risks (misuse, CBRN uplift, large-scale manipulation, loss-of-control scenarios for capable agentic systems).
- Serious-incident tracking and reporting to the AI Office.
- Adequate cybersecurity for the model and its physical infrastructure.

## 4. Code of Practice
The General-Purpose AI Code of Practice published by the AI Office provides a practical compliance route. Signing the Code is voluntary but **creates a presumption of conformity** for the relevant obligations. Track:
- Transparency commitments
- Copyright commitments
- Safety and security commitments (for systemic-risk models)

## 5. Obligations on deployers using GPAI in EU operations
- Compliance with Art. 50 transparency obligations if the use is a system that interacts with people, generates synthetic content, or performs emotion recognition / biometric categorisation.
- Marking of AI-generated content (machine-readable + visible label for deepfakes / public-interest text).
- If the GPAI underlies a High-risk system, full High-risk obligations apply to the system layer.

## 6. Internal programme actions
- Maintain a register of all GPAI models used (foundation models, fine-tunes, embeddings).
- Capture provider documentation, model cards, evaluations, and Code-of-Practice signatures.
- For each downstream system, document how baseline GPAI outputs are made safe (guardrails, filters, RAG grounding).
- Treat any internally trained model above the FLOPs threshold as systemic-risk by default and engage Legal early.

## 7. Working with API-based GPAI
- Contract clauses: data residency, training-on-customer-data opt-out, model-change notification, indemnity, audit rights.
- Logging of prompts and outputs in your tenancy (not vendor's).
- Output watermarking and disclosure built into the system layer.
- Exit plan: how would you replace the provider in 90 days?

## 8. Open-source nuance
Truly open-weight models with publicly released weights and architecture receive transparency-rule relief - but NOT if they are systemic-risk. If you fine-tune an open model for a High-risk use case, the **system-level High-risk obligations still apply**.
