# Anaxee Platform — Technology Stack Decisions

## Overview

This document defines the complete technology stack for the Anaxee digital platform, including frontend framework, CMS, hosting, analytics, and all supporting tools and services.

---

## 1. Frontend Stack

### 1.1 Core Framework

| Decision | Choice | Rationale |
|----------|--------|-----------|
| **Framework** | Next.js 14+ (App Router) | React-based, SSR/SSG, excellent DX, Vercel ecosystem |
| **Language** | TypeScript | Type safety, better DX, fewer runtime errors |
| **UI Library** | React 18+ | Component-based architecture, massive ecosystem |
| **Styling** | Tailwind CSS | Utility-first, design token integration, rapid development |
| **Package Manager** | pnpm | Fast, disk-efficient, strict dependency management |

**Why Next.js over alternatives:**
- **vs. Gatsby:** Better performance, simpler API, active development, Vercel support
- **vs. Remix:** More mature ecosystem, better static generation, larger community
- **vs. Nuxt:** React ecosystem larger than Vue, better TypeScript support
- **vs. Static-only (Astro):** Need React interactivity for maps, dashboards, forms

### 1.2 Next.js Configuration

```javascript
// next.config.mjs
/** @type {import('next').NextConfig} */
const nextConfig = {
  // Enable React Strict Mode
  reactStrictMode: true,

  // Image optimization
  images: {
    formats: ['image/avif', 'image/webp'],
    remotePatterns: [
      {
        protocol: 'https',
        hostname: 'cdn.sanity.io',
      },
    ],
  },

  // Headers for security
  async headers() {
    return [
      {
        source: '/(.*)',
        headers: [
          { key: 'X-Frame-Options', value: 'DENY' },
          { key: 'X-Content-Type-Options', value: 'nosniff' },
          { key: 'Referrer-Policy', value: 'strict-origin-when-cross-origin' },
        ],
      },
    ];
  },

  // Redirects (from migration plan)
  async redirects() {
    return [
      // Corporate website redirects
      {
        source: '/about/',
        destination: '/company/about/',
        permanent: true,
      },
      // Blog redirects
      {
        source: '/blog/:slug',
        destination: '/resources/blog/:slug',
        permanent: true,
      },
    ];
  },
};

export default nextConfig;
```

### 1.3 Tailwind CSS Configuration

```javascript
// tailwind.config.ts
import type { Config } from 'tailwindcss';

const config: Config = {
  content: [
    './src/pages/**/*.{js,ts,jsx,tsx,mdx}',
    './src/components/**/*.{js,ts,jsx,tsx,mdx}',
    './src/app/**/*.{js,ts,jsx,tsx,mdx}',
  ],
  darkMode: 'class',
  theme: {
    extend: {
      colors: {
        anaxee: {
          blue: '#1E40AF',
          dark: '#0F172A',
          white: '#FFFFFF',
        },
        electric: '#3B82F6',
        teal: '#14B8A6',
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        mono: ['JetBrains Mono', 'monospace'],
      },
      maxWidth: {
        content: '80rem',
      },
    },
  },
  plugins: [],
};

export default config;
```

---

## 2. CMS (Content Management System)

### 2.1 CMS Evaluation

| Criteria | Sanity | Strapi | Contentful |
|----------|--------|--------|------------|
| **Hosting** | Cloud-hosted | Self-hosted or cloud | Cloud-hosted |
| **Pricing** | Generous free tier | Open source (free) | Limited free tier |
| **API** | GROQ + GraphQL | REST + GraphQL | REST + GraphQL |
| **Content Modeling** | Excellent, flexible | Good, schema-based | Good, restricted |
| **Next.js Integration** | Excellent (official SDK) | Good | Good |
| **Real-time** | Built-in | Plugin required | Built-in |
| **Localization** | Built-in | Plugin | Built-in |
| **Media Handling** | Excellent (Sanity Studio) | Good | Good |
| **Customization** | Highly customizable | Very customizable | Limited |
| **Learning Curve** | Medium | Medium | Low |
| **Scalability** | Excellent | Good | Excellent |

