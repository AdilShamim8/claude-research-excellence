# Abstract Mastery Guide

## Purpose
The abstract is the most read and least well-written part of most papers. This guide provides a rigorous architecture for constructing abstracts that are precise, compelling, and impossible to misinterpret. Every word must earn its place within strict word limits.

---

## 1. The 7-Sentence Abstract Architecture

The abstract is not a summary — it is an argument compressed into its minimum viable form. Each sentence has one function. Do not combine functions. Do not skip functions.

### Sentence 1: THE HOOK

**Function**: Make someone outside your subfield care.

**Formula**: "[Broad domain] faces [specific problem] that [consequence]."

**What it does**: Establishes relevance. The reader should think "Yes, that matters" before they reach the period.

**Common mistakes**:
- Too narrow: "The dorsolateral prefrontal cortex has been implicated in working memory updating." (Only neuroscientists care.)
- Too vague: "Decision-making is important." (Everyone already knows.)
- Too trendy: "In the era of AI, decision-making faces new challenges." (Meaningless.)

**Good examples by field**:

*Social Psychology*: "Interpersonal trust deteriorates under economic uncertainty, yet the cognitive mechanisms driving this decline remain unidentified."

*Cognitive Neuroscience*: "Working memory capacity constrains complex reasoning, but whether this bottleneck arises from storage limitations or attentional filtering failures is debated."

*Clinical Psychology*: "Exposure therapy effectively reduces phobic responses, yet 30-40% of patients relapse within a year, suggesting a missing mechanistic target."

*Computational Science*: "Graph neural networks achieve state-of-the-art performance on node classification, but their vulnerability to adversarial perturbations limits deployment in safety-critical systems."

*Public Health*: "Vaccination hesitancy continues to undermine herd immunity, yet current communication strategies fail to address the specific belief architectures that sustain resistance."

### Sentence 2: THE GAP

**Function**: Identify exactly what is unknown and why it matters.

**Formula**: "However, [what is unknown] remains unclear because [why it is unknown]."

**What it does**: Creates the intellectual tension. The reader should think "I need to know the answer to this."

**Gap types and templates**:

| Gap Type | Template | Example |
|---|---|---|
| Mechanism gap | "However, the mechanism through which X produces Y remains unclear because [confound/design limitation]." | "However, the mechanism through which social exclusion increases aggression remains unclear because prior studies could not disentangle threat perception from belongingness loss." |
| Boundary gap | "However, whether X extends to [boundary condition] is unknown because [why not tested]." | "However, whether this effect extends to clinically diagnosed populations is unknown because laboratory studies have relied exclusively on subclinical samples." |
| Reconciliation gap | "However, whether X or Y accounts for [phenomenon] is unresolved because [methodological limitation]." | "However, whether cognitive load or motivational depletion accounts for the impairment is unresolved because prior manipulations confounded the two." |
| Existence gap | "However, whether [phenomenon] exists at all in [context] is unknown because [why not tested]." | "However, whether neural replay occurs during waking rest in humans is unknown because non-invasive methods lacked the temporal resolution to detect it." |
| Generalizability gap | "However, whether [finding] replicates across [dimension] remains untested because [sample limitation]." | "However, whether this framing effect replicates across cultures remains untested because all prior studies used Western samples." |

### Sentence 3: THE APPROACH (Method)

**Function**: State what you did — design, sample, and manipulation/measures.

**Formula**: "Using [design], we [action verb] [sample] on/with [key measures]."

**Examples**:

"Using a preregistered 2×2 between-subjects design, we randomly assigned 312 community-dwelling adults to social exclusion or inclusion conditions and measured aggression via the Taylor Aggression Paradigm."

"Using a longitudinal cohort design with three annual assessments, we tracked 1,847 adolescents and measured depressive symptoms, peer victimization, and emotion regulation strategies."

"Using a computational modeling approach, we fitted three competing decision-making architectures to choice data from 128 participants completing a novel two-armed bandit task."

### Sentence 4: THE APPROACH (Analysis)

**Function**: State how you tested the hypothesis — analysis method and specific prediction.

**Formula**: "[Analysis approach] tested whether [specific prediction]."

**Examples**:

"Bayesian multilevel mediation models tested whether threat perception mediated the exclusion-aggression link."

"Latent growth curve modeling tested whether emotion regulation strategies moderated the trajectory of depressive symptoms over time."

"Parameter recovery simulations and out-of-sample prediction tested whether the dual-learning-rate model outperformed single-rate alternatives."

### Sentence 5: FINDING 1 (Primary)

**Function**: Report the most important result with quantitative precision.

**Formula**: "[Direction of effect]: [quantitative description], [statistic], [effect size], [CI]."

