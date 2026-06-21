# Sahm Halal — Halal & Global Markets

A dark **green & gold**, finance-themed web app showing **live Islamic & global stocks** with
**3D** tilting cards, animated up/down trend charts, and **buy / sell / hold** signals.
Fully responsive, 4K-crisp (vector charts), and installable on iOS as a home-screen app
(PWA, works offline).

> ⚠️ Demo app with **simulated** live data. Signals are illustrative momentum indicators,
> **not financial advice.**

---

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire app (HTML + CSS + JS, self-contained) |
| `manifest.webmanifest` | Makes it installable as an app |
| `sw.js` | Service worker → works offline once loaded |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon.svg`, `favicon-32.png` | App icons (the gold seed-of-life emblem) |
| `404.html` | Friendly "page not found" |
| `robots.txt`, `sitemap.xml` | SEO |

---

## Run it locally
Just **double-click `index.html`** — it opens in your browser. (Offline mode + "install"
only activate when served over http/https, i.e. once it's on GitHub Pages.)

> Tip: the 3D card-tilt effect needs a mouse, so it shows on desktop; on phones the cards
> keep their depth and glow but don't tilt with touch.

---

## Option A — Publish as its own website (new GitHub Pages repo)

No terminal needed — all through the GitHub website.

1. Go to **https://github.com/new**
2. Repository name: **`sahm-halal`** → set to **Public** → click **Create repository**
3. On the new repo page, click **“uploading an existing file”**
4. Drag in **every file in this folder** (index.html, sw.js, all the icons, etc.) → **Commit changes**
5. Go to **Settings → Pages** → under *Branch* pick **`main`** + **`/ (root)`** → **Save**
6. Wait ~1 minute. Your site is live at:
   **https://ma67-ex.github.io/sahm-halal/**

To open on your iPhone: visit that URL in **Safari → Share → Add to Home Screen.**

---

## Option B — Add it to your portfolio site (ma67-ex.github.io)

This puts the app at **https://ma67-ex.github.io/stocks/** and links it from your portfolio.
The files are already prepared for you in the `portfolio/stocks/` folder, and your portfolio's
Work section already has a **Sahm Halal** card linking to it.

1. Go to your **`ma67-ex.github.io`** repo on GitHub
2. Upload the re-saved **`index.html`** (it now has the Sahm Halal card)
3. Click **Add file → Upload files**, then drag in the whole **`stocks/`** folder
4. **Commit changes**

Live in ~1 minute at **https://ma67-ex.github.io/stocks/**

---

## Customizing
- **Add/remove stocks:** edit the `STOCKS = [...]` list near the top of the `<script>` in `index.html`.
- **Colors/theme:** edit the CSS variables in `:root` at the top of the `<style>` block
  (`--gold`, `--bg`, `--up`, `--down`, …).
- **Update speed:** change `setInterval(tick, 1500)` (milliseconds) at the bottom of the script.
- **3D strength:** in `attachTilt()`, change the `rot` value (higher = more tilt).

## Next step (optional): real live prices
Swap the simulated feed for a free API (Finnhub or Twelve Data — free tier needs an API key).
Ask and it can be wired in.
