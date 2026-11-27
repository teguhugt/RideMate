# RideMate - paket siap unggah

Isi paket (semua file harus berada di satu folder yang sama):

- `index.html` : aplikasi RideMate
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` : agar bisa dipasang ke layar utama
- `sw.js` : service worker, membuat aplikasi tetap bisa dibuka saat offline setelah dibuka sekali

## Cloudflare Pages (disarankan)
1. Masuk ke dash.cloudflare.com, buka Workers & Pages, lalu Create, pilih Pages.
2. Pilih Upload assets (Direct Upload), beri nama proyek.
3. Unggah folder ini (atau file ZIP-nya), lalu Deploy.
4. Buka alamat `https://nama-proyek.pages.dev`.

## Netlify
1. Buka app.netlify.com/drop.
2. Seret folder ini ke halaman tersebut.

## GitHub Pages
1. Buat repository baru, unggah semua file di root repository.
2. Settings, Pages, pilih branch `main` dan folder `/ (root)`.

## Setelah online
- Buka alamat HTTPS di Chrome (Android) lalu pilih Instal aplikasi, atau di Safari (iPhone) pilih Bagikan, lalu Tambah ke Layar Utama. Menu Lainnya juga punya tombol Install.
- Data tersimpan di browser per alamat situs. Untuk memindahkan data dari versi lama: Profil, Cadangan data, Simpan (di versi lama), lalu Pulihkan (di versi baru).
- Setiap kali mengganti file, naikkan nomor versi di `sw.js` (misalnya `ridemate-v20` menjadi `ridemate-v21`) supaya pengguna mendapat pembaruan.
- Akun hanya tersimpan di perangkat (tanpa server). Untuk login lintas perangkat dibutuhkan backend.
