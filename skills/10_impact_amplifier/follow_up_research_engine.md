# Follow-Up Research Engine: From Single Paper to Research Program

> **A single paper is a data point. A research program is a career. This guide transforms your published findings into a sustained, impactful research agenda.**

---

## 1. Identifying Natural Follow-Up Directions

### The Follow-Up Identification Framework

Every paper contains the seeds of future research. Systematically identify these seeds using the following framework:

#### Source 1: Your Own Limitations Section

Your paper's limitations are the most direct roadmap to follow-up studies. Every limitation represents an unanswered question or untested boundary.

**Extraction protocol:**
```
For each limitation in your paper:
1. Rephrase it as a research question
2. Assess feasibility (low/medium/high)
3. Assess impact potential (low/medium/high)
4. Estimate timeline (3 months, 6 months, 1 year, 2+ years)
5. Identify required resources (data, collaborators, funding, equipment)
6. Classify as: quick follow-up (< 6 months) or major study (> 6 months)
```

**Example transformation:**
| Limitation | Research Question | Feasibility | Impact | Timeline |
|---|---|---|---|---|
| "We only tested on English-language data" | "Does the model generalize to multilingual settings?" | Medium | High | 6–12 months |
| "Sample size was modest (N=150)" | "Do findings replicate with N=1,000+?" | Low (requires new data collection) | High | 1–2 years |
| "We did not compare with Method X" | "How does our approach compare with Method X on benchmark Y?" | High | Medium | 3 months |
| "Single-site study" | "Do findings generalize across institutions?" | Medium | High | 1 year |

#### Source 2: Unexpected and Null Findings

Unexpected results are often more valuable than expected ones — they reveal gaps in theoretical understanding.

**Mining protocol:**
```
For each unexpected or null finding:
1. Document the finding precisely (what was expected, what was observed)
2. Generate 3 possible explanations
3. For each explanation, design a study that would test it
4. Prioritize by: (a) most likely explanation, (b) easiest to test,
   (c) most impactful if confirmed
```

#### Source 3: Reviewer Comments

Reviewer feedback often identifies the most important follow-up directions, even (especially) when you pushed back.

**Mining protocol:**
```
For each reviewer comment you:
- Addressed partially → The partial response is a seed for future work
- Disagreed with → You may be wrong; design a study to settle the debate
- Could not address due to scope → This is your next paper's starting point
- Addressed with additional analysis → Extend the analysis further
```

#### Source 4: Citation Analysis

When others cite your work, they reveal how they're building on it — and what they couldn't do.

**Mining protocol:**
1. Set up Google Scholar alerts for citations to your paper
2. For each citing paper, note:
   - What aspect of your work they cite
   - What they extend or modify
   - What they identify as a limitation of your approach
   - What new questions their extension raises
3. Identify clusters: if multiple papers extend the same aspect, that's a hot direction

---

## 2. Extending Current Findings

### Extension Dimension 1: New Populations

**Strategy**: Test whether findings generalize to different demographic, clinical, or cultural groups.

| Original Population | Extension Populations | Why It Matters |
|---|---|---|
| College students (WEIRD) | Community adults, older adults, non-Western populations | WEIRD samples may not generalize (Henrich et al., 2010) |
| Single clinical site | Multi-site, different healthcare systems | Practice patterns vary; generalizability uncertain |
| One language/culture | Multiple languages, cross-cultural comparison | Language and culture affect cognition and behavior |
| Adults | Children, adolescents, elderly | Developmental differences may change effects |
| High-resource setting | Low-resource setting | Equity and scalability considerations |

**Study design template:**
```
Title: [Original finding] in [new population]: A [study design] study

Rationale: [Original Author, Year] demonstrated [finding] in [original
population]. However, it remains unknown whether this effect extends
to [new population], which differs from the original sample in [key
differences]. Understanding this is important because [reason].

Methods: We replicate the study design of [Original Author, Year]
with the following modifications: [adaptations for new population].
Primary outcome: [same as original]. Sample size: [power analysis
referencing original effect size].
```

### Extension Dimension 2: New Contexts

**Strategy**: Test findings in different environmental, organizational, or temporal contexts.

