# RXpep Calculator — installable app package

This folder (`vialmath-app.zip`) is now a **Progressive Web App (PWA)** — a set of files that installs
like a real app with its own icon on iPhone, Android, and PC, and works offline after the first load.
Everything runs locally in the browser engine; no server, no build tools, no data leaves the device.

Files:
- `index.html` — the app
- `manifest.json` — tells the OS the app's name, icon, and that it should open full-screen (no browser bar)
- `service-worker.js` — caches the app so it works with no internet connection after first load
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon-32.png` — the app icon at various sizes

## Why you still need to host it once

iOS, Android, and desktop browsers only offer "Install app" / "Add to Home Screen" as a real installable
app for pages loaded over `https://` (a plain double-clicked local file can't trigger this — that's a
browser/OS security rule, not something in the code). The good news: after that one install step, the app
runs from the device itself, offline, with its own icon — you won't need the site again unless you want an update.

## Steps

**1. Host the folder (~2 minutes)**
1. Unzip `vialmath-app.zip`
2. Go to https://app.netlify.com/drop
3. Drag the whole unzipped folder onto the page
4. You get a live URL like `https://your-site-name.netlify.app`

**2. Install it as an app**

*iPhone (Safari):*
Open the URL in Safari → tap the Share icon → **Add to Home Screen**. It appears as an app icon and opens full-screen, no browser bar.

*Android (Chrome):*
Open the URL in Chrome → tap the **⋮** menu → **Install app** (or **Add to Home screen**). Same result — a real launcher icon.

*PC (Chrome or Edge):*
Open the URL → look for the **install icon** (a small monitor with a down arrow) in the address bar, or **⋮** menu → **Install RXpep Calculator**. It installs as its own desktop app with a taskbar/dock icon, separate from your regular browser window.

After installing on any device, you can turn off wifi and it still opens and works — your vial data is stored on that device only.

## Updating later

If you edit `index.html` and re-drag the folder to Netlify, open the app once while online — the service
worker checks for changes and updates the cached copy in the background.

## Later: Apple/Google app stores

This install-as-app approach gets you a real icon and offline use today without any store review or
fees. If you still want it listed in the App Store / Google Play later, the same hosted URL is exactly
what PWABuilder (Android) or Median (both) need to build a store-submittable package — nothing here
needs to change first.

