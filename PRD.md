# Anaxee Digital Platform — Product Requirements Document

**Version:** 1.0
**Date:** September 2026
**Status:** Draft
**Author:** Project Team

---

## 1. Executive Summary

### 1.1 Product Vision

Build a unified, world-class digital platform that positions Anaxee as **India's Reach Engine** — a technology-enabled network combining AI, data, climate intelligence, and 250,000+ Digital Runners to solve last-mile execution and intelligence challenges across India and beyond.

### 1.2 Problem Statement

Anaxee currently operates three disconnected digital properties:

| Property | Technology | Status |
|----------|-----------|--------|
| anaxee.com | WordPress | Outdated design, mispositioned as traditional outreach company |
| blog.anaxee.com | WordPress | Separate UX, inconsistent branding, poor content structure |
| prabhavak.anaxee.com | Next.js | Feels like independent product, not integrated Anaxee solution |

This fragmentation creates:
- Inconsistent brand perception across properties
- Disconnected customer journeys
- Wasted SEO equity across multiple domains
- Difficulty showcasing Anaxee's full technology and data capabilities
- Poor discoverability for AI-powered search engines

### 1.3 Proposed Solution

Consolidate all three properties into a single unified platform at **anaxee.com** built with modern technology, presenting Anaxee as a technology-driven organization delivering solutions across Retail Intelligence, AI Data Collection, Climate & Carbon, GTM Services, and Influence Marketing.

### 1.4 Target Launch

**20 weeks from project kickoff** (approximately 5 months)

---

## 2. Goals & Success Metrics

### 2.1 Business Goals

| Goal | Description |
|------|-------------|
| Brand Transformation | Reflected as technology company, not just field-force |
| Unified Experience | Single cohesive digital presence |
| Enterprise Positioning | Showcase solutions, products, and impact |
| SEO/GEO/AI Visibility | Dominate traditional and AI-powered search |
| Scalability | Support future products and verticals |

### 2.2 Success Metrics

#### Brand Metrics
- Increased direct traffic by 30% within 6 months
- Increased brand search volume by 25% within 6 months
- Improved engagement rates (time on site, pages per session)

#### Marketing Metrics
- Increased qualified leads by 40% within 6 months
- Improved conversion rates by 20%
- Lower bounce rates by 15%

#### SEO Metrics
- Increased organic traffic by 50% within 6 months
- Top 10 rankings for 20+ target keywords
- Featured in AI search results (ChatGPT, Gemini, Perplexity)

#### Performance Metrics
- Core Web Vitals all green (LCP < 2.5s, FID < 100ms, CLS < 0.1)
- Lighthouse score > 90 across all categories
- Page load time < 2 seconds

---

## 3. Target Users

### 3.1 Primary Audiences

| Audience | Role | Needs |
|----------|------|-------|
| **Enterprises** | Sales leaders, Marketing teams, Operations teams, Business decision makers | Understand Anaxee's scale and capabilities, request demos, view case studies |
| **Climate Organizations** | Carbon project developers, Sustainability consultants, Impact organizations | Explore climate solutions, view MRV capabilities, assess partnership |
| **Brands** | FMCG companies, Consumer brands, Retail networks | Discover retail intelligence, request market activation services |
| **NGOs** | Development organizations, Impact-focused institutions | Explore outreach capabilities, view community impact |
| **Government Agencies** | Public sector departments, M&E teams, Outreach programs | Understand field execution capabilities, view compliance |

### 3.2 User Journeys

#### Enterprise Buyer Journey
```text
Homepage → Solutions Overview → Specific Solution Page → Case Studies → Contact/Demo Request
```

#### Climate Organization Journey
```text
Homepage → Climate & Carbon Solution → Climate Command Centre Product → Case Studies → Contact
```

#### Brand/FMCG Journey
```text
Homepage → Retail Intelligence Solution → FMCG Industry Page → Case Studies → Contact
```

#### Content Consumer Journey
```text
Search/Arrival → Blog Post → Related Solution Page → Case Study → Contact
```

---

## 4. Information Architecture

### 4.1 Site Map

