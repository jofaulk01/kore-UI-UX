# 7. Data display

How information is shown. This is the heart of dashboards and business tools.

### Stat card
**Also called:** KPI card, metric card, stat, scorecard, number tile.
A card with one big number and its label: "Revenue this month · $42,180 · ▲ 12% vs last month". **Parts:** label (small, gray) · value (big) · change vs. previous period (green/red with arrow) · optional sparkline. **Use:** the top row of a dashboard, 3–5 of them. More than that and nothing stands out. [Polaris, Tremor, Carbon "Data visualization", NN/g "Dashboards"]
**Rules:** say what period it covers. Make "good" clear: a rise in costs is red, not green. Click it to see the detail.

### Chart
**Also called:** graph, data visualization.
Which kind to use:

| Question | Chart |
|---|---|
| How does it change over time? | Line or area chart |
| How do categories compare? | Bar chart (horizontal if labels are long) |
| What's the share of a whole? | Stacked bar, or donut if 2–4 parts |
| Is there a relationship? | Scatter plot |
| What's the trend at a glance? | Sparkline (tiny line, no axes) |

**Rules:** avoid pie charts with more than 4 slices, and avoid 3D. Label directly when possible. One highlighted series, others gray. [Carbon "Data visualization", Material, NN/g]

### Data table
**Also called:** table, data grid, grid.
Rows of records with columns. The most important element in business tools. **Parts:**
- **Toolbar:** search, filters, column picker, export, primary "New" button.
- **Header row:** column names, click to sort (↑↓ arrow shows direction).
- **Rows:** checkbox for bulk select · first column is the record's name and links to it · status badge · ⋯ menu at the end.
- **Footer:** pagination and "Showing 1–25 of 312".
**Rules:** right-align numbers and money, left-align text, same decimal places. Keep the header visible on scroll ("sticky header"). [Carbon "Data table", Polaris "IndexTable", Atlassian "Dynamic table", NN/g "Data tables"]

### Filters
**Also called:** filter bar, facets, filter chips.
Controls that narrow a list: a row of dropdown buttons ("Status ▾ · Owner ▾ · Date ▾") with active filters shown as removable chips and a "Clear all". [Polaris "Filters", Carbon]

### List
**Also called:** list view, item list.
Simple stacked rows (title, subtitle, action). **Use:** fewer fields than a table needs, like notifications or recent activity. [Gallery, Material "Lists"]

### Description list
**Also called:** key–value list, details list, property list, summary list (GOV.UK).
Label on the left, value on the right: "Email · ana@acme.com". **Use:** record detail pages. [GOV.UK "Summary list", Primer]

### Activity feed
**Also called:** timeline, history, audit log.
A vertical list of events with time and who did it: "Ana marked invoice #104 as paid · 2h ago". [Atlassian, Carbon]

### Accordion
**Also called:** collapsible, disclosure, expander, details.
Headers you click to expand their content. **Use:** FAQs, long settings, hiding advanced options. **Don't use:** to hide things people need all the time. [Gallery, NN/g "Accordions", GOV.UK]

### Tree view
Nested folders you can expand. **Use:** hierarchies (folders, categories, org charts).

### Kanban board
**Also called:** board, pipeline.
Columns of cards you drag between stages ("Lead → Quoted → Won"). **Use:** work that moves through stages.

### Calendar view
A month/week grid showing events. **Use:** bookings, schedules.

### Avatar
A round photo or initials representing a person. **Avatar group / stack:** overlapping avatars "+3". Always have an initials fallback. [Gallery, Material, Atlassian]

### Tag / chip
See [Badge](5-feedback.md#badge). Chips you can remove (✕) or click are "input chips" or "filter chips". [Material]

### Kbd
**Also called:** keyboard key, shortcut hint.
A small key-shaped label: `⌘K`. Shows shortcuts next to menu items. [shadcn, Primer]

### Code block / copy field
A monospace box with a copy button for IDs, API keys, snippets. [Primer, Vercel]

### Empty, loading and error versions
Every item on this page needs all three. See [patterns/](../patterns/).
