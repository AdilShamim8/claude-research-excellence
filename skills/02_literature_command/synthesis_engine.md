# Synthesis Engine

## A Multi-Method Framework for Literature Synthesis

### Purpose
This prompt provides a comprehensive methodology for synthesizing research literature across multiple dimensions — thematic, chronological, methodological, and theoretical. It moves beyond summary to genuine integration, revealing patterns, resolving contradictions, and generating new research questions from the synthesis itself.

---

## SECTION 1: THEMATIC SYNTHESIS METHODOLOGY

### When to Use
Thematic synthesis is the default approach for most literature reviews. It organizes findings by conceptual theme rather than by study, enabling pattern recognition across studies.

### Procedure

**Step 1: Code Generation**
- Read each included study and extract all findings as discrete statements
- Label each finding with a descriptive code (line-by-line coding)
- Codes should be close to the original text (not interpretive at this stage)
- Example: If a study reports "participants reported feeling overwhelmed by the volume of information," the code is "information overload — feeling overwhelmed"

**Step 2: Descriptive Theme Development**
- Group related codes into descriptive themes
- Descriptive themes organize the codes without reinterpreting them
- Example: Codes "information overload," "too many choices," "decision paralysis" → Descriptive theme: "Cognitive overload from abundance"

**Step 3: Analytical Theme Development**
- Go beyond the original studies to generate analytical themes that interpret and explain
- Analytical themes represent your synthesis contribution — they say something the original studies did not say individually
- Example: Descriptive theme "Cognitive overload from abundance" → Analytical theme: "The paradox of information access, where more information availability reduces decision quality, suggesting a curvilinear rather than linear relationship between information and performance"

**Step 4: Theme Validation**
- Check that each analytical theme is supported by evidence from multiple studies (not just one)
- Verify that no study's findings are forced into a theme where they don't fit
- Identify "orphan findings" that don't fit any theme — these may represent nascent themes or genuine outliers

### Thematic Synthesis Quality Criteria

| Criterion | Standard |
|-----------|----------|
| **Coverage** | Every included study contributes to at least one theme |
| **Coherence** | Studies within a theme share a meaningful conceptual link |
| **Distinctiveness** | Themes are conceptually distinct; no significant overlap |
| **Depth** | Each theme is developed with sub-themes, examples, and nuance |
| **Evidence** | Each theme is supported by multiple studies (minimum 3) |
| **Interpretation** | Analytical themes go beyond description to explain or theorize |

---

## SECTION 2: CHRONOLOGICAL SYNTHESIS METHODOLOGY

### When to Use
Chronological synthesis is appropriate when the field has undergone significant evolution over time, and understanding the trajectory of ideas is essential for interpreting current knowledge.

### Procedure

**Step 1: Period Demarcation**
- Identify natural breakpoints in the literature based on:
  - Methodological shifts (e.g., from behavioral to neuroimaging methods)
  - Theoretical revolutions (e.g., from behaviorism to cognitivism)
  - Technological enablers (e.g., introduction of fMRI, internet surveys, LLMs)
  - Key publications that changed the field's direction
- Name each period descriptively (not just "Phase 1" and "Phase 2")

**Step 2: Period Analysis**
For each period, document:
- **Dominant questions:** What were researchers trying to answer?
- **Available methods:** What tools and approaches were available?
- **Key findings:** What was established during this period?
- **Limitations recognized:** What problems did researchers identify?
- **Unresolved questions:** What carried forward to the next period?
- **Transition catalyst:** What triggered the shift to the next period?

**Step 3: Trajectory Mapping**
- Connect the periods: How did the limitations of one period drive the advances of the next?
- Identify accelerating trends: Are the intervals between major shifts getting shorter?
- Identify stagnation periods: Were there eras where progress stalled? Why?
- Identify parallel developments: Were there concurrent but non-interacting research streams that should have converged earlier?

**Step 4: Forward Projection**
- Based on the trajectory, what is the field moving toward?
- What current limitations are likely to drive the next shift?
- What methodological or theoretical developments might accelerate progress?

### Chronological Synthesis Output Template

```markdown
## Chronological Synthesis: [FIELD]

### Period 1: [NAME] ([YEARS])
- **Dominant Question:** [What researchers asked]
- **Methods Available:** [What tools they had]
- **Key Findings:** [What was established]
- **Recognized Limitations:** [What they knew they didn't know]
- **Transition Catalyst:** [What triggered the next period]

### Period 2: [NAME] ([YEARS])
[Same structure]

### Period 3: [NAME] ([YEARS])
[Same structure]

### Trajectory Analysis
- **Pattern:** [Accelerating / Linear / Stagnating]
- **Key Inflection Points:** [When and why the field changed direction]
- **Current Trajectory:** [Where the field is heading]
- **Predicted Next Shift:** [What will likely drive the next period]
```