```text
anaxee.com
├── / (Homepage)
├── /solutions/
│   ├── /solutions/retail-intelligence/
│   ├── /solutions/ai-data-collection/
│   ├── /solutions/climate-and-carbon/
│   ├── /solutions/gtm-services/
│   └── /solutions/influence-marketing/
├── /products/
│   ├── /products/prabhavak/
│   ├── /products/climate-command-centre/
│   └── /products/retail-intelligence-platform/
├── /industries/
│   ├── /industries/fmcg/
│   ├── /industries/agriculture/
│   ├── /industries/automotive/
│   ├── /industries/climate/
│   └── /industries/government/
├── /case-studies/
│   ├── /case-studies/[slug]/
├── /resources/
│   ├── /resources/blog/
│   │   ├── /resources/blog/[slug]/
│   │   ├── /resources/blog/category/[category]/
│   ├── /resources/reports/
│   ├── /resources/whitepapers/
│   └── /resources/research/
├── /insights/
│   ├── /insights/what-is-digital-mrv/
│   ├── /insights/what-is-last-mile-execution/
│   ├── /insights/what-is-retail-intelligence/
│   └── /insights/[slug]/
├── /impact/
├── /network/
├── /company/
│   ├── /company/about/
│   ├── /company/leadership/
│   ├── /company/careers/
│   └── /company/contact/
├── /contact/
├── /search/
├── /privacy-policy/
├── /terms-of-service/
└── /sitemap.xml
```

### 4.2 Navigation Structure

**Desktop:** Mega menu with Solutions, Products, Industries, Case Studies, Resources, Company, Contact CTA
**Mobile:** Hamburger menu with accordion sections

---

## 5. Functional Requirements

### 5.1 Homepage

| ID | Requirement | Priority |
|----|------------|----------|
| HOM-01 | Dynamic hero section with animated counters (250K+ Runners, 540+ Districts, 11K+ Pincodes) | P0 |
| HOM-02 | Interactive India coverage map with state/district drill-down | P0 |
| HOM-03 | Solution overview cards (5 verticals) | P0 |
| HOM-04 | Digital Runner network showcase with live counters | P0 |
| HOM-05 | Industry highlights section | P0 |
| HOM-06 | Client logos carousel | P0 |
| HOM-07 | Testimonials section | P0 |
| HOM-08 | Latest insights section (recent blog posts) | P0 |
| HOM-09 | CTA sections (Contact, Demo Request) | P0 |
| HOM-10 | Scroll-based storytelling sequence | P2 |

### 5.2 Solution Pages (5 pages)

| ID | Requirement | Priority |
|----|------------|----------|
| SOL-01 | Retail Intelligence solution page | P0 |
| SOL-02 | AI Data Collection solution page | P0 |
| SOL-03 | Climate & Carbon solution page | P0 |
| SOL-04 | GTM Services solution page | P0 |
| SOL-05 | Influence Marketing solution page | P0 |
| SOL-06 | Each page: Hero, problem/solution, features, metrics, related case studies, CTA | P0 |
| SOL-07 | Filter case studies by solution | P1 |

### 5.3 Product Pages (3 pages)

| ID | Requirement | Priority |
|----|------------|----------|
| PRD-01 | Prabhavak product page with link to app | P0 |
| PRD-02 | Climate Command Centre product page | P0 |
| PRD-03 | Retail Intelligence Platform product page | P0 |
| PRD-04 | Each page: Features, screenshots, demo request CTA | P0 |

### 5.4 Industry Pages (5 pages)

| ID | Requirement | Priority |
|----|------------|----------|
| IND-01 | FMCG industry page | P0 |
| IND-02 | Agriculture industry page | P0 |
| IND-03 | Automotive industry page | P0 |
| IND-04 | Climate industry page | P0 |
| IND-05 | Government industry page | P0 |
| IND-06 | Each page: Pain points, solutions, use cases, case studies | P0 |

### 5.5 Case Studies

| ID | Requirement | Priority |
|----|------------|----------|
| CS-01 | Case study listing page with filters (industry, solution, geography) | P0 |
| CS-02 | Individual case study template (problem, approach, scale, results, testimonial) | P0 |
| CS-03 | Related case studies on individual pages | P1 |

### 5.6 Blog & Resources

