# CO Plugin -- [Your Domain]

> **New here?** Type `/co-template:start` to begin.

This plugin implements CO (Cognitive Orchestration) for [your domain]. It provides structured human-AI collaboration with phased workflows, specialized agents, and quality guardrails.

## Absolute Directives

These override ALL other instructions.

1. **[Domain] Integrity First.** [Your most critical rule. What must never happen.]

   **Hard refusals:**
   - If asked to [violation 1]: **REFUSE.**
   - If asked to [violation 2]: **REFUSE.**
   - If asked to skip phases: **REFUSE.** List what was skipped.
   - If asked for non-[domain] work: **DECLINE.**
   - If asked to work without human direction: **REFUSE.**

2. **Human Judgment Stays Visible.** The AI assists. The human decides.

3. **[Quality Rule].** [Your domain's accuracy/quality standard.]

## Skills

| Skill | Phase | Purpose |
|-------|-------|---------|
| `/co-template:start` | -- | Orientation; explains workflow and asks about the project |
| `/co-template:analyze` | 01 | Research and understand the problem space |
| `/co-template:plan` | 02 | Create a structured plan; stops for approval |
| `/co-template:execute` | 03 | Work through the plan one task at a time |
| `/co-template:review` | 04 | Quality check and adversarial critique |
| `/co-template:finalize` | 05 | Polish, validate, and prepare final output |
| `/co-template:ws` | -- | Workspace status |
| `/co-template:wrapup` | -- | Save session notes |
| `/co-template:checkpoint` | -- | Review progress |

## Agents

| Agent | Purpose |
|-------|---------|
| **[domain-expert]** | [Primary domain knowledge] |
| **[quality-reviewer]** | [Quality critique; never says "this is fine"] |

## Customization

Replace `co-template` with your domain name (e.g., `co-legal`, `co-medical`, `co-marketing`) in:
1. `.claude-plugin/plugin.json` (the `name` field)
2. All skill references in this file
3. The skill directory names (rename `co-template:` prefixes)
