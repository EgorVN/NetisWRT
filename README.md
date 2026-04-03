# NetisWRT
# ImmortalWrt for Netis NX62 (Ultimate V6 - Mesh & Roaming Edition)
### Enterprise-Grade Networking, Seamless Wi-Fi, NAS, and Advanced VPN

This is the ultimate, feature-packed custom **ImmortalWrt** build for the **Netis NX62** (Netcore N60 Pro), powered by the quad-core **MediaTek MT7986 (Filogic 820)** SoC. 

**Ultimate V6** introduces massive upgrades for multi-node environments, including **B.A.T.M.A.N. Advanced Mesh** and **DAWN** for intelligent, seamless Wi-Fi roaming, alongside strict Access Control policies.

---

## 🚀 What's New in Ultimate V6?

* **Seamless Wi-Fi Roaming (DAWN):** Decentralized Automated Wi-Fi Node (DAWN) actively manages client connections, utilizing 802.11k/v/r to smoothly transition devices between access points and kick "sticky" clients.
* **B.A.T.M.A.N. Mesh:** True Layer-2 mesh networking support for creating a highly resilient, multi-router home network.
* **Access Control:** `luci-app-access-control` allows you to set internet access schedules and restrictions for specific devices (e.g., Parental Controls).
* **Modern Routing (nftset):** Added `dnsmasq_full_nftset` for direct integration with `nftables`. This enables ultra-fast, modern split-tunneling and policy-based routing.

---

## 💎 Core Capabilities

### ⚡ Peak Performance & Efficiency
* **Hardware Offloading:** `kmod-nft-offload` guarantees gigabit throughput with near-zero CPU usage.
* **SQM (Smart Queue Management):** Eliminates bufferbloat, ensuring stable ping for gaming even during heavy network saturation.
* **Core Optimization:** `irqbalance` and `kmod-rps` distribute network interrupts across all four CPU cores.

### 🛡️ Privacy & VPN Mastery
* **AmneziaWG (AWG):** Anti-DPI VPN technology to bypass the strictest network censorship.
* **L2TP Server:** Host your own VPN server via `xl2tpd` for secure remote access to your home network.
* **Ad-Blocking & DNS:** `adblock-fast` for DNS-level ad blocking, combined with `https-dns-proxy` (DoH) for encrypted DNS queries.

### 💾 Pro NAS & Storage (Disk-Master)
* **Visual Disk Management:** Use `luci-app-disk-man` to format, mount, and manage partitions directly from the WebUI.
* **File Systems:** Kernel-level **NTFS3**, **exFAT**, and **ext4** with CP866/UTF-8 localization.
* **Samba 4 & Discovery:** Share files across Windows/macOS/Linux effortlessly using `wsdd2` and `avahi`.
* **Drive Health:** `luci-app-hd-idle` to spin down idle disks and `badblocks` for sector health checks.

### 📶 Universal Connectivity (4G/5G)
* **ModemManager:** The modern standard for handling USB cellular modems (MBIM, QMI, RNDIS, NCM).
* **ISP Protocols:** Native support for PPPoE and L2TP (`xl2tpd`).

---

## 📦 Package Highlights

| Category | Essential Tools |
| :--- | :--- |
| **Mesh & Wi-Fi** | `dawn`, `kmod-batman-adv`, `batctl-default`, `wpad-openssl` |
| **Networking** | `firewall4`, `nftables`, `sqm`, `nlbwmon`, `access-control` |
| **VPN / WAN** | `luci-app-amneziawg`, `xl2tpd`, `ppp-mod-pppoe`, `ModemManager` |
| **Storage** | `luci-app-disk-man`, `samba4-server`, `hd-idle`, `badblocks` |
| **Admin Utilities**| `ttyd`, `mc`, `htop`, `tcpdump`, `iperf3`, `usbutils` |

---

## 🛠 Installation Guide

### 1. Initial Flash (from Stock)
1. Enter **U-Boot Web UI**: Hold the **Reset** button while powering on the device (keep holding for 10-15 seconds).
2. Set your PC's IP address to `192.168.1.2`.
3. Flash the `factory.bin` image via `192.168.1.1`.

### 2. Update (from OpenWrt/ImmortalWrt)
1. Navigate to **System -> Backup / Flash Firmware**.
2. Upload the `sysupgrade.bin` file.
3. **Crucial:** Uncheck "Keep settings" to ensure the new Mesh, DAWN, and nftset configurations initialize correctly without conflicts.

---

## ⚠️ Disclaimer
*Flashing custom firmware carries inherent risks. The author is not responsible for any hardware damage. Ensure you have a backup of your device's original Factory/EEPROM partition.*
