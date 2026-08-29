# Vyra Player — Android App

Project ini otomatis build jadi file `.apk` tiap kali kamu push ke branch `main`.

## Cara pake (via GitHub Desktop)

1. Clone repo ini pake GitHub Desktop.
2. Kalau mau update tampilan/fitur, edit file di dalam folder `www/` (itu source utamanya — `index.html`, dsb).
3. Commit & Push dari GitHub Desktop seperti biasa.
4. Buka repo ini di github.com, masuk tab **Actions** — tunggu sampai proses build selesai (centang hijau), biasanya 2-4 menit.
5. Ada dua cara ambil APK-nya:
   - **Releases** (di sidebar kanan repo, atau tab "Releases") — paling gampang, tinggal klik file `.apk`-nya buat download.
   - Atau di tab Actions, klik run yang barusan selesai, scroll ke bawah ke bagian "Artifacts", download `vyra-player-apk.zip` (isinya file apk).
6. Kirim/transfer file `.apk` itu ke HP Android, buka, install.

## Struktur folder

- `www/` — source HTML/CSS/JS aplikasinya (edit di sini)
- `android/` — project Android hasil generate Capacitor (biasanya gak perlu diutak-atik manual)
- `.github/workflows/build-apk.yml` — konfigurasi auto-build

## Catatan

- Lagu yang diupload user disimpan di IndexedDB di HP masing-masing, jadi aman kalau di-update.
- `applicationId` app ini: `com.vyra.player` — kalau ini ganti, Android bakal nganggep sebagai app yang beda (data lama gak nyambung ke versi baru).
