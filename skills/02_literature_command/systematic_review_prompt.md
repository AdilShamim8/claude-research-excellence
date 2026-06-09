# Systematic Review Prompt

## PRISMA-Compliant Systematic Review Procedure

### Purpose
This prompt guides the execution of a rigorous, PRISMA-compliant systematic review. It ensures transparency, reproducibility, and comprehensiveness in identifying, evaluating, and synthesizing research evidence. A systematic review is not a literature review with more papers — it is a replicable scientific investigation of the literature itself.

---

## STEP 1: PROTOCOL DEVELOPMENT

Before any searching begins, develop and register a review protocol.

### 1.1 Protocol Components

**Review Title:** Use the PICOS format in the title where possible.
- Example: "The effect of [INTERVENTION] on [OUTCOME] in [POPULATION]: A systematic review and meta-analysis"

**Review Question:** Frame using PICOS:
- **P**opulation: Who are the participants/subjects of interest?
- **I**ntervention/Exposure: What is the intervention, exposure, or independent variable?
- **C**omparator: What is the comparison or control condition?
- **O**utcome: What are the primary and secondary outcomes?
- **S**tudy Design: What study designs are eligible?

**Rationale:** Why is this review needed? What decisions will it inform? What previous reviews exist, and why is a new one necessary?

**Objectives:**
- Primary objective: [What is the main question the review addresses?]
- Secondary objectives: [What additional questions will be explored?]

### 1.2 Registration
- Register the protocol on PROSPERO (for health-related reviews) or OSF (for all disciplines)
- Registration should occur BEFORE screening begins
- Include: review question, search strategy, inclusion/exclusion criteria, data extraction plan, synthesis plan, and timeline

---

## STEP 2: SEARCH STRATEGY DEVELOPMENT

### 2.1 Database Selection

**Core databases (include ALL relevant):**

| Discipline | Primary Databases | Supplementary Databases |
|-----------|-------------------|------------------------|
| Medicine/Health | PubMed/MEDLINE, EMBASE, CINAHL | Cochrane Library, PsycINFO, Web of Science |
| Psychology | PsycINFO, PubMed, Web of Science | ERIC, Sociological Abstracts, Scopus |
| Education | ERIC, Web of Science, Scopus | PsycINFO, Sociological Abstracts, ProQuest Dissertations |
| Computer Science | ACM Digital Library, IEEE Xplore, Scopus | Web of Science, DBLP, arXiv |
| Social Sciences | Web of Science, Scopus, Sociological Abstracts | EconLit, IBSS, ASSIA |
| Engineering | Engineering Village, Scopus, IEEE Xplore | Web of Science, PubMed (for bioengineering) |

**Additional sources:**
- Reference lists of included studies (backward citation tracking)
- Citation tracking of included studies (forward citation tracking)
- Contact with authors for unpublished data
- Preprint servers (arXiv, bioRxiv, psyArXiv, SocArXiv)
- Clinical trial registries (ClinicalTrials.gov, WHO ICTRP)
- Dissertations and theses (ProQuest Dissertations & Theses)
- Conference proceedings not indexed in databases

### 2.2 Keyword Strategy

Develop a three-component search using the PICOS framework:

**Component 1: Population/Problem terms**
- Identify 5–10 synonyms and related terms for the population
- Include controlled vocabulary (MeSH terms, Thesaurus terms) AND free-text terms
- Example for "older adults": (older adult* OR elderly OR aged OR senior* OR geriatric* OR "older person*")

**Component 2: Intervention/Exposure terms**
- Identify 5–10 synonyms and related terms for the intervention
- Include both generic and specific intervention names
- Example for "mindfulness": (mindful* OR MBSR OR MBCT OR "mindfulness-based" OR meditation OR Vipassana)

**Component 3: Outcome terms (optional — may be too restrictive)**
- Consider whether outcome terms should be included or if they will exclude relevant studies
- For exploratory reviews, omit outcome terms to maximize sensitivity

**Boolean Operator Strategy:**
```
(Population terms) AND (Intervention terms) [AND (Outcome terms)]
```

### 2.3 Search Strategy Validation

- **Sensitivity check:** Run the search and verify that 3–5 known key studies are captured. If any are missing, revise the strategy.
- **Precision check:** If the initial search returns >10,000 results, add additional limits (date, language, study design filters) while maintaining sensitivity.
- **Document everything:** Save the exact search string used in each database, including the date of search and number of results.

---

