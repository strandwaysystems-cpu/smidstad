# Smidstad

Marketing site for **Smidstad** — AI-powered websites, portfolios, landing pages, and ghostwritten content for coaches and creators. [smidstad.com](https://smidstad.com)

## Structure

```
index.html          Full site (markup only — CSS/JS extracted to src/)
src/
  styles.css        All site styles
  main.js           Nav scroll + reveal animation
public/
  assets/           Logo, OG image, emblem
  mockups/          Spec mockup preview pages (served at /mockups/)
  favicon.svg
  robots.txt
  sitemap.xml
  site.webmanifest
package.json
vite.config.js
```

## Hostinger Deployment Settings

| Setting | Value |
|---|---|
| Framework | **Vite** |
| Branch | `main` |
| Install command | `npm install` |
| Build command | `npm run build` |
| Output / publish directory | `dist` |
| Root directory | *(repository root)* |

## Mockup Pages

Live at `smidstad.com/mockups/`:
- `/mockups/` — gallery index
- `/mockups/jordan-vance-fitness.html` — personal trainer (navy/blue)
- `/mockups/maya-solano-coaching.html` — life & career coach (terracotta/cream)
- `/mockups/tara-bloom-creator.html` — fitness creator (forest/sage)

## Local Dev

```bash
npm install
npm run dev       # dev server at localhost:5173
npm run build     # production build → dist/
npm run preview   # preview built site
```

## Contact Form

Posts to [FormSubmit](https://formsubmit.co/) at `hello@smidstad.com`. Activate by submitting once and clicking the confirmation email.
