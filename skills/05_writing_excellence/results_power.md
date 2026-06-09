# Results Power Guide

## Purpose
The results section is the evidentiary core of the paper. It must report findings with precision, structure, and narrative clarity. This guide provides the architecture, standards, and transformation protocols for results writing that reviewers cannot dispute.

---

## 1. Results Section Structure Template

### Overall Architecture

```
PARAGRAPH 1: OVERVIEW (Analytic roadmap)
├── Analytic strategy summary
├── Sample size and exclusions at analysis
├── Assumption check summary
└── Section preview

PARAGRAPH 2+: HYPOTHESIS TESTS (One per paragraph)
├── H1: [Hypothesis restated → Descriptives → Inferential → Interpretation]
├── H2: [Same structure]
├── H3: [Same structure]
└── etc.

PENULTIMATE PARAGRAPH: EXPLORATORY ANALYSES (if any)
├── Clearly labeled as exploratory
├── Same reporting standards
└── Explicitly noted as not preregistered

FINAL PARAGRAPH: SYNTHESIS
├── Which hypotheses were supported
├── Which were not supported
├── Key unexpected findings
└── No interpretation (save for Discussion)
```

---

## 2. One-Hypothesis-Per-Paragraph Protocol

### The 4-Sentence Structure

Every results paragraph follows this exact architecture. Do not deviate.

**Sentence 1 — Hypothesis Restatement**
"To test H[X] that [prediction], we conducted a [analysis name]."

This sentence serves two functions: (a) reminds the reader of the hypothesis, and (b) names the analysis. It does NOT report results.

**Sentence 2 — Descriptive Statistics**
"Participants in the [condition A] condition (M = X.XX, SD = X.XX, n = XX) [reported higher/lower/did not differ in] [DV] compared to those in the [condition B] condition (M = X.XX, SD = X.XX, n = XX)."

Always report M, SD, and n for every group before the inferential statistic. This grounds the reader in the actual data before the abstraction of the test.

**Sentence 3 — Inferential Statistics**
"This difference was [significant/not significant], [test statistic](df) = X.XX, p = .XXX, [effect size] = X.XX, 95% CI [X.XX, X.XX]."

Report: test statistic, degrees of freedom, exact p-value, effect size with confidence interval. No exceptions.

**Sentence 4 — Plain Language Interpretation**
"This [supports/does not support] H[X], indicating that [one-sentence plain-language interpretation of what the finding means]."

This sentence translates the statistic into a claim. It does NOT explain why (that is for Discussion). It does NOT compare to other studies (that is for Discussion).

### Extended Template for Complex Analyses

For ANOVA, regression, or mixed models that test multiple effects:

**Sentence 1**: "To test H[X] that [prediction], we conducted a [analysis name] with [IV(s)] as predictor(s) and [DV] as the outcome."

**Sentence 2**: "There was a [significant/not significant] main effect of [IV], [test statistic](df) = X.XX, p = .XXX, [effect size] = X.XX."

**Sentence 3** (if interaction): "This was qualified by a [significant/not significant] [IV1] × [IV2] interaction, [test statistic](df) = X.XX, p = .XXX, [effect size] = X.XX."

**Sentence 4** (follow-up): "Simple effects analysis revealed that [specific comparison]: [descriptive] → [inferential]."

**Sentence 5** (interpretation): "These results [support/partially support/do not support] H[X], suggesting that [interpretation]."

---

## 3. Statistical Reporting Standards

### APA 7th Edition (Psychology, Social Sciences)

| Statistic | Format | Example |
|---|---|---|
| t-test | t(df) = X.XX, p = .XXX, d = X.XX, 95% CI [X.XX, X.XX] | t(118) = 3.42, p = .001, d = 0.63, 95% CI [0.25, 1.01] |
| ANOVA | F(df1, df2) = X.XX, p = .XXX, η²_p = .XX | F(1, 118) = 11.72, p = .001, η²_p = .09 |
| Regression | b = X.XX, SE = X.XX, t(df) = X.XX, p = .XXX, β = .XX | b = 0.42, SE = 0.11, t(117) = 3.82, p < .001, β = .33 |
| Correlation | r(df) = .XX, p = .XXX, 95% CI [.XX, .XX] | r(118) = .34, p < .001, 95% CI [.18, .48] |
| Chi-square | χ²(df, N = XX) = X.XX, p = .XXX, V = .XX | χ²(2, N = 120) = 8.34, p = .015, V = .19 |
| Effect size d | d = X.XX, 95% CI [X.XX, X.XX] | d = 0.63, 95% CI [0.25, 1.01] |
| Bayes Factor | BF₁₀ = X.XX | BF₁₀ = 12.4 |

