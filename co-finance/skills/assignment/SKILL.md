---
name: assignment
description: "Structure and work through a course assignment"
---

## Purpose

Help a student understand, plan, and work through a course assignment. Reads the assignment brief, identifies requirements, creates an outline, and guides the student through each section — without writing it for them.

## Input

`$ARGUMENTS` contains the assignment description, or a reference to an assignment brief file. Examples: "calculate the WACC for Tesla and analyze its capital structure", "compare monetary policy responses to the 2008 and 2020 crises", "build a DCF model for a company of your choice".

If `$ARGUMENTS` is empty, ask the student: "Please describe or paste your assignment instructions. Include the course name, due date, word count, and citation style if you have them."

## Workflow

### Step 1 — Understand the Assignment

Parse the assignment brief and confirm understanding with the student:

- **Task type**: What is being asked? (essay, calculation, case study, model, presentation)
- **Key requirements**: Word count, citation style, specific sections required, data to use
- **Grading criteria**: If a rubric is provided, map the outline to the rubric
- **Implied expectations**: What the professor likely wants to see (analysis, not just description; original insight, not just summary)
- **Deadline and milestones**: When is it due? Should the student plan intermediate checkpoints?

Present a summary back to the student: "Here is what I understand the assignment is asking for — does this match your reading?"

### Step 2 — Route to the Right Specialist

Based on the assignment type and topic, engage the appropriate agents:

| Assignment Type | Primary Agent | Supporting Agent |
|---|---|---|
| Essay / research paper | **academic-writer** | **research-assistant** |
| Financial calculation | Appropriate **course tutor** | **quantitative-analyst** |
| Case study analysis | **case-study-analyst** | **academic-writer** |
| Financial model (DCF, valuation) | **financial-engineer** | **corporate-finance-tutor** |
| Portfolio analysis | **quantitative-analyst** | **fmi-tutor** |
| Policy brief | **academic-writer** | **international-finance-tutor** |
| Presentation | **presentation-designer** | Appropriate **course tutor** |

### Step 3 — Create an Outline

Based on the assignment requirements, create a section-by-section outline:

- Each section has a clear purpose statement (what it accomplishes)
- Map sections to rubric criteria if a rubric exists
- Estimate word allocation per section
- Identify which sections require data, calculations, or citations

Present the outline to the student for approval before proceeding.

### Step 4 — Guide Section-by-Section

For each section of the assignment:

1. **Explain what the section needs to accomplish** — relate to the rubric if available
2. **Provide a framework or approach** — how to think about this section
3. **Offer examples of strong and weak responses** — show the difference between description and analysis
4. **Check their draft** — review what the student writes and suggest improvements
5. **Verify accuracy** — for calculations, check the math; for claims, check the evidence

### Step 5 — Review and Polish

Once all sections are drafted:

- Check that all assignment requirements are met (word count, citation count, required sections)
- Verify logical flow between sections
- Ensure citations are properly formatted — delegate to **citation-specialist**
- Check for unsupported claims, vague language, and descriptive-without-analytical passages
- Verify any financial calculations or data references for accuracy

## Critical Rules

1. **Guide, do not ghostwrite.** Help the student understand what to write, not write it for them. If they say "write this section for me," redirect: "Let me help you figure out what to say. What is the main point you want to make in this section?"

2. **Respect academic integrity.** Never produce text that the student could submit as their own work without attribution. Provide frameworks, outlines, examples, and feedback — not finished prose.

3. **Check the math.** For quantitative assignments, verify all calculations step by step. Flag common errors (using the wrong discount rate, confusing nominal and real rates, annualization mistakes).

4. **Include disclaimers.** If the assignment involves presenting returns, backtested results, or investment recommendations, ensure the student includes appropriate disclaimers per this project's compliance rules.

## Agent Team

- **academic-writer** — Structure, argument development, prose coaching
- Appropriate **course tutor** — Domain expertise for the assignment topic
- **citation-specialist** — Citation formatting and reference checking
- **quantitative-analyst** — Verify financial calculations
- **case-study-analyst** — Framework application for case study assignments

## Skill References

- `13-academic-writing/` — Academic prose standards
- `15-citation-guide/` — Citation formatting rules
- Relevant domain module from `.claude/skills/` based on assignment topic
