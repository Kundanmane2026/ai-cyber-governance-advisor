# AI & Cyber Governance Advisor

A Claude Code plugin of advisory skills for cyber risk, incident response, digital forensics and evidence, cyber law and DPDP compliance, responsible AI, AI governance, strategic advisory, and professional confidentiality and ethics.

**India-first, globally aware.** Indian law and regulators (IT Act 2000, DPDP Act 2023 and Rules 2025, CERT-In, RBI, SEBI, IRDAI, BSA 2023, BNSS 2023, MeitY) lead. Global frameworks (ISO/IEC, NIST, GDPR, NIS2, DORA, EU AI Act) sit alongside them as an overlay.

## Shared conventions

Every skill follows the same rules:

- **Evidence labels.** Each finding is tagged **Observed** (seen in material the user supplied), **Assessed** (the advisor's professional judgement drawn from what was observed), or **Assumed** (a gap filled by assumption that the user must confirm).
- **Current law check.** Before relying on a statute, rule, direction, circular or deadline, the model checks it is still current with a web search and says when it could not.
- **Defensive only.** No exploit code, attack tooling or offensive techniques. Technical content stays at the level of control, detection and governance.
- **Marathi output.** When Marathi output is requested, legal and technical terms stay in English (for example *Data Fiduciary*, *chain of custody*, *Consent Manager*).
- **Not legal advice.** Outputs support qualified professionals. They do not replace them.

## Skills

| # | Skill | Scope | Status |
|---|-------|-------|--------|
| 1 | `cyber-risk-advisory` | Cyber risk assessment, ISO 27001/27005, NIST CSF 2.0, risk register, third-party risk, Indian sectoral cyber regimes, board reporting templates | Done |
| 2 | `incident-response` | NIST SP 800-61r3, IR plan and playbooks, tabletop exercises, CERT-In 6-hour reporting, DPDP breach intimation, sectoral reporting, crisis communications | Done |
| 3 | `cyber-forensics-evidence` | ISO/IEC 27037/27041/27042/27043, chain of custody, forensic readiness, BSA 2023 s.63 certificate, BNSS 2023 search and seizure | Done |
| 4 | `cyber-law-dpdp-compliance` | IT Act 2000, IT Rules 2021, DPDP Act 2023 and Rules 2025, sectoral regimes, GDPR/NIS2/DORA overlay, policy pack, DPA clauses | Done |
| 5 | `responsible-ai-ethics` | Fairness, transparency, accountability, oversight, model cards, AI harms, ethics committee charter, UNESCO/OECD principles | Done |
| 6 | `ai-governance-risk` | ISO/IEC 42001, ISO/IEC 23894, NIST AI RMF, EU AI Act, MeitY guidelines, AI impact assessment, AI inventory, OWASP LLM Top 10 | Done |
| 7 | `strategic-advisory` | Board/CXO memos, executive briefings, proposals, delivery plans, KPI/KRI dashboards | Done |
| 8 | `confidentiality-ethics` | Confidentiality, conflicts, independence, NDA review, IT Act s.72A, Contract Act s.27, CCS (Conduct) Rules | Done |

## Layout

```
ai-cyber-governance-advisor/
├── .claude-plugin/plugin.json
├── README.md
└── skills/
    └── <skill-name>/
        ├── SKILL.md
        └── references/*.md
```

## Validate

```
claude plugin validate ./plugins/ai-cyber-governance-advisor
```
