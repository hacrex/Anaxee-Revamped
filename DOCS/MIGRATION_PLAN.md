# Anaxee Platform — Migration Strategy

## Overview

This document defines the strategy for migrating Anaxee's digital properties into the unified anaxee.com platform:

1. **Corporate Website** (anaxee.com) — WordPress
2. **Blog** (blog.anaxee.com) — WordPress
3. **Prabhavak** (prabhavak.anaxee.com) — Next.js
4. **Anaxee Tech** (anaxeetech.com) — Lovable (React) — *Retirement*

**Goal:** Zero traffic loss, preserved SEO equity, improved user experience.

**Related Documents:**
- [ROADMAP.md](./ROADMAP.md) — Implementation timeline
- [SITE_ARCHITECTURE.md](./SITE_ARCHITECTURE.md) — Target sitemap
- [TECH_STACK.md](./TECH_STACK.md) — Technology decisions
- [PRD.md](../PRD.md) — Product requirements

---

## 1. Current State Summary

### 1.1 Corporate Website (anaxee.com)

| Attribute | Value |
|-----------|-------|
| Platform | WordPress |
| URL Structure | Mixed (some clean, some parameterized) |
| Content Types | Pages, Services, About, Contact |
| SEO Status | Established domain authority |
| Analytics | Google Analytics (assumed) |
| Forms | Contact forms |
| Integrations | Analytics, possibly CRM |

**Key Risks:**
- Established domain authority must be preserved
- Existing backlinks must not break
- Contact forms must continue working
- Search rankings must be maintained

### 1.2 Blog (blog.anaxee.com)

| Attribute | Value |
|-----------|-------|
| Platform | WordPress |
| URL Structure | `/YYYY/MM/post-slug/` or `/post-slug/` |
| Content Types | Posts, Categories, Tags |
| SEO Status | Active content with organic traffic |
| Content Volume | TBD (audit required) |
| Categories | Multiple (audit required) |
| Tags | Multiple (audit required) |

**Key Risks:**
- Existing organic traffic to blog posts
- Backlinks to individual posts
- Category/tag page rankings
- Internal links from other sites

### 1.3 Prabhavak (prabhavak.anaxee.com)

| Attribute | Value |
|-----------|-------|
| Platform | Next.js + React + Tailwind CSS |
| URL Structure | App-like (SPA) |
| Content Type | Product/Platform experience |
| SEO Status | Limited (SPA limitations) |
| Functionality | Application backend |
| Authentication | User accounts |

**Key Risks:**
- Existing user accounts and sessions
- Application functionality must not break
- API dependencies
- Brand repositioning (product of Anaxee, not separate entity)

### 1.4 Anaxee Tech (anaxeetech.com)

| Attribute | Value |
|-----------|-------|
| Platform | Lovable (AI app builder) |
| URL Structure | Client-side rendered |
| Content Type | Unfinished prototype |
| SEO Status | Minimal (UUID title, no meta description) |
| Functionality | None (abandoned) |
| Status | **To be retired** |

**Key Risks:**
- Low/zero traffic — minimal risk
- Possible backlinks — check before retirement
- Brand confusion if discovered by prospects/investors
- Should 301 redirect to anaxee.com after launch

---

## 2. Migration Strategy by Property

### 2.1 Corporate Website Migration

#### Approach: Content Rewrite + URL Preservation

**Phase 1: Audit & Classification**
- Crawl all pages on anaxee.com
- Record URL, title, traffic, backlinks, conversions for each page
- Classify each page: KEEP / REWRITE / MERGE / REDIRECT / REMOVE

**Phase 2: Content Preparation**
- Rewrite content for KEEP and REWRITE pages
- Consolidate MERGE pages
- Prepare redirects for REMOVED pages
- Create new content for gaps

**Phase 3: Implementation**
- Build new pages in Next.js
- Implement 301 redirects for all changed URLs
- Test all forms and integrations
- Verify analytics tracking

**Page Classification Matrix:**