## STEP 3: INCLUSION/EXCLUSION CRITERIA

### 3.1 Criteria Template

| Criterion | Inclusion | Exclusion |
|-----------|-----------|-----------|
| **Population** | [Specify age, condition, setting] | [Specify populations not relevant to the question] |
| **Intervention/Exposure** | [Specify type, dose, duration] | [Specify interventions that are different enough to confound synthesis] |
| **Comparator** | [Specify control conditions] | [Specify conditions that are not valid comparators] |
| **Outcome** | [Specify primary and secondary outcomes] | [Specify outcomes that do not address the review question] |
| **Study Design** | [Specify eligible designs] | [Specify designs that cannot answer the review question] |
| **Publication Type** | [Peer-reviewed, preprints, dissertations] | [Opinion pieces, editorials, non-empirical work] |
| **Language** | [Specify] | [Specify if excluding non-English] |
| **Date Range** | [Specify start date with justification] | [Specify if excluding older studies] |
| **Sample Size** | [Minimum if applicable] | [Studies with inadequate power if relevant] |

### 3.2 Screening Procedure

**Level 1: Title and abstract screening**
- Two independent reviewers screen all titles and abstracts
- Disagreements resolved by discussion or third reviewer
- Err on the side of inclusion — if uncertain, include for full-text review
- Record: number screened, number included, number excluded with reasons

**Level 2: Full-text screening**
- Two independent reviewers read full texts of all Level 1 passes
- Apply inclusion/exclusion criteria rigorously
- Document reason for exclusion for each rejected study
- Record: number reviewed, number included, number excluded with specific reasons

### 3.3 PRISMA Flow Diagram Data Collection

Track the following numbers for the PRISMA flow diagram:
- Records identified through database searching (per database)
- Records identified through other sources
- Duplicate records removed
- Records screened (title/abstract)
- Records excluded (title/abstract)
- Full-text articles assessed for eligibility
- Full-text articles excluded (with reasons)
- Studies included in qualitative synthesis
- Studies included in quantitative synthesis (meta-analysis)

---

## STEP 4: DATA EXTRACTION FRAMEWORK

### 4.1 Data Extraction Template

```markdown
## Study Identification
- Study ID: [Unique identifier]
- Authors: [List]
- Year: [YYYY]
- Country: [Country/Countries]
- Funding source: [Source]

## Study Design
- Design type: [RCT, quasi-experimental, cohort, etc.]
- Unit of randomization: [Individual, cluster, etc.]
- Duration: [Follow-up period]
- Number of arms: [Number of conditions]

## Participants
- Total sample size: [N]
- Sample per group: [N1, N2, ...]
- Age: [Mean, SD, range]
- Sex distribution: [% female]
- Key characteristics: [Diagnosis, setting, etc.]
- Inclusion criteria: [As stated]
- Exclusion criteria: [As stated]

## Intervention
- Description: [Full description]
- Duration: [Length of treatment]
- Frequency: [Sessions per week]
- Dose: [Total hours/sessions]
- Delivery: [Individual, group, online, etc.]
- Fidelity check: [Yes/No, method]

## Comparator
- Description: [Full description]
- Matched on: [What was controlled]

## Outcomes
- Primary outcome: [Name, measure, timepoint]
- Secondary outcomes: [Name, measure, timepoint]
- Adverse events: [Reported? What?]

## Results
- Primary outcome effect: [Effect size, CI, p-value]
- Secondary outcome effects: [Effect sizes, CIs, p-values]
- Attrition: [% per group]
- Analysis type: [ITT, per-protocol, etc.]
- Adjusted/unadjusted: [Covariates if adjusted]

## Risk of Bias Assessment
- Overall rating: [High, Low, Unclear]
- Specific concerns: [List]
```

