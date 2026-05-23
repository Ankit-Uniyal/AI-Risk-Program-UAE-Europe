# EU AI Act - Clause-by-Clause Control Mapping

Use this as the working reference when designing controls for an EU-operating AI system. Numbers refer to Regulation (EU) 2024/1689.

| Article | Topic | Applies to | Control reference (this repo) | Evidence required |
|---|---|---|---|---|
| Art. 4 | AI literacy | Providers and deployers | F.1, Section 10 (training) | LMS records, attestations |
| Art. 5 | Prohibited practices | All actors | Tier classification gate (`05-risk-assessment-methodology`) | Tier register, blocking decisions |
| Art. 6 | High-risk classification | Providers | Tier classification | Annex I and Annex III mapping |
| Art. 9 | Risk management system | High-risk providers | B1–B5 | Risk register, AIIA, residual scores |
| Art. 10 | Data and data governance | High-risk providers | C1–C7 | Data card, bias tests, provenance |
| Art. 11 | Technical documentation | High-risk providers | D1, D2 | Annex IV pack |
| Art. 12 | Record-keeping / logs | High-risk providers and deployers | D3 | Immutable inference logs |
| Art. 13 | Transparency and information to deployers | High-risk providers | E1–E4 | Instructions for use, limitations, accuracy |
| Art. 14 | Human oversight | High-risk providers and deployers | F1–F4 | Reviewer SOPs, override evidence |
| Art. 15 | Accuracy, robustness, cybersecurity | High-risk providers | G1–G7 | Test reports, red-team reports, SBOM |
| Art. 16 | Provider obligations (general) | Providers | A1–A5 | QMS evidence |
| Art. 17 | Quality management system | High-risk providers | A2, I1–I3 | QMS manual; ISO/IEC 42001 aligned |
| Art. 18 | Documentation retention | Providers | A4, D4 | 10-year retention proof |
| Art. 19 | Automatically generated logs | Providers | D3 | Log inventory and access controls |
| Art. 20 | Corrective actions and duty of information | Providers | K3, I6 | Incident records, regulator notifications |
| Art. 22 | Authorised representatives | Non-EU providers | A3 | Appointment letter |
| Art. 25 | Responsibilities along the value chain | All actors | J1–J4 | Contracts, value-chain map |
| Art. 26 | Deployer obligations | Deployers | A3, F1, K1–K4 | Deployer instructions, oversight, monitoring |
| Art. 27 | FRIA (Fundamental Rights Impact Assessment) | Public-body deployers and certain private deployers | B1 + AIIA | FRIA document |
| Art. 43–44 | Conformity assessment | High-risk providers | I1–I4 | CA certificate or self-declaration |
| Art. 47 | EU declaration of conformity | High-risk providers | I1 | Signed declaration |
| Art. 48 | CE marking | High-risk providers | I1 | Marking on product / documentation |
| Art. 49 | Registration in the EU database | Providers, public-body deployers | I1 | Database entry ID |
| Art. 50 | Transparency for certain AI systems | Providers and deployers | E1–E4 | Disclosure UX, watermarking |
| Art. 51–55 | GPAI obligations and systemic-risk GPAI | GPAI providers | See `gpai-obligations.md` | Model documentation, copyright policy, evaluations |
| Art. 56 | Codes of practice | GPAI providers | - | Signed code, evidence of adherence |
| Art. 60 | Sandboxes | Optional | - | Sandbox plan |
| Art. 61–62 | Post-market monitoring | High-risk providers | K1–K5 | Monitoring plan and reports |
| Art. 73 | Serious-incident reporting | Providers and deployers | K3, I6 | Notification records |
| Art. 99–101 | Penalties | All | - | (Risk-acceptance memos) |

## Working tips
- Mirror the **Annex IV** outline directly in the technical-documentation template; this avoids re-work later.
- Build the **post-market monitoring plan** at design time, not after go-live.
- For systems that are **also DORA-regulated**, register and document once and produce both views from a single source of truth.
- For systems also covered by **MDR**, sequence the Notified Body engagement carefully - most MDR Notified Bodies are still building AI-Act competence.
