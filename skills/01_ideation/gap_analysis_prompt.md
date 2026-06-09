# Gap Analysis Prompt

## Systematic Procedure for Identifying Research Gaps

### Purpose
This prompt guides a rigorous, systematic identification of research gaps in any domain. It moves beyond superficial "nobody has studied X" claims to provide validated, prioritized, and actionable gap statements that form the foundation for novel research contributions.

---

## STEP 1: PREPARATORY SCAN

Before identifying gaps, establish the knowledge boundary of the field:

1. **Map the literature topology:** Identify the 10–15 most cited review papers in the domain from the past 5 years
2. **Extract explicit gap statements:** Catalog every instance where review authors explicitly state "future research should..." or "a gap remains in..."
3. **Inventory implicit gaps:** Note topics that reviews omit entirely — absence of discussion can signal an unrecognized gap
4. **Check recent empirical work:** Scan the last 2 years of empirical publications to determine whether explicitly stated gaps have been addressed
5. **Document the knowledge frontier:** Create a written summary of what is known, what is debated, and what is unknown

**Output:** A knowledge frontier document organized as:
- **Established findings** (consensus exists, replication confirmed)
- **Contested findings** (conflicting evidence, active debate)
- **Unknown territory** (no empirical evidence, speculation only)

---

## STEP 2: GAP TAXONOMY — THE SEVEN TYPES

### Type 1: Knowledge Gap
**Definition:** A phenomenon or relationship that has not been empirically investigated at all. The field lacks basic descriptive or explanatory data about the topic.

**Diagnostic Questions:**
- Is there any empirical study that directly examines this phenomenon?
- Do we have even preliminary data about the existence, prevalence, or nature of this phenomenon?
- Is the absence of knowledge due to the topic being overlooked, or is it genuinely unstudiable?

**Examples by Field:**
- *Psychology:* No studies examine how chronic sleep restriction affects moral decision-making in healthcare professionals
- *Computer Science:* No empirical data on the failure modes of large language models when processing code with adversarial comments
- *Education:* No research on how asynchronous peer feedback affects self-regulated learning in STEM laboratory courses
- *Public Health:* No prevalence data on zoonotic disease spillover in urban peri-domestic rodent populations in Sub-Saharan Africa

**Red Flag:** Knowledge gaps are often claimed where the real issue is that the researcher has not searched thoroughly enough. Always verify through systematic search before claiming a knowledge gap.

---

### Type 2: Method Gap
**Definition:** Existing methods for studying a phenomenon are inadequate, biased, limited in scope, or entirely absent, making current findings unreliable or incomplete.

**Diagnostic Questions:**
- Do current methods capture the construct with adequate validity?
- Are existing measures systematically biased or limited in application?
- Could a new methodological approach reveal findings invisible to current methods?
- Is there a disconnect between the complexity of the phenomenon and the simplicity of tools used to study it?

**Examples by Field:**
- *Psychology:* Self-report measures of implicit bias are confounded with social desirability; no unobtrusive behavioral measure exists for clinical settings
- *Computer Science:* Existing code complexity metrics fail to capture cognitive load in functional programming paradigms
- *Education:* No validated instrument measures scientific reasoning in authentic laboratory environments (vs. paper-and-pencil tests)
- *Public Health:* Contact tracing methods for respiratory viruses rely on self-reported contacts; no digital proximity method has been validated against biological outcomes

---

### Type 3: Theory Gap
**Definition:** Empirical findings exist but lack adequate theoretical explanation. Data are observed without a coherent framework that explains why or how the phenomenon occurs.

**Diagnostic Questions:**
- Is there a theory that predicts this finding, or is it merely described post hoc?
- Do existing theories make conflicting predictions about this phenomenon?
- Has the phenomenon been observed but never integrated into a theoretical model?
- Would a new or extended theory generate novel, testable predictions?

**Examples by Field:**
- *Psychology:* The "testing effect" (retrieval practice enhances learning) is well-documented, but no unified theory explains why it works better for some material types than others
- *Computer Science:* Empirical observations that certain neural network architectures generalize better exist, but theoretical understanding of why remains incomplete
- *Education:* Service learning improves civic engagement outcomes, but no theoretical model specifies the active ingredients or mechanisms
- *Public Health:* The "healthy worker effect" is well-documented but lacks a formal theoretical model that predicts its magnitude across occupations

---

