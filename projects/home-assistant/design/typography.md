---
area: design/typography
project: home-assistant
owner: Marketing Team
last_reviewed: 2026-09-30
review_every: 180d
draft: true
---

# Home Assistant: typography

Two sets, as in `color.md`. Brand type is from the Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 53 and 60-63, imported 2026-09-30. Product UI type is from the frontend theme tokens (https://github.com/home-assistant/frontend/blob/dev/src/resources/theme/typography.globals.ts). This settles the earlier open question: Roboto is the UI face, not the brand face.

## Families
### Brand: print, packaging, marketing collateral
| Role | Family | Fallback | Source |
|---|---|---|---|
| logotype, headings, body | Biotif | Figtree (headings), Instrument Sans (body) | https://www.fontspring.com/fonts/degarism-studio/biotif (licensed) |
| headings and secondary copy where Biotif is unavailable | Figtree | sans-serif | https://fonts.google.com/specimen/Figtree |
| body and tertiary copy where Biotif is unavailable | Instrument Sans at 99% width | sans-serif | https://fonts.google.com/specimen/Instrument+Sans |

Biotif is not used for user interfaces or website content; the source says it is not optimized for screens. Whether Figtree and Instrument Sans are therefore the marketing web faces, or whether home-assistant.io keeps its current type, is not stated. TODO: confirm.

### Product UI
| Role | Family | Fallback | Source |
|---|---|---|---|
| headings | Roboto (inherits body) | Noto, sans-serif | `--ha-font-family-heading` |
| body | Roboto | Noto, sans-serif | `--ha-font-family-body` |
| long-form | ui-sans-serif | system-ui, sans-serif | `--ha-font-family-longform` |
| code | monospace | | `--ha-font-family-code` |

## Scale
Brand: TODO; the source gives only the 17 pt / 18 pt boundary between regular and large text used in the contrast table.

Product UI: base sizes before the user scale factor: 10, 12, 14, 16, 20, 24, 28, 32, 40 px (`--ha-font-size-xs` to `-5xl`). Weights: light 300, normal 400, medium 500, bold 700. Headings bold, body normal, actions medium. Line heights: condensed 1.2, normal 1.6, expanded 2. Mirrored in tokens.json.

## Usage
- Headings in written content: sentence case (`brand/style.md`). The logotype is Title Case; that is a logo rule, not a heading rule.
- Biotif OpenType features on: ligatures, Stylistic Alternates sets 2 and 3 (curled "t" and single-storey curled "g").
- Instrument Sans at 99% width (`font-stretch: 99%` on the variable font).
- Brand headings in HA Black, body in HA Grey on light backgrounds (`color.md`; note the contrast flag there).
