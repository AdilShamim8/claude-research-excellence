# Literature Command

## Skill Metadata
- **Skill Name:** Literature Command
- **Version:** 2.0.0
- **Purpose:** Master the research literature through systematic search, deep synthesis, and strategic citation — transforming scattered readings into a coherent intellectual foundation
- **Trigger:** User needs to conduct a literature review, synthesize findings across studies, write a related work section, or develop a citation strategy
- **Integration:** Receives gaps and questions from Ideation Engine (01), provides validated gap confirmation, feeds theoretical frameworks to Methodology Architect (03), and structures content for Writing Engine (06)

---

## ACTIVATE: LITERATURE

When the user invokes Literature Command, execute the following five-phase protocol. Each phase builds on the previous one. Do not proceed to the next phase until the current one produces output that meets the quality criteria.

---

### PHASE 1: LITERATURE ARCHITECTURE

**Objective:** Construct a comprehensive map of the intellectual landscape surrounding the research topic, revealing temporal patterns, intellectual lineages, and competing schools of thought.

#### 1.1 Temporal Mapping
- Identify the **Foundational Period** (earliest seminal works that established the domain)
- Identify the **Growth Period** (works that expanded the domain, including key replications and extensions)
- Identify the **Consolidation Period** (major reviews, meta-analyses, and theoretical syntheses)
- Identify the **Current Frontier** (works from the last 2–3 years that represent the cutting edge)
- For each period, list 5–10 anchor publications with their citation velocity (accelerating, stable, or decelerating)

**Output Format:**
```
FOUNDATIONAL (YYYY–YYYY): [Key works establishing the domain]
GROWTH (YYYY–YYYY): [Key works expanding the domain]
CONSOLIDATION (YYYY–YYYY): [Reviews, meta-analyses, syntheses]
CURRENT FRONTIER (YYYY–present): [Latest advances and emerging directions]
```

#### 1.2 Intellectual Genealogy
- Trace the lineage of ideas: which works cite which earlier works?
- Identify **Progenitor Works** — the 3–5 most-cited foundational papers that spawned research streams
- Map **Descendant Streams** — the major research traditions that descended from each progenitor
- Identify **Cross-Pollination Events** — moments when ideas from one stream were imported into another
- Flag **Orphan Ideas** — promising concepts from early work that were never followed up

**Output Format:**
```
PROGENITOR: [Author, Year] — [Core idea]
  ├─ STREAM A: [Description and key works]
  ├─ STREAM B: [Description and key works]
  └─ CROSS-POLLINATION: [How ideas migrated between streams]

ORPHAN IDEAS: [List with potential for revival]
```

#### 1.3 School Mapping
- Identify the **dominant paradigms** or "schools of thought" in the field
- For each school, document:
  - **Core assumptions:** What does this school take as given?
  - **Preferred methods:** What methodological approach does this school favor?
  - **Central constructs:** What are the key variables this school studies?
  - **Key proponents:** Who are the leading advocates?
  - **Critiques:** What are the most serious criticisms from other schools?
  - **Blind spots:** What does this school systematically overlook?

- Map the **inter-school relationships:**
  - Complementary (findings from different schools converge)
  - Competing (schools make contradictory predictions)
  - Orthogonal (schools study different aspects of the same phenomenon)
  - Superseding (one school has largely replaced another)

**Quality Gate:** Phase 1 must produce temporal maps, genealogies, and school maps covering at least 80% of the relevant literature. If significant gaps in coverage exist, expand the search strategy before proceeding.

---

### PHASE 2: DEEP SYNTHESIS ENGINE

**Objective:** Move beyond cataloging what has been studied to synthesizing what is known, what is contested, and what is missing.

#### 2.1 Consensus Mapping
Identify findings where the literature converges:

- **Strong Consensus:** Multiple independent replications with consistent results; meta-analytic evidence supports the finding; no credible challenge exists
- **Moderate Consensus:** Most studies agree, but some exceptions exist; the effect is established but boundary conditions are debated
- **Emerging Consensus:** A trend is apparent in recent studies, but insufficient replication has occurred to be confident

For each consensus finding, document:
- The finding (precise statement)
- Effect size and confidence interval (if meta-analytic data exists)
- Boundary conditions (where the finding does and does not hold)
- Methodological caveats (studies share a common limitation)

#### 2.2 Contradiction Mapping
Identify findings where the literature diverges:

- **Direct Contradiction:** Studies find opposite effects (e.g., X increases Y in some studies, decreases Y in others)
- **Magnitude Discrepancy:** Studies agree on direction but disagree on effect size by an order of magnitude
- **Null vs. Significant:** Some studies find an effect, others find none
- **Context Dependency:** Effects appear in some populations/settings but not others

