# Sitrep, Crisis Communications and Post-Incident Review

Have Legal and the DPO review every external text before release. Keep messaging consistent with the regulatory filings.

## 1. Incident situation report (sitrep)

```
INCIDENT SITREP #[n] | [Incident ID] | Severity: SEV-[1–4] | Classification: CONFIDENTIAL
Issued: [date, time IST]   Next update: [time IST]   Incident Commander: [name/role]

CLOCK: Noticed (T0) [IST] | CERT-In due [T0+6h] – [status] | DPDP 72h report due [IST] – [status]
       Sector regulator due [IST] – [status]

1. Summary (3 lines)
2. Known facts (each labelled Observed)
3. Working hypotheses (each labelled Assessed / Assumed, with the confidence level)
4. Impact: services | data (categories, approx. volume) | customers | financial
5. Actions completed since the last sitrep
6. Next actions (owner, due)
7. Decisions needed (by whom, by when)
8. Notifications made (recipient, time, reference)
9. Evidence preserved (item, custodian, chain-of-custody ref)
```

## 2. Holding statement (external, first hours)

> [Organisation] identified a cyber security incident on [date] affecting some of our systems. We acted immediately to contain it, engaged independent specialists, and informed the relevant authorities. [Critical services X remain available / are being restored.] Protecting our customers' information is our priority. We are investigating, and will update [customers/partners] directly if their information is affected. Updates: [URL / helpline].

Do not speculate on the cause, the attacker's identity, the data volume, or the timeline to recovery until confirmed. Do not say "no data was affected" unless that is established.

## 3. Data Principal breach intimation (DPDP Rules 2025 contents; verify)

**Subject:** Important: an incident involving your personal data at [Organisation]

1. **What happened:** a plain description of the breach, its nature and extent, and when and where it occurred (as far as known).
2. **What information was involved:** the categories relating to you.
3. **What this could mean for you:** likely consequences.
4. **What we have done:** mitigation measures taken and under way.
5. **What you can do:** specific safety steps (change your password, watch for phishing that uses your details, contact your bank, enable MFA).
6. **Contact:** name/role, email, phone of the person who can answer your questions.

Keep it concise and clear, and send it through the registered communication channel. Translate into the Data Principal's language where appropriate. Under the DPDP Act, notices should be available in English or any language in the Eighth Schedule of the Constitution.

## 4. Staff note (internal)

- What happened (brief); what staff must do (for example, do not use system X; report suspicious emails to [address]; do not discuss externally).
- Refer all media and customer questions to [Comms contact].
- Remind staff of confidentiality and the out-of-band communication channel.

## 5. Media Q&A (prepare; release only if asked)

| Likely question | Approved answer |
|---|---|
| Was customer data stolen? | "Our investigation is ongoing. If any customer's information is affected, we will contact them directly with guidance." |
| Did you pay a ransom? | "We are working with the authorities and specialists and do not comment on operational details of the response." (Legal approval required.) |
| Have you informed the regulators? | "Yes, we have informed the relevant authorities in line with our obligations." |
| When will services be back? | "[Service X] is available; we are restoring [Y] in phases and will update at [URL]." |

## 6. Release sequence (typical)

Regulators (CERT-In, sector) → Board → staff → affected Data Principals / key clients → stock exchanges (if material) → holding statement / website → media on request. Adjust for statutory timing and for market-sensitive information.

## 7. Post-incident review template

**Blameless.** Look for the causes in systems and processes, not individuals.

1. **Summary:** incident ID, dates, severity, scenario, one-paragraph narrative.
2. **Timeline:** detection → declaration → containment → notifications → recovery → closure (IST timestamps).
3. **Detection:** how it was detected, dwell time, missed signals.
4. **Root cause and contributing factors:** 5 Whys; control failures mapped to ISO/IEC 27001 Annex A / NIST CSF categories.
5. **Response effectiveness:**

   | Area | What worked | What did not | Evidence |
   |---|---|---|---|
   | Decision-making | | | |
   | Containment | | | |
   | Evidence preservation | | | |
   | Communications | | | |
   | Vendor coordination | | | |

6. **Notification performance:**

   | Regime | Deadline | Submitted | Met? | Notes |
   |---|---|---|---|---|

7. **Impact:** downtime by service, records affected, direct cost (response, recovery, legal, notification), indirect cost, regulatory outcome.
8. **Actions:**

   | # | Action | Type (people/process/technology) | Owner | Due | Priority | Risk register ref |
   |---|---|---|---|---|---|---|

9. **Updates required:** IR plan, playbooks, risk register, training, vendor contracts, BCP.
10. **Sign-off:** Incident Commander, CISO, DPO, Risk; then report to the Board/RMC.
