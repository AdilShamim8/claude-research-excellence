# Methodology Architect

## Skill Metadata
- **Skill Name:** Methodology Architect
- **Version:** 2.0.0
- **Purpose:** Design rigorous, appropriate, and defensible research methodology that aligns research questions with optimal designs, measures, and analytical plans
- **Trigger:** User needs to design a study, write a methods section, pre-register a study, or evaluate methodological rigor
- **Integration:** Receives research questions and contribution maps from Ideation Engine (01), theoretical frameworks from Literature Command (02), and feeds structured methodology to Writing Engine (06) and Review Simulator (07)

---

## ACTIVATE: METHODOLOGY

When the user invokes the Methodology Architect, execute the following four-phase protocol. Do not skip phases. Each phase must produce documented output before proceeding.

---

### PHASE 1: DESIGN SELECTION MATRIX

**Objective:** Select the research design that best matches the research question, the desired causal claim level, and the practical constraints.

#### 1.1 Causal Claim Levels

| Claim Level | What You Can Claim | Required Design | Example |
|-------------|-------------------|-----------------|---------|
| **Level 5: Causal Mechanism** | "X causes Y through mechanism M" | Experimental design + mediation test + mechanism manipulation | RCT with process measure showing the mediator is necessary and sufficient |
| **Level 4: Causal Effect** | "X causes Y" | Randomized controlled trial | RCT with random assignment to treatment and control |
| **Level 3: Quasi-Causal** | "X likely causes Y, but confounding cannot be fully ruled out" | Quasi-experimental design (DiD, RDD, IV, synthetic control) | Difference-in-differences comparing treated and untreated groups over time |
| **Level 2: Conditional Prediction** | "X predicts Y, controlling for Z" | Observational design with statistical controls | Multiple regression with covariates |
| **Level 1: Description/Association** | "X and Y are associated" or "The prevalence of X is Y%" | Cross-sectional, descriptive, or qualitative design | Survey reporting correlations or prevalence |

**Critical Rule:** The research design must match or exceed the causal claim level. A Level 2 claim (conditional prediction) with a Level 1 design (cross-sectional survey) is unjustified. Either upgrade the design or downgrade the claim.

#### 1.2 Identification Threats Assessment

For the selected design, systematically evaluate identification threats:

| Threat | Definition | Affected Designs | Mitigation |
|--------|-----------|-----------------|------------|
| **Selection bias** | Systematic differences between groups before treatment | All non-randomized designs | Propensity score matching, covariate adjustment, random assignment |
| **Reverse causality** | Y causes X rather than X causes Y | Cross-sectional, correlational | Temporal ordering (X measured before Y), instrumental variables |
| **Omitted variable bias** | An unmeasured confound explains both X and Y | All observational designs | Sensitivity analysis for unmeasured confounding, fixed effects |
| **Measurement error** | Variables are measured with error, biasing estimates | All designs | Validated instruments, multiple measures, latent variable models |
| **Attrition bias** | Differential dropout between conditions | Longitudinal, RCT | Intent-to-treat analysis, imputation, attrition analysis |
| **Spillover/contamination** | Treatment affects control group | Cluster RCT, field experiments | Cluster randomization, physical separation, statistical adjustment |
| **Hawthorne effect** | Participants change behavior because they know they are observed | All human subjects research | Blinding, unobtrusive measures, control for demand characteristics |
| **Regression to the mean** | Extreme groups naturally move toward the average | Pre-post designs, selection on extreme scores | Control group, ANCOVA with baseline as covariate |

#### 1.3 Statistical Power Planning

**Required parameters for power analysis:**
- **Expected effect size:** Based on prior literature or smallest effect size of interest (SESOI)
- **Alpha level:** Conventionally .05, but consider .005 for confirmatory research or .10 for exploratory
- **Desired power:** Minimum .80; .90 for high-stakes research; .95 for registered reports
- **Design specifics:** Number of groups, covariates, repeated measures, cluster structure

**Power by Design Type (minimum N for d = 0.5, α = .05, 1-β = .80):**