---

## SECTION 3: METHODOLOGICAL SYNTHESIS METHODOLOGY

### When to Use
Methodological synthesis is appropriate when the field's findings are inconsistent and the inconsistency may be driven by methodological differences across studies. It is also valuable when planning a new study to determine the optimal methodology.

### Procedure

**Step 1: Method Classification**
Classify each study by:
- **Design type:** Experimental, quasi-experimental, observational, qualitative, mixed methods
- **Sample characteristics:** Size, population, recruitment method
- **Measurement approach:** Self-report, behavioral, physiological, observational
- **Analytical strategy:** Statistical tests, corrections applied, effect sizes reported
- **Study quality:** Risk of bias rating

**Step 2: Method-Effect Contingency Analysis**
- Group studies by methodological characteristics
- Compare findings across groups: Do studies with similar methods produce similar results?
- Identify methodological features that systematically co-vary with findings
- Example: Do self-report studies find larger effects than behavioral studies? Do studies with student samples find different effects than clinical samples?

**Step 3: Methodological Strength-Weakness Mapping**
For each methodological approach used in the literature:
- **What it measures well:** The constructs and relationships it captures most validly
- **What it misses:** The constructs and relationships it cannot detect or systematically distorts
- **Known artifacts:** Biases and confounds associated with this approach
- **Complementary methods:** Other approaches that compensate for its weaknesses

**Step 4: Optimal Method Recommendation**
Based on the methodological synthesis:
- Recommend the methodological approach most likely to produce valid findings for the research question
- Specify which methodological features are essential vs. optional
- Identify the minimum methodological quality threshold for a study to contribute meaningful evidence

### Methodological Synthesis Output Template

```markdown
## Methodological Synthesis: [RESEARCH QUESTION]

### Method Distribution
| Method | Number of Studies | % of Literature |
|--------|------------------|-----------------|
| [Design type 1] | [N] | [%] |
| [Design type 2] | [N] | [%] |

### Method-Effect Contingency
| Method Feature | Effect Direction | Effect Size Range | Number of Studies |
|---------------|----------------|-------------------|-------------------|
| [Feature 1] | [Direction] | [Range] | [N] |

### Methodological Gaps
- **Underused methods:** [Methods that could contribute but haven't been applied]
- **Method-dependent findings:** [Findings that change depending on method]
- **Quality concerns:** [Systematic methodological weaknesses across the literature]

### Optimal Method Recommendation
[What methodology should the next study use and why]
```

---

## SECTION 4: THEORETICAL SYNTHESIS METHODOLOGY

### When to Use
Theoretical synthesis is appropriate when multiple theories have been applied to the same phenomenon and the field needs integration, comparison, or extension of these theories.

### Procedure

**Step 1: Theory Inventory**
For each theory applied to the phenomenon:
- **Name and origin:** Theoretical tradition, key proponents
- **Core constructs:** What variables does the theory identify as important?
- **Causal mechanisms:** How does the theory explain the phenomenon?
- **Predictions:** What specific, falsifiable predictions does the theory make?
- **Scope conditions:** When and where does the theory claim to apply?
- **Empirical support:** How much evidence supports the theory's predictions?
- **Known limitations:** Where has the theory failed to predict or explain?

**Step 2: Theory Comparison Matrix**

| Dimension | Theory A | Theory B | Theory C |
|-----------|----------|----------|----------|
| Core mechanism | [Mechanism] | [Mechanism] | [Mechanism] |
| Key predictor(s) | [Variables] | [Variables] | [Variables] |
| Predicted outcome | [Outcome] | [Outcome] | [Outcome] |
| Moderators | [Boundary conditions] | [Boundary conditions] | [Boundary conditions] |
| Unique predictions | [What only this theory predicts] | [What only this theory predicts] | [What only this theory predicts] |
| Empirical support | [Strong/Moderate/Weak] | [Strong/Moderate/Weak] | [Strong/Moderate/Weak] |
| Key limitation | [Limitation] | [Limitation] | [Limitation] |

**Step 3: Competitive Testing Assessment**
- Identify predictions where theories diverge (Theory A predicts X, Theory B predicts not-X)
- Determine which studies have tested these competing predictions
- Assess which theory's predictions have been better supported
- Identify untested competitive predictions that could decisively distinguish theories

