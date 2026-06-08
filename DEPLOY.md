# Deploying Smidstad to Hostinger

This is a **plain static site** — a single `index.html` plus a few assets, all
served straight from the repo root. There is **no build step**, no Node, no
Astro. Hostinger serves the files exactly as they sit in the repo.

## Files served

```
index.html        ← the whole site (HTML + inline CSS + inline JS)
favicon.svg       ← logo / favicon
site.webmanifest  ← PWA manifest
robots.txt        ← crawler rules
sitemap.xml       ← sitemap
```

## Connect GitHub → Hostinger (one-time)

1. In Hostinger **hPanel** → **Websites** → select `smidstad.com` → **Advanced** → **GIT**.
2. **Create a new repository** connection:
   - **Repository:** `git@github.com:strandwaysystems-cpu/smidstad.git`
     (or the HTTPS URL `https://github.com/strandwaysystems-cpu/smidstad.git`)
   - **Branch:** `main`
   - **Directory:** leave as the web root (`public_html`) — i.e. **blank / `/`**.
3. Click **Create**. Hostinger pulls the repo into `public_html`.
4. **Do NOT set a build command or output directory.** This is static — there is nothing to build. `index.html` is at the root, so it loads as the homepage automatically.

## Updating the site later

Every time you push to `main`:

- If you enabled **Auto Deployment** (webhook) in the GIT panel, Hostinger pulls automatically.
- Otherwise, open the GIT panel and click **Deploy / Pull** to fetch the latest commit.

## Domain & SSL

- Point `smidstad.com` DNS to your Hostinger account (A record to the server IP,
  or use Hostinger nameservers). If DNS is on Cloudflare, set the A record there.
- SSL is auto-provisioned via Hostinger's free Let's Encrypt once DNS resolves.

## Local preview

No tooling needed — just open `index.html` in a browser, or:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```