| Original Context | Extension Contexts | Research Questions |
|---|---|---|
| Laboratory | Field/real-world | Does the effect survive ecological validity? |
| Peace/calm | Crisis/urgent | Is the finding robust under pressure? |
| Individual decision | Group/team decision | Do social dynamics change the effect? |
| Static environment | Dynamic/changing environment | Does adaptation change the pattern? |
| Short-term | Long-term/follow-up | Is the effect durable? |

### Extension Dimension 3: New Methods

**Strategy**: Replicate findings using different methodological approaches to test robustness.

| Original Method | Extension Methods | What It Tests |
|---|---|---|
| Self-report survey | Behavioral/observational | Convergent validity |
| Cross-sectional | Longitudinal | Causal direction |
| Correlational | Experimental | Causality |
| Single method | Multi-method triangulation | Method invariance |
| Traditional statistics | Machine learning | Predictive validity |
| Small-scale qualitative | Large-scale quantitative | Generalizability + depth |

### Extension Priority Matrix

| Extension Type | Feasibility | Impact | Priority |
|---|---|---|---|
| New population + same method | Medium | High | **HIGH** |
| Same population + new method | Medium | Medium | **MEDIUM** |
| New context + same method | Low-Medium | High | **MEDIUM** |
| New population + new method | Low | Very High | **HIGH** (long-term) |
| Same everything + larger sample | Medium | Medium | **LOW-MEDIUM** |

---

## 3. Addressing Limitations Through New Studies

### Limitation → Study Design Protocol

For each identified limitation, use this protocol to design a targeted follow-up study:

```
LIMITATION: [Specific limitation from original paper]

TARGETED STUDY DESIGN:

Research Question: [Rephrased as a testable question]
  - Null hypothesis: [H0]
  - Alternative hypothesis: [H1]

Study Design: [Type: RCT, cohort, case-control, experimental, etc.]
  - Population: [Who]
  - Sample size: [N, justified by power analysis]
  - Key variables: [Independent, dependent, control]
  - Analysis plan: [Pre-specified]

How It Addresses the Limitation:
  [Explicit connection: "This study addresses the limitation that
  [original limitation] by [specific feature of new study]."]

Timeline: [Estimated duration]
Resources needed: [Funding, data, collaborators, equipment]
Dependencies: [What must happen first]
```

### Common Limitation Types and Study Designs

| Limitation Type | Best Follow-Up Design | Example |
|---|---|---|
| Small sample size | Replication with larger sample | Multi-site data collection |
| Cross-sectional design | Longitudinal follow-up | Prospective cohort study |
| Single method | Multi-method study | Add behavioral measure to self-report |
| WEIRD sample | Cross-cultural replication | International collaboration |
| Correlational only | Experimental manipulation | Randomized controlled trial |
| Self-report bias | Objective measurement | Wearable sensors, administrative data |
| Short follow-up | Extended follow-up | 5-year longitudinal extension |
| No active control | Controlled trial with active comparator | RCT with treatment-as-usual control |

---

## 4. Building a Research Program from a Single Paper

### The Research Program Maturity Model

```
STAGE 1: Single Paper (Foundation)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  One study, one finding, one paper
  ↓

STAGE 2: Paper Cluster (3-5 papers)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Extensions, replications, and methodological refinements
  connected by a common theme
  ↓

STAGE 3: Research Stream (8-15 papers)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  A coherent body of work establishing expertise in a niche
  Includes theoretical, methodological, and empirical contributions
  ↓

STAGE 4: Research Program (20+ papers)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  A recognized program with:
  - Theoretical framework
  - Methodological toolkit
  - Empirical evidence base
  - Practical applications
  - Trainees and collaborators
  - Sustained funding
```

### Stage Transitions

#### Stage 1 → Stage 2: From Paper to Cluster (Year 1–2)

**Goal**: Generate 2–4 follow-up papers from your initial finding.

**Actions:**
1. Complete the Follow-Up Identification Framework (Section 1)
2. Prioritize 3–4 follow-up studies by feasibility and impact
3. Begin the quickest follow-up immediately (parallel with dissemination)
4. Submit a grant proposal for the larger follow-up study
5. Present at 2–3 conferences to build visibility and find collaborators
6. Recruit a graduate student or postdoc to work on the research stream

