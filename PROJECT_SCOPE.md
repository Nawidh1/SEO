# PROJECT_SCOPE

## Overview
This project is a production-ready static website for Brasserie Pizzeria Hama, a local restaurant in Terneuzen. The site is built with Astro and Tailwind CSS for fast page delivery, strong crawlability, and a polished, mobile-first user experience focused on menu discovery, reservations, and ordering.

## Design direction
- Mood: bright, welcoming, family-friendly
- Primary accent: sky blue
- Heading accent: navy text only
- Backgrounds: white and warm-white surfaces
- Typography: Playfair Display for headings, Inter for body text
- Principles: generous spacing, clear calls to action, simple navigation, high readability

## Pages
| Route | Status | Description |
|---|---|---|
| `/` | Built | Homepage with hero, key info, featured offering, testimonials, visit section, CTA |
| `/menu` | Built | Core pizza and brasserie menu highlights |
| `/about` | Built | Restaurant story and positioning |
| `/gallery` | Built | Photo placeholders for space, food, and events |
| `/catering` | Built | Catering packages and FAQ content |
| `/private-events` | Built | Private dining and group event page |
| `/contact` | Built | Contact form UI, NAP, hours, map placeholder |
| `/order-online` | Built | External ordering CTA placeholder |
| `/404` | Built | Custom noindex page not found experience |

## Components
| Component | File | Purpose |
|---|---|---|
| Header | `src/components/Header.astro` | Sticky nav, desktop links, mobile toggle menu |
| Footer | `src/components/Footer.astro` | NAP, hours, footer links |
| Hero | `src/components/Hero.astro` | Homepage hero with dual CTA |
| PageHero | `src/components/PageHero.astro` | Interior page hero banner |
| Breadcrumb | `src/components/Breadcrumb.astro` | Breadcrumb UI + BreadcrumbList schema |
| SectionHeading | `src/components/SectionHeading.astro` | Reusable section heading block |
| Card | `src/components/Card.astro` | Feature/benefit cards |
| InfoCard | `src/components/InfoCard.astro` | Key business info highlights |

## Layouts
| Layout | File | Purpose |
|---|---|---|
| BaseLayout | `src/layouts/BaseLayout.astro` | Shared head SEO metadata, canonical, OG/Twitter, schema injection, header/footer |

## SEO checklist
- [x] Unique `<title>` and `<meta description>` on every page
- [x] Canonical URLs on every page
- [x] Open Graph tags (title, description, image, site_name, locale, type, url)
- [x] Twitter/X Card tags (card, title, description, image)
- [x] `apple-touch-icon` and `theme-color` meta
- [x] XML sitemap generated (with utility pages filtered out)
- [x] `robots.txt` with sitemap reference
- [x] Trailing slash consistency enforced
- [x] LocalBusiness JSON-LD with full NAP, geo, hours, sameAs, areaServed
- [x] WebSite JSON-LD on homepage
- [x] BreadcrumbList JSON-LD on all interior pages
- [x] FAQPage JSON-LD where applicable
- [x] Semantic HTML landmarks (`header`, `nav`, `main`, `footer`, `section`, `article`)
- [x] Proper heading hierarchy (single `h1`, sequential levels)
- [x] Skip-to-content link
- [x] ARIA attributes (`aria-label` on navs, `aria-current="page"`, `aria-expanded` on toggles)
- [x] NAP consistency (footer, contact page, schema all match)
- [x] Image `alt` attributes, `loading`/`fetchpriority`, explicit dimensions
- [x] Custom 404 page (noindexed)
- [x] All form inputs have `<label>` elements
- [x] Breadcrumb navigation on interior pages
- [x] Internal linking between related pages

## Content needs
- Final full menu with pricing and seasonal items
- Final restaurant story and team details
- Real testimonials with source consent
- Final opening hours and holiday schedule
- Verified business email address

## Photo assets needed
- Exterior storefront photo
- Interior dining room photos
- Signature pizza close-up
- Team/service photo
- Private event setup photo
- Branded OG social share image (1200x630)

## Integrations to configure
- Contact form backend (Formspree or Netlify Forms)
- Google Maps embed and official map URL
- Analytics (GA4 or Plausible)
- Online ordering platform URL
- Social profile links for schema `sameAs`

## Future: Deployment
1. Push repository to GitHub
2. Connect repository to Netlify
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Enable auto-deploy on push to main branch

## Future: CMS for non-technical editors
1. Move editable page content into `src/content/` Markdown collections
2. Add Decap CMS admin app (`public/admin/index.html` and `public/admin/config.yml`)
3. Enable Netlify Identity and Git Gateway
4. Editor workflow: login -> edit content -> publish changes

## File structure tree
```text
.
+-- public
¦   +-- apple-touch-icon.png
¦   +-- favicon.ico
¦   +-- favicon.svg
¦   +-- robots.txt
+-- src
¦   +-- components
¦   ¦   +-- Breadcrumb.astro
¦   ¦   +-- Card.astro
¦   ¦   +-- Footer.astro
¦   ¦   +-- Header.astro
¦   ¦   +-- Hero.astro
¦   ¦   +-- InfoCard.astro
¦   ¦   +-- PageHero.astro
¦   ¦   +-- SectionHeading.astro
¦   +-- layouts
¦   ¦   +-- BaseLayout.astro
¦   +-- pages
¦   ¦   +-- 404.astro
¦   ¦   +-- about.astro
¦   ¦   +-- catering.astro
¦   ¦   +-- contact.astro
¦   ¦   +-- gallery.astro
¦   ¦   +-- index.astro
¦   ¦   +-- menu.astro
¦   ¦   +-- order-online.astro
¦   ¦   +-- private-events.astro
¦   +-- styles
¦       +-- global.css
+-- astro.config.mjs
+-- package.json
+-- PROJECT_SCOPE.md
+-- tailwind.config.mjs
+-- tsconfig.json
```
