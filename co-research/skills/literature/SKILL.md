---
name: literature
description: Systematic literature search and structured assessment
arguments:
  - name: topic
    description: The topic or research question to survey
    required: true
---

# /literature $topic

You are conducting a systematic literature search on **$topic**. The goal is to find, assess, and synthesize the relevant scholarly literature, identifying what exists, what is missing, and how it connects to the researcher's argument.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load context**: Read the paper brief and existing literature notes in `01-analysis/literature/`
3. **Check for existing coverage**: Search for prior LITERATURE journal entries on this topic

## Search Strategy

### Phase 1: Broad Discovery
- Search for the topic across academic databases, arXiv, Google Scholar, SSRN
- Identify seminal works, recent surveys, and meta-analyses
- Note the key authors and research groups working on this topic

### Phase 2: Citation Chain Following
- Follow backward citations (what do key papers cite?)
- Follow forward citations (what cites key papers?)
- Identify the intellectual lineage of the main arguments

### Phase 3: Gap Identification
- What questions remain open in the literature?
- Where does the researcher's work make a novel contribution?
- What would a reviewer expect to see cited that is currently missing?

## Delegation

Spawn the **literature-researcher** agent to conduct the search. The agent will produce structured paper assessments.

## Output

### Literature Assessment File

Create a structured assessment in `01-analysis/literature/` named `[topic-slug].md`:

```markdown
# Literature Assessment: $topic

## Search Strategy
[What was searched and how]

## Key Papers

### [Author (Year)] - [Title]
- **Says**: [Key argument]
- **Does NOT say**: [Common misinterpretation]
- **Method**: [Research approach]
- **Relevance**: [Connection to our paper]
- **Confidence**: [High/Medium/Low]

## Themes
[Thematic synthesis across papers]

## Gaps
[What the literature does not address that our paper can]

## Reviewer Expectations
[Papers a reviewer would expect to see cited]
```

### Journal Entry

Produce a LITERATURE journal entry in the workspace's `journal/` directory:

```yaml
---
type: LITERATURE
date: [today]
paper: [paper name from brief]
topic: $topic
tags: [relevant tags]
---
```

Include: papers found, key themes, gaps identified, and implications for the paper.