### Type 4: Application Gap
**Definition:** Robust knowledge exists in research but has not been translated, adapted, or implemented in practical settings where it could create value.

**Diagnostic Questions:**
- Is there evidence that practitioners are aware of this research finding?
- Are there known barriers to applying this knowledge in practice?
- Has anyone attempted implementation, and if so, what failed?
- Is the gap between knowledge and application due to the research, the practitioners, or the system?

**Examples by Field:**
- *Psychology:* Cognitive behavioral therapy is effective for anxiety disorders, but fewer than 20% of primary care patients have access
- *Computer Science:* Differential privacy techniques are well-developed but rarely implemented in commercial data systems
- *Education:* Spaced repetition is among the most robust findings in learning science, yet most curricula use massed practice schedules
- *Public Health:* Hand hygiene protocols are evidence-based but compliance in hospitals remains below 50% globally

---

### Type 5: Replication Gap
**Definition:** Findings have been reported in the literature but lack independent replication, especially across different populations, contexts, or with improved methods.

**Diagnostic Questions:**
- Has this finding been independently replicated by a different research group?
- Has it been replicated with a larger sample than the original study?
- Has it been replicated in a different cultural, demographic, or geographic context?
- Were the original methods sufficiently transparent to enable replication?

**Examples by Field:**
- *Psychology:* Many classic social priming effects have never been independently replicated with adequately powered samples
- *Computer Science:* Benchmark performance claims for ML models are rarely replicated on independent hardware with independent code
- *Education:* The effect of growth mindset interventions has been replicated with mixed results; the boundary conditions remain unclear
- *Public Health:* Epidemiological findings from one country are often assumed to generalize without replication in different healthcare systems

---

### Type 6: Population Gap
**Definition:** Findings have been established in one or a few populations but have not been investigated in other relevant populations, limiting generalizability and creating equity concerns.

**Diagnostic Questions:**
- Who was the original sample, and who has been excluded?
- Are there theoretical reasons to expect different effects in excluded populations?
- Does the exclusion of certain populations create a biased evidence base?
- Are there populations for whom the current evidence might cause harm if applied uncritically?

**Examples by Field:**
- *Psychology:* Most cognitive psychology findings are based on WEIRD (Western, Educated, Industrialized, Rich, Democratic) samples; cross-cultural replication is sparse
- *Computer Science:* Facial recognition systems trained primarily on lighter-skinned populations show significantly higher error rates for darker-skinned individuals
- *Education:* Reading intervention research is dominated by English-language studies; efficacy in transparent orthographies (e.g., Spanish, Finnish) is under-explored
- *Public Health:* Clinical trial enrollment underrepresents elderly, pregnant, and minority populations, creating evidence gaps for these groups

---

### Type 7: Mechanistic Gap
**Definition:** A correlation or association between variables is established, but the causal mechanism — the process through which X leads to Y — remains unknown.

**Diagnostic Questions:**
- Is the relationship between X and Y merely correlational, or has causality been established?
- If causality is established, have mediators been tested?
- Are there multiple plausible mechanisms, and have they been distinguished empirically?
- Would understanding the mechanism enable targeted interventions?

**Examples by Field:**
- *Psychology:* Socioeconomic status predicts academic achievement, but the specific mechanisms (stress, resources, parenting, school quality, health) have not been disentangled
- *Computer Science:* Larger language models show emergent capabilities, but the mechanism by which scale produces qualitative shifts is not understood
- *Education:* Montessori education shows positive outcomes, but whether the mechanism is the materials, the teacher role, the mixed-age grouping, or the prepared environment is unknown
- *Public Health:* Air pollution is associated with cognitive decline, but whether the mechanism is inflammatory, vascular, or direct neurotoxicity is undetermined

---

## STEP 3: GAP SEVERITY ASSESSMENT

### Framework

| Severity Level | Definition | Criteria | Example |
|---------------|-----------|----------|---------|
| **Critical** | The field's foundational claims rest on this gap | Absence of this knowledge could invalidate major theories or practices | No replication of a finding that underpins a widely used clinical intervention |
| **Major** | A significant limitation in the field's understanding | Multiple research programs or practical applications are constrained | No valid measure exists for a construct central to the field's dominant theory |
| **Moderate** | A meaningful but not foundational limitation | Closing this gap would improve precision or generalizability | A finding established in two countries has not been tested in other cultural contexts |
| **Minor** | A narrow or peripheral limitation | Closing this gap would add nuance but not change the field's trajectory | A specific moderator has not been tested for an established effect |

