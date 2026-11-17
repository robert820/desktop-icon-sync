<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | Desktop Icon Sync" height="70" />
</a>

<br /><br />

[繁体中文](../../README.md) · **简体中文** · [English](README_en.md)

# 桌面图标备份与同步

### 重装、换分辨率或整理桌面前，先保存桌面图标排列

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com/robert820/desktop-icon-sync)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](../../LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-目前状态)

</div>

---

## 📖 软件简介

重装 Windows、更换屏幕分辨率或整理桌面前，先保存桌面图标排列快照。**Desktop Icon Sync** 可在本机备份与还原图标位置，并可选择同步到 Google Drive 私人应用程序文件夹，方便在自己的设备间保存快照。

工具同步的是「图标配置快照」，不是桌面上的文档或文件内容。

---

## 📌 目前状态

> 开发中（0.1.0）。Windows XP 为实验性目标；交叉编译成功不代表运行兼容。尚未发布可下载的运行档。

---

## ✨ 功能介绍

### 1. 💾 多份桌面配置快照
- 为桌面图标位置创建快照，并可加入备份注记，方便辨认不同时期的配置。

### 2. ↩️ 还原图标排列
- 将快照中的图标位置送给 Windows Explorer，依图标显示名称比对后还原；桌面内容或显示器配置改变时，建议先手动确认快照。

### 3. ☁️ 选用 Google Drive 同步
- 完成 Google OAuth 桌面应用程序设置并连接后，快照同步到 Drive 的 `appDataFolder`（仅请求 `drive.appdata` 范围）；启动时、每五分钟及添加备份后同步，首版的删除与重命名仅作用于本机。

### 4. 🔐 本机凭证保护
- OAuth 用户端密码与 refresh token 以 Windows DPAPI 保护后存放于本机设置档。

### 5. 🧾 更新档哈希验证
- 更新流程在安装前比对更新清单中的 SHA-256；仅使用您信任的更新清单主机。

### 6. 🌏 多语接口
- 包含繁体中文、简体中文、英文与日文接口文本。

---

## 💻 支持范围与限制

| 功能／环境 | 需求或状态 | 备注 |
| :--- | :--- | :--- |
| 本机备份与还原 | Windows 桌面 | 还原依图标显示名称比对；桌面变动后请先检查 |
| Google Drive | 选用 | 需自行创建 OAuth Desktop app 用户端并激活 Drive API |
| 同步行为 | 连接后自动同步 | 启动时、每五分钟及添加备份后；首版删除与重命名仅作用于本机 |
| Windows XP | 实验性目标 | GUI、Explorer IPC、TLS／OAuth 与更新仍待 VM 验证 |

---

## 🚀 使用流程

1. 启动程序，在桌面图标排列稳定时创建一份本机快照，并加上容易辨认的注记。
2. 如需云端备份，先在 Google Cloud 创建 OAuth **Desktop app** 用户端并激活 Drive API，再依程序设置连接。
3. 重装或调整显示器后，选择合适快照进行还原，并检查 Explorer 显示结果。

---

## 📦 下载与使用说明

目前尚未发布可下载的运行档；发布后将提供于本项目的 [Releases 页面](https://github.com/robert820/desktop-icon-sync/releases)。

---

## 🖥️ 系统与环境需求

- **操作系统**：Windows 桌面环境（XP 为实验性目标）
- **云端同步（选用）**：自行创建的 Google OAuth Desktop app 用户端，并激活 Drive API
- **运行环境**：原生 Rust 运行档，无须额外安装 .NET 或 VC++ 可转发套件

---

## ❓ 常见问题 (FAQ)

<details>
<summary><b>这个工具会把桌面文件也备份到 Google Drive 吗？</b></summary>

不会。工具同步的是桌面图标配置快照，不是桌面上的文档或文件内容。

</details>

<details>
<summary><b>还原后所有图标一定会回到原位置吗？</b></summary>

不一定。还原会依图标显示名称比对，桌面内容或屏幕配置变动可能影响结果。请先手动创建快照并确认还原结果。

</details>

---

## 💬 问题反馈与支持

- 🐛 **错误回报与功能建议**：欢迎至本项目的 [Issues 页面](https://github.com/robert820/desktop-icon-sync/issues) 提出。
- 🌐 **得翼科技官方网站**：[https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **技术支持与商务洽询**：请通过官方网站联系我们。

---

## 📄 授权条款 (License)

本软件采用专有免费软件授权（Proprietary Freeware），完整授权规范、使用条款与免责声明请参阅 [LICENSE](../../LICENSE) 文件。

- 第三方组件：本软件使用 Slint（Royalty-Free License）、YY-Thunks（MIT）与多个开源 Rust 套件，授权声明请见 [THIRD_PARTY_NOTICES.md](../../THIRD_PARTY_NOTICES.md)。

<a href="https://slint.dev"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-dark.png">
  <img src="https://raw.githubusercontent.com/slint-ui/slint/master/logo/MadeWithSlint-logo-light.png" alt="Made with Slint" width="160">
</picture></a>
