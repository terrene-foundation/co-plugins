---
name: finalize
description: Polish, validate, and prepare the final output. Last quality gate before delivery.
---

# /finalize

Prepare the final output for delivery.

## Protocol

1. **Check all review issues are addressed** from `04-review/`
2. **Polish the output** - formatting, consistency, completeness
3. **Run final validation** against the domain integrity rules
4. **Save the final version** to `05-output/`

## Pre-delivery checklist

- [ ] All critical review issues resolved
- [ ] All major review issues resolved or documented as known limitations
- [ ] Output meets the domain quality standards
- [ ] Human has approved the final version

## Output

Save to `05-output/` with a clear filename. Include a brief summary of what was produced and any known limitations.

## Journal Entry

Record what was learned during this project in `journal/`.
