# Statistical Analysis Engine Prompt

## Purpose
This document provides a comprehensive decision framework for selecting and executing statistical analyses. Use this as a step-by-step guide from research question to analysis execution, ensuring appropriate test selection, assumption verification, and robustness checking.

---

## 1. Analysis Decision Tree

### Step 1: Classify Your Research Question

| Question Type | Example | Analysis Family |
|---|---|---|
| Difference between groups | Does treatment X differ from control? | Comparison tests |
| Association between variables | Is X related to Y? | Correlation / regression |
| Prediction | Can X predict Y? | Regression / ML |
| Group membership | What distinguishes group A from B? | Classification / discriminant |
| Structure / Latent factors | What underlying dimensions explain these items? | Factor analysis / SEM |
| Change over time | Does Y change across time points? | Longitudinal / time series |
| Mediation | Does X affect Y through M? | Mediation analysis |
| Moderation | Does the X→Y relationship depend on W? | Moderation / interaction |
| Equivalence | Are X and Y practically equivalent? | Equivalence / TOST |
| Dose-response | Does more X lead to more Y? | Trend / dose-response |

### Step 2: Characterize Your Data

| Characteristic | Options | Impact on Analysis |
|---|---|---|
| DV type | Continuous, ordinal, categorical, count, time-to-event | Determines test family |
| IV type | Continuous, categorical (2 levels), categorical (3+ levels) | Determines test structure |
| IV relationship | Between-subjects, within-subjects, mixed | Determines error term |
| Sample size | Small (N<30), moderate (30-200), large (200+) | Affects power and test choice |
| Distribution | Normal, skewed, heavy-tailed, multimodal | Parametric vs non-parametric |
| Observations | Independent, paired, clustered, repeated | Determines model complexity |
| Missing data | MCAR, MAR, MNAR | Determines imputation strategy |

### Step 3: Select Analysis Path

```
START: What is your DV?
│
├── Continuous
│   ├── 1 IV, 2 groups, between → Independent t-test (or Mann-Whitney U)
│   ├── 1 IV, 2 groups, within → Paired t-test (or Wilcoxon signed-rank)
│   ├── 1 IV, 3+ groups, between → One-way ANOVA (or Kruskal-Wallis)
│   ├── 1 IV, 3+ groups, within → Repeated measures ANOVA (or Friedman)
│   ├── 2+ IVs, between → Factorial ANOVA
│   ├── 2+ IVs, mixed → Mixed ANOVA / Linear mixed model
│   ├── 1+ continuous IVs → Linear regression
│   ├── Nested/clustered → Multilevel model
│   └── Repeated measures, many time points → Growth curve / LMM
│
├── Binary/Categorical
│   ├── 2×2 table → Chi-square / Fisher's exact
│   ├── R×C table → Chi-square test of independence
│   ├── Predicting binary outcome → Logistic regression
│   ├── Predicting nominal outcome → Multinomial logistic regression
│   ├── Predicting ordinal outcome → Ordinal logistic regression
│   └── Paired categorical → McNemar's test
│
├── Count
│   ├── Simple count DV → Poisson regression
│   ├── Overdispersed count → Negative binomial regression
│   └── Excess zeros → Zero-inflated or hurdle model
│
├── Time-to-Event
│   ├── Standard → Cox proportional hazards
│   ├── Non-proportional hazards → Extended Cox with time interactions
│   ├── Competing risks → Fine-Gray subdistribution model
│   └── Recurrent events → Andersen-Gill / WLW models
│
└── Ordinal
    ├── 2 groups → Mann-Whitney U
    ├── 3+ groups → Kruskal-Wallis
    ├── With covariates → Ordinal logistic regression
    └── Repeated → Friedman test or cumulative mixed model
```

---

## 2. Parametric vs Non-Parametric Test Selection

### Decision Framework

| Criterion | Parametric | Non-Parametric |
|---|---|---|
| Distribution | Normal or near-normal | Any (distribution-free) |
| Scale | Interval/ratio | Ordinal or any |
| Sample size | N ≥ 30 per group (Central Limit Theorem) | Any N, especially small |
| Outliers | Robust with moderate outliers | Robust to extreme outliers |
| Power | Higher when assumptions met | Lower (5-15% efficiency loss) |
| Information | Uses all data (means, variances) | Uses ranks only |

### Assumption Checklist for Parametric Tests

