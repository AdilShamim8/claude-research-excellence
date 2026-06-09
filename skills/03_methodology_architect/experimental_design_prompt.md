# Experimental Design Prompt

## A Comprehensive Decision Framework for Selecting and Implementing Research Designs

### Purpose
This prompt provides a structured decision process for choosing and implementing the optimal research design for any empirical study. It covers experimental, quasi-experimental, observational, survey, qualitative, and mixed methods designs, with detailed specifications for each including sample size requirements and validity threats.

---

## SECTION 1: DESIGN SELECTION DECISION TREE

### Step 1: Determine Your Causal Claim

```
What claim do you want to make?
│
├─ "X causes Y" → Go to Step 2 (Experimental designs)
├─ "X likely causes Y, but I can't randomize" → Go to Step 3 (Quasi-experimental)
├─ "X is associated with Y" → Go to Step 4 (Observational)
├─ "The prevalence/nature of X is..." → Go to Step 5 (Survey/Descriptive)
├─ "How do people experience X?" → Go to Step 6 (Qualitative)
└─ "I need both breadth and depth" → Go to Step 7 (Mixed methods)
```

### Step 2: Can You Randomly Assign Participants to Conditions?

```
YES → Experimental Designs (Section 2)
├─ Can you assign individuals? → Parallel RCT
├─ Must you assign groups? → Cluster RCT
├─ Can participants serve as their own control? → Crossover RCT
└─ Do you want to test multiple factors? → Factorial RCT

NO (but treatment occurs) → Quasi-Experimental Designs (Section 3)
├─ Is there a clear cutoff for treatment? → Regression Discontinuity
├─ Are there before-and-after comparisons? → Difference-in-Differences
├─ Is there a natural instrument? → Instrumental Variables
└─ Is the treatment at the group level? → Synthetic Control
```

### Step 3: Can You Manipulate the Independent Variable?

```
NO (you can only observe) → Observational Designs (Section 4)
├─ Can you follow people forward in time? → Cohort Study
├─ Do you need to compare groups defined by outcome? → Case-Control
└─ Do you need a snapshot? → Cross-Sectional
```

---

## SECTION 2: RCT DESIGN TEMPLATES

### 2.1 Parallel Group RCT

**Structure:** Participants randomly assigned to one of two or more conditions; each participant receives only one condition.

**Design Diagram:**
```
R ─── O₁ ─── X ─── O₂    (Treatment group)
R ─── O₁ ─── ─── ─── O₂  (Control group)

R = Random assignment
O = Observation (measurement)
X = Treatment/intervention
```

**When to use:**
- Testing whether an intervention causes a change in an outcome
- You can ethically and practically randomize individuals
- You have a clear control condition

**Key design decisions:**
- **Active vs. passive control:** Active control receives an alternative treatment; passive control receives no treatment or treatment as usual
- **Allocation ratio:** Usually 1:1; can be unequal (e.g., 2:1) if treatment is scarce or expensive
- **Stratified randomization:** Stratify by prognostic variables (e.g., severity, site) to ensure balance
- **Block randomization:** Use blocks to ensure approximately equal group sizes throughout recruitment

**Sample size calculation:**
```
For two-group comparison (continuous outcome):
N per group = 2 × [(z_α/2 + z_β) / d]²

Where:
d = Cohen's d (standardized effect size)
z_α/2 = 1.96 for α = .05 (two-tailed)
z_β = 0.84 for 1-β = .80

For d = 0.5: N per group ≈ 64
For d = 0.3: N per group ≈ 176
For d = 0.8: N per group ≈ 26
```

**Threats to validity:**
- Differential attrition (mitigate with intent-to-treat analysis)
- Failure of randomization to achieve balance (mitigate with stratification and covariate adjustment)
- Non-compliance (mitigate with encouragement designs and CACE estimation)

---

### 2.2 Crossover RCT

**Structure:** Each participant receives both conditions in a random order, separated by a washout period.

**Design Diagram:**
```
R ─── O₁ ─── X_A ─── O₂ ─── [Washout] ─── O₃ ─── X_B ─── O₄
R ─── O₁ ─── X_B ─── O₂ ─── [Washout] ─── O₃ ─── X_A ─── O₄
```

