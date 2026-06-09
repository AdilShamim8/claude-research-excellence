# Citation Network Analysis

## A Framework for Mapping the Intellectual Structure of Research Fields Through Bibliometric Methods

### Purpose
This prompt provides a comprehensive framework for analyzing citation networks — the web of references that connects research publications. Citation network analysis reveals the invisible structure of intellectual influence: which works shape fields, which ideas cluster together, and where emerging trends are forming. It complements traditional literature review by providing quantitative evidence for claims about field structure, influence, and evolution.

---

## SECTION 1: BIBLIOMETRIC ANALYSIS FRAMEWORK

### 1.1 Data Collection for Bibliometric Analysis

**Required data fields for each publication:**
- Title, authors, year, journal, volume, issue, pages
- Abstract and keywords
- Reference list (cited references)
- Times cited (citation count)
- Document type (article, review, conference paper, etc.)

**Primary data sources:**
- **Web of Science (Clarivate):** Gold standard for citation data; covers 21,000+ journals; citation tracking from 1900
- **Scopus (Elsevier):** Broader coverage than WoS (25,000+ journals); better for recent publications and non-English journals
- **Dimensions (Digital Science):** Broadest coverage; includes grants, patents, and clinical trials alongside publications
- **OpenAlex:** Open-source; covers 250M+ works; good for large-scale analysis without subscription barriers
- **Semantic Scholar:** Free API; good for computer science and biomedical literature

**Data quality checklist:**
- [ ] Export includes all relevant document types (articles, reviews, conference papers)
- [ ] Date range is appropriate for the research question
- [ ] Author name disambiguation has been addressed (common problem: multiple authors with same initials/surname)
- [ ] Duplicate records have been removed
- [ ] Citation data is current (citations change over time)

### 1.2 Descriptive Bibliometric Indicators

**Publication-level indicators:**
- **Total citations:** Sum of all citations received (raw impact measure)
- **Average citations per year:** Normalizes for age of publication
- **Citations per year in last 5 years:** Measures current relevance (distinguishes legacy citations from ongoing influence)
- **Field-normalized citation score:** Compares a publication's citations to the average for its field and year (e.g., Field Citation Ratio)
- **Journal Impact Factor of publishing journal:** Proxy for visibility and selectivity

**Author-level indicators:**
- **h-index:** Maximum h such that h publications have ≥ h citations (balances productivity and impact)
- **h-index variants:** g-index (accounts for citation tail), i10-index (Google Scholar; publications with ≥10 citations)
- **Author Impact Factor:** Average citations per publication per year
- **Fractional citation count:** Divides citation credit among co-authors (addresses hyperauthorship)

**Journal-level indicators:**
- **Journal Impact Factor (JIF):** Average citations per article in the last 2 years (Clarivate)
- **CiteScore:** Average citations per article in the last 4 years (Scopus)
- **Source Normalized Impact per Paper (SNIP):** Contextualizes impact by subject field
- **SCImago Journal Rank (SJR):** Combines citations with journal prestige weighting

### 1.3 Field-Level Indicators

- **Total publications per year:** Measures field growth
- **Average citations per publication:** Measures field impact
- **Collaboration index:** Average number of authors per publication
- **International collaboration rate:** Percentage of publications with authors from multiple countries
- **Concentration ratio:** Percentage of citations going to the top 1% of publications (measures citation inequality)

---

## SECTION 2: CO-CITATION ANALYSIS METHODOLOGY

### 2.1 Concept

Co-citation analysis measures how often two documents are cited together by subsequent publications. Two documents that are frequently co-cited are likely to be conceptually related, even if they do not cite each other. Co-citation clustering reveals the intellectual structure of a field — its "invisible colleges" and research fronts.

### 2.2 Procedure

**Step 1: Build the Co-citation Matrix**
- Extract all cited references from the documents in your corpus
- For each pair of cited references, count how many citing documents reference both
- Result: A symmetric N × N matrix where N = number of unique cited references and cells = co-citation frequency

