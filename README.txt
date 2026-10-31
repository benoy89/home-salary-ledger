HOME SALARY LEDGER — Offline Android-installable web app

Included: index.html, app.js, service worker, manifest, icons.

INSTALL ON ANDROID:
1. Host the contents of this folder on an HTTPS website (e.g. GitHub Pages).
2. Open that HTTPS URL in Chrome on Android.
3. Tap Chrome's three-dot menu > Add to Home screen > Install.
4. Launch from the Home screen. After the first online visit, it works offline.

For a quick desktop test, run a local web server in this directory:
  python -m http.server 8000
then open http://localhost:8000 (service worker requires HTTPS or localhost).

IMPORTANT: This is an installable PWA, NOT an Android APK. There is no Android
build toolchain in this environment. It works as a home-screen app on Android.

Records are stored in the browser's localStorage on that device. Export a JSON
backup in Settings frequently. Clearing Chrome site data or uninstalling the app
may erase the records. Backups can be restored through Settings.

Salary credits are generated when the app is opened, beginning at the start month.
The default start month is the current month; set an earlier start month if needed.
Existing salary entries are retained when the monthly salary changes.
Leave has no automatic salary deduction.
