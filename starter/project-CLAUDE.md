# UI rules for this project (from Kore UI/UX library)

This project follows the Kore UI/UX library: https://github.com/jofaulk01/kore-UI-UX

## Before building any UI

1. Read the theme file (`kore-theme.css`) and the element picks listed at its bottom. Build each element the way `picker/variants.md` in the library describes for that pick.
2. If this project already has its own design system or brand, it wins. Map it onto the library's token names; use the library only to fill gaps.
3. Stack: Tailwind + shadcn/ui (Base UI or Radix underneath, whichever the project already uses), Lucide icons, Sonner toasts, TanStack Table, Recharts via shadcn charts, React Hook Form + Zod.

## Always

- Spacing only from the 4px scale (4, 8, 12, 16, 24, 32, 48, 64).
- One font; 14px body in the app; sizes from the type scale in `rules/typography.md`.
- Colors only from theme tokens. No raw hex values in components.
- One primary button per area; verb labels ("Send invoice").
- Every screen has loading, empty and error states (`patterns/`).
- Toasts only for confirmations; errors go in alerts or next to fields.
- Labels above inputs, never placeholder-only; validate on blur and submit.
- Numbers right-aligned with tabular figures; status badges always include text.
- Keyboard works everywhere; focus ring is never removed; contrast meets WCAG AA.
- Motion 150–250ms, ease-out, off when "reduce motion" is set.

## Project-specific notes

<!-- Record here: theme used, any overrides, how an existing design system was mapped. -->
