# Regulatory Reporting: India First, with Global Overlay

**Verify before reliance.** Timelines, formats, portals and addresses change. Web-search the official source for each row, and record the URL and the date checked in the deadline table.

## 1. Decision tree

```
Incident noticed / notified  →  record time T0 (IST)
│
├─ Q1. Is it a CERT-In reportable incident type (Annex I, Directions 28.04.2022)?
│      Yes → Report to CERT-In within 6 hours of T0 (deadline = T0 + 6h)
│
├─ Q2. Could personal data (digital) have been breached?  (DPDP s.2(u): unauthorised
│      processing, accidental disclosure, acquisition, sharing, use, alteration,
│      destruction or loss of access that compromises confidentiality, integrity
│      or availability)
│      Yes → Intimate Data Protection Board without delay; detailed report within 72h;
│            intimate each affected Data Principal without delay  (DPDP Rules 2025)
│      If you are a Data Processor → notify the Data Fiduciary immediately per contract
│
├─ Q3. Is the entity regulated by RBI / SEBI / IRDAI / PFRDA / DoT / CEA / NCIIPC?
│      Yes → sector report in the sector window (often 6h, verify), plus CSIRT-Fin if financial
│
├─ Q4. Is it a listed entity?  → assess materiality under SEBI LODR Reg. 30; disclose to
│      stock exchanges in the prescribed time if material
│
├─ Q5. Foreign triggers? (EU/UK data subjects, NIS2/DORA entity, SEC registrant, other)
│      → overlay table, section 4
│
├─ Q6. Contractual duties? (clients, partners, payment networks, insurer)
│      → check notice clauses; insurer notice is often a condition of cover
│
└─ Q7. Crime? (fraud, extortion, data theft)  → consider cybercrime.gov.in / 1930 / FIR
```

## 2. CERT-In Directions (No. 20(3)/2022-CERT-In, 28.04.2022, under IT Act s.70B(6))

| Item | Requirement (verify) |
|---|---|
| Who | Service providers, intermediaries, data centres, body corporates and government organisations |
| What | Annex I incident types. They include targeted scanning/probing of critical systems; compromise of critical systems/information; unauthorised access to IT systems/data; website defacement or intrusion; malicious code / ransomware; attacks on servers (database, mail, DNS) and network devices; identity theft, spoofing and phishing; DoS/DDoS; attacks on critical infrastructure, SCADA/OT and wireless networks; attacks on e-governance, e-commerce and payment systems; data breach; data leak; attacks on IoT devices; attacks on digital payment systems; malicious mobile apps; fake mobile apps; unauthorised access to social media accounts; attacks or suspicious activity on cloud; and attacks on Big Data, blockchain, crypto-assets, robotics, 3D/4D printing, additive manufacturing, drones and AI/ML systems. **Check the current Annex.** |
| When | Within **6 hours** of noticing or being brought to notice |
| How | Email incident@cert-in.org.in (or the current channel), using the format on the CERT-In website. Partial information is acceptable at first; update later |
| Other duties | Point of Contact designated to CERT-In; NTP sync; ICT logs kept 180 days in India and produced on demand; KYC retention for VPN/VPS/cloud/data centre and VASP |

## 3. DPDP Act 2023 and DPDP Rules 2025 (personal data breach)

**Commencement:** the Rules were notified in November 2025 with phased commencement. Confirm whether the breach intimation provisions are in force on the incident date. If they are not, the SPDI Rules 2011 / IT Act s.43A regime and CERT-In still apply.

| Recipient | Timing | Content (Rules; verify) |
|---|---|---|
| **Data Protection Board**, initial | Without delay on becoming aware | Description of the breach: nature, extent, timing, location, likely impact |
| **Data Protection Board**, detailed | **Within 72 hours** of becoming aware (or a longer period the Board allows on written request) | Updated and detailed description; broad facts on events, circumstances and reasons; mitigation measures; findings on the person who caused it (if known); remedial measures to prevent recurrence; report on intimations given to Data Principals |
| **Each affected Data Principal** | Without delay, through the user account or registered communication mode | Concise, clear, plain-language description (nature, extent, timing, location); likely consequences; mitigation measures taken; safety measures the Data Principal can take; business contact of a person who can answer questions |

