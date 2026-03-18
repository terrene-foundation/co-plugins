---
name: write-para
description: AI drafts a paragraph with margin notes; author must approve before moving on
arguments:
  - name: intent
    description: What this paragraph should accomplish in the argument
    required: true
---

# /write-para $intent

You are drafting a paragraph that should accomplish: **$intent**

This is the AI-drafts mode. You write the paragraph with inline margin notes explaining every structural choice. The author reviews, edits, and must explicitly approve before you move on.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load context**: Read the paper brief, existing drafts in `03-drafts/versions/`, relevant decision records, and the current section's preceding paragraphs
3. **Check voice**: Read existing approved paragraphs to match the author's established voice, register, and style

## Drafting Requirements

### Margin Notes
Every draft paragraph MUST include inline annotations in [MARGIN: ...] format explaining:
- Why this sentence is here
- Why this word/phrase was chosen over alternatives
- How this connects to the broader argument
- What a reviewer might think of this

### Writing Style
Follow all rules in `rules/academic-writing-style.md`:
- No em dashes
- No AI-signature words
- Vary sentence length
- Active voice for author claims
- First person for the author's contributions
- Domain-specific vocabulary
- Allow natural roughness

### Alternatives
For at least 2 key decisions in the paragraph, present alternatives:
- "Alternative A: [different phrasing] -- [why you might prefer this]"
- "Alternative B: [different phrasing] -- [why you might prefer this]"

## Author Approval Gate

After presenting the draft:

1. Ask if the paragraph accomplishes its intent
2. Ask if the voice matches the rest of the paper
3. Ask if any margin note decisions should be changed
4. **Do NOT proceed to the next paragraph without explicit approval**

## Delegation

Spawn the **writing-partner** agent for the drafting work.

## Journal Entry

Produce a MARGIN journal entry in the workspace's `journal/` directory:

```yaml
---
type: MARGIN
date: [today]
paper: [paper name from brief]
section: [current section]
paragraph: [paragraph number]
topic: $intent
tags: [relevant tags]
---
```

Include: key decisions made, alternatives rejected, voice notes.
