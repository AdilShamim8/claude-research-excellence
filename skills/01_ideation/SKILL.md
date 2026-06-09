# Ideation Engine

## Skill Metadata
- **Skill Name:** Ideation Engine
- **Version:** 2.0.0
- **Purpose:** Systematically generate, evaluate, and refine novel research ideas with quantified novelty assessment and contribution mapping
- **Trigger:** User wants to develop a new research idea, find a research gap, formulate hypotheses, or assess novelty of a proposed study
- **Integration:** Feeds into Literature Command (02) for gap validation, Methodology Architect (03) for design, and Writing Engine (06) for articulation

---

## ACTIVATE: IDEATION

When the user invokes the Ideation Engine, execute the following five-phase protocol. Do not skip phases. Do not proceed to the next phase until the current one produces output that meets the quality criteria specified.

---

### PHASE 1: FIELD CARTOGRAPHY

**Objective:** Map the intellectual terrain of the target domain to locate frontiers, adjacencies, and contrarian opportunities.

#### 1.1 Frontier Scan
- Identify the 5 most actively cited research streams in the domain over the past 3 years
- For each stream, catalog: leading authors, core journals, dominant methodologies, typical sample sizes, prevailing effect sizes
- Tag each stream as: **Advancing** (growing citation velocity), **Plateauing** (stable citation velocity), or **Retreating** (declining citation velocity)
- Flag streams where methodological sophistication exceeds theoretical depth — these represent opportunities for theoretical contribution

#### 1.2 Adjacency Scan
- Identify 3 neighboring fields whose methods, theories, or data could cross-pollinate into the target domain
- For each adjacency, specify:
  - **Transferable construct:** What concept or method could be imported?
  - **Adaptation requirement:** What modifications are needed for the target domain?
  - **Novelty potential:** Low / Medium / High — with justification
  - **Risk assessment:** Likelihood that the transfer produces trivial or forced results

#### 1.3 Contrarian Probe
- Identify 3 widely accepted claims in the field that have never been rigorously challenged
- For each claim, assess:
  - **Evidential basis:** How strong is the supporting evidence actually? (Rate: Iron-clad / Strong / Moderate / Weak / Folklore)
  - **Challenge feasibility:** Could a well-designed study plausibly overturn this? (Rate: High / Medium / Low)
  - **Impact if overturned:** How much would the field change? (Rate: Paradigm shift / Major revision / Moderate correction / Minor nuance)
- Generate one contrarian research question per challengeable claim

**Quality Gate:** Phase 1 output must include at least 5 frontier streams, 3 adjacencies, and 3 contrarian probes. If the domain is too narrow to support this, expand scope to the parent discipline.

---

### PHASE 2: GAP TYPOLOGY

**Objective:** Classify identified gaps using the seven-type taxonomy to ensure comprehensive coverage and avoid over-concentration on a single gap type.

#### Gap Types

| # | Gap Type | Definition | Diagnostic Question |
|---|----------|-----------|-------------------|
| 1 | **Knowledge Gap** | What is not yet known about a phenomenon | "What do we still not understand about X?" |
| 2 | **Method Gap** | Existing methods are inadequate or absent | "How could we study X more rigorously?" |
| 3 | **Theory Gap** | No adequate theoretical explanation exists | "Why does X occur — and can we explain it?" |
| 4 | **Application Gap** | Knowledge exists but is not applied | "How can we use what we know about X to solve Y?" |
| 5 | **Replication Gap** | Findings lack independent replication | "Has X been replicated in different contexts?" |
| 6 | **Population Gap** | Findings limited to specific populations | "Does X hold for underrepresented group Z?" |
| 7 | **Mechanistic Gap** | Correlation known but mechanism unknown | "Through what process does X lead to Y?" |

#### Gap Assessment Matrix
For each identified gap, score on:

- **Severity** (1-5): How significant is the gap's absence for the field?
- **Feasibility** (1-5): How tractable is addressing this gap with available resources?
- **Impact** (1-5): How much would closing this gap advance knowledge?
- **Novelty** (1-5): How many existing studies already target this gap?

Compute the **Gap Priority Index (GPI)** = (Severity × 0.3) + (Feasibility × 0.2) + (Impact × 0.3) + (Novelty × 0.2)

Rank gaps by GPI descending. Only gaps scoring ≥ 3.0 should advance to Phase 3.

**Quality Gate:** Must produce at least 3 gaps spanning at least 2 different gap types. No more than 40% of gaps should be of a single type.

---

