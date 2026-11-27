# Layout

## The standard SaaS layout

```
┌────────┬──────────────────────────────────────┐
│Sidebar │ Top bar (search · bell · account)    │
│ 220–   ├──────────────────────────────────────┤
│ 260px  │  Page header: title       [buttons]  │
│        │  (tabs)                              │
│        │  Content, max ~1280px wide           │
│        │                                      │
└────────┴──────────────────────────────────────┘
```

- **Sidebar:** 220–260px wide, collapsible to a 56–64px icon rail. Main sections on top, Settings and account at the bottom. [Carbon "UI shell", Polaris, Atlassian]
- **Top bar:** 48–64px tall. Global things only: search, notifications, help, account.
- **Page header:** title on the left, the page's actions on the right, primary action furthest right.
- **Content width:** forms and reading content max ~720px; general pages max ~1200–1440px; data tables and dashboards may go full width. [Polaris "Page" widths, Carbon grid, Material "Layout"]
- **Page padding:** 24–32px on desktop, 16px on phones.

## Where things go

| Thing | Where | Why |
|---|---|---|
| Logo | Top of sidebar (or top-left) | Convention; clicking goes to the home dashboard |
| Main nav | Sidebar | Room for 5–12 sections |
| Search | Top bar, left or center | Global; ⌘K opens it |
| Notifications, help, account | Top bar, right | Convention (Jakob's law) |
| Page title | Top-left of content | First thing scanned |
| Page's primary action ("New invoice") | Top-right of the page header | Convention across Polaris, Carbon, Atlassian |
| Bulk actions | Bar above the table when rows are selected | Close to what they act on |
| Row actions | ⋯ at the end of the row | Keeps rows clean |
| Form buttons | Bottom of the form (or sticky footer for long forms) | Done after filling in |
| Save state of a settings page | Sticky bar at the bottom ("Unsaved changes · Discard · Save") | Always visible |
| Destructive "Delete" | Away from the primary button, often in a ⋯ menu or a "Danger zone" at the bottom | Prevents accidents |
| Toasts | Bottom right (desktop), bottom center (phone) | Out of the way |

## Grid and alignment

- Use a **12-column grid** with 16–24px gutters for page layouts. Dashboard cards span 3, 4, 6 or 12 columns. [Carbon, Material]
- **Everything aligns to a few left edges.** The page title, cards and table all start on the same line.
- **Dashboards:** KPIs on top (3–5 across), then the main chart full width or 2/3, then supporting lists or tables. [NN/g "Dashboards", Polaris]

## Responsive

| Width | Layout |
|---|---|
| < 640px (phone) | Sidebar becomes a hamburger menu or bottom tab bar; one column; tables become cards or scroll sideways |
| 640–1024px (tablet) | Sidebar collapses to icon rail; 2 columns |
| > 1024px (desktop) | Full layout |

[Material "Window size classes", Tailwind breakpoints]
