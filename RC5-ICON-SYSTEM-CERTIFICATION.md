# Commander Companion v0.5.1 RC5 — Icon System Certification

RC5 removes the legacy/fallback mana icon renderer from every shipped HTML entry point.

Locked checks:
- One `v048ManaIcon()` renderer per entry point.
- One `v051ManaGlyph()` SVG glyph map per entry point.
- White, Blue, Black, Red, Green, and Colorless use the canonical SVG family.
- Blue uses the water-drop glyph inside the circular mana badge.
- White and Colorless are distinct.
- Exile uses its own zone glyph and does not share Blue mana artwork.
- Total Mana and Available Mana remain separate horizontal mana rows.
- JavaScript syntax check passes for all shipped HTML entry points.