**Rules**:
- Always include direction ("higher," "lower," "faster," "increased")
- Include a concrete magnitude (percent change, raw difference, or odds ratio)
- Include formal statistic when space permits
- Always include effect size

**Examples**:

"Excluded participants aggressed more: 43% higher punishment selections, b = 3.21, 95% CI [2.14, 4.28], d = 0.62."

"Peer victimization predicted a 2.4-fold increase in depressive symptom growth rate, β = 0.18, SE = 0.04, p < .001."

"The dual-learning-rate model provided superior fit: protected exceedance probability = 0.91, with the learning rate for negative outcomes twice that for positive outcomes (α⁻ = 0.38 vs α⁺ = 0.19)."

### Sentence 6: FINDING 2 (Secondary or Mechanism)

**Function**: Report the second key result. If mediation was tested, this is the mechanism finding.

**Formula**: "[Secondary finding or mechanism result with quantification]."

**Examples**:

"Threat perception fully mediated this effect: indirect effect = 1.87, 95% CI [0.93, 2.94]."

"Cognitive reappraisal buffered the victimization-depression link: the interaction reduced the growth rate by 38%, β = −0.07, p = .008."

"Model comparison revealed that the asymmetry was driven by the loss-learning rate alone, as the gain-learning rate did not differ from the single-rate model (pxp = 0.04)."

### Sentence 7: THE IMPLICATION

**Function**: State what this means — calibrated between overclaiming and underclaiming.

**Formula**: "These findings [contribution verb] by [mechanism], suggesting that [implication]."

**Calibration levels**:

| Strength | Language | When Appropriate |
|---|---|---|
| Strong | "These findings establish that..." | Multiple converging experiments; large effect; preregistered |
| Moderate | "These findings advance understanding by..." | Single well-designed study; clear mechanism |
| Cautious | "These findings suggest that..." | Exploratory analysis; first evidence in new domain |
| Minimal | "These findings provide initial evidence that..." | Pilot; very small N; unreplicated |

**Examples**:

*Strong*: "These findings establish threat perception as the active mechanism linking exclusion to aggression, suggesting that interventions targeting threat appraisal — not social belonging — may reduce reactive aggression."

*Moderate*: "These findings advance emotion regulation theory by identifying cognitive reappraisal as a resilience factor, suggesting that prevention programs should prioritize reappraisal skills training."

*Cautious*: "These findings suggest that asymmetric learning rates may underlie the negativity bias in decision-making, warranting investigation of whether this mechanism generalizes to clinical populations."

---

## 2. Field-Specific Abstract Conventions

### Empirical / Experimental
- Emphasize design and causal inference
- Report N, design type, and randomization
- Include effect sizes with CIs
- State the mechanism if tested
- Word allocation: Hook (10%), Gap (10%), Method (25%), Analysis (10%), Findings (30%), Implication (15%)

### Computational / Modeling
- Emphasize model comparison and prediction
- State the competing models or algorithms
- Report fit indices, prediction accuracy, or parameter recovery
- Note generalization or out-of-sample validation
- Word allocation: Hook (10%), Gap (10%), Approach (25%), Model comparison (20%), Results (20%), Implication (15%)

### Theoretical / Review
- Emphasize the integrative argument
- State the scope of evidence reviewed
- Describe the novel framework or synthesis
- Identify testable predictions generated
- Word allocation: Hook (15%), Gap (15%), Scope (15%), Synthesis (30%), Predictions (15%), Implication (10%)

### Clinical / Translational
- Emphasize clinical relevance and patient impact
- Report sample characteristics (diagnosis, severity)
- Include clinical significance metrics (NNT, clinically meaningful change)
- State implications for treatment or assessment
- Word allocation: Hook (10%), Gap (10%), Method (20%), Analysis (10%), Findings (30%), Clinical implication (20%)

---

## 3. Abstract Word Budget Strategies

### Common Word Limits and Allocation

| Limit | Hook | Gap | Method | Analysis | Finding 1 | Finding 2 | Implication |
|---|---|---|---|---|---|---|---|
| 150 words | 15 | 20 | 30 | 15 | 30 | 25 | 15 |
| 200 words | 20 | 25 | 40 | 20 | 40 | 35 | 20 |
| 250 words | 25 | 30 | 50 | 25 | 50 | 45 | 25 |
| 300 words | 30 | 35 | 60 | 30 | 60 | 55 | 30 |

### Compression Techniques