| Page | Current URL | Traffic | Backlinks | Action | New URL |
|------|------------|---------|-----------|--------|---------|
| Homepage | `/` | High | High | REWRITE | `/` |
| About | `/about/` | Medium | Medium | KEEP | `/company/about/` |
| Services | `/services/` | Medium | Medium | REWRITE | `/solutions/` |
| Contact | `/contact/` | Medium | Low | KEEP | `/contact/` |
| Team | `/team/` | Low | Low | MERGE | `/company/about/` |
| Careers | `/careers/` | Low | Low | REWRITE | `/company/careers/` |
| ... | ... | ... | ... | ... | ... |

#### Redirect Rules

```nginx
# 301 Redirects (nginx syntax for reference)
# Preserve as many existing URLs as possible

# Service pages → Solution pages
/location-services/ → /solutions/retail-intelligence/
/data-collection/ → /solutions/ai-data-collection/
/climate-services/ → /solutions/climate-and-carbon/
/influence/ → /solutions/influence-marketing/

# Company pages
/about-us/ → /company/about/
/about/ → /company/about/
/team/ → /company/about/
/careers/ → /company/careers/

# Contact
/contact-us/ → /contact/
/contact/ → /contact/
```

### 2.2 Blog Migration

#### Approach: Content Migration + URL Redirect

**Phase 1: Content Audit**
- Export all blog posts from WordPress
- Record: URL, title, date, author, categories, tags, traffic, backlinks
- Classify each post: MIGRATE / REWRITE / CONSOLIDATE / ARCHIVE

**Phase 2: Content Preparation**
- Map old categories to new content hub taxonomy
- Map old tags to new tag system
- Rewrite posts that need optimization
- Consolidate duplicate or near-duplicate content
- Archive low-value content

**Phase 3: Migration Implementation**
- Create new blog post schema in CMS
- Migrate content with proper formatting
- Migrate images and media assets
- Set up redirects for all changed URLs
- Test all internal links

**Blog URL Redirect Strategy:**

```nginx
# Blog URL patterns
# Old: /YYYY/MM/post-slug/ or /post-slug/
# New: /resources/blog/post-slug/

# Pattern 1: Direct path
/blog/post-slug/ → /resources/blog/post-slug/

# Pattern 2: Date-based
/2024/01/post-slug/ → /resources/blog/post-slug/

# Pattern 3: Category-based
/blog/category/retail/ → /resources/blog/category/retail-intelligence/
```

**Content Migration Priority:**

| Priority | Criteria | Action |
|----------|----------|--------|
| High | Posts with > 100 monthly organic visits | Migrate as-is with redirect |
| High | Posts with > 5 backlinks | Migrate as-is with redirect |
| High | Posts ranking top 10 for target keywords | Migrate as-is with redirect |
| Medium | Posts with 10–100 monthly visits | Rewrite + migrate |
| Medium | Posts < 12 months old | Migrate with redirect |
| Low | Posts with 0 traffic in 12 months | Archive or consolidate |
| Low | Duplicate content | Consolidate into canonical version |
| Low | Posts < 500 words with no value | Archive |

**Image Migration:**
- Download all blog images
- Upload to new image storage (Cloudinary or similar)
- Update image URLs in migrated content
- Optimize images for web (WebP format)

### 2.3 Prabhavak Migration

#### Approach: Landing Page + App Preservation

**Strategy:**
Prabhavak will NOT be fully migrated into the main site. Instead:

1. **Marketing/Landing Page** → `/products/prabhavak/` on anaxee.com
2. **Application** → Remains at prabhavak.anaxee.com (app functionality)
3. **Integration** → Header navigation links between main site and app

**Landing Page Content (`/products/prabhavak/`):**
- Product overview
- Features and benefits
- How it works
- Screenshots/demo
- Pricing or demo request
- Link to app (prabhavak.anaxee.com)
- Case studies using Prabhavak
- FAQ section

**What Stays on prabhavak.anaxee.com:**
- User authentication
- Application dashboard
- API endpoints
- User data and sessions

