---
name: using-diaco-skills
description: Routes project work to the appropriate Diaco workflow. Use when starting a new session, opening an existing project, or deciding which Diaco skill should govern the task.
---

# Using Diaco Skills

## Overview

Use the smallest applicable workflow. Skills are operating procedures, not background reading.

## Routing

- Continuing work across sessions or Agents → `project-context-handoff`
- Making GitHub the durable project memory → `github-project-memory`
- Building or reusing consistent application UI → `shared-ui-system`
- Changing an established/working codebase → `safe-existing-project-change`
- Working with Supabase web applications → `supabase-webapp-guardrails`
- Automating Word/documents with R or similar tooling → `document-r-automation`

Multiple skills may apply.

## Shared rules

1. Inspect current repository state before making non-trivial changes.
2. Project-specific rules override generic Diaco defaults.
3. Do not invent missing state when it can be inspected.
4. Keep changes scoped and reversible.
5. Verify before declaring completion.
6. Persist important state for the next session.

## Verification

Before finishing:
- [ ] Correct skill(s) were used.
- [ ] Repository state was inspected.
- [ ] Relevant verification was performed.
- [ ] Durable state/handoff was updated when continuation is expected.
