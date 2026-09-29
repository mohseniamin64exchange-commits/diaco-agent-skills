# Diaco UI Standard

**Status:** DRAFT  
**Version:** 0.3

## Goal

Build a reusable Diaco visual and interaction language so new applications do not invent UI conventions from scratch.

## Approved rules already in force

- Inspect an existing approved/reference UI before creating new patterns.
- Reuse shared tokens and components before adding variants.
- Keep navigation, forms, tables, dialogs, notifications, and states consistent where applicable.
- Project-specific branding may intentionally override shared defaults.
- Accessibility, keyboard behavior, focus, loading, empty, validation, and error states are part of UI quality.
- Do not infer colors, dimensions, typography, or layout details that have not yet been approved.
- When visual direction is genuinely undecided, exploration should happen in an isolated prototype rather than by repeatedly rewriting production UI.
- Meaningful alternatives should differ in layout, density, interaction model, hierarchy, or motion—not merely color.
- The user selects the visual direction. The Agent may explain tradeoffs but should not silently choose a universal Diaco style.
- Motion should have a functional purpose and must not make frequent workflows feel slower.
- Before adding a new UI library, inspect what the project already uses and avoid unnecessary dependency churn.
- **Structure is more persistent than theme:** preserve approved information order, hierarchy, direction, and workflow even when colors, icons, or branding change.
- For Persian-first data-heavy interfaces, RTL is the approved default.
- For Persian data tables, structured values are centered by default unless a field clearly benefits from another alignment.
- For Persian application shells, a right-side primary sidebar/navigation is the preferred baseline unless an approved project reference intentionally differs.
- Approved structured-data behavior is defined in `structured-data-presentation-standard.md`.

## External reference hierarchy

For UI/design work use this order:

1. approved project-specific UI/reference
2. ACTIVE Diaco UI rules
3. `emilkowalski/skills` — **Priority UI / Design Engineering Reference**
4. `adamtossell/ui-skills` — additional UI workflow reference
5. other external design references

External repositories provide specialist guidance; they do not define Diaco's visual identity.

See:
- `references/emil-kowalski-skills.md`
- `skills/ui-design-engineering/SKILL.md`
- `standards/structured-data-presentation-standard.md`

## Where Emil Kowalski Skills is especially useful

- UI polish and interaction details
- animation decision-making and implementation
- reviewing existing animations
- isolated multi-variant UI prototyping
- choosing UI/component libraries
- mobile-web interaction polish
- React Native/Expo motion when relevant

Exact animation constants, colors, typography, layout values, or library choices do **not** automatically become Diaco-wide defaults.

## To be defined from real reference implementations

The following are intentionally not yet fixed:
- primary/secondary colors
- typography/font family and size scale
- spacing scale
- border radius/shadow rules
- exact sidebar/header dimensions
- form field appearance
- button hierarchy
- table density and actions beyond the approved structured-data rules
- modal/dialog appearance
- toast/notification appearance
- fine-grained RTL exceptions and mixed-language handling
- Windows-specific controls and high-DPI rules
- approved Diaco motion tokens/durations/easing values

## Reference extraction workflow

When the user identifies a screen or project section as the desired reference:

1. inspect the actual implementation/screens,
2. record exact reusable choices,
3. separate product-specific content from reusable design rules,
4. separate **structure** from **theme**,
5. use specialist references to improve craft without changing approved identity,
6. add only approved reusable rules here,
7. mark visual rules ACTIVE only after approval.

Until then, do not claim a specific visual theme is the Diaco standard.
