# Plan: Greenwood Landscaping LLC — Complete Business Launch

## Context

Greenwood Landscaping LLC is a newly licensed heavy machinery land services business in Charlottesville, VA (serving Albemarle, Greene, and Nelson counties). The owner (Andrew's uncle) is a solo operator who uses apps casually. Andrew manages all technical infrastructure. The business is a complete blank slate — no domain, no logo, no invoicing, no photos, no social media. Budget is free-tier-first, scaling to ~$50/mo as value is proven.

Two HTML mockups already exist: V1 (dark, self-contained SVG) and V2 (light, Pexels stock photography). V2 light theme is the recommended production starting point.

---

## Phase 0: Information Gathering (Week 1)

**Goal:** Collect everything from uncle before any technical work begins.

### Checklist for Uncle (Andrew sits down with him)

**Business Identity**
- Full legal name as registered, EIN, VA business license number
- Phone number to use publicly (personal cell or get Google Voice?)
- Confirm email: Grnwoodland@gmail.com
- Physical/mailing address (or service-area-only for Google Business Profile?)
- Hours of operation (mockup has Mon-Fri 7-6, Sat 8-2 — confirm)

**Services & Pricing**
- Verify services list against mockup (brush clearing, retaining walls, earth moving, bushhogging, grading, driveways, land clearing, site prep)
- Pricing structure: hourly? per-job estimate? minimum job size?
- Typical price ranges per service (internal reference)
- Deposit policy: percentage upfront? Fixed amount?
- Payment terms: due on completion? Net 15? Net 30?
- Does he charge for site visit estimates? (industry standard: free for residential)

**Equipment Inventory**
- Full list with make/model/year
- Owned vs. rented per-job

**Service Area**
- Confirm Albemarle, Greene, Nelson counties
- Max travel distance, any exclusions
- Specific towns/communities (for SEO pages): Crozet, Ivy, Free Union, Earlysville, Keswick, Batesville, Nellysford, Stanardsville, Ruckersville, etc.

**About / Story**
- Years of equipment experience (even if LLC is new)
- Why he started the business
- Connection to Charlottesville / the land
- Any certs, training, military service
- 2-3 sentences in his own words about what makes his work different

**Competitors**
- 3-5 local competitor names (for SEO research)

### Photography Guide (Print/Text to Uncle)

**Phone Camera Tips:** Clean lens, landscape (horizontal), tap to focus, shoot during golden hour (sunrise/sunset), no filters.

**Priority 1 — Equipment Shots (before website launch):**
- Each piece of equipment individually, parked on clean ground
- 3/4 angle shot + detail shot of each machine

**Priority 2 — Before/After Jobs (ongoing, starting NOW):**
- Same angle for both before and after (use a landmark to match position)
- Wide establishing shot + closer detail shot
- Take before photo BEFORE any work begins

**Priority 3 — Action Shots (ongoing):**
- Equipment working on site, from safe distance

**Photo Storage:** Create shared Google Photos album "Greenwood Jobs", share with Andrew. Caption each set with: location, service, date.

**Cost:** $0 | **Timeline:** 3-5 days

---

## Phase 1: Foundation (Weeks 2-3)

### 1A. Domain Name
- Primary: `greenwoodlandscaping.com` (check availability)
- Fallbacks: `greenwoodlandscapingva.com`, `greenwoodva.com`
- Register at Cloudflare Registrar (~$12/yr, at-cost pricing, integrated DNS)

### 1B. Professional Email (Free)
- Cloudflare Email Routing: `info@greenwoodlandscaping.com` → `Grnwoodland@gmail.com`
- Configure Gmail "Send As" so uncle replies FROM the custom domain
- Add professional Gmail signature (name, phone, license #, website)
- **$0/month** — upgrade to Google Workspace ($7/mo) later if needed

### 1C. Brand Identity
- **Color palette:** Amber/gold `#b8860b`, dark `#1c1c1a`, warm white `#faf8f4`, clay `#6b4a32`, green `#5a7a4a` (from V2 mockup)
- **Logo:** Start with Canva wordmark (free). Upgrade to professional logo via Fiverr ($50-150) when revenue supports
- **Business cards:** Vistaprint, 250 count (~$25). Include: name, phone, email, website, license #, QR code to website
- **Vehicle magnets:** Pair for truck doors (~$45). Include: business name, phone, website URL

### 1D. Google Business Profile (Critical)
- Create at business.google.com
- Categories: "Landscaping Company" (primary) + "Excavating Contractor", "Land Clearing Service", "Grading Contractor"
- Service area: Charlottesville, Albemarle, Greene, Nelson counties
- Service-area mode (no physical address displayed) if uncle works from home
- Add all services, hours, phone, email, photos
- Verification via postcard (5-14 days) — uncle watches for it in mail
- **$0**

### 1E. Social Media Accounts
- **Facebook Business Page** — essential for local customers 35+
- **Instagram Business** — visual portfolio (before/after, equipment, scenery)
- **Nextdoor Business** — hyperlocal, extremely effective for home services
- Consistent NAP (name, address, phone) across all platforms
- Andrew manages all posting

### 1F. Directory Listings (free profiles)
- Yelp, Angi, Thumbtack, BBB, HomeAdvisor, YP.com
- **NAP consistency is critical** — identical business name, address, phone everywhere

**Phase 1 Cost:** ~$82 one-time (domain + cards + magnets), $0/mo recurring
**Timeline:** 1-2 weeks (Google verification may extend to 3 weeks)

---

## Phase 2: Website Launch (Weeks 3-5)

### Tech Stack Decision
**Keep as static HTML.** Rationale:
- V2 mockup is 95% production-ready already
- Uncle never edits the site — Andrew makes all changes
- Zero dependencies, zero cost, fastest load times, zero security surface
- No Node.js needed (not installed). No CMS needed for a 5-page site
- Squarespace/Wix would cost $12-40/mo with no benefit

**Hosting:** Vercel free tier (Andrew's existing workflow) or Cloudflare Pages
**Contact Form:** Formspree free tier (50 submissions/mo, email forwarding, auto-responder)
**Analytics:** Cloudflare Web Analytics (free, no cookies) or Vercel Analytics

### Production Changes to V2 Mockup

**Content:**
- Replace placeholder phone/email with real values
- Update About with uncle's real story/bio
- Update equipment fleet with actual inventory
- Confirm/adjust services list
- Add real service area towns

**Photos:**
- Replace stock hero with real scenic or equipment photo
- Replace gallery stock photos with real job/equipment photos
- Optimize all images to WebP, lazy load

**Working Contact Form:**
- Formspree endpoint, honeypot spam protection, success/error states
- Auto-responder: "We received your request" confirmation email

**SEO:**
- `<meta>` description, Open Graph, Twitter Card tags
- LocalBusiness JSON-LD schema markup (business name, services, service area, phone, etc.)
- `robots.txt`, `sitemap.xml`
- Favicon + Apple touch icons
- Canonical URL

**County SEO Pages (high-ROI):**
- `albemarle-county-land-services.html`
- `greene-county-land-services.html`
- `nelson-county-land-services.html`
- Each targets "[service] in [county]" keywords with local content (town names, landmarks, common land types)

**Legal Pages:**
- `privacy.html` — contact form data collection disclosure
- `terms.html` — estimates non-binding, price subject to site conditions, VA 811 responsibility

### Site Structure
```
greenwoodlandscaping.com/
  index.html                           (main 5-section site)
  albemarle-county-land-services.html
  greene-county-land-services.html
  nelson-county-land-services.html
  privacy.html
  terms.html
  robots.txt / sitemap.xml / favicon.ico
  images/ (equipment, jobs, hero, og-image)
```

### Post-Launch
- Submit to Google Search Console + Bing Webmaster Tools
- Submit sitemap.xml
- Update all profiles/listings with live URL
- Run Lighthouse audit (target 90+ all metrics)

**Phase 2 Cost:** $0/mo | **Timeline:** 1-2 weeks (depends on photo availability)

---

## Phase 3: Lead Capture & Communication (Weeks 6-8)

### Notification Pipeline
1. Form submission → Formspree → email to Grnwoodland@gmail.com
2. Gmail filter auto-labels as "Website Lead"
3. SMS notification to uncle via Zapier/IFTTT free tier

### Auto-Responder
Formspree auto-reply: "Thanks for contacting Greenwood Landscaping. We'll respond within 1 business day. For urgent needs, call (434) XXX-XXXX."

### Lead Tracking
Google Sheets with columns: Date, Name, Phone, Email, Service, Location, Source, Status, Notes, Follow-up Date

**Status flow:** New → Contacted → Site Visit → Estimate Sent → Accepted → Scheduled → In Progress → Complete → Invoiced → Paid

### Communication Templates (save to uncle's phone)
1. Initial response to inquiry
2. Scheduling site visit confirmation
3. Estimate delivery
4. Job scheduling confirmation
5. Job complete + invoice coming
6. Review request (7 days post-completion)

**Phase 3 Cost:** $0/mo | **Timeline:** 1 week

---

## Phase 4: Estimates, Invoicing & Payments (Weeks 8-12)

### Estimate Template
Professional template (Google Docs or Wave) including:
- Business header with logo, license #
- Customer info, job site address
- Scope of work (explicit inclusions AND exclusions)
- Line-item pricing, deposit amount
- Terms: valid 30 days, deposit to schedule, balance due on completion
- VA 811 notice, cancellation policy
- Acceptance line (signature or email reply)

### Invoicing: Wave Accounting (Free)
- $0/month for invoicing + basic accounting
- Professional templates, tracks paid/unpaid, mobile app
- Receipt scanning, expense categorization, profit/loss reports
- **Why Wave over QuickBooks:** QB is $30/mo. Wave is free. Migrate to QB when complexity demands it.

### Payment Options
| Method | Cost | Notes |
|--------|------|-------|
| Wave Payments (card) | 2.9% + $0.30/txn | Link in invoice, customer clicks to pay |
| Venmo Business | Free | QR code on invoices |
| Zelle | Free | Bank transfer, instant |
| Check | Free | Mailing address on invoice |

### Deposit Collection
Jobs over $500: send deposit invoice via Wave at estimate acceptance. Schedule work only after deposit clears.

### Future: Website "Pay Your Bill" Page
Simple page with Wave payment portal link, Venmo QR, Zelle info.

**Phase 4 Cost:** $0/mo (plus 2.9% on card transactions) | **Timeline:** 1-2 weeks

---

## Phase 5: Operations Optimization (Months 3-4)

### Job Pipeline
Upgrade Sheets to Notion kanban board: Lead → Estimate → Accepted → Scheduled → In Progress → Complete → Invoiced → Paid
(Eventually upgrade to Jobber at $39/mo when revenue supports it)

### Mileage Tracking
**Stride app (free)** — automatic GPS, IRS-compliant export. Uncle taps start/stop when driving to jobs.

### Expense Tracking
Wave (already set up) — log every business expense, photograph receipts, categorize.

### Equipment Maintenance
Google Calendar recurring events for oil changes, filter replacements, greasing, hydraulic checks.

### Quarterly Tax Prep
- Export Wave P&L + Stride mileage each quarter
- Calculate/pay estimated taxes (IRS Direct Pay)
- Budget $200-500 for a CPA for year 1 (heavy equipment depreciation deductions are substantial)

**Phase 5 Cost:** $0/mo | **Timeline:** 1-2 weeks setup

---

## Phase 6: Growth & Marketing (Months 4-6+)

### Google Reviews Strategy
- Send review request text after every completed job (template from Phase 3)
- Direct link to Google review page (create short URL)
- Ask in person at job completion, follow up with text
- Review request cards: small card with QR code, hand to customer (~$15 for 100)
- Respond to every review professionally
- **Goal: 10+ five-star reviews in first 6 months**

### Before/After Portfolio
- Uncle photographs every job (per photography guide)
- Andrew swaps stock photos on website with real job photos over time
- Post to Instagram + Facebook with location tags

### Social Media Cadence
- **Instagram:** 1-2 posts/week (before/after reveals, equipment action, scenic shots)
- **Facebook:** 2-3 posts/week (same content + share in local groups, respond to "looking for" posts)
- **Nextdoor:** Respond to local service requests, post project updates

### Offline Marketing
- Yard signs ($5 each, buy 10-20): place at every job site with permission
- Door hangers ($0.15 each, 200 ct): distribute to 10-20 neighbors of each job site
- Referral cards: "Refer a friend, get $50 off your next service"

### Seasonal Campaigns (email/text to past customers)
- March: spring clearing season
- May: building season prep
- July: bushhogging season
- October: fall driveway/grading work
- January: book spring site prep early

### Paid Leads (when revenue supports ~$200-500/mo)
- Angi Leads, Thumbtack, Google Local Service Ads
- Only start when ROI can be tracked

**Phase 6 Cost:** ~$150 one-time (signs, hangers, cards), $0/mo | **Timeline:** Ongoing from month 4

---

## Legal & Insurance (Address ASAP)

### Insurance (Before Doing Work on Others' Property)
- **General Liability:** $400-800/yr (Next Insurance, Thimble, or local agent)
- **Commercial Auto:** Notify current insurer or get separate policy
- **Equipment/Inland Marine:** Covers theft, damage to heavy equipment
- Display "Licensed and Insured" on site once obtained

### Compliance
- **VA 811 (Miss Utility):** Call 3 business days before any digging. Note on all estimates.
- **Lien Waivers:** Provide to customers upon final payment (free VA templates available)

---

## Uncle's Ongoing Responsibilities (Minimal)

| Frequency | Task |
|-----------|------|
| Daily | Respond to leads (templates provided), log mileage (Stride: tap start/stop) |
| Each job | Before/after photos, photograph receipts |
| After job | Send invoice (Wave app), send review request text |
| Weekly | 5-min lead review call with Andrew |
| Monthly | Review P&L in Wave with Andrew |
| Quarterly | Export records for tax prep |

**Everything else** (website, social media, SEO, directories, marketing) is Andrew's responsibility.

---

## Cost Summary

| | One-Time | Monthly |
|--|----------|---------|
| Phase 0 | $0 | $0 |
| Phase 1 | ~$82 (domain, cards, magnets) | $0 |
| Phase 2 | $0 | $0 |
| Phase 3 | $0 | $0 |
| Phase 4 | $0 | $0 (+ card txn fees) |
| Phase 5 | $200-500 (CPA) | $0 |
| Phase 6 | ~$150 (signs, hangers, cards) | $0 |
| **Total** | **~$432-732** | **~$1/mo (domain renewal)** |

---

## Critical Files

- `leviathan-landworks-v2-light.html` — V2 light theme, production starting point
- `leviathan-landworks-mockup.html` — V1 dark theme, reference for SVG assets
- `GREENWOOD_ROADMAP.md` — Previous roadmap, will be superseded by this plan

## Verification

- Phase 0: Uncle completes checklist and starts taking photos
- Phase 1: Domain resolves, email sends/receives, Google Business Profile submitted, social accounts live
- Phase 2: Website live at custom domain, contact form tested end-to-end, Lighthouse 90+, county pages indexed
- Phase 3: Test form → email → SMS notification pipeline, verify auto-responder
- Phase 4: Create and send a test invoice via Wave, verify payment link works
- Phase 5: Verify Stride tracks a test drive, verify Wave expense entry
- Phase 6: Verify Google review link works, test yard sign design proof
