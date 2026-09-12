# Anaxee Platform — Pre-Launch & Post-Launch Checklist

## Overview

Comprehensive checklist for launching the Anaxee digital platform, covering pre-launch preparation through post-launch monitoring.

**Properties Managed:**
- anaxee.com (main site)
- blog.anaxee.com (redirected to anaxee.com)
- prabhavak.anaxee.com (app remains, marketing page on main site)
- anaxeetech.com (retired, 301 redirect to anaxee.com)

**Related Documents:**
- [ROADMAP.md](./ROADMAP.md) — Implementation timeline
- [MIGRATION_PLAN.md](./MIGRATION_PLAN.md) — Migration strategy
- [PRD.md](../PRD.md) — Product requirements

---

## Phase 1: Pre-Launch (2–4 Weeks Before)

### Content Readiness

- [ ] All pages written and reviewed
- [ ] All blog posts migrated from blog.anaxee.com
- [ ] All case studies created
- [ ] All images optimized (WebP, correct sizes)
- [ ] All alt text added to images
- [ ] All internal links verified
- [ ] All external links verified
- [ ] All forms tested
- [ ] All CTAs reviewed and functional
- [ ] Legal pages complete (Privacy, Terms, Cookies)
- [ ] All author profiles created
- [ ] All categories and tags mapped
- [ ] Content reviewed by stakeholders

### SEO Readiness

- [ ] Meta titles on all pages (50–60 chars)
- [ ] Meta descriptions on all pages (150–160 chars)
- [ ] H1 tags on all pages (one per page)
- [ ] H2–H6 hierarchy correct
- [ ] Schema markup on all pages
- [ ] Open Graph tags on all pages
- [ ] Twitter Card tags on all pages
- [ ] Canonical URLs set
- [ ] XML sitemap generated and accessible
- [ ] robots.txt configured correctly
- [ ] Internal linking strategy implemented
- [ ] Topic clusters linked
- [ ] Breadcrumbs on all pages
- [ ] No duplicate content
- [ ] No orphan pages

### Technical Readiness

- [ ] All pages render correctly
- [ ] All navigation works (desktop + mobile)
- [ ] All forms submit correctly
- [ ] All CTAs function
- [ ] Search functionality works
- [ ] Filter functionality works
- [ ] Dark mode toggle works
- [ ] Responsive design verified (mobile, tablet, desktop)
- [ ] Cross-browser tested (Chrome, Firefox, Safari, Edge)
- [ ] Accessibility audit passed (WCAG 2.1 AA)
- [ ] Lighthouse score > 90 (all categories)
- [ ] Core Web Vitals passing
- [ ] Page load time < 2 seconds
- [ ] No JavaScript errors in console
- [ ] No broken links
- [ ] 404 page designed and functional

### Redirect Readiness

- [ ] All redirects mapped (old URL to new URL)
- [ ] All redirects implemented
- [ ] All redirects tested (no chains, no loops)
- [ ] Redirect rules documented
- [ ] All redirects are 301 (permanent)
- [ ] anaxeetech.com 301 redirect configured at DNS level
- [ ] anaxeetech.com redirect tested (resolves to anaxee.com)
- [ ] blog.anaxee.com redirect rules configured
- [ ] prabhavak.anaxee.com navigation links verified

### Analytics Readiness

- [ ] Google Analytics 4 installed
- [ ] GA4 events configured
- [ ] Google Search Console verified
- [ ] Sitemap submitted to Search Console
- [ ] Microsoft Clarity installed
- [ ] Vercel Analytics enabled
- [ ] Sentry error tracking installed
- [ ] Custom events tracking verified
- [ ] Conversion events defined

### Integration Readiness

- [ ] CRM integration tested
- [ ] Email service integration tested
- [ ] WhatsApp integration tested
- [ ] Social media links verified
- [ ] Newsletter signup functional
- [ ] Form submissions reaching CRM
- [ ] Email notifications working

### Infrastructure Readiness

- [ ] Production environment configured
- [ ] DNS configured for anaxee.com
- [ ] SSL certificate installed and verified
- [ ] CDN configured (Vercel Edge Network)
- [ ] Caching strategy implemented
- [ ] Environment variables set in Vercel
- [ ] Build pipeline working
- [ ] Deployment pipeline working
- [ ] Monitoring configured
- [ ] Alerting configured

### Security Readiness

- [ ] Security headers configured
- [ ] Content Security Policy set
- [ ] HTTPS enforced
- [ ] No sensitive data in client-side code
- [ ] API keys secured (server-side only)
- [ ] No secrets in git history
- [ ] Dependencies audited
- [ ] No known vulnerabilities

### Stakeholder Readiness

- [ ] Stakeholder approval obtained
- [ ] Content team trained on CMS
- [ ] Development team briefed on maintenance
- [ ] Support team briefed on new platform
- [ ] Communication plan prepared
- [ ] Rollback plan reviewed

