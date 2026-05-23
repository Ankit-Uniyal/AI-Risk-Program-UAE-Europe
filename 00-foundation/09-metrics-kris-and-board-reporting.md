# 09 - Metrics, KRIs and Board Reporting

## 1. Principles
- Few, decision-useful metrics - not vanity counts.
- Mix of leading indicators (KRIs) and lagging indicators (incidents, audit findings).
- Tier-weighted: High-risk systems contribute more to the headline view.
- Trended over time, with appetite thresholds and breach actions.

## 2. Core KRIs

### 2.1 Coverage KRIs
- KRI-01: Percent of known AI systems in the inventory with all mandatory fields populated. Target ≥ 98%.
- KRI-02: Percent of High-risk systems with completed AI Impact Assessment before go-live. Target = 100%.
- KRI-03: Percent of vendors with completed AI due-diligence. Target ≥ 95%.

### 2.2 Lifecycle KRIs
- KRI-04: Percent of High-risk systems with current independent validation (within cadence). Target ≥ 95%.
- KRI-05: Percent of models with drift monitoring in place. Target ≥ 95%.
- KRI-06: Mean age of model card (days since last update). Target ≤ 90 days for High-risk.

### 2.3 Quality and fairness KRIs
- KRI-07: Number of fairness-test breaches per quarter. Target = 0.
- KRI-08: Percent of High-risk systems with documented protected-attribute monitoring. Target = 100%.
- KRI-09: Hallucination / error rate for customer-facing GenAI (model-evaluated and human-spot-checked). Threshold per use case.

### 2.4 Security KRIs
- KRI-10: Number of AI-related security incidents (prompt injection, data exfil, model theft).
- KRI-11: Percent of LLM endpoints behind enforced guardrails. Target = 100%.
- KRI-12: Mean time to detect (MTTD) and mean time to respond (MTTR) for AI incidents.
- KRI-13: Shadow-GenAI use detected per month (trend).

### 2.5 Privacy KRIs
- KRI-14: Number of DPIA-required systems without a current DPIA. Target = 0.
- KRI-15: Data-subject-rights requests resolved within SLA, % .

### 2.6 Compliance KRIs
- KRI-16: Open regulatory observations related to AI.
- KRI-17: Open audit findings related to AI; ageing.
- KRI-18: Percent of staff in AI-handling roles with current training. Target ≥ 95%.

### 2.7 Operational KRIs
- KRI-19: Production AI availability (per system SLA).
- KRI-20: Concentration risk: percent of AI workload on a single foundation-model provider. Threshold per appetite.

## 3. Lagging metrics
- Number of serious incidents (definitions per EU AI Act Art. 73 and equivalents).
- Customer complaints attributable to AI.
- Adverse media events.
- Regulatory fines and enforcement actions.
- Value realised (revenue, cost saved, hours returned) - to balance risk story with business outcome.

## 4. Heat-map structure
2D heat-map: inherent risk (rows) × residual risk (columns), bubble size = number of systems, colour = highest tier. Drill-down to system list per cell.

## 5. Board reporting pack (quarterly)
1. Executive summary (one page).
2. KRI dashboard with appetite breaches and remediation status.
3. Heat-map.
4. Material changes since last quarter (new High-risk systems, vendor changes, regulatory developments).
5. Incident summary (root cause, lessons learned).
6. Regulatory horizon: EU AI Act milestones, UAE / sector developments.
7. Forward look: pipeline of AI use cases and risk implications.
8. Decisions requested.

## 6. Decision thresholds
- Any single High-risk system with residual risk = High → ARC review same month, BRC informed.
- Any Critical residual → automatic BRC paper with go / no-go decision.
- Three or more amber KRIs simultaneously → ARC investigates concentration of weakness.

## 7. Data sources
- Governance tool / inventory.
- MLOps platform (drift, performance).
- LLM observability (hallucination, guardrail events).
- SIEM (AI security events).
- GRC platform (findings, exceptions).
- Procurement (vendor coverage).
- HR LMS (training completion).