1. **Normality**: Shapiro-Wilk test (N < 50) or Kolmogorov-Smirnov (N ≥ 50), visual Q-Q plot
   - Moderate violations acceptable with N > 30 per group (CLT)
   - Severe skew: Consider transformation or non-parametric

2. **Homogeneity of variance**: Levene's test (between-subjects)
   - If violated: Welch's t-test, Welch's ANOVA, or Brown-Forsythe

3. **Sphericity**: Mauchly's test (repeated measures)
   - If violated: Greenhouse-Geisser (ε < 0.75) or Huynh-Feldt (ε ≥ 0.75)

4. **Independence**: Design-based (verify, do not test)
   - If violated: Use mixed models with random effects

5. **Linearity**: Residual plots for regression
   - If violated: Polynomial terms, splines, or non-linear models

6. **Homoscedasticity**: Breusch-Pagan or White test (regression)
   - If violated: Robust standard errors (HC0-HC5) or WLS

### When to Prefer Non-Parametric
- Small samples (N < 15 per group) with non-normal distributions
- Ordinal data with few categories
- Severe outliers that cannot be legitimately removed
- When the hypothesis is about medians or distributions, not means
- When distribution shape itself is of interest

---

## 3. Regression Model Selection Framework

### Selection by Outcome Type

| Outcome | Model | Key Assumptions | Diagnostics |
|---|---|---|---|
| Continuous | OLS Linear Regression | Linearity, normality of residuals, homoscedasticity | Residual plots, VIF, Q-Q |
| Binary | Logistic Regression | Linearity of logit, no perfect separation | Hosmer-Lemeshow, ROC/AUC |
| Ordinal | Ordinal Logistic | Proportional odds assumption | Brant test |
| Count (rare) | Poisson | Mean = variance | Dispersion test |
| Count (common) | Negative Binomial | Overdispersion parameter | Compare to Poisson |
| Survival | Cox PH | Proportional hazards | Schoenfeld residuals |
| Zero-inflated count | ZIP / ZINB | Two-process data generation | Vuong test vs standard |
| Continuous, bounded | Beta Regression | (0,1) bounded outcome | Residual analysis |
| Multivariate | MANOVA / MV Regression | MV normality, homogeneity | Box's M test |

### Model Building Strategy (Top-Down)

1. **Start with theory**: Enter all variables justified by prior research
2. **Check multicollinearity**: VIF < 5 (strict) or < 10 (lenient); if violated, consider combining or removing collinear predictors
3. **Assess model fit**: R², adjusted R², AIC, BIC
4. **Residual diagnostics**: Plot residuals vs fitted, Q-Q plot, leverage/cook's distance
5. **Sensitivity**: Remove cases with Cook's D > 4/N, re-run, compare
6. **Report**: Full model with all theoretically motivated variables; do not report stepwise results as if they were confirmatory

### Model Comparison

| Approach | Use When | Method |
|---|---|---|
| Nested models | Comparing simpler vs complex | Likelihood ratio test (LRT) |
| Non-nested models | Different predictors | AIC / BIC comparison |
| Many candidate models | Model uncertainty | Information-theoretic (AICc weights) |
| Pre-registered model | Confirmatory analysis | Report single model, no selection |
| Exploratory | Many predictors, small N | Elastic net or LASSO (with cross-validation) |

---

## 4. Mediation and Moderation Analysis Procedures

### Simple Mediation (X → M → Y)

