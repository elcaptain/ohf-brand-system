---
area: design/color
project: open-home-foundation
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
draft: false
---

# Open Home Foundation: colour

Tokens are the source of truth in tokens.json; this file explains them. Source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), file `Brand_Guidelines__V03-Aug26__1.pdf`, pp. 28-46. Imported 2026-09-30. The source is signed off by the board (`decisions/2026-09-30-import-partner-guidelines-v1-1.md`). Use HSL, RGB, or hex on screen and CMYK or Pantone in print.

## Palette
### Primary
Signature blue dominates; neutrals, dark blue, and light grey support it.

| Token | Value | Name | Print |
|---|---|---|---|
| ohf-light-blue | #18BCF2 | OHF Light Blue (brand blue; the source also calls it "OHF Blue") | Pantone 298 C; CMYK 65, 3, 0, 0 |
| ohf-dark-blue | #09202E | OHF Dark Blue | Pantone 5395 C; CMYK 100, 44, 10, 91 |
| ohf-dark-grey | #5A6675 | OHF Dark Grey | Pantone 431 C; CMYK 63, 45, 34, 25 |
| ohf-grey | #A2AAB6 | OHF Grey | Pantone 429 C; CMYK 35, 23, 19, 2 |
| ohf-light-grey | #F7F6F2 | OHF Light Grey | Pantone Stalactite; CMYK 4, 3, 5, 0 |

### Secondary: one sub-palette per pillar
Each pillar has a main color, an accent, a gradient from main to accent, a third tone, plus OHF Light Grey and OHF Dark Blue as grounding neutrals.

| Token | Value | Name | Print |
|---|---|---|---|
| privacy | #BECFE5 | Privacy, main (soft blue: peace of mind) | Pantone 5455 C; CMYK 23, 8, 2, 0 |
| privacy-accent | #00A4EB | Privacy, accent | not given |
| privacy-neutral | #5C7391 | Privacy, neutral | not given |
| choice | #E10054 | Choice, main (magenta: action) | Pantone 1925 C; CMYK 0, 100, 52, 0 |
| choice-accent | #F8B34C | Choice, accent (warm yellow) | not given |
| choice-neutral | #89223C | Choice, neutral | not given |
| sustainability | #D6E96D | Sustainability, main (luminous green) | Pantone 2296 C; CMYK 15, 0, 71, 0 |
| sustainability-accent | #41D09B | Sustainability, accent (Deep Mint) | Pantone 2413 C; CMYK 71, 0, 55, 0 |
| sustainability-neutral | #66988E | Sustainability, neutral | not given |

## Semantic roles
| Role | Token |
|---|---|
| brand, dominant color | ohf-light-blue |
| headings on light backgrounds | ohf-dark-blue |
| body text on light backgrounds | ohf-dark-grey |
| body text on dark backgrounds | ohf-grey |
| background, light | ohf-light-grey |
| background, dark | ohf-dark-blue |
| replaces pure black | ohf-dark-blue |
| replaces pure white | ohf-light-grey |
| topic color for privacy, choice, sustainability | the matching secondary sub-palette |

Pure #000000 and #FFFFFF are for monochrome graphics only.

## Light and dark
Light: OHF Light Grey background, OHF Dark Blue headings, OHF Dark Grey body. Dark: OHF Dark Blue background, OHF Light Grey headings, OHF Grey body. Avoid OHF Light Blue text on light backgrounds.

## Contrast
The source gives pass or fail for each pairing in three uses: regular text (17 pt and below), large text (18 pt and above), graphic components. The table records the source's verdicts and the WCAG 2.x ratio computed from the hex values. The source's verdicts are board-approved and are the rule. Flagged rows fall below WCAG 2.x AA; where an output must meet WCAG (websites, docs, apps), do not use a flagged pairing for the uses it fails.

| Foreground | Background | Ratio | Source: regular / large / graphic | Note |
|---|---|---|---|---|
| ohf-dark-blue | ohf-light-grey | 15.44:1 | pass / pass / pass | |
| ohf-dark-grey | ohf-light-grey | 5.41:1 | pass / pass / pass | |
| ohf-grey | ohf-light-grey | 2.17:1 | fail / fail / fail | |
| ohf-light-blue | ohf-light-grey | 2.04:1 | fail / pass / pass | Flag: below the 3:1 AA minimum for large text and graphics |
| ohf-dark-blue | ohf-light-blue | 7.57:1 | pass / pass / pass | |
| ohf-dark-grey | ohf-light-blue | 2.65:1 | fail / fail / fail | |
| ohf-grey | ohf-light-blue | 1.06:1 | fail / fail / fail | |
| ohf-light-grey | ohf-light-blue | 2.04:1 | fail / pass / pass | Flag: below 3:1 |
| ohf-dark-blue | ohf-grey | 7.13:1 | pass / pass / pass | |
| ohf-dark-grey | ohf-grey | 2.49:1 | fail / fail / fail | |
| ohf-light-blue | ohf-grey | 1.06:1 | fail / fail / fail | |
| ohf-light-grey | ohf-grey | 2.17:1 | fail / fail / fail | |
| ohf-light-grey | ohf-dark-grey | 5.41:1 | pass / pass / pass | |
| ohf-grey | ohf-dark-grey | 2.49:1 | fail / fail / fail | |
| ohf-light-blue | ohf-dark-grey | 2.65:1 | fail / fail / fail | |
| ohf-dark-blue | ohf-dark-grey | 2.86:1 | fail / fail / fail | |
| ohf-light-grey | ohf-dark-blue | 15.44:1 | pass / pass / pass | |
| ohf-grey | ohf-dark-blue | 7.13:1 | pass / pass / pass | |
| ohf-light-blue | ohf-dark-blue | 7.57:1 | pass / pass / pass | |
| ohf-dark-grey | ohf-dark-blue | 2.86:1 | fail / fail / fail | |
| ohf-dark-blue | privacy | 10.53:1 | pass / pass / pass | |
| ohf-dark-grey | privacy | 3.69:1 | fail / pass / pass | |
| ohf-grey | privacy | 1.48:1 | fail / fail / fail | |
| ohf-light-grey | privacy | 1.47:1 | fail / fail / fail | |
| ohf-dark-blue | choice | 3.44:1 | fail / pass / pass | |
| ohf-dark-grey | choice | 1.21:1 | fail / fail / fail | |
| ohf-grey | choice | 2.07:1 | fail / fail / fail | |
| ohf-light-grey | choice | 4.49:1 | fail / pass / pass | |
| ohf-dark-blue | sustainability | 12.51:1 | fail / pass / pass | Flag: passes AA for regular text; the source's "fail" looks like an error |
| ohf-dark-grey | sustainability | 4.38:1 | fail / pass / pass | |
| ohf-grey | sustainability | 1.76:1 | fail / fail / fail | |
| ohf-light-grey | sustainability | 1.23:1 | fail / fail / fail | |

Pairings for the accent and neutral tokens are not in the source.

## Open question
The Privacy description says its accent is "OHF Blue"; the swatch is #00A4EB, not OHF Light Blue #18BCF2. This file uses the swatch.
