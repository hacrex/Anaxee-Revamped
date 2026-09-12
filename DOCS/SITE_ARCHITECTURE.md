# Anaxee Platform — Complete Sitemap & Information Architecture

## Overview

This document defines the complete site structure for the unified Anaxee digital platform at anaxee.com. It consolidates the corporate website, blog, and Prabhavak into a single, cohesive experience.

**Related Documents:**
- [PRD.md](../PRD.md) — Product requirements (Section 4: Information Architecture)
- [TECH_STACK.md](./TECH_STACK.md) — URL patterns and Next.js configuration
- [CONTENT_STRATEGY.md](./CONTENT_STRATEGY.md) — SEO and content hub strategy
- [MIGRATION_PLAN.md](./MIGRATION_PLAN.md) — Redirect strategy from old URLs

---

## Architecture Principles

1. **Unified Experience** — All content lives under one domain (anaxee.com)
2. **Audience-First Navigation** — Visitors find relevant content by role/need
3. **Solution-Centric** — Solutions and products are prominently featured
4. **Scalable** — New pages, products, and verticals can be added without restructuring
5. **SEO-Optimized** — Flat hierarchy, keyword-rich URLs, clear topic clusters
6. **Mobile-First** — Navigation works seamlessly on all devices

---

## Complete Sitemap

```text
anaxee.com
│
├── / (Homepage)
│
├── /solutions/
│   ├── /solutions/retail-intelligence/
│   ├── /solutions/ai-data-collection/
│   ├── /solutions/climate-and-carbon/
│   ├── /solutions/gtm-services/
│   └── /solutions/influence-marketing/
│
├── /products/
│   ├── /products/prabhavak/
│   ├── /products/climate-command-centre/
│   ├── /products/retail-intelligence-platform/
│   └── /products/reach-os/ (future)
│
├── /industries/
│   ├── /industries/fmcg/
│   ├── /industries/agriculture/
│   ├── /industries/automotive/
│   ├── /industries/climate/
│   └── /industries/government/
│
├── /case-studies/
│   ├── /case-studies/[slug]/ (dynamic individual pages)
│   └── ?industry=&solution=&geography= (filtering)
│
├── /resources/
│   ├── /resources/blog/
│   │   ├── /resources/blog/[slug]/ (dynamic individual posts)
│   │   ├── /resources/blog/category/[category]/
│   │   └── /resources/blog/tag/[tag]/
│   │
│   ├── /resources/reports/
│   │   └── /resources/reports/[slug]/
│   │
│   ├── /resources/whitepapers/
│   │   └── /resources/whitepapers/[slug]/
│   │
│   └── /resources/research/
│       └── /resources/research/[slug]/
│
├── /insights/ (GEO & AI-optimized content hub)
│   ├── /insights/what-is-digital-mrv/
│   ├── /insights/what-is-last-mile-execution/
│   ├── /insights/what-is-retail-intelligence/
│   ├── /insights/what-is-rural-market-research/
│   ├── /insights/what-is-carbon-project-verification/
│   ├── /insights/what-is-influence-marketing/
│   └── /insights/[slug]/ (future educational content)
│
├── /impact/
│   └── (Public impact dashboard with live counters)
│
├── /network/
│   └── (Digital Runner network showcase)
│
├── /company/
│   ├── /company/about/
│   ├── /company/leadership/
│   ├── /company/careers/
│   │   └── /company/careers/[slug]/ (individual job postings)
│   ├── /company/partners/
│   └── /company/contact/
│
├── /contact/
│
├── /search/
│   └── ?q= (site-wide search results)
│
├── /sitemap.xml (XML sitemap)
├── /robots.txt
│
└── Legal pages
    ├── /privacy-policy/
    ├── /terms-of-service/
    └── /cookie-policy/
```

---

## Page Descriptions

### Homepage (`/`)

**Purpose:** Establish Anaxee as India's Reach Engine. Create immediate understanding of scale, capability, and technology.

**Sections:**
1. Hero — "India's Reach Engine" with animated counters
2. Coverage Map — Interactive India map with drill-down
3. Solutions Overview — Cards for each solution vertical
4. Digital Runner Network — Live counters and network visualization
5. Industry Highlights — Key industries served
6. Products Showcase — Featured products (Prabhavak, Climate Command Centre, etc.)
7. Impact Metrics — Scale indicators (250,000+ Runners, 540+ Districts, etc.)
8. Client Logos — Enterprise trust signals
9. Testimonials — Client success stories
10. Latest Insights — Recent blog posts and reports
11. CTA Section — Contact, Demo Request, or Newsletter

