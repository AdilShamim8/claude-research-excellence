# Statistical Rigor Framework

## A Comprehensive Guide to Ensuring Statistical Validity in Research

### Purpose
This framework provides detailed protocols for every aspect of statistical rigor in empirical research — from pre-registration through analysis, reporting, and interpretation. It ensures that statistical inferences are valid, reproducible, and honestly reported.

---

## SECTION 1: PRE-REGISTRATION REQUIREMENTS

### 1.1 What Must Be Pre-Registered

| Element | Required | Optional | Rationale |
|---------|----------|----------|-----------|
| Hypotheses (directional) | ✓ | | Distinguishes confirmatory from exploratory |
| Primary outcome(s) | ✓ | | Prevents outcome switching |
| Secondary outcomes | ✓ | | Prevents selective reporting |
| Analysis plan (exact tests) | ✓ | | Prevents p-hacking via analytic flexibility |
| Sample size justification | ✓ | | Ensures adequate power |
| Inclusion/exclusion criteria | ✓ | | Prevents post-hoc sample selection |
| Covariates | ✓ | | Prevents covariate hacking |
| Multiple comparison correction | ✓ | | Controls familywise error rate |
| Transformation/normalization | ✓ | | Prevents data-driven transformations |
| Mediation/moderation analysis plan | | ✓ | | If planned a priori |
| Subgroup analyses | | ✓ | | If planned a priori |
| Handling of outliers | ✓ | | Prevents selective exclusion |
| Missing data strategy | ✓ | | Prevents selective imputation |

### 1.2 Pre-Registration Platforms

| Platform | Best For | Cost | Features |
|----------|---------|------|----------|
| **OSF** | All disciplines; comprehensive | Free | Timestamped, DOI, version control, integrations |
| **AsPredicted** | Quick pre-registration | Free | 9-question format, fast, simple |
| **ClinicalTrials.gov** | Clinical trials (mandatory) | Free | Legal requirement for many trials |
| **PROSPERO** | Systematic reviews | Free | Required by many journals |
| **EGAP** | Development/political science experiments | Free | Domain-specific templates |

### 1.3 Pre-Registration Timing
- **Ideal:** Before any data collection begins
- **Acceptable:** Before any analysis of the data (for existing datasets)
- **Not acceptable:** After seeing the data, even if before writing the manuscript (this is still HARKing)

### 1.4 Registered Reports
For maximum rigor, submit as a Registered Report:
1. Submit the introduction, methods, and analysis plan before data collection
2. Journal conducts peer review and grants in-principle acceptance
3. Collect data according to the accepted plan
4. Submit results and discussion; journal commits to publication regardless of outcome (subject to methodological fidelity)

**Benefits:** Eliminates publication bias, prevents p-hacking, and ensures results are published even if null

---

## SECTION 2: POWER ANALYSIS PROTOCOLS

### 2.1 A Priori Power Analysis

**Purpose:** Determine the minimum sample size needed before data collection.

