---
name: using-diaco-skills
description: Routes work to the appropriate Diaco standards, workflows, platform profile, and approved tools/references.
---

# Using Diaco Skills

## Skill routing

- Continuing work across sessions or Agents → `project-context-handoff`
- GitHub durable memory → `github-project-memory`
- Shared UI consistency → `shared-ui-system`
- Persian Excel/list/table output → `structured-data-output`
- UI polish / animation / prototyping / UI review → `ui-design-engineering`
- Local business / supplier / lead discovery → `local-business-data`
- Repeatable/automated marketing workflows → `automated-marketing-growth`
- Safe changes in existing codebases → `safe-existing-project-change`
- Supabase web apps → `supabase-webapp-guardrails`
- Windows desktop apps → `windows-desktop-standard`
- PR review → `pull-request-review`
- Authorized security review → `security-review`
- Word/document automation → `document-r-automation`

## Standard routing

- Persian structured tables / lead lists / spreadsheet layout → `standards/structured-data-presentation-standard.md`
- General UI → `standards/ui-standard.md`
- Tool selection → `standards/engineering-toolchain-standard.md`
- Testing → `standards/testing-standard.md`
- Security → `standards/security-review-standard.md`
- Release → `standards/release-standard.md`

## Tool/reference routing

- Current external library/API documentation → Context7
- Web browser verification → Playwright CLI
- Supabase operations → official Supabase MCP
- UI design engineering → Emil Kowalski Skills
- Additional UI reference → UI Skills
- Local business data → `Mahanaicoach/google-maps-scraper-kit`
- Marketing/growth execution → `coreyhaines31/marketingskills`
- Authorized security automation → Strix

## Marketing combination

When the user wants automated marketing:
1. load `automated-marketing-growth`
2. establish product-marketing context
3. use Google Maps Scraper Kit for discovery if local-business data is needed
4. use Marketing Skills for qualification/strategy/content/outreach preparation
5. use `structured-data-output` for Persian list/spreadsheet delivery
6. test on a small pilot
7. automate only after measurable validation

## Shared rules

1. Inspect current repository/data state.
2. Load only relevant standards, skills, and tools.
3. Project-specific rules override generic Diaco defaults.
4. Read `00-AI-HUB/WORKING-PREFERENCES.md` when reusable user preferences matter.
5. Do not invent missing state.
6. Keep changes scoped and reversible.
7. Verify before declaring completion.
8. Persist important state.
9. Preserve approved structure even when the project theme changes.
10. For marketing automation, do not scale before a pilot passes quality checks.
