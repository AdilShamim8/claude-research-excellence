# Reproducibility Framework

## A Comprehensive Guide to Ensuring Research Reproducibility, Replicability, and Robustness

### Purpose
This framework provides detailed standards and procedures for ensuring that research can be independently reproduced, replicated, and verified. It addresses the full lifecycle of reproducibility — from code and data to computational environments and documentation — and provides practical checklists for meeting community standards.

---

## SECTION 1: DEFINITIONS — REPRODUCIBILITY VS. REPLICABILITY VS. ROBUSTNESS

These terms are frequently conflated but refer to fundamentally different standards. Precise usage is essential.

### 1.1 The Three R's

| Term | Definition | What Is Repeated | What May Differ | Gold Standard |
|------|-----------|-----------------|----------------|---------------|
| **Reproducibility** | Same data + same code = same results | Data and code | Nothing (exact computational reproduction) | Bit-for-bit identical output |
| **Replicability** | New data + same methods = consistent results | Methods and analysis plan | Data (new sample, new collection) | Same direction, similar magnitude, statistical significance |
| **Robustness** | Same data + different analytic choices = consistent conclusions | Data and research question | Analytic methods, model specifications, covariates | Same substantive conclusion regardless of reasonable analytic variation |

### 1.2 Why All Three Matter

- **Reproducibility** ensures that the reported results are not computational errors or data handling mistakes
- **Replicability** ensures that the finding is not a false positive specific to one sample
- **Robustness** ensures that the finding is not an artifact of a specific analytic choice

### 1.3 Failure Rates

| Type | Estimated Failure Rate | Source |
|------|----------------------|--------|
| Computational reproducibility | 25–40% of published papers cannot be reproduced | Stodden et al., 2018 |
| Replicability (psychology) | ~40% of effects replicate | Open Science Collaboration, 2015 |
| Replicability (cancer biology) | ~11% of preclinical findings replicate | Begley & Ellis, 2012 |
| Robustness | ~30–50% of findings are sensitive to analytic choices | Silberzahn et al., 2018 (Many Analysts) |

---

## SECTION 2: CODE REPRODUCIBILITY STANDARDS

### 2.1 Code Quality Requirements

| Standard | Requirement | Verification |
|----------|------------|--------------|
| **Readability** | Code is commented, uses descriptive variable names, follows style guide | Peer review of code |
| **Completeness** | All analyses in the manuscript can be run from the provided code | Independent execution |
| **Correctness** | Code produces the results reported in the manuscript | Computational audit |
| **Portability** | Code runs on a different machine than the original author's | Independent execution |
| **Version control** | Code is version-controlled with meaningful commit messages | Git history review |

### 2.2 Code Organization Template

```
project/
├── README.md                  # Project overview and instructions
├── LICENSE                    # Code license (MIT, GPL, etc.)
├── requirements.txt           # Python dependencies / R package versions
├── environment.yml            # Conda environment specification
├── Dockerfile                 # Container specification (if applicable)
├── data/
│   ├── raw/                   # Original, immutable data files
│   ├── processed/             # Cleaned and transformed data
│   └── README.md              # Data documentation
├── code/
│   ├── 01_data_cleaning.py    # Data preprocessing (numbered for execution order)
│   ├── 02_descriptive_stats.py # Descriptive analyses
│   ├── 03_primary_analysis.py  # Primary hypothesis tests
│   ├── 04_secondary_analysis.py # Secondary analyses
│   ├── 05_sensitivity_analysis.py # Robustness checks
│   └── 06_figures_tables.py   # Generate manuscript figures and tables
├── output/
│   ├── tables/                # Generated tables
│   └── figures/               # Generated figures
├── results/                   # Final results and manuscript
└── preregistration/           # Pre-registration documents
```

### 2.3 Code Documentation Standards

**Every script must include:**
```python
"""
Script: 03_primary_analysis.py
Purpose: Test primary hypotheses H1 and H2 using [METHOD]
Author: [NAME]
Date: [YYYY-MM-DD]
Input: data/processed/cleaned_data.csv
Output: output/tables/table_2.csv, output/figures/figure_1.png
Dependencies: pandas 2.0, scipy 1.10, statsmodels 0.14
Pre-registration: [LINK] (Deviations documented in Section X)
"""
```

