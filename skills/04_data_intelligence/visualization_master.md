# Data Visualization Mastery Guide

## Purpose
This guide provides comprehensive standards for creating publication-quality data visualizations. Every figure you produce must communicate clearly, withstand scrutiny, and serve the paper's argument. This guide covers figure selection, design standards, color systems, statistical annotation, and software-specific implementation.

---

## 1. Figure Type Selection Decision Tree

### Start Here: What Are You Showing?

```
What is the primary message?
│
├── COMPARISON between groups or conditions
│   ├── 2 groups → 
│   │   ├── Small N (<30) → Dot plot with individual points + mean ± CI
│   │   └── Large N (≥30) → Box plot with jittered points or violin plot
│   ├── 3+ groups → 
│   │   ├── Independent → Box plot with pairwise significance brackets
│   │   ├── Related/repeated → Slope chart or parallel coordinates
│   │   └── Many groups (>6) → Dot plot with confidence intervals (Cleveland plot)
│   └── Factorial (2+ IVs) → 
│       ├── 2×2 → Grouped bar or interaction plot with error bars
│       └── Complex → Small multiples (facet by one IV)
│
├── RELATIONSHIP between continuous variables
│   ├── 2 variables → Scatter plot with regression line and CI ribbon
│   ├── 3 variables (one categorical) → Scatter plot colored/faceted by group
│   ├── 3 variables (all continuous) → Bubble chart or contour plot
│   ├── Many variables → Correlation matrix heatmap or scatter plot matrix
│   └── Non-linear → LOESS smooth or spline with confidence band
│
├── COMPOSITION or PROPORTIONS
│   ├── 2-5 categories → Horizontal bar chart (never pie chart in science)
│   ├── Parts of a whole over time → Stacked area chart
│   ├── Proportional comparison → Diverging stacked bar (Likert-type)
│   └── Hierarchical composition → Treemap or nested bar chart
│
├── DISTRIBUTION of a single variable
│   ├── Continuous, unimodal → Histogram with density overlay
│   ├── Continuous, comparing groups → Overlaid density plots or ridge plot
│   ├── Small N, all points visible → Strip chart or beeswarm plot
│   └── Key summary only → Box plot or violin plot
│
├── CHANGE OVER TIME
│   ├── Few time points, few series → Line plot with points
│   ├── Many time points → Line plot without points (smooth)
│   ├── Many series → Small multiples (facet by series)
│   ├── Uncertainty over time → Line with CI ribbon
│   └── Irregular intervals → Line plot with varying point sizes
│
├── MODEL RESULTS
│   ├── Coefficients → Forest plot with CIs
│   ├── Prediction accuracy → Calibration plot or ROC curve
│   ├── Variable importance → Horizontal dot plot (Cleveland plot)
│   ├── Model comparison → Coefficient plot across models
│   └── Structural equation model → Path diagram with standardized coefficients
│
├── GEOGRAPHIC/SPATIAL
│   ├── Choropleth → Gradient-filled map (use perceptually uniform palette)
│   ├── Point locations → Dot density map
│   └── Flow/connection → Network or flow map
│
└── MULTIVARIATE
    ├── 3-5 variables → Parallel coordinates or radar chart
    ├── Many variables, reduce dimension → PCA biplot or t-SNE
    └── Clustering → Dendrogram or cluster scatter plot
```

---

## 2. Publication-Quality Figure Standards

### Resolution and Format
| Output | Resolution | Format | Notes |
|---|---|---|---|
| Print journal | 300-600 DPI | TIFF or EPS | Check journal requirements |
| Online-only journal | 150-300 DPI | PNG or SVG | SVG preferred for scalability |
| Presentation | 150 DPI | PNG or PDF | Wider aspect ratio |
| Supplementary | 150 DPI | PNG | May be lower quality |

### Size Standards
- Single column: 3.5 inches (89 mm) wide
- 1.5 column: 5.0 inches (127 mm) wide
- Double column: 7.0 inches (178 mm) wide
- Maximum height: 9.0 inches (229 mm)
- Maintain aspect ratios between 1:1 and 2:1

