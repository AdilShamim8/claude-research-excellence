# NeurIPS / ICML / ICLR Conference Paper Format Template

> **CRES Template — ML Conference Style**
> Covers NeurIPS (Neural Information Processing Systems), ICML (International Conference on Machine Learning), and ICLR (International Conference on Learning Representations).

---

## 1. Overview

NeurIPS, ICML, and ICLR are the premier machine learning conferences, collectively receiving 20,000+ annual submissions. All three share a common format lineage: single-column, 8.5"×11" paper with strict page limits. NeurIPS uses its own style; ICML and ICLR use variants. This template provides unified guidance with venue-specific callouts where differences exist.

---

## 2. Page Layout & Margins

| Parameter              | NeurIPS         | ICML            | ICLR            |
|------------------------|-----------------|-----------------|-----------------|
| Paper size             | Letter (8.5"×11") | Letter (8.5"×11") | Letter (8.5"×11") |
| Column count           | 1 (single)      | 1 (single)      | 1 (single)      |
| Top margin             | 0.75"           | 0.75"           | 0.75"           |
| Bottom margin          | 1"              | 1"              | 1"              |
| Left margin            | 0.625"          | 0.625"          | 0.625"          |
| Right margin           | 0.625"          | 0.625"          | 0.625"          |
| Text width             | 6.875"          | 6.875"          | 6.875"          |

### Page Limits
| Venue    | Main Text | Appendix/Supplementary | Total Submission |
|----------|-----------|------------------------|------------------|
| NeurIPS  | 9 pages   | Unlimited              | No hard total    |
| ICML     | 8 pages   | Unlimited              | No hard total    |
| ICLR     | 9 pages   | Unlimited              | No hard total    |

**Critical:** Pages beyond the main text limit can ONLY contain references, appendix, and supplementary. No main content (figures, tables, text from core sections) may appear beyond the page limit.

---

## 3. Typography

| Element                | Size      | Style                      |
|------------------------|-----------|----------------------------|
| Title                  | 18 pt     | Bold, centered             |
| Author name            | 11 pt     | Centered                   |
| Affiliation            | 10 pt     | Italic, centered           |
| Abstract heading       | 10 pt     | Bold, centered             |
| Abstract body          | 10 pt     | Italic, centered block     |
| Section heading        | 12 pt     | Bold, numbered             |
| Subsection heading     | 10 pt     | Bold, numbered (X.Y)       |
| Body text              | 10 pt     | Regular, single-column     |
| Figure caption          | 10 pt     | Regular, below figure      |
| Table title             | 10 pt     | Regular, above table       |
| References             | 9 pt      | Regular                    |

**Font:** Times Roman (NeurIPS), or as specified by the template. ICML 2024+ uses the `icml2024.sty` package.

---

## 4. Title & Author Format

### Title
- Centered, 18 pt bold
- Capitalize using Title Case
- Keep concise (recommended ≤12 words)
- Avoid "A," "An," "The" as first word
- Can include a short subtitle after a colon
- Mathematical notation in titles should be LaTeX-formatted

### Author Block
```
First Author¹    Second Author²,³    Third Author¹

¹Department of Computer Science, University of Example, City, Country
²Department of Statistics, Another University, City, Country
³Google DeepMind, City, Country

Correspondence to: first@university.edu
```

### Author Block Rules
- **Double-blind (NeurIPS/ICML):** Author names and affiliations OMITTED from submission
- **Double-blind (ICLR):** Author names and affiliations OMITTED from submission
- For camera-ready: centered, equal spacing between authors
- Affiliations in 10 pt italic below author names
- Equal contribution footnote: "Equal contribution." as footnote
- Include email for corresponding author in camera-ready

### NeurIPS Pre-Submission Format
```
\title{Title of the Paper}

% For blind submission:
\author{Anonymous}

% For camera-ready:
\author{
  First Author \\
  Department of Computer Science \\
  University of Example \\
  \texttt{first@university.edu}
  \And
  Second Author \\
  Google DeepMind \\
  \texttt{second@google.com}
}
```

---

