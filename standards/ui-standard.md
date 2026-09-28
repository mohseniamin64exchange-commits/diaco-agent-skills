# Diaco UI Standard

**Status:** DRAFT  
**Version:** 0.1

## Goal

Build a reusable Diaco visual and interaction language so new applications do not invent UI conventions from scratch.

## Approved rules already in force

- Inspect an existing approved/reference UI before creating new patterns.
- Reuse shared tokens and components before adding variants.
- Keep navigation, forms, tables, dialogs, notifications, and states consistent where applicable.
- Project-specific branding may intentionally override shared defaults.
- Accessibility, keyboard behavior, focus, loading, empty, validation, and error states are part of UI quality.
- Do not infer colors, dimensions, typography, or layout details that have not yet been approved.

## To be defined from real reference implementations

The following are intentionally not yet fixed:
- primary/secondary colors
- typography/font family and size scale
- spacing scale
- border radius/shadow rules
- sidebar/header dimensions
- form field appearance
- button hierarchy
- table density and actions
- modal/dialog appearance
- toast/notification appearance
- RTL/LTR behavior details
- Windows-specific controls and high-DPI rules

## Reference extraction workflow

When the user identifies a screen or project section as the desired reference:

1. inspect the actual implementation/screens,
2. record exact reusable choices,
3. separate product-specific content from reusable design rules,
4. add the reusable rules here,
5. only mark them ACTIVE after approval.

Until then, do not claim a specific visual style is the Diaco standard.
