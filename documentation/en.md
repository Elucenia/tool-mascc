<!-- ELUCENIA technical documentation · mascc · en · no clinical/professional/rights approval -->

# MASCC index

[conditions, sources and permissions](https://elucenia.org/en/tools/mascc)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Burden of illness (symptoms of the febrile episode)

`carga`

- `0` — Severe or moribund
- `3` — Moderate
- `5` — None or mild

### Hypotension (systolic blood pressure \< 90 mmHg)

`hipotensao`

- `0` — Yes
- `5` — No

### Active COPD

`dpoc`

- `0` — Yes
- `4` — No

### Cancer type

`tumor`

- `0` — Hematological malignancy with prior fungal infection
- `4` — Solid tumor, or hematological malignancy without prior fungal infection

### Dehydration requiring intravenous fluids

`desidratacao`

- `0` — Yes
- `3` — No

### Where fever began

`local`

- `0` — During hospitalization
- `3` — Outpatient

### Age

`idade`

- `0` — ≥ 60 years
- `2` — \< 60 years

## Method edition

MASCC/Klastersky 2000: 7 domains, total 0–26, cutoff ≥21; ASCO/IDSA 2018 context

## Documented formula

Burden of illness: none/mild 5, moderate 3, severe 0 · no hypotension 5 · no COPD 4 · solid tumour 4, or haematological malignancy without prior fungal infection 4 · no dehydration 3 · outpatient 3 · age \<60 years 2. Maximum: 26.

## Limits and population

MASCC ≥21 indicates a lower risk of complications but does not, on its own, authorize discharge, oral antibiotics or outpatient management. In the ASCO/IDSA 2018 context, selection depends on clinical assessment, stability, comorbidities, ability to attend return visits, a caregiver at home, and access to a telephone and transport. Candidates for outpatient management must be observed for at least 4 hours before discharge and require follow-up. The hypotension criterion in this implementation follows the original 2000 variable: SBP \<90 mmHg.

## References

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
