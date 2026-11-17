<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | Desktop Icon Sync" height="70" />
</a>

<br /><br />

**繁體中文** · [简体中文](docs/readme/README_zh-CN.md) · [English](docs/readme/README_en.md)

# 桌面圖示備份與同步

### 重灌、換解析度或整理桌面前，先保存桌面圖示排列

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com/robert820/desktop-icon-sync)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-目前狀態)

</div>

---

## 📖 軟體簡介

重灌 Windows、更換螢幕解析度或整理桌面前，先保存桌面圖示排列快照。**Desktop Icon Sync** 可在本機備份與還原圖示位置，並可選擇同步到 Google Drive 私人應用程式資料夾，方便在自己的裝置間保存快照。

工具同步的是「圖示配置快照」，不是桌面上的文件或檔案內容。

---

## 📌 目前狀態

> 開發中（0.1.0）。Windows XP 為實驗性目標；交叉編譯成功不代表執行相容。尚未發布可下載的執行檔。

---

## ✨ 功能介紹

### 1. 💾 多份桌面配置快照
- 為桌面圖示位置建立快照，並可加入備份註記，方便辨認不同時期的配置。

### 2. ↩️ 還原圖示排列
- 將快照中的圖示位置送給 Windows Explorer，依圖示顯示名稱比對後還原；桌面內容或顯示器配置改變時，建議先手動確認快照。

### 3. ☁️ 選用 Google Drive 同步
- 完成 Google OAuth 桌面應用程式設定並連線後，快照同步到 Drive 的 `appDataFolder`（僅請求 `drive.appdata` 範圍）；啟動時、每五分鐘及新增備份後同步，首版的刪除與重新命名僅作用於本機。

### 4. 🔐 本機憑證保護
- OAuth 用戶端密碼與 refresh token 以 Windows DPAPI 保護後存放於本機設定檔。

### 5. 🧾 更新檔雜湊驗證
- 更新流程在安裝前比對更新清單中的 SHA-256；僅使用您信任的更新清單主機。

### 6. 🌏 多語介面
- 包含繁體中文、簡體中文、英文與日文介面文字。

---

## 💻 支援範圍與限制

| 功能／環境 | 需求或狀態 | 備註 |
| :--- | :--- | :--- |
| 本機備份與還原 | Windows 桌面 | 還原依圖示顯示名稱比對；桌面變動後請先檢查 |
| Google Drive | 選用 | 需自行建立 OAuth Desktop app 用戶端並啟用 Drive API |
| 同步行為 | 連線後自動同步 | 啟動時、每五分鐘及新增備份後；首版刪除與重新命名僅作用於本機 |
| Windows XP | 實驗性目標 | GUI、Explorer IPC、TLS／OAuth 與更新仍待 VM 驗證 |

---

## 🚀 使用流程

1. 啟動程式，在桌面圖示排列穩定時建立一份本機快照，並加上容易辨認的註記。
2. 如需雲端備份，先在 Google Cloud 建立 OAuth **Desktop app** 用戶端並啟用 Drive API，再依程式設定連線。
3. 重灌或調整顯示器後，選擇合適快照進行還原，並檢查 Explorer 顯示結果。

---

## 📦 下載與使用說明

目前尚未發布可下載的執行檔；發布後將提供於本專案的 [Releases 頁面](https://github.com/robert820/desktop-icon-sync/releases)。

---

## 🖥️ 系統與環境需求

- **作業系統**：Windows 桌面環境（XP 為實驗性目標）
- **雲端同步（選用）**：自行建立的 Google OAuth Desktop app 用戶端，並啟用 Drive API
- **執行環境**：原生 Rust 執行檔，無須額外安裝 .NET 或 VC++ 可轉發套件

---

## ❓ 常見問題 (FAQ)

<details>
<summary><b>這個工具會把桌面檔案也備份到 Google Drive 嗎？</b></summary>

不會。工具同步的是桌面圖示配置快照，不是桌面上的文件或檔案內容。

</details>

<details>
<summary><b>還原後所有圖示一定會回到原位置嗎？</b></summary>

不一定。還原會依圖示顯示名稱比對，桌面內容或螢幕配置變動可能影響結果。請先手動建立快照並確認還原結果。

</details>

---

## 💬 問題反饋與支援

- 🐛 **錯誤回報與功能建議**：歡迎至本專案的 [Issues 頁面](https://github.com/robert820/desktop-icon-sync/issues) 提出。
- 🌐 **得翼科技官方網站**：[https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **技術支援與商務洽詢**：請透過官方網站聯繫我們。

---

## 📄 授權條款 (License)

本軟體採用專有免費軟體授權（Proprietary Freeware），完整授權規範、使用條款與免責聲明請參閱 [LICENSE](LICENSE) 檔案。

- 第三方元件：本軟體使用 Slint（Royalty-Free License）、YY-Thunks（MIT）與多個開源 Rust 套件，授權聲明請見 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

<a href="https://slint.dev"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-dark.png">
  <img src="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-light.png" alt="Made with Slint" width="160">
</picture></a>