### Required Elements
1. **Figure number**: Bold, above the figure (e.g., "Figure 1")
2. **Caption below**: Starts with key takeaway, then describes what is shown
3. **Axis labels**: Descriptive, with units in parentheses
4. **Axis tick marks**: Pointing outward, at reasonable intervals
5. **Error bars**: Clearly defined in caption (SE vs 95% CI vs SD)
6. **Sample sizes**: Reported in caption or on figure
7. **Statistical annotations**: Asterisks with correction method noted, or exact p-values
8. **Legend**: Only if direct labeling is impossible; positioned to minimize whitespace

### Forbidden Elements
- 3D effects on 2D data (never use 3D bar charts)
- Pie charts (use bar charts instead; humans cannot compare angles accurately)
- Exploded pie charts (doubly forbidden)
- Redundant gridlines (use only if precise reading is needed)
- Decorative images or clip art
- Dual y-axes (use separate panels instead)
- Moiré patterns or cross-hatching (use solid fills or distinct patterns for B&W)
- Rainbow color scales (use viridis or other perceptually uniform scales)

---

## 3. Color Palette Recommendations

### Categorical Palettes (Colorblind-Safe)

**Okabe-Ito (Primary Recommendation for ≤8 categories):**
```
#E69F00 — Orange
#56B4E9 — Sky Blue
#009E73 — Bluish Green
#F0E442 — Yellow
#0072B2 — Blue
#D55E00 — Vermillion
#CC79A7 — Reddish Purple
#000000 — Black
```

**Wong Palette (Alternative):**
```
#000000 — Black
#E69F00 — Orange
#56B4E9 — Sky Blue
#009E73 — Green
#F0E442 — Yellow
#0072B2 — Blue
#D55E00 — Red
#CC79A7 — Pink
```

**IBM Design Library (for >8 categories):**
Use up to 12 colors with verified colorblind accessibility.

### Sequential Palettes (Continuous, Ordered)

| Palette | Best For | Light → Dark |
|---|---|---|
| Viridis | Default for most uses | Yellow → Dark purple |
| Plasma | High contrast needed | Pink → Yellow |
| Inferno | Dark backgrounds | Black → Yellow |
| Magma | Subtle, elegant | Black → Pink |
| Cividis | Blue-yellow colorblind optimized | Blue → Yellow |

### Diverging Palettes (Two Directions from Neutral)

| Palette | Neutral Center | Positive | Negative |
|---|---|---|---|
| RdBu | White | Red | Blue |
| PiYG | Light yellow | Pink | Green |
| PRGn | Light gray | Purple | Green |
| BrBG | Light tan | Brown | Teal |
| coolwarm | White | Red | Blue |

### Accessibility Testing Protocol
1. Run all figures through Coblis (colorblind simulator) or Color Oracle
2. Test for: Protanopia, Deuteranopia, Tritanopia, Achromatopsia
3. If any test fails: Replace palette, add pattern differentiation, or use direct labeling
4. Never rely solely on color to convey information; always add secondary encoding (shape, pattern, label)

---

## 4. Typography and Labeling Standards

### Font Hierarchy
| Element | Size (points) | Weight | Font |
|---|---|---|---|
| Figure title | 10-12 | Bold | Sans-serif (Helvetica/Arial) |
| Axis labels | 9-10 | Regular | Sans-serif |
| Tick labels | 8-9 | Regular | Sans-serif |
| Legend text | 8-9 | Regular | Sans-serif |
| Annotation text | 7-8 | Regular | Sans-serif |
| Statistical annotations | 7-8 | Bold | Sans-serif |

### Labeling Rules
1. **Axis labels**: Always horizontal; never rotate y-axis label (rotate tick labels instead if needed)
2. **Units**: Include in parentheses after axis label (e.g., "Reaction Time (ms)")
3. **Direct labeling**: Prefer over legends when possible; label directly on or next to data
4. **Abbreviations**: Define in caption if not defined in text; never use undefined abbreviations
5. **Numbers on axes**: Round to reasonable precision; avoid excessive decimals
6. **Zero baseline**: Always include zero for bar charts; for line charts, zero is optional but the y-axis range should not exaggerate small differences

### Annotation Placement
- Place significance brackets above compared groups
- Place effect sizes within or adjacent to the relevant comparison
- Place sample sizes in corners or as subtitle
- Avoid annotations that overlap data points
- Use leader lines for labels pointing to specific features

