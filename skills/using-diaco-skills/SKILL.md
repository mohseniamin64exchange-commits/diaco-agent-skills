---
name: using-diaco-skills
description: Routes project work to the appropriate Diaco standards, workflows, platform profile, and approved engineering tools.
---

# Using Diaco Skills

## Overview

Use the smallest applicable combination of:
1. shared standard,
2. operational skill,
3. platform profile,
4. specialized engineering tool,
5. project-specific rule.

## Standards routing

- New/existing project setup → `standards/project-standard.md`
- UI/layout/components/forms/tables/dialogs → `standards/ui-standard.md`
- Printing/preview/report output → `standards/print-standard.md`
- Backup/restore → `standards/backup-restore-standard.md`
- Users/roles/permissions → `standards/user-management-standard.md`
- Windows desktop application baseline → `standards/windows-app-standard.md`
- Testing/verification → `standards/testing-standard.md`
- Tool selection → `standards/engineering-toolchain-standard.md`
- PR/diff review → `standards/pull-request-review-standard.md`
- Security review → `standards/security-review-standard.md`
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
- Reviewing a substantial diff/PR → `pull-request-review`
- Performing authorized security review → `security-review`
- Automating Word/documents with R or similar tooling → `document-r-automation`

## Tool routing

- Current external library/API documentation → Context7 when available
- Web browser automation/verification → Playwright CLI when available
- Supabase schema/config/project operations → official Supabase MCP when authorized
- UI workflow inspiration → UI Skills as a non-authoritative reference
- Authorized application security automation → Strix when appropriate

Multiple standards, skills, and tools may apply.

## Shared rules

1. Inspect current repository state before making non-trivial changes.
2. Identify the project platform.
3. Load only the relevant standards, skills, and tools.
4. Project-specific rules override generic Diaco defaults when intentionally defined.
5. Do not invent missing state or missing DRAFT-standard details.
6. Keep changes scoped and reversible.
7. Verify before declaring completion.
8. Persist important state for the next session.

## Verification

Before finishing:
- [ ] Correct standard(s), skill(s), and tools were used.
- [ ] Repository state was inspected.
- [ ] Correct platform profile was selected.
- [ ] Relevant verification was performed.
- [ ] Significant changes received review when appropriate.
- [ ] DRAFT standards were not silently treated as approved.
- [ ] Durable state/handoff was updated when continuation is expected.
