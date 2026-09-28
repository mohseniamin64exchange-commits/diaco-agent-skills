# Diaco Project Standard

**Status:** ACTIVE  
**Version:** 0.1

## Minimum files

Every Diaco-managed application repository should contain:

- `AGENTS.md` — project-specific rules and precedence
- `HANDOFF.md` — current cross-session state
- `README.md` — project purpose and basic usage/build information

Use the templates in `templates/` when starting a new project.

## Startup order for an Agent

1. Central hub: `00-AI-HUB/AGENT-START-HERE.md`
2. Shared Diaco rules: `diaco-agent-skills/AGENTS.md`
3. Relevant Diaco skill(s)
4. Relevant Diaco standard(s)
5. Project-specific `AGENTS.md`
6. Project `HANDOFF.md`
7. Actual source, tests, configuration, and Git state

## Existing projects

Adopting Diaco does not justify restructuring a working codebase.

For an existing project:
- add the minimum continuity files,
- inspect existing architecture,
- preserve working conventions unless a change is explicitly required,
- migrate standards incrementally.

## Reuse rule

If a feature/pattern becomes reusable across projects, evaluate whether it belongs in:
- a shared standard,
- a reusable template/component,
- a dedicated Diaco skill,
- or a separate shared repository.

## Completion

Before ending substantial work:
- verify relevant behavior,
- record unresolved failures,
- update `HANDOFF.md` when continuation is expected,
- keep secrets out of Git.
