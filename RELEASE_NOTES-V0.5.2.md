# Commander Companion V0.5.2

## Visual Master
- Implements the September 3, 2026 locked iPhone Visual Master.
- Commander card remains proportional and aligns with the two mana rows.
- Battlefield is the elastic vertical region; card slots remain 5:7 and overflow horizontally only.
- Tap/Untap All is an icon-only battlefield control.
- Status sits with the player name and only contains a label when a status is active.
- Commander Tax remains on the commander card and in public summary counters.
- Action tiles use visual enabled/disabled state rather than AVAILABLE/NOT AVAILABLE text.
- Opponent summaries expose life at a glance with battlefield previews directly beneath.

## Functional fixes carried forward
- Draw-step confirmation no longer depends on the fragile legacy dynamic-action node.
- `dynamicActionFields` lifecycle is guarded/recreated to prevent the startup null dereference.
- Card Finder type categories are retained, including Lands.
- Interactive text and icon/text groups remain centered.
