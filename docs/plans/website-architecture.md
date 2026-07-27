# Website Architecture Plan — Crawford Law PLLC

**Status:** Planning (research complete; messaging draft ready; build not started)  
**Brand:** Crawford Law PLLC — **law only** (not joint with finance)  
**Location:** 300 Bello Drive, Leander, Texas 78641 (Williamson County / North Austin metro)  
**Attorney:** Andrew M. Crawford, J.D., SPHR (licensed TX & IL)  
**Entity:** Texas PLLC, SOS File No. 806712661 (effective 07/24/2026)  
**Scheduling phone (current):** `(309) 391-3489`  
**Planned:** New local number + Twilio AI assistant for intake/scheduling  
**Content sources:** Resume (primary for bio/proof) · [crawfordlawfinance.com](https://crawfordlawfinance.com/) (Andrew photos + adaptable employment copy only)

---

## 1. Strategic positioning (drives all IA)

### Recommended brand thesis
**Primary:** Employer-side labor & employment counsel for Central Texas — workplace investigations, FMLA/ADA leave & accommodations, trainings, labor relations, and day-to-day employer counsel — grounded in **Fortune 100–scale in-house experience** (Deere & Company; Microsoft / Activision Blizzard King).  
**Secondary:** Trusted local counsel for business formations, contracts, family law, and estate planning.

### Core differentiator
Andrew is not a brochure “outside advisor” bio. He advised senior leadership inside **Deere & Company** (Labor Relations Manager; CBA covering **10,000** unionized employees; compliance for **1,200+** distribution employees) and within **Microsoft’s Activision Blizzard King** organization (HR Manager & Legal Advisor; first-contract bargaining for **700+** QA employees), plus employment-law HR leadership at The Boring Company. **J.D. Magna Cum Laude + SPHR + dual TX/IL licensure.** That operator-at-scale story is the trust engine.

### Brand boundary (firm)
**Crawford Law PLLC is solo law.** No finance co-brand, no joint homepage, no Vicky/finance services in navigation. Prior Law & Finance site may donate Andrew photos and employment copy only.

### Homepage promise (draft)
> Crawford Law PLLC — Employment counsel shaped by Fortune 100 in-house experience, for Leander and Central Texas employers — plus practical counsel for business and personal matters.

Headline options:
- “Fortune 100–tested employment counsel — now for Central Texas employers.”
- “Investigations, leave, labor, and training — from someone who has owned those problems inside the company.”
- “Clear counsel when work gets complicated.”

---

## 2. Information architecture

```text
/
├── /employment/                          ← Specialty hub
│   ├── /workplace-investigations/        ← resume expertise + CLF copy
│   ├── /fmla-ada-leave-accommodations/   ← resume “Accommodation and Leaves”
│   ├── /workplace-training/              ← NEW productized offering
│   ├── /labor-relations/                 ← Deere / ABK bargaining proof
│   ├── /agency-defense/                  ← NLRB / EEOC / ULP
│   └── /employer-counsel/                ← consulting, policies, contracts, pay design
├── /business-personal/                   ← Secondary hub
│   ├── /business-formations/
│   ├── /contracts/
│   ├── /family-law/
│   └── /estate-planning/
├── /start-a-file/                        ← Web intake router
├── /schedule/                            ← Book consultation
├── /about/                               ← Resume-accurate Fortune 100 bio
├── /approach/                            ← How we work / engagement models
├── /resources/                           ← Guides & insights (AEO content)
│   └── /resources/[slug]/
├── /service-area/                        ← Leander + North Austin / Williamson
├── /contact/                             ← (309) 391-3489 + forms; later Twilio number
├── /client-portal/
├── /privacy/
└── /disclaimer/
```

**MVP trim if needed:** Ship Investigations, Leave/Accommodations, Training, Labor Relations, Employer Counsel first; fold Agency Defense into Employer Counsel until content is ready.

### Navigation (desktop)
**Primary:** Employment · Business & Personal · About · Resources · **Start a File** (button) · **Schedule** (button)

Mobile: sticky bottom bar — **Call (309) 391-3489** | Schedule | Start a File

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
2. One headline (Fortune 100–tested / employer counsel — see messaging doc)
3. One supporting sentence (Leander / Central Texas · TX & IL licensed)
4. CTA group: **Schedule a Consultation** · **Start AI Intake** (→ Instant Attorney) · tap-to-call **(309) 391-3489**
5. One dominant full-bleed visual — professional attorney photography (user-preferred portrait when provided)

**Below the fold (ordered):**
1. Two-path chooser: *For Employers* | *For Business & Personal Matters*
2. Employment service cluster: Investigations · Leave & Accommodations · Training · Labor Relations
3. **Fortune-scale credibility band** (Deere · Microsoft/ABK · headcounts — short; see messaging doc)
4. **AI Intake band** — Instant Attorney free-chat (Phase I disclaimer; deep link with UTMs)
5. Short “How engagement works” (4 steps) — AI intake *or* schedule *or* call
6. About Andrew teaser → `/about`
7. Local trust line (Leander · Williamson County · Texas · also licensed in Illinois)
8. Final CTA band + phone

**Avoid on first viewport:** logo soup, multi-card grids, floating badges, schedule widgets, address blocks, blog teasers, finance co-branding.

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

**Content source map:**

| Spoke | Source | Build note |
|---|---|---|
| Workplace Investigations | Resume expertise + CLF investigations copy | Lead with Fortune-scale investigation experience |
| FMLA / ADA / Leave | Resume “Accommodation and Leaves” + Boring FLSA/FMLA counsel | Texas-forward process page — priority specialty |
| Workplace Training | New productization | Managers / HR / investigations / leave modules |
| Labor Relations | Resume Deere CBA + ABK/CWA bargaining | Strongest differentiator — keep prominent |
| Agency Defense (NLRB/EEOC/ULP) | CLF defense copy + resume ER/LR work | Own page or subsection of Employer Counsel |
| Employer Counsel | Resume counseling + handbook/policy/incentive pay | Policies, RIFs, agreements, compensation design |

### C. Business & Personal hub + spokes
Same template, lighter depth at launch. Prioritize formations, contracts, estate planning, family law with honest scope language (what you handle vs refer).

### D. About (`/about`)
Full publish-ready draft: [Attorney bio & messaging](../content/attorney-bio-and-messaging.md)

1. Hero photo + Andrew M. Crawford, J.D., SPHR  
2. Licensure: Texas & Illinois · Leander · `(309) 391-3489`  
3. Fortune 100 / in-house professional summary  
4. Narrative: Deere → Boring Company → Microsoft/ABK  
5. Career timeline + education  
6. CTA: Schedule / Start a File / Call  
7. `Person` schema with credentials, `alumniOf`, `knowsAbout`, `sameAs`

### E. Start a File (`/start-a-file`) — conversion spine

**Step 0 — Path:** Employer / workplace · Business · Personal / family / estate  

**Step 1 — Short pre-screen (3–6 fields):** name, email, phone, organization (if applicable), one-sentence issue, urgency, preferred consult mode  

**Step 2 — Conflict basics:** adverse parties + acknowledgment that consult ≠ representation  

**Step 3 — Schedule:** embedded scheduler **or** call `(309) 391-3489` (later: Twilio AI books / creates lead)  

**Step 4 — Confirmation:** next steps + deeper questionnaire + secure upload instructions  

**Step 5 — Post-consult:** engagement letter → LawPay → CMS matter + portal  

### F. Resources
Publishing cadence target: 2 posts/month initially, mapped to practice FAQs. Every article links to the relevant spoke + Start a File.

### G. Service Area
One substantive page: Leander base (300 Bello Drive), North Austin / Williamson County employers and families, in-person + remote counsel. Real local context — no thin city doorway pages.

---

## 4. Intake & appointment system architecture

```text
Website / Phone / (later) Twilio AI
    ↓
Lead captured (web form | call | AI voice/SMS)
    ↓
CRM / intake tool (Clio Grow | Lawmatics | MyCase)
    ↓
Auto: confirmation + conflict flag to attorney
    ↓
Scheduler books consult  OR  AI offers slots
    ↓
Deeper matter questionnaire (conditional by practice)
    ↓
Consult → engagement letter → LawPay → CMS matter + portal
```

**Current public phone:** `(309) 391-3489`  
**Soon:** New firm number + Twilio AI assistant — see [Intake & Twilio AI assistant](intake-and-twilio-assistant.md)

### Recommended stack options (solo-friendly)

| Need | Option A (Clio-centric) | Option B (intake-first) |
|---|---|---|
| Intake + CRM | Clio Grow | Lawmatics |
| Practice management | Clio Manage | Clio Manage or MyCase |
| Scheduling | **Cal.com** → Outlook/Apple | Same (AI uses Cal.com API) |
| Voice/SMS AI (Phase 2) | Twilio + Agent Connect / ConversationRelay | Same |
| E-sign | Native / HelloSign | Native |
| Payments | LawPay | LawPay |
| Portal | Clio portal | MyCase portal |

**Decision rule:** If you already plan Clio for billing/matters, use **Clio Grow + Scheduler** for least glue code. Add Twilio as the phone front door once the new number is ready — do not block MVP launch on AI.

### Ethical / operational requirements
- Clear disclaimer before consult and on AI channels (assistant is not a lawyer; no legal advice)
- Conflict check before engagement
- No legal advice via public forms or AI assistant
- Secure transport of uploads; avoid emailing sensitive investigation files unencrypted
- Texas advertising / communication rules compliance on testimonials and outcomes language
- NAP cutover plan when replacing `(309) 391-3489` on public listings
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
- [ ] Domain + professional firm email (not personal Gmail as primary)
- [ ] GBP claimed (Crawford Law PLLC, Leander) with phone **(309) 391-3489**
- [ ] State Bar / Avvo / Justia profiles with consistent NAP
- [ ] Professional photography (import or new headshot) + distinctive brand direction
- [ ] Confirm public wording for current/most recent Microsoft–ABK role

### Phase 1 — MVP site (conversion-ready)
- [ ] Home (Fortune 100 credibility + dual path + phone CTA)
- [ ] Employment hub + spokes: Investigations, Leave/Accommodations, Training, Labor Relations, Employer Counsel
- [ ] Business & Personal hub + 4 spokes (lighter)
- [ ] About (resume-accurate bio), Contact, Service Area
- [ ] Start a File + Schedule wired to CRM/calendar; click-to-call `(309) 391-3489`
- [ ] Privacy + disclaimer
- [ ] Schema + sitemap + Search Console / Bing

### Phase 2 — Twilio AI + authority
- [ ] Provision new firm number on Twilio
- [ ] AI voice/SMS assistant for intake/scheduling (no legal advice)
- [ ] Cut over NAP on site, GBP, directories
- [ ] Agency Defense spoke (if not folded earlier)
- [ ] Resource articles + FAQ expansion
- [ ] Reviews + local backlinks

### Phase 3 — Optimization
- [ ] Conversion tuning (form fields, CTA copy by path)
- [ ] AI citation audits monthly
- [ ] Expand only high-performing subtopics

---

## 7. Sitemap wireframe (user flows)

### Employer in crisis
Google/AI → Investigations page → Call `(309) 391-3489` or Start a File (Urgent) → Schedule → Deep intake → Consult

### HR planning training
Resources or Training page → Schedule → Scoped engagement / retainer discussion

### Local small business formation
Business Formations page → Start a File (Business) → Schedule → Engagement

### Family / estate
Spoke page → Schedule (often lower urgency) → Consult → Engagement

### After Twilio launch
Missed call / after-hours SMS → AI qualifies + books or creates CRM lead → Andrew confirms

---

## 8. Messaging guardrails

**Do**
- Lead with Fortune 100–scale in-house facts (Deere; Microsoft/ABK) and concrete headcounts
- Speak to employers as operators (“investigate cleanly”, “document the interactive process”)
- Name Texas / Leander / Central Texas where true; note IL license when relevant
- Separate employer vs personal paths early
- Keep the firm **law-only** and visually restrained/professional

**Don’t**
- Co-brand with finance or imply a joint firm
- Imply plaintiff-side employment representation if that’s not the practice
- Guarantee investigation or case outcomes
- Overload the hero with every practice area or logo walls
- Use thin multi-city doorway pages
- Publish personal Gmail as the primary firm email

---

## 9. Open decisions (resolve before build)

1. **Domain:** crawfordlaw.com / crawfordlawpllc.com / crawford.law / other?
2. **Practice management stack:** Clio vs MyCase vs other? (Keep **Cal.com** for public/AI booking unless you deliberately choose Clio Scheduler-only.)
3. **Personal calendar backend:** Microsoft 365 Outlook (recommended) vs Apple Calendar?
4. **Office posture:** Publish 300 Bello Drive on GBP/site, or service-area only?
5. **Fee posture:** publish consult fee / ranges, or “contact for engagement terms”?
6. **Family law / estate scope:** full representation vs uncontested / planning-only at launch?
7. **Photos:** Import prior `andrew.jpg` or commission new professional headshots?
8. **Primary CTA verb:** “Start a File” + “Schedule” (recommended) vs phone-first?
9. **ABK role wording:** “Present” vs “Most recently” at launch?
10. **Twilio number:** prefer 512/737 local vs keep 309 publicly until cutover?
11. **Firm email:** which domain mailbox becomes public contact?

---

## 10. Success criteria

| Goal | Signal |
|---|---|
| Professional first impression | Bounce/time on home; qualitative feedback |
| Search visibility | GBP actions; rankings for core Leander + employment queries |
| AI visibility | Named in answers for 3+ target queries within ~90 days of content+schema |
| Conversion | Intake starts + booked consults from web and phone |
| Ops ease | New matter data lands in CMS without retyping; later AI leads arrive structured |

---

## Related docs
- [Attorney bio & messaging](../content/attorney-bio-and-messaging.md)
- [Intake & Twilio AI assistant](intake-and-twilio-assistant.md)
- [Scheduler recommendation](scheduler-recommendation.md)
- [Small-firm website benchmarks](../research/small-firm-website-benchmarks.md)
- [Local & AI search research](../research/local-and-ai-search.md)
- [CLF content inventory (photos/copy only)](../research/crawfordlawfinance-content-inventory.md)