| ID | Requirement | Priority |
|----|------------|----------|
| BLOG-01 | Blog listing page with category/tag filtering | P0 |
| BLOG-02 | Blog post template with author bio, related articles, reading time | P0 |
| BLOG-03 | Table of contents for long-form content | P1 |
| BLOG-04 | 7 content hubs (Retail Intelligence, AI Data Collection, Climate & Carbon, Influence Marketing, Rural Market Intelligence, GTM Strategy, Data Verification) | P1 |
| RES-01 | Reports listing and detail pages | P1 |
| RES-02 | Whitepapers listing and detail pages | P1 |
| RES-03 | Gated content with lead capture | P2 |

### 5.7 Insights Hub (GEO/AI Optimized)

| ID | Requirement | Priority |
|----|------------|----------|
| INS-01 | "What is Digital MRV?" page | P0 |
| INS-02 | "What is Last-Mile Execution?" page | P0 |
| INS-03 | "What is Retail Intelligence?" page | P0 |
| INS-04 | "What is Rural Market Research?" page | P0 |
| INS-05 | "What is Carbon Project Verification?" page | P0 |
| INS-06 | "What is Influence Marketing?" page | P0 |
| INS-07 | "What is AI Data Collection?" page | P0 |
| INS-08 | FAQ sections on all insight pages | P0 |
| INS-09 | Schema markup (Article, FAQPage) | P0 |

### 5.8 Impact Dashboard

| ID | Requirement | Priority |
|----|------------|----------|
| IMP-01 | Public impact page with animated counters | P1 |
| IMP-02 | Metrics: Runners, States, Districts, Pincodes, Tasks, Audits, Climate | P1 |
| IMP-03 | Time period filtering | P2 |
| IMP-04 | API endpoint for data | P2 |

### 5.9 Digital Runner Network

| ID | Requirement | Priority |
|----|------------|----------|
| NET-01 | Dedicated /network/ page | P1 |
| NET-02 | Who are Digital Runners section | P1 |
| NET-03 | Network statistics | P1 |
| NET-04 | Runner stories and profiles | P2 |

### 5.10 Company Pages

| ID | Requirement | Priority |
|----|------------|----------|
| CO-01 | About page (story, mission, milestones) | P0 |
| CO-02 | Leadership page | P0 |
| CO-03 | Careers page with job listings | P0 |
| CO-04 | Contact page with form, office locations, WhatsApp | P0 |

### 5.11 Search

| ID | Requirement | Priority |
|----|------------|----------|
| SRC-01 | Site-wide search functionality | P1 |
| SRC-02 | Real-time search suggestions | P2 |
| SRC-03 | Filter by content type | P2 |

### 5.12 Navigation & UI

| ID | Requirement | Priority |
|----|------------|----------|
| NAV-01 | Desktop mega menu | P0 |
| NAV-02 | Mobile hamburger menu | P0 |
| NAV-03 | Breadcrumb navigation on all pages | P0 |
| NAV-04 | Back-to-top button | P0 |
| NAV-05 | Dark mode toggle | P0 |
| NAV-06 | Responsive design (mobile-first) | P0 |

---

## 6. Non-Functional Requirements

### 6.1 Performance

| Metric | Target | Threshold |
|--------|--------|-----------|
| LCP (Largest Contentful Paint) | < 2.0s | < 2.5s |
| FID (First Input Delay) | < 50ms | < 100ms |
| CLS (Cumulative Layout Shift) | < 0.05 | < 0.1 |
| INP (Interaction to Next Paint) | < 150ms | < 200ms |
| Lighthouse Performance Score | > 90 | > 80 |
| Page Load Time | < 2s | < 3s |
| Time to Interactive | < 3s | < 5s |

### 6.2 SEO

- Unique meta titles (50–60 characters) on all pages
- Unique meta descriptions (150–160 characters) on all pages
- Proper H1–H6 heading hierarchy
- JSON-LD schema markup on all pages
- Open Graph and Twitter Card tags
- Canonical URLs
- XML sitemap
- robots.txt
- Internal linking strategy
- Breadcrumbs

### 6.3 GEO & AI Search

- Entity-First content structure
- FAQ sections on insight pages
- Structured data for AI extraction
- Clear definitions and explanations
- Citation-ready content format
- Knowledge graph alignment

### 6.4 Accessibility

- WCAG 2.1 AA compliance minimum
- Keyboard navigation for all interactive elements
- Screen reader compatibility
- Color contrast ratio minimum 4.5:1
- Focus indicators on all interactive elements
- Alt text on all images
- Proper heading hierarchy
- Skip navigation links

