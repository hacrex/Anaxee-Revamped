# Anaxee Platform — UI/UX Direction

## Purpose

This is the recommended UI/UX direction for the unified `anaxee.com` platform. It turns the project brief into a practical experience strategy: help an enterprise, climate, government, or brand buyer understand **what Anaxee does, why its reach is credible, and what to do next** within the first visit.

It is based on the repository's current-state audit of `anaxee.com`, `blog.anaxee.com`, `prabhavak.anaxee.com`, and `anaxeetech.com`; the live-site colour and logo audit; the PRD; sitemap; content strategy; and design system. The live properties could not be re-fetched during this review because outbound HTTP access was denied by the execution environment. The colour recommendations therefore preserve the audit's confirmed `#54C5D0` teal rather than treating an unverified screenshot sample as a source of truth.

## Executive recommendation

Create a **calm, data-led, India-rooted enterprise experience**—not a generic SaaS landing page and not a consumer-growth funnel. The visual system should feel like a reliable national operating layer: dark ink for trust, the existing Anaxee teal for identity and motion, restrained blue for interactive data, and vertical accents used only as wayfinding.

The homepage should tell one progressive story:

1. **Reach:** Anaxee can act anywhere in India.
2. **Proof:** The network and data systems make that claim credible.
3. **Relevance:** Buyers can see their solution, industry, and evidence.
4. **Action:** They can request a conversation without leaving the site or deciphering an external form.

Keep Prabhavak's consumer acquisition flow separate from this B2B/B2G journey. Give it shared branding and a product overview on the main site, but preserve its specialized signup conversion path on its subdomain.

## What the audit implies

| Property | Current role | UX implication for the new platform |
| --- | --- | --- |
| `anaxee.com` | Legacy corporate and Digital Runner narrative | Replace text-heavy, service-led discovery with clear solution and evidence paths. |
| `blog.anaxee.com` | Most current Climate, AI-data, retail, and influence thought leadership | Migrate into `anaxee.com/resources/` and expose it through solution pages, not a disconnected chronological archive. |
| `prabhavak.anaxee.com` | Consumer recruitment and paid signup funnel | Present a B2B product story on `anaxee.com/products/prabhavak/`; retain the optimized acquisition flow separately. |
| `anaxeetech.com` | Incomplete prototype | Retire with a mapped 301 redirect after validating traffic and backlinks. |

Do not reproduce the present fragmentation in the redesign. A visitor should always see the same logo, global navigation, type scale, interaction states, footer, and contact pattern regardless of entry page.

## Audience and jobs to be done

Use one primary navigation organized by **solution**, with homepage routes that help visitors self-identify by need. Do not create duplicate audience-specific site trees.

| Visitor | They need to establish | Primary path | Conversion |
| --- | --- | --- | --- |
| Enterprise / brand buyer | Scale, commercial relevance, and measurable outcomes | Solution → industry → case study | Request a consultation |
| Climate organization | MRV credibility, field verification, and project fit | Climate & Carbon → product → proof | Discuss a project |
| Government / NGO | Coverage, accountability, and implementation capability | Industry → network → impact | Start a program conversation |
| Research/content visitor | A clear answer plus evidence | Insight/blog → related solution → case study | Subscribe or contact |
| Prospective Digital Runner / Prabhavak | A distinct participation journey | Network or Prabhavak overview → dedicated flow | Join the network |

## Information architecture and navigation

### Desktop navigation

Use the existing planned structure, but make the mega menus useful decision aids rather than link dumps:

`Solutions` · `Products` · `Industries` · `Case Studies` · `Resources` · `Company` · **Talk to an expert**

Each mega menu should include:

- 4–6 clearly named destinations with a one-line outcome, not only a label.
- One featured proof link (for example, a relevant case study or report).
- A stable layout, keyboard navigation, escape-to-close behavior, and visible focus.
- No hover-only dependency: open on click/Enter and keep the trigger state clear.

Make **Talk to an expert** the single global B2B CTA. Use contextual labels within pages—“Discuss retail visibility,” “Plan a carbon project,” “See the platform”—so the action reflects the visitor's task without proliferating competing CTAs.

### Mobile navigation

Use a full-height, scrollable sheet with accordion groups, search, and the primary CTA pinned at the bottom. Keep targets at least 44px tall. Do not hide essential destinations behind hover mechanics or force the user to traverse a very long menu before seeing contact.

### Search and wayfinding

- Add search as a high-priority utility for the resource-heavy site; show result type, topic, and reading time.
- Use breadcrumbs on all deep pages, including insight and case-study templates.
- Use “Related solution,” “Related industry,” and “Evidence” modules to connect content to conversion paths.
- Keep a compact sticky in-page table of contents on long resources; it should collapse to a disclosure on mobile.

## Homepage blueprint

Avoid trying to explain every vertical in the hero. Make the first screen decisive, then use the page to progressively reveal proof.

