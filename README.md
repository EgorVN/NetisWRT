# NetisWRT
# ImmortalWrt for Netis NX62 (Ultimate V2)
### The Complete Networking & Storage Solution for MediaTek MT7986

This is an updated, high-performance custom build of **ImmortalWrt** for the **Netis NX62** (Netcore N60 Pro). **Version 2** focuses on superior disk management and expanded connectivity options, making it a perfect choice for a home NAS, a secure VPN gateway, or a 5G mobile router.

---

## 💎 What's New in V2?

* **Integrated Disk Manager:** Added `luci-app-disk-man` for a full-featured graphical partition and disk management experience.
* **Expanded DDNS Support:** Beyond Cloudflare, V2 includes a wide array of DDNS services for remote access.
* **Refined NAS Stack:** Optimized Samba 4 and NTFS3 configuration for maximum USB 3.0 throughput.

---

## 🚀 Key Features

### 🛡️ Privacy & VPN Mastery
* **AmneziaWG (AWG):** Anti-DPI VPN technology to bypass strict censorship and blocks.
* **DNS-over-HTTPS:** Encrypted DNS queries via `https-dns-proxy`.
* **Advanced Routing:** `dnsmasq-full` with `ipset` support for domain-based traffic steering (split tunneling).

### 💾 Storage & NAS (Disk-Master)
* **Disk-Man UI:** Format, partition, and manage your HDDs/SSDs directly from LuCI.
* **Modern FS Support:** High-speed kernel-level **NTFS3**, **exFAT**, and **ext4**.
* **Maintenance Ready:** Includes `e2fsprogs` and `ntfs-3g-utils` for disk health and repairs.
* **UAS Support:** USB Attached SCSI for SSD-grade speeds over USB 3.0.

### 📶 Universal Connectivity
* **4G/5G Ready:** Modern `ModemManager` stack with support for MBIM, QMI, and RNDIS protocols.
* **ISP Protocols:** Full support for PPPoE and L2TP (`xl2tpd`).
* **Wi-Fi 6:** Secure WPA3-SAE connectivity powered by `wpad-openssl`.

### 🛠️ System Tools
* **Terminal:** `ttyd` (Web-based terminal access).
* **File Manager:** `Midnight Commander (mc)`.
* **Monitoring:** `htop` and `luci-app-statistics` for real-time load and temperature tracking.

---

## 📦 Package Summary

| Category | Highlights |
| :--- | :--- |
| **WAN/Internet** | `ModemManager`, `ppp-mod-pppoe`, `xl2tpd`, `usb-modeswitch` |
| **VPN** | `luci-app-amneziawg`, `kmod-amneziawg` |
| **Disk/NAS** | `luci-app-disk-man`, `samba4-server`, `kmod-fs-ntfs3`, `kmod-fs-exfat` |
| **Security** | `https-dns-proxy`, `wpad-openssl`, `dnsmasq-full` |
| **Admin Tools** | `mc`, `nano`, `htop`, `luci-app-ttyd`, `usbutils` |

---

## 🛠 Installation

### Initial Flash (from Stock)
1.  Enter **U-Boot Web UI**: Hold the **Reset** button while powering on (hold for 10-15s).
2.  Set PC IP to `192.168.1.2`.
3.  Flash the `factory.bin` via `192.168.1.1`.

### Upgrade (from OpenWrt)
1.  Use the `sysupgrade.bin` file in **System -> Backup / Flash Firmware**.
2.  **Recommendation:** Uncheck "Keep settings" for the most stable transition to V2.

---

## ⚠️ Disclaimer
*Flashing custom firmware involves risks. The author is not responsible for any hardware damage. Always back up your Factory/EEPROM partition before flashing.*
