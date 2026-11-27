# Spacing

Spacing is the biggest single difference between amateur and professional UI. Amateurs use random gaps (13px here, 20px there). Professionals pick from a short scale.

## The scale

| Token | px | Typical use |
|---|---|---|
| 1 | 4 | Icon to its label, tiny gaps |
| 2 | 8 | Between buttons, inside compact controls |
| 3 | 12 | Label to its field, inside table cells |
| 4 | 16 | Padding inside cards (compact), between form fields |
| 6 | 24 | Padding inside cards (comfortable), between related sections |
| 8 | 32 | Between unrelated sections |
| 12 | 48 | Between major page areas |
| 16 | 64 | Marketing page sections |

These match Tailwind's default spacing units (1 unit = 4px), so `gap-4` = 16px. [Tailwind, Polaris, Atlassian, Primer]

> **Sources disagree: 4px or 8px base?**
> Material and Carbon describe an 8px grid. Polaris, Atlassian, Primer and Tailwind use 4px steps.
> **We follow:** 4px steps, but prefer the multiples of 8 (8, 16, 24, 32) for layout. 4 and 12 are for small details inside components. In practice both camps end up with the same values.

## Rules

1. **Proximity groups things.** A label sits 4–8px from its field but 16–24px from the next field. If everything has the same gap, nothing looks grouped. [Laws of UX "Law of proximity", NN/g "Gestalt principles"]
2. **Inside is smaller than outside.** Gaps inside a card are smaller than the card's padding, and the space between sections is bigger than both. [Material "Layout", Polaris "Spacing"]
3. **Start with too much space, then remove.** Cramped looks cheap; generous looks confident. Business tools can be denser, but denser by choice, using the Compact density.
4. **Use `gap` on rows and columns, not margins on each item.** Fewer surprises.
5. **Same thing, same spacing, everywhere.** All cards have the same padding; all page headers sit the same distance from the content.

## Density

The picker offers three densities. They change control height and padding, not the scale itself.

| Density | Control height | Card padding | Table row padding | Use for |
|---|---|---|---|---|
| Compact | 30–32px | 14–16px | 6px | Data-heavy tools used all day |
| Comfortable | 36px | 18–24px | 10px | Default |
| Spacious | 40–44px | 24px | 14px | Occasional users, touch screens |

[Carbon "Spacing", Atlassian "Spacing", Material "Density"]

## Touch targets

Anything clickable is at least **24×24px** (WCAG 2.2 minimum) and ideally **44×44px** on phones (Apple). A small icon can stay small if its clickable area is padded out. [WCAG 2.5.8, Apple HIG, Material (48dp)]
