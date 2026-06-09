# REPLICATION STUDY WORKFLOW — Replication and Extension Protocol

> **CRES Workflow v1.0** | A comprehensive guide to designing, conducting, and publishing replication research. In an era of replication crisis, well-executed replications are among the most valuable scientific contributions — yet they remain among the most challenging to publish. This workflow provides the structure to maximize both rigor and impact.

---

## Table of Contents

1. [The Replication Crisis Context](#the-replication-crisis-context)
2. [Why Replications Matter](#why-replications-matter)
3. [Types of Replication](#types-of-replication)
4. [Phase 1: Target Selection](#phase-1-target-selection)
5. [Phase 2: Protocol Development](#phase-2-protocol-development)
6. [Phase 3: Pre-Registration](#phase-3-pre-registration)
7. [Phase 4: Execution](#phase-4-execution)
8. [Phase 5: Writing the Replication](#phase-5-writing-the-replication)
9. [Phase 6: Publication Strategy](#phase-6-publication-strategy)
10. [Statistical Considerations for Replications](#statistical-considerations-for-replications)
11. [When a "Failed" Replication Is Actually a Contribution](#when-a-failed-replication-is-actually-a-contribution)
12. [Extension Strategies](#extension-strategies)
13. [Multi-Lab Replication Protocols](#multi-lab-replication-protocols)
14. [Dealing with Original Authors](#dealing-with-original-authors)
15. [Making Your Replication Maximally Useful](#making-your-replication-maximally-useful)
16. [Replication Reporting Standards](#replication-reporting-standards)

---

## The Replication Crisis Context

### The Scope of the Problem

The replication crisis — sometimes called the reproducibility crisis — refers to the systematic failure of published research findings to be reproduced when independent researchers attempt to replicate them. The crisis has been documented across multiple disciplines:

| Field | Key Finding | Source |
|-------|-------------|--------|
| **Psychology** | Only 36% of 100 studies replicated (significant effect in same direction) | Open Science Collaboration (2015) |
| **Oncology** | Only 11% of 53 preclinical studies could be validated | Begley & Ellis (2012) |
| **Economics** | Only 61% of 18 studies replicated in lab experiments | Camerer et al. (2016) |
| **Social Sciences** | Only 13 of 21 (62%) social science experiments in Nature/Science replicated | Camerer et al. (2018) |
| **Biomedical** | 65% of researchers have failed to reproduce another's experiment | Baker (2016, Nature survey) |
| **Machine Learning** | Reproducibility of 401 papers: only 20–30% fully reproducible | Research across multiple studies |

### Root Causes

The replication crisis has multiple, interacting causes:

1. **Publication bias:** Journals preferentially publish novel, significant findings, creating a distorted literature
2. **P-hacking:** Researchers analyze data in multiple ways and report only the approach that yields significance
3. **HARKing:** Hypothesizing After Results Known — presenting post-hoc findings as if they were predicted
4. **Low statistical power:** Underpowered studies produce inflated effect sizes and unreliable results
5. **Questionable research practices (QRPs):** Selective reporting, optional stopping, outlier exclusion
6. **Incentive structures:** "Publish or perish" culture rewards novelty over reliability
7. **Methodological flexibility:** Ambiguous analytic choices allow researchers to "find" significant results
8. **Lack of transparency:** Insufficient reporting of methods, data, and code prevents verification

### The Paradigm Shift

The scientific community is undergoing a paradigm shift in how it values replication:

**Old paradigm:** Replication is unglamorous, low-priority work that journals won't publish and hiring committees won't reward.

**New paradigm:** Replication is essential scientific infrastructure. Without it, we cannot distinguish real findings from false positives, and the entire knowledge base is built on uncertain ground.

**Your role:** By conducting rigorous replications, you are not doing "lesser" science — you are performing an essential service that the scientific community increasingly recognizes and rewards.

---

## Why Replications Matter

### Epistemic Functions

| Function | Description | Example |
|----------|-------------|---------|
| **Verification** | Confirming that a reported finding is reliable | Replicating a classic effect with a larger sample |
| **Boundary testing** | Determining the conditions under which a finding holds | Testing whether an effect observed in students generalizes to older adults |
| **Effect size estimation** | Providing more accurate estimates of effect magnitude | Original study: d = 0.80; Replication: d = 0.35 |
| **Robustness testing** | Testing whether findings hold under methodological variation | Using a different measure of the same construct |
| **Generalization** | Testing whether findings extend to different populations or contexts | Replicating a US-based finding in a non-WEIRD sample |
| **Cumulative science** | Building a cumulative evidence base rather than isolated findings | Multiple replications providing a meta-analytic evidence base |

### Practical Functions

| Function | Description | Impact |
|----------|-------------|--------|
| **Resource allocation** | Preventing wasted resources on unreliable findings | Billions saved by not building on false positives |
| **Policy calibration** | Ensuring evidence-based policy is based on actual evidence | Policy decisions revised based on replication evidence |
| **Clinical application** | Verifying that clinical findings are real before applying them | Patient safety protected by replication failures |
| **Theoretical refinement** | Identifying which theoretical predictions are supported | Theories revised based on what replicates vs. doesn't |
| **Methodological improvement** | Identifying which methods produce reliable results | Research practices improved based on replication evidence |

### Career Functions

While replications have historically been undervalued, the landscape is changing rapidly:

- **Dedicated replication journals:** Journal of Negative Results, Comprehensive Results in Social Psychology, replication sections in major journals
- **Registered Reports:** Pre-accepted study designs reduce publication bias against replications
- **Open science badges:** Replications can earn transparency badges that enhance visibility
- **Grant funding:** Some funders now specifically support replication research
- **Citation advantage:** Replications of high-profile studies are highly cited
- **Professional reputation:** Conducting rigorous replications signals methodological seriousness

---

## Types of Replication

### The Replication Taxonomy

Understanding the different types of replication is essential for designing your study and framing your contribution.

| Type | Description | Fidelity | Goal | Publication Potential |
|------|-------------|----------|------|-----------------------|
| **Direct (Exact) Replication** | Repeats the original study as closely as possible | Very High | Verify the finding | Moderate — most journals undervalue this |
| **Close Replication** | Repeats the study with minor unavoidable modifications | High | Verify with contextual updates | Moderate-High — modifications add novelty |
| **Conceptual Replication** | Tests the same hypothesis using different methods/operationalizations | Moderate | Test the theoretical claim | High — methodological variation adds value |
| **Constructive Replication** | Tests the same finding with different samples, measures, or contexts | Variable | Test generalizability | High — extends the finding |
| **Extension Replication** | Replicates the original AND adds new conditions/variables | Variable | Replicate + Extend | Very High — adds original contribution |
| **Multi-Lab Replication** | Coordinated replication across multiple independent labs | High | Large-scale verification | Very High — collaborative, high power |
| **Systematic Replication** | Series of replications varying one parameter systematically | Moderate | Map boundary conditions | High — produces generalizability map |

### Decision Framework: Which Type to Choose

```
What is your primary goal?
│
├── VERIFY whether a specific finding is real
│   → Direct or Close Replication
│   → Add Extension to increase publication value
│
├── TEST whether the theoretical claim generalizes
│   → Conceptual Replication
│   → Tests the theory, not just the specific finding
│
├── MAP the boundary conditions of an effect
│   → Systematic Replication
│   → Varies key parameters across multiple studies
│
├── PRODUCE the most publishable replication
│   → Extension Replication
│   → Replicates AND extends in one package
│
└── PROVIDE definitive evidence on a controversial finding
    → Multi-Lab Replication
    → Maximum power and credibility
```

### The Replication Value Matrix

When deciding which type to pursue, consider:

| Factor | Direct | Conceptual | Extension | Multi-Lab |
|--------|--------|-----------|-----------|-----------|
| **Scientific value** | High (if finding is important) | High | Very High | Very High |
| **Publication ease** | Low-Moderate | Moderate | Moderate-High | High |
| **Effort required** | Moderate | High | High | Very High |
| **Citation potential** | High (if original is highly cited) | Moderate | High | Very High |
| **Career benefit** | Moderate | Moderate-High | High | Very High |
| **Risk of null finding** | Moderate | High | Moderate | Moderate |
| **Controversial impact** | High | Moderate | Moderate | Very High |

---

## Phase 1: Target Selection

**Duration: 1–2 weeks** | **Goal:** Identify the optimal study to replicate based on scientific importance, feasibility, and publication potential.

### Step 1.1: Priority Criteria for Target Selection

Not all studies are equally worth replicating. Use this prioritization framework:

#### Tier 1: MUST-REPLICATE (Highest Priority)
- Highly cited studies that form the basis for substantial subsequent research
- Studies that inform public policy, clinical practice, or major business decisions
- Studies with surprising or counterintuitive findings that challenge existing theory
- Studies with large effect sizes that seem too good to be true
- Studies that are frequently cited in textbooks as established facts

#### Tier 2: SHOULD-REPLICATE (High Priority)
- Studies published in top journals with moderate citation counts
- Studies that have never been independently replicated
- Studies that are widely assumed to be true without verification
- Studies with methodological features that inflate Type I error rates
- Studies whose findings are used to justify research funding

#### Tier 3: COULD-REPLICATE (Moderate Priority)
- Studies with interesting but less central findings
- Studies that are moderately cited
- Studies in emerging areas where the evidence base is thin
- Studies that use novel methods that haven't been validated

#### Tier 4: LOW PRIORITY (Consider Carefully)
- Studies with small effect sizes in well-replicated areas
- Studies that are trivially easy to replicate (no one doubts them)
- Studies in areas with robust replication evidence already
- Studies that are so methodologically complex that replication is impractical

### Step 1.2: Target Evaluation Rubric

Score each potential replication target on these dimensions:

| Criterion | Weight | Score (1–10) | Weighted Score |
|-----------|--------|-------------|----------------|
| **Citation impact** (How many downstream studies depend on this?) | 20% | — | — |
| **Policy/practice relevance** (Are real-world decisions based on this?) | 15% | — | — |
| **Replication gap** (Has this been replicated before? How many times?) | 15% | — | — |
| **Methodological concern** (Are there red flags in the original methods?) | 15% | — | — |
| **Feasibility** (Can you realistically replicate this with your resources?) | 15% | — | — |
| **Publication potential** (Will journals publish this replication?) | 10% | — | — |
| **Theoretical centrality** (Is this finding central to an important theory?) | 10% | — | — |

**Decision rule:** Proceed with targets scoring ≥ 7.0 weighted average. Below 5.0, find a better target.

### Step 1.3: The Replication Feasibility Assessment

Before committing to a replication target, assess feasibility honestly:

```
FEASIBILITY CHECKLIST:

□ Can you obtain or recreate the original materials?
  - Stimuli, questionnaires, software, equipment
  - If not available, can you create equivalent versions?

□ Can you recruit a comparable or adequate sample?
  - Same population? If not, is the difference justifiable?
  - Sample size sufficient for adequate power?

□ Can you implement the original procedure?
  - Same experimental conditions and timing?
  - Same measures and assessment points?

□ Can you access the same analysis approach?
  - Original analysis code available?
  - If not, can you reproduce the analysis from the methods description?

□ Is the timeline realistic?
  - How long did the original study take?
  - Can you complete replication within your constraints?

□ Are there ethical barriers?
  - IRB approval obtainable?
  - Same consent procedures feasible?

□ Are there financial barriers?
  - Required equipment, compensation, software?
  - Budget adequate?

□ Is there a co-author/collaborator available?
  - Especially important for complex protocols
  - Expert in the original methodology?
```

### Step 1.4: Contacting Original Authors

**Best practice:** Contact the original authors before beginning your replication. This is not required but is strongly recommended for several reasons:

1. **Access to materials:** Original authors may share stimuli, code, or detailed protocols
2. **Accuracy verification:** They can confirm your protocol matches their study
3. **Professional courtesy:** Prevents the perception that you are "attacking" their work
4. **Potential collaboration:** Some original authors welcome replications and may co-author
5. **Contextual insight:** They may share unpublished details that affect the replication

**Contact Template:**

```
Dear Dr. [NAME],

I am writing to inform you that I am planning a replication of your
study "[TITLE]" ([YEAR], [JOURNAL]). I believe this finding is
important and worth verifying with an independent sample.

I want to ensure that my replication is as faithful as possible to
your original protocol. Would you be willing to:

1. Share the original materials, stimuli, or code used in your study?
2. Review my replication protocol for accuracy before I begin?
3. Provide any unpublished details about the procedure that may
   not have been included in the paper?

I am committed to conducting a fair and rigorous replication and
welcome any input you can provide. I will share my results with
you before publication, giving you the opportunity to comment.

Thank you for your time and for producing work worth replicating.

Best regards,
[YOUR NAME]
```

**Important notes on contacting original authors:**
- You are NOT asking permission to replicate; you are informing and requesting cooperation
- If authors do not respond or decline to share materials, proceed with the best available information
- Document all communication; it may be relevant for the methods section
- Do NOT allow the original authors to control or veto your replication

---

## Phase 2: Protocol Development

**Duration: 2–4 weeks** | **Goal:** Develop a detailed replication protocol that is as faithful as possible to the original while being transparent about any deviations.

### Step 2.1: Original Study Deep Analysis

Before designing your replication, conduct a forensic-level analysis of the original study:

```
ORIGINAL STUDY ANALYSIS TEMPLATE:

1. RESEARCH QUESTION & HYPOTHESES
   - Exact research question stated
   - Exact hypotheses stated (directional or non-directional)
   - Theoretical framework invoked

2. PARTICIPANTS / SAMPLE
   - Population, sampling method, sample size
   - Demographic characteristics
   - Inclusion/exclusion criteria
   - How were participants recruited?
   - Compensation provided?

3. DESIGN
   - Between-subjects? Within-subjects? Mixed?
   - Number of conditions and their descriptions
   - Randomization procedure
   - Counterbalancing (if applicable)

4. MATERIALS / MEASURES
   - Stimuli (exact descriptions or examples)
   - Questionnaires (which ones, which version)
   - Equipment / software
   - Psychometric properties of measures

5. PROCEDURE
   - Step-by-step description of what participants experienced
   - Timing and sequencing
   - Instructions given to participants
   - Deception used (if any)

6. ANALYSIS
   - Statistical tests used
   - Software and version
   - Exclusion criteria for analysis
   - Covariates included
   - Multiple comparison correction

7. REPORTED RESULTS
   - Exact test statistics (F, t, χ², etc.)
   - Degrees of freedom
   - p-values
   - Effect sizes (if reported)
   - Confidence intervals (if reported)

8. IDENTIFIED CONCERNS
   - Methodological red flags
   - Unreported analyses
   - Potential p-hacking indicators
   - Unusually high effect sizes
   - Inconsistencies between reported N and df
```

### Step 2.2: Faithful Reproduction vs. Adapted Replication

One of the most important decisions in replication design is how closely to follow the original protocol:

**Faithful Reproduction (Recommended as default):**
- Reproduce the original study as closely as possible
- Any deviations are documented and justified
- Maximizes comparability with the original
- Strongest test of whether the finding replicates

**Adapted Replication (Use with caution):**
- Modify aspects of the original study to improve methodology
- Changes are explicitly documented and justified
- Risk: If replication fails, it's unclear whether the failure is due to the original finding being false or your modifications introducing a confound

**Decision Rule:** Start with faithful reproduction. Only deviate when:
1. The original method is clearly flawed (and the flaw could produce a false positive)
2. The original materials are unavailable (and cannot be recreated)
3. Ethical standards have changed since the original study
4. The population context has changed (e.g., technology used in the original is obsolete)

### Step 2.3: Deviation Documentation Protocol

For every deviation from the original protocol, document:

```
DEVIATION LOG:

Deviation # [N]:
ORIGINAL PROTOCOL: [Exact description from original paper]
MY PROTOCOL: [Exact description of my approach]
JUSTIFICATION: [Why this deviation is necessary]
EXPECTED IMPACT: [How this might affect results, if at all]
DIRECTION OF BIAS: [Could this deviation increase or decrease the likelihood of replication?]
```

**Critical principle:** Deviations that could decrease the likelihood of replication are MORE defensible than deviations that could increase it. If you deviate in a direction that makes replication easier and then find a "successful" replication, critics can argue the deviation explains the success rather than the finding being genuine.

### Step 2.4: Power Analysis for Replications

Power analysis for replications requires special consideration. The standard approach has important limitations:

**The Problem with Using Original Effect Sizes:**
Original studies typically overestimate effect sizes (due to publication bias, p-hacking, and winner's curse). Powering your replication based on the original effect size will often result in an underpowered replication.

**Recommended Approach:**

1. **Start with the original effect size** but assume it is inflated
2. **Apply a shrinkage factor** based on the evidence quality:
   - Large, well-conducted original study: shrink by 25%
   - Typical original study: shrink by 50%
   - Small original study with p just below .05: shrink by 75%
3. **Power for the shrunken effect size**, targeting power ≥ 0.90 (higher than the typical 0.80)
4. **Report both:** "We powered for d = 0.40 (50% shrinkage from original d = 0.80), requiring N = [X] for 90% power."

**Alternative: Smallest Effect Size of Interest (SESOI)**
Instead of powering for the expected effect, power for the smallest effect that would be scientifically meaningful:

```
"What is the smallest effect size that, if real, would matter
for theory or practice? Power the study to detect that effect."
```

This approach is often preferred because:
- It doesn't depend on the (likely inflated) original effect size
- It forces explicit discussion of what effect size matters
- It provides a clear criterion for interpreting results

### Step 2.5: Protocol Review

Before proceeding, have your protocol reviewed by:

1. **A methods expert** — Is the design sound? Is the power analysis appropriate?
2. **A subject matter expert** — Is the protocol faithful to the original? Are deviations justified?
3. **The original authors** (if willing) — Can they confirm accuracy or identify missing details?
4. **A skeptical colleague** — Would a reasonable critic accept this as a fair test?

---

## Phase 3: Pre-Registration

**Duration: 1 week** | **Goal:** Pre-register your replication protocol to maximize credibility and minimize flexibility.

### Why Pre-Registration Is ESSENTIAL for Replications

Pre-registration is always good practice, but for replications it is absolutely essential. Here's why:

1. **Credibility:** A pre-registered replication plan demonstrates that you did not alter your protocol after seeing the data
2. **Specificity:** Replications must specify in advance exactly what would constitute a "successful" replication
3. **Transparency:** Pre-registration makes your analytic decisions visible before data collection
4. **Fairness:** It protects you from accusations of bias — whether you find replication or not
5. **Distinguish confirmatory from exploratory:** Any analyses not in the pre-registration are clearly labeled exploratory

**Without pre-registration, a replication is merely another study with the same research question — not a rigorous test of the original finding.**

### Step 3.1: Replication Pre-Registration Content

Your pre-registration should include everything in a standard pre-registration PLUS the following replication-specific elements:

```
REPLICATION PRE-REGISTRATION TEMPLATE:

1. ORIGINAL STUDY
   - Full citation of the study being replicated
   - Brief summary of original finding
   - Original effect size and confidence interval

2. REPLICATION TYPE
   - Direct / Close / Conceptual / Extension
   - Justification for type chosen

3. REPLICATION CRITERIA
   - What constitutes a "successful" replication? (BE SPECIFIC)
     * Primary criterion: [e.g., p < .05 in same direction AND effect size within 50% of original]
     * Secondary criteria: [e.g., confidence interval overlap, equivalence test]
   - What constitutes a "failed" replication?
   - What constitutes an "ambiguous" replication?

4. DEVIATIONS FROM ORIGINAL
   - Complete list of deviations (from Deviation Log)
   - Justification for each
   - Expected impact of each

5. SAMPLE
   - Target sample size (with power analysis)
   - Population and recruitment method
   - Inclusion/exclusion criteria (same as original or modified?)

6. ANALYSIS PLAN
   - Primary analysis (must match original if direct replication)
   - Additional analyses (sensitivity, equivalence, Bayesian)
   - Handling of exclusions, outliers, missing data

7. DATA TRANSPARENCY
   - Will data be made publicly available? Where?
   - Will analysis code be shared? Where?
```

### Step 3.2: Defining Replication Success

One of the most consequential decisions in replication research is how to define "success." Different criteria can lead to different conclusions about the same data.

**Common Criteria for Replication Success:**

| Criterion | Definition | Strengths | Weaknesses |
|-----------|-----------|-----------|-----------|
| **Statistical significance** | p < .05 in same direction | Simple; widely understood | Binary; doesn't consider effect size; p-hackable original may not replicate at same N |
| **Effect size within range** | Replication effect size within X% of original | Considers magnitude | What X% is appropriate? Arbitrary |
| **Confidence interval overlap** | CI of replication overlaps original point estimate | Considers precision | Overlap is necessary but not sufficient |
| **Small telescopes** | Replication can detect effect at 75% of original | Tests whether original was adequately powered | Complex to explain |
| **Equivalence testing** | Can reject effect as large as original | Provides positive evidence of "no effect" | Requires large samples |
| **Bayesian** | Bayes factor supports same direction | Provides evidence for and against | Requires specifying prior |
| **Practical significance** | Effect size exceeds SESOI | Focuses on what matters | Requires defining SESOI |

**CRES Recommendation:** Use a multi-criteria approach. Report ALL of the above. Do not reduce replication assessment to a single binary judgment.

**Suggested reporting:**
```
"We assess replication success using multiple criteria:
1) Statistical significance (p < .05, same direction as original)
2) Effect size comparison (replication d relative to original d)
3) Confidence interval overlap (replication CI overlaps original point estimate)
4) Equivalence test (can we reject the original effect size?)
5) Bayesian analysis (Bayes factor for H1 vs. H0)
6) Practical significance (does the effect exceed our SESOI of d = [X]?)
No single criterion is definitive; the pattern across criteria
provides the most informative assessment."
```

---

## Phase 4: Execution

**Duration: Varies (4–16 weeks typical)** | **Goal:** Collect data and conduct analyses according to the pre-registered protocol.

### Step 4.1: Data Collection Protocol

**Principles for Replication Data Collection:**

1. **Follow the pre-registered protocol exactly** — This is non-negotiable for confirmatory analyses
2. **Document everything** — Record any procedural hiccups, deviations, or unexpected events
3. **Maintain data integrity** — Regular backups, clear naming conventions, version control
4. **Collect richer data than the original** — Additional measures allow for exploratory analyses that may explain replication success/failure
5. **Track participant flow** — Use CONSORT flow diagram to document recruitment, screening, enrollment, and attrition

### Step 4.2: Data Collection Monitoring

Set up monitoring checkpoints throughout data collection:

```
MONITORING SCHEDULE:

At 25% of target N:
□ Check data quality (response patterns, missing data rate)
□ Verify procedure is being followed
□ Do NOT look at results by condition (risk of bias)

At 50% of target N:
□ Check data quality again
□ Verify attrition rate is as expected
□ Do NOT look at results by condition

At 75% of target N:
□ Final data quality check
□ Prepare analysis code (but do NOT run on actual data)
□ Do NOT look at results by condition

At 100% of target N:
□ Final data quality check
□ Proceed to analysis per pre-registered plan
□ NOW you may look at results
```

**Critical rule:** Do not check results by condition until data collection is complete. This prevents optional stopping (collecting more data if results are "almost significant") and other forms of bias.

### Step 4.3: Analysis Execution

Execute analyses in this order:

1. **Pre-registered primary analysis** — Run exactly as specified, no deviations
2. **Pre-registered secondary analyses** — As specified
3. **Sensitivity analyses** — Test robustness of primary result
4. **Equivalence testing** — Can you reject the original effect size?
5. **Bayesian analysis** — What does the evidence say about H1 vs. H0?
6. **Exploratory analyses** — Clearly labeled as such; any analyses not in pre-registration

### Step 4.4: Handling Unexpected Results

**If the replication succeeds (finding replicates):**
- Report straightforwardly
- Compare effect sizes: Is the replication effect smaller? By how much?
- Note any deviations that might explain differences
- Discuss implications for the theoretical framework

**If the replication fails (finding does not replicate):**
- Do NOT immediately conclude the original finding is false
- Consider these alternative explanations systematically:

```
FAILED REPLICATION DIAGNOSTIC:

1. Power: Was the replication adequately powered?
   → If underpowered, the failure may be a Type II error

2. Fidelity: Were there any deviations from the original protocol?
   → If yes, the deviation may explain the failure

3. Sample: Was the replication sample comparable to the original?
   → Cultural, demographic, or temporal differences may moderate the effect

4. Context: Were there contextual factors that could suppress the effect?
   → Time of year, setting, experimenter characteristics, cultural shifts

5. Analysis: Was the analysis approach identical?
   → Different analytical choices can produce different results from the same data

6. Original study quality: Was the original study itself methodologically sound?
   → Small N, p-hacking, or QRPs in the original may explain the failure

7. Moderation: Is the effect moderated by unmeasured variables?
   → The effect may be real but conditional on specific factors
```

---

## Phase 5: Writing the Replication

**Duration: 3–4 weeks** | **Goal:** Write a replication report that is fair, transparent, and maximally informative.

### Step 5.1: Framing the Replication

The framing of your replication report is critical. Avoid these common pitfalls:

**Pitfall 1: The "Gotcha" Frame**
❌ "We show that [Author]'s finding is false."
✅ "We conducted an independent replication of [Finding]. The results [replicated/did not replicate], [with effect sizes X compared to original Y]."

**Pitfall 2: The "Equivalence" Frame**
❌ "We found the same thing as the original study."
✅ "Our replication produced an effect in the same direction as the original [d = X], though [smaller/larger/similar] in magnitude [original d = Y]."

**Pitfall 3: The "Null" Frame**
❌ "There was no effect."
✅ "The effect was not statistically significant [t(X) = Y, p = Z]. The 95% CI [lower, upper] was [consistent with/inconsistent with] the original effect size."

### Step 5.2: Replication Report Structure

Use this structure for your replication report:

```
1. ABSTRACT
   - State that this is a replication (in the first sentence)
   - Name the original study being replicated
   - State the replication type and sample size
   - Report the key result (with effect size comparison)
   - State the conclusion (replicated, not replicated, ambiguous)

2. INTRODUCTION
   - Describe the original finding and its significance
   - Explain why replication is needed
   - State your replication approach and criteria for success
   - Note any pre-registration (with DOI)

3. METHOD
   - Original study summary (brief)
   - Replication protocol (detailed)
   - Deviations from original (explicit, with justification)
   - Power analysis and sample size justification
   - Pre-registration details

4. RESULTS
   - Primary analysis (per pre-registration)
   - Effect size comparison with original
   - Confidence interval analysis
   - Equivalence test results
   - Bayesian analysis results
   - Sensitivity analyses
   - Exploratory analyses (clearly labeled)

5. DISCUSSION
   - Replication assessment (multi-criteria)
   - Comparison with original effect size
   - Possible explanations for any discrepancy
   - Implications for theory and practice
   - Limitations of the replication
   - Recommendations for future research

6. TRANSPARENCY STATEMENT
   - Pre-registration DOI
   - Data availability URL
   - Code availability URL
   - Materials availability
   - Deviations from pre-registration (if any)
   - Funding and conflicts of interest
```

### Step 5.3: Effect Size Comparison Best Practices

The comparison between original and replication effect sizes is the heart of your replication report. Present this comparison clearly and comprehensively:

**Required elements:**
1. Original effect size with CI
2. Replication effect size with CI
3. Visual comparison (forest plot or similar)
4. Percentage of original effect size reproduced
5. Formal test of whether the difference is significant
6. Whether the replication CI includes or excludes the original effect size

**Forest Plot Template:**

```
         Original Study    ●───────────────|───────────────    d = 0.80 [0.45, 1.15]
         Replication       ●─────────────────────|─────────    d = 0.35 [0.12, 0.58]
                            |----|----|----|----|----|----|
                           -0.5   0    0.5   1.0   1.5   2.0
                                                Effect Size (Cohen's d)
```

### Step 5.4: Tone and Language Guidelines

| Avoid | Instead Use | Reason |
|-------|-------------|--------|
| "Failed to replicate" | "Did not replicate" / "Effect was not statistically significant" | "Failed" implies the researchers failed; the effect may not exist |
| "Debunked" | "Not supported by replication evidence" | "Debunked" is overly aggressive |
| "Confirmed" | "Replicated" / "Consistent with original" | "Confirmed" implies certainty beyond what a single replication provides |
| "The effect is real/unreal" | "The evidence supports/does not support the effect" | Avoid metaphysical claims about reality |
| "The original study was wrong" | "The replication finding was inconsistent with the original" | Focus on the evidence, not on judging the authors |
| "Null result" | "Effect was not statistically significant" | "Null result" implies the null hypothesis is true |

---

## Phase 6: Publication Strategy

**Duration: 1–2 weeks** | **Goal:** Identify the optimal publication venue and strategy for your replication.

### Where Replications Get Published

| Venue | Acceptance Rate for Replications | Review Speed | Visibility | Best For |
|-------|----------------------------------|-------------|-----------|----------|
| **Registered Reports** | High (pre-accepted) | Slow (two-stage) | Moderate | Rigorous replications with clear criteria |
| **Replication-specific sections** | Moderate | Moderate | Moderate | Direct replications of important findings |
| **Original journal** | Variable | Slow-Moderate | High | Replications of that journal's own publications |
| **Field-specific journals** | Low-Moderate | Moderate | Moderate | Replications with extensions |
| **Interdisciplinary journals** | Low-Moderate | Moderate | High | Replications with broad significance |
| **Open access mega-journals** | High | Fast | Moderate | All replications that meet basic rigor standards |
| **Preprint servers** | N/A | Immediate | Variable | Rapid dissemination; priority establishment |

### The Registered Reports Strategy

Registered Reports are the gold standard for replication publication. In this format:

1. **Stage 1:** Submit your introduction, methods, and analysis plan before data collection
2. **Peer review of the plan:** Reviewers evaluate the question and methodology, not the results
3. **In-principle acceptance:** If the plan is sound, the journal commits to publishing regardless of results
4. **Stage 2:** After data collection, submit the completed manuscript
5. **Final review:** Reviewers verify you followed the approved protocol; results are irrelevant to acceptance

**Advantages:**
- Eliminates publication bias (null results are published)
- Pre-commitment to methodology reduces flexibility
- High credibility — reviewers can't reject based on unwanted results
- Growing number of journals offer this format

**Journals offering Registered Reports for replications:**
- Comprehensive Results in Social Psychology
- Journal of Experimental Social Psychology (replication section)
- Advances in Methods and Practices in Psychological Science
- Royal Society Open Science
- Many journals across disciplines now offer this format

### Publication Strategy Decision Tree

```
Is the original study highly cited (>100 citations)?
├── YES
│   └── Is a Registered Report option available?
│       ├── YES → Submit as Registered Report (best option)
│       └── NO → Submit to original journal or high-visibility journal
└── NO
    └── Does the replication include a meaningful extension?
        ├── YES → Submit to field-specific journal as "Replication + Extension"
        └── NO → Submit to open access mega-journal or preprint
```

---

## Statistical Considerations for Replications

### Power Analysis for Replications

As discussed in Phase 2, power analysis for replications requires special care. Here is a more detailed treatment.

**The "Small Telescopes" Approach (Simonsohn, 2015)**

Simonsohn proposed that a replication should be powered to detect the smallest effect size that the original study could have reliably detected (75% power for 33% of the reported effect). This ensures that if the replication fails, it's not because the study was underpowered relative to the original.

```
SMALL TELESCOPES CALCULATION:
1. From original study: N_original, reported effect size d_original
2. Compute: d_33% = d_original × 0.33 (the effect the original had 33% power to detect)
3. Power the replication for d_33% at 90% power
4. This typically requires N_replication ≈ 2.5 × N_original
```

### Equivalence Testing

Equivalence testing provides a principled way to claim that an effect is "practically zero" — something standard null hypothesis testing cannot do.

**Procedure:**
1. Define a smallest effect size of interest (SESOI) — the smallest effect that would matter
2. Set up equivalence bounds: [-SESOI, +SESOI]
3. Test whether the observed effect falls within these bounds
4. If the 90% CI falls entirely within the equivalence bounds, you can claim the effect is practically zero

```
EQUIVALENCE TEST TEMPLATE:
"Using a SESOI of d = [X], we conducted a two one-sided test (TOST)
for equivalence. The observed effect was d = [Y], 90% CI [lower, upper].
The CI [fell entirely within / did not fall entirely within] the
equivalence bounds of [-X, +X], [providing / failing to provide]
evidence that the effect is practically equivalent to zero."
```

### Bayesian Analysis for Replications

Bayesian analysis provides evidence for both H1 and H0, avoiding the asymmetry of frequentist testing.

**Recommended approach:**
1. Use a Bayes factor (BF) to quantify evidence for H1 vs. H0
2. Use a prior centered on the original effect size (or a more conservative prior)
3. Interpret the BF using standard guidelines:
   - BF > 10: Strong evidence for H1
   - BF 3–10: Moderate evidence for H1
   - BF 1/3–3: Inconclusive
   - BF 1/10–1/3: Moderate evidence for H0
   - BF < 1/10: Strong evidence for H0

```
BAYESIAN ANALYSIS TEMPLATE:
"Using a Cauchy prior (scale = [X]) centered at the original effect
size (d = [Y]), the Bayes factor was BF₁₀ = [Z]. This constitutes
[strong/moderate/anecdotal] evidence [for/against] the hypothesis
relative to the null."
```

### Meta-Analytic Thinking

Always situate your replication in the context of all available evidence:

1. **Combine your replication with the original study** in a mini-meta-analysis
2. **Search for other replications** of the same finding
3. **Report the cumulative evidence** — what does the total evidence base suggest?
4. **Compute a meta-analytic effect size** across original + all replications

---

## When a "Failed" Replication Is Actually a Contribution

### The Value of Non-Replication

A "failed" replication (one that does not reproduce the original finding) is a valuable scientific contribution when it is:

1. **Well-powered:** Adequately powered to detect the original effect (or a meaningful fraction of it)
2. **Pre-registered:** Analysis plan specified in advance
3. **Transparent:** All data, code, and materials publicly available
4. **Fair:** Protocol faithfully reproduces the original study
5. **Carefully interpreted:** Considers alternative explanations beyond "the original was wrong"

### Reframing "Failed" Replications

| "Failed" Finding | Reframe | Interpretation |
|-------------------|---------|---------------|
| Effect not significant | Effect size is smaller than originally reported | The original likely overestimated the effect |
| Effect in opposite direction | Boundary condition identified | The effect may be moderated by context |
| Effect significant but much smaller | Effect exists but is weaker than claimed | Theoretical and practical implications need recalibration |
| Effect present in some subgroups only | Moderation discovered | The effect is conditional, not universal |
| Effect entirely absent | Strong evidence against the original claim | The original finding may be a false positive |

### When Non-Replication Reveals New Knowledge

Some of the most important discoveries in science have come from failed replications:

- **New boundary conditions:** The failure reveals where the effect holds and where it doesn't
- **Moderator identification:** Systematic variation in replication success reveals moderating variables
- **Methodological insight:** The failure reveals which aspects of the method are essential vs. incidental
- **Theoretical refinement:** The failure forces theory revision, leading to more accurate models
- **Hidden assumptions:** The failure reveals assumptions that were invisible in the original context

---

## Extension Strategies

### How to Add Value Beyond Pure Replication

The most publishable and impactful replications combine verification with extension. Here are strategies for adding value:

#### Strategy 1: Boundary Testing

Add conditions that test the limits of the original finding:

```
ORIGINAL: Effect X observed in college students
EXTENSION: + Add older adult sample
           + Add clinical population
           + Add cross-cultural sample
CONTRIBUTION: Tests generalizability + replicates original
```

#### Strategy 2: Mechanism Elucidation

Add measures or conditions that test WHY the effect occurs:

```
ORIGINAL: Treatment A reduces anxiety
EXTENSION: + Add mediators (cognitive, behavioral, physiological)
           + Test whether mediators account for the effect
CONTRIBUTION: Replicates effect + explains mechanism
```

#### Strategy 3: Moderator Discovery

Add variables that might moderate the original effect:

```
ORIGINAL: Framing effect on decision-making
EXTENSION: + Add individual difference measures (cognitive style, expertise)
           + Test whether the effect varies by individual differences
CONTRIBUTION: Replicates effect + identifies who it works for
```

#### Strategy 4: Methodological Improvement

Replicate using improved methodology:

```
ORIGINAL: Small-sample study with methodological limitations
EXTENSION: + Larger sample (adequately powered)
           + Pre-registered analysis plan
           + Improved measures (validated, multi-item)
           + Active control condition
CONTRIBUTION: More rigorous test + replicates with better methods
```

#### Strategy 5: Longitudinal Extension

Test whether the effect persists over time:

```
ORIGINAL: Immediate effect of intervention
EXTENSION: + Add follow-up assessments (1 week, 1 month, 6 months)
           + Test durability of the effect
CONTRIBUTION: Replicates effect + tests persistence
```

#### Strategy 6: Dose-Response Extension

Test the effect at different intensities:

```
ORIGINAL: Effect observed at one dosage/intensity level
EXTENSION: + Test multiple dosage levels
           + Map dose-response curve
CONTRIBUTION: Replicates effect + characterizes dose-response relationship
```

---

## Multi-Lab Replication Protocols

### When to Pursue Multi-Lab Replication

Multi-lab replications are the gold standard for resolving controversial findings. Consider this approach when:

- The original finding is highly influential (cited 500+ times)
- Existing evidence is conflicting (some replications succeed, others fail)
- The finding is controversial (active debate in the literature)
- Single-lab replication is insufficient to resolve the question
- You want to estimate between-site variability

### Multi-Lab Replication Structure

```
COORDINATION STRUCTURE:

Lead Lab: [Responsible for overall coordination, protocol, analysis]
Participating Labs: [2–20+ labs running the same protocol]

Protocol Development:
1. Lead lab develops draft protocol
2. All participating labs review and suggest modifications
3. Consensus protocol finalized
4. Pre-registration as a multi-site study

Data Collection:
1. Each lab collects data from local sample
2. Each lab follows identical protocol (with site-specific adaptations documented)
3. Data reported to lead lab in standardized format

Analysis:
1. Primary analysis: Meta-analytic combination across sites
2. Between-site heterogeneity assessment
3. Moderator analysis: Which site characteristics predict replication success?
4. Pooled effect size with prediction interval

Publication:
1. Joint authorship (all contributing labs)
2. Published as a single paper or registered report
```

### Key Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| **Protocol heterogeneity** | Extremely detailed protocol document; video training; practice sessions |
| **Data quality across sites** | Standardized data format; automated quality checks; regular communication |
| **Differential attrition** | Minimum sample size per site; report and analyze attrition differences |
| **Authorship disputes** | Agree on authorship model before data collection (CRediT) |
| **Timeline coordination** | Set data collection window; regular progress updates; realistic milestones |
| **Analysis disputes** | Pre-specify primary analysis; agree on decision rules before data collection |

---

## Dealing with Original Authors

### Proactive Engagement

The best approach is proactive, respectful engagement:

1. **Before replication:** Inform original authors of your plans; request materials
2. **During replication:** Share protocol for verification; ask questions about ambiguous procedures
3. **Before publication:** Share results with original authors; invite their commentary
4. **At publication:** Acknowledge their cooperation; frame findings fairly

### When Original Authors Are Cooperative

If original authors are cooperative:
- Request their materials, code, and any unpublished details
- Ask them to review your protocol for accuracy
- Consider inviting them to co-author (especially for extensions)
- Give them advance notice of results before publication

### When Original Authors Are Hostile or Unresponsive

If original authors are hostile or unresponsive:
- Document your attempts to contact them (dates, methods, responses)
- Proceed with the best available information from the published report
- Be extra careful about protocol fidelity (no room for critics to claim your replication was unfair)
- Frame your findings carefully and neutrally
- Be prepared for public criticism; have your documentation in order
- Consider offering the original authors space for a commentary alongside your replication

### Responding to Criticism from Original Authors

Common criticisms and how to respond:

| Criticism | Response |
|-----------|----------|
| "Your sample was different" | Document sample differences; test whether they moderate the effect; report demographic details |
| "You didn't follow our protocol exactly" | Document all deviations; justify each; report analyses showing deviations don't explain the result |
| "The effect is real but moderated by [variable]" | Test the proposed moderator if possible; acknowledge this possibility in discussion |
| "You're just trying to tear down our work" | Frame your replication as a service to the field, not an attack on individuals |
| "One replication failure doesn't mean the effect isn't real" | Agree; call for further replications; present your finding as one data point |
| "You must have done something wrong" | Invite them to specify what; offer to share materials and data; propose collaboration on a follow-up |

---

## Making Your Replication Maximally Useful

### Principles of Maximum Usefulness

A maximally useful replication is one that other researchers can:

1. **Trust** — Pre-registered, transparent, well-powered
2. **Understand** — Clear presentation of methods, analyses, and results
3. **Build on** — Data and code available; extensions suggested
4. **Contextualize** — Situated within the broader evidence base
5. **Apply** — Practical implications clearly stated

### The Usefulness Checklist

- [ ] Pre-registered with detailed analysis plan
- [ ] All data publicly available in open repository
- [ ] All analysis code publicly available and documented
- [ ] All materials publicly available (stimuli, questionnaires, codebooks)
- [ ] Effect sizes reported with confidence intervals
- [ ] Multiple criteria for replication success assessed
- [ ] Comparison to original effect size with visual display
- [ ] Bayesian analysis reported
- [ ] Equivalence testing reported
- [ ] Mini-meta-analysis combining original + replication
- [ ] Deviations from original protocol documented and justified
- [ ] Limitations honestly acknowledged
- [ ] Future research directions specified
- [ ] Relationship with original authors described
- [ | Registered Report format used (if available)

---

## Replication Reporting Standards

### CREED Standards (Collaborative Replication and Education in Enterprise Development)

The CREED framework provides standards for reporting replications. Key elements:

1. **Study identification:** Full citation of original study; DOI
2. **Replication type:** Direct, close, conceptual, extension
3. **Pre-registration:** DOI and platform
4. **Power analysis:** Justification for sample size
5. **Protocol fidelity:** Deviations documented
6. **Results comparison:** Side-by-side with original
7. **Data availability:** Repository URL and DOI
8. **Code availability:** Repository URL and DOI

### Replication Markers

Proposed standard markers that should appear in every replication report:

```
╔══════════════════════════════════════════════════════╗
║              REPLICATION MARKERS                      ║
╠══════════════════════════════════════════════════════╣
║ Original Study:     [Citation]                        ║
║ Replication Type:   [Direct/Close/Conceptual/Extension]║
║ Pre-registered:     [Yes/No] [DOI]                    ║
║ Power (1-β):        [Value] for d = [Value]           ║
║ Sample Size:        [N] (original: [N])               ║
║ Effect Size:        d = [X] (original: d = [Y])       ║
║ Statistical Sig.:   p = [X] (original: p = [Y])       ║
║ CI Overlap:         [Yes/No]                          ║
║ Equivalence Test:   [Significant/Not Significant]     ║
║ Bayes Factor:       BF₁₀ = [X]                       ║
║ Replication Verdict: [Successful/Ambiguous/Failed]    ║
║ Data Available:     [URL]                             ║
║ Code Available:      [URL]                            ║
║ Materials Available: [URL]                            ║
╚══════════════════════════════════════════════════════╝
```

### Reporting Template for Key Statistics

```
PRIMARY RESULT:
Original: t(df₁) = X.XX, p = .XXX, d = X.XX, 95% CI [X.XX, X.XX]
Replication: t(df₂) = X.XX, p = .XXX, d = X.XX, 95% CI [X.XX, X.XX]

EFFECT SIZE COMPARISON:
Original d = X.XX vs. Replication d = X.XX
Difference: Δd = X.XX
Replication effect is [X%] of original effect size

CONFIDENCE INTERVAL OVERLAP:
Original 95% CI [X.XX, X.XX]
Replication 95% CI [X.XX, X.XX]
Replication CI [includes/excludes] original point estimate

EQUIVALENCE TEST (SESOI = d 0.XX):
TOST: t(df) = X.XX, p = .XXX
90% CI [X.XX, X.XX] [falls/does not fall] within equivalence bounds

BAYES FACTOR:
BF₁₀ = X.XX ([strong/moderate/anecdotal] evidence [for/against] H₁)
Prior: Cauchy(scale = X.XX)

META-ANALYTIC COMBINATION:
Pooled d = X.XX, 95% CI [X.XX, X.XX]
Heterogeneity: Q = X.XX, p = .XXX, I² = XX%
Prediction interval: [X.XX, X.XX]
```

---

## Replication Workflow Timeline Summary

| Phase | Duration | Key Activities | Key Output |
|-------|----------|----------------|------------|
| 1. Target Selection | 1–2 weeks | Literature scan, priority assessment, feasibility check | Selected target study |
| 2. Protocol Development | 2–4 weeks | Original study analysis, protocol design, deviation documentation | Complete replication protocol |
| 3. Pre-Registration | 1 week | Write and submit pre-registration | Pre-registration DOI |
| 4. Execution | 4–16 weeks | Data collection, analysis, monitoring | Complete results |
| 5. Writing | 3–4 weeks | Replication report drafting, effect size comparison, framing | Replication manuscript |
| 6. Publication Strategy | 1–2 weeks | Venue selection, submission preparation | Submitted replication |
| **Total** | **12–29 weeks** | | |

---

*Replication is not the enemy of originality — it is its foundation. A science that cannot verify its own findings is a science built on sand. By conducting rigorous, transparent replications, you are performing one of the most important services a researcher can provide: ensuring that the knowledge we build upon is solid enough to support the structures we place on top of it.*

**CRES Replication Study Workflow v1.0** | Part of the Claude Research Excellence System