---

### Solution Pages (`/solutions/*`)

**Purpose:** Deep-dive into each solution vertical. Explain the problem, how Anaxee solves it, capabilities, and impact.

#### `/solutions/retail-intelligence/`
- Store audits and verification
- Competitor tracking and benchmarking
- Merchandising compliance
- Availability and visibility checks
- Market intelligence and analytics
- Dashboard screenshots and heatmaps

#### `/solutions/ai-data-collection/`
- AI training dataset collection
- Image, audio, and video collection
- Human validation and annotation
- Quality assurance processes
- Scale and coverage metrics
- Positioning: "India's largest distributed human data collection network"

#### `/solutions/climate-and-carbon/`
- Digital MRV (Monitoring, Reporting, Verification)
- Carbon project implementation
- Field verification and monitoring
- Sustainability data collection
- Community engagement programs
- Carbon credit support metrics

#### `/solutions/gtm-services/`
- Go-to-market strategy execution
- Rural and urban market activation
- Distribution network management
- Brand launch support
- Market penetration services

#### `/solutions/influence-marketing/`
- Prabhavak platform integration
- Rural and regional influencer network
- Campaign management
- Impact measurement
- Positioning: "India's largest rural and regional influence network"

---

### Product Pages (`/products/*`)

**Purpose:** Showcase Anaxee's technology products with features, screenshots, pricing (if applicable), and sign-up/demo CTAs.

#### `/products/prabhavak/`
- Influence Marketing Platform
- Features and capabilities
- How it works
- Pricing or demo request
- Link to prabhavak.anaxee.com for app access
- Case studies using Prabhavak

#### `/products/climate-command-centre/`
- Climate project monitoring dashboard
- Digital MRV capabilities
- Carbon tracking and reporting
- Sustainability metrics visualization

#### `/products/retail-intelligence-platform/`
- Retail analytics dashboard
- Store audit management
- Real-time visibility tracking
- Reporting and insights

#### `/products/reach-os/` (future)
- Unified field operations platform
- Digital Runner management
- Task assignment and tracking
- Performance analytics

---

### Industry Pages (`/industries/*`)

**Purpose:** Speak directly to industry-specific pain points and demonstrate relevant use cases.

#### `/industries/fmcg/`
- Retail audits for FMCG
- Product launch support
- Visibility tracking
- Distribution monitoring
- Case studies from FMCG clients

#### `/industries/agriculture/`
- Farmer outreach programs
- Agricultural data collection
- Training campaign execution
- Crop monitoring support
- Rural market intelligence

#### `/industries/automotive/`
- Dealer network audits
- Customer satisfaction surveys
- Market research
- Last-mile execution for automotive brands

#### `/industries/climate/`
- Carbon project implementation
- Impact measurement and reporting
- Community engagement
- Digital MRV services
- Sustainability monitoring

#### `/industries/government/`
- Survey execution
- Program monitoring
- Field verification
- Data collection for public programs
- Monitoring and evaluation support

---

### Case Studies (`/case-studies/*`)

**Purpose:** Build enterprise credibility through documented client success stories.

**Individual Case Study Structure:**
- Client name and industry
- Problem statement
- Anaxee's approach
- Scale of execution
- Results and impact metrics
- Client testimonial
- Related solutions

**Filtering Options:**
- By Industry (FMCG, Agriculture, Climate, Government, etc.)
- By Solution (Retail Intelligence, AI Data, Climate, etc.)
- By Geography (State, District)
- By Client Type (Enterprise, Government, NGO)

---

### Resources (`/resources/*`)

**Purpose:** Centralized knowledge hub for all content assets.

#### `/resources/blog/`
Transformed blog with:
- Category-based navigation
- Tag filtering
- Search functionality
- Related articles
- Author profiles
- Reading time estimates
- Table of contents for long-form content

**Content Hub Categories:**
1. Retail Intelligence
2. AI Data Collection
3. Climate & Carbon
4. Influence Marketing
5. Rural Market Intelligence
6. GTM Strategy
7. Data Verification

#### `/resources/reports/`
- Industry reports
- Rural India insights
- Retail intelligence reports
- Downloadable PDFs (gated and ungated)

#### `/resources/whitepapers/`
- Climate whitepapers
- AI data collection research
- Last-mile execution insights
- Technology deep-dives

