# ViralClip AI V4.7 Production Hybrid

V4.7 melanjutkan V4.6 dan menambahkan dua sumber video: **Import Lokal** dan **Import dari URL**.

## Sumber URL
Mendukung URL publik dari platform yang didukung oleh `yt-dlp`, termasuk banyak URL YouTube, Instagram, TikTok, Facebook, Threads, dan situs video lain. Dukungan aktual bergantung pada perubahan platform, status publik/private, login, age restriction, dan kebijakan layanan.

### Engine URL
- Instal `yt-dlp` dan pastikan `yt-dlp.exe` tersedia di PATH Windows, **atau** pilih executable melalui Admin → Engine → yt-dlp.exe.
- FFmpeg disarankan tersedia/diatur karena diperlukan untuk penggabungan format tertentu dan export.
- Video URL diunduh ke folder data aplikasi lalu diperlakukan sebagai video lokal untuk analisis/edit/export.

## Hybrid
- Offline: SQLite lokal, analisis lokal, editor, export.
- Online: Cloud API, sinkronisasi akun, status langganan, pembayaran backend.
- Saat cloud tidak tersedia, aplikasi tetap dapat menggunakan data lokal sesuai aturan akses yang sudah tersimpan.

## Free/Pro
Batas penggunaan dan paket Pro tetap dikelola Admin. Masa Pro memiliki tanggal mulai/berakhir dan dapat disinkronkan dari cloud.

## Build Windows
```bash
npm install
npm run dist
```
atau jalankan `build-windows.bat`.

## Catatan Production
Jangan memasukkan secret pembayaran ke aplikasi desktop. Server Key/payment secrets hanya berada di backend.

Untuk URL privat/login-required, jangan menyimpan atau meminta kredensial pengguna secara sembarangan. Jika sumber membutuhkan autentikasi, gunakan mekanisme resmi platform atau konfigurasi yang sesuai hukum/kebijakan layanan.
