---
name: teach
description: "Explain a concept, paper, or field area in depth. Research tutor mode."
---

## What This Command Does (present to user)

Deep-dive into an academic concept, paper, or field area. You'll get the full context: what it means, who disagrees, how it connects to your argument, and what reviewers would expect you to know.

## Your Role (communicate to user)

Listen, ask questions, push back. This is a teaching conversation — if something doesn't make sense, say so. By the end, you should be able to explain this concept to a reviewer.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store teaching notes in `workspaces/<project>/01-analysis/literature/`

## Workflow

### 1. Parse the topic

Extract the concept, paper, or field area from `$ARGUMENTS`.

### 2. Teach with depth

Delegate to **field-expert** agent. The teaching must include:

- **Historical context** — When and why this work emerged
- **Core argument** — What it actually says (not what people think)
- **Key debates** — Who disagrees and why
- **Common miscitations** — How this is frequently misused
- **Connection to your paper** — How this relates to the user's research
- **Gap alert** — "If you cite X, expect reviewers to also want Y"

### 3. Find canonical citations

Delegate to **literature-researcher** to find the primary source and key secondary sources. Verify citations exist.

### 4. Store teaching notes

Save a structured note in `workspaces/<project>/01-analysis/literature/<topic-slug>.md` containing:

- The concept explained
- Key citations with verification status
- Connection to the paper
- Debates and limitations

### 5. Journal the teaching

Create a TEACH journal entry in `workspaces/<project>/journal/NNNN-TEACH-<topic>.md` with frontmatter (type, date, paper, section, topic, tags). Include:

- The concept taught
- Key debates identified
- Connection to the paper
- Gap alerts (what reviewers would expect)
- Any CONNECTION entries for cross-concept links discovered

### 6. Present to user

Explain in accessible language. Ask: "Does this make sense? Any questions before we move on?"

## Agent Team

- **field-expert** — Primary: teaches the concept
- **literature-researcher** — Support: finds and verifies sources
