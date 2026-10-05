# IR Plan Structure and Scenario Playbooks

All content is defensive. Playbooks describe what the defender does. They do not describe how attacks are carried out.

## 1. NIST SP 800-61 Rev. 3 mapping

Rev. 3 (April 2025) replaces the stand-alone four-phase lifecycle with incident response integrated into the CSF 2.0 functions:

| CSF 2.0 function | IR role | Classic 800-61r2 phase |
|---|---|---|
| Govern (GV) | IR policy, roles, risk strategy, supplier expectations | Preparation |
| Identify (ID) | Asset and risk knowledge; improvement from lessons learned | Preparation / Post-incident |
| Protect (PR) | Controls that reduce incident likelihood and impact | Preparation |
| Detect (DE) | Monitoring and adverse event analysis | Detection and Analysis |
| Respond (RS) | Incident management, analysis, reporting, communication, mitigation | Containment, Eradication |
| Recover (RC) | Restoration and recovery communications | Recovery / Post-incident |

International reference: ISO/IEC 27035-1/-2 (incident management principles, planning and preparation).

## 2. Severity matrix

| Severity | Criteria (any one) | Escalation | Update cadence |
|---|---|---|---|
| **SEV-1 Critical** | Critical service down or at imminent risk; confirmed exfiltration of sensitive or large-volume personal data; ransomware spreading; regulator or media aware | CEO, Board chair (or RMC chair), CISO, Legal, DPO; activate the crisis team | Every 2 h |
| **SEV-2 High** | Confirmed compromise contained to a limited scope; personal data possibly affected; important service degraded | CISO, CIO, Legal, DPO | Every 4 h |
| **SEV-3 Medium** | Suspicious activity under investigation; single host or account; no data impact known | SOC lead, IT owner | Daily |
| **SEV-4 Low** | Policy violation or blocked attempt; no compromise | SOC | Close in ticket |

Reportability is decided separately from severity: a SEV-3 can still be CERT-In reportable.

## 3. RACI (core roles)

| Activity | Incident Commander | Technical Lead | Legal / DPO | Comms | Business Owner | Exec Sponsor |
|---|---|---|---|---|---|---|
| Declare incident and severity | A | R | C | I | C | I |
| Containment decisions affecting production | A | R | C | I | C | C (SEV-1) |
| Evidence preservation | A | R | C | – | I | – |
| Regulatory notification decision | C | C | A/R | C | I | I |
| Notification submission | I | C | R | – | – | A |
| Public / customer statements | C | C | C | R | C | A |
| Engage external IR / forensics | R | C | A (privilege) | – | – | C |
| Recovery and return to service | A | R | I | I | R | I |
| Post-incident review | A | R | C | C | C | I |

## 4. IR plan structure

1. Purpose, scope, authority (board approval)
2. Definitions: event, incident, personal data breach, reportable incident
3. Severity matrix and reportability criteria
4. Roles, RACI, decision rights, deputies
5. Detection and reporting channels (internal hotline, SOC, vendor notices)
6. Response phases (section 1) with standard actions
7. Regulatory and contractual notification annex (see `regulatory-reporting-india.md`)
8. Communications protocol (internal, external, out-of-band channel if email is compromised)
9. Evidence handling and chain of custody (see the `cyber-forensics-evidence` skill)
10. Third-party coordination (MSSP, cloud, vendors, insurer, external IR, counsel)
11. Recovery and business continuity linkage
12. Post-incident review and continual improvement
13. Training, testing (at least annual tabletop), plan maintenance
14. Annexes: contact lists (verify), templates, playbooks, the first-hour card

**First-hour card:** record T0 → open the incident log → classify → call the Incident Commander → isolate without powering off → preserve logs → protect backups → start the deadline tracker (CERT-In T0 + 6 h) → brief Legal/DPO.

## 5. Playbook skeleton (use for every scenario)

Each playbook covers: Triggers / indicators → Severity guide → 0–1 h → 1–6 h → 6–24 h → 24–72 h → Containment → Eradication → Recovery → Evidence → Notifications → Communications → Decision points → Exit criteria.

