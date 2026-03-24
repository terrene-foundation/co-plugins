---
name: implement
description: "Load phase 03 (implement) for the current workspace. Repeat until all todos complete."
---

## What This Phase Does (present to user)

Execute the work one task at a time from the approved roadmap. Each run of `/co-research:implement` completes one task — drafting documents, analyzing structures, creating specifications, or building content.

## Your Role (communicate to user)

Your role is to answer questions when decisions come up — these will always be about what the content should say, what position to take, or what stakeholders need. You can check progress anytime with `/co-research:ws`.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name or todo, parse accordingly
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the user to create one first
4. Read all files in `workspaces/<project>/briefs/` for user context

## Phase Check

- Read files in `workspaces/<project>/co-research:todos/active/` to see what needs doing
- Read files in `workspaces/<project>/co-research:todos/completed/` to see what's done
- If `$ARGUMENTS` specifies a specific todo, focus on that one
- Otherwise, pick the next active todo
- Reference plans in `workspaces/<project>/02-plans/` for context

## Workflow

### NOTE: Run `/co-research:implement` repeatedly until all todos/active have been moved to todos/completed

### 1. Prepare todos

Use the todo-manager to create detailed todos for EVERY SINGLE TODO in `todos/000-master.md`.

### 2. Execute

Implement the next todo using the appropriate team of agents.

- Read relevant existing documents before writing new content
- Check foundational documents for alignment (if they exist in this repo)
- Check related documents for consistency

### 3. Quality standards

Always involve review agents:

- Cross-reference accuracy (clause numbers, section names)
- Naming conventions
- License accuracy
- No placeholder content
- Consistency with existing documents

### 4. Completion evidence

Before closing ANY todo, you MUST provide concrete evidence:

**For document creation/editing:**

- [ ] File path(s) where work is stored
- [ ] Reviewer has reviewed (note findings)
- [ ] Cross-references verified (all links resolve)

**For research content:**

- [ ] Claims verified against cited sources
- [ ] Citation integrity checked
- [ ] Terminology consistent with paper

A todo is NOT complete until evidence is provided. "Verified with evidence" means specific file paths, review attestations, and cross-reference checks — not a general statement.

### 5. Decision log

When the user makes a decision during implementation, capture it:

```yaml
decision: [What was decided]
rationale: [Why — the reasoning]
alternatives_rejected: [What other options were considered]
date: [When]
initiative: [Which initiative]
```

Store decisions in the workspace for `/co-research:codify` to capture later.

### 6. Communicate progress and surface decisions

When reporting to the user:

- **Progress**: State what was accomplished in plain terms. "The methodology section now addresses the reviewer's likely concern about generalizability" not "Created methodology.md"
- **Decisions needed**: Present choices with impact. "Should we frame this as a design science contribution or a position paper? Design science requires a more rigorous evaluation section."
- **Scope changes**: If work reveals something not in the plan, explain what and why.

### 7. Update and close todos

After completing each todo:

- Move it from `todos/active/` to `todos/completed/`
- Ensure completion evidence (step 4) is documented in the todo file

## Agent Teams

Deploy these agents as a team for each implementation cycle:

**Core team (always):**

- **cross-reference-auditor** — Document review after changes
- **claims-verifier** — Verify factual claims
- **todo-manager** — Track progress, update todo status

**Research co-authorship (invoke for paper writing):**

- **literature-researcher** — Find and verify sources
- **field-expert** — Domain knowledge and context
- **writing-partner** — Draft with annotations
- **argument-critic** — Adversarial review

**Analysis (invoke for complex decisions):**

- **deep-analyst** — Risk analysis, failure points, cascading effects
- **requirements-analyst** — Requirements breakdown, decision records

**Quality gate (before closing each todo):**

- Review all claims and cross-references before marking complete
