# CRES Framework Example: Social Science Research

## Research Area: Social Media's Effect on Democratic Deliberation

This document demonstrates a complete walkthrough of the Claude Research Excellence System (CRES) applied to a social science research paper on how social media platforms affect the quality of democratic deliberation.

---

## Step 1: IDEATION

### 1.1 Field Cartography — Frontier Scan

**Domain:** Social Media and Democratic Deliberation
**Scan Date:** 2025-02-28
**Literature Corpus:** 1,124 papers (2004–2025)

| Sub-area | Saturation | Growth Rate | Key Venues | Representative Papers |
|---|---|---|---|---|
| Echo Chambers / Filter Bubbles | HIGH (0.87) | Plateau | APSR, Poetics | Sunstein 2001; Pariser 2011; Bail et al. 2018 |
| Political Polarization & Social Media | HIGH (0.82) | Declining | AJPS, JOP | Boxell et al. 2017; Guess 2021; Tucker et al. 2018 |
| Misinformation Spread | HIGH (0.78) | Plateau | Science, PNAS | Vosoughi et al. 2018; Pennycook & Rand 2021 |
| Platform Algorithm Effects | MEDIUM (0.56) | Growing | Nature, Science | Huszár et al. 2022; Thorson et al. 2023 |
| Deliberative Quality Metrics | LOW (0.31) | Growing | J Delib. Dem., Polit. Theory | Steenbergen et al. 2003; Black et al. 2011 |
| Cross-Cultural Comparative Studies | VERY LOW (0.18) | Nascent | — | Very few; mostly single-country |
| Algorithm vs. User Attribution | LOW (0.24) | Accelerating | JOP, POQ | Guess et al. 2023; Makhortykh et al. 2023 |
| Causal Mechanisms of Deliberative Degradation | VERY LOW (0.12) | Nascent | — | No canonical papers; mostly correlational |
| Deliberation in Authoritarian Contexts | LOW (0.27) | Growing | J Dem., Comp. Polit. | King et al. 2013; Roberts 2020 |
| Interventions to Improve Deliberation | LOW (0.33) | Growing | PNAS, Science | Pennycook et al. 2020; Mosleh et al. 2024 |

**Frontier Verdict:** The most promising unsaturated zones are **causal mechanisms of deliberative degradation** (0.12 saturation, nascent), **cross-cultural comparative studies** (0.18 saturation, nascent), and **algorithm vs. user attribution** (0.24 saturation, accelerating). The echo chamber and polarization literatures are saturated (0.82–0.87) and unlikely to yield high-novelty contributions.

---

### 1.2 Gap Typology — Identified Gaps

**Gap 1: No Causal Evidence on the Mechanisms Through Which Social Media Degrades Deliberative Quality**
- **Type:** Causal Identification Gap
- **Description:** The existing literature documents correlations between social media use and various indicators of poor deliberation (polarization, incivility, misinformation belief), but almost no studies identify the *causal mechanisms* through which social media exposure degrades deliberative quality. Three candidate mechanisms remain untested: (a) *attention fragmentation* — social media reduces the sustained attention necessary for complex argument evaluation; (b) *affective priming* — algorithmic ranking of emotionally arousing content primes affective rather than deliberative processing; and (c) *norm erosion* — exposure to uncivil online discourse shifts perceived norms of acceptable deliberative behavior. Each mechanism implies different interventions but has not been causally isolated.
- **Evidence of Gap:** Bail et al. (2018) shows effects of exposure but does not isolate mechanisms. Guess (2021) documents behavioral patterns without causal chain. Vosoughi et al. (2018) describes diffusion but not deliberative impact. The deliberative democracy literature (Habermas, 1984; Dryzek, 2000) theorizes mechanisms but has not been empirically linked to social media research.
- **Opportunity Score:** 9.5/10

**Gap 2: Absence of Cross-Cultural Comparative Evidence on Social Media and Deliberation**
- **Type:** External Validity / Generalizability Gap
- **Description:** Over 87% of studies on social media and democratic deliberation use data from the United States or Western Europe. This creates a profound generalizability problem: deliberative norms, media ecosystems, institutional contexts, and platform usage patterns differ radically across cultural contexts. Whether social media degrades deliberation in the same ways and through the same mechanisms in, for example, India, Brazil, Nigeria, or Japan is empirically unknown. The assumption of universal effects is theoretically unjustified given well-documented cultural variation in deliberative norms (Hansen, 2020; Yamamura & Tsutsui, 2022).
- **Evidence of Gap:** King et al. (2013) studied Chinese social media but from a control rather than deliberation perspective. Roberts (2020) examines authoritarian contexts but not deliberative quality. No study systematically compares deliberative degradation across diverse democratic contexts.
- **Opportunity Score:** 8.8/10

**Gap 3: No Decomposition of Algorithm vs. User-Driven Effects on Deliberative Quality**
- **Type:** Attribution Gap
- **Description:** When social media users encounter poor deliberative content (incivil arguments, misinformation, homogeneous viewpoints), it is unclear whether this results from (a) algorithmic curation that prioritizes engagement-optimized content (algorithm-driven), (b) users' own preferences for affectively congruent and simplified content (user-driven), or (c) an interaction between the two. This attribution matters enormously for policy: regulating algorithms is feasible while regulating user preferences is not. No study has experimentally decomposed the relative contribution of algorithmic vs. user-driven factors to deliberative quality.
- **Evidence of Gap:** Huszár et al. (2022) characterizes algorithm behavior but without user-side comparison. Guess et al. (2023) examines user demand but without algorithm manipulation. Makhortykh et al. (2023) audits algorithms but not in interaction with user behavior.
- **Opportunity Score:** 9.0/10

