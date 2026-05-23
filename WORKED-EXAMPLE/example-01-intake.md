# Worked Example 01 — Intake Form (CV-Screening AI)

This is a fully filled-in copy of toolkit/02-intake-form.md for a fictional use case so you can see what "good" looks like before you do your own.

Use case ID: AI-2026-0001
Use case name: CV-Screening AI for HR
Date submitted: 12 March 2026
Submitted by: Sara Al Mansoori, Head of Talent Acquisition
Business owner: Director of Human Resources
Region of deployment: UAE (Abu Dhabi HQ) and EU (Frankfurt office)

---

## 1. What problem are you trying to solve?
We receive 18,000+ job applications per year across the UAE and EU. Recruiters spend 60% of their time screening CVs manually. We want to automatically rank CVs by fit-to-job-description so recruiters can focus on the top 20%.

## 2. What will the AI actually do?
Read each CV (PDF or DOCX), extract skills, education, experience, and produce a 0-100 "fit score" against the job description. Recruiters see a ranked list. The AI does NOT auto-reject anyone — a human recruiter reviews every shortlist.

## 3. Who are the users?
Internal recruiters (about 25 people) in HR.

## 4. Who is affected by the decisions?
Job applicants — both internal employees applying for transfers and external candidates. Estimated 18,000 people per year.

## 5. What data does it use?
Input: CV file uploaded by the applicant + the job description. Training data: 5 years of historical CVs and hiring outcomes from our ATS (~80,000 records).

## 6. Does it use personal data?
Yes. Name, contact details, nationality, date of birth, employment history, education, photo (sometimes). Some applicants include health or family information voluntarily.

## 7. Vendor or in-house?
Vendor: TalentRank.ai (Series B startup, US-based, hosted on AWS Frankfurt for EU data and AWS Bahrain for UAE data).

## 8. Is it generative AI or a foundation model?
No. It is a fine-tuned classification model (gradient-boosted trees + sentence embeddings). Vendor confirms no LLM is used in the scoring path.

## 9. What decisions does it influence?
Shortlisting for interview. The human recruiter still makes the interview/no-interview call but in 78% of cases follows the AI ranking.

## 10. What happens if it is wrong?
A qualified candidate is ranked low and never interviewed. Possible discrimination claim. Reputational harm. Under GDPR Article 22 and the EU AI Act (employment = high-risk), regulatory exposure is significant. In the UAE, PDPL and DOH/CBUAE do not directly apply (we are not health or financial sector) but UAE Charter for the Development and Use of AI applies.

## 11. Go-live target date
1 September 2026.

## 12. Budget owner
HR Operations cost centre. Annual licence USD 240,000.

---

## Triage decision (filled by AI Risk team)

Initial tier (pre-assessment): **Tier 2 — High risk**
Reason: Employment / worker management use case = Annex III high-risk under EU AI Act. Affects access to employment for ~18,000 people/year. Personal data + automated profiling triggers GDPR Article 22.

Routed to: Full risk assessment (toolkit/03-risk-assessment-workbook.md)
Assessor assigned: Ankit U. (AI Risk Lead)
Target assessment completion: 30 April 2026
