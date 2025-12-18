# Supernote Tools - 語言包安裝器

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**專為 Supernote 墨水屏設備設計的手寫識別語言包安裝工具**

[English](./README.md) | [简体中文](./README_ZH-CN.md) | 繁體中文 | [日本語](./README_JA.md) | [한국어](./README_KO.md) | [Deutsch](./README_DE.md)

---

## 📖 項目簡介

Supernote Tools 是一款專為 Supernote 墨水屏設備開發的**離線語言包安裝器**，幫助用戶在設備本地直接安裝 MyScript 手寫識別語言包，無需聯網即可完成安裝，支持 **66種語言** 的手寫識別功能。

### ✨ 主要特性

- 📴 **離線安裝**：無需聯網，直接在設備上安裝語言包
- 🌍 **多語言支持**：支持66種語言的手寫識別
- 📦 **雙版本選擇**：提供 Lite（精簡版）和 Standard（標準版）兩種語言包
- 🚀 **簡單易用**：圖形化界面，一鍵安裝
- 💾 **智能管理**：自動檢測和覆蓋已有語言包
- ⚡ **快速安裝**：幾秒鐘即可完成安裝

### 🎯 適用設備

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 下載安裝

### 下載應用

從 [Releases](../../releases) 頁面下載最新版本的 `SupernoteTools.apk` 文件。

### 安裝到設備

> ⚠️ **重要提示**：Supernote 設備默認無法直接安裝第三方 APK 應用，需要通過 ADB（Android Debug Bridge）工具進行側載安裝。

#### 安裝步驟概述

**第一步：在 Supernote 上啟用側載功能**
1. 打開 Supernote 的 **設置**
2. 進入 **安全和隱私**
3. 啟用 **側載（Sideload）** 選項

**第二步：連接設備到電腦**
1. 使用 USB 數據線將 Supernote 連接到電腦
2. 如果設備上出現提示，點擊 **確定** 允許連接

**第三步：使用 ADB 安裝 APK**

根據您的操作系統選擇對應的方法：

<details>
<summary><b>Windows 用戶</b></summary>

1. 從 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 項目下載 `platform-tools-latest-windows.zip` 並解壓到 `C:\adb`

2. 按 `Win + R`，輸入 `cmd`，按回車打開命令提示符

3. 進入 ADB 目錄：
   ```bash
   cd C:\adb\platform-tools
   ```

4. 驗證設備連接：
   ```bash
   adb devices
   ```
   如果顯示設備序列號，說明連接成功

5. 安裝 APK（替換為您的 APK 文件路徑）：
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**快捷方法**：輸入 `adb install ` 後，直接將 APK 文件拖入命令窗口，然後按回車。

</details>

<details>
<summary><b>Mac 用戶</b></summary>

1. 從 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 項目下載 `platform-tools-latest-darwin.zip` 並解壓

2. 打開終端，進入解壓目錄：
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. 授予執行權限（首次使用）：
   ```bash
   chmod +x adb
   ```

4. 驗證設備連接：
   ```bash
   ./adb devices
   ```

5. 安裝 APK：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux 用戶</b></summary>

1. 從 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 項目下載 `platform-tools-latest-linux.zip` 並解壓

2. 打開終端，進入解壓目錄

3. 授予執行權限：
   ```bash
   chmod +x adb
   ```

4. 驗證設備連接：
   ```bash
   ./adb devices
   ```

