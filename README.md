# Diaco Agent Skills

Reusable workflows and operating rules for AI-assisted projects.

This repository is the **custom skill layer** used across Diaco projects. It is intentionally separate from application repositories and from third-party upstream repositories.

## Purpose

Diaco Agent Skills exists to make project work portable across:
- different ChatGPT accounts
- mobile and desktop
- Codex and other coding agents
- new chat sessions
- different machines

The repository stores **how we work**, not the full source code of every product.

## Core principles

1. GitHub is the durable source of truth.
2. Important project state must not live only in chat history.
3. Read before modifying an existing project.
4. Preserve scope and working behavior.
5. Verify changes with evidence.
6. Keep UI/design conventions reusable.
7. Keep secrets out of Git.
8. Distinguish third-party upstream projects from Diaco-customized versions.
9. Leave a usable handoff for the next Agent.

## Start here

Agents should begin with:

1. `AGENTS.md`
2. `skills/using-diaco-skills/SKILL.md`
3. the specific skill relevant to the task

## Initial skills

- `using-diaco-skills`
- `project-context-handoff`
- `github-project-memory`
- `shared-ui-system`
- `safe-existing-project-change`
- `supabase-webapp-guardrails`
- `document-r-automation`

## Relationship to upstream Agent Skills

This project was inspired in part by the workflow-oriented approach in:

`addyosmani/agent-skills`

The upstream repository remains a separate external reference. See `UPSTREAM.md`.

Diaco-specific workflows are maintained independently here.
