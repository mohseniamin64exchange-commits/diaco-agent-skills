---
name: using-diaco-skills
description: Routes project work to the appropriate Diaco standards, workflows, and platform profile. Use when starting a new session, opening an existing project, or deciding which Diaco rules should govern the task.
---

# Using Diaco Skills

## Overview

Use the smallest applicable combination of:
1. shared standard,
2. operational skill,
3. platform profile,
4. project-specific rule.

## Standards routing

- New/existing project setup → `standards/project-standard.md`
- UI/layout/components/forms/tables/dialogs → `standards/ui-standard.md`
- Printing/preview/report output → `standards/print-standard.md`
- Backup/restore → `standards/backup-restore-standard.md`
- Users/roles/permissions → `standards/user-management-standard.md`
- Windows desktop application baseline → `standards/windows-app-standard.md`
- Testing/verification → `standards/testing-standard.md`
- Version/release/rollback → `standards/release-standard.md`

Check `standards/README.md` for each standard's status.

A DRAFT standard is not permission to invent details. Use an approved reference implementation and persist only approved reusable rules.

## Skill routing

- Continuing work across sessions or Agents → `project-context-handoff`
- Making GitHub the durable project memory → `github-project-memory`
- Building or reusing consistent application UI → `shared-ui-system`
- Changing an established/working codebase → `safe-existing-project-change`
- Working with Supabase web applications → `supabase-webapp-guardrails`
- Working with Windows desktop applications → `windows-desktop-standard`
- Automating Word/documents with R or similar tooling → `document-r-automation`

Multiple standards and skills may apply.

## Shared rules

1. Inspect current repository state before making non-trivial changes.
2. Identify the project platform.
3. Load only the relevant standards and skills.
4. Project-specific rules override generic Diaco defaults when intentionally defined.
5. Do not invent missing state or missing DRAFT-standard details.
6. Keep changes scoped and reversible.
7. Verify before declaring completion.
8. Persist important state for the next session.

## Verification

Before finishing:
- [ ] Correct standard(s) and skill(s) were used.
- [ ] Repository state was inspected.
- [ ] Correct platform profile was selected.
- [ ] Relevant verification was performed.
- [ ] DRAFT standards were not silently treated as approved.
- [ ] Durable state/handoff was updated when continuation is expected.
