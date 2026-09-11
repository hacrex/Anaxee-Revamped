# Anaxee Platform — Phased Implementation Roadmap

## Overview

This roadmap outlines the phased approach to transform Anaxee's fragmented digital presence into a unified, modern, enterprise-grade platform. Each phase builds upon the previous one, with clear deliverables and decision gates.

---

## Phase 0 — Discovery & Foundation (Weeks 1–2)

**Goal:** Establish baseline understanding, finalize decisions, and prepare the project foundation.

### Activities

- Audit all existing properties (anaxee.com, blog.anaxee.com, prabhavak.anaxee.com)
- Capture SEO baseline (Search Console exports, top pages, top queries, backlinks)
- Capture Analytics baseline (GA4 data, traffic sources, conversion events, device split)
- Complete content inventory across all three properties
- Brand audit (logo, colors, typography, tone of voice across all properties)
- Technology audit (WordPress versions, plugins, hosting, Prabhavak stack)
- Infrastructure inventory (DNS, domains, SSL, CI/CD, integrations)
- Competitor and inspiration research (10–15 reference sites)
- Finalize brand positioning ("India's Reach Engine")
- Finalize information architecture (see SITE_ARCHITECTURE.md)
- Finalize technology stack decisions (see TECH_STACK.md)
- Document migration risks and mitigation strategies (see MIGRATION_PLAN.md)

### Deliverables

- [ ] SEO baseline report
- [ ] Analytics baseline report
- [ ] Complete content inventory spreadsheet
- [ ] Brand audit document
- [ ] Technology audit document
- [ ] Infrastructure map
- [ ] Integration inventory
- [ ] Finalized sitemap
- [ ] Finalized IA
- [ ] Technology stack decision document
- [ ] Migration risk register

### Decision Gates

- CMS selection finalized
- Hosting platform finalized
- Brand positioning approved
- IA approved
- Migration strategy approved

---

## Phase 1 — Design System & Brand (Weeks 3–5)

**Goal:** Establish the visual foundation that all pages and components will build upon.

### Activities

- Define color palette (primary, secondary, accent, semantic colors)
- Select and configure typography (heading font, body font, monospace)
- Design core component library (buttons, cards, inputs, navigation, modals)
- Create logo usage guidelines
- Define spacing, grid, and layout system
- Create iconography guidelines
- Define motion and animation principles
- Design responsive breakpoints and mobile-first patterns
- Create Figma/design file with all components
- Establish design token system for Tailwind CSS integration

### Deliverables

- [ ] DESIGN_SYSTEM.md (see DOCS/DESIGN_SYSTEM.md)
- [ ] Tailwind CSS configuration with design tokens
- [ ] Figma component library
- [ ] Color palette documentation
- [ ] Typography scale documentation
- [ ] Component specifications

### Decision Gates

- Design system approved by stakeholders
- Tailwind configuration finalized
- Component library approved

---

## Phase 2 — Technical Foundation (Weeks 4–6)

**Goal:** Set up the project skeleton, tooling, CI/CD, and core infrastructure.

### Activities

- Initialize Next.js project with TypeScript and App Router
- Configure Tailwind CSS with design tokens
- Set up ESLint, Prettier, and Husky pre-commit hooks
- Configure TypeScript strict mode
- Set up CMS (Sanity recommended) with initial schema
- Configure Vercel deployment with preview environments
- Set up Google Analytics 4, Search Console, and Microsoft Clarity
- Create base layout components (Header, Footer, Navigation, Layout)
- Set up internationalization (i18n) framework for future global expansion
- Configure image optimization pipeline (Next.js Image + Cloudinary or similar)
- Set up error monitoring (Sentry or similar)
- Create .env.example with all required environment variables
- Set up GitHub Actions CI/CD pipeline

### Deliverables

- [ ] Next.js project scaffolded
- [ ] Tailwind configured with design tokens
- [ ] CI/CD pipeline operational
- [ ] CMS configured with base schemas
- [ ] Vercel deployment working
- [ ] Analytics integration verified
- [ ] Base layout components built
- [ ] .env.example documented

