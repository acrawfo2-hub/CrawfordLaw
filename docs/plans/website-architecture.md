# Website Architecture Plan — Crawford Law PLLC

**Status:** Planning (research complete; build not started)  
**Brand:** Crawford Law PLLC  
**Location:** Leander, Texas (Williamson County / North Austin metro)  
**Attorney:** Andrew Michael Crawford, J.D., SPHR (licensed IL & TX)  
**Entity:** Texas PLLC, SOS File No. 806712661 (effective 07/24/2026)  
**Existing content donor:** [crawfordlawfinance.com](https://crawfordlawfinance.com/) — Andrew’s bio, employment services, and photos (see inventory doc)

---

## 1. Strategic positioning (drives all IA)

### Recommended brand thesis
**Primary:** Employer-side labor & employment counsel for Central Texas businesses — workplace investigations, FMLA/ADA leave & accommodations, trainings, labor relations, and day-to-day employer counsel.  
**Secondary:** Trusted local counsel for business formations, contracts, family law, and estate planning.

### Core differentiator (from existing site — keep)
Andrew is not a pure outside advisor bio. He spent nearly a decade in labor & employee relations at **John Deere** (bargaining opposite 10,000+ UAW members; strikes; NLRB), then HR leadership in Central Texas (**Activision Blizzard**, **The Boring Company**), with **J.D. (Magna Cum Laude) + SPHR**. That “operator who became counsel” story is the trust engine for employer buyers — stronger than generic solo-attorney stock language.

### Why this split
Top boutique sites that convert employers (Perez Law, Treaty Oak) win by **sharp product clarity**. Flat “full-service” solos dilute SEO, AEO entity signals, and buyer confidence. Architecture should make employment the **depth engine** and general practice the **local relationship engine**.

### Relationship to crawfordlawfinance.com
That site is a joint Law & Finance brand (Andrew + Vicky). **Crawford Law PLLC** should be the law-only entity site: port Andrew’s legal copy and assets; do **not** port finance services into PLLC navigation. Optional later: soft referral to finance — not required for MVP.

### Homepage promise (draft direction)
> Crawford Law PLLC — Employment counsel grounded in real HR and labor experience, plus practical legal guidance for Leander and Central Texas.

Headline options to stress-test later:
- Employer path: “Workplace issues handled correctly — investigations, leave, labor, and training.”
- Operator path: “Counsel from someone who has sat in the HR seat — and at the bargaining table.”
- Combined: “Clear counsel when work gets complicated — and when life or business needs a lawyer.”

---

## 2. Information architecture

```text
/
├── /employment/                          ← Specialty hub
│   ├── /workplace-investigations/        ← port + expand from CLF
│   ├── /fmla-ada-leave-accommodations/   ← NEW (PLLC focus; weak on CLF)
│   ├── /workplace-training/              ← NEW (PLLC focus)
│   ├── /labor-relations/                 ← port from CLF (major differentiator)
│   ├── /agency-defense/                  ← NLRB / EEOC / ULP (port from CLF)
│   └── /employer-counsel/                ← consulting, policies, contracts, pay design
├── /business-personal/                   ← Secondary hub (from CLF “General Legal”)
│   ├── /business-formations/
│   ├── /contracts/
│   ├── /family-law/
│   └── /estate-planning/
├── /start-a-file/                        ← Intake router (conversion spine)
├── /schedule/                            ← Book consultation
├── /about/                               ← Andrew bio from CLF (rewritten for PLLC)
├── /approach/                            ← How we work / engagement models
├── /resources/                           ← Guides & insights (AEO content)
│   └── /resources/[slug]/
├── /service-area/                        ← Leander + North Austin / Williamson
├── /contact/
├── /client-portal/                       ← Link out or embed (Clio/MyCase/etc.)
├── /privacy/
└── /disclaimer/
```

**MVP trim if needed:** Ship Investigations, Leave/Accommodations, Training, Labor Relations, Employer Counsel first; fold Agency Defense into Employer Counsel until content is ready.

### Navigation (desktop)
**Primary:** Employment · Business & Personal · About · Resources · **Start a File** (button) · **Schedule** (button)

Mobile: sticky bottom bar — Call | Schedule | Start a File

### URL principles
- Human-readable, keyword-honest, stable
- No city spam in every slug; put locality in titles/H1s/schema `areaServed`
- Employment spokes nest under `/employment/` for topical strength

---

## 3. Page-level specs

### A. Landing page (`/`)
**Job:** One professional composition that earns trust in ≤3 seconds and routes the right visitor.

**Above the fold (only):**
1. Brand: Crawford Law PLLC
2. One headline
3. One supporting sentence (specialty + Leander/Central Texas; optional “IL & TX licensed”)
4. CTA group: **Start a File** · **Schedule a Consultation** (optional text link: Call — candidate number `(512) 739-2100` pending confirm)
5. One dominant full-bleed visual — prefer imported **`andrew.jpg`** / office photography from crawfordlawfinance.com

**Below the fold (ordered):**
1. Two-path chooser: *For Employers* | *For Business & Personal Matters*
2. Employment service cluster (not equal-weight clutter): Investigations · Leave & Accommodations · Training · Labor Relations
3. Operator-credibility band (John Deere / Central Texas HR — short, not a résumé dump)
4. Short “How engagement works” (4 steps)
5. About Andrew teaser → `/about`
6. Local trust line (Leander · Williamson County · Texas · also licensed in Illinois)
7. Final CTA band

**Avoid on first viewport:** stats strips, multi-card grids, floating badges, schedule widgets, address blocks, blog teasers.

### B. Employment hub + spokes
Each spoke page is a **solution hub**:

| Section | Purpose |
|---|---|
| Answer-first intro (80–120 words) | SEO + AI extract |
| Who this is for / not for | Qualify employer buyers |
| Process steps | Reduce anxiety |
| What you receive | Deliverables / engagement shape |
| Texas-specific notes (IL notes where dual-license matters) | E-E-A-T / AEO |
| Proof / representative scenarios (ethical, no guarantees) | Trust |
| FAQs (6–10) + FAQ schema | AEO |
| CTA module (Start a File / Schedule) | Conversion |

**Content source map (CLF = crawfordlawfinance.com):**

| Spoke | Source | Build note |
|---|---|---|
| Workplace Investigations | Port CLF “Workplace Investigations” | Strongest ready copy; align to PLLC brand |
| FMLA / ADA / Leave | **New** | Your stated specialty; write Texas-forward process page |
| Workplace Training | **New** | Productize formats (managers, HR, investigations, leave) |
| Labor Relations | Port CLF bargaining / union-management | Rare local differentiator — keep |
| Agency Defense (NLRB/EEOC/ULP) | Port CLF defense copy | Own page or subsection of Employer Counsel |
| Employer Counsel | Port CLF Employment Law Consulting + contracts + incentive pay | Policies, RIFs, agreements, compensation design |

### C. Business & Personal hub + spokes
Same template, lighter depth at launch. Seed from CLF “General Legal Services.” Prioritize formations, contracts, estate planning, family law with honest scope language (what you handle vs refer).

### C2. About (`/about`) — content outline from CLF
1. Hero photo (`andrew.jpg`) + name line: Andrew Crawford, J.D., SPHR  
2. Licensure: Illinois & Texas · based in Leander / Austin metro  
3. Medium bio (investigations, bargaining, SPHR + J.D.)  
4. Career highlights (verify Activision “Present” before publish)  
5. Education + credentials  
6. CTA: Schedule / Start a File  
7. `Person` schema with `hasCredential`, `alumniOf`, `knowsAbout`, `sameAs`

### D. Start a File (`/start-a-file`) — conversion spine
This is the system that makes “start a file with me” easy.

**Step 0 — Path**
- Employer / workplace matter
- Business matter
- Personal / family / estate

**Step 1 — Short pre-screen (3–6 fields)**
- Name, email, phone
- Organization (if employer/business)
- One-sentence issue
- Urgency (this week / this month / planning)
- Preferred consult mode (video / phone / in person)

**Step 2 — Conflict basics**
- Adverse party / opposing company / other involved names (as applicable)
- Acknowledgment that consult ≠ representation

**Step 3 — Schedule**
- Embedded scheduler (Clio Scheduler / Calendly / Lawmatics — pick one stack)

**Step 4 — Confirmation**
- What happens next
- Secure link to deeper intake questionnaire (practice-specific)
- Optional document upload instructions

**Step 5 — Post-consult (ops, may be off-site)**
- Engagement letter e-sign
- Retainer payment (LawPay)
- Matter opened in practice management + client portal invite

### E. About
Named trust page: photo, bio narrative, bar admission, education, `Person` schema, sameAs (LinkedIn, State Bar, Avvo). Solo sites convert when the human is visible.

### F. Resources
Publishing cadence target: 2 posts/month initially, mapped to practice FAQs. Every article links to the relevant spoke + Start a File.

### G. Service Area
One substantive page: Leander base, North Austin / Williamson County employers and families, in-person + remote counsel. Mention real context (local employers, growth corridor) without thin city doorway pages.

---

## 4. Intake & appointment system architecture

```text
Website CTA
    ↓
/start-a-file (path + short form)
    ↓
CRM / intake tool (Clio Grow | Lawmatics | MyCase)
    ↓
Auto: confirmation email + conflict flag to attorney
    ↓
Scheduler books consult
    ↓
Deeper matter questionnaire (conditional by practice)
    ↓
Consult → engagement letter → LawPay → CMS matter + portal
```

### Recommended stack options (solo-friendly)

| Need | Option A (Clio-centric) | Option B (intake-first) |
|---|---|---|
| Intake + CRM | Clio Grow | Lawmatics |
| Practice management | Clio Manage | Clio Manage or MyCase |
| Scheduling | Clio Scheduler | Calendly → CRM |
| E-sign | Native / HelloSign | Native |
| Payments | LawPay | LawPay |
| Portal | Clio portal | MyCase portal |

**Decision rule:** If you already plan Clio for billing/matters, use **Clio Grow + Scheduler** for least glue code. If intake automation is the priority and Clio isn’t chosen yet, evaluate Lawmatics.

### Ethical / operational requirements
- Clear disclaimer before consult
- Conflict check before engagement (and ideally before deep consult when possible)
- No legal advice via public forms
- Secure transport of uploads; avoid emailing sensitive investigation files unencrypted
- Texas advertising / communication rules compliance on testimonials and outcomes language

---

## 5. Technical architecture (site build)

### Suggested stack (when implementation starts)
- **Next.js** (App Router) + clean semantic components
- Hosting: **Vercel**
- CMS: MDX or headless (Sanity/Contentful) for resources + practice FAQs
- Forms: server actions → CRM webhook (do not store sensitive matter details only in a generic email inbox)
- Analytics: privacy-aware (e.g. Plausible or GA4 with consent)
- Schema helpers shared across pages
- Image pipeline for imported photography (next/image, proper alt text)

### SEO / AEO technical must-haves
- `LegalService` + `Person` + `FAQPage` + `BreadcrumbList` JSON-LD
- `robots.txt` allowing major AI crawlers
- XML sitemap
- Canonical URLs
- Open Graph for LinkedIn sharing of resources
- Accessible forms (labels, focus, error states)

### Performance / mobile
- LCP under ~2.5s on practice pages
- Sticky mobile CTAs
- Tap-to-call in header on small screens

---

## 6. Content launch priorities

### Phase 0 — Foundations
- [ ] Domain + professional email
- [ ] GBP claimed (Crawford Law PLLC, Leander)
- [ ] State Bar / Avvo / Justia profiles with consistent NAP
- [ ] Import photography from CLF (`andrew.jpg`, optional `office.png`) + brand direction (avoid generic legal purple / Inter-default look from CLF)
- [ ] Confirm phone `(512) 739-2100`, public address, and current employment disclosures

### Phase 1 — MVP site (conversion-ready)
- [ ] Home (operator-credibility + dual path)
- [ ] Employment hub + spokes: Investigations, Leave/Accommodations, Training, Labor Relations, Employer Counsel (port/adapt CLF where noted)
- [ ] Business & Personal hub + 4 spokes (lighter)
- [ ] About (full Andrew bio from CLF inventory), Contact, Service Area
- [ ] Start a File + Schedule wired to CRM/calendar
- [ ] Privacy + disclaimer
- [ ] Schema + sitemap + Search Console / Bing

### Phase 2 — Authority & AEO depth
- [ ] Agency Defense spoke (if not folded into Employer Counsel)
- [ ] 8–12 resource articles from real FAQ demand
- [ ] FAQ expansion on top 4 pages
- [ ] Review generation process
- [ ] First local backlinks (Chamber, SHRM talk, guest post)
- [ ] Decide CLF ↔ PLLC cross-linking / redirect strategy for overlapping queries

### Phase 3 — Optimization
- [ ] Conversion tuning (form fields, CTA copy by path)
- [ ] AI citation audits monthly
- [ ] Expand only high-performing subtopics

---

## 7. Sitemap wireframe (user flows)

### Employer in crisis
Google/AI → Investigations page → Start a File (Employer / Urgent) → Schedule this week → Deep intake → Consult

### HR planning training
Resources or Training page → Schedule → Scoped engagement / retainer discussion

### Local small business formation
Business Formations page → Start a File (Business) → Schedule → Engagement

### Family / estate
Spoke page → Schedule (often lower urgency) → Consult → Engagement

---

## 8. Messaging guardrails

**Do**
- Speak to employers as operators (“investigate cleanly”, “document the interactive process”)
- Lead with in-house / bargaining-table credibility (Deere, Central Texas HR)
- Name Texas / Leander / Central Texas where true; note IL license when relevant
- Separate employer vs personal paths early
- Reuse proven CLF service language where accurate, under **Crawford Law PLLC**

**Don’t**
- Imply plaintiff-side employment representation if that’s not the practice
- Guarantee investigation or case outcomes
- Overload the hero with every practice area
- Use thin multi-city doorway pages
- Port Vicky/finance offerings into PLLC IA
- Clone the CLF “Law Meets Financial Strategy” thesis on the PLLC homepage

---

## 9. Open decisions (resolve before build)

1. **Domain:** crawfordlaw.com / crawfordlawpllc.com / crawford.law / other?
2. **Practice management stack:** Clio vs MyCase vs other?
3. **Office posture:** Leander address public on GBP/site, Austin metro only, or by appointment only?
4. **Phone:** Keep `(512) 739-2100` as PLLC line?
5. **Fee posture on site:** publish consult fee / ranges, or “contact for engagement terms”?
6. **Family law / estate scope:** full representation vs uncontested / planning-only at launch?
7. **Photos:** Import `andrew.jpg` / `office.png` as-is, or new headshots?
8. **Primary CTA verb:** “Start a File” vs “Schedule a Consultation” (CLF used the latter) vs both?
9. **CLF site future:** keep both brands, redirect employment URLs, or soft cross-link?
10. **Employment disclosure:** How to present Activision Blizzard / current roles alongside solo PLLC?

---

## 10. Success criteria

| Goal | Signal |
|---|---|
| Professional first impression | Bounce/time on home; qualitative feedback |
| Search visibility | GBP actions; rankings for core Leander + employment queries |
| AI visibility | Named in answers for 3+ target queries within ~90 days of content+schema |
| Conversion | ≥ target % of practice-page visitors start intake or book |
| Ops ease | New matter data lands in CMS without retyping |

---

## Related docs
- [Small-firm website benchmarks](../research/small-firm-website-benchmarks.md)
- [Local & AI search research](../research/local-and-ai-search.md)
- [CLF content inventory (Andrew portions)](../research/crawfordlawfinance-content-inventory.md)
