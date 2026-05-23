# UAE Sub-Project

This sub-project overlays the **UAE regulatory and supervisory stack** on the common foundation in `../00-foundation/`. The UAE is a federation with **federal** and **emirate-level** layers, and **free zones** (DIFC, ADGM) operating independent civil and common-law regimes — so a single organisation can face multiple parallel frameworks.

## 1. Federal anchors
- **National Strategy for Artificial Intelligence 2031** — sets the policy direction; expects responsible, ethical, and human-centric AI.
- **UAE Charter for the Development and Use of Artificial Intelligence** (issued by the Minister of State for AI) — twelve principles spanning safety, human well-being, transparency, accountability, technological excellence, peaceful coexistence, alignment with values, security and inclusion.
- **UAE Council for AI and Blockchain** — federal coordinating body.
- **Federal Decree-Law No. 45 of 2021 on the Protection of Personal Data (UAE PDPL)** — federal data protection law (applies outside DIFC and ADGM). Articles on automated processing and profiling are directly relevant to AI.
- **Federal Decree-Law No. 34 of 2021 on Combating Rumours and Cybercrimes** — relevant for synthetic media / deepfake harms.
- **Telecommunications and Digital Government Regulatory Authority (TDRA)** — digital identity, cybersecurity policies that affect AI deployments.

## 2. Sectoral anchors
- **Central Bank of the UAE (CBUAE)** — supervisory expectations on governance, risk management, technology and information security, outsourcing, and model risk that apply to licensed financial institutions; AI deployments must fit into the existing risk-management and ICT frameworks. See `cbuae-financial-sector-addendum.md`.
- **Department of Health — Abu Dhabi (DOH)** — **Policy on Use of Artificial Intelligence in the Healthcare Sector of the Emirate of Abu Dhabi** — binding for healthcare providers and payers in Abu Dhabi. See `doh-healthcare-addendum.md`.
- **Dubai Health Authority (DHA)** — equivalent expectations in Dubai for healthcare AI.
- **Securities and Commodities Authority (SCA)** — securities markets including algorithmic and AI-driven trading and advice.
- **Insurance Authority (now under CBUAE)** — insurance underwriting and claims AI.
- **Roads and Transport Authority (RTA)** and federal road authorities — autonomous mobility.

## 3. Free zones
- **DIFC (Dubai International Financial Centre)** — common-law jurisdiction with its own laws.
  - **DIFC Data Protection Law (DPL 2020)** and **Regulation 10 on the Processing of Personal Data through Autonomous and Semi-Autonomous Systems** — the most explicit AI-specific data-protection regulation in the region.
- **ADGM (Abu Dhabi Global Market)** — its own common-law jurisdiction; ADGM's data-protection regulations and FSRA technology risk guidance apply.
- **DIFC Innovation Hub and Dubai Future Foundation** — sandboxes and ethical-AI initiatives.

## 4. Files in this folder
- `uae-regulatory-mapping.md` — control mapping across the UAE stack.
- `cbuae-financial-sector-addendum.md` — banks, finance companies, exchanges, payment providers, insurers.
- `doh-healthcare-addendum.md` — DOH and broader Abu Dhabi healthcare AI requirements.
- `difc-data-protection-addendum.md` — DIFC DPL and Regulation 10 specific obligations.
- `roadmap-uae.md` — phased programme delivery for the UAE.

## 5. Cross-border considerations
- Data residency expectations from CBUAE, DOH and DIFC may **require UAE-resident processing** for certain classes of data.
- Data export to the EU triggers GDPR rules in reverse; adequacy decisions and SCCs apply.
- For groups operating in both EU and UAE, a **single AIIA + DPIA** template with jurisdiction-specific addenda is recommended to avoid duplication.
