# Bewind BIMI Logo

This repository hosts the BIMI-compatible SVG logo for **bewindagency.com**.

## File
- `bewind_bimi_logo_margin.svg` — dark background with flat gold "BEWIND" text and extra margins for circular inbox display.

The file is **SVG Tiny 1.2**, flat (no gradients or filters), square (1:1), and under 50KB.

## GitHub Pages
To publish and host your logo publicly:

1. Go to **Settings → Pages**
2. In **Build and deployment**, select:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
3. Click **Save**.

GitHub Pages will generate a public URL such as:
https://<your-username>.github.io/bimi-logo/bewind_bimi_logo_margin.svg

Ensure that when you open the link, the SVG displays directly in your browser.

## DNS BIMI Record (Porkbun)
Add a new TXT record:

| Field | Value |
|-------|-------|
| **Host** | `default._bimi` |
| **Type** | `TXT` |
| **Value** | `v=BIMI1; l=https://<your-username>.github.io/bimi-logo/bewind_bimi_logo_margin.svg; a=;` |
| **TTL** | `300` |

Replace `<your-username>` with your GitHub username.

## Requirements
Ensure that:
- SPF ✅ is correctly set (`include:zohomail.com`)
- DKIM ✅ is verified
- DMARC ✅ exists (e.g. `v=DMARC1; p=none; rua=mailto:dmarc@bewindagency.com;`)

Once your domain reputation improves (after warm-up), Gmail and Yahoo may display your logo automatically.  
For guaranteed display, a **VMC (Verified Mark Certificate)** is required (optional, paid).