| Order | Module | Content and interaction | Primary success signal |
| --- | --- | --- | --- |
| 1 | Hero | `India's Reach Engine` + a plain-language supporting sentence + two actions: **Talk to an expert** and **Explore solutions**. Show an abstract, performant coverage field or map detail—not an autoplay video. | Visitor understands the category and sees a next step. |
| 2 | Proof strip | Three verified live/static numbers: Digital Runners, districts, and pincodes, each linked to methodology or the network page. | Trust before persuasion. |
| 3 | Coverage explorer | An India map that begins with a useful national view; filters progressively reveal capability rather than requiring drill-down. Provide a static summary and accessible data table equivalent. | Visitor discovers reach relevant to their need. |
| 4 | Solution router | Five outcome-led cards: know the market, collect AI-ready data, deliver climate MRV, execute GTM, activate local influence. | Visitor selects a relevant solution. |
| 5 | How it works | A concise three-step system: local execution → quality/data layer → actionable outcome. | Technology and field network feel integrated. |
| 6 | Proof library | One featured case study plus three filtered metrics/outcomes; use client approval rules and show methodology where claims are material. | Visitor moves into evidence. |
| 7 | Industry entry | Industry chips/cards that change the supporting proof and recommended solution. | Buyer sees themselves represented. |
| 8 | Insights | Three current, topic-tagged resources selected by relevance, not merely recency. | Organic visitors continue to solution content. |
| 9 | Closing CTA | A low-friction native form or meeting request with expectation setting: who replies and when. | Qualified contact start. |

### India map rule

The map is a differentiator, not decoration. Ship an accessible, fast **overview** at launch and lazy-load richer drill-down/heatmap data after intent. Never make the map the only way to access coverage information; give a searchable state/district list and a text equivalent. Treat live indicators carefully: label timestamps and do not imply real-time data where it is not real-time.

## Reusable page templates

### Solution page

1. Outcome-led hero with one clear CTA and relevant trust signal.
2. Buyer problem in plain language.
3. “How Anaxee works” process with field, technology, and reporting proof.
4. Capabilities, each tied to an outcome rather than a feature list.
5. Data/coverage proof with source or methodology.
6. Related industry use cases and one full case study.
7. Related product or insight content.
8. Contextual form CTA.

### Industry page

Lead with the industry's operating problem, then map it to the relevant solutions, evidence, and use cases. Avoid re-skinning a generic solution page with only the industry name changed.

### Product page

Use product UI/screenshots, the user role, a clear “what it enables” story, integration/security facts where appropriate, and a demo CTA. The Prabhavak overview must say “powered by Anaxee” and distinguish partner/brand value from the consumer join flow.

### Case study

Make the result scannable before the narrative: client/sector, challenge, Anaxee intervention, geography/scale, measurable result, quote, and related next step. Use filters for industry, solution, and geography, but always retain a browseable no-JavaScript listing.

### Resource and insight page

Use a plain-language lead answer, key facts, dated sources, reading time, author/reviewer, in-page TOC, diagrams where they add understanding, FAQ, and a restrained related-solution CTA. Do not interrupt a research reader with a modal gate; reserve gating for high-value downloadable assets.

## Visual language

### Colour decision

There is a documented conflict to resolve before visual production: the live-site audit confirms a cyan/teal `#54C5D0`, while the current design-system proposal makes `#1E40AF` (blue) the primary brand colour. Do **not** silently replace the established teal with generic corporate blue.

Adopt the following hierarchy, subject to final contrast testing against the approved logo artwork:

| Token | Value | Role | Do not use for |
| --- | --- | --- | --- |
| Ink | `#0F172A` | Primary text, dark hero, high-trust surfaces | Large blocks of small reversed copy without testing |
| Anaxee Teal | `#54C5D0` | Brand highlight, map/coverage signal, decorative data marks | Small text or white-text CTA backgrounds; contrast is insufficient |
| Action Teal | `#007C89` | Primary button fill, links when teal identity is needed, focus treatment | Success/error meaning |
| Data Blue | `#2563EB` | Interactive charts, links, and product/data emphasis | The sole brand identity |
| Climate Green | `#16803C` | Climate-specific data and positive outcomes | Primary CTA across the entire platform |
| Warm Amber | `#B45309` | Influence/GTM emphasis and warning-adjacent highlights | Error status |
| Surface | `#F8FAFC` | Page sections and card backgrounds | A substitute for sufficient hierarchy |
| Border | `#CBD5E1` | Delineation and inputs | The only visible focus indicator |

Use colour as a supporting signal, never the only signal. Pair it with labels, icons, and position. Confirm every text/background and interactive-state pair at WCAG 2.1 AA before implementation; do not rely on the values in this document as a substitute for a contrast audit.

### Typography and layout

