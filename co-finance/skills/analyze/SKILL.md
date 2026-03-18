---
name: analyze
description: "Load phase 01 (analyze) — research and analyze a topic before writing begins"
---

## What This Phase Does (present to student)

Research and analyze your topic in depth before any writing begins. We find relevant sources, identify key theories and debates, map out the literature, and build a clear picture of the intellectual landscape. Nothing gets drafted until this research is solid.

## Your Role (communicate to student)

Review our research findings and confirm the direction. You will see an overview of what the literature says, the key arguments and debates, where the gaps are, and a proposed structure for your work. Tell us if anything is off, missing, or if you want to take a different angle.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the student to create one first
4. Read all files in `workspaces/<project>/briefs/` for student context (this is the student's input surface — assignment description, research question, professor's requirements)

## Phase Check

- Output goes into `workspaces/<project>/01-analysis/`, `workspaces/<project>/02-plans/`, and `workspaces/<project>/03-structure/`

## Workflow

### 1. Understand the assignment or research question

Before diving into research, clarify:

- What exactly is the assignment asking? (essay, case study, thesis, presentation, problem set)
- What is the research question or topic?
- What course is this for, and what level? (introductory, intermediate, advanced, graduate)
- Are there specific requirements from the professor? (length, sources, format, methodology)
- What is the deadline?

### 2. Deep research: find relevant sources, theories, and data

Document findings in detail in `workspaces/<project>/01-analysis/01-research`.

- Use as many subdirectories and files as required
- Name them sequentially as 01-, 02-, etc, for easy referencing
- Identify seminal papers, textbooks, and key authors in the field
- Find relevant empirical data, case studies, and real-world examples
- Note competing theories, schools of thought, and ongoing debates
- Locate relevant financial data sources (FRED, World Bank, Bloomberg, etc.)

### 3. Organize: identify key themes, debates, and gaps

Analyze the research to find structure:

- What are the major themes and arguments in the literature?
- Where do scholars agree, and where do they disagree?
- What gaps exist in the current research?
- What theoretical frameworks are most relevant?
- What evidence is strongest for different positions?
- What counterarguments must be addressed?

### 4. Create outline: structure the argument or analysis

Build a proposed structure for the student's work:

- Thesis statement or central argument (for essays and papers)
- Logical flow of sections — each building on the previous
- Which evidence and sources support each section
- Where data analysis or calculations are needed
- How counterarguments will be addressed
- Proposed conclusion and implications

Document the outline in `workspaces/<project>/02-plans/` and the detailed section structure in `workspaces/<project>/03-structure/`.

### 5. Red team: check for gaps in research

Review the analysis critically:

- Are there gaps in the research — important perspectives or sources we missed?
- Is the proposed argument logically sound?
- Are there weak points a professor would challenge?
- Is the evidence sufficient for each major claim?
- Does the structure flow logically from introduction to conclusion?
- Are the sources credible and appropriately academic?

### 6. Present findings to the student

Summarize the research in plain language. Cover:

- **Your topic** — one paragraph restating the research question and why it matters
- **What the literature says** — the major arguments, theories, and findings
- **Key debates** — where scholars disagree and what the evidence supports
- **Proposed approach** — how we suggest structuring your paper or project, and why
- **Sources collected** — an overview of the key sources found and their relevance
- **Gaps and considerations** — anything that needs more research or where you will need to make judgment calls

Ask the student: "Does this cover your topic? Is the direction right? Anything we should add, remove, or rethink?"

## Agent Teams

Deploy these agents as a team for analysis:

- **research-assistant** — Find sources, evaluate credibility, organize literature
- **deep-analyst** — Identify gaps in arguments, assess complexity, spot weak reasoning
- **assignment-analyst** — Break down assignment requirements, ensure all rubric criteria are addressed
- **concept-explainer** — Explain complex finance theories and concepts the student encounters during research

For finance-specific analysis, additionally deploy as needed:

- **quantitative-analyst** — For topics involving portfolio theory, risk metrics, or optimization
- **financial-engineer** — For topics involving valuation, derivatives, or financial modeling
- **curriculum-designer** — For understanding the pedagogical context and learning objectives

Red team the analysis with agents until they confirm no gaps remain in research, structure, and source coverage.
