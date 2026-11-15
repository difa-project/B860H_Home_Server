# B860H Monitoring — ESP32 & OLED

## Tujuan

Membuat layar monitoring kecil untuk menampilkan kondisi B860H tanpa harus selalu membuka antarmuka administrasi OpenWrt.

## Konsep arsitektur

```text
ZTE B860H (OpenWrt)
        |
   Local Wi-Fi
        |
      ESP32
        |
   OLED 0.96 inch
```

ESP32 direncanakan mengambil data dari B860H melalui jaringan. Dengan demikian, port USB STB tetap dapat digunakan untuk dongle Wi-Fi dan penyimpanan.

## Informasi yang ingin ditampilkan
- CPU usage.
- RAM usage.
- Suhu perangkat.
- Status koneksi jaringan.
- Kapasitas HDD.
- Status mount/storage.

## Status komponen

| Komponen | Status |
|---|---|
| B860H | Tersedia |
| ESP32 | Rencana |
| OLED 0.96 inci | Belum dimiliki menurut catatan |
| Software monitoring | Belum dibuat |

## Tahapan implementasi
1. Memilih board ESP32 dan OLED yang kompatibel.
2. Menentukan metode pengambilan data dari OpenWrt.
3. Membuat endpoint atau skrip pembaca status pada B860H.
4. Mengirim data melalui jaringan lokal.
5. Menampilkan data pada OLED.
6. Menguji stabilitas dan interval pembaruan.

Semua tahap di atas masih merupakan rencana.
