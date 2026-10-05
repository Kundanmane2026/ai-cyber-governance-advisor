# AI Harms and the Ethics Committee

**Verify before reliance.** Deepfake rules, MeitY advisories and AI copyright litigation are changing fast. Search for the current position and record the date checked. This file is defensive: it covers no creation of deepfakes, no watermark removal, and no attack prompts.

## 1. Harm taxonomy

| Category | Description | Example | Who is harmed |
|---|---|---|---|
| Allocative | Unfair distribution of opportunities or resources | Loan, job or benefit denied | Applicants, especially marginalised groups |
| Quality-of-service | Works worse for some groups | Speech recognition fails for regional accents | Users of under-represented languages |
| Representational | Stereotyping, demeaning, erasure | Image generator depicts professions by caste or gender stereotype | Groups depicted; society |
| Privacy | Exposure, inference, surveillance | Model regurgitates personal data; profiling | Data Principals, non-users |
| Safety | Physical, psychological or financial harm | Wrong medical or legal advice; unsafe instructions | Users, third parties |
| Information integrity | Misinformation, hallucination, deepfakes | Fabricated case law; synthetic video of a politician | Users, public, democratic processes |
| Autonomy / manipulation | Dark patterns, persuasion, dependency | Companion chatbot fosters emotional dependence in teens | Vulnerable users |
| IP and economic | Unlicensed training; output infringement; displacement | Model reproduces copyrighted text; artists' styles imitated | Creators, rights-holders, workers |
| Security | Misuse, prompt injection, data leakage | Agent tricked into sending data externally (see `ai-governance-risk` OWASP LLM) | Organisation, users |
| Environmental | Energy and water footprint | Large training runs | Society |

**Rating:** Severity (1–5) × Likelihood (1–5), adjusted upward for **irreversibility**, **scale** and **vulnerable populations**.

## 2. Hallucination and factual error

- **High-stakes contexts:** legal (fake citations have led to court sanctions abroad, and Indian courts have flagged AI-generated fictitious citations, so verify recent instances), medical, financial, safety, journalism.
- **Controls:** retrieval-augmented generation with source citations shown to users; restrict the system to approved sources; abstain or express uncertainty when low confidence; verification steps by human experts; output disclaimers; domain evaluation sets; monitor the user-reported error rate.
- **Policy:** professionals remain responsible for AI-assisted work products. For example, advocates must verify every authority cited.

## 3. Deepfakes and synthetic media

**As a target (impersonation, fraud, defamation):**
- Prevention: call-back verification for payment instructions; code words for executives; staff awareness; monitor brand and executive likeness online.
- Response: preserve evidence (URLs, hashes, screenshots plus native downloads; see `cyber-forensics-evidence`); takedown requests to intermediaries under the IT Rules 2021 (24-hour removal for impersonation or intimate imagery on complaint; 36 hours on an order); Grievance Appellate Committee; police complaint / cybercrime.gov.in; civil injunction.
- **Indian legal levers (verify):** IT Act s.66C (identity theft), s.66D (cheating by personation), s.66E (privacy), s.67/67A (obscene / sexually explicit); BNS defamation (s.356), cheating (s.318–319), criminal intimidation; **personality and publicity rights** injunctions from the Delhi and Bombay High Courts (for example *Amitabh Bachchan* (Del HC 2022), *Anil Kapoor v. Simply Life India* (Del HC 2023), *Arijit Singh* (Bom HC 2024); verify citations); MeitY advisories to intermediaries on deepfakes and AI models (Nov–Dec 2023, Mar 2024); and IT Rules amendments on labelling synthetically generated information (proposed 2025, so verify whether notified).

**As a creator or platform:**
- Consent from people depicted; no synthetic intimate imagery; no impersonation of real persons without authorisation.
- **Label** synthetic content (visible label plus metadata/provenance, for example C2PA Content Credentials; watermarking).
- Usage policy prohibiting deceptive use; detection and takedown process; user reporting.
- EU AI Act Art. 50 transparency duties for deepfakes if EU-facing (see `ai-governance-risk`).

## 4. IP in training data and outputs

| Issue | Indian position (Assessed; verify) | Practice |
|---|---|---|
| Training on copyrighted works | Copyright Act 1957 s.14 (exclusive rights, including reproduction) and s.52 (fair dealing: closed list of purposes, narrower than US fair use). No specific text-and-data-mining exception. *ANI Media v. OpenAI* (Delhi HC, filed 2024) pending; verify. DPIIT committee examining AI and copyright (2025); verify | Document data provenance and licences; honour opt-outs (robots.txt, TDM reservations); prefer licensed or public-domain or own data; keep a record of the dataset composition |
| Outputs reproducing protected works | Infringement risk if substantially similar | Output filters for verbatim reproduction; similarity checks for high-risk outputs |
| Authorship of AI-generated works | s.2(d)(vi) "person who causes the work to be created" for computer-generated works; registration of AI-as-co-author was contested (RAGHAV painting, 2020–21); verify | Keep a record of human creative contribution |
| Vendor models | Indemnity scope varies | Negotiate IP indemnity; check exclusions and conditions |
| Personal data in training | DPDP applies to digital personal data; publicly available data made public by the Data Principal is excluded (s.3(c)(ii)), but scraped data may not all qualify | DPIA; minimise; filter; erasure handling |

