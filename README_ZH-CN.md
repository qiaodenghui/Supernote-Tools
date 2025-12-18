# Supernote Tools - 语言包安装器

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**专为 Supernote 墨水屏设备设计的手写识别语言包安装工具**

[English](./README.md) | 简体中文 | [繁體中文](./README_ZH-TW.md) | [日本語](./README_JA.md) | [한국어](./README_KO.md) | [Deutsch](./README_DE.md)

---

## 📖 项目简介

Supernote Tools 是一款专为 Supernote 墨水屏设备开发的**离线语言包安装器**，帮助用户在设备本地直接安装 MyScript 手写识别语言包，无需联网即可完成安装，支持 **66种语言** 的手写识别功能。

### ✨ 主要特性

- 📴 **离线安装**：无需联网，直接在设备上安装语言包
- 🌍 **多语言支持**：支持66种语言的手写识别
- 📦 **双版本选择**：提供 Lite（精简版）和 Standard（标准版）两种语言包
- 🚀 **简单易用**：图形化界面，一键安装
- 💾 **智能管理**：自动检测和覆盖已有语言包
- ⚡ **快速安装**：几秒钟即可完成安装

### 🎯 适用设备

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 下载安装

### 下载应用

从 [Releases](../../releases) 页面下载最新版本的 `SupernoteTools.apk` 文件。

### 安装到设备

> ⚠️ **重要提示**：Supernote 设备默认无法直接安装第三方 APK 应用，需要通过 ADB（Android Debug Bridge）工具进行侧载安装。

#### 安装步骤概述

**第一步：在 Supernote 上启用侧载功能**
1. 打开 Supernote 的 **设置**
2. 进入 **安全和隐私**
3. 启用 **侧载（Sideload）** 选项

**第二步：连接设备到电脑**
1. 使用 USB 数据线将 Supernote 连接到电脑
2. 如果设备上出现提示，点击 **确定** 允许连接

**第三步：使用 ADB 安装 APK**

根据您的操作系统选择对应的方法：

<details>
<summary><b>Windows 用户</b></summary>

1. 从 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 项目下载 `platform-tools-latest-windows.zip` 并解压到 `C:\adb`

2. 按 `Win + R`，输入 `cmd`，按回车打开命令提示符

3. 进入 ADB 目录：
   ```bash
   cd C:\adb\platform-tools
   ```

4. 验证设备连接：
   ```bash
   adb devices
   ```
   如果显示设备序列号，说明连接成功

5. 安装 APK（替换为您的 APK 文件路径）：
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**快捷方法**：输入 `adb install ` 后，直接将 APK 文件拖入命令窗口，然后按回车。

</details>

<details>
<summary><b>Mac 用户</b></summary>

1. 从 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 项目下载 `platform-tools-latest-darwin.zip` 并解压

2. 打开终端，进入解压目录：
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. 授予执行权限（首次使用）：
   ```bash
   chmod +x adb
   ```

4. 验证设备连接：
   ```bash
   ./adb devices
   ```

5. 安装 APK：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux 用户</b></summary>

