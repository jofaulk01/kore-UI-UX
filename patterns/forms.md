# Forms

## Layout

1. **One column.** People fill forms top to bottom; two columns cause skipped fields. Exception: short related pairs on one line (First name / Last name, City / ZIP). [NN/g "Web form design", Baymard research summarized by NN/g, GOV.UK]
2. **Labels above fields**, not beside them. Faster to scan and works on phones. [NN/g, Material, Carbon, GOV.UK]
3. **Group related fields** under a small heading (Client, Items, Payment) with more space between groups than within.
4. **Field width matches the answer:** short for ZIP, long for address.
5. **Ask only what you need.** Every field costs completions. Mark the rare optional ones "(optional)".
6. **Sensible defaults:** pre-fill what you can (today's date, the usual payment terms).

## Buttons

- Primary action at the end of the form, labeled with what happens ("Create invoice").
- Secondary "Cancel" next to it, less prominent.
- Long forms or settings: **sticky footer** with the buttons, always visible.
- Disable submit only while saving, not before the form is valid. A disabled button doesn't tell people what's missing. Let them click and show the errors. [GOV.UK, Adam Silver "Form Design Patterns" summarized by GOV.UK, NN/g]

> **Sources disagree: disabled submit button until the form is valid?**
> Many apps do it. GOV.UK and NN/g advise against it because people can't tell why the button is dead.
> **We follow:** keep the button enabled, validate on submit, and show what's missing.

## Validation: when to show errors

| When | Do |
|---|---|
| While typing | Don't show errors yet (it's rude to say "invalid email" after one letter) |
| On leaving the field (blur) | Check format (email, phone, date) |
| On submit | Check everything; scroll to the first error; for long forms show an error summary at top |
| After an error, while fixing | Re-check as they type so the error disappears the moment it's fixed |

[NN/g "Inline validation", GOV.UK "Validation", Polaris]

## Saving

| Kind of form | Pattern |
|---|---|
| Create something new | Explicit "Create" button |
| Settings page | Sticky "Unsaved changes · Discard · Save" bar appears when something changes (Polaris contextual save bar) |
| Toggles and quick preferences | Save instantly, confirm with a subtle "Saved" |
| Long documents and notes | Autosave, with "Saved 2 min ago" text |

After saving: toast "Invoice created", then go to the new record (or back to the list with it highlighted).

## Inputs that help

- Correct keyboard on phones: email, number, phone (`type` and `inputmode`).
- Autocomplete hints for name, email, address, card fields (`autocomplete`).
- Show/hide password toggle.
- Format as people type (phone, money) but accept any reasonable input.

> ⚠ **Security note:** check every field again on the server. Browser checks are for convenience only; anyone can bypass them.
