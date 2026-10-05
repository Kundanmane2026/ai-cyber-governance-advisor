# OWASP Top 10 for LLM Applications (2025): Defensive Guide

**Defensive only.** This file names risks and controls. It contains no payloads, jailbreak prompts, extraction or poisoning techniques. Verify the current list on genai.owasp.org. OWASP also publishes agentic AI threat and mitigation guidance; check for updates.

## 1. The Top 10 with controls

| ID | Risk | What can go wrong (plain terms) | Key defensive controls |
|---|---|---|---|
| **LLM01** | Prompt injection | Untrusted input (from the user or from retrieved documents, emails, web pages) changes the model's behaviour against the developer's intent | Treat all model inputs and retrieved content as untrusted; separate and mark untrusted content; least-privilege tools; **human approval for consequential actions**; output validation before use; restrict the model's ability to call tools based on untrusted content; monitoring and anomaly detection; governed adversarial testing |
| **LLM02** | Sensitive information disclosure | The model reveals personal data, secrets, proprietary data or other users' data | Data minimisation in training, fine-tuning and retrieval; access-controlled retrieval (enforce the user's permissions at query time); PII redaction; no secrets in prompts; output filtering; tenant isolation; DPDP-aligned retention; user notices |
| **LLM03** | Supply chain | Compromised or vulnerable models, datasets, plugins, libraries; licence issues | Vet model and dataset sources; verify integrity (signatures, hashes); SBOM / AI-BOM; pin versions; vendor assessments (see `cyber-risk-advisory` Workflow 4); licence review |
| **LLM04** | Data and model poisoning | Manipulated training, fine-tuning or retrieval data alters behaviour or plants hidden behaviours | Data provenance and validation; restricted write access to training and RAG corpora; anomaly detection on data; evaluation against held-out benchmarks after each update; versioning and rollback |
| **LLM05** | Improper output handling | Model output passed unchecked to browsers, shells, databases or APIs leads to downstream exploitation | Treat output as untrusted user input: encode or escape for context, parameterised queries, strict schemas, sandboxed execution, allow-lists; never directly execute model-generated code in privileged contexts |
| **LLM06** | Excessive agency | The agent has too many tools, too much permission or too much autonomy, causing damaging actions | Minimise tools and functions; scope permissions per user; read-only by default; **human-in-the-loop for high-impact actions**; rate and spend limits; complete action logging; kill switch |
| **LLM07** | System prompt leakage | System prompts reveal secrets, internal logic or controls | Never place credentials or security-critical logic in prompts; enforce controls outside the model; assume prompts may be disclosed |
| **LLM08** | Vector and embedding weaknesses | RAG stores leak across tenants or permission levels, are poisoned, or allow inversion of embeddings | Permission-aware retrieval; tenant partitioning; validate ingestion sources; encrypt the stores; monitor retrieval patterns |
| **LLM09** | Misinformation | Confident but false output (hallucination) relied on by users | Grounding with citations; abstain when uncertain; domain evaluation; human review for high-stakes use; user warnings (see `responsible-ai-ethics` Workflow 4) |
| **LLM10** | Unbounded consumption | Excessive use causes cost blow-out, denial of service, or model extraction through high-volume querying | Rate limiting and quotas; input size limits; timeouts; cost alerts; abuse monitoring; authenticated access |

## 2. Agentic AI: additional controls

- **Identity and authorisation:** each agent has its own identity, credentials scoped to the task, short-lived tokens, and no shared admin keys.
- **Tool governance:** a registry of approved tools; schema-validated inputs and outputs; deny-by-default for network, file and payment actions.
- **Approval gates:** human approval for irreversible, financial, external-communication or data-export actions.
- **Memory hygiene:** control what is persisted in agent memory; prevent cross-user contamination; retention limits.
- **Multi-agent trust:** do not let one agent's output automatically authorise another's privileged action.
- **Observability:** complete trace logs (prompts, retrieved content IDs, tool calls, approvals), retained per policy, for incident response and forensics (see `cyber-forensics-evidence`).
- **Containment:** sandboxed execution; egress controls; kill switch; staged rollout.

## 3. Review template (Workflow 7)

| OWASP ID | Exposure in this system (Observed/Assessed/Assumed) | Controls present | Gaps | Priority (Critical/High/Medium/Low) | Recommended controls | Owner | Due |
|---|---|---|---|---|---|---|---|
| LLM01 | | | | | | | |
| LLM02 | | | | | | | |
| … | | | | | | | |

**Architecture questions to ask:**
1. Which data sources feed the model at runtime (user input, documents, email, web, APIs)? Which of them are untrusted?
2. Which tools or actions can the model trigger? With whose permissions? Which need human approval?
3. Where does model output go (UI, code execution, database, email, other systems)?
4. Is retrieval permission-aware per user?
5. What is logged, for how long, and where (CERT-In and DPDP log retention)?
6. Which third-party models and plugins are used, and how are updates controlled?
7. What are the cost, rate and size limits?
8. How are incidents (harmful output, data leak, misuse) detected and escalated?

## 4. Red-team governance (process, not content)

1. **Authorisation:** written scope, systems, time window, and approvers; legal review; no production data unless approved.
2. **Team:** internal or external testers under contract with confidentiality; diverse testers including Indian-language expertise.
3. **Coverage:** map test objectives to the OWASP IDs, NIST AI 600-1 risks and the organisation's harm taxonomy.
4. **Safety:** testing in a staging environment where possible; stop conditions; handling of any harmful material produced (secure storage, deletion).
5. **Recording:** log all tests; findings rated with severity and reproducibility; evidence stored securely.
6. **Remediation:** findings go into the AI risk register; retest; residual risk accepted by the owner.
7. **Reporting:** a summary to the AI risk committee; lessons into the AI policy and secure development standards.
8. **External obligations:** EU AI Act Art. 55 adversarial testing for GPAI with systemic risk; sector expectations; disclosure policies.
