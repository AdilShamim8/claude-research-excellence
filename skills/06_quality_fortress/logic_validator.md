# Logic Validation Framework

## Purpose
This framework provides a systematic method for checking the logical integrity of research arguments. Every claim in a paper should be licensed by the evidence presented. Every inference should follow from the premises. Every conclusion should be the logical consequence of the results. This framework detects and repairs logical gaps before reviewers find them.

---

## 1. Argument Structure Analysis

### The Toulmin Model Applied to Research Papers

Every research claim follows this structure:

```
CLAIM (Conclusion)
    ↑
  WARRANT (Why the data support the claim)
    ↑
  GROUNDS (The data/evidence)
    ↑
  BACKING (The theoretical justification for the warrant)
    ↑
  QUALIFIER (How certain the claim is)
    ↑
  REBUTTAL (Conditions under which the claim would not hold)
```

### How to Audit an Argument

For each major claim in the paper, identify all six elements:

**Example claim**: "Cognitive load drives the framing effect."

| Element | What to Check | Common Failure |
|---|---|---|
| Grounds | Is the data presented sufficient to support this claim? | Insufficient data; wrong data |
| Warrant | Does the warrant logically connect grounds to claim? | Non sequitur; hidden assumption |
| Backing | Is the theoretical backing accurate and relevant? | Misrepresented theory; outdated theory |
| Qualifier | Is the certainty level appropriate? | Over-claiming or under-claiming |
| Rebuttal | Are conditions noted where the claim might not hold? | Missing limitations; ignored alternatives |

### Argument Mapping

Map the paper's argument as a chain:

1. **Premise 1**: [Statement accepted as true, e.g., "Framing effects are robust"]
2. **Premise 2**: [Statement from your data, e.g., "Time pressure amplifies framing"]
3. **Inference Rule**: [General principle, e.g., "If X amplifies Y, and Z is a mechanism of amplification, then Z may drive Y"]
4. **Intermediate Conclusion**: ["Time pressure's amplification of framing suggests a load mechanism"]
5. **Premise 3**: [Additional data, e.g., "Cognitive load mediates the amplification"]
6. **Final Claim**: ["Cognitive load drives the framing effect"]

Check each link in the chain: Is each inference valid? Are any steps missing?

---

## 2. Common Logical Fallacies in Research Papers

### Fallacy 1: Overclaiming

**Definition**: Making a claim that is stronger than the evidence licenses.

**Example**: 
- Evidence: Observational study showing X and Y are correlated
- Claim: "X causes Y"
- Why it's fallacious: Correlation ≠ causation; no design features support causal inference

**Detection**: Search for causal verbs (causes, produces, leads to, results in, drives) and check whether the design permits causal inference. If the design is observational, replace with associative language (is associated with, predicts, is related to).

**Fix**: "X is associated with Y" or "X predicts Y, controlling for [covariates], though causal direction cannot be established with this design."

### Fallacy 2: Underpowered Certainty

**Definition**: Stating conclusions with high confidence when the evidence is ambiguous.

**Example**: 
- Evidence: Single study, p = .04, d = 0.21 (small effect, wide CI)
- Claim: "These findings establish that X produces Y"
- Why it's fallacious: A small, barely significant effect in a single study provides weak evidence, not establishment

**Detection**: Check whether claim language (establish, demonstrate, confirm) matches the evidence strength (small effect, borderline p, wide CI, single study). Use the calibrated courage framework.

**Fix**: "These findings provide evidence consistent with the hypothesis that X predicts Y, though replication with a larger sample is needed to establish the effect's magnitude."

### Fallacy 3: Reverse Causation

**Definition**: Assuming A causes B when B could cause A.

**Example**: 
- Evidence: Depression scores predict social withdrawal (cross-sectional)
- Claim: "Depression causes social withdrawal"
- Why it's fallacious: Social withdrawal could cause depression; both could be caused by a third variable; bidirectional causation is possible

**Detection**: For every causal claim, ask: "Could the arrow point the other way?" If the design is cross-sectional, the answer is almost always "yes."

**Fix**: Use longitudinal or experimental designs for causal claims. In cross-sectional data: "Depression is associated with social withdrawal, though the direction of this relationship cannot be determined."

### Fallacy 4: Confound Blindness

**Definition**: Failing to acknowledge or control for plausible alternative causes.

