---
standard: partner-packaging
title: Packaging for partner hardware
scope: core
applies_outputs: [partner-packaging]
conformance: none
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
status: active
source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 105-115. File Brand_Guidelines__V03-Aug26__1.pdf
---

# Packaging for partner hardware

Governs the box, trays, inserts, and printed matter for hardware a commercial partner makes that carries the Open Home Foundation or a project brand. Exists so packaging from any partner is recognizably ours on a shelf, and so the sustainability pillar is visible in the material itself, not only claimed in copy. The source marks each element as required or recommended; this file keeps that distinction.

Partner-specific: applies only to material a commercial partner of the Open Home Foundation makes or co-brands with us. The Open Home Foundation's and the projects' own material follows each project's `design/` and `brand/` files, not this standard. Product logos on the box follow `core/standards/partner-product-logos.md`.

## Required elements
- Material: paper-based and aimed at 100% recyclable. Unbleached or natural brown kraft paper or card for boxes. Accessory trays, flyers, and instructions also paper.
- Ink: two colors at most, one of them white. White is Spot White with UV coating.
- Cut-out: a house-shaped cut-out on the front side panel, used as the opening, with the project logomark printed so it shows through it.
- Left side panel: the full product logo (logomark and logotype, for example "Home Assistant Connect ZBT-2") so the product is identifiable when stacked or shelved, and so the trademarked version of the logo appears on the box.

## Recommended elements
- Top panel: a product silhouette or geometric illustration, vector art with white or colored fill. Subtle patterns or complementary geometric elements are allowed if they stay on-brand. Project logotype top left with the line or product name; logomark top right, vertically aligned and centered against the left-hand elements. A short payoff or tagline at the bottom if space allows.
- Bottom panel: logotype; box contents; hardware requirements if any; regulatory marks (CE, FCC, WEEE) at the size their own rules set. Optional: product description, and vector exploded views or internal diagrams in the top-panel style, as long as the layout stays minimal.
- Right side panel: on the left, the partnership line (below); on the right, Open Home Foundation logo and partner logo, horizontal by preference, vertical if space requires, per `core/standards/partner-co-branding.md`. The partnership line may move to another panel if this one does not fit.
- Front side panel: Open Home Foundation logo on the left, partner logo on the right, plus the cut-out.
- Reverse side panel: SKU, EAN, UPC, or other codes needed for retail and logistics.

### Partnership line
Approved wording, set in capitals, with the bracketed parts replaced:

DESIGNED AND BUILT BY THE OPEN HOME FOUNDATION AND [PARTNER BRAND]. MADE IN [COUNTRY]. POWERED BY A WORLDWIDE COMMUNITY OF TINKERERS AND DIY ENTHUSIASTS.

## Rules

### White does the lifting
Use white for contrast and negative space, to lift logos and text off the kraft, and as a base under the second color when that color needs to print more vividly. Because the kraft is the third color and white is how the design reads on it.
- Yes: white logotype on kraft; white base printed under the blue illustration.
- No: blue logotype printed directly on kraft with no white base, losing contrast.

### The second color carries the brand
Use the second color for logotypes, icons, patterns, and graphic accents. Think in flat shapes, not gradients. Build apparent extra tones with overprinting, hatching, stippling, or linework. For Home Assistant products, the second color is the product color in `projects/home-assistant/design/color.md`.
- Yes: flat Connect blue (#006FBB) illustration with hatched shading.
- No: a gradient from blue to white across the top panel.

### No neon
Pantone neon was tried as the second color and rejected for readability.
- Yes: Pantone 300 U for the Connect line.
- No: a fluorescent Pantone for extra pop.

### Split the logo only for product lines
Separating logotype and logomark on the box is allowed only when the product belongs to a line (for example Connect), to fit the layout or make the name stand out. The logomark must then still appear elsewhere on the same surface.
- Yes: "Home Assistant Connect" top left, logomark top right, on a Connect line box.
- No: logomark dropped from the box entirely because the name fitted better without it.

## Never
- The commercial partner badge on packaging (`core/standards/partner-co-branding.md`).
- Non-paper materials without approval. The source asks for paper-based packaging, 100% recyclable wherever possible.
- More than two ink colors.
- Gradients.
- The foundation's "legs" (dark blue foundation element) inside a project logomark.

## Machine checks
| Check | How | Fix |
|---|---|---|
| Ink count | count distinct inks in the print file; white counts as one | reduce to white plus one |
| Cut-out present | dieline has a house-shaped cut-out on the front side panel, logomark visible through it | add the cut-out and logomark print |
| Product logo on left side | left side panel contains logomark plus logotype plus product name | add the full product logo |
| Partnership line | text matches the approved wording with partner and country filled | copy the approved wording |
| Badge absent | badge file not in the print file | remove it |
| Regulatory marks | CE, FCC, WEEE present where the product needs them, at their own minimum sizes | check against each authority's rules |

## How skills use this
Skills whose output type is `partner-packaging` load this file and `core/standards/partner-co-branding.md` in their "Context to load" step, and run both files' Machine checks in review. Packaging always needs Open Home Foundation approval before print; no skill may mark packaging as final.
