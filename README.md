# NetisWRT
# ImmortalWrt for Netis NX62 (The Ultimate Edition)
### All-in-One Powerhouse: VPN, NAS, Disk Tools & 5G Gateway

Custom **ImmortalWrt** build specifically optimized for the **Netis NX62** (Netcore N60 Pro), powered by the **MediaTek MT7986 (Filogic 820)** SoC. This "Ultimate" image is a feature-complete solution combining high-speed encryption, advanced storage management, and carrier-grade mobile broadband.

---

## 🌟 Key Capabilities

### 🛡️ Next-Gen VPN & Privacy
* **AmneziaWG (AWG):** Full native support for the anti-DPI WireGuard fork. Secure your tunnel against advanced filtering and deep packet inspection (DPI).
* **Encrypted DNS:** Integrated `https-dns-proxy` (DNS-over-HTTPS) to prevent ISP-level tracking and DNS hijacking.
* **Policy-Based Routing Ready:** Built with `dnsmasq-full` and `ipset` support for complex split-tunneling (e.g., routing specific domains through VPN).
* **Full Protocol Stack:** Built-in support for **PPPoE**, **L2TP**, and **Cloudflare DDNS**.

### 📶 4G/5G Mobile Broadband Gateway
* **ModemManager:** The modern industry standard for mobile connectivity. Manage 4G/5G modems (Quectel, Fibocom, Sierra, etc.) with a dedicated LuCI interface.
* **Wide Compatibility:** Includes drivers for MBIM, QMI, RNDIS, and CDC-Ether protocols.
* **USB 3.0 Optimization:** Stable power and data handling for high-speed modem connections.

### 💾 Ultimate Storage & NAS (Disk-Master)
* **Samba 4 NAS:** Turn your router into a high-speed file server for Windows, Linux, and macOS.
* **Complete Disk Utility Suite:** Includes `fdisk`, `gdisk`, and `luci-app-fdisk` for partitioning and formatting drives directly from the WebUI.
* **File System Mastery:** Kernel-level **NTFS3** (Paragon), **exFAT**, and **ext4** support. 
* **Maintenance Tools:** Includes `e2fsprogs`, `ntfs-3g-utils`, and `dosfstools` to repair or check disks without a PC.
* **Performance:** **UAS (USB Attached SCSI)** support for SSD speeds and `hd-idle` for disk longevity.

### ⚡ Networking & Hardware
* **Wi-Fi 6 (802.11ax):** Full WPA3-SAE support via `wpad-openssl` for maximum security and speed.
* **Hardware Monitoring:** `autocore` and `luci-app-statistics` for tracking CPU temperature, frequency, and real-time bandwidth.

---

## 📦 Included Packages

| Category | Key Packages |
| :--- | :--- |
| **Connectivity** | `modemmanager`, `luci-proto-ppp`, `ppp-mod-pppoe`, `xl2tpd`, `usb-modeswitch` |
| **VPN** | `luci-app-amneziawg`, `kmod-amneziawg`, `amneziawg-tools` |
| **NAS / Samba** | `luci-app-samba4`, `samba4-server`, `samba4-utils`, `luci-app-hd-idle` |
| **Disk Tools** | `fdisk`, `gdisk`, `luci-app-fdisk`, `e2fsprogs`, `ntfs-3g-utils`, `dosfstools` |
| **System** | `dnsmasq-full`, `https-dns-proxy`, `wpad-openssl`, `ip-full`, `luci-app-ttyd` |
| **Utilities** | `mc`, `nano`, `htop`, `curl`, `usbutils`, `luci-app-statistics` |

---

## 🛠 Installation

### 1. Initial Flash (from Stock Firmware)
1.  Enter **U-Boot Web UI** mode: Hold the **Reset** button while plugging in the power. Continue holding for 10-15 seconds.
2.  Set a static IP on your PC: `192.168.1.2` (Subnet: `255.255.255.0`).
3.  Open `192.168.1.1` in your browser.
4.  Upload the `factory.bin` image from this build.

### 2. Updating (from OpenWrt/ImmortalWrt)
1.  Navigate to **System -> Backup / Flash Firmware**.
2.  Upload the `sysupgrade.bin` file.
3.  **Note:** It is highly recommended to **uncheck** "Keep settings" to ensure all "Ultimate" features and new disk utilities are initialized correctly.

---

## ⚠️ Disclaimer
*Flashing custom firmware involves risks. The author is not responsible for any hardware damage. Ensure you have a backup of your device's original Factory/EEPROM partition before proceeding.*
