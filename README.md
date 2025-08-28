# The (un)Stable Net — Static Site

A single–page, static website for **The (un)Stable Net** with a blue tech-style hero canvas, editable project covers, and an editable portrait.

## Local preview

Just open `index.html` in a browser.

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `the-unstable-net`).
2. Add these files (at repo root):
   - `index.html`
   - `.nojekyll` (empty file to disable Jekyll)
   - `README.md`
3. Commit & push.
4. On GitHub: **Settings → Pages → Build and deployment**
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` / `/ (root)`
5. Your site will be served at `https://<your-username>.github.io/<repo-name>/`.

> Notes
> - All asset paths are relative, so it works in a project subpath (no extra config).
> - The page stores custom covers & your portrait in **localStorage** (browser-only). To make those images permanent for visitors, replace the default SVG covers with your chosen images in `index.html`, or host them in the repo and reference them with relative paths.

## Deploy to Vercel

### One-click via GitHub import
1. Push this folder to a GitHub repo.
2. Go to Vercel → **Add New Project** → **Import GitHub Repo**.
3. **Framework Preset:** `Other` (Static Site).
4. **Build Command:** _None_
5. **Output Directory:** `.`
6. Deploy.

### Or via Vercel CLI
```bash
npm i -g vercel
vercel --prod
```

## Optional: Social metadata
Add these tags in `<head>` if you want rich link previews:
```html
<meta property="og:title" content="The (un)Stable Net" />
<meta property="og:description" content="A blog about Business, AI & Content Creation" />
<meta property="og:type" content="website" />
<meta property="og:image" content="https://your-domain/og-image.png" />
<meta name="twitter:card" content="summary_large_image" />
```

## License
You own your content. No license is included; add one if desired (MIT/Apache-2.0/etc.).
