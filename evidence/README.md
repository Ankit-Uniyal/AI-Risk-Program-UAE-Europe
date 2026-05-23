# Evidence Folder

This folder is the **evidence vault** referenced by every `evidence_artifact` path in `toolkit/04-risk-register.csv` and `toolkit/05-treatment-plan.csv`.

## Convention

```
evidence/
  <AI-ID>/
    <YYYY-MM-DD>-<artifact-name>.<ext>
```

Examples (matching seed rows in the worked example):

```
evidence/AI-2026-0001/2026-05-28-vendor-confirmation-features.eml
evidence/AI-2026-0001/2026-06-15-bias-test-q2-2026.pdf
evidence/AI-2026-0001/2026-06-22-pentest-2026-Q2.pdf
evidence/AI-2026-0001/2026-06-28-vendor-addendum-signed.pdf
evidence/AI-2026-0001/2026-07-10-portal-screenshot.png
evidence/AI-2026-0001/2026-08-15-notice-v3.pdf
evidence/AI-2026-0001/2026-08-31-training-completion-log.xlsx
evidence/AI-2026-0002/2026-02-25-architecture-rag-v2.pdf
evidence/AI-2026-0002/2026-03-28-evals-weekly.xlsx
```

## What goes here
- Test reports (bias, fairness, robustness, security pen tests, red-team).
- Signed approvals (DPIA, ARC sign-off, vendor addendum, model card).
- Screenshots of UI disclosures, banners, candidate portals.
- Evaluation outputs and dashboards (CSV/XLSX/PDF).
- Training completion logs.
- Vendor questionnaire responses.
- Incident reports and post-mortems.

## What does NOT go here
- **Personal data** of any kind (no raw CVs, no candidate identifiers, no end-user PII).
- Live credentials, API keys, model weights, or proprietary training data.
- Anything subject to legal hold without coordination with Legal.

## Access and retention
- Access is restricted to AI Risk team, DPO, CISO, Internal Audit, and named approvers per use case.
- Retention follows the records-management policy: minimum 7 years from the date the related AI system is retired.
- All evidence files are immutable — corrections are added as new dated files, never overwritten.

## In this repository
This is a **placeholder folder**. In a real deployment, replace this folder with your organisation's evidence store (SharePoint, S3, Drive, GRC platform) and update the paths in the CSVs accordingly. The folder structure convention should stay the same so the CSVs do not need re-mapping.

## Cross-references
- Risk register: `toolkit/04-risk-register.csv` (`controls_in_place` evidence implied per risk)
- Treatment plan: `toolkit/05-treatment-plan.csv` (`evidence_artifact` column points here)
- Workbook acceptance memos: `toolkit/03-risk-assessment-workbook.md` Section D
- Board reports: `toolkit/06-board-report.md` (audit trail of decisions)
