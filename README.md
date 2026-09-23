# Personal site and blog — Astro on Cloudflare Workers

A small Astro blog: markdown/MDX posts, RSS feed, sitemap, and static assets served from a Cloudflare Worker. Good starting point for a personal site, portfolio or writing archive.

## Features

- **Astro** with MDX support (`src/content/blog/*.md`, `src/content.config.ts`)
- **RSS feed** at `/rss.xml` and an auto-generated **sitemap**
- **Cloudflare Workers** deployment through the `@astrojs/cloudflare` adapter + `wrangler.json`
- Typed content collections, small component set (`Header`, `Footer`, `BaseHead`, `FormattedDate`)

## Getting started

```sh
npm install
npm run dev        # http://localhost:4321
```

Build and deploy:

```sh
npm run build      # astro build
npm run preview    # build + local worker preview (wrangler dev)
npm run deploy     # wrangler deploy
npm run check      # type check + deploy dry run
```

## Where things live

| Path | Purpose |
|---|---|
| `src/content/blog/` | posts (markdown / MDX) |
| `src/components/` | layout components |
| `src/pages/` | routes, including `rss.xml.js` |
| `astro.config.mjs` | integrations: mdx, sitemap, cloudflare |
| `wrangler.json` | worker name, assets binding, compatibility flags |

## Notes

The repository name is left over from an earlier experiment; the code in here is the Astro blog template, not a proxy service.

---

Built by **Cody Wang**, front-end engineer. I build and optimise Prismic, Next.js and SvelteKit sites. Website: [prismicaudit.com](https://prismicaudit.com)
