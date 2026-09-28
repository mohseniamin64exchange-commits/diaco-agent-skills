# Emil Kowalski Skills — Diaco Reference

## Source

Repository: `emilkowalski/skills`  
URL: https://github.com/emilkowalski/skills  
Owner: Emil Kowalski  
Default branch: `main`  
License: MIT  
Observed README blob: `fedfecf4f14fc03dc22185c0009a594dc4fa618a`  
Observed indexed snapshot: `d16ebe60d09a5ba2afcb7054ede9d0a10c9f6128`

## Diaco role

**Priority UI / Design Engineering Reference**

Use this repository as a specialist reference for:
- UI polish and interaction quality
- deciding whether motion is appropriate
- implementing and reviewing animation
- isolated UI prototyping with multiple meaningful variants
- choosing appropriate UI libraries instead of unnecessary hand-rolled components
- making web UI feel more native on mobile
- React Native / Expo motion when the project actually uses that stack

## High-value skills observed

- `emil-design-eng`
- `animate`
- `animate-expo`
- `review-animations`
- `improve-animations`
- `find-animation-opportunities`
- `animation-vocabulary`
- `apple-design`
- `write-swift`
- `pick-ui-library`
- `prototype`
- `mobile-native`
- `ask-sonner`

## Diaco adoption policy

This repository is **not** the source of truth for Diaco visual identity.

Precedence:
1. approved project-specific UI/reference
2. ACTIVE Diaco UI rules
3. Emil Kowalski Skills as specialist design-engineering guidance
4. other external UI references

Do not copy arbitrary colors, typography, layout, or product-specific aesthetics into Diaco merely because an external skill recommends them.

## Prototype policy

When the user has not yet approved a visual direction and comparison would materially help:
- build alternatives in an isolated prototype surface,
- keep production code unchanged during exploration,
- make variants meaningfully different rather than cosmetic recolors,
- let the user select the direction,
- only then promote the chosen variant into production.

The user's selection remains authoritative.

## Motion policy

Use Emil's motion guidance as specialist input, especially for:
- frequency of interaction,
- purpose of motion,
- perceived responsiveness,
- interruption behavior,
- reduced-motion handling,
- avoiding animation that makes frequent workflows slower.

Do not automatically import exact durations, easing values, or implementation libraries as universal Diaco constants. Promote those only when approved in our own UI standard/design system.

## Platform scope

### Web
Highly applicable.

### Mobile web / PWA
Highly applicable, especially touch, viewport, safe-area, and mobile interaction details.

### React Native / Expo
Applicable when the project uses that stack.

### Native Windows desktop
Use the interaction/design principles selectively. Web/CSS/React-specific implementation details are not directly authoritative for WinForms, WPF, WinUI, or other native desktop stacks.

## Review rule

When an external recommendation conflicts with a proven working project pattern, inspect the reason before changing the project. Avoid dependency churn and architecture changes that are unrelated to the user's goal.
