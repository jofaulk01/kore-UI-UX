# Typography

## One font

Use one font family for the whole app, plus a monospace font for IDs, codes and numbers in tables if you like. All five in the picker are free (Google Fonts, Open Font License): **Geist, Figtree, IBM Plex Sans, Manrope, Nunito Sans**. Monospace: **Geist Mono**. [Carbon, Primer, Polaris all use one family]

Why not Inter? It's excellent but so common in AI-generated apps that it now reads as default. Use it only if a project already does.

## The type scale (app UI)

| Role | Size | Weight | Line height | Example |
|---|---|---|---|---|
| Page title (H1) | 24px | 650–700 | 1.25 | "Invoices" |
| Section title (H2) | 18px | 600 | 1.3 | "Payment details" |
| Card / group title (H3) | 15–16px | 600 | 1.35 | "Acme Studio" |
| Body | **14px** | 400 | 1.5 | Table cells, descriptions |
| Small / labels | 13px | 500 | 1.4 | Field labels, table headers |
| Tiny | 12px | 500 | 1.4 | Badges, hints, timestamps |
| KPI number | 28–32px | 650 | 1.15 | "$42,180" |

Six sizes is enough. If you need a new one, you probably need weight or color instead. [Carbon "Type sets", Atlassian "Typography", Polaris, Primer]

> **Sources disagree: 14px or 16px body?**
> Carbon, Atlassian, Primer, Polaris and most SaaS apps: **14px** for dense app screens.
> GOV.UK, Material (body large) and most readability research: **16px**.
> **We follow:** 14px inside the app, 16px for long reading (help articles, marketing pages) and for **form inputs on phones** (iPhones zoom into any input under 16px).

## Weights

Use three: **400** regular, **500–550** medium (labels, buttons), **600–700** semibold/bold (titles, KPI numbers). More weights look messy. [Material, Carbon]

## Rules

1. **Line length 50–75 characters** for paragraphs. Long lines are hard to read. [NN/g, Material, WCAG guidance]
2. **Hierarchy with size and weight first, color second.** Secondary text is the "muted" gray, not a smaller size every time.
3. **Numbers line up:** use tabular figures (`font-variant-numeric: tabular-nums`) in tables and KPIs so digits are equal width. Right-align money. [Carbon, Polaris]
4. **Sentence case** for everything: "Create invoice", not "Create Invoice". Every major system agrees. [Material, Carbon, Polaris, Atlassian, GOV.UK]
5. **ALL CAPS only for tiny labels** (badges, overlines), with a little extra letter spacing.
6. **Don't center long text.** Center only short headings in empty states and marketing heroes.
7. **Headings get tighter letter spacing** (−0.01 to −0.02em) at 20px and above; small text never.
