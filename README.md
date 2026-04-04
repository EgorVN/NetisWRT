# NetisWRT
# ImmortalWrt for Netis NX62 (Ultimate V9 - Enterprise Routing Edition)
### BGP, VxLAN, Seamless Mesh, NAS, and Advanced VPN Gateway

This is the definitive **ImmortalWrt** custom build for the **Netis NX62** (Netcore N60 Pro), powered by the quad-core **MediaTek MT7986 (Filogic 830)** SoC. 

**Ultimate V9** bridges the gap between home networking and data center routing. It introduces dynamic routing protocols (BGP/OSPF via BIRD2, Babel) and L2 overlay networks (VxLAN), making it the ultimate tool for complex network topologies, automated policy-based routing, and multi-site bridging.

---

## 🚀 What's New in Ultimate V9?

* **Dynamic Routing (BIRD 2):** Full support for BGP, OSPF, and RIP. Perfect for receiving automated route updates (e.g., dynamic split-tunneling lists) without manual IPSet management.
* **Babel Routing Protocol:** A loop-avoiding distance-vector routing protocol (`babeld`) that excels in wireless and mesh environments.
* **VxLAN Overlay Networks:** Stretch your Layer 2 network across the internet (Layer 3) using `kmod-vxlan`. Connect multiple remote sites as if they were plugged into the same physical switch.

---

## 💎 Core Capabilities

### 🌍 Enterprise Routing & Overlays
* **BGP / OSPF / RIP:** Powered by `bird2` for industrial-grade dynamic routing.
* **Mesh Routing:** Combine B.A.T.M.A.N. (Layer 2 Mesh) with Babel (Layer 3 dynamic routing) for an indestructible multi-node topology.
* **VxLAN:** Seamless Layer 2 bridging over WAN/VPN tunnels.

### ⚡ Peak Performance & Efficiency
* **Hardware Offloading:** `kmod-nft-offload` guarantees gigabit throughput with near-zero CPU usage.
* **SQM (Smart Queue Management):** Eliminates bufferbloat, ensuring stable ping for gaming even during heavy network saturation.
* **Core Optimization:** `irqbalance` and `kmod-rps` distribute network interrupts across all four CPU cores.

### 🛡️ Privacy & VPN Mastery
* **AmneziaWG (AWG):** Anti-DPI VPN technology to bypass the strictest network censorship.
* **L2TP Server:** Host your own VPN server via `xl2tpd` for secure remote access.
* **Ad-Blocking & Encrypted DNS:** `adblock-fast` for DNS-level ad blocking, combined with `https-dns-proxy` (DoH).

### 💾 Pro NAS & Storage (Disk-Master)
* **Visual Disk Management:** Use `luci-app-disk-man` to format, mount, and manage partitions directly from the WebUI.
* **File Systems:** Kernel-level **NTFS3**, **exFAT**, and **ext4** with CP866/UTF-8 localization.
* **Samba 4 & Discovery:** Share files effortlessly using `wsdd2` and `avahi`.

### 📶 Universal Connectivity (4G/5G)
* **ModemManager:** The modern standard for handling USB cellular modems (MBIM, QMI, RNDIS, NCM).
* **Seamless Wi-Fi Roaming:** DAWN (Decentralized Automated Wi-Fi Node) handles 802.11k/v/r client transitions.

---

## 📦 Package Highlights

| Category | Essential Tools |
| :--- | :--- |
| **Enterprise Routing**| `bird2`, `bird2c`, `babeld`, `kmod-vxlan` |
| **Mesh & Wi-Fi** | `dawn`, `kmod-batman-adv`, `batctl-default` |
| **Networking** | `nftables`, `sqm`, `nlbwmon`, `access-control` |
| **VPN / WAN** | `luci-app-amneziawg`, `xl2tpd`, `ModemManager` |
| **Storage** | `luci-app-disk-man`, `samba4-server`, `hd-idle` |
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
3. **Crucial:** Uncheck "Keep settings" to ensure the new routing daemons and DAWN/Mesh configurations initialize correctly without conflicts.

---

## ⚠️ Disclaimer
*Flashing custom firmware carries inherent risks. The author is not responsible for any hardware damage. Ensure you have a backup of your device's original Factory/EEPROM partition.*
