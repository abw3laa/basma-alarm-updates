# مستودع تحديثات منبّه بصمة

يحتوي هذا المستودع على بيان التحديث الذي يقرأه التطبيق عند فتحه. رابط البيان العام:

`https://raw.githubusercontent.com/abw3laa/basma-alarm-updates/main/update.json`

## الإصدار المشار إليه حالياً

البيان يشير إلى APK الإصدار **1.2.0** (`versionCode: 3`) على MediaFire:

`https://www.mediafire.com/file/y4pbowg4xr61cun/basma+alarm+1.2.0.apk/file`

## صيغة البيان

```json
{
  "versionCode": 3,
  "versionName": "1.2.0",
  "apkUrl": "https://www.mediafire.com/file/y4pbowg4xr61cun/basma+alarm+1.2.0.apk/file"
}
```

عند إصدار تحديث جديد، ارفع APK Release الموقّع على MediaFire ثم عدّل هذه القيم الثلاث في `update.json`. يجب أن يكون `versionCode` أكبر من النسخة المثبتة على الجهاز، وأن يعكس `versionName` رقم الإصدار، وأن يكون `apkUrl` رابط مشاركة الملف الصحيح. استخدم رابط صفحة MediaFire الثابتة، لا رابط تنزيل مؤقتاً من نوع `downloadNNN.mediafire.com`.

## متطلبات التوافق والأمان

- التطبيق: `com.abw3laa.basmaalarm`.
- كل تحديث يجب أن يستخدم **شهادة التوقيع/keystore نفسها** المستخدمة في النسخة المثبتة. لا تغيّر مفتاح التوقيع ولا ترفعه إلى GitHub.
- يتحقق التطبيق من معرّف الحزمة ورقم الإصدار والتوقيع قبل فتح مثبت Android.
- يبدأ التطبيق تنزيل التحديث في الخلفية عبر `DownloadManager`، ثم يطلب من المستخدم تأكيد التثبيت. يلزم السماح بالتثبيت من هذا المصدر، ولا يوجد تثبيت صامت.
- المستودع يحفظ البيان والرابط فقط؛ ملف APK مستضاف في MediaFire.

النسخة التالية التي يجري إعدادها في مستودع التطبيق هي **1.3.0 / versionCode 4**. بعد بناء Release ورفعه إلى MediaFire، حدّث `update.json` إلى `versionCode: 4` و`versionName: "1.3.0"` ثم استبدل `apkUrl` برابط MediaFire الجديد.