### 6.5 Security

- HTTPS enforced
- Security headers (X-Frame-Options, X-Content-Type-Options, etc.)
- Content Security Policy
- No sensitive data in client-side code
- API keys server-side only
- Regular dependency audits

### 6.6 Responsive Design

| Breakpoint | Width | Layout |
|-----------|-------|--------|
| Mobile | 0–639px | Single column, hamburger nav |
| Tablet | 640–1023px | 2-column layouts, hamburger nav |
| Desktop | 1024–1279px | Full layout, mega menu |
| Wide | 1280px+ | Max-width constrained |

---

## 7. Technology Stack

| Layer | Decision | Rationale |
|-------|----------|-----------|
| Framework | Next.js 14+ (App Router) | SSR/SSG, React ecosystem, Vercel integration |
| Language | TypeScript | Type safety, better DX |
| UI Library | React 18+ | Component-based architecture |
| Styling | Tailwind CSS | Utility-first, design token integration |
| CMS | Sanity | Flexible content modeling, GROQ queries, real-time |
| Hosting | Vercel | Native Next.js support, global edge network |
| Analytics | GA4 + Search Console + Microsoft Clarity | Traffic, SEO, UX insights |
| Error Monitoring | Sentry | Error tracking, performance monitoring |
| Package Manager | pnpm | Fast, disk-efficient |
| Testing | Vitest + Playwright | Unit and E2E testing |
| CI/CD | GitHub Actions + Vercel | Automated testing and deployment |

---

## 8. Content Requirements

### 8.1 Content Types

| Type | Quantity | Priority |
|------|----------|----------|
| Homepage | 1 | P0 |
| Solution Pages | 5 | P0 |
| Product Pages | 3 | P0 |
| Industry Pages | 5 | P0 |
| Case Studies | 10+ | P0 |
| Blog Posts | 20+ (migrated + new) | P0 |
| Insight Pages | 7 | P0 |
| Company Pages | 4 | P0 |
| Reports | 2+ | P1 |
| Whitepapers | 2+ | P1 |
| Legal Pages | 3 | P0 |

### 8.2 Content Migration

- Migrate all blog posts from blog.anaxee.com
- Migrate corporate content from anaxee.com
- Create Prabhavak landing page on anaxee.com/products/prabhavak/
- Set up 301 redirects for all changed URLs
- Preserve SEO equity during migration

---

## 9. Design Requirements

### 9.1 Brand Positioning

**From:** Last-mile outreach company
**To:** India's Reach Engine — technology-powered intelligence, data, climate, and execution network

### 9.2 Design Principles

1. Technology-First — Visually communicate innovation and data
2. India-Focused — Warmth and accessibility with enterprise credibility
3. Data-Driven — Metrics, dashboards, visualizations are core
4. Clean & Modern — Minimal clutter, clear hierarchy, purposeful whitespace
5. Scalable — Design tokens and components that grow

### 9.3 Design Inspiration

Stripe, Vercel, Notion, HubSpot, Snowflake, Datadog

### 9.4 Color System

| Color | Hex | Usage |
|-------|-----|-------|
| Anaxee Blue | #1E40AF | Primary brand, CTAs |
| Anaxee Dark | #0F172A | Headings, dark backgrounds |
| Electric Blue | #3B82F6 | Links, interactive elements |
| Teal | #14B8A6 | Climate/sustainability content |
| Green | #22C55E | Success states |
| Amber | #F59E0B | Warnings, highlights |

### 9.5 Typography

- **Headings:** Inter (weights 600–800)
- **Body:** Inter (weight 400)
- **Monospace:** JetBrains Mono

---

## 10. Migration Requirements

### 10.1 Migration Scope

| Property | Strategy | Risk Level |
|----------|----------|------------|
| anaxee.com (WordPress) | Content rewrite + URL preservation | High |
| blog.anaxee.com (WordPress) | Content migration + URL redirect | High |
| prabhavak.anaxee.com (Next.js) | Landing page on main site, app stays on subdomain | Medium |

### 10.2 Redirect Requirements

- Every old URL must either serve same content, redirect (301), or show helpful 404
- No redirect chains (A → B → C)
- No redirect loops (A → B → A)
- All redirects must be 301 (permanent)

### 10.3 SEO Preservation