---

## Phase 2: Launch Day

### Pre-Deployment

- [ ] Final staging review complete
- [ ] All team members available
- [ ] Communication channels open
- [ ] Rollback plan reviewed
- [ ] DNS TTL reduced (if applicable)

### Deployment

- [ ] Deploy to production
- [ ] Verify deployment successful
- [ ] Verify build completed without errors
- [ ] Verify environment variables loaded

### Post-Deployment Verification

- [ ] Homepage loads correctly
- [ ] All navigation links work
- [ ] All pages load correctly
- [ ] All forms submit
- [ ] All CTAs function
- [ ] Search works
- [ ] Dark mode works
- [ ] Mobile navigation works
- [ ] 404 page works
- [ ] Redirects work

### Analytics Verification

- [ ] GA4 tracking fires on page load
- [ ] Search Console indexing initiated
- [ ] Clarity recording active
- [ ] Vercel Analytics showing data
- [ ] Sentry capturing errors (if any)

### SEO Verification

- [ ] XML sitemap accessible at /sitemap.xml
- [ ] robots.txt accessible at /robots.txt
- [ ] Canonical URLs correct
- [ ] Meta tags present
- [ ] Schema markup valid
- [ ] No 404 errors on key pages
- [ ] No redirect issues

### DNS and SSL

- [ ] anaxee.com resolves correctly
- [ ] www.anaxee.com resolves correctly
- [ ] anaxeetech.com redirects to anaxee.com (301)
- [ ] blog.anaxee.com redirects work correctly
- [ ] prabhavak.anaxee.com resolves correctly
- [ ] SSL certificate valid on all domains
- [ ] HTTPS enforced on all domains
- [ ] No mixed content warnings

### Performance Verification

- [ ] Lighthouse score > 90
- [ ] Core Web Vitals passing
- [ ] Page load time < 2 seconds
- [ ] Image optimization working
- [ ] Font loading optimized

---

## Phase 3: Post-Launch (Week 1)

### Daily Monitoring

- [ ] Monitor 404 errors
- [ ] Monitor analytics traffic
- [ ] Monitor Search Console for crawl errors
- [ ] Monitor Sentry for errors
- [ ] Check form submissions
- [ ] Verify redirects working
- [ ] Check social media links

### Issue Resolution

- [ ] Fix any 404 errors
- [ ] Fix any broken links
- [ ] Fix any redirect issues
- [ ] Fix any form issues
- [ ] Fix any visual issues
- [ ] Fix any performance issues

### SEO Monitoring

- [ ] Check indexing status in Search Console
- [ ] Monitor organic traffic
- [ ] Check keyword rankings
- [ ] Verify sitemap submitted
- [ ] Request indexing for key pages

---

## Phase 4: Post-Launch (Week 2–4)

### Weekly Reviews

- [ ] Review analytics trends
- [ ] Review Search Console data
- [ ] Review Clarity heatmaps
- [ ] Review error logs
- [ ] Review conversion rates
- [ ] Gather stakeholder feedback

### Content Optimization

- [ ] Identify content gaps
- [ ] Plan content calendar
- [ ] Optimize underperforming pages
- [ ] Update any outdated content
- [ ] Create new content based on data

### Performance Optimization

- [ ] Optimize slow pages
- [ ] Optimize images
- [ ] Optimize JavaScript bundles
- [ ] Review caching strategy
- [ ] Monitor Core Web Vitals

---

## Phase 5: Post-Launch (Month 2–3)

### Performance Review

- [ ] Compare traffic vs baseline
- [ ] Compare conversions vs baseline
- [ ] Compare rankings vs baseline
- [ ] Identify improvement areas
- [ ] Plan next phase features

### Content Strategy

- [ ] Execute content calendar
- [ ] Publish new blog posts
- [ ] Create new case studies
- [ ] Update existing content
- [ ] Monitor content performance

### SEO Strategy

- [ ] Build topic clusters
- [ ] Create new insight pages
- [ ] Build backlinks
- [ ] Monitor keyword rankings
- [ ] Optimize for AI search

---

## Rollback Checklist

If critical issues are discovered:

- [ ] Decision to rollback made
- [ ] DNS reverted to old site
- [ ] Old site verified as accessible
- [ ] Stakeholders notified
- [ ] Issue investigated
- [ ] Fix prepared
- [ ] Re-deployment planned

### Rollback Triggers

- Critical bugs affecting > 10% of users
- Complete analytics tracking failure
- Form submission failures across all forms
- SEO ranking drops > 20%
- Core Web Vitals failing
- Security vulnerability discovered

---

## Sign-Off

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Project Lead | | | |
| Tech Lead | | | |
| Content Lead | | | |
| SEO Lead | | | |
| Stakeholder | | | |
