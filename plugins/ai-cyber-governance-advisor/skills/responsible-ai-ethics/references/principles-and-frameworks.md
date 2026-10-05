# Principles and Frameworks

**Verify before reliance.** Search for the current text (unesco.org, oecd.ai, niti.gov.in, indiaai.gov.in, meity.gov.in) and record the date checked.

## 1. UNESCO Recommendation on the Ethics of AI (adopted November 2021, 193 Member States)

**Four values:** human rights and human dignity; living in peaceful, just and interconnected societies; ensuring diversity and inclusiveness; environment and ecosystem flourishing.

**Ten principles:**
1. Proportionality and do no harm
2. Safety and security
3. Right to privacy and data protection
4. Multi-stakeholder and adaptive governance and collaboration
5. Responsibility and accountability
6. Transparency and explainability
7. Human oversight and determination
8. Sustainability
9. Awareness and literacy
10. Fairness and non-discrimination

**Policy areas (11):** ethical impact assessment; ethical governance and stewardship; data policy; development and international cooperation; environment and ecosystems; gender; culture; education and research; communication and information; economy and labour; health and social well-being.

**Tools:** Readiness Assessment Methodology (RAM) for countries; Ethical Impact Assessment (EIA) for systems.

## 2. OECD Recommendation on AI (2019; revised May 2024)

**Five values-based principles:**
1. Inclusive growth, sustainable development and well-being
2. Respect for the rule of law, human rights and democratic values, **including fairness and privacy** (2024 wording)
3. Transparency and explainability
4. Robustness, security and safety (2024: mechanisms to override, repair or decommission systems causing undue harm)
5. Accountability (2024: risk management across the lifecycle, including with the supply chain)

**Five recommendations to governments:** invest in AI R&D; foster an inclusive AI-enabling ecosystem; enable an interoperable governance and policy environment; build human capacity and prepare for labour market transition; international cooperation.

The 2024 revision also updated the definition of an "AI system" (aligned with the EU AI Act) and addressed misinformation and information integrity. India adheres to the G20 AI Principles, which draw on the OECD principles.

## 3. NITI Aayog: Responsible AI for All (Part 1, Feb 2021; Part 2, Aug 2021)

**Seven principles:**
1. Safety and reliability
2. Equality
3. Inclusivity and non-discrimination
4. Privacy and security
5. Transparency
6. Accountability
7. Protection and reinforcement of positive human values

Also: the *Responsible AI for All: Facial Recognition Technology* discussion paper (2022), which applies the principles to FRT (for example DigiYatra).

## 4. India AI Governance Guidelines (MeitY / IndiaAI, 2025)

Use the `ai-governance-risk` skill for detail. Headline: a principles-based, light-touch approach that favours voluntary frameworks and the use of existing laws, with institutions to coordinate. **Verify the final text and its principle list ("sutras") before citing.**

## 5. Indian constitutional and legal anchors

| Anchor | Relevance |
|---|---|
| Art. 14 equality; Art. 15 non-discrimination (religion, race, caste, sex, place of birth); Art. 16 public employment | Fairness in state or state-instrumentality AI; discrimination standards |
| Art. 19(1)(a) speech | Content moderation, deepfake takedown proportionality |
| Art. 21 life and personal liberty; *Puttaswamy* (2017) privacy and proportionality | Surveillance, profiling, FRT, data minimisation |
| DPDP Act 2023 | Notice, consent, purpose limitation, children (no behavioural tracking or targeted ads), accuracy for decisions (s.8(3)) |
| RPwD Act 2016 | Accessibility, reasonable accommodation in AI interfaces |
| Consumer Protection Act 2019 + CCPA dark-patterns guidelines (2023) | Manipulative design in AI interfaces |
| IT Act / IT Rules 2021 | Deepfakes, intermediary duties |

## 6. Crosswalk of the core dimensions

| Dimension | UNESCO | OECD | NITI Aayog | ISO/IEC 42001 (Annex A themes; see `ai-governance-risk`) |
|---|---|---|---|---|
| Fairness | Fairness and non-discrimination | Rule of law, human rights (fairness) | Equality; inclusivity and non-discrimination | Data for AI; impact assessment |
| Transparency | Transparency and explainability | Transparency and explainability | Transparency | Information for interested parties |
| Accountability | Responsibility and accountability | Accountability | Accountability | Roles, policies, third-party relationships |
| Privacy | Right to privacy | Rule of law (privacy) | Privacy and security | Data for AI |
| Safety and robustness | Safety and security; do no harm | Robustness, security and safety | Safety and reliability | AI system lifecycle |
| Human oversight | Human oversight and determination | Robustness (override) | Positive human values | Use of AI systems |
| Societal / environment | Sustainability; awareness | Inclusive growth, well-being | Positive human values | Impact assessment |

## 7. Review questions by dimension (Workflow 1)

**Fairness**
- Who could receive worse outcomes or service quality? On which attributes (including caste, religion, region, language, gender, disability, age, income)?
- Are the training and evaluation data representative of the deployment population?
- What proxies for protected attributes exist (PIN code, surname, language, device type)?
- Which fairness metric fits the decision, and why?

**Transparency**
- Do users know they are interacting with AI or receiving AI-generated content?
- Can we explain the main factors behind an individual outcome in plain language?
- Are model, data and system documentation complete?

**Accountability**
- Who is the named owner? Who can stop the system?
- Is there an audit trail of decisions, versions and changes?
- Are vendor responsibilities defined in contract?

**Privacy**
- Lawful ground under DPDP for training and inference data? Purpose limitation?
- Can the model memorise or reveal personal data? Are there controls?
- Are children's data excluded from tracking and targeted advertising?

**Safety and robustness**
- What happens on out-of-distribution input, adversarial input or a failure? Is there a safe fallback?
- Has it been red-teamed (process, not attack content) and stress-tested?
- Is there monitoring for drift and incidents?

**Human oversight**
- Which oversight model applies and why?
- Can affected people contest outcomes and reach a human?
- Are reviewers trained against automation bias?

**Societal and environmental**
- Effects on jobs, information integrity, democratic processes, vulnerable communities?
- Compute and energy footprint proportional to the benefit?
