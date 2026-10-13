# Basma Alarm Updates

Place an `update.json` file in the repository root, with a versionCode greater than the installed app and a direct MediaFire APK download URL:

```json
{"versionCode":2,"versionName":"1.0.1","apkUrl":"https://www.mediafire.com/file/.../basma.apk"}
```

Publish only APK files signed with the same private signing key and application ID as the installed app. Do not commit signing keys. The Android package fetches this manifest at launch and requests the user's confirmation before installation; Android does not permit silent installation for ordinary apps.

The APK URL is intentionally not configured until the first signed release is available.
