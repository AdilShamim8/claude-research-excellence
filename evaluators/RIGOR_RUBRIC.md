# Methodological Rigor Rubric

## 🔬 QUANTITATIVE RIGOR ASSESSMENT SYSTEM (0–100)

```
ACTIVATE: RIGOR_SCORE
```

This rubric assesses the methodological integrity, statistical power, and experimental defensibility of a scientific study. It pre-empts methodological critiques from adversarial peer reviewers.

---

### Scoring Dimensions

#### DIMENSION 1 — STATISTICAL POWER & SAMPLE JUSTIFICATION (0–25)
*Assesses sample size adequacy, power analysis, and effect estimation.*

* **25 pts**: Formal a priori power calculation reported with justified effect size (SESOI); adequate power (≥0.85); all sample recruitment targets met without post-hoc data peeking.
* **20 pts**: A priori power calculation conducted with standard parameters; slight shortfall in recruitment adequately discussed with sensitivity power analysis.
* **15 pts**: Post-hoc power analysis or sample size justified by resource constraints / field norms; point estimates accompanied by confidence intervals throughout.
* **10 pts**: Sample size justified only by precedent ("similar to previous studies"); CI reported inconsistently; bare p-values dominate.
* **5 pts**: Substantially underpowered sample without justification; high risk of Type II error; arbitrary sample size cutoff.
* **0 pts**: No sample justification, severe underpowering, or evident sample peeking / optional stopping.

#### DIMENSION 2 — INTERNAL VALIDITY & CONFOUNDER CONTROL (0–25)
*Assesses causal identification, randomization, blinding, and control conditions.*

* **25 pts**: True random assignment or quasi-experimental identification strategy (IV, RDD, DiD with parallel trends test); double-blind execution where possible; active and negative control groups; balance checks confirmed.
* **20 pts**: Strong experimental design with appropriate control conditions; single blinding or automated objective measurement; minor potential confounds measured and statistically adjusted.
* **15 pts**: Standard control groups present; blinding not feasible but objective endpoints used; reasonable covariate adjustment in observational setups.
* **10 pts**: Observational design with residual confounding risk; weak or passive control group; self-report endpoints without blinding.
* **5 pts**: High risk of unmeasured confounding; obvious alternative explanations unaddressed; no control group or inappropriate comparator.
* **0 pts**: Completely confounded design; fatal selection bias; reverse causality plausible and unaddressed.

#### DIMENSION 3 — MEASUREMENT RELIABILITY & CONSTRUCT VALIDITY (0–25)
*Assesses tool calibration, operationalization, assay validity, and error handling.*

* **25 pts**: Multi-trait multi-method validation; validated psychometric or biophysical instruments with reported internal consistency (ω or α ≥ 0.85) or calibration curves; test-retest reliability documented; measurement error explicitly modeled.
* **20 pts**: Established, standard instruments used with documented reliability; calibration procedures reported; floor/ceiling effects checked and absent.
* **15 pts**: Adaptations of validated measures used; reliability assessed and acceptable; modest measurement noise acknowledged.
* **10 pts**: Ad-hoc measures created without formal psychometric or technical validation; single-item indicators used for complex latent constructs.
* **5 pts**: Uncalibrated instrumentation or proxy measures with questionable relation to target construct.
* **0 pts**: Invalid construct operationalization; severe measurement contamination or circular measurement.

#### DIMENSION 4 — REPRODUCIBILITY & OPEN SCIENCE ARTIFACTS (0–25)
*Assesses pre-registration fidelity, data sharing, code availability, and computational reproducibility.*

* **25 pts**: Detailed timestamped pre-registration (OSF / AsPredicted / ClinicalTrials.gov) with clear distinction between confirmatory and exploratory analyses; open data in FAIR repository with DOI; fully reproducible containerized code (Docker / Conda); deterministic random seeds.
* **20 pts**: Pre-registration completed prior to data collection; data and analysis scripts shared in public repository; minor manual setup steps required.
* **15 pts**: Pre-registered protocol with minor unannounced deviations; data available upon reasonable request or with access controls; code shared as scripts without dependency pinning.
* **10 pts**: Not pre-registered; data availability statement present with external restrictions; partial code scripts shared.
* **5 pts**: No pre-registration; data available only "upon request from corresponding author" with no code provided.
* **0 pts**: Complete absence of data, code, or registration; methods described with insufficient detail to permit independent replication.

---

### Total Rigor Score Interpretation

| Score Band | Classification | Peer Review Outlook | Recommended Actions |
|---|---|---|---|
| **90–100** | **Ironclad Rigor** | Immunity to methodological rejection at top-tier venues | Highlight open science badges and pre-registration in cover letter |
| **75–89** | **High Rigor** | Strong methodology; typical revisions will be minor or clarification-based | Ensure all sensitivity analyses and boundary checks are in Supplementary Information |
| **60–74** | **Acceptable Rigor** | Methodological concerns likely raised by Reviewer 1 (The Skeptic) | Add robustness checks, specify covariate selection models, and deposit code/data to Zenodo |
| **45–59** | **Fragile Rigor** | Major revision or desk-reject risk due to power or confounder vulnerabilities | Re-analyze with stronger controls or collect targeted replication sample |
| **< 45** | **Fatal Vulnerability** | High probability of rejection across all reputable journals | Redesign experimental protocol; activate `SKILL: METHODOLOGY` |
