# Greenwood Land Works LLC

Production website and business automation project for a heavy equipment land services company in Charlottesville, VA. Built and managed by Andrew Robb for his uncle Peter Farrell.

## Business Details
- **Name:** Greenwood Land Works LLC
- **Owner:** Peter Farrell (solo operator)
- **Location:** Charlottesville, VA
- **Service Area:** Albemarle, Greene, Nelson counties
- **Services:** Land clearing, brush clearing, excavation, earth moving, grading, site prep, retaining walls, driveways, access roads, bushhogging
- **Brand Values:** Environmentally mindful, minimum impact, smaller footprint, working with the land

## Current Status
- **Business license:** Obtained
- **Domain:** `greenwoodlandworks.com` — NOT YET REGISTERED (available, ~$12/yr at Cloudflare)
- **Email:** Grnwoodland@gmail.com (will set up Cloudflare Email Routing for custom domain)
- **Website:** Production-ready static HTML in `site/` — needs real phone number, Formspree form ID, and uncle's photos before deploying
- **Hosting:** Not yet deployed — Vercel or Cloudflare Pages (free tier)
- **Insurance:** Licensed, NOT yet bonded or insured
- **Social media:** None yet
- **Google Business Profile:** Not yet set up

## Project Structure
```
greenwood-landworks/
  site/                                 ← Production website (deploy this directory)
    index.html                          ← Main 5-section site (Home, Services, About, Gallery, Contact)
    albemarle-county-land-services.html ← County SEO page
    greene-county-land-services.html    ← County SEO page
    nelson-county-land-services.html    ← County SEO page
    privacy.html                        ← Privacy policy
    terms.html                          ← Terms of service
    robots.txt                          ← Search engine crawl rules
    sitemap.xml                         ← Sitemap for Google Search Console
    images/                             ← Uncle's real photos go here
  mockups/                              ← Original design mockups (reference only)
    leviathan-landworks-mockup.html     ← V1 dark theme (self-contained SVG)
    leviathan-landworks-v2-light.html   ← V2 light theme (Pexels stock photos)
  docs/                                 ← Business planning documents
    MASTER_PLAN.md                      ← Full 7-phase implementation plan
    greenwood-uncle-checklist.md        ← Info gathering checklist for uncle
    greenwood-photo-guide.md            ← Photography guide for uncle
  GREENWOOD_ROADMAP.md                  ← Quick-reference roadmap with all phases
  CLAUDE.md                             ← This file
```

## Before Deploying (Blockers)
1. Register `greenwoodlandworks.com` at Cloudflare Registrar
2. Create Formspree account → get form ID → replace `YOUR_FORM_ID` in `site/index.html` line containing `formspree.io/f/YOUR_FORM_ID`
3. Replace placeholder phone `(434) 555-0187` with uncle's real number (in `site/index.html` and all 3 county pages)
4. Get real photos from uncle (equipment, job sites) → place in `site/images/` → update `<img>` tags

## Implementation Phases (Summary)
See `docs/MASTER_PLAN.md` for full details.

- **Phase 0:** Information gathering from uncle (checklist + photo guide in `docs/`)
- **Phase 1:** Domain, email, Google Business Profile, social media, directory listings
- **Phase 2:** Deploy website with real content ← CURRENT PHASE
- **Phase 3:** Lead capture, auto-responder, notification pipeline, CRM (Google Sheets)
- **Phase 4:** Invoicing (Wave free), payments (Stripe/Venmo/Zelle), estimate templates
- **Phase 5:** Operations — mileage tracking (Stride), expense logging, equipment maintenance
- **Phase 6:** Growth — Google Reviews, social media cadence, yard signs, seasonal campaigns

## Tech Stack
| Component | Tool | Cost |
|-----------|------|------|
| Website | Static HTML (no framework) | $0 |
| Hosting | Vercel or Cloudflare Pages | $0/mo |
| Domain | Cloudflare Registrar | ~$12/yr |
| Email | Cloudflare Email Routing → Gmail | $0/mo |
| Contact Form | Formspree (free tier, 50/mo) | $0/mo |
| Analytics | Cloudflare Web Analytics or Vercel | $0/mo |
| Invoicing | Wave Accounting (future) | $0/mo |
| Payments | Wave + Venmo + Zelle (future) | Per-txn |

## People
- **Andrew Robb** — manages all tech (website, hosting, SEO, social media, integrations)
- **Peter Farrell** — business owner/operator, uses apps casually on phone
- **Budget:** Free tier now → $50/mo later → more when business grows

## Conventions
- Site is pure static HTML — no build step, no dependencies
- Deploy the `site/` directory only (not root)
- Stock photos from Pexels (free, attribution not required) — replace with real photos ASAP
- All copy emphasizes environmental sensitivity: minimum impact, small footprint, selective clearing, working with the land
- Color palette: amber `#b8860b`, dark `#1c1c1a`, warm white `#faf8f4`, clay `#6b4a32`, green `#5a7a4a`
- Typography: Georgia (display), system fonts (body)

## Key Gotchas
- `YOUR_FORM_ID` placeholder in index.html — must be replaced before deploying
- Placeholder phone `(434) 555-0187` in multiple files — search and replace
- `site/images/` is empty — stock photos are loaded via Pexels CDN URLs until replaced
- County pages link back to `index.html` sections — if site structure changes, update these links
- Formspree free tier = 50 submissions/month — sufficient for a new business, upgrade if needed
