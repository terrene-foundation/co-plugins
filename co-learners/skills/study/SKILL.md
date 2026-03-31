---
name: study
description: "Research the subject, gather sources, build conceptual understanding"
---

## Purpose

Research the topic and build understanding before structuring the assignment. Identifies key concepts, theories, debates, and gaps in the student's subject area.

## Input

`$ARGUMENTS` contains the topic or assignment name (e.g., "the French Revolution", "photosynthesis", "Hamlet's indecision").

If `$ARGUMENTS` is empty, ask: "What topic would you like to study?"

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)
3. If no workspace exists, ask the student to create one first

## Protocol

1. **Read the assignment brief** from `briefs/` if available
2. **Research the topic** — identify key concepts, theories, debates, and gaps
3. **Gather sources** — find relevant academic sources, evaluate quality (CRAAP test)
4. **Build understanding** — explain concepts at the student's level, connect to what they know
5. **Document findings** — save research notes and source evaluations to `01-research/`

## Output

Save to `01-research/`:

- Research notes organized by subtopic
- Source evaluations with quality assessments
- Key concepts and their relationships
- Gaps or questions that need further investigation

## Journal Entry

Record key findings, discoveries, or gaps in `journal/`. Type: DISCOVERY or GAP.

## Next Step

After research is sufficient, recommend `/outline` to structure the assignment.
