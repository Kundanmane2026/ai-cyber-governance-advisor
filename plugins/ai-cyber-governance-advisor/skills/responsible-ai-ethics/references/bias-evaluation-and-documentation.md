# Bias Evaluation and Transparency Documentation

## 1. Sources of bias (where to look)

| Stage | Bias type | Example (Indian context) |
|---|---|---|
| Problem framing | Target or proxy bias | Using "past repayment" as a proxy for creditworthiness excludes first-time borrowers (often rural or women) |
| Data collection | Representation / sampling bias | Speech data dominated by Hindi and English; few Marathi, Tamil or tribal-language speakers |
| Labelling | Annotator bias | Annotators from one region label dialect as "low quality" or "toxic" |
| Features | Proxy discrimination | PIN code or surname correlates with caste or religion |
| Historical data | Historical bias | Past hiring data reflects gender imbalance |
| Model | Aggregation bias | One model for all regions hides subgroup errors |
| Evaluation | Benchmark bias | English-only benchmarks for a multilingual product |
| Deployment | Feedback loops; context shift | Predictive policing concentrates patrols in already over-policed areas |

## 2. Fairness criteria (concepts)

| Criterion | Plain meaning | When it fits | Caution |
|---|---|---|---|
| **Demographic (statistical) parity** | Same rate of positive outcomes across groups | Allocation where base rates *should* be equal, or for representation goals | Can conflict with accuracy if real base rates differ |
| **Equal opportunity** | Same true-positive rate across groups | Benefits: qualified people should be approved equally | Ignores false positives |
| **Equalised odds** | Same true-positive *and* false-positive rates | High-stakes decisions where both error types matter | Harder to achieve; may reduce accuracy |
| **Predictive parity / calibration** | A score means the same probability in each group | Risk scores used by human decision-makers | Incompatible with equalised odds when base rates differ |
| **Counterfactual fairness** | Outcome unchanged if only the protected attribute changes | Causal reasoning available | Needs causal assumptions |
| **Individual fairness** | Similar individuals are treated similarly | Where a sound similarity measure exists | Defining "similar" is value-laden |

**Impossibility result:** when base rates differ between groups, calibration and equalised odds cannot both hold (except for a perfect predictor). Choose based on the harm, the law and stakeholder input, and record the rationale. Leave the value judgement to accountable humans.

**Rule-of-thumb screen:** the "four-fifths rule" (selection rate for a group less than 80% of the highest group's rate) is a US employment heuristic. It is useful as a screen, not a legal standard in India.

## 3. Generative AI evaluation (concepts)

- **Representational harms:** stereotyping, demeaning content, erasure (for example, image prompts for "a doctor" across gender, skin tone, region; story prompts across castes and religions). Use paired or counterfactual prompts that vary only the identity term.
- **Quality-of-service:** accuracy, fluency and refusal rates across Indian languages, scripts (Devanagari, Latin transliteration) and dialects.
- **Toxicity and hate:** measured with classifiers validated for Indian languages and code-mixed text (Hinglish, Marathi–English); human review of samples.
- **Factuality / hallucination:** domain test sets with references; citation accuracy for retrieval-based systems.
- **Safety:** policy-violating output rates on a governed evaluation set. Red-teaming is a **governed process**: scoped, authorised, logged, with findings fed into mitigation. This skill does not produce attack prompts.

## 4. Evaluation plan template

```
BIAS & FAIRNESS EVALUATION PLAN — [System name, version]          Owner: [ ]   Date: [ ]
1. Decision / output and its consequences
2. Affected groups and attributes (incl. intersectional slices); lawful basis to hold group labels (DPDP)
3. Harm type(s): allocative / quality-of-service / representational
4. Fairness criteria chosen + rationale + trade-offs accepted (approved by: [ ])
5. Data: evaluation set source, size per group (min. [n] per slice), languages/scripts, labelling process
6. Metrics and thresholds
   | Metric | Groups compared | Threshold | Confidence method |
7. Qualitative review protocol (generative): prompts, reviewers (diverse), rubric
8. Mitigations if thresholds are missed
9. Post-deployment monitoring: metrics, frequency, alert thresholds, owner
10. Sign-off
```

**Results table:**

| Group / slice | n | Selection rate | TPR | FPR | Precision | Calibration gap | Ratio to reference | Pass/Fail | Label |
|---|---|---|---|---|---|---|---|---|---|

## 5. Model card template (after Mitchell et al., 2019)

```
MODEL CARD — [Model name, version]                       Last updated: [ ]
1. Model details: developer, date, version, type/architecture, licence, contact
2. Intended use: primary uses; intended users; OUT-OF-SCOPE uses
3. Factors: relevant groups, languages, environments, instrumentation
4. Metrics: performance measures; decision thresholds; variation approaches
5. Evaluation data: datasets, motivation, preprocessing
6. Training data: summary (or link to the datasheet); provenance and licences
7. Quantitative analyses: disaggregated results (unitary and intersectional)
8. Ethical considerations: sensitive data, risks, mitigations, known harms
9. Caveats and recommendations: limitations, known failure modes, monitoring
10. For generative models: safety evaluations; content policies; watermarking/provenance (C2PA etc.);
    known hallucination patterns; jailbreak resistance testing summary (no attack content)
```

## 6. Datasheet for datasets template (after Gebru et al., 2018/2021)

```
DATASHEET — [Dataset name, version]
1. Motivation: why created, by whom, funding
2. Composition: instances, counts, labels, missing data, confidential/personal data, sub-populations,
   whether individuals are identifiable; children's data
3. Collection process: how, who, timeframe, consent / notice (DPDP s.5–6), ethical review
4. Preprocessing / cleaning / labelling: steps; raw data retained?; annotator demographics and pay
5. Uses: used for; should NOT be used for
6. Distribution: to whom, licence, export / transfer restrictions
7. Maintenance: owner, update cadence, erasure requests handling (DPDP s.12), versioning
8. IP: copyright status, licences, opt-outs honoured
```

## 7. System card / AI fact sheet (system-level)

System purpose; components (models, retrieval, tools, rules); human roles and oversight points; data flows; deployment context; performance and fairness summary; safety measures; monitoring; incident process; contact for complaints; change log.

## 8. User-facing AI notice (plain language)

> **You are using an AI-assisted service.** [Service] uses artificial intelligence to [purpose]. It may make mistakes, so please check important information. [A person reviews / You can ask a person to review] decisions about [X]. To ask for human review or to correct your information, [contact/link]. Learn more about how we use AI and your data: [link].

Provide the notice in English and the relevant Indian languages. For a decision affecting a person, add the main factors, the right to contest, and the timelines.
