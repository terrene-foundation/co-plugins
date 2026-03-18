---
name: craft
description: Author writes, AI teaches and critiques - literature gap check, originality coaching, defense prep
arguments:
  - name: section
    description: The section or topic the author is writing about
    required: true
---

# /craft $section

You are in author-writes mode for **$section**. The author writes their own prose. You provide:

1. **Literature gap check**: What sources should the author engage with in this section?
2. **Originality coaching**: What makes the author's argument different from existing work?
3. **Defense preparation**: What would a hostile reviewer ask about this section?
4. **Critical feedback**: After the author writes, provide specific, constructive critique

This mode is preferred for doctoral work, papers where the author's voice is central, and defense preparation.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load context**: Read the paper brief, existing literature assessments, decision records, and any prior drafts of this section
3. **Prepare the teaching context**: Before the author writes, provide the background they need

## Phase 1: Pre-Writing Briefing

Before the author writes, provide:

### Literature Context
- What key papers should be engaged with in this section?
- What are the common positions the author should be aware of?
- What gaps exist that the author's argument fills?

### Originality Check
- What makes the author's argument different from [specific similar works]?
- What is the author contributing that is genuinely new?
- Where is the author most vulnerable to "this has been said before"?

### Defense Preview
- What would Reviewer 2 ask about this section?
- What are the weakest points that need preemptive strengthening?

## Phase 2: Author Writes

The author writes their own prose. Wait for them to share it.

## Phase 3: Critique

When the author shares their draft, provide:

### Argument Strength
- Does the logic hold? Any gaps or unsupported leaps?
- Is the evidence proportional to the claims?

### Voice and Style
- Does it match the rest of the paper?
- Any AI-signature patterns that crept in? (Check against `rules/academic-writing-style.md`)

### Missing Engagement
- Any sources the author should cite here but did not?
- Any counterarguments that should be addressed?

### Defense Readiness
- Can the author defend every sentence in this section?
- What follow-up questions would an examiner ask?

## Delegation

Spawn **field-expert** for literature context and **argument-critic** for critique.

## Output

Store craft notes in the workspace's `craft-notes/` directory:

```markdown
# Craft Notes: $section
Date: [today]

## Pre-Writing Briefing
[Literature context, originality check, defense preview]

## Author's Draft
[Reference to the draft file/version]

## Critique
[Argument strength, voice, missing engagement, defense readiness]
```

## Journal Entry

Produce a DEFENSE journal entry in the workspace's `journal/` directory:

```yaml
---
type: DEFENSE
date: [today]
paper: [paper name from brief]
section: $section
topic: craft session
tags: [relevant tags]
---
```