## 5. Abstract Requirements

### Rules
- **NeurIPS:** No strict word limit; typically 150–300 words
- **ICML:** No strict word limit; typically 150–250 words
- **ICLR:** No strict word limit; typically 150–300 words
- Centered block, italic text
- Single paragraph
- No citations
- No undefined abbreviations
- Should convey: problem → approach → key result → significance

### Abstract Template
```
We present [method name], a novel approach to [problem] that
[brief description of approach]. Unlike existing methods that
[limitation of prior work], our method [key innovation]. We
[detailed approach]. Our method achieves [quantitative result]
on [benchmark], outperforming [baseline] by [margin]. We further
demonstrate [additional result]. These results suggest [broader
implication].
```

### Key Abstract Principles
- Lead with the contribution, not background
- Include at least one quantitative result
- Differentiate from prior work explicitly
- Keep accessible to the general ML audience
- Avoid overly broad claims without support

---

## 6. Section Structure

### Standard Section Order
```
1 Introduction
2 Related Work
3 Background / Preliminaries
4 Method
5 Experiments
6 Conclusion / Discussion
Acknowledgments
References
Appendix
```

### Introduction (Section 1)
The ML community has specific expectations for introductions:

1. **Opening hook** (1 paragraph): What is the problem and why does it matter?
2. **Limitation of prior work** (1 paragraph): What's wrong with existing approaches?
3. **Our contribution** (1 paragraph): What do we do differently? Be specific.
4. **Contributions list** (numbered/bulleted):
   ```
   Our main contributions are:
   • We propose [method], which [what it does]...
   • We provide theoretical analysis showing [result]...
   • We demonstrate empirically that [finding]...
   • We release code and models at [URL]...
   ```
5. **Paper organization** (1 sentence): Optional but common.

### Related Work (Section 2)
- **NeurIPS convention:** Often placed after Introduction or after Method
- **ICML convention:** Can be a separate section or integrated into Introduction
- Organize by approach family, not chronologically
- Be constructive: identify specific gaps, not just list papers
- Include a comparison table when many methods exist
- If related work is short, some papers merge with Introduction

