# Novelty Score Rubric

## 🧪 NOVELTY QUANTIFICATION SYSTEM (0–100)

```
ACTIVATE: NOVELTY_SCORE
```

This rubric provides an objective, multi-dimensional assessment of a scientific manuscript's novelty. The total score (0–100) maps directly to publication potential across journal and conference tiers.

---

### Scoring Dimensions

#### DIMENSION 1 — FIRST-OF-ITS-KIND SCORE (0–25)
*Measures conceptual precedence and formulation novelty.*

* **25 pts**: Literally no prior study has asked this question in this way. Opens a new area of inquiry.
* **20 pts**: Minor conceptual precedent exists, but in a fundamentally different domain, context, or scale.
* **15 pts**: Related questions have been investigated, but not with this specific theoretical formulation.
* **10 pts**: Incremental variant or direct parameter extension of existing work.
* **5 pts**: Replication study with minor contextual variation.
* **0 pts**: Direct literal replication with no new formulation.

#### DIMENSION 2 — METHODOLOGICAL INNOVATION SCORE (0–25)
*Measures procedural, algorithmic, or experimental novelty.*

* **25 pts**: Introduces a genuinely new method, algorithm, or experimental paradigm to the scientific community.
* **20 pts**: Creatively imports and adapts an established method from another field in a non-obvious way.
* **15 pts**: Substantially extends an existing method to overcome major documented failure modes.
* **10 pts**: Makes technical optimizations or minor refinements to an established procedure.
* **5 pts**: Applies standard methods with higher execution precision or sample size.
* **0 pts**: Off-the-shelf standard methodology with zero technical innovation.

#### DIMENSION 3 — THEORETICAL ADVANCEMENT SCORE (0–25)
*Measures explanatory power and conceptual reorganization.*

* **25 pts**: Proposes an entirely new theoretical framework that explains previously anomalous phenomena.
* **20 pts**: Substantially revises or refutes the dominant theoretical paradigm in the field.
* **15 pts**: Bridges and formally integrates previously competing, contradictory theories.
* **10 pts**: Extends existing theoretical mechanisms to a previously unmodeled domain.
* **5 pts**: Empirically confirms an existing theoretical prediction in a standard context.
* **0 pts**: Strictly descriptive or empirical observation with no theoretical contribution.

#### DIMENSION 4 — EMPIRICAL IMPACT SCORE (0–25)
*Measures evidentiary significance and real-world consequences.*

* **25 pts**: Conclusively overturns a foundational or widely accepted consensus finding.
* **20 pts**: Resolves a major, long-standing empirical controversy with definitive evidence.
* **15 pts**: Substantially shifts quantitative estimates of an important effect size or relationship.
* **10 pts**: Confirms or refines an important finding using significantly superior experimental controls.
* **5 pts**: Corroborates prior findings in an additional routine test setting.
* **0 pts**: Uninformative null result or underpowered empirical test in a saturated subfield.

---

### Score Interpretation & Venue Calibration

| Score Band | Classification | Target Venue Tier | Expected Reviewer Response |
|---|---|---|---|
| **90–100** | **Paradigm Shift** | *Nature*, *Science*, *Cell*, *NEJM* | Immediate editor interest; sent for rapid peer review; high likelihood of cover highlight |
| **75–89** | **Major Contribution** | Top field-specific journals (*JACS*, *NeurIPS*, *APSR*, *PRL*) | Strong accept recommendations; minimal pushback on novelty; review focuses on technical execution |
| **60–74** | **Solid Contribution** | High-quality specialist journals (*Bioinformatics*, *JCIM*, *PNAS Nexus*) | Favorable review; reviewers may request additional baselines or boundary-condition tests |
| **45–59** | **Incremental Advance** | Standard specialist journals | Mixed reviews; often flagged as "sound but incremental"; venue pivot recommended |
| **30–44** | **Minor Advance** | Niche regional journals / workshop papers | High desk-reject rate at top tiers; requires reframing or expanding the empirical core |
| **< 30** | **Derivative / Flawed** | Pre-print only / Revise research question | Re-evaluate research question; activate `SKILL: IDEATION` to establish genuine novelty |
