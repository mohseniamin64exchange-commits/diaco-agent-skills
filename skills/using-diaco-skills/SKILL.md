---
name: using-diaco-skills
description: Routes work to the appropriate Diaco standards, workflows, platform profile, and approved tools/references.
---

# Using Diaco Skills

## Skill routing

- Continuing work across sessions or Agents → `project-context-handoff`
- GitHub durable memory → `github-project-memory`
- Shared UI consistency → `shared-ui-system`
- UI polish / animation / prototyping / UI review → `ui-design-engineering`
- Local business / supplier / lead discovery → `local-business-data`
- Repeatable/automated marketing workflows → `automated-marketing-growth`
- Safe changes in existing codebases → `safe-existing-project-change`
- Supabase web apps → `supabase-webapp-guardrails`
- Windows desktop apps → `windows-desktop-standard`
- PR review → `pull-request-review`
- Authorized security review → `security-review`
- Word/document automation → `document-r-automation`

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
5. test on a small pilot
6. automate only after measurable validation

## Shared rules

1. Inspect current repository/data state.
2. Load only relevant standards, skills, and tools.
3. Project-specific rules override generic Diaco defaults.
4. Do not invent missing state.
5. Keep changes scoped and reversible.
6. Verify before declaring completion.
7. Persist important state.
8. For marketing automation, do not scale before a pilot passes quality checks.
