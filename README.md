# NetisWRT
# ImmortalWrt for Netis NX62 (Ultimate V2 - Performance Optimized)
### Enterprise-Grade Powerhouse: High-Speed Networking, NAS, and Security

This is the definitive **ImmortalWrt** custom build for the **Netis NX62** (Netcore N60 Pro), powered by the **MediaTek MT7986 (Filogic 830)** quad-core SoC. 

**Ultimate V2** is not just about features; it's about **efficiency**. We've added hardware-level optimizations to ensure gigabit speeds with minimal CPU load and advanced tools for network health.

---

## 🚀 Key Enhancements in V2

### ⚡ Peak Performance & Efficiency
* **Hardware Offloading:** Enabled `kmod-nft-offload` for near-zero CPU usage during high-speed routing.
* **Core Optimization:** `irqbalance` and `kmod-rps` distribute network interrupts across all four cores, preventing bottlenecks.
* **SQM (Smart Queue Management):** Integrated `luci-app-sqm` to eliminate bufferbloat, ensuring low latency for gaming and VOIP even during heavy downloads.
* **Monitoring:** `nlbwmon` for detailed bandwidth tracking by device and `iperf3` for network speed testing.

### 🛡️ Privacy & Advanced Security
* **AmneziaWG 2.0 (AWG):** Superior anti-DPI VPN technology to bypass strict censorship.
* **Ad-Blocking:** `adblock-fast` provides a high-performance, lightweight solution to block ads and trackers at the DNS level.
* **L2TP Server:** Includes `xl2tpd`, allowing you to host your own VPN server for remote access.
* **Encrypted DNS:** `https-dns-proxy` for secure, private DNS queries (DoH).

### 💾 Pro NAS & Disk Management
* **Disk-Man Interface:** A complete graphical manager for partitions, formatting, and mounting.
* **Health Check:** Added `badblocks` to scan and monitor the physical health of your drives.
* **Samba 4 & Discovery:** Full NAS functionality with `wsdd2` and `avahi` for seamless discovery on Windows/macOS/Linux.
* **File Systems:** Kernel-level support for **NTFS3**, **exFAT**, and **ext4** with proper NLS (UTF-8/CP866) encoding.

---

## 📦 Package Highlights

| Category | Essential Tools |
| :--- | :--- |
| **Networking** | `firewall4`, `nftables`, `sqm`, `nlbwmon`, `irqbalance`, `ethtool` |
| **VPN / WAN** | `luci-app-amneziawg`, `xl2tpd` (Server), `ppp-mod-pppoe`, `ddns-scripts` |
| **Modem** | `ModemManager`, `cdc-mbim`, `qmi-wwan`, `rndis` |
| **Storage** | `luci-app-disk-man`, `samba4-server`, `badblocks`, `usb-storage-uas` |
| **Admin Utilities**| `ttyd`, `mc`, `htop`, `tcpdump`, `iperf3`, `logrotate`, `usbutils` |

---

## 🛠 Installation

### 1. Initial Flash (from Stock)
1. Enter **U-Boot Web UI**: Hold **Reset** while powering on (hold for 12-15s).
2. Set PC IP to `192.168.1.2`.
3. Flash the `factory.bin` via `192.168.1.1`.

### 2. Update (from OpenWrt)
1. Use the `sysupgrade.bin` file in **System -> Backup / Flash Firmware**.
2. **Important:** Uncheck "Keep settings" to initialize all new V2 performance tweaks correctly.

---

## ⚠️ Disclaimer
*Flashing custom firmware carries inherent risks. Ensure you have a backup of your device's original Factory/EEPROM partition.*
