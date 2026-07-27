# Intake, scheduling & Twilio AI assistant

**Current scheduling number:** `(309) 391-3489`  
**Soon:** New local/firm number + AI assistant on Twilio for after-hours and first-line intake  
**Brand:** Crawford Law PLLC only (no finance co-brand)

---

## Phase 1 — Launch (human + web)

```text
Site CTAs
  ├─ Call (309) 391-3489     → Andrew / voicemail
  ├─ Schedule                → calendar embed (Clio / Calendly)
  └─ Start a File            → short web intake → CRM → confirm + deeper questionnaire
```

**NAP consistency:** Use `(309) 391-3489` on website, GBP, directories, schema `telephone` until the new number cuts over.

**Disclosure on contact/schedule pages:**  
> Calls and messages may be returned during business hours. For urgent workplace matters, note urgency in your intake form.

---

## Phase 2 — New number + Twilio AI assistant

### Goals
1. Always-on first response (voice + SMS)
2. Qualify path: Employer / Business / Personal
3. Capture name, callback number, short matter summary, urgency
4. Offer bookable consult slots or warm transfer / callback request
5. Hand off cleanly to CRM + Andrew for legal judgment (AI must not give legal advice)

### Recommended channel split

| Channel | Role |
|---|---|
| New Twilio number (primary public) | Voice + SMS front door |
| `(309) 391-3489` | Temporary / personal bridge during cutover, then retire from public NAP |
| Web Start a File | Structured intake (still primary for document-heavy matters) |
| Web Schedule | Self-serve booking for known consult types |

### High-level Twilio architecture

```text
Caller / SMS
    ↓
Twilio number (Voice | SMS)
    ↓
AI assistant (Agent Connect / ConversationRelay or Conversations + LLM)
    ├─ Greets as Crawford Law PLLC virtual assistant
    ├─ States: not a lawyer; no legal advice; confidential intake for scheduling
    ├─ Asks path + urgency + basics
    ├─ Books via scheduler API  OR  creates CRM lead + SMS confirmation
    └─ Escalates to Andrew (SMS alert / warm transfer) when flagged urgent
```

### Compliance & ethics guardrails (non-negotiable)
- Scripted disclaimer at start of every AI voice/SMS session
- No legal advice, no outcome predictions, no interpretation of statutes
- No privileged strategy discussion with AI — intake facts only
- Conflict check remains attorney-side before engagement
- Log retention policy aligned with firm recordkeeping
- Texas advertising / communication rules: AI must not misrepresent who is speaking

### Website UX when AI is live
- Header/click-to-call uses **new Twilio number**
- Contact page: “Speak with our assistant anytime — or schedule directly online”
- Start a File remains available (better for investigations / document upload)
- Optional web chat widget later (same assistant backend)

### Cutover checklist
- [ ] Provision Twilio number (prefer 512 / 737 Austin-area if available)
- [ ] Point DNS/branding; update site + GBP + citations same day
- [ ] 301/notice period for old public number if it was listed elsewhere
- [ ] Test: after-hours SMS, voice booking, urgent escalation
- [ ] Update schema `telephone` and NAP everywhere

---

## CRM handoff fields (AI + web forms)

Minimum payload into Clio Grow / Lawmatics / equivalent:

- full_name  
- phone  
- email (if collected)  
- matter_path (employment | business | personal)  
- urgency (this_week | this_month | planning)  
- summary (short text)  
- source (voice_ai | sms_ai | web_intake | web_schedule)  
- requested_slot (if booked)  
- transcript_url / recording_url (internal only)

---

## Related
- [Website architecture plan](../plans/website-architecture.md)
- [Attorney bio & messaging](attorney-bio-and-messaging.md)
