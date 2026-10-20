# SubMeter Pro Android wrapper

This Android Studio project wraps the supplied `Submeter Scanner & Billing App.html` as an Android WebView app. It enables JavaScript, local asset loading through a secure appassets origin, camera permission prompts, and image selection.

## Build the APK
1. Install Android Studio (with Android SDK Platform 35 or newer available).
2. Open this `SubMeterProAndroid` folder in Android Studio.
3. Allow Gradle sync to complete (internet is required for Gradle dependencies).
4. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Android Studio will show the APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.
6. Copy the APK to your Android phone and install it. If prompted, allow installing apps from that file manager.

## Notes
- The HTML file is preserved as supplied. It loads Tailwind CSS, Lucide icons, and Tesseract.js from CDNs, so an internet connection is needed for those libraries.
- Camera scanning requires granting camera permission when prompted.
- The supplied JavaScript stores its tenant and bill data in in-memory variables; data persistence across app restarts is not added by this wrapper.
- For distribution beyond testing, create a signed release APK from Android Studio.
