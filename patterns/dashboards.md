# Dashboards

## Start with the question

A dashboard answers "How are things, and what needs my attention?" in five seconds. Before building, write down the 3–5 questions the user asks every morning. Every widget must answer one of them. [NN/g "Dashboards: making charts and graphs easier to understand", Polaris "Home", Stephen Few's dashboard principles]

## Order on the page

1. **Needs attention** (if anything): an alert or a short list ("7 invoices overdue · Review").
2. **KPIs:** 3–5 stat cards across the top, each with period and change.
3. **Main trend:** one big chart (usually over time).
4. **Breakdowns:** smaller charts or tables (by client, by category).
5. **Recent activity or to-dos.**

## KPI cards

- Label · value · change vs previous period · optional sparkline.
- Make "good" obvious: costs going up is red.
- Same period across all cards, shown in one place ("Last 30 days ▾").
- Clicking a KPI goes to the detailed list behind it.

## Charts

- Pick the chart by the question (see [glossary/7-data-display.md](../glossary/7-data-display.md#chart)).
- One message per chart; the title says it ("Revenue is up 12% since June" or plainly "Revenue, last 6 months").
- Accent color for the key series, gray for comparison.
- Tooltips on hover with exact values.
- No 3D, no pie charts over 4 slices, no dual axes unless the audience is analysts.
- Empty chart: say "Not enough data yet" instead of a flat line at zero.

## Date range

A single date-range picker at the top applies to everything, with presets (Today, Last 7 days, Last 30 days, This month, Custom). Show the comparison period clearly.

## Avoid

- Vanity widgets nobody acts on.
- More than ~9 widgets on one screen (Miller's law).
- Real-time updating numbers that jump around unless the job is monitoring.
