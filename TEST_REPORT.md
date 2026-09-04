# Commander Companion V0.5.1 RC1 — Certification Report

Date: 2026-09-02
Baseline: Commander Companion V0.4.8 + approved handoff
Candidate: V0.5.1 RC1
Release decision: **HOLD — issues require owner review before fixes**

## Passed automated checks
- All modular JavaScript files parse with `node --check`.
- All six inline script blocks in each of the three HTML entry points parse successfully.
- Runtime version is coherent at `0.5.1` in the primary state engine and standalone entry points.
- Six-player state creation: all commanders begin in Command Zone; battlefield starts empty.
- Draw boundary: library count never becomes negative when a draw request exceeds cards remaining.
- Smart mana payment: tracked sources are selected/tapped and pools remain nonnegative.
- Undo/checkpoint state restoration test passed.
- 60-turn six-player combat stress model passed with creatures, tokens, deaths, graveyards, trample and state rotation.
- 240-turn six-player state stress model passed with 35 permanents/player, graveyard recursion, exile, statuses, commander casts, floating mana, turn/round rotation and nonnegative zone/counter invariants.
- ManaBox parser passed standard quantity, `4x` quantity, set/collector and Commander/Mainboard/Sideboard section formats.
- Deck-builder save/load/import function surfaces are present.
- Full Play Tracking, Freeplay and Mana Tracker modes are present.
- Optional first-run flow contains both Learn and “Skip — I already know what I’m doing.”
- Bottom utility dock contains Card ID, Game Chat and Help.
- Game Stats replacement for duplicate top Game Settings is present.
- Active-card cleanup removes upper Hand/Cmd Tax and relocates Graveyard/Exile to the lower zone row.
- Empty Status collapse logic is present.
- Blue mana is a water-drop glyph; Exile uses a different glyph; White and Colorless are distinct.
- Player-side reconnect session storage, retry scheduling, connection state UI, duplicate-seat protection and host-side reconnect approval/release controls are implemented at source level.
- V0.5.1 unified polish and reduced-motion-aware microanimations are present.

## Formal QA findings — not fixed
See `ISSUE_REVIEW-V0.5.1-RC1.md`.
1. **CC-051-001 Critical:** PeerJS transport is not loaded by the shipped package; multiplayer cannot be certified and appears nonfunctional without external injection.
2. **CC-051-002 High:** Service worker precache references missing/stale assets.
3. **CC-051-003 High:** Freeplay still routes plays through mandatory legality blocking.
4. **CC-051-004 Medium:** Board reconstruction is partial rather than a complete one-flow public-state rebuild.

## Not truthfully certifiable in this workspace
The managed browser blocks local files and localhost, so the following require real-device/hosted testing after issue approval/fix:
- Full click-through of every screen/modal on iPhone/iPad Safari.
- Actual Host/Player WebRTC room creation, join, six-device state sync and reconnect.
- Private-hand preservation across real browser refresh/termination.
- Camera Card ID permissions/scanning.
- Live Scryfall/MTGJSON network resolution.
- PWA install/offline launch.
- Touch layout / safe-area / rotation / no-overflow verification on real iPhones.
- Long-duration battery/memory behavior.

## Certification stance
This is a genuine **V0.5.1 RC1 implementation artifact**, but it is **not approved as the external tester build** because a Critical multiplayer issue and two High issues were found. Per project instructions, none of those QA findings were silently fixed.