### 2.2 Recommendation: Sanity

**Primary Choice:** Sanity

**Rationale:**
1. **GROQ Query Language** — Powerful, flexible content queries
2. **Sanity Studio** — Best-in-class content editing experience
3. **Next.js Integration** — Official `@sanity/client` and `@sanity/image-url`
4. **Real-time Collaboration** — Built-in, no extra setup
5. **Generous Free Tier** — 100K API requests/month, 500MB assets
6. **Content Modeling** — Highly flexible, supports complex schemas
7. **Preview Mode** — Excellent Next.js preview support
8. **Community** — Growing, active community

**Backup Choice:** Strapi (if self-hosting preferred for cost or data control)

### 2.3 Sanity Schema Design

```groovy
// Schema types needed:

// Pages
- HomePage
- SolutionPage
- ProductPage
- IndustryPage
- CaseStudy
- CompanyPage
- ContactPage
- InsightPage

// Resources
- Post (blog post)
- Report
- Whitepaper
- Research

// Content
- Author
- Category
- Tag
- Testimonial
- ClientLogo

// Components (Portable Text blocks)
- Hero
- Metrics
- FAQ
- CTA
- MediaBlock
- RichText
```

### 2.4 Sanity Project Structure

```text
sanity/
├── sanity.config.ts
├── sanity.cli.ts
├── schemas/
│   ├── documents/
│   │   ├── homePage.ts
│   │   ├── solutionPage.ts
│   │   ├── productPage.ts
│   │   ├── industryPage.ts
│   │   ├── caseStudy.ts
│   │   ├── post.ts
│   │   ├── report.ts
│   │   ├── author.ts
│   │   └── ...
│   ├── objects/
│   │   ├── hero.ts
│   │   ├── metrics.ts
│   │   ├── faq.ts
│   │   ├── cta.ts
│   │   └── ...
│   └── index.ts
├── structure/
│   └── deskStructure.ts
└── plugins/
    └── ...
```

---

## 3. Hosting & Deployment

### 3.1 Hosting Evaluation

| Criteria | Vercel | Azure | GCP |
|----------|--------|-------|-----|
| **Next.js Support** | Native (created Next.js) | Good (Azure Static Web Apps) | Good (Cloud Run) |
| **Deployment** | Git-based, instant | Manual or CI/CD | Manual or CI/CD |
| **Edge Network** | Global CDN included | Azure CDN (extra setup) | Cloud CDN (extra setup) |
| **Preview Deployments** | Automatic per PR | Manual | Manual |
| **Analytics** | Vercel Analytics (extra) | — | — |
| **Pricing** | Free tier, then pay-per-use | Pay for resources | Pay for resources |
| **Scalability** | Automatic | Manual scaling | Manual scaling |
| ** DX** | Excellent | Good | Good |

### 3.2 Recommendation: Vercel

**Primary Choice:** Vercel

**Rationale:**
1. **Native Next.js Support** — Created by the same team, best integration
2. **Automatic Previews** — Every PR gets a preview URL
3. **Global Edge Network** — Fast loading worldwide
4. **Zero Configuration** — Works out of the box with Next.js
5. **Git Integration** — Push to deploy
6. **Analytics** — Built-in Web Vitals monitoring
7. **Free Tier** — Generous for most use cases

**Backup Choice:** Azure Static Web Apps (if Azure ecosystem preferred)

### 3.3 Vercel Configuration

```json
// vercel.json
{
  "framework": "nextjs",
  "buildCommand": "pnpm build",
  "outputDirectory": ".next",
  "installCommand": "pnpm install",
  "regions": ["sin1"],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        }
      ]
    }
  ]
}
```

---

## 4. Analytics & Monitoring

### 4.1 Analytics Stack

