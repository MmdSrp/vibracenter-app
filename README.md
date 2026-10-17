# Vibra Center (اپ اندروید)

اپ یه WebView ساده است که https://vibracenter.ir رو کامل باز می‌کنه.

- صفحه سایت و استایل‌ها و عکس‌ها توی کش گوشی ذخیره می‌شن.
- اگه اینترنت قطع باشه: اگه نسخه ذخیره‌شده باشه با یه نوار نارنجی نشون داده می‌شه، وگرنه صفحه خطا با پیغام «اینترنتت مشکل داره» و دکمه «رفرش صفحه» میاد.
- با برگشتن اینترنت، صفحه خودکار رفرش می‌شه. کشیدن صفحه به پایین هم رفرش می‌کنه.
- دکمه Back گوشی توی تاریخچه سایت برمی‌گرده.

## گرفتن APK

### روش ۱: Android Studio
1. پوشه پروژه رو با Android Studio باز کن و صبر کن Gradle سینک بشه.
2. منوی Build ← Build Bundle(s) / APK(s) ← Build APK(s)
3. فایل توی `app/build/outputs/apk/debug/app-debug.apk` ساخته می‌شه.

### روش ۲: GitHub Actions (بدون نصب چیزی)
1. یه ریپوی جدید توی GitHub بساز و کل این پوشه رو آپلود کن (پوشه `.github` هم باید باشه).
2. برو به تب Actions ← Build APK ← Run workflow.
3. بعد از چند دقیقه، فایل APK رو از قسمت Artifacts همون اجرا دانلود کن.

## تغییرات رایج
- آدرس سایت: `START_URL` در `MainActivity.kt`
- اسم اپ و متن پیغام‌ها: `app/src/main/res/values/strings.xml`
- آیکون: `app/src/main/res/drawable/ic_launcher.xml` (می‌تونی با لوگوی خودت عوضش کنی)
