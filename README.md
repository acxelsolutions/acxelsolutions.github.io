# Acxel Solutions — Contact Page Template

A static, single-page contact template (original design, not a copy of any
existing company's branding, logo, or copy) inspired by the general layout of
a typical B2B consultancy contact page: top nav, a split hero with contact
details + map on one side and a form on the other, a partner/client strip,
and a dark footer.

## Files

```
index.html        the page
styles.css         all styling
assets/logo.svg    light logo (for dark backgrounds)
assets/logo-dark.svg  ink logo (for light backgrounds, also used as favicon)
assets/map.svg     illustrated map graphic
assets/pattern.svg tiny background texture used on the dark panel
```

No build step, no dependencies besides two Google Fonts loaded via `<link>`
tags in `index.html`. Everything else is plain HTML/CSS.

## Launch it on GitHub Pages

1. Create a new repository on GitHub (e.g. `contact-page`).
2. Add these files to the repo root (keep the `assets/` folder structure).
3. Commit and push:
   ```
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
4. In the repo, go to **Settings → Pages**.
5. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
6. GitHub will publish it at `https://<your-username>.github.io/<repo-name>/`
   within a minute or two.

## Before you launch for real

- The contact form currently submits via `mailto:` (opens the visitor's email
  client) — fine for a demo, but replace `action="mailto:..."` in
  `index.html` with a real backend or a form service (Formspree, Getform,
  Netlify Forms, etc.) for production use.
- Swap the placeholder name, address, phone, email, and partner names for
  your own.
- Replace `assets/map.svg` with a real embedded map (e.g. a Google Maps
  iframe) if you want an interactive one.