**Every analysis must include:**
- Input data path (explicit, not hardcoded relative paths)
- Output file paths
- Random seed specification (for any stochastic process)
- Version numbers of all packages
- Deviation from pre-registration (if any)

### 2.4 Random Seed Management

**Rule:** Every analysis that involves randomness (bootstrapping, permutation tests, MCMC, train-test splits, multiple imputation) must set a random seed.

```python
import numpy as np
import random

SEED = 42  # Document why this specific seed
np.random.seed(SEED)
random.seed(SEED)
# For scikit-learn:
# model = RandomForestClassifier(random_state=SEED)
```

**Document the seed choice** and verify that results are stable across nearby seed values (if results change dramatically with seed, the analysis is unstable).

---

## SECTION 3: DATA SHARING REQUIREMENTS

### 3.1 What to Share

| Data Type | Sharing Standard | Format | Documentation |
|-----------|-----------------|--------|---------------|
| **Raw data** | Share if possible (subject to consent and ethics) | CSV, TSV, or open format | Data dictionary with variable names, types, coding, and missing value codes |
| **Processed data** | Always share | CSV with code that produces it from raw | Same as raw + transformation documentation |
| **Synthetic data** | If raw data cannot be shared, provide synthetic data preserving key statistical properties | CSV | Documentation of generation method and properties preserved |
| **Simulation data** | Share code that generates it | Code only | Parameter specifications |
| **Proprietary/restricted data** | Cannot share; provide detailed access instructions | N/A | Access procedures, cost, timeline, restrictions |

### 3.2 Data Documentation (Data Dictionary)

**Required for every dataset:**

| Field | Content |
|-------|---------|
| Variable name | Exact name as it appears in the data file |
| Variable label | Human-readable description of what this variable measures |
| Data type | Numeric, string, date, boolean, categorical |
| Valid range | Minimum, maximum, valid codes |
| Missing value code | How missing values are represented (e.g., -99, NA, blank) |
| Measurement unit | If applicable (e.g., years, kilograms, Likert scale 1-5) |
| Source | How the variable was collected (self-report, observation, computed) |
| Transformation | Any transformations applied (log, standardization, reverse-coding) |
| Notes | Any special considerations (e.g., "value capped at 100") |

### 3.3 Data Sharing Platforms

| Platform | Best For | DOI | Access Control | Cost |
|----------|---------|-----|---------------|------|
| **OSF** | All disciplines; integrates with workflows | Yes | Public/private; embargo | Free |
| **Zenodo** | Large datasets; EU-funded research | Yes | Public; embargo up to 2 years | Free (10GB) |
| **Figshare** | Supplementary materials; figures | Yes | Public/private | Free (20GB) |
| **Dryad** | Published article data | Yes | Public | $120+ |
| **ICPSR** | Social science data | Yes | Restricted possible | Institutional |
| **Harvard Dataverse** | All disciplines; good for large datasets | Yes | Public/private | Free |
| **OpenNeuro** | Neuroimaging data | Yes | Public | Free |
| **PhysioNet** | Physiological signal data | Yes | Public (some restricted) | Free |

### 3.4 De-identification Protocol

Before sharing human subjects data:

- [ ] Remove all direct identifiers (name, address, phone, email, SSN, MRN)
- [ ] Remove or generalize quasi-identifiers (exact date of birth → age; exact location → region; specific occupation → occupational category)
- [ ] Assess re-identification risk using k-anonymity (minimum k = 5) or differential privacy
- [ ] Check for unique combinations of variables that could identify individuals
- [ ] Obtain IRB/ethics approval for data sharing
- [ ] Use a data use agreement if sharing restricted data

---

## SECTION 4: COMPUTATIONAL ENVIRONMENT DOCUMENTATION

### 4.1 Why Environment Matters

"I ran the same code on the same data and got different results" is a common reproducibility failure. Causes include:
- Different software versions (function behavior changes between versions)
- Different operating systems (floating-point arithmetic differences)
- Different dependency versions (a package update changes defaults)
- Different hardware (GPU vs. CPU; different BLAS implementations)

### 4.2 Documentation Levels

