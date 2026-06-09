# Methods Precision Guide

## Purpose
The methods section must enable exact replication. Every decision, every instrument, every procedure must be documented with sufficient detail that another researcher could recreate your study without asking you a single question. This guide provides the architecture, templates, and standards for methods writing that is precise, complete, and reproducible.

---

## 1. Methods Section Architecture by Study Type

### Experimental Study
1. Participants
2. Design
3. Materials / Stimuli
4. Measures
5. Procedure
6. Data Preparation
7. Statistical Analysis Plan

### Observational / Survey Study
1. Participants
2. Measures
3. Procedure
4. Data Preparation
5. Statistical Analysis Plan

### Longitudinal Study
1. Participants
2. Measures (by time point)
3. Procedure (by time point)
4. Retention and Attrition
5. Data Preparation
6. Statistical Analysis Plan

### Clinical Trial
1. Trial Design and Registration
2. Participants (inclusion/exclusion criteria)
3. Randomization and Blinding
4. Interventions
5. Outcomes (primary, secondary)
6. Procedure
7. Sample Size Calculation
8. Statistical Analysis Plan

### Secondary Data / Archival Study
1. Data Source
2. Sample Selection and Exclusion
3. Measures (with validation for secondary use)
4. Variables and Operationalizations
5. Statistical Analysis Plan

### Computational / Modeling Study
1. Model Specification
2. Parameter Space and Priors
3. Simulation Protocol
4. Model Comparison Framework
5. Validation and Robustness
6. Software and Reproducibility

---

## 2. Participants Subsection Template

### Standard Template

**Participants.** [N] [population description] were [recruited from/selected from] [source]. [Pre-screening criteria, if any]. Participants were [randomly assigned / self-selected] to [conditions]. [Compensation/incentives]. The sample was [X]% [demographic category 1], [Y]% [demographic category 2], with a mean age of [M] years (SD = [SD], range = [min–max]).

A power analysis using [method/software] indicated that a sample of [N] was required to detect [effect size] with [alpha] and [power] in a [design type]. [If N deviates from power target, explain why: "Data collection was terminated at [N] due to [reason], resulting in [actual power]% power to detect [effect size]."]

[Exclusions:] [N] participants were excluded: [N] for [reason 1], [N] for [reason 2], [N] for [reason 3]. [If preregistered exclusions, note this]. The final analytic sample included [N] participants ([N] per condition). [Sensitivity analysis for exclusions: "Including excluded participants did not change the pattern of results."]