---

### 1.3 Question Forge — Research Questions

**RQ1: Through which causal mechanisms does social media exposure degrade the quality of democratic deliberation, and can these mechanisms be experimentally isolated?**
- **Specificity:** 9/10 — Defines the outcome (deliberative quality), the causal question (mechanisms), and the methodological approach (experimental isolation)
- **Feasibility:** 7/10 — Requires a multi-experiment design with novel manipulation development; feasible with adequate funding but complex
- **Novelty:** 10/10 — No existing study causally isolates deliberative degradation mechanisms
- **Impact:** 9/10 — Directly informs intervention design and platform regulation
- **Composite Score:** **8.9/10** ★ SELECTED

**RQ2: Does social media degrade deliberative quality through the same mechanisms across culturally diverse democratic contexts?**
- **Specificity:** 8/10 — Cross-cultural comparison with mechanism focus; well-defined
- **Feasibility:** 5/10 — Requires multi-site international collaboration; translation; cultural adaptation of instruments
- **Novelty:** 9/10 — First cross-cultural comparative study of deliberative mechanisms
- **Impact:** 8/10 — Important for generalizability but secondary to causal identification
- **Composite Score:** **7.5/10**

**RQ3: What are the relative contributions of algorithmic curation versus user preferences to the degradation of deliberative quality on social media?**
- **Specificity:** 8/10 — Clear attribution question with policy relevance
- **Feasibility:** 6/10 — Requires platform cooperation or sophisticated simulation; challenging
- **Novelty:** 8/10 — Novel decomposition but builds on existing algorithm audit work
- **Impact:** 9/10 — Directly relevant to regulation (Section 230, EU DSA)
- **Composite Score:** **7.8/10**

---

### 1.4 Contribution Map — For RQ1 (Causal Mechanisms)

| Contribution Type | Description | Novelty Level | Priority |
|---|---|---|---|
| **C1: Theoretical** | A formalized three-mechanism model of deliberative degradation specifying (a) attention fragmentation via micro-interruption, (b) affective priming via emotional content ranking, and (c) norm erosion via exposure to incivil discourse — with testable predictions for each mechanism's distinct behavioral signature | HIGH — First formal causal model connecting social media features to deliberative outcomes | PRIMARY |
| **C2: Empirical** | Three pre-registered experiments isolating each mechanism: (E1) attention fragmentation manipulation via notification interruption during deliberation, (E2) affective priming manipulation via exposure to emotionally-valenced vs. neutral content feeds, (E3) norm erosion manipulation via exposure to civil vs. incivil online discourse | HIGH — First experimental isolation of deliberative degradation mechanisms | PRIMARY |
| **C3: Methodological** | A validated behavioral measure of deliberative quality (the Deliberative Capacity Index, DCI) combining (a) argument complexity, (b) perspective-taking, (c) evidence citation, and (d) willingness to revise — measured through a structured deliberation task with behavioral coding | MEDIUM-HIGH — Extends Steenbergen et al. (2003) DQI to online contexts with behavioral validation | SECONDARY |
| **C4: Mediation Analysis** | Formal mediation analysis demonstrating that the three mechanisms account for 67% of the total effect of social media exposure on deliberative quality, with affective priming as the dominant pathway (indirect effect: β = 0.31, 95% CI: [0.24, 0.38]) | MEDIUM — Standard mediation contribution but with novel mediators | SUPPORTING |
| **C5: Policy** | A mechanism-targeted intervention framework showing that (a) attention-protective features (reading mode, focus timers) address fragmentation, (b) affect-labeling and emotion regulation prompts address affective priming, and (c) norm-nudging and civility commitments address norm erosion — with preliminary pilot data | MEDIUM-HIGH — Translational contribution with direct policy relevance | SUPPORTING |

---

### 1.5 Novelty Certificate

```
╔══════════════════════════════════════════════════════════════════╗
║                    CRES NOVELTY CERTIFICATE                      ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  Research Question: Through which causal mechanisms does social   ║
║  media exposure degrade the quality of democratic deliberation,   ║
║  and can these mechanisms be experimentally isolated?             ║
║                                                                  ║
║  Proposed Title: "Unraveling the Mechanisms: How Social Media    ║
║  Degrades Democratic Deliberation"                               ║
║                                                                  ║
║  ┌─ Novelty Assessment ──────────────────────────────────────┐   ║
║  │                                                            │   ║
║  │  Conceptual Novelty:     9.5 / 10  (██████████)          │   ║
║  │  • First formal causal model of deliberative degradation  │   ║
║  │  • Bridges deliberative theory & media effects research   │   ║
║  │                                                            │   ║
║  │  Methodological Novelty: 8.8 / 10  (█████████░)          │   ║
║  │  • First experimental isolation of mechanisms              │   ║
║  │  • Novel DCI behavioral measure                            │   ║
║  │                                                            │   ║
║  │  Empirical Novelty:      9.0 / 10  (█████████░)          │   ║
║  │  • Causal evidence where only correlations existed         │   ║
║  │  • Three-experiment design with mediation                  │   ║
║  │                                                            │   ║
║  │  COMPOSITE NOVELTY:      9.1 / 10  (█████████░)          │   ║
║  │                                                            │   ║
║  │  Novelty Classification: VERY HIGH NOVELTY                 │   ║
║  │  Risk Assessment: Moderate — experimental manipulations    │   ║
║  │  require careful validation; ecological validity concern    │   ║
║  └────────────────────────────────────────────────────────────┘   ║
║                                                                  ║
║  Nearest Prior Art:                                              ║
║  1. Bail et al. (2018) — Exposure effects, no mechanism test     ║
║  2. Vosoughi et al. (2018) — Diffusion, not deliberation         ║
║  3. Pennycook & Rand (2021) — Misinformation, not deliberation   ║
║  4. Steenbergen et al. (2003) — DQI measure, not online/social   ║
║                                                                  ║
║  Differentiation: This is the FIRST study to experimentally      ║
║  isolate the CAUSAL MECHANISMS through which social media         ║
║  degrades deliberation, moving beyond correlational patterns.     ║
║                                                                  ║
║  Certificate ID: CRES-NC-2025-SS-0057                            ║
║  Date: 2025-02-28                                                ║
╚══════════════════════════════════════════════════════════════════╝
```

