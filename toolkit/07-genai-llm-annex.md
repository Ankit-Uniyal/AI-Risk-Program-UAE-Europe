# 07 — GenAI / LLM Annex

Apply this annex to any AI use case that involves a large language model, foundation model, or generative AI (text, image, audio, video, code). It supplements — does not replace — the standard workbook in toolkit/03-risk-assessment-workbook.md.

When to use this annex: if Section F of the intake form names a foundation model OR the AI technique is LLM / RAG / agent / generative, complete this annex in addition to Sections A–E of the workbook.

---

## G1. GenAI-specific scoring overlay

Add these to the relevant Section B dimensions of the standard workbook. If any G-score is higher than the equivalent B-score, use the G-score.

### G1.1 Hallucination risk (replaces / overrides B5 Robustness)
- 1 — Closed-domain, fully grounded, deterministic outputs.
- 2 — RAG-grounded with strong retrieval over curated source; output cited.
- 3 — RAG over mixed-quality sources; some hallucination expected; evaluation in place.
- 4 — Open-domain LLM, partial grounding; hallucination evaluation ad-hoc.
- 5 — Open-domain generative output, no grounding, no hallucination evaluation.

### G1.2 Prompt injection / jailbreak (replaces / overrides B4 Security)
- 1 — No untrusted input reaches the model.
- 2 — Untrusted input passes through a hardened gateway; tested prompt filters.
- 3 — Untrusted input reaches the model with output filters and rate limits.
- 4 — Untrusted input + tool/agent access without strong guardrails.
- 5 — Untrusted input + autonomous tool use, no guardrails, no monitoring.

### G1.3 Training-data and IP exposure (overrides B2 Privacy when the model is trained on customer/proprietary data)
- 1 — No customer or proprietary data sent to the model; no fine-tuning.
- 2 — Customer data used only in-context (RAG / prompt); contractual no-training.
- 3 — Customer data used for fine-tuning on a dedicated instance; access controls in place.
- 4 — Customer data used for fine-tuning on a shared instance, or weak no-training contract.
- 5 — Customer data, including PII or special-category, used to train a model that other tenants may benefit from.

### G1.4 Provenance and disclosure (overrides B6 Transparency for generative outputs)
- 1 — Output is clearly labelled as AI-generated and includes citation/provenance.
- 2 — Output is labelled as AI-generated.
- 3 — AI-use disclosed at the surface level but no per-output labelling.
- 4 — AI use not disclosed to end-users.
- 5 — Output is presented as human-authored and could be used to deceive (EU AI Act Art. 50).

---

## G2. Mandatory GenAI controls (always required if this annex applies)

| # | Control | Evidence |
|---|---|---|
| G2.1 | LLM gateway with prompt/response logging, rate limits, abuse detection, and content filters | Gateway config + sample log |
| G2.2 | System prompt versioning under change-management; production prompts stored in a controlled repo | Prompt repo + change log |
| G2.3 | Evaluation harness with a frozen gold set (≥ 100 items) run on every prompt or model change; pass-rate threshold defined | Eval results + thresholds |
| G2.4 | Hallucination test against the gold set; minimum acceptable pass rate documented | Eval results |
| G2.5 | Red-team test pre-launch covering prompt injection, jailbreak, data exfiltration, IP exposure, harmful content, bias | Red-team report |
| G2.6 | Output filters: PII, profanity, regulated content (legal/medical/financial advice), and policy-violation classes | Filter config + test cases |
| G2.7 | Disclosure to end-users that output is AI-generated; provenance/watermarking where the EU AI Act Art. 50 applies | UI screenshots |
| G2.8 | Vendor / provider obligations: model-change notification, training-data sourcing statement, copyright indemnity, exit/portability | Contract addendum |
| G2.9 | Incident playbook updated to cover GenAI-specific events (mass hallucination, prompt-injection breach, IP leak, harmful output) | Updated runbook |
| G2.10 | Tokens/cost limits per user per day; alerting on spend anomalies | Cost dashboard |

---

## G3. Post-deployment monitoring (in addition to Section E)

| Metric | Cadence | Threshold |
|---|---|---|
| Gold-set pass rate | Weekly | ≥ 95% |
| Prompt-injection attempts blocked vs reaching model | Daily | Blocked ≥ 99% |
| Harmful-content filter hits | Daily | Investigate any spike > 2σ |
| Cost per request | Daily | Investigate > 1.5× baseline |
| User feedback (thumbs up/down) | Continuous | Investigate negative-rate spike |
| Drift in retrieval relevance (RAG) | Weekly | Recall@K ≥ baseline – 5% |
| Vendor model-change notifications | As received | Re-run eval before adopting new version |

---

## G4. EU AI Act and standards alignment

- **General-Purpose AI (GPAI)** providers: Art. 53 obligations apply from 2 Aug 2025 (transparency, copyright policy, model card, training-data summary). Deployers should obtain the provider's GPAI model card before deployment.
- **Systemic-risk GPAI** (Art. 51): additional evaluation, adversarial testing, incident reporting obligations on the provider — request evidence.
- **Art. 50 transparency** for generative content: AI-generated text on matters of public interest must be labelled; deepfakes labelled unless artistic exception applies; emotion recognition disclosure where deployed.
- **NIST AI RMF Generative AI Profile (2024)** — use the four risk categories (confabulation, dangerous content, data privacy, value chain) as a parallel checklist.
- **ISO/IEC 42001** clause 8 (operational planning) — document GenAI-specific operational controls in the AI Management System.

---

## G5. Agentic AI — extra red flags

If the system uses tool-calling, autonomous workflows, MCP, or chains models together, also tick these:

- [ ] The agent can make outbound API calls or write to systems without human approval — increases B7 Oversight to 5.
- [ ] The agent has access to a credential, key, or signed identity — model as privileged service account.
- [ ] The agent can read or modify files outside a sandbox — apply data-access controls per file class.
- [ ] The agent can take actions that have a cost or external effect (sending email, money movement, public posts) — require pre-approval policy and rate limits.
- [ ] Multiple agents communicate with each other — assess emergent behaviour risk.
- [ ] The agent loop has no termination guarantee — require step-budget and kill-switch.

Any tick on G5 → tier escalates to at least Tier 2 High-risk regardless of Section A result.

---

## G6. Documentation deliverables

For every GenAI system, the following must exist alongside the workbook:

- Model card (templates/model-card.md) — covers the provider, version, training-data summary, eval results.
- Data card (templates/data-card.md) — covers any data the deployer adds (RAG sources, fine-tune data).
- Prompt/persona spec — the controlled system prompt or instructions, with version history.
- Eval report — gold-set results + red-team summary.
- DPIA addendum — if personal data is used in prompts or training.

---

End of GenAI/LLM annex. Return to toolkit/03-risk-assessment-workbook.md Section D for approval routing using the higher of the standard score or the G-overlay score.