For each contradiction, diagnose the likely cause:
1. **Methodological differences:** Different measures, designs, or analyses produce different results
2. **Population differences:** Effects are genuine but population-specific
3. **Statistical artifacts:** Small samples, p-hacking, or publication bias create apparent contradictions
4. **Theoretical inadequacy:** Neither side is correct; a more nuanced theory is needed
5. **Unexamined moderators:** A third variable explains when each result holds

#### 2.3 Methodological Audit
Systematically evaluate the methods used across the literature:

- **Design distribution:** What percentage of studies use experimental vs. correlational vs. qualitative designs?
- **Sample characteristics:** What populations have been studied? What populations are missing?
- **Measure quality:** Are validated instruments used, or are ad-hoc measures common?
- **Statistical rigor:** Are appropriate sample sizes achieved? Are assumptions checked? Are corrections for multiple comparisons applied?
- **Replication status:** How many findings have been independently replicated?
- **Open science practices:** How many studies are pre-registered? How many share data/code?

**Output:** A methodological scorecard for the literature, identifying systematic methodological weaknesses that affect the reliability of conclusions.

#### 2.4 Theoretical Void Detection
Identify areas where empirical data exists but theoretical integration is lacking:

- **Ungrounded findings:** Robust empirical results with no theoretical explanation
- **Untested theories:** Well-developed theories that have never been empirically tested
- **Theory-data misalignment:** Theories that predict one thing but data show another (and the discrepancy is ignored)
- **Parallel theories:** Multiple theories explain the same phenomenon but have never been directly compared

**Quality Gate:** Phase 2 must produce at least 3 consensus findings, 2 contradictions with diagnoses, a methodological scorecard, and 2 theoretical voids. If any category is empty, the literature search was insufficient.

---

### PHASE 3: RELATED WORK SYNTHESIS

**Objective:** Construct a compelling, synthesized related work section that positions the research within the intellectual landscape — NOT a study-by-study summary.

#### 3.1 Five-Paragraph Architecture

The related work section follows this structure:

**Paragraph 1: The Landscape**
Establish the broad intellectual context. What is the domain? Why does it matter? What are the major research streams? This paragraph orients the reader and establishes the scope.

**Paragraph 2: What We Know**
Synthesize the consensus findings. What is established? What can we confidently claim? Group findings thematically, not chronologically. Use synthesis verbs (see 3.3 below).

**Paragraph 3: What We Don't Know**
Identify the gaps. What is missing from the literature? What contradictions remain unresolved? What populations, contexts, or questions have been overlooked? This paragraph creates the intellectual need that your study fills.

**Paragraph 4: What You Do**
Position your study as the response to the gaps. How does your research address what is missing? What is new about your approach? This paragraph connects the gap to your contribution.

**Paragraph 5: Why It Matters**
Articulate the significance. What will the field gain from your study? How will findings advance theory, method, or practice? This paragraph motivates the reader to continue.

#### 3.2 Citation Integration Template

Citations should be woven into the argument, not listed. Use these patterns:

**Synthesis Pattern (preferred):**
```
[CONCEPTUAL CLAIM], as demonstrated across multiple studies examining
[PHENOMENON] (Author1, Year; Author2, Year; Author3, Year).
```

**Contrast Pattern:**
```
While [AUTHOR A, Year] found [FINDING A], [AUTHOR B, Year] demonstrated
[FINDING B], suggesting that [SYNTHESIS OF THE DISCREPANCY].
```

**Evolution Pattern:**
```
Early work established [FOUNDATIONAL FINDING] (Author1, Year), which was
later extended by [Author2, Year] to [EXTENSION], and most recently refined
by [Author3, Year] who showed [REFINEMENT].
```

**NEVER use the "laundry list" pattern:**
```
[X] has been studied by many researchers (Author1, Year; Author2, Year;
Author3, Year; Author4, Year; Author5, Year).  ← AVOID THIS
```

#### 3.3 Action Verb Hierarchy

Use strong, precise verbs that convey the intellectual relationship between your work and prior work. Avoid weak, non-committal verbs.

**Strong Synthesis Verbs (use these):**
- **Demonstrate** — Shows with compelling evidence
- **Establish** — Provides definitive evidence for
- **Reveal** — Uncovers something previously hidden
- **Confirm** — Provides additional evidence supporting a prior claim
- **Challenge** — Presents evidence against a prior claim
- **Extend** — Builds on prior work by adding new elements
- **Refine** — Narrows or qualifies a prior finding
- **Integrate** — Combines previously separate findings or theories
- **Resolve** — Settles a prior contradiction or debate
- **Transcend** — Moves beyond the limitations of prior approaches

**Weak Verbs (avoid these):**
- **Discuss** — Says things about, without claiming anything
- **Look at** — Examines without asserting
- **Focus on** — Pays attention to without concluding
- **Explore** — Investigates without committing to a finding
- **Note** — Observes without evaluating
- **Mention** — Refers to without engaging