---

## 5. Statistical Annotation Standards

### Significance Stars (If Required by Journal)
| Symbol | Meaning | p-value range |
|---|---|---|
| ns | Not significant | p ≥ .05 |
| * | Significant | p < .05 |
| ** | Significant | p < .01 |
| *** | Significant | p < .001 |

**Note**: Always report exact p-values in the caption in addition to stars. Never use stars alone.

### Preferred: Exact p-Value Annotation
Instead of stars, annotate with exact values:
- "p = .032" or "p < .001"
- Place above bracket or comparison line
- More informative and recommended by APA 7th edition

### Effect Size Annotations
Always pair significance with effect size:
- "d = 0.65" next to comparison
- "η²_p = .12" in caption or annotation
- "R² = .34" visible on scatter plot

### Confidence Interval Display
- Show as error bars on bar/dot plots
- Show as shaded ribbon on line plots
- Show as horizontal bars on forest plots
- Always state in caption: "Error bars represent 95% CIs"

### Correction Method
When multiple comparisons are made, state the correction:
- "p-values adjusted using Bonferroni correction"
- "FDR-corrected using Benjamini-Hochberg procedure"
- "All p-values are two-tailed with Holm correction applied"

---

## 6. Figure Panel Composition Guidelines

### When to Use Panels
- Related analyses that tell a sequential story
- Same analysis across subgroups
- Model comparison or sensitivity analysis results
- Main figure + supplementary validation

### Panel Layout Principles
1. **Reading order**: Left-to-right, top-to-bottom (panels A, B, C, D)
2. **Shared axes**: Align axes across panels for easy comparison
3. **Shared legends**: One legend for all panels, not one per panel
4. **Consistent scale**: Same scale across panels unless variation is the point
5. **Panel labels**: Bold uppercase letters (A, B, C, D) in top-left corner
6. **White space**: 0.5-1.0 inches between panels; avoid cramped layouts

### Composite Figure Strategy
- **Main figures (3-5 in manuscript)**: Each tells one key part of the story
  - Figure 1: Overview / descriptive / main finding
  - Figure 2: Primary hypothesis test
  - Figure 3: Secondary analyses or interaction effects
  - Figure 4: Model results or mediation/moderation
  - Figure 5: Robustness or sensitivity analysis
- **Supplementary figures**: Supporting evidence, diagnostics, additional analyses

---

## 7. Table Design Standards

### Table vs Figure Decision
- Use a **table** when: exact values matter; readers need to look up specific numbers; few patterns to visualize
- Use a **figure** when: patterns, trends, or comparisons are the message; precise values are less important

### Table Anatomy
1. **Number and title**: Above the table, bold number, italicized descriptive title
2. **Column headers**: Clear, concise, with units; spanner headers for grouped columns
3. **Stub (leftmost column)**: Row labels, indented for hierarchy
4. **Body**: Numbers aligned on decimal point; same precision within columns
5. **Notes below**: General notes, specific notes (superscript letters), probability notes (*p < .05)

### Table Formatting Rules
- No vertical lines (only horizontal rules)
- Three rules minimum: top, below header, bottom
- Additional rules only to separate logical sections
- Numbers: Align on decimal; right-align integers; center text columns
- Blank cells: Never leave blank; use em-dash (—) for not applicable, "n/a" for not available
- Negative numbers: Use minus sign (−), not hyphen (-)
- Leading zeros: Include for values that can exceed 1 (0.52); omit for p-values in APA (p = .042)

### Descriptive Statistics Table Template

| Variable | n | M (SD) | Range | Skewness | Kurtosis |
|---|---|---|---|---|---|
| [Variable 1] | XX | XX.XX (X.XX) | XX.XX–XX.XX | X.XX | X.XX |
| [Variable 2] | XX | XX.XX (X.XX) | XX.XX–XX.XX | X.XX | X.XX |

### Correlation Table Template

| Variable | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1. [Variable 1] | — | | | |
| 2. [Variable 2] | .XX** | — | | |
| 3. [Variable 3] | .XX* | .XX** | — | |
| 4. [Variable 4] | −.XX | .XX* | .XX** | — |

