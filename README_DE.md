# Supernote Tools - Sprachpaket-Installer

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**Handschrifterkennungs-Sprachpaket-Installationstool für Supernote E-Ink-Geräte**

[English](./README.md) | [简体中文](./README_ZH-CN.md) | [繁體中文](./README_ZH-TW.md) | [日本語](./README_JA.md) | [한국어](./README_KO.md) | Deutsch

---

## 📖 Projektübersicht

Supernote Tools ist ein **Offline-Sprachpaket-Installer**, der speziell für Supernote E-Ink-Geräte entwickelt wurde und Benutzern hilft, MyScript-Handschrifterkennungs-Sprachpakete direkt auf dem Gerät ohne Internetverbindung zu installieren, mit Unterstützung für **66 Sprachen**.

### ✨ Hauptfunktionen

- 📴 **Offline-Installation**: Installieren Sie Sprachpakete direkt auf dem Gerät ohne Internetverbindung
- 🌍 **Mehrsprachige Unterstützung**: Unterstützt Handschrifterkennung für 66 Sprachen
- 📦 **Zwei Versionen**: Bietet Lite (kompakt) und Standard-Versionen
- 🚀 **Einfach zu bedienen**: Grafische Benutzeroberfläche mit Ein-Klick-Installation
- 💾 **Intelligente Verwaltung**: Erkennt und überschreibt automatisch vorhandene Sprachpakete
- ⚡ **Schnelle Installation**: Abschluss in Sekunden

### 🎯 Kompatible Geräte

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 Download und Installation

### App herunterladen

Laden Sie die neueste `SupernoteTools.apk`-Datei von der [Releases](../../releases)-Seite herunter.

### Auf Gerät installieren

> ⚠️ **Wichtig**: Supernote-Geräte können standardmäßig keine Drittanbieter-APK-Anwendungen direkt installieren. Sie müssen das ADB (Android Debug Bridge)-Tool zum Sideloading verwenden.

#### Installationsschritte Übersicht

**Schritt 1: Sideload auf Supernote aktivieren**
1. Öffnen Sie **Einstellungen** auf Ihrem Supernote
2. Navigieren Sie zu **Sicherheit und Datenschutz**
3. Aktivieren Sie die Option **Sideload**

**Schritt 2: Gerät mit Computer verbinden**
1. Verbinden Sie Supernote mit einem USB-Datenkabel mit Ihrem Computer
2. Wenn eine Eingabeaufforderung auf dem Gerät erscheint, tippen Sie auf **OK**, um die Verbindung zuzulassen

**Schritt 3: APK mit ADB installieren**

Wählen Sie die Methode für Ihr Betriebssystem:

<details>
<summary><b>Windows-Benutzer</b></summary>

1. Laden Sie `platform-tools-latest-windows.zip` von [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) herunter und entpacken Sie es nach `C:\adb`

2. Drücken Sie `Win + R`, geben Sie `cmd` ein und drücken Sie Enter, um die Eingabeaufforderung zu öffnen

3. Navigieren Sie zum ADB-Verzeichnis:
   ```bash
   cd C:\adb\platform-tools
   ```

4. Geräteverbindung überprüfen:
   ```bash
   adb devices
   ```
   Wenn die Geräteseriennummer angezeigt wird, war die Verbindung erfolgreich

5. APK installieren (ersetzen Sie durch Ihren APK-Dateipfad):
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**Schnellmethode**: Geben Sie `adb install ` ein, ziehen Sie dann die APK-Datei in das Befehlsfenster und drücken Sie Enter.

</details>

<details>
<summary><b>Mac-Benutzer</b></summary>

1. Laden Sie `platform-tools-latest-darwin.zip` von [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) herunter und entpacken Sie es

2. Öffnen Sie Terminal und navigieren Sie zum entpackten Verzeichnis:
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. Ausführungsberechtigung erteilen (nur beim ersten Mal):
   ```bash
   chmod +x adb
   ```

4. Geräteverbindung überprüfen:
   ```bash
   ./adb devices
   ```

5. APK installieren:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux-Benutzer</b></summary>

1. Laden Sie `platform-tools-latest-linux.zip` von [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) herunter und entpacken Sie es

