---
name: exam-prep
description: "Exam preparation — topic review, practice problems, study schedule"
---

## Purpose

Build a structured exam preparation plan. Works for any subject — adapts practice problems and study strategies to the student's discipline and course.

## Input

`$ARGUMENTS` contains the course name or exam topic (e.g., "organic chemistry", "European history 1789-1914", "introduction to psychology").

If `$ARGUMENTS` is empty, ask: "What course or exam are you preparing for? What topics will it cover?"

## Protocol

1. **Identify the exam scope** — what topics, what format (multiple choice, essay, short answer, calculations, problem sets)?
2. **Create a topic checklist** — every testable concept, organized by importance
3. **Review weak areas** — check journal/ for GAP entries from past assignments
4. **Generate practice problems** — progressive difficulty (easy -> medium -> hard)
5. **Build a study schedule** — spaced repetition over available days
6. **Create a concept/reference sheet** — one-page quick reference for the key material

## Output

- Topic coverage checklist with confidence ratings
- Practice problems with hidden solutions (reveal on request)
- Suggested study schedule with spaced repetition
- Quick reference sheet for key concepts

## Study Guide Structure

### 1. What Is It?
Plain-language definition, no jargon without explanation. One-sentence flashcard summary.

### 2. Why Does It Matter?
Real-world context, analogy to anchor the concept, connection to prerequisites.

### 3. How It Works
Level-appropriate explanation with worked example where applicable.

### 4. Practice Problems
- **Level 1**: Direct recall or basic application (2-3 problems)
- **Level 2**: Conceptual twist requiring understanding (2-3 problems)
- **Level 3**: Multi-step exam-style combining related concepts (1-2 problems)
- Answers provided separately

### 5. Common Mistakes
3-5 most frequent errors with explanations of why they are wrong and the correct approach.