*Note. N = XXX. *p < .05. **p < .01.*

---

## 8. Supplementary Figure Strategy

### What Goes in Supplementary
1. Assumption check plots (Q-Q plots, residual diagnostics)
2. Alternative model specifications
3. Subgroup analyses
4. Individual participant data (when feasible)
5. Full correlation matrices
6. Stimuli or apparatus images
7. Extended time series
8. Convergence diagnostics for Bayesian analyses
9. Sensitivity analysis plots
10. Full results tables that were summarized in main text

### Supplementary Figure Standards
- Same quality as main figures (reviewers notice)
- Self-contained: caption must be fully interpretable without main text
- Numbered S1, S2, S3...
- Referenced in main text at least once
- Include methodological details in caption if not in main methods

---

## 9. Software-Specific Guides

### Matplotlib (Python)

```python
import matplotlib.pyplot as plt
import matplotlib as mpl

# Publication-quality defaults
mpl.rcParams.update({
    'font.family': 'sans-serif',
    'font.sans-serif': ['Helvetica', 'Arial', 'DejaVu Sans'],
    'font.size': 10,
    'axes.labelsize': 10,
    'axes.titlesize': 12,
    'xtick.labelsize': 9,
    'ytick.labelsize': 9,
    'legend.fontsize': 9,
    'figure.dpi': 300,
    'savefig.dpi': 300,
    'savefig.bbox': 'tight',
    'axes.spines.top': False,
    'axes.spines.right': False,
})

# Colorblind-safe colors
OKABE_ITO = ['#E69F00', '#56B4E9', '#009E73', '#F0E442',
             '#0072B2', '#D55E00', '#CC79A7', '#000000']

# Example: Scatter plot with regression
fig, ax = plt.subplots(figsize=(3.5, 3))
ax.scatter(x, y, alpha=0.6, color=OKABE_ITO[0], edgecolor='white', s=40)
ax.plot(x_smooth, y_pred, color=OKABE_ITO[4], linewidth=1.5)
ax.fill_between(x_smooth, y_lower, y_upper, alpha=0.2, color=OKABE_ITO[4])
ax.set_xlabel('Variable X (units)')
ax.set_ylabel('Variable Y (units)')
ax.set_title('X Predicts Y in Sample', fontweight='bold')
fig.savefig('figure1.png', dpi=300)
```

### ggplot2 (R)

```r
library(ggplot2)
library(ggpubr)  # For publication-ready themes

# Publication-quality theme
theme_pub <- theme_minimal(base_size = 10, base_family = "Helvetica") +
  theme(
    panel.grid.minor = element_blank(),
    panel.grid.major = element_line(color = "grey90"),
    axis.text = element_text(size = 9, color = "black"),
    axis.title = element_text(size = 10, face = "bold"),
    plot.title = element_text(size = 12, face = "bold", hjust = 0),
    legend.position = "right",
    legend.key.size = unit(0.4, "cm"),
    plot.margin = margin(5, 5, 5, 5, unit = "pt")
  )

# Colorblind-safe scale
okabe_ito <- c("#E69F00", "#56B4E9", "#009E73", "#F0E442",
               "#0072B2", "#D55E00", "#CC79A7", "#000000")

scale_color_okabe <- function(...) scale_color_manual(values = okabe_ito, ...)
scale_fill_okabe <- function(...) scale_fill_manual(values = okabe_ito, ...)

# Example: Box plot with points
ggplot(data, aes(x = group, y = outcome, fill = group)) +
  geom_boxplot(width = 0.5, outlier.shape = NA, alpha = 0.7) +
  geom_jitter(width = 0.15, alpha = 0.5, size = 1.5) +
  scale_fill_okabe() +
  labs(x = "Condition", y = "Outcome Measure (units)",
       title = "Group Differences in Outcome") +
  theme_pub +
  guides(fill = "none")  # Direct labeling preferred
```

### seaborn (Python)

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Set publication defaults
sns.set_theme(
    style="ticks",
    font="Helvetica",
    font_scale=1.0,
    rc={
        'axes.spines.top': False,
        'axes.spines.right': False,
        'figure.dpi': 300,
        'savefig.dpi': 300,
    }
)

# Use colorblind palette
sns.set_palette(sns.color_palette("colorblind"))

