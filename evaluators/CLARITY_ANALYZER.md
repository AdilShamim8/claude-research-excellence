# Clarity Analyzer Rubric

## ✍️ SCIENTIFIC PROSE & ARCHITECTURE SCORING SYSTEM (0–100)

```
ACTIVATE: CLARITY_SCORE
```

This rubric evaluates the communicative power, narrative architecture, and readability of a scientific manuscript. It ensures prose achieves maximum clarity for editors, reviewers, and readers.

---

### Scoring Dimensions

#### DIMENSION 1 — HOURGLASS INFORMATION ARCHITECTURE (0–25)
*Evaluates macro-structure and the progressive transition between general context and specific findings.*

* **25 pts**: Flawless hourglass execution: Introduction transitions smoothly from broad significance to specific knowledge gap to exact RQ; Discussion expands symmetrically from principal finding to mechanisms to field-wide implications; zero non-sequiturs.
* **20 pts**: Strong structural hierarchy; gap is clearly articulated and answered; minor imbalance in breadth between introduction and discussion.
* **15 pts**: Standard paper structure followed; transition between broad context and specific contribution is somewhat abrupt; discussion summarizes results without fully contextualizing implications.
* **10 pts**: Inverted or fragmented structure; key motivation buried in mid-introduction; discussion repeats results without theoretical synthesis.
* **5 pts**: Highly disjointed narrative; paper reads as a collection of separate notes rather than a coherent scientific argument.
* **0 pts**: Total structural failure; reader cannot identify the central research question or principal takeaway.

#### DIMENSION 2 — PARAGRAPH COHESION & SENTENCE DYNAMICS (0–25)
*Evaluates micro-structure, topic sentences, given-new contract, and syntactic momentum.*

* **25 pts**: Every paragraph begins with a clear, functional claim (not generic background); sentences follow the Given-New contract (known information at the beginning, stress position at the end); active voice dominates (>80%); diverse sentence lengths create rhythmic cadence.
* **20 pts**: Consistent paragraph structure; clear transitions between sentences; high active voice ratio (>70%); occasional nominalization.
* **15 pts**: Paragraphs have identifiable topics but some drift into secondary points; transitions sometimes rely on mechanical connectors ("Moreover", "Furthermore"); moderate passive voice.
* **10 pts**: Frequent orphan sentences; paragraphs exceed 250 words with multiple competing ideas; heavy reliance on passive constructions.
* **5 pts**: Wall-of-text paragraphs; sentences consistently exceed 40 words with nested clauses; pervasive passive voice obscurity.
* **0 pts**: Incoherent phrasing, severe dangling modifiers, and broken syntactic logic that obscures meaning.

#### DIMENSION 3 — COGNITIVE LOAD & JARGON ECONOMY (0–25)
*Evaluates technical precision versus needless obfuscation.*

* **25 pts**: Complex concepts explained through intuitive structural analogies without sacrificing mathematical or empirical rigor; technical acronyms defined on first use and kept to essential minimum (<7 unique acronyms); zero scientific buzzwords / empty filler phrases.
* **20 pts**: Clear technical explanations; acronyms controlled; disciplined use of domain terminology; occasional specialized jargon that could be simplified.
* **15 pts**: Standard academic prose; relies somewhat on disciplinary shorthand; readable by domain specialists but impenetrable to adjacent fields.
* **10 pts**: Acronym soup (>15 acronyms); excessive nominalization (turning verbs into nouns: "conducted an investigation of" instead of "investigated"); high cognitive friction.
* **5 pts**: Pervasive obfuscation; dense jargon used as a substitute for clear thinking; reader must repeatedly re-read passages to decode meaning.
* **0 pts**: Incomprehensible technical jargon; pseudo-intellectual verbiage masking lack of substantive content.

#### DIMENSION 4 — FIGURE-TEXT INTEGRATION & CAPTION SELF-SUFFICIENCY (0–25)
*Evaluates multi-modal communication and graphic storytelling.*

* **25 pts**: Figures are entirely self-sufficient (a reader can understand the key message from the figure and caption alone without reading the main text); explicit declarative caption titles stating the finding; consistent visual grammar, palettes (colorblind-accessible), and typography matching text.
* **20 pts**: High-quality figures with informative captions; clear labels, legends, and error bar definitions; minor minor formatting discrepancies.
* **15 pts**: Standard figures with descriptive captions ("Figure 1: Results of Experiment 2"); requires reference to main text to fully interpret axes or abbreviations.
* **10 pts**: Low-contrast or cluttered figures; legends missing or unreadable at publication size; captions merely label axes without stating the finding.
* **5 pts**: Distorted aspect ratios, pixelated graphics, missing error bar explanations, or inaccessible color palettes (rainbow/jet).
* **0 pts**: Unreadable, mislabeled, or misleading graphics that actively confuse or contradict the text.

---

### Total Clarity Score Interpretation

| Score Band | Classification | Editorial Verdict | Actionable Prescription |
|---|---|---|---|
| **90–100** | **Prose Mastery** | Immediate editorial delight; effortless to read for multi-disciplinary editors | Paper is ready for submission; text serves as an exemplar for lab trainees |
| **75–89** | **Clear & Compelling** | Smooth review experience; reviewers focus entirely on science rather than expression | Polish paragraph topic sentences and convert remaining passive constructions |
| **60–74** | **Standard Academic** | Understandable but fatiguing; reviewers will ask for "editorial polishing" | Run `SKILL: WRITING_EXCELLENCE` (Abstract Mastery & Introduction Craft prompts) |
| **45–59** | **High Cognitive Friction** | Risk of reviewer misunderstanding leading to false technical objections | Ruthlessly cut acronyms, split compound sentences, and rewrite figure captions |
| **< 45** | **Obscure / Disorganized** | High probability of desk rejection due to unreadable presentation | Full manuscript rewrite required; restructure using CRES Hourglass Framework |
