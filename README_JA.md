# Supernote Tools - 言語パックインストーラー

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**Supernote 電子ペーパーデバイス専用の手書き認識言語パックインストールツール**

[English](./README.md) | [简体中文](./README_ZH-CN.md) | [繁體中文](./README_ZH-TW.md) | 日本語 | [한국어](./README_KO.md) | [Deutsch](./README_DE.md)

---

## 📖 プロジェクト概要

Supernote Tools は、Supernote 電子ペーパーデバイス専用に開発された**オフライン言語パックインストーラー**で、インターネット接続なしでデバイス上で直接 MyScript 手書き認識言語パックをインストールでき、**66言語**の手書き認識機能をサポートしています。

### ✨ 主な機能

- 📴 **オフラインインストール**：インターネット接続なしでデバイス上で直接言語パックをインストール
- 🌍 **多言語サポート**：66言語の手書き認識に対応
- 📦 **2つのバージョン**：Lite版(軽量版)とStandard版(標準版)を提供
- 🚀 **簡単操作**：グラフィカルインターフェースでワンクリックインストール
- 💾 **スマート管理**：既存の言語パックを自動検出して上書き
- ⚡ **高速インストール**：数秒で完了

### 🎯 対応デバイス

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 ダウンロードとインストール

### アプリのダウンロード

[Releases](../../releases) ページから最新版の `SupernoteTools.apk` ファイルをダウンロードしてください。

### デバイスへのインストール

> ⚠️ **重要な注意事項**：Supernote デバイスはデフォルトでサードパーティ APK アプリを直接インストールできません。ADB（Android Debug Bridge）ツールを使用してサイドロードする必要があります。

#### インストール手順の概要

**ステップ1：Supernote でサイドロード機能を有効にする**
1. Supernote の **設定** を開く
2. **セキュリティとプライバシー** に移動
3. **サイドロード（Sideload）** オプションを有効にする

**ステップ2：デバイスをコンピュータに接続**
1. USB データケーブルで Supernote をコンピュータに接続
2. デバイスにプロンプトが表示されたら、**OK** をタップして接続を許可

**ステップ3：ADB を使用して APK をインストール**

お使いのオペレーティングシステムに応じた方法を選択してください：

<details>
<summary><b>Windows ユーザー</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) プロジェクトから `platform-tools-latest-windows.zip` をダウンロードし、`C:\adb` に解凍

2. `Win + R` を押し、`cmd` と入力して Enter を押してコマンドプロンプトを開く

3. ADB ディレクトリに移動：
   ```bash
   cd C:\adb\platform-tools
   ```

4. デバイス接続を確認：
   ```bash
   adb devices
   ```
   デバイスのシリアル番号が表示されれば、接続成功です

5. APK をインストール（APK ファイルのパスに置き換えてください）：
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**クイック方法**：`adb install ` と入力した後、APK ファイルをコマンドウィンドウにドラッグして Enter を押します。

</details>

<details>
<summary><b>Mac ユーザー</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) プロジェクトから `platform-tools-latest-darwin.zip` をダウンロードして解凍

2. ターミナルを開き、解凍したディレクトリに移動：
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. 実行権限を付与（初回のみ）：
   ```bash
   chmod +x adb
   ```

4. デバイス接続を確認：
   ```bash
   ./adb devices
   ```

5. APK をインストール：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux ユーザー</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) プロジェクトから `platform-tools-latest-linux.zip` をダウンロードして解凍

2. ターミナルを開き、解凍したディレクトリに移動

3. 実行権限を付与：
   ```bash
   chmod +x adb
   ```

4. デバイス接続を確認：
   ```bash
   ./adb devices
   ```

