# Worked Example 01 — Intake Form (CV-Screening AI)

This is a fully filled-in copy of `toolkit/02-intake-form.md` for a fictional use case so you can see what "good" looks like before you do your own. Section letters and field names mirror the toolkit template exactly.

Date: 12 March 2026  AI-ID (assigned by ARWG): **AI-2026-0001**

---

## A. Who and what
- Submitter name and role: Sara Al Mansoori, Head of Talent Acquisition
- Business unit: Human Resources
- Sponsoring executive: Director of Human Resources
- Working title of the AI use case: CV-Screening AI for HR
- One-paragraph description of what it does: Reads each applicant CV (PDF/DOCX), extracts skills, education, and experience, and produces a 0–100 fit score against the job description. Recruiters see a ranked shortlist; the AI does not auto-reject any candidate.

## B. Why
- Business problem this solves: 18,000+ applications/year across UAE and EU; recruiters spend 60% of time on first-pass screening.
- Expected benefit: 12,000 recruiter hours saved/year; time-to-shortlist down from 9 days to 3.
- What is the non-AI alternative? Why not just use that? Keyword search in the ATS — high false-negative rate and still requires manual review. Hiring volume has doubled and headcount has not.

## C. Who is affected
- Who uses the AI? Internal recruiters (about 25 people) in HR.
- Who is affected by the AI's decisions? Job applicants — internal transfers and external candidates.
- Approximate number of people affected per month: ~1,500.
- Are any vulnerable groups affected? Y — early-career candidates and persons with disabilities self-identifying in the application. Special care on accessibility of the candidate notice and human-review route.

## D. Decision impact
- What kind of decision does the AI inform? Recommend (shortlist for human review).
- Does a human review every decision? Y — every shortlist is reviewed by a recruiter before any interview invite is sent.
- Could the decision affect: employment ☑ · dignity ☑ · access to services ☐ · health ☐ · safety ☐ · finances ☑ (indirect) · freedom ☐

## E. Data
- What data does the AI use? CV file (PDF/DOCX), job description, 5 years of historical CVs + hiring outcomes (~80,000 records) for training.
- Does it include personal data? Y. Lawful basis: legitimate interest (recruitment) for EU; consent + contract necessity for UAE PDPL.
- Does it include special-category data? Y — applicants sometimes include health or family information voluntarily. Mitigation: strip from features.
- Where will the data be stored and processed? EU candidates: AWS Frankfurt. UAE candidates: AWS Bahrain (vendor tenancy). Vendor support: US (under SCCs).

## F. The AI itself
- Built in-house / bought from vendor / hybrid: Bought (vendor).
- AI technique: Classical ML — gradient-boosted trees + sentence embeddings.
- Foundation model used: None in the scoring path (vendor written confirmation on file).
- Vendor name(s) and contract status: TalentRank.ai — MSA signed; AI addendum in negotiation; go-live conditional on signed addendum.

## G. Jurisdictions
- Where will it be deployed? EU (Frankfurt office), UAE Mainland (Abu Dhabi HQ).
- Sector regulator(s) likely involved: None directly (not financial, not healthcare). Cross-cutting: EU AI Act (high-risk Annex III §4 employment); GDPR + national DPAs (DE BfDI); UAE PDPL + UAE Data Office; UAE Charter for AI.

## H. Quick risk flags (tick if YES)
- ☐ Could be used for emotion recognition, social scoring, or biometric ID
- ☑ Affects credit, insurance, hiring, education, or essential services (hiring)
- ☐ Used in a medical, safety, or law-enforcement context
- ☐ Generates content that could be mistaken for human-created
- ☐ The vendor will train its models on our data (explicit opt-out in draft addendum)
- ☐ We do not yet know all the answers above

→ One of the first three is ticked → **fast-track to full assessment**.

## I. Timeline
- Target pilot date: 1 July 2026 (single business unit, EU only)
- Target production date: 1 September 2026 (EU + UAE)
- Any hard regulatory or business deadline? Aligned with EU AI Act high-risk obligations (most apply from 2 August 2026) — we choose go-live after that date deliberately.

---

## ARWG decision (filled in by the Working Group)
- ☑ **Accept for full assessment.** Assigned analyst: Ankit U. (AI Risk Lead). Target completion: 30 April 2026.
- ☐ Need more info — questions to answer: —
- ☐ Reject — reason: —

**Provisional tier: Tier 2 High-risk** (EU AI Act Annex III §4 employment; affects access to employment for ~18,000 people/year; personal data + automated profiling triggers GDPR Art. 22).

Triage signature: Ankit U., AI Risk Lead  Date: 13 March 2026

Next step: open toolkit/03-risk-assessment-workbook.md (the completed version is at WORKED-EXAMPLE/example-02-workbook.md).
