# Network Documentation

## Tujuan jaringan

B860H pernah dikembangkan untuk menerima koneksi Wi-Fi utama `Fabeils` melalui USB Wi-Fi dongle, dengan target menyediakan koneksi bagi perangkat lain melalui LAN dan/atau radio internal.

## Perangkat dan interface

- Wi-Fi upstream: jaringan `Fabeils`.
- USB Wi-Fi: TP-Link TL-WN727N, chipset MediaTek MT7601U.
- Interface station yang pernah disebut: `phy0-sta0`.
- Bridge LAN yang pernah dibahas: `br-lan`.
- IP B860H yang digunakan untuk akses Samba: `192.168.2.1`.

## Konsep topologi

```text
Main Wi-Fi: Fabeils
        |
USB Wi-Fi dongle (MT7601U)
        |
     ZTE B860H
      OpenWrt
        |
   LAN / Wi-Fi clients
```

Diagram ini menggambarkan tujuan desain, bukan bukti bahwa semua jalur bridge bekerja secara bersamaan pada konfigurasi saat ini.

## Hal yang perlu diverifikasi
- IP LAN aktual B860H.
- Mode dan nama radio wireless.
- Apakah `phy0-sta0` masih aktif.
- Isi `/etc/config/network`.
- Isi `/etc/config/wireless`.
- Apakah LAN dan Wi-Fi client berada pada subnet yang sama atau menggunakan routing/NAT.

## Pemeriksaan aman

Jalankan perintah berikut untuk membaca kondisi saat ini:

```sh
ip addr
ip route
iw dev
uci show network
uci show wireless
```

Simpan hasilnya sebelum mengubah konfigurasi. Hapus atau samarkan kata sandi Wi-Fi dan informasi sensitif sebelum membagikan output.