5. 安裝 APK：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **詳細安裝教程**：如需更詳細的 ADB 安裝說明和常見問題解決，請訪問 [Supernote APK 安裝工具](https://github.com/qiaodenghui/Supernote-Install) 項目。
✅ **安裝完成後**，您可以在 Supernote 的應用列表中找到 **Supernote Tools** 應用。

---

## 🚀 使用指南

### 第一步：下載語言包

1. 訪問 MyScript 官方網站：
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. 找到 **Recognition Assets 3.2** 版本

3. 選擇需要的語言包下載（ZIP格式）

### 第二步：傳輸語言包

將下載的語言包 ZIP 文件傳輸到 Supernote 設備（建議放在 `EXPORT` 或 `Document` 文件夾）

### 第三步：安裝語言包

1. 打開 **Supernote Tools** 應用
2. 點擊 **"選擇語言包文件"** 按鈕
3. 選擇下載的語言包 ZIP 文件
4. 選擇語言包類型：
   - **Lite版（精簡版）**：文件小，速度快，適合小屏設備
   - **Standard版（標準版）**：精度高，適合大屏設備和專業用戶
5. 點擊 **"安裝語言包"** 按鈕
6. 等待安裝完成

### 第四步：啟用語言包

在 Supernote 的手寫識別設置中選擇已安裝的語言即可使用。

---

## ⚙️ 技術說明

### 語言包版本

- **必須使用 MyScript Recognition Assets 3.2 版本**
- 其他版本可能不兼容

### 語言包類型對比

| 類型 | 文件大小 | 識別速度 | 識別精度 | 推薦設備 |
|------|---------|---------|---------|---------|
| Lite（精簡版） | 5-15 MB | 快 | 中等 | A5X/A6X |
| Standard（標準版） | 20-50 MB | 中等 | 高 | A5X2/A6X2 |

### 支持的語言

支持66種語言，包括但不限於：
- 中文（簡體/繁體）
- 英語
- 日語
- 韓語
- 法語、德語、西班牙語等歐洲語言
- 阿拉伯語、希伯來語等中東語言
- 更多語言請參考 MyScript 官方文檔

---

## ⚠️ 注意事項

1. ✅ 語言包必須是 **ZIP 格式**，不要解壓
2. ✅ 確保設備有足夠的存儲空間
3. ✅ 重複安裝會自動覆蓋舊版本
4. ✅ 安裝後可能需要重啟應用或設備

---

## 🔍 常見問題

<details>
<summary><b>Q: 安裝失敗怎麼辦？</b></summary>

- 檢查語言包版本是否為 3.2
- 確認文件是 ZIP 格式且未損壞
- 確保設備有足夠的存儲空間
- 檢查語言代碼是否在支持列表中
</details>

<details>
<summary><b>Q: 可以安裝多個語言包嗎？</b></summary>

可以，重複上述步驟安裝其他語言包即可。
</details>

<details>
<summary><b>Q: 如何卸載語言包？</b></summary>

在 Supernote 的手寫識別設置中可以刪除已安裝的語言。
</details>

<details>
<summary><b>Q: Lite版和Standard版可以混裝嗎？</b></summary>

可以，不同語言可以選擇不同版本。
</details>

---

## 🛠️ 技術說明

### 技術棧

- Android SDK
- Java
- MyScript Recognition SDK 3.2

### 應用架構

- 文件選擇器：用於選擇語言包 ZIP 文件
- ZIP 解析器：解析和驗證語言包文件
- 安裝引擎：將語言包安裝到系統目錄
- 版本管理：支持 Lite 和 Standard 兩種版本

---

## 📄 許可證

本項目基於開源協議發布，僅供學習和個人使用。

---

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

如果您有任何建議或發現了 Bug，請：
1. 提交 [Issue](../../issues) 描述問題
2. Fork 本項目並提交 Pull Request
3. 在社區中分享您的使用經驗

---

## 📞 聯繫與支持

如有問題或建議，請通過以下方式聯繫：

- 💬 提交 [Issue](../../issues)
- 🌐 訪問 [Supernote 社區](https://www.reddit.com/r/Supernote/)

---

## 🔗 相關項目

- [Supernote APK 安裝工具](https://github.com/qiaodenghui/Supernote-Install) - 詳細的 APK 安裝教程
- [MyScript 官方文檔](https://developer.myscript.com/) - 手寫識別技術文檔

---

## 🙏 致謝

- 感謝 [MyScript](https://www.myscript.com/) 提供手寫識別技術
- 感謝 Supernote 社區的支持

---

**如果這個項目對您有幫助，請給個 ⭐ Star 支持一下！**
