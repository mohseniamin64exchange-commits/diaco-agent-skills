---
name: shared-ui-system
description: Preserves a consistent reusable UI language across Diaco applications. Use when designing a new application, adding screens/components, or reusing navigation, forms, tables, dialogs, layout, typography, colors, and interaction patterns across projects.
---

# Shared UI System

## Goal

A new Diaco application should reuse an established visual and interaction language instead of inventing a new interface in every chat.

## Before building UI

1. Look for an existing project design system or shared UI repository.
2. Inspect representative working screens/components.
3. Identify reusable tokens:
   - colors
   - typography
   - spacing
   - radii
   - borders/shadows
   - breakpoints
4. Identify reusable structures:
   - app shell
   - sidebar/navigation
   - header
   - forms
   - tables
   - cards
   - dialogs
   - notifications
   - empty/error/loading states

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
- [ ] Intentional deviations are documented.
