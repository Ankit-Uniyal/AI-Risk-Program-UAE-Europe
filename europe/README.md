# Europe Sub-Project

This sub-project overlays the **EU regulatory stack** on the common foundation in `../00-foundation/`.

## Regulatory anchors
- **Regulation (EU) 2024/1689** — the AI Act. Entered into force 1 August 2024. Phased application:
  - 2 February 2025 — prohibitions (Art. 5) and AI literacy (Art. 4).
  - 2 August 2025 — General-Purpose AI (GPAI) obligations and governance provisions.
  - 2 August 2026 — most remaining provisions including High-risk Annex III systems.
  - 2 August 2027 — High-risk systems that are safety components of regulated products (Annex I).
- **GDPR (Regulation (EU) 2016/679)** — lawfulness, DPIA (Art. 35), Art. 22 automated-decision rights.
- **NIS2 (Directive (EU) 2022/2555)** — cybersecurity for essential and important entities; AI systems supporting essential services in scope of incident reporting.
- **DORA (Regulation (EU) 2022/2554)** — ICT third-party risk, including AI vendors, for financial entities.
- **Product Liability Directive (revised) (EU) 2024/2853** — strict liability extended to software, including AI.
- **Cyber Resilience Act (CRA)** — security requirements for products with digital elements, including AI components.
- **Data Act** and **Data Governance Act** — for data sharing and B2B/B2G data access.
- **Sectoral overlays** — Medical Device Regulation (MDR), Machinery Regulation, vehicle type-approval, AML.
- **Standards** — harmonised standards (CEN-CENELEC JTC 21) for conformity presumption; ISO/IEC 42001 for management system; NIST AI RMF as a complementary methodology.

## Files in this folder
- `eu-ai-act-mapping.md` — clause-by-clause control mapping.
- `high-risk-conformity-checklist.md` — what to evidence for a High-risk system.
- `gpai-obligations.md` — provider and deployer obligations for general-purpose AI.
- `roadmap-europe.md` — phased programme delivery aligned to the AI Act dates.

## Supervisory landscape
- **European AI Office** at the Commission — supervises GPAI providers and coordinates the AI Board.
- **National Competent Authorities (NCAs)** — designated by each Member State; market surveillance for High-risk systems.
- **Sector regulators** — ECB / EBA / SSM (banking), EIOPA (insurance), ESMA (markets), EMA / national medicines agencies, ENISA (cyber), EDPB / national DPAs (data).
- **Notified Bodies** — third-party conformity assessment where required (e.g., remote biometric identification, certain product-safety AI).

## Programme implications
- Treat the AI Act as the **anchor regulation** but plan for parallel obligations: GDPR, NIS2, DORA, MDR, CRA.
- For financial entities, **DORA + AI Act + Model Risk** combine into a single oversight stream.
- For medical entities, **MDR + AI Act + DOH (if also operating in Abu Dhabi)** combine.
- Plan technical documentation to satisfy **Annex IV** plus DPIA plus DORA register simultaneously to avoid duplicate evidence.
