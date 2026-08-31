# cvpe.dev

Static landing page for **CVPE Development Ltd**, a Finland-registered holding and innovation hatchery (Business ID 3651473-2).

## Stack

- Plain HTML + CSS (no build step)
- Hosted on Cloudflare Pages

## Deployment

The site is deployed from this repo to Cloudflare Pages.

- **Build command:** (none / leave empty)
- **Build output directory:** `.` (repo root)
- Configuration is also declared in `wrangler.toml`.

### Deploy manually

```bash
wrangler pages deploy .
```

## SEO & social sharing

- Meta description, Open Graph, and Twitter Card tags are in `index.html`.
- `og.png` (1200×630) is the social preview image.
- `favicon.svg` is the high-contrast favicon.
- JSON-LD structured data for `Organization` and `WebSite` is included in `index.html`.

## IndexNow / search-engine indexing

The site participates in [IndexNow](https://www.indexnow.org/) so participating search engines are notified when the page changes.

- **Ownership key file:** `c35db314cf66eaaad8f38cd4cd51fb12.txt`
- **Key value:** `c35db314cf66eaaad8f38cd4cd51fb12`
- **Host:** `cvpe.dev`
- **Endpoint:** `https://api.indexnow.org/indexnow`

### Submit a change

After updating the page, ping IndexNow:

```bash
KEY=c35db314cf66eaaad8f38cd4cd51fb12
curl "https://api.indexnow.org/indexnow?url=https%3A%2F%2Fcvpe.dev%2F&key=${KEY}"
```

A successful submission returns HTTP `202 Accepted`. The search engine verifies ownership by fetching the key file from the site root, so the key file must be deployed.

## Files

- `index.html` — the full landing page
- `og.png` — Open Graph / Twitter preview image
- `favicon.svg` — favicon
- `wrangler.toml` — Cloudflare Pages output configuration
- `_headers` — security and cache headers
- `c35db314cf66eaaad8f38cd4cd51fb12.txt` — IndexNow ownership key
