# The stack: free libraries to build on

Everything here is free and open source (MIT, Apache or similar licenses that allow commercial client work). Checked November 2026.

## The pick

| Layer | Use | Why |
|---|---|---|
| Styling | **Tailwind CSS** | The standard for utility styling; every library below speaks it; our theme file plugs straight in |
| Components | **shadcn/ui** | Not a dependency: it copies the component code into your project, so you own and can restyle everything. Uses our exact token names. Huge community and AI tools know it well |
| Behavior under the components | **Base UI** (shadcn's default since July 2026) or **Radix** | Handles keyboard, focus and screen readers for menus, dialogs, popovers. Radix is still fully supported; keep it in existing projects |
| Icons | **Lucide** (default) or **Phosphor** / **Tabler** | One set per project. Lucide ships with shadcn |
| Toasts | **Sonner** | shadcn's toast component |
| Tables | **TanStack Table** | Sorting, filtering, pagination logic; shadcn's Data Table is built on it |
| Charts | **Recharts** via shadcn Charts, or **Tremor** for ready-made dashboard blocks | Both free; shadcn charts read our theme colors |
| Forms | **React Hook Form** + **Zod** | shadcn's form pattern; Zod rules can be reused on the server for validation |
| Command palette | **cmdk** (shadcn "Command") | Powers ⌘K menus |
| Dates | **date-fns** + shadcn Calendar | Small, free |
| Rich text | **Tiptap** (free core) or **Lexical** | Only when needed |
| Fonts | **Google Fonts** (Geist, Figtree, IBM Plex Sans, Manrope, Nunito Sans) | Free for commercial use |

Sources: [shadcn changelog, July 2026: Base UI default](https://ui.shadcn.com/docs/changelog/2026-07-base-ui-default), [shadcn docs](https://ui.shadcn.com), [Base UI](https://base-ui.com), [Radix](https://www.radix-ui.com).

## Why shadcn over the alternatives

| Library | Strengths | Why not the default for you |
|---|---|---|
| **Mantine** | 100+ components, great date pickers and hooks, free | Its own styling system; harder to make every project share one theme file with Tailwind |
| **MUI (Material UI)** | Most complete, strong data grid | Looks like Google out of the box; the advanced data grid features are paid (MUI X Pro) |
| **Ant Design** | Huge enterprise set, strong tables and forms | Very recognizable "Ant" look; heavier |
| **Chakra UI** | Pleasant, accessible | Smaller ecosystem than shadcn now |
| **HeroUI** (was NextUI) | Pretty defaults, Tailwind-based | Fewer business-data components |
| **React Aria** (Adobe) | Best-in-class accessibility, unstyled | More work to style; great if a client demands strict accessibility |
| **Tremor** | Dashboard charts and KPI blocks | Not a full component set; use it *alongside* shadcn |

> **Sources disagree:** comparison articles rank these differently every year. The consistent picture: shadcn is the most-used starting point for new React SaaS apps in 2025–26, Mantine and MUI win on out-of-the-box completeness, and React Aria wins on accessibility.
> **We follow:** shadcn, because you own the code, AI tools write it reliably, and one theme file restyles everything.

## Not on React?

The rules, patterns, glossary and theme file still apply. The CSS variables work with any framework. For Vue use **shadcn-vue**; for Svelte **shadcn-svelte**; for plain HTML, use the CSS variables directly.

## Paid things to avoid (or know you're avoiding)

Tailwind Plus (formerly Tailwind UI), MUI X Pro/Premium data grid, AG Grid Enterprise, Untitled UI Pro, Flowbite Pro, Figma paid kits. None are needed for this library.

> ⚠ **Risk to flag:** free component libraries are code you copy or install from the internet. Install only from the official package names above, keep them updated, and don't copy random "free component" snippets from unknown sites into client projects.