| Level | What to Document | When Required |
|-------|-----------------|---------------|
| **Minimum** | Language version, key package versions, OS | All publications |
| **Standard** | Full package list with versions, random seeds, all software specifications | Recommended for all publications |
| **Comprehensive** | Container specification (Docker/Singularity) | Required for complex computational analyses |
| **Complete** | Full virtual machine or compute snapshot | Required for high-stakes or regulatory analyses |

### 4.3 Environment Capture Methods

**Python:**
```bash
# Capture all packages and versions
pip freeze > requirements.txt

# Or create a reproducible conda environment
conda env export > environment.yml

# Or create a Docker container
docker build -t my-analysis .
```

**R:**
```r
# Capture session information
sessionInfo()

# Or use renv for project-specific package management
renv::init()
renv::snapshot()
```

### 4.4 Container Specifications

**Docker (most common):**
```dockerfile
FROM python:3.11-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    gcc \
    && rm -rf /var/lib/apt/lists/*

# Install Python packages
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . /analysis
WORKDIR /analysis

# Run the analysis
CMD ["python", "code/01_data_cleaning.py"]
```

**When to use containers:**
- The analysis involves complex software dependencies
- The analysis needs to run on different machines
- You are sharing computational methods with other researchers
- The analysis may need to be rerun years later

---

## SECTION 5: VERSION CONTROL REQUIREMENTS

### 5.1 What to Version Control

| Item | Version Control? | Storage |
|------|-----------------|---------|
| Analysis code | Yes — Git | GitHub, GitLab, OSF |
| Documentation | Yes — Git | Same as code |
| Pre-registration | Yes — Git or OSF | OSF (timestamped) |
| Raw data | No (too large; immutable) | Data repository |
| Processed data | Yes (derived from code + raw data) | Regenerated from code |
| Output (tables, figures) | No (regenerated from code) | Regenerated from code |
| Manuscript | Yes — Git | GitHub, OSF |
| Correspondence | No | N/A |

### 5.2 Git Best Practices for Research

**Commit message format:**
```
[TYPE]: [BRIEF DESCRIPTION]

[OPTIONAL LONGER DESCRIPTION]

Types:
  analysis: Analytical code changes
  data: Data processing changes
  docs: Documentation changes
  fig: Figure generation changes
  fix: Bug fixes
  refactor: Code restructuring without functional change
```

**Branching strategy:**
- `main`: Stable, reproducible state matching the manuscript
- `analysis/[name]`: Analysis development branches
- `sensitivity/[name]`: Sensitivity analysis branches

**Tagging:**
- Tag the exact code version that produced each manuscript submission
- Tag the exact code version that produced the final published results

### 5.3 .gitignore for Research Projects

```
# Data files (stored in data repository, not Git)
data/raw/
data/processed/

# Output (regenerated from code)
output/

# System files
.DS_Store
Thumbs.db

# Python
__pycache__/
*.pyc
.ipynb_checkpoints/

# R
.Rhistory
.RData
.Rproj.user/

# IDE
.vscode/
.idea/
```

---

## SECTION 6: REPRODUCIBILITY CHECKLIST FOR MANUSCRIPTS

### Pre-Submission Checklist

**Data:**
- [ ] Data is deposited in a trusted repository with a DOI
- [ ] Data dictionary is complete and accurate
- [ ] De-identification has been verified
- [ ] Access restrictions (if any) are documented
- [ ] Data citation is included in the manuscript

**Code:**
- [ ] All analyses can be reproduced from the provided code
- [ ] Code is commented and readable
- [ ] Random seeds are set for all stochastic processes
- [ ] Package versions are documented
- [ ] Code is deposited in a repository with a DOI
- [ ] A README explains how to run the analysis end-to-end

**Environment:**
- [ ] Software and package versions are specified in the manuscript
- [ ] Container specification is provided (if applicable)
- [ ] Operating system and hardware are documented (if relevant)

**Methods:**
- [ ] Pre-registration is linked in the manuscript
- [ ] All deviations from pre-registration are documented and justified
- [ ] All exclusion criteria are applied and documented
- [ ] All analyses (including non-significant) are reported
- [ ] Exploratory analyses are clearly labeled

