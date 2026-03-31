---
name: ws
description: "Show academic workspace status dashboard. Read-only."
---

Display the current workspace status in plain language. Do not modify any files.

1. List all directories under `workspaces/` (excluding `_template/`).

2. For the most recently modified workspace (or `$ARGUMENTS` if specified):
   - Show workspace name and path
   - Derive current phase and present using plain-language descriptions:
     - Has `01-research/` files -> "Research completed — topic analyzed, sources collected"
     - Has `02-outline/` files -> "Outline ready — awaiting your approval"
     - Has `03-drafts/` files -> "Drafting in progress" + progress summary
     - Has `04-review/` files -> "Review completed — feedback ready"
     - Has `05-output/` files -> "Work finalized — ready for submission review"
   - Show progress: "X of Y tasks completed" (count files in `todos/active/` vs `todos/completed/`)
   - Show academic progress details:
     - Sections drafted vs total sections planned
     - Sources collected and cited
     - Key deliverables status
   - List the 5 most recently modified files in the workspace
   - If `.session-notes` exists, show its contents and age
   - Suggest the next action based on current phase:
     - After research: "Next: run `/outline` to plan your structure"
     - After planning: "Next: run `/draft` to start writing"
     - During drafting: "Next: run `/draft` to continue with the next section"
     - After drafting: "Next: run `/challenge` to stress-test your arguments"
     - After review: "Next: address the feedback, then run `/submit` to package for submission"

3. Present as a compact, friendly summary. Use plain language throughout.
