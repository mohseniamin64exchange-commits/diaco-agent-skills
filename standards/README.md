# Diaco Standards Registry

This directory contains reusable standards shared across Diaco projects.

## Status model

Each standard is marked with one of these states:

- **ACTIVE** — approved baseline; use by default when relevant.
- **DRAFT** — structure exists, but details are not yet approved as a universal Diaco standard.
- **PROJECT-REFERENCE** — a project may be used as the current reference implementation until the rule is promoted to ACTIVE.
- **DEPRECATED** — retained only for migration/history.

## Rule

Do not invent missing standards.

If a standard is DRAFT:
1. inspect the real project/reference implementation,
2. extract the repeated pattern,
3. ask for approval when the pattern would become universal,
4. then promote the rule to ACTIVE.

## Current standards

| Standard | Status | Purpose |
|---|---|---|
| [Project Standard](project-standard.md) | ACTIVE | Minimum structure and project continuity |
| [Structured Data Presentation Standard](structured-data-presentation-standard.md) | ACTIVE | Persian RTL structured data, table ordering, numbering and structure-vs-theme rules |
| [UI Standard](ui-standard.md) | DRAFT | Shared visual and interaction language |
| [Print Standard](print-standard.md) | DRAFT | Reusable print/preview conventions |
| [Backup & Restore Standard](backup-restore-standard.md) | DRAFT | Reusable backup and restore behavior |
| [User Management Standard](user-management-standard.md) | DRAFT | Reusable users/roles/permissions patterns |
| [Windows App Standard](windows-app-standard.md) | ACTIVE | Windows desktop platform baseline |
| [Testing Standard](testing-standard.md) | ACTIVE | Minimum verification discipline |
| [Engineering Toolchain Standard](engineering-toolchain-standard.md) | ACTIVE | Context7, Playwright CLI, Supabase MCP, UI references, business-data and marketing tool-selection policy |
| [Pull Request Review Standard](pull-request-review-standard.md) | ACTIVE | Diff-based pre-merge quality gate |
| [Security Review Standard](security-review-standard.md) | ACTIVE | Authorized application-security review |
| [Release Standard](release-standard.md) | ACTIVE | Versioning, release, rollback and handoff |

## Promotion rule

A pattern should be considered for Diaco standardization when:
- it is reused in more than one project, or
- the user explicitly says it should become the standard, or
- it is a foundational cross-project rule such as handoff, security, testing, data presentation, or Git discipline.

Project-specific exceptions remain allowed and must be documented in that project's `AGENTS.md`.
