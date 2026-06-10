# IEEE Journal & Conference Paper Format Template

> **CRES Template — IEEE Style**
> Covers IEEE Transactions, Journals, Magazines, and Conference proceedings format requirements.

---

## 1. Overview

The Institute of Electrical and Electronics Engineers (IEEE) publishes over 200 peer-reviewed journals and hosts 1,800+ annual conferences. IEEE formatting follows a two-column layout with specific typography, citation, and structural conventions. This template provides comprehensive guidance for both journal (Transactions) and conference paper submissions.

---

## 2. Page Layout & Margins

| Parameter            | Journal (Letter) | Conference (Letter) |
|----------------------|-------------------|---------------------|
| Paper size           | 8.5" × 11"       | 8.5" × 11"         |
| Column count         | 2                 | 2                   |
| Column gutter        | 0.2" (5 mm)      | 0.2" (5 mm)        |
| Top margin           | 0.75" (19 mm)    | 0.75" (19 mm)      |
| Bottom margin        | 1" (25.4 mm)     | 1" (25.4 mm)       |
| Left margin          | 0.625" (16 mm)   | 0.625" (16 mm)     |
| Right margin         | 0.625" (16 mm)   | 0.625" (16 mm)     |
| Text width           | 6.875" (175 mm)  | 6.875" (175 mm)    |
| Text height          | 9" (228 mm)      | 9" (228 mm)        |

### Page Limits

- **Regular papers (Transactions):** 8–14 pages (varies by journal)
- **Short papers / Letters:** 4–6 pages
- **Conference papers:** Typically 4–8 pages (check CFP)
- **Overlength charges:** Apply beyond the page limit (~$200–$250 per extra page)

---

## 3. Typography

| Element              | Size      | Style         |
|----------------------|-----------|---------------|
| Title                | 24 pt     | Bold, centered |
| Author name          | 11 pt     | Regular, centered |
| Author affiliation   | 9 pt      | Italic, centered |
| Abstract heading     | 9 pt      | Bold, italic  |
| Abstract body        | 9 pt      | Regular, justified |
| Section heading      | 10 pt     | Bold, Roman numerals, small caps |
| Subsection heading   | 10 pt     | Bold, italic, lettered (A, B, C) |
| Body text            | 10 pt     | Regular, justified, two-column |
| Figure caption        | 8 pt      | Regular, centered below figure |
| Table title           | 8 pt      | Regular, centered above table |
| References            | 8 pt      | Regular, two-column |
| Footnotes             | 8 pt      | Regular |

**Font:** Times Roman (serif) for body; Helvetica/Arial for figure labels if needed.

---

## 4. Title Page Format

### Title
- Centered at top of first column
- 24 pt bold, capitalize first letter of major words
- Avoid abbreviations; keep under 15 words recommended
- Do NOT use "A," "An," or "The" as first word unless essential

### Author Block
```
First A. Author¹, Second B. Author², and Third C. Author¹

¹Department of Electrical Engineering, University Name, City, State ZIP, USA
²Department of Computer Science, Another University, City, Country
```

- List all authors with superscript affiliation numbers
- Include ORCID identifiers where possible (superscript after name)
- Provide email addresses (usually in footnote)
- Conference papers: add membership grade (e.g., "IEEE Member," "IEEE Fellow")

### Abstract
- Heading: "Abstract—" (bold italic, followed by em-dash)
- 150–250 words recommended (check specific journal)
- Written as a single paragraph
- No citations, no undefined abbreviations
- State problem, approach, key results, and significance

### Keywords
- Heading: "Index Terms—" (bold italic, followed by em-dash)
- Comma-separated list
- Use IEEE approved terms from the IEEE Thesaurus where possible
- 5–10 terms recommended
- Capitalize only the first term; lowercase remaining terms

---

## 5. Section Structure

### Standard Section Order

```
I.   INTRODUCTION
II.  RELATED WORK
III. PROPOSED METHOD / METHODOLOGY / SYSTEM MODEL
IV.  EXPERIMENTAL RESULTS / SIMULATION RESULTS
V.   DISCUSSION
VI.  CONCLUSION
     ACKNOWLEDGMENT
     REFERENCES
```

### Introduction (Section I)
- Provide context and motivation (2–3 paragraphs)
- Identify the specific problem or gap
- Summarize contributions (use a brief enumerated list when multiple)
- Provide paper organization roadmap

### Related Work (Section II)
- Organize by theme/approach, not chronologically
- Compare and contrast existing methods
- Identify limitations your work addresses
- Use a summary table when comparing many methods

