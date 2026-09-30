---
date: 2026-09-30
area: design
project: core
trigger: correction
change: Logo files come from the OpenHomeFoundation/brand-assets repository, not the Google Drive folder named in the partner guidelines
affected:
  - core/standards/co-branding.md
  - projects/open-home-foundation/design/logo.md
  - projects/home-assistant/design/logo.md
  - projects/esphome/design/logo.md
  - projects/music-assistant/design/logo.md
by: @elcaptain
---

# Logo files come from the brand assets repository

## What happened
The partner guidelines v1.1 point partners to a Google Drive folder for logos. The Open Home Foundation keeps the logos in https://github.com/OpenHomeFoundation/brand-assets (read at commit `163c942`, 2026-08-04), which gives every file a stable path. That closes the "stable per-file paths" TODO in each `design/logo.md`.

## What changed
- `core/standards/co-branding.md` names the repository as the one source for logo files and describes its layout and naming once. The Drive folder is kept as a reference because the source names it.
- Each project's `design/logo.md` gives its directory and file prefix (`OHF-`, `HA-`, `ESPH-`, `MA-`).

## What the repository does not hold
Recorded as TODOs in the project files:
- Logotype-alone files for Home Assistant, ESPHome and Music Assistant.
- Product logos (for example Home Assistant Connect ZBT-2).
- Icons, favicons and app icons.
- Project logomarks come as a single `-color` file, with no light and dark versions. The Open Home Foundation logomark has both.

## Not settled here
- The repository also holds badges (`open-home-foundation/badge/`), one file per badge. The co-branding standard still points to the badges in the openhomefoundation.org repository, where the source describes three background variants.
- The repository README gives partner@openhomefoundation.org as the contact for commercial use, and the partner guidelines give brand@openhomefoundation.org. The standards keep brand@ until someone confirms which address is right.
