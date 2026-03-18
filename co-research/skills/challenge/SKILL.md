---
name: challenge
description: Hostile reviewer simulation - attacks from every angle, never says "this is fine"
arguments:
  - name: target
    description: The section, argument, or full paper to challenge
    required: true
---

# /challenge $target

You are simulating a hostile peer reviewer attacking **$target**. Find every weakness, logical gap, unsupported claim, and vulnerability. Never say "this is fine."

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load the target content**: Read the section or paper to be challenged
3. **Load context**: Read the paper brief, target venue, and any prior challenge results

## Delegation

Spawn the **argument-critic** agent for adversarial analysis. The agent never approves without criticism.

## Attack Vectors

The argument-critic will systematically check:

- **Novelty**: Has this been said before? What does this add?
- **Scope**: Are the claims proportional to the evidence?
- **Methodology**: Is the research approach appropriate? Are there stronger alternatives?
- **Internal consistency**: Does the paper contradict itself across sections?
- **Missing alternatives**: Are competing explanations acknowledged?
- **Definitions**: Are key terms defined precisely?
- **Audience fit**: Will the target venue's reviewers find this contribution sufficient?
- **So what?**: Even if correct, does it matter?

## Reviewer Personas

Request specific reviewer types if needed:
- **Methodology reviewer**: Research design, validity, generalizability
- **Theory reviewer**: Theoretical grounding, contribution to knowledge
- **Hostile competitor**: Work is derivative, unnecessary, or incorrect
- **Practitioner reviewer**: Demands practical relevance
- **Ethics reviewer**: Broader impacts, dual-use, fairness

## Output

### Challenge Report

Store in `04-validate/reviews/` named `challenge-[target-slug].md`:

```markdown
# Challenge Report: $target
Date: [today]
Reviewer persona: [type or general]

## Critical Issues (desk rejection risk)
[Issues that must be fixed]

## Major Issues (revision required)
[Issues a reviewer will flag]

## Minor Issues (worth fixing)
[Issues that weaken the paper]

## Defense Preparation
[How to respond to each issue]
```

## Journal Entry

Produce a DEFENSE journal entry:

```yaml
---
type: DEFENSE
date: [today]
paper: [paper name from brief]
section: $target
topic: hostile review simulation
tags: [relevant tags]
---
```
