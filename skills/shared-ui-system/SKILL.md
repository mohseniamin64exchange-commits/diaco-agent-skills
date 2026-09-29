---
name: shared-ui-system
description: Preserves a consistent reusable UI language across Diaco applications. Use when designing a new application, adding screens/components, or reusing navigation, forms, tables, dialogs, layout, typography, colors, and interaction patterns across projects.
---

# Shared UI System

## Goal

A new Diaco application should reuse an established information and interaction structure instead of inventing a new interface in every chat.

## Core distinction

**Structure and theme are separate layers.**

Preserve structure when it is approved:
- information order
- navigation placement
- field hierarchy
- table/form organization
- RTL/LTR behavior
- interaction flow

Allow theme variation:
- colors
- icons
- branding
- decorative styling
- shadows/radii where project-specific

A different theme is not a reason to redesign an approved structure.

## Before building UI

1. Read the Diaco UI Standard.
2. Read `standards/structured-data-presentation-standard.md` for data-heavy Persian screens.
3. Look for an approved project/reference implementation.
4. Inspect representative working screens/components.
5. Identify reusable tokens and reusable structures.
6. If the task involves polish, animation, prototyping, UI-library choice, or mobile-web behavior, load `ui-design-engineering`.

## Persian baseline

For Persian-first interfaces:
- use RTL by default,
- prefer right-side primary navigation/sidebar unless an approved project reference differs,
- keep repeated forms/tables in a consistent information order,
- center structured table values by default.

## Priority Design Engineering reference

`emilkowalski/skills` is Diaco's **Priority UI / Design Engineering Reference**.

Use it especially for:
- UI polish
- animation decisions and review
- isolated multi-variant prototyping
- component/library selection
- mobile-web interaction details
- React Native/Expo motion where relevant

It is **not** the authority for Diaco's visual identity or approved information structure.

## Additional UI reference

`adamtossell/ui-skills` may also be consulted for reusable design workflows and frontend practices.

## Precedence

1. approved project-specific UI/reference
2. ACTIVE Diaco structure/UI rules
3. Emil Kowalski Skills
4. UI Skills and other external design references

## Prototype rule

When the visual direction is undecided:
- explore outside production code,
- make variants genuinely different,
- preserve approved information structure unless the user explicitly asks to compare structural alternatives,
- let the user choose,
- integrate only the selected direction.

## Verification

- [ ] Existing shared patterns were inspected.
- [ ] Approved structure was preserved.
- [ ] Persian RTL/navigation/alignment rules were applied when relevant.
- [ ] New values/components were introduced only when needed.
- [ ] Loading/error/empty states are handled.
- [ ] Responsive and keyboard behavior were checked where applicable.
- [ ] External UI references did not silently override approved Diaco/project rules.
- [ ] Theme changes did not silently change information architecture.
