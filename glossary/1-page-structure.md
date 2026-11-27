# 1. Page structure

The large pieces almost every SaaS screen is made of. Picture a typical admin app: a dark or light strip down the left (sidebar), a thin bar across the top (header), and a content area with a title row (page header) and boxes (cards).

```
┌──────────┬──────────────────────────────────────────┐
│          │ Header: search · notifications · avatar  │
│ Sidebar  ├──────────────────────────────────────────┤
│          │ Breadcrumbs                              │
│ Logo     │ Page title            [Secondary][Primary]│
│ Nav      ├──────────────────────────────────────────┤
│ items    │ ┌──────┐ ┌──────┐ ┌──────┐               │
│          │ │ Card │ │ Card │ │ Card │               │
│          │ └──────┘ └──────┘ └──────┘               │
│ Settings │ ┌──────────────────────────┐             │
│ Account  │ │ Table                    │             │
└──────────┴──────────────────────────────────────────┘
```

---

### App shell
**Also called:** layout, frame, chrome.
The fixed outer frame (sidebar + header) that stays put while the content inside changes. **Use:** every logged-in app. **Rule:** it must never jump or reload when you change pages; only the content area changes. [Carbon, Polaris, Atlassian]

### Sidebar
**Also called:** side nav, navigation rail (collapsed, icons only), left nav.
Vertical list of the app's main sections. **Use:** apps with 5+ sections, which is most business tools. **Don't use:** apps with 2–4 sections; a top nav is enough. Can collapse to icons only to save space. [Carbon "UI shell", Polaris "Navigation", Material "Navigation rail/drawer"]

### Header
**Also called:** top bar, app bar, navbar, masthead.
Thin bar across the top. Holds global things: search, notifications bell, help, user avatar menu. **Rule:** global things only; page actions go in the page header, not here. [Material, Carbon]

### Page header
**Also called:** title bar, page heading.
The top of the content area: page title on the left, the page's main action buttons on the right, sometimes breadcrumbs above and tabs below. **Use:** every page. [Polaris "Page", Atlassian "Page header", Primer "PageHeader"]

### Content area
**Also called:** main, body, canvas.
Where the actual work happens. Usually has a max width (around 1200–1440px) on wide screens so lines don't stretch. Tables and dashboards may go full width. [Carbon grid, Polaris "Page" widths]

### Card
**Also called:** tile (Carbon), panel, box, container.
A box with a border or light shadow grouping related content. **Use:** dashboard widgets, grouping a section of a settings form, items in a grid. **Don't use:** to wrap everything. Cards inside cards is a common amateur mistake. [Material, Polaris, Carbon]

### Section
A titled group of content inside a page, separated by spacing or a divider rather than a box. **Use:** long settings pages. Often better than a card when you don't need the box.

### Divider
**Also called:** separator, rule, hr.
A thin line between groups. **Rule:** reach for spacing first; use a divider only when spacing alone isn't clear. [Material, Atlassian]

### Split view
**Also called:** master–detail, list–detail, two-pane.
A list on the left, the selected item's details on the right (like email). **Use:** working through many records one by one. [Apple, Fluent, Material "List-detail"]

### Footer
Bottom bar. In apps it's rare; in marketing sites it holds links. In forms and modals, a "footer" is the row of buttons at the bottom.

### Grid
The invisible columns content lines up to (usually 12 columns). You rarely see it, but it's why good pages look aligned. [Carbon "2x Grid", Material "Layout"]
