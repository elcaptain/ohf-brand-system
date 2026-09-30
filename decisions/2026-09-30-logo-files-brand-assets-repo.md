---
date: 2026-09-30
area: design
project: core
trigger: correction
change: The OpenHomeFoundation/brand-assets repository is the source of truth for logo and badge files; no project has a wordmark
affected:
  - core/standards/partner-co-branding.md
  - core/standards/partner-product-logos.md
  - projects/open-home-foundation/design/logo.md
  - projects/home-assistant/design/logo.md
  - projects/esphome/design/logo.md
  - projects/music-assistant/design/logo.md
by: @elcaptain
---

# Logo files come from the brand assets repository

## What happened
The partner guidelines v1.1 point to a Google Drive folder for logos and list logotype-alone (wordmark) variants for the projects and for product logos. Both are wrong. @elcaptain confirmed:
- https://github.com/OpenHomeFoundation/brand-assets is the source of truth for logo files. It was read at commit `163c942`, 2026-08-04.
- No project has a wordmark. The guidelines should have said so.

## What changed
- `core/standards/partner-co-branding.md` names the repository as the only source for logo and badge files and describes its layout and naming. The Drive folder is no longer referenced.
- The commercial partner badge now points to `open-home-foundation/badge/` in the repository, not the openhomefoundation.org repository.
- Each project's `design/logo.md` gives its directory and file prefix (`OHF-`, `HA-`, `ESPH-`, `MA-`).
- The logotype-alone variant is removed. "The logotype without the logomark" is now listed under Misuse. This matches the Open Home Foundation logo, where the source already forbade it.

## What the repository does not hold
- Product logos (for example Home Assistant Connect ZBT-2).
- Icons, favicons and app icons.
- Background variants of the commercial partner badge. The source describes three, and the repository has one.
- Project logomarks come as a single `-color` file, with no light and dark versions. The Open Home Foundation logomark has both.

## Not settled here
- The split product lockup, and the packaging top panel that sets the logotype apart from the logomark, both need a wordmark file. They are marked TODO until the Open Home Foundation confirms how to handle them.
- The repository README gives partner@openhomefoundation.org as the contact for commercial use, and the partner guidelines give brand@openhomefoundation.org. The standards keep brand@ until someone confirms which is right.
