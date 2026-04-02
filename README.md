# NetisWRT
ImmortalWrt for Netis NX62 (Netcore N60 Pro)
High-Performance Custom Build: NAS, VPN, and 5G/LTE Ready

This repository contains a custom ImmortalWrt build specifically optimized for the Netis NX62 (hardware clone of Netcore N60 Pro), powered by the MediaTek MT7986 (Filogic 830) SoC.

This firmware is designed for power users who need a robust networking hub that combines high-speed VPN capabilities, NAS-grade storage features, and reliable mobile broadband failover.

🚀 Key Features

🛡️ Advanced VPN & Privacy

AmneziaWG (AWG): Integrated support for the modified WireGuard protocol, designed to bypass DPI (Deep Packet Inspection) and VPN blocks. Includes LuCI interface.

Encrypted DNS: https-dns-proxy (DNS-over-HTTPS) to prevent ISP DNS hijacking and snooping.

Split Tunneling Ready: Built with dnsmasq-full and ipset support for advanced policy-based routing.

Legacy Support: Full support for PPPoE, L2TP (xl2tpd), and Cloudflare DDNS.

📂 NAS & Media Server Capabilities

High-Speed Storage: USB 3.0 support with UAS (USB Attached SCSI) for maximum throughput on external SSDs/HDDs.

Samba 4 Server: Windows-compatible file sharing with wsdd2 for network discovery on Windows 10/11.

Apple Time Machine: Fully compatible with macOS backups via avahi (mDNS) and Samba 4.

NFS v3/v4: Kernel-level NFS server for high-performance sharing with Linux clients and media players.

Modern File Systems: High-performance NTFS3 (Paragon driver), exFAT, and ext4 support.

📶 Mobile Broadband (4G/5G)

ModemManager: The modern standard for mobile broadband. Supports 4G/5G modems (Quectel, Fibocom, etc.) via MBIM, QMI, and RNDIS.

Carrier Grade Performance: Includes usb-modeswitch and serial drivers for maximum modem compatibility.

🛠️ Hardware & Monitoring

Hardware Optimization: SoC temperature monitoring and frequency scaling via autocore.

Full LED/Button Support: Proper mapping for the NX62 LEDs (lp5523) and physical buttons.

Real-time Statistics: luci-app-statistics with CPU, RAM, and Network usage graphing.

Built-in Tools: Midnight Commander (mc), htop, nano, and ttyd (Web-based Terminal).

📦 Detailed Package List
Category	Included Packages
System Core	autocore, kmod-phy-aquantia, kmod-leds-lp5523, kmod-gpio-button-hotplug
Networking	dnsmasq-full, ppp, ppp-mod-pppoe, xl2tpd, https-dns-proxy, ip-full
VPN	kmod-amneziawg, amneziawg-tools, luci-app-amneziawg, luci-app-ddns
Storage/NAS	samba4-server, nfs-kernel-server, avahi-dbus-daemon, wsdd2, kmod-usb-storage-uas
File Systems	kmod-fs-ntfs3, kmod-fs-exfat, kmod-fs-vfat, block-mount
USB/Modem	modemmanager, usb-modeswitch, kmod-usb-net-cdc-mbim, kmod-usb-net-qmi-wwan
Interface	luci-ssl, luci-i18n-base-ru, luci-app-ttyd, luci-app-statistics
Utilities	openssl-util, mc, htop, nano, curl
🛠 Installation
Initial Flash (from Stock Firmware)

Enter U-Boot Recovery Mode by holding the Reset button while powering on the device.

Set your computer's IP to 192.168.1.2.

Access 192.168.1.1 via browser and upload the factory.bin image.

Note: It is highly recommended to follow the OpenWrt Layout (MTD write) guide to unlock the full 128MB flash capacity.

Update (from OpenWrt/ImmortalWrt)

Navigate to System -> Backup / Flash Firmware.

Upload the sysupgrade.bin file.

Uncheck "Keep settings" if moving from a different branch/build to avoid configuration conflicts.

⚠️ Disclaimer
Use this firmware at your own risk. The authors are not responsible for any damage or bricked devices. Ensure you have a backup of your original calibration/factory partitions.
