# Design Notes — DTE Homepage Redesign

Every section below ties back to a specific finding or priority in the SEO & CRO Strategy deck. The brief was: **keep the branding, fix the structure.**

## Branding fidelity

Sampled directly from the live site so the mock-up reads as "DTE", not a generic template.

| Token | Value | Source |
|---|---|---|
| Primary amber | `#F0A020` | Sampled from the live logo (the "gold nugget" brand colour) |
| Ink / near-black | `#1A1A1A` | Logo + nav |
| Theme background | `#F5F5F5` | Live `theme-color` meta |
| Display type | Oswald (condensed, uppercase) | Matches the live site's heavy condensed headings |
| Body type | Inter | Clean neutral substitute for the live body face |
| Logo | Live black/yellow + white/yellow PNGs | Hotlinked from WordPress |

Em dashes avoided throughout the copy; British English spelling used (optimise, colour, organisation).

## Navigation & internal linking

**Primary nav = real site navigation with mega-menus.** The header parent tabs are Machine Types, Applications, Carriers and Brands, each opening a mega-menu in the same layout as the current site's Products mega-menu (thumbnail + label grid, with a "view all" footer). This replaces the section-anchor nav from v1. News, About and Contact sit alongside as standard links.

**All internal links point to real, live URLs.** Every machine/application/brand link in the nav, finder, cards and footer resolves to an existing page on dte-equipment.com.au (verified 200, indexed). Full inventory in `image-assets.md` is mirrored by the URL map below.

| Pathway | Real URL pattern used |
|---|---|
| Machine types | `/product-category/greentec/flail-mowers/`, `/boom-arms/`, `/quadsaws/`, `/cutterbars/`, `/barrier-mowers/`, `/rotary-hedge-cutters/`; `/product-category/niubo-mulchers/tractor-mulchers/`, `/excavator-mulchers/`; `/product-category/virnig/` + sub-categories |
| Applications | `/orchards/`, `/municipality/`, `/forestry/`, `/agriculture/`, `/markets/` |
| Brands | `/product-category/greentec/`, `/product-category/virnig/`, `/product-category/niubo-mulchers/tractor-mulchers/` |
| Carriers | No dedicated carrier pages exist yet → linked to the closest category and to `/products/` (which has carrier filter facets: Tractor, Excavator, Skid Steer, Telehandler, Loader). **Flagged as a build opportunity** — dedicated carrier landing pages would capture carrier-led searches. |

## Section-by-section rationale

**1. Hero — pathway-led, not brand-story-led**
The current hero leads with a rotating brand slogan. Buyers searching "flail mower" or "forestry mulcher" land and can't tell what DTE leads in. New hero states the categories plainly and pushes straight to "Find Your Machine" and a phone CTA. The background image now has a slow 20s zoom-in (Ken Burns) and the text content is left-aligned on desktop. Respects `prefers-reduced-motion`.
→ *Slide 2 priority #4 (rebuild homepage around buyer pathways); Slide 4 (homepage buyer pathways scored 8/15).*

**2. Pathway Finder — the core CRO addition**
A four-way tabbed finder: **By Application · By Machine Type · By Carrier · By Brand**. This is the single biggest structural fix. It mirrors exactly how the strategy says buyers shop and replaces the buried "find your product" search.
→ *Slide 6 medium-priority #1 (no clear navigation by application, machine type or carrier); Slide 2 priority #4.*

**3. Priority Machine Lines**
Surfaces the four build-target machine types directly on the homepage: **flail mowers, forestry mulchers, reach mowers, skid steer cutters**. These are the high-volume, near-zero-difficulty terms competitors win uncontested. Putting them on the homepage with their own hub links seeds the internal linking the new hubs will need.
→ *Slide 11 (build targets: flail mower 900, forestry mulcher 350, skid steer mulcher 150, reach mower); Slide 12 (machine-type hubs to create).*

**4. Applications**
Upgrades the four thin market pages (Orchards, Municipality, Forestry, Agriculture) into prominent intent cards. Keeps the existing market structure the client knows, but frames each as a buyer entry point.
→ *Slide 12 (application hubs: upgrade thin market pages into intent-rich landing pages).*

**5. Brands**
Greentec / Virnig / Niubo as a clean shop-by-brand strip. Supports the "by brand" pathway and reinforces the AU & NZ distributor positioning.
→ *Slide 9 (build authority by brand, all interlinked).*

**6. Why DTE + stats**
Condenses the existing About copy and pulls the real "Gold Nugget" customer quote. Trust signals (50+ years, AgriTechnica medal, AU&NZ) are now scannable stats rather than buried prose.

**7. Testimonials**
Real customer quotes from the current site, restyled as cards with star ratings for credibility at the decision stage.

**8. Lead band — phone-first**
The current site's only CTA is one 16-field form. This band leads with the **phone number as the primary action** (the strategy's stated highest-quality lead), backed by a short 4-field quote form. Form length cut from 16 fields to 4.
→ *Slide 6 medium-priority #2 (single long-form funnel, no phone-first prompt); Slide 13 KR (add a phone-first CTA).*

**9. Blog / resources**
Keeps the latest-posts pattern but reframes as "Resources & Buyer Guides", setting up the TAYA buyer-guide content from the strategy.
→ *Slide 12 (TAYA buyer guides).*

## Technical / on-page fixes baked in

- `lang="en-AU"` and `og:locale = en_AU` (fixes the sitewide en_US locale error — Slide 6 high-priority #2).
- Single `<h1>`, clean heading hierarchy (Slide 6 medium #3: multiple/missing H1s).
- Commercial, keyword-aligned title tag and meta description (Slides 5–6).
- Descriptive `alt` text on all images (Slide 6 high-priority #5: 299 images missing alt text).
- Lightweight: one HTML file, two web fonts, no page-builder bloat (Slide 5 #3: page-speed crisis from stacked builders/plugins).

## Deliberately out of scope for this mock-up

- Live links / functional forms (review prototype only).
- Product/Organisation **schema markup** — flagged as a separate deliverable (Slide 6 medium #5).
- The mega-menu product taxonomy (kept as simple nav here; the finder carries the load).
- Final production photography (see `image-assets.md`).