### Method (Section III)
- Present technical approach systematically
- Include mathematical formulations with proper notation
- Use subsections for complex methods:
  - A. Problem Formulation
  - B. Algorithm Design
  - C. Complexity Analysis

### Results (Section IV)
- Present findings in logical order
- Include quantitative comparisons (tables)
- Include visual evidence (figures)
- Report statistical significance where applicable
- Use subsections aligned with method subsections

### Discussion (Section V)
- Interpret results beyond mere reporting
- Compare with prior state of the art
- Discuss limitations and failure cases
- Identify broader implications

### Conclusion (Section VI)
- Summarize key findings (not a repetition of abstract)
- State significance and impact
- Identify future research directions
- Keep concise (1–2 paragraphs)

### Acknowledgment
- Spell "Acknowledgment" (American spelling, no "e" after "g")
- Grant numbers in full (e.g., "NSF Grant CNS-1234567")
- Thank reviewers indirectly; do NOT identify them

---

## 6. Figure Formatting Standards

### General Rules
- Figures span one column (3.375"/86 mm) or full width (6.875"/175 mm)
- Minimum resolution: **300 dpi** for raster images; vector preferred
- Accepted formats: EPS, PDF, TIFF, PNG (not JPEG for line art)
- Number figures sequentially: "Fig. 1", "Fig. 2", etc.
- Captions placed **below** the figure
- Captions: "Fig. X. Description of the figure." (period after number, sentence case)
- Refer to figures as "Fig. X" mid-sentence, "Figure X" at sentence start

### Figure Caption Template
```
Fig. 1. Overview of the proposed framework. The input data flows through
the feature extraction module, followed by the attention-based classifier.
Best viewed in color.
```

### Multi-Part Figures
- Use (a), (b), (c) labels inside the figure
- Caption: "Fig. 1. Comparison of methods. (a) Baseline. (b) Ours. (c) Ablation."
- Label each sub-figure with lowercase letter in 8 pt font

### Color Guidelines
- Ensure figures are readable in grayscale
- Use patterns/hatching in addition to color for bar charts
- IEEE allows color figures at no charge in most journals

---

## 7. Table Formatting Standards

### General Rules
- Tables numbered sequentially: "TABLE I", "TABLE II", etc.
- Roman numerals for table numbers
- Title placed **above** the table
- Title: "TABLE I: Description of the table." (colon after number)
- Horizontal rules only (no vertical rules)
- Three rules: top, below header, bottom
- Use `\hline` in LaTeX

### Table Template
```
TABLE I: PERFORMANCE COMPARISON ON BENCHMARK DATASETS

| Method        | Accuracy (%) | F1 Score | Time (s) |
|---------------|-------------|----------|----------|
| Baseline [3]  | 85.2        | 0.841    | 12.3     |
| Method A [7]  | 87.6        | 0.869    | 15.7     |
| **Proposed**  | **91.3**    | **0.907**| 14.2     |
```

### Table Notes
- Use superscript symbols (†, ‡, *) for notes
- Place notes below the bottom rule
- Example: "* Results reported by original authors."

---

## 8. Mathematical Notation & Equations

### Conventions
- Number equations sequentially: (1), (2), (3), ...
- Place equation numbers flush right in parentheses
- Center equations between margins
- Use italic for variables (x, y, z), roman for functions (sin, cos, log, max)
- Bold italic for vectors (**x**), bold uppercase for matrices (**A**)
- Define every symbol at first use

### Equation Formatting
```latex
\begin{equation}
  \mathbf{y} = \mathbf{W}\mathbf{x} + \mathbf{b}
  \label{eq:linear}
\end{equation}
```

### Key LaTeX Math Commands
```latex
\usepackage{amsmath,amssymb,amsfonts}
\newcommand{\R}{\mathbb{R}}
\newcommand{\E}{\mathbb{E}}
\DeclareMathOperator*{\argmin}{arg\,min}
```

### Inline vs. Display
- Simple expressions inline: $f(x) = x^2 + 1$
- Important or complex equations: display mode with number
- Refer to equations as "Eq. (1)" mid-sentence, "Equation (1)" at sentence start

---

## 9. Algorithm & Pseudocode Formatting

Use the `algorithmic` or `algorithm2e` package:

