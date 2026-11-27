# Empty and error states

## Empty states: four kinds

| Kind | Example | Show |
|---|---|---|
| **First use** | New account, no invoices yet | What will appear here, why it's useful, one primary button ("Create invoice"). Optionally sample data or a setup checklist |
| **No results** | Search or filters match nothing | "No invoices match 'acme overdue'", and a **Clear filters** button. Never just a blank table |
| **Cleared** | Inbox zero, all tasks done | A short positive message. No button needed |
| **No permission** | User can't see this area | Say so plainly and who to ask ("Ask an admin for access") |

**Rules:** keep the page frame and title visible; use a simple icon, not a big illustration, in work tools; one button, not three. [NN/g "Designing empty states in complex applications", Polaris "EmptyState", Carbon "Empty states", Atlassian "Empty state"]

## Error states

### Field errors (forms)
Next to the field, in red, saying how to fix it. See [forms.md](forms.md).

### Action errors (save failed, send failed)
- Keep what the person typed. Never clear a form after an error.
- Show an alert near the action or a toast **that stays** until dismissed, with **Try again**.
- Say what happened in plain words: "Couldn't send invoice. Acme's email address bounced." Not "Error 422".

### Page or section errors (data didn't load)
- Replace only the broken part (one card or the table), not the whole page.
- Message + **Try again** button + a way out (back, or contact support).

### Whole app errors
- **404:** "We can't find that page" + link to the dashboard + search.
- **500 / outage:** "Something went wrong on our end" + try again + status page link if you have one.
- **Offline:** a banner "You're offline. Changes will save when you reconnect."

## Writing error messages

1. Say what happened.
2. Say why, if you know.
3. Say what to do next.
4. Don't blame the user, don't joke, don't apologize three times.
5. Show technical details (error code) small, for support, after the plain message.

[NN/g "Error-message guidelines", GOV.UK "Error message", Polaris "Error messages", Atlassian "Writing error messages"]

> ⚠ **Security note:** error messages shown to users should never include stack traces, database details, or whether an email exists in your system ("No account with that email" helps attackers find valid accounts). Use "Email or password is incorrect".
