# Diaco Agent Operating Rules

## Source of truth

For project work, prefer this order when information conflicts:

1. Current repository files and Git state
2. Project-specific rules/specifications
3. Latest project handoff
4. Diaco shared skills and references
5. Conversation history

Do not assume an old chat accurately reflects the current repository.

## Before modifying an existing project

- inspect the target repository
- read its README / AGENTS / rules / handoff
- inspect the relevant files and tests
- identify existing patterns before creating new ones
- preserve unrelated working behavior

## During implementation

- keep changes scoped
- prefer small, reversible steps
- do not silently replace architecture
- do not delete code merely because it appears unused
- do not add dependencies without a reason
- do not commit credentials or secrets

## Verification

A task is not complete merely because code was written.

Where applicable, verify:
- build
- tests
- type checking
- linting
- runtime behavior
- affected user flow

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

Existing projects can adopt this standard without restructuring the application: add these two files first, then preserve the existing architecture unless the task explicitly requires changes.

The standard startup order for an Agent working on a project is:

1. Central hub: `00-AI-HUB/AGENT-START-HERE.md`
2. Shared Diaco rules: `diaco-agent-skills/AGENTS.md`
3. Relevant Diaco skill(s)
4. Project-specific `AGENTS.md`
5. Project `HANDOFF.md`
6. Actual repository files and Git state

Project-specific rules take precedence over generic Diaco defaults when intentionally defined.
