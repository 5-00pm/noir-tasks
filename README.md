# Noir Tasks
Offline to-do app (Capacitor + vanilla JS). Data is stored on the device.

## Get the APK (no Android Studio needed)
1. Create an empty repo on github.com.
2. In this folder: `git init && git add -A && git commit -m init && git branch -M main`
   `git remote add origin <your-repo-url> && git push -u origin main`
3. Repo > Actions > "Build APK" (runs on push, or press "Run workflow").
4. When green, open the run > Artifacts > download `noir-tasks-apk`, unzip.
5. Copy `app-debug.apk` to your phone, open it, allow "Install unknown apps".

## Build locally instead
Needs Node 20, JDK 17, Android SDK:
`npm install && npx cap add android && npx cap sync android && cd android && ./gradlew assembleDebug`
APK: android/app/build/outputs/apk/debug/app-debug.apk