**Example**: 
- Evidence: Schools with music programs have higher test scores
- Claim: "Music education improves academic performance"
- Why it's fallacious: Schools with music programs likely have more resources, more involved parents, and other advantages that independently predict test scores

**Detection**: For every claimed effect, brainstorm three plausible confounds. If none are addressed in the analysis or limitations, the paper has confound blindness.

**Fix**: Acknowledge confounds explicitly. If measurable, control for them statistically. If not measurable, state this as a limitation with the direction of bias.

### Fallacy 5: Straw Man

**Definition**: Presenting a weak or distorted version of an opposing argument to make it easy to refute.

**Example**: 
- Claim: "The rational choice model predicts that people always maximize expected value, but our data show they don't — therefore the rational model is wrong"
- Why it's fallacious: No serious rational choice theorist claims people always maximize EV; the model makes conditional predictions under specific assumptions

**Detection**: Before criticizing an opposing view, check whether proponents would recognize your characterization. If they would say "that's not what we claim," you have a straw man.

**Fix**: Present the strongest version of the opposing argument, then explain why your evidence challenges even that strong version.

### Fallacy 6: Cherry Picking

**Definition**: Selectively reporting results that support the hypothesis while ignoring results that don't.

**Example**: 
- Evidence: 10 analyses conducted; 2 significant results reported
- Claim: "Our findings support the hypothesis"
- Why it's fallacious: With 10 analyses and α = .05, we expect ~0.5 significant results by chance alone; 2 is not impressive

**Detection**: Count the number of analyses implied by the design and compare to the number reported. If the study had multiple DVs, multiple IVs, or multiple time points, all should be reported or the selection should be justified.

**Fix**: Report all preregistered analyses. If exploratory, label them as such. Apply multiple comparison corrections.

### Fallacy 7: Ecological Fallacy

**Definition**: Drawing conclusions about individuals from group-level data.

**Example**: 
- Evidence: Countries with higher chocolate consumption have more Nobel laureates
- Claim: "Eating chocolate makes you smarter"
- Why it's fallacious: The group-level correlation does not imply individual-level causation; the relationship is likely driven by wealth/education confounds

**Detection**: When claims jump from group data to individual behavior, check whether the inference is warranted.

**Fix**: "Countries with higher chocolate consumption also tend to have higher GDP per capita and educational investment, which are more plausible explanations for the Nobel laureate association."

### Fallacy 8: Base Rate Fallacy

**Definition**: Ignoring the base rate when interpreting probabilities or effect sizes.

**Example**: 
- Evidence: A diagnostic test is 95% accurate
- Claim: "A positive test means there's a 95% chance you have the disease"
- Why it's fallacious: If the disease prevalence is 1%, the positive predictive value is only ~16% (not 95%)

**Detection**: When interpreting predictive accuracy, always consider base rates. High accuracy with rare events produces many false positives.

**Fix**: Report positive predictive values, sensitivity, and specificity. In clinical contexts, report NNT (number needed to treat).

### Fallacy 9: Argument from Authority

**Definition**: Claiming something is true because an authority said it, rather than because of evidence.

**Example**: 
- Claim: "As Kahneman (2011) noted, System 1 is fast and System 2 is slow, so framing effects must reflect System 1 dominance"
- Why it's fallacious: Kahneman's authority does not make the specific inference correct; the data must support it

**Detection**: Check whether citations are used as evidence or as authority. If removing the citation removes the only support for the claim, the argument relies on authority.

**Fix**: "Consistent with dual-process theory's prediction that reduced deliberation amplifies biases (Kahneman, 2011), our mediation analysis showed that cognitive load increased framing effects."

### Fallacy 10: Circular Reasoning (Begging the Question)

**Definition**: The conclusion is assumed in the premises.

**Example**: 
- Premise: "People who are depressed withdraw from social interaction"
- Claim: "Social withdrawal is a symptom of depression"
- Why it's fallacious: The conclusion restates the premise without adding new information

**Detection**: Check whether the conclusion could be false even if the premises are true. If not, the argument is circular.

**Fix**: Provide independent evidence for each claim. The premise should be established by data; the conclusion should follow from the premise plus additional reasoning or evidence.

### Fallacy 11: False Dichotomy

**Definition**: Presenting two options as the only possibilities when more exist.

**Example**: 
- Claim: "Either the effect is driven by cognitive load OR by motivational depletion"
- Why it's fallacious: Both could contribute; a third factor could be responsible; they could interact

