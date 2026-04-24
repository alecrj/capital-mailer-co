# Capital Mailer Co. — Operator Runbook

The private playbook for running each card from first Facebook post to USPS drop.
Public site content lives in `index.html`. This file is for you.

---

## Part 1 — One-Time Setup

Do these once. Reuse forever.

### 1.1 Payments — Zelle
- Primary phone: **954-614-5352**
- Secondary (backup): personal email registered with your bank
- On every invoice text: *"Zelle $350 to 954-614-5352. I'll confirm when it lands."*

### 1.2 Sponsor intake — Google Form
Create at [forms.google.com](https://forms.google.com). Name: **"Capital Mailer Co. — Sponsor Intake"**.

Fields (exactly):
1. Business name — short answer, required
2. Your name — short answer, required
3. Phone — short answer, required
4. Website URL (for QR code) — short answer, required
5. Industry/trade — short answer, required
6. Logo upload — file upload (PNG/JPG/PDF, 10MB max), required
7. Your offer (e.g. "Free roof inspection — mention this card") — paragraph, required
8. Brand colors (hex or description) — paragraph, optional
9. Anything else we should know? — paragraph, optional
10. Which card? — dropdown (Killearn #001, SouthWood #002, etc.) — required
11. Confirm: "I've Zelled $350 to 954-614-5352" — checkbox, required

Link responses to a Google Sheet → that sheet is your production dashboard.

### 1.3 QR codes — Bitly (free tier)
- Sign up at [bitly.com](https://bitly.com) free
- Free tier: 10 dynamic QR codes / month (enough for one card)
- Each QR: point to sponsor's website URL (or landing page if they have one)
- Save every QR's link in the Google Sheet so you can pull scan data at day 30

### 1.4 Design — Canva
- Create a free Canva account
- Custom size: **1875 × 3375 px** (6.25" × 11.25" at 300 DPI with 0.125" bleed)
- Build ONE master template and duplicate per card

### 1.5 Printers — local Tallahassee (get quotes from 2-3)
| Printer | Phone | Notes |
|---|---|---|
| **Gandy Printers** | (850) 878-8171 | 1800 S Monroe St. 48-72 hr turnaround. Known EDDM shop. |
| **Target Print & Mail** | (850) 671-6600 | 2843 Industrial Plaza Dr. Has in-house designer if needed. |
| **Minuteman Press** | (850) 385-4787 | Delta Court. 3-5 day turnaround, backup option. |

Always say: *"2,500 × 6"×11" postcards, 14-pt UV gloss, full color 2 sides, with USPS EDDM indicia on the back, bundled in 100s with facing slips."*

### 1.6 USPS EDDM
- Retail submission portal: [eddm.usps.com](https://eddm.usps.com) — no permit needed
- Drop location: **North Tallahassee Post Office, 3300 Capital Circle NE** — (850) 216-3500
- Rate: ~$0.247/piece (confirm at time of drop, rates drift)
- Form: PS Form 3587 (generated automatically by eddm.usps.com when you select routes)

### 1.7 Facebook groups to join
Join immediately, spend 2 days lurking before posting:
- Tallahassee Business Network
- Tallahassee Small Business Owners
- Tally Local Businesses
- Leon County Business Owners
- Network of Entrepreneurs & Business Advocates (NEBA)
- Access Tallahassee
- Women Wednesdays (if relevant to sponsor mix)
- Killearn Estates Community (Nextdoor equivalent on FB)

Also: Nextdoor app, Killearn Estates neighborhood.

---

## Part 2 — Per-Card Execution Timeline

Target: **7-10 days from first post to mailbox delivery**, aggressive but doable.

### Day 0 — Card setup (30 min)
- [ ] Duplicate the Canva master template, rename to `Killearn #001 — Front + Back`
- [ ] Duplicate the Google Form, rename, update "Which card?" dropdown
- [ ] Update `index.html` — change hero headline if different neighborhood
- [ ] Deploy: `npx vercel --prod`
- [ ] Draft FB post in notes app (see Part 3 templates)

### Day 1-5 — Sales (primary effort)
- [ ] Tue/Wed/Thu @ 6:45-7:15 PM: post in 3-5 FB groups
- [ ] Immediately like/comment on your own post from your business page for algorithmic boost
- [ ] Monitor comments, DM anyone who shows interest within 5 min
- [ ] Send intake form link + Zelle info as soon as someone says yes
- [ ] Update slot tiles on `index.html` (change `data-status="open"` → `"claimed"`) as they pay; redeploy
- [ ] Log every sponsor in Google Sheet

**Stop rule:** if you hit **10 paid sponsors**, the card is break-even — lock the print date and keep selling to fill remaining slots. If at day 14 you have <5, extend by one more week; at day 21, decide to refund or push.

### Day 6 — Asset collection
- [ ] Chase every sponsor for intake form completion (text them directly if not done)
- [ ] Generate Bitly QR for every website URL, save to sheet
- [ ] Verify every logo is high-res (ask for vector/300dpi if blurry)

### Day 7 — Design
- [ ] Open Canva template
- [ ] Drop in logos, business names, offers, phones, QR codes for each of the 14 slots
- [ ] If a slot is empty (card only hit 5-7 sponsors), use "This slot still open — text 954-614-5352" as a filler to preserve the grid visual
- [ ] Export PDF proof — one per sponsor, cropped to their slot
- [ ] Export full card PDF (front + back)

### Day 8 — Proofs + approvals
- [ ] Email each sponsor: their cropped slot PNG + full card PDF
- [ ] Subject: *"Your Killearn card proof — approve or revise by [date, 48 hrs out]"*
- [ ] Log approvals in Google Sheet
- [ ] Accept ONE revision per sponsor, then lock

### Day 9 — Send to printer
- [ ] Final PDF to Gandy (call first, confirm they're ready)
- [ ] Specs: *2,500 × 6"×11", 14pt UV gloss, full color both sides, EDDM indicia on back, bundled 100s with facing slips*
- [ ] Pay on pickup

### Day 10-11 — USPS EDDM drop
- [ ] Log into eddm.usps.com, select routes in 32309 totaling 2,500 homes
- [ ] Print PS Form 3587
- [ ] Drive bundles + form to 3300 Capital Circle NE
- [ ] Pay at counter: 2,500 × $0.215 = **~$537.50**
- [ ] Delivery window: 2-4 business days

### Day 12-15 — Delivery + follow-through
- [ ] Drive to Killearn 2-3 days after drop, snap a photo of the card in a real mailbox
- [ ] Text photo to every sponsor: *"Your card hit Killearn today 📮"*
- [ ] Calendar reminder: 30 days from drop → pull Bitly scan counts, send scan report

---

## Part 3 — Sales Playbook

### 3.1 Primary Facebook post template

```
Putting together a shared postcard going out to 2,500 high-income Killearn
Estates homes (32309). It's 14 local businesses on one oversized card —
one per industry. $350 flat, first come first served, no competitors on
the card with you.

10-sponsor floor or full refund. We don't print until the card is safe.

Who's in?
- Landscaping / lawn ☐
- HVAC / air ☐
- Plumbing ☐
- Roofing ☐
- Pest control ☐
- Pool service ☐
- Pressure washing ☐
- Home cleaning ☐
- Handyman / remodel ☐
- Family dentist ☐
- Insurance agent ☐
- Med spa / aesthetics ☐
- Gym / fitness ☐
- Any other non-competing trade (florist, attorney, real estate, tutor, pet groomer, wine shop) ☐

I'll even help you write an offer that converts — most business owners send me a weak "10% off" and I rewrite it into something like "free [thing], no purchase necessary" that actually gets scans.

Comment your trade or DM me. Site: capitalmailer.co
```

**Post timing:** Tue/Wed/Thu 6:45-7:15 PM. Within 60 sec of posting, like it from your business page and comment from personal account to trigger the FB algorithm.

### 3.2 DM-close script (use verbatim-ish)

Opener (within 5 min of their comment):
> "Hey [name] — saw your comment. [Their industry] slot is still open. Want me to send over a mockup of the card and the Killearn demographics?"

Follow with:
- Link to capitalmailer.co
- Screenshot of the filled "See the card" section (shows real layout)
- Sentence: *"10-sponsor floor means worst case is full refund, no risk on you."*

On yes:
> "Awesome. Zelle $350 to 954-614-5352. Once I see it, I'll lock your slot and send the intake form for your logo + offer. Takes 5 min to fill out."

### 3.3 Objection handling

| They say | You say |
|---|---|
| "How do I know it'll actually ship?" | "10-sponsor floor — we don't print until 10 local businesses are in. If we don't hit 10 in 30 days, you get every penny back. Zero risk." |
| "$350 seems steep" | "Running your own postcard to 2,500 homes is $1,500-4,800 and gets tossed. A shared card stays on the fridge. You're paying ~$0.16 per home for the only ad in your trade." |
| "Does it actually work?" | "Direct mail to homeowners at 80K+ income converts 3-5x better than digital for home services. And nobody else in your trade is on the card — zero competition on this specific piece of paper." |
| "Can I see one that's already run?" | For card #1: be honest — "This is the first Killearn card. That's why the price is low and the refund guarantee is ironclad. Future cards will have case studies." |
| "Can I split payment?" | "Yeah — $200 to lock the slot, $200 when the card hits 10 sponsors. But that's a one-time exception." |

### 3.4 Pricing flexibility

- Standard: **$350**
- Double slot: **$600**
- Last 2 slots, day 10+: can drop to **$300** to fill fast (tell them it's an "early neighbor rate")
- Friends/family: **$300** — but only one of these per card, and they must be a real business with a real offer

Never go below $250 — you're eroding margin for zero gain.

---

## Part 4 — Canva Template Spec

**Document:** 1875 × 3375 px (6.25" × 11.25" at 300 DPI, includes 0.125" bleed each side)

**Safe zone:** 0.125" inside trim on all sides (i.e., stay ≥40px from edge).

### Front side layout
- Top 40px bleed
- Masthead strip (6% of height, ~200px): red bar with "KILLEARN NEIGHBORS CARD" in Playfair/Fraunces serif, "Trusted local services · [Month] 2026" small caps below
- Ad grid: 5 cols × 2 rows, ~6% gap between cells
- Each ad: logo box (left), business name (serif, 14-16pt), offer (sans, in dashed box), phone + QR code row at bottom

### Back side layout
- Top band: return address (left) + USPS indicia (right)
- Middle: "Your Killearn neighbors trust these 14 local businesses" headline + 2-3 sentence intro
- Bottom right: address block — "ECRWSS EDDM Retail / LOCAL POSTAL CUSTOMER / Killearn Estates, Tallahassee FL 32309"
- Bottom left: small CMC stamp logo

### USPS EDDM requirements (non-negotiable)
- Indicia must appear top-right on the address side
- Clear space around address block — no images/text within 0.125" of address
- ECRWSS marking near address block
- Printer usually handles these — verify proof before approving

---

## Part 5 — Post-Ship Playbook

### 5.1 Delivery photo (day of expected drop)
- Drive to Killearn, find any visible residential mailbox
- Photograph the card either sticking out or on the sidewalk (if allowed)
- If you can't get one in a real mailbox, stage one at a friend's house in 32309
- Text to every sponsor with: *"Yours hit mailboxes today 📮 — expect a few calls this week."*

### 5.2 30-day scan report
- Pull Bitly analytics for each sponsor's QR
- Email each sponsor their personal scan count + a thank-you
- Template: *"Your QR was scanned [N] times in the 30 days after delivery. Card #002 (SouthWood) drops [date] — want to lock your trade again? Same $350."*

### 5.3 Testimonial ask
- At day 30, if any sponsor mentions they got leads from the card, ask for a 2-sentence testimonial
- Use on capitalmailer.co for card #002 onward

### 5.4 Repeat sale
- Every sponsor who ran card #1 gets first right of refusal for card #2 at the same $350
- Push this 2-3 days before opening card #2 to FB groups

---

## Part 6 — Deployment Commands

```bash
cd /Users/alec/projects/capital-mailer-co

# Preview locally
open index.html

# Deploy to Vercel
npx vercel                 # first time, log in and accept defaults
npx vercel --prod          # promote to production

# Update a slot status (after a sponsor pays)
# Edit index.html:
#   <div class="slot-card" data-status="open">
# Change to:
#   <div class="slot-card" data-status="claimed">
# And change the tag <div class="slot-card__tag">OPEN</div> to CLAIMED

# Quick git check (if you hook this up to version control later)
git status
```

---

## Part 7 — Financial Reference

### Per-card unit economics (2,500-home Killearn card)

| Line | Amount |
|---|---|
| Revenue (14 × $350) | $4,900 |
| Printing (14pt UV gloss, est. local) | $500-650 |
| USPS EDDM postage (2,680 × $0.247) | $662 |
| Bitly (free tier) | $0 |
| Canva (free tier) | $0 |
| **Total cost** | **$1,162-1,312** |
| **Net profit** | **$3,588-3,738** |

One double slot ($600 vs two standards at $700): card fully sold with 1 double = $4,800 revenue → $3,488-3,638 net profit.

### Break-even math
- 10 sponsors × $350 = $3,500 revenue → $2,188-2,338 profit (hits your $2K target)
- 8 sponsors × $350 = $2,800 revenue → $1,488-1,638 profit (profitable but below $2K goal)
- Floor is 10. Below that, refund and reset.

---

## Part 7.5 — Per-Sponsor Fulfillment Checklist

Every promise on the site maps to a specific action. Copy this into your Google Sheet as a new tab called "Fulfillment Tracker" — one row per sponsor, one column per checkbox. Don't ship a card until every box for every sponsor is checked.

### Per-sponsor tracker (columns in your sheet)

| Column | When | How to verify |
|---|---|---|
| 1. Zelle received ($350) | Day of sale | Bank app confirmation |
| 2. Intake form completed | Within 48 hrs of payment | Google Form response row |
| 3. Offer reviewed — strong? | Upon form submission | If "10% off" → rewrite to "free [thing]" or "$X off by [date]"; confirm with sponsor |
| 4. Bitly dynamic QR created | Day of form submission | Save short link to sheet |
| 5. QR tested (scans to their site) | Before design | Scan with phone → lands on their URL |
| 6. Ad designed in Canva | After 10+ sponsors paid | Proof PNG in shared folder |
| 7. Proof sent to sponsor | Day of design | Email with cropped slot + full card PDF |
| 8. Sponsor approved (or 1 revision done) | 48 hrs after proof sent | "Approved" email reply saved |
| 9. Included in print-ready PDF | Before sending to printer | Visual check of final PDF |
| 10. Card printed + picked up | Print day | Physical card in hand |
| 11. Card dropped at USPS | Drop day | PS Form 3587 receipt |
| 12. Mailbox delivery photo sent | 2-3 days post-drop | Text with photo saved to sheet |
| 13. 30-day scan report sent | 30 days post-drop | Calendar reminder + Bitly screenshot emailed |
| 14. High-res digital copy delivered | After print | Sponsor reply confirming receipt |
| 15. Testimonial request sent (optional) | 30-45 days post-drop | For Card #002 social proof |

### Map — each promise on the site → specific action

| FAQ / site promise | How you fulfill it |
|---|---|
| "6"×11" full-color two-sided postcard" | Gandy print spec: "14-pt UV gloss, full color 2 sides, oversize 6×11" |
| "We design your ad" | Canva layout with their logo + offer + QR + phone; 1 free revision |
| "Help you craft an offer that converts" | Review their intake form offer; rewrite weak ones; confirm back |
| "Embed a trackable QR code" | Bitly dynamic QR pointing to their website URL |
| "Print on 14-pt UV gloss" | Printer spec; verify physical sample before full run |
| "Mail to 2,500 Killearn homes via EDDM" | USPS EDDM Retail submission, 5 routes in 32309 |
| "Industry exclusivity" | Google Sheet locks trade at payment; FB post enforces first-come |
| "30-day scan report" | Bitly dashboard pull at day 30, email each sponsor their number |
| "Photo of your card in a real mailbox" | Drive to Killearn 2-3 days after drop, snap + text |
| "High-res digital copy for your socials" | Export final Canva as high-res PNG, email after print |
| "5-sponsor floor or full refund" (now 10) | Zelle held in your account untouched; refund same day if floor missed |

### Quality gates (don't skip these)

1. **Before accepting a payment**: verify the trade isn't already claimed. Check the sheet.
2. **Before designing**: verify logo is high-res (300 DPI or vector). If not, ask for better file or typeset business name.
3. **Before print**: physical sample from printer to touch-test 14-pt UV gloss stock.
4. **Before USPS drop**: verify bundles are 50-100 per stack with facing slips attached.
5. **Before 30-day scan report**: verify Bitly is still tracking and URLs haven't changed.

If you skip gate #3, you risk printing 2,680 flimsy cards that embarrass you and your sponsors. If you skip gate #4, USPS rejects your mailing at the counter.

---

## Part 8 — Known Gotchas

- **Facebook groups require account age.** A brand-new FB account may be auto-rejected by some groups. Use your real personal account if possible, or lurk 48 hours before posting.
- **USPS EDDM has a 5,000/day/zip limit.** Fine for 2,500 but if you scale to 10K later, split across days.
- **Printer rush fees.** Gandy's 48hr turnaround is standard; 24hr may incur a rush fee. Build 3 days into your timeline.
- **Zelle holds above $1,000.** Some banks flag new-payee Zelles at higher amounts. Confirm your bank doesn't delay $350 transfers from strangers.
- **EDDM facing slips.** Every 100-card bundle needs a facing slip. Printer should do this; if not, use the template from eddm.usps.com and print yourself.
- **Refund UX.** If you refund, send the Zelle back same day with a brief note. Don't ghost. The sponsor becomes a potential buyer for card #2.
