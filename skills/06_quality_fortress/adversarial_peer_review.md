# Adversarial Peer Review Simulation Guide

## Purpose
This guide provides a systematic methodology for simulating realistic peer review before manuscript submission. By running an adversarial review simulation, you identify and fix problems that reviewers would otherwise catch — on your terms, on your timeline, without the stress of actual rejection.

---

## 1. How to Run a Realistic Peer Review Simulation

### Step-by-Step Protocol

**Step 1: Cooling Period (Minimum 48 hours)**
After completing the manuscript, set it aside for at least 48 hours. Fresh eyes catch problems that fatigued eyes normalize. During this period, do not read or edit the manuscript.

**Step 2: Role Assignment**
Assign (or mentally adopt) five distinct reviewer personas (see Section 2). Each persona brings a different adversarial lens. Do not attempt to review from all perspectives simultaneously — switch fully between personas.

**Step 3: First Read (Holistic Impression)**
Read the entire manuscript once without stopping to make notes. After reading, write a single paragraph answering: "What is this paper's single most important claim, and am I convinced by it?" If you cannot state the claim clearly, the paper has a clarity problem.

**Step 4: Structured Review by Persona**
Work through each reviewer persona using the questions and criteria defined in the SKILL.md. For each persona:
- Read the manuscript from that reviewer's perspective
- Answer every question explicitly
- Assign a verdict category
- List specific issues with location, severity, and required fix

**Step 5: Conflict Resolution**
When reviewers disagree (e.g., Methodologist says "PASS" but Logician says "FATAL FLAW"), resolve by determining which reviewer's domain is more critical for the specific paper. Methodological flaws trump all others; logical flaws trump communication issues.

**Step 6: Synthesis**
Compile the Priority-Ordered Fix List using the Synthesis Report Template. Ensure every issue from every reviewer appears in the list, with the highest-severity version taking priority.

**Step 7: Fix and Re-Check**
Fix issues in priority order. After fixing, re-run the relevant reviewer persona to verify the fix resolved the issue without creating new problems.

---

## 2. Reviewer Persona Construction Methodology

### The BELIEF Method for Constructing Reviewer Personas

**B — Background**: What is this reviewer's disciplinary training? What methods do they trust? What methods do they distrust?

**E — Epistemic Values**: What does this reviewer consider good evidence? (Large N? Replication? Preregistration? Ecological validity?)

**L — Literature Knowledge**: What literature does this reviewer know deeply? What citations would they expect to see?

**I — Irritations**: What pet peeves does this reviewer have? (Passive voice? Missing effect sizes? Overclaiming? Bar charts?)

**E — Evaluation Style**: How does this reviewer read? (Linear? Abstract-first? Methods-first? Figures-only?)

**F — Fairness Threshold**: How much benefit of the doubt does this reviewer give? (Charitable? Neutral? Hostile?)

### Constructing Specific Reviewer Personas

**The Statistics Traditionalist**
- Background: Quantitative psychology, biostatistics
- Epistemic values: Large N, preregistration, robust replication
- Irritations: Missing CIs, p-hacking, stepwise regression, one-tailed tests
- Fairness: Neutral — gives credit for good methods, penalizes sloppy ones
- What they always check: Assumption tests, effect sizes, multiple comparison correction

**The Theory Purist**
- Background: Theoretical psychology, philosophy of science
- Epistemic values: Clear theoretical mechanism, falsifiable predictions
- Irritations: Data-driven hypotheses, post-hoc storytelling, "more research is needed"
- Fairness: Charitable to good theory, hostile to atheoretical empiricism
- What they always check: Are hypotheses derived from theory? Is the mechanism specified?

**The Clinical Pragmatist**
- Background: Clinical psychology, medicine, public health
- Epistemic values: Clinical significance, effect sizes in context, NNT
- Irritations: Statistically significant but clinically meaningless effects
- Fairness: Neutral — wants to know if this helps patients
- What they always check: Clinical significance metrics, practical implications, generalizability to real settings

**The Methodological Skeptic**
- Background: Open science, meta-science, reproducibility
- Epistemic values: Preregistration, open data, replication, robustness
- Irritations: Undisclosed flexibility, HARKing, selective reporting
- Fairness: Hostile — assumes the worst until proven otherwise
- What they always check: Preregistration compliance, analytic flexibility, alternative specifications

**The Interdisciplinary Browser**
- Background: Adjacent field (e.g., economics reviewing psychology)
- Epistemic values: Causal identification, natural experiments, instrumental variables
- Irritations: Overclaiming from correlational data, omitted variable bias
- Fairness: Charitable to interesting ideas, hostile to causal overclaiming
- What they always check: Identification strategy, confound controls, alternative explanations