**Detection**: Search for "either...or" constructions and check whether the alternatives are truly exhaustive.

**Fix**: "Cognitive load and motivational depletion represent two candidate mechanisms; our data favor the load account, though we cannot rule out contributions from depletion or from mechanisms we did not test."

### Fallacy 12: Post Hoc Ergo Propter Hoc

**Definition**: Assuming that because B followed A, A caused B.

**Example**: 
- Evidence: After the intervention, symptoms decreased
- Claim: "The intervention caused symptom reduction"
- Why it's fallacious: Symptoms might have decreased naturally (regression to the mean), due to time, or due to non-specific treatment factors

**Detection**: In pre-post designs without control groups, causal claims are almost always post hoc fallacies.

**Fix**: Use control groups. Without a control: "Symptoms decreased following the intervention, though without a control condition, causal attribution is not possible."

---

## 3. Claim-License Matching

### The Core Principle
Every claim must be licensed by evidence of appropriate strength. The data licenses only certain claims; claiming more is a logical error.

### License Levels

| Evidence Type | Claims Licensed | Claims NOT Licensed |
|---|---|---|
| RCT with active control | "X caused Y in this sample" | "X will cause Y in all contexts" |
| RCT with no-treatment control | "X produced change relative to no treatment" | "X's specific mechanism caused Y" (no control for non-specific factors) |
| Longitudinal with temporal precedence | "X preceded Y" | "X caused Y" (confounds not controlled) |
| Cross-sectional correlation | "X and Y are associated" | "X causes Y"; "X predicts Y over time" |
| Mediation analysis | "The X→Y relationship operates partly through M" | "M causes the X→Y relationship" (mediation ≠ mechanism without experimental manipulation of M) |
| Moderation analysis | "The X→Y relationship depends on W" | "W determines whether X causes Y" |
| Meta-analysis | "The average effect across studies is [size]" | "The true effect is [size]" (publication bias) |
| Single case study | "X can occur in context Y" | "X typically occurs in context Y" |

### The License Check
For every claim in the Discussion, ask:
1. What type of evidence supports this claim? (RCT, observational, correlational, theoretical)
2. What claims does this evidence type license? (see table above)
3. Does the claim stay within the licensed scope?

If the claim exceeds the license, downgrade the language.

---

## 4. Inference Strength Calibration

### The Inference Strength Scale

| Strength Level | Description | Example |
|---|---|---|
| 5: Causal mechanism | Established through experimental manipulation of the mechanism | "Manipulating cognitive load directly alters framing effects, confirming load as the causal mechanism" |
| 4: Causal effect | Established through RCT but mechanism not experimentally verified | "The intervention reduced symptoms relative to control" |
| 3: Strong association | Longitudinal with temporal precedence and confound control | "X predicted Y over time, controlling for plausible confounds" |
| 2: Association | Cross-sectional correlation with covariate adjustment | "X and Y are associated, controlling for Z" |
| 1: Co-occurrence | Observed pattern without control | "X and Y co-occurred in our sample" |

### Matching Language to Inference Strength

