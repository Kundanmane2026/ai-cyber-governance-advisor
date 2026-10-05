# Chain of Custody and Forensic Readiness

## 1. Chain of custody form

```
CHAIN OF CUSTODY RECORD                                   Case / Matter No.: __________
Organisation / Agency: __________________                  Exhibit ID: __________
Legal authority for collection: [consent / policy cl. __ / warrant no. __ / BNSS s.__ notice no. __ / court order __]

A. EXHIBIT DESCRIPTION
Item type: [laptop / HDD / SSD / mobile / USB / cloud export / log export / other]
Make / model: __________   Serial no.: __________   IMEI(s): __________
Capacity: ______   Condition / damage: __________   Powered on at seizure? [Y/N]   Screen state: ______
Owner / user: __________   Location found: __________
Photographs taken: [Y/N] Ref: ______   Audio-video recording (BNSS s.105): [Y/N] Ref: ______

B. ACQUISITION
Acquired by (name, role, org): __________   Date/time (IST): __________ (UTC: ______)
Method: [physical image / logical / file-system / targeted export / live memory]
Write-blocker used: [Y/N, model ____]   Tool and version: __________
Source hash (SHA-256): ____________________   Image hash (SHA-256): ____________________
Verification hash matches: [Y/N]   Notes: __________

C. SEALING
Seal no.: ______   Sealed by: ______   Witnesses (name, signature): 1. ______ 2. ______
Panchnama / seizure memo ref: ______

D. TRANSFERS
| # | Date/time (IST) | Released by (name, sign) | Received by (name, sign) | Purpose | Seal intact? | Storage location |
|---|-----------------|--------------------------|--------------------------|---------|--------------|------------------|
| 1 |                 |                          |                          |         |              |                  |

E. FINAL DISPOSITION
[returned to owner / produced in court on ___ / retained / destroyed under order ___]   By: ______ Date: ______
```

## 2. Evidence register (multi-exhibit matters)

| Exhibit ID | Description | Source / custodian | Acquired (IST) | Method | SHA-256 | Seal no. | Current location | Analysed by | s.63 certificate ref | Status |
|---|---|---|---|---|---|---|---|---|---|---|

## 3. Labelling and sealing conventions

- Exhibit ID format: `[Matter]-[Location code]-[Seq]`, for example `ACME24-MUM-007`.
- Label every item and every container. Use tamper-evident bags or tape, sign across the seal, and photograph the sealed item.
- Store originals in a locked, access-logged evidence store; keep digital images on encrypted, access-controlled storage with hash verification on each access.
- Never write on the evidence itself; label the container.

## 4. Forensic readiness plan: structure

**Goal:** maximise the ability to gather credible digital evidence while minimising the cost of an investigation (ISO/IEC 27043 readiness processes; ISO/IEC 30121 governance).

1. **Purpose and scope:** the business units, systems and jurisdictions covered.
2. **Business scenarios requiring evidence:**

   | Scenario | Likely forum | Key evidence | Sources | Retention needed | Owner |
   |---|---|---|---|---|---|
   | Ransomware / intrusion | CERT-In, police, insurer | Initial access, lateral movement, exfiltration | EDR, firewall, VPN, AD, cloud audit | ≥ 180 days in India (CERT-In) | CISO |
   | Insider data theft | Disciplinary, civil injunction, police | USB/cloud uploads, email forwarding, access logs | DLP, M365/Google audit, endpoint artefacts | ≥ 1 year | CISO + HR |
   | Financial fraud / BEC | Police, bank, civil recovery | Mailbox audit, payment system logs | Email, ERP, banking portal | ≥ 3 years | CFO |
   | Harassment / POSH | Internal Committee, police | Chats, emails | Collaboration platforms | Per policy | HR |
   | Regulatory inquiry | RBI/SEBI/IRDAI/DPDP Board | Access logs, consent records, breach records | Apps, consent manager logs | Per regulation | Compliance / DPO |

3. **Evidence sources and collection capability:** a log source inventory; centralised logging; NTP sync; immutability of logs; export procedures.
4. **Legal and policy foundations:** an acceptable use policy and employee notices covering monitoring and device collection; BYOD terms; legal hold procedure; DPDP-compliant notices (legitimate use for employment); privilege protocol (engage external forensics through counsel where appropriate).
5. **People:** a trained first responder (DEFR) per site; an external DES/lab on retainer; escalation contacts; competence records.
6. **Tools and storage:** validated acquisition tools; write-blockers; Faraday bags; secure evidence storage; licences and validation records (ISO/IEC 27041).
7. **Procedures:** first-response SOP; chain of custody; s.63 certificate procedure and signatories; police notice handling; cloud provider preservation requests.
8. **Integration:** IR plan (`incident-response`), BCP, risk register.
9. **Testing and review:** an annual exercise including a mock evidence production; post-incident lessons.
10. **Gap list and roadmap:** item, gap, action, cost/effort, owner, due date.

## 5. First-responder SOP card

1. Secure the scene; stop others touching devices.
2. Note the time (IST); photograph the devices and screens.
3. **Do not** switch on devices that are off; **do not** power off running systems without specialist advice.
4. Mobile: isolate from networks using the documented method; keep it charged.
5. Record everything: who was present, the device state, the actions taken.
6. Call the designated DES / external lab; start the chain-of-custody form.
7. Preserve the logs and cloud data (trigger legal hold; extend retention).
