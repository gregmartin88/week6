# SIMULATED EVIDENCE FILE — Brightline Talent Systems

> **⚠ SIMULATED / FICTIONAL — FOR A GOVERNANCE CASE EXERCISE ONLY.**
> Brightline Talent Systems, its people, customers, documents, emails, and tickets are invented. Any resemblance to real organizations or persons is coincidental. Nothing here is a real record. Every exhibit below carries the same label.

| | |
|---|---|
| **Prepared for** | Audit Committee, Brightline Talent Systems (fictional) |
| **Prepared by** | Independent Reviewer |
| **Matter** | Whistleblower allegation that the Responsible AI Charter is "decorative" |
| **Review period** | 1 Oct 2024 – 30 Sep 2026 (8 fiscal quarters) |
| **File date** | 18 Oct 2026 |

### Contents
- **Exhibit A**: Responsible AI Charter, excerpts
- **Exhibit B**: Fairness Review Board meeting cadence, and model release vs. model card log
- **Exhibit C**: Sales email to a prospect
- **Exhibit D**: Internal ticket log (12 tickets; full data in [`ticket_log.csv`](ticket_log.csv))
- **Reviewer's index**: allegations mapped to the evidence, caveats, and what is still needed

---

## Exhibit A — Responsible AI Charter (excerpts)
*SIMULATED. Source: "Brightline Responsible AI Charter, v1.0," adopted by the Board 12 Sep 2024, published at brightline.example/responsible-ai. Executive sponsor: Chief Product Officer.*

> **Our Promise.** "At Brightline, we believe hiring technology should open doors, not close them. These seven principles guide every model we build and every product we sell."

| # | Principle | Charter text (excerpt) | Operational commitment stated in the charter |
|---|---|---|---|
| 1 | **Fairness** | "We test every model for adverse impact before it reaches a single candidate." | Before each production release, adverse impact ratio (AIR) of at least **0.80** (four-fifths rule) across sex, race/ethnicity, and age 40+ cohorts. A release that fails this is **blocked** until the Fairness Review Board signs off. |
| 2 | **Transparency** | "Customers and candidates deserve to know how our models work." | A public **model card** is updated **with every material model change, including retraining**, within 30 days of release. |
| 3 | **Accountability** | "Responsibility for AI outcomes sits with named leaders, not with algorithms." | The **Fairness Review Board** (7 members, quorum 5) meets **at least quarterly** and reports to the Audit Committee twice a year. |
| 4 | **Human Oversight** | "Our models recommend; people decide." | Customers are told the score is advisory. No auto-rejection without customer opt-in. |
| 5 | **Privacy** | "Candidate data is used only to serve the hiring decision it was provided for." | Data minimization and a 24-month retention limit. |
| 6 | **Robustness** | "We monitor our models in the real world, not only in the lab." | Quarterly drift and disparity monitoring on live customer data. |
| 7 | **Listening & Continuous Improvement** | "Every concern raised is a gift." | Any customer or employee report tagged *Fairness* is **triaged by the RAI Office within 10 business days**. A Fairness item may be reclassified **only with RAI Office approval**, and the reason is recorded. |

**§8. External Communications (excerpt):** "Public and customer-facing claims about the fairness of Brightline products must be reviewed by the RAI Office and Legal before use. Brightline does not claim its products eliminate bias; we claim we measure and mitigate it."

*— END EXHIBIT A (SIMULATED) —*

---

## Exhibit B — Fairness Review Board: meeting cadence, and model governance log
*SIMULATED. Source: FRB calendar export, minutes repository (SharePoint "RAI-Governance"), and ML release registry.*

### B-1. Meeting cadence against the charter's quarterly requirement

