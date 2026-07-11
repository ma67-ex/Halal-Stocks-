# Sahm Halal: Halal and Global Markets

![PWA](https://img.shields.io/badge/PWA-installable-5A0FC8)
![Offline](https://img.shields.io/badge/offline-ready-2ea44f)
![Stack](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-f7df1e)

A dark **green and gold**, finance-themed web app showing **live Islamic and global stocks** with **3D** tilting cards, animated up and down trend charts, and **buy, sell, hold** signals. Fully responsive, 4K-crisp (vector charts), and installable on iOS as a home-screen app (PWA, works offline).

> ⚠️ Demo app with **simulated** live data. Signals are illustrative momentum indicators, **not financial advice.**

## What problem this solves

Halal-conscious investors don't have many places that show Islamic-compliant and global stocks side by side with a quick visual read on momentum. Sahm Halal demos that experience: one screen, clear buy/sell/hold signals, no backend to pay for, and it still works with the phone offline once it's loaded.

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire app (HTML + CSS + JS, self-contained) |
| `manifest.webmanifest` | Makes it installable as an app |
| `sw.js` | Service worker, works offline once loaded |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon.svg`, `favicon-32.png` | App icons (the gold seed-of-life emblem) |
| `404.html` | Friendly "page not found" |
| `robots.txt`, `sitemap.xml` | SEO |

## Deploy on your device

### Run it locally

Double-click `index.html`. It opens straight in your browser, no install step. Offline mode and "add to home screen" only turn on once the file is served over http/https, which happens automatically after you publish it (see below).

> The 3D card-tilt effect needs a mouse, so it shows on desktop. On phones the cards keep their depth and glow but don't tilt with touch.

### Option A: publish as its own website (new GitHub Pages repo)

No terminal needed, all through the GitHub website.

1. Go to **https://github.com/new**
2. Repository name: **`sahm-halal`**, set to **Public**, click **Create repository**
3. On the new repo page, click **"uploading an existing file"**
4. Drag in every file in this folder (index.html, sw.js, all the icons, etc.), then **Commit changes**
5. Go to **Settings → Pages**, under *Branch* pick **`main`** and **`/ (root)`**, then **Save**
6. Wait about a minute. The site goes live at **https://ma67-ex.github.io/sahm-halal/**

To open it on an iPhone: visit that URL in **Safari → Share → Add to Home Screen.**

### Option B: add it to your portfolio site (ma67-ex.github.io)

This puts the app at **https://ma67-ex.github.io/stocks/** and links it from the portfolio. The files are already prepared in the `portfolio/stocks/` folder, and the portfolio's Work section already has a **Sahm Halal** card linking to it.

1. Go to the **`ma67-ex.github.io`** repo on GitHub
2. Upload the re-saved **`index.html`** (it now has the Sahm Halal card)
3. Click **Add file → Upload files**, then drag in the whole **`stocks/`** folder
4. **Commit changes**

Live in about a minute at **https://ma67-ex.github.io/stocks/**

## Customizing

- **Add or remove stocks:** edit the `STOCKS = [...]` list near the top of the `<script>` in `index.html`.
- **Colors and theme:** edit the CSS variables in `:root` at the top of the `<style>` block (`--gold`, `--bg`, `--up`, `--down`, and so on).
- **Update speed:** change `setInterval(tick, 1500)` (milliseconds) at the bottom of the script.
- **3D strength:** in `attachTilt()`, change the `rot` value (higher means more tilt).

## Next step (optional): real live prices

Swap the simulated feed for a free API such as Finnhub or Twelve Data (free tier, needs an API key). Ask and it can be wired in.
