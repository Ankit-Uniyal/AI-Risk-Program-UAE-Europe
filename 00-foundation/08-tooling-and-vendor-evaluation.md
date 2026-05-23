# 08 - Tooling and Vendor Evaluation

This guide selects tooling for **four control planes**: governance / inventory, model risk, AI security, and observability. It is technology-neutral; replace examples with your shortlist.

## 1. Capability map

| Capability | What it does | Example tools |
|---|---|---|
| AI Governance and Inventory | Inventory, risk register, control evidence, regulator-ready reporting. | Credo AI, Holistic AI, Fairly AI, Saidot, OneTrust AI Governance, IBM watsonx.governance, ServiceNow IRM AI, Collibra AI Governance. |
| Model Lifecycle and MLOps | Track experiments, register models, deploy, monitor. | MLflow, Vertex AI, SageMaker, Azure ML, Databricks MLflow, Weights & Biases, Domino, Dataiku, DataRobot. |
| Bias and Fairness Testing | Detect disparate impact and mitigate. | IBM AIF360, Fairlearn, Aequitas, Holistic AI library, What-If Tool. |
| Explainability | Local and global explanations. | SHAP, LIME, Captum, InterpretML, Alibi, Google Model Cards Toolkit. |
| Data Quality and Lineage | Profile, validate, track datasets. | Great Expectations, Soda, Monte Carlo, Collibra, Alation, OpenLineage. |
| Privacy and PII | Detect, redact, govern PII; DP and synthetic data. | Microsoft Presidio, Google DLP, Skyflow, MOSTLY AI, Tonic, Gretel. |
| LLM Observability and Eval | Trace prompts, evaluate outputs, hallucination metrics. | LangSmith, LangFuse, Arize Phoenix, WhyLabs, TruEra, Helicone. |
| LLM Security / Guardrails | Prompt-injection detection, jailbreak defence, output filtering. | NVIDIA NeMo Guardrails, Lakera Guard, Protect AI, HiddenLayer, Robust Intelligence, Guardrails AI, Rebuff, LLM Guard, Cloudflare AI Gateway. |
| AI Red Teaming | Automated adversarial testing. | Microsoft PyRIT, Garak, Promptfoo, HiddenLayer, CalypsoAI. |
| Shadow GenAI Discovery | Detect unsanctioned tool usage. | Netskope, Zscaler, Harmonic Security, Nightfall, Wing Security. |
| Policy and Awareness | E-learning, attestation, policy distribution. | KnowBe4, OneTrust, Junipr. |

## 2. Evaluation framework

Score each candidate on:
1. **Regulatory fit** - explicit support for EU AI Act, GDPR, ISO/IEC 42001 evidence; UAE data residency.
2. **Coverage** - across lifecycle, model types, and modalities (incl. GenAI).
3. **Integration** - fit with current MLOps, IAM, SIEM, GRC.
4. **Data residency and sovereignty** - UAE North / Frankfurt / Dublin options; on-prem availability.
5. **Security posture** - SOC 2 Type II, ISO 27001, customer data isolation, BYOK.
6. **Total cost of ownership** - licence, implementation, BAU effort.
7. **Vendor viability** - funding, customer base, roadmap, exit risk.
8. **Time-to-value** - pilot in 30/60/90 days.

## 3. RFP must-asks
- Where is data processed and stored? Data-residency options for EU and UAE?
- Customer logical isolation, encryption, key management.
- Sub-processors list; right to object.
- Model-change notification SLA.
- Right to audit and to request independent assurance reports.
- Standard contract clauses for EU AI Act Art. 25 value-chain obligations.
- Indemnity for IP infringement caused by vendor outputs.
- Exit and data-portability terms.
- Roadmap alignment to NIST AI RMF, ISO/IEC 42001, EU AI Act timelines.

## 4. Reference architecture (illustrative)

```
[ Source data ] -> [ Feature store / RAG index ] -> [ Model / LLM ]
                                                      |
            [ Guardrails / DLP / PII redaction ] -----+
                                                      |
                                              [ Inference API ]
                                                      |
                    [ Observability + audit log ] <---+
                                                      |
                                              [ Human reviewer UI ]
                                                      |
            [ Governance plane: inventory, risk, controls, evidence ]
```

## 5. Buy / build / partner heuristic
- **Buy**: governance plane, guardrails, observability - fast-moving, vendor specialisation high.
- **Build**: thin orchestration, business glue, prompts, evaluations - competitive advantage.
- **Partner**: red-team services, ISO/IEC 42001 audit, legal review.

## 6. Open-source baseline (zero-budget start)
- Inventory: Git repo of YAML files + JSON schema validation in CI.
- Model risk: MLflow + Great Expectations.
- Fairness: Fairlearn + Aequitas.
- Explainability: SHAP.
- LLM observability: LangFuse self-hosted.
- Guardrails: Guardrails AI + LLM Guard.
- Red team: PyRIT + Garak + Promptfoo.

This stack proves the program before committing to a commercial governance suite.
