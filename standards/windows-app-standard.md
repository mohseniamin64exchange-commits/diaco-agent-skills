# Diaco Windows Application Standard

**Status:** ACTIVE  
**Version:** 0.1

Use together with `skills/windows-desktop-standard/SKILL.md`.

## Baseline

For Windows desktop applications:
- detect the actual framework/language before acting,
- do not force web architecture onto desktop software,
- separate application binaries from mutable user data where appropriate,
- avoid hard-coded machine-specific paths,
- preserve user data across ordinary updates,
- treat installer/update/rollback as product behavior,
- protect local databases during migrations,
- apply shared UI/print/backup standards when relevant,
- preserve keyboard/focus and high-DPI usability where applicable.

## Technology neutrality

This standard does not prescribe WinForms, WPF, WinUI, .NET, Electron, Python, Java, or another stack.

The repository decides the implementation technology. Diaco defines workflow and quality constraints around it.

## Project exceptions

A project's own `AGENTS.md` may define:
- supported Windows versions,
- architecture target,
- installer technology,
- storage paths,
- database engine,
- update strategy,
- printing engine,
- offline/online behavior.

These project rules take precedence over generic defaults.
