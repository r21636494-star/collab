COLLAB Android prototype — v0.1.0

WHAT THIS IS
A small Android Studio project that wraps the COLLAB mobile prototype in an Android WebView.
It is intended for installing on your own Android phone for an early UI test.

IMPORTANT LIMITATIONS
- This is a LOCAL demo. Account, posts, likes, bio and communities are stored only on this phone.
- It does not connect to other users or the internet.
- It is not a production social network and has not had a security review.
- It does not yet include messaging, real follow relationships, moderation tools or a server.

HOW TO BUILD AN APK ON WINDOWS
1. Install Android Studio from the official Android developer site:
   https://developer.android.com/studio
2. Extract this ZIP.
3. In Android Studio choose File > Open and select the extracted COLLAB_Android folder.
4. Wait for Gradle sync. If prompted, install the Android SDK Platform 35 and accept the license.
5. Select Build > Build Bundle(s) / APK(s) > Build APK(s).
6. When the build finishes, click "locate" in the notification.
   The APK is normally at: app/build/outputs/apk/debug/app-debug.apk
7. Send app-debug.apk to your Android phone (USB, Drive, Bluetooth, etc.).
8. Open it on the phone. If Android asks, allow installation from that file source.
   Only install APKs you built yourself from this project.

REQUIREMENTS
- Android Studio with Android SDK Platform 35
- JDK 17 (Android Studio normally supplies its own)
- Android phone running Android 6.0 or newer

PROJECT PACKAGE
Application ID: com.collab.app
Version: 0.1.0


BUILD WITHOUT ANDROID STUDIO (CLOUD BUILD)
This project includes .github/workflows/android-apk.yml for GitHub Actions.
You can build the APK on GitHub's cloud Linux runner; your 32-bit Windows laptop
does not need Android Studio or a local Android SDK.

1. Create/sign in to a GitHub account at https://github.com
2. Create a NEW repository. A public repository is simplest for GitHub Actions.
3. Upload the CONTENTS of this extracted project folder to the repository
   (including the hidden .github folder and its workflow file).
4. Open the repository's Actions tab and enable Actions if GitHub asks.
5. Select "Build COLLAB Android APK" and click "Run workflow".
6. Wait for the workflow to finish successfully.
7. Open the completed run and download the "COLLAB-debug-APK" artifact.
   GitHub downloads it as a ZIP; extract it to get app-debug.apk.
8. Send app-debug.apk to your Android phone and install it.

Keep in mind: this is an unsigned-for-release debug APK for personal testing.
Do not publish it as a production app. The app is still an offline local demo.
