# Diaco Engineering Toolchain Standard

**Status:** ACTIVE  
**Version:** 0.3

## Goal

Use specialized engineering tools only when they improve correctness, context quality, verification, design quality, business-data gathering, or security. Do not install every tool into every project.

## Tool selection

### Context7 — current library/API documentation

Use for version-sensitive external libraries/frameworks/APIs.

**Diaco rule:**
- Prefer Context7 for current, version-specific documentation when available.
- If unavailable or incomplete, use official vendor documentation.
- Project source and lockfiles determine the actual installed version.

### Playwright CLI — browser automation for coding Agents

Use for web UI/browser flow verification, screenshots, traces, selectors, and interaction checks.

**Diaco rule:**
- Prefer Playwright CLI for agent-driven browser interaction when available.
- Existing project tests remain authoritative.
- Do not apply it to native Windows desktop UI.

### Supabase MCP — direct Supabase project access

Use when a project actually uses Supabase and authorized access exists.

**Diaco rule:**
- Prefer the official Supabase MCP over guessing schema/configuration.
- Confirm organization/project/environment before writes.
- Keep credentials and secrets out of Git.
- Destructive production changes require explicit scope and recovery/migration planning.

### Emil Kowalski Skills — priority Design Engineering reference

Use for UI polish, motion, animation review, prototyping, component/library selection, and mobile-web craft.

**Diaco rule:**
- Project-approved UI and the Diaco UI Standard remain authoritative.
- Use external guidance to improve craft, not to silently define Diaco visual identity.

### UI Skills — additional design workflow reference

Use as an additional frontend/UI reference when helpful.

### Google Maps Scraper Kit — priority Local Business Data tool

Primary registered source:
`Mahanaicoach/google-maps-scraper-kit`

Use when the task needs:
- local business discovery
- supplier/vendor discovery
- lead/prospect lists
- local market research
- competitor discovery
- business contact enrichment

**Diaco rule:**
- Default to light, targeted use.
- Prefer small validation runs and one job at a time.
- Keep depth conservative unless the user explicitly needs more.
- Clean and deduplicate results before downstream use.
- Verify important business records before relying on them operationally.
- Do not treat scraping results as permission for automated bulk outreach.
- Prefer one reusable local/server deployment rather than installing a scraper into every application.
- Do not silently substitute a different fork for the user-selected repository.

See:
- `references/google-maps-scraper-kit.md`
- `skills/local-business-data/SKILL.md`

### Strix — application security testing

Use for authorized security reviews of systems we own or are explicitly allowed to test.

**Diaco rule:**
- Prefer local/staging/test environments.
- Use non-destructive testing by default.
- Validate automated findings before treating them as confirmed.

### Pull Request Review — quality gate

This is a Diaco capability rather than a dependency on one particular plugin.

Use available GitHub/Agent review tooling while keeping the review criteria owned by Diaco.

## Installation policy

- Do not globally add dependencies just because a tool/reference is approved.
- Install/connect a tool when the current task needs it.
- Prefer shared services for reusable capabilities where practical.
- Preserve source attribution/licensing.
- Record project-local setup only when another Agent needs it to reproduce the workflow.

## Precedence

1. Project-specific rules and approved project references
2. Current repository state
3. Diaco ACTIVE standards
4. Specialist external references/tools
5. Generic Agent assumptions
