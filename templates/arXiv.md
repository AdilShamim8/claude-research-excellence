# arXiv Preprint Format Template

> **CRES Template — arXiv Style**
> Covers arXiv.org preprint formatting, submission, and best practices across all subject areas.

---

## 1. Overview

arXiv is the world's largest open-access preprint repository, hosting over 2.4 million articles across physics, mathematics, computer science, quantitative biology, quantitative finance, statistics, electrical engineering, systems science, and economics. Unlike journals, arXiv has no peer review, no page limits, and no strict formatting requirements beyond basic PDF compilation. However, following best practices ensures your preprint is professional, discoverable, and taken seriously by the research community.

---

## 2. Article Structure

### Flexibility with Responsibility
arXiv imposes minimal structural requirements. However, adopting conventional academic structure improves readability and credibility:

```
Title
Authors & Affiliations
Abstract
1 Introduction
2 Related Work (optional)
3 Background / Preliminaries
4 Method / Main Contribution
5 Experiments / Results / Analysis
6 Discussion
7 Conclusion
Acknowledgments
References
Appendix (if any)
```

### Key Structural Notes
- Section numbering is standard and expected
- Subsections and sub-subsections are fine
- Appendices are common and encouraged for supplementary material
- No word or page limits exist
- Methods can be integrated with results or placed separately
- Theoretical and experimental sections can be interleaved

---

## 3. Title & Author Format

### Title
- No length restriction, but brevity is valued (recommended ≤15 words)
- Mathematical notation in titles is allowed but discouraged for discoverability
- Avoid ALL-CAPS titles
- Use Title Case or Sentence case consistently
- Can include subtitle after colon
- Include key search terms for discoverability

### Title Examples
```
✅ Good:  "Diffusion Models for Image Generation: A Comprehensive Survey"
✅ Good:  "On the convergence of stochastic gradient descent with adaptive learning rates"
❌ Avoid: "A STUDY ON THE USE OF DEEP LEARNING FOR..."
❌ Avoid: "$\mathcal{O}(n \log n)$ algorithm for..." (math in title hurts search)
```

### Author Block
```
John A. Smith¹, Jane B. Doe²,³, Robert C. Lee¹

¹Department of Computer Science, University of Example, Cambridge, UK
²Department of Statistics, Stanford University, Stanford, CA, USA
³Google DeepMind, London, UK

Corresponding author: j.smith@university.edu
```

### Author Block with ORCID (Recommended)
```latex
\author{
  John A. Smith\orcidlink{0000-0001-2345-6789}$^{1}$,
  Jane B. Doe\orcidlink{0000-0002-3456-7890}$^{2,3}$, and
  Robert C. Lee$^{1}$
}
```

### Author Block Rules
- Full names preferred (not just initials)
- Affiliations with superscript numbers
- Multiple affiliations comma-separated
- Corresponding author marked with asterisk or note
- ORCID IDs strongly recommended (improves discoverability)
- Equal contribution noted as footnote
- Deceased authors noted as footnote
- Group/consortium names included with member list in appendix

### arXiv-Specific: Collaboration Author Lists
- Large collaborations (e.g., LHC, SKA): use collaboration name as author
- Full member list can be in appendix
- Use `\collaboration` macro if available in your field's template

---

## 4. Abstract Requirements

### Rules
- No word limit, but 150–300 words is standard
- Must be a single paragraph
- No citations or footnote markers
- No undefined abbreviations
- Should work as a standalone summary
- Appears in search results — make it count for discoverability

### Abstract Best Practices
```
[Context and motivation, 1–2 sentences]. [Problem statement, 1 sentence].
[Approach, 1–2 sentences]. [Key results with quantitative details, 2–3
sentences]. [Significance and implications, 1 sentence].
```

### arXiv-Specific Abstract Considerations
- The abstract is indexed by search engines (Google Scholar, Semantic Scholar)
- Include key terms naturally in the abstract for discoverability
- Avoid LaTeX macros in the abstract (they may not render in metadata)
- The abstract appears on the arXiv listing page — it is your "advertisement"
- Include methodology keywords: "deep learning," "variational inference," etc.

