# AI Regulatory Landscape: EU AI Act and India

**Verify before reliance.** The EU AI Act implementation dates may be amended (a November 2025 "digital omnibus" proposal suggested delaying some high-risk obligations, so check whether it was adopted). Commission guidelines, harmonised standards and the GPAI Code of Practice keep evolving. Indian AI governance is guideline-led and changes quickly. Search for each item and record the date checked.

## Part A: EU AI Act (Regulation (EU) 2024/1689)

### A1. Scope (Art. 2)
Applies to:
- providers placing on the market or putting into service AI systems or GPAI models in the EU, wherever they are established;
- deployers established or located in the EU;
- providers and deployers in third countries **where the output produced by the AI system is used in the EU**;
- importers and distributors, product manufacturers, authorised representatives, and affected persons in the EU.

Exclusions include military, defence and national security; scientific R&D; personal non-professional use; and free and open-source models (except prohibited, high-risk, Art. 50 and GPAI-systemic cases).

**Indian relevance:** Indian IT and SaaS firms are often *providers* (they build systems placed on the EU market) or their outputs are used in the EU, so the Act can apply even with no EU establishment.

### A2. Risk tiers

| Tier | Provision | Examples | Consequence |
|---|---|---|---|
| **Prohibited** | Art. 5 | Subliminal, manipulative or deceptive techniques causing significant harm; exploiting vulnerabilities (age, disability, socio-economic situation); social scoring; predicting criminal offences solely from profiling; untargeted scraping of facial images for databases; emotion recognition in the workplace and education (except medical/safety); biometric categorisation to infer sensitive traits; real-time remote biometric identification in public spaces for law enforcement (narrow exceptions) | Banned |
| **High-risk** | Art. 6(1) + Annex I | Safety component of products under EU harmonisation legislation (machinery, toys, medical devices, vehicles, and so on) needing third-party conformity assessment | Full provider/deployer obligations |
| | Art. 6(2) + **Annex III** | (1) Biometrics; (2) critical infrastructure; (3) education and vocational training; (4) employment and worker management (recruitment, promotion, termination, task allocation, monitoring); (5) access to essential private and public services (public benefits, **creditworthiness / credit scoring**, **life and health insurance risk and pricing**, emergency dispatch); (6) law enforcement; (7) migration, asylum, border; (8) administration of justice and democratic processes | Full obligations, unless the Art. 6(3) derogation applies (no significant risk: narrow procedural task, improving a prior human activity, detecting patterns without replacing human assessment, preparatory task). Never available if the system profiles natural persons. The provider must document this and register |
| **Transparency** | Art. 50 | Chatbots (disclose AI interaction); synthetic audio/image/video/text (machine-readable marking); emotion recognition and biometric categorisation (inform people); **deepfakes** (disclose); AI-generated text published to inform the public on matters of public interest (disclose unless human-reviewed under editorial responsibility) | Disclosure duties |
| **Minimal** | — | Spam filters, games | Voluntary codes; Art. 4 AI literacy still applies |

### A3. Obligations by role (high-risk systems)

| Provider (Art. 16) | Deployer (Art. 26) |
|---|---|
| Risk management system (Art. 9) | Use in accordance with instructions |
| Data and data governance (Art. 10) | Assign human oversight to competent, trained persons |
| Technical documentation (Art. 11, Annex IV) | Ensure input data is relevant and representative (where under their control) |
| Record-keeping / automatic logs (Art. 12) | Monitor operation; inform the provider and authorities of risks and serious incidents |
| Transparency and instructions for use (Art. 13) | Keep logs ≥ 6 months (where under their control) |
| Human oversight design (Art. 14) | Inform workers' representatives before using at the workplace |
| Accuracy, robustness, cybersecurity (Art. 15) | Inform affected persons that they are subject to high-risk AI decisions (Annex III) |
| Quality management system (Art. 17) | **FRIA (Art. 27)**: public bodies, private entities providing public services, and deployers of Annex III 5(b) credit scoring and 5(c) life/health insurance |
| Documentation keeping (Art. 18); logs (Art. 19) | Right to explanation (Art. 86) for affected persons |
| Corrective actions; cooperation with authorities (Art. 20–21) | Registration (public-authority deployers, Art. 49) |
| Conformity assessment (Art. 43); EU declaration of conformity (Art. 47); CE marking (Art. 48) | |
| Registration in the EU database (Art. 49) | |
| Post-market monitoring (Art. 72); serious incident reporting (Art. 73) | |
| **Authorised representative in the EU** if established outside the EU (Art. 22) | |

**Art. 25 (value chain):** a distributor, importer, deployer or other third party becomes a **provider** if it puts its name or trademark on a high-risk system, makes a substantial modification, or modifies the intended purpose so the system becomes high-risk. Providers of components and tools must cooperate by written agreement.

**Importers (Art. 23) and distributors (Art. 24):** verify conformity, documentation and CE marking.

### A4. General-purpose AI models

| Duty | Article | Notes |
|---|---|---|
| Technical documentation for the AI Office and downstream providers | Art. 53(1)(a)–(b), Annex XI–XII | Open-source exemption, except for systemic risk |
| Copyright policy, including honouring text-and-data-mining opt-outs | Art. 53(1)(c) | |
| Public summary of training content (Commission template) | Art. 53(1)(d) | |
| Authorised representative (non-EU providers) | Art. 54 | |
| **Systemic risk** (presumed above 10^25 FLOPs of training compute, or by designation): model evaluation including adversarial testing, systemic risk assessment and mitigation, serious incident reporting, cybersecurity | Art. 51, 55 | |
| **GPAI Code of Practice** (published July 2025: transparency, copyright, safety and security chapters) | Art. 56 | Adherence demonstrates compliance; verify the signatories and status |