**Baron & Kenny Steps (historical, now supplementary):**
1. X significantly predicts Y (total effect, path c)
2. X significantly predicts M (path a)
3. M significantly predicts Y controlling for X (path b)
4. The X→Y relationship is reduced when M is included (path c')

**Modern Approach (Preferred):**
- Use bootstrap confidence intervals for the indirect effect (ab)
- Hayes PROCESS Model 4 or structural equation modeling
- Report: indirect effect (ab), bootstrap SE, 95% CI, direct effect (c'), total effect (c)
- 5,000+ bootstrap samples; bias-corrected CIs recommended
- The total effect (path c) need NOT be significant for mediation to exist

**Reporting template:**
"We tested whether [M] mediated the relationship between [X] and [Y] using a bootstrap mediation analysis (5,000 samples). The indirect effect of [X] on [Y] through [M] was [significant/not significant], ab = X.XX, 95% CI [X.XX, X.XX]. The direct effect of [X] on [Y] controlling for [M] was [significant/not significant], c' = X.XX, p = .XXX."

### Moderation (X × W → Y)

**Procedure:**
1. Mean-center continuous predictors (reduces multicollinearity, aids interpretation)
2. Create interaction term: X × W
3. Enter in hierarchical regression:
   - Step 1: Main effects (X, W)
   - Step 2: Interaction term (X × W)
4. If ΔR² significant: Probing required
5. Probe with simple slopes at W = -1SD, M, +1SD (or Johnson-Neyman technique for continuous moderators)
6. Plot interaction with simple slope lines and 95% CIs

**Reporting template:**
"A hierarchical multiple regression tested whether [W] moderated the relationship between [X] and [Y]. The interaction term accounted for significant additional variance, ΔR² = .XX, ΔF(X, XX) = X.XX, p = .XXX. Simple slopes analysis revealed that [X] significantly predicted [Y] when [W] was [high (+1SD), b = X.XX, p = .XXX / at the mean, b = X.XX, p = .XXX / low (-1SD), b = X.XX, p = .XXX]."

### Moderated Mediation (Conditional Indirect Effects)

- Hayes PROCESS Model 7 (first-stage), Model 14 (second-stage), Model 8 (both stages), Model 59 (all paths)
- Report the index of moderated mediation with bootstrap CI
- If the CI does not include zero, moderated mediation is present

---

## 5. Multilevel / Mixed Effects Modeling Guide

### When to Use Multilevel Models

- Data are nested (students within schools, patients within clinics, observations within persons)
- Intraclass correlation (ICC) > .05 justifies multilevel approach
- Repeated measures with unequal time points or missing data
- Cross-classified data (students nested in schools AND neighborhoods)

### Model Building Sequence

1. **Null model (intercept-only):** Y_ij = γ₀₀ + u₀ⱼ + e_ij
   - Calculate ICC = u₀ⱼ variance / (u₀ⱼ variance + e_ij variance)
   - If ICC < .05, consider fixed-effects (single-level) model

2. **Random intercept model:** Add Level 1 predictors
   - Y_ij = γ₀₀ + γ₁₀X_ij + u₀ⱼ + e_ij
   - Test whether Level 1 predictors significantly predict outcome

3. **Random slope model:** Allow predictor effects to vary across clusters
   - Y_ij = γ₀₀ + γ₁₀X_ij + u₀ⱼ + u₁ⱼX_ij + e_ij
   - Compare with LRT: Is variance in slope significant?

4. **Cross-level interactions:** Add Level 2 predictors of slopes
   - Y_ij = γ₀₀ + γ₁₀X_ij + γ₀₁W_j + γ₁₁X_ij × W_j + u₀ⱼ + u₁ⱼX_ij + e_ij
   - Interpret γ₁₁ as the effect of cluster-level W on the X→Y relationship

### Key Decisions

| Decision | Options | Recommendation |
|---|---|---|
| Estimation method | REML vs ML | REML for final model; ML for model comparison (LRT) |
| Degrees of freedom | Satterthwaite, Kenward-Roger, PB | Kenward-Roger for small samples |
| Random effects structure | Maximal vs parsimonious | Start maximal; simplify if convergence fails; report what was tried |
| Centering | Grand mean vs cluster mean | Cluster-mean centering for Level 1 effects; grand mean for Level 2 |
| Missing data | Complete case vs FIML | FIML preferred (assumes MAR); multiple imputation as alternative |

### Reporting Essentials

- ICC from null model
- Variance components at each level (with confidence intervals)
- Fixed effects with standard errors, t/z values, p-values, CIs
- Random effects variances (and correlations if slopes are random)
- Model comparison statistics (AIC, BIC, LRT χ²)
- R² measures: Marginal R² (fixed effects only) and Conditional R² (fixed + random)

---

## 6. Time Series Analysis Procedures

### Pre-Analysis Requirements

1. **Stationarity check**: Augmented Dickey-Fuller test, KPSS test
   - If non-stationary: First-difference or detrend
   - If seasonal: Seasonal differencing or decomposition

2. **Autocorrelation analysis**: ACF and PACF plots
   - Identify AR and MA components from ACF/PACF patterns

3. **Structural breaks**: Chow test, Bai-Perron test
   - If breaks exist: Segment analysis or regime-switching models

### Model Selection

| Pattern | Model | Identification |
|---|---|---|
| AR signature | AR(p) | PACF cuts off after lag p; ACF tails off |
| MA signature | MA(q) | ACF cuts off after lag q; PACF tails off |
| ARMA signature | ARMA(p,q) | Both ACF and PACF tail off |
| Trend + ARMA | ARIMA(p,d,q) | Differencing needed (d times) |
| Seasonal pattern | SARIMA(p,d,q)(P,D,Q)_s | Seasonal ACF/PACF patterns |
| Exogenous predictors | ARIMAX / SARIMAX | Include external predictors |
| Time-varying variance | GARCH(p,q) | Volatility clustering in residuals |
| Latent states | HMM / State-space | Unobserved regime changes |

### Forecasting Validation

- Train-test split: Use 70-80% for training, 20-30% for testing
- Walk-forward validation for time series (no random cross-validation)
- Metrics: RMSE, MAE, MAPE, MASE
- Compare to naive benchmarks (random walk, seasonal naive)
- Report prediction intervals, not just point forecasts

---

## 7. Machine Learning Analysis Frameworks

### When ML Is Appropriate

- Prediction is the goal (not explanation)
- Many potential predictors with unknown relevance
- Complex, non-linear relationships suspected
- Sufficient sample size (minimum: 10-20 observations per feature for regularization methods; much more for deep learning)

### Supervised Learning Framework

| Component | Options | Selection Criteria |
|---|---|---|
| Algorithm | LASSO, Random Forest, XGBoost, SVM, Neural Net | Data size, linearity, interpretability needs |
| Validation | k-fold CV, nested CV, LOOCV | Sample size, computational cost |
| Preprocessing | Standardization, normalization, PCA | Algorithm requirements |
| Feature selection | LASSO, Boruta, RFE, domain knowledge | Interpretability vs accuracy trade-off |
| Hyperparameter tuning | Grid search, random search, Bayesian | Computational budget |
| Evaluation | Accuracy, F1, AUC, RMSE, MAE | Problem type and class balance |

### Reporting Standards for ML in Research

1. **Dataset description**: N, number of features, class distribution
2. **Preprocessing pipeline**: Every transformation step documented
3. **Feature engineering**: All derived features explained
4. **Model selection**: Algorithms compared and selection justified
5. **Hyperparameter values**: Final values reported with search ranges
6. **Validation strategy**: k, folds, stratification, random seed
7. **Performance metrics**: Multiple metrics on held-out test set
8. **Baseline comparison**: Comparison to simple/heuristic models
9. **Feature importance**: Which features drive predictions
10. **Reproducibility**: Code and data availability statement

### Common Pitfalls

- **Data leakage**: Test data information leaking into training (e.g., scaling before splitting)
- **Overfitting**: Model memorizing noise; detect with train-test gap
- **P-hacking analog**: Trying many algorithms and reporting only the best
- **Class imbalance**: Accuracy is misleading; use F1, AUC, or balanced accuracy
- **Temporal leakage**: Future data used to predict past (in time series)

---

## 8. Bayesian Analysis Guidelines

### When to Use Bayesian Methods

- Small sample sizes where frequentist methods are underpowered
- Prior information exists that should be formally incorporated
- You want to make probability statements about parameters (not just data)
- Model comparison with unequal complexity
- Hierarchical models with partial pooling

### Prior Selection

| Prior Type | When to Use | Example |
|---|---|---|
| Informative | Strong prior evidence exists | N(μ_prior, σ²_prior) from meta-analysis |
| Weakly informative | Constrain to plausible ranges | N(0, 10²) for standardized effects |
| Default/Reference | No prior information | Cauchy(0, 0.707) for standardized effects (BayesFactor default) |
| Improper flat | Avoid unless necessary | Uniform(-∞, +∞) — use with caution |

### Reporting Bayesian Results

1. **Posterior distribution**: Report median/MAP and 95% credible interval (HDI)
2. **Bayes Factor**: Report BF₁₀ and interpret on Jeffreys scale
   - BF₁₀ = 1-3: Anecdotal evidence for H₁
   - BF₁₀ = 3-10: Moderate evidence for H₁
   - BF₁₀ = 10-30: Strong evidence for H₁
   - BF₁₀ = 30-100: Very strong evidence for H₁
   - BF₁₀ > 100: Extreme evidence for H₁
3. **Prior sensitivity**: Report results under at least two prior specifications
4. **MCMC diagnostics**: R̂ < 1.01, effective sample size > 400, trace plots inspected
5. **Model comparison**: WAIC, LOO-CV for comparing models

---

## 9. Sensitivity Analysis Protocols

### Types of Sensitivity Analysis

| Type | Purpose | Procedure |
|---|---|---|
| Assumption sensitivity | Test impact of violated assumptions | Re-run under alternative assumptions |
| Exclusion sensitivity | Test impact of outlier decisions | Re-run with/without outliers; with/without trimming |
| Covariate sensitivity | Test impact of covariate selection | Re-run with different covariate sets |
| Model specification | Test impact of functional form | Linear vs quadratic vs spline |
| Measurement sensitivity | Test impact of operationalization | Alternative measures of same construct |
| Missing data sensitivity | Test impact of missing data handling | Complete case vs MI vs FIML; pattern-mixture models for MNAR |
| Threshold sensitivity | Test impact of arbitrary cutpoints | Vary cutpoints and re-analyze |
| Subgroup sensitivity | Test robustness across subgroups | Re-run within demographic subgroups |

### Quantifying Sensitivity

- **E-value**: Minimum strength of unmeasured confounder needed to explain away an effect
  - E-value = RR + √[RR × (RR - 1)] for risk ratios
  - Report for every causal claim

- **Fragility index**: Number of event reclassifications needed to change significance
  - Particularly important for small RCTs

- **Robustness value (R²)**: Proportion of variance an unmeasured confounder would need to explain to eliminate the effect

---

## 10. Robustness Check Taxonomy

### Tier 1: Essential (Always Report)

1. **Alternative model specifications**: At least one alternative functional form
2. **Covariate adjustment**: Results with and without key covariates
3. **Sample exclusions**: Results with and without outliers/sensitive cases
4. **Missing data handling**: Results under alternative missing data assumptions

### Tier 2: Recommended (Report When Possible)

5. **Alternative estimators**: OLS vs robust regression; ML vs REML
6. **Subgroup analysis**: Results broken down by key demographic variables
7. **Placebo tests**: Test the hypothesis where the effect should not exist
8. **Pre-registration compliance**: Report any deviations from pre-registered plan
9. **Multiple comparison correction**: Bonferroni, FDR, or Holm corrections applied

### Tier 3: Comprehensive (For High-Stakes Claims)

10. **Design-based placebo**: Apply same analysis to control group only
11. **Permutation tests**: Empirical null distribution for exact inference
12. **Bootstrap validation**: Stability of results across bootstrap samples
13. **Specification curve analysis**: Run all reasonable specifications, plot distribution of results
14. **Multi-method triangulation**: Address same question with different methodological approaches
15. **External validation**: Test key findings in independent dataset

### Reporting Template

"We conducted the following robustness checks on our primary findings:

1. **Alternative model specification**: [Describe alternative; report result; note if conclusion changes]
2. **Covariate adjustment**: [Describe alternative covariate set; report result]
3. **Outlier sensitivity**: [Describe alternative treatment; report result]
4. **Missing data**: [Describe alternative handling; report result]

[Primary finding] was robust across [X of Y] sensitivity analyses. The conclusion changed when [specific condition], suggesting [interpretation of boundary condition]."

---

## Quick Reference: Analysis Selection by Design

| Design | Primary Analysis | Secondary / Robustness | Effect Size |
|---|---|---|---|
| RCT, 2 groups | Independent t-test / ANCOVA | Mann-Whitney; bootstrap CI | Cohen's d; η²_p |
| RCT, 3+ groups | One-way ANOVA + planned contrasts | Kruskal-Wallis; Welch ANOVA | η²; pairwise d with correction |
| Pre-post design | Paired t-test | Wilcoxon;bootstrap mean diff | d_z; within-subject η² |
| Factorial RCT | Factorial ANOVA | Linear model with interaction | η²_p for each effect |
| Correlational | Multiple regression | Robust regression; bootstrap | R²; standardized β |
| Longitudinal | Mixed effects model | GEE; alternative covariance | Marginal/conditional R² |
| Mediation | Bootstrap mediation | Sensitivity to omitted confounders | ab with CI; κ² |
| Moderation | Hierarchical regression with interaction | Johnson-Neyman; simple slopes | ΔR²; region of significance |
| Observational causal | Propensity score matching + outcome model | Multiple PS methods; IV if available | ATT/ATE with CI; E-value |
