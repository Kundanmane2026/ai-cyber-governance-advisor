# Proposal and Delivery Templates

Run the conflict and independence check in `confidentiality-ethics` before drafting. Do not reuse another client's facts or findings.

## 1. Client proposal template

1. **Cover:** client, engagement title, proposal reference, date, validity (for example 30 days), confidentiality marking.
2. **Our understanding:** the client's situation and trigger (regulatory observation, incident, audit, certification, new law such as the DPDP Rules 2025, board request), stated back in their words. Tag inferred points as Assessed or Assumed.
3. **Objectives:** 3–5 outcomes, each measurable.
4. **Scope:**
   - In scope: entities, locations, business units, systems, frameworks or laws, period.
   - Out of scope: stated explicitly (for example "remediation implementation", "legal opinion", "testing of third-party systems").
5. **Approach:** phases with activities and the standards followed (for example ISO/IEC 27001:2022, NIST CSF 2.0, NIST SP 800-61r3, ISO/IEC 42001, DPDP Act and Rules).
6. **Deliverables:** each with format, owner and acceptance criteria.
7. **Timeline:** phases and milestones with absolute dates; regulatory dates marked as fixed.
8. **Team:** roles, relevant credentials, time allocation; independence statement.
9. **Client dependencies and assumptions:** documents, access, interviewees, timely sign-offs, single point of contact. Assumptions drive the fee; list them.
10. **Commercials:** fee basis (fixed / time and materials / retainer), fees by phase, GST at the applicable rate, out-of-pocket expenses, payment milestones, invoicing terms.
11. **Terms:** confidentiality and NDA reference; data handling (what client data we take, where it is stored, retention and return); IP (client owns deliverables, advisor retains pre-existing know-how and templates); liability cap; no legal advice unless engaged as counsel; non-solicitation; governing law and jurisdiction; termination.
12. **Why us** (short, factual; no claims that cannot be evidenced).
13. **Acceptance:** signature block.

### Government and PSU clients

- Respond to the tender's own format first; follow GFR 2017 and GeM terms where they apply; observe integrity pact and conflict declarations.
- If any team member is a serving government employee, check the CCS (Conduct) Rules 1964 (Rules 11 and 15) for prior permission before any private engagement (see `confidentiality-ethics`).

## 2. Scope note / statement of work (one page)

| Field | Entry |
|---|---|
| Engagement | |
| Client sponsor / decision-maker | |
| Objective | |
| In scope | |
| Out of scope | |
| Deliverables and acceptance criteria | |
| Milestones and dates | |
| Client dependencies | |
| Assumptions | |
| Fees and payment milestones | |
| Change control | Any change in scope, assumptions or dates goes through a written change request |
| Signatures | |

## 3. Testing-engagement scope language (VAPT, red team, tabletop)

Describe governance only; never describe techniques.

- **Authorisation:** written authorisation from the system owner with authority over every in-scope asset; third-party (cloud, SaaS, hosting) permissions where their terms require them.
- **Scope:** asset list (IPs, URLs, applications), environments, exclusions, testing windows.
- **Standards:** CERT-In empanelled auditor where the client's regulator requires one; sector frequency rules (RBI, SEBI CSCRF, IRDAI); OWASP testing guides at the methodology-reference level.
- **Rules of engagement:** permitted test types at category level, prohibited actions (for example denial of service, social engineering of named individuals unless approved, access to production personal data beyond what is needed), stop conditions, emergency contacts.
- **Data handling:** minimal access to personal data; no copies retained; secure deletion with certificate.
- **Reporting:** severity scale, evidence format, retest, executive summary.
- **Legal:** safe-harbour wording; compliance with IT Act s.43 and s.66 by acting only within written authorisation.

## 4. Project delivery plan

| Phase | Work package | Activities | Deliverable | Owner | Start | End | Dependency | Gate |
|---|---|---|---|---|---|---|---|---|
| 0. Mobilise | Kick-off | Confirm scope, contacts, document request, access | Kick-off deck; document request list | Engagement lead | | | Signed SoW | Kick-off held |
| 1. Discover | Interviews and document review | | Interview notes; evidence register | | | | Client availability | |
| 2. Analyse | Assessment against framework / law | | Draft findings | | | | | Findings validated with client |
| 3. Recommend | Roadmap and business case | | Draft report | | | | | |
| 4. Report | Final report and board presentation | | Final report; board deck | | | | Client review comments | Acceptance |
| 5. Close | Handover, data return or deletion | | Closure note; deletion certificate | | | | | |

## 5. RACI

| Activity | Engagement lead | Advisor team | Client sponsor | Client CISO / DPO | Client legal |
|---|---|---|---|---|---|
| Scope approval | A | C | R | C | C |
| Evidence collection | A | R | I | C | I |
| Findings validation | A | R | I | C | C |
| Final report | R/A | R | I | C | C |
| Board presentation | R | C | A | C | C |

R = Responsible, A = Accountable, C = Consulted, I = Informed. One A per row.

## 6. RAID log

| ID | Type (Risk / Assumption / Issue / Dependency) | Description | Impact | Owner | Action | Due | Status |
|---|---|---|---|---|---|---|---|

## 7. Status report (weekly or fortnightly)

1. Overall RAG and one-line reason.
2. Done this period / planned next period.
3. Milestones: planned vs forecast date.
4. Top RAID items needing client action.
5. Change requests raised or approved.
6. Budget used vs plan (if time and materials).

## 8. Change request

| Field | Entry |
|---|---|
| CR number and date | |
| Requested by | |
| Description of change | |
| Reason | |
| Impact on scope, deliverables, dates, fees | |
| Approval (client and advisor) | |
