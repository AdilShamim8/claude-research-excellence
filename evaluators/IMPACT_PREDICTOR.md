# Scholarly Impact Predictor

## 📈 CITATION TRAJECTORY & IMPACT FORECASTING MODEL

```
ACTIVATE: IMPACT_PREDICTOR
```

This evaluator operationalizes empirical bibliometric research to predict the citation trajectory, h-index contribution, and disciplinary reach of a scientific manuscript over 2-, 5-, and 10-year horizons.

---

### Quantitative Impact Predictors

#### 1. VENUE PRESTIGE & AUDIENCE MULTIPLIER (Base Weight: 1.0 – 5.0×)
* **5.0×**: Top-tier general multidisciplinary (*Nature*, *Science*, *Cell*, *NEJM*, *Lancet*)
* **3.5×**: Top flagship field journals / Tier-1 CS conferences (*JACS*, *NeurIPS*, *ICML*, *APSR*, *PRL*)
* **2.0×**: Leading specialist society journals (*J. Med. Chem.*, *Bioinformatics*, *PNAS Nexus*, *IEEE TPAMI*)
* **1.2×**: Established disciplinary open-access journals (*PLOS ONE*, *Scientific Reports*, *Frontiers*)
* **0.8×**: Regional or specialized niche publications

#### 2. UTILITY ARTIFACT BONUS (Additive Boost: 0 to +60%)
Papers that provide reusable artifacts consistently outperform purely theoretical or descriptive papers in long-term citations:
* **+25%**: Novel reusable computational tool, library, or foundation model (e.g., PyTorch library, Hugging Face checkpoint)
* **+20%**: Curated, open-access benchmark dataset formatted with standardized APIs and evaluation splits
* **+15%**: Standardized experimental protocol, wet-lab assay SOP, or pre-registration template adopted by others

#### 3. OPEN SCIENCE & ACCESSIBILITY FACTOR (Multiplier: 1.0 – 1.6×)
* **1.5–1.6×**: Full Open Access + preprint posted on arXiv/bioRxiv/medRxiv prior to peer review + code/data deposited on Zenodo with DOI
* **1.2–1.3×**: Hybrid Open Access (APC paid) without preprint deposition
* **1.0×**: Paywalled / subscription access only

#### 4. METHODOLOGICAL GENERALIZABILITY (Additive Boost: 0 to +40%)
* **+40%**: Method or framework bridges two major disjoint communities (e.g., ML algorithms + biophysical validation)
* **+25%**: Domain-general technique applicable across ≥3 distinct scientific problems
* **+10%**: Domain-specific optimization applicable to a single narrow assay or model

#### 5. PENALTY DRIVERS (Negative Multipliers: 0.5 – 0.9×)
* **0.6×**: Paywalled with closed proprietary data and no code sharing
* **0.7×**: Extreme topic hyperspecialization with estimated global researcher cohort < 200 people
* **0.8×**: Published during annual academic attention slumps (mid-December to mid-January) without active post-launch dissemination

---

### Citation Velocity Forecasting Model

Compute your manuscript's **Estimated Impact Index (EII)**:

$$\text{EII} = \text{Venue Weight} \times (1 + \text{Utility Bonus} + \text{Generalizability}) \times \text{Open Science Factor} \times \text{Penalty Multipliers}$$

#### Estimated 5-Year Citation Trajectory by EII:

| EII Range | Predicted 2-Year Citations | Predicted 5-Year Citations | Lifetime Impact Classification |
|---|---|---|---|
| **> 8.0** | 80 – 250+ | 300 – 1,500+ | **Field Landmark Paper** (Top 1% in field; durable foundation for decade) |
| **5.5 – 8.0** | 35 – 80 | 120 – 300 | **High-Impact Work** (Major citation driver; essential literature in subfield) |
| **3.5 – 5.4** | 15 – 35 | 50 – 120 | **Solid Contributor** (Consistent citations from active peer group) |
| **2.0 – 3.4** | 5 – 15 | 20 – 50 | **Standard Specialist Paper** (Modest citations; serves niche inquiry) |
| **< 2.0** | 0 – 5 | 5 – 20 | **Low-Velocity Output** (Risk of becoming part of the uncited literature) |

---

### Post-Publication Impact Acceleration Checklist

To ensure your manuscript reaches its maximum predicted trajectory:
1. **Week 1 (Launch Window)**:
   - Post open-access preprint link with executive graphic summary on Twitter/X, LinkedIn, and academic Discord/Slack channels.
   - Send personal emails with clean PDF attached to 15 key researchers whose work you directly extended or challenged.
2. **Month 1 (Dissemination Momentum)**:
   - Deposit presentation slide deck and video walkthrough to Zenodo / YouTube.
   - Release interactive demonstration or Hugging Face Space / Colab notebook for the core model or analysis.
3. **Year 1 (Citation Network Solidification)**:
   - Actively monitor and respond to follow-up preprints and papers citing your work.
   - Submit proposal for workshop or tutorial at premier field conference.
