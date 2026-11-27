# 5. Feedback

How the app tells people what's happening. Pick by **how important** the message is and **whether people must act**.

| Message | Interrupts? | Goes away by itself? | Use |
|---|---|---|---|
| "Saved" | No | Yes | Toast |
| "Your trial ends in 3 days" | No | No (until dismissed) | Banner |
| "This invoice is overdue" | No | No | Alert (inline) |
| "Card number is wrong" | No | When fixed | Field error |
| "Delete 12 clients?" | **Yes** | No | Alert dialog ([overlays](6-overlays.md)) |

### Toast
**Also called:** snackbar (Material), notification (Carbon "toast notification"), flash message.
A small message that slides in at a corner and disappears after a few seconds. **Use:** confirming something just happened ("Invoice sent"). Can include one action ("Undo"). **Don't use:** for errors people must fix, or anything important; it disappears before people read it. [Material, Carbon, Polaris, shadcn "Sonner"]

> **Sources disagree: should toasts exist at all?**
> Material, Carbon, Polaris, Atlassian: yes, for low-importance confirmations.
> GOV.UK: avoids them; uses a notification banner at the top of the next page, because disappearing messages fail people who read slowly or use screen readers. WCAG requires enough time to read.
> **We follow:** toasts for confirmations only, shown for at least 5 seconds, paused while hovered, never for errors. Anything people must see goes in an alert or banner.

> **Sources disagree: where toasts appear.**
> Material: bottom center (or bottom left on desktop). Carbon, Polaris, Sonner default: bottom right / top right. **We follow:** bottom right on desktop, bottom center on phones.

### Alert
**Also called:** callout, inline notification (Carbon), message, section message (Atlassian).
A colored box inside the page. Four types, each with its color and icon: **info** (blue), **success** (green), **warning** (amber), **error/danger** (red). **Use:** something about this page or section that stays until resolved. [Gallery, Carbon, Atlassian, Polaris "Banner"]

### Banner
**Also called:** announcement bar, global alert, system message.
A full-width strip at the very top of the app. **Use:** things affecting the whole account ("Payment failed, update your card", "Scheduled maintenance Sunday"). Only one at a time. [Atlassian, Polaris, GOV.UK "Notification banner"]

### Field error
**Also called:** validation message, inline error.
Red text under a form field. See [4-inputs.md](4-inputs.md#parts-of-a-form-field).

### Error summary
A box at the top of a form listing every error with links to each field. **Use:** long forms after a failed submit. [GOV.UK]

### Spinner
**Also called:** loader, loading indicator, activity indicator.
A small spinning circle. **Use:** short waits (1–10 seconds) where you can't predict the shape of what's coming, and inside buttons while saving. [NN/g "Progress indicators", Carbon "Loading"]

### Skeleton
**Also called:** skeleton loader, placeholder, shimmer.
Gray shapes in the layout of the content that's about to load. **Use:** first load of pages, cards and tables. Feels faster than a spinner because the layout appears instantly. [NN/g "Skeleton screens", Carbon, Polaris, Atlassian]

### Progress bar
**Also called:** progress, determinate progress.
A bar filling from left to right with a percentage. **Use:** waits over 10 seconds where you know how far along it is (uploads, imports). [NN/g, Material, Carbon]

### Top loading bar
**Also called:** page progress bar.
A thin bar across the very top that runs while a new page loads (GitHub, YouTube). **Use:** page-to-page navigation.

### Badge
**Also called:** tag, label, chip, pill, status, lozenge (Atlassian).
A small colored label. **Use:** status ("Paid", "Overdue", "Draft"), categories, or counts. **Two kinds:** status badges (fixed colors meaning something) and count badges (the red "3" on a bell). [Gallery, Atlassian "Lozenge", Polaris, Primer "Label"]

### Status dot
**Also called:** indicator, presence dot.
A tiny colored dot ("● Online"). Always pair with text; color alone fails color-blind users. [WCAG 1.4.1, Carbon]

### Empty state
What a page shows when there's no data yet. See [patterns/empty-error-states.md](../patterns/empty-error-states.md).

### Notification center
**Also called:** inbox, activity panel, bell menu.
The panel that opens from the bell icon, listing recent events with unread dots. [Carbon, Atlassian]

### Onboarding checklist
**Also called:** setup guide, getting-started card.
"3 of 5 steps done: ✓ Add your logo ✓ Invite team ○ Connect bank". **Use:** first days of a new account. [Polaris "Setup guide"]
