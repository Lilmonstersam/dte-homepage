# Design Notes — DTE Homepage Redesign

Every section below ties back to a specific finding or priority in the SEO & CRO Strategy deck. The brief was: **keep the branding, fix the structure.**

## Branding fidelity

Sampled directly from the live site so the mock-up reads as "DTE", not a generic template.

| Token | Value | Source |
|---|---|---|
| Primary amber | `#F0A020` | Sampled from the live logo (the "gold nugget" brand colour) |
| Ink / near-black | `#1A1A1A` | Logo + nav |
| Theme background | `#F5F5F5` | Live `theme-color` meta |
| Display type | Plus Jakarta Sans, weight 800 (uppercase via CSS) | Confirmed as the live site's actual typeface (checked computed styles on dte-equipment.com.au: h1–h4, nav and body all render in Plus Jakarta Sans) |
| Body type | Plus Jakarta Sans, weight 400 | Matches live site exactly, was previously Inter as a placeholder — corrected in the July 2026 revision |
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

## Revision — July 2026 client feedback

Round of edits applied against client feedback on the first draft:

- **Typography**: swapped the placeholder Oswald + Inter pairing for **Plus Jakarta Sans**, confirmed via the live site's computed styles as the actual typeface in use (headings 800, nav/labels 700, body 400).
- **Header**: taller nav row (84px → 100px) and wider item gaps (28px → 40px) for breathing room; phone number restyled as a quiet secondary link so "Get a Quote" reads as the strongest CTA.
- **Hero**: eyebrow now larger, bolder and a lighter gold with a text-shadow for guaranteed contrast; overlay gradient darkened; paragraph gets a text-shadow safety net; content block pinned to a yellow left-rule (matching the Why DTE quote motif) so it reads as anchored rather than floating.
- **Shop by Application**: darkened the image overlay and added text-shadows so card copy stays legible regardless of the photo underneath.
- **Why DTE**: stats moved out of the right-hand grid and into the copy column (below the quote, above the CTA); the right column is now a supporting photo; more vertical space throughout.
- **Market-Leading Partners**: brand pills upgraded to full cards with a product photo, description and "View Range" link, replacing the plain text pills.
- **Quote/lead section**: background changed from a solid yellow block to a dark gradient (yellow now used only for the phone number, the accent left-rule and the primary button); added generous section and quote-box padding.
- **Latest From DTE**: "Read More" links now carry a permanent yellow underline so they read as links at rest, not just on hover.
- **Sitewide**: fixed the root cause of the cramped eyebrow/heading spacing — `.eyebrow` was an inline `<span>` so its margin was being ignored by the browser; it's now block-level with its own margin, which fixes the spacing everywhere the class is used.

## Revision — July 2026 differentiation pass

Applied after the client flagged that this mock-up read too closely to the Vortec Global mock-up (same agency, same page template):

