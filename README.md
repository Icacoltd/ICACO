# ICACO LTD. website

Static one-page site. No build step — just push and go.

## Deploy to GitHub Pages

1. Create a new GitHub repo, push everything in this folder to the `main` branch (root).
2. Repo → Settings → Pages → Source: `main` branch, `/ (root)`.
3. Repo → Settings → Pages → Custom domain: enter `icaco.uk`, save (this reads the CNAME file already in the repo).
4. In Cloudflare DNS for icaco.uk, add:
   - A records (apex) → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME `www` → yourusername.github.io
   - Keep proxy status **DNS only (grey cloud)** until GitHub issues the SSL cert, then switch to proxied.
5. Back in GitHub Pages settings, tick "Enforce HTTPS" once the domain check passes.

## Editing content

Everything is in `index.html` — copy, colours, and layout are all in one file (styles in the `<style>` tag at the top). Swap the placeholder email, sector tags, and service copy for the real thing before launch.
