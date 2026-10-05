# Indian Electronic Evidence Law

**Verify before reliance.** BSA 2023 and BNSS 2023 came into force on 01.07.2024. Section numbers below reflect the enacted text as understood when drafted. Check the bare acts on indiacode.nic.in, the BSA Schedule (certificate format), and the latest Supreme Court and High Court rulings on s.63. Record the date checked.

## 1. Which law applies?

- **Proceedings and evidence after 01.07.2024:** generally BSA and BNSS.
- **Pending matters and investigations started before 01.07.2024:** check the repeal and savings provisions (BNSS s.531; BSA s.170) and current judicial interpretation. Courts have taken different views on pending cases, so verify.
- Case law under IEA s.65B is widely Assessed to apply by analogy to BSA s.63, because the structure is similar. Confirm that courts have adopted this.

## 2. Key BSA 2023 provisions (verify)

| BSA 2023 | Subject | IEA 1872 equivalent |
|---|---|---|
| s.2(1)(d) | "Document" includes electronic and digital records | s.3 |
| s.57 | Primary evidence. Explanations treat electronic records stored simultaneously or in sequence, and records from proper custody, as primary evidence | s.62 (expanded) |
| s.61 | Electronic or digital records are not to be denied admissibility merely on that ground; same legal effect as other documents, subject to s.63 | New |
| s.62 | Contents of electronic records proved per s.63 | s.65A |
| **s.63** | Admissibility of electronic records; conditions; **certificate** | s.65B |
| s.39(2) | Opinion of the Examiner of Electronic Evidence (IT Act s.79A) is a relevant fact | s.45A |

## 3. BSA s.63: structure

- **s.63(1):** information in an electronic record that is printed, stored, recorded or copied in optical or magnetic media or semiconductor memory produced by a computer or communication device ("computer output") is deemed a document and admissible without production of the original, if the conditions are met.
- **s.63(2):** the conditions. The computer or device was regularly used to create, store or process information for activities regularly carried on by a person with lawful control; information of the relevant kind was regularly fed in during the ordinary course of those activities; the computer or device was operating properly throughout the material part of the period, or any malfunction did not affect the record or its accuracy; and the information reproduced is derived from information fed in during ordinary course.
- **s.63(3):** a combination of computers or devices is treated as one.
- **s.63(4):** a certificate, in the form specified in the **Schedule**, must accompany the electronic record each time it is submitted for admission. It identifies the record and how it was produced, gives device particulars, deals with the s.63(2) conditions, and is signed by **the person in charge of the computer/communication device or management of the relevant activities, and an expert**. This expert requirement is new compared with s.65B.
- **s.63(5):** information is taken to be supplied to a device if supplied in any appropriate form, directly or through equipment.

### Key differences from IEA s.65B

| Point | IEA s.65B | BSA s.63 |
|---|---|---|
| Devices | "Computer" | "Computer or communication device" (expressly includes smartphones) |
| Certificate signatories | Person occupying a responsible official position | Person in charge **and** an expert (Schedule Part A and Part B) |
| Format | No prescribed form | Prescribed Schedule format |
| Hash values | Not mentioned | Schedule format calls for hash value(s) and algorithm (verify) |
| Timing | "When" submitted, as interpreted in Khotkar | "Each time" submitted for admission |

## 4. Certificate under BSA s.63(4): working template

*Adapt this to the official Schedule format, which prevails over this template.*

```
CERTIFICATE UNDER SECTION 63(4)(c) OF THE BHARATIYA SAKSHYA ADHINIYAM, 2023

PART A  (to be filled by the party / person in charge)
I, [name], son/daughter of [ ], aged [ ], [designation] at [organisation], residing at [ ],
do hereby solemnly affirm and state:

1. I produce the electronic record / output of the digital record taken from:
   Device / system: [computer / communication device / server / cloud service]
   Make & model: [ ]   Serial no.: [ ]   IMEI / identifier: [ ]   Other: [ ]
2. The device/system was under the lawful control of [ ] and was regularly used to [create /
   store / process] information for the purpose of [activity] regularly carried on.
3. Information of the kind contained in the record was regularly fed into the device in the
   ordinary course of those activities.
4. Throughout the material part of the period the device was operating properly / any
   malfunction did not affect the electronic record or the accuracy of its contents.
5. The electronic record is a true reproduction of the original, as follows:
   Description of record: [ ]   Date/time range: [ ]
   Hash value(s): [ ]   Algorithm: [SHA-256]
6. I am in charge of / responsible for the management of the relevant activities.

Signature: ______  Name: ______  Designation: ______  Date: ______  Place: ______

PART B  (to be filled by the expert)
I, [name], [qualification], [designation/organisation], state that I have examined the
electronic record described in Part A, produced from [device], and:
1. The record was obtained by [method: imaging / logical extraction / export], using [tool, version].
2. Hash value(s) computed: [ ]  Algorithm: [SHA-256]  — matches Part A: [Yes/No]
3. [Any observations on integrity]

Signature: ______  Name: ______  Date: ______  Place: ______
```

