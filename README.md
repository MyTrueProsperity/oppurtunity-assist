# Opportunity Assist — Landing Site

Public marketing landing page for **Opportunity Assist**, a My True Prosperity product.
*Opportunity Intelligence for Mission-Driven Growth — Stop chasing. Start choosing.*

Static site: plain HTML, CSS, and JS. No build step. Deploys to Netlify.

## Structure
```
opportunity-assist-site/
├── index.html          # Full landing page (SEO meta + JSON-LD baked in)
├── assets/
│   ├── styles.css      # Styles
│   └── app.js          # Mobile nav + footer year
├── robots.txt          # Crawl directives + sitemap reference
├── sitemap.xml         # Sitemap (update as pages are added)
├── netlify.toml        # Netlify config + security/cache headers
└── .gitignore
```

## What's included (SEO / GEO / AEO)
- Unique title + meta description, canonical URL, Open Graph + Twitter cards
- JSON-LD: Organization, SoftwareApplication, Product offers, FAQPage
- One H1, logical H2/H3, crawlable HTML text, descriptive alt/aria
- robots.txt + sitemap.xml, mobile-friendly, fast (no frameworks)

## Run locally
Just open `index.html` in a browser, or serve it:
```bash
python3 -m http.server 8080   # then visit http://localhost:8080
```

## Deploy: GitHub → Netlify (recommended)
1. Create an empty GitHub repo named `opportunity-assist`.
2. From this folder, push the existing local repo (already initialized):
   ```bash
   git remote add origin https://github.com/<your-account>/opportunity-assist.git
   git branch -M main
   git push -u origin main
   ```
3. In Netlify: **Add new site → Import an existing project → GitHub →** select `opportunity-assist`.
   - Build command: *(leave blank)*
   - Publish directory: `.`
4. Every `git push` to `main` now auto-deploys.

## Custom domain
In Netlify → Domain settings, add `opportunityassist.com` once the domain is ready.
Update the URLs in `index.html` (og/canonical), `robots.txt`, and `sitemap.xml` if the final domain differs.
