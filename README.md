# Vbluetech website

Marketing site for Vbluetech — AI voice receptionists, AI chat agents and custom websites for US small businesses.
Plain HTML/CSS/JS: no framework, no build step, no source maps. The only JavaScript is `script.js` (mobile menu toggle, under 1 KB).

## Structure
| Path | Purpose |
|---|---|
| `index.html` | Home (ProfessionalService + WebSite JSON-LD) |
| `services/index.html` | Services |
| `industries/index.html` | Industries |
| `contact/index.html` | Contact (demo booking + email) |
| `404.html` | Custom not-found page (noindex) |
| `styles.css`, `script.js` | Shared styles and menu script |
| `favicon.svg`, `favicon-32x32.png`, `apple-touch-icon.png`, `icon-512.png`, `site.webmanifest` | Icons |
| `og-image.png` | 1200×630 social share image |
| `sitemap.xml`, `robots.txt`, `llms.txt` | Crawler / AI discovery files |
| `netlify.toml` | Publish dir + security headers |
| `CNAME` | `vbluetech.com` (for GitHub Pages; Netlify uses its dashboard) |

All pages share the same header/footer and use root-relative links (`/services/`), so the site must be served from a domain root.
Every page has a unique title, meta description, canonical URL on `https://vbluetech.com/`, Open Graph/Twitter tags and one `<h1>`; inner pages have breadcrumbs with BreadcrumbList JSON-LD. When adding a page, also add it to the nav/footer, `sitemap.xml` and `llms.txt`.

Booking: https://calendly.com/vbluetech/vbluetech-demo-call · Contact: hello@vbluetech.com

## Preview locally
```
python3 -m http.server 8000   # open http://localhost:8000
```

## Deploy
Netlify auto-deploys `main` (https://golden-licorice-225b80.netlify.app). Build command: none; publish directory: `.`.
Custom domain `vbluetech.com` is not connected yet — add it under Netlify → Domain management and point DNS as Netlify instructs.
