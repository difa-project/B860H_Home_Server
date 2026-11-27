## Latest Development — 27 November 2026

### 1. Wi-Fi Repeater

B860H was configured as a Wi-Fi repeater.

- Uses a TP-Link TL-WN727N USB Wi-Fi adapter to receive the upstream Wi-Fi connection.
- Uses the internal Wi-Fi interface to broadcast the connection.
- Allows other devices to connect through the B860H.

### 2. Samba File Server

An external 1 TB HDD was connected to the B860H and configured as network storage.

- Samba was configured for file sharing.
- HDD mount point: `/mnt/sda1`
- Samba share: `stb-hdd`
- Local access path: `\\192.168.2.1\stb-hdd`

The Samba share was successfully accessed through Windows File Explorer on the home network.

### 3. Remote Access with Tailscale

Tailscale was installed and configured to enable private remote access.

Testing confirmed that:

- Tailscale connectivity between devices was successful.
- Samba could be accessed from the home network.
- Samba could also be accessed remotely through a mobile hotspot.
- Windows File Explorer successfully opened the remote Samba share.

No public port forwarding was required.

### Current Project Status

The B860H is currently used as:

1. Wi-Fi repeater.
2. Samba file server with external HDD storage.
3. Private remote storage server through Tailscale.

### Next Development Plan

The next planned project is system and network monitoring.

Potential monitoring features include:

- CPU usage.
- RAM usage.
- System temperature.
- Network connectivity.
- HDD storage capacity and health.

Monitoring is still a planned development and has not yet been implemented.

# Project History — ZTE B860H

**Perangkat:** ZTE B860H  
**Sistem operasi:** OpenWrt  
**Kernel yang pernah dilaporkan:** Linux 5.15.135-ophub  
**Periode dokumentasi:** 2026  
**Status:** Active development

## 1. Latar belakang

Proyek ini berawal dari eksplorasi pemanfaatan perangkat jaringan yang tersedia di rumah. B860H kemudian dikembangkan menjadi perangkat multifungsi berbasis OpenWrt, dengan fokus pada konektivitas Wi-Fi dan file server lokal.

F660 Playmedia merupakan proyek perangkat terpisah. Pengalaman menggunakan F660 sebagai penyimpanan jaringan menjadi konteks, tetapi konfigurasi F660 tidak boleh dianggap sebagai konfigurasi B860H.

## 2. Eksperimen Wi-Fi repeater

Tujuan eksperimen adalah menghubungkan B860H ke jaringan Wi-Fi utama bernama `Fabeils` melalui USB Wi-Fi dongle, lalu menyediakan konektivitas bagi perangkat lain melalui B860H.

Perangkat yang digunakan:
- ZTE B860H dengan OpenWrt.
- TP-Link TL-WN727N.
- Chipset MediaTek MT7601U.
- USB ID yang pernah diidentifikasi: `148F:7601`.

Interface wireless `phy0-sta0` pernah digunakan dalam mode managed/station untuk koneksi ke jaringan upstream.

Eksperimen juga mencakup penggunaan radio internal sebagai access point dan menjaga koneksi laptop melalui LAN. Detail konfigurasi akhir dan isi file konfigurasi lama belum tersedia lengkap.

## 3. Eksperimen bridge dan interface

Konfigurasi jaringan mencakup pembahasan `br-lan`, interface station, dan hubungan LAN dengan wireless. Tujuannya adalah menyederhanakan jaringan dan menjaga akses LAN.

Tidak semua kombinasi konfigurasi berhasil dipertahankan. Karena itu, dokumen ini tidak menyatakan konfigurasi bridge tertentu sebagai konfigurasi final.

## 4. Kendala dan pemulihan

Dalam pengembangan, perangkat sempat mengalami kendala akses dan tampilan HDMI menunjukkan pesan non-supported. Pemulihan dilakukan melalui failsafe.

Langkah yang dilaporkan:
1. Masuk ke failsafe.
2. Menjalankan `firstboot` untuk reset konfigurasi.
3. Melakukan reboot.
4. Menguji konektivitas menggunakan ping.
5. Akses ke perangkat berhasil dipulihkan.

`firstboot` adalah reset konfigurasi OpenWrt, bukan instalasi ulang firmware. Setelah reset, konfigurasi lama tidak boleh diasumsikan masih aktif.

## 5. Perkembangan menjadi file server

Pada November 2026, B860H juga digunakan sebagai file server lokal. HDD 1 TB terhubung dan diakses melalui Samba.

Alamat share yang pernah dilaporkan:
`\\192.168.2.1\stb-hdd`

Mount point HDD utama pernah disebut sebagai `/mnt/sda1`. Periksa kembali langsung di perangkat sebelum menggunakan path ini untuk tindakan administratif.

## 6. Ekspansi penyimpanan

HDD 350 GB direncanakan sebagai penyimpanan tambahan. Rencana nama share adalah `stb-hdd-350`, dengan alamat IP STB yang sama tetapi share berbeda.

Penggunaan HDD kedua belum dikonfirmasi berhasil. Rencana ekspansi USB hub juga muncul karena port USB STB sudah digunakan dongle Wi-Fi dan koneksi HDD.

## 7. Monitoring OLED

Pada 14 November 2026 muncul gagasan menambahkan layar OLED 0.96 inci menggunakan ESP32. ESP32 direncanakan mengambil data dari B860H melalui jaringan, sehingga tidak menggunakan port USB STB.

Informasi yang direncanakan:
- CPU usage.
- RAM usage.
- Suhu perangkat.
- Status jaringan.
- Kapasitas dan status HDD.

Hardware OLED dan implementasi software belum dikonfirmasi tersedia atau berjalan.

## 8. Prinsip pengembangan

- Pertahankan fungsi yang sudah berjalan.
- Cadangkan konfigurasi sebelum perubahan.
- Uji satu perubahan dalam satu waktu.
- Pisahkan proyek B860H dan F660.
- Catat perintah, hasil, dan tanggal eksperimen.
- Jangan tandai rencana sebagai fitur selesai.

## 9. Batasan dokumentasi

Dokumen ini direkonstruksi dari percakapan yang tersedia. Detail perintah terminal dan konfigurasi historis lengkap—termasuk isi lama `/etc/config/network` dan `/etc/config/wireless`—belum tersedia. Dokumentasi harus diperbarui setelah pemeriksaan langsung perangkat.
