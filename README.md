# Capital Mailer Co.

Shared direct-mail co-op for Tallahassee. One postcard, 2,500 Killearn Estates mailboxes, one business per industry.

## Stack

- Plain HTML + CSS, no build step.
- Google Fonts: Fraunces (display) + Inter (body).
- Font-loading gate on `<body>` to prevent FOUT.
- Deploys as a static site to Vercel.

## Local preview

```bash
cd /Users/alec/projects/capital-mailer-co
open index.html          # just double-click in Finder
# or:
python3 -m http.server 8000   # then http://localhost:8000
```

## Deploy to Vercel (free subdomain for now)

```bash
cd /Users/alec/projects/capital-mailer-co
npx vercel              # first time: log in, accept defaults
npx vercel --prod       # promote to production
```

You'll get `capital-mailer-co.vercel.app` (or similar). Point a real domain at it later.

## Updating content

- **Claimed a slot?** Edit `index.html`, find the `<div class="slot-card" data-status="open">` for that industry, change `data-status="open"` to `data-status="claimed"` and the `<div class="slot-card__tag">OPEN</div>` to `CLAIMED`. Redeploy.
- **New card / next neighborhood?** Duplicate `index.html` into `southwood.html` or similar; update headline, zip code, slot list.
- **Logo drop-in:** replace the `<span class="stamp">` blocks with an `<img src="assets/logo.svg">` once Gemini generates the real logo.

## Contact / payments

- Text: 954-614-5352
- Zelle: 954-614-5352
- Email: hello@capitalmailer.co (set up once domain is live)
- Facebook DM: update `<a href="https://facebook.com/">` in `index.html` once the account handle is known.

## Copy rules

- 5th-grade reading level.
- No "AI", no jargon, no "platform" (it's a "card").
- Refund guarantee mentioned at least twice on every page.
