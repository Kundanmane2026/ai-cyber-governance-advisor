# Sectoral and Global Overlay

**Verify before reliance.** Circulars are often amended or superseded. Search for each and record the date checked. DPDP s.16(2) preserves stricter sectoral rules on transfer abroad, and s.38 makes DPDP additional to other laws.

## 1. Indian sectoral data rules

| Sector | Instrument (verify current version) | Data-specific requirements |
|---|---|---|
| **Banking / payments (RBI)** | Storage of Payment System Data (06.04.2018) and FAQs | Entire payment system data stored **only in India**; foreign leg may be processed abroad but must be brought back (and deleted abroad) within the stipulated time |
| | Master Direction on IT Governance, Risk, Controls and Assurance Practices (2023) | Information security; data classification; access control; IS audit |
| | Master Direction on Outsourcing of IT Services (2023) | Confidentiality and security of customer data with vendors; regulator access; data location |
| | Digital Lending Directions (2025 consolidation; verify) | Data collection need-based with explicit consent; no access to phone resources (contacts, media) except one-time camera/mic/location for KYC with consent; storage in India; deletion policy |
| | KYC Master Direction | Customer data confidentiality; CKYCR |
| | Credit Information Companies (Regulation) Act 2005 | Credit data handling and access |
| **Securities (SEBI)** | Cybersecurity and Cyber Resilience Framework (CSCRF, 2024) | Data classification and localisation expectations for certain REs; log retention; cloud adoption framework (2023) |
| **Insurance (IRDAI)** | Information and Cyber Security Guidelines (2023); Outsourcing Regulations; Maintenance of Insurance Records Regulations | Records (including electronic) held in India; data security; policyholder confidentiality |
| **Pensions (PFRDA)** | Cyber security and outsourcing circulars | Subscriber data protection |
| **Health** | ABDM Health Data Management Policy; Telemedicine Practice Guidelines 2020; Clinical Establishments Act / state rules; MCI/NMC ethics (patient confidentiality) | Consent-based health data exchange; record retention |
| **Telecom** | Telecommunications Act 2023; Telecom Cyber Security Rules 2024; licence conditions (Unified Licence) | Subscriber data confidentiality; lawful interception; data localisation under licence; incident reporting |
| **Government / public sector** | MeitY guidelines; NIC policies; CERT-In guidelines for government entities (2023) | Hosting with empanelled cloud providers (MeitY empanelment); classification |
| **All (CERT-In)** | Directions 28.04.2022 | ICT logs 180 days in India; incident reporting; KYC for VPN/VPS/cloud |
| **Employment** | Labour codes (as notified); state Shops and Establishments Acts | Employee records retention periods |

## 2. Global overlay: when each applies

| Regime | Territorial trigger | Must-know points for an Indian entity |
|---|---|---|
| **GDPR (EU) 2016/679** | Art. 3(1): establishment in the EU. Art. 3(2): offering goods/services to, or monitoring the behaviour of, individuals in the EU | Art. 27 EU representative if no establishment; Art. 6 lawful bases; Art. 9 special categories; Art. 28 processor contracts; Art. 30 records; Art. 32 security; Art. 33/34 breach (72 h); Art. 35 DPIA; Art. 37 DPO; **Chapter V transfers**: no EU adequacy decision for India, so Indian importers receiving EU data typically sign **SCCs (2021/914)** with a transfer impact assessment and supplementary measures |
| **UK GDPR + DPA 2018** | UK establishment or targeting | IDTA or the UK Addendum to the EU SCCs |
| **NIS2 Directive (EU) 2022/2555** | Essential/important entities providing services in the EU (sector + size rules); non-EU providers of certain digital services must designate an EU representative | Art. 20 management body accountability and training; Art. 21 risk-management measures (including supply-chain security); Art. 23 reporting (24 h / 72 h / 1 month); member-state transposition differs, so verify the national law |
| **DORA (EU) 2022/2554** (applies from 17.01.2025) | EU financial entities; **ICT third-party service providers** to them (Indian IT services firms commonly are) | ICT risk management framework; incident classification and reporting; digital operational resilience testing (TLPT for significant entities); Art. 28–30 contractual requirements for ICT providers (service levels, locations, audit, exit, cooperation); critical ICT third-party provider oversight |
| **EU AI Act** | See the `ai-governance-risk` skill | — |
| **US** | Operations, data subjects, or listing in the US | State comprehensive privacy laws (California CCPA/CPRA and others); sectoral (HIPAA, GLBA); SEC cyber disclosure; FTC Act s.5 |
| **Others** | Operations there | Singapore PDPA, UAE PDPL / DIFC DP Law, Saudi PDPL, Australia Privacy Act; verify locally |

## 3. Indian IT/ITeS service providers serving EU clients: typical stack

1. Client is the GDPR controller; the Indian entity is the processor. **Art. 28 DPA** plus **SCCs Module 2 (controller-to-processor)** or **Module 3 (processor-to-processor)**.
2. A **transfer impact assessment** covering Indian government access laws (IT Act s.69, CERT-In Directions, DPDP s.36 information calls). Document the safeguards (encryption, access controls, challenge policy for government requests).
3. If the client is an EU financial entity: **DORA Art. 30** contract clauses plus participation in the client's resilience testing.
4. If the client is an NIS2 entity: supply-chain security requirements flowed down.
5. Internally, the Indian entity is still a DPDP Data Fiduciary for its own employee and business data. Client data processed for foreign clients may fall under the **s.17(1)(d) exemption** (processing of non-residents' personal data under a contract with a person outside India), but **s.8(5) security and the CERT-In duties still apply**. Verify the scope of the exemption.

## 4. Conflict handling rule

Where obligations differ (for example breach timelines, retention, localisation), **meet the strictest applicable requirement** unless meeting it would breach another law. Document the conflict and the decision, with legal sign-off.

| Topic | India | EU | Approach |
|---|---|---|---|
| Breach notice timing | CERT-In 6 h; DPDP Board without delay plus a 72 h report | GDPR 72 h; NIS2 24 h early warning | Prepare for 6 h; parallel tracks |
| Log retention | CERT-In 180 days (India); DPDP Rule 6 one year | GDPR storage limitation | Retain security logs per Indian law; minimise their personal data content; document the legal obligation basis |
| Localisation | RBI payment data; sectoral | Transfer restrictions on EU data leaving the EU | Data-flow map per regime |
| Children | Under 18 | Under 16 (13–16 by member state) | Design to 18 for India-facing services |
