---
name: redteam
description: "Adversarial stress-test — harder than /review, find every weakness"
---

## Purpose

Attack the work from every angle. This is harder than /review — the goal is to find every weakness before the grader does.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project, use `workspaces/$ARGUMENTS/`
2. Otherwise, use most recently modified under `workspaces/` (excluding `_template/`)

## Protocol

1. **Challenge every claim** — what evidence would disprove this? Is the evidence actually sufficient?
2. **Attack methodology** — are there alternative explanations? Selection bias? Confounding factors?
3. **Question sources** — are they the strongest available? Would a skeptical reader accept them?
4. **Find logical gaps** — missing counterarguments, unstated assumptions, logical fallacies
5. **Simulate a tough grader** — what would the most demanding version of the instructor say?
6. **Never say "this is fine"** — always find at least one real problem

## Output

Save to `04-review/redteam-[topic-slug].md` with issues ranked by severity.

## Journal Entry

Record risks and gaps found in `journal/`.