### Background / Preliminaries (Section 3)
- Define all notation used in the paper
- Review necessary background (not exhaustive; just what's needed)
- Introduce the problem formally
- Set up mathematical framework

### Method (Section 4)
This is the core of the paper. Typical subsection structure:

```
4 Method
  4.1 Problem Formulation
  4.2 [Core Innovation Name]
  4.3 [Component/Module Name]
  4.4 Training Objective
  4.5 Theoretical Analysis (optional)
  4.6 Implementation Details (brief; full details in Appendix)
```

### Experiments (Section 5)
Critical for acceptance. Typical subsection structure:

```
5 Experiments
  5.1 Experimental Setup
    - Datasets
    - Baselines
    - Evaluation metrics
    - Implementation details (or reference to Appendix)
  5.2 Main Results
  5.3 Ablation Studies
  5.4 Analysis / Qualitative Results
```

### Conclusion / Discussion (Section 6)
- Summarize key findings concisely
- Discuss limitations honestly (reviewers value this)
- Identify future directions
- State broader impact if relevant (NeurIPS encourages this)
- Keep to 1–2 paragraphs

---

## 7. Figure & Table Formatting

### Figure Best Practices
- Single-column width: ~6.875" (full text width)
- Use vector formats (PDF, EPS) for plots and diagrams
- Use high-resolution raster (≥300 dpi) for images
- Captions below figures
- Number sequentially: Figure 1, Figure 2
- Use "Figure" or "Fig." consistently (check venue style)

### Common Figure Types in ML Papers
1. **Architecture diagrams:** Show model structure clearly
2. **Training curves:** Loss/accuracy vs. epochs
3. **Performance comparison charts:** Bar charts or tables
4. **Qualitative results:** Example outputs, attention maps, visualizations
5. **Ablation plots:** Showing effect of hyperparameters

### Table Format
- Tables are the primary way to report numerical results
- Bold the best result in each column
- Underline the second-best (optional)
- Include ± standard deviation where applicable
- Use `booktabs` package (three-line style)

### Standard Results Table Template
```
Table 1: Comparison with state-of-the-art methods on benchmark datasets.

Method               CIFAR-10     CIFAR-100    ImageNet     Params (M)
───────────────────────────────────────────────────────────────────
ResNet-50 [1]        93.6 ± 0.2   74.8 ± 0.3   76.1 ± 0.1    25.6
ViT-B/16 [2]         98.1 ± 0.1   87.1 ± 0.2   81.8 ± 0.1    86.6
Swin-B [3]           97.3 ± 0.1   85.4 ± 0.2   83.5 ± 0.1    88.0
───────────────────────────────────────────────────────────────────
Ours                  98.7 ± 0.1   89.2 ± 0.1   84.3 ± 0.1    62.4
───────────────────────────────────────────────────────────────────
```

### Ablation Table Template
```
Table 2: Ablation study on [dataset]. Each row removes one component.

Configuration                        Accuracy (%)    Δ
──────────────────────────────────────────────────────
Full model                            89.2           —
  w/o attention module                86.1          -3.1
  w/o pre-training                    84.7          -4.5
  w/o data augmentation               87.3          -1.9
──────────────────────────────────────────────────────
```

---

## 8. Mathematical Notation Standards

### Notation Conventions
| Symbol Type          | Convention               | Example          |
|----------------------|--------------------------|------------------|
| Scalars              | Lowercase italic         | $x, y, z, \alpha$|
| Vectors              | Lowercase bold           | $\mathbf{x}$     |
| Matrices             | Uppercase bold           | $\mathbf{W}$     |
| Sets                 | Uppercase calligraphic   | $\mathcal{S}$    |
| Distributions        | Uppercase calligraphic   | $\mathcal{N}$    |
| Functions            | Lowercase roman/italic   | $f(x), g(\theta)$|
| Operators            | Uppercase roman          | $\mathbb{E}, \mathbb{P}$|
| Loss functions       | Calligraphic             | $\mathcal{L}$    |
| Random variables     | Uppercase italic         | $X, Y, Z$        |
| Estimates            | Hat accent              | $\hat{y}, \hat{\theta}$|

### Key LaTeX Commands
```latex
\usepackage{amsmath,amssymb,amsfonts,mathtools}

% Common definitions
\newcommand{\R}{\mathbb{R}}
\newcommand{\E}{\mathbb{E}}
\newcommand{\Prob}{\mathbb{P}}
\newcommand{\bx}{\mathbf{x}}
\newcommand{\bW}{\mathbf{W}}
\DeclareMathOperator*{\argmin}{arg\,min}
\DeclareMathOperator*{\argmax}{arg\,max}

% Common expressions
\mathcal{L}(\theta)                              % Loss
\nabla_\theta \mathcal{L}(\theta)                % Gradient
\mathbb{E}_{x \sim p_{\text{data}}} [f(x)]      % Expectation
\min_\theta \mathbb{E}[\mathcal{L}(\theta)]      % Objective
```

### Equation Formatting
```latex
\begin{equation}
  \mathcal{L}(\theta) = \mathbb{E}_{(x,y) \sim \mathcal{D}}
  \left[ \ell\left(f_\theta(x), y\right) \right]
  + \lambda \|\theta\|_2^2
  \label{eq:objective}
\end{equation}
```

- Number all referenced equations
- Use `\label{eq:name}` for cross-referencing
- Refer as "Equation (1)" or "Eq.~(\ref{eq:objective})"
- Align multi-line equations with `\begin{align}`

---

## 9. Algorithm & Pseudocode Formatting

### Using algorithm2e (Preferred)
```latex
\usepackage[ruled,vlined,linesnumbered]{algorithm2e}

\begin{algorithm}[t]
\caption{Contrastive Learning with Adaptive Margin}\label{alg:clam}
\KwIn{Dataset $\mathcal{D}$, learning rate $\eta$, epochs $T$}
\KwOut{Trained encoder $f_\theta$}
Initialize encoder parameters $\theta$ randomly\;
\For{$t \leftarrow 1$ \KwTo $T$}{
  Sample mini-batch $\{x_i\}_{i=1}^B$ from $\mathcal{D}$\;
  Generate augmented views $\tilde{x}_i^{(1)}, \tilde{x}_i^{(2)}$
    for each $x_i$\;
  Compute embeddings $z_i^{(k)} = f_\theta(\tilde{x}_i^{(k)})$
    for $k \in \{1,2\}$\;
  Compute contrastive loss $\mathcal{L}_{\text{con}}$ via
    Eq.~(\ref{eq:conloss})\;
  Update $\theta \leftarrow \theta - \eta \nabla_\theta
    \mathcal{L}_{\text{con}}$\;
}
\Return $f_\theta$
\end{algorithm}
```

### Using algorithmic
```latex
\usepackage{algorithm}
\usepackage{algorithmic}

\begin{algorithm}[t]
\caption{Contrastive Learning with Adaptive Margin}
\label{alg:clam}
\begin{algorithmic}[1]
\REQUIRE Dataset $\mathcal{D}$, learning rate $\eta$
\ENSURE Trained encoder $f_\theta$
\STATE Initialize $\theta$ randomly
\FOR{epoch $= 1$ to $T$}
  \STATE Sample mini-batch $\{x_i\}_{i=1}^B$
  \STATE Compute contrastive loss $\mathcal{L}_{\text{con}}$
  \STATE $\theta \leftarrow \theta - \eta \nabla_\theta \mathcal{L}_{\text{con}}$
\ENDFOR
\RETURN $f_\theta$
\end{algorithmic}
\end{algorithm}
```

### Algorithm Conventions
- Keep algorithms concise and high-level
- Move implementation details to Appendix
- Use mathematical notation consistent with the paper
- Include complexity analysis when relevant
- Number lines for reference

---

## 10. Reference Format

### In-Text Citation
- Author-year style: "(Smith et al., 2024)" or "Smith et al. (2024)"
- Multiple: "(Smith et al., 2024; Wang & Lee, 2023)"
- Numbered style: [1], [2] (check specific venue year)

### Bibliography Entry Examples
```bibtex
@inproceedings{smith2024contrastive,
  title     = {Contrastive Learning with Adaptive Margins},
  author    = {Smith, John A. and Doe, Jane B.},
  booktitle = {Advances in Neural Information Processing Systems},
  volume    = {37},
  pages     = {1234--1246},
  year      = {2024}
}

@inproceedings{wang2024efficient,
  title     = {Efficient Transformer Architectures},
  author    = {Wang, Li and Chen, Ming},
  booktitle = {Proceedings of the 41st International Conference on
               Machine Learning},
  series    = {ICML'24},
  year      = {2024}
}

@article{lee2023diffusion,
  title   = {Diffusion Models for Image Generation: A Survey},
  author  = {Lee, Robert C. and Garcia, Maria},
  journal = {Journal of Machine Learning Research},
  volume  = {24},
  number  = {1},
  pages   = {1--45},
  year    = {2023}
}
```

---

## 11. Supplementary Material Guidelines

### What Goes in Supplementary / Appendix
- Detailed proofs and derivations
- Additional experimental results
- Extended ablation studies
- Implementation details (hyperparameters, training setup)
- Additional visualizations
- Dataset details and statistics
- Broader impact statement (NeurIPS)

### Appendix Structure
```latex
\appendix
\section{Proof of Theorem 1}
\label{sec:proof}

\section{Additional Experimental Results}
\label{sec:addl_results}

\section{Implementation Details}
\label{sec:implementation}
\subsection{Hyperparameters}
\subsection{Training Details}
\subsection{Compute Resources}

\section{Extended Related Work}
\label{sec:ext_related}

\section{Broader Impact}
\label{sec:impact}
```

### Supplementary Material Rules
- Must be self-contained and readable
- Numbered separately: "Appendix A," "Appendix B" or "Section A.1"
- Figures numbered: "Figure 5," "Figure 6" (continuing from main text)
- Tables numbered: "Table 3," "Table 4" (continuing from main text)
- Equations numbered: continuing or (S1), (S2) style
- Cross-references from main text encouraged: "see Appendix A"
- NeurIPS: Broader Impact statement encouraged (check current year's policy)

---

## 12. Double-Blind Review Requirements

All three venues enforce double-blind review:

### Anonymization Rules
- [ ] Remove ALL author names and affiliations from title page
- [ ] Replace with "Anonymous" or leave blank per template
- [ ] Remove acknowledgments (or replace with "Acknowledgments removed for blind review")
- [ ] Anonymize self-citations:
  - "In our previous work (Smith et al., 2024)..." → "Smith et al. (2024)..."
  - Do NOT say "our previous work" or "we previously showed"
- [ ] Remove URLs to personal pages or code repositories with identifying info
- [ ] Remove identifying information from PDF metadata/properties
- [ ] Use third person for all self-references
- [ ] Do not include ORCID IDs in submission
- [ ] If citing simultaneously-submitted work, use "Anonymous (2024)" format

### What Is Allowed
- Citing your own published work (in third person)
- Referring to your code repository IF it is already public and not identifying
- Mentioning that code will be released upon acceptance

### What Is NOT Allowed
- Any form of "our previous work" or "we previously demonstrated"
- Author names in the paper
- Acknowledgments naming specific people or grants
- File names containing author names
- Links to non-anonymized repositories

---

## 13. LaTeX Template Skeleton (NeurIPS)

```latex
\documentclass{article}
\usepackage{neurips_2024}

\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{hyperref}
\usepackage{url}
\usepackage{booktabs}
\usepackage{amsfonts}
\usepackage{amsmath}
\usepackage{nicefilelist}
\usepackage{algorithm}
\usepackage{algorithmic}
\usepackage{graphicx}
\usepackage{subcaption}

\title{Contrastive Learning with Adaptive Margins}

% For blind submission:
\author{Anonymous}

% For camera-ready:
% \author{
%   John A. Smith \\
%   Department of Computer Science \\
%   University of Example \\
%   \texttt{smith@university.edu}
%   \And
%   Jane B. Doe \\
%   Google DeepMind \\
%   \texttt{doe@google.com}
% }

\begin{document}

\maketitle

\begin{abstract}
  We present a novel contrastive learning framework with adaptive
  margins that dynamically adjusts the separation between positive
  and negative pairs. Our method achieves state-of-the-art performance
  on three benchmarks, outperforming SimCLR by 3.2% on ImageNet
  linear evaluation.
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
\subsection{Training Procedure}

\section{Experiments}
\label{sec:experiments}
\subsection{Setup}
\subsection{Main Results}
\subsection{Ablation Studies}
\subsection{Analysis}

\section{Conclusion}
\label{sec:conclusion}

% For blind submission, remove or anonymize:
% \section*{Acknowledgments}
% This work was supported by...

\bibliography{references}
\bibliographystyle{plainnat}

% Appendix starts here (does not count toward page limit)
\newpage
\appendix
\section{Proof of Theorem 1}
\section{Additional Results}
\section{Implementation Details}

\end{document}
```

### ICML LaTeX Template
```latex
\documentclass{article}
\usepackage{icml2024}

% Same package imports as NeurIPS above

\icmltitle{Contrastive Learning with Adaptive Margins}

\icmlauthor{Anonymous}{}
% Camera-ready:
% \icmlauthor{John A. Smith}{university}
% \icmlauthor{Jane B. Doe}{deepmind}
% \icmlaffiliation{university}{Department of CS, University of Example}
% \icmlaffiliation{deepmind}{Google DeepMind}

\begin{document}
\maketitle
% ... rest follows same structure as NeurIPS
\end{document}
```

---

## 14. Common ML Conference Formatting Mistakes

| # | Mistake | Correction |
|---|---------|-----------|
| 1 | Main content beyond page limit | Only appendix/references after page 9 (or 8 for ICML) |
| 2 | Not anonymizing for double-blind | Remove ALL identifying information |
| 3 | Self-citing as "our previous work" | Use third person: "Smith et al. (2024)" |
| 4 | Missing ablation studies | Reviewers expect thorough ablations |
| 5 | No error bars / standard deviations | Report variance across runs |
| 6 | Tables without bold best results | Bold the best; underline second-best |
| 7 | Vague contribution list | Be specific: "We propose X which achieves Y" |
| 8 | Missing compute / resource details | Report GPU hours, hardware, training time |
| 9 | Overclaiming without evidence | "State-of-the-art" only with comprehensive comparison |
| 10 | Not releasing code | Strongly expected; at minimum, promise in paper |
| 11 | Ignoring limitations section | Reviewers actively look for this |
| 12 | Using multiple citation styles | Be consistent: author-year OR numbered, not mixed |
| 13 | Figure text too small | Minimum 8 pt in figures at print size |
| 14 | Not cross-referencing appendix | Every appendix section should be cited from main text |
| 15 | Missing related work comparisons | Must compare with concurrent/recent methods |

---

## 15. Submission Checklist

### Content Completeness
- [ ] Main text within page limit (9 NeurIPS, 8 ICML, 9 ICLR)
- [ ] Contributions explicitly enumerated in Introduction
- [ ] All methods described with sufficient detail
- [ ] Experiments include: main results, ablations, analysis
- [ ] All baselines are recent and appropriate
- [ ] Statistical significance reported (±std, multiple seeds)
- [ ] Limitations discussed
- [ ] Compute resources documented

### Double-Blind Compliance
- [ ] Author names and affiliations removed
- [ ] Self-citations in third person
- [ ] Acknowledgments anonymized
- [ ] No identifying URLs or repositories
- [ ] PDF metadata stripped of author info
- [ ] No "our previous work" phrasing

### Formatting
- [ ] Correct template version for venue and year
- [ ] Single-column layout
- [ ] Figures high-resolution (vector preferred)
- [ ] Tables use booktabs style
- [ ] Algorithms properly formatted
- [ ] Mathematical notation consistent throughout
- [ ] All figures/tables/equations referenced in text

### Supplementary Materials
- [ ] Proofs complete and readable
- [ ] Additional results included
- [ ] Implementation details provided
- [ ] Hyperparameter tables included
- [ ] Broader impact statement (NeurIPS, if required)
- [ ] Code repository prepared (or promised)

### Final
- [ ] Spell-checked and proofread
- [ ] All authors reviewed and approved
- [ ] Supplementary PDF compiled correctly
- [ ] Submit via OpenReview (ICLR, NeurIPS) or CMT (ICML)
- [ ] No deadline extensions missed
- [ ] Supplementary files uploaded in correct format

---

## 16. Venue-Specific Notes

### NeurIPS Specifics
- Datasets track available (separate review criteria)
- Broader impact statement encouraged (check annual policy)
- Supplementary: single PDF + separate code ZIP
- Two round review process (initial + rebuttal)
- Poster/oral decision after rebuttal

### ICML Specifics
- Often has both conference and workshop tracks
- Strong emphasis on theoretical contributions alongside empirical
- Supplementary: single PDF preferred
- Rebuttal period typically 7 days
- awards for outstanding papers

### ICLR Specifics
- Open review from the start (publicly visible)
- No page limit on supplementary (same as others)
- Strong culture of reproducibility and open code
- Poster/spotlight/oral decisions
- Focus on representation learning

---

## 17. Additional Resources

- **NeurIPS Author Instructions:** https://neurips.cc/Conferences/2024/AuthorInstructions
- **ICML Author Instructions:** https://icml.cc/Conferences/2024/AuthorInstructions
- **ICLR Author Instructions:** https://iclr.cc/Conferences/2024/AuthorInstructions
- **NeurIPS LaTeX Template:** https://github.com/neurips-ai/neurips-2024-latex-template
- **ICML LaTeX Template:** Available from ICML website
- **Mathematical Typesetting Guide:** https://arxiv.org/help/jref#math

---

*Last updated: 2024 | CRES Template Version 1.0*
