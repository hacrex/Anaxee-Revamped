# Day 0 — Project Kickoff & Discovery

## Anaxee Digital Platform Transformation

**Objective:** Establish the baseline, understand the existing digital ecosystem, define project ownership, and prepare the foundation for the redesign.

---

## 1. Day 0 Objective

Day 0 is the **Discovery & Baseline Day**.

No major development or redesign decisions should be finalized before the existing platforms, content, technology, analytics, SEO, and business requirements are understood.

The primary objective is to answer:

> **Where are we today, where do we want to go, and what must not be lost during the transformation?**

---

# 2. Existing Digital Properties

Review all current properties:

### Corporate Website

`https://anaxee.com`

Technology:

* WordPress
* Existing SEO configuration
* Existing content
* Existing forms
* Existing analytics

### Blog

`https://blog.anaxee.com`

Technology:

* WordPress
* Existing articles
* Categories and tags
* Search visibility
* Existing backlinks

### Prabhavak

`https://prabhavak.anaxee.com`

Technology:

* Next.js
* React
* Tailwind CSS
* Product/platform experience

---

# 3. Business Understanding

Document Anaxee's current business positioning.

## Current Business Verticals

* Retail Intelligence
* AI Data Services
* Data Collection
* Climate & Carbon Projects
* Influence Marketing
* GTM Services
* Last-Mile Execution

## Core Differentiator

Anaxee combines:

```text
Technology
     +
AI
     +
Data
     +
Digital Runner Network
     +
Last-Mile Execution
     =
India's Reach Engine
```

---

# 4. Target Audiences

Identify the primary audiences for the new website.

### Enterprise

* Business leaders
* Marketing teams
* Sales teams
* Operations teams
* Data teams

### Climate Organizations

* Climate companies
* Carbon project developers
* Sustainability organizations
* NGOs

### Brands

* FMCG
* Consumer brands
* Retail businesses

### Government

* Government departments
* Public-sector organizations
* Development programs

### NGOs & Social Organizations

* NGOs
* Foundations
* Impact organizations

---

# 5. Existing Website Audit

Create an inventory of all important pages.

Record:

| Page      | URL       | Traffic | Ranking | Leads | Action   |
| --------- | --------- | ------: | ------: | ----: | -------- |
| Homepage  | `/`       |     TBD |     TBD |   TBD | Redesign |
| About     | `/about/` |     TBD |     TBD |   TBD | Review   |
| Solutions | TBD       |     TBD |     TBD |   TBD | Rebuild  |
| Contact   | TBD       |     TBD |     TBD |   TBD | Preserve |
| Blog      | TBD       |     TBD |     TBD |   TBD | Migrate  |

### Page Classification

Every existing page should eventually be classified as:

* **KEEP**
* **REWRITE**
* **MERGE**
* **REDIRECT**
* **REMOVE**

---

# 6. SEO Baseline

Before changing URLs or content, capture the existing SEO state.

## Search Console

Record:

* Total clicks
* Total impressions
* Average CTR
* Average position
* Top queries
* Top pages
* Indexed pages
* Countries
* Devices

## Technical SEO

Check:

* Sitemap
* Robots.txt
* Canonical URLs
* Meta titles
* Meta descriptions
* H1 structure
* Internal links
* Broken links
* 404 pages
* Redirects
* Schema markup

---

# 7. Analytics Baseline

Review existing analytics.

Capture:

* Monthly users
* Sessions
* Top landing pages
* Traffic sources
* Conversion events
* Contact submissions
* CTA clicks
* Device distribution
* Geographic distribution

Create a baseline report so the new website can be measured against the old website.

---

# 8. Content Inventory

Create a complete content inventory covering:

### Website

* Pages
* Services
* Solutions
* Team
* About
* Contact

### Blog

* Articles
* Authors
* Categories
* Tags
* Images

### Marketing Assets

* Case studies
* Reports
* Whitepapers
* Videos
* Presentations
* Customer testimonials

---

# 9. Brand Audit

Review:

* Logo
* Colors
* Typography
* Icons
* Photography
* Illustrations
* Tone of voice
* Messaging
* Product branding

Identify inconsistencies between:

```text
Anaxee
   |
   ├── Corporate Website
   ├── Blog
   └── Prabhavak
```

---

# 10. Technology Audit

Document the current technology stack.

## Corporate Website

* WordPress
* Theme
* Plugins
* PHP version
* Database
* Hosting
* CDN
* SSL

