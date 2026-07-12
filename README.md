# VialMath — RxPep Calculator

A Progressive Web App (PWA) — installs like a real app with its own icon on iPhone, Android, and PC,
and works offline after the first load. Everything runs locally in the browser; no server, no
database, no data ever leaves the device. Each person who opens it gets their own private data —
nothing is shared between visitors.

Files:
- `index.html` — the whole app
- `manifest.json` — app name, icon, and full-screen install behavior
- `service-worker.js` — caches the app so it works offline after first load
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon-32.png` — app icon at various sizes

## Hosting on GitHub Pages (recommended)

1. Create a free GitHub account at github.com if you don't have one
2. Click **+** (top right) → **New repository** → name it (e.g. `vialmath`) → set **Public** → **Create repository**
3. On the new repo page, click **"uploading an existing file"**
4. Drag in every file from this folder (not the folder itself — the files inside it) → **Commit changes**
5. Go to **Settings → Pages** → under "Build and deployment": **Source: Deploy from a branch**,
   **Branch: main**, folder **/ (root)** → **Save**
6. Wait ~1 minute — your live URL will appear, e.g. `https://yourusername.github.io/vialmath/`

**To update later:** click into any changed file in the repo, hit the pencil (edit) icon, paste in the
new content, and commit — or use "Add file → Upload files" to overwrite. The live site updates within
a minute or two, same URL every time. Each commit is automatically a saved version, so nothing is ever
truly lost even if an update goes wrong.

## Installing it as an app (after hosting, on any device)

- **iPhone (Safari):** Share icon → **Add to Home Screen**
- **Android (Chrome):** ⋮ menu → **Install app**
- **PC (Chrome/Edge):** install icon in the address bar, or ⋮ menu → **Install VialMath**

After installing, it opens full-screen with its own icon and keeps working with wifi off.

## Alternative: Netlify Drop

app.netlify.com/drop also works — drag this folder in for an instant URL. The one catch: an anonymous
drop is deleted within an hour unless you sign up (free) to claim it. GitHub Pages skips that step
entirely, which is why it's the default recommendation here.