### A5. Timeline (from entry into force 01.08.2024; verify amendments)

| Date | What applies |
|---|---|
| 02.02.2025 | Chapters I–II: definitions, **AI literacy (Art. 4)**, **prohibited practices (Art. 5)** |
| 02.08.2025 | Notified bodies; **GPAI obligations**; governance (AI Office, Board); **penalties**; confidentiality |
| 02.08.2026 | Most remaining provisions, including **Annex III high-risk**, Art. 50 transparency, and enforcement (**check whether delayed by the digital omnibus**) |
| 02.08.2027 | **Art. 6(1) / Annex I** product-embedded high-risk; GPAI models placed on the market before 02.08.2025 must comply |

### A6. Penalties (Art. 99; the lower amount applies for SMEs and start-ups)

| Infringement | Maximum |
|---|---|
| Prohibited practices (Art. 5) | €35 million or 7% of worldwide annual turnover, whichever is higher |
| Most other obligations (operators, notified bodies, Art. 50) | €15 million or 3% |
| Supplying incorrect, incomplete or misleading information | €7.5 million or 1% |
| GPAI providers (Art. 101) | €15 million or 3% |

## Part B: India

| Instrument | Status | Key points (verify) |
|---|---|---|
| **India AI Governance Guidelines** (MeitY / IndiaAI, released November 2025) | Non-binding guidelines | A pro-innovation, principles-based approach that relies on existing laws (IT Act, DPDP, consumer, sectoral) rather than a new AI law for now. Principles ("sutras") reported as: trust as the foundation; people first; innovation over restraint; fairness and equity; accountability; understandable by design; safety, resilience and sustainability. Proposed institutions include an AI Governance Group, a Technology and Policy Expert Committee, and a role for the AI Safety Institute. Recommends voluntary frameworks, graded liability, techno-legal tools, and an India-specific risk classification and incident database. **Confirm the final text before citing** |
| **IndiaAI Mission** (Cabinet approval March 2024; outlay about ₹10,372 crore) | Programme | Pillars: compute capacity; innovation centre (foundation models); datasets platform (AIKosh); application development; FutureSkills; startup financing; **Safe and Trusted AI** |
| **IndiaAI Safety Institute** (announced January 2025) | Institution | Standards, risk research and tools; hub-and-spoke model |
| **MeitY advisories to intermediaries / platforms** (26.12.2023 on deepfakes; 01.03.2024 on AI models, revised 15.03.2024) | Advisory under IT Rules due diligence | Do not permit unlawful content via AI; label unreliable or under-tested models and inform users of possible unreliability; label or embed metadata in synthetic content to identify it; users informed of consequences of unlawful content. The 15.03.2024 revision removed the prior-permission requirement. **Verify the current advisories** |
| **IT Rules amendment on "synthetically generated information"** (draft October 2025) | Draft or notified (verify) | Proposed: a definition of synthetic content; mandatory visible labelling (with a proportion-of-display requirement in the draft) and metadata; SSMI duties to obtain user declarations and verify them |
| **IT Act 2000 / IT Rules 2021** | Statute / rules | Intermediary due diligence; takedown; s.66C/66D/66E/67 for misuse |
| **DPDP Act 2023 + Rules 2025** | Statute / rules (phased) | Personal data in training and inference; notice and consent; children (no behavioural monitoring); SDF duty of **algorithmic due diligence** (Rule 13) |
| **RBI FREE-AI Framework** (Framework for Responsible and Ethical Enablement of AI; committee report August 2025) | Report / recommendations to REs (verify the adoption status) | Board-approved AI policy, AI inventory, risk-based approach, model governance and lifecycle, consumer protection and disclosure, incident reporting, audits; seven "sutras" for financial-sector AI |
| **SEBI** | Circulars (2019 AI/ML reporting for intermediaries, MIIs and mutual funds); 2025 consultation on responsible AI/ML use (verify) | Reporting of AI/ML systems; accountability of REs for AI-based outcomes; proposed guidelines on governance, testing, disclosure, data security |
| **Other sectors** | Verify | ICMR ethical guidelines for AI in biomedical research and healthcare (2023); TRAI recommendations on AI (2023); CDSCO on software as a medical device |
| **NITI Aayog** | Strategy / papers | National Strategy for AI (2018); Responsible AI principles (2021); FRT paper (2022) |

## Part C: Other jurisdictions (scan as needed)

- **US:** no federal AI statute. Federal policy has shifted with executive orders since 2025 (verify current). State laws include the Colorado AI Act (effective date deferred, so verify), the NYC Local Law 144 (AEDT bias audits), and California AI transparency laws. Sectoral regulators (FTC, EEOC, CFPB) apply existing law.
- **UK:** a principles-based, regulator-led approach; the AI Security Institute.
- **China:** algorithm recommendation, deep synthesis and generative AI measures; labelling measures (2025).
- **Others:** Korea AI Basic Act (2025, effective 2026); Japan AI Promotion Act (2025); Singapore Model AI Governance Framework (including for GenAI) and AI Verify; Canada (AIDA lapsed; verify); Council of Europe Framework Convention on AI (2024).
- **International:** G7 Hiroshima Process Code of Conduct; OECD AI Principles; UNESCO Recommendation; UN resolutions; the Bletchley/Seoul/Paris summit declarations (India co-chaired the Paris AI Action Summit in February 2025 and hosts the AI Impact Summit in February 2026; verify).