**What Moves to anaxee.com/products/prabhavak/:**
- Marketing content
- Product description
- Sales-focused messaging
- Demo request form

**Navigation Integration:**
```text
anaxee.com Header:
├── Products ▾
│   ├── Prabhavak → /products/prabhavak/
│   │   └── [Launch App →] prabhavak.anaxee.com
│   ├── Climate Command Centre → /products/climate-command-centre/
│   └── Retail Intelligence Platform → /products/retail-intelligence-platform/
```

### 2.4 Anaxee Tech Retirement

#### Approach: 301 Redirect to Main Domain

**Strategy:**
Anaxee Tech (anaxeetech.com) is an unfinished prototype that should be retired rather than migrated.

**Actions:**
1. **Before launch:** Check analytics/backlinks for any value
2. **At launch:** Set up 301 redirect from anaxeetech.com to anaxee.com
3. **After launch:** Monitor for any traffic or backlink issues

**Redirect Rules:**
```nginx
# anaxeetech.com → anaxee.com
# Wildcard redirect to preserve any traffic
server {
    server_name anaxeetech.com www.anaxeetech.com;
    return 301 https://anaxee.com$request_uri;
}
```

**Pre-Retirement Checklist:**
- [ ] Check Google Analytics for traffic volume
- [ ] Check Ahrefs/Moz for backlinks
- [ ] Verify no active integrations or API calls
- [ ] Confirm no internal team dependencies
- [ ] Set up 301 redirect to anaxee.com
- [ ] Monitor for 30 days post-redirect

---

## 3. Redirect Strategy

### 3.1 Redirect Rules

**Principle:** Every old URL must either:
1. Serve the same content at the same URL (ideal)
2. Redirect to the closest matching new URL (301)
3. Show a helpful 404 page with navigation (last resort)

### 3.2 Redirect Implementation

```javascript
// next.config.js redirects
module.exports = {
  async redirects() {
    return [
      // Corporate website redirects
      {
        source: '/about/',
        destination: '/company/about/',
        permanent: true,
      },
      {
        source: '/contact-us/',
        destination: '/contact/',
        permanent: true,
      },
      // ... more redirects

      // Blog redirects
      {
        source: '/blog/:slug',
        destination: '/resources/blog/:slug',
        permanent: true,
      },
      // ... more redirects
    ];
  },
};
```

**Note:** anaxeetech.com redirects must be configured at the DNS/ registrar level (not in Next.js) since it's a separate domain.

### 3.3 Redirect Testing

**Before Launch:**
- Generate complete redirect map
- Test every redirect manually
- Verify no redirect chains (A → B → C)
- Verify no redirect loops (A → B → A)
- Test with curl or similar tool

**After Launch:**
- Monitor 404 errors for 30 days
- Check Search Console for crawl errors
- Fix any missed redirects immediately
- Update any external links you control

---

## 4. SEO Preservation Strategy

### 4.1 Pre-Migration SEO Checklist

- [ ] Export Search Console data (top pages, top queries)
- [ ] Export all backlinks (Ahrefs, Moz, or similar)
- [ ] Document current rankings for target keywords
- [ ] Document current organic traffic (GA4)
- [ ] Create full URL inventory with status codes
- [ ] Identify high-value pages (traffic + backlinks)
- [ ] Map old URLs to new URLs
- [ ] Prepare redirect rules
- [ ] Set up staging environment for testing

### 4.2 During Migration

- [ ] Implement 301 redirects for all changed URLs
- [ ] Preserve meta titles and descriptions
- [ ] Preserve H1 tags
- [ ] Preserve internal linking structure
- [ ] Preserve schema markup
- [ ] Preserve Open Graph tags
- [ ] Keep analytics tracking codes
- [ ] Test all pages on staging before launch

### 4.3 Post-Migration SEO

