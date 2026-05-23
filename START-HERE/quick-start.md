# Start Here — 5-Minute Quick Start

You are about to run an **AI risk assessment** on a real or planned AI use case in your organisation. This page tells you exactly what to do, in order, in plain language.

If you read nothing else, read this page.

---

## What this toolkit gives you

Six concrete files you fill in. Together they form a complete end-to-end AI risk assessment.

| # | File | What you do with it |
|---|---|---|
| 1 | `toolkit/01-ai-inventory.csv` | List every AI system in your organisation, one row per system. |
| 2 | `toolkit/02-intake-form.md` | Capture a NEW use case in 15 minutes when someone proposes it. |
| 3 | `toolkit/03-risk-assessment-workbook.md` | Answer 30 questions; the workbook scores the risk and tells you what tier the system is. |
| 4 | `toolkit/04-risk-register.csv` | Log every identified risk with owner, score, and treatment plan. |
| 5 | `toolkit/05-treatment-plan.csv` | Track every control / action you commit to, with due dates and status. |
| 6 | `toolkit/06-board-report.md` | One-page summary for the Board / ExCo every quarter. |

That is it. Six files. You do not need to read the rest of the repo to get started.

---

## The 8-step process

Run these eight steps for every AI use case. They take about **half a day** for a typical use case.

```
1. DISCOVER  -> Find AI systems in use or planned   -> fill row in 01-ai-inventory.csv
2. INTAKE    -> Capture the use case details        -> 02-intake-form.md
3. CLASSIFY  -> Decide the risk tier (1 to 4)       -> Section A of 03-workbook
4. SCORE     -> Score risks across 8 dimensions     -> Section B of 03-workbook
5. TREAT     -> Pick controls that reduce the risk  -> Section C of 03-workbook + 05-treatment-plan.csv
6. APPROVE   -> Get the right approver to sign-off  -> Section D of 03-workbook
7. MONITOR   -> Set up ongoing checks               -> Section E of 03-workbook
8. REPORT    -> Roll up to the Board                -> 06-board-report.md
```

Each step is also explained in detail in `HOW-TO-RUN-AN-ASSESSMENT.md`.

---

## See it done first — open the Worked Example

Before doing your own assessment, look at the **fully completed example** in `WORKED-EXAMPLE/`. It is a fictional **CV-Screening AI for HR** with every file filled in, every score explained, and the Board report written. Copy the format.

Files in WORKED-EXAMPLE:
- `example-01-intake.md` — how the use case was first captured.
- `example-02-workbook.md` — the completed assessment.
- `example-03-risk-register-extract.csv` — the risks that made it onto the register.
- `example-04-treatment-plan-extract.csv` — the controls being implemented.
- `example-05-board-report.md` — the one-pager that went to the Board.

---

## Where the big regulatory documents fit in

The folders `00-foundation/`, `europe/` and `uae/` are the **reference library** — read them once to understand WHY the toolkit asks each question. You do not need to read them to USE the toolkit. They explain:

- `00-foundation/` — the underlying program design (governance, taxonomy, controls).
- `europe/` — EU AI Act mapping (read if you operate in the EU).
- `uae/` — UAE-specific overlays for CBUAE, DOH, DIFC (read if you operate in the UAE).

Think of it this way:

- **toolkit/** = the tools you USE every day.
- **WORKED-EXAMPLE/** = the demo of how to use them.
- **00-foundation/, europe/, uae/** = the textbook behind the tools.

---

## Your first 60 minutes

1. **Minute 0–10**: Read this page (you are doing it).
2. **Minute 10–25**: Open `WORKED-EXAMPLE/example-02-workbook.md` and read the completed CV-screening assessment.
3. **Minute 25–35**: Open `toolkit/01-ai-inventory.csv` and add the FIRST AI system you can think of in your organisation as a single row.
4. **Minute 35–55**: Take that same system, open `toolkit/03-risk-assessment-workbook.md`, copy it into your own working doc, and answer the 30 questions for that system.
5. **Minute 55–60**: Look at the auto-generated tier and residual score. Decide who needs to approve.

You have just completed your first AI risk assessment.

---

## Common questions

**Do I need to be a data scientist to use this?**
No. The workbook is written for risk, compliance, audit, security, and business roles. If you can fill in a questionnaire and use a heat-map, you can run an assessment.

**What if my org has 50 AI systems and I am one person?**
Start with the 5 most consequential ones. Add the rest to the inventory but do not try to assess everything at once. Use the tiering in Step 3 to prioritise.

**What if I am in financial services or healthcare or DIFC?**
Run the standard workbook first, then add the sector-specific questions from the relevant addendum in `uae/` or the EU sector overlays in `europe/`.

**What if I do not know the answer to a question?**
Mark it Unknown — that is itself a risk and goes on the register. The workbook tells you what to do with Unknowns.

**Do I need to buy any tool?**
No. The CSV files open in Excel, Google Sheets, or any text editor. The markdown files open in any editor. You can run the entire program for free.

---

## Next: open `HOW-TO-RUN-AN-ASSESSMENT.md` for the step-by-step playbook.