| Design | Minimum Total N | Notes |
|--------|----------------|-------|
| Two-group between-subjects t-test | 128 | 64 per group |
| One-way ANOVA (3 groups) | 159 | 53 per group |
| 2×2 factorial ANOVA | 128 | 32 per cell |
| Repeated measures (2 time points) | 34 | Within-subjects; assumes r = .50 |
| Correlation (r = .30) | 84 | For detecting medium correlation |
| Multiple regression (3 predictors) | 77 | For medium effect (f² = .15) |
| Mediation (a × b path) | ~200–500 | Depends on effect sizes; use Monte Carlo |
| Cluster RCT (10 clusters) | ~500–1000 | Depends on ICC; always more than individual RCT |

**Quality Gate:** Phase 1 must produce a design selection with explicit justification, an identification threats assessment with mitigations, and a power analysis with sample size rationale. If the power analysis shows the study is underpowered with available resources, flag this as a critical limitation and recommend either increasing the sample size, reducing the number of hypotheses, or reframing the study as exploratory.

---

### PHASE 2: METHODS SECTION ARCHITECTURE

**Objective:** Construct a complete, reproducible methods section following discipline-standard structure.

#### 2.1 Participants / Data

**Required elements:**
- **Eligibility criteria:** Inclusion and exclusion criteria with rationale for each
- **Recruitment method:** How participants were identified, contacted, and enrolled
- **Sample size:** Target N, achieved N, and justification (power analysis reference)
- **Demographics:** Age (M, SD, range), sex/gender distribution, ethnicity, education, relevant clinical characteristics
- **Representativeness:** How the sample compares to the target population; known biases
- **Compensation:** What participants received, if anything
- **Ethical approval:** IRB/ethics committee name and approval number
- **Data source (for secondary data):** Dataset name, version, access method, any restrictions

**Template:**
```
Participants were [N] [POPULATION DESCRIPTION] recruited from [SOURCE] through
[METHOD]. Inclusion criteria were [CRITERIA], and exclusion criteria were
[CRITERIA] to ensure [RATIONALE]. The target sample size of [N] was determined
by an a priori power analysis (see Analysis Plan) for detecting [EFFECT SIZE]
with [POWER] power at α = [ALPHA]. Of [N APPROACHED], [N CONSENTED] consented,
and [N COMPLETED] completed all study procedures. The final sample (N = [N];
[AGE], [GENDER], [ETHNICITY]) was [COMPARISON TO POPULATION]. This study was
approved by [IRB/COMMITTEE] (Protocol #[NUMBER]).
```

#### 2.2 Measures

**For each measure, document:**