### Decision Gates

- CI/CD pipeline passes
- CMS schemas approved
- Deployment workflow verified

---

## Phase 3 — Core Pages & Components (Weeks 6–10)

**Goal:** Build all primary page templates and reusable components.

### Activities

#### Homepage
- Dynamic hero section with animated counters
- Interactive India coverage map (26+ states, 540+ districts, 11,000+ pincodes)
- Digital Runner network showcase with live counters
- Solution overview cards
- Industry highlights
- Client logos carousel
- Testimonial section
- CTA sections (Contact, Demo, etc.)

#### Solution Pages (5 pages)
- Retail Intelligence
- AI Data Collection
- Climate & Carbon
- GTM Services
- Influence Marketing

Each page includes:
- Hero with solution-specific imagery
- Problem statement
- How Anaxee solves it
- Key features/capabilities
- Metrics and impact data
- Related case studies
- CTA

#### Product Pages (3 pages)
- Prabhavak (Influence Marketing Platform)
- Climate Command Centre
- Retail Intelligence Platform

#### Industry Pages (5 pages)
- FMCG
- Agriculture
- Automotive
- Climate
- Government

#### Case Studies Library
- Case study listing page with filters
- Individual case study template
- Filter by industry, geography, solution, client type

#### Company Pages
- About Anaxee
- Impact page (public dashboard)
- Network (Digital Runner showcase)
- Careers

#### Contact Page
- Multi-purpose contact form
- Office locations
- WhatsApp integration

### Deliverables

- [ ] Homepage built and responsive
- [ ] 5 solution pages
- [ ] 3 product pages
- [ ] 5 industry pages
- [ ] Case study library
- [ ] Company pages
- [ ] Contact page
- [ ] All components responsive across breakpoints

### Decision Gates

- All pages reviewed and approved
- Mobile responsiveness verified
- Accessibility audit passed
- Performance benchmarks met

---

## Phase 4 — Content Platform & Blog (Weeks 8–12)

**Goal:** Transform the blog into a knowledge platform integrated into the main site.

### Activities

- Build blog listing page with category/tag filtering
- Build individual blog post template with:
  - Author bio
  - Related articles
  - Social sharing
  - Reading time estimate
  - Table of contents for long-form content
- Create 7 content hubs:
  - Retail Intelligence
  - AI Data Collection
  - Climate & Carbon
  - Influence Marketing
  - Rural Market Intelligence
  - GTM Strategy
  - Data Verification
- Build research center section:
  - Reports listing and detail pages
  - Whitepapers listing and detail pages
- Implement SEO features:
  - Dynamic meta titles and descriptions
  - Open Graph and Twitter Card tags
  - JSON-LD structured data
  - Canonical URLs
  - XML sitemap generation
- Set up content migration pipeline from WordPress

### Deliverables

- [ ] Blog listing page
- [ ] Blog post template
- [ ] 7 content hub pages
- [ ] Research center pages
- [ ] SEO meta system
- [ ] Structured data implementation
- [ ] XML sitemap
- [ ] Content migration scripts

### Decision Gates

- Blog design approved
- Content hub taxonomy finalized
- SEO implementation verified
- Migration scripts tested

---

## Phase 5 — Content Migration (Weeks 10–14)

**Goal:** Migrate all existing content from WordPress and Prabhavak to the new platform.

### Activities

- Migrate blog articles from blog.anaxee.com
  - Map categories and tags to new taxonomy
  - Preserve URLs where possible
  - Set up redirects for changed URLs
  - Migrate images and media
- Migrate corporate content from anaxee.com
  - Rewrite and restructure service pages
  - Migrate case studies
  - Migrate team/about content
  - Migrate contact information
- Migrate Prabhavak content from prabhavak.anaxee.com
  - Reposition as product page under anaxee.com/products/prabhavak
  - Preserve Prabhavak app functionality on subdomain
  - Create marketing/landing page on main site
- Set up comprehensive redirect map (301 redirects)
- Verify all migrated content renders correctly
- Check all internal links
- Verify image/media loading

### Deliverables

