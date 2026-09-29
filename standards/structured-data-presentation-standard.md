# Diaco Structured Data Presentation Standard

**Status:** ACTIVE  
**Version:** 1.0

## Goal

Keep structured data outputs consistent across spreadsheets, reports, business lists, admin tables, and data-heavy application screens while allowing each project to use its own visual theme.

## Core principle

**Structure is reusable. Theme is replaceable.**

Do not confuse:
- information architecture, ordering, alignment, direction, and behavior
with
- colors, icons, branding, shadows, and decoration.

A project may change the visual skin without changing the approved information structure.

## Persian data presentation

For Persian-first structured outputs:

- use RTL direction,
- keep structured table cells centered by default,
- keep headers clearly separated from data,
- use predictable field order,
- use continuous numbering starting at 1 when rows represent an ordered result set,
- keep key identifiers and contact fields easy to scan,
- prefer compact, readable information over unnecessary raw fields.

Exceptions are allowed when a field's semantics clearly require a different alignment or a project-specific approved reference says otherwise.

## Business / lead-list core schema

Preferred core order:

1. `ردیف`
2. `نام کسب‌وکار`
3. human-friendly type/classification, e.g. `نوع تعمیرگاه`
4. source category, e.g. `دسته‌بندی`
5. `آدرس خلاصه`
6. `شماره تلفن`
7. `وب‌سایت`
8. rating, e.g. `امتیاز Google`
9. review count, e.g. `تعداد Review`

Additional task-specific fields may be added, but preserve the core reading order when practical.

## Spreadsheet behavior

For polished Persian list workbooks:

- worksheet direction: RTL,
- hide gridlines when a formatted table is used,
- title and optional subtitle may span the table width,
- leave visual separation between title/subtitle and the table header,
- freeze the table header area for long lists,
- enable filtering on the actual data table,
- use readable fixed widths instead of uncontrolled autofit,
- center headers and structured data by default,
- use restrained borders/row banding for scanability,
- preserve phone numbers as text when needed,
- format ratings consistently,
- never invent missing values.

## Application / website behavior

For Persian data-heavy applications:

- RTL is the default reading direction,
- right-side primary sidebar/navigation is the preferred baseline unless an approved project reference differs,
- tables and forms should preserve consistent field ordering across screens,
- structured table values are centered by default,
- colors and icons may vary by project without changing the information hierarchy.

## Theme flexibility

The following are **not** fixed by this standard:

- exact colors,
- icon family,
- font family,
- border radius,
- shadow values,
- decorative backgrounds,
- brand-specific visual identity.

These belong to the project theme or the broader UI standard.

## Verification

Before delivering a structured data output:

- [ ] RTL is correct for Persian output.
- [ ] Core fields follow an intentional order.
- [ ] Row numbering is continuous when used.
- [ ] Data cells are aligned consistently.
- [ ] Duplicate or obviously irrelevant records were handled when relevant.
- [ ] Missing data was not fabricated.
- [ ] Long tables remain usable through freeze/filter or equivalent behavior.
- [ ] Theme changes did not break the approved structure.

## Reference implementation

See:

`references/babol-mechanics-excel-golden-template.md`
