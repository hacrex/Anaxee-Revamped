# Anaxee.com — Logo & Color Scheme Audit

*Compiled from anaxee.com's live markup, linked assets, and cross-referenced blog/CTA assets. Where a value is directly confirmed in code, it's marked **Confirmed**. Where it's inferred from consistent visual patterns across pages/blog banners but not pulled from raw CSS, it's marked **Inferred**.*

## 1. Logo

- **Primary logo file:** `anaxee.com/wp-content/uploads/2019/10/B_logo.png` — used in the site header, linked to the homepage. Filename suggests a stylized **"B" mark** (likely a legacy/short-form icon rather than a full wordmark), dating to the original 2019 site build.
- **Favicon / tile icon:** `anaxee.com/wp-content/uploads/2021/11/cropped-ezgif.com-resize1-270x270.png` — set as the `msapplication-TileImage`, meaning the favicon was produced by cropping/resizing an existing asset (an ezgif export) rather than being purpose-built at the right dimensions. This is a small but telling sign of ad hoc asset management.
- **Social share image (OG image):** `anaxee.com/wp-content/uploads/2021/12/facebook_cover-e1640778692541.png` (713×280) — used for Facebook/Twitter link previews.
- **Blog logo:** blog.anaxee.com uses a **separate, newer logo file** (`cropped-Anaxee-Blog-new-logo-PNG.png`, uploaded 2026), distinct from the corporate site's header logo — another concrete instance of brand-asset drift between the two properties.
- **Recurring visual motif (Inferred):** Blog banner graphics and press assets consistently place the Anaxee logo over a **teal/blue textured background**, often paired with green map-of-India or eco-iconography (tree, wind turbine, CO₂ symbol) for climate content — suggesting an established but informally-applied secondary palette for climate/carbon storytelling.

## 2. Color Scheme

| Color | Value | Status | Where it shows up |
|---|---|---|---|
| **Brand cyan/teal** | `#54c5d0` | **Confirmed** | Set as the `theme-color` meta tag on blog.anaxee.com (controls mobile browser chrome color) |
| **Cyan (CTA accent)** | referenced as `cyan` | **Confirmed** | The homepage's "Join as Digital Runner" button links to an Airtable embed with `backgroundColor=cyan` explicitly set in the URL — cyan is being used as the primary action-button color |
| **Deep blue / navy** | not pulled as hex | **Inferred** | Recurring "blue textured background" and "teal-blue skyline" description across blog banner graphics; likely a darker navy/blue used as a background or secondary brand color alongside the lighter cyan |
| **Green** | not pulled as hex | **Inferred** | Climate/carbon content banners consistently use green (map of India, tree silhouettes, eco icons) — functioning as an unofficial "climate vertical" color, not part of the core UI palette |
| **Black/white base** | — | **Inferred** | Homepage assets include a black India map graphic (`map-india-black.jpg`) and standard black text on white background for body copy — a neutral, unremarkable base palette typical of a stock WordPress theme |

### Reading on the palette
The confirmed data points (`#54c5d0` teal and the explicit `cyan` CTA parameter) indicate Anaxee's actual brand color is a **cyan/teal**, not a generic "corporate blue." However, this doesn't appear to be applied as a disciplined system — it shows up as a theme-color meta tag and a button background choice rather than as a defined, documented palette carried consistently across headers, links, icons, and hover states. The green used in climate content and the deeper blue used in banner backgrounds appear to be organic, per-asset choices rather than named palette tokens.

## 3. What this means for the redesign

- **There is a real, usable brand color already** (`#54c5d0` cyan/teal) — the new design system shouldn't invent a new primary color from scratch; it should formalize this one (define tints/shades, accessible text-contrast pairings, hover states) rather than replace it.
- **The logo itself is due for review.** A single-letter "B" mark from 2019, a cropped/resized favicon, and a completely different blog logo are three inconsistent signals for one company. Given Anaxee's repositioning as "India's Reach Engine" across Retail, Climate, Data, AI, Carbon, and Influence Marketing, this is a good moment to commission (or formalize) a single primary logo — full wordmark + icon mark — with proper export sizes (favicon, social cards, app icon) generated at build time rather than cropped ad hoc.
- **No accessible source-of-truth exists.** There's no visible brand guideline, style tile, or design-token file backing any of this — colors and logos are living inside scattered image uploads and inline theme CSS. Recommend the redesign project starts with a one-page brand sheet (logo usage, primary/secondary/accent colors with hex + accessibility-checked pairings, typography) before any component build begins.

## 4. Suggested next step

I don't have direct file-system/CSS access to anaxee.com's stylesheet (only rendered content), so the hex values above beyond the confirmed `#54c5d0` are best-effort inference from visual patterns, not extracted from source. For pixel-accurate colors (exact hex of the logo mark, link colors, hover states, button gradients), the fastest path is either:
1. Someone with site access exporting the theme's CSS/`style.css` file, or
2. A quick screenshot-based color-pick pass once I can view the rendered logo image directly.

Happy to do a deeper pass if you can share the logo file directly or grant access to the WordPress theme files.