1. **Merge Method + Analysis**: "We used [design] and tested predictions with [analysis]" — saves 5-8 words
2. **Combine Findings**: "X was [Y% higher/lower] and this effect was mediated by [M]" — saves 8-12 words
3. **Use parentheses for CIs**: "d = 0.62 [0.31, 0.93]" instead of "d = 0.62, 95% CI [0.31, 0.93]" — saves 3 words
4. **Abbreviate after first use**: Define once, then use acronym
5. **Remove methodological qualifiers**: "a preregistered 2×2 between-subjects design" → "a 2×2 design" if preregistration is noted elsewhere
6. **Active voice saves words**: "We measured aggression" (3) vs "Aggression was measured" (3, but requires "by [instrument]" adding words)

---

## 4. Hook Sentence Formula with Examples

### Formula Structure
[Broad domain] + [active verb: faces/produces/constrains/threatens/drives] + [specific problem] + [that/which] + [consequence]

### Examples from Top-Tier Publications

**Science-style hook**: "Social networks amplify emotional contagion, creating cascades of affective states that shape collective behavior."

**Nature-style hook**: "Protein folding misregulation drives neurodegeneration, yet the cellular quality control mechanisms that prevent toxic aggregation in living neurons remain unidentified."

**Lancet-style hook**: "Antimicrobial resistance threatens modern medicine, with resistant infections causing 1.27 million deaths annually — a toll projected to exceed cancer mortality by 2050."

**PNAS-style hook**: "Human cooperation sustains societies, yet the conditions under which cooperation emerges among strangers without repeated interaction remain fiercely debated."

**Psych Science-style hook**: "First impressions form within milliseconds, but whether these rapid judgments are driven by perceptual fluency or stereotype activation has proven difficult to disentangle."

### Anti-Patterns (What NOT to Do)

❌ "Research on X has grown in recent years." (Says nothing.)
❌ "X is a pervasive phenomenon." (So what?)
❌ "Many studies have examined X." (And?)
❌ "The study of X has a long history." (Irrelevant.)
❌ "In today's world, X is increasingly important." (Vague and cliché.)

---

## 5. Quantification Standards for Findings in Abstracts

### Rules for Reporting Numbers in Abstracts

1. **Always report direction**: "higher," "lower," "faster," "slower" — never just "different"
2. **Always report magnitude**: Percent change, raw difference, or ratio — never just "significant"
3. **Always report effect size**: d, η², β, OR — something that communicates practical significance
4. **Always report precision**: CI or SE — indicate uncertainty
5. **Use concrete numbers over descriptors**: "23% higher" not "substantially higher"

### What to Report by Analysis Type

| Analysis | Report in Abstract | Example |
|---|---|---|
| t-test | Direction, d, CI | "higher, d = 0.65, 95% CI [0.31, 0.99]" |
| ANOVA | Direction, η²_p | "higher, η²_p = .14" |
| Regression | β, p | "β = 0.32, p < .001" |
| Logistic regression | OR, CI | "OR = 2.41, 95% CI [1.63, 3.56]" |
| Mediation | Indirect effect, CI | "indirect effect = 0.18, 95% CI [0.06, 0.31]" |
| Mixed model | b, CI | "b = 1.23, 95% CI [0.67, 1.79]" |
| Model comparison | Fit metric | "BF₁₀ = 34.2" or "AIC difference = 12.4" |

---

## 6. Implication Sentence Calibration

### The Overclaim-Underclaim Spectrum

| Claim Strength | Example | Verdict |
|---|---|---|
| Overclaim | "These findings prove that X causes Y, revolutionizing our understanding." | Rejected — "prove" and "revolutionize" are unjustified |
| Strong (appropriate for RCT with large effect) | "These findings establish that X causes Y, suggesting that interventions targeting X could reduce Y." | Appropriate — "establish" warranted by design; "could" hedges application |
| Moderate (appropriate for well-powered observational study) | "These findings advance understanding by showing that X predicts Y, suggesting that X may be a viable intervention target." | Appropriate — "advance" is moderate; "may" hedges |
| Cautious (appropriate for exploratory/correlational study) | "These findings provide initial evidence that X and Y are associated, warranting experimental investigation." | Appropriate — "initial" and "warranting" calibrate correctly |
| Underclaim | "These findings are consistent with the possibility that X might be related to Y in some contexts." | Rejected — triple hedging ("consistent with," "possibility," "might") undermines contribution |

### Hedging Calibration Table

| Evidence Strength | Appropriate Hedges |
|---|---|
| Preregistered RCT, large N, replicated | "establish," "demonstrate" (in causal sense), "indicate clearly" |
| Well-powered RCT, single study | "show," "indicate," "provide evidence that" |
| Preregistered observational, strong design | "suggest," "provide evidence consistent with" |
| Exploratory observational | "provide initial evidence," "suggest," "raise the possibility" |
| Correlational, small N | "are consistent with," "may," "warrant further investigation" |

