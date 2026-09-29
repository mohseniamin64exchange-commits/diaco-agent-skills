# Diaco Agent Skills

Reusable workflows, shared standards, engineering tools, design-engineering references, business-data tooling, structured-data presentation, and repeatable marketing workflows for AI-assisted projects.

**Current version:** 0.7.0

## Important capabilities

- project continuity and GitHub-backed memory
- Windows and Supabase platform profiles
- UI design engineering
- **approved Persian structured-data presentation**
- local-business and supplier discovery
- repeatable marketing and growth workflows
- testing, security review, and PR review

## Approved cross-project presentation model

Diaco now explicitly separates:

**Structure**
- information order
- hierarchy
- RTL/LTR behavior
- alignment logic
- row numbering
- navigation placement
- table/form organization

from:

**Theme**
- colors
- icons
- branding
- decorative styling

Approved Persian defaults:
- RTL for Persian-first structured output
- centered structured table data by default
- continuous numbering from 1 for result lists
- right-side primary navigation/sidebar as the preferred Persian application baseline unless a project-specific approved reference differs

Authoritative files:
- `standards/structured-data-presentation-standard.md`
- `skills/structured-data-output/SKILL.md`
- `references/babol-mechanics-excel-golden-template.md`

## Business / lead-list output

The approved baseline was extracted from the user-approved workbook `babol_mechanics_clean_rtl.xlsx`.

Preferred order:
`ردیف → نام کسب‌وکار → نوع کاربردی → دسته‌بندی منبع → آدرس خلاصه → شماره تلفن → وب‌سایت → امتیاز → تعداد Review`

The workbook's current blue theme is a reference theme only; it is not a universal Diaco color rule.

## Marketing workflow

Diaco treats this combination as an important reusable capability:

- `Mahanaicoach/google-maps-scraper-kit`
- `coreyhaines31/marketingskills`

Typical flow:

```text
Product context
→ Local business discovery
→ Clean / deduplicate
→ Qualify / categorize
→ Structured Persian output
→ Marketing preparation
→ Human review
→ Measure
→ Repeat only after pilot success
```

Relevant skills:
- `skills/local-business-data/SKILL.md`
- `skills/structured-data-output/SKILL.md`
- `skills/automated-marketing-growth/SKILL.md`

## Core principles

1. GitHub is the durable source of truth.
2. Important project state must not live only in chat history.
3. Read approved working preferences before substantial cross-project work.
4. Read before modifying an existing project.
5. Preserve scope and working behavior.
6. Preserve approved structure even when the project theme changes.
7. Verify changes with evidence.
8. Use specialized tools only when relevant.
9. Keep secrets out of Git.
10. Do not scale a workflow before its pilot is validated.
11. Real business/project/customer data outranks generic model assumptions.