**Step 2: Normalize the Co-citation Matrix**
- Raw co-citation counts are influenced by the individual citation counts of each reference (highly cited papers co-cite more by chance)
- Apply normalization: Pearson correlation, cosine similarity, or Jaccard index
- Pearson correlation is most common: converts raw frequencies to correlation coefficients between -1 and +1

**Step 3: Apply Clustering/Scaling**
- **Multidimensional scaling (MDS):** Projects the co-citation matrix into 2D or 3D space; documents that are frequently co-cited appear close together
- **Hierarchical cluster analysis:** Groups documents into a tree structure; documents in the same cluster are conceptually related
- **Factor analysis / PCA:** Identifies underlying dimensions that explain the co-citation pattern; each factor represents a research theme

**Step 4: Interpret Clusters/Factors**
- For each cluster, identify the most central (highest co-citation frequency) and most representative documents
- Label each cluster based on the common theme of its constituent documents
- Map clusters to research streams, theoretical traditions, or methodological approaches

**Step 5: Temporal Analysis**
- Repeat the co-citation analysis for different time windows (e.g., 5-year slices)
- Track how clusters emerge, merge, split, or disappear over time
- Identify the intellectual trajectory of the field

### 2.3 Co-citation Variants

| Type | What It Analyzes | What It Reveals |
|------|-----------------|-----------------|
| **Document co-citation** | Pairs of cited documents | Intellectual structure of the field's knowledge base |
| **Author co-citation** | Pairs of cited authors | Intellectual schools of thought and theoretical traditions |
| **Journal co-citation** | Pairs of cited journals | Disciplinary boundaries and cross-disciplinary connections |

### 2.4 Output Format

```markdown
## Co-citation Analysis Results

### Cluster 1: [LABEL] (N documents, % of total co-citations)
- **Central documents:** [Top 5 most co-cited within this cluster]
- **Representative authors:** [Authors most frequently associated with this cluster]
- **Key journals:** [Journals most frequently associated with this cluster]
- **Interpretation:** [What intellectual tradition or research theme does this cluster represent?]

### Cluster 2: [LABEL]
[Same structure]

### Cross-Cluster Connections
[Which clusters are most frequently connected by co-citation? What do these connections represent?]

### Temporal Evolution
[How have clusters changed over time?]
```

---

## SECTION 3: BIBLIOGRAPHIC COUPLING

### 3.1 Concept

Bibliographic coupling measures the similarity of two documents based on their shared references. Two documents that cite many of the same sources are bibliographically coupled. Unlike co-citation (which links cited documents), bibliographic coupling links citing documents — it reveals current research fronts rather than historical knowledge bases.

### 3.2 Procedure

**Step 1: Build the Coupling Matrix**
- For each pair of citing documents, count the number of shared references
- Coupling strength = number of shared references (can be normalized by total references)

**Step 2: Normalize**
- Raw coupling counts favor documents with longer reference lists
- Apply Jaccard coefficient: |A ∩ B| / |A ∪ B| (shared references / total unique references)
- Or Salton's cosine: |A ∩ B| / √(|A| × |B|)

**Step 3: Cluster**
- Apply the same clustering methods as co-citation analysis (MDS, hierarchical clustering, modularity-based community detection)
- Documents in the same cluster share similar intellectual foundations and likely address similar research questions

### 3.3 Co-citation vs. Bibliographic Coupling: When to Use Each

| Feature | Co-citation Analysis | Bibliographic Coupling |
|---------|---------------------|----------------------|
| **Links** | Cited documents (older, foundational) | Citing documents (newer, current) |
| **Reveals** | Knowledge base / intellectual structure | Research fronts / current themes |
| **Temporal focus** | Historical | Contemporary |
| **Stability** | More stable over time (accumulates citations) | Changes as new publications emerge |
| **Best for** | Mapping theoretical traditions | Identifying emerging research clusters |
| **Data requirement** | Larger corpus needed for stability | Works with smaller corpora |

### 3.4 Combined Approach
For the most complete picture, run both co-citation and bibliographic coupling analyses:
- Co-citation reveals what the field's knowledge is built upon (the foundation)
- Bibliographic coupling reveals what the field is currently working on (the frontier)
- The relationship between the two reveals whether current research is building on established foundations or diverging from them

