---
name: windows-desktop-standard
description: Platform profile for Diaco Windows desktop applications. Use when creating, modifying, packaging, updating, printing from, backing up, restoring, or maintaining a Windows desktop application.
---

# Windows Desktop Standard

## Goal

Keep Diaco's shared engineering rules platform-independent while applying Windows-specific conventions only to Windows desktop applications.

## Rule layers

Apply rules in this order:

1. Diaco core operating rules
2. Relevant shared standards such as UI, safe changes, project memory, print, and backup
3. This Windows Desktop platform profile
4. Project-specific `AGENTS.md`
5. Current repository implementation and constraints

Project-specific rules may intentionally override generic defaults.

## Detect before acting

Before changing a Windows application, inspect the repository and identify:
- framework and language
- application architecture
- UI technology
- supported Windows versions and architecture targets
- local vs remote data storage
- installer/deployment method
- update mechanism
- printing behavior
- backup/restore behavior

Do not assume a specific Windows stack when the repository shows otherwise.

## Windows-specific concerns

### Application files and user data
- Keep installed application binaries separate from mutable user data.
- Do not hard-code machine-specific absolute paths.
- Use appropriate Windows user/application data locations when the existing project supports them.
- Preserve backward compatibility with existing user data unless a migration is explicitly designed and verified.

### Installer and updates
- Treat installation, upgrade, uninstall, and rollback as part of product behavior.
- Do not silently change installer technology or deployment strategy.
- Preserve user data across ordinary upgrades.
- Record breaking migration requirements explicitly.

### Database and local storage
- Back up data before destructive schema/data migrations when applicable.
- Make migrations reversible where practical.
- Never replace or reset a user's production/local database merely to simplify development.

### Printing
- Reuse the Diaco print standard when one is defined for the project or shared system.
- Preserve printer selection, page size, margins, orientation, scaling, header/footer, RTL/LTR behavior, and preview conventions as applicable.
- Separate printable document layout from ordinary screen layout when needed.

### Backup and restore
- Reuse the Diaco backup/restore standard when available.
- Define exactly what is included in a backup, its format, naming, destination, version compatibility, validation, and restore process.
- A backup feature is incomplete until restore has been verified on representative data.

### Windows UX
- Follow the shared Diaco UI language unless the project intentionally defines another design system.
- Preserve expected keyboard navigation, focus behavior, dialogs, validation, loading states, and high-DPI/resolution behavior where applicable.

## Safety rules

- Do not convert a desktop project to a web architecture unless explicitly requested.
- Do not introduce a web/Supabase requirement into an offline/local Windows application by default.
- Do not apply `supabase-webapp-guardrails` unless the project actually uses Supabase or the task introduces it intentionally.
- Avoid unrelated framework, runtime, installer, or database upgrades.
- Preserve existing working print, backup, installer, and update flows unless they are in scope.

## Verification checklist

Where applicable, verify:
- [ ] clean build
- [ ] application starts normally
- [ ] changed user flow works
- [ ] existing local data opens correctly
- [ ] migrations do not destroy data
- [ ] print preview/output matches the required standard
- [ ] backup can be created
- [ ] backup can actually be restored
- [ ] installer/update path remains valid
- [ ] keyboard/focus and common screen-size behavior remain usable
- [ ] handoff records important Windows-specific constraints
