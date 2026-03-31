---
name: present
description: "Create structured presentations with speaker notes and data visualization"
---

## Purpose

Create a presentation from research or draft content. Helps students structure slides, design visuals, write speaker notes, and prepare for delivery.

## Input

`$ARGUMENTS` contains the presentation topic.

If `$ARGUMENTS` is empty, ask: "What is the presentation about? Also helpful to know: how long is the time slot and who is the audience?"

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project, use `workspaces/$ARGUMENTS/`
2. Otherwise, use most recently modified under `workspaces/` (excluding `_template/`)

## Protocol

1. **Determine scope** — what's the audience, time limit, key message?
2. **Create slide outline** — title, key points per slide, visual suggestions
3. **Write speaker notes** — what to say for each slide (not just what's on the slide)
4. **Suggest data visualizations** — charts, diagrams, or images that support the argument
5. **Add delivery tips** — pacing, emphasis points, audience engagement
6. **Save to `03-drafts/`**

## Presentation Templates

**For Research Presentations (thesis defense, conference):**
```
Slide 1:  Title — title, author, affiliation, date
Slide 2:  Motivation — why should the audience care?
Slide 3:  Research question — the specific question
Slide 4:  Literature context — where this fits (2-3 key works)
Slide 5:  Methodology — how you studied this
Slide 6:  Data/Sources — sample description
Slide 7-9: Results — main findings with visuals
Slide 10: Implications — what this means
Slide 11: Conclusion — answer the question, acknowledge limitations
Slide 12: Thank you + Q&A
```

**For Topic Presentations (classroom):**
```
Slide 1:  Title
Slide 2:  What is [topic]? — definition with example
Slide 3:  Why it matters — relevance and significance
Slide 4-6: How it works — the key ideas, with visuals
Slide 7:  Example — concrete case or worked example
Slide 8:  Key takeaways — 3 bullet points maximum
Slide 9:  Discussion or Q&A
```

## Output

Presentation outline with speaker notes saved to `03-drafts/presentation-[topic-slug].md`.
