# Color

## The roles

Professional apps use color by **role**, not by taste. Each theme in the picker fills these roles:

| Role | Token (shadcn name) | Use |
|---|---|---|
| Background | `--background` | The page |
| Surface | `--card`, `--popover` | Cards, menus, dialogs |
| Muted | `--muted`, `--secondary` | Subtle fills, hover rows, gray buttons |
| Border | `--border`, `--input` | Lines, field outlines |
| Text | `--foreground` | Main text |
| Muted text | `--muted-foreground` | Labels, hints, secondary info |
| Accent / primary | `--primary` | The main button, links, selected items, focus ring |
| Success / warning / danger / info | `--success` `--warning` `--destructive` `--info` | Status only |

[shadcn theming, Material "Color roles", Carbon "Color tokens", Atlassian "Color tokens"]

## Rules

1. **90% neutral.** Grays carry the interface. The accent appears in a few places per screen: the primary button, the active nav item, links, focus. If everything is blue, nothing is. [Polaris, Atlassian, NN/g "Color in UI"]
2. **Tint your grays.** Pure #808080 gray looks dead. Each theme's grays lean slightly toward its accent (cool for blue, green-ish for teal).
3. **Status colors are fixed and mean one thing.** Green = good/done, amber = attention, red = error/destructive, blue = info. Don't use red for decoration or your accent for warnings. [Carbon, Atlassian, Polaris, Material]
4. **Never color alone.** Pair color with text or an icon: "● Overdue", not just a red dot. About 1 in 12 men is color-blind. [WCAG 1.4.1]
5. **Contrast minimums** (WCAG AA): normal text **4.5:1**, large text (24px+, or 19px bold) **3:1**, borders of controls and icons **3:1**. Check with any free contrast checker (for example WebAIM's). [WCAG 1.4.3, 1.4.11]
6. **Muted text still passes 4.5:1.** The most common failure is light-gray text on white.
7. **Dark mode isn't inverted light mode.** Use dark grays (not pure black) for backgrounds, lighten the accent so it stays readable, and use borders more than shadows (shadows barely show on dark). All five picker themes ship both. [Material "Dark theme", Apple]
8. **Avoid AI-default palettes** unless a brand calls for them: purple-to-blue gradients, terracotta/cream, neon green on black.

> **Sources disagree: how many colors in a palette?**
> Material and Carbon publish 10–13 shades per color. shadcn and most small SaaS use a handful of role tokens.
> **We follow:** role tokens (above). They are what components actually need, and they make swapping themes a one-file change.

## Charts

Use the accent for the main series and grays for comparison. For several series, use a set built for charts (see [stack.md](../stack.md)) rather than inventing colors. Never red/green as the only difference between two series. [Carbon "Data visualization color", WCAG]