| Tool | Purpose | Priority |
|------|---------|----------|
| **Google Analytics 4** | Traffic analysis, conversions, user behavior | High |
| **Google Search Console** | SEO monitoring, indexing, search performance | High |
| **Microsoft Clarity** | Heatmaps, session recordings, UX insights | Medium |
| **Vercel Analytics** | Core Web Vitals, performance monitoring | Medium |
| **Sentry** | Error tracking, performance monitoring | Medium |

### 4.2 Google Analytics 4

**Implementation:**
```typescript
// Using nextjs-gtag or @next/third-parties
import { GoogleAnalytics } from '@next/third-parties/google';

// In layout.tsx
<GoogleAnalytics gaId={process.env.NEXT_PUBLIC_GA_ID} />
```

**Events to Track:**
- Page views (automatic)
- Scroll depth (25%, 50%, 75%, 100%)
- CTA clicks
- Form submissions
- Newsletter signups
- Resource downloads
- Search usage
- Case study views
- Blog post reads

### 4.3 Google Search Console

**Setup:**
- Verify anaxee.com
- Submit XML sitemap
- Monitor indexing status
- Track search performance
- Set up alerts for critical issues

### 4.4 Microsoft Clarity

**Implementation:**
```html
<!-- In _document.tsx or layout.tsx head -->
<script>
  (function(c,l,a,r,i,t,y){
    c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
    t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
    y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);
  })(window, document, "clarity", "script", "YOUR_CLARITY_ID");
</script>
```

**Use Cases:**
- Identify rage clicks (user frustration)
- Find dead clicks (non-interactive elements clicked)
- Analyze scroll behavior
- Understand navigation patterns
- Identify form abandonment

### 4.5 Error Monitoring (Sentry)

**Implementation:**
```bash
pnpm add @sentry/nextjs
npx @sentry/wizard@latest -i nextjs
```

**Features:**
- Automatic error capturing
- Performance monitoring
- Release tracking
- User context
- Breadcrumbs

---

## 5. Image & Media

### 5.1 Image Optimization

| Tool | Purpose | Choice |
|------|---------|--------|
| **Image Format** | Next-gen formats | WebP + AVIF (via Next.js Image) |
| **CDN** | Image delivery | Sanity CDN or Cloudinary |
| **Optimization** | Resize, compress | Next.js Image component |
| **Lazy Loading** | Performance | Built-in with Next.js Image |

### 5.2 Next.js Image Component

```tsx
import Image from 'next/image';

// Usage
<Image
  src="/images/hero.jpg"
  alt="Anaxee Digital Runner network"
  width={1200}
  height={600}
  priority // for above-the-fold images
  placeholder="blur"
  blurDataURL={blurDataUrl}
/>
```

### 5.3 Sanity Image URL

```typescript
import imageUrlBuilder from '@sanity/image-url';
import { client } from '@/lib/sanity/client';

const builder = imageUrlBuilder(client);

export function urlFor(source: any) {
  return builder.image(source);
}

// Usage
<img src={urlFor(image).width(800).url()} alt="..." />
```

---

## 6. Development Tools

### 6.1 Code Quality

| Tool | Purpose | Configuration |
|------|---------|---------------|
| **ESLint** | Code linting | Next.js recommended + custom rules |
| **Prettier** | Code formatting | Consistent style |
| **Husky** | Git hooks | Pre-commit linting |
| **lint-staged** | Staged files | Run linters on commit |
| **TypeScript** | Type checking | Strict mode |

### 6.2 ESLint Configuration

```json
// .eslintrc.json
{
  "extends": [
    "next/core-web-vitals",
    "eslint:recommended",
    "@typescript-eslint/recommended",
    "prettier"
  ],
  "rules": {
    "@typescript-eslint/no-unused-vars": "error",
    "@typescript-eslint/no-explicit-any": "warn",
    "no-console": "warn"
  }
}
```

### 6.3 Prettier Configuration

```json
// .prettierrc
{
  "semi": true,
  "trailingComma": "es5",
  "singleQuote": true,
  "printWidth": 100,
  "tabWidth": 2,
  "useTabs": false
}
```

