---
name: challenge
description: "Attack this argument from every angle. Be the hostile reviewer. Never says 'this is fine.'"
---

## What This Command Does (present to user)

Simulates the most hostile reviewer your paper could face. Every weakness gets found. Every unsupported claim gets challenged. The goal is to make your arguments bulletproof before submission.

## Your Role (communicate to user)

Review the attacks. For FATAL findings, you must address them — no exceptions. For MAJOR, you should address them. For MINOR and STYLE, your call. For each attack, you can either fix the argument, strengthen the defense, or explain why the criticism doesn't apply.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store results in `workspaces/<project>/04-validate/reviews/`

## Workflow

### 1. Parse target

If `$ARGUMENTS` is a section (e.g., "Part III") — attack that section.
If `$ARGUMENTS` is a quoted phrase — attack the argument around that phrase.
If `$ARGUMENTS` is "full-paper" — attack the entire paper.

### 2. Deploy the critic

Delegate to **argument-critic** in reviewer simulation mode:

- Simulate a hostile reviewer at the target venue
- Find every logical gap, unsupported leap, circular reasoning, missing qualification
- Challenge the novelty claim
- Question the evidence base
- Attack the methodology
- Probe the limitations section for gaps

### 3. Severity classification

Every finding gets classified:

- **FATAL** — Will cause desk rejection
- **MAJOR** — Reviewer will require revision
- **MINOR** — Could be stronger
- **STYLE** — Preference, not substance

### 4. Store results

Save attack report in `workspaces/<project>/04-validate/reviews/challenge-<date>.md`.

### 5. Journal defenses

For each finding, create a DEFENSE journal entry in `workspaces/<project>/journal/NNNN-DEFENSE-<topic>.md`. Include:
- The attack (what a reviewer would say)
- The defense (how to respond)
- Tags for the concept being attacked
- Any GAP entries for weaknesses that need new literature or argument work

These DEFENSE entries become the author's preparation material for conference Q&A, viva, or reviewer responses.

### 6. Present to user

For each finding: the attack, why it matters, and a suggested defense. Ask: "Which of these do you want to address? FATAL findings must be fixed."

## Approval Gate

FATAL findings block further writing on the affected section. The author must decide how to respond before proceeding.

## Agent Team

- **argument-critic** — Primary: adversarial analysis
- **field-expert** — Support: suggests defenses from the literature
- **claims-verifier** — Support: verifies claims challenged by the critic
