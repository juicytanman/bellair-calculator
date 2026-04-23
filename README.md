# Bellair Calculator — Deployment Guide

Five files make up the app:

- `index.html` — the calculator itself (both tabs)
- `manifest.json` — tells iPhone how to treat it as an installable app
- `sw.js` — service worker so it works offline once loaded
- `icon-192.png` — home-screen icon
- `icon-512.png` — larger icon used by some devices / splash screens

---

## Step 1 — Create the GitHub repo

1. Go to **[github.com](https://github.com)** and sign in with your Bellair Google account.
2. Top-right click the **+** → **New repository**.
3. Name: `bellair-calculator`
4. Set to **Public** (required for the free Vercel plan).
5. Tick **Add a README** — not necessary, we'll overwrite it.
6. Click **Create repository**.

---

## Step 2 — Upload the files

1. On the new repo page, click **Add file → Upload files**.
2. Drag in all five files from this folder:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. Scroll down, click **Commit changes**.

---

## Step 3 — Deploy to Vercel

1. Go to **[vercel.com](https://vercel.com)** and click **Sign Up** → **Continue with GitHub**.
2. Authorise Vercel to see your repos.
3. On the Vercel dashboard click **Add New… → Project**.
4. Find `bellair-calculator` and click **Import**.
5. Leave every setting on default — Vercel detects it as a static site automatically.
6. Click **Deploy**. Takes about 60 seconds.
7. You'll get a URL like `https://bellair-calculator.vercel.app`.

---

## Step 4 — Install on your iPhone

1. Open the Vercel URL in **Safari** (not Chrome — Safari is the only browser that can install PWAs on iOS).
2. Tap the **Share** button (square with up-arrow).
3. Scroll down, tap **Add to Home Screen**.
4. Name stays as "Bellair" — tap **Add**.
5. The icon now sits on your home screen and opens full-screen like any other app.
6. Works offline after the first load.

Send the same Vercel URL to your team — they follow the same four taps.

---

## Updating later

Any time you want to change the calculator:

1. Go to your GitHub repo → click `index.html` → pencil icon to edit.
2. Paste in the new version → **Commit changes**.
3. Vercel auto-redeploys within about a minute.
4. Team members just need to close and reopen the app once to pull the update.