- Keep the system font stack as the default performance baseline; use Inter only after confirming its loading and language coverage strategy. Include Noto Sans Devanagari or a tested fallback when Hindi/local-language content ships.
- Use a compact editorial display style for major headlines: `clamp(2.25rem, 5vw, 4.5rem)`, 1.05–1.1 leading, and modest negative tracking at large sizes. Keep body text 16–18px with 1.5–1.65 leading and 65–75 character line lengths.
- Use an 8px spacing rhythm (with 4px increments for fine alignment), 12-column desktop / 6-column tablet / 4-column mobile grids, and constrain content to roughly 1200–1280px.
- Use real Indian field photography, documentation-style product screenshots, and purposeful data visualization. Avoid generic “AI” particles, stock handshakes, and decorative dashboard noise.

### Components

Use a small component vocabulary: primary/secondary/quiet buttons; text links; metric tiles; solution cards; evidence cards; filter chips; data tables; native-form fields; and a single modal/sheet pattern. Design every component in default, hover, pressed, focus-visible, disabled, loading, error, and dark-surface states before page assembly.

## Motion and interaction

Use motion to explain spatial change or response, not to decorate pages.

- Provide immediate pointer-down feedback and preserve 1:1 tracking for drag interactions.
- Use interruptible, critically damped springs for sheets, menus, and gesture-driven map panels; do not lock input during transitions.
- Hand off release velocity and project momentum only where the object is directly manipulated, such as map panels or a mobile sheet.
- Use a short fade or static change under `prefers-reduced-motion`; remove parallax, continuous map pulses, and elastic overshoot.
- Keep data counters honest: reveal verified values once and avoid looping numbers that imply live operations.
- Use translucent, blurred navigation or sheets only where it improves hierarchy. Make solid, high-contrast fallbacks for reduced transparency and busy backgrounds.

## Forms and conversion

Replace third-party Airtable handoffs for primary B2B leads with a branded, native-feeling form that remains measurable and trustworthy.

1. Ask only for name, work email, organization, need, and optional message initially.
2. Explain response expectations and privacy beside the submit action.
3. Validate inline; preserve submitted content after errors; never use colour alone for errors.
4. Route the selected need into CRM attribution and display a relevant success state.
5. Provide phone/WhatsApp as alternatives, not as the only escape from a failing form.

Use progressive profiling only after an initial exchange. A contact form that asks for every project detail before showing value is a conversion barrier.

## Accessibility, performance, and measurement

### Non-negotiable experience criteria

- Meet WCAG 2.1 AA; provide keyboard operation, visible focus, semantic headings, skip links, labels, descriptive alt text, and error copy that does not rely on colour.
- Ensure maps/charts have equivalent tables or written summaries.
- Support 320px screens, 200% zoom, and text resizing without clipping or horizontal page scrolling.
- Keep the first page view light: use an optimized hero image/poster, defer map data, and lazy-load video and heavy visualizations.
- Test the important journeys with keyboard, VoiceOver/NVDA, slow network, and touch devices before sign-off.

### Measure the UX

Instrument the funnel by intent, not only page views:

- Solution selection from hero and navigation.
- Map filter/select interactions and fallback-table use.
- Case-study depth (result section seen, CTA clicked).
- Resource-to-solution transitions.
- Form start, field error, completion, and qualified-lead rate.
- Search success rate and zero-result queries.
- Core Web Vitals, accessibility defects, and mobile conversion by landing page.

Review recordings and analytics monthly, then prioritize changes from observed friction—not visual preference alone.

## Delivery sequence

1. **Resolve brand foundations:** approve logo exports, the teal/blue colour hierarchy, type fallback, voice, and evidence/data-claim rules.
2. **Prototype two journeys:** enterprise buyer (solution → case study → contact) and climate buyer (solution → product → contact) at mobile and desktop widths.
3. **Build the shell:** header, mega menu, mobile sheet, footer, CTA/form, and accessible tokens before individual pages.
4. **Ship the conversion core:** homepage, five solution pages, key case studies, company/contact, and resource templates.
5. **Migrate and connect content:** map old URLs, bring blog authority into the resource/insight structure, and add related-content modules.
6. **Add differentiated data experiences:** launch the lightweight coverage overview first; add richer map/dashboard controls after performance, accessibility, and data governance checks.
7. **Validate:** conduct usability tests with at least one participant from each primary buyer group and test the end-to-end lead route before launch.

## Decisions needed before high-fidelity design

- Approve whether `#54C5D0` remains the core brand teal and whether the proposed blue becomes a supporting data token.
- Provide the approved wordmark, icon mark, favicon, dark/light variants, and social-card assets.
- Confirm which operational metrics are current, sourced, and safe to show with a timestamp or methodology.
- Decide the Prabhavak boundary: B2B overview on the main domain plus separate consumer flow is recommended.
- Define the CRM owner, lead-routing SLA, and consent/privacy copy for native forms.