---

## 5. Section Structure (Flexible)

While arXiv is flexible, following conventional academic structure is recommended:

### For Empirical/Experimental Papers
```
1 Introduction
2 Related Work
3 Background
4 Method
  4.1 Problem Formulation
  4.2 [Core Method]
  4.3 [Analysis/Theory]
5 Experiments
  5.1 Setup
  5.2 Main Results
  5.3 Ablation Studies
  5.4 Qualitative Analysis
6 Discussion & Limitations
7 Conclusion
```

### For Theoretical Papers
```
1 Introduction
2 Related Work
3 Preliminaries
4 Main Results
  4.1 Theorem 1 and Proof
  4.2 Theorem 2 and Proof
5 Discussion
6 Conclusion
Appendix: Full proofs
```

### For Survey Papers
```
1 Introduction
2 Background
3–N [Thematic survey sections]
N+1 Open Problems and Future Directions
N+2 Conclusion
```

---

## 6. Figure & Table Formatting

### General Guidelines
- No strict format requirements, but follow your target journal's style
- Use vector formats (PDF, EPS) when possible
- Raster images at ≥300 dpi
- Captions below figures, titles above tables
- Numbered sequentially
- Consistent font sizes across all figures (minimum 8 pt)
- Ensure readability when printed on A4 or Letter

### arXiv-Specific Figure Considerations
- arXiv compiles your LaTeX → figures must be in the source bundle
- Use `\includegraphics{filename}` with relative paths
- Supported formats: PDF, PNG, JPG, EPS
- Do NOT use absolute file paths
- Large figures can slow compilation — optimize file sizes
- Consider using `\graphicspath{{figures/}}` for organization

### Recommended Figure Organization
```
paper/
├── main.tex
├── references.bib
├── figures/
│   ├── fig1_architecture.pdf
│   ├── fig2_results.pdf
│   ├── fig3_qualitative.png
│   └── fig4_ablation.pdf
└── sections/
    ├── intro.tex
    ├── method.tex
    └── experiments.tex
```

---

## 7. Reference Format

### Flexibility
arXiv does not enforce a specific citation style. Choose one consistent style:

- **Author-year:** (Smith et al., 2024) — common in ML, NLP, AI
- **Numbered:** [1], [2], [3] — common in physics, math, engineering
- **Specific journal style** — if targeting a particular journal

### arXiv-Specific Citation Best Practices
- Always include arXiv IDs for preprints: `arXiv:2401.12345`
- Use the `biblatex` or `natbib` package
- Cite the published version when available (not just the arXiv preprint)
- Include DOIs when available

### arXiv Citation Entry
```bibtex
@article{smith2024contrastive,
  title         = {Contrastive Learning with Adaptive Margins},
  author        = {Smith, John A. and Doe, Jane B.},
  year          = {2024},
  eprint        = {2401.12345},
  archivePrefix = {arXiv},
  primaryClass  = {cs.LG},
  url           = {https://arxiv.org/abs/2401.12345}
}
```

### Citing arXiv Preprints
```bibtex
% Preferred format (when no published version exists):
@article{wang2024efficient,
  title         = {Efficient Transformer Architectures},
  author        = {Wang, Li and Chen, Ming},
  year          = {2024},
  eprint        = {2402.54321},
  archivePrefix = {arXiv},
  primaryClass  = {cs.CL}
}

% When published version exists:
@inproceedings{vaswani2017attention,
  title     = {Attention Is All You Need},
  author    = {Vaswani, Ashish and others},
  booktitle = {Advances in Neural Information Processing Systems},
  volume    = {30},
  year      = {2017},
  eprint    = {1706.03762},
  archivePrefix = {arXiv}
}
```

---

## 8. LaTeX Template for arXiv Submission