- [ ] All blog content migrated
- [ ] All corporate content migrated
- [ ] Prabhavak landing page created
- [ ] Redirect map implemented
- [ ] Content verification complete
- [ ] 404 error check complete
- [ ] Internal link audit complete

### Decision Gates

- All content migrated and verified
- No broken links
- Redirects tested and working
- SEO equity preserved (no traffic drops)

---

## Phase 6 — Advanced Features & Integrations (Weeks 12–16)

**Goal:** Implement advanced features, interactive elements, and third-party integrations.

### Activities

- Build interactive India coverage map with drill-down
- Build public impact dashboard with animated counters
- Implement scroll-based storytelling sections
- Build Digital Runner network showcase page
- Implement search functionality across all content
- Set up email newsletter integration
- Build downloadable resources section (gated and ungated)
- Implement WhatsApp chat integration
- Build careers/jobs section
- Implement multi-step contact/demo request forms
- Set up marketing automation integration
- Build sitemap pages for human navigation
- Implement dark mode toggle (optional)

### Deliverables

- [ ] Interactive India map
- [ ] Impact dashboard
- [ ] Search functionality
- [ ] Newsletter integration
- [ ] WhatsApp integration
- [ ] Careers section
- [ ] Multi-step forms

### Decision Gates

- All integrations tested
- Performance benchmarks met
- User acceptance testing passed

---

## Phase 7 — SEO, GEO & AI Optimization (Weeks 14–17)

**Goal:** Maximize search visibility across traditional search engines and AI-powered platforms.

### Activities

- Implement comprehensive schema markup:
  - Organization
  - Website
  - BreadcrumbList
  - Article
  - Product
  - FAQPage
  - HowTo
  - LocalBusiness
- Create GEO-optimized pages:
  - "What is Digital MRV?"
  - "What is Last-Mile Execution?"
  - "What is Retail Intelligence?"
  - "What is Rural Market Research?"
  - "What is Carbon Project Verification?"
- Optimize content structure for AI search:
  - Clear entity definitions
  - Structured headings
  - FAQ sections on key pages
  - Research-based content
- Set up Google Search Console monitoring
- Configure robots.txt and XML sitemap
- Implement canonical URLs
- Set up internal linking strategy
- Optimize page speed for Core Web Vitals
- Create topic clusters across content hubs

### Deliverables

- [ ] Schema markup on all pages
- [ ] GEO landing pages (5+)
- [ ] robots.txt configured
- [ ] XML sitemap submitted
- [ ] Internal linking strategy implemented
- [ ] Core Web Vitals passing
- [ ] Topic clusters mapped and linked

### Decision Gates

- Core Web Vitals all green
- Schema validation passing
- GEO content reviewed
- AI search visibility baseline established

---

## Phase 8 — Testing & QA (Weeks 16–18)

**Goal:** Comprehensive testing across all devices, browsers, and scenarios.

### Activities

- Cross-browser testing (Chrome, Firefox, Safari, Edge)
- Responsive testing (mobile, tablet, desktop)
- Accessibility audit (WCAG 2.1 AA compliance)
- Performance testing (Lighthouse scores > 90)
- SEO audit (all pages)
- Link checking (internal and external)
- Form submission testing
- Analytics event verification
- CMS workflow testing
- Content accuracy review
- Security audit
- Load testing
- Uptime monitoring setup

### Deliverables

- [ ] Cross-browser test report
- [ ] Responsive test report
- [ ] Accessibility audit report
- [ ] Lighthouse performance report
- [ ] SEO audit report
- [ ] Form testing report
- [ ] Analytics verification report
- [ ] Security audit report

### Decision Gates

- All critical issues resolved
- Lighthouse scores > 90
- WCAG 2.1 AA compliance
- Zero broken links
- All forms functional

---

## Phase 9 — Launch Preparation (Weeks 18–19)

**Goal:** Prepare for production launch with all safety nets in place.

### Activities