---

## Step 2: LITERATURE

### 2.1 Temporal Mapping

**Era 1: Early Internet Studies (2004–2010) — Optimism and Concern**
- Sunstein (2001) — *Republic.com*; raises the echo chamber concern theoretically before social media dominance
- Dahlberg (2001) — The internet and democratic discourse; early normative framework
- Hindman (2009) — *The Myth of Digital Democracy*; challenges cyber-optimism with empirical evidence
- Key insight: The internet's democratic promise is contingent on design, not inherent

**Era 2: Social Media Emergence (2010–2016) — Platform Politics**
- Pariser (2011) — *The Filter Bubble*; popularizes algorithmic curation concerns
- Barbera et al. (2015) — Tweeting from left to right; first large-scale network analysis of polarization
- Flaxman et al. (2016) — Filter bubbles and echo chambers on Facebook; exposure diversity measurement
- Key insight: Algorithmic curation and social network structure jointly shape information exposure

**Era 3: Post-2016 Reckoning (2016–2020) — Empirical Turn**
- Bail et al. (2018) — Exposure to opposing views on Twitter can increase polarization; landmark experimental study
- Vosoughi et al. (2018) — The spread of true and false news online; Science paper documenting misinformation velocity
- Boxell et al. (2017) — Greater internet use is NOT associated with faster polarization growth; challenges narrative
- Guess (2021) — (Almost) everything is correlated with political polarization; methodological caution
- Key insight: The causal story is far more complex than the popular narrative; correlation ≠ causation

**Era 4: Mechanistic and Intervention Research (2020–2025) — Current Frontier**
- Pennycook et al. (2020) — Accuracy nudges reduce misinformation sharing; intervention-oriented
- Mosleh et al. (2024) — Reflection interventions for sharing behavior
- Huszár et al. (2022) — Algorithmic amplification on Twitter
- Guess et al. (2023) — User demand vs. algorithm supply for political content
- Thorson et al. (2023) — Algorithm effects on political attitudes
- **THE GAP:** No study has experimentally isolated the causal mechanisms through which social media degrades deliberative quality. The literature has moved from documenting correlations to testing interventions without identifying the underlying causal chain.

### 2.2 Competing Schools of Thought

| School | Core Claim | Key Proponents | Strength | Weakness | Relation to This Work |
|---|---|---|---|---|---|
| **Techno-Optimist** | Social media expands deliberative participation and democratizes discourse; problems are transitional | Shirky (2008); Coleman & Blum-Ross (2019) | Highlights genuine participation gains | Downplays structural platform incentives; survivorship bias toward positive cases | Our work tests whether the mechanisms of degradation outweigh participation gains |
| **Techno-Pessimist** | Social media inherently degrades deliberation through algorithmic manipulation, echo chambers, and misinformation | Sunstein (2001, 2017); Pariser (2011); Zuboff (2019) | Identifies real structural problems | Often relies on correlational evidence; assumes uniform effects; can be paternalistic | Our work provides causal evidence that can refine or challenge pessimist claims |
| **Contextualist** | Social media's effects on deliberation are conditional on institutional context, platform design, and user characteristics | Chadwick & Vaccari (2019); Tucker et al. (2018); Guess (2021) | Theoretically nuanced; accounts for heterogeneity | Can be empirically vague; "it depends" is unsatisfying for policy | Our work identifies specific mechanisms that may vary across contexts (linking to RQ2) |

### 2.3 Synthesis Paragraph Example

> The scholarly debate over social media's democratic effects has reached an impasse between techno-optimist narratives of expanded participation (Shirky, 2008) and techno-pessimist accounts of deliberative degradation (Sunstein, 2017), with contextualists correctly noting the heterogeneity of effects (Tucker et al., 2018) but offering insufficient guidance on *which contextual factors matter and why*. This impasse persists because the literature has overwhelmingly documented *whether* social media affects deliberation — through correlational studies of polarization (Barbera et al., 2015), experimental studies of exposure effects (Bail et al., 2018), and observational studies of misinformation spread (Vosoughi et al., 2018) — without isolating *through which mechanisms* these effects operate. Three candidate mechanisms emerge from the theoretical literature — attention fragmentation (Carr, 2010; Wu, 2016), affective priming (Brady et al., 2017; Vosoughi et al., 2018), and norm erosion (Cialdini et al., 1990; Anderson et al., 2014) — but no study has experimentally decomposed their independent contributions. This mechanistic gap is not merely academic: each mechanism implies a fundamentally different intervention strategy (attention-protective design, affect-regulation prompts, or norm-nudging, respectively), making causal mechanism identification a prerequisite for evidence-based platform governance.

