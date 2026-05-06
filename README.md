# 🏃 BEASTBORNE — Fitness App

A mobile-first HTML fitness tracker with two modes + GPS run tracking. No framework, no backend — pure HTML/CSS/JS, runs offline.

## 📁 File Structure

```
/
├── index.html      ← Mode selector (start here)
├── draglak.html    ← "กูจะลากมึงเอง" — Trainer / Friend Mode
├── beastborne.html ← BEASTBORNE — RPG Quest Mode  
└── run.html        ← GPS Run Tracker with live map & summary
```

## 🚀 Quick Start (GitHub Pages)

1. Fork this repo
2. Go to **Settings → Pages → Source: main branch / root**
3. Your app will be live at `https://YOUR_USERNAME.github.io/beastborne/`
4. Open on your phone and **Add to Home Screen** for full PWA experience

## 📱 Add to Home Screen (PWA)

### iOS (Safari)
1. Open the URL in Safari
2. Tap the **Share** button `⎋`
3. Scroll down → tap **"Add to Home Screen"**
4. The app opens fullscreen like a native app

### Android (Chrome)
1. Open the URL in Chrome
2. Tap the **⋮ menu** → **"Add to Home screen"**
3. Or Chrome will show an install banner automatically

## ⌚ Smartwatch Support

This app targets **mobile-first** but has responsive CSS for small screens:

- **Wear OS (Samsung Galaxy Watch etc.)**: Open browser in watch, navigate to the URL. The `run.html` page is most useful — shows live distance, pace, time in large text readable on a small screen.
- **Apple Watch**: Use the companion iPhone Safari, not directly on watch.
- **Garmin / Polar**: Use phone companion to share stats after run.

> **Best approach for watch integration**: After running, use the "Share" button in the run summary — it copies your run stats text that you can paste into Garmin Connect or Strava manually.

## ✨ Features

### 🏰 BEASTBORNE (RPG Mode)
- Character progression (LV 1–50+, 7 classes)
- Quest system with XP rewards
- Boss battle metaphor for weight loss goals
- Marathon training plan (10K / 21K / 42K)
- Workout generator (10+ equipment types)
- Water tracker, streak calendar

### 💀 กูจะลากมึงเอง (Trainer Mode)
- Roast-style feedback after each log
- Same features as BEASTBORNE, different tone
- Aggressive coach persona

### 🏃 Run Tracker (GPS)
- **Live GPS tracking** with Leaflet.js map
- Real-time: distance, pace, elapsed time
- Route polyline on dark map
- **Lap tracking** with per-lap pace analysis
- **Elevation profile chart**
- **Run Summary page** with full stats + map
- Run history with all previous sessions
- Native **Web Share API** for sharing results
- Fallback demo mode if GPS not permitted

## 🛠 Tech Stack

| Layer | Tech |
|-------|------|
| UI | Vanilla HTML/CSS/JS |
| Maps | Leaflet.js + OpenStreetMap |
| GPS | Web Geolocation API |
| Storage | localStorage |
| Fonts | Google Fonts (Bebas Neue, Cinzel, Sarabun) |
| PWA | Web App Manifest + Service Worker |

## 📊 GPS Accuracy Notes

- Requires **HTTPS** for Geolocation API (GitHub Pages provides this)
- On HTTP (localhost), it may work on Chrome but not Safari
- App shows GPS accuracy in meters during tracking
- Filters out GPS noise < 2m to prevent phantom distance

## 🔗 Linking to Other Apps

The run summary share button outputs:
```
🏃 วิ่ง 5.23 KM | Pace 6:12 min/km | 32:28
#RunTracker #BeastBorne #วิ่ง
```

You can paste this into:
- **Strava** manual entry
- **Garmin Connect** manual activity  
- **Line / Instagram** for sharing

## 📁 Data & Privacy

- All data stored in **browser localStorage** — never leaves your device
- Use the **Backup** button (Settings tab) to export a base64 string
- Save the backup string in Notes to restore later

## 🤝 Contributing

PRs welcome! Especially for:
- Actual heart rate via Web Bluetooth API
- Garmin/Polar Bluetooth integration
- Strava OAuth auto-sync
- Better GPS smoothing algorithm
- Thai language improvements