---

## SECTION 4: CITATION NETWORK VISUALIZATION APPROACHES

### 4.1 Network Construction

**Nodes:** Publications, authors, or journals
**Edges:** Citation links (directed: A cites B) or co-citation/coupling links (undirected)
**Edge weights:** Citation frequency, co-citation frequency, or coupling strength

### 4.2 Visualization Tools

| Tool | Strengths | Limitations |
|------|-----------|-------------|
| **VOSviewer** | User-friendly; excellent for bibliometric maps; supports co-citation, coupling, co-authorship, keyword co-occurrence; produces publication-quality visualizations | Limited to VOSviewer-specific analyses; less flexible than programming approaches |
| **CiteSpace** | Powerful temporal analysis; identifies burst citations and turning points; generates timeline and timezone visualizations | Steep learning curve; interface can be confusing; requires Java |
| **Gephi** | General network analysis; highly customizable visualizations; supports various layout algorithms; open-source | Not bibliometric-specific; requires manual data preparation; large networks can be slow |
| **Bibliometrix (R)** | Fully programmable; integrates with R ecosystem; reproducible analyses; comprehensive bibliometric functions | Requires R programming knowledge; visualization quality depends on user skill |
| **Python (NetworkX + Matplotlib/Plotly)** | Maximum flexibility; integrates with data science workflows; supports custom analyses | Requires significant programming; no built-in bibliometric functions |

### 4.3 Visualization Design Principles

1. **Node size:** Proportional to citation count, betweenness centrality, or burst weight
2. **Node color:** Represents cluster membership (modularity class), time period, or journal
3. **Edge thickness:** Proportional to co-citation frequency or coupling strength
4. **Layout algorithm:**
   - **Force-directed (e.g., Fruchterman-Reingold):** Natural clustering; good for exploratory visualization
   - **VOS mapping:** Optimized for bibliometric data; minimizes overlapping labels
   - **Kamada-Kawai:** Preserves graph-theoretic distances; good for structural analysis
5. **Label placement:** Only label the most significant nodes (top 20–50 by centrality or citation count) to avoid visual clutter
6. **Temporal overlay:** Use color gradients or animation to show how the network evolves over time

### 4.4 Reading a Citation Network Map

- **Dense clusters** represent established research traditions with coherent knowledge bases
- **Sparse regions** represent emerging areas where the intellectual structure is not yet formed
- **Bridge nodes** (high betweenness centrality) connect otherwise separate clusters and often represent interdisciplinary or integrative work
- **Peripheral nodes** may be irrelevant or may be early indicators of emerging trends
- **Hub nodes** (high degree centrality) are the most-cited works that define the field's core

---

## SECTION 5: IDENTIFYING INFLUENTIAL WORKS AND CLUSTERS

### 5.1 Centrality Measures for Identifying Influence

| Measure | What It Captures | Interpretation |
|---------|-----------------|----------------|
| **Degree centrality** | Number of direct citation connections | Most directly connected works; the field's most referenced publications |
| **Betweenness centrality** | Frequency of lying on the shortest path between other nodes | Works that bridge different research areas; intellectual gatekeepers |
| **Closeness centrality** | Average distance to all other nodes | Works that are central to the entire network's flow of information |
| **Eigenvector centrality** | Connectedness to other well-connected nodes | Works that are influential within the most influential cluster |
| **PageRank** | Recursive measure of importance based on the importance of citing works | Works cited by other highly cited works; quality-weighted influence |

### 5.2 Citation Bursts

**Concept:** A citation burst occurs when a publication suddenly receives a dramatic increase in citations over a short period, indicating that it has become a focal point of research attention.

**Detection method:** Kleinberg's burst detection algorithm (implemented in CiteSpace)
- Identifies the time period during which a publication's citation rate is significantly higher than expected
- Burst strength indicates the magnitude of the deviation from baseline
- Burst onset indicates when the publication became influential

**Interpretation:**
- A burst in a foundational paper → The field is experiencing a theoretical renaissance or controversy
- A burst in a recent paper → A new idea is rapidly gaining traction
- Multiple bursts in the same time period → A research frontier is forming
- A burst followed by rapid decline → A fad or methodological fashion

