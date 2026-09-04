# Commander Companion V0.5.1

This is the first external-playtest candidate based on the approved V0.4.8 handoff. Upload every file in this folder to the GitHub Pages repository root. Use `index.html` as the entry point, or open `CommanderCompanion-Standalone.html` directly for the self-contained build.

## V0.5.1 highlights

- Unified industrial UI treatment across app screens with subtle micro-animations and reduced-motion support.
- Final active-player cleanup: expanded top line keeps Library while Hand/Commander Tax are removed as duplicates; Commander Tax remains on the commander card; Graveyard is authoritative in the lower zone row.
- Locked mana visual set: white sun, blue water drop in a circle, black skull, red heat/flame mark, green tree-style club, distinct colorless diamond.
- Exile uses a distinct zone symbol and never shares the blue-mana icon.
- Empty status presentation collapses when there are no statuses or poison.
- Bottom utility dock for Card ID, Game Chat, and Help; Detailed Board + Game Stats remain in the compact top game toolbar.
- Player-side multiplayer reconnect foundation: persisted room/seat/name/guidance, automatic retry, seat recovery, duplicate-seat protection, grace-period retention, and connection-state indicator. Private hand data remains device-local through the existing private storage system.
- Optional first-run onboarding with an explicit “Skip — I already know what I’m doing” path.
- Mid-game Board Reconstruction entry in game controls for Free Play recovery/setup.

See `TEST_REPORT.md` and `KNOWN_ISSUES.md` for certification status.