```latex
\usepackage{algorithm}
\usepackage{algorithmic}
% or: \usepackage[ruled,vlined]{algorithm2e}

\begin{algorithm}[t]
\caption{Adaptive Gradient Descent}\label{alg:agd}
\begin{algorithmic}[1]
\REQUIRE Learning rate $\eta$, iterations $T$
\ENSURE Optimized parameters $\theta^*$
\STATE Initialize $\theta_0$ randomly
\FOR{$t = 1$ \TO $T$}
  \STATE Compute gradient: $g_t \leftarrow \nabla_\theta \mathcal{L}(\theta_{t-1})$
  \STATE Update: $\theta_t \leftarrow \theta_{t-1} - \eta \cdot g_t$
\ENDFOR
\RETURN $\theta_T$
\end{algorithmic}
\end{algorithm}
```

### Algorithm Conventions
- Place algorithm in a float: `[t]` or `[h]`
- Use small caps for keywords (REQUIRE, ENSURE, FOR, IF, etc.)
- Number lines for reference
- Keep algorithms concise; omit trivial initialization steps
- Use mathematical notation consistent with the paper

---

## 10. Reference Format (IEEE Citation Style)

### In-Text Citation
- Single reference: [1]
- Multiple references: [1], [2], [5] or [1]–[3] for consecutive
- Author mentioned: "As Smith [1] demonstrated..."
- NEVER: "In [1], the authors..." (prefer "Smith et al. [1] proposed...")

### Reference List Format

```bibtex
@article{smith2024deep,
  author  = {Smith, John A. and Doe, Jane B. and Lee, Robert C.},
  title   = {Deep Learning for Signal Processing: A Comprehensive Survey},
  journal = {IEEE Trans. Signal Process.},
  volume  = {72},
  number  = {3},
  pages   = {112--135},
  year    = {2024},
  doi     = {10.1109/TSP.2024.1234567}
}

@inproceedings{wang2024efficient,
  author    = {Wang, Li and Chen, Ming},
  title     = {Efficient Transformer Architectures for Edge Computing},
  booktitle = {Proc. IEEE Conf. Comput. Vis. Pattern Recognit. (CVPR)},
  pages     = {2345--2354},
  year      = {2024}
}

@book{jones2023optimization,
  author    = {Jones, Peter R.},
  title     = {Optimization Methods in Machine Learning},
  publisher = {Springer},
  address   = {New York, NY, USA},
  year      = {2023}
}
```

### Reference List Rules
- Number references in order of first citation
- Abbreviate journal names per IEEE standard abbreviations
- Include DOI when available
- List all authors (do NOT use "et al." in the reference list)
- Italicize journal/book titles, not article titles

---

## 11. LaTeX Template Skeleton

```latex
\documentclass[journal]{IEEEtran}
% Conference: \documentclass[conference]{IEEEtran}

\usepackage{amsmath,amssymb,amsfonts}
\usepackage{algorithmic}
\usepackage{algorithm}
\usepackage{graphicx}
\usepackage{textcomp}
\usepackage{xcolor}
\usepackage{cite}
\usepackage{url}
\usepackage{booktabs}
\usepackage{multirow}

\hyphenation{op-tical net-works semi-conduc-tor}

\begin{document}

\title{Deep Learning for Signal Processing: A Comprehensive Survey}

\author{
  \IEEEauthorblockN{First A. Author\IEEEauthorrefmark{1},
  Second B. Author\IEEEauthorrefmark{2}, and
  Third C. Author\IEEEauthorrefmark{1}}
  \IEEEauthorblockA{\IEEEauthorrefmark{1}Dept.\ of Electrical Engineering,
    University Name, City, State ZIP, USA\\
    Email: \{first.author, third.author\}@university.edu}
  \IEEEauthorblockA{\IEEEauthorrefmark{2}Dept.\ of Computer Science,
    Another University, City, Country\\
    Email: second.author@another.edu}
}

\maketitle

\begin{abstract}
  The abstract goes here. State the problem, describe the approach,
  summarize key results, and state significance. Do not cite references
  [1], [2], [3]. Avoid undefined abbreviations.
\end{abstract}

\begin{IEEEkeywords}
  deep learning, signal processing, neural networks, survey
\end{IEEEkeywords}

\section{Introduction}
\label{sec:introduction}
% Your introduction content here

\section{Related Work}
\label{sec:related}

\section{Proposed Method}
\label{sec:method}
\subsection{Problem Formulation}
\subsection{Algorithm Design}

\section{Experimental Results}
\label{sec:results}

\section{Discussion}
\label{sec:discussion}

\section{Conclusion}
\label{sec:conclusion}

\section*{Acknowledgment}
The authors would like to thank...

\bibliographystyle{IEEEtran}
\bibliography{references}

\end{document}
```