### 5.3 Research Front Identification

**Method:** Price's clustering of citing documents
1. Identify the most recent publications (current research front)
2. Cluster them by bibliographic coupling
3. Each cluster represents a current research front
4. Trace each cluster back to its foundational documents via co-citation

**Alternative:** Characteristic scaling (Small's approach)
1. Identify highly co-cited pairs of documents (high co-citation frequency)
2. Expand outward from these pairs to identify co-citation clusters
3. Each cluster is a "research specialty"

---

## SECTION 6: DETECTING EMERGING TRENDS THROUGH CITATION PATTERNS

### 6.1 Leading Indicator Metrics

**1. Citation acceleration:** The second derivative of citation count (is the rate of citation increase itself increasing?)
- Compute: Compare the citation growth rate in the last 2 years vs. the previous 2 years
- Positive acceleration → Emerging trend
- Negative acceleration → Declining interest

**2. Cross-disciplinary citation inflow:** Is a publication or cluster receiving increasing citations from outside its traditional discipline?
- Compute: Track the proportion of citations from journals outside the core field
- Increasing cross-disciplinary inflow → The idea is being adopted by new communities (often precedes a breakthrough)

**3. Recent-first citation ratio:** What proportion of a cluster's citations come from publications in the last 2 years?
- High ratio → Active, growing research area
- Low ratio → Established but possibly stagnating area

**4. Author migration patterns:** Are prominent researchers from other fields beginning to publish in this area?
- Track author publication histories to detect field-switching
- Author migration often precedes methodological innovation (they bring methods from their home field)

**5. Keyword emergence:** Are new keywords appearing in the titles and abstracts of citing documents?
- Compute keyword frequency over time; identify terms with the steepest growth curves
- New keywords often name new concepts before they become established research streams

### 6.2 Trend Classification

| Trend Type | Indicators | Interpretation |
|-----------|-----------|----------------|
| **Emerging** | High citation acceleration; increasing cross-disciplinary inflow; new keywords | A new research stream is forming |
| **Growing** | Steady citation acceleration; expanding author base; increasing publication volume | An established stream gaining momentum |
| **Mature** | Stable citation rates; large author base; few new keywords | An established stream; likely to produce incremental advances |
| **Declining** | Negative citation acceleration; author outmigration; decreasing publication volume | A stream losing relevance or being superseded |
| **Cyclical** | Periodic bursts of citation activity | A stream that revives in response to external events |

### 6.3 Trend Validation Protocol

Before claiming an emerging trend:
1. **Statistical significance:** Is the citation acceleration greater than expected by chance? (Use Poisson regression on citation counts over time)
2. **Replication across databases:** Does the trend appear in both Web of Science and Scopus?
3. **Substantive basis:** Is there a theoretical or practical reason for the trend, or is it a statistical artifact?
4. **Sustainability:** Has the trend persisted for at least 2 years, or is it a single-year spike?
5. **Independent confirmation:** Do content analysis and expert interviews support the bibliometric finding?

---

## SECTION 7: JOURNAL INFLUENCE MAPPING

### 7.1 Journal Citation Network Analysis

**Purpose:** Map which journals cite which other journals to reveal the flow of intellectual influence across publications.

**Procedure:**
1. Construct a directed journal-journal citation matrix (Journal A cites Journal B: X times)
2. Normalize by the total citations from each journal
3. Apply network analysis to identify:
   - **Core journals:** High in-degree and out-degree (both cited and citing widely)
   - **Source journals:** High out-degree, low in-degree (export ideas but don't import)
   - **Sink journals:** High in-degree, low out-degree (import ideas but don't export)
   - **Bridge journals:** High betweenness centrality (connect otherwise separate journal clusters)

### 7.2 Journal Landscape Mapping

**Bradford's Law application:**
- Rank journals by the number of relevant articles they publish
- Divide into three zones:
  - Zone 1 (core): Small number of journals publishing the most relevant articles
  - Zone 2 (related): Moderate number of journals with some relevant articles
  - Zone 3 (peripheral): Large number of journals with few relevant articles
- Focus search and monitoring efforts on Zone 1 journals

**Journal cluster interpretation:**
- Journals that cite each other heavily form a disciplinary cluster
- Journals that bridge clusters serve as interdisciplinary conduits
- The position of a journal in the network predicts its role in disseminating findings

---

## SECTION 8: AUTHOR INFLUENCE AND COLLABORATION NETWORKS

### 8.1 Author Influence Mapping

**Identify key authors by:**
- **Total citation count:** Overall impact (but skewed by a few highly cited papers)
- **h-index:** Balanced productivity and impact
- **Adjusted citation count:** Fractional counting by co-author position
- **First-author citation count:** Measures independent contribution
- **Mentorship index:** Number of former trainees who have become independent, cited researchers

### 8.2 Co-authorship Network Analysis

**Network construction:**
- Nodes = authors
- Edges = co-authored publications
- Edge weight = number of co-authored publications

**Analysis:**
- **Giant component:** The largest connected subgraph — represents the field's collaborative core
- **Isolates:** Authors who publish alone or only with fixed collaborators — may represent independent or peripheral researchers
- **Clustering coefficient:** Measures the tendency of an author's collaborators to collaborate with each other (high clustering = close-knit research group; low clustering = broker between groups)
- **Betweenness centrality:** Identifies authors who connect different collaborative communities — these are intellectual brokers

### 8.3 Collaboration Dynamics

**Track over time:**
- **Network density:** Is the field becoming more or less collaborative?
- **Average path length:** Is the field becoming a small world (any two researchers connected through few intermediaries)?
- **Modularity:** Is the field fragmenting into insular groups or integrating across boundaries?
- **International collaboration rate:** Is the field globalizing?
- **Inter-institutional collaboration rate:** Are institutional boundaries becoming more porous?

### 8.4 Invisible College Detection

**Concept:** Derek Price identified "invisible colleges" — small groups of researchers who communicate directly and frequently, shaping the direction of a field before their work appears in formal publications.

**Detection method:**
1. Identify the most productive authors in the field (top 20 by publication count)
2. Map their co-authorship and co-citation networks
3. Identify dense subgraphs within this elite network
4. These subgraphs represent invisible colleges — groups that set the field's research agenda

**Interpretation:**
- Invisible colleges are not inherently problematic, but they can create echo chambers
- Understanding who belongs to which invisible college helps anticipate which research directions will be promoted and which will be overlooked
- If invisible colleges correlate with geographic or institutional boundaries, the field may suffer from parochialism

---

## OUTPUT FORMAT

```markdown
# Citation Network Analysis Report

## 1. Descriptive Bibliometrics
- Total publications analyzed: [N]
- Date range: [YYYY–YYYY]
- Top 10 most-cited works: [Table]
- Publication growth trend: [Description]
- Key journals (Zone 1): [List with impact factors]

## 2. Co-citation Analysis
- Number of clusters identified: [N]
- Cluster descriptions: [For each cluster: label, central documents, interpretation]
- Cross-cluster connections: [Bridge documents and what they connect]

## 3. Bibliographic Coupling
- Current research fronts: [Number and description]
- Emerging clusters: [Identified by recent publications]

## 4. Influential Works
- Top 10 by betweenness centrality: [List]
- Top 10 by citation burst: [List with burst periods]
- Foundational works (high eigenvector centrality): [List]

## 5. Emerging Trends
- Trend classification: [Emerging/Growing/Mature/Declining for each cluster]
- Validation status: [Which trends pass the 5-point validation]

## 6. Journal Map
- Core journals: [Zone 1]
- Bridge journals: [High betweenness]
- Journal clusters: [Description]

## 7. Author Network
- Key authors: [Top 10 by influence metrics]
- Invisible colleges: [Detected groups]
- Collaboration trends: [Density, internationalization, modularity over time]

## 8. Implications for Literature Review
- Which works must be cited (foundational + central)
- Which emerging trends should be acknowledged
- Which invisible colleges' perspectives may be underrepresented
- Which journals to monitor for new developments
```
