# Loading

## Pick by how long the wait is

| Wait | What people feel | Show |
|---|---|---|
| Under 0.1s | Instant | Nothing |
| 0.1–1s | Slight delay, still in flow | Nothing for the first ~300ms, then a subtle indicator. Avoids a flash of spinner |
| 1–10s | Waiting | **Skeleton** for content that's loading; **spinner** in the button for an action |
| Over 10s | Leaving to do something else | **Progress bar** with percentage and time left, and let them leave (notify when done) |

The thresholds come from Nielsen's response-time limits. [NN/g "Response times: 3 important limits", NN/g "Progress indicators", Carbon "Loading", Material "Progress indicators"]

## Skeleton or spinner?

- **Skeleton:** first load of a page, card, table or list. The shapes match the real layout so nothing jumps when data arrives. [NN/g "Skeleton screens 101", Polaris, Atlassian, Carbon]
- **Spinner:** inside buttons while saving, small areas, or when you can't predict the layout.
- **Top loading bar:** moving between pages.
- **Never a full-page spinner** that hides everything if you can show the page frame (sidebar, header, page title) immediately.

> **Sources disagree: shimmer or pulse?**
> Carbon and Polaris use a static or pulsing skeleton; many SaaS apps use a moving shimmer. Both are fine. Pick one in the picker and use it everywhere. Turn the movement off when the user has "reduce motion" on.

## Make it feel faster

1. **Keep the frame:** sidebar, top bar and page header never disappear during loading.
2. **Optimistic updates:** when someone ticks a task or renames something, show the change right away and save in the background. If the save fails, undo it and show an error. [Common in Linear, Notion; NN/g on perceived performance]
3. **Keep old content while refreshing:** when filtering a table, keep the old rows (dimmed) with a top bar instead of blanking to a skeleton.
4. **Load the most important part first:** KPIs before the long table.
5. **Reserve space** for images and charts so the page doesn't jump (layout shift).
6. **Buttons while saving:** keep the button the same width, show a spinner and "Saving…", disable it to prevent double submits.

## Long jobs (imports, exports, reports)

Run them in the background. Show a progress bar or a status ("Processing 1,204 of 5,000"), let people leave, and send a notification or email when done. [Carbon, Polaris]
