# Hypothesis Forge

## A Systematic Framework for Constructing Precise, Testable, and Falsifiable Research Hypotheses

### Purpose
This prompt provides a rigorous framework for transforming research questions into well-formed hypotheses. It ensures that every hypothesis is specific, falsifiable, theoretically grounded, and precisely articulated — avoiding the vague, untestable, or tautological statements that undermine research from the start.

---

## SECTION 1: HYPOTHESIS CONSTRUCTION FRAMEWORK

### The H-O-A-R Structure

Every well-formed hypothesis should contain four elements:

**H** — **Hypothesized relationship:** The specific, directional prediction about the relationship between variables

**O** — **Operationalization:** How each variable will be measured or manipulated

**A** — **Antecedent conditions:** The conditions under which the hypothesis is expected to hold

**R** — **Rationale:** The theoretical or empirical basis for the prediction

#### Template:
```
Based on [THEORY/PRIOR EVIDENCE], we hypothesize that [INDEPENDENT VARIABLE],
operationalized as [MEASURE/MANIPULATION], will [DIRECTION OF EFFECT]
[DEPENDENT VARIABLE], operationalized as [MEASURE], under conditions of
[MODERATOR/CONTEXT], because [MECHANISM/THEORETICAL REASONING].
```

#### Example:
```
Based on cognitive load theory (Sweller, 1988), we hypothesize that worked-example
instruction, operationalized as step-by-step problem-solving demonstrations, will
produce higher far-transfer performance, operationalized as score on novel problem
sets, under conditions of high element interactivity (complex problems), because
worked examples reduce extraneous cognitive load, freeing working memory resources
for schema construction.
```

---

## SECTION 2: STRONG VS. WEAK HYPOTHESIS CRITERIA

### Strong Hypotheses

| Criterion | Strong Hypothesis | Weak Hypothesis |
|-----------|------------------|-----------------|
| **Specificity** | Names specific variables and direction | Refers to vague constructs ("will affect") |
| **Falsifiability** | A clearly defined outcome could disprove it | No possible outcome could disprove it |
| **Groundedness** | Derived from explicit theory or evidence | Based on intuition or "common sense" |
| **Testability** | Can be tested with available methods | Requires impossible or unethical methods |
| **Precision** | States magnitude, direction, and boundary conditions | States only that a relationship exists |
| **Non-triviality** | Predicts something not already known | Restates established findings |
| **Parsimony** | The simplest explanation for the predicted effect | Requires multiple unsupported assumptions |

### Weak Hypothesis Examples and Repairs

**Weak:** "Social media affects mental health."
- **Problem:** No direction, no specificity, no operationalization, no mechanism
- **Repair:** "Greater daily social media use (hours/day, self-report + screen time logs) will predict increased depressive symptoms (PHQ-9 scores) one month later, controlling for baseline depression, because upward social comparison mediates the relationship."

**Weak:** "There will be a difference between the groups."
- **Problem:** Non-directional when direction is predictable; no specificity
- **Repair:** "Participants in the growth mindset intervention condition will show higher persistence on unsolvable puzzles (time spent before giving up) than participants in the control condition, because growth mindset beliefs increase the perceived value of effort."

**Weak:** "Personality is related to job performance."
- **Problem:** Too broad — which personality traits? Which aspect of performance?
- **Repair:** "Conscientiousness, measured by the BFI-2, will positively predict task performance ratings (supervisor-rated) but not contextual performance, because conscientiousness drives goal-directed behavior but not necessarily interpersonal helping."

---

## SECTION 3: FALSIFIABILITY ASSESSMENT PROTOCOL

### The Falsifiability Test

For each hypothesis, apply the following seven-item assessment:

1. **Can you specify an observation that would disconfirm the hypothesis?**
   - If no → The hypothesis is unfalsifiable. Reformulate.
   - If yes → Name the specific disconfirming observation.

2. **Is the hypothesis distinguishable from a tautology?**
   - "People who are more motivated will try harder" is tautological.
   - "People with higher self-efficacy will persist longer on difficult tasks" is empirical.

3. **Could the hypothesis be confirmed by any possible outcome?**
   - "Treatment will have an effect" (could be positive, negative, or null — "confirmed" by any non-zero effect) → Unfalsifiable in its non-directional form
   - "Treatment will reduce symptoms" → Falsifiable (symptom increase disconfirms)

4. **Are the variables independently measurable?**
   - If the independent and dependent variables cannot be measured without referencing each other, the hypothesis is circular.

