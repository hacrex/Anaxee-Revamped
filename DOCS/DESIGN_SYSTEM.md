# Anaxee Platform — Design System

## Overview

This document defines the complete design system for the Anaxee digital platform. It establishes the visual language, components, and patterns that ensure consistency across all pages and experiences.

**Design Inspiration:** Stripe, Vercel, Notion, HubSpot, Snowflake, Datadog

**Core Principles:**
1. **Technology-First** — Visually communicate innovation and data
2. **India-Focused** — Warmth and accessibility while maintaining enterprise credibility
3. **Data-Driven** — Metrics, dashboards, and visualizations are core to the brand
4. **Clean & Modern** — Minimal clutter, clear hierarchy, purposeful whitespace
5. **Scalable** — Design tokens and components that grow with the platform

---

## 1. Brand Identity

### 1.1 Logo

**Primary Logo:**
- Anaxee wordmark
- Icon/symbol mark (if applicable)
- Minimum clear space: 1.5x height of the logo mark on all sides

**Logo Variations:**
- Full color (primary)
- White (for dark backgrounds)
- Black (for light backgrounds)
- Icon-only (for favicons, app icons, small spaces)

**Logo Usage Rules:**
- Never stretch, distort, or rotate
- Never add effects (shadows, gradients, outlines)
- Never change the logo colors
- Always maintain minimum clear space
- Use approved versions only

### 1.2 Tagline

**Primary:** "India's Reach Engine"

**Supporting:**
- "Technology. Data. Execution. At Scale."
- "250,000+ Digital Runners. 11,000+ Pincodes. One Platform."

---

## 2. Color System

### 2.1 Primary Colors

| Color Name | Hex | RGB | Usage |
|-----------|-----|-----|-------|
| Anaxee Blue | `#1E40AF` | 30, 64, 175 | Primary brand color, CTAs, key elements |
| Anaxee Dark | `#0F172A` | 15, 23, 42 | Headings, text, dark backgrounds |
| Anaxee White | `#FFFFFF` | 255, 255, 255 | Backgrounds, text on dark |

### 2.2 Secondary Colors

| Color Name | Hex | RGB | Usage |
|-----------|-----|-----|-------|
| Deep Navy | `#1E3A5F` | 30, 58, 95 | Secondary headings, borders |
| Slate | `#475569` | 71, 85, 105 | Body text, captions |
| Light Gray | `#F8FAFC` | 248, 250, 252 | Backgrounds, cards |
| Border Gray | `#E2E8F0` | 226, 232, 240 | Borders, dividers |

### 2.3 Accent Colors

| Color Name | Hex | RGB | Usage |
|-----------|-----|-----|-------|
| Electric Blue | `#3B82F6` | 59, 130, 246 | Links, interactive elements |
| Teal | `#14B8A6` | 20, 184, 166 | Climate/sustainability content |
| Green | `#22C55E` | 34, 197, 94 | Success states, positive metrics |
| Amber | `#F59E0B` | 245, 158, 11 | Warnings, highlights |
| Red | `#EF4444` | 239, 68, 68 | Error states, alerts |

### 2.4 Semantic Colors

| Semantic | Light Mode | Dark Mode | Usage |
|----------|-----------|-----------|-------|
| Background | `#FFFFFF` | `#0F172A` | Page background |
| Surface | `#F8FAFC` | `#1E293B` | Card backgrounds |
| Text Primary | `#0F172A` | `#F8FAFC` | Headings |
| Text Secondary | `#475569` | `#94A3B8` | Body text |
| Text Muted | `#94A3B8` | `#64748B` | Captions, labels |
| Border | `#E2E8F0` | `#334155` | Borders, dividers |
| Primary | `#1E40AF` | `#3B82F6` | CTAs, links |
| Success | `#22C55E` | `#22C55E` | Success states |
| Error | `#EF4444` | `#EF4444` | Error states |

### 2.5 Color Usage by Vertical

| Vertical | Accent Color | Usage |
|----------|-------------|-------|
| Retail Intelligence | Anaxee Blue `#1E40AF` | Headers, icons, accents |
| AI Data Collection | Electric Blue `#3B82F6` | Headers, icons, accents |
| Climate & Carbon | Teal `#14B8A6` | Headers, icons, accents |
| Influence Marketing | Amber `#F59E0B` | Headers, icons, accents |
| GTM Services | Green `#22C55E` | Headers, icons, accents |

---

## 3. Typography

### 3.1 Font Selection

**Primary Font (Headings):** Inter
- Clean, modern, highly readable
- Excellent for data-heavy interfaces
- Wide language support (including Devanagari for future Hindi content)

**Body Font:** Inter
- Consistent with headings
- Optimized for screen reading
- Multiple weights available