- [ ] Submit updated XML sitemap to Search Console
- [ ] Request re-indexing of key pages
- [ ] Monitor 404 errors daily for first week
- [ ] Monitor organic traffic daily for first month
- [ ] Monitor keyword rankings weekly for first month
- [ ] Fix any redirect issues immediately
- [ ] Update any external backlinks you control
- [ ] Submit updated sitemap to Bing Webmaster Tools

### 4.4 SEO Monitoring Dashboard

**Daily (First 2 Weeks):**
- 404 error count
- Crawl error count
- Organic traffic
- Index status

**Weekly (First Month):**
- Keyword rankings
- Backlink profile
- Organic traffic trend
- Conversion rate

**Monthly (Ongoing):**
- Overall organic traffic
- Top performing pages
- New backlinks
- AI search visibility

---

## 5. Content Migration Checklist

### 5.1 Pre-Migration

- [ ] Complete content inventory for all properties
- [ ] Classify all content (KEEP / REWRITE / MERGE / REDIRECT / REMOVE)
- [ ] Map old taxonomy to new taxonomy
- [ ] Identify content gaps
- [ ] Prepare content for new CMS schema
- [ ] Set up CMS content models
- [ ] Set up image/media storage

### 5.2 Migration Execution

- [ ] Migrate corporate website pages
- [ ] Migrate blog posts (high priority first)
- [ ] Migrate case studies
- [ ] Migrate images and media
- [ ] Migrate author profiles
- [ ] Migrate categories and tags
- [ ] Set up redirects
- [ ] Test all content rendering

### 5.3 Post-Migration Verification

- [ ] Verify all pages render correctly
- [ ] Verify all images load
- [ ] Verify all links work
- [ ] Verify all forms function
- [ ] Verify analytics tracking
- [ ] Verify SEO meta tags
- [ ] Verify schema markup
- [ ] Verify redirect rules

---

## 6. Technology Migration

### 6.1 WordPress to Next.js

**Data Export:**
- Export all posts, pages, and custom post types
- Export media library
- Export user data (if applicable)
- Export comments (if applicable)
- Export redirects (if any existing)

**Data Import:**
- Import into new CMS (Sanity/Strapi/Contentful)
- Map WordPress fields to CMS schema
- Transform content format if needed
- Import media assets
- Verify data integrity

### 6.2 Analytics Migration

**GA4:**
- Keep existing GA4 property
- Update tracking code placement
- Set up new events for new platform
- Verify cross-domain tracking
- Create new views/reports

**Search Console:**
- Verify new site in Search Console
- Submit updated sitemap
- Monitor indexing status
- Track search performance

**Microsoft Clarity:**
- Install Clarity on new platform
- Set up heatmaps for key pages
- Monitor session recordings

### 6.3 Form Migration

- Document all existing forms
- Map form fields to new structure
- Integrate with existing CRM/email
- Test all form submissions
- Verify email notifications
- Test error handling

### 6.4 Integration Migration

| Integration | Action | Priority |
|------------|--------|----------|
| Google Analytics | Keep property, update tracking | High |
| Search Console | Verify new site, submit sitemap | High |
| CRM | Update form endpoints | High |
| Email Service | Update integration | Medium |
| WhatsApp | Re-integrate | Medium |
| Social Media | Update links | Low |
| Maps | Re-integrate | Low |

---

## 7. Testing Strategy

### 7.1 Staging Environment

- Deploy new site to staging URL
- Test all pages and functionality
- Test all forms
- Test all redirects
- Test analytics tracking
- Test performance
- Test accessibility
- Get stakeholder approval

### 7.2 Pre-Launch Testing

**Functional Testing:**
- [ ] All pages load correctly
- [ ] All navigation works
- [ ] All forms submit
- [ ] All CTAs function
- [ ] All links work
- [ ] Search functionality works
- [ ] Filter functionality works
- [ ] Dark mode toggle works

**SEO Testing:**
- [ ] All redirects work (301)
- [ ] No redirect chains
- [ ] No redirect loops
- [ ] XML sitemap valid
- [ ] robots.txt correct
- [ ] Meta tags present on all pages
- [ ] Schema markup valid
- [ ] Open Graph tags present
- [ ] Canonical URLs correct

