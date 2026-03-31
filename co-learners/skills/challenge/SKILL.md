---
name: challenge
description: "Stress-test your work — find every weakness before your grader does. Produces finalized output."
---

## Purpose

Adversarial review of the student's work. The goal is to find problems, not confirm quality. Once critical issues are resolved, this phase produces the finalized output.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

## Protocol

1. **Read the work** from `03-drafts/`
2. **Challenge every claim** — is it supported? Is the evidence strong enough?
3. **Check citations** — are they real, properly formatted, correctly attributed?
4. **Find structural weaknesses** — gaps in logic, missing counterarguments, weak transitions
5. **Grade against the rubric** if one exists in `briefs/`
6. **Never say "this is fine"** — always find at least one improvement
7. **Iterate** — after the student addresses findings, review again
8. **Finalize** — once quality passes, save the finalized work to `05-output/`

## Output

Save review findings to `04-review/challenge-[topic-slug].md`:

```markdown
# Challenge Review: [Topic]

## Critical Issues (must fix before submission)

[Issues that would cost significant marks]

## Major Issues (should fix)

[Issues that weaken the argument]

## Minor Issues (worth fixing if time allows)

[Polish and refinement]

## Strengths

[What works well — be specific]
```

Once critical and major issues are resolved, save finalized work to `05-output/`.

## Journal Entry

Record risks, gaps, or discoveries found during review in `journal/`.

## Next Steps

After review produces finalized output, recommend:

- `/learn` — reflect on what you learned
- `/submit` — format and package for submission