---

## Step 3: METHODOLOGY

### 3.1 Mixed Methods Design

**Overall Design:** Three-experiment sequence + qualitative interviews (Explanatory Sequential Mixed Methods)

**Experiment 1: Attention Fragmentation (E1)**
- **Design:** Between-subjects, 3 conditions
  - Condition A: Deliberation task WITH micro-interruptions (notifications every 45 seconds mimicking social media)
  - Condition B: Deliberation task WITHOUT interruptions (focused mode)
  - Condition C: Deliberation task with NON-SOCIAL interruptions (neutral tone, same frequency)
- **Sample:** n = 450 (150 per condition; MTurk/Prolific pre-screened for political engagement)
- **Task:** Participants read a policy brief on immigration reform, then engage in a structured written deliberation with a confederate presenting counterarguments
- **Outcome:** Deliberative Capacity Index (DCI) score
- **Mechanism Test:** If Condition A < Condition B AND Condition A < Condition C, fragmentation is not just about interruption frequency but the social-media-specific quality of interruptions

**Experiment 2: Affective Priming (E2)**
- **Design:** Between-subjects, 4 conditions
  - Condition A: Exposure to emotionally-arousing social media feed (moral outrage content) before deliberation
  - Condition B: Exposure to emotionally-neutral social media feed before deliberation
  - Condition C: Exposure to emotionally-arousing content in NON-social-media format (news article)
  - Condition D: No exposure control
- **Sample:** n = 600 (150 per condition)
- **Task:** Same deliberation task as E1
- **Outcome:** DCI score + physiological arousal measures (self-reported affect + optional heart rate from wearable for subset)
- **Mechanism Test:** If Condition A < Condition B AND Condition A < Condition C, the effect is specific to social media–formatted emotional content, not emotional arousal per se

**Experiment 3: Norm Erosion (E3)**
- **Design:** Between-subjects, 3 conditions
  - Condition A: Exposure to incivil online deliberation (real social media threads with hostile exchanges)
  - Condition B: Exposure to civil online deliberation (same topics, respectful exchanges)
  - Condition C: No exposure control
- **Sample:** n = 450 (150 per condition)
- **Task:** Same deliberation task as E1/E2
- **Outcome:** DCI score + civility of participant's own discourse (coded independently)
- **Mechanism Test:** If Condition A < Condition B, exposure to incivil norms shifts perceived norms and degrades deliberation

**Qualitative Component:**
- Semi-structured interviews with n = 40 participants (drawn from all conditions, stratified by DCI performance)
- Focus: How participants experienced the deliberation task; what they perceived as barriers to high-quality deliberation; their typical social media deliberation experiences
- Purpose: Mechanism validation and ecological grounding; identifying unexpected pathways

### 3.2 Power Analysis

```
Primary outcome: Deliberative Capacity Index (DCI), continuous 0–100
Expected effect size: d = 0.35 (small-to-medium, based on Bail et al. 2018 effect sizes)
Alpha: 0.05 (two-tailed)
Power: 0.80
Required n per condition: 128

Adjusted for:
- Attention check failures: +15% → 147 per condition
- Attrition: +5% → 155 per condition
- Rounded to: 150 per condition

Total across 3 experiments: 1,500 participants
Plus qualitative subsample: 40 interview participants
Grand total: 1,540 participants
```

### 3.3 Pre-Registration Template (Filled)

```yaml
pre_registration:
  title: "Unraveling the Mechanisms: How Social Media Degrades Democratic 
          Deliberation"
  registration_platform: "AsPredicted"
  registration_date: "2025-03-15"
  registration_id: "XXXXX"
  
  hypotheses:
    H1: "Micro-interruptions mimicking social media notifications will reduce 
         deliberative quality (DCI) compared to both uninterrupted and 
         neutrally-interrupted conditions (E1)."
    H2: "Exposure to emotionally-arousing social media content will reduce 
         deliberative quality compared to both neutral social media and 
         emotionally-arousing non-social-media content (E2)."
    H3: "Exposure to incivil online discourse will reduce deliberative quality 
         and increase incivility in participants' own deliberation compared to 
         exposure to civil discourse (E3)."
    H4_mediation: "The three mechanisms (attention fragmentation, affective 
         priming, norm erosion) will mediate the relationship between social 
         media exposure and deliberative quality, with affective priming as 
         the strongest mediator."
  
  design:
    type: "Three-experiment sequence + qualitative interviews"
    E1:
      design: "Between-subjects, 3 conditions"
      n: 450
      iv: "Interruption type (social media / none / neutral)"
      dv: "DCI score"
    E2:
      design: "Between-subjects, 4 conditions"
      n: 600
      iv: "Content valence × format"
      dv: "DCI score + self-reported affect"
    E3:
      design: "Between-subjects, 3 conditions"
      n: 450
      iv: "Discourse norm exposure (incivil / civil / control)"
      dv: "DCI score + participant civility"
    qualitative:
      n: 40
      method: "Semi-structured interviews"
      analysis: "Thematic analysis (Braun & Clarke, 2006)"
  
  exclusion_criteria:
    - "Failed attention checks (2+ of 3)"
    - "Completion time < 50% of median (rushing)"
    - "Duplicate IP addresses"
    - "Self-reported non-serious participation"
  
  analysis_plan:
    primary: "One-way ANOVA with planned contrasts for each experiment"
    mediation: "Structural equation modeling (lavaan package in R)"
    multiple_comparison: "Bonferroni correction within each experiment"
    effect_size: "Cohen's d with 95% CI"
    qualitative: "Thematic analysis with dual coding; inter-rater reliability κ ≥ 0.80"
  
  data_availability: "All data, code, and materials will be deposited at 
    Harvard Dataverse upon publication. Qualitative transcripts will be 
    de-identified and shared with participant consent."
```

