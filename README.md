# STARFOLD — Android APK (GitHub Actions build)

A native Android WebView wrapper around the STARFOLD game. Push this repo to
GitHub and the included workflow builds a debug APK for you — no Android Studio
needed.

## Build it

1. Create a new GitHub repo (e.g. `starfold-android`).
2. Upload **all** of these files, keeping the exact folder paths.
3. Commit/push to the `main` branch.
4. Open the **Actions** tab → wait for **Build STARFOLD APK** to finish (~3–5 min).
5. Open the finished run → download the **starfold-debug-apk** artifact → unzip → `app-debug.apk`.
6. Transfer to your phone and install (enable "Install unknown apps" for your file manager/browser).

This produces a **debug-signed** APK — perfect for sideloading and testing. For a
Play Store release you'd add a release signing config.

## Structure

```
starfold-android/
├─ .github/workflows/build.yml
├─ app/
│  ├─ build.gradle
│  └─ src/main/
│     ├─ AndroidManifest.xml
│     ├─ assets/index.html
│     ├─ java/com/markfold/starfold/MainActivity.java
│     └─ res/
│        ├─ drawable/ic_launcher.xml
│        └─ values/themes.xml
├─ build.gradle
├─ settings.gradle
└─ gradle.properties
```