**Step 4: Theory Integration (if warranted)**
- Determine whether theories are complementary (explain different aspects) or competing (explain the same aspect differently)
- If complementary: Propose an integrated framework that specifies when each theory applies
- If competing: Assess which theory has stronger evidence and propose a crucial test
- If partially overlapping: Identify the unique contribution of each and propose a unified model that preserves their distinct insights

**Step 5: Theory Gap Identification**
- Identify phenomena that no existing theory adequately explains
- Identify theoretical constructs that are invoked but never operationalized
- Identify predictions that are assumed but never tested
- Identify scope conditions that are claimed but never verified

### Theoretical Synthesis Output Template

```markdown
## Theoretical Synthesis: [PHENOMENON]

### Theory Inventory
[Summary of each theory]

### Competitive Assessment
- **Where theories agree:** [Shared predictions]
- **Where theories diverge:** [Competing predictions]
- **Crucial tests needed:** [Studies that could distinguish theories]

### Integration Proposal
[If integration is warranted, the proposed framework]

### Theoretical Gaps
- [Gap 1]: [Description and proposed resolution]
- [Gap 2]: [Description and proposed resolution]
```

---

## SECTION 5: SYNTHESIS QUALITY CRITERIA

### Universal Quality Standards (Apply to All Synthesis Types)

| Criterion | Standard | Assessment Method |
|-----------|----------|-------------------|
| **Comprehensiveness** | All relevant studies are included | Search strategy documented; multiple databases used |
| **Transparency** | Every synthesis claim is traceable to specific studies | Each claim cites supporting evidence |
| **Objectivity** | Contradictory evidence is not suppressed | Contradictions are acknowledged and explained |
| **Coherence** | The synthesis forms a logically consistent narrative | No internal contradictions without resolution |
| **Depth** | Goes beyond surface-level description | Analytical themes or insights emerge from integration |
| **Utility** | The synthesis informs research or practice | Clear implications are drawn |
| **Reproducibility** | Another researcher could replicate the synthesis | Methods are documented in sufficient detail |

### Synthesis Validation Protocol
1. **Triangulation:** Do findings from different methodological approaches converge?
2. **Member checking:** Would the original study authors recognize their findings in the synthesis?
3. **Deviant case analysis:** Are there studies that contradict the synthesis, and have they been adequately addressed?
4. **External review:** Has the synthesis been reviewed by someone not involved in its creation?

---

## SECTION 6: PATTERN RECOGNITION ACROSS STUDIES

### Pattern Types to Look For

**1. Convergence Patterns**
Multiple studies using different methods find the same result. This is the strongest form of evidence.
- Diagnostic: The finding holds across designs, populations, measures, and analytical approaches
- Confidence level: High — this finding is likely robust

**2. Divergence Patterns**
Studies consistently find different results under different conditions.
- Diagnostic: The difference is systematic, not random; it correlates with specific methodological or contextual features
- Confidence level: Moderate — the main effect is moderated by something not yet identified
- Action: Conduct moderation-focused synthesis or meta-analysis

**3. Trajectory Patterns**
The direction or magnitude of findings changes systematically over time.
- Diagnostic: The change is not explained by methodological improvements alone
- Confidence level: Low-Moderate — could reflect genuine change or evolving methods
- Action: Investigate whether the phenomenon itself is changing (e.g., cohort effects, cultural shifts)

**4. Gap Patterns**
Specific questions, populations, or contexts are systematically absent from the literature.
- Diagnostic: The absence is not explained by irrelevance; there is a theoretical reason the missing work should exist
- Confidence level: Moderate — the gap may exist because the research is unfeasible, not merely unstudied
- Action: Validate the gap by confirming it is not addressed by studies you haven't found

**5. Escalation Patterns**
Findings become more extreme or more nuanced as methods improve.
- Diagnostic: Early studies with weak methods find large, simple effects; later studies with stronger methods find smaller or more conditional effects
- Confidence level: Moderate — likely reflects publication bias in early work and improved methods later
- Action: Weight recent, methodologically strong studies more heavily

---

## SECTION 7: CONTRADICTION RESOLUTION FRAMEWORK

### When Studies Disagree: A Diagnostic Decision Tree