---

## 12. Word Template Guidelines

- Download the official IEEE template from [IEEE Author Center](https://ieeeauthorcenter.ieee.org/)
- Use the **IEEEtran.dot** template for Word
- Configure two-column layout: Page Layout → Columns → Two
- Set margins: Top 0.75", Bottom 1", Left/Right 0.625"
- Use Times New Roman throughout
- Title: 24 pt bold centered
- Body: 10 pt justified
- Insert column breaks before starting new sections at column tops
- Use Equation Editor for all mathematical expressions
- Embed all fonts when saving as PDF
- Use IEEE Reference Style in citation manager

---

## 13. Common IEEE Formatting Mistakes

| # | Mistake | Correction |
|---|---------|-----------|
| 1 | Using "Fig." at start of sentence | Use "Figure" at sentence start, "Fig." mid-sentence |
| 2 | "Table 1" instead of "TABLE I" | Use Roman numerals and small caps for tables |
| 3 | Forgetting to define acronyms at first use | Spell out first, then acronym in parentheses |
| 4 | Citing as "In [1]..." without author name | Prefer "Smith et al. [1] demonstrated..." |
| 5 | Using vertical lines in tables | Use only horizontal rules (three-line style) |
| 6 | Low-resolution figures | Minimum 300 dpi; use vector graphics when possible |
| 7 | Not italicizing "et al." | Always italicize: *et al.* |
| 8 | Abstract exceeding word limit | Keep to 150–250 words (check specific journal) |
| 9 | Missing page numbers in conference citations | Always include page range |
| 10 | Using JPEG for line art | Use vector (EPS/PDF) or lossless (TIFF/PNG) formats |
| 11 | Equations without numbers | Number all equations that are referenced |
| 12 | Forgetting \label{} for cross-references | Label all figures, tables, equations, sections |
| 13 | Non-IEEE bibliography style | Use `\bibliographystyle{IEEEtran}` strictly |
| 14 | Overfull hbox warnings in LaTeX | Fix line-breaking issues before submission |
| 15 | Missing DOI in references | Include DOI for all references where available |

---

## 14. Submission Checklist

### Pre-Submission
- [ ] Paper within page limit (check specific journal/conference)
- [ ] Abstract within word limit
- [ ] All figures at ≥300 dpi; vector preferred
- [ ] All tables use three-line format (no vertical rules)
- [ ] All acronyms defined at first use
- [ ] All equations referenced in text
- [ ] All figures and tables referenced in text
- [ ] References in IEEE format with complete information
- [ ] DOIs included where available
- [ ] Supplementary materials prepared (if applicable)
- [ ] No identifying information for blind review (conference)

### Formatting
- [ ] Two-column layout with correct margins
- [ ] Title 24 pt bold, centered
- [ ] Author block with affiliations and emails
- [ ] Abstract with "Abstract—" heading
- [ ] Index Terms with "Index Terms—" heading
- [ ] Section headings in Roman numerals, bold
- [ ] Figure captions below figures, table titles above tables
- [ ] Consistent mathematical notation throughout
- [ ] Algorithms properly formatted with line numbers

### Compliance
- [ ] IEEE copyright form signed (post-acceptance)
- [ ] Electronic file formatted per guidelines
- [ ] PDF checked for embedded fonts
- [ ] No copyrighted material without permission
- [ ] Data availability statement included (if required)
- [ ] Conflict of interest statement included (if required)
- [ ] Ethics approval documented (if human/animal subjects)

### Final
- [ ] Spell-checked and grammar-checked
- [ ] All authors reviewed and approved
- [ ] Cover letter prepared
- [ ] Suggested reviewers identified (if requested)
- [ ] Submit via IEEE's ScholarOne or conference system

---

## 15. Additional Resources

- **IEEE Author Center:** https://ieeeauthorcenter.ieee.org/
- **IEEE Editorial Style Manual:** Available from IEEE Author Center
- **IEEEtran LaTeX Class:** https://www.ieee.org/conferences/publishing/templates.html
- **IEEE Abbreviations:** https://ieeeauthorcenter.ieee.org/wp-content/uploads/IEEE-Editorial-Style-Manual.pdf
- **Graphics Checker Tool:** IEEE PDF eXpress (validates PDF compliance)

---

*Last updated: 2024 | CRES Template Version 1.0*
