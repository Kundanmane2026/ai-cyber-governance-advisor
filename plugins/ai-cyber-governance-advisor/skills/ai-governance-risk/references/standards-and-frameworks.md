# AI Standards and Frameworks

**Verify before reliance.** Confirm the current editions and any amendments on iso.org and nist.gov. Do not reproduce copyrighted ISO text. The summaries below are paraphrased.

## 1. ISO/IEC 42001:2023: AI management system (AIMS)

A certifiable management system standard with the Harmonised Structure (the same clauses 4–10 as ISO/IEC 27001), so the two integrate easily.

### Clauses 4–10 checklist

| Clause | Requirement (paraphrased) | Evidence to look for |
|---|---|---|
| 4 Context | Internal and external issues; interested parties; the organisation's AI roles (provider, producer, customer, user, and so on); AIMS scope | Context analysis; scope statement; role determination |
| 5 Leadership | Top management commitment; **AI policy**; roles, responsibilities, authorities | Approved AI policy; RACI; board minutes |
| 6 Planning | Actions on risks and opportunities; **AI risk assessment**; **AI risk treatment** (with a Statement of Applicability against Annex A); **AI system impact assessment**; AI objectives | Risk methodology; risk register; SoA; impact assessments; objectives |
| 7 Support | Resources; competence; awareness; communication; documented information | Training records; competence matrix |
| 8 Operation | Operational planning and control; perform risk assessments, treatment and impact assessments at planned intervals and on change | Lifecycle procedures; change records |
| 9 Performance evaluation | Monitoring and measurement; internal audit; management review | KPIs; audit reports; review minutes |
| 10 Improvement | Continual improvement; nonconformity and corrective action | CAPA log |

### Annex A control objectives (themes; paraphrased)

| Annex A | Theme | Examples of controls |
|---|---|---|
| A.2 | Policies related to AI | AI policy; alignment with other policies; review |
| A.3 | Internal organisation | Roles and responsibilities; reporting of concerns |
| A.4 | Resources for AI systems | Documenting data, tooling, system and computing, and human resources |
| A.5 | Assessing impacts of AI systems | Impact assessment process; documentation; impacts on individuals, groups and society |
| A.6 | AI system lifecycle | Objectives for responsible development; design and development processes; requirements; verification and validation; deployment; operation and monitoring; technical documentation; event logs |
| A.7 | Data for AI systems | Data for development and enhancement; quality; provenance; preparation |
| A.8 | Information for interested parties | System documentation and information for users; external reporting; communication of incidents |
| A.9 | Use of AI systems | Processes for responsible use; objectives; intended use |
| A.10 | Third-party and customer relationships | Allocating responsibilities; suppliers; customers |

Annex B gives implementation guidance; Annex C covers potential AI-related objectives and risk sources; Annex D covers use across domains and sectors.

### Related standards
- **ISO/IEC 22989:2022:** AI concepts and terminology.
- **ISO/IEC 23053:2022:** framework for AI systems using machine learning.
- **ISO/IEC 23894:2023:** AI risk management guidance (below).
- **ISO/IEC 42005:2025:** AI system impact assessment (verify the publication status and content).
- **ISO/IEC 42006:** requirements for bodies auditing and certifying AIMS (verify status).
- **ISO/IEC TR 24027:** bias in AI systems; **ISO/IEC TR 24028:** trustworthiness; **ISO/IEC 25059:** quality model for AI systems.

## 2. ISO/IEC 23894:2023: AI risk management guidance

Applies ISO 31000:2018 to AI:
1. **Principles:** integrated, structured, customised, inclusive, dynamic, best available information, human and cultural factors, continual improvement, interpreted for AI.
2. **Framework:** leadership, integration, design, implementation, evaluation, improvement.
3. **Process:** scope, context and criteria → **risk assessment** (identification, analysis, evaluation) → **treatment** → monitoring and review → recording and reporting, all with communication and consultation.
4. **AI-specific risk sources** (Annex): lack of transparency, level of automation, ML-specific issues (data quality, drift), system hardware issues, lifecycle issues, technology readiness, complexity of the environment.
5. Annex: mapping of risk management to the AI system lifecycle.

