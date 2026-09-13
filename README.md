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

## Set up the contact form (Formspree)

The form now posts to Formspree instead of using a `mailto:` link, which
avoids the "this connection isn't secure" browser warning and doesn't
depend on the visitor having an email client configured.

1. Go to [formspree.io](https://formspree.io) and create a free account.
2. Create a new form and copy the form ID it gives you (looks like
   `https://formspree.io/f/xyzabcde`).
3. In `index.html`, find the `<form>` tag and replace `YOUR_FORM_ID` in
   `action="https://formspree.io/f/YOUR_FORM_ID"` with your real ID.
4. Optionally update the `_next` hidden field to wherever you want visitors
   redirected after submitting (defaults to the site's own contact page).
5. Submit a test message from the live site — it'll show up in your
   Formspree dashboard and get emailed to whichever address you configured
   there. Formspree's free plan includes 50 submissions/month.

The hidden `_gotcha` field is a basic honeypot Formspree uses to filter out
spam bots — leave it in place, just don't remove `display:none` from it.

## Before you launch for real

- Finish the Formspree setup above (the form won't send anywhere until you
  swap in your real form ID).
- Swap the placeholder name, address, phone, email, and partner names for
  your own.
- Replace `assets/map.svg` with a real embedded map (e.g. a Google Maps
  iframe) if you want an interactive one.
