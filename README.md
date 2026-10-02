# RuangKita — Community Web App

Prototype antarmuka komunitas bergaya aplikasi chat, responsif untuk Android dan desktop. Termasuk login/daftar demo, kanal, feed pesan, reaksi sederhana, PWA, serta empat file animasi Rive yang diberikan.

## Jalankan di browser / SPCK
1. Ekstrak ZIP.
2. Buka folder `komunitas-x` di editor atau jalankan `index.html` melalui local server.
3. Koneksi internet diperlukan untuk memuat runtime Rive dan font Google pada versi ini.
4. Login saat ini hanya simulasi lokal. Jangan gunakan kata sandi asli.

## Build APK dengan Capacitor
Persyaratan: Node.js LTS, Android Studio, Android SDK.

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Di Android Studio, tunggu Gradle selesai, lalu pilih **Build > Build Bundle(s) / APK(s) > Build APK(s)**.

Jika direktori `android` sudah ada, jangan jalankan `cap add android` lagi; cukup `npx cap sync android`.

## Catatan status
- Login, registrasi, kanal, dan pengiriman pesan adalah demo frontend; data tidak tersimpan ke server dan tidak sinkron antar pengguna.
- Untuk menjadi komunitas sungguhan diperlukan backend, database, autentikasi aman, chat realtime, moderasi, dan penyimpanan media.
- Nama input dan state machine pada file Rive belum dipetakan; saat ini runtime mencoba memainkan artboard default. Interaksi teddy mengikuti input Rive setelah nama input diverifikasi.
- Jangan deploy publik dengan autentikasi demo ini.
