# Smidstad

Marketing one-pager for **Smidstad** — AI-powered websites, portfolios, landing
pages, and ghostwritten content. [smidstad.com](https://smidstad.com)

## What this is

A single static page. Everything (markup, styling, and the small scroll/reveal
script) lives inline in `index.html`. No build step, no dependencies, no
framework — it deploys to any static host by copying the files.

```
index.html        Full site
favicon.svg       Logo / favicon
site.webmanifest  PWA manifest
robots.txt        Crawler rules
sitemap.xml       Sitemap
assets/           Web logo (transparent PNG) + OG social image
brand/            Source brand renders (wordmark + slate SS monogram)
DEPLOY.md         Hostinger deploy guide
```

## Brand

Forge identity: charcoal `#161614` + lime `#ccf24d`. The nav/footer logo is the
lime/grey **SMIDSTAD DIGITAL** wordmark (`assets/logo.png`, transparent). The
slate 3D **SS** monogram render is the social share image (`assets/og-image.jpg`).

## Deploy

Served from the repo root on Hostinger via GitHub. See [DEPLOY.md](./DEPLOY.md).

## Edit

Open `index.html` and edit directly. The contact form posts to
[FormSubmit](https://formsubmit.co/) at `hello@smidstad.com`.
