# V0.5.1 RC3 — Mana Layout Regression Fix

- Total Mana and Available Mana now share one explicit two-column mana console in the active player card.
- The two sections are hard-locked side by side at desktop and iPhone breakpoints; they cannot collapse into a vertical stack.
- Mana symbols inside each section remain horizontal.
- The existing approved mana symbol mapping is preserved.
- Service-worker cache was bumped to `commander-companion-v051-rc3`, and registration now bypasses cached service-worker scripts so an older UI cannot mask the correction after deployment.

This pass intentionally targets the reported mana-layout regression and its stale-cache delivery path.
