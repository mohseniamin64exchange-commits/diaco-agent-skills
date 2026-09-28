# Diaco Agent Skills

Reusable workflows, shared standards, engineering tool selection, and platform profiles for AI-assisted projects.

**Current version:** 0.3.0

This repository is the **custom skill and standards layer** used across Diaco projects. It is intentionally separate from application repositories and third-party upstream repositories.

## Architecture

Diaco is organized in layers:

1. **Core operating rules** — source of truth, safe changes, verification, handoff, Git discipline.
2. **Shared standards** — project structure, UI, printing, backup/restore, users, testing, security, PR review, releases, and engineering tool selection.
3. **Skills** — operational workflows for recurring tasks.
4. **Platform profiles** — rules for the actual technology/platform, such as Windows Desktop or Supabase/Web.
5. **Specialized tools** — used only when they improve the current task.
6. **Project-specific rules** — constraints and exceptions stored in each application's own `AGENTS.md`.

## Start here

Agents should begin with:

1. `AGENTS.md`
2. `skills/using-diaco-skills/SKILL.md`
3. relevant standards from `standards/`
4. relevant operational skills
5. relevant specialized tools
6. the correct platform profile
7. project-specific `AGENTS.md` and `HANDOFF.md`
8. actual project files and Git state

## Approved engineering tools

Use only when relevant:

- **Context7** — current version-specific library/API documentation
- **Playwright CLI** — preferred agent-driven browser automation for web projects
- **Supabase MCP** — preferred direct Supabase project access when connected and authorized
- **UI Skills** — external design/workflow reference; not authoritative over Diaco UI
- **Strix** — authorized application-security testing when appropriate
- **Pull Request Review** — Diaco-owned quality gate independent of any single plugin

See `standards/engineering-toolchain-standard.md`.

## Standards

See `standards/README.md` for the authoritative registry.

### ACTIVE
- Project Standard
- Windows Application Standard
- Testing & Verification Standard
- Engineering Toolchain Standard
- Pull Request Review Standard
- Security Review Standard
- Release Standard

### DRAFT
- UI Standard
- Print Standard
- Backup & Restore Standard
- User Management Standard

DRAFT standards must not be filled with invented visual or behavioral details.

## Skills

### Core/shared
- `using-diaco-skills`
- `project-context-handoff`
- `github-project-memory`
- `shared-ui-system`
- `safe-existing-project-change`
- `pull-request-review`
- `security-review`
- `document-r-automation`

### Platform profiles
- `supabase-webapp-guardrails`
- `windows-desktop-standard`

## Core principles

1. GitHub is the durable source of truth.
2. Important project state must not live only in chat history.
3. Read before modifying an existing project.
4. Preserve scope and working behavior.
5. Verify changes with evidence.
6. Reuse approved standards instead of reinventing recurring behavior.
7. Use specialized tools only when they fit the task.
8. Keep secrets out of Git.
9. Distinguish third-party upstream projects from Diaco-customized versions.
10. Leave a usable handoff for the next Agent.
11. Detect the project platform before applying platform-specific rules.
12. Do not invent details for a DRAFT standard.

## Upstream references

Important third-party tools and references are registered in `00-AI-HUB`. Diaco keeps external ownership/licensing separate from our own standards and workflows.
