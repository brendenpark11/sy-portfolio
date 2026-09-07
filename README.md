# SY Website — Skeleton

Static HTML/CSS/JS site for Seongmin Yoo's portfolio. No build step, no framework —
GitHub Pages can serve this repo directly. Deliberately kept static: it's the
most secure, most crash-resistant, and fastest option for a site this size
(see `1 - Atlas/SY Website - Launch Checklist` in the Brain vault for why).

## Structure

- `index.html` — home
- `book.html`, `installation.html`, `public-art.html`, `paintings.html`, `performance.html` — category pages
- `artwork-detail.html` — template for one artwork; once real pieces exist, either duplicate per piece or move to a static site generator
- `about.html`, `contact.html`, `shop.html`
- `privacy.html`, `terms.html` — legal pages (required: site has a contact form + a Shopify-linked shop)
- `404.html`
- `css/style.css` — all styling, uses design tokens pulled from the Figma file (colors `#1c1917` / `#78716c`, fonts Cormorant Garamond + Inter)
- `js/main.js` — mobile nav toggle only, intentionally minimal
- `robots.txt`, `sitemap.xml` — SEO scaffolding

## What's already handled

- Real header/nav/footer copy and structure (matches the Figma file)
- Meta tag scaffolding per page (title/description/OG — need real copy)
- Form validation + a honeypot spam field on the contact form
- Mobile nav
- Accessibility: skip link, semantic nav, `aria-current` on active nav item

## TODO before launch (search files for "TODO")

1. **Content** — real images, artwork copy, bio, etc. Nothing here is fake/placeholder text on purpose.
2. **Domain** — replace every `TODO-your-domain.com` (in every `<head>`, `robots.txt`, `sitemap.xml`) once a domain is picked.
3. **Favicon + social preview image** — needs a logo/mark first.
4. **Contact form** — create a Formspree (or similar) account, drop the endpoint into `contact.html`'s `<form action="...">`.
5. **Shop** — set up Shopify, generate a Buy Button embed, paste into `shop.html`.
6. **Legal pages** — `privacy.html` / `terms.html` are drafted; just fill in the remaining `[bracketed]` specifics (form provider, analytics, shipping/return policy, launch date).
7. **Analytics** — pick a lightweight/privacy-friendly tool; add a cookie banner only if it needs one.

## Deploying to GitHub Pages

1. Repo Settings → Pages → Deploy from branch → `main` → `/ (root)`.
2. GitHub Pages gives you free HTTPS automatically.
3. If using a project page (`username.github.io/repo-name`) rather than a custom domain, note the site will live at that subpath — all links here are relative, so they'll still work either way.
