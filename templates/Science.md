# Science & Science Advances Format Template

> **CRES Template — Science Family Style**
> Covers Science Research Articles, Reports, and Science Advances Research Articles.

---

## 1. Overview

*Science* is the flagship journal of the American Association for the Advancement of Science (AAAS), with *Science Advances* as its open-access sibling. Both demand concise, high-impact writing accessible to a broad scientific audience. Science enforces strict word limits, forbids subheadings in main text, and has distinctive formatting for references, figures, and supplementary materials. This template covers the specific requirements for both journals.

---

## 2. Article Types & Word Limits

| Article Type              | Journal         | Main Text | Abstract | Figures/Tables |
|---------------------------|-----------------|-----------|----------|----------------|
| Research Article          | Science         | 4,500     | 125      | 4–6 display items |
| Report                    | Science         | 2,500     | 125      | 3–4 display items |
| Research Article          | Science Advances| 6,000     | 150      | 6–8 display items |
| Review                    | Science         | 6,000     | 125      | 6–10 display items |

**Word counts** include all main text from the first word to the last word before References. Methods section is separate and not counted in the main text word limit for Science; for Science Advances, Methods count toward the total.

---

## 3. Title & Author Format

### Title
- **Maximum 95 characters** (including spaces) for Science
- **Maximum 120 characters** for Science Advances
- Must be a declarative statement, not a question
- No abbreviations (except DNA, RNA, HIV, ATP, etc.)
- Avoid filler words ("Novel," "Comprehensive," "First")
- Active, punchy style
- ❌ Bad: "A study investigating the role of CRISPR in gene editing efficiency"
- ✅ Good: "CRISPR enhances gene editing efficiency through guide RNA optimization"

### Author List
```
John A. Smith¹²*, Jane B. Doe³, Robert C. Lee¹, Maria Garcia⁴,
William T. Johnson¹²†

Affiliations listed with superscript numbers.
*Corresponding author. Email: j.smith@cam.ac.uk
†Present address: Department of Biology, MIT, Cambridge, MA, USA.
```

### Author List Rules
- Full first name, middle initial, last name
- Superscript numbers for affiliations
- Asterisk (*) marks corresponding author
- Cross (†) for present address if different
- Up to two corresponding authors allowed
- Group/consortium authors: listed after individual authors with all members in appendix
- ORCID IDs strongly encouraged

### Affiliation Format
```
¹Department of Molecular Biology, University of Cambridge,
  Cambridge CB2 1TN, UK.
²Cambridge Institute for Therapeutic Immunology, University of
  Cambridge, Cambridge CB2 1TN, UK.
```
- Department, Institution, City, State/Postal Code, Country
- No street addresses

---

## 4. Abstract Requirements

### Rules
- **Maximum 125 words** for Science (strictly enforced)
- **Maximum 150 words** for Science Advances
- Single paragraph
- **No citations**
- **No specialized jargon** without explanation
- Must be comprehensible to a reader in any scientific discipline
- Should convey: context → gap → approach → result → significance
- Written in active voice preferred

### Abstract Template
```
[One sentence of broad context]. [One sentence identifying the problem].
[One sentence describing the approach]. [Two to three sentences of
key results with quantitative details]. [One sentence of broader
significance].
```

### Example Abstract
```
The tumor suppressor p53 is mutated in over 50% of human cancers,
yet strategies to restore its function remain limited. Here we show
that a small molecule, REPAIR-1, reactivates mutant p53 by stabilizing
its DNA-binding domain. In mouse models of lung cancer, REPAIR-1
treatment reduced tumor burden by 73% and extended median survival
from 142 to 289 days. Structural analysis revealed that REPAIR-1 binds
to a cryptic pocket in the p53 DNA-binding domain, restoring wild-type
conformation. These findings establish a framework for pharmacological
reactivation of tumor suppressors.
```

---

## 5. Main Text Structure

### Critical Rule: NO Subheadings in Science Main Text

Science main text is continuous prose without ANY subheadings. The text must flow logically from introduction through results to discussion, using paragraph transitions rather than section breaks.

### Main Text Organization

```
[Title]
[Authors & Affiliations]
[Abstract]

Paragraph 1: Broad introduction and context
Paragraph 2: Specific problem and motivation
Paragraph 3: What this paper does — the approach
Paragraphs 4–N: Results (interwoven with interpretation)
Final paragraphs: Discussion, significance, future directions

---
[Materials and Methods — separate section]
[References]
[Acknowledgments]
```

