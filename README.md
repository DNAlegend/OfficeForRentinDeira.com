# officeforrentindeira.com

SEO-focused static landing page for **office space for rent in Deira, Dubai**, funnelling visitors to WhatsApp (+971 50 891 0940 — Phygital Business Center).

## Stack
Pure static HTML/CSS/JS — no build step. Fast, great Core Web Vitals, SEO-ready.

## Files
| File | Purpose |
|------|---------|
| `index.html` | The landing page + SEO meta + JSON-LD (LocalBusiness + FAQ schema) |
| `styles.css` | All styles (dark "members club" theme, responsive) |
| `script.js` | Mobile nav, scroll reveal, footer year |
| `favicon.svg` | Site icon |
| `robots.txt` / `sitemap.xml` | Crawler directives |
| `vercel.json` | Clean URLs, caching + security headers |

## Run locally
```bash
npx serve .        # or: python3 -m http.server 3000
```
Then open http://localhost:3000

## Deploy to Vercel
**Option A — CLI**
```bash
npm i -g vercel
vercel            # first run links/creates the project
vercel --prod     # deploy to production
```

**Option B — Git (recommended)**
1. Push this folder to a GitHub repo.
2. In Vercel → **Add New Project** → import the repo.
3. Framework preset: **Other** (no build command, output dir = root). Deploy.

## Connect the domain
In Vercel → Project → **Settings → Domains** → add `officeforrentindeira.com`.
In GoDaddy DNS, point the domain to Vercel:
- **A** record `@` → `76.76.21.21`
- **CNAME** `www` → `cname.vercel-dns.com`

(Or set GoDaddy nameservers to Vercel's if you prefer Vercel-managed DNS.)

## To customise
- **Photos** — replace the Unsplash URLs in `index.html` with your own office photos for best results (and SEO). Drop images in the repo and reference e.g. `/images/office-1.jpg`.
- **Pricing / address / phone** — search `index.html` for the values; the WhatsApp number `971508910940` appears in every CTA link.
- **OG image** — set a real 1200×630 share image and update the `og:image` / `twitter:image` tags.

## Post-launch SEO checklist
- Submit `sitemap.xml` in Google Search Console.
- Create / link a Google Business Profile for the Deira location.
- Add real customer reviews and photos.
