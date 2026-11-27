# Kore UI/UX Library

A free, reusable guide for making business web apps look and behave like polished, modern SaaS. Every project borrows from here. No paid libraries or services.

## What's inside

| Folder | What it's for |
|---|---|
| [**picker/**](picker/) | The visual picker. Choose a theme and up to 5 looks per element, then export a theme file. [Open the picker](https://claude.ai/artifact/WH9fmFbz11Ar16BT69qFiG) |
| [**glossary/**](glossary/) | Every UI element by name, in plain words: what it is, when to use it, when not to |
| [**rules/**](rules/) | Spacing, type, color, hierarchy, layout, motion, accessibility, as numbers you can follow |
| [**patterns/**](patterns/) | How screens behave: loading, page changes, empty and error states, forms, tables, dashboards |
| [**stack.md**](stack.md) | The free libraries to build on (Tailwind + shadcn/ui) and why |
| [**starter/**](starter/) | 5 stock theme files, setup steps, and the CLAUDE.md to drop into each project |
| [**sources.md**](sources.md) | Every source used. Pages cite several and flag where they disagree |

## How a project uses it

1. Pick your looks in the picker (or choose a stock theme).
2. Copy the theme file into the project.
3. Copy `starter/project-CLAUDE.md` into the project's CLAUDE.md.
4. Claude Code builds with shadcn/ui, styled by the theme file, following the rules and patterns.

If a project already has a design system, it wins; the library fills the gaps. See [starter/README.md](starter/README.md).
