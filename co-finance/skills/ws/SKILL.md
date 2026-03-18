---
name: ws
description: "Show academic workspace status dashboard. Read-only."
---

Display the current workspace status in plain language. Do not modify any files.

1. List all directories under `workspaces/` (excluding `instructions/`).

2. For the most recently modified workspace (or `$ARGUMENTS` if specified):
   - Show workspace name and path
   - Derive current phase and present using plain-language descriptions:
     - Has `01-analysis/` files -> "Research completed — topic analyzed, sources collected"
     - Has `todos/active/` files -> "Project plan ready — awaiting your approval"
     - Has `todos/completed/` files -> "Drafting in progress" + progress summary
     - Has `04-feedback/` files -> "Review completed — professor-style feedback ready"
     - Has completed all phases -> "Project finalized — ready for submission review"
   - Show progress: "X of Y tasks completed" (count files in `todos/active/` vs `todos/completed/`)
   - Show academic progress details:
     - Sections drafted vs total sections planned
     - Sources collected and cited
     - Key deliverables status (data tables, charts, appendices)
   - List the 5 most recently modified files in the workspace
   - If `.session-notes` exists, show its contents and age
   - Suggest the next action based on current phase:
     - After research: "Next: run `/todos` to plan your deliverables"
     - After planning: "Next: run `/assignment` or `/thesis` to start drafting"
     - During drafting: "Next: run `/assignment` or `/thesis` to continue working on the next section"
     - After drafting: "Next: run `/challenge` to stress-test your arguments"
     - After feedback: "Next: address the feedback, then run `/challenge` again or prepare for submission"

3. Present as a compact, friendly summary. Use plain language throughout.
