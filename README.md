# LIVE – ReadMe File – Mtgbyriaz.io

## Context

This README powers the **mtgbyriaz.io** GitHub Pages site. It documents structure, setup, and compliant defaults for Team Riaz (Pilgrim Mortgage).

## Next 3 Actions

1. Push the starter files to the repo root and verify Pages is serving the pre‑landing selector.
2. Swap in real links: application URL, Monday.com referral embeds, SharePoint Team Hub button.
3. Drop brand assets (logos, favicon) and add GA4.

---

# mtgbyriaz.io — Team Riaz Website

A fast, static GitHub Pages site with a pre‑landing selector, client & partner hubs, a referral hub, partner marketing requests, reviews, and compliant global CTAs.

## Live URLs

* Root (pre‑landing): [https://mtgbyriaz.io/](https://mtgbyriaz.io/)
* Home: [https://mtgbyriaz.io/home/](https://mtgbyriaz.io/home/)
* Clients hub: [https://mtgbyriaz.io/clients/](https://mtgbyriaz.io/clients/)
* Partners hub: [https://mtgbyriaz.io/partners/](https://mtgbyriaz.io/partners/)
* Referral hub: [https://mtgbyriaz.io/referral/](https://mtgbyriaz.io/referral/)
* Apply: [https://mtgbyriaz.io/apply.html](https://mtgbyriaz.io/apply.html)
* Reviews: [https://mtgbyriaz.io/reviews.html](https://mtgbyriaz.io/reviews.html)
* Legal: [https://mtgbyriaz.io/legal/](https://mtgbyriaz.io/legal/)
* Sitemap: [https://mtgbyriaz.io/sitemap.xml](https://mtgbyriaz.io/sitemap.xml)

## Project Structure

```plaintext
/
├─ index.html                  # Pre-landing selector (“Where would you like to start?”)
├─ about.html
├─ apply.html
├─ contact.html
├─ reviews.html
├─ 404.html
├─ robots.txt
├─ sitemap.xml
├─ home/
│  └─ index.html              # Primary homepage/welcome
├─ referral/
│  └─ index.html              # “I am a Client / Realtor-Partner” split
├─ clients/
│  ├─ index.html              # Client Hub
│  ├─ referral.html           # Embed Monday client referral form
│  ├─ journey.html
│  ├─ first-time-buyers.html
│  ├─ tools.html
│  └─ resources.html
├─ partners/
│  ├─ index.html              # Partner Hub
│  ├─ referral.html           # Embed Monday partner referral form
│  ├─ tools.html
│  ├─ resources.html
│  └─ marketing/
│     └─ index.html           # CE Request, Co-Branded, Partner App, Events/Open House
├─ legal/
│  ├─ index.html
│  ├─ disclosures.html
│  ├─ privacy.html
│  └─ terms.html
├─ thank-you/
│  ├─ apply.html
│  ├─ referral.html
│  └─ contact.html
└─ assets/
   ├─ css/styles.css
   ├─ js/main.js
   └─ img/                    # logos, headshot, favicon, etc.
```

> Multiple `index.html` files are intentional: visiting `/clients/` loads `/clients/index.html`, etc.

## What to Customize First

1. **Application link**

   * File: `/apply.html`
   * Replace the placeholder button with your official Pilgrim application URL.

2. **Referral forms (Monday.com)**

   * Files: `/clients/referral.html`, `/partners/referral.html`
   * Swap the `iframe` `src` with the Monday embed URL. Optionally redirect success to `/thank-you/referral.html`.

3. **Partner Marketing requests**

   * File: `/partners/marketing/index.html`
   * Point each card button to a form embed or external link (CE Request, Co‑Branded Marketing, Partner App, Events/Open House).

4. **Analytics (GA4)**

   * Add your GA4 snippet in `/home/index.html` (`<head>`) or load via `assets/js/main.js`.

5. **Brand images & favicon**

   * Place assets in `assets/img/`.
   * Add `<link rel="icon" href="/assets/img/favicon.ico">` (or `.png`) in your templates’ `<head>`.

6. **Team Hub (internal)**

   * If hosted on SharePoint, add a button anywhere you like:

     ```html
     <a href="https://your-sharepoint-private-url" class="btn btn-gold">Team Hub</a>
     ```
   * Style example in `assets/css/styles.css`:

     ```css
     .btn{display:inline-block;padding:12px 18px;border-radius:12px;text-decoration:none;font-weight:600}
     .btn-gold{background:#C9A646;color:#0D1B2A}
     .btn-gold:hover{filter:brightness(1.05)}
     ```

## Compliance Guardrails

* Footer appears on every page and includes:

  * “Pilgrim Mortgage | NMLS #225091 | Equal Housing Lender”
  * “Riaz Pooran | NMLS #1212168”
  * “This is not a commitment to lend. All loans subject to credit approval.”
* External Pilgrim profile link opens in a new tab.
* Primary CTA “Get Pre‑Approved” is highlighted in gold.

## GitHub Pages Setup

1. **Settings → Pages**
2. **Source:** `main` branch, Folder: `/ (root)`
3. **Custom domain:** `mtgbyriaz.io`
4. Enable **Enforce HTTPS** once the certificate is issued.
5. Test: [https://mtgbyriaz.io/](https://mtgbyriaz.io/) should show the pre‑landing selector.

## Uploading From iPad (Codespaces)

* Repo → **Code** → **Codespaces** → **Create codespace on main**.
* Drag files into the Codespaces file explorer to upload.
* Use the **Source Control** panel to Commit → Push.

If you accidentally uploaded into a nested folder, move contents to repo root:

```bash
mv mtgbyriaz_full_starter/* ./ 2>/dev/null || true
mv mtgbyriaz_full_starter/.* ./ 2>/dev/null || true
rm -rf mtgbyriaz_full_starter
```

---

### What changed / Next edit

* Cleaned markdown (fixed headings/links, removed duplicates, added code fences).
* Added **Team Hub** button pattern for SharePoint.
* Next: insert real URLs (app, Monday embeds, SharePoint), drop assets, and push to `main`.
