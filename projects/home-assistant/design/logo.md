---
area: design/logo
project: home-assistant
owner: Marketing Team
last_reviewed: 2026-09-30
review_every: 180d
draft: true
---

# Home Assistant: logo

Source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 50-59, 77-79 and 96-100, file `Brand_Guidelines__V03-Aug26__1.pdf`. Imported 2026-09-30. The source is signed off by the board (`decisions/2026-09-30-import-partner-guidelines-v1-1.md`). The source states that these rules are shared by every project logo, so ESPHome and Music Assistant point here.

Note: https://github.com/home-assistant/brands holds icons and logos for the brands Home Assistant integrates with, not Home Assistant's own identity. Its rules are a project-owned standard; see `standards/integration-brand-assets.md`.

## Anatomy
- **Logomark.** The Open Home Foundation house shape as an enclosure, in blue, with a white "antenna" inside (read as a tree, a set of nodes, or a PCB). The dark blue foundation "legs" of the Open Home Foundation mark never appear in a project logomark.
- **Logotype.** "Home Assistant" in Biotif semibold, Title Case (not capitals). Aligned on its baseline with the inner border of the house.

## Files
| Variant | File | Use |
|---|---|---|
| Main lockup | `home-assistant/logo/<screen or print>/lockup/main/` | Default. Certified and trademark-registered. Use whenever in doubt. |
| Stacked lockup | `.../lockup/stacked/` | Only where space or alignment rules out the main lockup, such as too little width. |
| Logomark alone | `.../logomark/` | Social avatars, or third parties publishing the mark only, and only where the name is nearby. |
| Colored, light background | lockups: files ending `-color-on-light`; logomark: `-color` (one file for both backgrounds) | Default and official. |
| Colored, dark background | lockups: files ending `-color-on-dark` | Dark backgrounds only. |
| Monochrome black or white | files ending `-monochrome-on-light` or `-monochrome-on-dark` | Photographic backgrounds, or print without color. |
| Icon, favicons, app icons | TODO | not covered by the source or the repository |

Paths are in the brand assets repository, https://github.com/OpenHomeFoundation/brand-assets/tree/main/home-assistant/logo; file prefix `HA-`. Layout and naming: `core/standards/partner-co-branding.md`, Required elements. The file prefix is internal, like the photography file names; it is not a way to write the name.

There is no wordmark: the logotype never appears without the logomark. This applies to ESPHome and Music Assistant as well. Product logos for partner hardware: `core/standards/partner-product-logos.md`.

## Clear space and size
- Exclusion zone on every side: one third of the height of the logomark. (The Open Home Foundation logo measures from the width instead; this is how the source states it.)
- The logo is drawn on a square modular grid; do not change its proportions.
- TODO: minimum size for print and screen. The source does not give one.

## Backgrounds
- Light: colored version (default).
- Dark: colored version for dark backgrounds.
- Photographic: monochrome black or white, whichever reads.

## Misuse
- Distorting, rotating, resizing, or moving any element.
- Replacing solid color with an outline.
- Placing on a background without contrast.
- Changing any color or adding a gradient. Only the palette in `color.md`.
- Drop shadows.
- Changing letter spacing.
- The logotype without the logomark.
- Deprecated versions, including the pre-2020 mark. The source shows them as images; TODO list them by file.

## Co-branding
With commercial partners: `core/standards/partner-co-branding.md`, and on their packaging `core/standards/partner-packaging.md`. Attribution wording is in naming.md. Lockup files with the Open Home Foundation mark: TODO. Partner marks ("Works with Home Assistant"): see marketing/partners.md.
