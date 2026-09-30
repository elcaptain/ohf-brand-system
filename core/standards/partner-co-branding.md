---
standard: partner-co-branding
title: Co-branding with commercial partners
scope: core
applies_outputs: [partner-packaging, partner-co-branded-asset, partner-announcement, partner-page, partner-deck, partner-landing-page, partner-readme]
conformance: none
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
status: active
source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 4-5, 101-104, 124-127. File Brand_Guidelines__V03-Aug26__1.pdf
---

# Co-branding with commercial partners

Governs every output that puts a commercial partner's logo, name, or copy next to the Open Home Foundation or one of its projects: packaging, product pages, launch assets, decks, GitHub repositories. Exists so partner material gets through approval without rework, and so a partner mark never outweighs, crowds, or impersonates ours. The failure it prevents is the most common one in the source document: a co-branded asset that is sent back because the logos are mismatched in format or scale.

Partner-specific: applies only to material a commercial partner of the Open Home Foundation makes or co-brands with us. The Open Home Foundation's and the projects' own material follows each project's `design/` and `brand/` files, not this standard. Related partner standards: `core/standards/partner-product-logos.md`, `core/standards/partner-packaging.md`, `core/standards/partner-photography.md`.

## Required elements
- Final approval from the Open Home Foundation before anything carrying our branding is published or printed. Route per `core/escalation.md` (partnership terms go to leadership). Contact: partner@openhomefoundation.org (`core/escalation.md`, Contacts).
- Our logos taken only from the brand assets repository, never redrawn or screenshotted: https://github.com/OpenHomeFoundation/brand-assets. One directory per brand (`open-home-foundation/`, `home-assistant/`, `esphome/`, `music-assistant/`), each with `logo/print/` (CMYK EPS and PDF) and `logo/screen/` (PNG and SVG), split into `lockup/<variant>/` and `logomark/`. File names follow `<brand>-<type>-<variant>-<theme>-<background>.<ext>`, for example `HA-lockup-main-color-on-light.svg`. Each project's `design/logo.md` lists its paths. The repository is the source of truth for logo and badge files; the Google Drive folder the partner guidelines v1.1 name is not used. No project has a wordmark: the logotype never appears without the logomark.
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
The "A commercial partner of the Open Home Foundation" badge carries our identity by itself. Use it mainly in GitHub repositories, and also on websites or marketing material where it serves a clear purpose. Do not add the Open Home Foundation logo next to it. Badge files: `open-home-foundation/badge/` in the brand assets repository (https://github.com/OpenHomeFoundation/brand-assets/tree/main/open-home-foundation/badge), `ohf-badge-commercialpartner.svg` and `.png`. There is one variant, for every background; the three background variants the source describes do not exist. This badge is not the "Works with Home Assistant" mark, which is not in the repository.
- Yes: the badge alone in the README of the partner's repository.
- No: the badge plus the Open Home Foundation logo in the same README header.

### The badge ends when the partnership ends
A partner may use the badge only while the partnership is active.
- Yes: badge removed from the repository and site when the agreement lapses.
- No: badge kept on an archived product page after the partnership ended.

## Never
- The commercial partner badge on product packaging. Packaging follows `core/standards/partner-packaging.md`.
- Any alteration of the badge: proportions, stretch, rotation, distortion, color.
- A partner logo inside our logo's clear space.
- Logos redrawn, recolored, or outlined (see each project's `design/logo.md`, Misuse).
- Publishing before Open Home Foundation approval.

## Machine checks
| Check | How | Fix |
|---|---|---|
| Like-for-like pairing | list the component used for each logo in the asset (mark or lockup); they must match | swap to the matching component |
| Clear space | measure the gap between logos against the logotype or logomark height | widen the gap to at least that height |
| Badge on packaging | output type is `packaging` and the badge file appears | remove the badge; follow the packaging standard |
| Badge plus logo | badge file and an Open Home Foundation logo file both present | remove the logo |
| Asset source | logo and badge files come from the brand assets repository | replace with official files |
| Banned words in partner copy | list in `core` and the validator | the specific thing |

## Project partner pages
Each project's `marketing/partners.md` points here for who may use the brand and how partner logos appear. Its own content is one section, Partner copy: what the partner guidelines (pp. 124-127) tell partners about writing for that voice. That section is a summary handed to partners, not a rule set. The project's `brand/voice.md`, `brand/style.md` and `brand/messaging.md` govern, and where the summary disagrees with them, they win. It is paraphrased, because the source's own wording contains words the validator bans (`decisions/2026-09-30-import-partner-guidelines-v1-1.md`).

## How skills use this
Skills whose output type is in `applies_outputs` load this file in their "Context to load" step and run Machine checks and Required elements in their review step. No skill needs editing when this standard changes.
