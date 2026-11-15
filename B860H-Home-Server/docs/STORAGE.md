# Storage & Samba

## HDD utama

| Parameter | Catatan |
|---|---|
| Kapasitas | 1 TB |
| Mount point yang pernah dilaporkan | `/mnt/sda1` |
| IP STB untuk akses | `192.168.2.1` |
| Nama Samba share | `stb-hdd` |
| Path Windows | `\\192.168.2.1\stb-hdd` |

Path mount dapat berubah tergantung urutan perangkat, konfigurasi mount, dan sistem. Verifikasi dengan `lsblk`, `mount`, atau `df -h` sebelum menjalankan operasi file.

## HDD tambahan

Rencana ekspansi:
- Kapasitas: 350 GB.
- Nama share yang direncanakan: `stb-hdd-350`.
- Akses melalui IP B860H yang sama, dengan nama share berbeda.

HDD tambahan belum dikonfirmasi berhasil dipasang dan diuji.

## Target struktur share

```text
B860H (192.168.2.1)
├── stb-hdd       -> HDD 1 TB
└── stb-hdd-350   -> HDD 350 GB (planned)
```

## Verifikasi

```sh
lsblk
df -h
mount
```

Sebelum mengubah partisi atau filesystem, pastikan disk yang dipilih benar dan data penting sudah dicadangkan.