```latex
\documentclass{article}

% --- arXiv-style packages ---
\usepackage{arXiv}  % Optional: community-maintained arXiv style
% Or use standard article class with the following:

\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{hyperref}
\usepackage{url}
\usepackage{booktabs}
\usepackage{amsfonts}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{graphicx}
\usepackage{algorithm}
\usepackage{algorithmic}
\usepackage{subcaption}
\usepackage{natbib}
\usepackage{microtype}      % Better typography
\usepackage{cleveref}        % Smart cross-references
\usepackage{orcidlink}       % ORCID symbols

% --- Custom commands ---
\newcommand{\R}{\mathbb{R}}
\newcommand{\E}{\mathbb{E}}
\DeclareMathOperator*{\argmin}{arg\,min}

% --- Theorem environments ---
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{proposition}[theorem]{Proposition}
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{definition}[theorem]{Definition}
\newtheorem{remark}[theorem]{Remark}

% --- Metadata ---
\title{Contrastive Learning with Adaptive Margins:\\
A Unified Framework}

\author{
  John A. Smith\orcidlink{0000-0001-2345-6789}$^{1}$ \and
  Jane B. Doe\orcidlink{0000-0002-3456-7890}$^{2,3}$ \and
  Robert C. Lee$^{1}$ \\
  \\
  $^{1}$Department of Computer Science, University of Cambridge,
  Cambridge, UK \\
  $^{2}$Department of Statistics, Stanford University, Stanford, CA, USA \\
  $^{3}$Google DeepMind, London, UK \\
  \\
  Correspondence: \texttt{j.smith@cam.ac.uk}
}

\begin{document}

\maketitle

\begin{abstract}
  We present a novel contrastive learning framework with adaptive
  margins that dynamically adjusts the separation between positive
  and negative pairs based on sample difficulty. Unlike existing
  methods that use fixed margins, our approach learns instance-specific
  margins through a lightweight auxiliary network. We prove that our
  adaptive margin loss is a tighter bound on the classification error
  than fixed-margin alternatives. On ImageNet linear evaluation, our
  method achieves 79.3\% top-1 accuracy, outperforming SimCLR by 3.2\%
  and BYOL by 1.1\%, while requiring 30\% fewer training epochs.
  Code is available at \url{https://github.com/smithlab/clam}.
\end{abstract}

\section{Introduction}
\label{sec:intro}

\section{Related Work}
\label{sec:related}

\section{Background}
\label{sec:background}

\section{Method}
\label{sec:method}
\subsection{Problem Formulation}
\subsection{Adaptive Margin Contrastive Loss}
\subsection{Theoretical Analysis}
\subsection{Training Procedure}

\section{Experiments}
\label{sec:experiments}
\subsection{Setup}
\subsection{Main Results}
\subsection{Ablation Studies}
\subsection{Qualitative Analysis}

\section{Discussion \& Limitations}
\label{sec:discussion}

\section{Conclusion}
\label{sec:conclusion}

\section*{Acknowledgments}
This work was supported by EPSRC Grant EP/X01234/1. We thank
the anonymous reviewers for their constructive feedback.

\bibliographystyle{plainnat}
\bibliography{references}

% --- Appendix ---
\newpage
\appendix
\section{Proof of Theorem 1}
\label{sec:proof}

\section{Additional Experimental Results}
\label{sec:addl}

\section{Implementation Details}
\label{sec:impl}

\end{document}
```

