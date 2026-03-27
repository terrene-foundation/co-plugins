---
name: review
description: "Peer review of academic writing for argument strength and citations"
---

## Purpose

Provide structured peer review feedback on academic writing — evaluating argument strength, evidence quality, citation accuracy, logical flow, and formatting compliance. Designed to help students improve their work before submission.

## Input

`$ARGUMENTS` contains a file path to the draft, or the student can paste their text directly. Examples: "review my essay in workspaces/thesis/drafts/chapter2.md", "review this paper on capital structure theory".

If `$ARGUMENTS` is empty, ask the student: "Please share the writing you would like reviewed. You can paste the text directly or point me to a file. Also let me know the citation style required (APA, Chicago, Harvard) and the assignment type (essay, thesis chapter, case study)."

## Workflow

### Step 1 — Read and Understand the Draft

- Read the entire document before making any comments
- Identify the paper type (essay, thesis chapter, case study, literature review, policy brief)
- Identify the thesis statement or central argument
- Note the citation style used
- Note the approximate word count and number of sources

### Step 2 — Evaluate Argument Strength

For each major section, assess:

**Thesis / Central Argument**
- Is there a clear, debatable thesis statement?
- Is the thesis specific enough to be tested or argued?
- Does the conclusion deliver on what the introduction promises?

**Evidence and Support**
- Is every claim supported by evidence (data, citation, or logical reasoning)?
- Are sources credible, current, and relevant?
- Is there a mix of source types (journals, data, industry reports)?
- Are there orphan statistics (numbers without source or context)?

**Analysis vs. Description**
- Does the student analyze (explain why and what it means) or just describe (summarize what happened)?
- Are findings interpreted, not just presented?
- Does the student explain the significance of each piece of evidence?

**Counterarguments**
- Does the paper acknowledge alternative perspectives?
- Are counterarguments addressed fairly, not straw-manned?
- Does the paper explain why its position is stronger despite counterarguments?

**Logical Flow**
- Does each paragraph follow logically from the previous one?
- Are transitions clear?
- Does the paper build toward its conclusion progressively?

### Step 3 — Check Citation Quality

Delegate detailed citation checking to **citation-specialist**, but flag:

- Missing citations for claims of fact
- In-text citations without corresponding reference list entries
- Reference list entries not cited in the text
- Inconsistent citation formatting
- Over-reliance on a single source
- Absence of seminal/foundational sources the topic demands

### Step 4 — Check Formatting and Compliance

- Does the paper follow the required citation style consistently?
- Are headings, tables, and figures properly formatted?
- Is the word count within range?
- For finance content: are disclaimers included where required?
- For quantitative content: are calculations documented with methodology?

### Step 5 — Produce Feedback Report

Structure the feedback as a clear, actionable report:

```
## Peer Review Feedback

### Overall Assessment
[1-2 paragraphs summarizing the paper's strengths and areas for improvement]

### Strengths
- [Specific things the paper does well — be precise, not generic]

### Areas for Improvement

#### Argument and Analysis
- [Specific issues with evidence, reasoning, or analysis depth]

#### Structure and Flow
- [Issues with organization, transitions, or logical progression]

#### Citations and Sources
- [Missing citations, formatting issues, source quality concerns]

#### Writing Quality
- [Clarity, precision, academic tone, jargon without definition]

### Specific Comments
[Line-by-line or paragraph-by-paragraph feedback on key issues]

### Recommended Next Steps
1. [Most important revision to make first]
2. [Second priority]
3. [Third priority]
```

## Critical Rules

1. **Be specific, not generic.** "Your argument is weak" is unhelpful. "In paragraph 3, you claim that diversification eliminates risk, but your source (Markowitz, 1952) actually says it eliminates unsystematic risk — this distinction matters for your argument" is useful.

2. **Balance criticism with recognition.** Always identify what the student is doing well before discussing what needs improvement. Students learn better when they know what to keep doing.

3. **Explain the why.** Do not just say "add more citations." Explain: "This paragraph makes three factual claims without sources. An academic reader will not accept these as established facts without evidence."

4. **Prioritize.** Not all issues are equally important. Clearly distinguish between critical revisions (these must change) and suggestions (these would improve the paper).

5. **Do not rewrite.** Identify problems and suggest approaches, but do not produce replacement text. The goal is to make the student a better writer, not to write for them.

## Agent Team

- **peer-reviewer** — Argument evaluation, logical flow analysis, feedback structure
- **citation-specialist** — Citation accuracy and formatting review
- **academic-writer** — Writing quality assessment, structural suggestions
- Appropriate **course tutor** — Domain expertise to verify financial accuracy

## Skill References

- `13-academic-writing/` — Academic prose standards
- `15-citation-guide/` — Citation formatting rules
