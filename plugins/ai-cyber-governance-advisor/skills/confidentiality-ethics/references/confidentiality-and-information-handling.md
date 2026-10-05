# Confidentiality and Information Handling

**Verify before reliance.** The Jan Vishwas (Amendment of Provisions) Act 2023 converted IT Act s.72 and s.72A from offences into civil penalties with effect from 30.11.2023 (S.O. 4745(E), 31.10.2023). DPDP commencement phases, the status of IT Act s.43A (to be omitted on commencement of DPDP s.44) and section numbering under the BSA 2023 should be checked against indiacode.nic.in, meity.gov.in and egazette.gov.in. Record the date checked.

## 1. Legal sources of the duty of confidence (India)

| Source | What it does | Notes |
|---|---|---|
| Contract (engagement letter, NDA, MSA) | Primary source: defines confidential information, permitted use and remedies | Breach → damages (Contract Act s.73–74) and injunction (Specific Relief Act 1963) |
| Equity / common law of confidence | Protects information imparted in confidence even without a contract | Indian courts apply it to trade secrets and confidential know-how; India has no trade-secret statute (verify) |
| IT Act 2000 s.72 | Civil penalty (up to ₹5 lakh) on a person who, *under powers conferred by the Act*, accesses electronic material and discloses it without consent | Applies to persons exercising statutory powers (for example officials, adjudicators) |
| IT Act 2000 s.72A | Civil penalty on any person, including an intermediary, who while providing services under a lawful contract accesses personal information and discloses it, with intent or knowledge of wrongful loss or gain, without consent or in breach of contract | Directly relevant to consultants, auditors and service providers; penalty up to ₹25 lakh, adjudicated under s.46 (before 30.11.2023: up to 3 years and/or fine up to ₹5 lakh) |
| IT Act 2000 s.43A | Compensation for negligent failure of reasonable security over sensitive personal data | To be omitted when DPDP s.44(2) commences; check status |
| DPDP Act 2023 + Rules 2025 | Data Fiduciary must ensure processors act under a valid contract (s.8(2)), keep reasonable security safeguards (s.8(5)), intimate breaches (s.8(6)), erase data (s.8(7)) | The advisor is usually a Data Processor; the penalty sits with the Fiduciary, but contracts pass liability down |
| BSA 2023 ss.132–134 (formerly IEA ss.126–129; verify numbering) | Professional communications between client and advocate are privileged | Privilege attaches to advocates, not to non-lawyer consultants; work done at counsel's direction for litigation may be protected, so structure forensic engagements through counsel where privilege matters |
| Official Secrets Act 1923; CCS (Conduct) Rules 1964 Rule 11 | Government information | See `professional-conduct-and-public-servants.md` |
| Professional codes (BCI, ICAI, ISACA, ISC2) | Duty of confidentiality as a conduct obligation | Disciplinary exposure |

**Global overlay:** GDPR Art. 28 (processor contract terms), Art. 32 (security), Art. 29 (processing only on instructions); UK and US law of confidence and trade secrets (US Defend Trade Secrets Act 2016) where the client or information is foreign.

## 2. Classification scheme (default)

| Level | Examples | Handling |
|---|---|---|
| Restricted | Forensic evidence, privileged legal advice, credentials, unredacted vulnerability details, board-confidential, personal data of children or financial or health data | Named individuals only; encrypted at rest and in transit; no personal devices; no AI or third-party tools; logged access |
| Confidential | Client policies, assessment findings, contracts, personal data generally | Engagement team only; approved repositories; encrypted transfer |
| Internal | Templates, methodology, non-client project plans | Firm staff |
| Public | Published material | No restriction |

If the client has its own scheme, adopt it and map to it.

## 3. Engagement data-handling plan (annex to engagement letter)

| Item | Entry |
|---|---|
| Information required (by category) | |
| Personal data involved? Categories, volume | |
| Advisor's role under DPDP / GDPR | Data Processor (usual) / Fiduciary / none |
| Preferred access mode | On-site / client VDI / client-hosted repository / copies |
| Storage location and jurisdiction | |
| Encryption (at rest / in transit) | |
| Access list (named) | |
| Sharing channels permitted | |
| Use of AI or other third-party tools | Prohibited / permitted with written client consent for [tool], inputs not used for training, retention [x] days, location [y] |
| Subcontractors and flow-down | |
| Retention period | |
| Return / deletion method and certificate | |
| Breach notification to client | Within [x] hours of discovery |
| Client contact for data questions | |

## 4. Rules for AI and cloud tools

1. Default: **no client confidential or personal data in public generative AI tools.**
2. Permitted only with written client consent, an enterprise agreement that excludes training on inputs, defined retention and location, access controls and logging.
3. Prefer redaction, pseudonymisation or synthetic examples; check the redaction does not leave identifying context.
4. Record the tool, the data class and the consent in the engagement file.
5. Treat AI outputs as drafts needing professional review; never cite unverified authorities generated by a tool.

## 5. Day-to-day controls

- Need-to-know access; remove access at roll-off.
- Clean desk and screen; no client discussions in public places or on unsecured calls.
- Verify recipient addresses before sending; use the client's secure portal for Restricted material; disable autocomplete for external domains where possible.
- Label documents with classification and client name; watermark drafts.
- Separate repositories per client; no cross-client folders.
- Device encryption, MFA, and remote wipe on all devices holding client data.
- Do not use client material as examples in proposals, training or publications without written clearance.

## 6. Return and deletion certificate (template)

> We confirm that on [date] all information received from [Client] for the engagement [name/reference], including copies, extracts and derived working papers containing client confidential information, has been [returned / securely deleted] from all systems and media under our control, except: [items retained under legal or professional obligation, with reason, location and retention period]. Backups will be overwritten by [date] in the normal cycle and remain protected until then.
>
> Signed: [Engagement lead], [Firm], [date]
