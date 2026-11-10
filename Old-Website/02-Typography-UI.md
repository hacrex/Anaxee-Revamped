# Anaxee.com — Typography & UI Layout

## Typography

| Element | Font | Notes |
|---------|------|-------|
| **Body copy** | `Poppins`, sans-serif | Font-weight 400, base 15px, line-height 1.5–1.7 |
| **Headings / display numbers** | `Barlow Condensed` (Google Fonts) | Giant stats, section subheads, hero display |
| **Icons** | Font Awesome 4.7.0 | Social icons, nav search/user icons, UI glyphs |
| **Weight utilities** | 300 light · 400 regular · 500 medium · 600 semibold · 700 bold | `.f-light` … `.f-bold` |
| **Size utilities** | `.f-10` … `.f-20` (10px–19px) | Plus giant display: `.k25` (240px), `.k25-home` (120px), `.k25-home-lg` (192px), `.of` (47px), `.heading-believe` (70px) |

---

## UI / Layout Structure

### Header / Navigation

- Height: 100px desktop (70px on tablets ≤1536px)
- Background: `#292929` dark; scrolled state `.nav-inner` = `#fff` with `#231f20` links
- Container padding: 30px L/R
- Nav links: white on dark; `#5cc6d0` underline accent (height 4px, grows 0→100% on hover)
- Utility icons: Search (`icon-search.png`, 18px) and User (`icon-user.png`, 10px inside `#5cc6d0` circle, 30×30px, 50% radius)
- Sticky: `body { padding-top: 100px }`
- Mobile: hamburger toggler, full-width black overlay menu

### Recurring section patterns

- Section padding: `.pady-80` → `80px 0` (most content sections)
- Box pattern: `.box-our-reach`, `.box-partners`, `.box-our-services`, `.box-runners`, `.box-blog` — all `padding: 80px 0`, `h3` at 30px/600 weight
- Heading style: `.heading-lined` — relative heading with 2px × 50px `#5cc6d0` vertical accent line left; `.heading-lined-right` variant
- Images: service images grayscale by default → colour on hover; dark gradient overlays on image cards with text fading up
- Sliders: Owl Carousel, `#5cc6d0` nav arrows (44×44px circles), pagination dots
- Cards: `.ax-pcard` proof cards (white, `#d7ebee` border, `#0b7c89` 24px/800 weight number, hover lift + shadow); `.ax-rcard` related cards (150px thumb, 14.5px bold title)
- Buttons: `.btn-primary` (`#5cc6d0` → `#38b5c1`), `.btn-outline-primary`, `.btn-rounded` (50px radius, shadow `0 4px 17px rgba(0,0,0,0.2)`), padding `0.75rem 65px`
- Forms: `.input_animated` animated-label inputs (54px height, transparent bg, `#cdcdcd` border, focus → `#5cc6d0` border + white bg); newsletter input with icon arrow
- Footer: `#212121` bg, 12px text, white links → `#5cc6d0` hover, social circles `#5cc6d0`/`#fff` (28×28px)
- WhatsApp float: fixed right-center, `#25D366`, 60×60px, scale hover
- Animations: AOS library; word-rotation typewriter in hero (18s loop)

### Breakpoints (responsive)

1536px · 1366px · 1200px · 1024px · 992px · 768px · 767px · 576px · 320px