#### `/resources/research/`
- Original research
- Market analysis
- Trend reports
- Data-driven insights

---

### Insights Hub (`/insights/*`)

**Purpose:** GEO and AI search optimized educational content. Designed to be the authoritative source for key industry terms.

**Content Strategy:**
- Each page defines and explains a core concept
- Structured for AI search engines (ChatGPT, Gemini, Claude, Perplexity)
- FAQ sections on each page
- Internal linking to relevant solutions and case studies
- Schema markup (Article, FAQPage, HowTo)

**Key Pages:**
- "What is Digital MRV?"
- "What is Last-Mile Execution?"
- "What is Retail Intelligence?"
- "What is Rural Market Research?"
- "What is Carbon Project Verification?"
- "What is Influence Marketing?"
- "What is AI Data Collection?"

---

### Impact Dashboard (`/impact/`)

**Purpose:** Build trust through transparent, real-time impact metrics.

**Metrics Displayed:**
- Active Digital Runners
- States Covered (26+)
- Districts Covered (540+)
- Pincodes Covered (11,000+)
- Tasks Completed (millions)
- Retail Audits Performed
- Survey Responses Collected
- Climate Activities Supported
- Trees Monitored
- Carbon Credits Supported

**Implementation:**
- Animated counters
- Optional real-time updates via API
- Filterable by time period
- Embeddable for partner sites

---

### Network Page (`/network/`)

**Purpose:** Showcase the Digital Runner network as a key differentiator.

**Sections:**
- Who Are Digital Runners? (local entrepreneurs, community connectors, data collectors)
- How the Network Works
- Network Statistics (live counters)
- Runner Stories (humanized content)
- Geographic Coverage Map
- Join the Network CTA

---

### Company Pages (`/company/*`)

#### `/company/about/`
- Anaxee story and mission
- Evolution from last-mile outreach to technology platform
- Key milestones
- Leadership team
- Values and culture

#### `/company/leadership/`
- Individual leadership profiles
- Photos, bios, and social links

#### `/company/careers/`
- Open positions
- Benefits and culture
- Application process
- Individual job posting pages

#### `/company/partners/`
- Technology partners
- Implementation partners
- Channel partners

#### `/company/contact/`
- Office locations
- Contact form
- WhatsApp integration
- Email addresses
- Phone numbers

---

### Search (`/search/`)

**Purpose:** Site-wide search functionality.

**Features:**
- Real-time search suggestions
- Filter by content type (blog, case study, report, page)
- Recent searches
- Popular searches
- Search analytics integration

---

## URL Strategy

### Principles

1. **Lowercase only** — All URLs lowercase
2. **Hyphens for separators** — No underscores or spaces
3. **Descriptive** — URLs describe content (not IDs)
4. **Flat hierarchy** — Maximum 3 levels deep
5. **Keyword-rich** — Include target keywords in URLs
6. **No file extensions** — No .html, .php, etc.

### URL Patterns

| Content Type | Pattern | Example |
|-------------|---------|---------|
| Solution | `/solutions/[slug]/` | `/solutions/retail-intelligence/` |
| Product | `/products/[slug]/` | `/products/prabhavak/` |
| Industry | `/industries/[slug]/` | `/industries/fmcg/` |
| Case Study | `/case-studies/[slug]/` | `/case-studies/fmcg-retail-audit/` |
| Blog Post | `/resources/blog/[slug]/` | `/resources/blog/climate-mrv-guide/` |
| Report | `/resources/reports/[slug]/` | `/resources/reports/rural-india-2025/` |
| Insight | `/insights/[slug]/` | `/insights/what-is-digital-mrv/` |
| Job | `/company/careers/[slug]/` | `/company/careers/senior-data-engineer/` |

---

## Navigation Structure

### Primary Navigation (Desktop)

```text
Solutions ▾  |  Products ▾  |  Industries ▾  |  Case Studies  |  Resources ▾  |  Company ▾  |  [Contact Us]
```

### Mega Menu — Solutions

```text
┌─────────────────────────────────────────────────────────┐
│  Solutions                                              │
│                                                         │
│  Retail Intelligence    AI Data Collection              │
│  Climate & Carbon       GTM Services                    │
│  Influence Marketing                                      │
│                                                         │
│  [View All Solutions →]                                 │
└─────────────────────────────────────────────────────────┘
```

### Mega Menu — Products

