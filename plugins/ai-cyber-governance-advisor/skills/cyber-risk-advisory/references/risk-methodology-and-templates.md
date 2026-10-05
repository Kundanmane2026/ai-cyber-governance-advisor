# Risk Methodology and Templates

These are the default scales and templates. If the organisation already has ERM scales, adopt those instead and note the change.

## 1. Likelihood scale (12-month horizon)

| Score | Label | Guide |
|---|---|---|
| 1 | Rare | Not expected; no known occurrence in sector in 5 years |
| 2 | Unlikely | Could occur; known in sector, not at peers of similar size |
| 3 | Possible | Has occurred at peers; partial controls in place |
| 4 | Likely | Expected within the year; weak or untested controls; active threat campaigns against the sector |
| 5 | Almost certain | Already occurring or occurred in the last 12 months; controls absent |

## 2. Impact scale (use the highest applicable row)

| Score | Financial (calibrate to revenue) | Operational | Regulatory / legal | Data subjects / customers | Reputation |
|---|---|---|---|---|---|
| 1 Minimal | < 0.1% revenue | < 1 hr disruption to non-critical service | None | No personal data | Internal only |
| 2 Minor | 0.1–0.5% | < 4 hrs to a critical service | Query from regulator | < 1,000 records, low sensitivity | Local / limited media |
| 3 Moderate | 0.5–2% | 4–24 hrs to a critical service | Mandatory report (CERT-In / DPDP Board / sector regulator) | 1,000–100,000 records or any sensitive category | National media, short-lived |
| 4 Major | 2–5% | 1–3 days to a critical service | Inspection, directions, penalty probable | > 100,000 records, or financial / health / children's data | Sustained national coverage, customer loss |
| 5 Severe | > 5% or threat to solvency | > 3 days; breach of the regulator's impact tolerance | Licence action, DPDP penalty at the upper end, prosecution | Mass exposure; harm to individuals | Loss of franchise / market confidence |

**Risk score = Likelihood × Impact** (1–25).

| Score | Rating | Default response |
|---|---|---|
| 20–25 | Critical | Escalate to Board/RMC; treat immediately; executive owner |
| 12–19 | High | Treatment plan within 30 days; CXO owner |
| 6–11 | Medium | Treatment within 90 days or formal acceptance |
| 1–5 | Low | Monitor; accept within appetite |

**Inherent risk** = rating before counting existing controls. **Residual risk** = rating after counting controls that are *evidenced as operating* (not merely documented). A documented but untested control should reduce likelihood by at most one point; mark it Assessed.

## 3. Maturity scale (for Workflow 2)

| Level | Name | Description |
|---|---|---|
| 0 | Non-existent | No practice |
| 1 | Initial | Ad hoc, person-dependent |
| 2 | Repeatable | Practised but not documented consistently |
| 3 | Defined | Documented, approved, communicated |
| 4 | Managed | Measured with metrics; reviewed; exceptions tracked |
| 5 | Optimised | Continuously improved; automated; benchmarked |

A regulated entity should generally target level 3 at minimum on regulator-mandated controls and level 4 on controls protecting critical services. Mark the target as Assessed.

## 4. Vendor tiering (for Workflow 4)

| Tier | Criteria (any one) | Assurance required |
|---|---|---|
| Tier 1 – Critical | Supports a critical business service; holds large volumes of personal or regulated data; has privileged or network access; hard to substitute | Full questionnaire, evidence review, contract security schedule, annual reassessment, right to audit exercised |
| Tier 2 – Important | Processes personal data in moderate volume; has user-level access; moderately substitutable | Questionnaire plus certificates, biennial reassessment |
| Tier 3 – Low | No data access, no connectivity, easily substitutable | Due-diligence checklist only |

## 5. Risk register template

| ID | Risk statement (threat → gap → asset → impact) | Owner | Asset / service | Inh. L | Inh. I | Inh. score | Existing controls | Res. L | Res. I | Res. score | Treatment | Action | Due | KRI | Status | Label |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CR-01 | Ransomware enters through phishing; no MFA on remote access; core banking and file servers encrypted; multi-day outage and CERT-In/RBI reporting | CIO | Core banking | 4 | 5 | 20 | EDR on 70% endpoints; daily backups (not immutable) | 4 | 5 | 20 | Mitigate | MFA on VPN/email; immutable offline backups; EDR to 100% | 60 days | % endpoints with EDR; days since last restore test | Open | Assessed |

Write risk statements as one sentence a non-specialist can follow.

## 6. Cyber risk appetite statement (template)

> [Organisation] has a **low** appetite for cyber risk that could disrupt [critical services] beyond [impact tolerance, e.g. 4 hours], compromise customer personal data, or result in a breach of law or regulatory direction. It has a **moderate** appetite for cyber risk arising from adopting new technology where compensating controls are in place and the risk is formally accepted by [role].

**Tolerances (examples):**
- Critical vulnerabilities on internet-facing systems patched within 7 days (target ≥ 95%).
- MFA coverage on privileged and remote access: 100%.
- Successful restore test of crown-jewel systems: at least every quarter.
- Tier 1 vendors assessed within 12 months: 100%.
- Incidents reported to CERT-In within 6 hours of noticing: 100%.

## 7. Board cyber risk report (template)

1. **Purpose and ask** (2–3 lines): decision, approval or assurance sought.
2. **Headline posture:** overall rating, trend arrow versus last quarter, one-sentence reason.
3. **Top risks against appetite:** a table of the top 5 with residual rating, trend, owner and the date by which it returns within appetite.
4. **Key Risk Indicators:** RAG table against tolerances.
5. **Incidents and near misses:** count, the material ones, regulatory reports made (CERT-In, DPDP Board, RBI/SEBI/IRDAI).
6. **Regulatory and audit:** open observations, upcoming deadlines, new rules.
7. **Programme progress:** roadmap milestones, budget used and still needed.
8. **Decisions requested:** risk acceptances, budget, policy approvals.
9. **Annexes:** full register, heat map, glossary.

## 8. KRI library (select 6–10)

| KRI | Typical tolerance |
|---|---|
| % critical/high vulnerabilities past SLA | < 5% |
| Mean time to patch internet-facing critical | ≤ 7 days |
| MFA coverage (privileged / remote / email) | 100% |
| EDR coverage of endpoints and servers | ≥ 98% |
| Phishing simulation click rate | < 5% and falling |
| Privileged accounts reviewed this quarter | 100% |
| Days since last successful restore test (crown jewels) | ≤ 90 |
| Tier 1 vendors with current assessment | 100% |
| Mean time to detect / contain (MTTD / MTTC) | Trend down |
| Regulatory reports made within deadline | 100% |
| Log sources retained ≥ 180 days in India (CERT-In) | 100% |
| Open high audit observations past due | 0 |
