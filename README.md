# DTE Equipment — Homepage Redesign Mock-up

Static HTML mock-up of a rebuilt DTE Equipment homepage, prepared by **Digilari** for client review as part of the Q1 SEO & CRO foundation engagement (June 2026).

**Live reference site:** https://www.dte-equipment.com.au/
**Source strategy:** `DTE-Equipment-SEO-CRO-Strategy.pptx` (slides 2, 4, 6, 9, 11, 12)

## What this is

A single-file HTML mock-up that keeps DTE's existing branding (black/yellow "gold nugget" palette, logo, Oswald-style display type) but restructures the homepage around **buyer pathways** instead of the current brand-story layout. It directly addresses the strategy's finding that the site is "structured for people who already know DTE, not for buyers searching by machine type."

This is a review prototype, not production code. Links are placeholders, the quote form is non-functional, and product images are hotlinked from the live WordPress media library so the client sees a realistic page immediately.

## Quick start

Open `index.html` in any browser. No build step, no dependencies (fonts load from Google Fonts CDN).

## Repo structure

```
homepage-redesign/
├── index.html          # the mock-up (self-contained: HTML + CSS + JS)
├── README.md           # this file
├── design-notes.md     # section-by-section rationale mapped to the strategy
├── image-assets.md     # every hotlinked image + recommended production swaps
└── .gitignore
```

## Key changes vs. the current homepage

| Current homepage | This mock-up | Strategy driver |
|---|---|---|
| Brand-story hero ("Orchard maintenance made easy") | Pathway hero (slow zoom bg, left-aligned) + "Find Your Machine" | Slide 6: homepage buyer pathways |
| Products-only mega-menu | **Mega-menus on Machine Types, Applications, Carriers, Brands** (same layout as current Products menu) | Slide 2 priority #4; slide 6 medium #1 |
| "Find your product" search buried | Prominent 4-way **Pathway Finder** (application / machine type / carrier / brand) | Slide 2 priority #4; slide 6 medium-priority |
| Products shown by market only | **Priority machine-line hubs** surfaced (flail, forestry mulcher, reach, skid steer) | Slide 11 build targets; slide 12 hubs |
| Single 16-field quote form as only CTA | **Phone-first CTA** + short 4-field quote form | Slide 6: phone-first lead capture |
| `og:locale = en_US` | `en_AU` + AU intent signals | Slide 6 high-priority: wrong locale |
| Generic page targeting | Commercial machine-type language in headings/meta | Slides 5, 9: keyword-to-page mapping |

All nav, finder, card and footer links point to **real, live URLs** on dte-equipment.com.au (verified 200/indexed). Carriers have no dedicated pages yet, so those links go to the closest category and the filterable `/products/` page — flagged in `design-notes.md` as a build opportunity.

## Deploying to GitHub

This folder is ready to push as its own repo (or as a subfolder). For client preview, GitHub Pages will serve `index.html` directly:

```bash
cd seo/homepage-redesign
git init && git add . && git commit -m "DTE homepage redesign mock-up v1"
# create repo on GitHub, then:
git remote add origin <repo-url>
git push -u origin main
# enable Pages: Settings → Pages → deploy from main / root
```

## Status

- [x] v1 mock-up matching brand + new structure
- [ ] Client review / feedback round
- [ ] Production images swapped (see `image-assets.md`)
- [ ] Schema markup (Organisation + Product) — separate deliverable
- [ ] Handoff to Lightning Sites for WordPress build
