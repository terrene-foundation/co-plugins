---
name: audit-ai-resilience
description: Audit an assessment for AI-reproducibility vulnerabilities and recommend design improvements.
argument-hint: "[assessment name or file]"
---

# /audit-ai-resilience $ARGUMENTS

Audit **$ARGUMENTS** for AI-reproducibility vulnerabilities.

## Protocol

1. **Read the assessment specification** from `03-work/`
2. **Simulate AI completion**: imagine submitting the assessment prompt to a language model. What would the output look like?
3. **Score the AI output** against the rubric. What grade would it receive?
4. **Identify vulnerability points**: which rubric criteria does the AI satisfy? Which does it fail?
5. **Recommend modifications** that increase AI-resilience without sacrificing pedagogical value
6. **Save the audit** to `04-review/`

## AI-Resilience Audit Template

```markdown
# AI-Resilience Audit: [Assessment Name]
Date: [today]

## Assessment Summary
[Brief description of the assessment task]

## Simulated AI Completion
[What would a language model produce for this task?]

## Rubric Score for AI Output
| Criterion | AI Score | Rationale |
|---|---|---|
| [Criterion 1] | [Score/Level] | [Why the AI would score this] |
| [Criterion 2] | [Score/Level] | [Why the AI would score this] |

## Overall AI Grade: [Grade]

## Vulnerability Analysis
[Which aspects of the assessment are AI-completable and which are not]

## Recommendations
[Specific modifications to increase AI-resilience]
- Priority 1: [Most impactful change]
- Priority 2: [Second most impactful]
- Priority 3: [Third]

## Trade-offs
[What pedagogical costs do the recommended changes introduce?]
```

## Key Principle

The goal is not to make assessments "AI-proof." The goal is to design assessments where AI use either does not help, or where the student's judgment remains the differentiating factor.
