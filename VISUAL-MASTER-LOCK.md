# Commander Companion — Visual Master Lock

## Authority
`VISUAL-MASTER-V0.5.2.png` is the frozen visual authority for the in-game screen.

The production UI must preserve the master's:
- overall iPhone portrait orientation and density
- player header structure
- commander card placement and proportional sizing
- commander-tax badge placement inside the commander-card box
- compact public Commander Tax value in player/opponent summaries
- commander/color-identity-dependent mana display
- Total Mana above Available Mana
- battlefield size and proportional 5:7 card slots
- horizontal-only battlefield overflow when card count exceeds visible capacity
- compact zone strip
- NEXT PHASE / END TURN controls
- compact action controls
- opponent life-at-a-glance summaries and battlefield rails
- Card ID / Game Chat / Help bottom dock
- dark industrial black/gray/orange visual language

## Change control
Do not alter the frozen layout unless the user explicitly unlocks it in conversation first.

## Build verification
Every future build should be rendered on the target iPhone viewport and compared back to
`VISUAL-MASTER-V0.5.2.png` before being presented as visually correct.