**When to use:**
- The intervention effect is temporary (no lasting change)
- A washout period can eliminate carryover effects
- Participant recruitment is difficult (maximizes power per participant)
- Individual differences are large relative to treatment effects

**Critical requirements:**
- **Washout period:** Must be long enough for the treatment effect to return to baseline
- **Carryover test:** Must test for order effects; if present, only the first period data is usable
- **Stable condition:** The underlying condition must not change over the study period

**Sample size calculation:**
```
For crossover design (continuous outcome):
N per sequence = [(z_α/2 + z_β) × σ_d / δ]²

Where:
σ_d = standard deviation of within-pair differences
δ = expected mean difference between treatments

Typically requires 50-75% fewer participants than parallel design
For d = 0.5, r = 0.5: N per sequence ≈ 20
```

**Threats to validity:**
- Carryover effects (most serious threat; mitigate with adequate washout)
- Period effects (systematic changes over time; mitigate with counterbalancing)
- Period-by-treatment interaction (different treatment effects in different periods; fatal if present)
- Unblinding due to recognizable treatment effects

---

### 2.3 Cluster RCT

**Structure:** Groups (clusters) rather than individuals are randomly assigned to conditions. All individuals within a cluster receive the same condition.

**Design Diagram:**
```
Cluster 1 (R) ─── X_A ─── All members measured
Cluster 2 (R) ─── X_B ─── All members measured
Cluster 3 (R) ─── X_A ─── All members measured
...
```

**When to use:**
- Individual randomization is impractical (e.g., school-based interventions)
- Treatment contamination between conditions is likely with individual assignment
- The intervention naturally operates at the group level (e.g., policy changes)

**Sample size calculation:**
```
N_effective = N_simple × [1 + (m - 1) × ICC]

Where:
N_simple = sample size from simple randomization formula
m = average cluster size
ICC = intraclass correlation coefficient

Design effect = 1 + (m - 1) × ICC

Example: If N_simple = 128, m = 20, ICC = 0.05:
Design effect = 1 + 19 × 0.05 = 1.95
N_effective = 128 × 1.95 = 250
Need at least 250/20 ≈ 13 clusters per condition
```

**Threats to validity:**
- ICC inflation: Clustering reduces effective sample size dramatically
- Between-cluster heterogeneity: Clusters may differ on important variables
- Limited number of clusters: Small number of clusters limits degrees of freedom
- Spillover between clusters (mitigate with geographic or temporal separation)

---

### 2.4 Factorial RCT

**Structure:** Two or more independent variables (factors) are manipulated simultaneously, creating all possible combinations of factor levels.

**Design Diagram (2×2):**
```
                Factor B: Present
               ┌────────────────┐
Factor A:      │ Cell 1: A+B    │  Cell 3: B only
Present        │                │
               ├────────────────┤
Factor A:      │ Cell 2: A only │  Cell 4: Neither
Absent         │                │
               └────────────────┘
                    Factor B: Absent
```

**When to use:**
- You want to test the independent and interactive effects of two or more factors
- You want to test whether combining interventions produces additive or synergistic effects
- You want to efficiently test multiple interventions in a single study

**Key design decisions:**
- **Full vs. fractional factorial:** Full tests all combinations; fractional tests a subset when there are many factors
- **Main effects vs. interaction:** The study must be powered for the interaction effect (which requires more participants)
- **Between vs. within factors:** Between-subjects factors require more participants but avoid carryover

**Sample size calculation:**
```
For 2×2 factorial (testing interaction):
N per cell = 4 × [(z_α/2 + z_β) / d_interaction]²

The interaction effect is typically smaller than main effects.
If d_interaction = 0.3: N per cell ≈ 176, Total N ≈ 704
If only testing main effects: N per cell ≈ 44, Total N ≈ 176
```

**Threats to validity:**
- Underpowered interaction tests (most common problem)
- Interpretation difficulty: Is the interaction ordinal (same direction, different magnitude) or disordinal (different directions)?
- Multiple comparison burden if testing many effects

---

