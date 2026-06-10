# ACM Digital Library Paper Format Template

> **CRES Template — ACM Style**
> Covers ACM journal and conference proceedings format requirements for the ACM Digital Library.

---

## 1. Overview

The Association for Computing Machinery (ACM) publishes 50+ journals and hosts 170+ annual conferences. ACM formatting follows the `acmart` document class with sigchi, sigconf, acmjds, and other variants. All ACM publications now require CCS Concepts, accessibility compliance, and open-access licensing metadata. This template provides comprehensive guidance for SIGCHI, SIGCOMM, SIGKDD, SIGMOD, and all other ACM venues.

---

## 2. Page Layout & Margins

| Parameter              | Conference (sigconf) | Journal (acmjds)  |
|------------------------|----------------------|--------------------|
| Paper size             | Letter (8.5" × 11")  | Letter (8.5" × 11") |
| Column count           | 2                    | 2                  |
| Column gutter          | 0.33" (8.4 mm)      | 0.33" (8.4 mm)    |
| Top margin             | 0.75"                | 0.75"              |
| Bottom margin          | 1"                   | 1"                 |
| Left margin            | 0.75"                | 0.75"              |
| Right margin           | 0.75"                | 0.75"              |
| Text width             | 7" (178 mm)          | 7" (178 mm)        |
| Text height            | 9" (229 mm)          | 9" (229 mm)        |

### Page Limits
- **Full papers:** 10–20 pages (varies by venue)
- **Short papers:** 4–6 pages
- **Posters/Demos:** 2–4 pages
- **References:** Do NOT count toward page limit (since ACM 2017 format)
- **Overlength:** Submissions exceeding limits may be desk-rejected

---

## 3. Typography

| Element                | Size      | Style                    |
|------------------------|-----------|--------------------------|
| Title                  | 18 pt     | Bold, sans-serif         |
| Author name            | 11 pt     | Sans-serif               |
| Affiliation            | 10 pt     | Sans-serif, italic       |
| Abstract heading       | 9 pt      | Bold, italic             |
| Abstract body          | 9 pt      | Regular                  |
| Section heading        | 11 pt     | Bold, numbered           |
| Subsection heading     | 10 pt     | Bold, italic, numbered   |
| Body text              | 9 pt      | Regular, justified       |
| Figure caption          | 9 pt      | Regular, sans-serif      |
| Table title             | 9 pt      | Regular, sans-serif      |
| References             | 8 pt      | Regular                  |

**Font:** The `acmart` class uses Libertine for serif and biolinum for sans-serif by default. ACM Serif (a variant of Noto Serif) is also supported.

---

## 4. Title Page Format

### Title
- Centered at top of page
- 18 pt bold
- Capitalize using Title Case
- Avoid abbreviations in the title
- Subtitles after a colon are acceptable

### Author Block
```
First A. Author
University Name, City, Country
author@university.edu

Second B. Author
Another University, City, Country
second@another.edu
```

- Each author on a separate line with affiliation below
- Include email addresses
- ORCID identifiers strongly encouraged
- Conference: affiliation block centered; Journal: left-aligned
- For multi-affiliation: use footnote markers

### ACM Reference Format (Required)
Every ACM paper must include the ACM Reference Format citation at the top of the first column, immediately below the author block:

```
ACM Reference Format:
First Author, Second Author, and Third Author. 2024. Title of the Paper.
In Proceedings of the ACM Conference (Conference '24), Month Date–Date, Year,
City, Country. ACM, New York, NY, USA, 10 pages. https://doi.org/10.1145/1234567
```

### Abstract
- Heading: "Abstract" (bold italic)
- 100–200 words for conference; 150–300 for journals
- Single paragraph, no citations
- No undefined abbreviations
- Must stand alone as a summary

### CCS Concepts (Required)
```
CCS Concepts:
• Human-centered computing → Visualization; Visualization techniques;
• Computing methodologies → Machine learning; Neural networks;
```

- Select from the official ACM Computing Classification System: https://dl.acm.org/ccs
- Include at least one second-level concept
- Three-level hierarchy preferred (leaf nodes)
- Separated by semicolons within a level; "→" between levels

### Keywords
- Heading: "Keywords" (bold)
- Comma-separated, 3–5 terms
- Lowercase except proper nouns