5. APK をインストール：
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **詳細なチュートリアル**：より詳細な ADB インストール手順とトラブルシューティングについては、[Supernote APK インストールツール](https://github.com/qiaodenghui/Supernote-Install) プロジェクトをご覧ください。

✅ **インストール完了後**、Supernote のアプリケーションリストで **Supernote Tools** アプリを見つけることができます。

---

## 🚀 使用ガイド

### ステップ1：言語パックをダウンロード

1. MyScript 公式ウェブサイトにアクセス：
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. **Recognition Assets 3.2** バージョンを見つける

3. 必要な言語パックをダウンロード（ZIP形式）

### ステップ2：言語パックを転送

ダウンロードした言語パック ZIP ファイルを Supernote デバイスに転送（`EXPORT` または `Document` フォルダに配置することを推奨）

### ステップ3：言語パックをインストール

1. **Supernote Tools** アプリを開く
2. **「言語パックファイルを選択」** ボタンをタップ
3. ダウンロードした言語パック ZIP ファイルを選択
4. 言語パックのタイプを選択：
   - **Lite版（軽量版）**：ファイルサイズが小さく、速度が速い、小画面デバイスに適している
   - **Standard版（標準版）**：精度が高い、大画面デバイスとプロフェッショナルユーザーに適している
5. **「言語パックをインストール」** ボタンをタップ
6. インストールが完了するまで待つ

### ステップ4：言語パックを有効にする

Supernote の手書き認識設定でインストールした言語を選択して使用できます。

---

## ⚙️ 技術仕様

### 言語パックのバージョン

- **MyScript Recognition Assets 3.2 バージョンを使用する必要があります**
- 他のバージョンは互換性がない可能性があります

### 言語パックタイプの比較

| タイプ | ファイルサイズ | 認識速度 | 認識精度 | 推奨デバイス |
|------|-----------|---------|---------|---------|
| Lite（軽量版） | 5-15 MB | 速い | 中程度 | A5X/A6X |
| Standard（標準版） | 20-50 MB | 中程度 | 高い | A5X2/A6X2 |

### サポートされている言語

66言語をサポート、以下を含むがこれに限定されません：
- 中国語（簡体字/繁体字）
- 英語
- 日本語
- 韓国語
- ヨーロッパ言語（フランス語、ドイツ語、スペイン語など）
- 中東言語（アラビア語、ヘブライ語など）
- その他の言語については MyScript 公式ドキュメントを参照してください

---

## ⚠️ 注意事項

1. ✅ 言語パックは **ZIP 形式** である必要があります、解凍しないでください
2. ✅ デバイスに十分なストレージスペースがあることを確認してください
3. ✅ 再インストールすると古いバージョンが自動的に上書きされます
4. ✅ インストール後、アプリまたはデバイスの再起動が必要な場合があります

---

## 🔍 よくある質問

<details>
<summary><b>Q: インストールに失敗した場合はどうすればよいですか？</b></summary>

- 言語パックのバージョンが 3.2 であることを確認してください
- ファイルが ZIP 形式で破損していないことを確認してください
- デバイスに十分なストレージスペースがあることを確認してください
- 言語コードがサポートリストにあることを確認してください
</details>

<details>
<summary><b>Q: 複数の言語パックをインストールできますか？</b></summary>

はい、上記の手順を繰り返して他の言語パックをインストールできます。
</details>

<details>
<summary><b>Q: 言語パックをアンインストールするにはどうすればよいですか？</b></summary>

Supernote の手書き認識設定でインストールした言語を削除できます。
</details>

<details>
<summary><b>Q: Lite版とStandard版を混在させることはできますか？</b></summary>

はい、異なる言語で異なるバージョンを選択できます。
</details>

---

## 🛠️ 技術情報

### 技術スタック

- Android SDK
- Java
- MyScript Recognition SDK 3.2

### アプリケーションアーキテクチャ

- ファイルピッカー：言語パック ZIP ファイルを選択するため
- ZIP パーサー：言語パックファイルを解析および検証
- インストールエンジン：言語パックをシステムディレクトリにインストール
- バージョン管理：Lite と Standard の両方のバージョンをサポート

---

## 📄 ライセンス

このプロジェクトはオープンソースライセンスの下で公開されており、学習および個人使用のみを目的としています。

---

## 🤝 貢献

Issue と Pull Request を歓迎します！

提案がある場合やバグを見つけた場合は：
1. 問題を説明する [Issue](../../issues) を提出してください
2. このプロジェクトを Fork して Pull Request を提出してください
3. コミュニティで経験を共有してください

---

## 📞 お問い合わせとサポート

質問や提案がある場合は、以下の方法でお問い合わせください：

- 💬 [Issue](../../issues) を提出
- 🌐 [Supernote コミュニティ](https://www.reddit.com/r/Supernote/) を訪問

---

## 🔗 関連プロジェクト

- [Supernote APK インストールツール](https://github.com/qiaodenghui/Supernote-Install) - 詳細な APK インストールチュートリアル
- [MyScript 公式ドキュメント](https://developer.myscript.com/) - 手書き認識技術ドキュメント

---

## 🙏 謝辞

- 手書き認識技術を提供してくれた [MyScript](https://www.myscript.com/) に感謝します
- Supernote コミュニティのサポートに感謝します

---

**このプロジェクトが役に立った場合は、⭐ Star をお願いします！**
