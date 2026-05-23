# AI Risk Program — UAE & Europe

A practical, ready-to-use toolkit for designing and running an AI Risk Management program end-to-end. Industry-neutral. Two regional lenses: **UAE** and **Europe**. Built so a CISO, CRO, Chief AI Officer, DPO, Internal Audit lead, or risk analyst can pick it up and **actually run an assessment today**.

---

## ⚡ Start here (5 minutes)

If you only read three things, read these — in this order:

1. **[START-HERE/quick-start.md](START-HERE/quick-start.md)** — what this repo is, who it is for, and the 8-step process in one page.
2. **[START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md](START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md)** — the step-by-step playbook you follow for every new AI use case.
3. **[WORKED-EXAMPLE/](WORKED-EXAMPLE/)** — a fully filled-in assessment for a fictional CV-Screening AI so you can see exactly what "done" looks like before you do your own.

---

## 🧰 The toolkit (the files you actually fill in)

These live in [`toolkit/`](toolkit/) and are deliberately plain — Markdown and CSV — so they open in Excel, Google Sheets, Notion, Jira, or anywhere you already work.

| # | File | What it is | When you use it |
|---|---|---|---|
| 01 | [`toolkit/01-ai-inventory.csv`](toolkit/01-ai-inventory.csv) | One row per AI use case in the organisation | Always-on; first thing you build |
| 02 | [`toolkit/02-intake-form.md`](toolkit/02-intake-form.md) | 12 plain-language questions for the business owner | Whenever a new AI use case appears |
| 03 | [`toolkit/03-risk-assessment-workbook.md`](toolkit/03-risk-assessment-workbook.md) | Tiering + 8-dimension scoring + treatment + approval + monitoring | For every Tier 1+ use case |
| 04 | [`toolkit/04-risk-register.csv`](toolkit/04-risk-register.csv) | Every identified risk, its inherent and residual score | Updated continuously |
| 05 | [`toolkit/05-treatment-plan.csv`](toolkit/05-treatment-plan.csv) | Every control / action with owner, due date, evidence | Updated continuously |
| 06 | [`toolkit/06-board-report.md`](toolkit/06-board-report.md) | One-page quarterly pack for ARC / Board | Quarterly |

A complete worked example of all six is in [`WORKED-EXAMPLE/`](WORKED-EXAMPLE/).

---

## 🗺️ The 8-step process

The toolkit operationalises this loop. The full version (with who does what, when, evidence to keep) is in [START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md](START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md).

1. **Discover** AI in use — inventory
2. **Intake** — business owner answers 12 questions
3. **Classify** — Tier 0 / 1 / 2 / 3
4. **Score** — 8 risk dimensions
5. **Treat** — controls + owners + dates
6. **Approve** — right approver for the tier
7. **Monitor** — KPIs + triggers
8. **Report** — board pack + regulator-ready evidence

---

## 🇦🇪 UAE and 🇪🇺 Europe lenses

The toolkit is region-agnostic. The two sub-projects below give you the regulatory mapping and the deltas you need to drop into the toolkit.

- [`uae/`](uae/) — UAE AI Office Charter, **CBUAE** model risk and tech-risk expectations, **DOH** Abu Dhabi AI guidance, DIFC, UAE PDPL, sector-specific notes.
- [`europe/`](europe/) — EU AI Act (incl. timeline), GDPR Art. 22, NIST AI RMF crosswalk, ISO/IEC 42001, sectoral overlays (EBA, EIOPA, EMA).

---

## 📚 Reference foundation

Background and design rationale — read only if you need it.

- [`00-foundation/`](00-foundation/) — governance charter, RACI, three-lines model, risk taxonomy, policies.
- [`templates/`](templates/) — additional templates (policies, model cards, DPIA, vendor questionnaire).
- [`roadmap/`](roadmap/) — 12-month implementation roadmap.

---

## How to use this repository

**Fork it.** Replace organisation-specific placeholders. Start with your three highest-risk AI use cases. Run them through the 8-step process using the toolkit. Bring the worked example to your first AI Risk Committee so the format is agreed before debate begins.

**Read order for a first-time user:**
1. `START-HERE/quick-start.md`
2. `START-HERE/HOW-TO-RUN-AN-ASSESSMENT.md`
3. `WORKED-EXAMPLE/example-01-intake.md` → `example-02-workbook.md` → `example-05-board-report.md`
4. Then open the blank toolkit files in `toolkit/` and start your own.

---

## Sources (authoritative only)

EU AI Act (eur-lex.europa.eu) · GDPR · NIST AI RMF 1.0 + Generative AI Profile · ISO/IEC 42001 · ISO/IEC 23894 · UAE AI Office Charter · **CBUAE** (model risk + tech & cyber risk) · **DOH** Abu Dhabi · DIFC Data Protection Regulations · UAE PDPL.

---

License: MIT. Use freely, attribution appreciated.
