# Commander Companion v0.5.1 RC2 — Mana Regression Fix

User-approved correction after RC1 review.

## Corrected
- Total Mana and Available Mana now render side-by-side, matching the approved in-game reference.
- Each mana section flows its legal commander-identity symbols horizontally.
- White: unique sun symbol in circular mana badge.
- Blue: water drop in circular mana badge.
- Black: skull in circular mana badge.
- Red: flame symbol in circular mana badge.
- Green: tree symbol in circular mana badge.
- Colorless: diamond symbol in circular mana badge, distinct from White.
- Exile keeps an independent upward-arrow zone icon and cannot share the Blue mana symbol.

## Regression guards
The phone and narrow-screen CSS now explicitly preserves the two-column Total/Available layout and `row / nowrap` icon flow. Static checks verify the approved symbol renderer and commander color-identity filter remain present in index.html, standalone HTML, and app-ui.js.

No unrelated issues from the RC1 issue report were changed in this correction pass.
