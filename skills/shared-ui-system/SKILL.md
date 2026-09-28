---
name: shared-ui-system
description: Preserves a consistent reusable UI language across Diaco applications. Use when designing a new application, adding screens/components, or reusing navigation, forms, tables, dialogs, layout, typography, colors, and interaction patterns across projects.
---

# Shared UI System

## Goal

A new Diaco application should reuse an established visual and interaction language instead of inventing a new interface in every chat.

## Before building UI

1. Read the Diaco UI Standard.
2. Look for an approved project/reference implementation.
3. Inspect representative working screens/components.
4. Identify reusable tokens:
   - colors
   - typography
   - spacing
   - radii
   - borders/shadows
   - breakpoints
5. Identify reusable structures:
   - app shell
   - sidebar/navigation
   - header
   - forms
   - tables
   - cards
   - dialogs
   - notifications
   - empty/error/loading states

## UI Skills reference

`adamtossell/ui-skills` may be consulted for reusable design workflows, reference-capture techniques, prompting patterns, interaction ideas, and frontend practices.

It is **not** the authority for Diaco's visual identity.

Precedence:
1. approved project-specific UI/reference
2. ACTIVE Diaco UI rules
3. UI Skills or other external design references

Do not import an external style as a Diaco-wide standard without explicit approval.

## Rules

- Reuse tokens and components before introducing new variants.
- Do not redesign stable shared navigation without explicit need.
- Keep responsive behavior consistent.
- Use semantic design tokens instead of scattered raw values.
- Accessibility and keyboard behavior are part of component quality.
- Product-specific branding may override shared defaults intentionally.

## Design contract

For a new screen, record:
- screen purpose
- primary action
- reused components
- required states
- responsive behavior
- intentional deviations from the shared system

## Verification

- [ ] Existing shared patterns were inspected.
- [ ] New values/components were introduced only when needed.
- [ ] Loading/error/empty states are handled.
- [ ] Responsive and keyboard behavior were checked where applicable.
- [ ] External UI references did not silently override approved Diaco/project rules.
- [ ] Intentional deviations are documented.
