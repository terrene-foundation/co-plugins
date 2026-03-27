---
name: research
description: "Start a structured research workflow for a finance topic"
---

## Purpose

Guide a student through a structured research workflow — from forming a research question to producing an annotated bibliography and synthesis. Designed for UG/PG finance students working on research papers, literature reviews, or thesis proposals.

## Input

`$ARGUMENTS` contains the research topic or question. Examples: "impact of ESG scores on stock returns", "central bank digital currencies and monetary policy", "dividend policy and firm value".

If `$ARGUMENTS` is empty, ask the student: "What topic or question would you like to research? This can be broad ('cryptocurrency regulation') or narrow ('how does Bitcoin halving affect altcoin prices?'). I will help you refine it."

## Workspace Resolution

1. If a workspace is active, output goes to `workspaces/<project>/research/`
2. Otherwise, present the output directly to the student

## Workflow

### Step 1 — Define the Research Question

Work with the student to sharpen a vague topic into a focused, answerable research question.

- Apply the PICO/FINER framework adapted for finance:
  - **P**opulation: Which market, firms, or time period?
  - **I**ntervention/Factor: What variable or event is being studied?
  - **C**omparison: What is the baseline or alternative?
  - **O**utcome: What is being measured?
- Test the question: Is it specific enough to research in a semester? Is it too narrow to find sources?
- Output: A refined research question with scope boundaries

### Step 2 — Identify Source Types Needed

Based on the research question, identify which types of sources the student should seek:

| Source Type | When to Use | Examples |
|---|---|---|
| Academic journals | Theory, empirical evidence | Journal of Finance, Review of Financial Studies |
| Working papers | Cutting-edge research not yet published | SSRN, NBER Working Papers |
| Textbooks | Foundational concepts and frameworks | Brealey/Myers, Hull, Damodaran |
| Industry reports | Practitioner perspectives, market data | McKinsey, IMF, World Bank |
| News/media | Current events, case context | Financial Times, WSJ, Bloomberg |
| Data sources | Empirical analysis | WRDS, FRED, Bloomberg Terminal, yfinance |

Recommend a minimum number of sources based on the assignment level (UG: 8-12, PG: 15-25).

### Step 3 — Evaluate Sources (CRAAP Test)

Teach the student to evaluate each source using the CRAAP framework:

- **C**urrency: When was it published? Is the data still relevant?
- **R**elevance: Does it directly address the research question?
- **A**uthority: Who wrote it? What are their credentials?
- **A**ccuracy: Is the methodology sound? Are claims supported?
- **P**urpose: Is the source objective, or does the author have an agenda?

Provide a template for source evaluation notes.

### Step 4 — Organize by Theme

Help the student organize sources into thematic clusters rather than a flat list.

- Identify 3-5 major themes or perspectives in the literature
- Map each source to one or more themes
- Identify gaps: Which themes have strong evidence? Where is more research needed?
- Note areas of agreement and disagreement among sources

### Step 5 — Synthesize Findings

Guide the student in writing a synthesis narrative:

- What does the literature collectively tell us about the research question?
- Where do scholars agree? Where do they disagree? Why?
- What methodological approaches dominate? Are there limitations?
- What gaps remain that the student's own research could address?

### Step 6 — Create Annotated Bibliography

For each source, produce:

```
Author(s). (Year). Title. Publication.
[Citation in the student's required format — delegate to citation-specialist]

Summary: 2-3 sentences describing the source's main argument and findings.
Evaluation: 1-2 sentences on the source's quality, methodology, and relevance.
Relevance: How this source contributes to the student's research question.
```

## Output

If writing to workspace, create these files:
- `research/01-research-question.md` — Refined question with scope
- `research/02-source-plan.md` — Types of sources needed and search strategy
- `research/03-source-evaluation.md` — CRAAP evaluations for each source
- `research/04-thematic-analysis.md` — Sources organized by theme
- `research/05-synthesis.md` — Narrative synthesis of findings
- `research/06-annotated-bibliography.md` — Formatted annotated bibliography

## Agent Team

- **research-assistant** — Literature search strategy, source identification, evaluation
- **citation-specialist** — Citation formatting, bibliography generation
- **academic-writer** — Synthesis writing, argument construction
- Appropriate **course tutor** — Domain expertise for evaluating source relevance

## Skill References

- `14-research-methods/` — Research methodology guidance
- `15-citation-guide/` — Citation formatting rules
- `13-academic-writing/` — Academic prose standards
