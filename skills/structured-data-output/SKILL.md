---
name: structured-data-output
description: Creates consistent Persian RTL structured outputs such as Excel lead lists, business directories, data tables, and report tables using the user's approved information structure while allowing project-specific colors and icons.
---

# Structured Data Output

## Use when

- creating Persian Excel workbooks
- exporting lead/business lists
- creating directory tables
- designing data-heavy admin tables
- converting scraper/API results into polished user-facing data
- the user asks for "خروجی استاندارد من" or equivalent

## Required standard

Read:

`standards/structured-data-presentation-standard.md`

For Excel/business-list tasks also read:

`references/babol-mechanics-excel-golden-template.md`

## Workflow

1. Identify the actual data source and fields.
2. Remove irrelevant raw fields unless the user needs them.
3. Deduplicate when applicable.
4. Create useful human-facing categories separately from source categories when useful.
5. Apply the approved Persian information order.
6. Number rows continuously from 1.
7. Apply RTL direction.
8. Center structured tabular data by default.
9. Add filter/freeze behavior for long tables when the output format supports it.
10. Apply the current project theme without changing the approved structure.
11. Verify that missing values were not invented.

## Business-list baseline

Prefer:

`ردیف → نام کسب‌وکار → نوع کاربردی → دسته‌بندی منبع → آدرس خلاصه → شماره تلفن → وب‌سایت → امتیاز → تعداد Review`

Add task-specific fields only when they improve the output.

## Structure vs theme

Preserve:
- RTL
- order
- hierarchy
- alignment logic
- numbering
- table usability

Allow project-specific variation in:
- colors
- icons
- fonts when required by the project
- decorative styling
- brand identity

## Verification

- [ ] Persian RTL is enabled.
- [ ] Row numbering is continuous.
- [ ] Core columns are ordered intentionally.
- [ ] Structured data cells are centered unless a justified exception exists.
- [ ] Categories are understandable.
- [ ] Duplicates/irrelevant rows were handled when required.
- [ ] Missing data was not fabricated.
- [ ] Theme changes did not change the information architecture.
