# Motion

Animation should explain what changed, never decorate. Subtle and fast reads as quality; slow and bouncy reads as a template.

## Timing

| What | Duration | Easing |
|---|---|---|
| Hover, press, color change | 100–150ms | ease-out |
| Dropdowns, tooltips, popovers opening | 150–200ms | ease-out |
| Modals, drawers opening | 200–300ms | ease-out (enter), slightly faster on exit |
| Page transitions | 150–250ms, or none | ease-out |
| Skeleton shimmer | ~1.5s loop | linear |

Exits are faster than entrances. Nothing in an app should take longer than 300ms to animate. [Material "Motion" (easing and duration), Carbon "Motion" (productive vs expressive), Apple]

> **Sources disagree: how much motion?**
> Material encourages expressive motion and shared-element transitions. Carbon splits "productive" (quick, subtle) from "expressive" motion and recommends productive for work tools. GOV.UK uses almost none.
> **We follow:** Carbon's productive motion: short fades and slides that confirm a change. Business users repeat actions hundreds of times; a 400ms flourish becomes a delay.

## Rules

1. **Respect "reduce motion".** When the user's system asks for less motion, turn off slides, shimmer and parallax; keep simple fades. [WCAG 2.3.3, Apple, Material]
2. **Animate opacity and position (transform), not size or layout**: smoother on slow devices.
3. **Things enter from where they come from:** a drawer slides from its edge, a dropdown grows from its button.
4. **No animation on first page load** beyond a quick fade. Content should be readable immediately.
5. **Never block input** while something animates.
