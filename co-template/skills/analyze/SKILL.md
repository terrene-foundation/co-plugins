---
name: analyze
description: Research and understand the problem space. Gather information, identify constraints, map the landscape.
argument-hint: "[topic or question]"
---

# /analyze $ARGUMENTS

Research and analyze **$ARGUMENTS** thoroughly.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project
2. **Read the project brief** if one exists in the workspace
3. **Research the topic**: gather relevant information, identify key sources, map competing approaches
4. **Identify constraints**: what limits apply? What standards must be met?
5. **Document findings** in `01-research/`

## Output

Save a structured analysis to `01-research/analysis-[topic-slug].md`:

```markdown
# Analysis: $ARGUMENTS
Date: [today]

## Key Findings
[What you discovered]

## Sources and References
[Where the information comes from]

## Constraints and Considerations
[What limits or standards apply]

## Recommendations
[What the human should consider for the next phase]
```

## Next Step

After analysis, recommend `/plan` to create a structured plan based on findings.
