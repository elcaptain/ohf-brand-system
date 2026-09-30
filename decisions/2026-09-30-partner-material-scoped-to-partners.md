---
date: 2026-09-30
area: standards
project: core
trigger: correction
change: Co-branding, product logos, packaging, photography and partner copy apply to commercial partners only
affected:
  - core/standards/partner-co-branding.md
  - core/standards/partner-product-logos.md
  - core/standards/partner-packaging.md
  - core/standards/partner-photography.md
  - projects/home-assistant/design/logo.md
  - projects/open-home-foundation/design/imagery.md
  - projects/home-assistant/design/imagery.md
  - projects/esphome/design/imagery.md
  - projects/music-assistant/design/imagery.md
  - INDEX.md
by: @elcaptain
---

# Partner material applies to partners only

## What happened
The partner guidelines v1.1 do two jobs. They contain the basic brand guidelines (logo, colour, typography), and they contain rules written for commercial partners. The first import treated the partner sections as general rules. The co-branding standard applied to every deck, landing page and README. The photography standard applied to every product page. Product logos sat in the Home Assistant logo file. @elcaptain clarified that product logos, co-branding, packaging, photography and written content are partner-specific.

## What changed
- The standards are renamed with a `partner-` prefix, and each states in its body that it applies only to partner material: `partner-co-branding`, `partner-packaging`, `partner-photography`.
- Product logos have moved out of `projects/home-assistant/design/logo.md` into a new `core/standards/partner-product-logos.md`.
- `applies_outputs` now lists only partner output types, for example `partner-packaging` and `partner-readme`. A skill building the foundation's own deck or README no longer loads them.
- Each project's `design/imagery.md` no longer adopts the partner photography rules as its own. The project photography section is a TODO again.
- `INDEX.md` gains one line saying when to load the partner standards.
- Written content was already partner-specific: the Partner copy section in each `marketing/partners.md`, whose status is described in `partner-co-branding.md`. It is unchanged.
- Logo, colour and typography stay general project rules in each `design/` directory.

## Left as is
- Home Assistant's product colours stay in `design/color.md`. They are palette tokens, and the partner packaging standard uses them.
- `brand/naming.md` in three projects still says "Conforms to the core co-branding standard". That line predates this import. It refers to attribution wording in general, not partner co-branding, and no such general standard exists. TODO for the core owner.
