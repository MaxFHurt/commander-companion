# Commander Companion v0.5.1 RC5 — Mana Visual Lock

The mana display is locked to the approved in-game reference.

- Total Mana is the first full-width horizontal row.
- Available Mana is the second full-width horizontal row directly below it.
- Mana colors within each row flow horizontally.
- White: sun.
- Blue: water drop inside a circular mana badge.
- Black: skull.
- Red: flame.
- Green: tree.
- Colorless: diamond, visually distinct from White.
- Exile remains a separate zone icon and does not reuse Blue mana.

RC5 removes legacy duplicate mana renderers and styles. Each shipped HTML variant contains exactly one `v048ManaIcon()` function, one `v051ManaGlyph()` function, and one canonical mana stylesheet (`v051-canonical-mana-system`).
