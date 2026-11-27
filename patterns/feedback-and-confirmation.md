# Feedback and confirmation

## Every action gets a response

People need to know their click worked. Pick the lightest response that's clear:

| Action | Response |
|---|---|
| Toggle, tick, small edit | The change itself is the feedback (plus optional subtle "Saved") |
| Create, send, save a form | Toast: "Invoice #1042 sent" |
| Action that can be undone | Toast with **Undo** (5–10 seconds) |
| Action that fails | Alert or persistent toast with **Try again**; keep the user's input |
| Action that affects other people or money and can't be undone | **Confirmation dialog** first |
| Background job finished | Notification (bell) and/or email |

## Undo beats "Are you sure?"

People click through confirmation dialogs without reading. Where possible, do the action and offer **Undo**. Save confirmations for things that truly can't be reversed (deleting an account, sending money, emailing 500 clients). [NN/g "Confirmation dialogs can prevent user errors (if not overused)", Polaris, Atlassian]

## Confirmation dialogs done right

- Title asks the specific question: "Delete 3 invoices?"
- Body says the consequence: "They'll be removed for everyone. This can't be undone."
- The confirm button repeats the action: "Delete 3 invoices" (red). Not "Yes" or "OK".
- Cancel is the safe default focus.
- For very destructive actions, ask people to type the name ("Type ACME to confirm"). [GitHub/Primer pattern]

## Toast rules (from the glossary)

Confirmations only, at least 5 seconds, pause on hover, one action max, never for errors that need fixing, bottom right on desktop.

## Disabled things

Prefer showing why something isn't available ("Add a bank account to send payments", via tooltip or helper text) over silently graying it out.
