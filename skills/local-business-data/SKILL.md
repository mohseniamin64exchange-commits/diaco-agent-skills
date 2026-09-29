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
6. Create a useful human-facing classification when raw source categories are too technical.
7. Verify high-value records when necessary.
8. Export using the project's requested format.
9. For Persian spreadsheet/list output, load `structured-data-output`.
10. Record the source and date when results may be reused.

## Preferred business-list fields

For Persian user-facing output, prefer:

1. ردیف
2. نام کسب‌وکار
3. نوع / طبقه‌بندی کاربردی
4. دسته‌بندی منبع
5. آدرس خلاصه
6. شماره تلفن
7. وب‌سایت
8. امتیاز
9. تعداد Review

Add email, coordinates, socials, query source, or other fields only when the task benefits from them.

## Presentation rule

For Persian Excel/list output use:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`
- `references/babol-mechanics-excel-golden-template.md`

Structure is reusable; colors and branding may vary.

## Diaco defaults

- light use by default
- one job at a time
- avoid unnecessary high depth
- avoid repeated mass scraping
- do not install a separate scraper copy into every application
- prefer a reusable local/server service when this becomes a shared Agent capability

## Safety/data-quality

- scraped data may be stale or incomplete
- verify important contact or supplier records before operational use
- comply with applicable privacy, marketing, and platform rules
- scraping results do not imply permission for automated bulk contact
- never invent missing contact information to complete a row
