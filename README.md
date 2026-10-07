# portenv.com

The website for [Portenv](https://github.com/portenv/portenv).

Plain static HTML and CSS: no framework, no build step, no third-party requests.

| File | What it is |
| --- | --- |
| `index.html` | Home page |
| `privacy.html` | Privacy notice for the website (served at `/privacy`) |
| `404.html` | Not-found page |
| `styles.css` | All styles |
| `favicon.svg` | Site icon |
| `_headers` | Security headers for Cloudflare Pages |

## Preview locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Hosted on Cloudflare Pages, connected to this repository. Every push to `main` deploys to portenv.com; other branches get preview URLs. Build command: none. Output directory: `/`.
