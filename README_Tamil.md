# Skywall Combined Business Hub (v2.0)

இந்த project-ல் இரண்டு ZIP-களின் அம்சங்கள் ஒன்றிணைக்கப்பட்டுள்ளன:

- Skywall AI Business Hub: customer, project, labour, expenses, quotations, existing A-Book / B-Book Cash Book dashboard, backup and reports.
- Skywall Cash Book Pro: detailed cash book, multiple books, search/filter, reports, Tally XML export, backup/restore.
- Android: WebView-based APK project.
- Desktop: PWA; HTTPS hosting செய்த பின் Chrome / Edge-ல் Install App மூலம் நிறுவலாம்.

## Android APK build
1. Android Studio-வில் `android` folder-ஐ Open செய்யவும்.
2. Gradle sync முடிந்ததும் Build > Build Bundle(s) / APK(s) > Build APK(s).
3. APK: `android/app/build/outputs/apk/debug/app-debug.apk`

GitHub Actions வழியாகவும் `.github/workflows/build-apk.yml` workflow-ஐ இயக்கி APK artifact பெறலாம்.

## Web / Desktop PWA
`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `cashbook-pro.html` ஆகியவற்றை ஒரே hosting root-ல் வைத்து HTTPS மூலம் publish செய்யவும்.

## Cash Book data note
Hub A-Book / B-Book data `skywall_hub_v1` storage-ல் உள்ளது. Cash Book Pro-க்கு செல்ல Settings > Import > “இந்த browser-இல் இருந்து” என்பதை அழுத்தி Hub-இன் Cash Book பதிவுகளை இறக்குமதி செய்யலாம். இரு தொகுதிகளும் தனித்தனி storage keys பயன்படுத்துவதால் இது ஒருமுறைத் தொடங்கும் இறக்குமதி; தொடர்ச்சியான live-sync அல்ல.

## Important
- Original Hub assets and logo artwork are reused without redrawing.
- Before using real financial records, make a backup.
- This ZIP contains the Android source project; it is not a prebuilt APK. Build the APK with Android Studio or GitHub Actions.