**Reporting:**
- [ ] Exact p-values are reported (not just p < .05)
- [ ] Effect sizes with confidence intervals are reported for all primary analyses
- [ ] Descriptive statistics (M, SD, n) are provided for all variables
- [ ] Assumption checks are reported
- [ ] Missing data handling is documented
- [ ] Outlier handling is documented with sensitivity analyses

**Transparency:**
- [ ] A transparency and openness promotion (TOP) compliance statement is included
- [ ] Data availability statement specifies where and how to access data
- [ ] Code availability statement specifies where and how to access code
- [ ] Conflicts of interest are declared
- [ ] Funding sources are declared

---

## SECTION 7: COMMON REPRODUCIBILITY FAILURES AND PREVENTION

### 7.1 Failure Catalog

| Failure | Cause | Prevention | Detection |
|---------|-------|-----------|-----------|
| **Results don't reproduce from same data and code** | Hardcoded paths, undocumented manual steps, version drift | Use relative paths; script everything; document environment | Independent reproduction attempt |
| **Different results on different machines** | OS differences, BLAS implementations, floating-point handling | Use containers; specify environment; test on clean machine | Run on different OS |
| **Data processing errors** | Manual data editing, spreadsheet auto-correction, copy-paste errors | Never manually edit raw data; script all transformations; validate at each step | Checksums on raw data; automated validation |
| **Analysis code bugs** | Incorrect formula, wrong variable, mislabeled conditions | Code review; unit tests; comparison with known results; sanity checks | Independent audit; test against synthetic data with known results |
| **Selective reporting** | Only significant analyses reported; non-significant analyses omitted | Pre-register; report all analyses; include analysis log | Audit trail; compare pre-registration to manuscript |
| **P-hacking** | Trying many analyses and reporting only the "best" | Pre-register; correct for multiple comparisons; multiverse analysis | Compare analytic choices to pre-registration |
| **Figure manipulation** | Axis truncation, selective zoom, misleading color scales | Follow figure standards; provide raw data for figures | Audit figure against data |
| **Mistaken authorship** | Wrong person credited; ghost authorship | Follow ICMJE criteria; document contributions | CRediT taxonomy |

### 7.2 Prevention Strategies by Research Phase

**Before data collection:**
- Pre-register hypotheses, methods, and analysis plan
- Write the analysis code before data collection (template analysis)
- Create synthetic data to test the analysis pipeline
- Document the computational environment

**During data collection:**
- Store raw data immediately and immutably (never modify raw data)
- Back up data regularly (3-2-1 rule: 3 copies, 2 media types, 1 offsite)
- Log any deviations from the protocol in real time
- Check data integrity at regular intervals (e.g., checksums)

**During analysis:**
- Never overwrite raw data files
- Script every transformation (no manual edits)
- Use version control for all code
- Document every decision (even rejected alternatives)
- Run sensitivity analyses for subjective choices

**During writing:**
- Link every claim to a specific analysis and result
- Report all analyses, not just significant ones
- Include a data and code availability statement
- Use the TOP guidelines checklist
- Have a colleague attempt reproduction before submission

---

## SECTION 8: OSF/ZENODO INTEGRATION GUIDANCE

### 8.1 OSF (Open Science Framework)

**Project Structure:**
```
OSF Project
├── Pre-registration/
│   ├── Hypotheses and analysis plan
│   └── Deviations documentation
├── Materials/
│   ├── Stimuli
│   ├── Measures/Surveys
│   └── Experimental protocol
├── Data/
│   ├── Raw data (if shareable)
│   ├── Processed data
│   └── Data dictionary
├── Analysis/
│   ├── Code (GitHub integration)
│   ├── Environment specification
│   └── Output (tables, figures)
├── Manuscript/
│   ├── Drafts
│   └── Supplementary materials
└── Communication/
    └── Authorship and contributions (CRediT)
```

**Key OSF Features for Reproducibility:**
- **Timestamping:** Every upload is timestamped; provides proof of prior discovery
- **Versioning:** Files can be updated with version history preserved
- **Preregistration:** Built-in templates for pre-registration
- **GitHub integration:** Automatically mirrors GitHub repositories
- **DOI assignment:** Projects and components can receive DOIs for citation
- **Embargo:** Data and materials can be embargoed until publication
- **Licensed storage:** Choose CC0, CC-BY, or other open licenses

