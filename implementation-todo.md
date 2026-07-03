# DTE Homepage Redesign — Implementation To-Do

What is left to build/fix on dte-equipment.com.au before the new homepage can go live. Compiled July 2026 by cross-checking every mock-up link against the live site and sitemaps (page, post, product_cat). Mock-up-side gaps (missing categories in the mega-menu, wrong Niubo links, Loader placeholder, footer Videos link) have already been fixed in the mock-up, so this list is only the site-side work.

## 1. Missing / broken landing pages (blockers for the new navigation)

1. **Markets hub (`/markets/`).** The Applications nav parent and "View all markets →" link to it, and the live nav links it too, but it is absent from the page sitemap (likely a stub or noindexed). Build it as a proper applications hub. The live mega-menu's market descriptions literally say "Test" — placeholder copy is on the live site today.
2. **Niubo tractor and skid-steer mulcher categories.** `/product-category/niubo-mulchers/tractor-mulchers/` and `/skid-steer-mulchers/` are linked in the live nav but missing from the product_cat sitemap, which Yoast does when a category is empty or noindexed. The mock-up's headline "Forestry Mulchers" hub points at tractor-mulchers, so populate both categories with products and get them indexed.
3. **Carrier landing pages.** The new Carriers nav (tractor / excavator / skid steer / telehandler / loader) has no dedicated pages; the mock-up borrows brand categories and Loader has no destination at all (marked "Page TBC"). Market-by-carrier subcategories already exist (e.g. `/product-category/orchards/tractor/`, `/agriculture/loader-agriculture/` across all four markets, built Feb 2026) but nothing links to them — decide whether carrier hubs aggregate these or new global carrier pages are built.
4. **Thin market pages.** `/orchards/`, `/municipality/`, `/forestry/`, `/agriculture/` exist but are thin; the new homepage makes them primary pathways (nav, finder, application cards, footer), so they need proper hub content: intro copy, matched machine grids, case studies and quote CTAs.
5. **Videos page.** Linked in the live nav (and now the mock-up footer) but not in the page sitemap — verify it exists, has content and is indexable, or drop it.

## 2. Functional build (theme/CMS)

6. **Grouped mega-menus** (Machine Types 18 items, Applications, Carriers, Brands) replacing the current nested dropdown; keyboard- and touch-accessible. Current theme runs Slider Revolution + standard WP menus.
7. **Pathway Finder tabs, mobile drawer and scroll-aware sticky mobile CTA bar** — port from mock-up into the theme.
8. **Short segmented quote form.** Mock-up form is static (4 fields: name, phone, email, application). The live Gravity Forms quote form is 10+ fields — and its "What best describes your business?" dropdown is Vortec's list (Hydroseeding Contractor, Landfill, Cattle Farmers Growing Leucaena…), copy-pasted from the sister site. Rebuild with DTE-relevant segments (orchardist, council, forestry contractor, farmer, hire company…), wire to the form handler and add GA4/GTM conversion events (container GTM-W28LCV7) for form submissions and phone clicks.
9. **Hero slider replacement.** Live homepage runs three Slider Revolution slides; the mock-up uses a single static hero + finder. Confirm the slider plugin is retired on the new homepage (performance win) rather than rebuilt.

## 3. Content, hygiene and decisions

10. **Promo decision:** the live site has a "WIN a Polaris Ranger 500" banner above the header; the mock-up has no promo bar. Decide whether promos get a slot on the new homepage (text-based bar recommended).
11. **Claims sign-off:** "50+ years combined experience", "3 world-leading brand partners", "AgriTechnica 2019 innovation medal" (hero + Why DTE stats). Testimonials are real (taken from the live site) — no action needed there.
12. **Footer email:** live footer shows an email address; mock-up is phone-only. Decide in or out.
13. **LinkedIn link:** the live site links LinkedIn through an authwall redirect URL; use the clean `au.linkedin.com/company/dte-equipment` (already used in the mock-up).
14. **Taxonomy sprawl.** Product categories overlap three ways (brand: greentec/virnig/niubo; market: orchards/forestry/agriculture/municipality + carrier subcats; plus `/vegetation-management/`, `/other/`, legacy `/orchards/mowers/`, `/orchards/mulchers/`, `/orchards/canopy-management/`). Agree the canonical browse taxonomy and noindex/301 the rest so the new nav doesn't split ranking signals.
15. **Locale and metadata:** live `og:locale` is `en_US` — switch to `en_AU`; adopt the mock-up's keyword-aligned title tag and meta description (live title is brand-only). Single-H1 structure per the mock-up.
16. **Images:** mock-up hotlinks the WP media library and uses local brand-logo files (`images/`); production needs self-hosted, compressed WebP with srcset, and the brand logos loaded into the media library.

## Suggested build order

Phase 1 (unblocks nav): items 1–5, 14.
Phase 2 (homepage build): items 6–9, 16.
Phase 3 (content + decisions): items 10–13, 15.