## SECTION 3: QUASI-EXPERIMENTAL DESIGNS

### 3.1 Difference-in-Differences (DiD)

**Structure:** Compare changes over time between a treated group and an untreated comparison group.

**Design Diagram:**
```
            Pre-treatment  Post-treatment
Treated:    O₁ ──────────────── O₂
Control:    O₃ ──────────────── O₄

DiD estimate = (O₂ - O₁) - (O₄ - O₃)
```

**When to use:**
- A policy or intervention is introduced for one group but not another
- You have pre- and post-treatment data for both groups
- Random assignment was not possible

**Critical assumption: Parallel trends**
- In the absence of treatment, the treated and control groups would have followed the same trajectory
- Test by examining pre-treatment trends (need at least 3 pre-treatment time points)
- If parallel trends assumption fails, DiD estimates are biased

**Sample size considerations:**
- Need sufficient pre-treatment periods to verify parallel trends (minimum 3)
- Power depends on the number of time points and the variance of the outcome
- Cluster-level DiD (e.g., state-level policy changes) requires many clusters

**Threats to validity:**
- Violation of parallel trends assumption (most serious)
- Anticipation effects (groups change behavior before treatment)
- Ashenfelter's dip (treated group was on a different trajectory before treatment)
- Composition changes (different people in pre and post periods)

---

### 3.2 Regression Discontinuity Design (RDD)

**Structure:** Treatment assignment is determined by whether a running variable crosses a known cutoff.

**Design Diagram:**
```
Outcome
  │        ╱ Treatment group
  │       ╱
  │      ╱
  │─────╳───── Cutoff
  │    ╱
  │   ╱ Control group
  │  ╱
  └──────────── Running variable
```

**When to use:**
- Treatment assignment is based on a cutoff on a continuous variable (e.g., test score above threshold for program eligibility)
- The cutoff is known and sharp (or fuzzy with known compliance rates)

**Critical assumption: Continuity at the cutoff**
- In the absence of treatment, the outcome would be continuous at the cutoff
- Test by examining the density of the running variable (no bunching at the cutoff)
- Use narrow bandwidth around the cutoff for local estimation

**Sample size considerations:**
- Effective sample is observations near the cutoff, not the full sample
- Need dense observations around the cutoff (minimum 100–200 observations within bandwidth)
- Power is typically lower than RCT for the same total N

**Threats to validity:**
- Manipulation of the running variable (people gaming the cutoff)
- Imprecise cutoff assignment (fuzzy RDD)
- Misspecification of the functional form near the cutoff
- Covariate discontinuities at the cutoff (suggests sorting)

---

### 3.3 Instrumental Variables (IV)

**Structure:** Use an instrument Z that affects X but does not directly affect Y (except through X) to estimate the causal effect of X on Y.

**Requirements:**
1. **Relevance:** Z must be strongly correlated with X (F-statistic > 10 in first stage)
2. **Exclusion restriction:** Z affects Y only through its effect on X (untestable)
3. **Independence:** Z is not correlated with unmeasured confounders

**When to use:**
- You have a plausible instrument that affects treatment but not the outcome directly
- Randomization is not possible
- Omitted variable bias is a serious concern

**Sample size considerations:**
- IV estimation is always less efficient than OLS; requires larger samples
- Weak instruments (first-stage F < 10) produce biased and imprecise estimates
- Rule of thumb: N for IV should be at least 2–3× the N needed for RCT

**Threats to validity:**
- Weak instruments (most common problem; produce biased estimates)
- Violation of exclusion restriction (untestable; must be argued theoretically)
- LATE interpretation: IV estimates the local average treatment effect for compliers only, not the ATE
- Over-identification test failure (when multiple instruments disagree)

---

### 3.4 Synthetic Control

**Structure:** Construct a weighted combination of control units that matches the pre-treatment trajectory of the treated unit.

**When to use:**
- A single unit (e.g., a state, country, or organization) receives a treatment
- You have long pre-treatment time series data
- There is no single control unit that is a good match

