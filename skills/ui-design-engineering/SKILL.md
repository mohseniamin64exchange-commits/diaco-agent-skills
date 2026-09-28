---
name: ui-design-engineering
description: Routes Diaco UI work through approved project references and specialist design-engineering guidance. Use for UI creation, UI polish, animation, design alternatives, component/library selection, mobile-web polish, or UI review.
---

# Diaco UI Design Engineering

## Goal

Produce polished interfaces without allowing an external style guide to replace Diaco's approved visual identity.

## Required order

1. Read `standards/ui-standard.md`.
2. Inspect the project's existing UI, tokens, components, and approved references.
3. Determine the task type.
4. Use the appropriate specialist reference/workflow.
5. Verify the result in the actual target platform.
6. Promote reusable approved decisions back into Diaco only when appropriate.

## Task routing

### New UI or redesign
Use the project's approved reference first.

If the visual direction is not yet approved and multiple directions would help, use the **prototype workflow**:
- isolate the exploration from production code,
- create genuinely different variants,
- present tradeoffs neutrally,
- let the user choose,
- integrate only the selected variant.

### Animation / motion
Consult `emilkowalski/skills` as the priority specialist reference.

Before adding motion:
- decide whether the interaction should animate at all,
- identify the purpose,
- preserve responsiveness,
- respect reduced-motion/accessibility,
- avoid unnecessary motion on high-frequency actions.

### UI review / polish
Use Emil's design-engineering and animation-review guidance to find concrete interaction/polish issues.

Do not manufacture findings merely to make a review look comprehensive.

### UI library / component choice
Inspect the project's existing dependencies first.

Prefer reusing a suitable existing library/component system over adding a competing dependency or hand-rolling complex accessibility-sensitive primitives.

### Mobile web / PWA
Use specialist mobile-native web guidance where relevant, but verify on real hardware when the issue depends on touch, browser chrome, viewport, safe areas, or mobile keyboard behavior.

### Native Windows
Apply design principles selectively, but use the actual Windows UI stack and `windows-desktop-standard` for implementation.

## Reference hierarchy

1. approved project-specific UI/reference
2. ACTIVE Diaco UI Standard
3. `references/emil-kowalski-skills.md`
4. `adamtossell/ui-skills` and other external references

## Never

- silently replace the project's visual language
- copy an external product aesthetic as Diaco identity
- add motion only because it looks impressive
- add a new UI dependency without checking what already exists
- modify production UI during design exploration unless the user selected that direction
- treat web-specific CSS/React instructions as native Windows implementation rules

## Verification

- [ ] Approved project/Diaco UI rules were respected.
- [ ] Relevant specialist reference was used only where applicable.
- [ ] Accessibility and interaction states were considered.
- [ ] Prototype exploration did not contaminate production code before selection.
- [ ] The target platform was actually verified where practical.
- [ ] Reusable approved decisions were documented when they should become Diaco standards.