---

## Step 4: DATA

### 4.1 Example Results Paragraph

> **Experiment 1: Attention Fragmentation.** Participants in the social media interruption condition (M = 54.2, SD = 14.3) scored significantly lower on the Deliberative Capacity Index than participants in the uninterrupted condition (M = 63.7, SD = 12.1), with a medium effect size (d = 0.72, 95% CI: [0.49, 0.95], p < 0.001). Critically, the neutral interruption condition (M = 59.8, SD = 13.0) fell between the two, and the planned contrast comparing social media vs. neutral interruptions was significant (d = 0.40, 95% CI: [0.17, 0.63], p = 0.001), indicating that the quality of interruptions — not merely their frequency — degrades deliberation. Decomposing the DCI subscales, the attention fragmentation effect was largest for argument complexity (d = 0.81) and evidence citation (d = 0.68), and smallest for willingness to revise (d = 0.22), suggesting that interruptions primarily disrupt the construction of complex arguments rather than openness to perspective change.

### 4.2 Mediation Analysis Results

> **Mechanism Decomposition.** Across the three experiments, the combined mediation model explained 67% of the total effect of social media exposure on deliberative quality (pseudo-R² = 0.67). Affective priming emerged as the dominant mediator (indirect effect: β = 0.31, 95% CI: [0.24, 0.38], proportion mediated: 46%), followed by attention fragmentation (indirect effect: β = 0.18, 95% CI: [0.12, 0.24], proportion mediated: 27%) and norm erosion (indirect effect: β = 0.13, 95% CI: [0.07, 0.19], proportion mediated: 19%). The remaining 8% of the total effect was unexplained by the three measured mechanisms, suggesting additional pathways (e.g., information overload, social identity activation) that warrant investigation. The dominance of affective priming was robust to alternative model specifications (sobel test p < 0.001; bootstrapped CI with 10,000 iterations).

### 4.3 Example Figure Description

**Figure 2: Three-Mechanism Mediation Model**

```
[Path diagram with three parallel mediators]

Social Media Exposure ──► Affective Priming ──► Deliberative Quality
        (β = 0.53)              (β = -0.58)           (β = -0.67)
           │                          │
           │    Indirect effect:      │
           │    β = 0.31 (46%)        │
           │                          │
           ├──► Attention Fragmentation ──►
           │    (β = 0.41)    (β = -0.44)
           │    Indirect: β = 0.18 (27%)
           │
           └──► Norm Erosion ──────────►
                (β = 0.37)    (β = -0.35)
                Indirect: β = 0.13 (19%)

All paths significant at p < 0.001.
Direct effect (residual): β = -0.05, p = 0.23 (ns)
Total effect: β = -0.67, p < 0.001
Proportion mediated: 92% of total effect

Model fit: χ²(3) = 4.2, p = 0.24; CFI = 0.99; 
RMSEA = 0.03; SRMR = 0.02
```

**Figure 3: DCI Scores Across Experiments and Conditions**

```
[Three-panel bar chart]

Panel (a) — E1 (Attention Fragmentation):
  No interruption: 63.7 (reference)
  Neutral interruption: 59.8 (d = 0.40*)
  Social media interruption: 54.2 (d = 0.72***)

Panel (b) — E2 (Affective Priming):
  No exposure control: 66.1 (reference)
  Emotional non-social: 61.3 (d = 0.38*)
  Neutral social media: 59.7 (d = 0.52**)
  Emotional social media: 48.2 (d = 1.21***)

Panel (c) — E3 (Norm Erosion):
  No exposure control: 65.4 (reference)
  Civil discourse: 64.8 (d = 0.05, ns)
  Incivil discourse: 53.1 (d = 0.87***)

Error bars = 95% CI. * p < 0.05, ** p < 0.01, *** p < 0.001
Note the especially large effect in E2 Condition D (emotional social 
media), consistent with the mediation finding that affective priming 
is the dominant mechanism.
```

---

## Step 5: WRITING

### 5.1 Abstract (CRES Framework)

