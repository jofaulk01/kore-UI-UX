# Starter: putting the library into a project

## New project

1. Set up Next.js (or Vite) + Tailwind + shadcn/ui (`npx shadcn@latest init`).
2. Copy your theme file in:
   - Your own picks: open the [picker](https://claude.ai/artifact/WH9fmFbz11Ar16BT69qFiG), click **Get theme file**, save as `app/kore-theme.css`.
   - Joseph's saved picks (Nov 2026): [`joseph-theme.css`](joseph-theme.css).
   - Or a stock theme: copy one of [`themes/`](themes/) (crisp, soft, dense, ink, friendly).
3. Import it after Tailwind in your main CSS file, and replace shadcn's default color variables (the theme file uses the same names).
4. Load the theme's font from Google Fonts.
5. Copy [`project-CLAUDE.md`](project-CLAUDE.md) into the project's `CLAUDE.md` so Claude Code follows the library.

## Existing project that already has a design system

Don't replace it. Claude Code should:

1. **Find what exists:** a tokens or theme file, Tailwind config colors, a component folder, a brand guide.
2. **Map, don't overwrite:** match their colors, font and radius to our token names (their brand blue becomes `--primary`, and so on). Keep their values.
3. **Fill the gaps only:** where they have no rule (empty states, loading, toasts, table behavior), use this library's rules and the closest picker option.
4. **Note the mapping** in the project's CLAUDE.md so later sessions stay consistent.

Order of authority: the client's brand and existing system → your saved picks → this library's defaults.

## Existing project with no design system

Treat it like a new project: pick a theme, add the theme file, then restyle screen by screen, starting with the app shell (sidebar, top bar, page header), then tables and forms.
