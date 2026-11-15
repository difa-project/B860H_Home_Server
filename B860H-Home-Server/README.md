# ZTE B860H Home Server

Dokumentasi pengembangan STB ZTE B860H berbasis OpenWrt sebagai perangkat jaringan dan server lokal.

## Tujuan proyek
- Mengembangkan B860H sebagai perangkat jaringan multifungsi.
- Menggunakan koneksi Wi-Fi melalui USB dongle.
- Menyediakan penyimpanan lokal melalui HDD eksternal dan Samba.
- Mengembangkan monitoring perangkat menggunakan ESP32 dan OLED.

## Status singkat
- OpenWrt berjalan pada B860H.
- USB Wi-Fi TP-Link TL-WN727N dengan chipset MediaTek MT7601U pernah terdeteksi.
- Fungsi repeater dan Samba server dilaporkan berfungsi.
- HDD 1 TB digunakan sebagai penyimpanan jaringan.
- HDD 350 GB dan monitoring OLED masih berupa rencana.

## Struktur dokumentasi
- [`PROJECT_HISTORY.md`](PROJECT_HISTORY.md): perjalanan proyek secara kronologis.
- [`CHANGELOG.md`](CHANGELOG.md): ringkasan perubahan berdasarkan tanggal.
- [`docs/HARDWARE.md`](docs/HARDWARE.md): perangkat keras.
- [`docs/NETWORK.md`](docs/NETWORK.md): topologi dan konfigurasi jaringan.
- [`docs/STORAGE.md`](docs/STORAGE.md): HDD, mount point, dan Samba.
- [`docs/TROUBLESHOOTING.md`](docs/TROUBLESHOOTING.md): kendala dan pemulihan.
- [`docs/MONITORING.md`](docs/MONITORING.md): rencana monitoring OLED.
- [`configs/README.md`](configs/README.md): panduan menyimpan konfigurasi.

## Catatan akurasi
Dokumentasi ini disusun dari histori percakapan yang tersedia, bukan hasil audit langsung perangkat. Status yang belum diuji atau belum dikonfirmasi ditandai sebagai rencana atau perlu verifikasi. Jangan menganggap contoh konfigurasi sebagai konfigurasi aktif.

## Prinsip pengembangan
1. Cadangkan konfigurasi sebelum mengubah jaringan.
2. Ubah satu hal dalam satu waktu.
3. Uji konektivitas setelah perubahan.
4. Jangan memformat HDD sebelum memastikan isi dan target perangkat.
5. Pisahkan fakta teruji, percobaan, dan rencana.
