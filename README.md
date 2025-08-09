# AwanDemo (Android, Kotlin + Compose)

Aplikasi Android sederhana dengan satu layar (counter) menggunakan Jetpack Compose.
Data klik disimpan di `SharedPreferences` (persisten).

## Cara build lokal (APK Debug)
1. Install **Android Studio** (JDK 17, Android SDK 34).
2. Buka folder proyek ini.
3. Jalankan Gradle task: **:app:assembleDebug**.
4. APK akan muncul di: `app/build/outputs/apk/debug/app-debug.apk` (sudah *debug-signed* dan bisa di-install).

> Jika gradle wrapper belum ada, Anda bisa pakai perintah `gradle :app:assembleDebug` dengan Gradle 8.8+ terpasang secara global.

## Build via GitHub Actions (otomatis menghasilkan APK)
1. Buat repo GitHub baru dan push isi folder proyek ini.
2. Buka tab **Actions**, jalankan workflow **Android Debug APK** (atau push ke branch `main`).
3. APK dapat diunduh dari **Artifacts** bernama `app-debug-apk`.

## Kustomisasi
- Ubah nama app di `app/src/main/res/values/strings.xml`.
- Ubah package name di `app/build.gradle.kts` (`namespace` & `applicationId`) dan struktur folder `java/com/example/awandemo`.
- Tambahkan fitur dengan Jetpack Compose di `MainActivity.kt`.

## Rilis (Release APK/AAB)
- Untuk Play Store, buat keystore, set `signingConfigs` & `buildTypes.release` agar signed.
- Bangun dengan `assembleRelease` (butuh signing) atau buat **AAB** dengan `bundleRelease`.

---
Dibuat otomatis oleh ChatGPT.