**Paper cluster structure:**
```
Paper 1 (original): "We found X" [Published]
Paper 2 (extension): "X also holds in population B" [6-12 months]
Paper 3 (method): "A better way to measure X" [9-15 months]
Paper 4 (application): "Using X to solve real-world problem Y" [12-18 months]
Paper 5 (review): "The state of X: A systematic review" [18-24 months]
```

#### Stage 2 → Stage 3: From Cluster to Stream (Year 2–4)

**Goal**: Establish a coherent research identity with 8–15 papers.

**Actions:**
1. Develop a unifying theoretical framework that connects your papers
2. Create methodological standards or tools that others adopt
3. Build a collaborative network (5–10 active collaborators)
4. Secure multi-year funding (R01, ERC, or equivalent)
5. Train graduate students who extend the work in new directions
6. Write a review article that positions your stream within the broader field
7. Organize a conference symposium or special issue on your topic

#### Stage 3 → Stage 4: From Stream to Program (Year 4–8)

**Goal**: Become the recognized authority in your research niche.

**Actions:**
1. Publish a book or definitive review establishing your framework
2. Develop open-source tools or datasets widely adopted by the community
3. Lead multi-site or international collaborations
4. Mentor junior researchers who establish their own programs
5. Influence policy or practice through translational work
6. Contribute to editorial boards and funding panels
7. Establish a research center or lab focused on the program

---

## 5. Collaborative Follow-Up Opportunities

### Identifying Collaboration Partners

**Collaboration identification protocol:**
```
1. Identify researchers who cite your work (Google Scholar alerts)
2. Note researchers whose work you cite (your Tier 2 engagement citations)
3. Look for complementary expertise:
   - You do computational work → Find a clinical collaborator
   - You do empirical studies → Find a theoretical collaborator
   - You work in one population → Find someone in a different population
4. Attend conferences and note speakers whose work intersects yours
5. Review funding calls for collaborative opportunities
```

### Collaboration Outreach Template

```
Subject: Potential collaboration on [topic]

Dear Dr. [Name],

I've been following your work on [their specific contribution], 
particularly your recent paper on [specific paper]. I found your
approach to [specific aspect] very compelling.

We recently published a study showing [your finding, 1 sentence].
I believe there's a natural synergy between our approaches:
[Specific connection — e.g., "Our computational framework could
be applied to your clinical dataset" or "Your theoretical model
could explain the pattern we observe empirically"].

Would you be interested in exploring a collaboration? I'd be happy
to schedule a brief call to discuss potential directions.

Best regards,
[Name]
```

### Collaboration Models

| Model | Description | Best For | Timeline |
|---|---|---|---|
| **Co-analysis** | Each party analyzes the same data with different methods | Method comparison studies | 3–6 months |
| **Data sharing** | One party provides data, other provides analysis | Leveraging unique datasets | 6–12 months |
| **Parallel studies** | Each party runs their own study with coordinated protocols | Cross-site replication | 12–24 months |
| **Sequential studies** | One party's output is the other's input | Multi-stage research | 12–36 months |
| **Co-design** | Jointly design and execute a new study | Large-scale projects | 12–48 months |

---

## 6. Grant Proposal Generation from Paper Findings

### From Paper to Grant: The Transformation

A published paper demonstrates feasibility. A grant proposal extends that feasibility into a sustained research plan.

**Key transformation principles:**
1. **Paper = proof of concept.** Grant = scaling and extending the concept.
2. **Paper answers one question.** Grant answers a family of related questions.
3. **Paper has one method.** Grant has a multi-method approach.
4. **Paper has local impact.** Grant has field-level impact.

### Grant Proposal Structure from Paper Findings

```
SPECIFIC AIM 1: [Extend the primary finding]
  Rationale: [Based on Paper 1 finding]
  Approach: [Larger sample, additional sites, longitudinal design]
  Expected outcome: [Confirm generalizability, identify boundary conditions]
  Innovation: [What's new beyond the original paper]

SPECIFIC AIM 2: [Address key limitation]
  Rationale: [Limitation identified in Paper 1]
  Approach: [New method or design that addresses the limitation]
  Expected outcome: [Stronger causal inference or broader applicability]
  Innovation: [Methodological advance]

SPECIFIC AIM 3: [Apply the finding]
  Rationale: [Practical implication identified in Paper 1 Discussion]
  Approach: [Intervention, tool development, or implementation study]
  Expected outcome: [Real-world impact, translational milestone]
  Innovation: [Bridging research-practice gap]
```