[IRB/Ethics:] This study was approved by [institution's] Institutional Review Board (Protocol #[number]). All participants provided [informed consent / assent with parental consent].

### Required Elements Checklist
- [ ] Total N (before and after exclusions)
- [ ] Demographic composition (age, gender, ethnicity/race, education or relevant demographics)
- [ ] Recruitment source and method
- [ ] Compensation
- [ ] Inclusion and exclusion criteria
- [ ] Power analysis or sample size justification
- [ ] Randomization method (if experimental)
- [ ] IRB approval and consent procedure
- [ ] Exclusion reasons and counts
- [ ] Comparison of excluded vs included participants (if exclusion rate > 5%)

---

## 3. Measures Subsection Template (For Every Variable)

### Template for Each Measure

**[Variable Name].** [Construct definition in one sentence]. [Measure name] ([Author, Year]) was used to assess [variable]. This [X]-item scale measures [what it measures] on a [response format, e.g., 5-point Likert scale from 1 (strongly disagree) to 5 (strongly agree)]. Sample items include "[item 1]" and "[item 2]." Items were [summed/averaged] such that higher scores indicate [higher/lower] [construct]. Internal consistency in the present sample was [α/ω] = [value], which is [consistent with/higher than/lower than] the reported reliability of [value] in the validation sample.

[If adapted:] The measure was adapted by [specific change] to [reason for adaptation]. [Validation of adaptation if available.]

[If newly created:] Because no existing measure captured [specific aspect], we developed a [X]-item measure. Items were generated based on [theory/prior measures/expert consultation] and refined through [pilot testing/cognitive interviewing/expert review]. Exploratory factor analysis (N_pilot = [N]) revealed a [one/two]-factor structure. Confirmatory factor analysis in the present sample supported this structure, χ²(df) = [value], CFI = [value], RMSEA = [value].

### Required Elements for Every Measure
- [ ] Construct being measured (with brief definition)
- [ ] Measure name and citation
- [ ] Number of items
- [ ] Response format (scale anchors, range)
- [ ] Sample items (at least 2)
- [ ] Scoring method
- [ ] Reliability in present sample (with comparison to validation sample)
- [ ] Validity evidence (if newly created or adapted)

### Measure Type-Specific Additions

| Measure Type | Additional Required Information |
|---|---|
| Behavioral task | Number of trials, trial structure, dependent measure, practice trials, task validity |
| Physiological | Equipment model, sampling rate, filtering, artifact rejection, scoring method |
| Observational | Coding scheme, coder training, inter-rater reliability, unit of analysis |
| Self-report (existing) | Citation, adaptation details if any, subscales used |
| Self-report (new) | Item generation, pilot testing, factor structure, validity evidence |
| Manipulation check | Measure, timing, results (brief, with direction) |
| Demographic | Which variables measured, how measured (e.g., open-ended vs categories) |

---

## 4. Procedure Subsection Template

### Standard Template

**Procedure.** Upon arrival, participants [were greeted and seated / completed online consent / etc.]. After providing informed consent, participants completed a [demographic questionnaire / pre-measure]. They were then [randomly assigned / instructed] to [condition manipulation description].

[Detailed description of each phase, in chronological order:]
In the [experimental/first] phase, participants in the [condition A] condition [specific instructions and actions]. Participants in the [condition B] condition [specific instructions and actions]. [Manipulation details: duration, stimulus parameters, delivery method, what participants were told.]

[For each subsequent phase:]
After the [experimental phase], participants completed [measure name] ([timing — immediately after / after X-minute delay]). [If multiple measures, list in order with brief description of what each measured.]

[Manipulation check:] To verify the manipulation, participants completed [manipulation check measure], which confirmed that [condition] participants reported [higher/lower] [manipulation check variable] than [other condition] participants, t(df) = [value], p = [value], d = [value].

[Debriefing:] At the conclusion of the study, participants were [debriefed / probed for suspicion / thanked]. [Funnel debriefing details if used.]

[Total duration:] The entire procedure took approximately [X] minutes.

### Required Elements Checklist
- [ ] Chronological order of all events
- [ ] Exact instructions or paraphrased instructions (note which)
- [ ] Manipulation details (stimulus parameters, duration, delivery method)
- [ ] Timing between phases
- [ ] Counterbalancing or randomization details
- [ ] Manipulation check (measure and result)
- [ ] Debriefing procedure
- [ ] Total study duration
- [ ] What participants were told about the study's purpose (cover story)
- [ ] Where full materials can be found (OSF, supplemental)

---

## 5. Statistical Analysis Plan Template

### Standard Template

**Statistical Analysis.** All analyses were preregistered at [URL] unless otherwise noted. We analyzed data using [software] version [X.X] with [package names and versions].

[Primary Analysis:]
To test H1 that [prediction], we conducted a [test name] with [IV] as the predictor and [DV] as the outcome, controlling for [covariates if any]. [Assumption checks:] Normality was assessed with [test/visual method], homogeneity of variance with [test], and [other assumptions] with [method]. [If assumptions violated:] Because [assumption] was violated, we [action taken: used robust test, transformed data, used non-parametric alternative].

[Secondary Analysis:]
To test H2 that [prediction], we [analysis description with same level of detail].

[Mediation/Moderation if applicable:]
We tested whether [M] mediated the relationship between [X] and [Y] using [method: bootstrap mediation / SEM] with [5,000] bootstrap samples. [Moderation:] We tested whether [W] moderated the X→Y relationship by including the interaction term [X × W] in a hierarchical regression, entering main effects at Step 1 and the interaction at Step 2. Continuous predictors were mean-centered before creating the interaction term.

[Missing Data:]
Missing data ([X]% of data points) were handled using [method: FIML / multiple imputation / pairwise deletion]. [Pattern analysis:] Little's MCAR test was [significant/not significant], χ²(df) = [value], p = [value], suggesting data were [MCAR/MAR/MNAR]. [If MI:] [N] imputed datasets were created using [method] with [N] iterations.

[Multiple Comparisons:]
For analyses involving [multiple comparisons / multiple outcomes], we applied [correction method: Bonferroni / FDR / Holm / none with justification]. Adjusted α = [value].

[Effect Sizes:]
We report [Cohen's d / η²_p / R² / OR] as the effect size for all analyses, with 95% confidence intervals. [Benchmarks:] Following Cohen (1988), [d = 0.20/0.50/0.80] represent [small/medium/large] effects.

[Robustness:]
We conducted the following sensitivity analyses: [list]. [Software/packages for reproducibility.]

### Required Elements Checklist
- [ ] Preregistration statement (or explanation if not preregistered)
- [ ] Software and version numbers
- [ ] Each hypothesis with its corresponding analysis
- [ ] Assumption checks and remedies for violations
- [ ] Covariates listed and justified
- [ ] Missing data handling
- [ ] Multiple comparison correction
- [ ] Effect size specifications
- [ ] Robustness/sensitivity analysis plan
- [ ] Alpha level
- [ ] One-tailed vs two-tailed (with justification if one-tailed)

---

## 6. Reproducibility Standards for Methods

### The Replication Test
A methods section passes the replication test if a competent researcher in your field could reproduce your study exactly without contacting you. Test this by asking: "Could someone who has never seen this protocol recreate it from this description alone?"

### Minimum Reproducibility Standards

1. **Materials**: All stimuli, questionnaires, and code are publicly available
   - OSF repository with DOI
   - GitHub repository with version control
   - Supplemental materials with exact stimuli

2. **Code**: Analysis code is complete and runnable
   - Script from raw data to reported results
   - Package versions specified (use renv or requirements.txt)
   - Random seeds set for reproducible results
   - Data dictionary/codebook provided

3. **Data**: De-identified data is available
   - Open data statement
   - Variables match the names used in the paper
   - Codebook explains every variable

4. **Protocol**: Step-by-step protocol is documented
   - Timestamps for each phase
   - Verbatim instructions or scripts
   - Randomization procedure

### Transparency Statements

Include at the end of the Methods section:

**Open Practices Statement.** This study was preregistered at [URL]. All data, analysis code, and materials are publicly available at [URL]. The study was approved by [IRB] (Protocol #[number]).

---

## 7. Common Methods Writing Failures

### Failure 1: The Black Box Procedure
**Problem**: The procedure section says "Participants completed the task" without describing what the task involved.
**Fix**: Describe what participants saw, what they did, and what they were told. Include screenshots if possible.

### Failure 2: The Missing Measure
**Problem**: A variable appears in the results section but was never described in the measures section.
**Fix**: Every variable in the results must appear in the measures section. Audit the results against the methods before submission.

### Failure 3: The Unjustified Exclusion
**Problem**: Participants were excluded without stating the criterion before data analysis.
**Fix**: Pre-specify exclusion criteria. If post-hoc exclusions were made, disclose this and run sensitivity analyses with and without excluded participants.

### Failure 4: The Unstated Analysis
**Problem**: An analysis appears in the results that was not described in the analysis plan.
**Fix**: If you added an analysis after seeing the data, label it as exploratory and note it was not preregistered.

### Failure 5: The Vague Sample
**Problem**: "We recruited 200 participants from a university" — which university? What population? How recruited?
**Fix**: Be specific about source, recruitment method, eligibility, and demographics.

### Failure 6: The Borrowed Reliability
**Problem**: Reporting the validation sample's reliability (α = .89) without reporting the present sample's reliability (which might be .62).
**Fix**: Always report reliability for your sample. If it differs substantially from the validation sample, discuss why.

### Failure 7: The Missing Power Analysis
**Problem**: No justification for sample size.
**Fix**: Even post-hoc, report a sensitivity analysis: "With N = 120, we had 80% power to detect d = 0.51."

---

## 8. Methods Length and Detail Calibration

### Length by Journal Type

| Journal Type | Methods Word Count | Level of Detail |
|---|---|---|
| High-impact general (Science, Nature) | 500-800 | Compressed; full details in supplementary |
| Top field journal | 1000-1500 | Standard detail |
| Methods-heavy journal | 1500-3000 | Extensive detail |
| Clinical journal (JAMA, Lancet) | 800-1200 | Per CONSORT guidelines |
| Online-only / unlimited space | No limit | Maximum detail |

### What Goes in Supplementary Methods
When the journal imposes word limits, move to supplementary:
1. Full stimulus descriptions and examples
2. Complete questionnaire items
3. Power analysis calculations
4. Detailed assumption checks
5. Alternative analysis specifications
6. Pilot study details
7. Codebook and variable descriptions

### Detail Calibration Principle
**Rule**: The rarer the method, the more detail required. A standard t-test needs one sentence. A novel Bayesian hierarchical model needs a paragraph plus supplementary equations.

### Cross-Referencing Standard
If you describe a standard procedure in one paper and reuse it: "The task was identical to that used in Smith et al. (2023), with the exception that [specific change]." Do not repeat the entire description if nothing changed.
