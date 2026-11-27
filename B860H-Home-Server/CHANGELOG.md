# Changelog

Semua perubahan penting proyek dicatat di sini. Catatan ini merupakan ringkasan berdasarkan histori percakapan; tanggal yang lebih spesifik hanya digunakan jika tersedia.

## [2026-11-27] - Remote Access Successfully Implemented

### Added
- Configured Tailscale on the B860H for private remote access.
- Added remote access documentation in `docs/REMOTE_ACCESS.md`.

### Tested
- Verified Tailscale connectivity between devices.
- Successfully accessed Samba from the local home network.
- Successfully accessed Samba remotely using a mobile hotspot.
- Verified remote file access through Windows File Explorer.

### Result
- B860H can now provide remote access to its Samba file server.
- No public port forwarding is required.

## 2026-11-15
- Menyusun dokumentasi proyek B860H.
- Mendokumentasikan penggunaan HDD 1 TB sebagai penyimpanan jaringan.
- Mencatat alamat Samba `\\192.168.2.1\stb-hdd`.
- Mencatat rencana ekspansi HDD 350 GB dan USB hub.

## 2026-11-14
- Membahas keterbatasan dua port USB pada STB.
- Merencanakan ekspansi perangkat USB.
- Mengembangkan konsep monitoring B860H menggunakan ESP32 dan OLED 0.96 inci.

## Oktober 2026 — tanggal rinci perlu diverifikasi
- Mengembangkan eksperimen Wi-Fi repeater menggunakan USB Wi-Fi TP-Link TL-WN727N.
- Mengidentifikasi chipset MediaTek MT7601U dan USB ID `148F:7601`.
- Mengeksplorasi interface `phy0-sta0`, mode managed/station, access point, dan bridge LAN.
- Mengalami kendala akses dan melakukan pemulihan melalui failsafe serta `firstboot`.
- Akses perangkat berhasil dipulihkan setelah reset konfigurasi.

## Catatan
Jangan menambahkan fitur ke bagian “Added” atau menandainya selesai sebelum pengujian langsung berhasil.
