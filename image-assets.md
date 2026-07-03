# Image Assets

All images in the mock-up are **hotlinked from the live DTE WordPress media library** so the client sees a realistic page during review. Before production, swap to optimised, locally hosted, properly compressed versions (WebP, sized to display) — the page-speed crisis on the live site (Slide 5) partly stems from oversized media.

| Section | Element | Live URL |
|---|---|---|
| Hero | Background | `2023/09/20230215-Greentec-Quadsaw-Marathon-Man-Go-010-Resized-scaled.jpg` |
| Header / Footer | Logo (black), Logo (white) | `2022/08/DTE-logo.-black-_-yellow-png-cropped-v2.png` · `2018/12/DTE-logo_-white-_-yellow.-png-v2.png` |
| Machines | Flail mower | `2023/06/FR-92-Featured-image.png` |
| Machines | Forestry mulcher | `2023/06/FMR-NIUBO-Diamond-Mulcher-300x187.png` |
| Machines | Reach mower | `2023/09/Scorpion-630-FR-1903x840-1.webp` |
| Machines | Skid steer cutter | `2025/07/V70_Drum-Mulcher_Featured_800px.jpg` |
| Applications | Orchards | `2023/06/20230215-Greentec-Quadsaw-Marathon-Man-Go-032-Resized.jpg` |
| Applications | Municipality | `2022/09/Reach-Mower.jpg` |
| Applications | Forestry | `2023/08/Forestry_1_50_50_card_768x550-768x550.jpg.webp` |
| Applications | Agriculture | `2023/08/1692597721975.jpg` |
| Blog | 3 thumbnails | `2026/04/jack-evans-thumbnail1...` · `2026/01/compressed_image_under_1mb.jpg` · `2026/02/20230215-...-001-Resized-scaled.jpg` |

All paths are relative to `https://www.dte-equipment.com.au/wp-content/uploads/`.

**Exception — Partners logos**: the Greentec, Virnig and Niubo logos in the Market-Leading Partners section are locally hosted (client-supplied) at `images/greentec-logo.png`, `images/virnig-logo.jpeg` and `images/niubo-logo.jpeg`, not hotlinked, since no logo assets exist in the live WordPress media library.

## Production recommendations

1. **Compress and resize** every image to its actual display size; serve WebP with JPG fallback.
2. **Hero**: source a high-res landscape shot of a flagship machine working (reach mower or forestry mulcher) at ~1920px wide, under 250KB.
3. **Machine cards**: consistent aspect ratio (4:3), clean background, machine front-and-centre. The current mix of transparent PNGs and photos looks inconsistent at card size.
4. **Alt text**: descriptive and keyword-aware (e.g. "Greentec Scorpion reach mower cutting a roadside verge"), not the current filename-style alt.
5. Self-host all media (no hotlinking) once approved.
