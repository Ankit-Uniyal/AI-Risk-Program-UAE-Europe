# How to Run an AI Risk Assessment — Step by Step

This is the **playbook**. Follow these 8 steps for any AI use case and you have done an end-to-end risk assessment.

Time required: about **4 hours** of focused work for a typical use case, spread over 1 to 2 weeks of elapsed time (because you need inputs from several people).

---

## STEP 1 — DISCOVER (find the AI)

**Goal:** know which AI systems exist or are being planned.

**What to do:**
1. Open `toolkit/01-ai-inventory.csv` in Excel or Google Sheets.
2. For every AI system you can identify, add one row. Fill in as many columns as you can. Leave blanks where unknown.
3. Sources to find AI systems: ask BU heads; check procurement contracts; check cloud spend for ML / GPU SKUs; ask "anyone using ChatGPT, Copilot, Claude for work?"; check IT systems for embedded AI features.

**Output:** populated inventory with at least System name, Owner, Purpose, Tier (provisional), Status.

**Common pitfalls:** missing shadow GenAI usage; missing AI embedded in vendor products (e.g. CRM scoring, email security).

---

## STEP 2 — INTAKE (capture the use case)

**Goal:** for a NEW use case, get the basic facts in 15 minutes.

**What to do:**
1. Open `toolkit/02-intake-form.md`.
2. Copy the form into a new document for this use case.
3. Ask the proposer (business owner) the questions on the form. Fill in the answers.
4. Decide: Accept for full assessment / Need more info / Reject (because Prohibited).

**Output:** completed intake form, decision recorded.

---

## STEP 3 — CLASSIFY (assign a risk tier)

**Goal:** decide if the system is Tier 1 (Prohibited), Tier 2 (High-risk), Tier 3 (Limited), or Tier 4 (Minimal).

**What to do:**
1. Open `toolkit/03-risk-assessment-workbook.md`, **Section A**.
2. Answer the tier-classification questions (yes/no).
3. The decision rules at the bottom of Section A tell you the tier.

**Tier consequences:**
- Tier 1 Prohibited -> STOP. Do not deploy. Inform sponsor.
- Tier 2 High-risk  -> Full assessment required; ARC + BRC approval.
- Tier 3 Limited    -> Lightweight assessment; transparency obligations apply.
- Tier 4 Minimal    -> Light-touch; record in inventory, refresh annually.

**Output:** confirmed tier, recorded in inventory.

---

## STEP 4 — SCORE (assess inherent risk)

**Goal:** score the system across 8 risk dimensions.

**What to do:**
1. Open `toolkit/03-risk-assessment-workbook.md`, **Section B**.
2. For each of the 8 dimensions (Impact, Privacy, Bias, Security, Robustness, Transparency, Oversight, Vendor), answer the questions and give a score from 1 (low) to 5 (critical).
3. The workbook gives you the **inherent risk score** = the highest score across the 8 dimensions.

**Output:** 8 dimension scores + inherent risk = Low / Medium / High / Critical.

---

## STEP 5 — TREAT (choose controls)

**Goal:** lower the risk by adding controls.

**What to do:**
1. Open `toolkit/03-risk-assessment-workbook.md`, **Section C**.
2. For each high-scoring dimension, the workbook lists the recommended controls.
3. Decide which controls you will implement, by whom, by when.
4. For every control, add a row to `toolkit/05-treatment-plan.csv` with: Risk ID, Control description, Owner, Due date, Status.
5. For every residual risk that remains (where controls cannot fully eliminate it), add a row to `toolkit/04-risk-register.csv`.

**Output:** treatment plan + risk register entries.

---

## STEP 6 — APPROVE (get sign-off)

**Goal:** the right authority accepts the residual risk.

**What to do:**
1. Open `toolkit/03-risk-assessment-workbook.md`, **Section D**.
2. Compute the **residual risk** (inherent minus the strength of controls).
3. The workbook tells you who must approve based on residual:
   - Low / Low-Medium -> Head of AI Risk
   - Medium           -> AI Risk Committee
   - High             -> ARC + Board notification
   - Critical         -> Board approval (default: do not deploy)
4. Prepare the approval memo (template in Section D).
5. Send for signature. Record the date and reference.

**Output:** signed acceptance memo, system can now go live (or is rejected).

---

## STEP 7 — MONITOR (set up ongoing checks)

**Goal:** know if the risk profile changes after go-live.

**What to do:**
1. Open `toolkit/03-risk-assessment-workbook.md`, **Section E**.
2. Pick the right monitoring KPIs from the menu (performance, drift, bias, security events, complaints, incidents).
3. Set the cadence (real-time, daily, monthly, quarterly).
4. Set the reassessment trigger (e.g. retraining, regulatory change, incident).
5. Add the next reassessment date to the inventory.

**Output:** monitoring plan attached to the system; calendar entry for reassessment.

---

## STEP 8 — REPORT (roll up to Board)

**Goal:** every quarter, give the Board a one-page view of all AI risk.

**What to do:**
1. Open `toolkit/06-board-report.md`.
2. Pull the numbers from your inventory + risk register + treatment plan.
3. Fill in: total AI systems, new this quarter, by tier, top 5 residual risks, incidents, decisions requested.
4. Send to the Board Risk Committee.

**Output:** one-page Board pack.

---

## The whole flow on one diagram

```
+-----------+      +----------+      +-----------+      +--------+
| 1.DISCOVER|----->| 2.INTAKE |----->| 3.CLASSIFY|----->|4.SCORE |
|inventory  |      |intake    |      |tier 1-4   |      |8 dims  |
+-----------+      +----------+      +-----------+      +--------+
                                                              |
                                                              v
+-----------+      +----------+      +-----------+      +--------+
| 8.REPORT  |<-----| 7.MONITOR|<-----| 6.APPROVE |<-----|5.TREAT |
|board pack |      |drift, KPI|      |sign-off   |      |controls|
+-----------+      +----------+      +-----------+      +--------+
```

---

## Roles needed (small org version)

You do not need a big team. Minimum:
- **Business owner** of the AI system (answers the intake).
- **Risk lead** (runs the workbook).
- **One technical reviewer** (data scientist, MLE, or IT lead).
- **Approver** depending on tier (manager / ExCo / Board).

If you are a one-person team, you play Risk lead and use the workbook to interview the others.

---

## When to reassess

Run the assessment again when ANY of these happen:
- The model is retrained or the prompt template changes materially.
- A new data source is added.
- The vendor changes the underlying foundation model.
- A new jurisdiction is added.
- An incident or near-miss occurs.
- A regulator publishes new guidance.
- 12 months have passed (Tier 2 High-risk: 6 months).

---

## What to do if you get stuck

| Situation | What to do |
|---|---|
| The workbook score says Critical but business insists on going live | Escalate to ARC / Board. Document the disagreement. Do not let the system go live without written approval. |
| You cannot get an answer to a question | Mark Unknown, add it to the risk register, set a due date to resolve. |
| The vendor refuses to answer the due-diligence questionnaire | That is itself a red flag. Score the Vendor dimension at 4 or 5. Reconsider procurement. |
| You find an AI system already in production that has never been assessed | Treat it as a NEW intake today. Do not retroactively pretend it was approved. |

You now know the entire process. Next: open `WORKED-EXAMPLE/example-02-workbook.md` to see it done end-to-end on a real-looking use case.
