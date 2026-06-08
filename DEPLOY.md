# Hostinger Deployment

## GitHub Connection

1. Push this repo to `main` on GitHub (already done).
2. In Hostinger hPanel → **Hosting** → your domain → **Git** tab.
3. Connect your GitHub account and select **strandwaysystems-cpu/smidstad**.
4. Set branch: `main`.
5. Set build command: `npm run build`.
6. Set output directory: `dist`.
7. Save — Hostinger will pull, build, and serve `dist/` automatically on every push to `main`.

## Manual Build (local check)

```bash
npm install
npm run build
# Output in dist/
```

## Domain

Point `smidstad.com` DNS A record to your Hostinger server IP.
SSL is provisioned automatically via Hostinger's Let's Encrypt integration.
