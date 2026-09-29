# M3E Canvas

## Source

- Repository: https://github.com/lnkiai/m3e-canvas
- Owner: `lnkiai`
- Default branch: `main`
- License: MIT
- Observed upstream commit: `de2d97a577b2b77f33428db11c658e3548335b5e` (2026-09-27)
- Stack observed: Next.js 16, React 19, TypeScript, Tailwind CSS 4, Motion
- Deployment model: static export; no application backend required
- Persistence: browser `localStorage`

## Diaco role

**Priority UI Prototyping / Screen-Flow Tool**

M3E Canvas is used to quickly sketch screens before production implementation, connect screens into flows, preview interactions, explore Material 3 Expressive layouts, and convert the prototype into a concise prompt for a coding Agent.

It is a prototyping and handoff tool, **not the authority for Diaco's final visual identity**.

## Useful capabilities

- drag-and-drop UI parts
- phone and desktop canvases
- multi-screen flows
- tap/swipe navigation
- preview of screen transitions
- layers and groups
- theme controls
- prompt generation for AI coding tools
- PNG export
- share links / AI draft workflow
- static local/browser-first operation

## Target workflow

Preferred Diaco flow:

```text
Approved Diaco/project structure
→ M3E Canvas prototype
→ user review/selection
→ exported prompt/spec
→ coding Agent implementation
→ browser/device verification
→ project handoff
```

## Diaco precedence

When using M3E Canvas:

1. approved project-specific structure/reference
2. ACTIVE Diaco structure and presentation rules
3. approved user working preferences
4. M3E Canvas for rapid visual prototyping and screen-flow exploration
5. external UI design references for polish
6. final production implementation in the project's actual stack

Do not let the tool replace an already approved project structure merely because its default Material 3 Expressive style differs.

## Important user-approved defaults

For Persian-first Diaco applications, preserve these when relevant:

- RTL reading direction
- right-side primary navigation/sidebar baseline
- consistent information order
- centered structured table values by default
- stable form/table hierarchy
- project-specific colors/icons/branding may vary without changing approved structure

## Limitations / caveats

- M3E Canvas is Material 3 Expressive-oriented; it is not a universal final UI system.
- Its README currently lists prompt output languages as Japanese, English, Chinese, and Korean. Do not claim native Persian prompt generation unless verified in the current upstream.
- Native Windows/desktop-heavy product behavior still needs the real project stack and Windows-specific Diaco profile.
- A prototype is not proof that the production UI is responsive, accessible, keyboard-correct, or functionally complete.
- The optional AI helper uses user-provided API keys in the browser and sends requests directly to the selected provider according to upstream documentation; do not store such keys in Git.

## Installation policy

Do not install or copy M3E Canvas into every project.

Use one of these approaches:
- public/live upstream for quick exploration when suitable,
- a local clone for repeatable/private prototyping,
- a separately maintained Diaco customization only if the user later approves one.

Any customized copy must preserve MIT attribution and be clearly distinguished from upstream.