> **[Context]** Social media platforms are increasingly the primary venue for political discourse in democracies worldwide, yet growing evidence suggests that these platforms may systematically degrade the quality of democratic deliberation — the reasoned exchange of arguments, evidence, and perspectives that underpins legitimate collective decision-making. **[Gap]** Despite extensive documentation of correlations between social media use and indicators of poor deliberation, no study has experimentally isolated the causal mechanisms through which social media exposure degrades deliberative quality, leaving the field unable to design targeted interventions or evaluate regulatory proposals. **[Purpose]** We identify and experimentally test three candidate mechanisms — attention fragmentation, affective priming, and norm erosion — in three pre-registered experiments (total N = 1,500) supplemented by qualitative interviews (n = 40). **[Method]** In Experiment 1, participants deliberated with or without social media–style micro-interruptions; in Experiment 2, they were exposed to emotionally-arousing versus neutral social media feeds before deliberation; in Experiment 3, they observed incivil versus civil online discourse before deliberating. Deliberative quality was measured using the novel Deliberative Capacity Index (DCI). **[Results]** All three mechanisms significantly reduced deliberative quality, with affective priming as the dominant pathway (proportion mediated: 46%), followed by attention fragmentation (27%) and norm erosion (19%); the combined model explained 67% of the total effect of social media exposure on deliberative quality. **[Contribution]** This is the first experimental decomposition of the causal mechanisms linking social media to deliberative degradation, providing a mechanistic framework that bridges deliberative democratic theory and media effects research. **[Implication]** The dominance of affective priming as a mechanism suggests that platform design interventions targeting emotional amplification (e.g., affect labeling, cooling-off periods) may be more effective for protecting deliberative quality than approaches focused solely on content moderation or echo chamber reduction.

### 5.2 Introduction (Hourglass Structure)

**[Wide — Broad Context]**

Democratic governance depends on the quality of public deliberation — the capacity of citizens to engage with arguments, weigh evidence, consider opposing perspectives, and revise their views in light of new information (Habermas, 1984; Gutmann & Thompson, 2004). This deliberative ideal, while never fully realized, has served as a normative benchmark for evaluating the health of democratic discourse and has informed institutional designs from citizen assemblies to deliberative polls (Fishkin, 2018). The quality of public deliberation is not merely an academic concern: it shapes policy outcomes, legitimacy perceptions, and citizens' willingness to accept collective decisions with which they disagree (Mansbridge et al., 2012).

**[Narrowing — Specific Progress]**

The rise of social media has fundamentally transformed the infrastructure of public discourse. Platforms like Twitter/X, Facebook, TikTok, and YouTube have become the primary venues through which citizens encounter political information, form opinions, and engage with opposing viewpoints — with over 60% of adults in advanced democracies reporting that they regularly encounter political content on social media (Newman et al., 2024). This transformation has generated a substantial body of research documenting associations between social media use and indicators of poor deliberation: increased affective polarization (Iyengar et al., 2019), the spread of misinformation (Vosoughi et al., 2018), the formation of ideological echo chambers (Bail et al., 2018), and declining trust in democratic institutions (Fukuyama, 2022).

**[Narrow — The Gap]**

Yet this literature suffers from a fundamental causal identification problem. The vast majority of studies document *that* social media is associated with deliberative degradation but cannot identify *through which mechanisms* this degradation occurs. Three candidate mechanisms emerge from the theoretical literature — attention fragmentation, in which micro-interruptions and rapid context-switching disrupt the sustained attention required for complex argument evaluation (Carr, 2010; Wu, 2016); affective priming, in which algorithmic prioritization of emotionally arousing content primes affective rather than deliberative processing (Brady et al., 2017; Vosoughi et al., 2018); and norm erosion, in which exposure to uncivil online discourse shifts perceived norms of acceptable deliberative behavior (Cialdini et al., 1990; Anderson et al., 2014). Each mechanism implies a fundamentally different intervention strategy, yet no study has experimentally isolated their independent contributions to deliberative degradation.

**[Narrowest — This Paper]**

We report three pre-registered experiments (total N = 1,500) that decompose the causal mechanisms through which social media degrades democratic deliberation. Our results identify affective priming as the dominant pathway, accounting for 46% of the total effect, with attention fragmentation (27%) and norm erosion (19%) as complementary mechanisms. These findings provide the first mechanistic evidence base for platform governance, suggesting that interventions targeting emotional amplification — rather than content removal or diversity of exposure — may be most effective for protecting deliberative quality.

---

## Step 6: QUALITY

### 6.1 Five-Reviewer Panel Simulation

**Reviewer 1 — The Causal Identification Expert (Methodology Focus)**

> **Verdict:** WEAK ACCEPT (6/10)
>
> **Strengths:** The three-experiment design is the strongest approach to mechanism isolation available. The planned contrasts within each experiment are well-specified. Pre-registration is commendable.
>
> **Concerns:**
> 1. **Ecological validity:** The deliberation task (reading a policy brief + written deliberation with a confederate) is far removed from naturalistic social media deliberation. Participants know they are in an experiment. The social desirability bias on a topic like "deliberative quality" is enormous. How do you know the lab effect generalizes to the platform?
> 2. **Confederate standardization:** The confederate's arguments must be perfectly standardized across conditions. Any variation in confederate behavior introduces noise. Was the confederate scripted? What about interaction effects (some participants may push back, changing the confederate's natural response pattern)?
> 3. **Mediation assumptions:** The mediation analysis assumes no unmeasured confounders between the mediators and the outcome. Given that all three mechanisms were measured in separate experiments, the combined mediation model is essentially cross-experimental, which is problematic. The authors should acknowledge this limitation explicitly.
> 4. **Multiple hypothesis testing:** With 3 experiments, 4 conditions each, planned contrasts, subscale decompositions, and a mediation model, the effective number of tests is very large. The Bonferroni correction within each experiment may not be sufficient.
>
> **Required Revisions:** (a) Address ecological validity with a field study or natural experiment as robustness; (b) Describe confederate protocol in detail; (c) Acknowledge cross-experimental mediation limitation; (d) Consider FDR correction across experiments.