**Moderate Verbs (use sparingly with justification):**
- **Suggest** — Implies but does not demonstrate (use when evidence is suggestive but not conclusive)
- **Indicate** — Points toward (use when the evidence is indirect)
- **Propose** — Puts forward as a possibility (use for theoretical claims without direct evidence)

**Quality Gate:** The related work section must contain zero "laundry list" citation patterns, use strong synthesis verbs for at least 60% of citations, and follow the five-paragraph architecture.

---

### PHASE 4: CITATION STRATEGY

**Objective:** Develop a principled, strategic approach to citation that ensures fairness, completeness, and persuasive positioning.

#### 4.1 Inclusion Rules

Cite a work if ANY of the following apply:
1. It directly addresses your research question or a closely related one
2. It provides the theoretical framework you are using or testing
3. It reports findings that your study replicates, extends, or challenges
4. It developed a measure or method that you are using
5. It represents the most recent or most comprehensive review of your topic
6. It is a foundational work that the field considers essential background
7. It reports findings that contradict your hypothesis or prior findings you discuss
8. It was published by likely reviewers of your manuscript (strategic but ethical — cite only if genuinely relevant)

#### 4.2 Exclusion Rules

Do NOT cite a work if ALL of the following apply:
1. It is only tangentially related to your specific research question
2. It is superseded by more recent or more rigorous work on the same topic
3. It is included only to inflate your reference count
4. It is included only to cite friends, colleagues, or your own prior work without relevance

#### 4.3 Citation Balance Principles

- **Temporal balance:** Include foundational works AND recent works. A reference list containing only pre-2010 works suggests the literature is outdated; only post-2020 works suggests ignorance of the foundations.
- **Geographic balance:** Cite work from multiple research traditions and countries, especially when the phenomenon may be culturally variable.
- **Methodological balance:** Cite studies using different methods; do not only cite studies that share your methodological biases.
- **Perspective balance:** Cite works that support AND challenge your position. Acknowledging counter-evidence strengthens credibility.
- **Self-citation restraint:** Self-citations should not exceed 10% of the reference list unless the paper directly builds on a series of your prior publications.

#### 4.4 Citation Density Guidelines

| Section | Citations per paragraph | Maximum |
|---------|------------------------|---------|
| Introduction | 3–5 | 8 |
| Related Work | 5–10 | 15 |
| Method | 1–3 | 5 |
| Results | 0–1 | 3 |
| Discussion | 3–7 | 10 |

**Quality Gate:** The citation strategy must pass all balance principles. At least 30% of cited works should be from the last 3 years. At least 15% should be foundational (more than 10 years old). Self-citation must be below 10%.

---

### PHASE 5: ANTI-SUMMARY PROTOCOL

**Objective:** Ensure that the literature review synthesizes rather than summarizes. This is the most critical quality gate.

#### The Summary vs. Synthesis Distinction

**Summary** = Sequential description of what each study found
**Synthesis** = Integration of findings across studies to reveal patterns, contradictions, and gaps

#### Comparison Examples

**Example 1: Learning Styles**

❌ **Summary (AVOID):**
> Coffield et al. (2004) reviewed 71 learning style models and found limited evidence for their validity. Pashler et al. (2008) conducted a review and found no evidence that matching instruction to learning styles improves outcomes. Rogowsky et al. (2015) tested the meshing hypothesis with visual and auditory learners and found no effect. Husmann and O'Loughlin (2019) tested learning styles in anatomy education and also found no effect.

