# Front Door — website

The complete Front Door website: one self-contained page plus a content file,
ready to publish for free on GitHub Pages at **frontdoorcollective.co.za**.

## What's in here
- **index.html** — the entire website (all HTML, CSS and JavaScript in one file, images embedded).
- **content.json** — the published text, images and settings visitors see. You update this to change the live site.
- **CNAME** — points GitHub Pages at frontdoorcollective.co.za. Leave as is.
- **.nojekyll** — serves the files as-is. Leave as is.
- **README.md** — this guide.

## 1 · Put it live on GitHub Pages
1. Create a free account at github.com (if needed).
2. Create a new **public** repository, e.g. `frontdoor-website`.
3. Upload every file in this folder to the repo root: `index.html`, `content.json`, `CNAME`, `.nojekyll`, `README.md`.
   (On github.com: **Add file → Upload files**, drag them in, **Commit changes**.)
4. Go to **Settings → Pages**. Under *Build and deployment* set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**. Save.
5. Wait ~1 minute. The site is live at `https://<your-username>.github.io/frontdoor-website/`.

## 2 · Connect your domain (frontdoorcollective.co.za)
1. *(Recommended)* In **Settings → Pages → Verify your custom domain**, follow the steps to prove you own it.
2. In **Settings → Pages → Custom domain**, enter `frontdoorcollective.co.za` and Save. (The included CNAME file already sets this.)
3. In your domain registrar's DNS panel (where you bought the domain) add:
   - **A** records, name `@`, one for each GitHub Pages IP:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - **CNAME** record, name `www`, value `<your-username>.github.io`
   - *(optional IPv6)* **AAAA** records, name `@`: 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153
4. DNS can take minutes to 24 hours. When it resolves, return to **Settings → Pages** and tick **Enforce HTTPS**.

GitHub's step-by-step (with screenshots): https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## 3 · Editing the site yourself (no code)
On the live site:
1. Click **Edit site** (bottom of the page).
2. Click any text to rewrite it; click any photo to swap in one from your device.
3. Use the **Design** panel for colours, fonts and Shopify settings.
4. Click **Export & publish** — this downloads a fresh `content.json`.
5. Upload that `content.json` to the repo, replacing the old one (Add file → Upload files → Commit). The live site updates within a minute.

Edits are saved in your own browser as you work; publishing (steps 4–5) is what makes them public.

## 4 · Taking real payments (Shopify)
The basket works already; checkout runs a demo order. To take live card payments:
1. Create matching products in Shopify (with a South African gateway such as Payfast or Yoco).
2. On the site: **Design → Shopify checkout** → enter your store domain and each product's variant ID.
3. **Export & publish** and upload the new `content.json`.
Checkout then hands the basket to Shopify's secure cart.

---
Need changes or new features? Bring `index.html` back to Claude and describe what you want.