### AMA Style (Medicine, Public Health)

| Statistic | Format | Example |
|---|---|---|
| t-test | t₁₁₈ = 3.42; P = .001; d = 0.63 (95% CI, 0.25-1.01) | Note: Subscript df, P capitalized |
| Regression | β = 0.33 (SE = 0.11); P < .001 | β is standardized; b for unstandardized |
| Odds ratio | OR = 2.41; 95% CI, 1.63-3.56 | No p-value required with CI |
| Hazard ratio | HR = 1.87; 95% CI, 1.32-2.64 | Same format as OR |
| Risk ratio | RR = 1.34; 95% CI, 1.12-1.61 | Same format |

### Journal-Specific Variations to Check

- **Nature/Science**: Report statistics in text; exact p-values; effect sizes required; no stars in text
- **Lancet/JAMA**: P values with capital P; CIs for all estimates; CONSORT flow diagram for trials
- **PNAS**: Same as APA with additional requirements for error bars in figures
- **Journal-specific**: Always check the author guidelines before final formatting

### Universal Rules (Regardless of Style)

1. Every p-value must be accompanied by an effect size
2. Every point estimate must be accompanied by a confidence interval
3. Exact p-values are reported (p = .032, not p < .05) except p < .001
4. Direction of effect is always stated
5. Degrees of freedom are always reported
6. The test statistic is identified (not just "p = .03" — what test produced it?)
7. N is stated for every analysis
8. Null results receive the same reporting standard as significant results

---

## 4. Table and Figure Reference Integration

### Rules for Referencing Tables and Figures

1. **Every table and figure must be referenced in the text at least once.**
2. **Reference at the point of first relevant discussion**, not at the end of a paragraph.
3. **Use parenthetical references** (see Figure 1) or (Table 2), not "Figure 1 shows that..." — the text should state the finding; the figure provides the visual evidence.
4. **Do not duplicate information** between text and table/figure. If exact values are in the table, summarize in text; if the figure shows the pattern, describe it briefly.
5. **Order of first reference** determines table/figure numbering. Figure 1 must be referenced before Figure 2.

### Integration Template

"To test H1, we compared outcomes across conditions. The treatment group (M = 4.32, SD = 1.12) scored higher than the control group (M = 3.68, SD = 1.05), t(158) = 3.72, p < .001, d = 0.59, 95% CI [0.27, 0.91] (see Figure 1 for group distributions)."

Note: The parenthetical figure reference supplements but does not replace the text reporting.

### Table vs Text Decision

| Content | Put in Table | Put in Text |
|---|---|---|
| Descriptive statistics for all variables | ✅ | ❌ |
| Correlation matrix | ✅ | ❌ |
| Regression coefficients | ✅ | Brief summary in text |
| ANOVA summary | ✅ | Key effects in text |
| Single comparison result | ❌ | ✅ |
| Primary hypothesis test (simple) | ❌ | ✅ |
| Primary hypothesis test (complex) | Key results in text | Full table in supplement |

---

## 5. Negative and Null Result Reporting

### Why Null Results Deserve Equal Treatment

1. A null result is data, not failure
2. Underpowered null results are uninformative; adequately powered null results ARE informative
3. Selective reporting of significant results creates publication bias
4. Reviewers will question omitted hypotheses — include all preregistered tests

### Reporting Template for Null Results

**Adequately powered (can rule out effects of interest):**
"To test H2 that [prediction], we conducted a [test]. [Condition A] (M = X.XX, SD = X.XX) did not differ from [Condition B] (M = X.XX, SD = X.XX), t(df) = X.XX, p = .XXX, d = 0.XX, 95% CI [−0.XX, 0.XX]. This does not support H2. The confidence interval excludes effects larger than d = 0.XX, indicating that any true effect, if present, is smaller than [smallest effect of practical interest]."

