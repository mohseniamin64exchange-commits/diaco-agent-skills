---
name: local-business-data
description: Uses approved Diaco tooling to collect, clean, verify, and export local-business listing data for research, supplier discovery, lead generation, and CRM enrichment. Prefer the registered Google Maps Scraper Kit when appropriate.
---

# Local Business Data

## Preferred tool

Primary registered tool:
`Mahanaicoach/google-maps-scraper-kit`

Reference:
`references/google-maps-scraper-kit.md`

## Use when

- finding businesses by category and location
- supplier/vendor discovery
- local market research
- prospect/lead list creation
- enriching business records
- comparing local competitors

## Workflow

1. Clarify business type and geographic scope.
2. Decide which fields are actually needed.
3. Prefer a small validation run first.
4. Run a targeted scrape.
5. Clean and deduplicate results.
6. Verify high-value records when necessary.
7. Export in the format the project needs.
8. Record the source and date when results may be reused.

## Default fields

Prefer a compact business record unless more is needed:
- name
- category
- address
- phone
- website
- rating
- review count

Add email, coordinates, or socials only when the task benefits from them.

## Diaco defaults

- light use by default
- one job at a time
- avoid unnecessary high depth
- avoid repeated mass scraping
- do not install a separate scraper copy into every application
- prefer a reusable local/server service when this becomes a shared Jarvis capability

## Safety/data-quality

- scraped data may be stale or incomplete
- verify important contact or supplier records before operational use
- comply with applicable privacy, marketing, and platform rules
- scraping results do not imply permission for automated bulk contact

## Jarvis integration

Jarvis can call this capability as a discovery step and then pass results to:
- CRM workflows
- supplier comparison
- price/research workflows
- Telegram/notification workflows
- spreadsheets/reports
- project databases