---

## 3. Escalating Review Intensity Levels

### Level 1: Constructive Review (Standard)
- Identify the most important strengths and weaknesses
- Provide specific, actionable feedback
- Focus on the 3-5 most critical issues
- Tone: Professional, helpful, assumes best intentions
- Time: 60-90 minutes

### Level 2: Rigorous Review (Recommended)
- Identify ALL strengths and weaknesses, including minor ones
- Provide detailed feedback on every section
- Check every statistical claim against the reported results
- Tone: Professional but demanding, does not accept weak claims
- Time: 2-3 hours

### Level 3: Adversarial Review (For High-Stakes Submissions)
- Actively try to find reasons to reject the paper
- Challenge every assumption, every claim, every conclusion
- Generate the strongest possible counter-arguments to each finding
- Tone: Hostile but fair — like the worst reviewer you might encounter
- Time: 3-5 hours

### Level 4: Destroy Review (For Science/Nature/Lancet Submissions)
- Assume the paper is wrong until proven otherwise
- Look for the single fatal flaw that would cause rejection
- Check whether the same conclusion could be reached by trivially different analyses
- Simulate what a competitor would say to dismiss this work
- Tone: Maximal skepticism, zero benefit of the doubt
- Time: 5-8 hours

---

## 4. Field-Specific Review Criteria

### Psychology / Social Sciences
| Criterion | Weight | Key Questions |
|---|---|---|
| Internal validity | 30% | Are confounds controlled? Is causal inference justified? |
| Statistical rigor | 25% | Correct tests? Assumptions met? Effect sizes reported? |
| Theoretical contribution | 20% | Does it advance theory? Is mechanism specified? |
| External validity | 15% | Generalizability? Ecological validity? |
| Clarity and writing | 10% | Is the argument clear? Is the paper readable? |

### Medicine / Clinical Research
| Criterion | Weight | Key Questions |
|---|---|---|
| Clinical significance | 30% | Does this matter for patients? NNT? Absolute risk reduction? |
| Study design | 25% | RCT? Blinding? Allocation concealment? |
| Statistical analysis | 20% | Intention-to-treat? Multiplicity? |
| Ethical considerations | 15% | IRB? Informed consent? Data safety? |
| Generalizability | 10% | Real-world applicability? Diverse sample? |

### Computational / Quantitative
| Criterion | Weight | Key Questions |
|---|---|---|
| Methodological innovation | 30% | Is the method new or a standard application? |
| Validation | 25% | Out-of-sample? Cross-validation? Baseline comparison? |
| Reproducibility | 20% | Code available? Random seeds? Version pinned? |
| Theoretical grounding | 15% | Why this model? Why these parameters? |
| Scalability and robustness | 10% | Does it scale? Is it robust to hyperparameters? |

### Economics / Political Science
| Criterion | Weight | Key Questions |
|---|---|---|
| Causal identification | 35% | Is the identification strategy credible? Endogeneity addressed? |
| Data quality | 20% | Measurement error? Sample selection? |
| Robustness | 20% | Alternative specifications? Sensitivity to assumptions? |
| Theoretical contribution | 15% | Does it test or refine economic theory? |
| Policy relevance | 10% | Are implications actionable? |

---

## 5. Quantitative Scoring Rubric for Each Dimension

### Scale: 1-7 (1 = Fatal flaw; 7 = Excellence)

| Score | Label | Description |
|---|---|---|
| 7 | Excellent | No concerns; could serve as a model for the field |
| 6 | Very Good | Minor concerns that do not affect conclusions |
| 5 | Good | Minor concerns; a few improvements would strengthen |
| 4 | Adequate | Moderate concerns; several improvements needed |
| 3 | Below Standard | Major concerns that affect interpretation |
| 2 | Problematic | Serious concerns; conclusions may not hold |
| 1 | Fatal | Fundamental flaws invalidate the work |

### Dimension Scores

| Dimension | Score | Threshold |
|---|---|---|
| Methodological rigor | ___ / 7 | Must be ≥ 5 for submission |
| Statistical analysis | ___ / 7 | Must be ≥ 5 for submission |
| Literature positioning | ___ / 7 | Must be ≥ 4 for submission |
| Logical coherence | ___ / 7 | Must be ≥ 5 for submission |
| Clarity of writing | ___ / 7 | Must be ≥ 4 for submission |
| Impact / contribution | ___ / 7 | Must be ≥ 4 for submission |
| Reproducibility | ___ / 7 | Must be ≥ 4 for submission |

**Submission rule**: If ANY dimension scores below threshold, do NOT submit until that dimension is raised above threshold.

---

