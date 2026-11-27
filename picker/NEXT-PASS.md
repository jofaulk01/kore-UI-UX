# Picker: what to fix in the next pass

Feedback from Joseph after his first full pass (2026-11-27): **most options looked very similar and hard to choose between; the set reads like standard AI-generated UI.** He's testing his picks in a real project first. Redo the picker after that, using what the test shows.

## Why the options feel samey (diagnosis)

1. **Every tile shares the same tokens.** Within a section, all 5 options use the same neutrals, font, accent and radius, so the only difference is a border vs a shadow or a 2px line. At thumbnail size those differences vanish.
2. **The 5 themes are one theme with different accents.** All are light-gray-plus-one-color, sans-serif, white cards. Real design directions differ in temperature, contrast, type personality and texture, not just hue.
3. **The vocabulary is the AI default.** Rounded white cards, soft tinted badges, lucide-style icons, tinted active nav items, gray skeletons: this is what shadcn starters and AI tools produce out of the box. See the `impeccable-tells` and `anti-ai-design` skills.
4. **Tiles are too small to judge a look.** Picking a button style in isolation doesn't show its effect on a whole screen.

## Plan for the redo

- **Make themes genuinely different directions** (for example: dense editorial with a serif display face; high-contrast monochrome with a single loud accent used sparingly; warm paper-toned neutrals; dark-first technical; colorful but structured). Each changes type pairing, neutral temperature, border weight, shadow use and density together.
- **Fewer, bolder element options.** Drop options that differ by one property. Keep 3 when 5 would be filler.
- **Judge in context.** Clicking an option should flash the change in the full app preview; consider showing options as whole-screen thumbnails for the big decisions (theme, sidebar, table, cards).
- **Swap AI tells for specific alternatives** (per `impeccable-tells`): no default icon-in-tinted-tile, no rounded-2xl by reflex, no generic soft badges everywhere; borrow conventions from the subject (ledgers, receipts, dashboards in finance tools).
- **Keep the small-element standards fixed** (Joseph wants consistency there).

## Joseph's first picks (for reference)

Base theme Friendly with overrides: raised buttons, glow-focus inputs, accent-hover menus, tag badges, soft alerts, pulse loading, thick progress bars, light tooltips, comfortable density. Theme file: [`starter/joseph-theme.css`](../starter/joseph-theme.css).

⚠ One pick to watch in the test: **drawer = bottom sheet** is a phone pattern. On desktop, record panels usually slide from the right. Fine to keep for phones; check how it feels on a laptop.
