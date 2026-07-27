# Instant Attorney × Crawford Law PLLC — product link plan

**Products (keep separate):**
| Product | Repo | Role |
|---|---|---|
| Firm site | `acrawfo2-hub/CrawfordLaw` | Professional brand, SEO/AEO, employer specialty, Cal.com schedule, traditional Start a File |
| AI intake product | `acrawfo2-hub/Instant_Attorney` → [instant-attorney.com](https://instant-attorney.com/) | Phase I free AI guidance → Phase II privileged intake → Phase III consult with Crawford Law |

**Do not merge the codebases.** Link them with clear CTAs, deep links, and shared analytics — two products, one firm.

---

## How to give me access to both repos

Any of these works (best → fine):

1. **Preferred:** In Cursor Cloud / environment settings, add **both** GitHub repos to the same agent environment (`CrawfordLaw` + `Instant_Attorney`). Then I can read and PR each repo cleanly.
2. **Also fine:** Paste the Instant Attorney GitHub URL in chat (already public: `https://github.com/acrawfo2-hub/Instant_Attorney`). I can clone it read-only for reference, as done this session under `/tmp/Instant_Attorney`.
3. **Not recommended:** Monorepo merge or git submodule just for planning — creates deploy and brand confusion.

For **build work** that touches Instant Attorney (e.g. UTM landing, “referred from firm site” banner), open a separate cloud agent or multi-repo environment on `Instant_Attorney` and reference this plan.

---

## Visitor paths on the firm site

Crawford Law PLLC homepage / practice pages should offer **three clear next steps** (not six):

| CTA | Best for | Destination |
|---|---|---|
| **Start AI Intake** (primary alternate) | People who need to get bearings, draft facts, or prefer async | `https://instant-attorney.com/free-chat` (+ query params below) |
| **Schedule a Consultation** | Ready to talk / employers with urgent matters | Cal.com `/schedule` on firm site |
| **Call** | Highest urgency | `(309) 391-3489` |

Optional quaternary: **Start a File** (short firm web form) for people who want traditional intake without Instant Attorney.

### Deep-link standards (firm → Instant Attorney)

Always append attribution so Instant Attorney (and you) can see firm-site referrals:

```text
https://instant-attorney.com/free-chat
  ?utm_source=crawfordlaw
  &utm_medium=website
  &utm_campaign=firm_ai_intake
  &ref=crawfordlaw
```

Practice-aware links (Instant Attorney already supports `area=` on free-chat):

| Firm page | Suggested Instant Attorney URL |
|---|---|
| Employment hub / investigations / leave | `.../free-chat?area=employment&utm_source=crawfordlaw&...` |
| Business formations / contracts | `.../free-chat?area=business&...` or `area=contract` |
| Estate | `.../free-chat?area=estate&...` |
| Family | `.../free-chat?area=family&...` |
| Generic / About / Home | `.../free-chat?utm_source=crawfordlaw&...` |

Phase III consult (if sending someone straight to paid consult inside Instant Attorney):

```text
https://instant-attorney.com/register?upgrade=consult&utm_source=crawfordlaw&utm_medium=website
```

Prefer **free-chat first** from the firm site so privilege/disclaimer messaging stays correct.

---

## Where “AI Intake” appears on the firm site

### Homepage
- Hero CTA group: **Schedule** · **Start AI Intake** (secondary) · Call text link  
  - Or: primary Schedule for employer brand; AI Intake as equally weighted second button if you want product growth.
- Below dual path (*Employers* | *Business & Personal*): add a slim band:

> **Prefer to start with AI?** Get free, plain-English bearings in Instant Attorney — then book a consult with Crawford Law when you’re ready.  
> [Start AI Intake →]

### Practice pages
- Sticky CTA: Schedule | AI Intake | Call  
- FAQ: “Can I start with an AI intake?” → yes, with Phase I disclaimer summary + link

### About / Contact
- Link Instant Attorney as the firm’s AI-powered intake channel  
- Keep Cal.com + phone as human paths

### Footer
- Instant Attorney · Privacy · Disclaimer (with privilege note pointing to IA Phase I limits)

---

## Recommended copy (firm site — professional)

**Button:** Start AI Intake  

**Supporting line:**  
> Free AI-powered guidance from Instant Attorney — operated with Crawford Law PLLC. General information only until you engage counsel.

**Employer nuance:**  
Instant Attorney’s public marketing leans broad/consumer (including wrongful termination framing). On **employer** practice pages, prefer:

> **Prepare your matter with AI intake** — gather facts and documents, then schedule a privileged consult with counsel.

…and deep-link `area=employment` (or a future employer-specific area if you add one in Instant Attorney).

If Instant Attorney remains primarily individual/plaintiff-oriented, keep the firm site’s **employer** primary CTA as **Schedule / Call**, and promote AI Intake more strongly on Business & Personal / general pages.

---

## Reverse links (Instant Attorney → firm site)

Already branded to Crawford Law. Ensure Instant Attorney also links:

- Firm homepage (SEO entity)  
- Attorney bio / About on firm domain  
- Direct Cal.com or firm `/schedule` as alternate to in-app Phase III when useful  

Suggested firm URL params from IA:

```text
https://<firm-domain>/schedule?utm_source=instantattorney&utm_medium=product
https://<firm-domain>/about?utm_source=instantattorney
```

---

## Photo placement (when re-attached)

Use the preferred photo where it builds **named trust**:

1. **Best:** `/about` primary portrait  
2. **Also strong:** Homepage below-fold credibility / About teaser (not competing with brand wordmark in the first 3 seconds if the hero is full-bleed atmosphere)  
3. **Avoid:** Tiny nav avatar only; don’t collage it with Instant Attorney UI screenshots in the hero  

**Note:** The image from your last message did not arrive in this environment’s uploads folder. Please re-attach it (or drop it into the CrawfordLaw repo / uploads) and I’ll place it in the asset plan and build.

---

## Technical integration (MVP vs later)

### MVP (firm site build)
- External links only (no iframe of Instant Attorney on firm domain — keeps privilege/disclaimer UX clean and avoids cookie/session mess)
- Shared UTM/`ref` query params  
- Optional `window.open` vs same-tab: prefer **same tab** for intake continuity  

### Later (nice)
- Instant Attorney reads `ref=crawfordlaw` and shows “Referred from Crawford Law PLLC”  
- Webhook: IA Phase III booked → firm CRM / Cal.com hold  
- Twilio firm assistant can offer: “I can start AI intake or book a live consult” → routes to free-chat or Cal.com API  

---

## Ethics / messaging checklist

- [ ] Firm site never implies Phase I Instant Attorney chat is privileged legal advice  
- [ ] Distinguish Instant Attorney product name vs Crawford Law PLLC firm name  
- [ ] Employer pages don’t accidentally sound like plaintiff mills  
- [ ] Consult pricing on IA ($49.99) vs firm Cal.com consult — keep consistent or explain difference  

---

## Proceed recommendation

1. Keep planning/build in **CrawfordLaw** for the firm site.  
2. Add Instant Attorney CTAs + deep links per this doc.  
3. Re-attach the preferred photo.  
4. Optionally add `Instant_Attorney` to the Cursor environment when you want me to implement referral banners / UTM handling on that side.  
5. Do **not** wait on merging repos to start the firm site.

---

## Related
- [Website architecture](website-architecture.md)
- [Scheduler recommendation](scheduler-recommendation.md)
- [Intake & Twilio](intake-and-twilio-assistant.md)