1. 从 [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 项目下载 `platform-tools-latest-linux.zip` 并解压

2. 打开终端，进入解压目录

3. 授予执行权限：
   ```bash
   chmod +x adb
   ```

4. 验证设备连接：
   ```bash
   ./adb devices
   ```

5. 安装 APK：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **详细安装教程**：如需更详细的 ADB 安装说明和常见问题解决，请访问 [Supernote APK 安装工具](https://github.com/qiaodenghui/Supernote-Install) 项目。

✅ **安装完成后**，您可以在 Supernote 的应用列表中找到 **Supernote Tools** 应用。

---

## 🚀 使用指南

### 第一步：下载语言包

1. 访问 MyScript 官方网站：
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. 找到 **Recognition Assets 3.2** 版本

3. 选择需要的语言包下载（ZIP格式）

### 第二步：传输语言包

将下载的语言包 ZIP 文件传输到 Supernote 设备（建议放在 `EXPORT` 或 `Document` 文件夹）

### 第三步：安装语言包

1. 打开 **Supernote Tools** 应用
2. 点击 **"选择语言包文件"** 按钮
3. 选择下载的语言包 ZIP 文件
4. 选择语言包类型：
   - **Lite版（精简版）**：文件小，速度快，适合小屏设备
   - **Standard版（标准版）**：精度高，适合大屏设备和专业用户
5. 点击 **"安装语言包"** 按钮
6. 等待安装完成

### 第四步：启用语言包

在 Supernote 的手写识别设置中选择已安装的语言即可使用。

---

## ⚙️ 技术说明

### 语言包版本

- **必须使用 MyScript Recognition Assets 3.2 版本**
- 其他版本可能不兼容

### 语言包类型对比

| 类型 | 文件大小 | 识别速度 | 识别精度 | 推荐设备 |
|------|---------|---------|---------|---------|
| Lite（精简版） | 5-15 MB | 快 | 中等 | A5/A6 小屏设备 |
| Standard（标准版） | 20-50 MB | 中等 | 高 | A5X/A6X 大屏设备 |

### 支持的语言

支持66种语言，包括但不限于：
- 中文（简体/繁体）
- 英语
- 日语
- 韩语
- 法语、德语、西班牙语等欧洲语言
- 阿拉伯语、希伯来语等中东语言
- 更多语言请参考 MyScript 官方文档

---

## ⚠️ 注意事项

1. ✅ 语言包必须是 **ZIP 格式**，不要解压
2. ✅ 确保设备有足够的存储空间
3. ✅ 重复安装会自动覆盖旧版本
4. ✅ 安装后可能需要重启应用或设备

---

## 🔍 常见问题

<details>
<summary><b>Q: 安装失败怎么办？</b></summary>

- 检查语言包版本是否为 3.2
- 确认文件是 ZIP 格式且未损坏
- 确保设备有足够的存储空间
- 检查语言代码是否在支持列表中
</details>

<details>
<summary><b>Q: 可以安装多个语言包吗？</b></summary>

可以，重复上述步骤安装其他语言包即可。
</details>

<details>
<summary><b>Q: 如何卸载语言包？</b></summary>

在 Supernote 的手写识别设置中可以删除已安装的语言。
</details>

<details>
<summary><b>Q: Lite版和Standard版可以混装吗？</b></summary>

可以，不同语言可以选择不同版本。
</details>

---

## 🛠️ 技术说明

### 技术栈

- Android SDK
- Java
- MyScript Recognition SDK 3.2

### 应用架构

- 文件选择器：用于选择语言包 ZIP 文件
- ZIP 解析器：解析和验证语言包文件
- 安装引擎：将语言包安装到系统目录
- 版本管理：支持 Lite 和 Standard 两种版本

---

## 📄 许可证

本项目基于开源协议发布，仅供学习和个人使用。

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

如果您有任何建议或发现了 Bug，请：
1. 提交 [Issue](../../issues) 描述问题
2. Fork 本项目并提交 Pull Request
3. 在社区中分享您的使用经验

---

## 📞 联系与支持

如有问题或建议，请通过以下方式联系：

- 💬 提交 [Issue](../../issues)
- 🌐 访问 [Supernote 社区](https://www.reddit.com/r/Supernote/)

---

## 🔗 相关项目

- [Supernote APK 安装工具](https://github.com/qiaodenghui/Supernote-Install) - 详细的 APK 安装教程
- [MyScript 官方文档](https://developer.myscript.com/) - 手写识别技术文档

---

## 🙏 致谢

- 感谢 [MyScript](https://www.myscript.com/) 提供手写识别技术
- 感谢 Supernote 社区的支持

---

**如果这个项目对您有帮助，请给个 ⭐ Star 支持一下！**