## 6. Ransomware

- **Triggers:** encrypted files or ransom notes; mass file renames; EDR alerts for encryption behaviour; backup deletion attempts; data-leak site claims.
- **0–1 h:** record T0; isolate affected segments (network isolation, not power-off); disable compromised accounts; suspend scheduled tasks and sync that could spread encryption to backups; take backups offline and protect them; notify the Incident Commander, Legal and DPO.
- **1–6 h:** scope affected hosts and identities; identify the strain from the ransom note (to look up public decryptors such as nomoreransom.org); preserve memory and disk from representative hosts; check for exfiltration indicators; **CERT-In report by T0 + 6 h**; sector regulator; notify the insurer.
- **6–24 h:** decide on the recovery strategy (clean rebuild versus restore); validate that backups are clean; reset credentials enterprise-wide, including privileged and service accounts; assess the personal data impact for the DPDP intimation.
- **24–72 h:** phased restoration of critical services within impact tolerance; DPDP 72 h report if personal data is involved; customer communications.
- **Decision points:** whether to involve law enforcement; **ransom payment.** Do not advise payment. Refer to counsel, law enforcement and sanctions screening (payment may breach sanctions or other laws and does not guarantee recovery or deletion).
- **Exit criteria:** threat actor access removed and verified; services restored; monitoring heightened for 30 days; review scheduled.

## 7. Business Email Compromise (BEC) / payment fraud

- **Triggers:** a changed beneficiary bank details request; an urgent payment request from an executive look-alike; inbox rules forwarding mail externally; an MFA fatigue report.
- **0–1 h:** **call the bank immediately** to recall or hold the transfer; report on 1930 / cybercrime.gov.in (speed matters for fund freezing); reset the account password; revoke sessions and tokens; remove malicious inbox rules; enforce MFA.
- **1–6 h:** review mailbox audit logs for access and data exposure; identify other recipients of fraudulent mail; warn counterparties out-of-band; assess CERT-In reportability (unauthorised access, phishing); preserve emails with full headers.
- **6–72 h:** police complaint / FIR with UTR numbers; personal data impact assessment (mailbox contents); vendor bank-detail verification process reinforced.
- **Exit criteria:** funds recovered or loss quantified; accounts secured; payment verification control (call-back on known numbers) in place.

## 8. Personal data breach

- **Triggers:** data found online; a vendor notice; misdirected email or file; an exposed storage bucket; lost device; a regulator or media enquiry.
- **0–1 h:** record T0; stop ongoing exposure (restrict access, take down where lawful); preserve evidence of what was exposed and to whom; notify the DPO.
- **1–6 h:** determine data categories, volume, Data Principals affected, and whether data was accessed or acquired; CERT-In report (data breach / data leak); DPDP initial intimation to the Board without delay.
- **6–72 h:** detailed Board report within 72 h; Data Principal intimations with safety measures (for example password reset, fraud watch); GDPR and other overlays if triggered; vendor accountability under contract.
- **Decision points:** the scope of notification; credit or fraud monitoring offer; takedown requests.
- **Exit criteria:** exposure closed; notices completed; root cause fixed; records updated.

## 9. Insider misuse

- **Triggers:** DLP alerts; unusual bulk downloads; access outside role; resignation followed by data movement; a whistle-blower report.
- **Principles:** involve HR and Legal early; keep a need-to-know circle; avoid tipping off; act proportionately and within employment law and policy; keep it consistent with the employee's privacy rights.
- **Actions:** preserve logs and device images lawfully (follow the policy on employer-owned devices); suspend access where justified; interview with HR present; assess CERT-In and DPDP reportability; consider a civil remedy (injunction; IT Act s.43 compensation; s.72A penalty, which is civil since the Jan Vishwas Act 2023) and/or a criminal complaint (IT Act s.66; BNS offences such as criminal breach of trust; verify sections).
- **Exit criteria:** access removed; data recovered or destroyed with undertaking; disciplinary outcome; controls improved.