| Element | Required Content |
|---------|-----------------|
| **Construct** | What theoretical construct does this measure assess? |
| **Instrument** | What is the name and version of the measure? |
| **Source** | Who developed it? Provide citation. |
| **Reliability** | What is the reported reliability (Cronbach's α, test-retest, inter-rater)? What was reliability in this sample? |
| **Validity** | What validity evidence exists (content, criterion, construct, convergent, discriminant)? |
| **Scoring** | How is the measure scored? Range, direction, clinical cutoffs. |
| **Adaptation** | Were any modifications made to the original measure? Why? Were they validated? |
| **Administration** | How and when was the measure administered? By whom? In what format? |

**Manipulation check (for experimental designs):**
- Describe the manipulation check measure
- Specify the criterion for successful manipulation (e.g., "Participants in the high-stress condition will report significantly higher state anxiety than those in the low-stress condition, p < .05")

**Template for each measure:**
```
[CONSTRUCT] was measured using the [INSTRUMENT NAME] ([AUTHOR, YEAR]), a
[NUMBER]-item self-report scale assessing [DESCRIPTION]. Items are rated on
a [SCALE] and summed/averaged to produce a total score ranging from [RANGE],
with higher scores indicating [DIRECTION]. The [INSTRUMENT] has demonstrated
good internal consistency (α = [VALUE]; [CITATION]), test-retest reliability
(r = [VALUE]; [CITATION]), and convergent validity with [RELATED MEASURE]
(r = [VALUE]; [CITATION]). In the current sample, Cronbach's α was [VALUE].
[ANY ADAPTATIONS MADE AND JUSTIFICATION].
```

#### 2.3 Procedure

**Required elements:**
- Step-by-step description of what participants experienced, in order
- Randomization procedure (if applicable): method, allocation ratio, concealment
- Blinding procedure: who was blinded, to what, and how
- Intervention description (if applicable): content, duration, frequency, delivery method, fidelity monitoring
- Timing: duration of each phase, total study duration, follow-up intervals
- Setting: where the study took place (lab, field, online, clinical)
- Data collection method: paper, digital, observation, physiological recording
- Debriefing (if applicable)

**Template:**
```
Upon enrollment, participants were randomly assigned to [CONDITION A] or
[CONDITION B] using [RANDOMIZATION METHOD], with allocation concealed through
[CONCEALMENT METHOD]. Participants in [CONDITION A] received [INTERVENTION
DESCRIPTION], while those in [CONDITION B] received [CONTROL DESCRIPTION].
The intervention consisted of [SESSIONS] sessions of [DURATION] each, delivered
by [WHO] in [SETTING]. Fidelity was monitored through [METHOD]. All participants
completed [MEASURES] at [TIMEPOINTS]. The study took approximately [DURATION]
per participant. Participants were debriefed at the conclusion of the study.
```

#### 2.4 Statistical Analysis Plan

**Required elements:**
- **Software:** Name, version, and any custom code or packages used
- **Preprocessing:** Data cleaning rules, outlier handling, missing data strategy, transformation rationale
- **Primary analysis:** Exact statistical test, model specification, and how it tests each hypothesis
- **Secondary analyses:** Additional tests with rationale
- **Exploratory analyses:** Clearly labeled as exploratory; not confirmatory
- **Assumption checks:** Which assumptions will be tested, how, and what happens if violated
- **Multiple comparison correction:** Which correction, applied to which tests
- **Effect size reporting:** Which effect sizes will be reported with confidence intervals
- **Sensitivity analyses:** Tests of robustness to assumptions and analytical decisions
- **Missing data plan:** How missing data will be handled (listwise deletion, MI, FIML) with justification

**Template for each hypothesis:**
```
To test H[X] ([HYPOTHESIS STATEMENT]), a [STATISTICAL TEST] was conducted
with [IV] as the predictor and [DV] as the outcome, controlling for
[COVARIATES]. Effect sizes are reported as [EFFECT SIZE METRIC] with 95%
confidence intervals. A significant [EFFECT] would support H[X], while a
non-significant effect with adequate power (≥ .80) would disconfirm it.
```

**Quality Gate:** Phase 2 must produce a complete methods section draft with all four subsections. Every measure must have reliability and validity documentation. The statistical analysis plan must specify the exact test for each hypothesis. Missing any element requires revision before proceeding.

---

### PHASE 3: PRE-REGISTRATION TEMPLATE

**Objective:** Create a complete pre-registration document that distinguishes confirmatory from exploratory analyses and prevents HARKing.

#### 3.1 Pre-Registration Template

```markdown
# Study Pre-Registration

## Study Information
- **Title:** [STUDY TITLE]
- **Authors:** [LIST]
- **Registration date:** [DATE]
- **Registration platform:** [OSF/AsPredicted/ClinicalTrials.gov]
- **Registration DOI/URL:** [LINK]

## 1. Hypotheses

### Primary Hypotheses
H1: [Full hypothesis statement]
- Direction: [Directional (specify) / Non-directional]
- Theoretical basis: [Theory and citation]
- Falsification condition: [What outcome would disconfirm?]

H2: [If applicable]

### Secondary Hypotheses
H3: [Full hypothesis statement]
[Same structure]

### Exploratory Questions
EQ1: [Question, not hypothesis — no directional prediction]
- Rationale for exploring: [Why this is worth examining]

## 2. Outcomes

### Primary Outcome
- Variable: [NAME]
- Measure: [INSTRUMENT]
- Timepoint: [WHEN MEASURED]
- Scoring: [HOW SCORED]

### Secondary Outcomes
[Same structure for each]

## 3. Analysis Plan

### Primary Analysis
- H1 test: [Exact statistical test]
- Model specification: [Equation or model description]
- Software: [Name and version]
- Assumptions: [What will be checked]
- Multiple comparison correction: [Method and which tests it applies to]
- Effect size: [Metric to be reported]
- Decision rule: [What constitutes support for H1]

### Secondary Analyses
[Same structure]

### Exploratory Analyses
[Same structure, clearly labeled as exploratory]

### Analysis Exclusions
- Exclusion criteria: [What data will be excluded and why]
- Outlier handling: [Definition and treatment]
- Missing data: [How handled]

### Sensitivity Analyses
[What robustness checks will be performed]

## 4. Sample Size

### Power Analysis
- Desired power: [VALUE]
- Alpha level: [VALUE]
- Expected effect size: [VALUE with source/justification]
- Required N: [VALUE]
- Statistical test: [TEST used for power calculation]
- Software: [G*Power, R, etc.]

### Stopping Rule
- Fixed N: [Will data collection stop at a predetermined N?]
- Sequential analysis: [If applicable, describe stopping boundaries]

## 5. Design

- Design type: [RCT, quasi-experimental, observational, etc.]
- Randomization: [Method, if applicable]
- Blinding: [Who is blinded to what]
- Conditions: [List all conditions with descriptions]
- Study duration: [Total time per participant]
- Follow-up: [Timepoints, if longitudinal]

## 6. Variables

### Independent Variables
- [Variable name]: [Levels/categories; how manipulated/measured]

### Dependent Variables
- [Variable name]: [How measured; primary/secondary]

### Covariates
- [Variable name]: [Why included; how measured]

### Moderators
- [Variable name]: [Why hypothesized to moderate; how measured]

### Mediators
- [Variable name]: [Why hypothesized to mediate; how measured]
```

**Quality Gate:** The pre-registration must include all sections. Hypotheses must be directional (or justified as non-directional). The analysis plan must specify exact tests. The sample size must be justified by power analysis. Exploratory analyses must be clearly labeled.

---

### PHASE 4: RIGOR STRESS TEST

**Objective:** Subject the proposed methodology to a systematic stress test across five validity types, identifying weaknesses before reviewers do.

#### 4.1 Five Validity Types

**1. Internal Validity** — Can you make a causal claim?

| Threat | Is it present? | Severity | Mitigation |
|--------|---------------|----------|------------|
| Selection bias | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Maturation | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| History | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Testing effects | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Instrumentation | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Regression to the mean | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Attrition | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Diffusion of treatment | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Ambiguous temporal precedence | [Y/N] | [High/Med/Low] | [What you're doing about it] |

**2. External Validity** — Do findings generalize?

| Threat | Is it present? | Severity | Mitigation |
|--------|---------------|----------|------------|
| Population validity | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Ecological validity | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Temporal validity | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Setting validity | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Treatment variation | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Outcome variation | [Y/N] | [High/Med/Low] | [What you're doing about it] |

**3. Construct Validity** — Are you measuring what you think you're measuring?

| Threat | Is it present? | Severity | Mitigation |
|--------|---------------|----------|------------|
| Construct underrepresentation | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Construct-irrelevant variance | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Mono-operation bias | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Mono-method bias | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Confounding constructs | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Inadequate preoperational definition | [Y/N] | [High/Med/Low] | [What you're doing about it] |

**4. Statistical Conclusion Validity** — Are your statistical inferences justified?

| Threat | Is it present? | Severity | Mitigation |
|--------|---------------|----------|------------|
| Low statistical power | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Violated assumptions | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Fishing/explicit p-hacking | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Unreliable measures | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Restricted range | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Unreliability of treatment implementation | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Multiple comparisons | [Y/N] | [High/Med/Low] | [What you're doing about it] |

**5. Replicability** — Could another researcher reproduce this study?

| Threat | Is it present? | Severity | Mitigation |
|--------|---------------|----------|------------|
| Insufficient methodological detail | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Non-standardized procedures | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Proprietary measures | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Undocumented analytic decisions | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Data/code not shared | [Y/N] | [High/Med/Low] | [What you're doing about it] |
| Sample not described adequately | [Y/N] | [High/Med/Low] | [What you're doing about it] |

#### 4.2 Weakness Classification

After identifying all threats, classify each weakness:

| Classification | Definition | Action Required |
|---------------|-----------|-----------------|
| **Fatal** | Threat undermines the core claim; no mitigation possible | Redesign the study or change the research question |
| **Major** | Threat significantly limits interpretability; mitigation possible but imperfect | Implement mitigation; acknowledge limitation; frame claims cautiously |
| **Moderate** | Threat is present but manageable; mitigation substantially reduces risk | Implement mitigation; briefly acknowledge limitation |
| **Minor** | Threat is theoretical but unlikely to materially affect results | Document in limitations section; no design change needed |

**Quality Gate:** No fatal weaknesses may remain. All major weaknesses must have documented mitigations. The rigor stress test results must be reflected in the final methods section's limitations acknowledgment.

---

## OUTPUT FORMAT

```markdown
# Methodology Architect Output

## 1. Design Selection
- Selected design: [TYPE]
- Causal claim level: [LEVEL]
- Justification: [Why this design]
- Identification threats: [Table with mitigations]
- Power analysis: [Parameters and required N]

## 2. Methods Section Draft
### Participants/Data
[Complete draft]
### Measures
[Complete draft for each measure]
### Procedure
[Complete draft]
### Statistical Analysis Plan
[Complete draft]

## 3. Pre-Registration Document
[Complete pre-registration in template format]

## 4. Rigor Stress Test Results
### Internal Validity
[Threat table]
### External Validity
[Threat table]
### Construct Validity
[Threat table]
### Statistical Conclusion Validity
[Threat table]
### Replicability
[Threat table]
### Weakness Summary
[Fatal: 0 | Major: N | Moderate: N | Minor: N]
[Required design changes]

## 5. Integration Notes
- Feedback for Ideation Engine: [Any hypothesis revisions needed based on design constraints]
- Feedback for Literature Command: [Any methodological context needed]
- Preparation for Writing Engine: [Key methodology phrasing and structure]
- Preparation for Review Simulator: [Anticipated reviewer concerns about methodology]
```

---

## INTEGRATION NOTES

### With Ideation Engine (01_ideation)
- Receive research questions and hypotheses; verify they are testable with the available design
- If design constraints prevent testing a hypothesis, feed back to Ideation Engine for refinement
- Novelty certificate dimensions should inform methodology choices (e.g., method gaps require methodological innovation)

### With Literature Command (02_literature_command)
- Receive effect size estimates from meta-analyses for power calculations
- Receive methodological scorecard to identify what design improvements the literature needs
- Contribute methodological description to the related work section's positioning

### With Writing Engine (06_writing_engine)
- Methods section draft feeds directly into the manuscript
- Pre-registration language informs the manuscript's analysis section
- Limitations section is pre-populated from the rigor stress test

### With Review Simulator (07_review_simulator)
- Rigor stress test results predict reviewer objections
- Weakness classifications inform response strategy
- Alternative analytical approaches (from sensitivity analyses) prepare for reviewer suggestions

---

## USAGE EXAMPLES

**Example 1: Designing a new experiment**
```
User: "I want to test whether a growth mindset intervention improves academic performance in first-year college students."
→ Execute all 4 phases, selecting an RCT design with appropriate power analysis.
```

**Example 2: Pre-registration only**
```
User: "I have my methods figured out. I just need to pre-register."
→ Execute Phase 3 only, extracting details from the user's existing design.
```

**Example 3: Stress-testing an existing design**
```
User: "Here's my methods section [PASTED TEXT]. What are the weaknesses?"
→ Execute Phase 4 only, identifying threats and recommending mitigations.
```

---

## VERSION HISTORY
- v2.0.0 — Added five validity types stress test, pre-registration template, causal claim levels, weakness classification system
- v1.0.0 — Initial release with basic design selection and methods drafting
