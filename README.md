# The Android SysAdmin Vault: 173 Power User Tools

> **"Your phone is a pocket server, not a consumption device."**

![Status: Maintained](https://img.shields.io/badge/Status-Maintained-green?style=for-the-badge&logo=github)
![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge&logo=open-source-initiative)
![Platform: Android](https://img.shields.io/badge/Platform-Android-android?style=for-the-badge&logo=android)
![Root: Optional](https://img.shields.io/badge/Root-Optional-orange?style=for-the-badge&logo=su)
![Apps & Tools: 173](https://img.shields.io/badge/Apps_%26_Tools-173-purple?style=for-the-badge&logo=google-play)

This repository is a curated collection of the most powerful, non-root **and** root utilities for Android System Administrators, Developers, and Power Users. The goal is simple: **Total device control.**

These tools allow you to debug networks, manage packages, script automation, host servers, and harden security—all open source and verified.

## ⚠️ Disclaimer
*   **Power User Territory:** Some tools listed here (especially Root tools) can brick your device if misused. Always backup.
*   **FOSS Focus:** We prioritize Free and Open Source Software.

---

## 📚 Table of Contents
1. [The "Core" Toolkit](#1-the-core-toolkit)
2. [Package Management](#2-package-management)
3. [Root Authority & System](#3-root-authority--system)
4. [Network & Security](#4-network--security)
5. [Identity & Authentication](#5-identity--authentication)
6. [Communication & P2P](#6-communication--p2p)
7. [Development & Scripting](#7-development--scripting)
8. [Data Sovereignty & Office](#8-data-sovereignty--office)
9. [Hardware Hacking](#9-hardware-hacking)
10. [Privacy & De-Googling](#10-privacy--de-googling)
11. [Navigation & Maps](#11-navigation--maps)
12. [IoT & Home Automation](#12-iot--home-automation)
13. [The CLI Arsenal (Termux)](#13-the-cli-arsenal-termux)
14. [The Root Ecosystem](#14-the-root-ecosystem)
15. [Pocket Servers](#15-pocket-servers)
16. [Forensics & Reverse Engineering](#16-forensics--reverse-engineering)
17. [Advanced Termux Add-ons](#17-advanced-termux-add-ons)
18. [The Mega-Repos & Linux](#18-the-mega-repos--linux)
19. [The "Kill List" Script](#19-the-kill-list-script)
20. [Contribute](#20-contribute)

---

## 1. The "Core" Toolkit
*The foundation for system modification and package management (Non-Root friendly).*

- **[Shizuku](https://github.com/RikkaApps/Shizuku)**
  - **Why SysAdmin:** Acts as a bridge to allow apps to use system APIs directly via ADB, bypassing normal permission restrictions without root.
- **[Hail](https://github.com/aistra0528/Hail)**
  - **Why SysAdmin:** Freezes (disables) unwanted apps and background services on demand. Prevents bloatware from consuming RAM/Battery.
- **[App Manager](https://github.com/MuntashirAkon/AppManager)**
  - **Why SysAdmin:** The `htop` of Android apps. View activities, services, receivers, and signatures. Block trackers and modify permissions at a low level.
- **[App Ops](https://github.com/RikkaApps/AppOps)**
  - **Why SysAdmin:** Manages hidden permissions (AppOps) that the standard settings menu doesn't show, like "Run in Background" or "Clipboard Access".
- **[Inure App Manager](https://github.com/Hamza417/Inure)**
  - **Why SysAdmin:** A beautiful, highly technical application manager and debloater with terminal access and sensor analysis.
- **[KDE Connect](https://github.com/KDE/kdeconnect-android)**
  - **Why SysAdmin:** Seamless integration with Linux/Windows desktops. Shared clipboard, remote input, command execution, and file transfer over LAN.

---

## 2. Package Management
*Tools to install, update, and manage software sources outside the Play Store.*

- **[Obtainium](https://github.com/ImranR98/Obtainium)**
  - **Why SysAdmin:** Gets updates directly from GitHub/GitLab Releases pages. Bypasses app stores entirely for bleeding-edge FOSS tools.
- **[Neo Store](https://github.com/NeoApplications/Neo-Store)**
  - **Why SysAdmin:** Modern, feature-rich F-Droid client. Supports third-party repos, fast index syncing, and ignores updates for specific packages.
- **[Aurora Store](https://github.com/WhyOrean/AuroraStore)**
  - **Why SysAdmin:** Anonymous Google Play Store client. Download apps without a Google account and spoof device information.
- **[Droid-ify](https://github.com/Droid-ify/Droid-ify)**
  - **Why SysAdmin:** Material F-Droid client with a modern UI and quick repo syncing.

---

## 3. Root Authority & System
*Tools that require Root (Magisk/KernelSU) or Shizuku for deep system modification.*

- **[Magisk](https://github.com/topjohnwu/Magisk)**
  - **Why SysAdmin:** The standard for systemless rooting. Allows modification of the system partition without actually touching it.
- **[KernelSU](https://github.com/tiann/KernelSU)**
  - **Why SysAdmin:** Kernel-based root solution. Offers better stealth and control than user-space root solutions.
- **[SmartPack-Kernel Manager](https://github.com/SmartPack/SmartPack-Kernel-Manager)**
  - **Why SysAdmin:** The active fork of Kernel Adiutor. Tweak CPU governors, I/O schedulers, and GPU frequencies for performance or battery.
- **[AdAway](https://github.com/AdAway/AdAway)**
  - **Why SysAdmin:** System-level ad blocking using `hosts` file modification. Blocks ads in all apps, not just browsers.
- **[AFWall+](https://github.com/ukanth/afwall)**
  - **Why SysAdmin:** `iptables` frontend. Whitelist-based firewall to strictly control which apps can access data/WiFi.
- **[Canta](https://github.com/samolego/Canta)**
  - **Why SysAdmin:** Uninstall any app (including system bloatware) without root using Shizuku. Safer than manual ADB commands.
- **[SuperFreezZ](https://gitlab.com/SuperFreezZ/SuperFreezZ)**
  - **Why SysAdmin:** Lightweight background process freezer. Doesn't require accessibility services like Greenify; works via Shizuku or Root.
- **[OAndBackupX](https://github.com/machiav3lli/oandbackupx)**
  - **Why SysAdmin:** Powerful, open-source backup solution. Backs up apps + data to local storage or cloud. Neo Backup alternative.
- **[MatLog](https://github.com/plusCubed/matlog)**
  - **Why SysAdmin:** Real-time Logcat reader. Essential for debugging app crashes and system errors on the fly.

<details>
<summary><b>🔻 Click to expand 50+ more Root Tools</b></summary>

*   **[Neo Backup](https://github.com/NeoApplications/Neo-Backup)** - Open-source Titanium Backup alternative.
*   **[SD Maid SE](https://github.com/d4rken-org/sdmaid-se)** - System cleaner and database optimizer.
*   **[Termux:Boot](https://github.com/termux/termux-boot)** - Run scripts at device boot.
*   **[USB Mountr](https://github.com/streetwalrus/android_usb_msd)** - Turn your phone into a bootable USB drive for PC repair.
*   **[DriveDroid](https://softwarebakery.com/projects/drivedroid)** - Host ISO files as USB devices (requires kernel patching on newer Androids).
*   **[AccA](https://github.com/MatteCarra/AccA)** - Advanced Charging Controller GUI. Limit charging to 80% to prolong battery life.
*   **[CPU Info](https://github.com/kgv/cpu_info)** - Detailed hardware information (SoC, Ram, Sensors).

</details>

---

## 4. Network & Security
*Firewalls, packet sniffers, and encrypted DNS.*

### 🛡️ Defense & Analysis
- **[PCAPdroid](https://github.com/emanuele-f/PCAPdroid)**
  - **Why SysAdmin:** No-root packet capture (pcap) tool. Decrypts SSL/TLS traffic locally using a mitmproxy approach for debugging malicious app traffic.
- **[InviZible Pro](https://github.com/Gedsh/InviZible)**
  - **Why SysAdmin:** Comprehensive suite running Tor, I2P, and DNSCrypt simultaneously. Anonymizes traffic and bypasses censorship.
- **[TrackerControl](https://github.com/TrackerControl/tracker-control-android)**
  - **Why SysAdmin:** Monitors and blocks hidden data collection in apps. Visualizes where your data is going.
- **[OONI Probe](https://github.com/ooni/probe-android)**
  - **Why SysAdmin:** Measure internet censorship and speed. Detects blocked websites and middleboxes.
- **[Orbot](https://github.com/guardianproject/orbot-android)**
  - **Why SysAdmin:** The official Tor proxy. Routes traffic from specific apps or the entire device through the Tor network.
- **[RethinkDNS](https://github.com/celzero/rethink-app)**
  - **Why SysAdmin:** Granular firewall + DNS resolver. Block connections per app, per IP, or per country. View real-time connection logs.
- **[NetGuard](https://github.com/M66B/NetGuard)**
  - **Why SysAdmin:** Simple, battery-efficient firewall to block internet access for specific apps.
- **[Port Authority](https://github.com/aaronjwood/PortAuthority)**
  - **Why SysAdmin:** Fast port scanner and LAN host discovery tool. Essential for auditing local networks.
- **[OpenVPN for Android](https://github.com/schwabe/ics-openvpn)**
  - **Why SysAdmin:** The full-featured open source OpenVPN client. Supports complex configurations, tap/tun, and tasker integration.
- **[URLCheck](https://github.com/TrianguloY/URLCheck)**
  - **Why SysAdmin:** Intercepts link clicks to analyze/strip parameters (UTM tags) and scan via VirusTotal before opening in a browser.
- **[Network Tools](https://github.com/yitsoshi/Network-Tools)**
  - **Why SysAdmin:** Collection of network utilities like Ping, Traceroute, Port Scanner, DNS Lookup, and Whois.
- **[Intra](https://github.com/Jigsaw-Code/intra)**
  - **Why SysAdmin:** Protects against DNS manipulation and censorship using DNS-over-HTTPS.
- **[Key Attestation](https://github.com/vvb2060/KeyAttestation)**
  - **Why SysAdmin:** Verifies the cryptographic security chain of the device (TEE/StrongBox). Essential for checking device integrity.

<details>
<summary><b>🔻 Click to expand more Network Tools</b></summary>

*   **[WireGuard](https://github.com/WireGuard/wireguard-android)** - Fast, modern VPN tunnel.
*   **[Nebulo](https://github.com/Ch4t4r/Nebulo)** - DNS-over-HTTPS/TLS client with query logging.
*   **[WiFiAnalyzer](https://github.com/VREMSoftwareDevelopment/WiFiAnalyzer)** - Optimize channel selection and debug signal strength (Open Source).
*   **[Privacy Friendly WiFi Manager](https://github.com/SecUSo/privacy-friendly-wifi-manager)** - Schedule WiFi on/off based on location to prevent tracking.

</details>

---

## 5. Identity & Authentication
*Password management, 2FA, and keys.*

- **[KeePassDX](https://github.com/Kunzisoft/KeePassDX)**
  - **Why SysAdmin:** Material Design KeePass port. Offline password manager with support for keyfiles and YubiKey.
- **[Aegis Authenticator](https://github.com/beemdevelopment/Aegis)**
  - **Why SysAdmin:** The gold standard for 2FA. Encrypted backups, icon packs, custom grouping, and biometric unlock.
- **[Bitwarden](https://github.com/bitwarden/android)**
  - **Why SysAdmin:** Open source cloud password manager (can self-host with Vaultwarden). Essential for team credential sharing.
- **[OpenKeychain](https://github.com/open-keychain/open-keychain)**
  - **Why SysAdmin:** OpenPGP implementation for Android. Encrypt/decrypt files and emails, manage keys, and integrate with other apps.
- **[FreeOTP+](https://github.com/helloworld1/FreeOTPPlus)**
  - **Why SysAdmin:** Enhanced fork of FreeOTP. Supports exporting/importing settings, dark theme, and searching tokens.

---

## 6. Communication & P2P
*Secure, decentralized, and encrypted communication.*

- **[Session](https://github.com/oxen-io/session-android)**
  - **Why SysAdmin:** Private messenger with no metadata, no phone number required, and onion routing.
- **[Briar](https://github.com/briar/briar)**
  - **Why SysAdmin:** P2P messenger that works without internet (via Bluetooth/Wi-Fi). Ideal for off-grid comms.
- **[Molly](https://github.com/mollyim/mollyim-android)**
  - **Why SysAdmin:** Hardened fork of Signal with database encryption and Tor support.
- **[Element](https://github.com/element-hq/element-android)**
  - **Why SysAdmin:** Matrix client for decentralized, secure communication. Supports E2EE and self-hosting.

---

## 7. Development & Scripting
*Turn Android into a portable Linux workstation.*

### 💻 Terminal & Automation
- **[Termux](https://github.com/termux/termux-app)**
  - **Why SysAdmin:** Full Linux environment. Run `ssh`, `git`, `python`, `nmap`, and `vim` directly on the device.
- **[UserLAnd](https://github.com/CypherpunkArmory/UserLAnd)**
  - **Why SysAdmin:** Run full Linux distros (Ubuntu, Kali, Debian) on Android without root using PRoot.
- **[Linux Deploy](https://github.com/meefik/linuxdeploy)**
  - **Why SysAdmin:** (Root) Deploys full Linux distros in a chroot environment for near-native performance.
- **[HTTP Shortcuts](https://github.com/Waboodoo/HTTP-Shortcuts)**
  - **Why SysAdmin:** Trigger complex REST API calls via home screen shortcuts. Ideal for controlling IoT devices or webhooks.
- **[Acode](https://github.com/deadlyjack/Acode)**
  - **Why SysAdmin:** Lightweight, high-performance code editor with syntax highlighting and FTP/SFTP support.
- **[ConnectBot](https://github.com/connectbot/connectbot)**
  - **Why SysAdmin:** The standard SSH client. robust, supports pubkey auth and port forwarding.
- **[SimpleUsbTerminal](https://github.com/kai-morich/SimpleUsbTerminal)**
  - **Why SysAdmin:** Connect to serial devices (routers, switches, Arduinos) via USB OTG. Essential for hardware debugging.
- **[Hacker's Keyboard](https://github.com/klausw/hackerskeyboard)**
  - **Why SysAdmin:** Provides a full 5-row PC keyboard layout with Ctrl, Alt, Esc, and Arrow keys. Critical for Termux/SSH usage.
- **[MGit](https://github.com/maks/MGit)**
  - **Why SysAdmin:** Full-featured Git client. Clone repos, commit changes, and push to remotes on the go.
- **[GitTouch](https://github.com/GitTouch/GitTouch)**
  - **Why SysAdmin:** Clean client for GitHub, GitLab, and Bitbucket. View issues, PRs, and code with syntax highlighting.
- **[GitNex](https://github.com/GitNex/GitNex)**
  - **Why SysAdmin:** Open-source Android client for Gitea/Forgejo. Manage issues, repositories, and organizations.

---

## 8. Data Sovereignty & Office
*File management, synchronization, and self-hosting clients.*

### 💾 Storage & Sync
- **[LocalSend](https://github.com/localsend/localsend)**
  - **Why SysAdmin:** AirDrop alternative. Open-source, local-only file transfer between Android, iOS, Windows, and Linux. No external servers.
- **[Syncthing](https://github.com/syncthing/syncthing-android)**
  - **Why SysAdmin:** Decentralized, continuous file synchronization. Keep your Keepass database or notes synced across devices without a cloud provider.
- **[Round Sync](https://github.com/newhinton/Round-Sync)**
  - **Why SysAdmin:** Rclone GUI for Android. Encrypt/Decrypt and mount cloud storage (S3, GDrive, Dropbox) locally.
- **[Nextcloud](https://github.com/nextcloud/android)**
  - **Why SysAdmin:** Official client for self-hosted Nextcloud instances. Auto-upload photos, sync files, and manage cloud data.
- **[DAVx5](https://github.com/bitfireAT/davx5-ose)**
  - **Why SysAdmin:** Syncs Contacts, Calendars, and Tasks via CalDAV/CardDAV. Essential for de-googling and using Nextcloud/Radicale.
- **[Joplin](https://github.com/laurent22/joplin)**
  - **Why SysAdmin:** Open source note-taking capable of syncing with Nextcloud/S3. End-to-end encrypted by default.
- **[Standard Notes](https://github.com/standardnotes/app)**
  - **Why SysAdmin:** A secure and private notes app with end-to-end encryption.
- **[Logseq](https://github.com/logseq/logseq)**
  - **Why SysAdmin:** Privacy-first, open-source knowledge base. Works with local Markdown files, supports properties and bidirectional linking.
- **[Material Files](https://github.com/zhanghai/MaterialFiles)**
  - **Why SysAdmin:** Clean, root-capable file manager. Supports SMB, SFTP, and FTP servers.
- **[Fossify File Manager](https://github.com/FossifyOrg/File-Manager)**
  - **Why SysAdmin:** Fork of Simple File Manager. Clean, privacy-focused, and supports hidden files/root access navigation.
- **[Seal](https://github.com/JunkFood02/Seal)**
  - **Why SysAdmin:** GUI for `yt-dlp`. Downloads video/audio from thousands of sites with metadata control and format selection.
- **[DiskUsage](https://github.com/IvanVolosyuk/diskusage)**
  - **Why SysAdmin:** Treemap visualization of storage. Instantly identify which directories or cache files are eating your space.
- **[RustDesk](https://github.com/rustdesk/rustdesk)**
  - **Why SysAdmin:** Open-source remote desktop client (TeamViewer alternative). Self-hostable server for full control.
- **[Librera](https://github.com/foobnix/LibreraReader)**
  - **Why SysAdmin:** Versatile document reader (PDF, EPUB, MOBI, etc.) with text-to-speech and extensive customization.
- **[MJ PDF](https://github.com/mudlej/MjPdfReader)**
  - **Why SysAdmin:** Minimalist, fast, and open-source PDF viewer.
- **[ImagePipe](https://github.com/kaangiray26/ImagePipe)**
  - **Why SysAdmin:** Modify images before sharing: resize, crop, and remove EXIF tags to protect privacy.
- **[Scrambled Exif](https://github.com/Fynn-F/ScrambledExif)**
  - **Why SysAdmin:** Removes EXIF data from pictures before sharing them.

---

## 9. Hardware Hacking
*Sensors, Radio, and WiFi analysis.*

### 📡 Signals
- **[WiGLE](https://github.com/wiglenet/wigle-wifi-wardriving)**
  - **Why SysAdmin:** Wardriving tool. Maps and logs WiFi/Bluetooth networks to a local database.
- **[Phyphox](https://github.com/phyphox/phyphox-android)**
  - **Why SysAdmin:** Access raw sensor data (Accelerometer, Gyroscope, Magnetometer). Useful for hardware diagnostics and physics experiments.
- **[GPSTest](https://github.com/barbeau/gpstest)**
  - **Why SysAdmin:** Detailed GNSS/GPS view. Check satellite fix status, accuracy, and raw NMEA data.
- **[Binary Eye](https://github.com/markusfisch/BinaryEye)**
  - **Why SysAdmin:** Pure, ad-free barcode/QR scanner. Reveals the raw payload text immediately without auto-executing malicious links.
- **[SatStat](https://gitlab.com/mvglasow/satstat)**
  - **Why SysAdmin:** Displays status of GPS, GLONASS, Galileo, etc., and sensor data. Useful for diagnosing location issues.

---

## 10. Privacy & De-Googling
*FOSS alternatives to proprietary spyware.*

### 👁️ Privacy
- **[Aurora Store](https://github.com/WhyOrean/AuroraStore)**
  - **Why SysAdmin:** Anonymous Google Play Store client. Download apps without a Google account and spoof device information.
- **[Neo Store](https://github.com/NeoApplications/Neo-Store)**
  - **Why SysAdmin:** Modern, feature-rich F-Droid client. Supports third-party repos, updates, and fast package installation.
- **[Insular](https://gitlab.com/secure-system/Insular)**
  - **Why SysAdmin:** Fork of Island. Leverages Android's "Work Profile" to sandbox untrusted apps or run dual instances of apps (e.g., WhatsApp).
- **[Shelter](https://github.com/PeterCxy/Shelter)**
  - **Why SysAdmin:** Isolates big-tech apps in a work profile. Can "freeze" heavy apps when not in use.
- **[K-9 Mail](https://github.com/thunderbird/thunderbird-android)**
  - **Why SysAdmin:** Powerful email client with OpenPGP encryption support.
- **[FairEmail](https://github.com/M66B/FairEmail)**
  - **Why SysAdmin:** Advanced email client focusing on privacy. Displays full message headers, tracking pixel protection, and unlimited accounts.
- **[Fossify Gallery](https://github.com/FossifyOrg/Gallery)**
  - **Why SysAdmin:** Fork of Simple Gallery. No internet permission required, privacy-focused media viewer.
- **[NewPipe](https://github.com/TeamNewPipe/NewPipe)**
  - **Why SysAdmin:** YouTube frontend. No ads, background play, and download capability without a Google account.
- **[Cromite](https://github.com/uazo/cromite)**
  - **Why SysAdmin:** Chromium fork with built-in adblocking and privacy patches (Bromite successor).
- **[Mull](https://github.com/DivestOS/Mull-Fenix)**
  - **Why SysAdmin:** Privacy-hardened browser based on Mozilla Firefox.
- **[Tor Browser](https://gitlab.torproject.org/tpo/applications/tor-browser)**
  - **Why SysAdmin:** The official browser for Tor, providing access to the Tor network and onion services.

---

## 11. Navigation & Maps
*Offline maps and navigation tools.*

- **[OsmAnd+](https://github.com/osmandapp/OsmAnd)**
  - **Why SysAdmin:** Offline maps and navigation using OpenStreetMap data. Powerful rendering and routing capabilities.
- **[Organic Maps](https://github.com/organicmaps/organicmaps)**
  - **Why SysAdmin:** Privacy-focused offline maps. Fast, lightweight, and easy to use.

---

## 12. IoT & Home Automation
*Control your smart home and devices.*

- **[Home Assistant](https://github.com/home-assistant/android)**
  - **Why SysAdmin:** Official app for Home Assistant. Control all your smart devices from a single, open-source platform.
- **[Gadgetbridge](https://codeberg.org/Freeyourgadget/Gadgetbridge)**
  - **Why SysAdmin:** Connects your pebble, mi band, amazfit and other devices to your mobile phone without the vendor's closed source application.

---

## 13. The CLI Arsenal (Termux)
*Install these via `pkg install <name>` inside Termux. This list turns your shell into a weapon.*

<details>
<summary><b>🔻 Click to expand 50+ CLI Tools</b></summary>

### Network Analysis & Transfer
*   `nmap` - Network exploration tool and security / port scanner.
*   `iperf3` - Perform network throughput tests.
*   `rsync` - Fast remote file copy program (essential for backups).
*   `curl` - Command line tool for transferring data with URLs.
*   `wget` - Network downloader.
*   `aria2` - High speed download utility with multi-protocol support.
*   `openssh` - Secure shell client and server (sshd).
*   `netcat-openbsd` - TCP/IP swiss army knife (`nc`).
*   `dnsutils` - Bind tools including `dig` and `nslookup`.
*   `whois` - Domain whois client.
*   `tracepath` - Traces path to a network host discovering MTU.
*   `mtr` - Network diagnostic tool (ping + traceroute).
*   `tcpdump` - Command-line packet analyzer.
*   `tshark` - Terminal-based Wireshark.
*   `masscan` - TCP port scanner, spews SYN packets asynchronously.
*   `socat` - Multipurpose relay (SOcket CAT).

### Development & Scripting
*   `git` - Distributed version control system.
*   `python` - Python 3 programming language.
*   `nodejs` - JavaScript runtime.
*   `golang` - Go programming language.
*   `rust` - Rust programming language.
*   `ruby` - Ruby programming language.
*   `php` - PHP scripting language.
*   `lua` - Lua scripting language.
*   `clang` - C language family frontend for LLVM.
*   `make` - Build automation tool.
*   `vim` - Vi IMproved, a programmer's text editor.
*   `neovim` - Hyperextensible Vim-based text editor.
*   `tmux` - Terminal multiplexer (run background sessions).
*   `jq` - Lightweight and flexible command-line JSON processor.
*   `ansible` - Automation platform (requires python).

### System & Forensics
*   `htop` - Interactive process viewer.
*   `btop` - Resource monitor that shows usage and stats.
*   `ncdu` - Disk usage analyzer with an ncurses interface.
*   `proot-distro` - Install Linux distributions (Ubuntu, Debian, Kali, Arch) inside Termux.
*   `ffmpeg` - Record, convert and stream audio and video.
*   `yt-dlp` - Command-line video downloader (YouTube-DL fork).
*   `imagemagick` - Edit, compose, or convert bitmap images.
*   `fzf` - Command-line fuzzy finder.
*   `ripgrep` - Line-oriented search tool (`rg`), faster than grep.
*   `bat` - A `cat` clone with syntax highlighting and Git integration.
*   `eza` - A modern, maintained replacement for `ls`.
*   `fd` - A simple, fast and user-friendly alternative to `find`.
*   `android-tools` - Contains `adb` and `fastboot` (yes, you can run ADB from Termux!).
*   `strace` - Diagnostic, debugging and instructional userspace utility.
*   `ltrace` - Library call tracer.
*   `gdb` - The GNU Debugger.

</details>

---

## 14. The Root Ecosystem
*Modules for Magisk, KernelSU, and Zygisk. These reshape the OS itself.*

- **[LSPosed](https://github.com/LSPosed/LSPosed)**
  - **Why SysAdmin:** The Xposed Framework successor. Hooks into system processes to modify behavior on the fly without touching APKs.
- **[Shamiko](https://github.com/LSPosed/Shamiko)**
  - **Why SysAdmin:** Hides Zygisk (Root) traces from apps that detect it. Essential for banking/enterprise apps.
- **[PlayIntegrityFix](https://github.com/chiteroman/PlayIntegrityFix)**
  - **Why SysAdmin:** Fixes Google's Play Integrity API (SafetyNet) to allow running security-sensitive apps on rooted devices.
- **[Tricky Store](https://github.com/5ec1cff/TrickyStore)**
  - **Why SysAdmin:** Uses a hardware-backed keystore spoofing technique to pass strong integrity checks on TEE-broken devices.
- **[Zygisk-Assistant](https://github.com/snake-4/Zygisk-Assistant)**
  - **Why SysAdmin:** Hides root for KernelSU, Magisk, and APatch. Works alongside other hiding modules for maximum stealth.
- **[Bootloop Saver](https://github.com/HuskyDG/BootloopSaver)**
  - **Why SysAdmin:** Automatically disables all Magisk modules if the device fails to boot, preventing a factory reset.

---

## 15. Pocket Servers
*Turn your device into a file, web, or media host.*

- **[Primitive FTPd](https://github.com/primftpd/primftpd)**
  - **Why SysAdmin:** Simple, robust SFTP and FTP server. Supports public key authentication for secure automated transfers.
- **[Alist](https://github.com/alist-org/alist)**
  - **Why SysAdmin:** A file list program that aggregates multiple storages (S3, GDrive, Local) into a single WebDAV/HTTP interface. Runs via Termux.
- **[Material Files](https://github.com/zhanghai/MaterialFiles)**
  - **Why SysAdmin:** Contains a built-in FTP server to quickly share local storage files over WiFi.

---

## 16. Forensics & Reverse Engineering
*Tools for analyzing files, firmware, and binaries.*

<details>
<summary><b>🔻 Click to expand Forensics Tools</b></summary>

*   `radare2` - (Termux) Advanced command-line hex editor, disassembler and debugger.
*   `binwalk` - (Termux) Firmware analysis tool.
*   `sleuthkit` - (Termux) Library and collection of command line tools for investigating disk images.
*   `exiftool` - (Termux) Read, write and edit metadata.
*   `hexedit` - (Termux) View and edit files in hexadecimal or in ASCII.
*   `testdisk` - (Termux) Recover lost partitions and fix boot sectors.
*   `photorec` - (Termux) File data recovery software designed to recover lost files including video, documents and archives.
*   `steghide` - (Termux) Steganography program that is able to hide data in various kinds of image- and audio-files.

</details>

---

## 17. Advanced Termux Add-ons
*Official plugins to extend Termux functionality.*

- **[Termux:API](https://github.com/termux/termux-api)**
  - **Why SysAdmin:** Exposes Android API (Battery, Camera, SMS, Location) to CLI scripts.
- **[Termux:Widget](https://github.com/termux/termux-widget)**
  - **Why SysAdmin:** Run scripts directly from the home screen launcher without opening the terminal.
- **[Termux:Boot](https://github.com/termux/termux-boot)**
  - **Why SysAdmin:** Execute scripts automatically when the device boots up.
- **[Termux:Styling](https://github.com/termux/termux-styling)**
  - **Why SysAdmin:** Customize the terminal font and color scheme for better readability.

---

## 18. The Mega-Repos & Linux
*Access to 5,000+ Verified FOSS Apps. Add these to your F-Droid client.*

- **[IzzyOnDroid](https://apt.izzysoft.de/fdroid/index.php)**
  - **Why SysAdmin:** A massive repository of FOSS apps that aren't yet on the official F-Droid repo. Contains bleeding-edge and niche tools.
- **[DivestOS Official](https://divestos.org/)**
  - **Why SysAdmin:** Highly vetted repo containing privacy-hardened versions of popular apps (Mull, Mulch, Hypatia).
- **[Nix-on-Droid](https://github.com/nix-community/nix-on-droid)**
  - **Why SysAdmin:** Installs the Nix package manager on Android. Gives access to the vast Nixpkgs collection (thousands of Linux tools) without root.
- **[Kali NetHunter Store](https://store.nethunter.com/)**
  - **Why SysAdmin:** The official app store for Kali NetHunter. Provides specialized security research, pentesting, and forensics tools.
- **[Guardian Project](https://guardianproject.info/)**
  - **Why SysAdmin:** Focused on privacy and security apps (Orbot, Onion Browser, Haven) for journalists and activists.

---

## 19. The "Kill List" Script

This section contains ADB commands to debloat common OEM garbage without root.
**Warning:** Verify package names before running.

<details>
<summary><b>🔻 Click to expand the Kill List</b></summary>

### How to use
1. Connect via ADB: `adb shell`
2. Copy and paste the relevant block.

#### Generic / Google
```bash
pm uninstall --user 0 com.google.android.apps.tachyon # Duo
pm uninstall --user 0 com.google.android.music # Google Music
pm uninstall --user 0 com.google.android.videos # Play Movies
pm uninstall --user 0 com.google.android.apps.subscriptions.red # Google One
```

#### Xiaomi (MIUI/HyperOS)
```bash
pm uninstall --user 0 com.miui.daemon # MIUI Daemon (Analytics)
pm uninstall --user 0 com.miui.analytics
pm uninstall --user 0 com.miui.msa.global # MSA (Main Ad Service)
pm uninstall --user 0 com.xiaomi.midrop # ShareMe
pm uninstall --user 0 com.miui.cloudservice
```

#### Facebook / Meta
```bash
pm uninstall --user 0 com.facebook.katana # App
pm uninstall --user 0 com.facebook.system # Installer
pm uninstall --user 0 com.facebook.appmanager # App Manager
pm uninstall --user 0 com.facebook.services
```

#### Samsung
```bash
pm uninstall --user 0 com.samsung.android.app.tips
pm uninstall --user 0 com.samsung.android.aremoji
pm uninstall --user 0 com.sec.android.app.sbrowser # Samsung Internet
```

</details>

---

## 20. Contribute

This vault is maintained by the open source community. We want **high quality, unabandoned, FOSS** tools.

1.  Fork the repo.
2.  Add your tool to the appropriate category.
3.  **Strict Requirement:** You must include a "Why SysAdmin:" bullet point explaining the technical utility.
4.  Submit a Pull Request.

---
*Maintained with ❤️ by the Android SysAdmin Community.*
