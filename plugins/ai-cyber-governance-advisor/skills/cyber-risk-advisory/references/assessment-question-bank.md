# Assessment Question Bank

Ask in plain language. Accept a document in place of an answer. Record each response with its evidence label: **Observed** if supported by a document or demonstration, **Assessed** if it is your inference, and **Assumed** if the item is unanswered and you made an assumption.

## A. Rapid assessment (about 25 questions)

**Context**
1. What does the organisation do, which regulators supervise it, and roughly how many staff and customers does it have?
2. Which 3–5 business services would hurt most if unavailable for a day?
3. What sensitive data do you hold (customer personal data, financial, health, children's, employee, IP), roughly how many records, and where?
4. What is on-premises, in the cloud (which providers) and in SaaS?

**Govern**
5. Is there a board-approved information/cyber security policy? When was it last reviewed?
6. Who is the CISO (or equivalent), and who do they report to?
7. Does the board or a committee review cyber risk? How often?
8. Is there a cyber risk register? Who owns it?

**Identify and protect**
9. Do you have a current inventory of hardware, software and data stores?
10. Is MFA enforced for email, remote access (VPN/VDI), cloud consoles and privileged accounts?
11. How are admin/privileged accounts managed (PAM, reviews, break-glass)?
12. What is the patching SLA for critical vulnerabilities, and what share of systems meets it?
13. Is EDR/antivirus deployed on all endpoints and servers?
14. How often is security awareness training run? Do you run phishing simulations?
15. Are backups taken of critical systems, kept offline or immutable, and restore-tested? When was the last test?
16. Is data encrypted at rest and in transit for sensitive systems?

**Detect and respond**
17. Are logs centrally collected? Are they retained 180 days within India (CERT-In)? Are clocks synchronised to NTP?
18. Is there a SOC (in-house or managed)? What hours does it cover?
19. Is there a written incident response plan? When was it last tested (tabletop)?
20. Do you know the CERT-In 6-hour reporting duty, and who the designated Point of Contact is?
21. Any security incidents or near misses in the last 24 months?

**Third parties and recovery**
22. Which vendors have access to your systems or sensitive data? Are they assessed?
23. Do contracts require vendors to notify you of incidents quickly enough to meet your own deadlines?
24. Is there a BCP/DR plan with defined RTO/RPO? When was it last drilled?
25. Do you hold cyber insurance? What are its notification conditions?

## B. Deep-dive sets (use for Workflow 2)

**Governance and risk:** policy hierarchy; roles (RACI); risk methodology; appetite; exception process; metrics reported to the board; internal and IS audit coverage; regulatory observations open.

**Asset and data:** CMDB accuracy; shadow IT discovery; data classification scheme; personal data inventory and processing records (DPDP); data retention and erasure.

**Identity and access:** joiner-mover-leaver process; access recertification frequency; SSO coverage; MFA type (phishing-resistant?); service accounts; PAM vaulting and session recording.

**Infrastructure and cloud:** secure configuration baselines (CIS Benchmarks); network segmentation; internet exposure management; cloud security posture management; key management; container/Kubernetes governance.

**Application security:** SDLC security gates; code review / SAST / DAST / SCA; secrets management; API security; third-party libraries; pre-release VAPT.

**Monitoring and incident response:** log source coverage; use-case library; alert triage SLAs; threat intelligence feeds (CERT-In advisories, CSIRT-Fin); IR roles; evidence preservation; regulatory reporting playbooks.

**Resilience:** business impact analysis; impact tolerances; DR architecture; immutable backups; ransomware recovery runbook; crisis communications.

**People:** training coverage by role; privileged user vetting; insider risk programme; disciplinary linkage.

**Physical:** data centre controls; clear desk; media disposal.

## C. Vendor questionnaire (Tier 1 / Tier 2)

1. Legal entity, locations of processing and support, sub-processors (with locations).
2. Certifications: ISO/IEC 27001 (scope and Statement of Applicability), ISO/IEC 27701, SOC 2 Type II (period and exceptions), PCI DSS if relevant. Request copies.
3. Data handled: categories, volume, whether stored or only accessed; data localisation compliance where required (RBI payment data, sector rules).
4. Access model: how vendor staff access client systems; MFA; PAM; logging; IP allow-listing.
5. Encryption at rest and in transit; key ownership (BYOK/HYOK options).
6. Vulnerability management: patch SLAs; last independent pen-test date and summary of findings.
7. Incident management: notification commitment to clients (hours) that allows the client to meet CERT-In's 6 hours and the DPDP/sector timelines; history of incidents in 36 months.
8. Logging: retention period and location; whether logs are available to the client on request (CERT-In and forensic needs).
9. BCP/DR: RTO/RPO for the contracted service; last test date and result.
10. Personnel: background verification; confidentiality undertakings; training.
11. Secure development (for software/SaaS vendors): SDLC, SBOM availability, secrets handling.
12. AI use: whether client data is used to train models; opt-out; AI sub-processors.
13. Exit: data return format, deletion certificate, transition support.
14. Insurance: cyber and professional indemnity cover.
15. Contract: right to audit, regulator access (required by RBI/SEBI/IRDAI outsourcing rules), liability caps, governing law and jurisdiction.

## D. Contract security schedule checkpoints

- Security standards the vendor must keep (named framework or certification).
- Breach notification: **within [2–4] hours** of detection, with an initial facts list, so the client can meet CERT-In's 6 hours.
- Cooperation with forensics and law enforcement; log preservation.
- Data Processor obligations under the DPDP Act: process only on instructions, security safeguards, erasure on termination, sub-processor approval.
- Audit and inspection rights for the client and its regulator.
- Data localisation and cross-border transfer restrictions.
- Subcontracting controls.
- Termination and exit assistance; data return and deletion.
- Indemnity and liability carve-outs for data breach.
