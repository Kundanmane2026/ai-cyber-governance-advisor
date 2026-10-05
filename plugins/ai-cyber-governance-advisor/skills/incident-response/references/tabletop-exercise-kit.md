# Tabletop Exercise Kit

Tabletops test **decisions, roles, communication and regulatory timing**, not technical attack skill. Describe what the attacker's actions caused, never how they were done.

## 1. Design steps

1. **Objectives:** 3–5 measurable ones, for example: "Decide CERT-In reportability and draft the report within the 6-hour window", or "Agree who authorises isolating the core banking system".
2. **Audience:** Board/executive (strategic, 90 min), management (operational, 2–3 h), technical (procedural, half day).
3. **Scenario:** plausible for the sector, linked to top risks in the risk register.
4. **Injects:** 4–6 timed developments that add pressure and information.
5. **Roles:** facilitator, scribe or observer, participants, and optionally a "white cell" playing regulators, media and the attacker's communications.
6. **Ground rules:** no-fault; decisions made with the information available; stay in role; it is fine to say "we don't know".
7. **Evaluation:** criteria per objective, observer notes, and a participant feedback form.
8. **After-action:** a report within 2 weeks; actions entered in the risk register and the IR plan.

## 2. Inject card template

| Field | Content |
|---|---|
| Inject # / Exercise time | e.g. Inject 2 / T0 + 2 h |
| Situation update | What participants now learn |
| Delivered as | Email, phone call, news clip, regulator query |
| Questions | 2–4 discussion questions |
| Expected actions | What a good response looks like (for the evaluator) |
| Plan / regulatory reference | IR plan section; CERT-In / DPDP / sector rule |

## 3. Sample: ransomware at a mid-size NBFC (executive tabletop, 90 minutes)

**Background:** a NBFC with 1,200 staff, a loan management system on-premises, a CRM in SaaS, and an MSSP for the SOC. Regulated by RBI.

| # | Time | Situation | Discussion questions | Expected actions |
|---|---|---|---|---|
| 1 | Mon 07:40 (T0) | Branch staff report they cannot open loan files; a ransom note is on file servers. The MSSP confirms encryption on 40 servers | Who is in charge? What is T0? What do we isolate? Who can authorise taking the LMS offline? | Declare SEV-1; record T0; Incident Commander named; isolate rather than power off; protect backups; start the deadline tracker |
| 2 | T0 + 2 h | The MSSP finds signs that 300 GB left the network two days earlier. Backups for the LMS appear intact but have not been restore-tested in 8 months | Is this a personal data breach? Which reports are due and when? What do we tell staff? | CERT-In by T0 + 6 h; RBI per the MD; DPDP Board intimation without delay; validate backups; staff holding note via an out-of-band channel |
| 3 | T0 + 5 h | The attacker emails the CEO demanding payment and threatening to leak customer KYC data | Who responds? Do we pay? Who else must know? | No engagement without counsel; no payment advice; involve law enforcement; notify the insurer; confirm the CERT-In report has been submitted |
| 4 | T0 + 20 h | A journalist calls about a "data leak at the NBFC"; samples appear on a leak site | Holding statement? Data Principal notices? | Approved holding statement; verify the sample data; prepare Data Principal intimation contents; the 72 h Board report is under way |
| 5 | T0 + 48 h | Restore succeeds for the LMS; the CRM vendor says it is unaffected but cannot share its logs | Return-to-service criteria? Vendor obligations? | Validate the environment is clean before reconnecting; invoke contract audit and cooperation clauses; heightened monitoring |
| 6 | T0 + 70 h | RBI asks for a detailed report and the root cause | What is our evidence? What lessons are emerging? | Submit the DPDP 72 h report; RBI follow-up; preserve the chain of custody; schedule the post-incident review |

## 4. Other scenario seeds

- **BEC:** a ₹3.2 crore vendor payment is diverted after a supplier's mailbox is compromised (bank recall, 1930, client notice).
- **Cloud data exposure:** a public storage bucket holds 2 lakh customer records, found by a researcher (responsible disclosure handling, DPDP, CERT-In).
- **Insider:** a departing relationship manager downloads a client list (HR and Legal coordination, DLP evidence, s.72A).
- **Third-party SaaS breach:** the payroll provider is breached, with employee data affected (processor-controller coordination).
- **Deepfake CEO voice:** an urgent fund transfer is requested by a cloned voice call (verification controls, staff awareness).

## 5. Evaluation form (per objective)

| Objective | Met / Partly / Not met | Evidence observed | Gap | Recommended action | Owner | Due |
|---|---|---|---|---|---|---|

Participant feedback: clarity of roles (1–5); confidence in the reporting deadlines (1–5); the most useful moment; the biggest concern.

## 6. After-action report outline

1. Exercise overview (date, participants, scenario, objectives)
2. Summary of performance
3. Strengths
4. Areas for improvement, mapped to the IR plan / playbook sections
5. Action plan (owner, due date, priority)
6. Appendix: timeline of decisions, observer notes
