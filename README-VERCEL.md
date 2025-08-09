# Deploy to Vercel

## Quick Deploy (UI)
1) Go to https://vercel.com and sign in with GitHub/Google.
2) Click **+ New Project** → **Import** → **Continue**.
3) Drag this folder in (or push it to GitHub and import the repo).
4) Click **Deploy**. You'll get a URL like `https://street-hockey.vercel.app`.

## Custom Domain (when you buy one)
1) In your project: **Settings → Domains → Add** → enter your domain (e.g., streethockeygame.com).
2) Vercel shows DNS records to add at your registrar (Namecheap/Cloudflare/etc.).
   - `www` subdomain → CNAME to `cname.vercel-dns.com`
   - Apex/root → use Vercel's A/ALIAS/NS guidance shown in the UI
3) Wait a few minutes → HTTPS auto-enables.

## Notes
- This app is a single static file (`index.html`) served via Vercel's global CDN.
- `vercel.json` pins a static build and routes all paths to `/index.html`.
- To update your site: deploy again (drag-drop or push to GitHub). Rollbacks are instant.