**Reviewer 2 — The Deliberative Democracy Theorist (Theory Focus)**

> **Verdict:** ACCEPT (8/10)
>
> **Strengths:** The paper makes a genuine theoretical contribution by formalizing the three-mechanism model and testing it empirically. The bridge between deliberative theory (Habermas, Gutmann & Thompson) and media effects is exactly what the field needs. The DCI measure is a welcome operationalization of deliberative ideals.
>
> **Concerns:**
> 1. The paper defines deliberative quality primarily in individual cognitive terms (argument complexity, evidence citation). But deliberative democracy is inherently *inter*-subjective — it requires mutual respect, listening, and reason-giving *to others*. The DCI may be capturing individual reasoning quality rather than deliberative quality per se.
> 2. The paper engages primarily with the empirical social science literature. It should more deeply engage with the normative deliberative theory literature (e.g., Mansbridge's "systemic deliberation" framework, Young's "inclusive communication") to justify its operationalization.
> 3. The dominance of affective priming is interesting but should be contextualized: deliberative theory has long recognized the role of emotion in deliberation (Marcus, 2002; Hall, 2005). Not all emotional arousal degrades deliberation — moral emotions like empathy can enhance it.
>
> **Suggested Improvements:** (a) Add inter-subjective DCI subscales (mutual responsiveness, reason-giving orientation); (b) Deeper engagement with normative theory; (c) Nuance the affective priming finding with positive emotion discussion.

**Reviewer 3 — The Survey/Experimental Methods Specialist (Measurement Focus)**

