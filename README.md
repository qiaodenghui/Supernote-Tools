# Supernote Tools - Language Pack Installer

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**Handwriting Recognition Language Pack Installation Tool for Supernote E-ink Devices**

English | [简体中文](./README_ZH-CN.md) | [繁體中文](./README_ZH-TW.md) | [日本語](./README_JA.md) | [한국어](./README_KO.md) | [Deutsch](./README_DE.md)

---

## 📖 Introduction

Supernote Tools is an **offline language pack installer** specifically designed for Supernote e-ink devices, helping users install MyScript handwriting recognition language packs directly on the device without internet connection, with support for **66 languages**.

### ✨ Key Features

- 📴 **Offline Installation**: Install language packs directly on device without internet connection
- 🌍 **Multi-language Support**: Supports handwriting recognition for 66 languages
- 📦 **Dual Version Options**: Provides Lite (compact) and Standard versions
- 🚀 **Easy to Use**: Graphical interface with one-click installation
- 💾 **Smart Management**: Automatically detects and overwrites existing language packs
- ⚡ **Fast Installation**: Completes installation in seconds

### 🎯 Compatible Devices

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 Download & Installation

### Download the App

Download the latest `SupernoteTools.apk` file from the [Releases](../../releases) page.

### Install on Device

> ⚠️ **Important**: Supernote devices cannot directly install third-party APK applications. You need to use ADB (Android Debug Bridge) tool for sideloading.

#### Installation Steps Overview

**Step 1: Enable Sideload on Supernote**
1. Open **Settings** on your Supernote
2. Navigate to **Security and Privacy**
3. Enable the **Sideload** option

**Step 2: Connect Device to Computer**
1. Use a USB data cable to connect Supernote to your computer
2. If a prompt appears on the device, tap **OK** to allow the connection

**Step 3: Install APK Using ADB**

Choose the method for your operating system:

<details>
<summary><b>Windows Users</b></summary>

1. Download `platform-tools-latest-windows.zip` from [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) and extract to `C:\adb`

2. Press `Win + R`, type `cmd`, and press Enter to open Command Prompt

3. Navigate to ADB directory:
   ```bash
   cd C:\adb\platform-tools
   ```

4. Verify device connection:
   ```bash
   adb devices
   ```
   If it shows the device serial number, connection is successful

5. Install APK (replace with your APK file path):
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**Quick Method**: Type `adb install ` then drag the APK file into the command window and press Enter.

</details>

<details>
<summary><b>Mac Users</b></summary>

1. Download `platform-tools-latest-darwin.zip` from [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) and extract

2. Open Terminal and navigate to the extracted directory:
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. Grant execute permission (first time only):
   ```bash
   chmod +x adb
   ```

4. Verify device connection:
   ```bash
   ./adb devices
   ```

5. Install APK:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux Users</b></summary>

1. Download `platform-tools-latest-linux.zip` from [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) and extract

2. Open Terminal and navigate to the extracted directory

3. Grant execute permission:
   ```bash
   chmod +x adb
   ```

4. Verify device connection:
   ```bash
   ./adb devices
   ```

5. Install APK:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **Detailed Tutorial**: For more detailed ADB installation instructions and troubleshooting, visit the [Supernote APK Installation Tool](https://github.com/qiaodenghui/Supernote-Install) project.

✅ **After Installation**, you can find the **Supernote Tools** app in your Supernote's application list.

---

## 🚀 User Guide

### Step 1: Download Language Pack

1. Visit MyScript official website:
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. Find **Recognition Assets 3.2** version

3. Select and download the desired language pack (ZIP format)

### Step 2: Transfer Language Pack

Transfer the downloaded language pack ZIP file to your Supernote device (recommended to place in `EXPORT` or `Document` folder)

### Step 3: Install Language Pack

1. Open **Supernote Tools** app
2. Tap **"Select Language Pack File"** button
3. Select the downloaded language pack ZIP file
4. Choose language pack type:
   - **Lite Version**: Smaller file size, faster speed, suitable for small screen devices
   - **Standard Version**: Higher accuracy, suitable for large screen devices and professional users
5. Tap **"Install Language Pack"** button
6. Wait for installation to complete

### Step 4: Enable Language Pack

Select the installed language in Supernote's handwriting recognition settings to use it.

---

## ⚙️ Technical Details

### Language Pack Version

- **Must use MyScript Recognition Assets 3.2 version**
- Other versions may not be compatible

### Language Pack Type Comparison

| Type | File Size | Recognition Speed | Accuracy | Recommended Devices |
|------|-----------|------------------|----------|---------------------|
| Lite | 5-15 MB | Fast | Medium | A5/A6 small screen devices |
| Standard | 20-50 MB | Medium | High | A5X/A6X large screen devices |

### Supported Languages

Supports 66 languages, including but not limited to:
- Chinese (Simplified/Traditional)
- English
- Japanese
- Korean
- European languages (French, German, Spanish, etc.)
- Middle Eastern languages (Arabic, Hebrew, etc.)
- For more languages, refer to MyScript official documentation

---

## ⚠️ Important Notes

1. ✅ Language pack must be in **ZIP format**, do not extract
2. ✅ Ensure device has sufficient storage space
3. ✅ Reinstalling will automatically overwrite old versions
4. ✅ May need to restart app or device after installation

---

## 🔍 FAQ

<details>
<summary><b>Q: What if installation fails?</b></summary>

- Check if language pack version is 3.2
- Confirm file is in ZIP format and not corrupted
- Ensure device has sufficient storage space
- Check if language code is in the supported list
</details>

<details>
<summary><b>Q: Can I install multiple language packs?</b></summary>

Yes, repeat the above steps to install other language packs.
</details>

<details>
<summary><b>Q: How to uninstall language packs?</b></summary>

You can delete installed languages in Supernote's handwriting recognition settings.
</details>

<details>
<summary><b>Q: Can I mix Lite and Standard versions?</b></summary>

Yes, different languages can use different versions.
</details>

---

## 🛠️ Technical Information

### Tech Stack

- Android SDK
- Java
- MyScript Recognition SDK 3.2

### Application Architecture

- File Picker: For selecting language pack ZIP files
- ZIP Parser: Parses and validates language pack files
- Installation Engine: Installs language packs to system directory
- Version Management: Supports both Lite and Standard versions

---

## 📄 License

This project is released under an open source license for learning and personal use only.

---

## 🤝 Contributing

Issues and Pull Requests are welcome!

If you have any suggestions or find bugs, please:
1. Submit an [Issue](../../issues) describing the problem
2. Fork this project and submit a Pull Request
3. Share your experience in the community

---

## 📞 Contact & Support

For questions or suggestions, please contact us through:

- 💬 Submit an [Issue](../../issues)
- 🌐 Visit [Supernote Community](https://www.reddit.com/r/Supernote/)

---

## 🔗 Related Projects

- [Supernote APK Installation Tool](https://github.com/qiaodenghui/Supernote-Install) - Detailed APK installation tutorial
- [MyScript Official Documentation](https://developer.myscript.com/) - Handwriting recognition technology documentation

---

## 🙏 Acknowledgments

- Thanks to [MyScript](https://www.myscript.com/) for providing handwriting recognition technology
- Thanks to the Supernote community for their support

---

**If this project helps you, please give it a ⭐ Star!**
