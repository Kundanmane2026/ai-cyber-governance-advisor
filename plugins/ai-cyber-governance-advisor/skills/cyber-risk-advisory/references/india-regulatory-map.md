# India Regulatory Map (with Global Overlay)

**Verify before reliance.** This map reflects the position as drafted. Directions, circulars, deadlines and penalty amounts change often. Before relying on any row, web-search the official source and record the date you checked. Official sites: meity.gov.in, cert-in.org.in, egazette.gov.in, rbi.org.in, sebi.gov.in, irdai.gov.in, nciipc.gov.in, dot.gov.in, pfrda.org.in.

## 1. Cross-sector

| Regime | Applies to | Core obligations | Reporting / timelines |
|---|---|---|---|
| **IT Act 2000** | All | s.43 (unauthorised access/damage, civil liability); s.43A (body corporate failing reasonable security for sensitive personal data: compensation; to be omitted when DPDP s.44 is commenced, so verify status); s.66-series offences; s.69 interception and decryption directions; s.70 Critical Information Infrastructure / protected systems; s.70B CERT-In powers; s.72A disclosure in breach of lawful contract (civil penalty up to ₹25 lakh since the Jan Vishwas Act 2023, in force 30.11.2023); s.79 intermediary safe harbour | See CERT-In row |
| **CERT-In Directions under s.70B(6)** (No. 20(3)/2022-CERT-In, 28.04.2022) and the FAQs | Service providers, intermediaries, data centres, body corporates, government organisations | Report listed cyber incidents **within 6 hours** of noticing or being notified; designate a Point of Contact; sync clocks to NIC/NPL NTP (or traceable sources); keep ICT system logs **180 days within India**; data centres, VPS, cloud and VPN providers keep subscriber KYC **5 years**; VASPs keep KYC/transaction records **5 years** | 6 hours to incident@cert-in.org.in in the prescribed format; respond to CERT-In information requests within the stated time |
| **DPDP Act 2023 + DPDP Rules 2025** (Rules notified November 2025 with phased commencement; verify which provisions are in force) | Data Fiduciaries processing digital personal data in India, or offering goods/services to Data Principals in India from abroad | s.8(5) reasonable security safeguards; s.8(6) intimate personal data breach to the Data Protection Board and each affected Data Principal; s.8(7) erasure; s.9 children; s.10 Significant Data Fiduciary duties (DPO in India, independent data auditor, DPIA); s.16 cross-border transfer (negative-list approach); Schedule penalties up to ₹250 crore | Rules: intimate the Board and affected Data Principals without delay; detailed report to the Board **within 72 hours** of becoming aware (or longer if the Board allows); verify the current rule text |
| **SPDI Rules 2011** (under s.43A) | Body corporates | Reasonable security practices (ISO/IEC 27001 is deemed compliant); privacy policy; consent for sensitive personal data | Being replaced by the DPDP regime; confirm the transition status |
| **NCIIPC / CII** (s.70; notified protected systems) | Notified CII entities | Protected system rules; CISO; audits; NCIIPC reporting | As notified per entity |
| **Telecommunications Act 2023 + Telecom Cyber Security Rules 2024** | Telecommunication entities | Security policy, CTSO, incident reporting | Short-window incident reporting to DoT (verify: about 6 hours initial) |

## 2. Financial sector

| Regime | Applies to | Core obligations | Reporting |
|---|---|---|---|
| **RBI Master Direction on IT Governance, Risk, Controls and Assurance Practices** (07.11.2023, effective 01.04.2024) | Banks, NBFCs (upper/middle layers), other regulated entities as listed | Board-level IT Strategy Committee; IT and information security policies; CISO; IT and cyber risk management; BCP/DR; IS audit | Cyber incidents to RBI within the prescribed window (verify: 6 hours) and to CERT-In |
| **RBI Master Direction on Outsourcing of IT Services** (10.04.2023) | Same | Due diligence, contractual safeguards, audit rights, concentration risk, exit plans | — |
| **RBI cyber security frameworks** (banks 2016; UCBs graded framework; payment system operators; digital payment security controls) | As applicable | Baseline controls, C-SOC, CCMP | As per circular |
| **RBI payment data storage** (06.04.2018) | Payment system operators | Payment system data stored only in India | — |
| **SEBI Cybersecurity and Cyber Resilience Framework (CSCRF)** (20.08.2024, phased) | SEBI Regulated Entities (categorised) | Governance, identify / protect / detect / respond / recover, SOC, VAPT, cyber audit, third-party risk | Incidents to SEBI and CERT-In / CSIRT-Fin within the prescribed window (verify: 6 hours) |
| **IRDAI Information and Cyber Security Guidelines** (24.04.2023) | Insurers, intermediaries | Board-approved policy; CISO; VAPT; audit; log retention; SOC | Incidents to CERT-In within 6 hours and to IRDAI as specified |
| **PFRDA cyber security guidelines** | Pension intermediaries | Policy, audits, reporting | Verify current circular |
| **CSIRT-Fin** | Financial sector | Sector CSIRT coordination with CERT-In | As directed |

## 3. Other relevant sectors (verify)

- **Health:** ABDM Health Data Management Policy; DISHA has not been enacted (check its status); hospitals under state regimes.
- **Power:** CEA (Cyber Security in Power Sector) Guidelines / Regulations.
- **Government:** MeitY / NIC information security policies; CERT-In guidelines for government entities (2023).
- **Listed companies:** SEBI LODR disclosure of material events, which may include material cyber incidents.

## 4. Global overlay (apply only if triggered)

| Regime | Trigger | Key points |
|---|---|---|
| **GDPR (EU) / UK GDPR** | Establishment in EU/UK, or offering to / monitoring EU/UK individuals | Art. 32 security; Art. 33 notify the supervisory authority within 72 hours; Art. 34 notify data subjects for high risk; transfer mechanisms |
| **NIS2 Directive (EU) 2022/2555** | Essential / important entities operating in the EU | Art. 21 risk-management measures; Art. 23 early warning in 24 hours, notification in 72 hours, final report in 1 month; management body liability |
| **DORA (EU) 2022/2554** (applies from 17.01.2025) | EU financial entities and critical ICT third-party providers | ICT risk framework, incident classification and reporting, TLPT, third-party register |
| **US** | Operations / data in the US | SEC cyber disclosure (Form 8-K Item 1.05, four business days after materiality determination) for SEC registrants; state breach laws; sector rules (HIPAA, GLBA, NYDFS 23 NYCRR 500) |
| **Singapore / UAE / others** | Operations there | PDPA, CSA, local regulators: verify case by case |

## 5. How to use this map

1. Determine the facts (Workflow 5, step 1).
2. Pick every row that applies, and mark each pick Observed (the entity confirmed it) or Assumed.
3. Search and verify each, then record the source URL and the date checked.
4. Build the obligations matrix: regime → obligation → owner → evidence → status.
5. Where two timelines conflict, plan to meet the **shortest** one (usually CERT-In's 6 hours) and prepare the others in parallel.