✅ **Synthesis (USE):**
> Despite the widespread adoption of learning style-based instruction in educational practice, a consistent body of evidence challenges its empirical foundation. Multiple independent reviews (Coffield et al., 2004; Pashler et al., 2008) and empirical tests (Rogowsky et al., 2015; Husmann & O'Loughlin, 2019) have failed to find evidence that matching instructional methods to learning styles improves learning outcomes, suggesting that the persistence of the learning styles concept is driven by intuitive appeal rather than empirical support.

**Example 2: Mindfulness Interventions**

❌ **Summary (AVOID):**
> Kabat-Zinn (1990) developed mindfulness-based stress reduction (MBSR). Teasdale et al. (2000) found MBSR reduced depression relapse. Grossman et al. (2004) conducted a meta-analysis and found moderate effect sizes. Kuyken et al. (2015) found MBSR was as effective as antidepressants. Goldberg et al. (2022) found publication bias inflated effects.

✅ **Synthesis (USE):**
> Mindfulness-based interventions have accumulated a substantial evidence base over three decades, progressing from initial feasibility demonstrations (Kabat-Zinn, 1990) through efficacy trials for depression relapse (Teasdale et al., 2000) to meta-analytic synthesis (Grossman et al., 2004). However, the field now faces a critical inflection point: while early meta-analyses reported moderate effect sizes, more recent work accounting for publication bias (Goldberg et al., 2022) suggests that the true effect may be smaller than initially believed, raising questions about whether mindfulness interventions offer clinically meaningful advantages over established treatments (Kuyken et al., 2015) or whether their apparent efficacy has been inflated by methodological and reporting biases.

**Example 3: Social Media and Mental Health**

❌ **Summary (AVOID):**
> Twenge et al. (2018) found social media use was associated with depression in adolescents. Orben and Przybylski (2019) found the effect size was very small. Coyne et al. (2020) found no longitudinal association. Boers et al. (2019) found a significant association. Valkenburg et al. (2022) found the relationship depends on type of use.

✅ **Synthesis (USE):**
> The relationship between social media use and adolescent mental health remains fiercely contested, with the literature divided between studies reporting significant associations (Twenge et al., 2018; Boers et al., 2019) and those finding negligible or null effects (Orben & Przybylski, 2019; Coyne et al., 2020). This contradiction appears increasingly resolvable through a moderation lens: the effect of social media on well-being depends not on time spent (the variable most commonly studied) but on the type of engagement — passive scrolling versus active communication (Valkenburg et al., 2022). This shift from a main-effect question to a moderated-effect question represents a theoretical advance that prior cross-sectional, time-use-only studies could not achieve.

#### Anti-Summary Checklist
- [ ] No paragraph describes only one study (except when a single study is the sole evidence on a critical point)
- [ ] Every paragraph makes a conceptual claim that is supported by citations, not a chronological list of findings
- [ ] The narrative has a clear argument structure (context → what is known → what is unknown → how this study addresses it)
- [ ] Strong synthesis verbs outnumber weak verbs by at least 3:1
- [ ] The reader can identify the gap in the literature without the author explicitly saying "there is a gap"
- [ ] Studies are grouped by finding, not by author
- [ ] Contradictions are acknowledged and diagnosed, not ignored or hidden

**Quality Gate:** The anti-summary protocol must pass all checklist items. If any item fails, revise the relevant section before considering the literature review complete.

---

## OUTPUT FORMAT

```markdown
# Literature Command Output

## 1. Literature Architecture
### Temporal Map
[Four-period structure with anchor publications]
### Intellectual Genealogy
[Progenitor works and descendant streams]
### School Map
[Paradigms with assumptions, methods, critiques, blind spots]

## 2. Deep Synthesis
### Consensus Findings
[Findings with effect sizes and boundary conditions]
### Contradictions
[Contradictions with diagnoses]
### Methodological Scorecard
[Systematic evaluation of literature methods]
### Theoretical Voids
[Unintegrated findings and untested theories]

## 3. Related Work Draft
[Five-paragraph architecture following the template]

## 4. Citation Strategy
[Inclusion/exclusion decisions with balance assessment]

## 5. Anti-Summary Verification
[Completed checklist with pass/fail status]

## 6. Validated Gaps
[Confirmed gaps ready for Ideation Engine or Methodology Architect]
```

---

## INTEGRATION NOTES

### With Ideation Engine (01_ideation)
- Receive proposed gaps from the Ideation Engine and validate them through systematic search
- Provide the Deep Synthesis Engine output as evidence for or against gap claims
- Feed confirmed gaps back to the Ideation Engine for refinement

### With Methodology Architect (03_methodology_architect)
- Provide methodological scorecard to inform design decisions
- Supply effect size estimates from meta-analyses for power analysis
- Identify methodological weaknesses in the literature that the proposed study should address

### With Writing Engine (06_writing_engine)
- The Related Work Draft feeds directly into the manuscript
- The five-paragraph architecture maps to the standard Related Work section
- Citation strategy ensures appropriate reference list construction

### With Review Simulator (07_review_simulator)
- Citation strategy informs likely reviewer identities and concerns
- Methodological audit identifies weaknesses that reviewers may target
- Contradiction mapping prepares responses to "but what about Study X that found the opposite?"

---

## USAGE EXAMPLES

**Example 1: Starting a literature review from scratch**
```
User: "I need to do a literature review on the effects of remote work on employee well-being."
→ Execute all 5 phases, building the architecture from systematic search.
```

**Example 2: Improving an existing related work section**
```
User: "Here's my related work section [PASTED TEXT]. It feels like a list of studies, not a synthesis."
→ Execute Phase 5 (Anti-Summary Protocol), identify summary patterns, and rewrite using synthesis.
```

**Example 3: Validating a gap claim**
```
User: "I think there's a gap in the literature on X. Can you verify?"
→ Execute Phase 2 (Deep Synthesis Engine), focusing on the claimed gap area.
```

---

## VERSION HISTORY
- v2.0.0 — Added Anti-Summary Protocol, five-paragraph architecture, action verb hierarchy, citation balance principles
- v1.0.0 — Initial release with basic search and synthesis capabilities
