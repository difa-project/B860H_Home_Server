# Troubleshooting Log

## 1. Akses STB terganggu setelah eksperimen konfigurasi

**Gejala**
- Akses konfigurasi perangkat terganggu.
- Tampilan HDMI menunjukkan pesan `non-supported`.

**Tindakan**
1. Masuk ke mode failsafe.
2. Menjalankan `firstboot`.
3. Reboot perangkat.
4. Menguji konektivitas dengan ping.

**Hasil**
- Ping berhasil.
- Akses perangkat dilaporkan pulih.

**Catatan**
`firstboot` mereset konfigurasi OpenWrt. Ini bukan instalasi ulang firmware dan dapat menghapus pengaturan yang sebelumnya dibuat.

## 2. Eksperimen bridge dan wireless

**Konteks**
- Pembahasan interface `phy0-sta0` dan `br-lan`.
- Target menggunakan USB Wi-Fi sebagai station dan radio internal untuk membagikan jaringan.

**Status**
- Detail penyebab kegagalan dan konfigurasi terakhir belum terdokumentasi lengkap.
- Jangan menganggap konfigurasi bridge tertentu sebagai solusi final.

## Template catatan masalah baru

### [Tanggal] — Judul masalah
- **Gejala:**
- **Kondisi sebelum masalah:**
- **Perintah/perubahan terakhir:**
- **Hasil pemeriksaan:**
- **Tindakan:**
- **Hasil akhir:**
- **Status:** Open / Investigating / Resolved