### Funding Source Mapping

| Follow-Up Type | Funding Sources | Typical Amount | Duration |
|---|---|---|---|
| **Replication/extension** | NSF, ESRC, DFG, internal grants | $50K–$300K | 1–2 years |
| **Multi-site study** | NIH R01, ERC, Wellcome Trust | $500K–$3M | 3–5 years |
| **Methodological development** | NSF, DARPA, EPSRC | $200K–$1M | 2–3 years |
| **Intervention/clinical trial** | NIH, PCORI, AHRQ | $1M–$10M | 3–7 years |
| **Technology translation** | NSF SBIR/STTR, EU Horizon | $150K–$2M | 1–3 years |
| **Cross-disciplinary** | NSF Crosscutting, EU Horizon | $300K–$2M | 2–4 years |

---

## 7. Preparing for Reviewer Requests for Future Work

### Proactive Future Work Section

Don't wait for reviewers to ask — include a compelling Future Directions section that demonstrates vision.

**Template:**
```
This study opens several promising avenues for future research:

1. IMMEDIATE EXTENSIONS (feasible within 6-12 months):
   [1-2 specific follow-up studies that extend the current findings]
   Example: "Testing whether the observed effect holds in [population]
   using [method] would address the generalizability limitation and
   is a priority for our ongoing work."

2. METHODOLOGICAL ADVANCES (12-24 months):
   [Methodological improvements that would strengthen the evidence]
   Example: "Developing [method/tool] would enable more precise
   measurement of [construct], potentially revealing [expected
   insight]."

3. TRANSLATIONAL DIRECTIONS (2-5 years):
   [Real-world applications of the findings]
   Example: "Applying this framework in [applied context] could
   transform [process/outcome], a direction we are pursuing through
   a collaboration with [partner]."

4. THEORETICAL IMPLICATIONS (ongoing):
   [How the findings challenge or advance theory]
   Example: "Our results are consistent with [Theory A] but
   inconsistent with [Theory B] on [specific point]. Resolving
   this tension requires [specific study design]."
```

### Reviewer Pre-Emption Strategy

Anticipate what reviewers will ask for future work and address it proactively:

| Likely Reviewer Request | Pre-Emptive Action in Manuscript |
|---|---|
| "The authors should test this in a different population" | Acknowledge in Limitations; describe planned replication in Future Directions |
| "A longitudinal design would strengthen this" | Note in Future Directions; if pilot longitudinal data exists, mention it |
| "The mechanism is unclear" | Propose mechanistic studies in Future Directions; cite relevant theory |
| "Clinical/practical implications are not clear" | Expand Discussion to include concrete applications |
| "How does this relate to [competing approach]?" | Address in Discussion; cite and compare with the alternative |

---

## 8. Research Agenda Planning

### 1-Year Research Agenda

**Template:**
```
YEAR 1: CONSOLIDATION AND EXTENSION

Q1 (Months 1-3):
  - Complete dissemination activities for Paper 1
  - Begin data collection/analysis for Paper 2 (quickest follow-up)
  - Submit grant proposal for 3-year follow-up study
  - Present Paper 1 at 1-2 conferences

Q2 (Months 4-6):
  - Submit Paper 2 for publication
  - Begin data collection for Paper 3 (methodological extension)
  - Set up collaboration for Paper 4 (different population)
  - Recruit graduate student for research stream

Q3 (Months 7-9):
  - Revise Paper 2 based on reviewer feedback
  - Continue Paper 3 analysis
  - Begin Paper 4 data collection (collaborative)
  - Present at 1-2 conferences

Q4 (Months 10-12):
  - Submit Paper 3 for publication
  - Continue Paper 4 data collection
  - Plan Year 2 agenda based on emerging results
  - Write review article or book chapter (Paper 5)

Year 1 Target: 2-3 papers submitted, 1 grant proposal, 1 collaboration established
```

### 3-Year Research Agenda