---

## 5. Section Structure

### Standard Section Order
```
1 INTRODUCTION
2 RELATED WORK
3 BACKGROUND / PRELIMINARIES
4 METHOD / APPROACH
5 EVALUATION / EXPERIMENTS
6 DISCUSSION
7 CONCLUSION AND FUTURE WORK
ACKNOWLEDGMENTS
REFERENCES
```

### Introduction (Section 1)
- Motivation and context (1–2 paragraphs)
- Problem statement
- Contributions — enumerate explicitly:
  ```
  The contributions of this work are:
  • We propose...
  • We demonstrate...
  • We release...
  ```
- Paper organization statement

### Related Work (Section 2)
- Organized by thematic categories
- Position your work relative to existing approaches
- Include a comparison table when feasible
- Acknowledge limitations of prior work constructively

### Method (Section 4)
- Technical details presented systematically
- Formal definitions before algorithms
- Design rationale explained
- Subsections for complex methods:
  - 4.1 Problem Definition
  - 4.2 Architecture Overview
  - 4.3 Training Procedure
  - 4.4 Complexity Analysis

### Evaluation (Section 5)
- Experimental setup (datasets, baselines, metrics, hardware)
- Quantitative results with statistical significance
- Qualitative analysis and case studies
- Ablation studies
- User study details (for HCI venues)

### Discussion (Section 6)
- Interpretation beyond results
- Limitations (explicit and honest)
- Ethical considerations (increasingly required)
- Generalizability analysis

### Conclusion (Section 7)
- Key takeaways
- Future work directions
- Do NOT repeat abstract or introduction verbatim

### Acknowledgments
- Spell as "Acknowledgments" (American English)
- Include grant numbers
- Anonymize for double-blind review: "Acknowledgments removed for blind review"

---

## 6. Figure, Table & Algorithm Formatting

### Figures
- Single-column width (3.33") or full-width (7")
- Minimum 300 dpi for raster; vector preferred (PDF, EPS)
- Captions placed **below** figures
- Caption format: "Figure 1: Description." (colon after number)
- Use color; ensure grayscale readability with patterns
- Refer to as "Figure 1" (full word, never "Fig.")

### Tables
- Numbered: "Table 1", "Table 2"
- Title placed **above** the table
- Three-line style (top rule, below header, bottom rule)
- Use `booktabs` package in LaTeX
- Caption format: "Table 1: Description." (colon after number)
- Table notes with superscript symbols below bottom rule

### Algorithms
- Use `algorithm2e` or `algorithmic` package
- Caption above the algorithm block
- Numbered: "Algorithm 1"
- Include line numbers for reference
- Use mathematical notation consistent with paper

```latex
\begin{algorithm}
\caption{Algorithm Name}\label{alg:example}
\begin{algorithmic}[1]
\Require Input parameters
\Ensure Output
\State Initialize $\theta$
\For{$t = 1$ to $T$}
    \State $\theta \leftarrow \theta - \eta \nabla \mathcal{L}(\theta)$
\EndFor
\State \Return $\theta$
\end{algorithmic}
\end{algorithm}
```

---

## 7. Reference Format (ACM Reference Format)

### In-Text Citation
- Author-date style for journals: "(Smith et al. 2024)" or "Smith et al. (2024)"
- Numbered style for conferences: "[1]" or "[Smith et al. 2024]"
- The `acmart` class handles citation style automatically

### Bibliography Entry Examples

```bibtex
@inproceedings{smith2024deep,
  author    = {Smith, John A. and Doe, Jane B.},
  title     = {Deep Learning for Graph Neural Networks},
  booktitle = {Proceedings of the 2024 ACM Conference on Knowledge Discovery
               and Data Mining (KDD '24)},
  pages     = {1234--1245},
  year      = {2024},
  doi       = {10.1145/3637528.3671842}
}

@article{wang2024survey,
  author    = {Wang, Li and Chen, Ming and Lee, Robert},
  title     = {A Survey on Foundation Models},
  journal   = {ACM Computing Surveys},
  volume    = {56},
  number    = {3},
  pages     = {1--38},
  year      = {2024},
  doi       = {10.1145/3617635}
}
```

