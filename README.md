# poetry-site

A warm, cozy personal site to promote Mac's poems and collections, with links out to Apple Books. Static HTML/CSS — no build step. Deployed on Cloudflare Pages.

## Files

- `index.html` — the whole site (hero, selected poems, collections, about, footer)
- `styles.css` — all styling (warm & cozy theme; edit colors in the `:root` block at the top)
- `images/` — drop your real book covers and author photo here

## How to customize

1. **Apple Books link** — find-and-replace every `APPLE_BOOKS_LINK` in `index.html` with your real Apple Books author/store URL.
2. **Poems** — replace the three placeholder poems in the `#poems` section with your own.
3. **Collections** — update the three book cards in the `#books` section (titles + descriptions). Replace each cover placeholder with a real image (see below).
4. **About** — edit the bio text in the `#about` section and add your photo.
5. **Name / branding** — the brand reads "Mac" in the nav, hero, about, and footer. Change it anywhere you like.

### Using real cover images

Put an image in `images/` (e.g. `images/small-hours.jpg`), then replace the placeholder block in `index.html`:

```html
<!-- replace this placeholder span -->
<span class="book__cover-placeholder" data-title="Small Hours"> ... </span>

<!-- with a real image -->
<img class="book__cover-img" src="images/small-hours.jpg" alt="Small Hours cover" />
```

## Deploying on Cloudflare Pages

This is a plain static site, so the Cloudflare Pages settings are:

- **Framework preset:** None
- **Build command:** _(leave empty)_
- **Build output directory:** `/`

Connect this GitHub repo in the Cloudflare dashboard (Workers & Pages → Create → Pages → Connect to Git) and Cloudflare will redeploy automatically on every push to the main branch.
