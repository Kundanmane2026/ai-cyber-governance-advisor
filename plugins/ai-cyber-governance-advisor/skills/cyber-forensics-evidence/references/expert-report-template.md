# Forensic / Expert Report Template

Write for the court. Keep **facts (Observed)** apart from **opinion (Assessed)**. State assumptions, limitations and alternative explanations. Never overstate.

## 1. Report structure

```
DIGITAL FORENSIC EXAMINATION REPORT
Matter: [title / case no. / court or forum]          Report no.: [ ]   Version: [ ]   Date: [ ]
Prepared by: [name, qualifications]                  Instructed by: [party / counsel / agency]
Classification: [Confidential / Privileged & Confidential – prepared at the request of counsel]

1. Summary of findings (one page, plain language)
2. Examiner
   2.1 Qualifications, certifications, experience, prior testimony
   2.2 Independence and conflict declaration
3. Instructions and scope
   3.1 Questions to be answered (verbatim from instructions)
   3.2 Legal authority for examination (warrant / order / consent / policy)
   3.3 Out of scope
4. Materials received
   | Exhibit | Description | Received from | Date/time | Seal intact? | SHA-256 on receipt | Matches acquisition hash? |
5. Methodology
   5.1 Standards followed (ISO/IEC 27037, 27041, 27042, 27043; NIST SP 800-86)
   5.2 Tools and versions; validation reference
   5.3 Procedures (imaging, verification, analysis steps), at a reproducible level of detail
   5.4 Time normalisation (timezone, clock offsets found)
6. Findings (facts)
   | # | Finding | Artefact / source | Exhibit & location | Timestamp (IST / UTC) | Label: Observed |
7. Analysis and opinion
   For each question in 3.1:
   - Relevant findings (cross-ref section 6)
   - Hypotheses considered (including alternatives)
   - Reasoning
   - Opinion, using the scale in section 2 below   (Label: Assessed)
8. Limitations and assumptions
   - Data not available / not examined; encryption; deleted data; retention gaps
   - Assumptions (Label: Assumed) and their effect on the opinion
9. Conclusion
10. Declaration
11. Annexes: chain of custody records; hash listings; timeline; s.63 certificate(s);
    glossary; tool validation records; photographs
```

## 2. Opinion language scale

Use consistent wording and explain the scale in the report.

| Level | Wording | Meaning |
|---|---|---|
| 5 | "The findings **establish** that…" | Direct artefacts; no reasonable alternative found |
| 4 | "The findings **strongly support**…" | Multiple independent artefacts consistent; alternatives considered and found unlikely |
| 3 | "The findings **support**…" | Artefacts consistent; some alternatives cannot be excluded |
| 2 | "The findings are **consistent with**…, but also with…" | Equally explained by alternatives |
| 1 | "The findings **do not allow a conclusion** on…" | Insufficient data |

Avoid "proves", "definitely", "beyond doubt". Attribution of a human actor to a device action needs separate evidence (an account login alone does not establish who was at the keyboard).

## 3. Declaration (adapt to forum requirements)

> I confirm that the facts stated in this report are within my knowledge or derived from the materials identified, and the opinions expressed are my honest professional opinions. I understand my duty is to assist the [court / tribunal] on matters within my expertise, and this duty overrides any obligation to the party instructing me. I have identified all matters I regard as relevant, including those that may detract from my opinion. I have no conflict of interest [save as disclosed].
>
> Signature: ______  Name: ______  Date: ______  Place: ______

## 4. Cross-examination readiness checklist

- [ ] Can you show the chain of custody for every exhibit without gaps?
- [ ] Were hashes verified at every stage, and are they recorded in the report?
- [ ] Is the tool validated, and do you know its known limitations and error rates?
- [ ] Did you consider and document alternative explanations (malware, remote access, a shared account, clock error)?
- [ ] Are timezone conversions explicit and correct?
- [ ] Is every opinion traceable to Observed findings?
- [ ] Did you stay within your instructions and legal authority?
- [ ] Is the s.63 certificate consistent with your report (devices, hashes, dates)?
- [ ] Can a peer reproduce your key findings from your notes?
- [ ] Are your qualifications and independence disclosed accurately?
- [ ] Does the plain-language summary match the detailed findings, with no overstatement?

## 5. Glossary starter (include in annexes)

| Term | Plain meaning |
|---|---|
| Hash value | A digital fingerprint of data; any change gives a different value |
| Forensic image | A complete bit-for-bit copy of a storage device |
| Write-blocker | A device that prevents any change to the source during copying |
| Metadata | Data about data, such as when a file was created or last modified |
| Unallocated space | Storage areas not currently assigned to files; may hold deleted data |
| Artefact | A trace left by system or user activity |
| Chain of custody | The documented record of who handled the evidence, when, and why |
| UTC / IST | Coordinated Universal Time / Indian Standard Time (UTC + 5:30) |
