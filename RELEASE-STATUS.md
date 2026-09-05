# Commander Companion v0.5.2 — Current Release Status

This CLEAN package supersedes the accumulated RC/hotfix documentation that was previously
shipped alongside the app. Historical notes were removed from the deploy package; they were
not used by the application at runtime.

## Current retained behavior
- Visual Master layout is frozen.
- Commander Tax badge is mounted inside the bottom of the commander-card box.
- Compact Commander Tax remains visible in public player/opponent summaries.
- Mana display remains dependent on the commander's color identity.
- NEXT PHASE and END TURN are the phase controls.
- Battlefield cards retain proportional card geometry and use horizontal-only overflow.
- Draw/startup lifecycle protections from the v0.5.1 hotfix line remain in the production HTML.
- Card Finder category work from the current codebase remains in the production HTML.

## Package cleanup
Removed from the deploy package:
- `index(1).html`
- `CommanderCompanion-Standalone.html`
- stale `UI-preview*.png` files
- duplicate `README(1).md`
- v0.5.1 RC handoff/release notes
- old mana regression notes/certification files
- prior hotfix notes
- prior visual parity audit
- unused standalone PNG assets that are already embedded/not referenced by production `index.html`

No runtime application logic was intentionally changed as part of this cleanup.
