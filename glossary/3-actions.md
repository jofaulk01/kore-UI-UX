# 3. Actions

Things people click to make something happen.

### Button
The basic "do something" control. Comes in levels of importance (the "button hierarchy"):

| Level | Looks like | Use for | How many per area |
|---|---|---|---|
| **Primary** | Solid brand color | The one main action ("Save", "Create invoice") | **One** |
| **Secondary** | Outlined or light gray fill | Other normal actions ("Export", "Cancel") | A few |
| **Tertiary / ghost** | Text only, no box | Low-importance actions ("Learn more", "Skip") | Any |
| **Destructive** | Red | Deleting or anything that can't be undone | Usually one |

**Rules:** label with a verb that says what happens ("Send invoice", not "OK" or "Submit"). One primary per screen area. Show a spinner inside the button and disable it while it's working so nobody double-clicks. [Material, Carbon, Polaris, Atlassian, GOV.UK]

> **Sources disagree: where the primary button goes.**
> Material, Polaris, Atlassian, Carbon, Apple: primary on the **right** in dialogs and page headers ("Cancel  [Save]").
> GOV.UK: primary on the **left**, at the end of the form, because people read top-down, left to right.
> **We follow:** right in dialogs, drawers and page headers; left-aligned under long single-column forms. That matches the business-tool systems and still keeps long forms readable.

### Icon button
A button that is only an icon (trash can, pencil, three dots). **Rule:** always add a tooltip and a hidden label for screen readers. Only use for icons everyone knows. [NN/g, WCAG, Vercel]

### Split button
A button with a small arrow attached: click the main part for the default action, the arrow for alternatives ("Save ▾ → Save as draft"). [Carbon "Combo button", Atlassian]

### Dropdown menu
**Also called:** menu, action menu, overflow menu, kebab menu (⋮), meatball menu (⋯).
A list of actions that opens from a button. **Use:** to tuck away less-used actions, like the ⋯ at the end of a table row. **Not the same as a select**: a menu *does* things; a select *picks a value*. [Carbon "Overflow menu", Polaris "ActionList", Material]

### Context menu
The menu that appears on right-click. Nice extra; never the only way to do something.

### Toggle / switch
On/off control that takes effect **immediately** ("Email notifications: on"). **Rule:** if the change only applies after pressing Save, use a checkbox instead. [NN/g "Toggle switch guidelines", Carbon, Apple]

### Floating action button (FAB)
Round button floating in a corner. A mobile/Material pattern. **Don't use** in desktop business apps; put the action in the page header. [Material; not used by Carbon, Polaris, Atlassian]

### Toolbar
A row of buttons for acting on content, like above a table or editor. [Carbon, Fluent]

### Bulk action bar
**Also called:** batch actions, action bar.
Appears when you tick rows in a table: "3 selected · Delete · Export". [Carbon "Data table batch actions", Polaris "BulkActions"]

### Copy button
Small button that copies a value (an API key, an ID) and briefly shows "Copied". [Primer, Vercel]
