# Commander Companion V0.5.1 RC1 — Issue Review

**Rule followed:** Issues discovered during formal QA were documented and were **not fixed**. They require product-owner approval before a fix pass.

## CC-051-001 — Multiplayer transport library is not loaded
- **Severity:** Critical / Release blocker
- **Category:** Multiplayer / Networking
- **Evidence:** All three standalone HTML entries initialize `window.Peer=null`, and the package contains no PeerJS script include or loader. Multiplayer startup functions immediately fall back to local mode or return “Peer networking library could not load.”
- **Expected:** Host/Join multiplayer should create a PeerJS/WebRTC room and allow client connections, including the new V0.5.1 reconnect flow.
- **Actual:** In this package as written, `window.Peer` never becomes available, so multiplayer cannot establish a room unless an external hosting layer injects PeerJS.
- **Recommendation:** Fix before external playtest. Add a controlled PeerJS load path or bundle the required client library, then test two-device through six-device connections and reconnects.
- **Status:** Awaiting approval. Not fixed.

## CC-051-002 — Service worker precache list references files not present in the release
- **Severity:** High
- **Category:** Offline / PWA / Packaging
- **Evidence:** `sw.js` attempts to cache `styles.css`, `app-actions.js`, `manifest.webmanifest`, `cc-skull-micro.png`, `cc-wordmark.png`, `icon-512.png` and other `?v=0.4.5` paths that are not in this release folder. `cache.addAll()` therefore rejects; the catch suppresses the error.
- **Expected:** Install/activation should establish a valid offline cache for the shipped release.
- **Actual:** The initial precache transaction can fail, leaving offline behavior dependent on later runtime fetch caching instead of a verified install cache.
- **Recommendation:** Fix before calling offline/PWA support certified. Synchronize the asset list/version and either ship every listed asset or remove unused paths.
- **Status:** Awaiting approval. Not fixed.

## CC-051-003 — Freeplay still uses mandatory legality blockers for card plays
- **Severity:** High
- **Category:** Gameplay mode / Requirements mismatch
- **Evidence:** `isFreeplay()` exists and bypasses the opening-hand gate, but card actions still route through `applyWithLegality()`, which always calls `validateAction()` before applying the action. No Freeplay bypass/override is present in that function.
- **Expected:** Per approved product behavior, Free Play should allow the table to do whatever is needed, including entering/reconstructing an already-running game, with validation available as assistance rather than mandatory blocking.
- **Actual:** Enabled legality rules can still block Freeplay actions.
- **Recommendation:** Add a Freeplay policy that defaults to permissive execution while offering optional validation/warnings. Preserve strict validation in Full Play Tracking.
- **Status:** Awaiting approval. Not fixed.

## CC-051-004 — Mid-game board reconstruction does not capture the complete public snapshot in one workflow
- **Severity:** Medium
- **Category:** Freeplay / Board reconstruction
- **Evidence:** The V0.5.1 reconstruction dialog captures life totals, commander cast counts, turn, and phase, then relies on separate battlefield controls for cards. It does not directly capture active player, poison, hand/library counts, statuses, mana/floating mana, graveyard/exile contents, or counters/attachments in the same wizard.
- **Expected:** A user should be able to rebuild the table state at a moment’s notice when Commander Companion is introduced mid-game.
- **Actual:** The current tool is a useful partial snapshot, but a full table recreation requires several additional screens/actions.
- **Recommendation:** Expand the wizard or explicitly make it a staged reconstruction flow covering all public state before external beta.
- **Status:** Awaiting approval. Not fixed.

## Test-environment limitation (not logged as an app defect)
Automated browser launch in this workspace is blocked from loading both local `file://` pages and localhost by the managed browser policy. Therefore visual runtime interactions, real WebRTC handshakes, camera access, iOS Safari behavior, live Scryfall/MTGJSON calls, and real-device reconnection could not be truthfully certified here. Static parsing, model stress tests, parser tests, package checks, and source-level feature verification were completed instead.