**Monospace Font:** JetBrains Mono
- For code snippets, technical content, data displays

### 3.2 Type Scale

| Level | Size (px) | Size (rem) | Weight | Line Height | Usage |
|-------|----------|------------|--------|-------------|-------|
| Display | 60 | 3.75 | 800 | 1.1 | Hero headlines |
| H1 | 48 | 3.0 | 700 | 1.2 | Page titles |
| H2 | 36 | 2.25 | 700 | 1.25 | Section headings |
| H3 | 30 | 1.875 | 600 | 1.3 | Subsection headings |
| H4 | 24 | 1.5 | 600 | 1.35 | Card titles |
| H5 | 20 | 1.25 | 600 | 1.4 | Small headings |
| H6 | 16 | 1.0 | 600 | 1.4 | Labels, overlines |
| Body Large | 18 | 1.125 | 400 | 1.6 | Lead paragraphs |
| Body | 16 | 1.0 | 400 | 1.6 | Default text |
| Body Small | 14 | 0.875 | 400 | 1.5 | Captions, metadata |
| Caption | 12 | 0.75 | 400 | 1.4 | Fine print, labels |

### 3.3 Responsive Type Scale

| Level | Mobile | Tablet | Desktop |
|-------|--------|--------|---------|
| Display | 36px | 48px | 60px |
| H1 | 32px | 40px | 48px |
| H2 | 28px | 32px | 36px |
| H3 | 24px | 28px | 30px |
| H4 | 20px | 22px | 24px |
| Body Large | 16px | 18px | 18px |
| Body | 16px | 16px | 16px |

### 3.4 Typography Rules

1. **Maximum line length:** 65–75 characters for body text
2. **Paragraph spacing:** 1.5x font size
3. **Heading spacing:** 2x font size above, 1x below
4. **Never use more than 2 font sizes per component**
5. **Contrast ratio:** Minimum 4.5:1 for normal text, 3:1 for large text

---

## 4. Spacing System

### 4.1 Base Unit

**Base unit:** 4px

All spacing values are multiples of 4px.

### 4.2 Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `space-0` | 0px | — |
| `space-1` | 4px | Tight spacing |
| `space-2` | 8px | Small spacing |
| `space-3` | 12px | Default inner spacing |
| `space-4` | 16px | Medium spacing |
| `space-5` | 20px | — |
| `space-6` | 24px | Default card padding |
| `space-8` | 32px | Section inner spacing |
| `space-10` | 40px | Large spacing |
| `space-12` | 48px | Section gaps |
| `space-16` | 64px | Page section spacing |
| `space-20` | 80px | Large section spacing |
| `space-24` | 96px | Hero section spacing |
| `space-32` | 128px | Page margins |

### 4.3 Section Spacing

| Section Type | Top/Bottom Padding |
|-------------|-------------------|
| Hero Section | 96–128px |
| Content Section | 64–96px |
| Card Grid | 64px |
| Footer | 64px |

---

## 5. Grid System

### 5.1 Layout Grid

**Max Width:** 1280px (content area)
**Gutter:** 24px (desktop), 16px (mobile)
**Margin:** 24px (desktop), 16px (mobile)

### 5.2 Breakpoints

| Name | Width | Columns | Gutter |
|------|-------|---------|--------|
| Mobile | 0–639px | 4 | 16px |
| Tablet | 640–1023px | 8 | 16px |
| Desktop | 1024–1279px | 12 | 24px |
| Wide | 1280px+ | 12 | 24px |

### 5.3 Layout Patterns

**Single Column:**
```text
[--------- 12 cols ---------]
```

**Two Column (6+6):**
```text
[-- 6 cols --][-- 6 cols --]
```

**Sidebar + Content (3+9):**
```text
[- 3 cols -][---- 9 cols ----]
```

**Three Column (4+4+4):**
```text
[-- 4 --][-- 4 --][-- 4 --]
```

**Four Column (3+3+3+3):**
```text
[-3-][-3-][-3-][-3-]
```

---

## 6. Component Library

### 6.1 Buttons

**Variants:**
| Variant | Usage | Style |
|---------|-------|-------|
| Primary | Main CTAs | Filled, Anaxee Blue |
| Secondary | Alternative actions | Outlined, Anaxee Blue |
| Ghost | Tertiary actions | Text only |
| Danger | Destructive actions | Filled, Red |
| Link | Inline actions | Text with underline |

**Sizes:**
| Size | Height | Padding | Font Size |
|------|--------|---------|-----------|
| Small | 32px | 12px 16px | 14px |
| Medium | 40px | 16px 24px | 16px |
| Large | 48px | 16px 32px | 18px |

