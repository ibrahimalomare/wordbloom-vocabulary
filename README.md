# WordBloom — Vocabulary PWA

A mobile-first English–Arabic vocabulary app. Includes flashcards, flip/reveal, previous/next, direction switching, shuffle, Known / Need Practice ratings, spaced review intervals, daily due review, decks, word search, add/edit/delete, CSV/JSON import, JSON backup export, stats, streaks, theme toggle, and local-device storage.

## Run locally for a quick preview
Open `index.html` in a browser. Core features work, but service workers and PWA installation generally require HTTPS or localhost.

## Install on Android (recommended)
A PWA must be served from an HTTPS website to install and cache offline. This ZIP is the complete site source.

1. Extract the ZIP.
2. Upload the **contents** of this folder to an HTTPS static host, such as GitHub Pages, Cloudflare Pages, or Netlify. No build command is needed; publish the folder containing `index.html`.
3. Open the published HTTPS URL in Chrome on your Android phone.
4. Open Chrome's ⋮ menu and choose **Install app** or **Add to Home screen**.
5. Launch WordBloom from the home screen once while online. After the first successful load, the service worker caches the app files for offline use.

## Data & backup
Vocabulary and progress are saved in the browser's local storage on that device. Clearing browser data or uninstalling may erase it; use **Export data** regularly. Import accepts JSON backups and CSV with a header row. CSV columns can include `english`, `arabic`, `definition`, `example`, and `deck` (also accepts `word`, `meaning`, `translation`, `sentence`, `category` aliases).

## Spaced repetition
Known cards are scheduled farther out over time; cards marked Need Practice return after about 10 minutes and are prioritized by their due date. This is a lightweight local algorithm, not a sync service. Streaks update when you rate cards on a new calendar day.

## Important limitations
This package is a complete installable PWA source, but it does not include an APK. An APK requires a separate Android build/signing workflow. This app stores data only in the browser profile where it is used; it does not sync between devices.
