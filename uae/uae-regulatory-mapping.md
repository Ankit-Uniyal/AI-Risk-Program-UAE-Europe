# UAE — Regulatory Control Mapping

Cross-mapping foundational controls to UAE federal, emirate and free-zone requirements.

| Foundation control | UAE federal | DIFC | ADGM | CBUAE | DOH (AD) | DHA (Dubai) |
|---|---|---|---|---|---|---|
| A1 Risk appetite | UAE Charter principle of accountability | DPL 2020 Art. 14 (privacy by design) | ADGM DP regs | Risk management framework expectations | DOH AI Policy governance section | DHA equivalents |
| A4 Inventory | UAE PDPL Art. 7 (record of processing for personal-data systems) | Reg. 10 register of autonomous systems | Required | Required for IT and model assets | Required for clinical AI | Required |
| B Risk management | UAE Charter | DIFC DPL Art. 14, Reg. 10 risk assessment | Required | CBUAE risk management framework expectations | DOH AI risk-classification | DHA risk-classification |
| C Data governance | UAE PDPL Arts. 6–10 | DIFC DPL Arts. 9–13 | Mirrors DIFC | Data quality and BCBS-aligned data governance expectations | Patient-data sovereignty, MOH licensing | DHA data rules |
| D Tech documentation | UAE Charter transparency | Reg. 10 documentation | Required | Model documentation expectations | DOH AI documentation | DHA documentation |
| E Transparency | UAE Charter transparency principle | DPL transparency obligations | Required | Customer fair-treatment expectations | Patient disclosure | Patient disclosure |
| F Human oversight | UAE Charter human-centricity | Reg. 10 Art. 6 (human review) | Required | Senior-management accountability | Clinician-in-the-loop | Clinician-in-the-loop |
| G Security | UAE Information Assurance Standards (NESA / TDRA) | DIFC DPL Art. 14 | Required | CBUAE Information Security Standard | DOH Information Security Policy | DHA cyber rules |
| H Privacy | UAE PDPL | DIFC DPL + Reg. 10 | ADGM DP regs | Customer data protection requirements | Patient data confidentiality | Patient data confidentiality |
| I Assurance | UAE Charter | DIFC DPL Art. 14(3) audit | Required | CBUAE supervisory inspections | DOH audits | DHA audits |
| J Third-party | UAE PDPL data-processor articles | DIFC DPL Arts. 24–26 | Required | CBUAE outsourcing expectations | DOH vendor approvals | DHA vendor approvals |
| K Monitoring | UAE Charter | Reg. 10 ongoing monitoring | Required | CBUAE BCM and incident reporting | DOH post-implementation monitoring | DHA monitoring |
| L GenAI | UAE Charter — alignment with values | DIFC guidance on GenAI in DP context | — | Customer fair treatment, market conduct | Clinical-decision-support boundaries | Clinical-decision-support boundaries |

## Operating recipe
1. Determine which UAE legal stack(s) apply to each AI system (federal PDPL; DIFC DPL + Reg. 10; ADGM; CBUAE; DOH; DHA).
2. Layer the relevant requirements on the foundation control catalogue.
3. Where requirements differ across stacks, **apply the strictest** unless conflict requires explicit choice — document the choice.
4. For multinational organisations, **build one global control set** and treat UAE / EU as configuration overlays.

## Specific cross-checks
- **Personal data of UAE residents processed in the EU**: ensure UAE PDPL Art. 22-style transfer mechanism + EU GDPR safeguards.
- **DIFC entities** must additionally comply with DIFC Reg. 10 if any autonomous decision affects individuals.
- **CBUAE-regulated entities** using third-party AI face outsourcing notification and pre-approval thresholds.
- **DOH-licensed entities** must validate clinical AI with safety, efficacy and clinical-evidence requirements **before** deployment.
