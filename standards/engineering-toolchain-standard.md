# Diaco Engineering Toolchain Standard

**Status:** ACTIVE  
**Version:** 0.4

## Goal

Use specialized engineering and business tools only when they improve correctness, context quality, verification, design quality, business-data gathering, marketing execution, or security. Do not install every tool into every project.

## Tool selection

### Context7
Use for version-sensitive external libraries/frameworks/APIs.

### Playwright CLI
Use for web UI/browser flow verification.

### Supabase MCP
Use for authorized Supabase project/schema/config access.

### Emil Kowalski Skills
Use for UI polish, motion, prototyping, and design-engineering review.

### UI Skills
Use as an additional UI/frontend reference.

### Google Maps Scraper Kit — priority Local Business Data tool

Primary source:
`Mahanaicoach/google-maps-scraper-kit`

Use for:
- local business discovery
- supplier/vendor discovery
- lead/prospect lists
- local market research
- competitor discovery
- business contact enrichment

Rules:
- light targeted use by default
- small validation runs first
- clean/deduplicate before downstream use
- verify important business records
- do not treat scraped data as outreach consent

See:
- `references/google-maps-scraper-kit.md`
- `skills/local-business-data/SKILL.md`

### Marketing Skills — priority Marketing & Growth reference

Primary source:
`coreyhaines31/marketingskills`

Use for:
- product marketing
- prospecting
- customer research
- competitor analysis
- content/copy
- SEO/AI SEO
- CRO
- ads
- email/cold email
- pricing
- launch
- analytics/attribution
- revops
- marketing loops

Rule:
- build product-marketing context first when downstream work depends on product/audience/positioning.
- real business/product/customer data remains authoritative.
- do not treat generated output as successful until measurable validation exists.

See:
- `references/marketing-skills.md`
- `skills/automated-marketing-growth/SKILL.md`

### Automated Marketing Pipeline

Preferred combined workflow:
1. product context
2. business discovery
3. clean/deduplicate
4. qualify/segment
5. generate appropriate marketing output
6. human checkpoint before real outbound action
7. measure results
8. automate only after a successful pilot

### Strix
Use for authorized security reviews.

### Pull Request Review
Use as a Diaco-owned quality gate.

## Installation policy

- Do not globally add dependencies just because a tool/reference is approved.
- Install/connect a tool when the current task needs it.
- Prefer shared services for reusable capabilities.
- Preserve source attribution/licensing.
- Record project-local setup only when another Agent needs it.

## Precedence

1. Project-specific rules and real business/project data
2. Current repository state
3. Diaco ACTIVE standards
4. Specialist external references/tools
5. Generic Agent assumptions
