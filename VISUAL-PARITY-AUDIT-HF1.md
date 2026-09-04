# Commander Companion v0.5.2 — Visual Master Parity Audit HF1

Compared shipped HTML against `VISUAL-MASTER-V0.5.2.png` after the user reported the deployed build did not match the approved master.

## Confirmed parity failures in the original v0.5.2 package

1. **The package contained a stale `UI-preview.png`.** It depicted the older Venom-era layout, not the locked Visual Master. This invalidated the release comparison itself.
2. **The bottom Card ID / Game Chat / Help dock was still coded as a fixed viewport overlay.** In the Visual Master it is a normal full-width row below the opponent summaries.
3. **The active player's private hand panel was still allowed to render.** It is not present in the locked Visual Master and changes vertical geometry.
4. **Empty Status behavior did not match the locked master.** Runtime logic blanked the pill while the frozen master visibly shows `No Status`.
5. **Legacy battlefield CSS still contained wrap/centering rules.** The Visual Master requires one proportional 5:7 horizontal card rail with horizontal-only overflow.

## HF1 corrections

- Dock is moved under `playersGrid` and is no longer fixed/floating.
- Private-hand panel is hidden in the locked game layout.
- Empty status renders `No Status` to match the frozen master image exactly.
- Active and opponent battlefield rails are explicitly single-row, left-aligned, horizontal-scroll-only.
- Existing locked commander/mana/battlefield/action/opponent geometry remains unchanged.

The locked image remains the release authority. No new layout decisions were introduced in this hotfix.