**Procedure:**
1. **Specify the effect size of interest**
   - Ideally: Smallest Effect Size of Interest (SESOI) — the smallest effect that would be theoretically or practically meaningful
   - Alternatively: Expected effect size from prior literature (meta-analytic estimate preferred over single-study estimate)
   - Avoid: Using "small," "medium," or "large" labels without justification (Cohen's conventions are field-specific)

2. **Specify alpha level**
   - Standard: α = .05
   - Strong evidence: α = .005 (recommended by Benjamin et al., 2018 for novel findings)
   - Exploratory: α = .10 (acceptable only for genuinely exploratory analyses)

3. **Specify desired power**
   - Minimum: 1-β = .80 (20% chance of missing a real effect)
   - Recommended: 1-β = .90 (10% chance of missing a real effect)
   - High-stakes: 1-β = .95 (5% chance of missing a real effect)

4. **Run the analysis**
   - Software: G*Power (free), R (pwr, WebPower), Python (statsmodels)
   - Document: The exact parameters, software, and version used

**Template for reporting:**
```
An a priori power analysis was conducted using G*Power 3.1 (Faul et al., 2007)
for a [TEST TYPE] with [PARAMETERS]. To detect an effect size of [d/f/r =
VALUE] (based on [JUSTIFICATION]), with α = [VALUE] and power = [VALUE],
the required sample size was N = [VALUE]. Anticipating [ATTRITION RATE]%
attrition, we aimed to recruit N = [VALUE] participants.
```

### 2.2 Post Hoc Power Analysis

**WARNING:** Post hoc (observed) power is a circular transformation of the p-value and provides no additional information. Do not report post hoc power.

**Instead, report:**
- The achieved power for the effect size you planned to detect (using a priori power analysis parameters)
- The minimum detectable effect size (MDES) given your actual sample size

**MDES reporting template:**
```
Given the achieved sample size of N = [VALUE], the minimum detectable effect
size (MDES) at α = [VALUE] with power = [VALUE] was [d/f/r = VALUE],
calculated using [SOFTWARE].
```

### 2.3 Sensitivity Power Analysis

**Purpose:** Determine the range of effect sizes that your sample can reliably detect.

**Procedure:**
1. Fix N at your achieved sample size
2. Fix α at your chosen level
3. Fix power at your chosen level
4. Compute the minimum detectable effect size

**When to use:**
- When you have a fixed sample size and need to know what effects you can detect
- When reporting the limitations of an underpowered study
- When planning secondary analyses that were not part of the original power analysis

---

## SECTION 3: MULTIPLE COMPARISON CORRECTIONS

### 3.1 When Corrections Are Needed

Multiple comparison corrections are required when you are conducting **confirmatory** statistical tests on the same dataset. The more tests you run, the higher the probability that at least one will be significant by chance alone.

**Familywise error rate:** P(at least one false positive) = 1 - (1 - α)^k, where k = number of tests

For k = 10 tests at α = .05: P(at least one false positive) = .40

### 3.2 Correction Methods

| Method | How It Works | When to Use | Trade-off |
|--------|-------------|-------------|-----------|
| **Bonferroni** | α_adjusted = α / k | Small number of tests; strict control | Very conservative; reduces power substantially |
| **Holm-Bonferroni** | Sequential rejection; step-down procedure | General purpose; better than Bonferroni | Less conservative than Bonferroni but still strict |
| **Benjamini-Hochberg (FDR)** | Controls proportion of false discoveries, not absolute number | Large number of tests; exploratory analyses; genomics | Less strict; allows some false positives |
| **Šidák** | α_adjusted = 1 - (1 - α)^(1/k) | When tests are independent | Slightly less conservative than Bonferroni |
| **Permutation-based** | Uses data-driven null distribution | When test statistics are correlated | Computationally intensive; best for complex designs |

### 3.3 Practical Decision Rules

**Confirmatory analyses with few tests (k < 6):**
- Use Holm-Bonferroni (better power than Bonferroni, valid for all dependency structures)

**Confirmatory analyses with many tests (k ≥ 6):**
- Use Benjamini-Hochberg FDR at q = .05 (controls expected proportion of false discoveries)

**Exploratory analyses:**
- Report uncorrected p-values with FDR q-values alongside
- Clearly label as exploratory
- Do not make strong claims based on exploratory findings

**Pre-registered primary outcomes:**
- If only one primary outcome was pre-registered, no correction is needed for that test
- Corrections apply to secondary and exploratory outcomes

### 3.4 What NOT to Correct

You do not need to correct for:
- A single pre-registered primary hypothesis test
- Tests of different hypotheses that are conceptually independent (though statistical independence should be verified)
- Assumption checks and diagnostic tests
- Sensitivity analyses that test the robustness of a single finding

---

## SECTION 4: EFFECT SIZE REPORTING STANDARDS

### 4.1 Required Effect Sizes by Test

| Test | Effect Size | Interpretation | Reporting Format |
|------|------------|---------------|-----------------|
| t-test (independent) | Cohen's d | Small = 0.2, Medium = 0.5, Large = 0.8 | d = [VALUE], 95% CI [LL, UL] |
| t-test (paired) | Cohen's d_z | Same as above (use within-subjects formula) | d_z = [VALUE], 95% CI [LL, UL] |
| ANOVA | Partial η² | Small = .01, Medium = .06, Large = .14 | η²_p = [VALUE], 90% CI [LL, UL] |
| Correlation | r | Small = .10, Medium = .30, Large = .50 | r = [VALUE], 95% CI [LL, UL] |
| Regression | f² | Small = .02, Medium = .15, Large = .35 | f² = [VALUE] |
| Chi-square | Cramér's V | Small = .10, Medium = .30, Large = .50 | V = [VALUE] |
| Logistic regression | Odds ratio | OR = 1.5 (small), 2.5 (medium), 4.3 (large) | OR = [VALUE], 95% CI [LL, UL] |
| Mediation | a × b (indirect effect) | Context-dependent | ab = [VALUE], 95% CI [LL, UL] |

### 4.2 Confidence Intervals for Effect Sizes

**Always report confidence intervals for effect sizes.** Point estimates without CIs are incomplete.

**CI interpretation:**
- A 95% CI means: If we repeated the study infinitely, 95% of the CIs would contain the true effect size
- It does NOT mean: There is a 95% probability the true effect size is in this interval (that's a Bayesian credible interval)

**If the CI includes zero (or the null value):** The effect is not statistically significant at α = .05, AND the data are consistent with a range of possible effect sizes. Report the full range and discuss its implications.

**If the CI is very wide:** The study is underpowered for this effect size. The data are consistent with both trivial and meaningful effects. Report this limitation explicitly.

---

## SECTION 5: CONFIDENCE INTERVAL INTERPRETATION

### 5.1 Six-Step Interpretation Protocol

1. **State the point estimate:** "The effect size was d = 0.42"
2. **State the confidence interval:** "95% CI [0.12, 0.72]"
3. **Assess whether the null is excluded:** "The CI excludes zero, indicating statistical significance at α = .05"
4. **Assess the range of plausible values:** "The data are consistent with effect sizes ranging from small (d = 0.12) to medium-large (d = 0.72)"
5. **Evaluate practical/theoretical significance:** "Even the lower bound (d = 0.12) would be [practically meaningful / trivial] because [JUSTIFICATION]"
6. **Compare to prior estimates:** "This CI overlaps with / excludes the meta-analytic estimate of d = 0.30 (Smith et al., 2020)"

### 5.2 Common Misinterpretations to Avoid

| Misinterpretation | Correction |
|-------------------|-----------|
| "There is a 95% probability the true effect is in this interval" | 95% of such intervals contain the true effect; this specific interval either does or does not |
| "Effects outside the CI are impossible" | Effects outside the CI are less compatible with the data but not impossible |
| "Overlapping CIs mean no significant difference" | CI overlap is not equivalent to a significance test; calculate the difference directly |
| "A wide CI means the effect is unreliable" | A wide CI means the effect size estimate is imprecise; the effect may be real but the study lacked precision |
| "If the CI includes zero, the effect is zero" | Absence of evidence is not evidence of absence; the data are consistent with a range of values including zero |

---

## SECTION 6: BAYESIAN VS. FREQUENTIST APPROACHES

### 6.1 When to Use Each

| Scenario | Recommended Approach | Rationale |
|----------|---------------------|-----------|
| Standard confirmatory hypothesis testing | Frequentist (with pre-registration) | Established norms; clear decision rules |
| Evaluating evidence for the null hypothesis | Bayesian (BF₀₁) | Frequentist methods cannot quantify evidence for the null |
| Sequential data collection | Bayesian (with appropriate priors) | Bayesian analysis does not require fixed sample sizes |
| Incorporating prior knowledge | Bayesian | Priors formally incorporate existing knowledge |
| Multiple comparisons | Bayesian (with hierarchical models) | Natural shrinkage reduces false discoveries |
| Small sample research | Bayesian (with informative priors) | Priors stabilize estimates when data are sparse |
| Regulatory/clinical trials | Frequentist (mandated by regulators) | Regulatory requirements |

### 6.2 Bayes Factor Interpretation

| BF₁₀ | Evidence Category | Interpretation |
|-------|------------------|----------------|
| > 100 | Extreme evidence for H₁ | Overwhelming support for the alternative |
| 30–100 | Very strong evidence for H₁ | Very strong support |
| 10–30 | Strong evidence for H₁ | Strong support |
| 3–10 | Moderate evidence for H₁ | Meaningful support |
| 1–3 | Anecdotal evidence for H₁ | Not worth more than a bare mention |
| 1 | No evidence | Data do not distinguish H₁ from H₀ |
| 1/3–1 | Anecdotal evidence for H₀ | Not worth more than a bare mention |
| 1/10–1/3 | Moderate evidence for H₀ | Meaningful support for the null |
| 1/30–1/10 | Strong evidence for H₀ | Strong support for the null |

### 6.3 Practical Recommendation
For most research, report both frequentist (p-value, CI) and Bayesian (Bayes Factor, posterior) results. This allows readers with different statistical philosophies to evaluate the evidence. When results agree across approaches, confidence increases.

---

## SECTION 7: MISSING DATA HANDLING STRATEGIES

### 7.1 Missing Data Mechanisms

| Mechanism | Definition | Probability of Missingness | Appropriate Method |
|-----------|-----------|---------------------------|-------------------|
| **MCAR** (Missing Completely at Random) | Missingness unrelated to any variable | Same for all observations | Listwise deletion (unbiased but loses power); MI preferred |
| **MAR** (Missing at Random) | Missingness related to observed variables but not unobserved | Depends on observed data only | Multiple imputation; Full information maximum likelihood |
| **MNAR** (Missing Not at Random) | Missingness related to the missing value itself | Depends on unobserved data | Pattern-mixture models; selection models; sensitivity analysis |

### 7.2 Methods Comparison

| Method | Assumption | Bias | Efficiency | Recommendation |
|--------|-----------|------|-----------|---------------|
| **Listwise deletion** | MCAR | Unbiased if MCAR; biased otherwise | Low (discards data) | Only if MCAR and missingness < 5% |
| **Pairwise deletion** | MCAR | Same as listwise | Higher than listwise | Only for correlation matrices; dangerous for complex analyses |
| **Mean imputation** | MCAR | Biased (underestimates variance) | Artificially high | Never use |
| **Last observation carried forward** | MCAR | Biased (assumes no change) | Artificially high | Never use |
| **Multiple imputation (MI)** | MAR | Unbiased if MAR | High | Recommended for MAR data |
| **Full information ML (FIML)** | MAR | Unbiased if MAR | High | Recommended for SEM/longitudinal models |
| **Pattern-mixture models** | MNAR | Depends on assumptions | Moderate | Use for sensitivity analysis under MNAR |

### 7.3 Multiple Imputation Protocol

1. **Include all analysis variables** plus auxiliary variables (variables correlated with missingness or the missing variable)
2. **Use appropriate imputation model:** Predictive mean matching for continuous; logistic for categorical; multinomial for multi-category
3. **Generate m imputations:** m = 20–100 (more is better; m = 5 is too few for modern standards)
4. **Analyze each imputed dataset** using the planned analysis model
5. **Pool results** using Rubin's rules (combined estimate, within- and between-imputation variance)

---

## SECTION 8: OUTLIER DETECTION AND HANDLING

### 8.1 Detection Methods

| Method | Univariate | Multivariate | Assumption | Recommended For |
|--------|-----------|-------------|-----------|----------------|
| **Z-score (|z| > 3.29)** | ✓ | | Normal distribution | Initial screening |
| **IQR method (1.5×IQR)** | ✓ | | No distribution assumption | Non-normal distributions |
| **Mahalanobis distance** | | ✓ | Multivariate normal | Detecting multivariate outliers |
| **Cook's distance** | | ✓ | Regression model | Influential cases in regression |
| **Leverage** | | ✓ | Regression model | High-leverage observations |
| **DFBETAS** | | ✓ | Regression model | Case influence on individual coefficients |

### 8.2 Handling Decision Tree

```
Is the outlier a data error?
├─ YES → Correct or delete with documentation
└─ NO ↓
    Is the outlier a legitimate extreme value?
    ├─ YES → Retain; consider robust methods or transformations
    └─ NO (ambiguous) ↓
        Does the outlier change the conclusions?
        ├─ YES → Report with and without; discuss sensitivity
        └─ NO → Retain; no action needed
```

### 8.3 Rules for Outlier Handling
1. **Never remove outliers based on their effect on p-values** (this is p-hacking)
2. **Pre-register outlier handling rules** when possible
3. **Always report** how many outliers were identified, by what method, and what was done
4. **Conduct sensitivity analysis** — analyze with and without outliers and report both
5. **Consider robust methods** (M-estimators, bootstrapping) instead of deletion

---

## SECTION 9: ASSUMPTION CHECKING PROCEDURES

### 9.1 Assumptions by Test

| Test | Normality | Homogeneity of Variance | Independence | Linearity | Other |
|------|-----------|------------------------|-------------|-----------|-------|
| Independent t-test | n ≥ 30: robust; otherwise check | Welch's t if violated | Design-dependent | N/A | — |
| ANOVA | n ≥ 30 per cell: robust | Levene's test; Welch's ANOVA if violated | Design-dependent | N/A | Sphericity (repeated measures) |
| Pearson r | Bivariate normality | N/A | Independent observations | Linear relationship | No outliers |
| Regression | Residual normality | Residual homoscedasticity | No autocorrelation | Linear relationships | No multicollinearity (VIF < 10) |
| Chi-square | Expected freq ≥ 5 per cell | N/A | Independent observations | N/A | — |
| MANOVA | Multivariate normality | Box's M test | Design-dependent | Linear relationships | — |

### 9.2 What to Do When Assumptions Are Violated

| Assumption Violated | Mild Violation | Severe Violation |
|--------------------|----------------|------------------|
| Normality | Proceed (most tests are robust with n ≥ 30) | Use nonparametric test or bootstrap |
| Homogeneity of variance | Use Welch's correction | Use robust methods or bootstrap |
| Independence | Use mixed models or GEE | Redesign the study |
| Linearity | Use polynomial or nonlinear terms | Use nonlinear model |
| Sphericity | Use Greenhouse-Geisser correction | Use multivariate approach (MANOVA) |
| Multicollinearity | Remove or combine collinear predictors | Use ridge regression or PCA |

---

## SECTION 10: REPRODUCIBILITY CHECKLIST

### Statistical Reproducibility Checklist

- [ ] All analyses were pre-registered (or deviations are documented and justified)
- [ ] The analysis code is available and produces the reported results when run on the data
- [ ] All data exclusions are documented with reasons
- [ ] The primary outcome is the one that was pre-registered
- [ ] All analyses (including non-significant ones) are reported
- [ ] Effect sizes are reported with confidence intervals for all primary analyses
- [ ] Assumption checks were conducted and violations are documented
- [ ] Multiple comparison corrections are applied to confirmatory analyses
- [ ] Missing data handling is documented and justified
- [ ] Outlier handling is documented and sensitivity analyses are reported
- [ ] The exact p-values are reported (not just p < .05)
- [ ] Descriptive statistics (M, SD, n) are reported for all variables
- [ ] The software, version, and packages used are specified
- [ ] The analysis script is commented and readable
- [ ] A reproducibility check was performed (someone else ran the code and got the same results)
