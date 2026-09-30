---
standard: product-photography
title: Product photography
scope: core
applies_outputs: [pack-shot, still-life-photo, campaign-photo, product-page]
conformance: none
owner: @liam
last_reviewed: 2026-09-30
review_every: 180d
status: active
source: Marketing and Product Guidelines for our commercial partners, v1.1 (August 2026), pp. 116-123. File Brand_Guidelines__V03-Aug26__1.pdf
---

# Product photography

Governs photographs of hardware products carrying an Open Home Foundation or project brand, whoever commissions them. Three formats, each with its own job: pack shots for marketplaces and shops, still life for the website and campaigns, campaign photography for products in real homes. Exists so images from different partners and shoots sit together without looking like different brands.

## Required elements
- Delivery as TIFF for all three formats.
- File names as `<project abbreviation> <product name>_<view name>`, for example `HA ZBT2_front view`. See the note under Rules on abbreviations.
- No props, text, or logos in pack shots or still life unless specifically requested.
- A cohesive look across an entire shoot.

## Rules

### Pack shots: nothing but the product
Pure white background (#FFFFFF). Diffused light with no harsh shadows, glare, or reflections. True-to-color. Same angle, distance, scale, and white balance across every product. Product centered and filling at least 85% of the frame.
- Yes: the device centered on #FFFFFF, soft even light, matching every other pack shot in the set.
- No: the device on a grey sweep with a hard shadow, shot slightly closer than the rest of the range.

Recommended shot list: front; back; bottom; isometric front-right; isometric back-left; close-ups of ports and labels; device being plugged in; device being unplugged; box closed, front-right view; box closed beside the device and its contents.

### Still life: retro-futuristic, technical, premium
Minimal and sharp. Colored light projections, lens reflections, soft gradients, and colored backdrops in both dark and light variants, using brand colors and the product's accent color. Soft three-point lighting with colored accent lights. Subtle shadows and reflections, for depth only. Product centered, filling at least 85% of the frame.
- Yes: the device on a dark backdrop with a Home Assistant blue rim light and a faint reflection.
- No: the device on a wooden table with a plant beside it (that is campaign photography, and props are not allowed here).

Recommended shot list: hero image x2; teaser image x2; front-right view; close-ups of ports and labels; close-up of the device being plugged in (for example into Home Assistant Green); close-up of the PCB or chip; family shot A (the whole line, for example Connect); family shot B (with other smart home devices); family shot C (all the packaging together).

### Campaign: the product belongs to the room
Real homes, real use cases, several rooms and kinds of people. Mostly soft, indirect daylight; no flash, no studio setups. No wide-angle lenses; use 3x zoom or equivalent, with a soft background blur that keeps context readable. Good contrast between product and background. Shoot every scene in both portrait and landscape. The product never dominates the frame. Human presence can be implied: a pushed-back chair, an open door, a figure entering the frame. Plan 6 to 10 shots.
- Yes: a sensor on a hallway shelf in morning light, the front door just opening, the product sharp and the room softly out of focus.
- No: a wide-angle shot of a styled kitchen with the product in the center under a flash.

For each campaign scene, define before the shoot: the room and setting, the feature or automation shown, mood, and light, and whether a person is present or implied.

### The file-name abbreviation is not public copy
The source's naming convention uses "HA" for Home Assistant. File names are internal. The rule that project names are never shortened (`projects/home-assistant/brand/naming.md`) still applies to every caption, alt text and piece of copy that ships with the image.
- Yes: file `HA ZBT2_front view.tiff`, alt text "Home Assistant Connect ZBT-2, front view".
- No: alt text "HA ZBT2 front".

## Never
- Other recognizable brands in campaign frames.
- Flash, harsh artificial light or studio setups in campaign photography.
- Props, text, or logos in pack shots or still life unless requested.
- Inconsistent angle, scale, or white balance within a pack-shot set.

## Machine checks
| Check | How | Fix |
|---|---|---|
| Format | file extension is .tif or .tiff | re-export as TIFF |
| File name | matches `<abbr> <product>_<view>` | rename |
| Pack-shot background | corner pixels are #FFFFFF | re-shoot or re-cut on pure white |
| Frame fill | product bounding box is at least 85% of the frame (pack shot, still life) | re-crop or re-shoot |
| Orientation pair | each campaign scene exists in portrait and landscape | shoot the missing orientation |
| Shortened names in captions | search captions and alt text for "HA", "MA" and other abbreviations | write the name in full |

## How skills use this
Skills that brief, review, or caption product imagery load this file and run its Machine checks in review. Each project's `design/imagery.md` points here for photography.