**States:** Default, Hover, Active, Disabled, Loading

### 6.2 Cards

**Variants:**
| Variant | Usage | Style |
|---------|-------|-------|
| Default | General content | White bg, border, rounded |
| Elevated | Featured content | Shadow, no border |
| Interactive | Clickable content | Hover effect, cursor pointer |
| Metric | Data display | Icon + number + label |
| Solution | Solution showcase | Icon + title + description |
| Case Study | Client stories | Image + title + industry tag |

**Card Anatomy:**
```text
┌─────────────────────────┐
│ [Optional Image]        │
│                         │
│ [Tag/Category]          │
│ Title                   │
│ Description text here   │
│                         │
│ [Optional CTA]          │
└─────────────────────────┘
```

### 6.3 Navigation

**Header:**
- Fixed/sticky on scroll
- Logo left, nav links center, CTA right
- Mega menu for desktop
- Hamburger for mobile
- Transparent → solid on scroll (homepage)

**Footer:**
- Multi-column layout
- Logo + tagline
- Solution links
- Product links
- Resource links
- Company links
- Social links
- Newsletter signup
- Legal links

### 6.4 Forms

**Input Fields:**
- Label + Input + Helper text + Error state
- Sizes: Small, Medium, Large
- States: Default, Focus, Error, Disabled

**Form Patterns:**
- Single column (default)
- Two column (wide screens)
- Inline forms (search, newsletter)
- Multi-step forms (contact, demo request)

### 6.5 Badges & Tags

**Variants:**
| Variant | Usage | Style |
|---------|-------|-------|
| Default | General | Gray background |
| Primary | Featured | Blue background |
| Success | Active/Complete | Green background |
| Warning | Pending | Amber background |
| Error | Error/Alert | Red background |
| Industry | Industry tags | Colored by vertical |

### 6.6 Icons

**Icon Library:** Lucide Icons (or Phosphor Icons)
- Consistent 24x24 size
- 1.5px stroke width
- Round line caps

**Custom Icons:**
- Anaxee logo mark
- Digital Runner icon
- Coverage map icon
- Vertical-specific icons (if needed)

### 6.7 Tables

**Features:**
- Sortable columns
- Responsive (horizontal scroll on mobile)
- Row hover state
- Sticky header
- Pagination
- Empty state

### 6.8 Modals & Dialogs

**Variants:**
- Confirmation dialog
- Information modal
- Form modal
- Full-screen modal (mobile)

### 6.9 Tooltips

- Trigger on hover/focus
- Max width: 250px
- Arrow pointing to trigger
- Delay: 300ms

### 6.10 Loading States

**Skeleton Screens:**
- Match content layout
- Animated shimmer effect
- Used for page loads and data fetching

**Spinners:**
- For inline loading
- For button loading states

**Progress Bars:**
- For multi-step processes
- For file uploads

---

## 7. Motion & Animation

### 7.1 Principles

1. **Purposeful** — Every animation has a reason
2. **Subtle** — Enhance, don't distract
3. **Fast** — Keep animations under 300ms
4. **Consistent** — Use the same easing curves

### 7.2 Easing Curves

| Name | Value | Usage |
|------|-------|-------|
| Default | `cubic-bezier(0.4, 0, 0.2, 1)` | Most transitions |
| In | `cubic-bezier(0.4, 0, 1, 1)` | Entering elements |
| Out | `cubic-bezier(0, 0, 0.2, 1)` | Exiting elements |
| Bounce | `cubic-bezier(0.68, -0.55, 0.265, 1.55)` | Playful elements |

### 7.3 Animation Types

| Animation | Duration | Usage |
|-----------|----------|-------|
| Fade In | 200ms | Page transitions |
| Slide Up | 300ms | Scroll-triggered reveals |
| Scale | 200ms | Button hover, card hover |
| Counter | 1500ms | Animated number counters |
| Map Pulse | 2000ms | India map interactions |

### 7.4 Scroll-Based Storytelling

**Homepage Story Sequence:**
1. India Map — Fade in with pulse animation
2. Digital Runner Network — Counter animation
3. Data Collection — Flow animation
4. AI Validation — Processing animation
5. Customer Insights — Dashboard reveal
6. Business Impact — Metric counters

### 7.5 Reduced Motion

- Respect `prefers-reduced-motion` media query
- Disable non-essential animations
- Keep functional animations (focus states, etc.)

---

## 8. Imagery & Visual Elements

### 8.1 Photography Style

- Real people (Digital Runners, field workers, offices)
- Indian context (rural, urban, diverse landscapes)
- Authentic, not stock-looking
- Warm color grading
- High quality, well-lit

### 8.2 Illustrations

