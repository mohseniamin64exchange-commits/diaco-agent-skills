# Babol Mechanics Excel — Approved Golden Template Reference

## Reference file

User-approved workbook:

`babol_mechanics_clean_rtl.xlsx`

Observed SHA-256:

`8d35f73dc9fc12f8f961c68c5a1a475a68041456b77a09e3c2dfe5cff46c6f3a`

This reference records the reusable structure observed in that workbook. The source workbook itself remains a user-provided reference artifact.

## Observed workbook structure

Worksheet:
- `تعمیرگاه‌های بابل`

Used range:
- `A1:I44`

Direction and view:
- RTL enabled
- gridlines hidden
- rows 1–4 frozen; data begins at row 5

Merged presentation:
- `A1:I1` — title
- `A2:I2` — subtitle
- row 3 — visual separator
- row 4 — table headers

Table:
- range `A4:I44`
- filtering enabled
- row striping enabled
- current table style: `TableStyleMedium2`

## Approved column order

1. `ردیف`
2. `نام کسب‌وکار`
3. `نوع تعمیرگاه`
4. `دسته‌بندی`
5. `آدرس خلاصه`
6. `شماره تلفن`
7. `وب‌سایت`
8. `امتیاز Google`
9. `تعداد Review`

The semantic pattern is more important than the exact subject-specific wording:
- ordinal
- primary entity name
- useful human classification
- source/original category
- concise location
- phone
- website
- rating
- review count

## Observed alignment and typography

- title: centered, bold, Arial 15
- subtitle: centered, italic, Arial 10
- header: centered, bold, Arial 10
- body: centered, Arial 10
- header wrapping enabled
- rating format: one decimal place
- row numbering: continuous starting at 1

## Observed sizing

Column widths:
- A: 7
- B: 28
- C: 22
- D: 26
- E: 48
- F: 20
- G: 32
- H: 14
- I: 14

Key row heights:
- row 1: 30
- row 2: 21.95
- row 4: 27.95

## Observed current visual skin

Current header/tab accent is based on dark blue `#1F4E78` with white header text.

This color is **reference-specific, not a universal Diaco color**.

The user explicitly approved:
- the structure,
- RTL behavior,
- centered data presentation,
- ordering,
- numbering,
- clean table organization.

The user explicitly allows these to change by project:
- colors,
- icons,
- branding,
- visual decoration.

## Reuse rule

When the user asks for:
- "خروجی استاندارد من"
- "طبق ساختار اکسل من"
- "مثل فایل قبلی مرتبش کن"
- or an equivalent request for a Persian structured list,

reuse the structural rules in `standards/structured-data-presentation-standard.md` and adapt the theme to the current project.
