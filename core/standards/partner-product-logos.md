---
standard: partner-product-logos
title: Product logos for partner hardware
scope: core
applies_outputs: [partner-packaging, partner-product-page, partner-co-branded-asset, partner-announcement]
conformance: none
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
status: active
source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 96-100. File Brand_Guidelines__V03-Aug26__1.pdf
---

# Product logos for partner hardware

Governs the logo a hardware product carries: the project logo plus the product name, for example "Home Assistant Connect ZBT-2". Exists so every product in a range is named the same way on the box, the product page and the launch assets.

Partner-specific: applies only to material a commercial partner of the Open Home Foundation makes or co-brands with us. The Open Home Foundation's and the projects' own material follows each project's `design/` and `brand/` files, not this standard.

## Required elements
- The project lockup from the brand assets repository (https://github.com/OpenHomeFoundation/brand-assets), unchanged, with the product name set beside it in Biotif regular. The project name stays in its own lockup; only the product name is typeset.
- The project logo's rules for color variants, backgrounds and misuse, as written in `projects/<slug>/design/logo.md`.
- The full product name, never shortened (`projects/<slug>/brand/naming.md`).

## Rules

### Pick the lockup by space
| Lockup | Use |
|---|---|
| Main | Default. |
| Inline | Wide, shallow spaces such as a website navigation bar. |
| Split | Only for products in a line (for example Connect): logotype and logomark separated to fit the layout or make the name stand out. TODO: no project has a wordmark file, so a split cannot be built from official files; confirm with the Open Home Foundation before using it. |

- Yes: main product lockup on the box's left side panel.
- No: inline lockup squeezed into a square social tile.

### No wordmark alone
The source lists a wordmark-alone product lockup. No project has a wordmark, so it is not available.
- Yes: logomark plus "Home Assistant Connect ZBT-2".
- No: "Home Assistant Connect ZBT-2" set as text with no logomark.

## Never
- A product logo typeset from scratch, including the project name.
- The product name shortened or abbreviated.
- The logotype without the logomark.

## Machine checks
| Check | How | Fix |
|---|---|---|
| Logomark present | every product logo instance includes the project logomark | use the main or inline lockup |
| Full name | product name matches the name in `brand/naming.md` | write it in full |
| Official lockup | project lockup file comes from the brand assets repository | replace with the official file |

## Open
- Product logo files are not in the brand assets repository. TODO: where they live, or whether partners build them from the project lockup.
- The source shows the product-logo exclusion zone as a diagram (1/3 and 1/5 annotations) without stating it in words. TODO: confirm.

## How skills use this
Skills whose output type is in `applies_outputs` load this file in their "Context to load" step and run its Machine checks in review.
