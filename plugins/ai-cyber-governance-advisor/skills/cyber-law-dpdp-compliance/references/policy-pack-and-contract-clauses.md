# Policy Pack and Contract Clauses

Templates for an advocate's review. Replace the [placeholders]. Keep definitions consistent with the DPDP Act s.2 across all documents.

## 1. Policy pack: contents

| # | Document | Audience | Key sources | Approver | Review |
|---|---|---|---|---|---|
| 1 | Privacy notice (external) | Data Principals | DPDP s.5, Rule 3; GDPR Art. 13/14 if applicable | Legal / DPO | Annual + on change |
| 2 | Data protection policy (internal) | Staff | DPDP Act; Rules | Board / RMC | Annual |
| 3 | Information security policy | Staff, vendors | DPDP s.8(5), Rule 6; ISO/IEC 27001; CERT-In; sector | Board | Annual |
| 4 | Data retention and erasure schedule | Data owners, IT | s.8(7), Rule 8; sector retention laws | DPO + Legal | Annual |
| 5 | Personal data breach response procedure | IR team | s.8(6), Rule 7; CERT-In; sector | CISO + DPO | Annual + post-incident |
| 6 | Data Principal rights procedure | Customer support, DPO | s.11–14, Rule 14 | DPO | Annual |
| 7 | Consent management standard | Product, engineering | s.6, Rule 3, Rule 4 | DPO | Annual |
| 8 | Children's data standard | Product | s.9, Rules 10–12 | DPO | Annual |
| 9 | Vendor / processor management policy | Procurement | s.8(2); sector outsourcing rules | CRO | Annual |
| 10 | Cross-border transfer standard | Legal, IT | s.16; sector localisation; GDPR Ch. V | Legal | Annual |
| 11 | DPIA procedure | Product, DPO | s.10, Rule 13; GDPR Art. 35 | DPO | Annual |
| 12 | Acceptable use and monitoring policy | Employees | s.7(i) employment; IT Act | HR + Legal | Annual |
| 13 | Grievance redressal policy | Data Principals | s.8(10), s.13 | DPO | Annual |

## 2. Privacy notice skeleton (DPDP Rule 3 aligned)

```
[ORGANISATION] PRIVACY NOTICE                               Last updated: [date]
Available in: English | [Marathi] | [Hindi] | [other Eighth Schedule language]

1. Who we are and how to contact us
   [Name, address]. Data Protection Officer / contact: [name/role, email, phone]   (s.8(9), Rule 9)
2. What personal data we collect and why
   | Personal data (itemised) | Purpose (specified) | Goods / service enabled | Legal ground (consent / legitimate use – s.7(_)) |
3. How long we keep it      [retention per category / criteria]
4. Who we share it with     [categories of Data Processors / recipients; purpose]
5. Transfers outside India  [countries/regions; safeguards]
6. Your rights              access information (s.11) · correction, completion, updating, erasure (s.12) ·
                            grievance redressal (s.13) · nominate (s.14) · withdraw consent anytime (s.6(4))
   How to exercise:         [link / in-app path / email]
7. Withdrawing consent      [link — as easy as giving consent]; consequences of withdrawal
8. Children                 [age gate; parental consent process; no targeted advertising to children]
9. Security                 [summary of safeguards]
10. Complaints              Contact us first: [grievance channel; resolution time]. You may then complain
                            to the Data Protection Board of India: [link / manner]
11. Changes to this notice
```

## 3. DPA clause bank (Data Fiduciary → Data Processor)