# Example: Violin plot with individual points
fig, ax = plt.subplots(figsize=(3.5, 3))
sns.violinplot(data=df, x='group', y='outcome', inner=None, alpha=0.6, ax=ax)
sns.stripplot(data=df, x='group', y='outcome', color='black', alpha=0.4,
              size=3, jitter=0.2, ax=ax)
ax.set_xlabel('Condition')
ax.set_ylabel('Outcome Measure (units)')
ax.set_title('Distribution by Condition', fontweight='bold')
fig.savefig('figure2.png', dpi=300, bbox_inches='tight')
```

---

## 10. Common Visualization Mistakes and Corrections

### Mistake 1: Bar Charts for Small Samples
**Problem**: Bar charts hide the distribution and individual data points.
**Fix**: Use dot plots (Cleveland plots), strip charts, or box plots with jittered points.
**When bar charts are OK**: Large N (100+) where distribution shape is not of interest and mean comparison is the only goal.

### Mistake 2: Red-Green Color Scales
**Problem**: ~8% of males and 0.5% of females are red-green colorblind.
**Fix**: Use Okabe-Ito for categorical; viridis for sequential; RdBu for diverging.

### Mistake 3: Dual Y-Axes
**Problem**: Two scales on one plot allow manipulation of apparent relationships.
**Fix**: Use two separate panels, or normalize both series to the same scale.

### Mistake 4: Truncated Y-Axis on Bar Charts
**Problem**: Starting y-axis above zero exaggerates differences.
**Fix**: Always start bar chart y-axis at zero. If differences are genuinely small, use a dot plot or table instead.

### Mistake 5: 3D Charts
**Problem**: 3D distortion makes precise reading impossible and comparison inaccurate.
**Fix**: Always use 2D representations. If you need to show a third variable, use color, size, or faceting.

### Mistake 6: Pie Charts for Comparison
**Problem**: Humans cannot accurately compare angles or slice areas.
**Fix**: Use horizontal bar charts sorted by value. Use pie charts only for showing "part of whole" composition with 2-4 categories.

### Mistake 7: Overloaded Figures
**Problem**: Too many data series, annotations, or panels make the figure unreadable.
**Fix**: One message per figure. Split into multiple figures. Remove every element that does not serve the message.

### Mistake 8: Missing Error Bars
**Problem**: Without uncertainty representation, readers cannot assess precision.
**Fix**: Always show error bars (95% CI preferred over SE). Define in caption.

### Mistake 9: Non-Uniform Axis Scales Across Panels
**Problem**: Different scales in panels mislead comparison.
**Fix**: Use the same axis scale across all panels unless variation is explicitly the point (and note this in the caption).

### Mistake 10: Using Default Software Colors
**Problem**: Default matplotlib (tab10) and ggplot2 colors are not all colorblind-safe.
**Fix**: Always explicitly set a verified colorblind-safe palette.

### Mistake 11: Unclear Figure Captions
**Problem**: Captions that merely describe ("Bar chart of scores by group") rather than communicate the finding.
**Fix**: Captions should state the takeaway: "Treatment group outperformed control on primary outcome."

### Mistake 12: Legend-Dependent Figures
**Problem**: Forcing readers to look back and forth between legend and data.
**Fix**: Directly label data series on the plot when possible. Use legends only when direct labeling creates clutter.

### Pre-Submission Figure Checklist

- [ ] Every figure passes the 30-second test (core message is immediately clear)
- [ ] Colorblind-safe palette used and verified with simulator
- [ ] All axes labeled with units
- [ ] Error bars shown and defined in caption
- [ ] Statistical annotations include exact p-values (not just stars)
- [ ] Effect sizes reported in figure or caption
- [ ] Sample sizes stated in caption
- [ ] No chartjunk (gridlines, borders, 3D effects, decorative elements removed)
- [ ] Ink-to-data ratio maximized
- [ ] Caption states the key finding, not just describes content
- [ ] Resolution meets journal requirements (300+ DPI for print)
- [ ] Figure dimensions fit journal column width
- [ ] Consistent style across all figures in the manuscript
- [ ] All figures referenced in the main text
- [ ] Supplementary figures are self-contained with full captions
