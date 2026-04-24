# Capital Mailer Co. — v1 Spec

Date: 2026-04-23
Status: Built.

## What this is

A shared direct-mail co-op. One postcard sold fourteen times, once per industry, mailed to 2,500 homes in a target Tallahassee zip code. Card #1 targets Killearn Estates (32309). Future cards target SouthWood (32311), Golden Eagle (32312), and other high-income zips.

## Business decisions (locked)

| Decision | Value | Why |
|---|---|---|
| Brand | Capital Mailer Co. | "Capital" = Tallahassee capitol + premium + scales beyond one zip |
| Entity | None yet — personal | Ultra-lean launch, no LLC until first card ships profitably |
| Payments | Zelle to 954-614-5352 | Zero fees, instant, most B2B-legit free option |
| Card size | 6"×11", 14-pt UV gloss, full-color 2 sides | Creator's proven "community card" format |
| Homes | 2,500 | Fillable in 1-2 weeks for first-time seller |
| Slots | 14 total (8 front + 6 back) with double-slot upsell available | Creator's 2,500-home model, dual-sided |
| Price | $350 standard / $600 double | ~13¢/home — balanced for first card |
| Break-even floor | 10 paid sponsors | 10 × $350 = $3,500 vs ~$1,162 cost = $2,338 cushion (hits $2K goal) |
| Refund policy | 100% refund if floor not hit in 30 days | Turns the biggest risk into the primary trust signal |
| Target zip | 32309 Killearn Estates | High route density, established wealth, service-business heavy |
| Distribution | USPS EDDM Retail | No mailing list purchase needed |
| Printer | UPrinting or GotPrint (online) | Cheaper than local, quality indistinguishable |
| Site | Plain HTML/CSS on Vercel free subdomain | Ships in 1 hour, upgrade to domain later |

## Unit economics (per 2,500-home card)

```
Revenue (14 slots sold):    $4,900
Printing (14pt UV gloss):   ~$500-650
Postage (EDDM, $0.247/pc):   $662  (verified 2,680 homes × actual rate)
Total cost:                 ~$1,162-1,312
Net profit:                 ~$3,588-3,738
```

With one double slot (saves buyer $100): 12 standard + 1 double = $4,800 revenue → ~$3,488-3,638 net.

## Value stack per sponsor ($350 buys)

1. Industry exclusivity — no competitor on the same card
2. Ad design in Canva + 1 free revision
3. Dynamic trackable QR code (via Bitly)
4. Custom offer/coupon printed on the card
5. Premium 14-pt UV gloss stock, 6"×11" oversize
6. High-res digital copy of final card
7. Mailbox delivery photo (proof of drop)
8. 30-day QR scan report
9. Cross-sponsor intro list
10. 100% refund guarantee if card doesn't fill

## Site structure (`index.html`)

1. Postal bar (branded header strip)
2. Nav (brand + 4 links + CTA)
3. Hero (headline + postcard mockup)
4. Offer (price card + full value stack)
5. How it works (4 steps)
6. 10-sponsor refund guarantee section
7. Where it lands (Killearn stats + stylized map)
8. Industry slots grid (10 cards, OPEN/CLAIMED state)
9. FAQ (10 questions)
10. Founder section
11. CTA (text / FB / email, all leading to Zelle payment)
12. Footer

## Design system

**Palette (Postal Editorial):**
- Postmark red `#B23A30`
- Red ink shadow `#8E2A22`
- Cream `#F5F1E8`
- Cream deep `#ECE6D5`
- Off-black `#1A1A1A`
- Brass accent `#B8935C`
- Paper `#FAF6EC`

**Type:**
- Display serif: Fraunces (600/700 weight, tight tracking, italic emphasis)
- Body sans: Inter (400/500/600)
- Eyebrow labels: Inter uppercase 12px with 0.22em tracking

**Motifs:**
- Circular postmark stamps with double-line borders
- Paper noise texture (fixed SVG filter)
- Dashed dots dividers (evokes perforation)
- Red dashed zone outline on the map (looks like a mailing boundary)
- Postcard slightly rotated in hero (hand-stamped feel)

## Go-to-market (tomorrow)

1. Create Facebook Business Page for Capital Mailer Co.
2. Join: Tallahassee Business Network, Tally Small Business Owners, NEBA, Access Tallahassee, Tallahassee Entrepreneurs (all FB).
3. Join Nextdoor — post in Killearn Estates community.
4. Tue/Wed/Thu 6:45-7:15 PM: post the offer in each group. Like from personal account + business page for algorithmic juice.
5. Drive Killearn yard-sign commercial strips — snap photos of service-biz yard signs, text them a link to capitalmailer.co.
6. Cold outreach via Google Maps business listings for each of the 14 industries filtered to 32309.
7. Send the site URL in every DM. The site closes; the DM is the handshake.

## Open items (not blocking launch)

- [ ] Generate real logo in Gemini using the prompt in the brainstorming transcript
- [ ] Set up `hello@capitalmailer.co` email (Cloudflare email routing)
- [ ] Buy `capitalmailer.co` domain once first card has 2 paid sponsors
- [ ] Set up Bitly account for dynamic QR code generation
- [ ] Draft Google Form for sponsor intake (logo, phone, offer, website, industry)
- [ ] Get 3 printer quotes (UPrinting, GotPrint, Gandy local) to lock cost
- [ ] Build Canva postcard template with 14 slot grid