| Strength | Appropriate Language | Inappropriate Language |
|---|---|---|
| 5 | "establishes," "confirms the mechanism" | "proves" (never appropriate) |
| 4 | "caused," "produced," "led to" | "established the mechanism" (mechanism not tested) |
| 3 | "predicted," "preceded," "was associated with over time" | "caused" (design doesn't license) |
| 2 | "was associated with," "was related to" | "predicted" (implies temporal order) |
| 1 | "co-occurred with," "was observed alongside" | "was associated with" (implies systematic relationship) |

---

## 5. Logical Flow Checking Across Sections

### The Cross-Section Consistency Audit

Check the logical flow between manuscript sections:

**Introduction → Methods**: 
- Does the Methods section test every hypothesis stated in the Introduction?
- Are the measures appropriate for the constructs mentioned in the Introduction?
- Is the design capable of answering the research question posed?

**Methods → Results**: 
- Are all analyses described in the Methods actually reported in the Results?
- Are there analyses in the Results that were not described in the Methods?
- Are the reported N, exclusions, and conditions consistent across both?

**Results → Discussion**: 
- Does every Discussion claim trace to a specific Result?
- Are there Results that are not discussed?
- Are the interpretations in the Discussion consistent with the statistical results?

**Abstract → Body**: 
- Does the Abstract accurately represent the Body (no overclaiming in Abstract)?
- Are all key findings mentioned in the Abstract?
- Are the effect sizes in the Abstract consistent with those in the Body?

### The Argument Chain Check

Trace the paper's central argument from start to finish:

1. **The claim**: What is the paper's single most important claim?
2. **The evidence**: What specific result most directly supports this claim?
3. **The design**: What design feature makes this evidence trustworthy?
4. **The alternative**: What is the strongest alternative explanation?
5. **The rebuttal**: What evidence or logic rules out this alternative?
6. **The qualifier**: What are the conditions under which the claim might not hold?

If any link in this chain is missing, the argument has a gap.

---

## 6. Premise-Auditing Methodology

### What Is a Premise?
A premise is any statement the paper assumes to be true without directly testing it. Every paper rests on premises. The question is whether those premises are reasonable.

### How to Audit Premises

1. **Identify all premises**: Read the paper and list every statement that is assumed, not demonstrated
2. **Classify each premise**:
   - **Shared premise**: Widely accepted in the field (e.g., "Working memory is capacity-limited")
   - **Contested premise**: Debated in the field (e.g., "Intelligence is unitary")
   - **Unstated premise**: Implicit but never stated (e.g., "Laboratory tasks generalize to real-world behavior")
   - **Novel premise**: Introduced by this paper without prior support
3. **Evaluate each premise**:
   - Shared premises: Acceptable, but cite the foundational work
   - Contested premises: Must be acknowledged and defended
   - Unstated premises: Must be made explicit and their plausibility assessed
   - Novel premises: Must be supported with evidence or clearly labeled as assumptions

### Common Unstated Premises

| Unstated Premise | When It Matters | How to Address |
|---|---|---|
| Lab tasks generalize to real behavior | When making practical claims | Acknowledge; test ecological validity if possible |
| Self-report reflects actual behavior | When using survey measures | Note limitations; cite validation if available |
| The sample is representative | When making population-level claims | Report sample demographics; compare to population |
| The statistical model is correctly specified | When making inferential claims | Test assumptions; report robustness to alternatives |
| The manipulation affected the intended construct | When making causal claims | Report manipulation checks; address alternative manipulations |
| The measures are reliable and valid | When interpreting scores | Report reliability; cite validity evidence |

---

## 7. Fixing Logical Gaps Without New Data

### Strategy 1: Recalibrate the Claim
If the data do not license the claim, weaken the claim to match the data.

**Before**: "X causes Y"
**After**: "X is associated with Y, consistent with a causal account, though this design cannot establish causation"

### Strategy 2: Add the Missing Step
If the argument skips a logical step, add the intermediate reasoning.

**Before**: "X predicts Y, so interventions targeting X should reduce Y"
**After**: "X predicts Y, and if this relationship is causal — which our design cannot establish — interventions targeting X might reduce Y"

### Strategy 3: Acknowledge the Alternative
If a plausible alternative explanation exists, acknowledge it and explain why your interpretation is favored.

**Before**: "The effect is driven by cognitive load"
**After**: "The effect is consistent with a cognitive load account, though a motivational depletion account cannot be ruled out without directly manipulating depletion independently of load"

### Strategy 4: Restrict the Scope
If the claim overgeneralizes, restrict it to the conditions under which the evidence applies.

**Before**: "Framing distorts all strategic decisions"
**After**: "Framing distorts strategic decisions under time pressure in our sample of financial managers; whether this extends to other populations or decision contexts requires further investigation"

### Strategy 5: Convert Assertion to Hypothesis
If a claim lacks sufficient support, convert it from a conclusion to a hypothesis for future testing.

**Before**: "Debiasing requires structural support"
**After**: "Our findings are consistent with the hypothesis that debiasing requires structural support; a direct test comparing structural vs. awareness interventions would be needed to confirm this"

### Strategy 6: Use the Qualifier
Add appropriate hedges that signal the uncertainty level.

**Before**: "This demonstrates that..."
**After**: "This provides evidence consistent with the possibility that..."

### Strategy 7: Add the Rebuttal
Explicitly state the conditions under which the claim would not hold.

**Before**: "Cognitive load drives framing effects"
**After**: "Cognitive load drives framing effects under the conditions tested here — where the load is induced by time pressure on numerical decisions. Whether this mechanism operates when load is induced by other means (e.g., concurrent tasks, emotional stress) remains to be tested."
