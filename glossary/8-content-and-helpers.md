# 8. Content and behind-the-scenes helpers

Less visible pieces. Mostly on marketing pages or inside other elements.

### Heading
Titles of pages and sections (H1 for the page title, H2 for sections, H3 inside). One H1 per page. Sizes in [rules/typography.md](../rules/typography.md). [Gallery, GOV.UK]

### Icon
Small symbols. Use one free icon set for the whole app (see [stack.md](../stack.md)), at one or two sizes, in one stroke weight. Icons support labels; they rarely replace them. [NN/g "Icon usability", Material, Carbon]

### Image, video
Media. Always reserve their space so the page doesn't jump when they load, and add alt text for images.

### Hero
**Also called:** jumbotron, banner.
The big top section of a marketing page: headline, subline, main button, image. Not used inside apps.

### Quote, testimonial
Marketing pages only.

### Carousel
**Also called:** content slider.
Slides that rotate. Research says most people only see the first slide. **Avoid**, or use only for image galleries people control. [NN/g "Auto-forwarding carousels", GOV.UK]

### Stack
An invisible layout helper that puts items in a row or column with equal gaps. Not something users see, but you'll hear the word. [Gallery, Primer]

### Scroll area
A box with its own scrollbar inside the page (a long list inside a card). [shadcn]

### Resizable panels
**Also called:** split pane.
Two panels with a draggable divider between them. [shadcn, Fluent]

### Aspect ratio box
Keeps an image or video at a fixed shape (16:9). [shadcn]

### Visually hidden
**Also called:** screen-reader only, sr-only.
Text hidden from the eye but read aloud by screen readers, e.g. the label of an icon button. [Gallery, WCAG]

### Skip link
See [2-navigation.md](2-navigation.md#skip-link).

### Footer
Bottom of marketing pages: links, legal, social. Rare inside apps.

---

## Coverage check

This glossary was cross-checked against the full component lists of component.gallery (60 elements tracked across 90+ design systems) and shadcn/ui, plus dashboard pieces those lists skip (stat cards, charts, filters, activity feeds, notification center, onboarding checklist, kanban, calendar view). If you see a name that isn't here, add it to the right section.