### Paragraph Structure

#### Opening Paragraphs (Introduction)
- **Paragraph 1 (2–3 sentences):** Broad scientific context. What is the field? Why does it matter?
- **Paragraph 2 (2–3 sentences):** The specific problem, gap, or question.
- **Paragraph 3 (2–4 sentences):** What you did and why. The approach and rationale.

#### Middle Paragraphs (Results + Interpretation)
- Each paragraph = one key finding
- Lead with the result, then provide interpretation
- Use transitions: "We next examined...," "To test this hypothesis...," "Consistent with this finding,..."
- Include quantitative details
- Reference figures and tables inline

#### Closing Paragraphs (Discussion)
- Broader significance beyond the specific results
- How results relate to the big picture
- Limitations and caveats
- Future directions and implications
- End with a strong concluding statement

### Key Writing Principles
- **One idea per paragraph**
- **Topic sentence states the key point**
- **Every claim supported by data or citation**
- **Avoid passive construction** when active is clearer
- **No jargon** without definition
- **Quantitative over qualitative**: "73% reduction" not "substantial reduction"

---

## 6. Materials and Methods Section

### Requirements
- Appears after the main text, before references
- Not counted in Science main text word limit (IS counted in Science Advances)
- Must be detailed enough for reproducibility
- Can use subheadings (unlike main text)
- Should include all experimental details, statistical methods, and software versions

### Methods Subsection Template
```
Materials and Methods

Study design. This was a randomized, double-blind, placebo-controlled
trial conducted at three academic medical centers. The primary endpoint
was overall survival at 24 months. The study was approved by the
institutional review board at each site (protocol IDs: IRB-2023-001,
IRB-2023-014, IRB-2023-027) and registered at ClinicalTrials.gov
(NCT05812345).

Cell culture. HEK293T cells (ATCC CRL-3216) were cultured in DMEM
supplemented with 10% FBS at 37°C with 5% CO₂. Cell lines were
authenticated by STR profiling and tested negative for mycoplasma
(DAPI staining, monthly).

CRISPR screening. A genome-wide CRISPR-Cas9 knockout library
(Brunello, Addgene #73179) was transduced at MOI 0.3 into Cas9-
expressing cells. Cells were selected with puromycin (2 μg/ml) for
7 days, then treated with REPAIR-1 (10 μM) or DMSO for 14 days.
Guide representation was quantified by next-generation sequencing.

Statistical analysis. All experiments were performed with ≥3
biological replicates. Two-tailed Student's t-test was used for
two-group comparisons; one-way ANOVA with Bonferroni correction
for multiple groups. Survival curves were compared using the
log-rank test. P < 0.05 was considered significant. Sample sizes
were determined by power analysis (α = 0.05, power = 0.80,
effect size = 0.8).
```

### Methods Must Include
- Study design and rationale
- Sample size determination and power analysis
- Inclusion/exclusion criteria
- Randomization and blinding procedures
- Detailed protocols with catalog numbers
- Software names, versions, and parameters
- Statistical methods with assumptions stated
- Ethics statements with approval numbers
- Clinical trial registration numbers (if applicable)

---

## 7. Figure & Table Formatting

### Figure Requirements

