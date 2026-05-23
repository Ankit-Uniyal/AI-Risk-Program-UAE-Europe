# 05 - Risk Assessment Methodology

This document defines how to assess, score, and accept risk for any AI system in <ORG>.

## 1. Five-stage methodology

1. **Triage** - confirm the system is in scope and gather first-pass facts (intake form).
2. **Tier classification** - assign Prohibited / High / Limited / Minimal based on the criteria below.
3. **Risk assessment** - score inherent risk across the taxonomy in `03-ai-risk-taxonomy.md`.
4. **Control evaluation** - map applicable controls from `06-control-catalogue.md` and rate their design and operating effectiveness.
5. **Residual-risk acceptance** - formal acceptance by the authorised approver based on residual score versus appetite.

## 2. Tier classification logic

### 2.1 Prohibited (do not build, do not buy)
- Subliminal manipulation harming users.
- Exploitation of vulnerabilities (age, disability, socioeconomic).
- Social scoring by public authorities or for general-purpose scoring with detrimental treatment.
- Real-time remote biometric identification in public spaces (with narrow law-enforcement exceptions in the EU).
- Emotion recognition in workplace or education (EU-prohibited).
- Predictive policing based solely on profiling.
- Untargeted scraping of facial images.
- Biometric categorisation to infer protected characteristics.

### 2.2 High-risk (EU Annex III equivalents + sector overlays)
- AI as a safety component of regulated products (medical devices, vehicles, machinery, toys).
- Critical infrastructure management (water, gas, electricity, traffic, digital).
- Education and vocational training (admissions, scoring, proctoring).
- Employment, worker management, access to self-employment (CV screening, performance, termination).
- Access to essential private and public services (credit scoring, insurance, public benefits, emergency triage).
- Law enforcement (risk assessment of individuals, polygraph, evidence reliability).
- Migration, asylum, border control (visa decisions, risk assessment).
- Administration of justice and democratic processes.
- Biometric identification, categorisation, and emotion recognition (where not prohibited).

### 2.3 Limited risk (transparency obligations)
- Chatbots, virtual assistants (must disclose AI).
- AI-generated or AI-manipulated content (deepfakes - must be labelled).
- Generative AI outputs (machine-readable marking obligations).
- Emotion-recognition outside the prohibited domains (transparency).

### 2.4 Minimal risk
- AI-enabled spam filters, video games, basic personalisation, predictive maintenance, IT operations.

## 3. Inherent-risk scoring (1–5)

Score each dimension. Inherent score = max across dimensions (worst-case anchor).

| Dimension | 1 - Negligible | 3 - Moderate | 5 - Critical |
|---|---|---|---|
| Impact on individuals | No effect | Inconvenience | Loss of rights, safety, livelihood |
| Number affected | <100 | 100–10,000 | >10,000 or vulnerable groups |
| Reversibility | Fully reversible | Partly reversible | Irreversible |
| Autonomy | Decision-support | HITL with override | Fully automated |
| Regulatory exposure | None | Sectoral | Cross-border, multi-supervisor |
| Reputational sensitivity | Internal only | Customer-visible | Media / political |
| Data sensitivity | Public / synthetic | Personal | Special category, children |
| Model opacity | Glass-box | Interpretable | Black-box / foundation model |

## 4. Control effectiveness rating
For each applicable control:
- Design rating: Effective / Partly effective / Ineffective / Not designed.
- Operating rating: same scale, evidenced by testing.
- Composite control score: 0.0 to 1.0 multiplier.

## 5. Residual risk
Residual = Inherent × (1 − weighted control effectiveness). Mapped to a 5-band heat-map (Low, Low-Medium, Medium, High, Critical).

## 6. Acceptance authority
| Residual | Approver |
|---|---|
| Low | Business owner + Head of AI Risk |
| Low-Medium | Head of AI Risk |
| Medium | ARC |
| High | ARC + BRC notification |
| Critical | BRC approval required; default = do not deploy |

## 7. Reassessment triggers
- Annual minimum for Limited/Minimal; semi-annual for High.
- Retraining, fine-tuning, prompt-template change.
- New data source, new jurisdiction, new user population.
- Regulatory change.
- Incident or near-miss.
- Vendor / foundation-model version change.

## 8. Documentation
Every assessment produces:
- AI Impact Assessment (template in `templates/ai-impact-assessment.md`).
- Updated model and data cards.
- Risk-acceptance memo signed by the approver.
- Entry in the AI inventory.