**Template:**
```
YEAR 1: FOUNDATION
  Papers: Submit Papers 2-3; begin Papers 4-5
  Funding: Secure initial grant for research stream
  Collaboration: Establish 2-3 active collaborations
  Visibility: Present at 4-6 conferences; 1 workshop/tutorial
  Team: Recruit 1 graduate student + 1 postdoc

YEAR 2: EXPANSION
  Papers: Submit Papers 4-6; begin Papers 7-8
  Funding: Submit larger grant (R01/ERC scale) based on Year 1 results
  Collaboration: Expand to international collaborations
  Visibility: Organize conference symposium; guest edit special issue
  Team: Graduate student producing independent papers

YEAR 3: CONSOLIDATION
  Papers: Submit Papers 7-9; write comprehensive review (Paper 10)
  Funding: Secure multi-year funding for research program
  Collaboration: Lead multi-site study
  Visibility: Keynote/invited talks; develop open-source tool
  Team: Growing lab; mentoring junior researchers

3-Year Target: 8-10 papers, sustained funding, recognized expertise
```

### 5-Year Research Agenda

**Template:**
```
YEARS 1-2: ESTABLISH (as above)

YEAR 3: DEEPEN
  - Publish the definitive methodological paper for your approach
  - Begin translating findings to practice
  - Establish international collaboration network
  - Secure second major grant
  - Target: 12-15 total papers

YEAR 4: TRANSLATE
  - Implement findings in applied settings
  - Develop tools or interventions based on research
  - Train practitioners or clinicians in your methods
  - Begin policy engagement (briefs, testimony, advisory roles)
  - Target: 18-22 total papers

YEAR 5: LEAD
  - Publish book or definitive review establishing your framework
  - Lead a multi-site or multi-national study
  - Mentor junior researchers with their own emerging programs
  - Influence standards or guidelines in your field
  - Target: 25+ papers; recognized research program
```

---

## 9. From Single Paper to Research Program Roadmap

### The Complete Roadmap

```
MONTH 0: PAPER PUBLISHED
│
├─ MONTH 1: Dissemination (Skill 10, Component 2)
│   └─ Social media, email, conference submission
│
├─ MONTHS 2-3: Follow-Up Identification
│   └─ Complete framework from Section 1
│   └─ Prioritize 3-4 follow-up studies
│   └─ Begin quickest follow-up immediately
│
├─ MONTHS 3-6: First Extensions
│   └─ Paper 2 (quick extension) in preparation
│   └─ Grant proposal submitted
│   └─ Collaboration outreach initiated
│
├─ MONTHS 6-12: Paper Cluster Formation
│   └─ Paper 2 submitted
│   └─ Paper 3 (methodological) in preparation
│   └─ Grant decision received (ideally funded)
│   └─ Graduate student/postdoc recruited
│
├─ YEAR 2: Stream Development
│   └─ Papers 3-5 submitted
│   └─ Multi-site or multi-method study initiated
│   └─ Conference symposium organized
│   └─ Review article drafted
│
├─ YEAR 3: Program Consolidation
│   └─ 8-10 papers published
│   └─ Theoretical framework refined
│   └─ International collaboration established
│   └─ Open-source tool or dataset released
│
├─ YEARS 4-5: Program Leadership
│   └─ 15-25 papers published
│   └─ Book or definitive review published
│   └─ Policy or practice impact achieved
│   └─ Research center or lab established
│   └─ Junior researchers mentored into independence
│
└─ YEAR 5+: Sustained Program
    └─ Self-sustaining research program
    └─ Next-generation researchers extending the work
    └─ Legacy: theoretical framework, methods, evidence base,
        practical applications, trained researchers
```

### Decision Points and Pivot Criteria

At each stage, assess whether to continue, pivot, or exit:

| Assessment | Continue If | Pivot If | Exit If |
|---|---|---|---|
| **Citation trajectory** | Growing as predicted | Plateauing with clear explanation | Declining with no recovery strategy |
| **Funding success** | Grant funded or promising resubmission | Rejected but reviewers suggest viable alternative | Repeatedly rejected; field may have moved on |
| **Collaborator interest** | Active collaborators engaging | Potential collaborators in adjacent area | No interest from anyone in 18+ months |
| **Personal interest** | Still excited about the questions | New questions within the same theme more compelling | Burnout or loss of interest |
| **Field dynamics** | Field is growing or stable | Field is shifting but your work can adapt | Field is declining or your approach is superseded |

---

*Last updated: 2024 | CRES v2.0 | Skill 10: Impact Amplifier*
