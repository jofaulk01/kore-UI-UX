# 6. Overlays

Things that float on top of the page. Rule of thumb: the bigger the overlay, the more it interrupts. Use the smallest one that works.

```
smallest  Tooltip → Hover card → Popover → Dropdown menu → Drawer → Modal → Full-screen  biggest
```

### Tooltip
**Also called:** toggletip (if it opens on click), hint.
A small dark label that appears on hover or keyboard focus. **Use:** naming an icon button, explaining a short term. **Don't use:** for anything people must read, anything clickable inside, or on phones (no hover). [Gallery, NN/g "Tooltip guidelines", Carbon]

### Hover card
**Also called:** preview card.
A richer card that appears on hover over a name or link (hover a customer name, see their email and plan). [shadcn, Primer]

### Popover
**Also called:** flyout (in some systems), toggletip.
A small floating panel opened by clicking, attached to its button. Can hold anything: a mini form, filters, details. Closes when you click outside. **Use:** quick edits or filters without leaving the page. [Gallery, Atlassian, Polaris]

### Dropdown menu
See [3-actions.md](3-actions.md#dropdown-menu). A popover that holds only a list of actions.

### Modal
**Also called:** dialog, popup, modal window, lightbox.
A box in the middle of the screen with the page dimmed behind it. You must finish or close it before doing anything else. **Use:** short focused tasks (rename, quick create with 1–5 fields), or important decisions. **Don't use:** for long forms, for content people need to compare with the page behind, or opening a modal from a modal. [Gallery, NN/g "Modal & nonmodal dialogs", Material, Carbon]

**Parts:** title · body · footer with buttons (Cancel, then primary on the right) · close ✕ in the corner. Esc closes it. Focus moves into it and returns to the button that opened it. [WCAG, shadcn/Base UI handle this for you]

### Alert dialog
**Also called:** confirmation dialog, destructive dialog.
A small modal asking "Are you sure?". **Use:** before actions that can't be undone. The button names the action ("Delete 12 clients"), not "Yes". Clicking outside doesn't close it. **Better alternative when possible:** do the action and offer "Undo" in a toast. [NN/g "Confirmation dialogs", Atlassian, Polaris]

### Drawer
**Also called:** sheet, side sheet, side panel, flyout, tray, slide-over.
A panel that slides in from the edge (usually the right), page still visible beside it. **Use:** viewing or editing one record while keeping the list in view, filters, settings panels. Mobile version slides up from the bottom ("bottom sheet"). [Gallery, Material "Side sheet", Atlassian, Polaris, shadcn "Sheet"/"Drawer"]

> **Sources disagree: modal or drawer for editing a record?**
> Material and Carbon lean toward full pages or modals; Atlassian, Linear-style SaaS and shadcn lean toward side drawers.
> **We follow:** drawer for viewing/editing a record from a list (people keep their place), modal for short create forms and confirmations, a full page when the form is long or the record is the main thing.

### Full-screen overlay
**Also called:** full-screen dialog, takeover.
Covers everything. **Use:** complex editors or multi-step creation on phones. Rare on desktop.

### Command palette
See [2-navigation.md](2-navigation.md#command-palette). Technically a modal.

### Lightbox
A dark full-screen viewer for images or documents.
