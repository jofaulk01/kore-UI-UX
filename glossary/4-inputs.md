# 4. Inputs

Things people fill in or choose. Rules that apply to all of them are at the bottom.

### Text input
**Also called:** text field, input, textbox.
A single line for typing. **Use:** names, emails, short values. Size the box to the expected answer (a ZIP code box is short). [GOV.UK, Material, Carbon]

### Textarea
**Also called:** multi-line text field.
A multi-line box. **Use:** notes, descriptions, messages. Let it grow or make it tall enough for the expected answer.

### Search input
**Also called:** search field, search bar.
A text input with a magnifying glass, sometimes with a ⌘K hint. **Use:** global search in the header, or filtering a list or table. Results should update as you type when the data is small. [Gallery, Primer]

### Number input
**Also called:** stepper (Gallery), quantity input, counter, nudger.
A field with − and + buttons. **Use:** small counts (quantity, seats). For money or big numbers, use a plain text input with a number keyboard.

### Select
**Also called:** dropdown, select input, picker.
Click to open a list, pick one value. **Use:** 5–15 fixed options. Under 5, use radio buttons so all choices are visible. Over 15, use a combobox. [NN/g "Dropdowns", GOV.UK]

### Combobox
**Also called:** autocomplete, autosuggest, typeahead, searchable select.
A select you can type into to filter. **Use:** long lists (countries, customers, products). [Gallery, shadcn, React Aria]

### Multi-select
**Also called:** tag input, chips input.
Pick several values; each shows as a removable chip. **Use:** assigning tags, people, categories.

### Checkbox
A square you tick. **Use:** yes/no choices that apply when you press Save, and choosing several items from a list. [GOV.UK, NN/g]

### Radio buttons
**Also called:** radio group.
Round options where only one can be chosen. **Use:** 2–5 mutually exclusive options you want people to see all at once. [GOV.UK, Carbon]

### Switch
See [Toggle / switch](3-actions.md#toggle--switch). Takes effect immediately; checkbox if it waits for Save.

### Slider
**Also called:** range input.
Drag a handle along a track. **Use:** rough values where precision doesn't matter (volume, price range filter). **Don't use** when people need an exact number; pair it with an input if so. [NN/g, Material]

### Date picker
**Also called:** calendar, datetime picker.
A field that opens a calendar. **Use:** picking dates near today, or date ranges for reports. **Exception:** for dates people know by heart (birthdays), three plain fields (day / month / year) are faster. [GOV.UK "Date input", NN/g]

> **Sources disagree: calendar or typed date?**
> GOV.UK prefers typed fields because calendars are slow for distant dates. Material, Carbon and most SaaS use calendar popovers.
> **We follow:** calendar popover that also accepts typing, plus preset ranges ("Last 7 days", "This month") for reports. Business users pick recent dates far more than distant ones.

### Time picker
Like a date picker, for times. Usually a select of 15- or 30-minute steps.

### File upload
**Also called:** file input, dropzone, uploader.
A button or a dashed area you drag files into. Show file name, size, progress, and a remove button for each. [Gallery, Carbon, Polaris "DropZone"]

### OTP input
**Also called:** one-time code input, PIN input.
A row of single-digit boxes for login codes. Paste must fill all boxes at once. [shadcn "Input OTP"]

### Color picker
Pick a color. Rare in business tools; use when people brand something (invoice color, labels).

### Rich text editor
**Also called:** WYSIWYG editor, RTE.
A text area with bold, lists, links. **Use:** notes, emails, descriptions that need formatting. Use an existing free editor (Tiptap, Lexical); don't build one.

### Rating
Stars or a 1–5 scale. Rare in business tools.

---

## Parts of a form field

```
Label            ← always visible, above the field
[ Field       ]  ← the input
Hint text        ← optional: format or example
⚠ Error message  ← replaces/joins hint when wrong
```

- **Label:** always visible above the field. **Never** use the placeholder (gray text inside) as the only label; it vanishes when you type. Every source agrees. [NN/g "Placeholders are harmful", GOV.UK, Carbon, WCAG]
- **Hint text / helper text:** small gray text explaining format ("We'll send the invoice here").
- **Error message:** red text under the field saying what's wrong and how to fix it ("Enter an email like name@company.com"), not just "Invalid".
- **Required vs optional:** mark the less common one. Business forms are usually mostly required, so mark "(optional)". [GOV.UK, NN/g]
- **Fieldset:** a group of related fields with one heading ("Billing address").
- **Form:** see [patterns/forms.md](../patterns/forms.md) for layout and validation timing.