**Underpowered (cannot rule out meaningful effects):**
"The comparison was not significant, t(df) = X.XX, p = .XXX, d = 0.XX, 95% CI [−0.XX, 0.XX]. However, the confidence interval includes effects as large as d = 0.XX, meaning that a meaningful effect cannot be ruled out. This null result should be interpreted with caution given the sample's limited power to detect small effects."

**Bayesian approach to null results:**
"The data were [X] times more likely under the null than the alternative, BF₀₁ = X.XX, providing [anecdotal/moderate/strong] evidence for the null hypothesis."

### What NEVER to Write for Null Results
❌ "The result was marginally significant" (p = .06-.10) — this phrase means nothing
❌ "The result approached significance" — results do not approach; they are
❌ "The result was in the predicted direction but not significant" — direction without significance is noise
❌ "Although not significant, the pattern suggests..." — this is interpretation disguised as results
❌ No mention of the hypothesis at all (silently dropping H2) — this is the worst option

---

## 6. Results Section Flow and Narrative

### The Narrative Arc

The results section tells the story of your hypotheses being tested. Like any story, it needs:

1. **Setting** (Overview paragraph): Where we are, what we will test
2. **Rising action** (H1-H3): Each test builds on the previous, adding complexity
3. **Climax** (Primary finding): The most important result
4. **Falling action** (Secondary/exploratory analyses): Additional context
5. **Resolution** (Synthesis paragraph): Where we stand after all tests

### Transition Sentences Between Paragraphs

Each paragraph's last sentence should set up the next paragraph:

- **From H1 to H2**: "Having established that [H1 finding], we next tested whether [H2 prediction]."
- **From main effect to interaction**: "This main effect raises the question of whether it holds across all [levels of moderator]."
- **From H2 to mediation**: "Given that [X predicts Y], we examined whether this relationship operates through [M]."
- **From primary to exploratory**: "In addition to the preregistered hypotheses, we conducted exploratory analyses to examine [question]."

### Parallel Structure

Maintain parallel sentence structure across hypothesis paragraphs:

**H1 paragraph**: "To test H1 that [A predicts B], we conducted [test]. [Result]. This supports H1, indicating that [interpretation]."

**H2 paragraph**: "To test H2 that [C moderates A→B], we conducted [test]. [Result]. This [supports/does not support] H2, indicating that [interpretation]."

**H3 paragraph**: "To test H3 that [M mediates A→B], we conducted [test]. [Result]. This [supports/does not support] H3, indicating that [interpretation]."

Parallel structure makes the results section predictable and scannable. Reviewers can quickly find each hypothesis test.

---

## 7. Common Results Writing Mistakes

### Mistake 1: The Data Dump
**Problem**: Reporting every analysis without structure. "We ran a t-test, then an ANOVA, then a regression, then a mediation..."
**Fix**: Organize by hypothesis. Each paragraph corresponds to one hypothesis. Follow the 4-sentence structure.

### Mistake 2: Buried Lead
**Problem**: The most important finding appears in the middle of a paragraph about something else.
**Fix**: The primary hypothesis (H1) gets the first results paragraph. The primary finding gets the most prominent reporting.

### Mistake 3: Missing Descriptives
**Problem**: Jumping straight to inferential statistics: "The effect was significant, F(1, 58) = 8.34, p = .005." What were the means?
**Fix**: Always report descriptive statistics before inferential statistics. The reader needs to know what the numbers actually look like.

### Mistake 4: Naked p-Values
**Problem**: "The groups differed significantly, p = .003." No effect size, no direction, no confidence interval.
**Fix**: Every p-value must be accompanied by: direction, effect size, and confidence interval.

### Mistake 5: Interpretation in Results
**Problem**: "Participants in the treatment condition scored higher because the intervention increased self-efficacy, which enhanced motivation."
**Fix**: Save "because" for Discussion. In Results: "Participants in the treatment condition scored higher (M = 4.32) than those in the control condition (M = 3.68), t(58) = 3.42, p = .001, d = 0.59."

### Mistake 6: Inconsistent Reporting
**Problem**: "p = .003" in one paragraph, "p < .01" in the next, "p = .0*" in a third.
**Fix**: Use consistent formatting throughout. APA: p = .003 (always exact, three decimals, except p < .001).

### Mistake 7: Dropped Hypotheses
**Problem**: The introduction stated H1, H2, and H3, but the results section only reports H1 and H2. H3 is never mentioned again.
**Fix**: Every hypothesis in the introduction must have a corresponding results paragraph. If a hypothesis was abandoned, explain why in a footnote.

