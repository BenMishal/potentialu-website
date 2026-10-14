# PotentialU Education — Official Website

Official institutional website for **PotentialU Education Ltd**, bridging universities, colleges, and students across the **United Kingdom**, **India**, and the **United Arab Emirates (UAE)**.

- **Primary Domain:** [potentialu.co.uk](https://potentialu.co.uk)
- **Registered Office:** 220 Bushy Hill Drive, Guildford, Surrey, GU1 2UT, United Kingdom
- **Company Registration:** England & Wales (No. 17184439)
- **Founders:** Ben Mishal (Co-Founder & Director) · Aly Lalji (Co-Founder)

---

## 🚀 Structure & Pages

* `index.html` — The main institutional website:
  * **Pillar 01:** Institutional Partnerships (Universities & Colleges curriculum co-design, BCS pathway, delivery models)
  * **Pillar 02:** The Student Platform (U Home Base, BridgED live employer briefs, portfolio proof)
  * **Global Footprint:** UK, India, and UAE operational hubs
  * **Leadership & Core Principles:** Ben Mishal and Aly Lalji profiles + 6 core values
  * **Enquiry System:** Form routed directly to `benmishal@potentialu.co.uk` and synced with private storage
  * **Downloadable Materials:** Partnership Overview Deck & At A Glance PDFs
  * **Student Links:** Waiting List (`test.potentialu.education/auth`) & Pilot Demo (`test.potentialu.education/pilot`)
* `admin.html` — Private Admin Dashboard:
  * Passcode-protected enquiry review (`potentialu2026` default, customizable inside dashboard)
  * Reply tracking buttons: **✓ Contacted** and **📁 Archive**
  * One-click mail reply & CSV data export
* `CNAME` — Points to `potentialu.co.uk`
* `assets/` — Production media assets (Logo, real founder headshots, official institutional PDFs)

---

## ☁️ Cloudflare Hosting Instructions

### Option A: Cloudflare Pages (Recommended - Fastest & Free SSL)
1. In your **Cloudflare Dashboard**, navigate to **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**.
2. Select your repository: `BenMishal/potentialu-website`.
3. Set build settings:
   - **Framework preset:** `None`
   - **Build command:** *(leave blank)*
   - **Build output directory:** `/` *(root)*
4. Click **Save and Deploy**.
5. Once deployed, go to **Custom domains** in the Pages project settings:
   - Click **Set up a domain**.
   - Enter `potentialu.co.uk` (and `www.potentialu.co.uk`).
   - Cloudflare will automatically configure the DNS records and issue universal SSL.

### Option B: Cloudflare DNS + GitHub Pages
1. In the GitHub repository settings:
   - Go to **Settings** > **Pages**.
   - Under **Build and deployment**, set Source to `Deploy from a branch` > branch `main` / `root`.
   - Under **Custom domain**, enter `potentialu.co.uk` and save.
2. In your **Cloudflare DNS Management**:
   - Add a `CNAME` record:
     - **Name:** `@` (or `potentialu.co.uk`)
     - **Target:** `benmishal.github.io`
     - **Proxy status:** Proxied (Orange cloud) or DNS only
   - Add a `CNAME` record for `www`:
     - **Name:** `www`
     - **Target:** `benmishal.github.io`
