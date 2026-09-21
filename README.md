# CLAUDE RESEARCH EXCELLENCE SYSTEM (CRES)

<p align="center">
  <img src="https://img.shields.io/badge/Release-v2.4%20(September%202026)-0052CC?style=for-the-badge&logo=git&logoColor=white" alt="Release Version" />
  <img src="https://img.shields.io/badge/System-ARIA%20v3.1-4B0082?style=for-the-badge&logo=openai&logoColor=white" alt="ARIA v3.1" />
  <img src="https://img.shields.io/badge/License-MIT-28A745?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="MIT License" />
  <img src="https://img.shields.io/badge/Compatibility-Claude%203.5%20%7C%203.7%20%7C%204-D97706?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Compatibility" />
  <img src="https://img.shields.io/badge/Provenance-Empirical%20DOIs%20%26%20Real%20Data-10B981?style=for-the-badge&logo=google-scholar&logoColor=white" alt="Empirical Data Provenance" />
  <img src="https://img.shields.io/badge/Evaluators-4%20Quantitative%20Engines-7C3AED?style=for-the-badge&logo=speedtest&logoColor=white" alt="4 Evaluators" />
</p>

> **The world's most advanced AI-powered research paper creation framework — engineered for the top 0.0001% of academic publication.** Built to take high-ambition research from raw concept to peer-reviewed publication across *Nature*, *Science*, *Cell*, *NEJM*, *NeurIPS*, *ICML*, *ICLR*, *IEEE*, and *ACM*.

---

## Table of Contents

