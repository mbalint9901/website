# balintmazzag.com

Personal site — static HTML/CSS, no build step, no framework.

## Structure

```
├── index.html          Home (bio + links)
├── projects.html        Portfolio of projects
├── publications.html    Publications list
├── styles.css            Shared, mobile-first stylesheet
├── LICENSE               MIT
├── .gitignore
└── logo.png              ← add your own square photo here (not included)
```

## Before deploying

1. **Add `logo.png`** — a roughly square photo of yourself. Used three ways: small (32–36px, circular) in the header nav, larger (72–88px, circular) in the Home hero, and as the favicon + social-share preview image. If you want a sharper link-preview image later, a dedicated 1200×630 `og-image.png` swapped into the `og:image`/`twitter:image` meta tags will look better than a cropped square photo — not required to start.
2. **Replace placeholder links** — search each file for:
   - `yourusername` → your GitHub username
   - `you@example.com` → your real email
3. **Fill in real content** — look for `<!-- REPLACE: ... -->` HTML comments in `projects.html` and `publications.html` for exact formatting to add real entries.

## Deploying (Cloudflare Pages)

1. Push this folder to a GitHub repo
2. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**
3. Framework preset: **None**, build command: empty, output directory: `/`
4. Once deployed, attach your custom domain under **Custom domains**

## Repo visibility

Fine to keep private while placeholders are still in place. Once real content is in and `logo.png` is added, there's no technical reason to keep it private — it's a static site, so the deployed page's HTML/CSS is already fully visible via "View Source" to anyone regardless of the repo's visibility.

## Design notes

- Typography: **Cardo** (headings) + **Inter** (body) — matches WordPress's Twenty Twenty-Four default theme, for visual consistency with the blog at blog.balintmazzag.com
- Mobile-first CSS: base styles in `styles.css` target small screens; the single `@media (min-width: 640px)` block layers on desktop spacing/sizing
- No JS, no build tooling — edit the HTML directly and redeploy
