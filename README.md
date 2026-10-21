# samvidhan (GitHub Pages shell)

A full-viewport frame around the Samvidhan Live Apps Script web app, served at https://samvidhan.online.

## Setup
1. **Apps Script deployment:** Deploy → Manage deployments → Web app → *Who has access: Anyone*. Without this, the frame shows a Google sign-in page.
2. **Script properties:** set `SHARE_URL=https://samvidhan.online`. `ALLOW_EMBED` is already `true` by default. Then run `diagnose()`.
3. **GitHub:** push this folder to `rrmlogs8896/samvidhan` on `main`, then Settings → Pages → Deploy from branch `main` / root. Custom domain `samvidhan.online` (the CNAME file is included) and tick *Enforce HTTPS*.
4. **DNS at your registrar:**
   - Apex `A` records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - Optional `AAAA` → 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153
   - `www` `CNAME` → rrmlogs8896.github.io
5. **Deep links:** `https://samvidhan.online/?a=21` opens Article 21. `/21` and `/article/21A` also work through 404.html.

If the deployment URL changes, update `EXEC` in index.html and the links in index.html/404.html.
