---
date: 2026-09-30
area: design
project: core
trigger: review
change: Imported the board-approved partner guidelines v1.1 into design, marketing/partners and three new core standards
affected:
  - core/standards/co-branding.md
  - core/standards/product-packaging.md
  - core/standards/product-photography.md
  - projects/open-home-foundation/design/
  - projects/home-assistant/design/
  - projects/esphome/design/
  - projects/music-assistant/design/
  - projects/open-home-foundation/marketing/partners.md
  - projects/home-assistant/marketing/partners.md
  - projects/esphome/marketing/partners.md
  - projects/music-assistant/marketing/partners.md
by: TODO-handle
---

# Imported the board-approved partner guidelines v1.1

## What happened
"Marketing and Product Guidelines for our commercial partners", v1.1 (August 2026), file `Brand_Guidelines__V03-Aug26__1.pdf`, was signed off by the board. A first draft of the file contained errors; the corrected version fixed the Open Home Foundation logotype weights (ExtraBold and Medium), the RGB value of Choice #E10054, the missing RGB values for HA Black, HA Grey and HA White, and the contact address (brand@openhomefoundation.org). This import uses the corrected file.

## What changed
- Three new core standards (`scope: core`, `conformance: none`): co-branding, product packaging, product photography. The builder's logo template already referred to a core co-branding standard; this creates it.
- Open Home Foundation, ESPHome and Music Assistant: `design/logo.md`, `design/color.md`, `design/typography.md` and `design/tokens.json` written from the source and set `draft: false`. They keep TODOs for things the source does not cover (minimum logo sizes, type scale, per-file asset paths).
- Home Assistant: brand palette, brand type, product colors and product logos added beside the existing product UI tokens. These files stay `draft: true` because they also hold UI tokens drafted from the frontend repository, which the board sign-off does not cover. The import settles two open questions in them: the brand blue is #18BCF2, and Roboto is the UI face, not the brand face.
- All four projects: `design/imagery.md` points to the photography standard; `marketing/partners.md` gains who may use the brand, partner logo rules, and a Partner copy summary. `partners.md` stays `draft: true` (mixed sources).
- `brand/` is untouched in every project.
- No project's `ready:` changes. `design` cannot be declared ready while layout, motion, templates and accessibility still hold TODOs.

## Not copied from the source, on purpose
- The source's project descriptions use "powerful", "empowers" and "seamlessly", which the validator bans in boilerplate and key messages. The Partner copy sections paraphrase instead. Boilerplate stays in each project's `brand/messaging.md`.
- The photography file-name convention uses "HA". Kept for file names only; captions and alt text still follow the never-shorten rule.

## Authored in this import, not in the source
The Yes and No contrast pairs in the three standards were written for this import to meet the spec's contrast-pair rule. They illustrate the source's rules; they are not quotations from it. The WCAG ratios in the contrast tables were computed from the hex values. The pass or fail verdicts were read from the source's pairing slides by pixel sampling and checked by eye on a sample.

## Open after sign-off
- Four approved pairings measure about 2:1, below the WCAG 3:1 minimum for large text and graphics: OHF Light Blue with OHF Light Grey, and HA Blue with HA White, in both directions. The source marks OHF Dark Blue on Sustainability (12.51:1) as failing for regular text. The board-approved verdicts are recorded as the rule; the tables flag the rows.
- The source directs body text in HA Grey on light backgrounds, but its own pairing for HA Grey on HA White fails for regular text (4.30:1).
- The Privacy description names "OHF Blue" as its accent while the swatch is #00A4EB.
- HA Grey shares Pantone 431 C and its CMYK with OHF Dark Grey.
- Packaging puts the Open Home Foundation logo and "designed and built by the Open Home Foundation" on commercial products. `core/voices.md` says the foundation never fronts a commercial push. The two may be compatible (a maker's mark is not a promotion) but the core owner should say so in `core/voices.md`.

## Why this and not a one-off
Partner packaging, photography and co-branded assets recur with every hardware launch. As standards, they are loaded by any skill whose output type matches, with no skill edits.