- Minimal use — photography preferred
- Flat, modern style when used
- Consistent color palette
- Data visualizations preferred over abstract illustrations

### 8.3 Data Visualizations

- Charts (bar, line, pie, area)
- Graphs (network, flow)
- Maps (India coverage, state-level)
- Dashboards (metrics, KPIs)
- Infographics (process, timeline)

**Chart Colors:**
```javascript
const chartColors = {
  primary: '#1E40AF',
  secondary: '#3B82F6',
  tertiary: '#14B8A6',
  quaternary: '#F59E0B',
  quinary: '#22C55E',
  senary: '#8B5CF6',
};
```

### 8.4 Video

- Hero background videos (subtle, looping)
- Client testimonials
- Product demos
- Process explainers
- Maximum 15 seconds for hero loops

---

## 9. Dark Mode

### 9.1 Implementation

- System preference detection (`prefers-color-scheme`)
- Manual toggle in header
- Toggle persists via localStorage
- All components support both modes

### 9.2 Dark Mode Colors

| Element | Light | Dark |
|---------|-------|------|
| Background | `#FFFFFF` | `#0F172A` |
| Surface | `#F8FAFC` | `#1E293B` |
| Text Primary | `#0F172A` | `#F8FAFC` |
| Text Secondary | `#475569` | `#94A3B8` |
| Border | `#E2E8F0` | `#334155` |
| Primary | `#1E40AF` | `#3B82F6` |

---

## 10. Accessibility

### 10.1 Standards

- WCAG 2.1 AA compliance minimum
- WCAG 2.1 AAA for key user journeys

### 10.2 Requirements

1. **Color Contrast:** Minimum 4.5:1 for normal text, 3:1 for large text
2. **Focus States:** Visible focus indicators on all interactive elements
3. **Keyboard Navigation:** All functionality accessible via keyboard
4. **Screen Reader:** Semantic HTML, ARIA labels where needed
5. **Alt Text:** All images have descriptive alt text
6. **Heading Hierarchy:** Proper H1–H6 nesting
7. **Form Labels:** All form inputs have associated labels
8. **Error Identification:** Errors identified by more than color alone
9. **Skip Links:** Skip to main content link
10. **Language:** HTML lang attribute set

### 10.3 Testing

- Automated testing with axe-core
- Manual keyboard testing
- Screen reader testing (NVDA, VoiceOver)
- Color contrast checking

---

## 11. Tailwind CSS Configuration

### 11.1 Design Tokens in Tailwind

```javascript
// tailwind.config.js
module.exports = {
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
      fontSize: {
        'display': ['3.75rem', { lineHeight: '1.1', fontWeight: '800' }],
        'h1': ['3rem', { lineHeight: '1.2', fontWeight: '700' }],
        'h2': ['2.25rem', { lineHeight: '1.25', fontWeight: '700' }],
        'h3': ['1.875rem', { lineHeight: '1.3', fontWeight: '600' }],
      },
      spacing: {
        '18': '4.5rem',
        '88': '22rem',
        '128': '32rem',
      },
      maxWidth: {
        'content': '80rem', // 1280px
      },
      borderRadius: {
        'card': '0.75rem',
        'button': '0.5rem',
      },
      boxShadow: {
        'card': '0 1px 3px rgba(0, 0, 0, 0.1)',
        'card-hover': '0 4px 12px rgba(0, 0, 0, 0.15)',
        'elevated': '0 8px 24px rgba(0, 0, 0, 0.12)',
      },
    },
  },
};
```

---

## 12. Design System File Structure

```text
src/
├── components/
│   ├── ui/                    # Base components
│   │   ├── Button.tsx
│   │   ├── Card.tsx
│   │   ├── Input.tsx
│   │   ├── Badge.tsx
│   │   ├── Modal.tsx
│   │   ├── Table.tsx
│   │   ├── Tooltip.tsx
│   │   └── ...
│   ├── layout/                # Layout components
│   │   ├── Header.tsx
│   │   ├── Footer.tsx
│   │   ├── Navigation.tsx
│   │   ├── Sidebar.tsx
│   │   └── PageLayout.tsx
│   ├── sections/              # Page sections
│   │   ├── Hero.tsx
│   │   ├── Metrics.tsx
│   │   ├── Testimonials.tsx
│   │   ├── CTABanner.tsx
│   │   └── ...
│   └── features/              # Feature-specific components
│       ├── IndiaMap.tsx
│       ├── ImpactDashboard.tsx
│       ├── CaseStudyCard.tsx
│       └── ...
├── lib/
│   ├── design-tokens.ts       # Design token exports
│   └── utils.ts               # Utility functions
└── styles/
    └── globals.css            # Global styles, CSS variables
```