**Performance Testing:**
- [ ] Lighthouse score > 90
- [ ] Core Web Vitals passing
- [ ] Page load time < 2 seconds
- [ ] Image optimization verified
- [ ] Font loading optimized
- [ ] JavaScript bundle size acceptable

**Accessibility Testing:**
- [ ] Keyboard navigation works
- [ ] Screen reader compatible
- [ ] Color contrast passing
- [ ] Focus states visible
- [ ] Alt text present on all images
- [ ] Form labels present

**Cross-Browser Testing:**
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)
- [ ] Mobile Chrome
- [ ] Mobile Safari

---

## 8. Rollback Plan

### 8.1 Rollback Triggers

- Critical bugs affecting > 10% of users
- Complete analytics tracking failure
- Form submission failures
- SEO ranking drops > 20%
- Core Web Vitals failing
- Security vulnerability discovered

### 8.2 Rollback Process

1. **Decision:** Team lead decides to rollback
2. **DNS:** Revert DNS to old WordPress site
3. **Verification:** Verify old site is accessible
4. **Communication:** Notify stakeholders
5. **Investigation:** Identify and fix root cause
6. **Re-attempt:** Fix issues and re-deploy

### 8.3 Rollback Timeline

- DNS propagation: 5–30 minutes
- Old site verification: 5 minutes
- Total rollback time: < 1 hour

---

## 9. Migration Timeline

| Week | Activity |
|------|----------|
| 1 | Content audit and classification (all 4 properties) |
| 2 | CMS setup and content model |
| 3 | Redirect map creation (including anaxeetech.com) |
| 4–6 | Content migration (high priority) |
| 6–8 | Content migration (medium priority) |
| 8–10 | Staging deployment and testing |
| 10 | Redirect testing |
| 11 | Stakeholder review |
| 12 | Launch preparation |
| 13 | Launch |
| 14–16 | Post-launch monitoring and fixes |
| 14–16 | anaxeetech.com 301 redirect activation and monitoring |

---

## 10. Risk Register

| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|------------|
| SEO traffic loss | High | Medium | Comprehensive redirects, monitor closely |
| Broken backlinks | High | Medium | Redirect mapping, outreach for updates |
| Content formatting issues | Medium | High | Thorough testing, manual review |
| Form failures | High | Low | Test all forms on staging |
| Image loading issues | Medium | Medium | Verify all images in staging |
| Analytics tracking gaps | Medium | Medium | Verify tracking before launch |
| CMS data loss | High | Low | Regular backups, version control |
| Redirect chains | Medium | Medium | Automated redirect testing |
| Mobile responsiveness | Medium | Medium | Test on real devices |
| Performance regression | Medium | Low | Performance budget, Lighthouse CI |
| anaxeetech.com redirect failure | Low | Low | Simple 301, minimal content on domain |

---

## 11. Communication Plan

### Pre-Launch

| Audience | Message | Timing |
|----------|---------|--------|
| Internal Team | Migration timeline and responsibilities | Week 1 |
| Stakeholders | Migration plan and expected outcomes | Week 2 |
| Content Team | Content preparation requirements | Week 3 |
| Partners | Upcoming website changes | Week 10 |
| Clients | New website launch announcement | Week 12 |

### Launch Day

| Audience | Message | Channel |
|----------|---------|---------|
| Internal Team | Launch status updates | Slack/Teams |
| Stakeholders | Launch confirmation | Email |
| Social Media | New website announcement | LinkedIn, Twitter |
| Email Subscribers | New website launch email | Newsletter |

### Post-Launch

| Audience | Message | Timing |
|----------|---------|--------|
| Internal Team | Performance metrics | Daily (Week 1) |
| Stakeholders | Performance report | Weekly (Month 1) |
| Partners | Updated links and resources | Week 1 |
| Content Team | Training and guidelines | Week 1–2 |
