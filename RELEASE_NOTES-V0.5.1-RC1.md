# Commander Companion V0.5.1 RC1

## Implemented for this candidate
- Unified V0.5.1 visual polish and microanimations.
- Active player-card redundancy cleanup.
- Empty Status removal.
- Lower Exile / Graveyard / Tokens / Attachments zone row.
- Locked mana identity visuals, including circled/drop-style Blue treatment in app CSS/logic and distinct Exile/White/Colorless symbols.
- Detailed Board + Game Stats upper utilities; duplicate upper Game Settings removed.
- Compact bottom Card ID / Game Chat / Help dock.
- Optional first-run Learn vs Skip flow.
- Mid-game board reconstruction entry point for Freeplay.
- Player-side reconnect persistence/retry, connection-state indicator, seat recovery, duplicate-seat protection, host approval/release manager.
- Current version raised coherently to 0.5.1.

## Release status
RC1 is being held for owner review because formal QA found four issues. No QA-discovered issue was fixed without approval.


## RC2 visual regression correction
- Restored the locked mana icon family using distinct vector symbols: white sun, blue water drop, black skull, red flame, green tree, and colorless diamond.
- Blue mana is explicitly a water drop inside its circular mana badge.
- White and colorless remain distinct. Exile retains its separate upward-arrow zone icon.
- Total Mana and Available Mana are locked as two side-by-side horizontal sections at phone, tablet, and desktop widths; mana symbols inside each section remain a horizontal row.
- Added hard CSS/runtime regression guards so mobile breakpoints cannot revert the mana console to a vertical stack.