**Foreign developments to check:** *NYT v. OpenAI/Microsoft* (US); the US Copyright Office AI reports; *Getty Images v. Stability AI* (UK High Court judgment 2025); the EU AI Act GPAI copyright policy and training-data summary duties; the Japanese and Singapore TDM exceptions.

## 5. Ethics committee charter (template)

```
[ORGANISATION] RESPONSIBLE AI / AI ETHICS COMMITTEE — CHARTER          Approved by: [Board/CEO]  Date: [ ]

1. Purpose
   To ensure AI systems developed, procured or deployed by [Org] are lawful, fair, transparent,
   accountable, safe and respectful of human rights, in line with [AI Policy], UNESCO, OECD and
   NITI Aayog principles.
2. Scope
   All AI systems meeting the AI definition in [AI Policy], incl. third-party and generative AI tools,
   across all business units and geographies.
3. Mandate and decision rights
   a. Review high-risk use cases (per escalation matrix) and issue: Approve / Approve with conditions /
      Require redesign / Reject.   Decisions are [binding / advisory to the CEO]; overruling requires
      [CEO + documented rationale reported to the Board Risk Committee].
   b. Approve and periodically review the AI ethics policy and standards.
   c. Review serious AI incidents and complaints.
   d. Commission audits and fairness evaluations.
4. Composition (min. [7])
   Chair: [senior, independent of product P&L]; Legal/Privacy (DPO); Information Security; Risk;
   Product/Engineering; Data Science; HR; Customer/user advocate; at least one external member
   (ethicist / academic / civil society). Strive for diversity of gender, region, language, disability,
   and lived experience relevant to the use cases.
5. Independence and conflicts
   Members declare conflicts per agenda item and recuse; the external member has no commercial ties.
6. Meetings and quorum
   [Monthly] and ad hoc for urgent items; quorum = [majority incl. chair + Legal + one external/independent].
7. Process
   Intake form → triage by Responsible AI Lead → review pack (use-case description, harms analysis,
   fairness evaluation, DPIA/AIIA, model/system card) → deliberation → decision with conditions,
   owners and review date → record.
8. Records and transparency
   Minutes and decisions kept [x years]; annual summary report to the Board; public transparency
   statement [optional].
9. Reporting line
   To the [Board Risk Management Committee] quarterly.
10. Review of charter
   Annually.
```

## 6. Escalation matrix

| Tier | Triggers (any) | Reviewer | Time limit |
|---|---|---|---|
| **Unacceptable / prohibited** | Social scoring; manipulative techniques exploiting vulnerabilities; untargeted scraping of facial images; emotion recognition at work or in education (mirrors EU AI Act Art. 5; adopt as policy); non-consensual synthetic intimate imagery | Do not build; report to the Committee | Immediate |
| **High** | Decisions on access to credit, employment, education, health, insurance, housing, public services; biometric identification; children as users; public-facing generative content at scale; use of sensitive data (health, financial, caste, religion); safety-critical functions; agentic systems with external actions | Ethics Committee | Decision within [15] working days |
| **Medium** | Internal decision support with human review; customer-service chatbots with escalation; personalisation | Responsible AI Lead + DPO | [5] working days |
| **Low** | Productivity tools on non-sensitive data; spell-check; code assistance with review | Self-assessment, logged in the AI inventory | — |
| **Incident** | Serious harm, complaint pattern, regulator or media enquiry | Chair + CISO/IR lead (see `incident-response`) | Within 24 h |

## 7. Review form (intake)

1. System name, owner, business unit, vendor (if any)
2. Purpose and decisions made or informed; degree of autonomy
3. Users and affected people (including vulnerable groups)
4. Data: sources, personal data categories, lawful ground (DPDP), children's data?
5. Model type (predictive / generative / agentic); in-house or third-party
6. Harms identified (table from section 1) with ratings and labels
7. Fairness evaluation summary
8. Transparency artefacts available (model card, datasheet, user notice)
9. Human oversight model and contestability route
10. Monitoring plan and incident process
11. Proposed tier and reviewer
12. Decision, conditions, review date (completed by the Committee)