5. **Does the hypothesis make a risky prediction?**
   - A risky prediction is one that could reasonably be wrong.
   - If the prediction is almost certain to be true, it lacks informational value.

6. **Is the hypothesis immune to post hoc redefinition?**
   - "The intervention will improve well-being" can be redefined post hoc (e.g., "Well-being didn't improve, but resilience did, which is what we really meant").
   - Pre-specify the primary outcome to prevent this.

7. **Can the hypothesis be derived from more than one theory?**
   - If only one theory could generate this prediction, it is a strong test of that theory.
   - If any theory could predict it, it is a weak test.

### Falsifiability Score
- Pass 6–7 items → High falsifiability (excellent)
- Pass 4–5 items → Moderate falsifiability (acceptable with revision)
- Pass <4 items → Low falsifiability (reformulate before proceeding)

---

## SECTION 4: DIRECTIONAL VS. NON-DIRECTIONAL HYPOTHESES

### When to Use Directional Hypotheses (Preferred)

Directional hypotheses specify the expected direction of the effect. They should be used when:
- Theory makes a clear directional prediction
- Prior empirical evidence consistently shows a direction
- A non-directional result would have different theoretical implications than a directional one
- You have sufficient theoretical basis to justify a directional claim

**Format:**
```
[IV] will [increase/decrease/positively predict/negatively predict] [DV].
```

### When to Use Non-Directional Hypotheses (Restricted)

Non-directional hypotheses state that a difference or relationship exists without specifying direction. They are appropriate only when:
- Competing theories make opposite directional predictions, and you are testing which is correct
- The phenomenon is genuinely novel with no directional basis
- You are conducting a true exploratory study (and label it as such)

**Format:**
```
[IV] will be related to [DV], but the direction of the relationship is
unspecified because [COMPETING PREDICTIONS].
```

### Why Directional is Preferred
1. Directional hypotheses require stronger theoretical commitment, producing more informative tests
2. They justify one-tailed statistical tests (when appropriate), increasing statistical power
3. They make the hypothesis more falsifiable (only one direction confirms)
4. They force the researcher to articulate a mechanism, not merely predict "an effect"
5. Journal reviewers and editors generally expect directional hypotheses when theory supports them

---

## SECTION 5: MEDIATION AND MODERATION HYPOTHESIS TEMPLATES

### Mediation Hypotheses

Mediation hypotheses specify that the effect of X on Y occurs through an intermediate variable M.

**Template:**
```
[X] will influence [Y] through [M], such that [X] affects [M], which in turn
affects [Y]. Specifically, the effect of [X] on [Y] will be [reduced/eliminated]
when [M] is statistically controlled, indicating [full/partial] mediation.
```

**Example:**
```
Socioeconomic status (SES) will influence academic achievement through school
quality, such that SES affects school quality (access to resources, teacher
expertise), which in turn affects academic achievement. Specifically, the effect
of SES on achievement will be substantially reduced when school quality is
statistically controlled, indicating partial mediation.
```

**Requirements for a valid mediation hypothesis:**
- Specify the mediator construct and its operationalization
- State the theoretical rationale for why X → M and M → Y
- Predict whether mediation will be full or partial (with justification)
- Identify potential alternative mediators that should be ruled out

### Moderation Hypotheses

Moderation hypotheses specify that the strength or direction of the X → Y relationship depends on a third variable W.

**Template:**
```
The relationship between [X] and [Y] will be moderated by [W], such that
[the positive/negative effect of X on Y] will be [stronger/weaker/only present]
when [W] is [high/low/present/absent], because [THEORETICAL REASONING].
```

**Example:**
```
The relationship between stress and illness will be moderated by social support,
such that the positive effect of stress on illness incidence will be weaker when
social support is high than when it is low, because social support buffers the
physiological stress response (Cohen & Wills, 1985).
```

**Requirements for a valid moderation hypothesis:**
- Specify the moderator construct and its operationalization
- State the theoretical rationale for the interaction
- Predict the specific pattern (stronger, weaker, reversed, or present-only-at-one-level)
- Explain why the moderation occurs, not merely that it occurs

### Moderated Mediation (Conditional Process) Hypotheses

**Template:**
```
The indirect effect of [X] on [Y] through [M] will be moderated by [W], such
that the mediation will be [stronger/weaker/present/absent] when [W] is
[high/low], because [THEORETICAL REASONING for the moderated path].
```

### Mediated Moderation Hypotheses

**Template:**
```
The moderating effect of [W] on the relationship between [X] and [Y] will be
mediated by [M], such that [W] influences [M], which in turn determines the
strength of the [X] → [Y] relationship, because [THEORETICAL REASONING].
```

