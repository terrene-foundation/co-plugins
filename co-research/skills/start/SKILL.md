---
name: start
description: "New user orientation — explains the workflow and how to get started"
---

Present this orientation to the user in a warm, clear way. Adapt tone based on context.

## What Is This?

This is a COR (Cognitive Orchestration for Research) workspace — a structured system for human-AI co-authorship of academic publications. The AI helps you research, draft, review, and publish academic papers while maintaining research integrity and preserving your authentic voice.

## The Core Workflow

Every initiative follows the same 5-phase chain. Each command works independently but they're designed to flow together:

| Step         | Command      | What Happens                                                                            | Your Role                                  |
| ------------ | ------------ | --------------------------------------------------------------------------------------- | ------------------------------------------ |
| 1. Research  | `/co-research:analyze`   | Research your topic — literature landscape, competing approaches, gaps                  | Confirm the analysis captures what matters |
| 2. Planning  | `/co-research:todos`     | Create a roadmap of deliverables                                                        | Approve the plan before work starts        |
| 3. Execution | `/co-research:implement` | Create documents, drafts, or analyses one task at a time                                | Answer questions when decisions come up    |
| 4. Review    | `/co-research:redteam`   | Stress-test from adversarial angles (logical gaps, weak arguments, consistency)         | Review findings                            |
| 5. Knowledge | `/co-research:codify`    | Capture what we learned for future sessions                                             | Confirm the knowledge is accurate          |

**After codification**, you may:

- `/co-research:publish` — Prepare work for academic submission (arXiv, SSRN, AIES)
- Start a new cycle with `/co-research:analyze` for the next initiative

Plus **`/co-research:ws`** anytime to check progress and **`/co-research:wrapup`** before ending a session.

## Getting Started

Walk the user through these steps:

1. **Check workspace**: Run `/co-research:ws` to see current status
2. **Start an initiative**: Create or update a brief in `workspaces/<project>/briefs/` describing what you want to accomplish
3. **Run `/co-research:analyze`**: This kicks off the research phase

### Brief Template

If the user needs a template for their brief:

```markdown
# [Initiative Name]

## What We're Doing

[1-2 paragraphs: What is this initiative and why does it matter?]

## Who It Affects

[List stakeholders and their concerns]

## Success Criteria

- [What does "done" look like?]
- [What outcomes matter?]

## Known Constraints

[Deadlines, regulatory requirements, dependencies, budget]

## Related Prior Work

[Links to existing docs, briefs, or prior decisions]
```

## The Workflow for Different Types of Work

The same 5-command chain works for all initiatives, but what happens inside each command adapts to the type of work:

**Research Co-Authorship** (the primary COR workflow):

- `/co-research:teach` and `/co-research:literature` to learn the field and find papers
- `/co-research:deliberate` to record structural decisions (scope, ordering, framing)
- `/co-research:craft` for author-writes mode (AI teaches and critiques) or `/co-research:write-para` for AI-drafts mode (author approves every paragraph)
- `/co-research:validate-claim` and `/co-research:challenge` to verify claims and simulate hostile reviewers
- `/co-research:check-refs` to audit citation integrity

**Publication Preparation** (papers for arXiv, SSRN, AIES):

- Use the core chain for research and drafting
- Then `/co-research:publish` for venue-specific preparation and quality checks

**General Research Initiative**:

- `/co-research:analyze` → `/co-research:todos` → `/co-research:implement` → `/co-research:redteam` → `/co-research:codify`
- Works for literature reviews, methodology development, or any structured research project

## Available Expertise

The AI has specialized knowledge in:

### Research Co-Authorship

- **Literature Research** — Systematic discovery, paper assessment, citation verification
- **Field Expertise** — Domain knowledge, historical context, debates, connections to your argument
- **Claims Verification** — Verifies claims against cited sources
- **Argument Critique** — Adversarial reviewer simulation
- **Writing Partnership** — Paragraph-level co-writing with margin notes
- **Citation Audit** — Cross-paper citation integrity, scope boundary enforcement

### Publication

- **Academic Venues** — arXiv, SSRN, AIES, AI & Society formatting and requirements
- **LaTeX Conversion** — Markdown to LaTeX for submission
- **Citation Management** — Reference formatting, bibliography generation

## Key Locations

| Content                    | Location                              |
| -------------------------- | ------------------------------------- |
| Paper briefs               | `workspaces/<project>/briefs/`        |
| Literature assessments     | `workspaces/<project>/01-analysis/`   |
| Decision records           | `workspaces/<project>/03-drafts/deliberation/` |
| Draft versions             | `workspaces/<project>/03-drafts/versions/`     |
| Validation reports         | `workspaces/<project>/04-validate/`   |
| Journal entries            | `workspaces/<project>/journal/`       |
