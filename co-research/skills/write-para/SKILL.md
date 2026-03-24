---
name: write-para
description: "Draft a paragraph together through deliberation. Present, discuss, refine. Author approves every paragraph."
---

## What This Command Does (present to user)

We write one paragraph together. You describe what the paragraph should accomplish. I draft it with annotations explaining every choice, present alternatives for key phrases, and explain the literature behind the argument. You approve, modify, or reject. Nothing gets written without your explicit approval.

## Your Role (communicate to user)

This is the most important command — your judgment drives the process. Tell me what the paragraph should say. I'll draft it with margin notes. You decide if it works. Push back on anything that doesn't sound like you or that you don't fully understand.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store deliberation in `workspaces/<project>/03-drafts/deliberation/`
4. Store draft versions in `workspaces/<project>/03-drafts/versions/`

## Workflow

### 1. Understand intent

Parse `$ARGUMENTS` for the paragraph intent. Read the surrounding context:

- What section is this paragraph in?
- What came before? What comes after?
- What argument does this paragraph need to make?

### 2. Draft with annotations

Delegate to **writing-partner**. The draft must include:

- **The paragraph** — Clean, publication-ready prose
- **Margin notes** — Why this opening, why this citation placement, why this word choice
- **Alternatives** — 2-3 options for the opening sentence or key phrasing
- **Citation rationale** — Why each source is cited where it is
- **Teaching note** — If the paragraph uses a concept the author may not fully know, explain it

### 3. Present to user

Show the draft with all annotations. Ask:

- "Does this say what you want it to say?"
- "Is anything unclear or doesn't sound like you?"
- "Do you understand the literature behind each sentence?"

### 4. Iterate

If rejected: understand why, redraft.
If partially approved: make specific changes.
If approved: finalize.

### 5. Record the decision

Store a deliberation record:

- What was decided about this paragraph
- What alternatives were rejected and why
- What teaching happened during the process

Save in `workspaces/<project>/03-drafts/deliberation/<section>-<para-num>.md`.

### 6. Journal all insights

Create journal entries in `workspaces/<project>/journal/` for EVERY insight produced:

- **MARGIN** entry: All margin notes (why this word, why this structure, why this citation)
- **TEACH** entry: Any concept explained to the author during drafting
- **CONNECTION** entry: Any cross-concept or cross-paper link identified
- **CLAIM** entry: Any claim that needs future verification

Use sequential naming: `NNNN-TYPE-topic.md`. Include frontmatter with type, date, paper, section, paragraph, topic, tags. These entries are the reusable knowledge trail for defense, presentations, and other materials.

### 7. Update draft version

Append the approved paragraph to the current draft version in `workspaces/<project>/03-drafts/versions/`.

## Approval Gate

FULL verification — every paragraph requires explicit author approval. This is a non-negotiable decision.

## Agent Team

- **writing-partner** — Primary: drafts with annotations
- **field-expert** — Support: teaches concepts the paragraph draws on
- **claims-verifier** — Support: verifies any claims in the paragraph
