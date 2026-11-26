# Aesthetic Launcher (Android / Samsung)

A minimalist Android HOME launcher starter project inspired by vertical-list launchers. It is an independent app, not Niagara Launcher.

## Included
- Vertical alphabetical app list with app icons
- Search
- Favorites (long-press an app)
- Hide/unhide apps
- Clock and date
- Six selectable themes
- Choose a custom image wallpaper
- Gestures: swipe down on the launcher background to refresh; swipe horizontally on the background to open settings
- Android HOME intent filter so it can be selected as the default launcher

## Build an installable APK
1. Install **Android Studio** on a Windows, macOS, or Linux computer.
2. Open Android Studio and choose **Open**. Select the `AestheticLauncher` folder (the folder containing `settings.gradle.kts`).
3. Allow Gradle sync. If prompted, install Android SDK Platform 35 and use JDK 17 (Android Studio's bundled JBR is suitable).
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. When the build finishes, click **locate** in the notification. The debug APK is normally at:
   `app/build/outputs/apk/debug/app-debug.apk`
6. Transfer `app-debug.apk` to your Samsung phone. Open it and allow installation from that source if Android asks. Install.
7. Press the Home button. Choose **Aesthetic Launcher**, then choose **Always** to make it your default home screen. You can change it later under Settings > Apps > Choose default apps > Home app (wording varies by One UI version).

## Optional command-line build
From the project folder, with Android SDK and JDK 17 installed:
- Windows: `gradlew.bat assembleDebug`
- macOS/Linux: `./gradlew assembleDebug`

The output is `app/build/outputs/apk/debug/app-debug.apk`.

## Important notes
- This project is source code; a prebuilt APK is not included. Build it with Android Studio to produce the APK.
- `QUERY_ALL_PACKAGES` is used so the launcher can display installed apps. This is appropriate for a sideloaded personal launcher; publishing on Google Play is subject to Play's package-visibility policy.
- This is a first version. Wallpaper is applied as a launcher background; it does not change the phone's system wallpaper.
- Gesture detection currently works on unused background space, not on top of app rows or the scrollable app list.
- Android/Samsung may show a system chooser the first time you press Home.
- To return to One UI Home: Settings > Apps > Choose default apps > Home app > One UI Home.
