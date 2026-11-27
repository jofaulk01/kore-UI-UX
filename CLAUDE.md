# Working on this repository

This repo is a documentation library, not an app. Its owner is a product engineer, not a designer: write in plain words and gloss any unavoidable term inline.

- Every rule cites at least two sources from `sources.md`. When sources disagree, add a "Sources disagree" box saying who says what, what we follow, and why. Prefer business-software systems (Carbon, Atlassian, Polaris, Primer) when breaking ties.
- Free and open source only. Never recommend a paid library, kit or service without labeling it as paid.
- The picker (`picker/index.html`) is published as an Artifact. Option ids in it must match `picker/variants.md` and the stock themes in `starter/themes/`. If you change one, change all three, and regenerate the stock theme files from the picker.
- Keep the glossary's coverage check current: new element names go in the right section with their "also called" names.
- Flag security or accessibility risks explicitly with a ⚠ note.

When another project asks to use this library, point it to `starter/README.md`.
