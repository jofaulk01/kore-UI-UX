# 2. Navigation

How people get around the app.

### Nav item
**Also called:** menu item, nav link.
One entry in a sidebar or top nav: icon + label. **Rule:** always show which one is current (highlighted background or bar). Always keep the text label; icons alone are guessed wrong. [NN/g "Icon usability", Polaris]

### Top nav
**Also called:** horizontal nav, navbar.
Main sections as links across the header. **Use:** 2–5 sections, or marketing sites. Above that, use a sidebar. [Material, Carbon]

### Tabs
Row of labels that switch between views of the same thing (e.g., a customer's Overview / Invoices / Notes). **Use:** 2–7 related views of one object. **Don't use:** for steps in a process (use a stepper) or for unrelated pages (use the nav). Tabs change content in place; they don't feel like going to a new page. [NN/g "Tabs, used right", Material, Carbon]

### Segmented control
**Also called:** button group, toggle group.
A small row of joined buttons where one is selected, like "Day | Week | Month". **Use:** switching how the same data is shown. Smaller and lighter than tabs. [Apple, Polaris "ButtonGroup", Carbon "Content switcher"]

### Breadcrumbs
"Clients › Acme Inc › Invoice 104". Shows where you are and lets you go back up. **Use:** anything 3+ levels deep. **Don't use:** flat apps. [NN/g, GOV.UK, Carbon]

### Pagination
Page numbers and next/previous under a long list. **Use:** tables people search and jump around in. **Alternative:** "Load more" button or infinite scroll for feeds. Business tables should use pagination, because people need to find their place again. [NN/g "Infinite scrolling", Carbon]

### Stepper
**Also called:** progress indicator (Carbon), wizard steps, steps.
"1 Details › 2 Payment › 3 Review". **Use:** a long task split into ordered steps. [Carbon, Material, Ant "Steps"]

### Command palette
**Also called:** Cmd+K menu, quick switcher, spotlight.
A search box that pops up with a keyboard shortcut and lets you jump to any page or run any action. **Use:** apps people use daily. A strong "modern SaaS" signal (Linear, Vercel, GitHub). Add it after the basics work. [Primer, shadcn "Command"]

### Link
Underlined or colored text that goes somewhere. **Rule:** a link *goes somewhere*; a button *does something*. Don't mix them up. [GOV.UK, NN/g, Vercel]

### Anchor nav
**Also called:** table of contents, "on this page".
Jump links to sections of a long page, often on the right. **Use:** long settings or docs pages.

### Skip link
Hidden link that appears when keyboard users press Tab, letting them jump past the nav. Free accessibility win. [GOV.UK, WCAG]