## 3. NIST AI Risk Management Framework 1.0 (NIST AI 100-1, January 2023)

**Seven characteristics of trustworthy AI:**
1. Valid and reliable (the base)
2. Safe
3. Secure and resilient
4. Accountable and transparent (spans all the others)
5. Explainable and interpretable
6. Privacy-enhanced
7. Fair, with harmful bias managed

**Four core functions:**

| Function | Purpose | Example categories |
|---|---|---|
| **GOVERN** | Culture, policies, accountability | Policies and processes; accountability structures; workforce diversity; risk culture; stakeholder engagement; third-party risk |
| **MAP** | Establish context and identify risks | Context; categorisation; capabilities, goals, costs and benefits; third-party components; impacts on individuals and society |
| **MEASURE** | Analyse, assess, track | Methods and metrics; evaluation for trustworthy characteristics; tracking over time; feedback on efficacy |
| **MANAGE** | Prioritise and act | Treatment of mapped and measured risks; benefit maximisation; third-party risk; response and recovery, communication |

Companion resources: the AI RMF Playbook; crosswalks (including to ISO/IEC 42001 and the EU AI Act); profiles.

## 4. NIST AI 600-1: Generative AI Profile (July 2024)

**Twelve risks unique to or worsened by GenAI:**
1. CBRN information or capabilities
2. Confabulation (hallucination)
3. Dangerous, violent or hateful content
4. Data privacy
5. Environmental impacts
6. Harmful bias and homogenisation
7. Human–AI configuration (automation bias, over-reliance, anthropomorphism)
8. Information integrity (mis/disinformation, deepfakes)
9. Information security (lowered barriers to offensive cyber; attacks on GenAI such as prompt injection)
10. Intellectual property
11. Obscene, degrading and/or abusive content (including CSAM and NCII)
12. Value chain and component integration (third-party models and data)

It suggests actions mapped to the AI RMF subcategories (for example content provenance, pre-deployment testing, incident disclosure, governance of third-party models).

## 5. Crosswalk (indicative)

| Topic | ISO/IEC 42001 | ISO/IEC 23894 | NIST AI RMF | EU AI Act |
|---|---|---|---|---|
| Governance and policy | Cl. 5; A.2, A.3 | Framework | GOVERN | Art. 17 QMS (providers); Art. 4 AI literacy |
| Risk management | Cl. 6.1; Cl. 8 | Process | MAP, MEASURE, MANAGE | Art. 9 risk management system |
| Impact assessment | Cl. 6.1.4; A.5 | — | MAP 5 | Art. 27 FRIA (deployers) |
| Data governance | A.7 | Risk sources | MAP / MEASURE | Art. 10 |
| Documentation | A.6, A.8 | Recording | GOVERN / MAP | Art. 11, Annex IV; Art. 18 |
| Logging | A.6 (event logs) | — | MEASURE | Art. 12, Art. 19, Art. 26(6) |
| Transparency to users | A.8 | Communication | GOVERN / MANAGE | Art. 13, Art. 50 |
| Human oversight | A.9 | Human factors | GOVERN / MANAGE | Art. 14, Art. 26(2) |
| Accuracy, robustness, security | A.6 V&V | Risk sources | MEASURE | Art. 15 |
| Third parties | A.10 | — | GOVERN 6; MANAGE 3 | Art. 25 value chain |
| Monitoring and incidents | Cl. 9; A.6, A.8 | Monitoring | MANAGE 4 | Art. 72 post-market; Art. 73 serious incidents |
| Improvement | Cl. 10 | Improvement | GOVERN / MANAGE | QMS |
