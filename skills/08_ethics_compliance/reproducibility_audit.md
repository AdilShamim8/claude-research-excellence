# Reproducibility Audit: Comprehensive Guide to Ensuring Research Reproducibility

> **If your research cannot be reproduced, it cannot be trusted. This guide provides a systematic framework for auditing and ensuring reproducibility at every stage.**

---

## 1. Reproducibility Audit Checklist

### Pre-Audit Setup

Before beginning the audit, establish:
- [ ] Audit team identified (at least one person who was NOT involved in the original analysis)
- [ ] Audit timeline and scope defined
- [ ] All materials accessible (data, code, documentation, environment specifications)
- [ ] Audit reporting template prepared

---

## 2. Code Audit Standards

### C2.1 Code Availability and Access

- [ ] **Source code publicly available** in a version-controlled repository (GitHub, GitLab, Bitbucket, etc.)
- [ ] Repository includes a clear README with setup instructions
- [ ] All code versions tagged or release-marked corresponding to manuscript figures/tables
- [ ] License specified (MIT, Apache 2.0, GPL, or CC0 for maximum reproducibility)
- [ ] DOI assigned through Zenodo or similar for permanent archival

### C2.2 Code Quality

- [ ] **Code is readable**: meaningful variable names, consistent style, appropriate comments
- [ ] Code follows a consistent style guide (PEP 8 for Python, Google Style for R, etc.)
- [ ] Magic numbers eliminated — all constants defined as named variables with comments
- [ ] No hardcoded file paths (use relative paths or configuration files)
- [ ] Functions are modular — each function does one thing well
- [ ] Code is DRY (Don't Repeat Yourself) — no duplicated logic

### C2.3 Code Documentation

- [ ] **README file** includes: purpose, requirements, installation, usage, output description
- [ ] Docstrings for all functions (inputs, outputs, behavior, edge cases)
- [ ] Comments explain WHY, not just WHAT (the code itself shows what; comments explain reasoning)
- [ ] Analysis pipeline documented step-by-step (what runs when, in what order)
- [ ] Mapping between code outputs and manuscript figures/tables is explicit

### C2.4 Code Testing

- [ ] Unit tests for critical functions (especially data transformations and statistical calculations)
- [ ] Integration tests for the full pipeline
- [ ] Known-answer tests: verify code produces correct output on simple test cases with hand-calculable results
- [ ] Edge case testing: verify behavior with missing data, single observations, zero-variance variables
- [ ] Continuous integration (CI) configured to run tests automatically

### C2.5 Randomness and Determinism

- [ ] **Random seeds set** and documented for all random processes
- [ ] Seeds set at the beginning of each analysis section, not just globally
- [ ] Stochastic processes run multiple times to verify stability of results
- [ ] If results vary with seed choice: report range across multiple seeds
- [ ] GPU non-determinism documented if applicable (some GPU operations are non-deterministic)

### Code Audit Scoring

| Category | Weight | Criteria for "Pass" |
|---|---|---|
| Availability | 25% | Code publicly available with DOI and license |
| Readability | 20% | Independent reviewer can understand the logic |
| Documentation | 20% | README + docstrings + pipeline mapping |
| Testing | 20% | Unit tests for critical functions; CI configured |
| Determinism | 15% | Seeds set; results reproducible across runs |

---

## 3. Data Audit Standards

### D3.1 Raw Data Preservation

- [ ] **Raw data preserved** in its original, unmodified form
- [ ] Raw data stored separately from processed/analyzed data
- [ ] No transformations applied to raw data files
- [ ] Raw data file formats are standard and accessible (CSV, JSON, HDF5, etc.)
- [ ] If raw data cannot be shared (privacy/legal): synthetic or anonymized dataset provided with documentation of what was changed

### D3.2 Data Documentation

- [ ] **Data dictionary / codebook** provided with:
  - Variable names, types, and descriptions
  - Valid ranges and coding schemes
  - Units of measurement
  - Missing data codes and their meanings
  - Source of each variable (measured, derived, computed)
- [ ] Data collection methodology documented
- [ ] Known data quality issues documented (outliers, measurement errors, etc.)

### D3.3 Data Processing Pipeline

- [ ] **All data transformations documented** step-by-step:
  - Filtering criteria (and how many observations removed at each step)
  - Variable transformations (log, standardization, recoding)
  - Derivation of computed variables (exact formulas provided)
  - Merging and joining operations (keys used, one-to-one or one-to-many)
- [ ] Processing steps are implemented in code (not manual Excel operations)
- [ ] Pipeline is reversible: processed data can be regenerated from raw data by running the code
- [ ] Intermediate datasets saved at key pipeline stages for verification

### D3.4 Data Integrity Checks

- [ ] Row counts verified at each pipeline stage (no silent row loss)
- [ ] Summary statistics verified at each pipeline stage (means, ranges, missing counts)
- [ ] Referential integrity verified (no orphaned records after joins)
- [ ] Consistency checks: categorical variable levels match expected values
- [ ] Temporal consistency: dates are in valid ranges, chronological order is maintained

### D3.5 Data Sharing Compliance

- [ ] Data shared in a trusted repository (Dryad, Figshare, Zenodo, ICPSR, institutional repository)
- [ ] DOI assigned to the dataset
- [ ] Data license specified (CC0, CC-BY, or CC-BY-SA recommended)
- [ ] Access restrictions documented with justification (if not fully open)
- [ ] Data access process described for restricted data

### Data Audit Scoring

| Category | Weight | Criteria for "Pass" |
|---|---|---|
| Raw data preservation | 25% | Original data intact and separate from processed data |
| Documentation | 25% | Complete codebook with all variable descriptions |
| Processing pipeline | 25% | All transformations in code; pipeline is reversible |
| Integrity checks | 15% | Automated checks at each pipeline stage |
| Sharing compliance | 10% | Data deposited with DOI and license |

---

## 4. Analysis Audit Standards

### A4.1 Analysis Reproducibility

- [ ] **All results in the manuscript** can be reproduced by running the provided code on the provided data
- [ ] Figure-by-figure and table-by-table verification completed
- [ ] Numerical results match to the stated precision (e.g., p-values, effect sizes)
- [ ] Minor discrepancies (< 0.1% for continuous values) are documented and explained
- [ ] No results appear in the manuscript that are not generated by the documented code

### A4.2 Statistical Method Verification

- [ ] **Statistical methods verified** against independent implementation:
  - Compare results with a second statistical package (e.g., if using R, verify with Python/statsmodels or Stata)
  - For custom implementations: compare against a reference package on a known dataset
- [ ] Assumption checks documented and verified (normality, homoscedasticity, etc.)
- [ ] Degrees of freedom verified (especially for mixed models, clustered standard errors)
- [ ] P-value calculations verified (one-tailed vs. two-tailed, correction for multiple comparisons)

### A4.3 Sensitivity Analysis Audit

- [ ] Results robust to reasonable alternative specifications:
  - [ ] Alternative model specifications tested
  - [ ] Alternative variable operationalizations tested
  - [ ] Alternative inclusion/exclusion criteria tested
  - [ ] Alternative missing data handling methods tested
- [ ] Sensitivity analysis results reported (in manuscript or supplementary materials)
- [ ] Conclusions are robust across specifications (or fragility is acknowledged)

### A4.4 Effect Size and Confidence Interval Verification

- [ ] Effect sizes independently recalculated for all primary outcomes
- [ ] Confidence intervals verified (correct formula, correct coverage level)
- [ ] No discrepancies between reported and recalculated values (or discrepancies documented)
- [ ] Forest plots or similar visualizations provided for meta-analytic results

### Analysis Audit Scoring

| Category | Weight | Criteria for "Pass" |
|---|---|---|
| Result reproducibility | 35% | All figures/tables reproduced with documented code |
| Method verification | 25% | Results verified against independent implementation |
| Sensitivity analysis | 20% | Robustness tested across reasonable alternatives |
| Effect size verification | 20% | All primary effect sizes independently recalculated |

---

## 5. Environment Audit Standards

### E5.1 Software Environment

- [ ] **Programming language versions** specified (e.g., Python 3.11.4, R 4.3.1)
- [ ] All package/library versions listed with exact version numbers
- [ ] Package versions locked via requirements.txt, renv.lock, or environment.yml
- [ ] Operating system specified (including version)
- [ ] Compiler versions specified if applicable (GCC, CUDA, etc.)

### E5.2 Computational Environment Reproducibility

- [ ] **Containerization** provided (Docker, Singularity/Apptainer, or similar)
- [ ] Container includes all dependencies pre-installed
- [ ] Container build file (Dockerfile) is version-controlled and documented
- [ ] Alternative: Virtual machine image or cloud compute snapshot provided
- [ ] Alternative: Conda/environment specification file provided with exact versions

### E5.3 Hardware Specification

- [ ] Hardware used for key computations specified (CPU, GPU, RAM)
- [ ] Training/computation time reported for major analyses
- [ ] Memory requirements estimated and reported
- [ ] Cloud compute specifications provided if applicable (instance type, region)

### E5.4 Computational Cost Reporting

- [ ] Total compute time reported (wall-clock and CPU-hours)
- [ ] Estimated carbon footprint calculated and reported (using tools like carbontracker, green-algorithms)
- [ ] Cost in cloud computing dollars reported if applicable
- [ ] Feasibility assessment: can the analysis be run on a standard laptop, or is specialized hardware required?

### Environment Audit Scoring

| Category | Weight | Criteria for "Pass" |
|---|---|---|
| Software specification | 30% | All versions listed and locked |
| Containerization | 30% | Docker or equivalent container provided |
| Hardware specification | 20% | Key hardware and compute time reported |
| Cost reporting | 20% | Compute time and environmental cost reported |

---

## 6. Documentation Audit Standards

### F6.1 Methods Documentation

- [ ] **Methods section provides sufficient detail** for an independent researcher to replicate the study
- [ ] All procedures described in chronological order
- [ ] Equipment and materials specified with manufacturer and model numbers
- [ ] Software and packages specified with versions and citations
- [ ] Analysis parameters specified (not left as defaults without stating what they are)

### F6.2 Protocol Documentation

- [ ] Study protocol available (as supplementary material or pre-registration)
- [ ] Protocol matches what was actually done (deviations documented)
- [ ] Standard Operating Procedures (SOPs) available for key procedures

### F6.3 Reproducibility Documentation

- [ ] **REPRODUCIBILITY.md** file in the repository containing:
  - Step-by-step instructions to reproduce each figure and table
  - Expected runtime for each step
  - Expected output for verification (e.g., "Figure 2a should show AUC = 0.89")
  - Troubleshooting guide for common issues
- [ ] Mapping between manuscript claims and code/data is explicit

### F6.4 Version Control

- [ ] All materials under version control (code, data processing scripts, manuscript)
- [ ] Commit messages are descriptive
- [ ] Tags or releases correspond to specific analysis milestones
- [ ] Branch strategy documented if complex

### Documentation Audit Scoring

| Category | Weight | Criteria for "Pass" |
|---|---|---|
| Methods documentation | 30% | Independent researcher could replicate the study |
| Protocol documentation | 20% | Protocol available and matches actual procedures |
| Reproducibility guide | 30% | Step-by-step reproduction instructions with expected outputs |
| Version control | 20% | All materials version-controlled with meaningful tags |

---

## 7. Reporting Audit Standards

### G7.1 Complete Reporting

- [ ] **All analyses reported**, not just significant ones
- [ ] All measured variables reported, even if not included in final models
- [ ] All study conditions reported, including pilot conditions
- [ ] Non-significant results reported with the same detail as significant results
- [ ] Effect sizes with confidence intervals reported for all tests

### G7.2 Transparent Reporting

- [ ] Pre-registration details provided (registry, registration number)
- [ ] Deviations from pre-registered plan documented and justified
- [ ] Exploratory vs. confirmatory analyses clearly distinguished
- [ ] Researcher degrees of freedom acknowledged
- [ ] Negative results and failed approaches reported

### G7.3 Reporting Standard Compliance

- [ ] Appropriate reporting checklist completed (CONSORT, STROBE, PRISMA, etc.)
- [ ] Checklist included as supplementary material
- [ ] All checklist items addressed or explanation provided for non-applicability

---

## 8. Pre-Submission Reproducibility Audit Protocol

### Step 1: Self-Audit (Weeks Before Submission)

1. Run all code from scratch in a fresh environment
2. Verify every figure and table against the manuscript
3. Check all numerical claims (p-values, effect sizes, sample sizes)
4. Ensure the repository README is complete and accurate

### Step 2: Independent Audit (2 Weeks Before Submission)

1. Ask a colleague who was NOT involved in the analysis to:
   - Clone the repository
   - Follow the README instructions
   - Attempt to reproduce all figures and tables
   - Document any issues encountered
2. Fix all identified issues
3. Have the same colleague re-verify the fixes

### Step 3: Container Verification (1 Week Before Submission)

1. Build the Docker container from the Dockerfile
2. Run the full analysis pipeline inside the container
3. Verify all outputs match the manuscript
4. Test on a different operating system if possible

### Step 4: Final Verification (Days Before Submission)

1. Re-read the manuscript with fresh eyes
2. Verify every numerical claim against code output
3. Confirm all supplementary materials are current
4. Verify all DOIs and URLs are functional
5. Run the complete reproducibility checklist one final time

---

## 9. Common Reproducibility Failures and Fixes

| Failure | Cause | Fix | Prevention |
|---|---|---|---|
| **Results differ on re-run** | Random seed not set; non-deterministic GPU operations | Set seeds explicitly; use deterministic GPU modes; run multiple times to assess variability | Always set seeds at the start of each analysis section |
| **Code doesn't run** | Missing dependencies; version incompatibilities | Use containers; pin all package versions; test in fresh environment | Docker from the start; CI pipeline |
| **Data files not found** | Hardcoded file paths; relative path errors | Use relative paths from repository root; use configuration files | Never hardcode absolute paths |
| **Different software versions, different results** | Algorithm changes across versions; floating point differences | Pin all versions; verify critical results across versions | Document exact versions; use containers |
| **Missing intermediate results** | Only final results saved; intermediate steps not documented | Save checkpoints; log all intermediate outputs | Implement logging at each pipeline stage |
| **Undocumented manual steps** | Manual data cleaning in Excel; point-and-click operations | Automate everything in code; document any manual steps | Rule: if it's not in code, it didn't happen |
| **Figures not reproducible** | Manual adjustments in graphics software; random seeds not set for figure generation | Generate all figures programmatically; set seeds before each figure | Script every figure; never manually edit |
| **Sample size mismatch** | Unclear exclusion criteria; silent data loss in pipeline | Document every exclusion step with counts; add assertions for expected row counts | Add data quality checks at each pipeline step |
| **Missing variables** | Variable computed during analysis but not documented | Add all derived variables to data dictionary with formulas | Update codebook immediately when creating new variables |
| **Time-dependent results** | Web scraping; API calls; database queries that change over time | Archive raw data at the time of analysis; timestamp all data snapshots | Never re-query; always use archived snapshots |

---

## 10. Reproducibility Score Calculation

### Scoring Rubric

Calculate a composite Reproducibility Score (RS) across all audit categories:

| Category | Max Points | Scoring Criteria |
|---|---|---|
| Code | 25 | Availability (7) + Quality (6) + Documentation (6) + Testing (6) |
| Data | 25 | Preservation (7) + Documentation (6) + Pipeline (6) + Sharing (6) |
| Analysis | 20 | Reproducibility (8) + Verification (6) + Sensitivity (6) |
| Environment | 15 | Software (5) + Containerization (5) + Hardware/Cost (5) |
| Documentation | 10 | Methods (3) + Reproducibility guide (4) + Version control (3) |
| Reporting | 5 | Completeness (2) + Transparency (2) + Standard compliance (1) |
| **Total** | **100** | |

### Score Interpretation

| Score Range | Grade | Interpretation |
|---|---|---|
| 90–100 | **A: Exemplary** | Research is fully reproducible with minimal effort; gold standard |
| 80–89 | **B: Strong** | Research is reproducible with minor effort; some improvements possible |
| 70–79 | **C: Adequate** | Research is likely reproducible but some barriers exist; improvements needed |
| 60–69 | **D: Marginal** | Reproducibility is uncertain; significant improvements required |
| Below 60 | **F: Inadequate** | Reproducibility is unlikely; major overhaul required before submission |

### Minimum Scores for Submission

- **Tier 1 journals**: Minimum RS = 85 (Grade B+)
- **Tier 2 journals**: Minimum RS = 75 (Grade C+)
- **Tier 3 journals**: Minimum RS = 65 (Grade D+)
- **Any journal**: Critical items (data preservation, code availability, result reproducibility) must score maximum points

---

## 11. Reproducibility Statement Template for Manuscripts

```
## Reproducibility Statement

We are committed to the full reproducibility of our research. The
following resources are publicly available:

**Code**: All analysis code is available at [GitHub URL] (licensed
under [License]). A permanently archived version is available at
[DOI from Zenodo].

**Data**: [All data / Anonymized data / Synthetic data] are available
at [Repository URL] (DOI: [DOI]). [If restricted: Data access can be
requested through (process) due to (justification).]

**Environment**: A Docker container with all dependencies pre-installed
is available at [Docker Hub URL / GitHub Container Registry]. Build
instructions and a complete environment specification file are included
in the repository.

**Verification**: All results in this manuscript have been independently
verified by [Name], who was not involved in the original analysis, by
running the provided code on the provided data in a fresh computational
environment. All figures, tables, and numerical results were reproduced
with no discrepancies.

**Computational requirements**: The full analysis pipeline requires
approximately [X] hours on a [hardware specification]. Estimated
computational cost is [$X / X kg CO₂]. Detailed timing information
is provided in the repository README.

**Pre-registration**: This study was pre-registered at [Registry]
([Registration DOI/URL]).

**Reproducibility score**: This study achieved a reproducibility score
of [X]/100 based on the CRES Reproducibility Audit Framework. Detailed
audit results are available in Supplementary Table S[X].
```

---

*Last updated: 2024 | CRES v2.0 | Skill 08: Ethics & Compliance*
