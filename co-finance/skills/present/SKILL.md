---
name: present
description: "Create a structured presentation on a finance topic"
---

## Purpose

Help a student create a clear, well-structured presentation on a finance topic. Produces a slide outline with speaker notes, data visualization suggestions, and delivery tips. Can integrate with Canva MCP for slide design if available.

## Input

`$ARGUMENTS` contains the presentation topic or assignment description. Examples: "10-minute presentation on the 2008 financial crisis", "group presentation comparing passive vs active fund management", "thesis defense slides on ESG and stock returns".

If `$ARGUMENTS` is empty, ask the student: "What is your presentation about? Include the topic, time limit, audience (classmates, professor, panel), and any specific requirements."

## Workflow

### Step 1 — Understand the Presentation Requirements

Gather key parameters:

- **Topic**: What is the presentation about?
- **Time limit**: How many minutes? (This determines number of slides — roughly 1-2 slides per minute)
- **Audience**: Classmates, professor, conference, thesis committee?
- **Purpose**: Inform, persuade, defend, or teach?
- **Requirements**: Specific sections, data requirements, citation rules?
- **Format**: Individual or group? If group, how are sections divided?

### Step 2 — Design the Slide Outline

Create a slide-by-slide outline following this structure:

```
Slide 1: Title Slide
  - Title, subtitle, presenter name(s), date, course

Slide 2: Agenda / Roadmap
  - 3-5 bullet points previewing the presentation structure
  - Helps the audience follow along

Slides 3-4: Context / Background
  - Why this topic matters
  - Key facts or data to set the stage
  - Keep text minimal — one key idea per slide

Slides 5-8: Main Content (Core Analysis)
  - One main point per slide
  - Data visualizations where applicable
  - Evidence supporting each point

Slide 9: Discussion / Implications
  - What does this mean for investors/policymakers/firms?
  - Counterarguments or limitations

Slide 10: Conclusion / Key Takeaways
  - 3-4 bullet points summarizing the presentation
  - Answer the central question

Slide 11: Questions
  - Invite discussion
  - Prepare 2-3 backup slides for anticipated questions

Slide 12: References
  - Properly formatted citations for all data and sources used
```

Adjust the number of content slides based on the time limit.

### Step 3 — Write Speaker Notes

For each slide, provide:

- **What to say** (2-3 sentences of narrative — not reading the slide)
- **Transition** (how to connect this slide to the next)
- **Timing** (approximate seconds or minutes per slide)
- **Engagement tip** (a question to pose, a pause for emphasis, an example to elaborate on)

### Step 4 — Suggest Data Visualizations

For slides containing data, recommend specific chart types:

| Data Type | Recommended Chart | Why |
|---|---|---|
| Time series (stock prices, GDP) | Line chart | Shows trends over time clearly |
| Comparison (firm A vs firm B) | Bar chart | Side-by-side comparison is intuitive |
| Composition (portfolio allocation) | Pie or stacked bar | Shows parts of a whole |
| Distribution (returns histogram) | Histogram | Shows shape of distribution |
| Relationship (risk vs return) | Scatter plot | Shows correlation between variables |
| Geographic (trade flows, FDI) | Map or heat map | Shows spatial patterns |

For each suggestion, note:
- What data to include
- What to label and highlight
- What the audience should take away from the visual
- Source attribution requirements

### Step 5 — Delivery Tips

Provide guidance tailored to the presentation context:

- **Opening**: Start with a hook — a surprising statistic, a question, or a brief story
- **Pacing**: Speak at conversational pace; silence after key points is powerful
- **Slides**: Do not read from slides — they support your narrative, they are not the narrative
- **Data**: When showing a chart, tell the audience what to look at: "Notice how the spread widened sharply in March 2020..."
- **Questions**: Repeat the question before answering so everyone hears it
- **Time management**: Practice with a timer; cut content rather than rushing

### Step 6 — Canva Integration (Optional)

If the Canva MCP is available:
- Offer to create the presentation in Canva using the slide outline
- Use a clean, professional template suitable for academic presentations
- Apply consistent branding (color scheme, fonts)
- Generate slides with proper layout for text and visuals

If Canva is not available, suggest the student use the outline to build slides in their preferred tool (PowerPoint, Google Slides, Keynote).

## Agent Team

- **presentation-designer** — Slide structure, visual design, delivery coaching
- Appropriate **course tutor** — Domain expertise for the presentation topic
- **financial-literacy-expert** — Plain-language explanations for audience accessibility
- **citation-specialist** — Reference formatting for the references slide

## Skill References

- `16-presentation-skills/` — Presentation design and delivery guidance
- Relevant domain module from `.claude/skills/` based on presentation topic
