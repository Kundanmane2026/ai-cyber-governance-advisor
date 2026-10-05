# Templates: AI Inventory, AI Impact Assessment, AI Policy, Vendor AI Terms

## 1. AI inventory template

| Field | Description |
|---|---|
| ID | AI-[BU]-[seq] |
| System name / version | |
| Business owner / technical owner | Named roles |
| Purpose and use case | What it does; decisions supported or made |
| Autonomy | Assistive / decision support (human decides) / automated decision with human review / fully automated / agentic (takes actions) |
| Users | Internal staff, customers, public |
| Affected people | Including non-users; vulnerable groups; children |
| Model type | Predictive ML / rules + ML / generative (text, image, audio, code) / agentic |
| Source | In-house / fine-tuned third-party model / third-party API / SaaS feature / open-source |
| Vendor(s) and model provider(s) | Including underlying foundation model |
| Data | Training / fine-tuning / retrieval / inference inputs; personal data? sensitive? children's? lawful ground (DPDP) |
| Data location and transfers | Where processed and stored |
| Deployment geography / output use | India / EU / US / other (drives EU AI Act scope) |
| EU AI Act role and tier | Provider / deployer / …; prohibited / high-risk (Annex I / III item) / Art. 50 / minimal / GPAI |
| India obligations | DPDP; IT Rules; sector (RBI FREE-AI, SEBI, IRDAI) |
| Internal risk tier | Low / Medium / High / Unacceptable (aligned to the ethics escalation matrix) |
| Assessments done | AIIA / FRIA / DPIA / fairness evaluation / security review (dates) |
| Documentation | Model card, system card, user notice (links) |
| Human oversight | Model and responsible role |
| Monitoring | Metrics, frequency, owner |
| Status | Idea / pilot / production / retired |
| Last review / next review | Dates |
| Label | Observed / Assessed / Assumed per row |

**Shadow-AI discovery checklist:** SSO and CASB logs for GenAI domains; expense claims for AI subscriptions; browser extension inventory; procurement "AI features" in existing SaaS; developer API keys for model providers; a staff survey with an amnesty message.

## 2. AI impact assessment (combined ISO/IEC 42005 / EU FRIA / DPIA)

```
AI IMPACT ASSESSMENT — [System name, version]   Ref: AIIA-[ ]   Owner: [ ]   Date: [ ]   Review by: [ ]
Assessment type(s) covered: [ ] ISO/IEC 42005 AIIA  [ ] EU AI Act Art. 27 FRIA  [ ] DPDP/GDPR DPIA

1. System description
   Purpose; intended use and out-of-scope use; autonomy; components (models, data, tools); vendor(s);
   lifecycle stage; deployment context, geography, period and frequency of use (FRIA Art. 27(1)(a)-(b))
2. Stakeholders
   Users; affected persons and groups (categories likely affected — FRIA Art. 27(1)(c)); vulnerable groups;
   consultation done (with whom, outcome)
3. Legal and policy context
   EU AI Act tier/role; DPDP lawful ground; sector rules; internal policies
4. Data
   Sources; personal/sensitive data; representativeness; quality; provenance and licences; retention
5. Benefits
   For organisation, users, affected persons, society
6. Impact analysis
   | Impact area | Description | Affected group | Likelihood (1-5) | Severity (1-5) | Reversibility | Label |
   Areas: fundamental rights (dignity, non-discrimination, privacy, expression, due process, children's
   rights); health and safety; fairness; privacy and data protection; economic; psychological;
   societal (information integrity, democratic processes); environmental
   (FRIA Art. 27(1)(d): specific risks of harm)
7. Mitigations
   Design; data; model; human oversight measures (FRIA Art. 27(1)(e)); transparency; contestability;
   governance and complaint mechanisms (FRIA Art. 27(1)(f)); security
8. Residual impact and acceptance
   Residual rating per area; acceptance by [role]; conditions
9. Monitoring
   Metrics; thresholds; review triggers (model change, new population, incidents)
10. Decision and sign-off
   Proceed / proceed with conditions / redesign / do not proceed
   Signed: AI owner · DPO · Risk · (Ethics Committee if High tier)
   FRIA: notify market surveillance authority of results where required (Art. 27(3))
```

