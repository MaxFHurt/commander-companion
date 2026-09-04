# Commander Companion — V0.5.1 RC1 Handoff

## Baseline
V0.5.1 RC1 was built from the supplied V0.4.8 source/handoff. The primary standalone entry remains `CommanderCompanion-Standalone.html`; `index.html` is the GitHub Pages entry.

## Locked decisions carried forward
- Industrial dark UI with restrained orange active accents; no green active shading.
- Commander remains top-left and begins in Command Zone; commander tax is displayed on the commander card.
- Active top line does not duplicate Hand, Graveyard or Commander Tax.
- Empty Status is absent.
- Exile and Graveyard live with other lower play-zone designations.
- Blue mana uses a water-drop visual; Exile is distinct; White and Colorless do not share a symbol.
- Card ID, Game Chat and Help use the compact bottom dock.
- Freeplay, Full Play Tracking and Mana Tracker remain separate experiences.
- First-run tutorial is optional and skippable.
- QA findings must be presented before fixes.

## Current QA status
See `TEST_REPORT.md` and `ISSUE_REVIEW-V0.5.1-RC1.md`. RC1 has one Critical, two High and one Medium finding. Do not promote to external tester build until owner-approved fixes are completed and the full regression pass is rerun.