### 4.2 Extraction Quality Control
- Extract data independently in duplicate for a random 20% subset
- Calculate inter-rater reliability (Cohen's kappa ≥ 0.80 required)
- Resolve discrepancies by consensus or third reviewer
- Contact authors for missing data (allow 2 weeks for response)

---

## STEP 5: QUALITY ASSESSMENT OF INCLUDED STUDIES

### 5.1 Risk of Bias Tools by Study Design

| Study Design | Recommended Tool | Key Domains |
|-------------|-----------------|-------------|
| RCT | Cochrane Risk of Bias 2.0 | Randomization, deviations from intended interventions, missing outcome data, measurement of outcome, selection of reported result |
| Quasi-experimental | ROBINS-I | Confounding, selection, classification of interventions, deviations, missing data, measurement, selection of reported result |
| Observational (cohort) | Newcastle-Ottawa Scale | Selection, comparability, outcome |
| Observational (case-control) | Newcastle-Ottawa Scale | Selection, comparability, exposure |
| Systematic reviews | ROBIS | Study eligibility, identification and selection, data collection, synthesis, overall |
| Qualitative | Critical Appraisal Skills Programme (CASP) | Aim, methodology, design, recruitment, data collection, analysis, reflexivity, ethics, findings, value |

### 5.2 Quality Assessment Procedure
- Two independent assessors rate each study
- Disagreements resolved by consensus or third assessor
- Use domain-level ratings (Low/High/Unclear risk) rather than a single overall score when possible
- Sensitivity analyses: exclude high-risk studies and re-run synthesis to test robustness
- Grade the certainty of evidence using GRADE (for intervention reviews) or certainty assessment frameworks appropriate to the review type

### 5.3 GRADE Certainty Assessment

| Factor that Lowers Certainty | Factor that Raises Certainty |
|------------------------------|------------------------------|
| Risk of bias in included studies | Large effect size |
| Inconsistency of results (heterogeneity) | Dose-response gradient |
| Indirectness of evidence | All plausible confounders would reduce the effect |
| Imprecision (wide confidence intervals) | |
| Publication bias | |

**GRADE Ratings:**
- **High certainty:** Very confident that the true effect lies close to the estimate
- **Moderate certainty:** Moderately confident; the true effect is likely close to the estimate
- **Low certainty:** Limited confidence; the true effect may be substantially different
- **Very low certainty:** Very little confidence; the true effect is likely substantially different

---

## STEP 6: SYNTHESIS METHODOLOGY

### 6.1 Narrative Synthesis

Use when quantitative synthesis is not feasible due to heterogeneity in interventions, outcomes, or study designs.

**Procedure:**
1. Group studies by similarity (intervention type, population, outcome)
2. Describe the direction and size of effects within each group
3. Identify patterns: Are effects consistent? What explains inconsistencies?
4. Assess the strength of evidence for each finding
5. Use vote counting cautiously (count of significant vs. non-significant) — it is a weak form of synthesis

**Quality criteria for narrative synthesis:**
- Go beyond vote counting — describe patterns, not just tallies
- Weight studies by quality (high-quality studies should influence conclusions more)
- Address heterogeneity explicitly — explain why studies differ
- Draw only conclusions supported by the evidence, not by the number of studies

### 6.2 Meta-Analytic Synthesis

Use when studies are sufficiently homogeneous in intervention, comparator, outcome, and design.

**Procedure:**
1. Select the effect size metric:
   - Continuous outcomes: Standardized mean difference (Cohen's d or Hedges' g)
   - Dichotomous outcomes: Odds ratio, risk ratio, or risk difference
   - Correlational: Fisher's z transformation of correlation coefficients
2. Calculate effect sizes and variances for each study
3. Assess statistical heterogeneity:
   - Q-test (significant = heterogeneity present)
   - I² statistic (0–40%: might not be important; 30–60%: moderate; 50–90%: substantial; 75–100%: considerable)
   - Tau² (between-study variance in random-effects model)
4. Choose the model:
   - Fixed-effect: When studies share a common true effect size (rare in practice)
   - Random-effects: When true effect sizes vary across studies (more common and conservative)
5. Conduct subgroup analyses to explore heterogeneity sources
6. Conduct sensitivity analyses to test robustness
7. Assess publication bias:
   - Funnel plot visual inspection
   - Egger's test (statistical test for asymmetry)
   - Trim-and-fill method (estimate missing studies)
8. Report using forest plot visualization

**Minimum requirements for meta-analysis:**
- At least 2 studies with comparable interventions and outcomes
- Sufficient data reported to calculate effect sizes (or obtainable from authors)
- Pre-specified analysis plan (not data-driven analytic choices)

### 6.3 Framework-Based Synthesis

Use when the review aims to map evidence onto a theoretical or conceptual framework.

**Procedure:**
1. Select or develop a conceptual framework a priori
2. Map each study's findings onto the framework's components
3. Identify which framework components have strong evidence, which have weak evidence, and which have no evidence
4. Assess whether the evidence supports, refutes, or extends the framework
5. Revise the framework if evidence contradicts it

---

## STEP 7: REPORTING STANDARDS CHECKLIST

### PRISMA 2020 Checklist (Key Items)

| Section | Item | Description |
|---------|------|-------------|
| **Title** | 1 | Identify as systematic review (with or without meta-analysis) |
| **Abstract** | 2 | Structured summary with all PRISMA abstract items |
| **Introduction** | 3 | Rationale for the review |
| | 4 | Objectives with PICOS |
| **Methods** | 5 | Protocol and registration |
| | 6 | Eligibility criteria |
| | 7 | Information sources (databases, dates) |
| | 8 | Search strategy (full strategy for at least one database) |
| | 9 | Selection process (who, how, disagreements) |
| | 10 | Data collection process (who, how, pilot tested?) |
| | 11 | Data items (list all variables collected) |
| | 12 | Risk of bias assessment (tool, who, how) |
| | 13 | Effect measures (specify primary effect measure) |
| | 14 | Synthesis methods (narrative, meta-analytic, with assumptions) |
| | 15 | Reporting bias assessment |
| | 16 | Certainty assessment (GRADE) |
| **Results** | 17 | Study selection (PRISMA flow diagram) |
| | 18 | Study characteristics (table of included studies) |
| | 19 | Risk of bias in studies |
| | 20 | Results of synthesis |
| | 21 | Reporting bias assessment results |
| | 22 | Certainty of evidence |
| **Discussion** | 23 | Summary of main findings |
| | 24 | Limitations |
| | 25 | Interpretation |
| **Other** | 26 | Registration and protocol |
| | 27 | Funding |

---

## STEP 8: TIMELINE AND RESOURCE ESTIMATION

### Typical Timeline for a Systematic Review

| Phase | Duration | Personnel |
|-------|----------|-----------|
| Protocol development and registration | 2–4 weeks | Lead reviewer |
| Search strategy development and validation | 1–2 weeks | Information specialist + lead |
| Searching and deduplication | 1 week | Research assistant |
| Title/abstract screening | 2–6 weeks | 2 reviewers |
| Full-text screening | 2–4 weeks | 2 reviewers |
| Data extraction | 3–6 weeks | 2 extractors |
| Quality assessment | 2–4 weeks | 2 assessors |
| Synthesis (narrative and/or meta-analytic) | 3–6 weeks | Lead + statistician |
| Report writing | 4–8 weeks | Lead + co-authors |
| **Total estimated time** | **20–41 weeks** | |

### Resource Requirements

| Resource | Estimate |
|----------|---------|
| Personnel | 1 lead reviewer, 1 second reviewer, 1 information specialist (optional), 1 statistician (if meta-analysis) |
| Database access | Institutional subscriptions required |
| Software | Covidence or Rayyan (screening), RevMan or R (meta-analysis), GRADEpro (certainty) |
| Studies to screen | Expect 500–10,000 initial results; 50–200 full-text reviews; 10–50 included studies |
| Budget (if applicable) | $0 (if all personnel are salaried) to $15,000+ (if hiring dedicated reviewers) |

### Feasibility Check Before Starting
- [ ] Do you have access to the required databases?
- [ ] Do you have at least two people available for screening?
- [ ] Is the review question clearly defined with PICOS?
- [ ] Do you have the statistical expertise required for the planned synthesis?
- [ ] Is the timeline realistic given your other commitments?
- [ ] Has a similar review been published or registered in the last 2 years?
- [ ] Is the expected number of included studies sufficient to answer the question?

---

## OUTPUT FORMAT

```markdown
# Systematic Review Report

## 1. Protocol
- Review question (PICOS)
- Registration details
- Rationale

## 2. Search Strategy
- Databases searched with dates
- Full search strategy for each database
- Results per database

## 3. PRISMA Flow Diagram
[Standard four-phase diagram with numbers]

## 4. Included Studies
[Table of study characteristics]

## 5. Risk of Bias Assessment
[Domain-level ratings per study]
[Summary figure]

## 6. Synthesis Results
### Narrative Synthesis
[Thematic grouping of findings]
### Meta-Analysis (if applicable)
[Forest plot, heterogeneity statistics, subgroup analyses]
### Publication Bias Assessment
[Funnel plot, Egger's test, trim-and-fill]

## 7. GRADE Certainty of Evidence
[Summary of findings table]

## 8. Discussion
- Summary of findings
- Strengths and limitations
- Comparison with prior reviews
- Implications for practice and research

## 9. Declarations
- Funding
- Conflicts of interest
- Data availability
```
