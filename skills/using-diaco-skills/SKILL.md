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
4. specialized engineering tool/reference,
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

## Skill routing

- Continuing work across sessions or Agents → `project-context-handoff`
- GitHub durable memory → `github-project-memory`
- Shared UI consistency → `shared-ui-system`
- UI polish / animation / prototyping / UI review / library choice → `ui-design-engineering`
- Local business / supplier / lead discovery → `local-business-data`
- Safe changes in existing codebases → `safe-existing-project-change`
- Supabase web apps → `supabase-webapp-guardrails`
- Windows desktop apps → `windows-desktop-standard`
- PR review → `pull-request-review`
- Authorized security review → `security-review`
- Word/document automation → `document-r-automation`

## Tool/reference routing

- Current external library/API documentation → Context7
- Web browser automation/verification → Playwright CLI
- Supabase schema/config/project operations → official Supabase MCP
- UI design engineering and motion → Emil Kowalski Skills
- Additional UI workflow inspiration → UI Skills
- Local business/supplier/lead data → `Mahanaicoach/google-maps-scraper-kit`
- Authorized application security automation → Strix

## Shared rules

1. Inspect current repository state before non-trivial changes.
2. Identify the project platform.
3. Load only relevant standards, skills, and tools.
4. Project-specific rules override generic Diaco defaults when intentionally defined.
5. Do not invent missing state or DRAFT-standard details.
6. Keep changes scoped and reversible.
7. Verify before declaring completion.
8. Persist important state for the next session.
9. For business-data scraping, default to light targeted collection and verify important records.

## Verification

Before finishing:
- [ ] Correct standards/skills/tools were used.
- [ ] Repository state was inspected.
- [ ] Correct platform profile was selected.
- [ ] Relevant verification was performed.
- [ ] Significant changes received review when appropriate.
- [ ] DRAFT standards were not silently treated as approved.
- [ ] External UI guidance did not silently become Diaco identity.
- [ ] Scraped business data was cleaned/verified as appropriate.
- [ ] Durable state/handoff was updated when continuation is expected.
