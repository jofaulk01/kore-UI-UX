# Navigation and page transitions

## Changing pages

1. **The frame stays put.** Sidebar and top bar never reload or flicker; only the content area changes. [Carbon "UI shell", Polaris]
2. **Show progress immediately:** a thin bar at the top, or the new page's skeleton. Never a frozen screen after a click.
3. **Transition:** none, or a quick fade (150–200ms). Avoid slides between top-level pages; they make apps feel slow. See [rules/motion.md](../rules/motion.md).
4. **Highlight where you are:** the active sidebar item, tab and breadcrumb must always match the page.
5. **Scroll position:** new pages start at the top; going **back** returns to where you were.

## URLs (the address bar)

Every meaningful view has its own URL, so people can bookmark, share and use the back button:

- Each page, each record (`/invoices/1042`), each tab (`/clients/88/invoices`).
- Filters, search and sort on lists (`/invoices?status=overdue&sort=due`). Coming back to the list keeps the filters.
- Open drawers can have a URL too, so a shared link opens the same record.

[NN/g "URLs are UI", Vercel guidelines]

## The back button

Must always do what people expect: go to the previous view. Never trap people, and never break back by opening things that aren't in the history (big modals that act like pages should be pages).

## Where people navigate

| Need | Pattern |
|---|---|
| Main sections | Sidebar |
| Views of one record | Tabs |
| Up one level | Breadcrumbs or a back arrow in the page header |
| Next/previous record | Arrows in the page or drawer header ("2 of 48") |
| Jump anywhere | Command palette (⌘K) |
| Keyboard power users | Shortcuts shown in menus and tooltips |

## Leaving with unsaved changes

Warn before leaving a page with unsaved edits ("You have unsaved changes. Leave anyway?"), or better, autosave drafts. [Polaris "Contextual save bar", NN/g]
