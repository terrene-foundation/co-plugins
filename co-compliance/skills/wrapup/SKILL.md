---
name: wrapup
description: Save session notes before ending. Captures compliance context for the next session.
---

# Session Wrapup

Write a `.session-notes` file capturing:

1. What was accomplished this session
2. What regulations were analyzed and what remains
3. What control mappings were completed
4. What gaps were identified
5. What decisions the compliance officer made (applicability, risk acceptance, remediation priority)
6. What the next steps are
7. Any unresolved questions or blockers
8. Current jurisdiction and regulatory scope context

Save to `.session-notes` in the project root. This file will be read by `/start` in the next session to restore context.