> **Verdict:** ACCEPT (7/10)
>
> **Strengths:** The DCI measure fills a real gap. The power analysis is adequate. The attention checks and exclusion criteria are standard.
>
> **Concerns:**
> 1. **DCI validation:** The DCI is described as combining four subscales (argument complexity, perspective-taking, evidence citation, willingness to revise), but I could not find evidence of its validation. Was it validated in a pilot study? What is its inter-rater reliability? Its convergent validity with existing measures (Steenbergen et al.'s DQI)?
> 2. **MTurk/Prolific sample:** Online convenience samples skew young, liberal, and digitally native. These participants may be *less* susceptible to social media effects precisely because they are more experienced with the medium. The estimated effects may be lower bounds.
> 3. **Self-reported affect in E2:** Self-reported affect is subject to demand characteristics. Consider using an implicit measure (e.g., affective priming task, facial EMG for subset) to triangulate.
> 4. **Multiple experiments, same pool:** If participants across experiments are drawn from the same online pool, there is a risk of cross-contamination (participants discussing the study on forums).
>
> **Required Revisions:** (a) Provide full DCI validation data; (b) Discuss sample limitations; (c) Consider implicit affect measure; (d) Describe anti-contamination procedures.

**Reviewer 4 — The Political Communication Scholar (Substantive Focus)**

> **Verdict:** STRONG ACCEPT (9/10)
>
> **Strengths:** This paper is the most important contribution to the social media and democracy literature since Bail et al. (2018). The mechanism decomposition finally moves the field beyond "is social media bad?" to "through which pathways is it bad, and what can we do about it?" The affective priming finding is particularly important and consistent with Brady et al.'s (2017) work on moral contagion.
>
> **Concerns:**
> 1. The policy implications section could be stronger. "Affect labeling" and "cooling-off periods" are mentioned, but the paper should more directly engage with specific platform design features (e.g., Twitter/X's community notes, Meta's emotional health prompts, YouTube's autoplay disable) and evaluate them through the mechanism lens.
> 2. The cross-cultural generalizability is a significant limitation. The entire sample is US-based. The authors should explicitly flag this and ideally propose a cross-cultural replication as a next step.
>
> **Suggested Improvements:** (a) Extend policy implications with specific feature evaluation; (b) Add a "Generalizability Limitations" subsection.

**Reviewer 5 — The External Validity Skeptic (Generalizability Focus)**

> **Verdict:** WEAK REJECT (4/10)
>
> **Strengths:** The experimental design is internally valid. The theoretical framework is compelling.
>
> **Concerns:**
> 1. **Fundamental external validity problem:** Lab experiments with MTurk participants deliberating about immigration with a confederate have unknown — and I would argue very low — generalizability to real social media deliberation. Real deliberation is public, identity-laden, extended over time, embedded in social networks, and consequential. None of these features are captured in the lab.
> 2. **No field validation:** Without at least one natural experiment or field study corroborating the lab findings, the mechanism claims are unsupported outside the lab.
> 3. **Political ideology:** The paper does not appear to test for ideological asymmetry. Do these mechanisms operate equally for liberals and conservatives? The literature on motivated reasoning suggests they may not.
> 4. **Topic dependency:** Immigration is a high-salience, high-affect topic. Would the same mechanisms hold for low-salience policy issues?
>
> **Required Revisions:** (a) Add a field validation study (even a modest one); (b) Test ideological asymmetry; (c) Test topic dependency; (d) Fundamentally reframe claims about generalizability.

### 6.2 Synthesis Report

| Criterion | R1 (Causal) | R2 (Theory) | R3 (Methods) | R4 (Comm) | R5 (Ext. Valid.) | Consensus |
|---|---|---|---|---|---|---|
| Novelty | 8 | 9 | 8 | 10 | 8 | **8.6** |
| Theoretical Contribution | 7 | 9 | 7 | 8 | 7 | **7.6** |
| Methodological Rigor | 8 | 7 | 7 | 8 | 6 | **7.2** |
| External Validity | 4 | 6 | 5 | 6 | 2 | **4.6** |
| Clarity | 8 | 8 | 7 | 9 | 7 | **7.8** |
| Policy Relevance | 7 | 7 | 7 | 9 | 5 | **7.0** |
| **Overall** | **6** | **8** | **7** | **9** | **4** | **6.8** |

**Critical Weakness: External Validity (4.6/10 consensus)**

**Action Items Before Submission:**
1. **CRITICAL:** Address external validity — at minimum, add a discussion section explicitly acknowledging the lab-to-field gap and proposing a field validation study as immediate next step; ideally, add a supplementary field study using observational social media data with matching/instrumental variables (addresses R1.1, R5.1, R5.2)
2. **CRITICAL:** Provide full DCI validation data — pilot study, inter-rater reliability, convergent validity with DQI (addresses R3.1)
3. **IMPORTANT:** Test ideological asymmetry as a moderator (addresses R5.3)
4. **IMPORTANT:** Acknowledge cross-experimental mediation limitation (addresses R1.3)
5. **RECOMMENDED:** Add inter-subjective DCI subscales (addresses R2.1)
6. **RECOMMENDED:** Extend policy implications with specific platform features (addresses R4.1)
7. **RECOMMENDED:** Add generalizability limitations subsection (addresses R4.2, R5)

**Revised Predicted Score: 7.5–8.2** (after addressing critical items, especially external validity)

---

## Step 7: JOURNAL

### 7.1 Venue Selection

| Rank | Venue | Impact Factor | Accept Rate | Fit Score | Rationale |
|---|---|---|---|---|---|
| 1 | **American Political Science Review (APSR)** | 8.0 | ~5% | **9.2/10** | Top political science journal; strong fit for deliberative democracy + causal methods; the mechanism decomposition is exactly the kind of contribution APSR values |
| 2 | **Nature Human Behaviour** | 21.4 | ~8% | **9.0/10** | Interdisciplinary audience; high visibility; values experimental + mechanistic contributions; the affective priming finding has broad appeal |
| 3 | **American Journal of Political Science (AJPS)** | 5.6 | ~4% | **8.8/10** | AJPS values rigorous causal identification; the three-experiment design is well-suited; slightly more methods-oriented audience |
| 4 | **Journal of Politics** | 3.2 | ~8% | **8.0/10** | Strong fit but slightly lower impact than APSR/AJPS |
| 5 | **Political Communication** | 6.9 | ~12% | **7.8/10** | Specialist journal; perfect topical fit but the theoretical ambition may exceed the venue's typical scope |

**Recommended Strategy:** Submit to **APSR** as first choice, leveraging the causal mechanism contribution. If desk-rejected, **Nature Human Behaviour** offers broader interdisciplinary visibility. **AJPS** is an excellent backup if the causal identification is the strongest selling point.

### 7.2 Cover Letter Excerpt

> Dear Editor,
>
> We submit "Unraveling the Mechanisms: How Social Media Degrades Democratic Deliberation" for consideration at the American Political Science Review.
>
> Despite a decade of research documenting correlations between social media use and deliberative degradation, the field has been unable to answer the most policy-relevant question: *through which mechanisms* does social media degrade deliberation? Without mechanistic knowledge, interventions are designed in the dark — we cannot tell whether content moderation, algorithmic reform, or norm-nudging is the appropriate remedy.
>
> This paper provides the first experimental decomposition of three candidate mechanisms — attention fragmentation, affective priming, and norm erosion — in three pre-registered experiments (N = 1,500) with qualitative interviews (n = 40). We find that affective priming is the dominant pathway (proportion mediated: 46%), with significant but smaller contributions from attention fragmentation (27%) and norm erosion (19%). These findings directly inform platform governance: interventions targeting emotional amplification may be more effective than content moderation or echo chamber reduction.
>
> We believe this work meets the APSR standard for both theoretical innovation and methodological rigor, and we are committed to full transparency through pre-registration, open data, and open materials.
>
> Sincerely,
> [Authors]

---

## Summary

This example demonstrates how the CRES framework transforms the research process for a social science research paper:

| Step | Key Output | Time Investment |
|---|---|---|
| IDEATION | Novel causal mechanism question with 8.9/10 score; three-mechanism model | 3–5 days |
| LITERATURE | 1,124-paper corpus mapped; three schools identified; mechanistic gap isolated | 5–7 days |
| METHODOLOGY | Three-experiment design + qualitative component; DCI measure; power analysis | 4–6 days |
| DATA | Results paragraphs with effect sizes; mediation model; figure protocols | 2–3 days |
| WRITING | CRES abstract; hourglass introduction connecting deliberative theory to media effects | 3–4 days |
| QUALITY | 5-reviewer panel; external validity weakness identified (4.6/10); action items specified | 2–3 days |
| JOURNAL | APSR as first target; Nature Human Behaviour as interdisciplinary alternative | 1 day |

**Total estimated time:** 20–29 days from idea to submission-ready manuscript.
