# High-Risk AI Conformity Checklist

Use this as a **pre-deployment gate** for any system classified High-risk under EU AI Act Art. 6.

## 1. Classification confirmed
- [ ] Annex I product safety component? Specify product.
- [ ] Annex III use case? Specify category and item.
- [ ] If Annex III, derogation under Art. 6(3) considered (and documented if claimed).

## 2. Risk-management system (Art. 9)
- [ ] Lifecycle risk-management process documented.
- [ ] Foreseeable misuse considered.
- [ ] Vulnerable populations considered (children, persons with disabilities).
- [ ] Residual risks justified against benefits.

## 3. Data and data governance (Art. 10)
- [ ] Training, validation and testing datasets documented.
- [ ] Data-collection methods and provenance recorded.
- [ ] Data quality and bias examined; statistical properties documented.
- [ ] Special-category data: necessity and safeguards justified.
- [ ] Lawful basis under GDPR confirmed by DPO.

## 4. Technical documentation (Art. 11, Annex IV)
- [ ] System description (purpose, version, providers).
- [ ] Detailed design (architecture, training methodology).
- [ ] Information about data (sources, labelling, cleaning).
- [ ] Validation and testing procedures and results.
- [ ] Cybersecurity measures.
- [ ] Risk-management documentation.
- [ ] Post-market monitoring plan.
- [ ] EU declaration of conformity prepared.

## 5. Logging (Art. 12)
- [ ] Automatic recording of events (inputs, outputs, decisions) configured.
- [ ] Retention period set and access controls in place.
- [ ] Logs immutable and integrity-checked.

## 6. Transparency to deployers (Art. 13)
- [ ] Instructions for use prepared.
- [ ] Performance characteristics, expected lifetime, maintenance documented.
- [ ] Known or foreseeable circumstances of risk to health, safety, fundamental rights documented.
- [ ] Input data specifications described.

## 7. Human oversight (Art. 14)
- [ ] Built-in human-oversight measures described.
- [ ] Reviewer competence and training provided.
- [ ] Override / stop mechanism tested.
- [ ] Automation-bias mitigations documented.

## 8. Accuracy, robustness, cybersecurity (Art. 15)
- [ ] Accuracy levels declared and tested.
- [ ] Robustness to errors, faults, inconsistencies tested.
- [ ] Resilience to attacks tested (adversarial, poisoning, model evasion, confidentiality attacks).
- [ ] Cyber controls aligned to relevant standards (ISO/IEC 27001, NIS2 where applicable).

## 9. Quality management system (Art. 17)
- [ ] QMS documented; ISO/IEC 42001 alignment recommended.
- [ ] Change control, design control, supplier control covered.

## 10. Conformity assessment (Arts. 43–47)
- [ ] Internal control route or Notified Body involvement determined.
- [ ] Conformity assessment completed.
- [ ] EU Declaration of Conformity signed.
- [ ] CE marking applied where applicable.

## 11. Registration (Art. 49)
- [ ] Registered in the EU database before placing on the market / putting into service.

## 12. Deployer obligations (Art. 26)
- [ ] Instructions provided to deployers.
- [ ] Deployer-side monitoring contract clauses in place.
- [ ] FRIA template provided where Art. 27 applies.

## 13. Post-market monitoring (Art. 61)
- [ ] Plan operational from day 1 of go-live.
- [ ] KPIs and triggers defined.
- [ ] Reporting lines clear.

## 14. Serious-incident reporting (Art. 73)
- [ ] Internal pathway tested in tabletop.
- [ ] 15-day / 2-day / immediate-notification thresholds understood.
- [ ] Contact points with NCA established.

## 15. Cross-regulation alignment
- [ ] DPIA completed (if personal data).
- [ ] DORA register entry (if financial entity).
- [ ] MDR conformity (if medical device).
- [ ] NIS2 incident-reporting linkage (if essential / important entity).
