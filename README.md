# Vbluetech – Landing Page

Static site: `index.html`, `styles.css`, `script.js`. No build step, no backend.

**Demo booking:** all "Book a Demo" buttons link to the live Calendly event https://calendly.com/vbluetech/vbluetech-demo-call (15 min, weekdays 9am-5pm Eastern).

## Preview locally
```
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy to GitHub Pages
1. Create a repo (e.g. `vbluetech-site`) and push these files to the `main` branch root.
2. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main` / `(root)` → Save.
3. Site goes live at `https://<user>.github.io/vbluetech-site/` (relative paths work in subfolders).
4. Custom domain: this folder includes a `CNAME` file containing `vbluetech.com`, so GitHub Pages will serve the site at https://vbluetech.com. Point DNS: apex A records to GitHub Pages IPs (185.199.108.153, .109.153, .110.153, .111.153) and/or `www` CNAME to `<user>.github.io`; enable "Enforce HTTPS". (Netlify ignores the CNAME file—set the domain in its dashboard.)

## Deploy to Netlify
- **Drag & drop:** go to https://app.netlify.com/drop and drop this folder (or the zip).
- **From Git:** New site → Import from Git → pick the repo; build command: *(empty)*, publish directory: `.`
- Add a custom domain under Site settings → Domain management.
