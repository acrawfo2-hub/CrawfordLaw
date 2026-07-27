# Content inventory — Andrew Crawford from crawfordlawfinance.com

**Source:** [https://crawfordlawfinance.com/](https://crawfordlawfinance.com/)  
**Captured:** July 27, 2026  
**Purpose:** Reuse Andrew-relevant copy, credentials, services, and media for **Crawford Law PLLC** (law-only entity). Finance/Vicky content is listed only for boundary clarity — do not port as PLLC offerings unless intentionally cross-referred.

---

## Brand boundary

| Existing site (Law & Finance) | New site (Crawford Law PLLC) |
|---|---|
| Joint brand: Andrew (law) + Vicky (finance) | Solo PLLC: legal services only |
| Positioning: “Where Law Meets Financial Strategy” | Positioning: employer-side employment + local business/personal counsel |
| Contact: info@crawfordlawfinance.com | New PLLC domain/email TBD |
| Phone: **(512) 739-2100** | Reuse if still the practice line |
| Location language: Austin metro | Prefer **Leander** primary + Austin / Williamson metro (per SOS filing) |

**Recommendation:** Treat the existing site as a **content & asset donor**, not a layout clone. Keep Andrew’s operator-credibility story; drop the dual-discipline “one firm” thesis unless you later add a soft referral to finance services.

---

## Assets to import

| Asset path on source | Use on PLLC site |
|---|---|
| `/andrew.jpg` | About + home visual (primary) |
| `/office.png` | About / contact atmosphere (if still accurate) |
| Logo PNG in `/assets/...GOLD_LOGO...` | Only if rights/brand still apply; PLLC may need a distinct mark |
| `/vicky.png` | Do **not** use on PLLC unless a referral/partner page is intentional |

Download during build; optimize with `next/image`; write descriptive alt text (e.g., “Andrew Crawford, attorney at Crawford Law PLLC”).

---

## Identity & credentials (port)

- **Name / style:** Andrew Crawford, J.D., SPHR  
- **Licensure:** Illinois and Texas  
- **Education:** University of Illinois College of Law — J.D., Magna Cum Laude, 2014  
  - Activities: Trial Team, Moot Court, ABA Negotiation Competition  
- **Credential:** SPHR (Senior Professional in Human Resources)  
- **Military:** Army National Guard, Army Officer, 2009–2015  

### Career highlights (port with date verification)

| Org | Role | Dates / location (as published) | Publish note |
|---|---|---|---|
| Activision Blizzard | HR Manager | 2022–Present · Austin, TX | **Verify** before launch — “Present” may conflict with solo practice messaging |
| The Boring Company | Human Resources Manager | 2022 · Bastrop, TX | Port |
| John Deere | Labor & Employee Relations Manager | 2013–2022 · Moline, IL | Core proof story — port |
| Army National Guard | Army Officer | 2009–2015 | Port |

---

## Bio copy blocks (Andrew-only — adaptable)

### Short (home / schema / directories)
> Andrew Crawford, J.D., SPHR — labor and employment counsel licensed in Illinois and Texas. Nearly a decade leading labor and employee relations at John Deere, plus HR leadership roles in Central Texas technology and manufacturing environments.

### Medium (About intro — adapted from source)
> Seasoned legal, labor, and employee relations leader with a proven track record across manufacturing, warehousing, engineering, software, and quality assurance. Andrew has bargained opposite more than 10,000 UAW members, navigated strikes, resolved Unfair Labor Practice and EEOC claims, and led organizations through complex bargaining-unit campaigns.

> He brings deep expertise in investigations — whether NLRB, EEOC, or internal — and experience designing and managing incentive pay systems that drive performance.

> Holding a J.D. from the University of Illinois College of Law (Magna Cum Laude, 2014) and an SPHR certification, Andrew combines legal counsel with strategic HR leadership for employers building productive, compliant teams.

### Differentiator line (keep — this is the E-E-A-T gold)
> Counsel from someone who has held the operational HR / labor seat — not only advised from the outside.

---

## Legal service offerings on source → PLLC mapping

| Source service | Source summary (condensed) | PLLC destination |
|---|---|---|
| **Workplace Investigations** | Defensible investigations; NLRB/EEOC/internal; Fortune 500 & high-growth tech; privilege where appropriate | `/employment/workplace-investigations/` — **priority spoke** |
| **Employment Law Consulting** | In-house-grounded counsel; RIFs; agreement audits; compliant HR infrastructure | `/employment/employer-counsel/` |
| **NLRB, EEOC & ULP Defense** | Defense of ULP/NLRB/EEOC matters across mfg, warehouse, eng, tech | `/employment/agency-defense/` **or** fold into Employer Counsel + Investigations |
| **Labor Relations & Collective Bargaining** | Full union-management cycle; 10K+ UAW table experience; bargaining campaigns | `/employment/labor-relations/` — strong specialty differentiator |
| **Employment Contracts & Agreements** | Offer letters through non-competes; IL & TX enforceability | Under Employment + link from `/business-personal/contracts/` |
| **Incentive Pay & Compensation Design** | Incentive systems from large-workforce experience | Spoke or subsection under Employer Counsel |
| **General Legal Services** | Practical guidance for businesses and individuals | Seed for `/business-personal/` hub |

### Gaps on source vs your stated PLLC focus (add — don’t only port)
- **FMLA / ADA accommodations & leaves** — primary specialty you called out; little dedicated page copy on the finance site → **new spoke required**
- **Trainings** — called out for PLLC; not productized on source → **new `/employment/workplace-training/` spoke**
- Family law / estate planning / business formations — mentioned for PLLC future; only “General Legal Services” on source → build lightly at launch

---

## Proof / stats worth reusing (with care)

| Claim | Use |
|---|---|
| 10K+ union members at the table | Home trust or labor-relations page — factual career claim, not case result guarantee |
| IL & TX licensed | Footer, About, schema `hasCredential` |
| J.D. · SPHR | About, Person schema, directories |
| Industries: manufacturing, warehousing, engineering, software, QA, tech, education | Service-area / About industry list |

Avoid inventing win rates or “results” modules from these stats.

---

## UX / conversion elements worth borrowing

From the source homepage (adapt, don’t clone finance dual-path):

1. **Accepting new clients** signal (if true for PLLC)
2. Clear primary CTA: **Schedule a Consultation**
3. Secondary CTA into practice areas
4. Short consultation request fields (name, email, phone, service needed, timing, channel)
5. Explicit licensure in contact block

Replace “Legal / Financial / Both” service selector with PLLC paths:
- Employment / workplace
- Business
- Personal / family / estate
- Not sure

---

## Contact facts to confirm before publish

- [ ] Keep **(512) 739-2100** on Crawford Law PLLC?
- [ ] Public address: Leander filing address vs Austin metro only?
- [ ] How to describe Activision Blizzard tenure now that PLLC is formed?
- [ ] Cross-link or soft-refer Crawford Law & Finance / Vicky, or fully separate brands?
- [ ] Redirect strategy if finance site URLs compete for Andrew/employment queries?

---

## Suggested reuse checklist for build

- [ ] Import `andrew.jpg` (+ office photo if desired)
- [ ] Rewrite About using medium bio + career/education blocks
- [ ] Port investigations, labor relations, agency defense, contracts, consulting copy into employment spokes (edit brand name → Crawford Law PLLC)
- [ ] Draft new FMLA/ADA/leave and Training pages from scratch
- [ ] Add Person schema: J.D., SPHR, IL/TX bar, sameAs links
- [ ] Use phone in sticky mobile CTA once confirmed
- [ ] Do not port Vicky finance services into PLLC nav