```text
┌─────────────────────────────────────────────────────────┐
│  Products                                               │
│                                                         │
│  Prabhavak                Climate Command Centre        │
│  Retail Intelligence Platform                           │
│                                                         │
│  [View All Products →]                                  │
└─────────────────────────────────────────────────────────┘
```

### Mega Menu — Industries

```text
┌─────────────────────────────────────────────────────────┐
│  Industries                                             │
│                                                         │
│  FMCG                 Agriculture                       │
│  Automotive           Climate                           │
│  Government                                             │
│                                                         │
│  [View All Industries →]                                │
└─────────────────────────────────────────────────────────┘
```

### Mega Menu — Resources

```text
┌─────────────────────────────────────────────────────────┐
│  Resources                                              │
│                                                         │
│  Blog                Reports                            │
│  Whitepapers         Research                           │
│                                                         │
│  Content Hubs:                                          │
│  Retail Intelligence │ Climate & Carbon                 │
│  AI Data Collection  │ Influence Marketing              │
│                                                         │
│  [View All Resources →]                                 │
└─────────────────────────────────────────────────────────┘
```

### Mobile Navigation

- Hamburger menu
- Full-screen overlay
- Accordion-style sections
- Quick access to Contact and Search

---

## Internal Linking Strategy

### Topic Clusters

Each solution area forms a topic cluster:

**Cluster 1: Retail Intelligence**
- Pillar: `/solutions/retail-intelligence/`
- Cluster: Blog posts about retail audits, market intelligence
- Cluster: Case studies featuring retail intelligence
- Cluster: `/industries/fmcg/`

**Cluster 2: AI Data Collection**
- Pillar: `/solutions/ai-data-collection/`
- Cluster: Blog posts about AI training data, data collection
- Cluster: `/insights/what-is-digital-mrv/`
- Cluster: `/insights/what-is-ai-data-collection/`

**Cluster 3: Climate & Carbon**
- Pillar: `/solutions/climate-and-carbon/`
- Cluster: Blog posts about carbon markets, MRV
- Cluster: `/products/climate-command-centre/`
- Cluster: `/industries/climate/`
- Cluster: `/insights/what-is-carbon-project-verification/`

**Cluster 4: Influence Marketing**
- Pillar: `/solutions/influence-marketing/`
- Cluster: Blog posts about influencer campaigns
- Cluster: `/products/prabhavak/`
- Cluster: `/insights/what-is-influence-marketing/`

**Cluster 5: GTM Services**
- Pillar: `/solutions/gtm-services/`
- Cluster: Blog posts about market activation
- Cluster: Case studies featuring GTM execution

### Cross-Linking Rules

1. Every solution page links to related products, industries, and case studies
2. Every industry page links to relevant solutions
3. Every case study links to the solution(s) it demonstrates
4. Every blog post links to at least one solution page
5. Every product page links to the solution it supports
6. Every insight page links to related solutions and case studies

---

## Breadcrumb Structure

```text
Home > Solutions > Retail Intelligence
Home > Products > Prabhavak
Home > Industries > FMCG
Home > Case Studies > [Case Study Title]
Home > Resources > Blog > [Post Title]
Home > Insights > What is Digital MRV?
Home > Company > Careers > [Job Title]
```

---

## Future Expansion

### Potential Additions

- `/academy/` — Training and certification platform
- `/partner/` — Partner portal
- `/investor/` — Investor relations
- `/press/` — Press releases and media kit
- `/events/` — Events and webinars
- `/community/` — Digital Runner community portal

### International Expansion

When ready for global markets:
- `/global/` or country-specific subdirectories
- Multi-language support via i18n
- Region-specific content and case studies

---

## Domain Strategy

### Primary Domain

- **anaxee.com** — All marketing, content, and product pages

### Redirected Domains

| Domain | Strategy | Implementation |
|--------|----------|----------------|
| blog.anaxee.com | Redirect to /resources/blog/ | DNS-level 301 redirect |
| anaxeetech.com | Redirect to anaxee.com | DNS-level 301 redirect |

### Preserved Domains

| Domain | Purpose | Notes |
|--------|---------|-------|
| prabhavak.anaxee.com | Application backend | User auth, dashboard, API — marketing page on main site |

### Redirect Rules

```nginx
# blog.anaxee.com → anaxee.com/resources/blog/
server {
    server_name blog.anaxee.com;
    return 301 https://anaxee.com/resources/blog$request_uri;
}

# anaxeetech.com → anaxee.com
server {
    server_name anaxeetech.com www.anaxeetech.com;
    return 301 https://anaxee.com$request_uri;
}
```