### 6.4 Husky Setup

```bash
# .husky/pre-commit
pnpm lint-staged
pnpm type-check

# .husky/commit-msg
pnpm commitlint --edit $1
```

### 6.5 Testing

| Tool | Purpose | Type |
|------|---------|------|
| **Vitest** | Unit testing | Unit tests |
| **Playwright** | E2E testing | Integration tests |
| **Testing Library** | Component testing | Component tests |
| **Lighthouse CI** | Performance testing | Performance budgets |

### 6.6 Testing Configuration

```typescript
// vitest.config.ts
import { defineConfig } from 'vitest/config';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  test: {
    environment: 'jsdom',
    globals: true,
    setupFiles: ['./tests/setup.ts'],
  },
});
```

---

## 7. Environment Variables

### 7.1 Required Environment Variables

```bash
# .env.local (not committed to git)

# Sanity
NEXT_PUBLIC_SANITY_PROJECT_ID=your_project_id
NEXT_PUBLIC_SANITY_DATASET=production
SANITY_API_TOKEN=your_api_token
SANITY_REVALIDATE_SECRET=your_revalidate_secret

# Analytics
NEXT_PUBLIC_GA_ID=G-XXXXXXXXXX
NEXT_PUBLIC_CLARITY_ID=your_clarity_id
NEXT_PUBLIC_GSC_VERIFICATION=your_verification_code

# Sentry
SENTRY_DSN=your_sentry_dsn
SENTRY_ORG=your_org
SENTRY_PROJECT=your_project

# App
NEXT_PUBLIC_SITE_URL=https://anaxee.com
NEXT_PUBLIC_WHATSAPP_NUMBER=+91XXXXXXXXXX

# Forms
FORM_SUBMISSION_ENDPOINT=your_form_endpoint
CRM_API_KEY=your_crm_api_key
```

### 7.2 .env.example

```bash
# Copy this file to .env.local and fill in values

# Sanity
NEXT_PUBLIC_SANITY_PROJECT_ID=
NEXT_PUBLIC_SANITY_DATASET=production
SANITY_API_TOKEN=
SANITY_REVALIDATE_SECRET=

# Analytics
NEXT_PUBLIC_GA_ID=
NEXT_PUBLIC_CLARITY_ID=
NEXT_PUBLIC_GSC_VERIFICATION=

# Sentry
SENTRY_DSN=
SENTRY_ORG=
SENTRY_PROJECT=

# App
NEXT_PUBLIC_SITE_URL=
NEXT_PUBLIC_WHATSAPP_NUMBER=

# Forms
FORM_SUBMISSION_ENDPOINT=
CRM_API_KEY=
```

---

## 8. CI/CD Pipeline

### 8.1 GitHub Actions Workflow

```yaml
# .github/workflows/ci.yml
name: CI/CD Pipeline

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: pnpm/action-setup@v2
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'pnpm'
      - run: pnpm install --frozen-lockfile
      - run: pnpm lint
      - run: pnpm type-check

  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: pnpm/action-setup@v2
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'pnpm'
      - run: pnpm install --frozen-lockfile
      - run: pnpm test

  build:
    runs-on: ubuntu-latest
    needs: [lint, test]
    steps:
      - uses: actions/checkout@v4
      - uses: pnpm/action-setup@v2
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'pnpm'
      - run: pnpm install --frozen-lockfile
      - run: pnpm build
```

### 8.2 Deployment Flow

```text
Push to main
    ↓
GitHub Actions CI (lint, test, build)
    ↓
Vercel Preview (on PR) / Production (on main)
    ↓
Deployment Complete
```

---

## 9. Project Structure