2. Öffnen Sie Terminal und navigieren Sie zum entpackten Verzeichnis

3. Ausführungsberechtigung erteilen:
   ```bash
   chmod +x adb
   ```

4. Geräteverbindung überprüfen:
   ```bash
   ./adb devices
   ```

5. APK installieren:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **Detailliertes Tutorial**: Für detailliertere ADB-Installationsanweisungen und Fehlerbehebung besuchen Sie das [Supernote APK-Installationstool](https://github.com/qiaodenghui/Supernote-Install)-Projekt.

✅ **Nach der Installation** finden Sie die **Supernote Tools**-App in der Anwendungsliste Ihres Supernote.

---

## 🚀 Benutzerhandbuch

### Schritt 1: Sprachpaket herunterladen

1. Besuchen Sie die offizielle MyScript-Website:
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. Finden Sie die **Recognition Assets 3.2**-Version
3. Laden Sie das gewünschte Sprachpaket herunter (ZIP-Format)

### Schritt 2: Sprachpaket übertragen

Übertragen Sie die heruntergeladene Sprachpaket-ZIP-Datei auf Ihr Supernote-Gerät (empfohlen im `EXPORT`- oder `Document`-Ordner)

### Schritt 3: Sprachpaket installieren

1. Öffnen Sie die **Supernote Tools**-App
2. Tippen Sie auf **"Sprachpaketdatei auswählen"**
3. Wählen Sie die heruntergeladene Sprachpaket-ZIP-Datei
4. Wählen Sie den Sprachpakettyp:
   - **Lite-Version**: Kleinere Dateigröße, schneller
   - **Standard-Version**: Höhere Genauigkeit
5. Tippen Sie auf **"Sprachpaket installieren"**
6. Warten Sie auf den Abschluss der Installation

### Schritt 4: Sprachpaket aktivieren

Wählen Sie die installierte Sprache in den Handschrifterkennungseinstellungen Ihres Supernote aus.

---

## ⚙️ Technische Spezifikationen

### Sprachpaketversion
- **Muss MyScript Recognition Assets 3.2-Version verwenden**

### Sprachpakettyp-Vergleich

| Typ | Dateigröße | Erkennungsgeschwindigkeit | Genauigkeit | Empfohlene Geräte |
|------|---------|---------|---------|---------|
| Lite | 5-15 MB | Schnell | Mittel | A5X/A6X |
| Standard | 20-50 MB | Mittel | Hoch | A5X2/A6X2 |

### Unterstützte Sprachen

66 Sprachen unterstützt: Chinesisch, Englisch, Japanisch, Koreanisch, Französisch, Deutsch usw.

---

## ⚠️ Hinweise

1. ✅ Sprachpaket muss im **ZIP-Format** sein
2. ✅ Ausreichend Speicherplatz sicherstellen
3. ✅ Neuinstallation überschreibt automatisch
4. ✅ Neustart nach Installation möglicherweise erforderlich

---

## 🔍 Häufig gestellte Fragen

<details>
<summary><b>F: Was tun bei Installationsfehlern?</b></summary>

- Version 3.2 überprüfen
- ZIP-Format überprüfen
- Speicherplatz überprüfen
</details>

<details>
<summary><b>F: Mehrere Sprachpakete installierbar?</b></summary>

Ja, wiederholen Sie die Schritte für weitere Sprachpakete.
</details>

---

## 🛠️ Technische Informationen

- Android SDK
- Java
- MyScript Recognition SDK 3.2

---

## 📄 Lizenz

Nur für Lern- und persönliche Zwecke.

---

## 🤝 Beitragen

Issues und Pull Requests willkommen!

---

## 📞 Kontakt

- 💬 [Issue](../../issues)
- 🌐 [Supernote Community](https://www.reddit.com/r/Supernote/)

---

## 🔗 Verwandte Projekte

- [Supernote APK-Installationstool](https://github.com/qiaodenghui/Supernote-Install)
- [MyScript Offizielle Dokumentation](https://developer.myscript.com/)

---

## 🙏 Danksagungen

- [MyScript](https://www.myscript.com/)
- Supernote Community

---

**⭐ Geben Sie einen Star, wenn es hilfreich war!**