### Key Rules
- List all authors (do NOT truncate with "et al.")
- Include DOI for all entries where available
- Conference proceedings must include full name and acronym
- Use "n.d." for undated works
- Include month/season for conference proceedings

---

## 8. CCS Concepts Formatting

### How to Select CCS Concepts
1. Visit https://dl.acm.org/ccs
2. Browse or search for relevant concepts
3. Select the most specific (leaf) nodes applicable
4. Minimum: one second-level concept
5. Preferred: multiple third-level concepts

### Formatting in LaTeX
```latex
\begin{CCSXML}
<ccs2012>
<concept>
<concept_id>10010147.10010178</concept_id>
<concept_desc>Computing methodologies~Neural networks</concept_desc>
<concept_significance>500</concept_significance>
</concept>
</ccs2012>
\end{CCSXML}

\ccsdesc[500]{Computing methodologies~Neural networks}
\ccsdesc[300]{Human-centered computing~Visualization}
```

- Significance values: 100 (minor), 300 (moderate), 500 (major)
- The `acmart` class generates the formatted CCS Concepts section automatically

---

## 9. Accessibility Requirements

ACM requires all submissions to meet accessibility standards:

### Figures
- Provide alt-text for every figure
- Use `\Description{...}` in LaTeX for alt-text
- Ensure color is not the sole means of conveying information
- Use patterns, labels, or annotations alongside color

```latex
\begin{figure}[t]
  \includegraphics[width=\columnwidth]{fig1.pdf}
  \Description{A bar chart showing accuracy comparison across five methods.
  The proposed method (blue bar) achieves the highest accuracy at 94.2%.}
  \caption{Comparison of model accuracy on the benchmark dataset.}
  \label{fig:comparison}
\end{figure}
```

### Tables
- Use proper HTML-like markup (header rows, scope attributes)
- Avoid merged cells that break screen reader navigation
- Provide table summaries for complex tables

### PDF Requirements
- Tagged PDF (the `acmart` class generates tagged PDFs)
- Embedded fonts
- Logical reading order
- Document language specified

### Mathematical Content
- Use MathML-compatible LaTeX
- Define all symbols in text
- Provide textual descriptions for complex equations

---

## 10. LaTeX Template Skeleton

```latex
\documentclass[sigconf]{acmart}
% Journal: \documentclass[acmjds]{acmart}
% SIGCHI: \documentclass[sigchi]{acmart}

\usepackage{amsmath,amssymb}
\usepackage{booktabs}
\usepackage{graphicx}
\usepackage{algorithm}
\usepackage{algorithmic}
\usepackage{balance}   % for last-page column balancing

\acmDOI{10.1145/1234567.1234568}
\acmISBN{978-1-4503-XXXX-X/24/06}
\acmConference[Conference '24]{ACM Conference}{June 2024}{City, Country}
\acmYear{2024}
\copyrightyear{2024}

\begin{document}

\title{Title of the Paper: Subtitle if Needed}

\author{First A. Author}
\affiliation{institution={University Name},
  city={City}, country={Country}}
\email{first@university.edu}

\author{Second B. Author}
\affiliation{institution={Another University},
  city={City}, country={Country}}
\email{second@another.edu}

\renewcommand{\shortauthors}{Author et al.}

\begin{abstract}
  Abstract text here. 100--200 words for conference papers.
\end{abstract}

\begin{CCSXML}
<ccs2012>
<concept>
<concept_id>10010147.10010178.10010224</concept_id>
<concept_desc>Computing methodologies~Neural networks</concept_desc>
<concept_significance>500</concept_significance>
</concept>
</ccs2012>
\end{CCSXML}

\ccsdesc[500]{Computing methodologies~Neural networks}

\keywords{deep learning, neural networks, survey}

\maketitle

\section{Introduction}
\label{sec:intro}

\section{Related Work}
\label{sec:related}

\section{Method}
\label{sec:method}
\subsection{Problem Formulation}
\subsection{Algorithm Design}

\section{Evaluation}
\label{sec:eval}

\section{Discussion}
\label{sec:discussion}

\section{Conclusion}
\label{sec:conclusion}

\section*{Acknowledgments}
This work was supported by...

\bibliographystyle{ACM-Reference-Format}
\bibliography{references}

\end{document}
```

---

## 11. Word Template Guidelines

