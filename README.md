# Sleep Sheeps for Android

A landscape, full-screen Android app. Ten sheep jump the fence under a starry sky and the glowing moon counts them up to 999. It works offline, keeps the screen on, remembers the count, and the Exit button closes the app.

## Build the APK in Android Studio
1. Install Android Studio (free) and open this folder with **File > Open**.
2. Let it finish syncing. It downloads the Android SDK and Gradle the first time.
3. Choose **Build > Build App Bundle(s) / APK(s) > Build APK(s)**.
4. The APK is in `app/build/outputs/apk/`. Copy it to your phone and open it to install (allow "Install unknown apps" when asked).

You can also plug in your phone with USB debugging on and press the green Run button.

## Build it on GitHub instead
Push this folder to a GitHub repository. The included workflow (`.github/workflows/build-apk.yml`) builds the APK on every push. Download it from the run's **Artifacts** section on the Actions tab.

## Where things are
- `app/src/main/assets/index.html` is the whole scene: sky, moon, sheep and fence.
- `app/src/main/java/com/sleepsheeps/app/MainActivity.java` shows it full screen in landscape and closes the app when Exit is tapped.
- The release build is signed with the debug key so it installs directly. Use your own key before publishing to Google Play.

Each push to `main` also publishes the APK to the repository's **latest** release, so you can download `SleepSheeps.apk` from the Releases page.