### PHASE 3: QUESTION FORGE

**Objective:** Transform validated gaps into precise, answerable, and novel research questions.

#### Research Question Template
```
[UNDER WHAT CONDITIONS / HOW / WHY / TO WHAT EXTENT]
does [INDEPENDENT VARIABLE / INTERVENTION / EXPOSURE]
[affect / influence / moderate / mediate / predict]
[DEPENDENT VARIABLE / OUTCOME]
in [POPULATION / CONTEXT]
given [THEORETICAL LENS / MECHANISM]?
```

#### Five-Dimensional Scoring

| Dimension | Weight | Scoring Criteria |
|-----------|--------|-----------------|
| **Specificity** | 0.20 | 1=Vague topic area → 5=Precise variables, direction, and population specified |
| **Answerability** | 0.20 | 1=Unanswerable with any method → 5=Clearly answerable with standard methods |
| **Novelty** | 0.25 | 1=Already answered in literature → 5=No prior work addresses this |
| **Impact** | 0.20 | 1=Niche interest only → 5=Field-altering implications |
| **Groundedness** | 0.15 | 1=No theoretical basis → 5=Directly derived from established theory |

**Research Question Quality Index (RQI)** = Σ(Dimension Score × Weight)

**RQI Interpretation:**
- 4.0–5.0: Excellent — proceed directly to Phase 4
- 3.0–3.9: Good — refine wording and re-score
- 2.0–2.9: Marginal — return to Phase 2 and identify alternative gap
- Below 2.0: Unviable — discard and restart

#### Question Refinement Checklist
- [ ] Variables are operationally definable
- [ ] The question implies a falsifiable hypothesis
- [ ] The population is specified and accessible
- [ ] The scope is neither too broad nor too narrow
- [ ] The question is not a disguised "does X exist?" (trivial)
- [ ] The question does not presuppose its answer
- [ ] Alternative explanations are acknowledged

**Quality Gate:** Must produce at least 2 research questions per gap, select the highest RQI question, and verify it scores ≥ 3.5.

---

### PHASE 4: CONTRIBUTION MAPPING

**Objective:** Forecast and articulate the specific contributions the proposed research will make across four domains.

#### Contribution Domains

**4.1 Theoretical Contribution**
- New theory construction: Does this create a new theoretical framework?
- Theory extension: Does this extend an existing theory to a new domain?
- Theory refinement: Does this refine or qualify an existing theory?
- Theory integration: Does this bridge two or more theoretical traditions?
- Theory falsification: Does this test a theory's predictions under new conditions?

**4.2 Methodological Contribution**
- New measure/instrument development
- Novel analytical approach or statistical technique
- Improved research design for existing questions
- New data collection methodology
- Validation of existing methods in new contexts

**4.3 Practical Contribution**
- Direct intervention or policy implication
- Clinical or organizational application
- Stakeholder decision-making support
- Tool or resource creation
- Training or educational application

**4.4 Field Impact**
- Opens new research stream
- Resolves standing debate
- Shifts methodological norms
- Bridges sub-disciplines
- Influences funding priorities

#### Contribution Statement Template
```
This study contributes to [FIELD] by [CONTRIBUTION TYPE] [WHAT IS CONTRIBUTED],
which [HOW IT ADVANCES] [SPECIFIC AREA], thereby [BROADER IMPLICATION].
Unlike prior work that [WHAT OTHERS DID], this study [WHAT IS DIFFERENT AND BETTER].
```

**Quality Gate:** The research must articulate at least one contribution in at least two domains. At least one contribution must be rated "substantial" (not merely incremental).

---

### PHASE 5: NOVELTY CERTIFICATE

**Objective:** Quantify the novelty of the proposed research using the four-dimension scoring system and issue a formal novelty assessment.

#### Scoring Dimensions (0–25 each)

| Dimension | 21–25 | 16–20 | 11–15 | 6–10 | 0–5 |
|-----------|-------|-------|-------|------|-----|
| **First-of-its-kind** | No prior work in this space | One preliminary study exists | A few studies exist but are narrow | Several studies exist | Well-trodden territory |
| **Methodological Innovation** | Entirely new method or paradigm | Significant adaptation of existing method | Moderate methodological refinement | Minor methodological tweak | Standard method, no innovation |
| **Theoretical Advancement** | New theory or paradigm shift | Major theory extension | Moderate theory refinement | Minor theoretical nuance | No theoretical contribution |
| **Empirical Impact** | Findings would reshape the field | Findings would influence multiple sub-fields | Findings would influence one sub-field | Findings would be cited but not transformative | Findings would have limited reach |

