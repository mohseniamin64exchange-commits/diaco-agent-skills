---
name: document-r-automation
description: Safely automates Word/report formatting and document transformations with R or similar scripts. Use when building or modifying formatters that must preserve scientific content, equations, tables, figures, captions, styles, or university/report templates.
---

# Document and R Automation

## Prime directive

Formatting automation must not silently damage or rewrite the document's substantive content.

## Before transformation

1. Work from a copy unless the user explicitly requests in-place replacement.
2. Identify the authoritative template/reference document.
3. Define what may change:
   - styles
   - numbering
   - spacing/layout
   - captions
   - permitted equation conversion
4. Define what must remain unchanged:
   - scientific text
   - tables/data
   - figures
   - references unless explicitly requested
   - equations that cannot be safely converted

## Failure-tolerant processing

For difficult elements:
- isolate processing per element
- do not let one unsupported equation stop the entire document
- skip safely when conversion is uncertain
- mark/log skipped items for review
- continue processing the remainder

Never "fix" an unreadable formula by guessing its intended mathematics.

## Template fidelity

When a template is authoritative:
- reuse its actual styles/numbering definitions when technically feasible
- do not approximate critical style definitions merely by visual similarity
- separate content import from style/numbering import

## Verification

After processing:
- confirm the output opens successfully
- compare structural counts where useful (headings/tables/figures/equations)
- inspect representative pages/elements
- report skipped/failed transformations
- preserve a recoverable original

## Verification checklist

- [ ] Original content is preserved.
- [ ] Output document opens.
- [ ] Required formatting rules are applied.
- [ ] Unsupported elements were skipped rather than corrupted.
- [ ] Skipped/failed elements are reported.