## 3. AI policy outline

1. Purpose, scope and the AI definition
2. Principles (align with the organisation's values plus NITI Aayog / OECD / UNESCO)
3. Roles: Board oversight; AI owner; Responsible AI Lead; Ethics Committee; DPO; CISO
4. Risk-based approach: tiers and required assessments per tier
5. Prohibited uses (mirror EU AI Act Art. 5 as policy, plus organisation-specific ones)
6. Lifecycle requirements: design, data, development, validation, deployment, monitoring, retirement
7. Third-party and generative AI tools: approval, permitted data, account controls
8. Staff use of GenAI: approved tools; no confidential or personal data in unapproved tools; output verification; disclosure; IP
9. Transparency and documentation requirements
10. Human oversight and contestability
11. Security (link to the OWASP LLM controls)
12. Incidents and complaints
13. Training and AI literacy (EU AI Act Art. 4)
14. Inventory and records
15. Compliance monitoring, audit, exceptions, review cycle

## 4. Vendor AI terms review checklist

| # | Topic | What to look for | Acceptable position (typical) |
|---|---|---|---|
| 1 | Training on customer data | Whether inputs, outputs or files are used to train or improve models | No training on customer data by default; written opt-in only |
| 2 | Data retention | Prompt and output retention; abuse-monitoring retention | Defined short retention; zero-retention option for sensitive use |
| 3 | Confidentiality | Customer data treated as confidential | Yes, including outputs |
| 4 | Security | Certifications, encryption, access controls, pen-tests | ISO/IEC 27001 / SOC 2; security schedule (see `cyber-law-dpdp-compliance`) |
| 5 | Sub-processors | Underlying model providers, hosting, locations | Listed; change notice; objection right |
| 6 | Data location and transfers | Processing regions | Region pinning where required; DPDP s.16; sector localisation |
| 7 | DPA | DPDP / GDPR processor terms | Signed DPA with breach notice in hours |
| 8 | Output ownership | Who owns outputs | Customer owns outputs (to the extent IP exists) |
| 9 | IP indemnity | Third-party claims over outputs or training data | Vendor indemnity for outputs; check exclusions (modified outputs, disabled filters) |
| 10 | Accuracy / warranties | Disclaimers of accuracy | Accept reasonable disclaimers; require documentation of known limitations |
| 11 | Transparency | Model or system cards, evaluation results, change logs | Provided on request; notice of material model changes |
| 12 | Model changes / deprecation | Silent model swaps; end-of-life | Advance notice (for example 90 days); version pinning |
| 13 | EU AI Act allocation | Provider/deployer roles; instructions for use; Art. 25(4) cooperation; GPAI documentation downstream | Clear allocation; cooperation and information clause |
| 14 | Acceptable use policy | Restrictions that could affect your use case | Compatible with intended use |
| 15 | Incident notice | AI-specific incidents (harmful outputs, data exposure) | Prompt notice; cooperation |
| 16 | Audit and assurance | Audit rights; third-party reports | Reports annually; audit for regulated entities (RBI/SEBI/IRDAI) |
| 17 | Liability | Caps; carve-outs | Data breach and IP indemnity outside the general cap or with a super-cap |
| 18 | Exit | Data export; deletion certification; fine-tuned model weights | Export in usable format; deletion certificate; ownership of fine-tunes clarified |
| 19 | Human review | Vendor staff access to prompts | Restricted; disclosed; opt-out |
| 20 | Content provenance | Watermarking / C2PA for generated media | Available where relevant (MeitY advisories; EU Art. 50) |

**Issues table:**

| # | Clause ref | Current wording (Observed) | Issue | Grade (OK / Negotiate / Unacceptable) | Proposed wording | Fallback |
|---|---|---|---|---|---|---|
