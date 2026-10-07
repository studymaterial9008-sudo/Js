# JeevanSetu Android APK Project

यह Android Studio project `JeevanSetu_FINAL_PERMISSION_REQUIRED.zip` के current web app को native Android WebView wrapper में पैक करता है.

## इसमें क्या है
- Firebase-enabled JeevanSetu web app bundled in `app/src/main/assets/`
- Native Android Location permission
- Native Android Camera permission
- Android 13+ Notification permission
- Permission gate: तीनों permissions Allowed होने तक app आगे नहीं जाता
- Camera/QR WebView permission handling
- Location WebView geolocation handling
- App icon and portrait orientation

## Android Studio में खोलना
1. Android Studio खोलो.
2. `Open` चुनो.
3. पूरा `JeevanSetu_Android` folder select करो.
4. Gradle sync पूरा होने दो. Internet ON रखें ताकि Android Gradle Plugin/dependencies download हो सकें.
5. अगर Android Studio SDK/Gradle version पूछे तो recommended version accept करो.
6. Phone में USB debugging ON करके phone connect करो, या emulator चलाओ.
7. पहले **Run ▶** करके app test करो.
8. APK के लिए: **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
9. APK आमतौर पर `app/build/outputs/apk/debug/app-debug.apk` में बनेगा.

## Permission test
- Location → Allow
- Notification → Allow
- Camera → Allow
- तीनों Allowed होने के बाद ही JeevanSetu खुलेगा.
- किसी permission पर Deny करने पर app permission screen पर ही रहेगा.
- बाद में permission बदलने के लिए Android Settings → Apps → JeevanSetu → Permissions में Allow करो.

## Firebase
`app/src/main/assets/firebase-config.js` में वही Firebase web configuration रखी गई है जो current JeevanSetu ZIP में थी.

## Important
यह debug APK होगा जब तक Android Studio में release signing configure नहीं किया जाता. College/demo testing के लिए debug APK पर्याप्त है.