---

## SECTION 6: HYPOTHESIS HIERARCHY

### Primary Hypotheses (1–3 maximum)
- Direct tests of the core research question
- Must be directional and derived from the primary theoretical framework
- Each should be independently testable (not contingent on another being confirmed)
- Must have sufficient statistical power (≥ .80) to detect the expected effect size

### Secondary Hypotheses (3–5 maximum)
- Tests of mechanisms, boundary conditions, or extensions
- May be non-directional if theory is equivocal
- Should clarify the "why" or "when" behind primary hypotheses
- Include mediation and moderation hypotheses here

### Exploratory Hypotheses (No limit, but be selective)
- Investigated without strong directional predictions
- Must be explicitly labeled as exploratory to prevent HARKing (Hypothesizing After Results are Known)
- Should be justified by at least a plausible mechanism, even if evidence is thin
- Report with appropriate statistical caution (no confirmatory language)

### Hierarchy Decision Rules
1. If you have more than 3 primary hypotheses, you likely have an unfocused research question. Reconsider the study's scope.
2. Secondary hypotheses should directly illuminate primary hypotheses, not introduce tangential questions.
3. Exploratory hypotheses should be pre-registered as exploratory to maintain the distinction between confirmatory and exploratory analysis.
4. Never retroactively promote an exploratory finding to a confirmatory hypothesis.

---

## SECTION 7: COMMON HYPOTHESIS PITFALLS AND HOW TO AVOID THEM

### Pitfall 1: The Vagueness Trap
**Problem:** "X will have an effect on Y" — so general it could mean anything.
**Fix:** Specify direction, magnitude, and mechanism. "X will increase Y by approximately [d = 0.3] through mechanism M."

### Pitfall 2: The Tautology Trap
**Problem:** "People who are better at X will perform better on X" — true by definition.
**Fix:** Ensure the independent and dependent variables are conceptually distinct, even if correlated. Test the prediction that a measure of one construct predicts behavior in a different domain.

### Pitfall 3: The Unfalsifiable Trap
**Problem:** "X will influence Y, or if it doesn't, there must be a moderating variable we haven't measured" — immunizes against disconfirmation.
**Fix:** Pre-specify the conditions under which you would consider the hypothesis disconfirmed. If you anticipate a moderator, include it in the hypothesis.

### Pitfall 4: The Kitchen Sink Trap
**Problem:** Proposing 15 hypotheses covering every possible relationship — indicates lack of theoretical focus.
**Fix:** Limit primary hypotheses to 1–3. Use theoretical parsimony as the selection criterion.

### Pitfall 5: The HARKing Trap
**Problem:** Formulating hypotheses after seeing the data, then presenting them as a priori predictions.
**Fix:** Pre-register hypotheses before data collection. If you develop hypotheses from data, label them as post hoc and treat as exploratory.

### Pitfall 6: The P-Hacking Enabler
**Problem:** Vague hypotheses that allow multiple operationalizations and analytic choices, each of which could produce significance.
**Fix:** Pre-specify primary outcomes, measures, and analysis plans. Use the hypothesis hierarchy to distinguish confirmatory from exploratory.

### Pitfall 7: The Mechanism-Free Trap
**Problem:** "X predicts Y" without explaining why — a prediction without understanding.
**Fix:** Include at least a proposed mechanism. Even if you don't test it directly, articulating the mechanism makes the hypothesis more falsifiable (if the mechanism is wrong, the prediction may be wrong too).

### Pitfall 8: The Universal Quantifier Trap
**Problem:** "X will always increase Y" — a single counterexample falsifies it.
**Fix:** Use probabilistic language appropriate to the domain: "X will tend to increase Y, on average, in the specified population." Add boundary conditions.

### Pitfall 9: The Correlation-Causation Trap
**Problem:** "X causes Y" stated for correlational designs.
**Fix:** Match causal language to design strength. Correlational designs: "X will be associated with Y." Experimental designs: "X will cause changes in Y."

### Pitfall 10: The Irreproducible Operationalization Trap
**Problem:** Variables are defined so vaguely that another researcher cannot replicate the operationalization.
**Fix:** Specify the exact measure, manipulation, or procedure. Name the instrument, the dosage, the stimulus, the coding scheme.

---

## SECTION 8: TEMPLATE FOR WRITING TESTABLE, PRECISE HYPOTHESES

