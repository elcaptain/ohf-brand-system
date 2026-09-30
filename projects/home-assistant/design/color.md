---
area: design/color
project: home-assistant
owner: Marketing Team
last_reviewed: 2026-09-30
review_every: 180d
draft: true
---

# Home Assistant: colour

Tokens are the source of truth in tokens.json; this file explains them. Two sets live here and they are not interchangeable:

- **Brand palette**, for marketing, print, packaging, and co-branded material. Source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 64-76, file `Brand_Guidelines__V03-Aug26__1.pdf`. Imported 2026-09-30.
- **Product UI tokens**, for anything that imitates or sits inside the Home Assistant interface. Source: the frontend theme (https://github.com/home-assistant/frontend/tree/dev/src/resources/theme/color).

The partner guidelines settle the earlier open question: the brand blue is HA Blue #18BCF2 (UI primary-50). primary-40 #009ac7 stays the UI primary and link color.

## Palette
### Brand: primary
HA Blue carries the brand; HA Black, HA Grey, and HA White support it.

| Token | Value | Name | Print |
|---|---|---|---|
| ha-blue | #18BCF2 | HA Blue | Pantone 298 C; CMYK 65, 3, 0, 0 |
| ha-black | #1D2126 | HA Black | Pantone 419 C; CMYK 76, 65, 66, 90 |
| ha-grey | #6E7191 | HA Grey | Pantone 431 C; CMYK 63, 45, 34, 25 (identical to OHF Dark Grey in the source; confirm) |
| ha-white | #F2F4F9 | HA White | CMYK 4, 2, 0, 0; no Pantone given |

### Brand: secondary
Home Assistant is the only project with a secondary palette. Five colors to tell key topics apart (the source names Community, Voice, and Roadmap as examples), mainly for social assets. The source does not say which color belongs to which topic; TODO.

| Token | Value | Name |
|---|---|---|
| ha-dark-blue | #007FA8 | Dark Blue |
| ha-light-blue | #CCF2FF | Light Blue |
| ha-dark-green | #528C77 | Dark Green |
| ha-light-green | #16F3BE | Light Green |
| ha-yellow | #FFD502 | Yellow |

No print values are given for the secondary palette.

### Brand: product colors
Each product or product line has one color, used with the primary palette and as the second ink on packaging (`core/standards/partner-packaging.md`).

| Token | Value | Product | Print |
|---|---|---|---|
| product-green | #417063 | Home Assistant Green | Pantone 342 U; CMYK 92, 12, 66, 43 |
| product-voice-pe | #DF735A | Home Assistant Voice Preview Edition | Pantone 7579 U; CMYK 0, 68, 93, 0 |
| product-connect | #006FBB | Home Assistant Connect line | Pantone 300 U; CMYK 100, 54, 0, 3 |

The source labels the second product "Voice PE". `brand/naming.md` has no product names yet; "Home Assistant Voice Preview Edition" is the full name as sold, written out here because project names are never shortened. Confirm, and add hardware names to `brand/naming.md`.

### Product UI tokens
| Token | Value | Name |
|---|---|---|
| primary-05 | #001721 | primary, darkest |
| primary-30 | #006787 | primary, dark |
| primary-40 | #009ac7 | primary (UI `--primary-color`, links) |
| primary-50 | #18bcf2 | brand blue |
| primary-60 | #37c8fd | primary, light |
| primary-80 | #b9e6fc | primary, pale |
| primary-95 | #eff9fe | primary, tint |
| neutral-05 | #141414 | text primary |
| neutral-40 | #5e5e5e | text secondary |
| neutral-60 | #989898 | text disabled |
| neutral-90 | #e6e6e6 | surface lower |
| neutral-95 | #f3f3f3 | surface low |
| white | #ffffff | surface default |
| accent | #ff9800 | accent (`--accent-color`) |
| error | #db4437 | danger |
| warning | #ffa600 | warning |
| success | #43a047 | success |
| info | #039be5 | info |

## Semantic roles
### Brand
| Role | Token |
|---|---|
| brand mark, hero accents | ha-blue |
| headings on light backgrounds | ha-black |
| body text on light backgrounds | ha-grey (see Contrast: fails AA for regular text on ha-white) |
| replaces pure black | ha-black |
| replaces pure white | ha-white |
| topic highlight | secondary palette |
| product or line identity | product colors |

Pure #000000 and #FFFFFF are for monochrome graphics only. Avoid HA Blue text on light backgrounds.

### Product UI
| Role | Token |
|---|---|
| primary action, links | primary-40 |
| brand mark, hero accents | primary-50 (confirm) |
| text primary | neutral-05 |
| text secondary | neutral-40 |
| surface default | white |
| surface low | neutral-95 |
| accent | accent |

## Light and dark
Brand: light is HA White background, HA Black headings, HA Grey body; dark is HA Black background with HA White and HA Blue for text. The source gives no dark-background body color for Home Assistant; HA Grey on HA Black fails for all uses.

Product UI: Dark mode surfaces: background #111111, card #1c1c1c; text primary #e1e1e1, secondary #9b9b9b (`--primary-background-color`, `--card-background-color` dark overrides). Semantic surfaces default to neutral-10 in dark mode.

## Contrast
### Brand pairings
The source's pass or fail per use (regular text 17 pt and below, large text 18 pt and above, graphic components) against the WCAG 2.x ratio computed from the hex values. The source's verdicts are board-approved and are the rule. Flagged rows fall below WCAG 2.x AA; where an output must meet WCAG (websites, docs, apps), do not use a flagged pairing for the uses it fails.

| Foreground | Background | Ratio | Source: regular / large / graphic | Note |
|---|---|---|---|---|
| ha-black | ha-white | 14.70:1 | pass / pass / pass | |
| ha-grey | ha-white | 4.30:1 | fail / pass / pass | Body text rule says HA Grey on light backgrounds; this pairing fails for regular text |
| ha-blue | ha-white | 2.01:1 | fail / pass / pass | Flag: below the 3:1 AA minimum for large text and graphics |
| ha-black | ha-blue | 7.33:1 | pass / pass / pass | |
| ha-grey | ha-blue | 2.15:1 | fail / fail / fail | |
| ha-white | ha-blue | 2.01:1 | fail / pass / pass | Flag: below 3:1 |
| ha-blue | ha-black | 7.33:1 | pass / pass / pass | |
| ha-grey | ha-black | 3.42:1 | fail / fail / fail | Source is stricter than AA for large text; follow the source |
| ha-white | ha-black | 14.70:1 | pass / pass / pass | |
| ha-black | ha-grey | 3.42:1 | fail / pass / pass | |
| ha-blue | ha-grey | 2.15:1 | fail / fail / fail | |
| ha-white | ha-grey | 4.30:1 | fail / pass / pass | |

No pairings are given for the secondary palette or product colors.

### Product UI pairings
Pairs for body text (ratios to confirm with a checker; listed pairs are the product defaults):
| Foreground | Background | Ratio |
|---|---|---|
| neutral-05 #141414 | white #ffffff | about 17:1 |
| neutral-40 #5e5e5e | white #ffffff | about 5.9:1 |
| #e1e1e1 | #111111 | about 14:1 |
| white | primary-40 #009ac7 | TODO check; borderline for small text |
