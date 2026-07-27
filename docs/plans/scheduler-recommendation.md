# Scheduler recommendation — no Google, AI-native ready

**Decision for Crawford Law PLLC:** use **Cal.com** as the scheduling system of record, synced to **Microsoft Outlook / Microsoft 365** (or Apple Calendar if you prefer). Do **not** depend on a Google account.

**Why this fits:** easiest path that still lets a future Twilio AI assistant **check availability and book** via API — not just text a link.

---

## Short answer

| Need | Choice |
|---|---|
| Calendar you live in daily | **Microsoft 365 Outlook** (recommended) or Apple Calendar |
| Public booking (website + AI) | **Cal.com** |
| Avoid | Building a custom scheduler; Google Calendar; Calendly-only if you care about AI booking |

Calendly is fine for “paste a link,” but its API is weaker for agents that must create bookings. Cal.com is built for that ([agent docs](https://cal.com/docs/agents): slots, create/reschedule/cancel).

---

## Recommended architecture

```text
Your day-to-day calendar
  Microsoft 365 Outlook  (or Apple Calendar)
           ↕ busy/free sync
        Cal.com
     ┌─────┴──────┐
 Website /schedule   Twilio AI assistant
 (embed / link)      (API: get slots → book)
           │
        Webhook
           ↓
   CRM / intake (Clio Grow, Lawmatics, etc.)
```

**System of record for consult bookings:** Cal.com  
**System of record for your personal busy time:** Outlook (or Apple)  
**System of record for matters/clients:** your PMS/CRM (chosen separately)

---

## Why not the other options?

| Option | Verdict |
|---|---|
| **Calendly + Outlook** | Easiest consumer UX; weaker programmatic booking for AI. OK fallback if you only want AI to send a link. |
| **Clio Scheduler** | Best *if* you already commit to Clio Grow + Manage and Outlook sync. AI booking via Clio APIs is heavier; great for legal ops, less “AI-native” out of the box. |
| **Microsoft Bookings** | Free with M365; awkward to drive cleanly from Twilio/LLM tools. |
| **Custom Next.js calendar** | Slowest path; you own every edge case (DST, reminders, no-shows). Don’t. |

**Hybrid later (optional):** Keep Cal.com for public consult booking + AI; sync events into Clio calendar via webhook/Zapier for matter timelines — once PMS is chosen.

---

## Easiest setup path (about 30–45 minutes)

### 1. Get a calendar (no Google)
1. Create a **Microsoft 365** account for the firm (e.g. `andrew@yourdomain.com`) — Business Basic is enough for Outlook calendar.  
2. Or use **Apple iCloud Calendar** if you already live on Apple.

### 2. Create Cal.com
1. Sign up at [cal.com](https://cal.com) (cloud is fine; no need to self-host at launch).  
2. Connect Outlook or Apple under calendar settings (two-way busy/free).  
3. Set timezone: **America/Chicago**.  
4. Create event types, for example:
   - **Intro consult (30 min)** — employers / general  
   - **Urgent workplace consult (20 min)** — limited slots  
   - (Optional) **Training scoping call (30 min)**

### 3. Availability rules
- Working hours you actually take calls (e.g. M–F 9–5 CT, buffers 15 min).  
- Block travel/court/personal on Outlook — Cal.com will show busy.  
- Minimum notice: 24 hours (waive manually for true emergencies).  
- Max per day: protect deep-work / investigation time.

### 4. Put it on the site
- `/schedule` embeds Cal.com (inline embed or branded link).  
- Home + practice pages CTA → `/schedule` or specific event type.  
- Confirmation email/SMS from Cal.com; optional Zapier/Make → CRM lead.

### 5. AI-native readiness (do this at setup — even before Twilio)
Enable now so Phase 2 is plug-and-play:
- [ ] Cal.com **API key** stored as a secret (not in git)  
- [ ] **Webhook** on `BOOKING_CREATED` / `BOOKING_CANCELLED` / `BOOKING_RESCHEDULED` → CRM or a small Next.js route  
- [ ] Note event type IDs/slugs the AI is allowed to book  
- [ ] Confirm booking payload includes: name, email, phone, notes, event type, start time

Twilio AI flow later:

```text
User: "I need a consult Thursday afternoon"
AI: GET Cal.com slots → offer 2–3 times → POST booking
   → SMS confirmation → webhook creates CRM lead
```

Cal.com also exposes agent-oriented tooling ([docs](https://cal.com/docs/agents)); that is the main reason to prefer it over Calendly for your roadmap.

---

## Event types to create first

| Event | Length | Who | Notes field prompt |
|---|---|---|---|
| Initial consultation | 30 min | Anyone | Path (employer/business/personal) + one-sentence issue |
| Employer urgent consult | 20 min | Employers | Urgency + company name (no privileged detail) |
| Training / retainer scoping | 30 min | Employers | Audience size + topic |

Collect **phone** as required on every booking (AI and humans will call/SMS).

---

## AI guardrails (scheduling-specific)

The assistant may:
- Check open slots  
- Book / reschedule / cancel *intro* event types  
- Capture intake path + callback number  

The assistant must not:
- Give legal advice while “scheduling”  
- Book arbitrary calendar holds outside approved event types  
- Discuss strategy or investigation facts on the call beyond short intake notes  

Script opener (reuse on voice/SMS):  
> “I’m the Crawford Law PLLC scheduling assistant — not a lawyer and I can’t give legal advice. I can help you book a consultation.”

---

## If you want the absolute easiest human setup this week

1. Microsoft 365 Outlook for the firm  
2. Cal.com free/cloud → connect Outlook → one “Initial consultation” event  
3. Put the Cal.com link on the site as **Schedule**  
4. Turn on API key + webhook the same day (even if Twilio waits)

That gets you live scheduling **without Google**, and leaves a clean socket for the AI assistant.

---

## Open choices for you

1. **Outlook vs Apple** as the personal calendar? (Recommendation: Outlook / M365 with firm email.)  
2. **Cal.com cloud** (recommended) vs self-host? (Cloud.)  
3. Will Clio be the PMS later? If yes, we still keep Cal.com for public/AI booking and sync into Clio — unless you prefer Clio Scheduler only and accept weaker AI booking.

---

## Related
- [Intake & Twilio AI assistant](intake-and-twilio-assistant.md)
- [Website architecture](website-architecture.md)
