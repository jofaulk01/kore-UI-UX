# Tables and lists

The core of business tools. Build these well and most of the app feels professional.

## Anatomy

```
[Search…]  [Status ▾] [Owner ▾] [Date ▾]   Clear      [Columns] [Export] [+ New]
Active filters: Status: Overdue ✕
┌──┬──────────┬──────────────┬────────┬───────────┬──────────┬──┐
│☐ │ Invoice ↓│ Client       │ Due    │    Amount │ Status   │  │
├──┼──────────┼──────────────┼────────┼───────────┼──────────┼──┤
│☐ │ #1042    │ Acme Studio  │ Nov 24 │ $4,250.00 │ ● Paid   │⋯ │
└──┴──────────┴──────────────┴────────┴───────────┴──────────┴──┘
Showing 1–25 of 312                               ‹ 1 2 3 … 13 ›
```

## Rules

1. **First column identifies the row** and links to the record.
2. **Alignment:** text left, numbers and money right, status and icons left or center. Header aligns with its column. [Carbon, Polaris, NN/g "Data tables"]
3. **Tabular numbers**, same decimals, currency symbol consistent.
4. **Sticky header** on long tables; sticky first column on wide ones.
5. **Sort** by clicking the header; show the arrow on the sorted column only. Default sort is the most useful one (usually newest first).
6. **Row click** opens the record (page or drawer). Checkboxes and ⋯ menus don't trigger it.
7. **Bulk actions** appear in a bar when rows are selected ("3 selected · Send reminders · Delete").
8. **Hover row** gets a subtle background.
9. **Truncate long text** with "…" and show the full value in a tooltip; never let a cell push the table wider than the screen.
10. **Don't show 30 columns.** Show the 5–7 that matter; let people add more from a column picker.

## Search and filters

- Search box filters as you type (debounced, roughly 300ms).
- Filters as dropdown buttons; active ones shown as removable chips with **Clear all**.
- Saved views or tabs for common filters ("All · Unpaid · Overdue · Drafts"). [Polaris "IndexFilters", Linear-style views]
- Filters and search live in the URL (see [navigation](navigation-and-transitions.md)).

## Pagination vs infinite scroll

> **Sources disagree.**
> Feeds and social apps use infinite scroll. NN/g and Carbon recommend pagination for data people search, compare or need to come back to.
> **We follow:** pagination (25 or 50 per page, selectable) for business tables; "Load more" for activity feeds.

## On phones

Tables turn into a list of cards (name, key value, status) or scroll sideways with the first column fixed.

## Lists vs tables

Use a **list** when each item has 1–3 pieces of info and no comparing is needed (notifications, recent activity). Use a **table** when people compare values across rows.