- Preserve all existing backlinks
- Maintain current search rankings
- Keep meta titles and descriptions where performing well
- Preserve internal linking structure
- Monitor organic traffic daily for first month post-launch

---

## 11. Constraints & Assumptions

### 11.1 Constraints

- Must preserve existing SEO equity and backlinks
- Must maintain or improve current organic traffic
- Must work across all modern browsers and devices
- Must comply with WCAG 2.1 AA accessibility
- Budget and timeline as defined in roadmap

### 11.2 Assumptions

- Brand positioning "India's Reach Engine" is approved
- CMS decision (Sanity) is approved before Phase 2
- Content team will be available for migration and ongoing publishing
- Existing analytics and Search Console access will be provided
- Stakeholder review and approval at each phase gate

---

## 12. Dependencies

| Dependency | Owner | Impact |
|-----------|-------|--------|
| Brand positioning approval | Leadership | Blocks Phase 1 |
| CMS selection decision | Project Lead | Blocks Phase 2 |
| Hosting selection decision | Tech Lead | Blocks Phase 2 |
| SEO baseline data | SEO Team | Blocks Phase 0 completion |
| Analytics baseline data | Analytics Team | Blocks Phase 0 completion |
| Content inventory | Content Team | Blocks Phase 0 completion |
| Existing site access (WordPress admin) | IT/DevOps | Blocks content audit |
| Sanity account setup | Tech Lead | Blocks Phase 2 |

---

## 13. Risks

| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|------------|
| SEO traffic loss during migration | High | Medium | Comprehensive redirects, monitor closely, preserve URLs |
| CMS selection delays | High | Low | Make decision in Phase 0 |
| Content migration complexity | Medium | High | Start migration scripts early, incremental migration |
| Scope creep | High | Medium | Strict phase gates, MVP mindset |
| Brand decision delays | Medium | Low | Get approval in Phase 0 |
| Performance issues | Medium | Low | Performance budgets from Phase 2 |
| Third-party integration failures | Medium | Medium | Test integrations early, have fallbacks |

---

## 14. Open Questions

| Question | Owner | Decision Needed By |
|----------|-------|-------------------|
| Is "India's Reach Engine" the final positioning? | Leadership | Phase 0 |
| Should Prabhavak remain on subdomain? | Product Lead | Phase 0 |
| Which blog articles should be migrated vs archived? | Content Lead | Phase 0 |
| Which existing URLs have high-value backlinks? | SEO Lead | Phase 0 |
| What are the primary lead-gen goals? | Business Lead | Phase 0 |
| Which CMS (Sanity vs Strapi)? | Tech Lead | Phase 0 |
| Which hosting platform (Vercel vs Azure)? | Tech Lead | Phase 0 |

---

## 15. Appendix

### 15.1 Related Documents

- [ROADMAP.md](./DOCS/ROADMAP.md) — Phased implementation plan
- [SITE_ARCHITECTURE.md](./DOCS/SITE_ARCHITECTURE.md) — Complete sitemap
- [CONTENT_STRATEGY.md](./DOCS/CONTENT_STRATEGY.md) — SEO + GEO + AI content plan
- [DESIGN_SYSTEM.md](./DOCS/DESIGN_SYSTEM.md) — Branding, colors, typography, components
- [FEATURES.md](./DOCS/FEATURES.md) — Wishlist and future enhancements
- [MIGRATION_PLAN.md](./DOCS/MIGRATION_PLAN.md) — WordPress + Blog + Prabhavak migration strategy
- [TECH_STACK.md](./DOCS/TECH_STACK.md) — Next.js, CMS, hosting, analytics decisions
- [LAUNCH_CHECKLIST.md](./DOCS/LAUNCH_CHECKLIST.md) — Pre-launch and post-launch tasks

### 15.2 Existing Repository Documents

- [README.md](./README.md) — Project overview
- [day0.md](./day0.md) — Day 0 kickoff and discovery
- [Transformation-Proposal.md](./Transformation-Proposal.md) — Current state assessment
- [Ideas & Vision Board.md](./Ideas & Vision Board.md) — Feature ideas and vision

### 15.3 Approval

| Role | Name | Date | Approved |
|------|------|------|----------|
| Product Owner | | | |
| Tech Lead | | | |
| Design Lead | | | |
| SEO Lead | | | |
| Business Lead | | | |