---

## 7. Abstract Revision Checklist

- [ ] Sentence 1 would interest someone outside my subfield
- [ ] Sentence 2 names a specific gap, not a vague "more research is needed"
- [ ] Sentence 3 states the design, sample, and key measures
- [ ] Sentence 4 states the analysis approach and specific prediction
- [ ] Sentence 5 reports the primary finding with direction, magnitude, and effect size
- [ ] Sentence 6 reports the secondary finding or mechanism
- [ ] Sentence 7 states an implication calibrated to evidence strength
- [ ] No sentence performs more than one function
- [ ] Every number is necessary (no decorative statistics)
- [ ] No word from the Never-Use list appears
- [ ] The abstract stands alone — fully interpretable without the rest of the paper
- [ ] Word count is within the journal limit
- [ ] Keywords are selected for discoverability (if required)

---

## 8. Before/After Abstract Transformations

### Example 1: Social Psychology

**BEFORE (Weak):**
The present study investigated the effect of social exclusion on aggressive behavior. Participants were randomly assigned to either an exclusion or inclusion condition. Results indicated that excluded participants were significantly more aggressive than included participants (p < .05). The findings are discussed in terms of their theoretical implications for understanding social behavior. These results contribute to the existing literature on exclusion and may have practical implications for interventions.

**Problems**: Vague hook, no gap, no effect sizes, no mechanism, hedged implication, never-use words ("significantly," "existing literature," "may have"), no direction or magnitude.

**AFTER (Strong):**
Social exclusion increases aggression, yet the cognitive mechanism driving this link remains unidentified because prior studies confounded threat perception with belongingness loss. Using a preregistered 2×2 design, we randomly assigned 312 adults to exclusion or inclusion and measured aggression via the Taylor Paradigm. Bayesian mediation models tested whether threat perception drives the exclusion-aggression link. Excluded participants aggressed 43% more, d = 0.62, 95% CI [0.31, 0.93]. Threat perception fully mediated this effect: indirect effect = 1.87, 95% CI [0.93, 2.94]. These findings establish threat appraisal — not belongingness — as the active mechanism, suggesting that interventions targeting threat interpretation could reduce reactive aggression.

### Example 2: Clinical Research

**BEFORE (Weak):**
Depression is a major public health problem. Many treatments exist but not everyone responds. We conducted a study to see if a new digital intervention would help. Participants used the app for 8 weeks. Results showed improvement in depression scores. The results were significant. Implications for digital mental health are discussed.

**Problems**: No specific gap, no design description, no quantification, no effect sizes, meaningless "significant," vague implication, multiple never-use phrases.

**AFTER (Strong):**
Digital cognitive behavioral therapy (dCBT) reduces mild-to-moderate depression, but 40% of patients fail to engage sufficiently — a barrier whose predictors remain unknown because adherence studies have relied on post-hoc self-report rather than objective usage metrics. In a randomized controlled trial, 456 adults with moderate depression received 8 weeks of dCBT with passive smartphone sensing of engagement. Latent class growth analysis tested whether early usage patterns predicted clinical response. Three engagement trajectories emerged: rapid adopters (32%), gradual engagers (41%), and non-engagers (27%). Rapid adopters showed 58% greater symptom reduction than non-engagers, β = −4.3, 95% CI [−5.8, −2.8], with day-3 usage predicting 8-week outcome (AUC = 0.81). These findings identify a 72-hour engagement window as the critical intervention point, suggesting that adaptive outreach triggered by early non-engagement could prevent treatment failure.

### Example 3: Computational Neuroscience

**BEFORE (Weak):**
We developed a new model of decision making under uncertainty. The model was compared to existing models. Our model fit the data better than the other models. The parameters of the model showed interesting patterns. We discuss the implications for understanding how people make decisions.

**Problems**: No hook, no gap, no quantification of model comparison, "interesting" is on the never-use list, vague implication, no methodological detail.

**AFTER (Strong):**
Decision-making under uncertainty requires balancing exploration and exploitation, yet whether humans achieve this balance through random noise or directed uncertainty-seeking remains debated because prior models could not dissociate the two. Using a novel three-armed bandit task (N = 128), we fitted three computational models: ε-greedy, softmax, and directed exploration. Parameter recovery simulations and out-of-sample prediction (10-fold cross-validation) tested model adequacy. Directed exploration outperformed alternatives: protected exceedance probability = 0.94, with an information bonus parameter of 3.8 ± 0.6 applied to uncertain options. These findings establish directed uncertainty-seeking as the dominant exploration strategy, suggesting that neural models of decision-making must incorporate epistemic value signals beyond expected reward.