**Penalty exposure (Schedule; verify):** failure to take reasonable security safeguards to prevent a breach can attract up to ₹250 crore; failure to notify the Board or Data Principals up to ₹200 crore.

**Data Processor:** the Act places the duty on the Data Fiduciary, so the contract must require the processor to notify immediately with full cooperation.

## 4. Sector regimes (verify every row)

| Regulator | Instrument | Report to | Window |
|---|---|---|---|
| RBI | Master Direction on IT Governance, Risk, Controls and Assurance Practices (2023); cyber security frameworks; payment system directions | RBI (DoS / CSITE or as specified), CERT-In, CSIRT-Fin | Commonly within 6 hours for cyber incidents; format as prescribed |
| SEBI | CSCRF (20.08.2024) and incident reporting circulars | SEBI, CERT-In, CSIRT-Fin, NCIIPC if protected system | Commonly within 6 hours; follow-up RCA within the prescribed days |
| IRDAI | Information and Cyber Security Guidelines (24.04.2023) | CERT-In within 6 h; IRDAI as specified | Verify |
| PFRDA | Cyber security policy circulars | PFRDA, CERT-In | Verify |
| DoT | Telecom Cyber Security Rules 2024 | DoT portal | Initial report about 6 h; details in about 24 h (verify) |
| NCIIPC | Notified CII / protected systems | NCIIPC (plus CERT-In) | As notified |
| SEBI LODR | Reg. 30 material events for listed entities | Stock exchanges | Within 24 hours of the materiality determination (verify current rule) |

## 5. Global overlay (only when triggered)

| Regime | Trigger | Deadline |
|---|---|---|
| GDPR / UK GDPR Art. 33 | Controller with EU/UK nexus | Supervisory authority within 72 hours of awareness |
| GDPR Art. 34 | High risk to individuals | Data subjects without undue delay |
| NIS2 Art. 23 | Essential or important entity in the EU | Early warning 24 h; incident notification 72 h; final report 1 month |
| DORA | EU financial entity | Initial, intermediate and final reports per the RTS (initial within 4 h of classification as major / 24 h of detection; verify) |
| US SEC Form 8-K Item 1.05 | SEC registrant, material incident | Four business days after the materiality determination |
| US state breach laws, HIPAA, NYDFS 500 | As applicable | Varies (NYDFS 72 h to the regulator) |

## 6. Notification content checklist (generic)

- Reporting entity, Point of Contact, contact details.
- Time noticed (T0); time of occurrence if known.
- Incident type (use the regulator's taxonomy).
- Affected systems, services, locations.
- Data involved: categories, approximate volume, whether personal / sensitive / children's data.
- Current status: ongoing or contained; actions taken.
- Indicators of compromise (IOCs) where known (shared defensively).
- Impact on customers, Data Principals and services.
- Other authorities notified.
- A statement that information is preliminary, with the next update time.

## 7. Deadline tracker (template)

| Regime | Trigger met? (label) | Deadline (IST) | Recipient / channel | Owner | Submitted (IST) | Reference no. | Verified source + date |
|---|---|---|---|---|---|---|---|
| CERT-In | Yes (Assessed) | T0 + 6 h | incident@cert-in.org.in | CISO | | | |
| DPDP Board, initial | | Without delay | Board portal / channel | DPO | | | |
| DPDP Board, 72 h report | | T0 + 72 h | | DPO | | | |
| Data Principals | | Without delay | Email / SMS / app | DPO + Comms | | | |
| Sector regulator | | | | Compliance | | | |
| Insurer | | Per policy | | CFO / Legal | | | |
