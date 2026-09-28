# Diaco Agent Skills

Reusable workflows, shared standards, and platform profiles for AI-assisted projects.

**Current version:** 0.2.0

This repository is the **custom skill and standards layer** used across Diaco projects. It is intentionally separate from application repositories and from third-party upstream repositories.

## Purpose

Diaco Agent Skills exists to make project work portable across:
- different ChatGPT accounts
- mobile and desktop
- Codex and other coding agents
- new chat sessions
- different machines
- different application platforms

The repository stores **how we work**, not the full source code of every product.

## Architecture

Diaco is organized in layers:

1. **Core operating rules** — source of truth, safe changes, verification, handoff, Git discipline.
2. **Shared standards** — reusable conventions such as project structure, UI, printing, backup/restore, users, testing, and releases.
3. **Skills** — operational workflows for recurring tasks.
4. **Platform profiles** — rules that apply only to the actual technology/platform, such as Windows Desktop or Supabase/Web.
5. **Project-specific rules** — intentional constraints and exceptions stored in each application's own `AGENTS.md`.

The core stays stable. Standards are applied when relevant. Platform-specific rules are applied only when the actual project uses that platform.

## Start here

Agents should begin with:

1. `AGENTS.md`
2. `skills/using-diaco-skills/SKILL.md`
3. relevant shared standard(s) from `standards/`
4. relevant operational skill(s)
5. the platform profile relevant to the project
6. project-specific `AGENTS.md` and `HANDOFF.md`
7. actual project files and Git state

## Standards

See `standards/README.md` for the registry and status of every standard.

### ACTIVE
- Project Standard
- Windows Application Standard
- Testing & Verification Standard
- Release Standard

### DRAFT — awaiting approved real reference implementations
- UI Standard
- Print Standard
- Backup & Restore Standard
- User Management Standard

A DRAFT standard must not be filled with invented visual or behavioral details. Approved real implementations are used to promote specific rules to ACTIVE.

## Skills

### Core/shared
- `using-diaco-skills`
- `project-context-handoff`
- `github-project-memory`
- `shared-ui-system`
- `safe-existing-project-change`
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
7. Keep secrets out of Git.
8. Distinguish third-party upstream projects from Diaco-customized versions.
9. Leave a usable handoff for the next Agent.
10. Detect the project platform before applying platform-specific rules.
11. Do not invent details for a DRAFT standard.

## Relationship to upstream Agent Skills

This project was inspired in part by the workflow-oriented approach in:

`addyosmani/agent-skills`

The upstream repository remains a separate external reference. See `UPSTREAM.md`.

Diaco-specific workflows and standards are maintained independently here.
