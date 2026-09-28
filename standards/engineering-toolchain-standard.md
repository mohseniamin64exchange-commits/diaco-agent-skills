# Diaco Engineering Toolchain Standard

**Status:** ACTIVE  
**Version:** 0.2

## Goal

Use specialized engineering tools only when they improve correctness, context quality, verification, design quality, or security. Do not install every tool into every project.

## Tool selection

### Context7 — current library/API documentation

**Use when:**
- implementing or debugging code against an external library/framework/API,
- syntax or behavior is version-sensitive,
- the Agent may otherwise rely on stale model knowledge.

**Diaco rule:**
- Prefer Context7 for current, version-specific documentation when available.
- If Context7 is unavailable or incomplete, use the official vendor documentation.
- Project source and lockfiles/package manifests determine the actual installed version.
- Documentation retrieval does not override project-specific constraints.

### Playwright CLI — browser automation for coding Agents

**Use when:**
- the project is a web application,
- a browser user flow must be verified,
- screenshots, traces, selectors, or generated browser tests are useful.

**Diaco rule:**
- Prefer Playwright CLI for agent-driven browser interaction when available.
- Keep the project's existing automated test suite authoritative.
- Do not apply Playwright CLI to native Windows desktop UI.
- Persist durable regression tests in the project when a one-off browser check exposes an important bug.

### Supabase MCP — direct Supabase project access

**Use when:**
- the project actually uses Supabase,
- the Agent needs current schema/config/log/project information,
- an authorized connection exists.

**Diaco rule:**
- Prefer the official Supabase MCP over guessing schema or configuration.
- Confirm the correct organization/project/environment before writes.
- Use least privilege where practical.
- Never place service-role keys, access tokens, or database passwords in Git.
- Destructive production changes require explicit scope and a recovery/migration plan.

### Emil Kowalski Skills — priority Design Engineering reference

**Use when:**
- creating or polishing UI,
- deciding whether and how to animate,
- reviewing interaction quality,
- comparing multiple UI directions,
- choosing a UI/component library,
- improving mobile-web behavior,
- working with React Native/Expo motion where relevant.

**Diaco rule:**
- Treat `emilkowalski/skills` as the priority specialist reference for UI craft and motion.
- Project-specific approved UI and the Diaco UI Standard remain authoritative.
- Use isolated prototyping when the visual direction is undecided and comparison would help.
- Do not import external colors, typography, layout, animation constants, or dependencies as Diaco-wide defaults without approval.
- For native Windows projects, adapt principles rather than blindly applying web/CSS implementation details.

See:
- `references/emil-kowalski-skills.md`
- `skills/ui-design-engineering/SKILL.md`

### UI Skills — additional design workflow reference

**Use when:**
- a reusable design workflow, capture method, or interaction pattern helps,
- additional frontend/UI reference material is useful.

**Diaco rule:**
- Treat UI Skills as an additional reference library.
- Emil Kowalski Skills is the priority specialist reference for design engineering/motion.
- Diaco's approved UI Standard and the project's approved reference implementation take precedence over both.

### Strix — application security testing

**Use when:**
- performing an authorized security review of our own application/environment,
- preparing a significant release,
- high-risk auth, permissions, API, or exposed web functionality changed.

**Diaco rule:**
- Prefer local/staging/test environments.
- Use non-destructive testing by default.
- Do not target systems we do not own or have permission to test.
- Treat automated findings as evidence to verify, not unquestionable truth.
- Security fixes must be regression-tested.

### Pull Request Review — quality gate

This is a Diaco capability, not a dependency on one specific third-party plugin.

**Use when:**
- a significant feature/fix/refactor is ready to merge,
- a risky data/security change is proposed,
- another Agent has made substantial changes.

**Diaco rule:**
Review the actual diff/PR for:
- correctness
- regressions
- scope creep
- security/privacy
- data and migration risks
- missing tests
- platform-specific risks
- documentation/handoff impact

Use available GitHub/Agent review tooling, but keep the review criteria owned by Diaco.

## Installation policy

- Do not globally add dependencies to application repositories just because a tool/reference is approved here.
- Install or connect a tool when the current project/task needs it.
- Prefer official packages/repositories and current vendor documentation.
- External skill repositories may be consulted without becoming project dependencies.
- Record project-local setup only when another Agent needs it to reproduce the workflow.

## Precedence

1. Project-specific rules and approved project references
2. Current repository state
3. Diaco ACTIVE standards
4. Specialist external references/tools
5. Generic Agent assumptions
