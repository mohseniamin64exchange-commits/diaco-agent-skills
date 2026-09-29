---
name: ui-design-engineering
description: Routes Diaco UI work through approved project references, rapid prototyping tools, and specialist design-engineering guidance. Use for UI creation, UI polish, animation, design alternatives, screen-flow prototyping, component/library selection, mobile-web polish, or UI review.
---

# Diaco UI Design Engineering

## Goal

Produce polished interfaces without allowing an external tool or style guide to replace Diaco's approved information structure or visual identity.

## Required order

1. Read `standards/ui-standard.md`.
2. For Persian/data-heavy screens, read `standards/structured-data-presentation-standard.md`.
3. Inspect the project's existing UI, tokens, components, and approved references.
4. Read `00-AI-HUB/WORKING-PREFERENCES.md` when cross-project user preferences matter.
5. Determine whether the task needs:
   - direct implementation,
   - rapid prototype/screen-flow,
   - visual alternatives,
   - polish/review.
6. Use the appropriate specialist tool/reference.
7. Verify the result in the actual target platform.
8. Promote reusable approved decisions back into Diaco only when appropriate.

## Task routing

### New UI or redesign

Use the project's approved reference first.

If the user wants to see the design before coding, or multiple directions would reduce rework, use **M3E Canvas** as the priority rapid prototyping/screen-flow tool when Material 3-style visual prototyping is suitable.

Reference:
`references/m3e-canvas.md`

Recommended flow:
- preserve approved information structure,
- prototype screens and navigation,
- review with the user,
- select/finalize,
- convert to a prompt/spec,
- implement in the real codebase,
- verify the production result.

### Prototype workflow

Keep exploration isolated from production code.

When multiple variants are useful:
- make variants meaningfully different,
- preserve approved user structure unless structural alternatives are explicitly being compared,
- let the user choose,
- integrate only the selected direction.

M3E Canvas is preferred when a clickable/flow-oriented screen prototype is useful. A simpler static prototype may be better when the task does not benefit from screen linking or Material 3 components.

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

Apply design principles selectively, but use the actual Windows UI stack and `windows-desktop-standard` for implementation. M3E Canvas may help communicate rough layout ideas but is not a native Windows implementation reference.

## Reference/tool hierarchy

1. approved project-specific UI/reference
2. ACTIVE Diaco UI/structured-data rules and approved working preferences
3. M3E Canvas for rapid visual prototyping / screen-flow when relevant
4. `references/emil-kowalski-skills.md` for polish/design engineering
5. `adamtossell/ui-skills` and other external references

## Never

- silently replace the project's information structure
- let M3E Canvas defaults become Diaco identity
- copy an external product aesthetic as Diaco identity
- add motion only because it looks impressive
- add a new UI dependency without checking what already exists
- modify production UI during design exploration unless the user selected that direction
- treat a prototype as proof that production accessibility/responsiveness is correct
- treat web-specific CSS/React instructions as native Windows implementation rules

## Verification

- [ ] Approved project/Diaco UI rules were respected.
- [ ] User-approved RTL/navigation/table/form structure was preserved when relevant.
- [ ] M3E Canvas was used only when it added value.
- [ ] Prototype/spec was translated into the real target stack rather than treated as production output.
- [ ] Relevant specialist reference was used only where applicable.
- [ ] Accessibility and interaction states were considered.
- [ ] Prototype exploration did not contaminate production code before selection.
- [ ] The target platform was actually verified where practical.
- [ ] Reusable approved decisions were documented when they should become Diaco standards.