### Severity Scoring Protocol
Rate each identified gap on four sub-dimensions (1–5 each):

1. **Foundational dependence:** How much does the field's core knowledge depend on this gap being filled?
2. **Practical consequence:** What are the real-world implications of this gap remaining unfilled?
3. **Theoretical bottleneck:** Does this gap prevent theoretical progress in other areas?
4. **Temporal urgency:** Is the gap becoming more severe over time as the field evolves?

**Severity Score** = Mean of the four sub-dimensions, mapped to:
- 4.0–5.0 → Critical
- 3.0–3.9 → Major
- 2.0–2.9 → Moderate
- 1.0–1.9 → Minor

---

## STEP 4: GAP VALIDATION CHECKLIST

**Critical step:** Before committing to a gap, verify it is real and not manufactured by incomplete searching or misinterpretation.

### Is the Gap Real or Manufactured?

- [ ] **Literature completeness:** Have I searched at least 5 databases with systematic keyword strategies? (If not, the "gap" may simply be an undiscovered study)
- [ ] **Search term adequacy:** Have I used synonyms, related terms, and discipline-specific vocabulary? (The same phenomenon may be studied under different names)
- [ ] **Language bias:** Am I assuming a gap exists because I only searched in English? (Relevant work may exist in other languages)
- [ ] **Publication bias:** Could the gap exist because null results were not published? (Check registries, preprints, dissertations)
- [ ] **Recency check:** Have I checked preprint servers and conference proceedings from the last 12 months? (A study addressing the gap may be in progress)
- [ ] **Implicit coverage:** Even if no study directly addresses the gap, have related studies incidentally collected relevant data? (Secondary analysis may have already addressed the gap)
- [ ] **Gray literature:** Have I checked technical reports, white papers, and institutional publications? (Applied fields often publish outside journals)
- [ ] **Overclaiming bias:** Am I inflating the gap's significance to make my research seem more important? (Seek disconfirming evidence actively)
- [ ] **Straw-man bias:** Am I mischaracterizing existing research to create a gap? (Accurately represent what prior work has actually found)
- [ ] **Feasibility check:** Is the gap genuinely addressable, or is it a philosophical question disguised as an empirical gap? (Distinguish empirical from conceptual gaps)

### Validation Decision Rules
- Passes 9–10 checks → Gap is validated; proceed with confidence
- Passes 7–8 checks → Gap is likely real but needs targeted additional search
- Passes 5–6 checks → Gap is uncertain; conduct expanded search before claiming
- Passes <5 checks → Gap is likely manufactured; do not build research on this foundation

---

## STEP 5: GAP-TO-QUESTION TRANSFORMATION TEMPLATES

### Template 1: Knowledge Gap → Exploratory Question
```
"What is the nature of [PHENOMENON] in [POPULATION/CONTEXT], and how does it
manifest under [CONDITIONS]?"
```

### Template 2: Method Gap → Methodological Question
```
"How can [CONSTRUCT] be measured/studied more validly and reliably than
existing methods, and what new insights does the improved method reveal?"
```

### Template 3: Theory Gap → Explanatory Question
```
"Why does [OBSERVED RELATIONSHIP] occur, and what theoretical mechanism
accounts for [PATTERN/BOUNDARY CONDITION]?"
```

### Template 4: Application Gap → Translation Question
```
"How can [ESTABLISHED FINDING] be effectively implemented in [PRACTICAL SETTING],
and what barriers and facilitators moderate implementation success?"
```

### Template 5: Replication Gap → Verification Question
```
"Does [FINDING] replicate in [NEW POPULATION/CONTEXT] using [IMPROVED METHOD],
and what are the boundary conditions of the effect?"
```

### Template 6: Population Gap → Generalizability Question
```
"Does [ESTABLISHED EFFECT] generalize to [UNDERSTUDIED POPULATION], and
do [MODERATORS] alter the magnitude or direction of the effect?"
```

### Template 7: Mechanistic Gap → Causal Question
```
"Through what mechanism does [CAUSE] lead to [EFFECT], and does [MEDIATOR]
account for the relationship when [CONFOUND] is controlled?"
```

---

## STEP 6: CROSS-DOMAIN GAP DETECTION HEURISTICS

