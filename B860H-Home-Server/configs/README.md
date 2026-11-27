# B860H Home Server

A home server project built using a ZTE B860H Android Set-Top Box running OpenWrt.

The project explores how low-cost hardware can be repurposed into a multifunctional home server.

## Current Features

- **Wi-Fi Repeater** — Receives an upstream Wi-Fi connection using an external USB Wi-Fi adapter and rebroadcasts it through the internal Wi-Fi interface.
- **Samba File Server** — Shares an external 1 TB HDD across the local network.
- **Remote Access** — Uses Tailscale to access the Samba file server privately from outside the home network.

## Hardware

| Component | Description |
|---|---|
| Device | ZTE B860H |
| RAM | 1 GB |
| Operating System | OpenWrt |
| External Storage | 1 TB HDD |
| USB Wi-Fi Adapter | TP-Link TL-WN727N |
| Wi-Fi Chipset | MediaTek MT7601U |

## Network & Storage

| Item | Configuration |
|---|---|
| STB Local IP | `192.168.2.1` |
| Samba Share | `stb-hdd` |
| HDD Mount Point | `/mnt/sda1` |
| Local Samba Path | `\\192.168.2.1\stb-hdd` |
| Remote Access | Tailscale |

## Documentation

- [Project History](PROJECT_HISTORY.md)
- [Changelog](CHANGELOG.md)
- [Hardware](docs/HARDWARE.md)
- [Network Configuration](docs/NETWORK.md)
- [Storage Configuration](docs/STORAGE.md)
- [Remote Access](docs/REMOTE_ACCESS.md)
- [Monitoring Development Plan](docs/MONITORING.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)

## Current Project Status

<text> </text>
**Operational:**
- Wi-Fi repeater
- Samba file sharing
- Remote Samba access through Tailscale

**Planned:**
- System monitoring
- Network monitoring
- Hardware monitoring dashboard

## Project Goals

1. Explore embedded Linux and OpenWrt.
2. Learn networking and Linux system administration.
3. Repurpose inexpensive hardware into a useful home server.
4. Gradually develop monitoring and automation capabilities.

---

*This repository documents the development, configuration, experiments, and lessons learned throughout the B860H Home Server project.*