**Practice notes (Assessed):**
- Prepare the certificate contemporaneously with the export, and record the hashes at the same time.
- Use one certificate per record set, and describe each file clearly (an annexed list with hashes).
- The signatory should have actual knowledge of the system; avoid signatures given "for formality".
- For WhatsApp or email evidence: identify the device, account, export method and hash. Be ready to prove authorship and integrity separately (for example by metadata and witness testimony).
- CCTV: identify the DVR/NVR, time offset, export method, and hash; preserve the original DVR where possible.

## 5. Leading case law (decided under IEA; Assessed relevance to BSA s.63)

| Case | Citation | Holding |
|---|---|---|
| State (NCT of Delhi) v. Navjot Sandhu (Parliament attack) | (2005) 11 SCC 600 | Secondary electronic evidence could be proved under s.63/65 even without a s.65B certificate. **Overruled on this point by Anvar.** |
| **Anvar P.V. v. P.K. Basheer** | (2014) 10 SCC 473 (3-judge bench) | s.65A/65B form a complete code; a **s.65B(4) certificate is mandatory** for secondary electronic evidence; without it the evidence is inadmissible. Where the original is produced (primary evidence under s.62), no certificate is needed |
| Shafhi Mohammad v. State of Himachal Pradesh | (2018) 2 SCC 801 (2-judge bench) | Certificate requirement procedural; may be relaxed where the party is not in possession of the device. **Overruled by Khotkar.** |
| State of Karnataka v. M.R. Hiremath | (2019) 7 SCC 515 | Non-production of the certificate with the charge-sheet is a curable defect |
| **Arjun Panditrao Khotkar v. Kailash Kushanrao Gorantyal** | (2020) 7 SCC 1 (3-judge bench) | Affirmed Anvar: the certificate is a **condition precedent** for secondary electronic evidence; no certificate is needed only when the original device is produced and its owner steps into the witness box. The certificate may be produced at a later stage if the trial is not prejudiced. If the person refuses, the court may direct production. Call-record retention guidance given to service providers. Overruled Shafhi Mohammad and clarified the "unless the original is produced" reading of Anvar |

Run a search for post-2024 rulings applying BSA s.63, especially on the expert signatory requirement and the Schedule format, before advising.

## 6. BNSS 2023: search, seizure and production (verify sections)

| BNSS 2023 | Subject | CrPC 1973 equivalent |
|---|---|---|
| s.94 | Summons to produce a document or other thing, **expressly including electronic communication devices** likely to contain digital evidence | s.91 |
| s.105 | **Audio-video recording** of search and seizure (including the list of seized items and witness signatures), preferably by mobile phone, forwarded without delay to the Magistrate | New |
| s.176(3) | For offences punishable with 7 years or more, a forensic expert visits the crime scene to collect forensic evidence and the process is videographed | New |
| s.185 | Search by a police officer | s.165 |
| s.106 | Power of police to seize property | s.102 |
| s.173 | Information in cognizable cases (zero FIR, e-FIR) | s.154 |
| s.530 | Trials, inquiries and proceedings may be held in electronic mode | New |

**IT Act 2000:** s.79A (Central Government notifies Examiners of Electronic Evidence); s.80 (police officer not below Inspector rank may enter, search and arrest in public places for IT Act offences); s.69 / s.69B (interception, monitoring, decryption, and traffic data under the 2009 Rules).

## 7. Admissibility checklist

- [ ] Primary or secondary evidence identified
- [ ] Lawful authority for acquisition documented
- [ ] Hashes recorded at acquisition and verified
- [ ] Chain of custody complete with no gaps
- [ ] s.63 certificate in the Schedule format, both parts signed by the right people
- [ ] Certificate filed each time the record is submitted
- [ ] Tool and method validation documented
- [ ] Clock and timezone issues explained
- [ ] Privacy and privilege review done (DPDP, legal professional privilege under BSA s.132–134)
- [ ] Expert available for testimony; s.79A examiner opinion considered
