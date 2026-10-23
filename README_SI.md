# Nubia ColourCam — Android source project

මෙය Nubia V60 ඇතුළු CameraX සහාය ඇති Android දුරකථන සඳහා Kotlin source project එකකි.

## ඇතුළත් දේ
- CameraX live camera preview
- Back/front camera මාරු කිරීම
- Auto, Cinematic, Nature, Night සහ Soft colour grading
- Photo එක `Pictures/ColourCam` වෙත JPEG ලෙස save කිරීම
- Camera permission request

## වැදගත් සීමාව
මෙම version එකේ **live preview එක සාමාන්‍ය camera preview එකකි**. තෝරාගත් colour grade එක photo එක capture කළ පසු apply වේ; preview එකට live colour effect එක තවම apply නොවේ. Night mode එක software brightness/tone adjustment එකක් පමණි; දිගු exposure, multi-frame night photography හෝ AI denoising නොවේ. Camera hardware/firmware quality වැඩි කරන්නේ නැහැ.

## APK build කරන ආකාරය
1. පරිගණකයක Android Studio (stable) install කරන්න.
2. මෙම ZIP එක extract කරන්න.
3. Android Studio → **Open** → `NubiaColourCam` folder එක තෝරන්න.
4. Gradle sync අවසන් වනතුරු ඉන්න. Internet අවශ්‍ය විය හැක (Gradle/dependencies download කිරීමට).
5. `Build` → `Build Bundle(s) / APK(s)` → `Build APK(s)` තෝරන්න.
6. APK එක සාමාන්‍යයෙන් `app/build/outputs/apk/debug/app-debug.apk` යටතේ ලැබේ.
7. APK එක Nubia V60 වෙත copy කර install කරන්න. Android prompt එකෙන් ඒ file manager එකට “Install unknown apps” permission දෙන්න අවශ්‍ය විය හැක. විශ්වාස කරන APK පමණක් install කරන්න.
8. App එක open කර Camera permission දෙන්න.

## අවශ්‍යතා
- Android Studio සහ Android SDK Platform 35
- JDK 17 (Android Studio bundled JDK භාවිත කළ හැක)
- Gradle wrapper මෙම ZIP එකට ထည့်ထားിട്ടില്ല; Android Studio project ကို open කළ විට Gradle setup ပြီး build လုပ်နိုင်သည်။ Wrapper generate လုပ်ရန် Android Studio/Gradle ကို အသုံးပြုနိုင်သည်.

## Troubleshooting
- Camera မဖွင့်လျှင် app permission စစ်ပြီး app ကို restart කරන්න.
- Build fail ဖြစ်လျှင် Android Studio/Gradle sync errors බලන්න; network access සහ JDK 17 තහවුරු කරන්න.
- මෙය source project එකකි, දැනට prebuilt APK එකක් නොවේ. APK එක build කිරීමට Android SDK build environment එකක් අවශ්‍යයි.
