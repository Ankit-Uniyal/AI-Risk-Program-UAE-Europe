# Template — AI Vendor Due Diligence Questionnaire

Issue this questionnaire to any vendor whose product or service uses AI, embeds AI, or processes data through AI. Score answers; track gaps in the procurement workflow.

---

## A. Vendor and product
1. Legal entity name, registered address, regulators:
2. Product name and version under evaluation:
3. Description of AI functionality (what does the AI do?):
4. AI technique(s) used (ML, deep learning, foundation model, RAG, agentic):
5. If foundation model: name, version, provider, hosting region:
6. Is the model fine-tuned on customer data? On what terms?

## B. Data
7. What customer data flows to the AI? (categories, volume, sensitivity)
8. Will customer data be used to train or improve the vendor's models? If yes, on what basis and how can it be turned off?
9. Where is data processed and stored? (regions)
10. Data residency options for EU and UAE customers?
11. Encryption at rest and in transit?
12. Customer-managed keys (BYOK / HYOK) supported?
13. Retention period and deletion guarantees?
14. Sub-processors list and notification process:

## C. Security and resilience
15. SOC 2 Type II, ISO 27001, ISO 27017/18, ISO/IEC 42001 status (and recent reports):
16. Penetration testing cadence; willing to share executive summary?
17. AI-specific threat-modelling: prompt injection, model theft, data poisoning, etc.:
18. Guardrail / content-filter capabilities:
19. Incident response: SLA for notification (e.g., 24h, 72h)?
20. Business continuity / DR posture and RTO/RPO:

## D. Model and lifecycle
21. Documented training data sources?
22. Bias and fairness testing performed? Evidence?
23. Explainability features?
24. Drift monitoring and retraining cadence?
25. Model-change notification: how much advance notice will you give for material model changes?
26. Versioning and rollback support?

## E. Privacy and compliance
27. GDPR / UAE PDPL / DIFC DPL alignment statements?
28. Standard DPA available?
29. Cross-border transfer mechanisms supported?
30. EU AI Act readiness: provider obligations, Code of Practice (if GPAI provider):
31. Children's data handling?

## F. Transparency
32. Will end-users know they are interacting with AI?
33. Watermarking / provenance markers in outputs?
34. Logs of prompts and outputs accessible to the customer?

## G. Contracts
35. Indemnity for IP infringement by outputs?
36. Right to audit (paper-based and on-site)?
37. Right to source code escrow (if appropriate)?
38. Exit and data-portability terms?
39. Limitation of liability — what is the cap?

## H. Ethics and responsible AI
40. Published responsible-AI principles? Link:
41. Internal AI governance and red-team capability:
42. Has the vendor declined any customer requests on ethical grounds?

## I. Concentration and viability
43. Funding runway / public financials:
44. Customer references in our sector:
45. Roadmap alignment with EU AI Act, NIST AI RMF, ISO/IEC 42001:

---

## Scoring
- Each section scored 0–5.
- Mandatory red-flags: failure on items 8, 9, 17, 19, 35, 38, 39 triggers escalation to Head of AI Risk and Legal.
- Composite minimum threshold for High-risk procurement: 80%.