- **Hero alignment**: fixed a flexbox bug where `.hero .wrap` had no explicit width — as a flex item it was shrinking to fit its content and then getting auto-margin-centred by the flex container, so the whole hero block sat centred on the page even though the copy inside was `text-align:left`. Added `width:100%` to `.hero .wrap`; content now anchors to the standard left-aligned page grid used everywhere else, matching the fix applied to the Vortec mock-up.
- **Priority Machine Lines → "Our Most In-Demand Machines"**: renamed the section heading (the internal-sounding "Priority" language read oddly to a buyer) and rebuilt the layout from a uniform 4-card grid (identical in structure to Vortec's product category grid) into a feature-plus-list layout — one large flagship panel (Flail Mowers, the highest-search-volume term per the strategy) alongside a compact stacked list for the other three lines.
- **Built For The Way You Work → "Smarter Ways To Work, By Application"**: the eyebrow, heading and paragraph were near-identical to Vortec's Applications section. Rewrote to tie into DTE's own established tagline ("Smarter Ways To Work", used in the Why DTE section) instead of generic buyer-pathway phrasing.
- **Market-Leading Partners imagery**: replaced the product-photo backgrounds on the Greentec/Virnig/Niubo pills with the actual brand logos (supplied by the client, now stored in `images/`), shown on a white contained tile rather than a full-bleed photo so they read as brand marks, not product shots.

## Revision — July 2026 brand-range correction

- **Niubo removed entirely** (no longer part of DTE's range, per client): brand mega-card, brand pill, finder brand card, drawer link, mega-menu Forestry/Excavator Mulcher items, footer link, hero lede and meta description. Brand sections now show Greentec and Virnig two-up (`.brand-row` and `.mega.simple` re-gridded to 2 columns). The `images/niubo-logo.jpeg` asset is orphaned and can be deleted. Site-side retirement work (301s, nav) added to `implementation-todo.md` item 2.
- **"Forestry Mulchers" pathway retargeted** from the Niubo tractor-mulchers category to `/product-category/virnig/skid-steer-drum-mulchers/` (Virnig V70 thumbnail), keeping the high-volume "forestry mulcher" keyword on the page. Excavator carrier card copy corrected to slashers/brush cutters (excavator mulchers were Niubo).
- **Flail mowers qualified as Greentec-only**: DTE supplies flail mowers exclusively from Greentec, so the flagship panel is now "Greentec Flail Mowers" with copy stating the range comes exclusively from Greentec; mega-menu, drawer, footer links and title/meta updated to match. Generic uses of "flail mowers" as a job description (e.g. the Agriculture application card) were left as-is, since they describe the work, not a multi-brand range.

## Revision — July 2026 advisory-positioning pass

Applied against client feedback: reduce clutter, simplify for mobile, and reposition DTE as a trusted advisory partner rather than an equipment supplier. The six messaging pillars from the feedback (application expertise; right solution not just right machine; productivity and commercial outcomes; reduced risk and downtime; long-term support and partnership; investment confidence) are now carried explicitly on the page.

- **Hero**: H1 changed to "The right solution, not just the right machine" (pillar 2, stated up front). Eyebrow now "Vegetation Management Specialists"; lede rewritten around telling us the job and being backed with setup, parts and after-sales support. Trust chips reworked to experience / after-sales support / exclusive distributor.
- **Why DTE**: heading now "A Partner In The Work, Not Just The Purchase". The four stat cards were removed (the numbers were already carried elsewhere on the page) and replaced with a plain six-point tick list mapping one-to-one to the six feedback pillars. Plain text list rather than icon cards, deliberately, to avoid template-y card clutter.
- **Testimonials + blog merged into one "Customer Success Stories" section**: the two sections were 80% redundant (two of three blog cards were the same case studies). Now a single section of three real case-study cards, each with an outcome tag, a pull quote and a link to the live story: Howard Meltzer / Yellingbo Olive Grove (2,000 trees pruned in ~10 days), Alf Pappalardo "Gold Nugget" mango pruning, and Jack Evans at Pinecliff Freedman Racing. The telehandler buyer guide and News hub are kept as a one-line footer link under the grid. Net effect: one fewer full section, stronger proof.
- **Lead band**: copy reframed around straight advice on solution, carrier match and return "before you spend a dollar"; Mick Andrew's after-sales quote (delivery, setup, follow-up call) added under the phone number as proof at the point of conversion.
- **Section intros** (machines, applications, brands, finder) each rewritten with one advisory line; the finder now carries a "Not sure where to start? Call…" prompt.
- **Mobile simplification**: finder cards stay two-across with subtitles hidden (halves scroll length instead of stacking 16 cards one-up); application cards and hero shortened; distributor line dropped from the top bar; brand logo tiles and quote box padding reduced; tighter section-head spacing.
- **Meta**: title and description updated to carry the advice/solution positioning alongside the machine keywords.

## Content-gap revisions (July 2026, live-site link audit)

Cross-checked every mock-up link against the live sitemaps (page, post, product_cat). Revisions made:

- **Machine Types mega-menu completed**: added the 8 live categories that were missing — Rotary Mowers (new Tiger series), Skid Steer Disc Mulchers, Excavator Slashers, Multi Carriers, Rotary Crushers, Weed Clearing Brushes, Ditch Cleaners and Grass Cutterbars — with live thumbnails. Rotary Mowers and Multi Carriers also added to the mobile drawer.
- **Niubo brand links corrected**: the brand mega-card, brand pill, finder card and drawer previously pointed at the tractor-mulchers subcategory; all now link to the existing `/product-category/niubo-mulchers/` parent.
- **Loader carrier placeholder**: no global loader landing page exists, so the Carriers mega-menu now shows Loader with a dashed "Page TBC" badge linking to `/products/` until the page is built (same convention as the Vortec mock-up).
- **Videos added to the footer** Company column — the live page exists in the nav but was dropped from the mock-up entirely.