- Set up production environment
- Configure DNS and SSL certificates
- Set up CDN (Vercel Edge Network or Azure CDN)
- Configure monitoring and alerting
- Set up uptime monitoring
- Prepare rollback plan
- Create launch communication plan
- Brief stakeholders on new platform
- Train content team on CMS
- Prepare redirect testing checklist
- Set up 404 monitoring
- Create post-launch monitoring dashboard

### Deliverables

- [ ] Production environment live
- [ ] DNS configured
- [ ] SSL verified
- [ ] Monitoring active
- [ ] Rollback plan documented
- [ ] CMS training complete
- [ ] Launch checklist completed

### Decision Gates

- All pre-launch checklist items verified
- Stakeholder sign-off obtained
- Content team trained
- Rollback plan tested

---

## Phase 10 — Launch & Post-Launch (Weeks 19–20+)

**Goal:** Execute launch and monitor performance in the critical post-launch period.

### Activities

#### Launch Day
- Deploy to production
- Verify all pages loading correctly
- Test all forms and CTAs
- Verify analytics tracking
- Verify search console indexing
- Monitor error rates
- Monitor performance metrics
- Communicate launch to stakeholders

#### Post-Launch (Week 1–4)
- Monitor Google Analytics for traffic changes
- Monitor Search Console for indexing issues
- Monitor for 404 errors
- Track conversion rates
- Gather stakeholder feedback
- Fix any post-launch issues
- Submit updated sitemap to search engines
- Monitor Core Web Vitals

#### Post-Launch (Month 2–3)
- Analyze performance vs baseline
- Identify content gaps
- Plan content calendar
- Optimize based on user data
- Plan Phase 2 features
- Monitor AI search visibility

### Deliverables

- [ ] Launch day verification complete
- [ ] Post-launch monitoring report (daily for first week)
- [ ] Performance comparison report (vs baseline)
- [ ] Issue tracking and resolution log
- [ ] Content calendar for month 2–3
- [ ] Phase 2 feature roadmap

---

## Timeline Summary

| Phase | Name | Duration | Weeks |
|-------|------|----------|-------|
| 0 | Discovery & Foundation | 2 weeks | 1–2 |
| 1 | Design System & Brand | 3 weeks | 3–5 |
| 2 | Technical Foundation | 3 weeks | 4–6 |
| 3 | Core Pages & Components | 5 weeks | 6–10 |
| 4 | Content Platform & Blog | 5 weeks | 8–12 |
| 5 | Content Migration | 5 weeks | 10–14 |
| 6 | Advanced Features | 5 weeks | 12–16 |
| 7 | SEO, GEO & AI Optimization | 4 weeks | 14–17 |
| 8 | Testing & QA | 3 weeks | 16–18 |
| 9 | Launch Preparation | 2 weeks | 18–19 |
| 10 | Launch & Post-Launch | 2+ weeks | 19–20+ |

**Total estimated duration: 20 weeks (5 months)**

Note: Phases overlap intentionally. Phases 3–7 run partially in parallel with different team members working on different areas.

---

## Risk Factors

| Risk | Impact | Mitigation |
|------|--------|------------|
| CMS selection delays | Phase 2 delayed | Make CMS decision in Phase 0 |
| Content migration complexity | Phase 5 delayed | Start migration scripts early |
| SEO traffic loss during migration | Business impact | Preserve URLs, implement redirects, monitor closely |
| Scope creep | Timeline delays | Strict phase gates, MVP mindset |
| Brand decision delays | Phase 1 delayed | Get brand approval in Phase 0 |
| Third-party integration issues | Phase 6 delayed | Test integrations early |
| Performance issues | Phase 8 delays | Performance budgets from Phase 2 |

---

## Success Criteria

### Launch Success

- All pages loading correctly
- All forms functional
- Zero critical bugs
- Analytics tracking verified
- Search console indexing confirmed
- Redirects working correctly

### 30-Day Post-Launch Success

- Organic traffic maintained or improved
- No significant ranking drops
- Conversion rates maintained or improved
- Core Web Vitals all green
- Zero critical post-launch issues

### 90-Day Post-Launch Success

- Organic traffic growth
- Improved keyword rankings
- AI search visibility improved
- Lead generation improved
- Stakeholder satisfaction confirmed
