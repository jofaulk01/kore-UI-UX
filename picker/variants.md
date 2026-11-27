# What each picker option means (for building)

The picker saves picks like `"button": "pill"`. This page tells Claude Code how to build each one with shadcn/ui + Tailwind. Token names refer to the theme file.

The live picker: https://claude.ai/artifact/WH9fmFbz11Ar16BT69qFiG (source: [index.html](index.html)).

## Theme-level

| Key | Options | Build |
|---|---|---|
| theme | crisp, soft, dense, ink, friendly | Copy `starter/themes/<theme>.css` (or the generated `kore-theme.css`) |
| accent | blue, teal, violet, graphite, rose | Sets `--primary` and `--ring` |
| font | geist, figtree, plex, manrope, nunito | Sets `--font-sans`; load from Google Fonts |
| radius | sharp 2, slight 4, medium 6, round 10, xround 14 (px) | Sets `--radius`; cards use radius × 1.4 |
| density | compact, comfortable, spacious | `--control-height` 30/36/40px, card padding 14/18/22px, table cell vertical padding 6/10/13px |

## Elements

| Key | Option → how to build |
|---|---|
| **button** | `solid`: default shadcn button. `pill`: `rounded-full`. `square`: `rounded-none`, text left-aligned with extra right padding. `soft`: secondary variant uses primary at 12% opacity as background and primary as text. `raised`: subtle `shadow-sm` + inner top highlight |
| **input** | `outlined`: default. `filled`: muted background, no border except a bottom line, top corners rounded only. `underline`: transparent, bottom border only, no radius. `ring`: default + 3px soft primary glow on focus. `inset`: muted background with inner shadow |
| **menu** | `inset`: default shadcn dropdown (rounded hover inside padding). `flush`: no inner padding, hover spans full width, square items. `dark`: always dark surface regardless of theme. `accent`: hovered item gets primary background. `roomy`: larger items with a second line of muted description |
| **sidebar** | `light`: surface background, active item primary-tinted. `dark`: near-black sidebar in both themes. `tinted`: background = primary mixed 7% into page background; active item is a white raised pill. `rail`: icons only, 56px, tooltips on hover. `floating`: sidebar is an inset card with margin and shadow; active item solid primary |
| **topbar** | `plain`: surface bar with bottom border. `center`: search centered and wider. `blend`: no background or border. `dark`: dark bar with logo. `nav`: no sidebar; logo + main links in the bar |
| **pageheader** | `simple`: title + actions. `crumbs`: breadcrumbs above title. `desc`: one-line description under title. `tabs`: tabs directly under title. `back`: back arrow + title + status badge (detail pages) |
| **card** | `outline`: border, no shadow. `shadow`: no border, soft two-layer shadow (border in dark mode). `filled`: muted background, no border. `header`: title in a muted band with a divider. `open`: no box, top border only |
| **tabs** | `underline`: 2px primary line under active. `segmented`: muted track, active is a raised surface pill. `enclosed`: folder tabs joined to content. `soft`: active gets primary-tinted background. `text`: active is bold and dark, no indicator |
| **kpi** | `simple`: label, big value, change chip + comparison text. `spark`: + sparkline under. `goal`: + progress bar toward target. `strip`: all KPIs in one bordered strip split by vertical lines. `bars`: value left, mini bar chart right |
| **table** | `lines`: horizontal dividers. `zebra`: alternate rows muted, no dividers. `boxed`: every cell bordered, muted header. `compact`: smaller padding and font. `rows`: each row is a separate rounded bordered card |
| **badge** | `soft`: status color at 14% background, colored text, pill. `solid`: full status color. `outline`: colored border. `dot`: colored dot + normal text. `tag`: small uppercase square label |
| **chart** | `line`: 2px line, last point marked. `dotted`: every point marked. `area`: line with gradient fill. `bars`: square bars, last highlighted. `rounded`: rounded bars |
| **avatar** | `soft`: tinted circle with initials. `solid`: full color circle. `square`: rounded square (companies). `neutral`: gray. `status`: soft + green presence dot |
| **pagination** | `plain`: numbers, current filled. `boxed`: each number boxed. `text`: current underlined. `info`: "1–25 of 312" + arrows only |
| **toast** | `dark`: inverted. `light`: surface card + colored icon. `edge`: 3px status color on left. `filled`: solid status color. `pill`: small round, bottom center. Use Sonner; position bottom-right except `pill` |
| **alert** | `soft`, `outline`, `edge`, `filled`, `plain` (same logic as toasts) |
| **loading** | `shimmer`: skeleton with moving shine. `pulse`: skeleton fading. `spinner`: centered spinner + text. `bar`: thin top progress bar, old content dimmed. `dots`: three bouncing dots |
| **empty** | `centered`: icon, title, line, button. `framed`: same in dashed border. `inline`: one-line text + link. `ghostrows`: faded fake rows behind a centered message. `checklist`: setup steps with progress |
| **modal** | `standard`: title, text, buttons right. `icon`: centered with icon. `footer`: buttons in a muted footer band. `titled`: title bar divided by a line. `stacked`: full-width stacked buttons |
| **drawer** | `overlay`: slides over, page dimmed. `floating`: inset with gap and radius. `push`: page shrinks beside it. `modal`: over with darker scrim. `bottom`: bottom sheet |
| **tooltip** | `dark` (default) or `light` |
| **crumbs** | `chevron` (default) or `slash` |
| **progress** | `thin` 4px or `thick` 10px |

## Fixed standards (no choice)

Checkbox 16px, radius up to 4px, primary when checked. Radio 16px circle. Switch 34×20 track, 16px knob, instant effect only. Slider 4px track, 16px handle, always show the value. Spinner primary ring, 0.8s. Focus ring 2px primary, 2px offset, never removed. Divider 1px border color. Keyboard keys in mono font.
