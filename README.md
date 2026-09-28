# Diaco Agent Skills

Reusable workflows, shared standards, engineering tool selection, design-engineering references, business-data tooling, and platform profiles for AI-assisted projects.

**Current version:** 0.5.0

This repository is the custom skill and standards layer used across Diaco projects. It is intentionally separate from application repositories and third-party upstream repositories.

## Architecture

Diaco is organized in layers:

1. Core operating rules
2. Shared standards
3. Skills
4. Platform profiles
5. Specialized tools/references
6. Project-specific rules

## Start here

Agents should begin with:
1. `AGENTS.md`
2. `skills/using-diaco-skills/SKILL.md`
3. relevant standards
4. relevant operational skills
5. relevant specialized tools/references
6. correct platform profile
7. project-specific `AGENTS.md` and `HANDOFF.md`
8. actual repository files and Git state

## Approved engineering tools and references

Use only when relevant:

- **Context7** — current version-specific library/API documentation
- **Playwright CLI** — agent-driven browser automation for web projects
- **Supabase MCP** — direct Supabase project access when connected and authorized
- **Emil Kowalski Skills** — Priority UI / Design Engineering Reference
- **UI Skills** — additional external design/workflow reference
- **Google Maps Scraper Kit** — **Priority Local Business Data / Lead Generation Tool**
- **Strix** — authorized application-security testing
- **Pull Request Review** — Diaco-owned quality gate

### Google Maps business-data source

Official Diaco-selected repository:

`Mahanaicoach/google-maps-scraper-kit`

Use it for supplier discovery, local business research, prospect/lead lists, CRM enrichment, and related Jarvis workflows. Default to light, targeted use.

See:
- `references/google-maps-scraper-kit.md`
- `skills/local-business-data/SKILL.md`

## UI reference precedence

1. approved project-specific UI/reference
2. ACTIVE Diaco UI rules
3. Emil Kowalski Skills
4. UI Skills and other external references

## Standards

See `standards/README.md`.

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

## Skills

### Core/shared
- `using-diaco-skills`
- `project-context-handoff`
- `github-project-memory`
- `shared-ui-system`
- `ui-design-engineering`
- `local-business-data`
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
7. Use specialized tools/references only when they fit the task.
8. Keep secrets out of Git.
9. Distinguish third-party upstream projects from Diaco-customized versions.
10. Leave a usable handoff for the next Agent.
11. Detect the platform before applying platform-specific rules.
12. Do not invent details for DRAFT standards.
13. External UI expertise may improve implementation quality but may not silently become Diaco visual identity.
14. Business-data collection should be targeted, cleaned, and verified before important downstream use.