### Mistake 8: Passive Voice Overuse
**Problem**: "A t-test was conducted. A significant difference was found."
**Fix**: "We conducted a t-test. The treatment group scored higher than the control group." Active voice is clearer and more engaging.

---

## 8. Before/After Results Paragraph Transformations

### Example 1: Independent t-test

**BEFORE (Weak):**
We ran a t-test to compare the two groups. The results showed a significant difference between the experimental and control groups (p < .05). The experimental group did better. This supports our hypothesis.

**Problems**: No descriptives, no effect size, no CI, no direction stated precisely, "did better" is vague, no df or t-value, "significant" without context, "supports our hypothesis" without restating the hypothesis.

**AFTER (Strong):**
To test H1 that the growth mindset intervention would improve academic performance, we conducted an independent-samples t-test. Students in the intervention condition (M = 72.4, SD = 10.3, n = 62) scored higher on the mathematics assessment than students in the control condition (M = 67.8, SD = 11.1, n = 64), t(124) = 2.38, p = .019, d = 0.43, 95% CI [0.08, 0.78]. This supports H1, indicating that the growth mindset intervention produced a moderate improvement in mathematics performance.

### Example 2: Regression with Interaction

**BEFORE (Weak):**
We did a regression analysis. The results are shown in Table 3. There was a significant interaction effect. The simple slopes showed that the effect was significant at high levels of the moderator but not at low levels.

**Problems**: No statistics in text, table-dumping, no direction, no effect sizes, vague "significant," no simple slopes reported, no interpretation.

**AFTER (Strong):**
To test H2 that cognitive ability moderates the relationship between practice time and chess performance, we conducted a hierarchical regression entering practice time and cognitive ability at Step 1 and their interaction at Step 2. The interaction accounted for significant additional variance, ΔR² = .06, ΔF(1, 96) = 7.24, p = .008. Simple slopes analysis revealed that practice time predicted performance when cognitive ability was high (+1SD), b = 4.32, SE = 1.12, t(96) = 3.86, p < .001, but not when cognitive ability was low (−1SD), b = 0.87, SE = 1.21, t(96) = 0.72, p = .473. This supports H2, indicating that the benefit of practice depends on cognitive ability — practice alone is insufficient when cognitive resources are limited.

### Example 3: Null Result

**BEFORE (Weak):**
We tested H3 but the result was not significant (p = .12). There was a trend in the predicted direction. Further research is needed.

**Problems**: "Trend" is banned, no descriptives, no effect size, no CI, no interpretation of what the null means, no power information.

**AFTER (Strong):**
To test H3 that perspective-taking reduces prejudice more than contact alone, we compared the two conditions on the prejudice composite. Participants in the perspective-taking condition (M = 2.34, SD = 0.82, n = 58) did not score significantly lower than those in the contact-only condition (M = 2.51, SD = 0.79, n = 61), t(117) = 1.15, p = .252, d = 0.21, 95% CI [−0.15, 0.57]. This does not support H3. The 95% CI includes effects as large as d = 0.57 but excludes effects larger than d = 0.57, suggesting that any true advantage of perspective-taking over contact, if present, is at most moderate in size.

### Example 4: Mediation

**BEFORE (Weak):**
Mediation analysis was conducted. The indirect effect was significant. The direct effect was reduced. This shows full mediation.

**Problems**: No statistics, "shows" overclaims, "full mediation" is a strong claim rarely justified, no bootstrap details, no indirect effect value or CI.

**AFTER (Strong):**
To test H4 that perceived threat mediates the effect of social exclusion on aggression, we conducted a bootstrap mediation analysis (5,000 samples; Hayes Model 4). The indirect effect through perceived threat was significant, ab = 1.47, SE = 0.42, 95% CI [0.71, 2.38]. The direct effect of exclusion on aggression after accounting for threat was no longer significant, c' = 0.62, SE = 0.48, 95% CI [−0.32, 1.56], whereas the total effect was significant, c = 2.09, SE = 0.51, 95% CI [1.08, 3.10]. This supports H4, indicating that perceived threat accounts for the exclusion-aggression relationship, though the wide CI on the direct effect means that partial mediation through additional pathways cannot be ruled out.