- Download official templates from [ACM Author Center](https://authors.acm.org/)
- Use the ACM Word template (matches `acmart` formatting)
- Set two-column layout: Layout → Columns → Two
- Margins: 0.75" all sides
- Body font: 9 pt Times Roman
- Heading font: 11 pt bold
- Use Equation Editor 3.0 or later for math
- Insert CCS Concepts manually from the ACM CCS tool
- Include ACM Reference Format block at top
- Save as PDF with embedded fonts before submission
- Use EndNote/Zotero with ACM Reference Format style

---

## 12. Common ACM Formatting Mistakes

| # | Mistake | Correction |
|---|---------|-----------|
| 1 | Missing ACM Reference Format block | Required at top of first column |
| 2 | Missing CCS Concepts | Mandatory for all ACM publications |
| 3 | Missing `\Description{}` for figures | Required for accessibility |
| 4 | Using "Fig." instead of "Figure" | ACM uses full "Figure" always |
| 5 | References counting toward page limit | Since 2017, references don't count |
| 6 | Using old `sig-alternate` class | Use `acmart` exclusively |
| 7 | Not anonymizing for blind review | Remove author names, affiliations, URLs |
| 8 | Missing DOI in bibliography entries | Include DOI for all entries |
| 9 | Unbalanced columns on last page | Use `\balance` command before bibliography |
| 10 | Alt-text missing or generic | Write descriptive alt-text for every figure |
| 11 | Using "Acknowledgements" (British) | Use "Acknowledgments" (American) |
| 12 | Inconsistent keyword capitalization | Use lowercase for keywords except proper nouns |
| 13 | Overfull/underfull hbox warnings | Fix before final submission |
| 14 | Missing ORCID for authors | Strongly recommended; add via `\orcid{}` |
| 15 | Not including rights management | ACM requires e-Rights form before camera-ready |

---

## 13. Submission Checklist

### Pre-Submission Content
- [ ] Paper within page limit (references excluded from count)
- [ ] Abstract within word limit
- [ ] Contributions explicitly enumerated in Introduction
- [ ] All acronyms defined at first use
- [ ] All figures, tables, and equations referenced in text
- [ ] Statistical significance reported for experimental results
- [ ] Limitations section/discussion included
- [ ] Ethical considerations addressed (if applicable)

### ACM-Specific Requirements
- [ ] ACM Reference Format block included
- [ ] CCS Concepts selected and formatted correctly
- [ ] `\Description{}` alt-text for every figure
- [ ] Keywords included (3–5 terms)
- [ ] ORCID identifiers added for all authors
- [ ] Paper uses `acmart` document class
- [ ] Correct venue variant selected (sigconf, sigchi, acmjds, etc.)
- [ ] Columns balanced on last page (`\balance`)

### Double-Blind Review (if applicable)
- [ ] Author names removed from title page
- [ ] Affiliations removed or anonymized
- [ ] Self-citations anonymized: "[Author(s) 2024]" → "[Anonymized 2024]"
- [ ] URLs to personal pages removed
- [ ] Acknowledgments anonymized
- [ ] No identifying information in metadata/PDF properties

### Formatting Quality
- [ ] All figures ≥300 dpi or vector format
- [ ] Color figures readable in grayscale
- [ ] Tables use booktabs three-line style
- [ ] Algorithms properly formatted
- [ ] No overfull hbox warnings
- [ ] PDF has embedded fonts
- [ ] No orphan/widow lines

### Final
- [ ] All authors reviewed and approved
- [ ] Supplementary materials uploaded (if applicable)
- [ ] Artifact evaluation materials ready (if applicable)
- [ ] ACM Rights Management form completed (camera-ready stage)
- [ ] Open-access option selected (if desired)
- [ ] Submitted via the conference/journal system

---

## 14. Additional Resources

- **ACM Author Center:** https://authors.acm.org/
- **acmart LaTeX Class:** https://github.com/borisveytsman/acmart
- **ACM CCS Tool:** https://dl.acm.org/ccs
- **ACM Accessibility Guide:** https://www.acm.org/publications/authors/accessibility
- **ACM Reference Format Citation:** https://www.acm.org/publications/authors/reference-formatting
- **Artifact Evaluation:** https://www.acm.org/publications/artifacts

---

*Last updated: 2024 | CRES Template Version 1.0*
