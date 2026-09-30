---
standard: co-branding
title: Co-branding with commercial partners
scope: core
applies_outputs: [packaging, co-branded-asset, partner-announcement, partner-page, deck, landing-page, github-readme]
conformance: none
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
status: active
source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 4-5, 101-104, 124-127. File Brand_Guidelines__V03-Aug26__1.pdf
---

# Co-branding with commercial partners

Governs every output that puts a commercial partner's logo, name, or copy next to the Open Home Foundation or one of its projects: packaging, product pages, launch assets, decks, GitHub repositories. Exists so partner material gets through approval without rework, and so a partner mark never outweighs, crowds, or impersonates ours. The failure it prevents is the most common one in the source document: a co-branded asset that is sent back because the logos are mismatched in format or scale.

## Required elements
- Final approval from the Open Home Foundation before anything carrying our branding is published or printed. Route per `core/escalation.md` (partnership terms go to leadership). Contact: brand@openhomefoundation.org.
- Our logos taken only from the brand assets repository, never redrawn or screenshotted: https://github.com/OpenHomeFoundation/brand-assets. One directory per brand (`open-home-foundation/`, `home-assistant/`, `esphome/`, `music-assistant/`), each with `logo/print/` (CMYK EPS and PDF) and `logo/screen/` (PNG and SVG), split into `lockup/<variant>/` and `logomark/`. File names follow `<brand>-<type>-<variant>-<theme>-<background>.<ext>`, for example `HA-lockup-main-color-on-light.svg`. Each project's `design/logo.md` lists its paths. The partner guidelines v1.1 name a Google Drive folder instead (https://drive.google.com/drive/folders/1zalvN7zf8SIVo_yH0BUiADq7YJT08Fve); the repository is the location to use.
- Each project's logo rules as written in `projects/<slug>/design/logo.md`.
- Clear space around each logo in the pairing of at least the height of the logotype or logomark.
- Like paired with like: logomark with logomark, full lockup with full lockup.
- Written copy that follows the project's `brand/voice.md` and uses boilerplate from `brand/messaging.md` verbatim. The project-level summary for partners is in `projects/<slug>/marketing/partners.md`.

## Rules

### Pair like with like
When our logo sits next to a partner logo, use the same component on both sides, on every surface in the set. Because a full lockup next to a bare mark reads as a hierarchy we did not agree to.
- Yes: Home Assistant main lockup beside the partner's full wordmark lockup; Home Assistant logomark beside the partner's symbol.
- No: Home Assistant logomark beside the partner's full wordmark lockup.

### Balance optically, not mathematically
Size the two logos so they look equal in both width and height and center them optically. If logos of similar scale still look unbalanced, reduce the heavier one. Because two marks with the same bounding box rarely carry the same visual weight.
- Yes: the denser partner mark scaled down until both read as equals.
- No: both logos set to the same pixel height regardless of shape.

### Use the badge instead of our logo where the badge fits
The "A commercial partner of the Open Home Foundation" badge carries our identity by itself. Use it mainly in GitHub repositories, and also on websites or marketing material where it serves a clear purpose. Do not add the Open Home Foundation logo next to it. Badge files: https://github.com/OpenHomeFoundation/openhomefoundation.org/tree/main/badges
- Yes: the badge alone in the README of the partner's repository.
- No: the badge plus the Open Home Foundation logo in the same README header.

### Pick the badge variant by background
Three variants exist. Use the one without a background on light or dark surfaces where its colors contrast, or when it sits among other badges without backgrounds. Use the light grey background version when the background cannot be predicted or controlled, such as a patterned image or a low-contrast surface. The source names only these two; the third variant is not described.
- Yes: light grey background version over a lifestyle photo.
- No: the transparent version over a busy product photo.

### The badge ends when the partnership ends
A partner may use the badge only while the partnership is active.
- Yes: badge removed from the repository and site when the agreement lapses.
- No: badge kept on an archived product page after the partnership ended.

## Never
- The commercial partner badge on product packaging. Packaging follows `core/standards/product-packaging.md`.
- Any alteration of the badge: proportions, stretch, rotation, distortion, color.
- A partner logo inside our logo's clear space.
- Logos redrawn, recolored, or outlined (see each project's `design/logo.md`, Misuse).
- Publishing before Open Home Foundation approval.

## Machine checks
| Check | How | Fix |
|---|---|---|
| Like-for-like pairing | list the component used for each logo in the asset (mark, lockup, wordmark); they must match | swap to the matching component |
| Clear space | measure the gap between logos against the logotype or logomark height | widen the gap to at least that height |
| Badge on packaging | output type is `packaging` and the badge file appears | remove the badge; follow the packaging standard |
| Badge plus logo | badge file and an Open Home Foundation logo file both present | remove the logo |
| Asset source | logo files come from the brand assets repository, badges from the badges repository | replace with official files |
| Banned words in partner copy | list in `core` and the validator | the specific thing |

## Project partner pages
Each project's `marketing/partners.md` points here for who may use the brand and how partner logos appear. Its own content is one section, Partner copy: what the partner guidelines (pp. 124-127) tell partners about writing for that voice. That section is a summary handed to partners, not a rule set. The project's `brand/voice.md`, `brand/style.md` and `brand/messaging.md` govern, and where the summary disagrees with them, they win. It is paraphrased, because the source's own wording contains words the validator bans (`decisions/2026-09-30-import-partner-guidelines-v1-1.md`).

## How skills use this
Skills whose output type is in `applies_outputs` load this file in their "Context to load" step and run Machine checks and Required elements in their review step. No skill needs editing when this standard changes.
