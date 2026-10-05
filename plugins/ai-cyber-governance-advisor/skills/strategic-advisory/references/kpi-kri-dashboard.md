# KPI and KRI Dashboard

**KPI** = is the programme performing? **KRI** = is the risk moving towards or beyond tolerance? Pick 6–12 per audience. This library extends the KRI list in `cyber-risk-advisory/references/risk-methodology-and-templates.md`; reuse those tolerances so the numbers match the risk register.

Tolerances below are typical starting points. Mark them **Assessed** until the organisation adopts its own, and mark any metric whose data source is not yet confirmed as **Assumed**.

## 1. Cyber security

| Metric | Type | Formula | Typical tolerance |
|---|---|---|---|
| Critical/high vulnerabilities past SLA | KRI | Past-SLA count ÷ open critical/high | < 5% |
| MFA coverage (privileged / remote / email) | KRI | Accounts with MFA ÷ in-scope accounts | 100% |
| EDR coverage | KRI | Endpoints with healthy agent ÷ asset inventory | ≥ 98% |
| Phishing simulation report rate | KPI | Reported ÷ delivered | Rising; > 60% |
| Days since last successful crown-jewel restore test | KRI | Today − last test date | ≤ 90 |
| Log sources retained ≥ 180 days in India | KRI | Compliant sources ÷ required sources | 100% (CERT-In) |
| Tier 1 vendors with current assessment | KRI | Assessed in 12 months ÷ Tier 1 vendors | 100% |
| Security roadmap milestones on time | KPI | On-time ÷ due | ≥ 85% |

## 2. Incident response

| Metric | Type | Formula | Typical tolerance |
|---|---|---|---|
| Mean time to detect (MTTD) | KRI | Average detection − start | Falling trend |
| Mean time to contain (MTTC) | KRI | Average containment − detection | Falling trend |
| CERT-In reports within 6 hours | KRI | On-time ÷ reportable incidents | 100% |
| DPDP Board detailed reports within 72 hours | KRI | On-time ÷ notifiable breaches | 100% (verify current rule) |
| Tabletop exercises completed | KPI | Held ÷ planned | 100%; at least annually per playbook |
| Post-incident actions closed on time | KPI | Closed on time ÷ due | ≥ 90% |

## 3. Privacy and DPDP

| Metric | Type | Formula | Typical tolerance |
|---|---|---|---|
| Processing activities with a valid notice and lawful basis | KRI | Compliant ÷ inventoried activities | 100% |
| Data Principal requests answered within the committed time | KPI | On-time ÷ received | ≥ 95% |
| Consent withdrawals actioned within the committed time | KRI | On-time ÷ received | 100% |
| Data Processors with a compliant contract | KRI | Compliant ÷ processors | 100% |
| Records past retention still held | KRI | Count | 0 and falling |
| DPIAs completed for high-risk processing (SDF) | KRI | Completed ÷ required | 100% |

## 4. AI governance

| Metric | Type | Formula | Typical tolerance |
|---|---|---|---|
| AI systems in inventory with an owner and risk tier | KRI | Complete records ÷ known systems | 100% |
| High-risk / material AI systems with an impact assessment | KRI | Assessed ÷ in scope | 100% |
| Shadow-AI tools discovered not yet assessed | KRI | Count | Falling to 0 |
| AI incidents (harmful output, data leak, bias complaint) | KRI | Count per quarter | Trend; each reviewed |
| Staff completing AI literacy training | KPI | Trained ÷ in-scope staff | ≥ 90% (EU AI Act Art. 4 where applicable) |
| Vendor AI contracts reviewed against checklist | KPI | Reviewed ÷ AI vendors | 100% |

## 5. Delivery (engagement or programme)

| Metric | Type | Formula | Target |
|---|---|---|---|
| Milestones met | KPI | On time ÷ due | ≥ 85% |
| Budget variance | KPI | (Actual − plan) ÷ plan | Within ±10% |
| Open high RAID items past due | KRI | Count | 0 |
| Deliverables accepted first time | KPI | Accepted without major rework ÷ delivered | ≥ 80% |
| Client dependencies late | KRI | Count | 0 |

## 6. Metric definition template

| Field | Entry |
|---|---|
| Name | |
| KPI or KRI | |
| Linked risk / objective | Risk register ID or programme objective |
| Owner | |
| Data source and system | |
| Formula | |
| Frequency | |
| Tolerance / target | |
| RAG thresholds | Green: … Amber: … Red: … |
| Action on Red | Who is notified, what happens, by when |
| Basis | Observed / Assessed / Assumed |

## 7. Dashboard layouts by audience

**Board / committee (quarterly, one page)**

```
Headline posture: [Rating]  Trend: [▲ ▼ ▶]  vs last quarter
Top 5 risks vs appetite      | 6–8 KRIs (RAG + trend)
Incidents & regulatory reports | Decisions requested
```

**Management (monthly)**

```
KRIs by domain (cyber / IR / privacy / AI) with RAG and 6-month trend
Roadmap milestones and budget
Exceptions: metrics in Red, owner, action, date
```

**Delivery team (weekly)**

```
Milestones, RAID items, dependencies, change requests, effort burn
```

Rules: show a trend, not only a number; every Red item has an owner and a date; never mix scales across dashboards; note data-quality limits in a footnote.