## Blog

* WordPress
* Theme
* Plugins
* Hosting
* Database
* SEO plugins

## Prabhavak

* Next.js
* React
* Tailwind CSS
* APIs
* Backend services
* Hosting
* Authentication

---

# 11. Infrastructure Review

Document:

* DNS
* Domains
* Subdomains
* SSL certificates
* Hosting
* CDN
* CI/CD
* Backups
* Monitoring
* Environment variables
* Third-party integrations

Do not expose credentials or secrets in project documentation.

---

# 12. Integration Inventory

Identify all integrations.

Potential integrations:

* Google Analytics
* Google Search Console
* Contact forms
* CRM
* Email
* WhatsApp
* Newsletter
* Social media
* Maps
* Marketing automation
* Prabhavak APIs
* Internal Anaxee systems

---

# 13. Conversion Audit

Identify current conversion points.

Examples:

* Contact Us
* Request Demo
* Talk to Sales
* WhatsApp
* Email
* Download Report
* Case Study
* Newsletter

For each CTA, document:

```text
CTA
 ↓
Landing Page
 ↓
Form
 ↓
CRM / Email
 ↓
Sales Team
```

---

# 14. Competitor & Inspiration Research

Create a shortlist of websites that represent the desired quality level.

Potential inspiration categories:

* Technology companies
* AI companies
* Data companies
* Climate technology companies
* Enterprise SaaS
* Digital platforms

Evaluate:

* Homepage storytelling
* Navigation
* Visual hierarchy
* Case studies
* Product presentation
* Motion
* Mobile UX
* Conversion strategy

---

# 15. Initial Information Architecture

Proposed top-level structure:

```text
Home

Solutions
├── Retail Intelligence
├── AI Data Services
├── Data Collection
├── Climate & Carbon
├── Influence Marketing
└── GTM Services

Products
├── Prabhavak
├── Climate Command Center
└── Retail Intelligence Platform

Industries
├── FMCG
├── Agriculture
├── Automotive
├── Climate
└── Government

Case Studies

Resources
├── Blog
├── Reports
├── Whitepapers
└── Research

Company
├── About
├── Impact
├── Network
└── Careers

Contact
```

This architecture should be treated as a starting point and finalized after discovery.

---

# 16. Day 0 Deliverables

By the end of Day 0, the team should have:

* [ ] Existing website inventory
* [ ] Blog content inventory
* [ ] Prabhavak overview
* [ ] SEO baseline
* [ ] Analytics baseline
* [ ] Technology inventory
* [ ] Infrastructure inventory
* [ ] Integration inventory
* [ ] Brand audit
* [ ] Target audience definition
* [ ] Business vertical definition
* [ ] Initial sitemap
* [ ] Initial conversion map
* [ ] Initial migration risks
* [ ] Initial project roadmap

---

# 17. Questions to Resolve

The following questions should be answered before development begins:

### Brand

* Is **"India's Reach Engine"** the primary positioning?
* What is the final brand tagline?
* What products should have independent identities?

### Architecture

* Should Prabhavak remain on a subdomain?
* Should the blog move completely under `/resources/blog/`?
* Which existing URLs must be preserved?

### Content

* Which pages need complete rewriting?
* Which blog articles should be migrated?
* Which case studies are ready?

### Technology

* Which CMS will be used?
* Where will the new platform be hosted?
* How will deployments work?

### SEO

* Which existing pages generate significant organic traffic?
* Which URLs have valuable backlinks?
* What redirects are required?

### Business

* What are the primary lead-generation goals?
* Which business verticals have the highest priority?
* Which audiences should receive dedicated landing experiences?

---

# 18. Definition of Done

Day 0 is complete when the team has a shared understanding of:

```text
CURRENT STATE
      ↓
BUSINESS REQUIREMENTS
      ↓
TARGET AUDIENCE
      ↓
BRAND POSITIONING
      ↓
INFORMATION ARCHITECTURE
      ↓
TECHNOLOGY DIRECTION
      ↓
MIGRATION REQUIREMENTS
      ↓
ROADMAP
```

The project should then move into:

> **Day 1 — Strategy & Information Architecture**

---

# 19. Guiding Principle

The redesign should not simply make the existing website look newer.

The objective is to fundamentally improve how the market understands Anaxee.

> **From a traditional last-mile outreach company**
>
> **to a technology-powered intelligence, data, climate, influence, and execution network.**

The new digital platform should make that transformation immediately visible.