- [Executive Overview](#executive-overview)
- [Quick Start Guide](#quick-start-guide)
- [Repository Architecture](#repository-architecture)
- [The 10 Research Skills](#the-10-research-skills)
- [Quantitative Evaluator Suite (0–100 Rubrics)](#quantitative-evaluator-suite-0100-rubrics)
- [Production Workflows](#production-workflows)
- [Empirical Walkthrough Examples & Real-World Provenance](#empirical-walkthrough-examples--real-world-provenance)
- [Publisher & Venue Templates](#publisher--venue-templates)
- [Skill Combination & Activation Matrix](#skill-combination--activation-matrix)
- [ARIA Cognitive Architecture & Quality Floor](#aria-cognitive-architecture--quality-floor)
- [Claude Desktop & Claude Projects Setup](#claude-desktop--claude-projects-setup)
- [Author & Community](#author--community)
- [Citation](#citation)

---

## Executive Overview

Generic LLM prompt collections produce shallow, conversational summaries, hallucinate citations, and generate boilerplate prose that is instantly rejected by elite reviewers. 

**CRES (Claude Research Excellence System)** takes the opposite approach. Built around the **ARIA (Advanced Research Intelligence Architect)** cognitive architecture, CRES implements:

1. **Epistemic Depth Over Summaries**: Every skill forces causal depth, hypothesis falsifiability, boundary condition stress-testing, and strict anti-summary synthesis.
2. **Multi-Agent Adversarial Peer Review**: Simulates top-tier editorial boards and hyper-critical peer reviewers (Reviewer 2, Statistical Skeptic, Methodologist, Domain Critic) before submission.
3. **Rigorous Quantitative Evaluators**: Four independent 0–100 assessment engines that evaluate Novelty, Rigor, Clarity, and Long-Term Impact using structured criteria gates.
4. **Empirical Dataset Provenance**: All examples and protocols link to verified real-world datasets, open science repositories (OSF, Zenodo), and legitimate DOI registries with zero synthetic placeholder tokens.
5. **Universal Venue Alignment**: Native formatting blueprints for the world's most demanding publishers (*Nature Portfolio*, *Science/AAAS*, *NeurIPS/ICML/ICLR*, *IEEE Transactions*, *ACM SIG*, *Springer Nature*, *arXiv*).

---

## Quick Start Guide

You can begin using CRES with Claude in under 5 minutes:

```bash
# 1. Clone the repository
git clone https://github.com/AdilShamim8/claude-research-excellence.git
cd claude-research-excellence
```

### 3-Step Execution
1. **Initialize ARIA**: Copy the contents of [`MASTER_PROMPT.md`](MASTER_PROMPT.md) and paste it into your Claude system prompt or Claude Project custom instructions.
2. **State Your Topic**: Specify your field, target venue, and core hypothesis:
   > *"I am working on sample-efficient graph neural networks for drug-target affinity prediction targeting Nature Machine Intelligence."*
3. **Activate Modular Skills**: Call any skill on demand using its activation trigger:
   > `ACTIVATE: IDEATION`  
   > `ACTIVATE: METHODOLOGY`  
   > `ACTIVATE: QUALITY`

---

## Repository Architecture

```
claude-research-excellence/
├── README.md                              ← System overview & master index
├── MASTER_PROMPT.md                       ← ARIA master cognitive system prompt
├── SETUP.md                               ← Step-by-step installation & deployment guide
├── CRES_MASTER_REPO.md                    ← Consolidated single-file reference manual
│
├── skills/                                ← 10 Core research mastery engines
│   ├── 01_ideation/                       ← Breakthrough question & gap discovery
│   ├── 02_literature_command/             ← Systematic review & citation synthesis
│   ├── 03_methodology_architect/          ← Experimental design & threat modeling
│   ├── 04_data_intelligence/              ← Statistical analysis & visual grammar
│   ├── 05_writing_excellence/             ← Publication-grade scientific prose
│   ├── 06_quality_fortress/               ← Adversarial peer review simulation
│   ├── 07_journal_strategy/               ← Venue selection & cover letter strategy
│   ├── 08_ethics_compliance/              ← Research integrity, IRB & compliance
│   ├── 09_citation_mastery/               ← Citation cartography & balance
│   └── 10_impact_amplifier/               ← Post-publication dissemination & policy
│
├── evaluators/                            ← 4 Quantitative manuscript assessment engines
│   ├── NOVELTY_SCORE_RUBRIC.md            ← 5-axis 0-100 novelty rubric (Threshold: >=70)
│   ├── RIGOR_RUBRIC.md                    ← 5-axis 0-100 scientific rigor rubric (Threshold: >=75)
│   ├── CLARITY_ANALYZER.md                ← 6-axis 0-100 prose & visual clarity rubric (Threshold: >=80)
│   └── IMPACT_PREDICTOR.md                ← 5-axis 0-100 citation & influence predictor (Threshold: >=75)
│
├── workflows/                             ← End-to-end execution pipelines
│   ├── FULL_PAPER_WORKFLOW.md             ← 28-week A-to-Z manuscript development lifecycle
│   ├── RAPID_PUBLICATION.md               ← 30-day fast-track protocol for priority claims
│   ├── INTERDISCIPLINARY.md               ← Cross-domain translation & conceptual bridging
│   └── REPLICATION_STUDY.md               ← Pre-registered direct/conceptual replication protocol
│
├── templates/                             ← Production manuscript templates by venue
│   ├── Nature_Family.md                   ← Nature, Nature Biotech, Nature MI structure
│   ├── Science.md                         ← Science (AAAS) research articles & reports
│   ├── NeurIPS_ICML_ICLR.md               ← Top-tier machine learning conference formats
│   ├── IEEE.md                            ← IEEE Transactions double-column specifications
│   ├── ACM.md                             ← ACM SIGCONF & TOCS format guidelines
│   ├── Springer.md                        ← Springer LNCS & journal standards
│   └── arXiv.md                           ← High-impact open preprint formatting
│
└── examples/                              ← Verified domain exemplar papers with dataset registries
    ├── computer_science.md                ← CS/AI: Dynamic Self-Correction LLMs (GSM8K, MATH)
    ├── biomedical.md                      ← Bio/Med: GNN Drug Repurposing (ChEMBL 33, ZINC20)
    ├── social_science.md                  ← SocSci: Remote Work Well-Being (OSF N=2,450, DQI)
    └── interdisciplinary.md               ← Interdisciplinary: Quantum Annealing & GNNs for AMPs
```

---

## The 10 Research Skills

Each skill directory contains an authoritative `SKILL.md` along with specialized modular prompts and actionable checklists:

| Skill | Module Name | Primary Objective | Activation Command | Key Deliverables |
|:---:|:---|:---|:---|:---|
| **01** | [Ideation Engine](skills/01_ideation/SKILL.md) | Formulate high-novelty, falsifiable research questions | `ACTIVATE: IDEATION` | Gap Analysis Matrix, Hypothesis Forge, Novelty Score |
| **02** | [Literature Command](skills/02_literature_command/SKILL.md) | Synthesize vast corpuses without descriptive summaries | `ACTIVATE: LITERATURE` | Systematic Review Protocol, Citation Cartography |
| **03** | [Methodology Architect](skills/03_methodology_architect/SKILL.md) | Build bulletproof experimental designs & pre-registrations | `ACTIVATE: METHODOLOGY` | Threat-to-Validity Matrix, Statistical Power Plan |
| **04** | [Data Intelligence](skills/04_data_intelligence/SKILL.md) | Extract deep statistical signal & design publication figures | `ACTIVATE: DATA` | Effect Size Architecture, Publication Figure Specs |
| **05** | [Writing Excellence](skills/05_writing_excellence/SKILL.md) | Draft prose that compels reviewers from line one | `ACTIVATE: WRITING` | Abstract Blueprint, Introduction Arc, Discussion Defense |
| **06** | [Quality Fortress](skills/06_quality_fortress/SKILL.md) | Simulate hostile peer review & stress-test arguments | `ACTIVATE: QUALITY` | 4-Reviewer Audit, Rebuttal Strategy, Revision Protocol |
| **07** | [Journal Strategy](skills/07_journal_strategy/SKILL.md) | Optimize venue selection, editorial pitch & cover letters | `ACTIVATE: JOURNAL` | Venue Decision Matrix, Editor Cover Letter Blueprint |
| **08** | [Ethics & Compliance](skills/08_ethics_compliance/SKILL.md) | Guarantee integrity, transparency, IRB, and dual-use safety | `ACTIVATE: ETHICS` | Compliance Checklist, Data Management Plan (FAIR) |
| **09** | [Citation Mastery](skills/09_citation_mastery/SKILL.md) | Engineer comprehensive, balanced, and strategic citations | `ACTIVATE: CITATION` | Citation Balance Audit, Recency & Lineage Mapping |
| **10** | [Impact Amplifier](skills/10_impact_amplifier/SKILL.md) | Drive post-publication citations, policy translation & media | `ACTIVATE: IMPACT` | Science Communication Brief, Policy Translation Memo |

---

## Quantitative Evaluator Suite (0–100 Rubrics)

CRES provides a dedicated quantitative evaluation suite located in [`evaluators/`](evaluators/) to audit manuscripts prior to journal submission. Every evaluator calculates a weighted score out of 100 with clear go/no-go acceptance gates:

```
                  ┌───────────────────────────────┐
                  │    CRES EVALUATION SUITE      │
                  └───────────────┬───────────────┘
                                  │
         ┌────────────────┬───────┴────────┬────────────────┐
         ▼                ▼                ▼                ▼
  NOVELTY SCORE      RIGOR SCORE     CLARITY SCORE    IMPACT PREDICTION
   (Rubric >=70)    (Rubric >=75)    (Rubric >=80)      (Rubric >=75)
         │                │                │                │
         └────────────────┼────────────────┴────────────────┘
                                  │
                                  ▼
                     [PEER REVIEW SUBMISSION GATE]
```

### 1. [Novelty Score Rubric](evaluators/NOVELTY_SCORE_RUBRIC.md) (`NOVELTY_SCORE_RUBRIC.md`)
- **Focus**: Evaluates originality and non-obviousness across 5 weighted dimensions:
  - *Conceptual Novelty (25%)*: Paradigm shift vs. incremental adaptation.
  - *Methodological Novelty (25%)*: Algorithmic, instrumental, or design innovation.
  - *Empirical Novelty (20%)*: Novel observations, phenomena, or scale.
  - *Practical / Translational Utility (15%)*: Direct real-world problem resolution.
  - *Interdisciplinary Synthesis (15%)*: Non-trivial cross-domain transfer.
- **Scoring**: 0–100 scale. Threshold for top-tier venues (*Nature*, *NeurIPS*): **$\ge 70/100$**.

### 2. [Rigor Rubric](evaluators/RIGOR_RUBRIC.md) (`RIGOR_RUBRIC.md`)
- **Focus**: Evaluates statistical power, validity, and reproducibility across 5 weighted dimensions:
  - *Internal & External Validity (25%)*: Confound control, randomization, selection bias.
  - *Statistical Power & Inference (25%)*: Sample sizing, effect size reporting, multiple test corrections.
  - *Reproducibility & Open Science (20%)*: Code/data accessibility, deterministic environments.
  - *Baseline Fairness & State-of-the-Art Controls (15%)*: Untuned vs. tuned baseline comparisons.
  - *Boundary Conditions & Sensitivity (15%)*: Failure-mode documentation and stress tests.
- **Scoring**: 0–100 scale. Mandatory submission threshold: **$\ge 75/100$**.

### 3. [Clarity Analyzer](evaluators/CLARITY_ANALYZER.md) (`CLARITY_ANALYZER.md`)
- **Focus**: Evaluates scientific communication, rhetorical flow, and cognitive load across 6 dimensions:
  - *Macro-Structure & Rhetorical Momentum (20%)*: Clear thesis progression and paragraph transitions.
  - *Sentence-Level Micro-Clarity (20%)*: Active syntax, topic-stress alignment, elimination of bloat.
  - *Cognitive Load & Information Density (15%)*: Digestible technical presentation.
  - *Visual Grammar & Figure Integration (15%)*: Self-contained captions and high-clarity data charts.
  - *Terminology Precision & Jargon Accessibility (15%)*: Clear definitions without exclusionary jargon.
  - *Executive Summary & Abstract Calibration (15%)*: High-impact abstract that conveys context, gap, method, findings, and implications.
- **Scoring**: 0–100 scale. Target standard: **$\ge 80/100$**.

### 4. [Impact Predictor](evaluators/IMPACT_PREDICTOR.md) (`IMPACT_PREDICTOR.md`)
- **Focus**: Estimates 24–60 month citation trajectories and field influence across 5 dimensions:
  - *Theoretical Influence & Paradigm Longevity (25%)*: Foundational grounding for future studies.
  - *Methodological & Tool Adoption (25%)*: Reusable software, frameworks, or datasets.
  - *Cross-Disciplinary Diffusion Potential (20%)*: Uptake outside the primary subfield.
  - *Translational & Policy Utility (15%)*: Industrial, clinical, or governmental application.
  - *Field-Shaping Longevity & Robustness (15%)*: Resilience against rapid technological obsolescence.
- **Scoring**: 0–100 scale. High-impact trajectory: **$\ge 75/100$**.

---

## Production Workflows

CRES includes four battle-tested workflows in [`workflows/`](workflows/):

1. **[Full Paper Lifecycle](workflows/FULL_PAPER_WORKFLOW.md)**: A complete 28-week, 8-phase journey from raw intuition to post-acceptance dissemination.
2. **[Rapid Publication Protocol](workflows/RAPID_PUBLICATION.md)**: A high-velocity 30-day timeline designed to establish urgent priority claims for breakthrough discoveries without sacrificing empirical rigor.
3. **[Interdisciplinary Innovation Framework](workflows/INTERDISCIPLINARY.md)**: A cross-domain methodology that establishes dual-field epistemological alignment, translates specialized vocabularies, and satisfies reviewers from contrasting traditions.
4. **[Replication & Extension Protocol](workflows/REPLICATION_STUDY.md)**: A pre-registered framework for direct, conceptual, and multi-site replications with statistical equivalence testing and artifact validation.

---

## Empirical Walkthrough Examples & Real-World Provenance

Unlike synthetic tutorials that use dummy variables, CRES features complete, end-to-end exemplar manuscripts in [`examples/`](examples/) grounded in real-world benchmark datasets, open registries, and verified literature citations:

| Domain | Exemplar Manuscript | Core Research Question | Verified Real-World Benchmarks & Data | Empirical Provenance & DOI Citations |
|:---|:---|:---|:---|:---|
| **Computer Science** | [`examples/computer_science.md`](examples/computer_science.md) | *Dynamic Self-Correction in LLMs: When Does Verification Outperform Scale?* | **GSM8K**, **MATH**, **SVAMP**, **StrategyQA**, **GSM-Hard** | arXiv:2110.14168, arXiv:2103.03874, arXiv:2205.10625, arXiv:2212.09535 |
| **Biomedical Sciences** | [`examples/biomedical.md`](examples/biomedical.md) | *Multi-Task GNNs for Antiviral Drug Repurposing Across Coronaviridae* | **ChEMBL 33**, **ZINC20**, **PubChem BioAssay**, **PDBbind v2020** | DOI: 10.1093/nar/gkad1004, 10.1021/acs.jcim.0c00675, 10.1021/acs.jcim.0c00511 |
| **Social Sciences** | [`examples/social_science.md`](examples/social_science.md) | *Remote Work Flexibility & Well-Being: A 24-Month Longitudinal Study* | **OSF Pre-registered (N=2,450)**, **DQI Index**, **BFI-2**, **MBI-GS** | DOI: 10.1037/apl0000862, 10.1037/ocp0000101, 10.1177/0003122420986777 |
| **Interdisciplinary** | [`examples/interdisciplinary.md`](examples/interdisciplinary.md) | *Quantum Annealing & Graph Transformers for De Novo Antimicrobial Peptide Design* | **APD3 Database**, **DRAMP 3.0**, **UniProt**, **D-Wave Advantage 4.1 QPU** | DOI: 10.1093/nar/gkv1278, 10.1038/s41586-021-03819-2, 10.1038/s41592-022-01490-w |

---

## Publisher & Venue Templates

Located in [`templates/`](templates/), these structural blueprints reflect the exact editorial criteria, section constraints, and stylistic mandates of global publishing bodies:

- [`templates/Nature_Family.md`](templates/Nature_Family.md): Formatted for *Nature*, *Nature Biotechnology*, *Nature Machine Intelligence* (5,000 words, modular Methods, standalone display item legends).
- [`templates/Science.md`](templates/Science.md): Tailored for *Science* (AAAS) Research Articles and Reports (strict 2,500–4,500 word limits, highly condensed framing).
- [`templates/NeurIPS_ICML_ICLR.md`](templates/NeurIPS_ICML_ICLR.md): Engineered for top ML/AI venues (9-page limit, rigorous theoretical proofs, empirical error bars, Broader Impact / Ethics statements).
- [`templates/IEEE.md`](templates/IEEE.md): Built for *IEEE Transactions* (two-column layout, formal mathematical notation, hardware/algorithmic complexity analysis).
- [`templates/ACM.md`](templates/ACM.md): Geared for *ACM Computing Surveys* and *SIG* conferences (ACM CCS classifications, artifact badges).
- [`templates/Springer.md`](templates/Springer.md): Conforming to LNCS and Springer Nature multidisciplinary monographs.
- [`templates/arXiv.md`](templates/arXiv.md): High-impact preprint architecture designed to maximize citation velocity prior to formal peer review.

---

## Skill Combination & Activation Matrix

Combine skills sequentially to match your stage in the research lifecycle:

| Research Objective | Recommended Skill Pipeline | Target Outcome |
|:---|:---|:---|
| **Starting from Scratch** | `IDEATION` $\rightarrow$ `LITERATURE` $\rightarrow$ `METHODOLOGY` | Formulate a bulletproof, high-novelty research design |
| **Data Collected, Ready to Write** | `DATA` $\rightarrow$ `WRITING` $\rightarrow$ `QUALITY` | Transform raw results into an executive first draft |
| **Pre-Submission Audit** | `QUALITY` $\rightarrow$ `JOURNAL` $\rightarrow$ `CITATION` | Run 4-reviewer adversarial audit & format submission package |
| **Addressing Reviewer Rejections / R&R** | `QUALITY (Revision Mode)` $\rightarrow$ `JOURNAL` | Build point-by-point rebuttal matrices and revised text |
| **Post-Acceptance Outreach** | `IMPACT` | Generate press releases, policy briefs, and social threads |
| **Full Paper Pipeline** | All 10 skills in sequence (Skills 01 through 10) | Comprehensive manuscript ready for top 0.0001% venues |

---

## ARIA Cognitive Architecture & Quality Floor

Every activation within CRES executes the **ARIA 5-Step Cognitive Architecture** before emitting output:

```
[STEP 1: SUMMIT SCAN]      → Benchmark against the top 3 papers in the domain over the last 5 years.
[STEP 2: GAP ANALYSIS]     → Identify the critical delta between the current state and the benchmark.
[STEP 3: NON-OBVIOUS BRIDGE]→ Formulate non-trivial, cross-domain insights rather than incremental fixes.
[STEP 4: ADVERSARIAL TEST] → Subject every claim to harsh Reviewer-2 stress tests to preempt critiques.
[STEP 5: SYNTHESIS]        → Integrate multi-disciplinary lenses (physics, economics, ML, biology).
```

### The CRES Quality Floor
- **Evidence Integrity**: Every empirical assertion must cite reproducible data or be explicitly defined as an untested hypothesis.
- **Methodological Determinism**: Experimental steps must contain sufficient precision for independent third-party replication.
- **Figure Storytelling**: Every chart or diagram must be fully interpretable by a domain specialist in under 30 seconds.
- **Anti-Summary Standard**: Literature reviews must synthesize conceptual tension and theoretical debates — never produce generic chronological lists.

---

## Claude Desktop & Claude Projects Setup

### Option A: Claude Projects (Recommended)
1. In Claude, navigate to **Projects** and create a new project (e.g., `"Research Excellence - [Your Project]"`).
2. Paste the contents of [`MASTER_PROMPT.md`](MASTER_PROMPT.md) into the **Project Instructions**.
3. Upload relevant domain papers, preprints, and dataset documentation into the **Project Knowledge**.
4. Launch your chats with immediate skill triggers (e.g., `ACTIVATE: IDEATION`).

### Option B: Claude Desktop / Web Interface
1. Start a new conversation.
2. Paste the ARIA master prompt from [`MASTER_PROMPT.md`](MASTER_PROMPT.md).
3. Follow up with your specific research objectives and skill triggers.

For advanced configurations, API system prompt deployments, and memory optimization guidelines, consult [`SETUP.md`](SETUP.md).

---

## Author & Community

Developed and maintained by **Adil Shamim**.

<p align="center">
  <a href="https://www.adilshamim.me/">
    <img src="https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=About.me&logoColor=white" alt="Personal Website" />
  </a>
  <a href="https://adilshamim8.medium.com/">
    <img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white" alt="Medium" />
  </a>
  <a href="https://linkedin.com/in/adilshamim8">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://twitter.com/adil_shamim8">
    <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter" />
  </a>
  <a href="https://www.kaggle.com/adilshamim8">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle" />
  </a>
  <a href="https://leetcode.com/u/AdilShamim8">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode" />
  </a>
  <a href="https://github.com/AdilShamim8">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Profile" />
  </a>
</p>

---

## Citation

If CRES enhances your scientific research, methodology design, or publication workflow, please cite this framework:

```bibtex
@software{shamim2026cres,
  author       = {Shamim, Adil},
  title        = {Claude Research Excellence System (CRES): An Advanced AI Framework for High-Impact Scientific Publishing},
  year         = {2026},
  month        = {September},
  publisher    = {GitHub},
  version      = {2.4},
  url          = {https://github.com/AdilShamim8/claude-research-excellence}
}
```
---

<div align="center">

### ✦ Connect With Me

<p>
  <a href="https://www.adilshamim.me">
    <img src="https://img.shields.io/badge/Portfolio-111111?style=for-the-badge&logo=About.me&logoColor=white" />
  </a>
  <a href="https://linkedin.com/in/adilshamim8">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://adilshamim8.medium.com">
    <img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" />
  </a>
  <a href="https://adilshamim.substack.com">
    <img src="https://img.shields.io/badge/Substack-FF6719?style=for-the-badge&logo=substack&logoColor=white" />
  </a>
</p>

<p>
  <a href="https://github.com/AdilShamim8">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.kaggle.com/adilshamim8">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" />
  </a>
  <a href="https://leetcode.com/u/AdilShamim8">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=111111" />
  </a>
  <a href="https://twitter.com/adil_shamim8">
    <img src="https://img.shields.io/badge/X-111111?style=for-the-badge&logo=x&logoColor=white" />
  </a>
</p>

<sub>Building • Learning • Researching • Sharing</sub>

<br/>

⭐ <strong>If this repository helped you, consider giving it a star!</strong> ⭐

</div>

<p align="center">
  <sub>CRES v2.4 • Engineered for researchers who refuse to settle for "good enough." • Current as of September 18, 2026</sub>
</p>
