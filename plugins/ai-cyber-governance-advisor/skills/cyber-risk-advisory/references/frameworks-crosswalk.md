# Frameworks Crosswalk

This is an indicative mapping for scoping and gap analysis. It is not an official crosswalk. For a certification audit, use the official texts: NIST publishes informative references for CSF 2.0, and ISO/IEC 27001:2022 Annex A has 93 controls in four themes.

## NIST CSF 2.0 function → ISO/IEC 27001:2022 → CIS Controls v8.1 → Indian overlay

| CSF 2.0 function / category | ISO/IEC 27001:2022 (clauses / Annex A) | CIS v8.1 | Indian overlay (verify current text) |
|---|---|---|---|
| **GOVERN (GV)** | | | |
| GV.OC Organisational context | Cl. 4.1–4.3 | — | RBI IT Governance MD 2023 (board/ITSC roles); SEBI CSCRF governance |
| GV.RM Risk management strategy | Cl. 6.1, 8.2, 8.3 | — | RBI MD: IT and cyber risk in ERM; IRDAI 2023 guidelines |
| GV.RR Roles and responsibilities | Cl. 5.3; A.5.2, A.5.3, A.6.x | — | CISO appointment (RBI, SEBI, IRDAI); CERT-In point of contact |
| GV.PO Policy | Cl. 5.2; A.5.1 | — | Board-approved cyber security policy (all sector regulators) |
| GV.OV Oversight | Cl. 9.2, 9.3 | — | Board / IT Strategy Committee review |
| GV.SC Supply chain risk management | A.5.19–A.5.23 | 15 | RBI outsourcing of IT services MD 2023; SEBI CSCRF third-party; DPDP s.8(2) |
| **IDENTIFY (ID)** | | | |
| ID.AM Asset management | A.5.9–A.5.13 | 1, 2, 3 | CSCRF asset inventory; DPDP data mapping |
| ID.RA Risk assessment | Cl. 6.1.2, 8.2; A.5.7, A.8.8 | 7 | Periodic VAPT (RBI, SEBI, IRDAI) |
| ID.IM Improvement | Cl. 10 | — | Audit closure tracking |
| **PROTECT (PR)** | | | |
| PR.AA Identity, authentication, access | A.5.15–A.5.18, A.8.2–A.8.5 | 5, 6 | MFA expectations in sector directions |
| PR.AT Awareness and training | A.6.3 | 14 | Board and staff training requirements |
| PR.DS Data security | A.5.33, A.5.34, A.8.10–A.8.12, A.8.24 | 3 | DPDP s.8(5) reasonable security safeguards; Rules 2025 safeguards; data localisation (RBI payment data) |
| PR.PS Platform security | A.8.9, A.8.19, A.8.25–A.8.32 | 4, 16 | Secure configuration baselines; SDLC |
| PR.IR Technology infrastructure resilience | A.5.29, A.5.30, A.8.13–A.8.14, A.8.20–A.8.22 | 11, 12 | BCP/DR drills; impact tolerances |
| **DETECT (DE)** | | | |
| DE.CM Continuous monitoring | A.8.15, A.8.16 | 8, 13 | CERT-In 180-day log retention in India; NTP sync; SOC (CSCRF) |
| DE.AE Adverse event analysis | A.5.25, A.8.16 | 8, 13 | CSCRF SOC efficacy |
| **RESPOND (RS)** | | | |
| RS.MA Incident management | A.5.24, A.5.26 | 17 | Cyber crisis management plan (CERT-In / sector) |
| RS.AN Incident analysis | A.5.25, A.5.28 | 17 | Forensic readiness; evidence for BSA s.63 |
| RS.CO Reporting and communication | A.5.5, A.5.6, A.5.24 | 17 | CERT-In 6 hours; DPDP Board intimation; RBI/SEBI/IRDAI |
| RS.MI Mitigation | A.5.26 | 17 | — |
| **RECOVER (RC)** | | | |
| RC.RP Recovery plan execution | A.5.29, A.5.30, A.8.13 | 11 | Restore within impact tolerance |
| RC.CO Recovery communication | A.5.24, A.5.26 | 17 | Customer / market disclosure (SEBI LODR for listed) |

## Testing (spans functions)

| Activity | ISO/IEC 27001 | CIS | Indian overlay |
|---|---|---|---|
| Vulnerability assessment and penetration testing (VAPT) | A.8.8, A.8.29 | 7, 18 | CERT-In empanelled auditors where required; sector frequency rules |
| Red team / cyber drill | A.5.24 | 18 | CERT-In / CSIRT-Fin drills; sector tabletop requirements |

## Related standards

- **ISO/IEC 27005:2022**: information security risk management. It allows event-based or asset-based risk identification, and the 5×5 method in this skill is consistent with it.
- **ISO/IEC 27002:2022**: implementation guidance for the Annex A controls.
- **ISO 22301:2019**: business continuity management.
- **ISO/IEC 27701:2019**: privacy information management extension (a revised edition has been published; verify the current version). Useful for DPDP/GDPR.
- **ISO/IEC 27017 / 27018**: cloud security / PII in public cloud.
- **NIST SP 800-30 Rev.1**: guide for conducting risk assessments.
- **NIST SP 800-161r1**: cyber supply chain risk management.