| # | Clause | Model wording (adapt) |
|---|---|---|
| 1 | Roles and scope | "The Processor shall process Personal Data only on behalf of the Fiduciary, for the purposes and in the manner set out in Annex 1 (subject matter, duration, nature, purpose, categories of data and Data Principals)." |
| 2 | Instructions | "The Processor shall process Personal Data only on documented instructions of the Fiduciary and shall immediately inform the Fiduciary if an instruction appears to infringe Applicable Data Protection Law." |
| 3 | Confidentiality | "The Processor shall ensure that persons authorised to process Personal Data are bound by written confidentiality obligations and receive appropriate training." |
| 4 | Security | "The Processor shall implement and maintain the technical and organisational measures in Schedule [S] (Security Schedule), which shall be no less protective than the reasonable security safeguards required under Section 8(5) of the DPDP Act and Rule 6 of the DPDP Rules 2025." |
| 5 | Sub-processors | "The Processor shall not engage a sub-processor without the Fiduciary's prior [specific/general] written authorisation, shall impose equivalent obligations by written contract, and remains fully liable for the sub-processor's acts." |
| 6 | Breach notification | "The Processor shall notify the Fiduciary without undue delay and in any event within [2–4] hours of becoming aware of any actual or suspected Personal Data Breach or cyber security incident affecting the Services, providing all information reasonably required for the Fiduciary to comply with Section 8(6) of the DPDP Act, Rule 7 of the DPDP Rules, the CERT-In Directions dated 28.04.2022 and [sectoral requirements], and shall cooperate in investigation, containment and notification." |
| 7 | Assistance with rights | "The Processor shall promptly (within [3] business days) forward any Data Principal request and assist the Fiduciary in responding within the applicable timelines." |
| 8 | Accuracy | "Where the Processor collects or updates Personal Data, it shall take reasonable steps to ensure completeness, accuracy and consistency." |
| 9 | Erasure and return | "On termination, or on the Fiduciary's instruction (including on withdrawal of consent or end of purpose), the Processor shall erase or return all Personal Data within [30] days and certify erasure in writing, save as retention is required by law (which shall be notified to the Fiduciary)." |
| 10 | Audit | "The Processor shall make available all information necessary to demonstrate compliance and allow audits and inspections by the Fiduciary, its auditors and any Regulator, on [reasonable] notice." |
| 11 | Cross-border | "The Processor shall not transfer or permit access to Personal Data outside India [or: outside the locations in Annex 2] without the Fiduciary's prior written consent and shall comply with Section 16 of the DPDP Act and [sectoral localisation requirements]." |
| 12 | Logs and records | "The Processor shall maintain logs of processing activities and access for at least [one year / 180 days in India per CERT-In], and make them available on request." |
| 13 | Government requests | "Unless legally prohibited, the Processor shall notify the Fiduciary of any request by a public authority for Personal Data and disclose only the minimum required." |
| 14 | Liability and indemnity | "The Processor shall indemnify the Fiduciary against losses, penalties (to the extent permitted by law) and claims arising from the Processor's breach of this DPA. [Carve out data-breach liability from the general cap / set a super-cap of ___]." |
| 15 | Survival | "Obligations relating to confidentiality, security, erasure and audit survive termination until all Personal Data is erased or returned." |
| 16 | Precedence | "In case of conflict between this DPA and the Agreement in relation to Personal Data, this DPA prevails." |

## 4. Security schedule (baseline)

| Domain | Minimum requirement |
|---|---|
| Governance | Named security lead; information security policy; ISO/IEC 27001 certification or equivalent [preferred] |
| Access control | Least privilege; MFA for all remote, privileged and cloud console access; quarterly access reviews; prompt revocation on exit |
| Encryption | In transit (TLS 1.2+); at rest (AES-256 or equivalent); key management with segregation of duties |
| Logging and monitoring | Security logs centralised; retained [1 year; 180 days within India]; clock synced to NTP (NIC/NPL); monitored 24×7 for [Tier 1] |
| Vulnerability management | Critical patches ≤ [7] days on internet-facing systems, ≤ [14] days internal; annual independent penetration test; summary shared |
| Endpoint and malware | EDR on all endpoints and servers handling Fiduciary data |
| Backups and resilience | Encrypted, tested backups; RTO/RPO per Annex; at least one immutable/offline copy |
| Secure development | SDLC with code review, SAST/DAST/SCA; secrets management; SBOM on request |
| Personnel | Background verification; confidentiality undertakings; annual training |
| Physical | Access-controlled facilities; secure media disposal with certificates |
| Data segregation | Logical segregation of the Fiduciary's data from other clients |
| Incident response | Documented IR plan; notification per Clause 6; forensic cooperation; evidence preservation |
| AI use | No use of Fiduciary data to train models without written consent; disclose AI sub-processors |
| Assurance | Annual SOC 2 Type II / ISO certificate; questionnaire responses; right to audit |

## 5. DPA review checklist (reviewing a counterparty's paper)

- [ ] Roles correctly characterised (Fiduciary/Processor; controller/processor for GDPR)
- [ ] Processing description complete (Annex 1)
- [ ] Processing only on instructions; no independent use (including analytics or AI training)
- [ ] Security measures specific, not "industry standard" only
- [ ] Breach notice in **hours**, not "without undue delay" only; content requirements stated
- [ ] Sub-processor list, notification of changes, objection right, flow-down
- [ ] Data location and transfer restrictions; sectoral localisation respected
- [ ] Erasure/return with certification; timeline
- [ ] Audit rights for the client **and its regulator** (required by RBI/SEBI/IRDAI outsourcing rules)
- [ ] Assistance with rights requests and DPIAs
- [ ] Government access request handling
- [ ] Liability: data-breach losses not trapped under a low general cap
- [ ] Governing law and dispute resolution consistent with the main agreement
- [ ] GDPR SCCs / DORA Art. 30 clauses where triggered

**Issues table format:**

| Clause | Current wording (Observed) | Issue | Risk (H/M/L) | Proposed wording | Fallback |
|---|---|---|---|---|---|
