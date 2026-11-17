<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | Desktop Icon Sync" height="70" />
</a>

<br /><br />

[繁體中文](../../README.md) · [简体中文](README_zh-CN.md) · **English**

# Desktop Icon Sync

### Snapshot your desktop icon layout before reinstalling, changing resolution or tidying up

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com/robert820/desktop-icon-sync)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](../../LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-current-status)

</div>

---

## 📖 Overview

Save a snapshot of your desktop icon layout before reinstalling Windows, changing the screen resolution or tidying up. **Desktop Icon Sync** backs up and restores icon positions locally and can optionally sync snapshots to the private Google Drive app-data folder so you can keep them across your own devices.

It syncs icon-layout snapshots only, not the documents or files on your desktop.

---

## 📌 Current status

> In development (0.1.0). Windows XP is an experimental target; a successful cross-build does not prove runtime compatibility. No downloadable build has been released yet.

---

## ✨ Features

### 1. 💾 Multiple desktop-layout snapshots
- Create snapshots of icon positions and add notes so you can tell layouts from different times apart.

### 2. ↩️ Restore icon layout
- Sends the stored positions to Windows Explorer, matching icons by their displayed names. If the desktop contents or monitor setup changed, verify the snapshot manually first.

### 3. ☁️ Optional Google Drive sync
- After you set up a Google OAuth Desktop-app client and connect, snapshots sync to Drive's `appDataFolder` (only the `drive.appdata` scope is requested) on startup, every five minutes and after each new backup. In this first version, deletes and renames affect the local copy only.

### 4. 🔐 Local credential protection
- The OAuth client secret and refresh token are protected with Windows DPAPI in the local config file.

### 5. 🧾 Verified updates
- The updater compares the SHA-256 from the update manifest before installing; use only manifest hosts you trust.

### 6. 🌏 Multilingual UI
- Includes Traditional Chinese, Simplified Chinese, English and Japanese UI text.

---

## 💻 Scope & limitations

| Feature / environment | Requirement / status | Notes |
| :--- | :--- | :--- |
| Local backup & restore | Windows desktop | Restore matches icons by displayed name; check after desktop changes |
| Google Drive | Optional | You must create your own OAuth Desktop-app client and enable the Drive API |
| Sync behaviour | Automatic once connected | On startup, every five minutes and after a new backup; deletes/renames are local-only in this version |
| Windows XP | Experimental target | GUI, Explorer IPC, TLS/OAuth and updates still need VM validation |

---

## 🚀 Workflow

1. Launch the app and create a local snapshot while your icon layout is stable, with a recognisable note.
2. For cloud backup, create a Google Cloud OAuth **Desktop app** client, enable the Drive API, then connect from the app.
3. After reinstalling or changing monitors, pick a suitable snapshot to restore and check the result in Explorer.

---

## 📦 Download

No downloadable build has been released yet. Once released, it will be provided on the [Releases page](https://github.com/robert820/desktop-icon-sync/releases).

---

## 🖥️ Requirements

- **OS**: Windows desktop (XP is an experimental target)
- **Cloud sync (optional)**: your own Google OAuth Desktop-app client with the Drive API enabled
- **Runtime**: native Rust executable; no .NET or VC++ redistributable required

---

## ❓ FAQ

<details>
<summary><b>Does it back up my desktop files to Google Drive?</b></summary>

No. It syncs icon-layout snapshots only, not the documents or file contents on your desktop.

</details>

<details>
<summary><b>Will every icon return to its exact place after a restore?</b></summary>

Not necessarily. Restore matches icons by displayed name, so changes to the desktop contents or monitor layout can affect the result. Create a snapshot manually and verify the restore.

</details>

---

## 💬 Feedback & support

- 🐛 **Bug reports & feature requests**: please use the [Issues page](https://github.com/robert820/desktop-icon-sync/issues).
- 🌐 **DEI Tech official website**: [https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **Support & business inquiries**: please contact us through the official website.

---

## 📄 License

This software is released under a Proprietary Freeware license. See the [LICENSE](../../LICENSE) file for the full terms and disclaimers.

- Third-party components: this software uses Slint (Royalty-Free License), YY-Thunks (MIT) and several open-source Rust crates; see [THIRD_PARTY_NOTICES.md](../../THIRD_PARTY_NOTICES.md) for the notices.

<a href="https://slint.dev"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-dark.png">
  <img src="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-light.png" alt="Made with Slint" width="160">
</picture></a>
