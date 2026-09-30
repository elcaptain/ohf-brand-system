---
area: design/color
project: esphome
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
draft: false
---

# ESPHome: colour

Tokens are the source of truth in tokens.json; this file explains them. Source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 80-87, file `Brand_Guidelines__V03-Aug26__1.pdf`. Imported 2026-09-30. The source is signed off by the board (`decisions/2026-09-30-import-partner-guidelines-v1-1.md`).

The source: "The color palette for ESPHome is the same as for Home Assistant", except that ESPHome has no secondary palette. Use only the four colors below. Values, print references, and the pairing table live in `projects/home-assistant/design/color.md`, Brand sections; they are repeated here only as tokens so a build can load one file.

## Palette
| Token | Value | Name |
|---|---|---|
| ha-blue | #18BCF2 | HA Blue (brand blue) |
| ha-black | #1D2126 | HA Black |
| ha-grey | #6E7191 | HA Grey |
| ha-white | #F2F4F9 | HA White |

No secondary palette. No product colors are defined for ESPHome.

## Semantic roles
| Role | Token |
|---|---|
| brand mark, hero accents | ha-blue |
| headings on light backgrounds | ha-black |
| body text on light backgrounds | ha-grey (fails AA for regular text on ha-white; see the Home Assistant contrast table) |
| background, light | ha-white |
| background, dark | ha-black |

Pure black and white for monochrome graphics only.

## Light and dark
As in `projects/home-assistant/design/color.md`, Brand.

## Contrast
Use the Brand pairings table in `projects/home-assistant/design/color.md`. It applies unchanged.
