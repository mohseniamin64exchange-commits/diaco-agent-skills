# Diaco Agent Operating Rules

## Source of truth

For project work, prefer this order when information conflicts:

1. Current repository files and verified Git state
2. Project-specific rules/specifications
3. Latest project handoff
4. Approved Diaco standards and relevant skills
5. Central hub guidance
6. Conversation history

Do not assume an old chat accurately reflects the current repository.

## Before modifying an existing project

- inspect the target repository
- read its README / AGENTS / rules / handoff
- inspect the relevant files and tests
- identify existing patterns before creating new ones
- preserve unrelated working behavior

## Standards layer

Before implementing a reusable feature, inspect `standards/README.md` and load the relevant standard.

Examples:
- project structure / onboarding → `standards/project-standard.md`
- UI/layout/components → `standards/ui-standard.md`
- printing → `standards/print-standard.md`
- backup/restore → `standards/backup-restore-standard.md`
- users/roles/permissions → `standards/user-management-standard.md`
- Windows application behavior → `standards/windows-app-standard.md`
- testing/verification → `standards/testing-standard.md`
- release/version/rollback → `standards/release-standard.md`

### Standard status rule

- **ACTIVE** means use it by default when relevant.
- **DRAFT** means do not invent missing details. Use an approved real project/reference implementation, then promote only approved reusable rules.
- Project-specific exceptions belong in the project's own `AGENTS.md`.

## During implementation

- keep changes scoped
- prefer small, reversible steps
- do not silently replace architecture
- do not delete code merely because it appears unused
- do not add dependencies without a reason
- do not commit credentials or secrets
- do not turn a DRAFT standard into a universal rule without evidence/approval

## Platform-aware rules

Diaco has one shared core and separate platform profiles.

Before implementation, identify the actual project platform from the repository. Then apply only the relevant platform-specific skill(s).

Examples:
- Windows desktop application → `skills/windows-desktop-standard/SKILL.md`
- Supabase/web application → `skills/supabase-webapp-guardrails/SKILL.md`

Do not automatically apply web/Supabase assumptions to a Windows desktop project, and do not force desktop conventions onto a web project.

## Verification

A task is not complete merely because code was written.

Where applicable, verify:
- build
- tests
- type checking
- linting
- runtime behavior
- affected user flow
- print/backup/restore behavior if changed

If verification fails, record the failure instead of declaring success.

## Cross-session persistence

When work is likely to continue in another session or Agent:
- update the project's handoff
- record the current branch/commit when useful
- record what changed
- record what was verified
- record unresolved problems
- record the next action
- record important do-not-change constraints

## External repositories

When adopting third-party work:
- preserve attribution and licensing
- record the original upstream
- keep upstream and Diaco-customized versions distinguishable
- avoid pretending third-party work was authored by Diaco

## Standard project adoption rule

Every Diaco-managed application repository should contain at minimum:

- `AGENTS.md` — project-specific operating rules and rule precedence
- `HANDOFF.md` — current cross-session project state

New projects should start from:
- `templates/PROJECT-AGENTS.md`
- `templates/PROJECT-HANDOFF.md`

Existing projects can adopt this standard without restructuring the application.

The standard startup order for an Agent working on a project is:

1. Central hub: `00-AI-HUB/AGENT-START-HERE.md`
2. Shared Diaco rules: `diaco-agent-skills/AGENTS.md`
3. Relevant Diaco standard(s)
4. Relevant Diaco skill(s), including the correct platform profile
5. Project-specific `AGENTS.md`
6. Project `HANDOFF.md`
7. Actual repository files, tests, configuration, and Git state

Project-specific rules take precedence over generic Diaco defaults when intentionally defined.