```
Studies disagree on finding X.
│
├─ Do they use the same operationalization of variables?
│   ├─ NO → Contradiction may be methodological. Compare measures.
│   └─ YES ↓
│
├─ Do they study the same population?
│   ├─ NO → Contradiction may be population-dependent. Identify moderators.
│   └─ YES ↓
│
├─ Do they have adequate statistical power?
│   ├─ NO → Contradiction may be Type II error. Check power and effect sizes.
│   └─ YES ↓
│
├─ Do they control for the same confounds?
│   ├─ NO → Contradiction may be due to confounding. Compare models.
│   └─ YES ↓
│
├─ Are the studies from the same time period?
│   ├─ NO → Contradiction may reflect temporal change. Check for cohort effects.
│   └─ YES ↓
│
└─ The contradiction is genuine. Possible explanations:
    ├─ Unidentified moderator
    ├─ Theory inadequacy (current theories cannot explain both findings)
    ├─ Nonlinear relationship (studies sample different ranges)
    └─ Context dependency (effect is real but situation-specific)
```

### Resolution Strategies

1. **Moderator search:** Identify a third variable that explains when each result holds. This is the most productive resolution.
2. **Nonlinear modeling:** Test whether the relationship is curvilinear, with studies at different parts of the curve finding different directions.
3. **Threshold effects:** Determine whether one result holds below a critical value and the other above it.
4. **Methodological refinement:** Design a study that eliminates the methodological differences between the conflicting studies.
5. **Theoretical revision:** If no methodological explanation resolves the contradiction, the field's theories may need revision.

---

## SECTION 8: GAP EMERGENCE DETECTION

### How Gaps Reveal Themselves in Synthesis

Gaps in the literature become visible through specific patterns during synthesis:

**1. The Missing Cell**
When you construct a matrix of factors (e.g., Population × Intervention × Outcome), some cells are empty. Empty cells that are theoretically important represent gaps.

**2. The Unexplained Boundary**
When a finding holds under some conditions but not others, and no study has systematically tested why, there is a mechanistic gap.

**3. The Assumed Mechanism**
When studies consistently cite a mechanism (e.g., "X works because of Y") but no study has directly tested whether Y mediates the effect, there is a mechanistic gap.

**4. The Overgeneralized Finding**
When a finding established in one context is assumed to apply broadly, but no replication exists in other contexts, there is a population or context gap.

**5. The Theoretical Tower**
When a theoretical framework is widely cited but has never been subjected to a direct, risky empirical test, there is a theory gap.

**6. The Method Monoculture**
When all studies in an area use the same method, findings may be method-dependent. The absence of methodological diversity is itself a gap.

**7. The Null That Wasn't Published**
When multiple studies report secondary analyses finding null effects on a variable of interest, but no study has been designed to test that variable as a primary outcome, there is likely a publication bias gap.

---

## SECTION 9: FROM SYNTHESIS TO RESEARCH QUESTION PIPELINE

### Transformation Procedure

**Step 1: Identify the Highest-Priority Gap**
From the synthesis, select the gap that meets all three criteria:
- It is validated (confirmed through systematic search, not merely unnoticed)
- It is feasible (addressable with available resources and methods)
- It is significant (closing it would advance the field meaningfully)

**Step 2: Articulate the Gap Precisely**
Write a gap statement using the template:
```
Although [WHAT IS KNOWN], [WHAT IS UNKNOWN] remains uninvestigated,
which limits our understanding of [WHY IT MATTERS] because
[CONSEQUENCE OF THE GAP].
```

**Step 3: Generate Research Questions**
Using the gap_analysis_prompt.md templates, transform the gap into 2–3 candidate research questions.

**Step 4: Evaluate Questions Against Synthesis**
Each candidate question must:
- Directly address a gap identified in the synthesis
- Be testable with methods that the methodological synthesis identifies as optimal
- Be grounded in a theory that the theoretical synthesis identifies as most promising
- Produce findings that would resolve a contradiction identified in the synthesis

**Step 5: Select and Refine**
Choose the question that scores highest on all four criteria and refine using the Question Forge in the Ideation Engine.

### Pipeline Output Template

```markdown
## Synthesis-to-Question Pipeline

### Priority Gap
[Gap statement]

### Candidate Questions
1. [Question 1] — Synthesis alignment: [Which gap, theory, method, contradiction it addresses]
2. [Question 2] — Synthesis alignment: [...]
3. [Question 3] — Synthesis alignment: [...]

### Selected Question
[Question with highest alignment]

### Justification
[Why this question, based on synthesis evidence]

### Recommended Methodology
[Based on methodological synthesis]

### Predicted Contribution
[Based on gap type and novelty assessment]

### Next Step
→ Forward to Methodology Architect (03_methodology_architect)
```