| Fiscal Qtr | Required by charter | Scheduled date | Outcome | Attendance (of 7) | Quorum? | Recorded reason / notes |
|---|---|---|---|---|---|---|
| Q4 2024 | Yes | 14 Nov 2024 | **Held** | 6 | Yes | Inaugural meeting. Adopted the 0.80 AIR release gate. **Action:** FRB to review v3.1 before release (owner: VP Product). |
| Q1 2025 | Yes | 20 Feb 2025 | Cancelled | — | — | "Conflicts with v3.1 launch week." Not rescheduled. *(v3.1 had already shipped 27 Jan 2025 with no FRB review.)* |
| Q2 2025 | Yes | 15 May 2025 | Postponed → cancelled | — | — | "Chair on leave." Chair role vacant 15 May – 1 Sep 2025. |
| Q3 2025 | Yes | 2 Oct 2025 *(slipped from Aug)* | **Held** | 4 | **No** | Discussed ENG-2215 (v3.2 AIR for age 55+ = 0.76). Minutes: *"Members expressed concern. No vote possible without quorum. Product to provide mitigation plan."* No mitigation plan is on file. v3.2 shipped 4 days later. |
| Q4 2025 | Yes | 11 Dec 2025 | Cancelled | — | — | "Year-end priorities." |
| Q1 2026 | Yes | — | **Not scheduled** | — | — | No calendar entry found. |
| Q2 2026 | Yes | 18 Jun 2026 | Cancelled | — | — | "Agenda items deferred to Q3." |
| Q3 2026 | Yes | 24 Sep 2026 | Cancelled | — | — | Invite withdrawn by organizer on 22 Sep 2026; no reason recorded. |

**Summary:** 8 meetings required; **2 held**; **1 of the 2 had quorum**. **0** of the 4 required semi-annual reports to the Audit Committee were delivered across FY2025–FY2026 (per Audit Committee minutes).

### B-2. Model releases vs. model card updates

| Model version | Production release | Retrain? | Pre-release fairness eval | FRB sign-off | Public model card version | Model card dated |
|---|---|---|---|---|---|---|
| v3.0 | 18 Mar 2024 *(pre-charter)* | Baseline | Third-party audit, Feb 2024 | n/a (FRB did not exist) | **v1.2** | 18 Mar 2024 |
| v3.1 | 27 Jan 2025 | Yes: new training data (2024 hires) | Internal, passed (report on file) | **None** | v1.2 *(unchanged)* | 18 Mar 2024 |
| v3.2 | 6 Oct 2025 | Yes: new data, new "communication" feature | Internal, **failed** (age 55+ AIR 0.76; see ENG-2215) | **None** (meeting lacked quorum) | v1.2 *(unchanged)* | 18 Mar 2024 |
| v3.3 | 12 May 2026 | Yes: new data, re-weighted education features | **Not run** (pipeline broken; see ENG-2388) | **None** | v1.2 *(unchanged)* | 18 Mar 2024 |

**Summary:** 3 retrains under the charter. **0** model card updates. The public card still describes v3.0's features and its Feb 2024 audit results. It does not mention the "communication" sub-score added in v3.2.

*— END EXHIBIT B (SIMULATED) —*

---

## Exhibit C — Sales email
*SIMULATED. Source: CRM email capture, Opportunity #OPP-88213. Produced by Sales Ops under the reviewer's document request.*

```
From:     Derek Thornton <d.thornton@brightline.example>  (Enterprise Account Executive)
To:       Priya Raman <praman@carrowfreight.example>  (Director of Talent Acquisition, Carrow Freight Co.)
Cc:       Lena Ford <l.ford@brightline.example>  (Regional Sales Director)
Date:     Tue, 14 Apr 2026 09:42 -0500
Subject:  RE: Follow-up: Brightline vs. your current ATS screening
Attach:   Brightline_RAI_Charter_v1.pdf ; Brightline_Overview_2026.pdf

Hi Priya,

Great speaking with you and your team yesterday. To your question about
risk: this is exactly where Brightline separates itself.

  * Brightline delivers truly BIAS-FREE SCREENING. Our model is blind to
    gender, race, and age, so those factors simply can't affect a score.
  * Every model release is independently audited and signed off by our
    Fairness Review Board before it ever touches your candidates.
  * Our model card is fully public and always current, so your legal team
    can see exactly what's under the hood.
  * Honestly, with Brightline in the loop you shouldn't have to worry about
    adverse-impact claims again. That's a big part of why 300 employers
    trust us.

I've attached our Responsible AI Charter. It's the gold standard in the
industry. If we can get the MSA signed by end of quarter, I can hold the
15% multi-year discount we discussed.

Best,
Derek

Derek Thornton | Enterprise AE | Brightline Talent Systems
"Hire on merit. Nothing else."
```