### Heuristic 1: Method Transfer Gap
Look for methods that are standard in one field but absent in another. Example: Genomic analysis methods (bioinformatics) applied to educational data (learning analytics).

### Heuristic 2: Construct Isomorph Gap
Identify constructs that are studied under different names in different fields but describe the same phenomenon. Example: "Flow" in psychology ≈ "Absorption" in consumer behavior ≈ "Immersion" in HCI.

### Heuristic 3: Level-of-Analysis Gap
Identify phenomena studied at one level (e.g., individual) that could be studied at another (e.g., group, organizational, societal). Example: Resilience is well-studied in individuals but under-studied at the team level.

### Heuristic 4: Temporal Gap
Identify phenomena studied cross-sectionally that need longitudinal investigation, or vice versa. Example: Most studies of technology adoption are cross-sectional; longitudinal trajectories are unknown.

### Heuristic 5: Negative Space Heuristic
Map what a field actively discusses and then identify what it systematically avoids. Systematic avoidance often signals an implicit assumption or an uncomfortable territory that could yield valuable gaps.

### Heuristic 6: Paradigm Clash Gap
When two fields study the same phenomenon with incompatible assumptions, the gap lies in reconciling or testing between paradigms. Example: Economics assumes rational actors; psychology demonstrates systematic irrationality — behavioral economics emerged from this gap.

### Heuristic 7: Granularity Gap
Identify findings established at a coarse level that have not been decomposed into finer-grained mechanisms or moderators. Example: "Exercise improves cognition" is established at a coarse level; the specific exercise types, intensities, durations, and cognitive domains that matter are not differentiated.

---

## STEP 7: EXAMPLES OF WELL-IDENTIFIED GAPS FROM VARIOUS FIELDS

### Example 1: Medicine — Mechanistic Gap (Well-identified)
**Gap Statement:** "While metformin is the first-line treatment for type 2 diabetes and observational studies suggest it reduces cancer incidence, the mechanism by which metformin may exert anti-cancer effects is unknown. Understanding this mechanism is critical because it would determine whether metformin's anti-cancer effect is direct (via AMPK activation in tumor cells) or indirect (via systemic insulin reduction), which has fundamentally different implications for repurposing metformin as a cancer preventive agent."
**Why it's well-identified:** Specifies the gap precisely, identifies competing mechanisms, explains why closing the gap matters for practice.

### Example 2: Education — Population Gap (Well-identified)
**Gap Statement:** "Reading intervention research has established the efficacy of explicit phonics instruction for English-speaking children with dyslexia, but these findings cannot be generalized to children learning to read in transparent orthographies such as Spanish or Finnish, where the grapheme-phoneme correspondence is near-perfect. The theoretical models and instructional approaches developed for opaque orthographies may be unnecessary or even counterproductive in transparent orthography contexts, yet no large-scale RCT has tested this."
**Why it's well-identified:** Explains why generalization is theoretically doubtful (not just untested), identifies the specific boundary condition, and articulates the practical risk of inappropriate generalization.

### Example 3: Computer Science — Method Gap (Well-identified)
**Gap Statement:** "Current evaluation of NLP models relies on benchmark performance on static test sets, which is known to be vulnerable to dataset contamination and annotation artifacts. No evaluation framework exists that dynamically generates novel test items that are guaranteed to be absent from training data while controlling for difficulty and construct validity. This method gap means that claims of model generalization are fundamentally unverifiable with current tools."
**Why it's well-identified:** Identifies the specific inadequacy of current methods, explains why the inadequacy matters (claims are unverifiable), and specifies what a solution would require.

---

## FINAL OUTPUT FORMAT

Present the gap analysis as:

```markdown
# Gap Analysis Report

## Knowledge Frontier Summary
[Established / Contested / Unknown]

## Identified Gaps

### Gap 1: [TYPE] — [BRIEF TITLE]
- **Description:** [Full gap statement]
- **Severity:** [Critical/Major/Moderate/Minor] (Score: X.X)
- **Validation Status:** [Passed X/10 checks]
- **Transformed Research Question:** [Question]
- **Key References:** [Authors who have noted this gap]

[Repeat for each gap]

## Gap Priority Ranking
[Ordered by severity, feasibility, and novelty combined]

## Cross-Domain Opportunities
[Gaps that could be addressed through cross-domain methods or theories]

## Recommended Next Steps
[Which gaps to pursue first and what further validation is needed]
```