### Community arXiv Style
The `arXiv.sty` package (https://github.com/kourgeorge/arxiv-style) provides a polished look:

```latex
\documentclass{article}
\usepackage{arXiv}
% Automatically sets up clean formatting, hyperref, etc.
```

---

## 9. Subject Category Selection Guide

Choosing the right primary and cross-list categories is crucial for discoverability.

### Primary Category
- Select the SINGLE most relevant category
- This determines which mailing lists your preprint appears on
- This determines the daily announcement section

### Cross-List Categories
- Select up to additional relevant categories
- Your preprint appears in these sections too
- Do NOT spam irrelevant categories (moderators may reject)

### Common Category Choices by Field

| Field               | Primary Category        | Common Cross-lists          |
|---------------------|-------------------------|-----------------------------|
| Deep Learning       | cs.LG                   | cs.CV, cs.AI, stat.ML       |
| Computer Vision     | cs.CV                   | cs.LG, cs.AI                |
| NLP                 | cs.CL                   | cs.LG, cs.AI                |
| Robotics            | cs.RO                   | cs.LG, cs.AI                |
| Reinforcement Learning | cs.LG               | cs.AI, stat.ML              |
| Theoretical ML      | stat.ML                 | cs.LG, math.ST              |
| Quantum Computing   | quant-ph                | cs.ET, physics.comp-ph      |
| Statistics          | math.ST or stat.ML      | stat.CO, cs.LG              |
| Applied Math        | math.NA                 | cs.NA, physics.comp-ph      |
| Computational Bio   | q-bio.QM               | cs.LG, stat.AP              |
| Physics (HEP)       | hep-ph or hep-th        | hep-ex, gr-qc               |
| Condensed Matter    | cond-mat.str-el         | cond-mat.mtrl-sci           |

### Full Category List
- **cs:** Computer Science (AI, CL, CV, LG, RO, CR, etc.)
- **math:** Mathematics (ST, NA, PR, CO, etc.)
- **stat:** Statistics (ML, AP, CO, ME, TH)
- **physics:** All physics sub-fields
- **q-bio:** Quantitative Biology
- **q-fin:** Quantitative Finance
- **eess:** Electrical Engineering and Systems Science
- **econ:** Economics

---

## 10. Version Management

arXiv supports versioning — each submission creates a new version (v1, v2, v3, ...).

### Version Strategy
- **v1:** Initial submission (often concurrent with conference submission)
- **v2:** Post-rebuttal updates, typo fixes, added experiments
- **v3:** Camera-ready version (after acceptance)
- **v4+:** Bug fixes, additional references, corrected errors

### Best Practices
- **Always link to the latest version** in communications: `arxiv.org/abs/2401.12345` (defaults to latest)
- **Link to a specific version** when referencing: `arxiv.org/abs/2401.12345v2`
- **Add a comment** for each version explaining changes:
  - v1: "Submitted to NeurIPS 2024"
  - v2: "Updated with additional experiments and corrected typos"
  - v3: "Accepted to NeurIPS 2024. Camera-ready version"
- **Do NOT delete previous versions** — they remain accessible permanently
- **Update the DOI** if the paper is published in a journal

### Timeline Considerations
- Submit to arXiv BEFORE or simultaneously with conference submission (check venue policy)
- Some venues allow arXiv posting during review (NeurIPS, ICML, ICLR)
- Some venues do NOT allow it (check each venue's policy)
- Journal policies vary: Nature/Science generally allow arXiv; some do not

### Updating Existing Versions
```bash
# arXiv submission update process:
1. Log in to arXiv.org
2. Click "Replace" on your submission
3. Upload new source files
4. Add version comment
5. Preview and confirm
6. New version appears within ~24 hours
```

---

## 11. Supplementary Material Handling

### Options for Supplementary Material

1. **Include in the same PDF** (simplest, most common)
   - Appendices after references
   - No size limit on arXiv
   - Single file for everything

2. **Separate ancillary files** (for code, data)
   - Upload as `.zip`, `.tar.gz`, or individual files
   - Linked from the paper
   - Available from the arXiv page under "Other Formats"

3. **External repositories** (for large datasets/code)
   - GitHub, Zenodo, Figshare, OSF
   - Include URL in the paper
   - Consider Zenodo DOI for long-term preservation

### Code Submission
```latex
% In the paper:
\section*{Code and Data Availability}
Source code is available at \url{https://github.com/smithlab/clam}.
Pre-trained models and datasets are available at
\url{https://zenodo.org/record/1234567}.
```

### Large Files
- arXiv has a 10 MB source file limit per submission
- If your submission exceeds this:
  - Optimize image sizes (use vector, compress raster)
  - Split very large figures into smaller files
  - Use `\externaldocument` for multi-file papers
  - Request an exception for very large submissions

---

## 12. Common arXiv Formatting Mistakes

| # | Mistake | Correction |
|---|---------|-----------|
| 1 | Missing arXiv IDs in citations | Include `eprint` and `archivePrefix` fields |
| 2 | Broken figures in compiled PDF | Use relative paths; include all figure files |
| 3 | Wrong primary category | Choose the most specific, relevant category |
| 4 | No version comments | Add descriptive comments for each update |
| 5 | Forgetting to update after acceptance | Post camera-ready as new version |
| 6 | Including proprietary fonts | Use standard LaTeX fonts or embed fonts |
| 7 | Source files too large (>10 MB) | Optimize images; request exception if needed |
| 8 | Not including ORCID | Add ORCID IDs for all authors |
| 9 | Abstract with LaTeX macros | Keep abstract simple; macros may break in metadata |
| 10 | Missing related work citations | Include all relevant prior art |
| 11 | Not linking to published version | Add journal reference in metadata when published |
| 12 | Uploading PDF only | Upload LaTeX source for better archiving |
| 13 | Using non-standard packages | Stick to common CTAN packages |
| 14 | No line numbers in source | Add line numbers for reviewer convenience |
| 15 | Ignoring compilation warnings | Fix overfull hboxes and missing references |

---

## 13. Submission Checklist

### Pre-Submission Content
- [ ] Title is descriptive and search-friendly
- [ ] Abstract is clear, self-contained, and keyword-rich
- [ ] All figures included in source bundle
- [ ] References include arXiv IDs for preprints
- [ ] ORCID IDs added for all authors
- [ ] Code repository linked (if applicable)
- [ ] All authors approve the preprint

### Formatting
- [ ] LaTeX compiles without errors
- [ ] All figures render correctly
- [ ] No missing bibliography entries
- [ ] PDF looks correct on screen and in print
- [ ] File size under 10 MB (or exception requested)
- [ ] Standard LaTeX packages used (available on CTAN)
- [ ] No absolute file paths in `\includegraphics`

### arXiv-Specific
- [ ] Primary category selected correctly
- [ ] Cross-list categories are relevant
- [ ] Version comment added (for updates)
- [ ] License selected (default: CC BY 4.0, or arXiv.org perpetual)
- [ ] DOI reserved (optional but recommended)
- [ ] Submit source files (not just PDF) for better archiving
- [ ] Preview the compiled PDF before finalizing

### After Submission
- [ ] Verify the compiled PDF on arXiv
- [ ] Check all figures rendered correctly
- [ ] Confirm metadata (title, authors, abstract)
- [ ] Share the arXiv link: `arxiv.org/abs/2401.12345`
- [ ] Update when accepted to a venue (add comment + version)
- [ ] Add published DOI when available

---

## 14. arXiv Submission Process

### Step-by-Step
1. **Register** an arXiv account (requires endorsement for new users)
2. **Start a new submission** at https://arxiv.org/submit
3. **Select subject category** (primary + cross-lists)
4. **Upload source files** (LaTeX, figures, bibliography)
5. **Verify metadata** (title, authors, abstract)
6. **Preview compiled PDF** (check carefully)
7. **Select license** (CC BY 4.0 recommended)
8. **Submit** — enters moderation queue
9. **Wait for announcement** — typically posted within 24–48 hours
10. **Verify** — check the public page for errors

### Endorsement (New Users)
- New submitters need endorsement from existing arXiv users
- Request endorsement from colleagues in your field
- Endorsers must have a track record in the relevant category
- Alternative: submit through institutional proxies

### Moderation
- arXiv moderators check for appropriateness (not quality)
- Common rejection reasons: off-topic, excessive length, spam, plagiarism
- Moderation typically takes 1–2 business days
- Appeals are possible through the arXiv support system

---

## 15. Additional Resources

- **arXiv Submit:** https://arxiv.org/submit
- **arXiv Author Help:** https://arxiv.org/help/submit
- **arXiv LaTeX Best Practices:** https://arxiv.org/help/submit_latex_best_practices
- **arXiv Category List:** https://arxiv.org/category_taxonomy
- **arXiv License Options:** https://arxiv.org/help/license
- **Community arXiv Style:** https://github.com/kourgeorge/arxiv-style
- **arXiv Vanity (HTML rendering):** https://www.arxiv-vanity.com/

---

*Last updated: 2024 | CRES Template Version 1.0*
