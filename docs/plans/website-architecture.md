# Website Architecture Plan — Crawford Law PLLC

**Status:** Planning (research complete; build not started)  
**Brand:** Crawford Law PLLC  
**Location:** Leander, Texas (Williamson County / North Austin metro)  
**Attorney:** Andrew Michael Crawford  
**Entity:** Texas PLLC, SOS File No. 806712661 (effective 07/24/2026)

---

## 1. Strategic positioning (drives all IA)

### Recommended brand thesis
**Primary:** Employer-side employment counsel for Central Texas businesses — workplace investigations, FMLA/ADA leave & accommodations, and practical trainings.  
**Secondary:** Trusted local counsel for business formations, contracts, family law, and estate planning.

### Why this split
Top boutique sites that convert employers (Perez Law, Treaty Oak) win by **sharp product clarity**. Flat “full-service” solos dilute SEO, AEO entity signals, and buyer confidence. Architecture should make employment the **depth engine** and general practice the **local relationship engine**.

### Homepage promise (draft direction)
> Crawford Law PLLC — Employment counsel and practical legal guidance for Leander and Central Texas.

Headline options to stress-test later:
- Employer path: “Workplace issues handled correctly — investigations, leave, and training.”
- Combined: “Clear counsel when work gets complicated — and when life or business needs a lawyer.”

---

## 2. Information architecture

```text
/
├── /employment/                          ← Specialty hub
│   ├── /workplace-investigations/
│   ├── /fmla-ada-leave-accommodations/
│   ├── /workplace-training/
│   └── /employer-counsel/                ← policies, handbooks, day-to-day advice
├── /business-personal/                   ← Secondary hub (general practice)
│   ├── /business-formations/
│   ├── /contracts/
│   ├── /family-law/
│   └── /estate-planning/
├── /start-a-file/                        ← Intake router (conversion spine)
├── /schedule/                            ← Book consultation
├── /about/                               ← Andrew + firm story
├── /approach/                            ← How we work / engagement models
├── /resources/                           ← Guides & insights (AEO content)
│   └── /resources/[slug]/
├── /service-area/                        ← Leander + North Austin / Williamson
├── /contact/
├── /client-portal/                       ← Link out or embed (Clio/MyCase/etc.)
├── /privacy/
└── /disclaimer/
```

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
3. One supporting sentence (specialty + Leander/Central Texas)
4. CTA group: **Start a File** · **Schedule a Consultation** (optional text link: Call)
5. One dominant full-bleed visual (imported photography preferred — attorney/office/real context)

**Below the fold (ordered):**
1. Two-path chooser: *For Employers* | *For Business & Personal Matters*
2. Employment service trio: Investigations · Leave & Accommodations · Training
3. Short “How engagement works” (4 steps)
4. About Andrew teaser → `/about`
5. Local trust line (Leander · Williamson County · Texas)
6. Final CTA band

**Avoid on first viewport:** stats strips, multi-card grids, floating badges, schedule widgets, address blocks, blog teasers.

### B. Employment hub + spokes
Each spoke page is a **solution hub**:

| Section | Purpose |
|---|---|
| Answer-first intro (80–120 words) | SEO + AI extract |
| Who this is for / not for | Qualify employer buyers |
| Process steps | Reduce anxiety |
| What you receive | Deliverables / engagement shape |
| Texas-specific notes | E-E-A-T / AEO |
| Proof / representative scenarios (ethical, no guarantees) | Trust |
| FAQs (6–10) + FAQ schema | AEO |
| CTA module (Start a File / Schedule) | Conversion |

### C. Business & Personal hub + spokes
Same template, lighter depth at launch. Prioritize formations, contracts, estate planning, family law with honest scope language (what you handle vs refer).

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
- [ ] Photography import + brand direction (type, color tokens — avoid generic legal purple)

### Phase 1 — MVP site (conversion-ready)
- [ ] Home
- [ ] Employment hub + 3 spokes (Investigations, Leave/Accommodations, Training)
- [ ] Business & Personal hub + 4 spokes (lighter)
- [ ] About, Contact, Service Area
- [ ] Start a File + Schedule wired to CRM/calendar
- [ ] Privacy + disclaimer
- [ ] Schema + sitemap + Search Console / Bing

### Phase 2 — Authority & AEO depth
- [ ] Employer Counsel spoke
- [ ] 8–12 resource articles from real FAQ demand
- [ ] FAQ expansion on top 4 pages
- [ ] Review generation process
- [ ] First local backlinks (Chamber, SHRM talk, guest post)

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
- Name Texas / Leander / Central Texas where true
- Separate employer vs personal paths early

**Don’t**
- Imply plaintiff-side employment representation if that’s not the practice
- Guarantee investigation or case outcomes
- Overload the hero with every practice area
- Use thin multi-city doorway pages

---

## 9. Open decisions (resolve before build)

1. **Domain:** crawfordlaw.com / crawfordlawpllc.com / crawford.law / other?
2. **Practice management stack:** Clio vs MyCase vs other?
3. **Office posture:** Leander address public on GBP/site, virtual-first, or by appointment only?
4. **Fee posture on site:** publish consult fee / ranges, or “contact for engagement terms”?
5. **Family law / estate scope:** full representation vs uncontested / planning-only at launch?
6. **Photo source:** which existing site assets to import; any new headshots needed?
7. **Primary CTA verb:** “Start a File” vs “Request Consult” vs “Begin Intake”?

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