```text
anaxee-platform/
├── .github/
│   └── workflows/
│       └── ci.yml
├── .husky/
│   ├── pre-commit
│   └── commit-msg
├── public/
│   ├── favicon.ico
│   ├── robots.txt
│   └── images/
├── sanity/
│   ├── schemas/
│   ├── structure/
│   └── sanity.config.ts
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   ├── solutions/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   ├── products/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   ├── industries/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   ├── case-studies/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   ├── resources/
│   │   │   ├── blog/
│   │   │   │   ├── page.tsx
│   │   │   │   └── [slug]/
│   │   │   │       └── page.tsx
│   │   │   ├── reports/
│   │   │   └── whitepapers/
│   │   ├── insights/
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   ├── company/
│   │   │   ├── about/
│   │   │   ├── careers/
│   │   │   └── contact/
│   │   └── api/
│   │       ├── revalidate/
│   │       └── search/
│   ├── components/
│   │   ├── ui/
│   │   ├── layout/
│   │   ├── sections/
│   │   └── features/
│   ├── lib/
│   │   ├── sanity/
│   │   ├── utils.ts
│   │   └── constants.ts
│   └── types/
│       └── index.ts
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── .env.example
├── .eslintrc.json
├── .prettierrc
├── next.config.mjs
├── package.json
├── pnpm-lock.yaml
├── postcss.config.js
├── tailwind.config.ts
├── tsconfig.json
├── vercel.json
└── vitest.config.ts
```

---

## 10. Package Dependencies

### 10.1 Core Dependencies

```json
{
  "dependencies": {
    "next": "^14.0.0",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "@sanity/client": "^6.0.0",
    "@sanity/image-url": "^1.0.0",
    "@sanity/vision": "^3.0.0",
    "next-sanity": "^9.0.0",
    "lucide-react": "^0.300.0",
    "clsx": "^2.0.0",
    "tailwind-merge": "^2.0.0"
  },
  "devDependencies": {
    "typescript": "^5.3.0",
    "@types/react": "^18.2.0",
    "@types/node": "^20.0.0",
    "tailwindcss": "^3.4.0",
    "postcss": "^8.4.0",
    "autoprefixer": "^10.4.0",
    "eslint": "^8.56.0",
    "eslint-config-next": "^14.0.0",
    "prettier": "^3.2.0",
    "eslint-config-prettier": "^9.1.0",
    "husky": "^9.0.0",
    "lint-staged": "^15.2.0",
    "vitest": "^1.2.0",
    "@vitejs/plugin-react": "^4.2.0",
    "playwright": "^1.40.0",
    "@sentry/nextjs": "^7.90.0"
  }
}
```

---

## 11. Technology Decision Summary

| Category | Decision | Backup |
|----------|----------|--------|
| Framework | Next.js 14+ (App Router) | — |
| Language | TypeScript | — |
| UI Library | React 18+ | — |
| Styling | Tailwind CSS | — |
| CMS | Sanity | Strapi |
| Hosting | Vercel | Azure Static Web Apps |
| Analytics | GA4 + Search Console + Clarity | — |
| Error Monitoring | Sentry | — |
| Image CDN | Sanity CDN | Cloudinary |
| Testing | Vitest + Playwright | — |
| Linting | ESLint + Prettier | — |
| Git Hooks | Husky + lint-staged | — |
| CI/CD | GitHub Actions + Vercel | — |
| Package Manager | pnpm | npm |

---

## 12. Security Considerations

### 12.1 Security Headers

- `X-Frame-Options: DENY` — Prevent clickjacking
- `X-Content-Type-Options: nosniff` — Prevent MIME sniffing
- `Referrer-Policy: strict-origin-when-cross-origin` — Control referrer
- `Content-Security-Policy` — Control resource loading
- `Permissions-Policy` — Control browser features

### 12.2 Environment Variables

- Never commit `.env.local` to git
- Use `.env.example` as template
- Rotate API tokens periodically
- Use least-privilege principle for API tokens

### 12.3 Dependencies

- Regularly audit dependencies (`pnpm audit`)
- Use Dependabot for automated updates
- Pin dependency versions in lockfile
- Review security advisories