#### Total Score Bands

| Score Range | Classification | Description |
|-------------|---------------|-------------|
| 90–100 | **Paradigm Shift** | Field-altering work; will be cited for decades |
| 75–89 | **Major Contribution** | Substantially advances understanding; high-impact publication likely |
| 60–74 | **Solid Contribution** | Meaningful advance; suitable for strong specialty journal |
| 45–59 | **Incremental** | Adds to literature but does not shift understanding |
| 30–44 | **Marginal** | Limited novelty; significant revision needed |
| 0–29 | **Redundant** | Insufficient novelty; do not pursue in current form |

#### Novelty Certificate Format
```
╔══════════════════════════════════════════════╗
║          NOVELTY CERTIFICATE                 ║
╠══════════════════════════════════════════════╣
║ Research Topic: [TOPIC]                      ║
║ Date: [DATE]                                 ║
║                                              ║
║ First-of-its-kind:      [XX]/25             ║
║ Methodological Innovation: [XX]/25           ║
║ Theoretical Advancement:  [XX]/25            ║
║ Empirical Impact:         [XX]/25            ║
║ ─────────────────────────────────            ║
║ TOTAL NOVELTY SCORE:      [XX]/100           ║
║ Classification: [CLASSIFICATION]             ║
║                                              ║
║ Key Strength: [STRONGEST DIMENSION]          ║
║ Key Weakness: [WEAKEST DIMENSION]            ║
║ Recommended Action: [PROCEED/REVISE/PIVOT]  ║
╚══════════════════════════════════════════════╝
```

**Quality Gate:** If the total novelty score is below 45, return to Phase 1 with expanded scope. If between 45–59, identify specific strategies from the novelty_calculator.md to strengthen the weakest dimensions before proceeding.

---

## OUTPUT FORMAT

The Ideation Engine produces the following structured output:

```markdown
# Ideation Engine Output

## 1. Field Cartography
### Frontier Streams
[Numbered list with tags]
### Adjacency Opportunities
[Numbered list with novelty potential]
### Contrarian Probes
[Numbered list with challengeability assessment]

## 2. Gap Analysis
[Gap Priority Matrix with GPI scores and rankings]

## 3. Research Questions
[Top questions with RQI scores and refinement notes]

## 4. Contribution Map
[Contributions by domain with substantiveness rating]

## 5. Novelty Certificate
[Full certificate with scores and classification]

## 6. Recommended Next Steps
[Suggested integration with Literature Command and Methodology Architect]
```

---

## INTEGRATION NOTES

### With Literature Command (02_literature_command)
- Feed identified gaps and questions into the Literature Command for systematic validation
- Use the Deep Synthesis Engine to confirm gaps are genuine (not already filled)
- Use Citation Strategy to identify which works to position against

### With Methodology Architect (03_methodology_architect)
- Feed the top-ranked research question and contribution map to the Methodology Architect
- The methodology must align with the gap type identified (e.g., Method Gaps require methodological innovation)
- Pre-registration should reference the novelty certificate's dimensions

### With Writing Engine (06_writing_engine)
- The Contribution Statement Template feeds directly into the Introduction and Discussion sections
- The Novelty Certificate informs the "contributions" subsection
- Gap typology terms should appear in the literature review framing

### With Review Simulator (07_review_simulator)
- Feed the Novelty Certificate to the Review Simulator to predict reviewer objections about novelty claims
- Use contrarian probes to anticipate reviewer skepticism

---

## USAGE EXAMPLES

**Example 1: Exploring a new domain**
```
User: "I want to study AI-assisted medical diagnosis but I'm not sure where the real gaps are."
→ Execute all 5 phases with "AI-assisted medical diagnosis" as the target domain.
```

**Example 2: Refining an existing idea**
```
User: "I think there's a gap in how mindfulness interventions affect decision-making under uncertainty, but I'm not sure if it's novel enough."
→ Skip Phase 1, validate the gap in Phase 2, forge questions in Phase 3, and assess novelty in Phase 5.
```

**Example 3: Assessing novelty of a drafted proposal**
```
User: "Here's my research proposal [PASTED TEXT]. How novel is it?"
→ Execute Phase 5 only, extracting contributions from the proposal text.
```

---

## VERSION HISTORY
- v2.0.0 — Added five-dimensional RQI scoring, Gap Priority Index, Novelty Certificate format, integration protocols
- v1.0.0 — Initial release with basic gap identification and question generation
