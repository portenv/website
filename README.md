# portenv.com

The website for [Portenv](https://github.com/portenv/portenv).

Plain static HTML and CSS: no framework, no build step, no third-party requests.

| File | What it is |
| --- | --- |
| `index.html` | Home page |
| `privacy.html` | Privacy notice for the website (served at `/privacy`) |
| `legal.html` | Legal notice (served at `/legal`) |
| `404.html` | Not-found page |
| `styles.css` | All styles; the pages link it as `/styles.css?v=N`, so bump `N` in every page when it changes (browsers keep it for 4 hours) |
| `favicon.svg` | Site icon |
| `_headers` | Security headers for Cloudflare Pages |
| `og-image.png` | Social card image (1200×630), rendered from `og/og-image.html`; bump `?v=` in the `og:image` and `twitter:image` tags when it changes |
| `og/og-image.html` | Template for `og-image.png` |
| `llms.txt` | Plain-text summary of Portenv for language models |
| `llms-full.txt` | The full plain-text description for language models |
| `cli.html`, `skill.html`, `mcp.html` | The short links `/cli`, `/skill` and `/mcp`: "coming with" pages until each target exists; nothing downloads or installs from them |
| `robots.txt`, `sitemap.xml` | Crawler rules and the list of pages |

## Docs pages

Docs pages will be generated from the files `portenv/portenv` generates from its command registry, from milestone 2.4 on (PLAN.md, Agent readiness). There are no docs pages yet; don't write them by hand.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Hosted on Cloudflare Pages, connected to this repository. Every push to `main` deploys to portenv.com; other branches get preview URLs. Build command: none. Output directory: `/`.
