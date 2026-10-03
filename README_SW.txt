ONE MAN SMART POS — ANDROID APK BUILDER

This project wraps the current Smart POS HTML in a native Android app using Capacitor.
It keeps the existing Supabase URL/key and existing cloud database calls in index.html; it does not create a new database or migrate data.

HOW TO GET THE APK WITHOUT ANDROID STUDIO
1. Sign in to https://github.com/ and create a new repository, e.g. one-man-smart-pos. Set it Private if you prefer.
2. Upload the contents of this ZIP (not the ZIP file itself) into the repository's main branch. Ensure .github/workflows/build-apk.yml is included.
3. Open the repository's Actions tab. Select “Build One Man Smart POS APK” and click “Run workflow” (or wait for the first push build).
4. When the run finishes with a green check, open that run and download the “One-Man-Smart-POS-APK” artifact. It downloads as a ZIP.
5. On the phone, extract the artifact ZIP and tap app-debug.apk. Allow “Install unknown apps” for the browser/files app if Android asks, then install.

NOTES
- This produces a debug-signed APK suitable for installing on your own Android phone. It is not a Play Store release APK.
- The app requires internet for Supabase cloud sync. It uses the same cloud backend as the existing web POS.
- Do not change Supabase credentials, database tables, or row-level security as part of this build.
- If your current site has any changes newer than the HTML bundled here, replace index.html with the latest source before building.
