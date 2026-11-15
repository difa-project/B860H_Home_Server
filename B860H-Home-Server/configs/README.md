# Configuration Backups

Folder ini disediakan untuk menyimpan salinan konfigurasi B860H yang sudah diperiksa dan disamarkan.

## File yang dapat disimpan
- `network` — salinan `/etc/config/network`.
- `wireless` — salinan `/etc/config/wireless`.
- `fstab` — konfigurasi mount.
- `samba` — konfigurasi Samba, jika relevan.

## Penting: keamanan
Jangan mengunggah kata sandi Wi-Fi, password Samba, private key, token, atau informasi rahasia lainnya ke repository publik.

Sebelum mengunggah:
1. Buat salinan konfigurasi.
2. Samarkan kredensial.
3. Beri nama file dengan tanggal, misalnya `network-2026-11-16.example`.
4. Catat apakah file merupakan konfigurasi aktif atau hanya contoh.

Jangan menimpa konfigurasi aktif pada STB hanya dengan menyalin file dari repository tanpa memeriksa kecocokan perangkat dan jaringan.
