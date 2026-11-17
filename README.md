# USB Pad Android

Projek Android WebView untuk menjalankan fail HTML USB Pad dalam aplikasi Android.

## Build APK melalui GitHub Actions
1. Muat naik semua kandungan folder projek ini ke repository GitHub.
2. Buka tab **Actions**.
3. Pilih workflow **Build USB Pad APK**.
4. Tekan **Run workflow** (atau push ke branch `main`).
5. Apabila selesai, buka run yang berjaya dan muat turun artifact **USBPad-debug-apk**.
6. Ekstrak ZIP artifact untuk mendapatkan `app-debug.apk`, kemudian pasang pada telefon Android.

## Build secara lokal
Perlu JDK 17 dan Gradle 8.9:
```bash
gradle assembleDebug
```
APK: `app/build/outputs/apk/debug/app-debug.apk`

## Had fungsi semasa
Fail HTML asal ialah pratonton kawalan. Fungsi `send()` hanya menulis mesej input ke log pada skrin; ia belum menghantar input kepada permainan, komputer, USB atau Bluetooth. Projek ini membungkus HTML tersebut sebagai aplikasi Android dan mengekalkan fungsi yang memang sudah ada.
