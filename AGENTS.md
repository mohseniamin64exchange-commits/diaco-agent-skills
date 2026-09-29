# Diaco Agent Operating Rules

## Source of truth

For project work, prefer this order when information conflicts:

1. Current repository files and verified Git state
2. Project-specific rules/specifications and approved project references
3. Latest project handoff
4. Approved Diaco standards and relevant skills
5. Central hub global rules and approved working preferences
6. Conversation history

Do not assume an old chat accurately reflects the current repository.

## Before modifying an existing project

- inspect the target repository
- read its README / AGENTS / rules / handoff
- inspect the relevant files and tests
- identify existing patterns before creating new ones
- preserve unrelated working behavior
- read `00-AI-HUB/WORKING-PREFERENCES.md` when cross-project presentation or workflow preferences matter

## Standards layer

Before implementing a reusable feature, inspect `standards/README.md` and load the relevant standard.

Examples:
- project structure / onboarding → `standards/project-standard.md`
- structured data / Persian tables / lead-list output → `standards/structured-data-presentation-standard.md`
- UI/layout/components → `standards/ui-standard.md`
- printing → `standards/print-standard.md`
- backup/restore → `standards/backup-restore-standard.md`
- users/roles/permissions → `standards/user-management-standard.md`
- Windows application behavior → `standards/windows-app-standard.md`
- testing/verification → `standards/testing-standard.md`
- engineering tools → `standards/engineering-toolchain-standard.md`
- pull-request review → `standards/pull-request-review-standard.md`
- security review → `standards/security-review-standard.md`
- release/version/rollback → `standards/release-standard.md`

### Standard status rule

- **ACTIVE** means use it by default when relevant.
- **DRAFT** means do not invent missing details. Use an approved real project/reference implementation, then promote only approved reusable rules.
- Project-specific exceptions belong in the project's own `AGENTS.md`.

## Approved presentation behavior

When relevant:

- preserve approved information structure even when the visual theme changes,
- Persian structured data defaults to RTL,
- structured Persian table values are centered by default,
- numbered result lists start at 1 and continue without gaps unless filtering semantics require otherwise,
- Persian application shells prefer right-side primary navigation unless a project-specific approved reference differs,
- colors/icons/branding may vary by project without changing the approved information hierarchy.

Use:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`

## Engineering tool and reference selection

Use specialized tools/references when they improve the current task; do not install everything everywhere.

- External library/API work → Context7 when available.
- Web UI/browser verification → Playwright CLI when available.
- Supabase project work → official Supabase MCP when connected and authorized.
- UI polish, animation, prototyping, UI review, mobile-web craft, or UI-library choice → load `ui-design-engineering` and use `emilkowalski/skills` as the priority specialist reference.
- Additional UI workflow ideas → UI Skills.
- Authorized security review → Diaco security workflow and Strix when useful.
- Significant change before merge/release → Diaco pull-request review workflow.

Approved project UI and Diaco standards always take precedence over external UI references.

## During implementation

- keep changes scoped
- prefer small, reversible steps
- do not silently replace architecture
- do not delete code merely because it appears unused
- do not add dependencies without a reason
- do not commit credentials or secrets
- do not turn a DRAFT standard into a universal rule without evidence/approval
- do not convert external UI taste into a Diaco-wide visual rule without approval
- do not replace an approved information structure merely to make a theme look different

## Platform-aware rules

Diaco has one shared core and separate platform profiles.

Before implementation, identify the actual project platform from the repository. Then apply only the relevant platform-specific skill(s).

Examples:
- Windows desktop application → `skills/windows-desktop-standard/SKILL.md`
- Supabase/web application → `skills/supabase-webapp-guardrails/SKILL.md`

## Verification

A task is not complete merely because code was written.

Where applicable, verify:
- build
- tests
- type checking
- linting
- runtime behavior
- affected user flow
- browser flow with Playwright CLI for web changes when useful
- UI interaction/polish on the actual target platform
- structured data ordering/RTL/alignment for data-heavy output
- print/backup/restore behavior if changed
- security impact for security-sensitive changes

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

- `AGENTS.md`
- `HANDOFF.md`

New projects should start from:
- `templates/PROJECT-AGENTS.md`
- `templates/PROJECT-HANDOFF.md`

Existing projects can adopt this standard without restructuring the application.

The standard startup order for an Agent working on a project is:

1. Central hub: `00-AI-HUB/AGENT-START-HERE.md`
2. Approved working preferences: `00-AI-HUB/WORKING-PREFERENCES.md`
3. Shared Diaco rules: `diaco-agent-skills/AGENTS.md`
4. Relevant Diaco standard(s)
5. Relevant Diaco skill(s), including the correct platform profile
6. Project-specific `AGENTS.md`
7. Project `HANDOFF.md`
8. Actual repository files, tests, configuration, and Git state

Project-specific rules take precedence over generic Diaco defaults when intentionally defined.
