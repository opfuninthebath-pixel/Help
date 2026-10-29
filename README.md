# CBSE Class 10 Checklist 2026–27 — PWA

This package preserves the uploaded checklist and adds Progressive Web App (PWA) installation metadata, an app icon, and offline caching.

## What it does
- Installs to an Android home screen and opens in a standalone, app-like window.
- Caches the checklist shell for offline use after the first successful online load.
- Keeps checkbox progress in browser local storage on that device/browser profile.
- Includes an install button where the browser supports the install prompt.

## Important: hosting is required
A PWA generally needs to be served from **HTTPS** (or `localhost`) for installation and service-worker offline support. Opening `index.html` directly from a file manager will not enable full PWA installation/offline caching.

## Easiest free setup: GitHub Pages
1. Create a GitHub repository and upload all files/folders from this package (keep `index.html`, `manifest.webmanifest`, `sw.js`, and `icons/` together at the same level).
2. In the repository, open **Settings → Pages** and publish from the main branch/root folder.
3. Open the published HTTPS URL in Chrome on Android.
4. Use the browser menu → **Install app** or **Add to Home screen**. If the install button appears inside the page, you can use that too.
5. Open it once while online, then test it offline.

## About the “widget” request
This is an installable PWA with a home-screen app icon and standalone app launch. A true interactive Android home-screen widget (for example, showing live completion progress without opening the app) cannot be created by a PWA alone; that requires a native Android app/widget wrapper. The current PWA keeps the checklist and its progress tracker inside the app.

## Notes
- Offline support works after the app shell has been cached once online.
- Progress is stored locally; it does not automatically sync between devices or browsers.
- The subject/chapter list is preserved from your uploaded HTML and has not been independently verified against CBSE updates.