**Setting up OSF for a research project:**
1. Create an OSF project before data collection begins
2. Add components for each project phase (pre-registration, data, analysis, manuscript)
3. Connect GitHub repository to the Analysis component
4. Upload pre-registration before data collection
5. Add data as it becomes available (with appropriate access controls)
6. Archive the project with a DOI upon publication

### 8.2 Zenodo

**When to use Zenodo instead of (or in addition to) OSF:**
- You need to archive large datasets (>50GB; Zenodo supports up to 50GB per file, 1TB total)
- You want a CERN-backed long-term preservation guarantee
- You are publishing EU-funded research (Zenodo is EU-recommended)
- You want GitHub integration with automatic DOI assignment for releases

**GitHub-Zenodo Integration:**
1. Go to zenodo.org and log in with GitHub
2. Enable the repository you want to archive
3. Create a GitHub release (tagged version)
4. Zenodo automatically creates a DOI for that release
5. Cite the DOI in your manuscript

**Best practice:** Archive both code (via GitHub-Zenodo) and data (via direct Zenodo upload or OSF-Zenodo integration)

### 8.3 Combined Workflow

**Recommended reproducibility workflow:**

1. **Create OSF project** — central hub for all project materials
2. **Pre-register on OSF or AsPredicted** — before data collection
3. **Store code on GitHub** — with OSF integration for automatic backup
4. **Collect data** — store raw data on OSF (with access controls if needed)
5. **Analyze data** — using version-controlled code on GitHub
6. **Create GitHub release** — when analysis is finalized
7. **Archive on Zenodo** — automatic DOI from GitHub release
8. **Deposit data on Zenodo or domain repository** — with separate DOI
9. **Link everything in manuscript** — data DOI, code DOI, pre-registration DOI, OSF project URL
10. **Publish** — with complete transparency and reproducibility infrastructure

### 8.4 Licensing Recommendations

| Material | Recommended License | Why |
|----------|-------------------|-----|
| **Code** | MIT or BSD-3-Clause | Permissive; encourages reuse; widely recognized |
| **Data** | CC0 (public domain dedication) | Maximizes reuse; no attribution required; eliminates legal uncertainty |
| **Documentation** | CC-BY 4.0 | Requires attribution; allows adaptation |
| **Pre-registration** | CC0 or CC-BY 4.0 | Either is appropriate |
| **Supplementary materials** | CC-BY 4.0 | Requires attribution; allows sharing |

**Never use:** CC-BY-NC (non-commercial), CC-BY-ND (no derivatives), or CC-BY-NC-ND — these restrict reuse and contradict open science principles.

---

## OUTPUT FORMAT

```markdown
# Reproducibility Plan

## 1. Reproducibility Assessment
- Current reproducibility level: [None / Partial / Full]
- Key gaps: [List]
- Priority actions: [List]

## 2. Data Management
- Raw data storage: [Platform, access controls]
- Processed data: [Regenerated from code + raw data]
- Data dictionary: [Location]
- De-identification status: [Complete / Pending]
- Data sharing plan: [Platform, DOI, embargo status]

## 3. Code Management
- Repository: [URL]
- Organization: [Directory structure]
- Documentation standard: [Level achieved]
- Reproducibility test: [Passed / Failed — describe]

## 4. Environment
- Language and version: [Specified]
- Package versions: [Documented in requirements.txt/environment.yml]
- Container: [Dockerfile provided / Not needed]
- Random seeds: [Set for all stochastic processes]

## 5. Version Control
- Platform: [GitHub/GitLab/OSF]
- Branching strategy: [Described]
- Tags: [Created for manuscript submissions]
- .gitignore: [Configured]

## 6. Pre-registration
- Platform: [OSF/AsPredicted/etc.]
- DOI/URL: [Link]
- Deviations from pre-registration: [Documented]

## 7. Archival and DOI
- Code DOI: [Zenodo DOI from GitHub release]
- Data DOI: [Repository DOI]
- OSF project: [URL]
- All DOIs cited in manuscript: [Yes]

## 8. Checklist Status
- Pre-submission reproducibility checklist: [N/N items passed]
- Items remaining: [List]
```
