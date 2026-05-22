# web

The source for [daena-protocol.org](https://daena-protocol.org).

Right now it's a single static page: the Daena manifesto with a hero, the full essay, and links to the other repos. No build step, no framework — just one `index.html` you can host anywhere.

## Contents

- **[`index.html`](./index.html)** — the public site. Plain HTML + inline CSS, ~10KB total, no JS. Light/dark mode follows the system preference.
- **[`manifesto.md`](./manifesto.md)** — the manifesto in markdown, for plain-text reading and easy quoting.

## Viewing locally

```bash
git clone https://github.com/daena-protocol/web.git
cd web
# either:
open index.html
# or, for any HTTP origin behaviour (CORS, etc):
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploying

Drop `index.html` on any static host:

- **Cloudflare Pages / Vercel / Netlify** — connect this repo, point at `main`, ship.
- **GitHub Pages** — enable Pages in repo settings, set source to `main`.
- **A CDN bucket** — `aws s3 cp index.html s3://daena-protocol.org/index.html`.

Once the domain is registered, the live site is just `index.html` at the root.

## What this is and isn't

This is the *recruiting* page. It exists so a developer, publisher, or curious reader who hears about Daena has a clean place to land, understand the pitch, and click through to the code.

It is **not** the documentation site. Once we have enough to document, real docs will live at `daena-protocol.org/docs` — likely an Astro or VitePress build, sourcing content from this repo's expanded structure plus the spec repo.

## License

Site content is licensed under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/). Source code (such as it is — there isn't much) is under [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0).
