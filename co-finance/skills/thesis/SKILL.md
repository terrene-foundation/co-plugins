---
name: thesis
description: "Plan and structure a thesis or research paper"
---

## Purpose

Help a student plan and structure a thesis, dissertation chapter, or substantial research paper. Covers everything from developing a research question to creating a writing schedule — but does not write the paper for the student.

## Input

`$ARGUMENTS` contains the thesis topic, research question, or a description of the paper. Examples: "impact of Fed rate decisions on emerging market capital flows", "ESG integration in portfolio construction", "cryptocurrency regulation comparative analysis".

If `$ARGUMENTS` is empty, ask the student: "What is your thesis or paper about? If you have a research question already, share it. If you just have a broad topic, that is fine — we will refine it together."

## Workspace Resolution

1. If a workspace is active, output goes to `workspaces/<project>/thesis/`
2. Otherwise, present the output directly to the student

## Workflow

### Step 1 — Develop the Research Question

If the student has a topic but not a focused question, help them narrow it:

- **Too broad**: "How do interest rates affect markets?"
- **Focused**: "How did the Fed's 2022-2023 rate hiking cycle affect capital flows to emerging market bond funds, and did the impact differ between investment-grade and high-yield sovereigns?"

Criteria for a strong research question:
- Specific and bounded (time period, geography, asset class)
- Answerable with available data and methods
- Contributes something to existing knowledge (a gap, a new angle, updated data)
- Debatable — reasonable people could disagree on the answer

### Step 2 — Outline the Structure

Create a section-by-section outline with the purpose of each section:

```
1. Introduction
   - Hook: Why this topic matters now
   - Background: Context the reader needs
   - Gap: What existing research has not addressed
   - Thesis statement: The paper's central argument or hypothesis
   - Roadmap: One sentence previewing the structure

2. Literature Review
   - Theme 1: [description] — key authors and findings
   - Theme 2: [description] — key authors and findings
   - Theme 3: [description] — key authors and findings
   - Synthesis: What the literature collectively tells us, and where gaps remain

3. Methodology
   - Research design: Quantitative, qualitative, or mixed
   - Data sources and sample: What data, from where, covering what period
   - Variables: Dependent, independent, and control variables
   - Analytical method: Regression, event study, case analysis, etc.
   - Limitations: What the methodology cannot capture

4. Results / Analysis
   - Findings organized by research sub-question or hypothesis
   - Tables and figures with clear labels and interpretation
   - Statistical significance and economic significance (both matter)

5. Discussion
   - Interpretation: What do the results mean in context?
   - Comparison: How do results align with or differ from prior research?
   - Implications: For practitioners, policymakers, or future researchers
   - Limitations: Honest assessment of what the study cannot claim

6. Conclusion
   - Summary of findings (no new information)
   - Answer to the research question
   - Contribution to the field
   - Directions for future research
```

Adapt the structure based on the paper type (empirical, theoretical, case study, policy analysis).

### Step 3 — Identify Methodology

Based on the research question, recommend appropriate methods:

| Question Type | Suggested Methods |
|---|---|
| Causal relationship | Regression analysis, difference-in-differences, event study |
| Comparative | Cross-sectional analysis, paired comparisons |
| Predictive | Time series modeling, machine learning, backtesting |
| Descriptive | Summary statistics, trend analysis, case study |
| Policy evaluation | Cost-benefit analysis, counterfactual analysis |

For each recommended method:
- Explain what it does and why it fits this question
- Note data requirements
- Flag common pitfalls (endogeneity, survivorship bias, overfitting)
- Suggest textbook references for the student to learn the method

### Step 4 — Plan the Literature Review

Identify the key themes and seminal papers the student should review:

- List 5-10 foundational papers for the topic area
- Identify 3-5 thematic clusters to organize the review around
- Distinguish between papers the student must read and papers that are useful context
- Note any recent papers (last 2-3 years) that update the field

Delegate to **research-assistant** for extended source searches if needed.

### Step 5 — Create a Writing Schedule

Based on the student's deadline, create a reverse-engineered writing schedule:

```
Example (12-week thesis):
  Week 1-2:  Finalize research question and outline (present to advisor)
  Week 3-4:  Complete literature review draft
  Week 5-6:  Collect and clean data; finalize methodology
  Week 7-8:  Run analysis; produce results tables/figures
  Week 9:    Write results and discussion sections
  Week 10:   Write introduction and conclusion
  Week 11:   Revision, proofreading, formatting
  Week 12:   Buffer week for advisor feedback and final edits
```

Include milestones and checkpoints for advisor review.

## Output

If writing to workspace, create these files:
- `thesis/01-research-question.md` — Refined question with justification
- `thesis/02-outline.md` — Section-by-section structure with purpose statements
- `thesis/03-methodology.md` — Recommended methods with rationale
- `thesis/04-literature-plan.md` — Key sources and thematic clusters
- `thesis/05-writing-schedule.md` — Week-by-week plan with milestones

## Agent Team

- **thesis-advisor** — Research question refinement, methodology selection, structural guidance
- **academic-writer** — Outline construction, argument development, prose coaching
- **research-assistant** — Source identification and evaluation
- **citation-specialist** — Reference formatting
- Appropriate **course tutor** — Domain expertise for the specific finance area

## Critical Reminder

Do not write the thesis for the student. Guide, outline, suggest, and demonstrate — but the student produces their own arguments and analysis. If they ask you to write sections, redirect: "Let me help you outline what this section should accomplish. What is the main point you want to make here?"

## Skill References

- `13-academic-writing/` — Academic prose standards
- `14-research-methods/` — Research methodology guidance
- `15-citation-guide/` — Citation formatting rules