## 6. How to Prioritize and Address Reviewer Feedback

### The Impact-Effort Matrix

|  | Low Effort | High Effort |
|---|---|---|
| **High Impact** | Quick Wins (Do immediately) | Major Projects (Schedule and execute) |
| **Low Impact** | Polish (Do if time permits) | Deprioritize (Skip unless required) |

### Priority Decision Rules

1. **Fatal flaws**: Fix immediately, regardless of effort. No paper with a fatal flaw should be submitted.

2. **Multiple reviewer agreement**: When 2+ reviewers flag the same issue, it is almost certainly real. Fix it.

3. **Methodologist + Logician overlap**: When these two agree on a problem, it is a design or inference issue that will be caught by real reviewers. Fix it.

4. **Communicator-only issues**: These are important but can be batched and fixed in a single editing pass.

5. **Impact Assessor concerns**: These are strategic, not tactical. They may require reframing rather than fixing.

### Feedback Response Template

For each piece of feedback:
1. **Restate the concern** in your own words (ensures you understood it)
2. **Assess validity** (is the concern legitimate? Most are.)
3. **Determine the fix** (what specific change addresses the concern?)
4. **Implement the fix** (make the change)
5. **Verify the fix** (re-read the relevant section; does the concern no longer apply?)
6. **Document the fix** (note what was changed and why, for your revision tracking)

---

## 7. Revision Tracking Methodology

### The Revision Log

Maintain a structured log of all changes made in response to the simulated review:

| ID | Reviewer | Issue | Severity | Fix Applied | Section Changed | Verification |
|---|---|---|---|---|---|---|
| R1-01 | Methodologist | Missing assumption check | Major | Added Shapiro-Wilk test | Methods | ✓ Re-ran analysis |
| R3-02 | Logician | Overclaiming causation | Major | Changed "caused" to "predicted" | Discussion P2 | ✓ Claim calibrated |
| R4-03 | Communicator | Undefined jargon | Minor | Defined "IAT" on first use | Introduction | ✓ Added definition |

### Version Control

- Save each major revision as a separate file: `manuscript_v1.docx`, `manuscript_v2.docx`
- Use track changes for the revision between versions
- Keep a master change log that maps reviewer concerns to specific revisions
- After all fixes, produce a clean version without tracked changes

### The Pre-Submission Checklist

Before submitting, verify:
- [ ] All fatal flaws are resolved
- [ ] All Priority 1 fixes are implemented and verified
- [ ] At least 80% of Priority 2 fixes are implemented
- [ ] The revision log is complete
- [ ] A final read-through reveals no new issues introduced by fixes
- [ ] All reviewer dimension scores are above threshold
- [ ] The paper has been read by at least one person not involved in writing it

---

## 8. Common Reviewer Objections and Preemptive Strategies

### Objection: "The sample is too small"
**Preemptive strategy**: Conduct and report a sensitivity analysis showing what effect sizes your sample can detect with 80% power. If you found significant effects, N was sufficient for detection. If null, acknowledge the power limitation.

### Objection: "This is just a replication with a twist"
**Preemptive strategy**: In the introduction, explicitly state how your study extends prior work. Use the Extension template: "While [Prior Study] showed X, we extend this by [specific new contribution]."

### Objection: "The effect is statistically significant but practically meaningless"
**Preemptive strategy**: Report and interpret effect sizes against practical benchmarks. If the effect is small, discuss its accumulated impact or theoretical significance independent of practical size.

### Objection: "There are unmeasured confounds"
**Preemptive strategy**: Acknowledge plausible confounds in the limitations section. State the direction of bias each confound would produce. If possible, conduct a sensitivity analysis (E-value) showing how strong a confound would need to be to explain away the effect.

### Objection: "The design cannot support causal claims"
**Preemptive strategy**: Match language to design. If observational, use "associated with" and "predicted" — never "caused" or "produced." If you want to make stronger claims, explain what design features support them (temporal precedence, controls, instrumental variables).

### Objection: "The findings would not replicate"
**Preemptive strategy**: If preregistered, note this. If not, acknowledge the need for replication. Report robustness checks. If the effect is large and theory-predicted, replication likelihood is higher.

### Objection: "The novelty is insufficient"
**Preemptive strategy**: State the specific contribution in the first sentence of the Discussion. Use precise language: "identifies the mechanism," "establishes the boundary condition," "resolves the debate between X and Y." Vague claims of novelty invite dismissal.

### Objection: "The methods section is incomplete"
**Preemptive strategy**: Use the Methods Precision template (Skill 05). Ensure every variable, every procedure, every analysis is described with enough detail for exact replication. Link to OSF for supplementary materials.
