# Anaxee Digital Properties: Current-State Audit & Consolidation Strategy

## 1. What I found on each property

### anaxee.com (Corporate site — WordPress)
- Positioning is stuck in the "last-mile network / data collection" era: hero message is "MAKE IMPACTFUL DECISIONS WITH MILLIONS OF DATA POINTS," nav is Home / About / Project Swaraksha / Climate / Services / Platform / Runner / Blog / Career / Students.
- Homepage still leans on the Runner-network story (40,000+ Digital Runners, 430 districts, 26 states, 11,000+ pincodes) and 2019–2022-era WordPress theme assets (`/wp-content/themes/Anaxee/images/...`).
- No visible mention of AI Data Services, Influence Marketing/Prabhavak, or the newer Carbon/Climate depth that the blog now carries — Climate appears as one nav item, not a full vertical.
- "Raise Business Enquiry" and "Join as Digital Runner" CTAs point to **Airtable embeds**, not a native lead-capture flow — this is a credibility and conversion-tracking gap for enterprise/government buyers.
- Blog preview on the homepage is pulling from **anaxee.com/blog/**, which is a *separate* WordPress instance from blog.anaxee.com — i.e., there appear to be two blog systems in play already.
- CTA phone numbers and generic "Info/HR/Sales" contact structure feel like an SMB, not an enterprise vendor to Retail/Climate/Government stakeholders.

### blog.anaxee.com (Blog — WordPress)
- Actually the **most current and strategically advanced asset** in the portfolio. Recent content (Sept 2026) is squarely aligned with the pitch: carbon credit strategy, biochar, dMRV, CBAM, AI training data / physical AI / ground-truth data, retail intelligence, and even a piece explicitly comparing Prabhavak to political-style local-influence networks.
- This blog is *ahead* of the corporate site's narrative — it's already selling Anaxee as a Climate + AI Data + Retail Intelligence + Influence company. The corporate homepage hasn't caught up to its own blog.
- Visually distinct theme/logo from anaxee.com, separate categories taxonomy, own CTA block ("Get Started" → same Airtable form). Functions as an isolated content silo rather than a driver of site-wide SEO equity.

### prabhavak.anaxee.com (Next.js + Tailwind)
- This is not a B2B marketing page — it's a **consumer acquisition funnel** for recruiting "Prabhavaks" (professionals monetizing influence), with a ₹299 paid signup, testimonials, FAQ objection-handling, and a hard-sell structure ("first 500 users," urgency, a ₹2,000 "free" kit).
- Tone, visual language, and even the underlying business model (consumer funnel vs. enterprise credibility site) are fundamentally different from anaxee.com and the blog. This is the most jarring brand discontinuity in the portfolio — a first-time visitor bouncing between anaxee.com and prabhavak.anaxee.com would struggle to tell it's the same company.
- Technically it's the newest and best-built property (modern stack, clean conversion design) — but it's an **acquisition/product microsite**, not a "showcase this vertical to enterprise buyers" page.

### anaxeetech.com
- Built on **Lovable** (AI app builder) — a client-side rendered app with generic scaffolding metadata still in place (title is a literal UUID: `7ad8ab8d-eb2a-4173-8c2b-03114882df04`, OG image is Lovable's own branding). Meta description: "Empowering brands with last-mile outreach and driving sustainable action through carbon projects across Bharat."
- This reads as an **unfinished or abandoned prototype** — possibly a newer attempt at repositioning ("Reach & Climate Solutions") that never got finished or promoted. It's a fourth, uncoordinated entry point into the Anaxee brand, on a fourth domain, on a fourth stack.
- This alone is a strong argument for consolidation: you have four domains, three tech stacks (WordPress ×2 instances, Next.js, Lovable/React), and at least three distinct visual identities live simultaneously today.

## 2. Cross-cutting findings

| Issue | Evidence |
|---|---|
| **Brand fragmentation** | 4 domains, 3+ tech stacks, no shared design system, no shared header/footer/nav pattern |
| **Narrative lag** | Corporate homepage markets 2019–2021 Anaxee (Runner network, rural reach); blog markets 2026 Anaxee (Carbon, AI data, Retail Intelligence, Influence). The blog has outrun the site that's supposed to represent the company. |
| **Two blogs, one brand** | anaxee.com/blog/ and blog.anaxee.com appear to be different WordPress instances with different themes |
| **Lead capture via third-party forms** | Primary "Raise Business Enquiry" and "Join as Digital Runner" CTAs route to Airtable — fine for MVP speed, weak for enterprise trust, CRM integration, and analytics/attribution |
| **No unified vertical structure** | Retail, Climate, Data Collection, AI Data Services, Carbon Projects, and Influence Marketing (Prabhavak) are not presented as six coherent business lines anywhere — each lives on a different property or nav item with different depth |
| **Consumer vs. enterprise tone collision** | Prabhavak's paid-funnel, urgency-driven consumer tone sits directly adjacent (subdomain) to a B2B/B2G-facing corporate identity |
| **Orphaned/prototype property** | anaxeetech.com appears unfinished, undermines credibility if a prospect or investor stumbles on it |
| **SEO equity split across properties** | Backlinks, domain authority, and topical authority (especially on Carbon/Climate, where blog.anaxee.com has real depth) are split across anaxee.com and blog.anaxee.com instead of compounding on one domain |

## 3. Implications for the proposal

Your proposal is directionally right, and the audit actually **strengthens the case** beyond what's in the brief — this isn't just "the design looks dated," it's "there are four different companies visible on four different URLs today." A few things I'd sharpen or add:

**a. This is a content/IA consolidation problem as much as a design problem.**
blog.anaxee.com already contains most of the substance you want the new site to communicate (Carbon/Climate depth, AI Data Services, retail intelligence, even Prabhavak positioning). The unified site's job is less "write new content" and more "restructure, re-home, and elevate existing content" under one IA — that changes scope/timeline for the better.

**b. Prabhavak needs a deliberate integration decision, not just a merge.**
Because its business model (consumer-facing paid funnel) is fundamentally different from the B2B/B2G marketing site, you have three real options and should decide explicitly rather than default:
1. Prabhavak gets a **B2B-toned overview page** on the unified site (for investors/partners/brands to understand the vertical) while keeping its **own high-converting funnel subdomain** for consumer signup (like a landing page ≠ marketing site pattern most consumer-facing product lines use).
2. Fully absorb Prabhavak's marketing into the unified design system but preserve the funnel mechanics (form, pricing, urgency) as a distinct page template.
3. Keep Prabhavak fully separate and only cross-link — lowest effort, but doesn't achieve "single unified experience."
Recommendation: **Option 1.** Don't force a consumer acquisition funnel into an enterprise IA — link it as "Anaxee Prabhavak — Influence Marketing Network" from the unified site's vertical page, with its own conversion-optimized subdomain retained.

**c. anaxeetech.com should likely be retired/redirected**, not merged — it doesn't appear to carry unique content, traffic, or backlink value worth preserving; carrying it forward adds a fourth surface to maintain for no clear benefit. Worth a quick check of its analytics/backlinks before killing it, but default should be 301 redirect to the new domain once live.

**d. Recommend consolidating onto a single domain (anaxee.com) rather than the current archipelago**, with blog content migrated in as `/blog` or `/insights` on that domain — folding blog.anaxee.com's strong recent content into the main domain is likely your single biggest quick-win for SEO/GEO, since it stops splitting domain authority and puts the Climate/Carbon/AI-data thought leadership under the same roof as the vertical pages that should convert on it.

## 4. Suggested technical direction

Given Prabhavak is already on Next.js + Tailwind and is your best-built property:
- **Standardize the unified site on Next.js + Tailwind** (or a headless-CMS-backed Next.js build), retiring the WordPress instances for the corporate site and migrating blog content via WordPress's REST/export API rather than manual copy.
- Use a **headless CMS** (Sanity, Contentful, or WordPress-as-headless-only) so the blog/insights section stays easy for non-technical content writers to publish into, without dragging the whole frontend back onto WordPress theming.
- Build the **design system first** (tokens, type scale, component library) before any page work — this is what actually prevents "yet another disconnected microsite" next time a new product launches (e.g., whatever comes after Prabhavak).
- Structured data / schema markup (Organization, Article, FAQPage, Service) from day one — directly supports the GEO/AI-search-visibility goal, since LLM-based answer engines lean heavily on structured, well-labeled content over crawled prose.

## 5. Suggested IA (six verticals + audiences, not either/or)

Rather than choosing between "organize by vertical" (Retail, Climate, Data, AI, Carbon, Influence) and "organize by audience" (Enterprise, Climate Orgs, Brands, NGOs, Government), use verticals as the primary nav and audience-tailored entry paths as homepage/landing-page routing — most B2B/B2G sites with multiple buyer types do this via a homepage "Who are you here as?" module rather than a duplicate parallel nav, which avoids doubling the IA.

## 6. Suggested phased approach

| Phase | Focus |
|---|---|
| 1. Discovery & content audit | Full inventory of all posts/pages across both blogs + anaxee.com + anaxeetech.com; decide what migrates, redirects, or retires; finalize IA and domain strategy |
| 2. Design system & brand | Unified visual identity, component library, voice/tone guide that can flex between enterprise credibility (main site) and conversion urgency (Prabhavak funnel) |
| 3. Build core site | Home, six vertical pages, about, case studies/impact, careers, contact — Next.js on unified domain |
| 4. Content migration + redirects | Move blog.anaxee.com content in, 301-map every old URL (both blogs, anaxeetech.com) to new URLs to preserve SEO equity |
| 5. Prabhavak integration | Build the B2B overview page in the new system; keep/refresh the funnel subdomain separately with shared visual DNA |
| 6. Launch, monitor, iterate | Search Console/analytics reconnection, monitor rankings through the domain consolidation (expect temporary volatility), then iterate on conversion data |

If useful, I can turn this into a slide deck or a formal Word document version of this analysis for internal circulation — happy to build either.
