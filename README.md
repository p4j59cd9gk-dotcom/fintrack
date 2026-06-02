# FinTrack — Offline-First Finance App

A fully offline, no-cloud personal finance PWA for Samsung S24 Ultra (and any Android device).

## Features
- ✅ Monthly budget tracking with progress bars
- ✅ Expense categories with emoji icons
- ✅ Income tracking
- ✅ Recurring payments (auto-applied monthly)
- ✅ Charts: spending by category (donut) + 6-month income vs expenses (bar)
- ✅ Multiple accounts/wallets
- ✅ No limits on transactions
- ✅ 100% offline — no internet needed after first load
- ✅ All data stays on your device (localStorage)
- ✅ No sync, no accounts, no cloud

---

## How to Install on Samsung S24 Ultra

### Option A — Install via Chrome (Recommended)
1. Copy the `fintrack-pwa` folder to a web server or use a local server tool
2. Open Chrome on your S24 Ultra and navigate to the site
3. Chrome will show **"Add to Home screen"** banner, or tap the ⋮ menu → "Add to Home screen"
4. Tap **Add** — it installs like a native app

### Option B — Local Server (easiest for testing)
On your computer:
```bash
cd fintrack-pwa
npx serve .
# or
python3 -m http.server 8080
```
Then open `http://YOUR_PC_IP:8080` on your phone.

### Option C — Convert to APK with PWABuilder
1. Go to https://www.pwabuilder.com
2. Enter your hosted URL
3. Click **Package for Android** → download the APK
4. Install the APK on your S24 Ultra (enable "Install from unknown sources" in Settings)

### Option D — GitHub Pages (free hosting)
1. Push the `fintrack-pwa` folder to a GitHub repo
2. Enable GitHub Pages in repo Settings
3. Open the Pages URL on your phone and install

---

## File Structure
```
fintrack-pwa/
├── index.html     ← The entire app (single file)
├── manifest.json  ← PWA manifest (makes it installable)
├── sw.js          ← Service worker (offline support)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Data
All data is stored in `localStorage` on your device. Use **Settings → Export Data** to save a JSON backup.