### Standard Hypothesis Statement
```
H[X]: Based on [THEORY] ([CITATION]), we predict that [PARTICIPANTS]
exposed to [IV MANIPULATION] will show [DIRECTION] [DV MEASURE]
compared to [COMPARISON CONDITION], because [MECHANISM].
This effect is expected to be [MAGITUDE ESTIMATE] in size,
and will be [MODERATION PATTERN] for [MODERATOR] because
[MODERATION RATIONALE].
```

### Full Hypothesis Documentation Template

```markdown
### H[X]: [HYPOTHESIS SHORT TITLE]

**Statement:** [Full hypothesis in the format above]

**Hypothesis Type:** [Primary / Secondary / Exploratory]

**Directionality:** [Directional (specify direction) / Non-directional (specify why)]

**Gap Addressed:** [Which gap from the gap analysis does this address?]

**Theoretical Basis:** [Which theory or prior evidence supports this?]

**Falsifiability:** [What specific outcome would disconfirm this hypothesis?]

**Operationalization:**
- IV: [Exact measure/manipulation]
- DV: [Exact measure]
- Moderators (if any): [Exact measure]
- Mediators (if any): [Exact measure]

**Expected Effect Size:** [Estimate with justification from prior literature]

**Statistical Test:** [Planned test, including correction for multiple comparisons if applicable]

**Boundary Conditions:** [When would this hypothesis NOT hold?]

**Alternative Explanations:** [What else could produce the predicted pattern?]

**Disconfirming Outcome:** [If the hypothesis is wrong, what will we observe?]
```

### Example of a Fully Documented Hypothesis

```markdown
### H1: Testing Effect Under Anxiety

**Statement:** Based on retrieval practice theory (Roediger & Karpicke, 2006) and the
attentional control theory (Eysenck et al., 2007), we predict that participants
who complete retrieval practice after studying will show higher long-term retention
(7-day delayed cued recall test, proportion correct) compared to participants who
complete restudy, but this testing effect will be attenuated under high state anxiety
(induced via timed testing with social-evaluative threat) because anxiety consumes
working memory resources needed for effective retrieval. The testing effect in the
low-anxiety condition is expected to be medium-to-large (d ≈ 0.60), based on prior
meta-analytic estimates (Rowland, 2014), and may be reduced to small (d ≈ 0.20)
in the high-anxiety condition.

**Hypothesis Type:** Primary

**Directionality:** Directional — testing effect predicted in low-anxiety; attenuated
effect predicted in high-anxiety

**Gap Addressed:** Mechanistic gap — the boundary conditions of the testing effect
are poorly understood, particularly under conditions of anxiety

**Theoretical Basis:** Retrieval practice theory + attentional control theory

**Falsifiability:** If retrieval practice produces equivalent benefits regardless
of anxiety level, the hypothesis is disconfirmed.

**Operationalization:**
- IV: Learning strategy (retrieval practice vs. restudy) × Anxiety condition (high vs. low)
- DV: 7-day delayed cued recall (proportion correct)
- Manipulation check: State-Trait Anxiety Inventory (STAI-S) post-manipulation

**Expected Effect Size:** d = 0.60 in low-anxiety; d = 0.20 in high-anxiety

**Statistical Test:** 2 × 2 ANOVA with planned contrasts; interaction effect is
the critical test

**Boundary Conditions:** May not hold for highly test-anxious individuals or for
material with very low or very high difficulty

**Alternative Explanations:** Anxiety could enhance encoding (Yerkes-Dodson) rather
than impairing retrieval; the timed condition could reduce total study time rather
than increasing anxiety per se

**Disconfirming Outcome:** No interaction between strategy and anxiety; testing
effect is equally strong in both conditions
```

---

## FINAL CHECKLIST: BEFORE SUBMITTING YOUR HYPOTHESES

- [ ] Each hypothesis is specific enough that another researcher could test it identically
- [ ] Each hypothesis has a clear falsification condition
- [ ] Primary hypotheses are limited to 1–3
- [ ] Directional hypotheses have theoretical justification for the direction
- [ ] Non-directional hypotheses are justified by competing predictions
- [ ] Mediation hypotheses specify the theoretical mechanism, not just the statistical path
- [ ] Moderation hypotheses explain why the interaction occurs, not just that it exists
- [ ] Exploratory hypotheses are clearly labeled as such
- [ ] Hypotheses do not overlap or depend on each other for confirmation
- [ ] The hypothesis-to-analysis plan is pre-specified (no HARKing)
- [ ] Expected effect sizes are justified with citations, not intuitions
- [ ] Boundary conditions are acknowledged, not ignored