**Procedure:**
1. Select a pool of potential control units (donor pool)
2. Use pre-treatment outcome and predictor data to find optimal weights
3. Construct synthetic control as weighted average of donor pool units
4. Compare post-treatment outcomes between treated unit and synthetic control
5. Use permutation tests (placebo tests) for inference

**Threats to validity:**
- Poor pre-treatment fit (synthetic control doesn't match treated unit before treatment)
- V-interference (treatment affects control units)
- Choppy or short pre-treatment data
- Overfitting to noise in pre-treatment period

---

## SECTION 4: OBSERVATIONAL DESIGNS

### 4.1 Cohort Study

**Structure:** Follow a group of people forward in time, comparing those exposed vs. not exposed to a risk factor.

**Types:**
- **Prospective:** Recruit participants and follow them forward (expensive, long duration)
- **Retrospective:** Use existing data to look back at exposure and outcomes (faster, limited data)

**When to use:**
- You want to study the natural development of outcomes over time
- Randomization is unethical or impractical (e.g., studying smoking and cancer)
- You need incidence data (new cases over time)

**Sample size considerations:**
- Depends on the expected incidence rate of the outcome
- For rare outcomes, very large samples are needed
- Loss to follow-up reduces effective sample size; plan for 20–30% attrition

**Threats to validity:**
- Confounding (primary threat; address with statistical adjustment)
- Loss to follow-up (differential attrition creates bias)
- Measurement error in exposure assessment
- Healthy worker effect (employed people are healthier than general population)

---

### 4.2 Case-Control Study

**Structure:** Compare people with the outcome (cases) to people without (controls) on their prior exposure.

**When to use:**
- The outcome is rare (cohort study would require enormous sample)
- You need results quickly (retrospective data collection)
- You want to explore multiple potential exposures

**Critical design decisions:**
- **Case definition:** Must be specific and consistently applied
- **Control selection:** Controls must be from the same source population as cases; matched on key variables but not over-matched
- **Matching:** Can match on confounders (individual or frequency matching); do not match on the exposure

**Threats to validity:**
- Recall bias (cases remember exposures differently than controls)
- Selection bias (controls not representative of the source population)
- Confounding (address with matching and statistical adjustment)
- Temporal ambiguity (exposure may not have preceded the outcome)

---

### 4.3 Cross-Sectional Study

**Structure:** Measure exposure and outcome at a single time point.

**When to use:**
- You need prevalence estimates
- You are exploring associations without causal claims
- Resources are limited and quick results are needed

**Threats to validity:**
- Cannot establish temporal precedence (key limitation)
- Survivor bias (only current members of population are observed)
- Prevalence-incidence bias (associations with survival differ from associations with incidence)

---

## SECTION 5: SURVEY AND QUESTIONNAIRE DESIGN

### 5.1 Survey Design Checklist

- [ ] Define the target population and sampling frame
- [ ] Choose sampling method (simple random, stratified, cluster, convenience)
- [ ] Calculate required sample size for desired precision (N ≈ 1/ME² for proportions)
- [ ] Use validated instruments where available; pilot new items
- [ ] Avoid leading, double-barreled, or ambiguous questions
- [ ] Use appropriate response scales (Likert, visual analog, semantic differential)
- [ ] Include attention checks and reverse-coded items
- [ ] Pre-test the survey with 10–20 participants from the target population
- [ ] Plan for non-response bias assessment (compare early vs. late responders)

### 5.2 Questionnaire Validation

**For new measures, conduct:**
1. **Content validity:** Expert review of item relevance and representativeness
2. **Cognitive interviewing:** Ask respondents to think aloud while answering
3. **Pilot testing:** Administer to a small sample; check distributions and reliability
4. **Exploratory factor analysis:** Identify the factor structure (minimum N = 5–10 per item)
5. **Confirmatory factor analysis:** Test the factor structure in an independent sample
6. **Reliability assessment:** Internal consistency (α ≥ .70), test-retest (r ≥ .70)
7. **Validity assessment:** Convergent, discriminant, criterion, and construct validity

---

## SECTION 6: QUALITATIVE AND MIXED METHODS DESIGN

### 6.1 Qualitative Design Types

| Type | Purpose | Sample Size | Data Collection |
|------|---------|------------|-----------------|
| **Phenomenology** | Understand lived experience of a phenomenon | 5–25 | In-depth interviews |
| **Grounded theory** | Develop a theory from data | 20–50 | Interviews, observation |
| **Case study** | In-depth analysis of a bounded case | 1–10 cases | Multiple sources |
| **Ethnography** | Understand culture and social practices | Extended immersion | Observation, interviews |
| **Narrative** | Understand how people construct stories about experiences | 5–15 | Life history interviews |

### 6.2 Mixed Methods Designs

| Type | Structure | When to Use |
|------|-----------|------------|
| **Convergent parallel** | Quant + qual collected simultaneously, analyzed separately, then merged | You want comprehensive understanding from two perspectives |
| **Explanatory sequential** | Quant first, then qual to explain quant findings | Quant results need deeper explanation |
| **Exploratory sequential** | Qual first, then quant to test qual findings | You need to develop and then test hypotheses |
| **Embedded** | One method nested within the other | You need one method to support a primarily different-method study |
| **Multiphase** | Series of studies, each building on the last | Complex research program requiring iterative investigation |

**Integration requirement:** Mixed methods must integrate findings, not merely present quant and qual side by side. Specify how findings from each method will be combined (triangulation, complementarity, development, initiation, or expansion).

---

## SECTION 7: SAMPLE SIZE CALCULATION PROCEDURES BY DESIGN

### Quick Reference Table

| Design | Minimum N (d = 0.5, α = .05, power = .80) | Formula Source |
|--------|---------------------------------------------|---------------|
| Parallel RCT (2 groups) | 128 total | Cohen (1988) |
| Crossover RCT | 34 total | Assumes r = .50 |
| Cluster RCT (ICC = .05, m = 20) | 250 total | Design effect adjustment |
| Factorial 2×2 (interaction) | 704 total | For detecting interaction |
| DiD | Varies; ~200–500 | Depends on number of time points |
| RDD | ~500+ near cutoff | Local linear estimation |
| Correlation (r = .30) | 84 total | Cohen (1988) |
| Multiple regression (3 predictors, f² = .15) | 77 total | Cohen (1988) |
| Mediation (a × b) | ~200–500 | Monte Carlo power analysis |
| Logistic regression (OR = 2.0) | ~400 total | Depends on event rate |

---

## SECTION 8: VALIDITY THREATS BY DESIGN

### Comprehensive Threat Matrix

| Design | Internal Validity | External Validity | Construct Validity | Statistical Validity |
|--------|------------------|-------------------|--------------------|--------------------|
| **Parallel RCT** | Low threat (randomization); attrition | Moderate (selected samples) | Moderate (lab vs. field) | Low (if powered) |
| **Crossover RCT** | Carryover effects | Moderate (stable conditions only) | Moderate | Low (within-subjects power) |
| **Cluster RCT** | Moderate (ICC) | Moderate | Low | Moderate (reduced df) |
| **DiD** | High (parallel trends) | Moderate | Low | Moderate (serial correlation) |
| **RDD** | Low (near cutoff) | Low (local estimate only) | Low | Moderate (bandwidth selection) |
| **IV** | High (exclusion restriction) | Low (LATE only) | Moderate | High (weak instruments) |
| **Cohort** | High (confounding) | High (if population-based) | Moderate | Low (if large N) |
| **Case-control** | High (recall, selection) | Moderate | Moderate | Low |
| **Cross-sectional** | Very high (no temporal order) | Moderate | Moderate | Low |
| **Qualitative** | N/A (different validity framework) | Moderate (transferability) | Moderate (credibility) | N/A |

**Key:** Low = minimal threat; Moderate = manageable with proper design; High = major limitation requiring careful mitigation; Very High = fundamental constraint of the design

### Mitigation Priority by Design

**For RCTs:** Prioritize minimizing attrition and ensuring allocation concealment
**For Quasi-experimental:** Prioritize verifying identifying assumptions (parallel trends, continuity, instrument validity)
**For Observational:** Prioritize comprehensive confounding control and sensitivity analysis
**For Qualitative:** Prioritize credibility (member checking, triangulation) and dependability (audit trail)