**Reviewer annotations (not part of the original email):**
- Sales Ops confirms the email was sent from a standard template, "Objection Handling: Bias/Risk v4." That template was **not** submitted for RAI Office or Legal review (Charter §8). The same template went out in **~140** emails between Jan and Sep 2026 (CRM query, 30 Sep 2026).
- At the time of sending, v3.3 had not been released yet. The model in production was **v3.2**, which failed its own fairness gate (Exhibit B-2). The model card was 25 months old.
- "Blind to … age" is contradicted by CS-4177 (graduation year acts as a proxy for age) and ENG-2215.

*— END EXHIBIT C (SIMULATED) —*

---

## Exhibit D — Internal ticket log (extract)
*SIMULATED. Source: "BrightDesk" ticketing system export, filter `label_history CONTAINS "Fairness" OR type = "Fairness*"`, plus two control tickets. Customer names replaced with CUST-IDs. Full data: [`ticket_log.csv`](ticket_log.csv).*

| Ticket | Opened | Reporter | Original type / Pri | Summary | Reclassified to / Pri | By (date) | Status |
|---|---|---|---|---|---|---|---|
| CS-4102 | 2025-02-11 | R. Okafor (CSM) | Fairness Issue / P2 | Candidates with 12+ month employment gaps (mostly women, per the customer's audit) score 18–22 pts lower | **Feature Request / P4** | J. Lindqvist, Sr. PM (02-19) | Backlog |
| CS-4177 | 2025-04-03 | M. Duarte (CSM) | Fairness Issue / P1 | Graduation year drives lower scores for applicants 50+ | **Feature Request / P3** | J. Lindqvist (04-07) | Backlog |
| CS-4230 | 2025-05-15 | T. Brennan (Support) | Fairness Issue / P3 | Dark mode for dashboard (mis-tagged) | Feature Request / P4 | J. Lindqvist (05-16) | Done ✔ *legitimate fix of a wrong tag* |
| CS-4311 | 2025-07-22 | R. Okafor (CSM) | Fairness Issue / P2 | Applicants listing HBCUs get lower "education match" scores at comparable GPA and major | **Feature Request / P4** | J. Lindqvist (07-30) | Won't Do |
| CS-4398 | 2025-08-28 | K. Ibarra (CSM) | Compliance / P2 | Customer requests a current bias-audit summary for NYC LL144 | — | — | Resolved: sent the **2024** audit (covers v3.0 only) |
| ENG-2215 | 2025-09-30 | A. Mensah (Data Sci.) | **Fairness – Release Blocker / P1** | v3.2 pre-release: age 55+ AIR = 0.76 (< 0.80) | **Known Limitation / P3** | S. Varga, VP Product (10-03) | Open; v3.2 shipped |
| CS-4460 | 2025-11-12 | M. Duarte (CSM) | Fairness Issue / P2 | Non-native English speakers score lower on the "communication" sub-score | **Feature Request / P4** | J. Lindqvist (11-20) | Backlog |
| CS-4519 | 2026-01-20 | T. Brennan (Support) | Feature Request / P3 | Bulk CSV export of shortlist | — | — | Done ✔ *control ticket* |
| CS-4588 | 2026-03-09 | R. Okafor (CSM) | Fairness Issue / P2 | Gaps from medical leave or disability penalized; customer raises an ADA concern | **Feature Request / P4** | J. Lindqvist (03-11) | Closed as duplicate of CS-4102 (itself in Backlog) |
| ENG-2388 | 2026-05-02 | A. Mensah (Data Sci.) | **Fairness – Release Blocker / P1** | v3.3: fairness eval suite did not run (pipeline broken) | **Tech Debt / P3** | S. Varga (05-05) | Open; v3.3 shipped |
| CS-4650 | 2026-06-17 | M. Duarte (CSM) | Fairness / Legal / P2 | Customer's counsel asks Brightline to substantiate the "bias-free screening" claim | **Collateral Update Request / P4** | Auto-routed to Sales Ops (06-18) | Open, unassigned |
| CS-4702 | 2026-08-25 | R. Okafor (CSM) | Fairness Issue / P1 | CS-4311 pattern reappears on v3.3; CSM emailed the RAI Office with no response | — | — | Closed "Not Reproducible" by J. Lindqvist (08-28); no repro steps recorded |

**Log statistics (reviewer-computed):**
- Fairness-tagged tickets: **10**. One (CS-4230) was a genuine mis-tag, which leaves **9 substantive fairness concerns**.
- Of those 9: **8** were reclassified to a non-fairness, lower-priority type (5 as *Feature Request*, 1 as *Collateral Update Request*, 1 as *Known Limitation*, 1 as *Tech Debt*). The 9th was closed as "Not Reproducible" within 3 days.
- **0 of 9** show RAI Office approval of the reclassification, which Charter Principle 7 requires. The audit trail shows no RAI Office user acting on any ticket.
- **0 of 9** led to a model change. Median priority moved from **P2 to P4**.
- 7 of the 9 substantive tickets were raised by the two CSMs who corroborate the whistleblower (R. Okafor: 4; M. Duarte: 3).
- Both release-blocker tickets from Data Science were downgraded by the same executive. Each time, the affected model shipped within 3–7 days.

*— END EXHIBIT D (SIMULATED) —*

---

## Reviewer's index: allegations vs. evidence
*SIMULATED analysis supporting the exercise.*

| Allegation | Exhibits | What the evidence shows | Caveats / alternative explanations | Still needed |
|---|---|---|---|---|
| 1. FRB met only twice in two years | A (P3), B-1 | Confirmed: 2 of 8 required meetings held, 1 with quorum. Chair vacant for 3.5 months. No reports to the Audit Committee. | Some FRB work may happen informally (Slack, email). Cancellations cite real operational conflicts. | Interviews with FRB members. Any informal decision records. Who owned rescheduling. |
| 2. Model card not updated through three retrains | A (P2), B-2 | Confirmed: card frozen at v1.2 (Mar 2024) through v3.1, v3.2, and v3.3. It omits the v3.2 feature and the failed eval. | Management may argue retrains are not "material." The charter text explicitly includes retraining. | Who owns the model card. Whether a draft update exists. Which customer contracts reference the card. |
| 3. Sales promises "bias-free screening" | A (§8), C, D (CS-4650) | Confirmed and systemic: the template was never reviewed and went out ~140 times. Claims contradict the charter and the internal evals. A customer's counsel has already challenged it. | One AE's wording vs. company policy: the template origin shows it was not one person's choice. | Template authorship and approval chain. Marketing collateral. Revenue tied to the claim. |
| 4. Fairness issues reclassified as "feature requests" | A (P7), D | Strongly supported: 8 of 9 substantive concerns downgraded with no RAI Office approval. Concentrated in 2 decision-makers. | Some items (e.g., field suppression) may be fixed through product features. One reclassification (CS-4230) was correct, so reclassification is not inherently improper. | Lindqvist and Varga rationale. RAI Office staffing and access. Any retaliation against the CSMs. |
| **Overall: "the charter is decorative"** | A–D | Each of the charter's specific operational commitments that was tested (P1, P2, P3, P7, §8) was not met in practice. Principles 4–6 were not tested in this file. | Absence of records is not proof that no activity took place. Hearing management's response is essential before any conclusion. | Testing of P4–P6. A fresh independent AIR test on v3.3. Legal privilege review before wider distribution. |

---

> **⚠ END OF SIMULATED EVIDENCE FILE.** All content is fictional and was created for an academic governance exercise.