| Parameter          | Specification                           |
|--------------------|-----------------------------------------|
| Single column      | 55 mm (2.2") width                      |
| 1.5 column        | 85 mm (3.4") width                      |
| Double column      | 170 mm (6.7") width                     |
| Maximum height     | 225 mm                                  |
| Resolution         | ≥300 dpi at print size                  |
| File format        | TIFF, EPS, or PDF (initial submission)  |
| Color mode         | RGB for online; CMYK for print          |
| Font in figures    | 6 pt minimum, Helvetica/Arial           |

### Multi-Panel Figures
- Label panels: **(A)**, **(B)**, **(C)** (uppercase, bold, Science style)
- Panel labels top-left of each panel
- Consistent font sizes across all panels within a figure
- 2–4 mm white space between panels
- Scale bars in microscopy images with unit labels

### Figure Caption Format
```
Fig. 1. REPAIR-1 reactivates mutant p53 and reduces tumor growth.
(A) Chemical structure of REPAIR-1. (B) Thermal stability assay
showing REPAIR-1 stabilizes p53 R175H (n = 3 independent
experiments). (C) Tumor volume in mice treated with REPAIR-1
(n = 15 per group) or vehicle over 8 weeks. **P < 0.01,
log-rank test. (D) Overall survival Kaplan-Meier curves for
REPAIR-1 and vehicle groups. P < 0.001, log-rank test.
```

### Figure Caption Rules
- "Fig. X." (period after number, not colon or pipe)
- Title is a complete declarative sentence
- Panel references: (A), (B), (C) — uppercase, parenthetical
- Define all symbols, colors, and error bars
- Include sample sizes (n) for each panel
- Report statistical tests and P values

### Table Format
- Title above table
- Horizontal rules only
- Footnotes with superscript lowercase letters
- Units in column headers where applicable

```
Table 1. Clinical response to REPAIR-1 treatment.

Characteristic          Vehicle      REPAIR-1     P value
────────────────────────────────────────────────────────
Objective response      3/15 (20%)   11/15 (73%)  0.004
Complete response       0/15 (0%)    4/15 (27%)   0.04
Median PFS (months)    4.2          11.7         <0.001
Median OS (months)     14.3         28.9         <0.001
────────────────────────────────────────────────────────
PFS, progression-free survival; OS, overall survival.
P values from Fisher's exact test or log-rank test.
```

---

## 8. Reference Format (Science Style)

### In-Text Citation
- Superscript numbers: "as shown previously³"
- Multiple citations: (³, ⁴) or (³–⁵)
- Place AFTER punctuation: "findings were significant.³"
- Numbered in order of appearance

### Reference List Format

```
1. J. A. Smith, J. B. Doe, R. C. Lee, p53 reactivation by small
   molecules in cancer therapy. Nature 610, 123–129 (2024).
   doi:10.1038/s41586-024-12345-6

2. L. Wang et al., Foundation models for scientific discovery.
   Science 383, 456–463 (2024).

3. W. T. Johnson, Deep Learning in Biomedicine (Cambridge Univ.
   Press, 2024).

4. M. Garcia, Gene editing in cancer therapy. Ph.D. thesis,
   University of Barcelona (2023).

5. NIH, Cancer Statistics 2024; https://www.cancer.gov/statistics
   [accessed 15 January 2024].

6. R. C. Lee, J. A. Smith, U.S. Patent 12,345,678 (2024).
```

### Key Reference Rules
- **Initials before surname:** J. A. Smith (not Smith, J. A.)
- List all authors up to 5; use "et al." for 6+
- Journal name italicized, no abbreviation: *Science* (not *Sci.*)
  - Exception: very long names may be abbreviated (check AAAS guidelines)
- Volume number in bold: **383**
- Year in parentheses: (2024)
- Include DOI when available
- Include URL and access date for web references
- Patent format: Inventor, U.S. Patent number (year)

---

## 9. Supplementary Materials Structure

### Organization
```
Supplementary Materials for
[Title]

Materials and Methods
Fig. S1. [Title]
Fig. S2. [Title]
Table S1. [Title]
Table S2. [Title]
Movie S1. [Title]
Data File S1. [Title]
References (1–N)
```

### Key Requirements
- Must be cited in the main text as "fig. S1," "table S1," "movie S1"
- Lowercase "fig." and "table" for supplementary items
- Compiled into a single PDF for Science
- Science Advances may accept separate files
- Movies and data files uploaded separately
- No page limit, but must be essential supporting material
- Figures must meet the same quality standards as main text figures

### Supplementary Materials Rules
- Peer-reviewed alongside the main manuscript
- Must be self-contained enough to understand
- Include additional experimental details
- Include raw data tables where appropriate
- Include code and computational details
- Include full statistical analyses
- Cross-reference from main text for every item

---

## 10. Author Contribution Requirements

### Science Format
```
Author contributions: J.A.S. conceived the study. J.A.S. and
J.B.D. designed experiments. J.B.D. and R.C.L. performed
experiments. M.G. analyzed data. W.T.J. supervised the project.
J.A.S. wrote the manuscript with input from all authors.
```

### Requirements
- Use initials for each author
- Describe each person's contribution specifically
- Corresponding author(s) typically wrote the manuscript
- Group/consortium members listed in supplementary materials
- Must acknowledge ALL contributors (including non-authors)
- CRediT taxonomy alignment recommended

### Competing Interests
- Required statement for every author
- If none: "The authors declare no competing interests."
- If any: describe specifically
  ```
  J.A.S. is a consultant for OncoPharma Inc. and holds equity in
  GeneEdit Therapeutics. W.T.J. is an inventor on patent
  application PCT/US2024/01234 related to this work.
  ```

---

## 11. Common Science Formatting Mistakes

| # | Mistake | Correction |
|---|---------|-----------|
| 1 | Using subheadings in main text | Science forbids ALL subheadings in main text |
| 2 | Abstract over 125 words | Strictly enforced; count carefully |
| 3 | Passive voice throughout | Use active voice for clarity |
| 4 | Jargon in abstract | Must be accessible to all scientists |
| 5 | Title as a question | Use declarative statement |
| 6 | "Figure" instead of "Fig." | Use "Fig." in captions and references |
| 7 | Lowercase panel labels (a, b) | Use uppercase (A), (B), (C) |
| 8 | Colon after figure number | Use period: "Fig. 1." not "Fig. 1:" |
| 9 | Methods counted in word limit | Methods separate for Science (not for Sci. Adv.) |
| 10 | Missing competing interests | Required for ALL authors |
| 11 | Supplementary figures as "Figure S1" | Use "fig. S1" (lowercase) in main text |
| 12 | Abbreviated journal names in references | Use full journal names |
| 13 | Missing DOI in references | Include DOI for all journal articles |
| 14 | Not citing all supplementary items | Every supplementary item must be cited in main text |
| 15 | First person in abstract | Avoid "we"; use third person or passive |

---

## 12. Submission Checklist

### Pre-Submission Content
- [ ] Main text within word limit (4,500 Research Article / 2,500 Report)
- [ ] Abstract ≤125 words, no citations, no jargon
- [ ] Title ≤95 characters, declarative statement
- [ ] No subheadings in main text
- [ ] Display items within limit
- [ ] Methods section separate and detailed
- [ ] Statistical tests fully reported
- [ ] Sample sizes justified

### Figure Quality
- [ ] All figures ≥300 dpi at print size
- [ ] Panel labels uppercase (A), (B), (C)
- [ ] Font in figures ≥6 pt
- [ ] Scale bars included where appropriate
- [ ] Colorblind-friendly palettes used
- [ ] Figure captions use "Fig. X." format

### Supplementary Materials
- [ ] All supplementary items cited in main text
- [ ] Compiled into single PDF
- [ ] Movies and data files uploaded separately
- [ ] Supplementary references numbered separately
- [ ] Same quality standards as main text

### Author & Compliance
- [ ] Author contributions statement included
- [ ] Competing interests declared for ALL authors
- [ ] Data availability statement included
- [ ] Code availability statement included
- [ ] Ethics approval documented
- [ ] Clinical trial registration (if applicable)
- [ ] ARRIVE/CONSORT guidelines followed

### Final
- [ ] Cover letter emphasizing broad significance
- [ ] All authors reviewed and approved
- [ ] Suggested reviewers identified (4–8)
- [ ] Opposed reviewers listed (optional, with justification)
- [ ] Submit via Science's online submission system
- [ ] No identifying information in manuscript for initial review

---

## 13. Science vs. Science Advances Key Differences

| Feature                   | Science                | Science Advances       |
|---------------------------|------------------------|------------------------|
| Access model              | Subscription           | Open Access (APC)      |
| Main text limit           | 4,500 words (Article)  | 6,000 words            |
| Abstract limit            | 125 words              | 150 words              |
| Title limit               | 95 characters          | 120 characters         |
| Methods counted           | No (separate)          | Yes (in total)         |
| Subheadings in main text  | No                     | Yes (permitted)        |
| Supplementary format      | Single PDF             | Separate files OK      |
| Presubmission inquiry     | Recommended            | Not required           |
| Review process            | Board + external       | External peer review   |
| Publication timeline      | ~4–6 months            | ~2–3 months            |

---

## 14. Additional Resources

- **Science Author Portal:** https://www.science.org/content/page/instructions-preparing-initial-manuscript
- **Science Advances Instructions:** https://www.science.org/journal/sciadv/instructions-for-authors
- **Science Figure Preparation:** https://www.science.org/content/page/instructions-preparing-figures
- **Science Editorial Policies:** https://www.science.org/content/page/editorial-policies
- **AAAS E-CSF (Competing Interests):** https://www.science.org/content/page/editorial-policies

---

*Last updated: 2024 | CRES Template Version 1.0*
