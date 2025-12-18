# Supernote Tools - 언어 팩 설치 프로그램

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Supernote-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

**Supernote 전자잉크 기기 전용 필기 인식 언어 팩 설치 도구**

[English](./README.md) | [简体中文](./README_ZH-CN.md) | [繁體中文](./README_ZH-TW.md) | [日本語](./README_JA.md) | 한국어 | [Deutsch](./README_DE.md)

---

## 📖 프로젝트 소개

Supernote Tools는 Supernote 전자잉크 기기 전용으로 개발된 **오프라인 언어 팩 설치 프로그램**으로, 인터넷 연결 없이 기기에서 직접 MyScript 필기 인식 언어 팩을 설치할 수 있으며 **66개 언어**의 필기 인식 기능을 지원합니다.

### ✨ 주요 기능

- 📴 **오프라인 설치**: 인터넷 연결 없이 기기에서 직접 언어 팩 설치
- 🌍 **다국어 지원**: 66개 언어의 필기 인식 지원
- 📦 **이중 버전 선택**: Lite(경량판)와 Standard(표준판) 두 가지 언어 팩 제공
- 🚀 **간편한 사용**: 그래픽 인터페이스로 원클릭 설치
- 💾 **스마트 관리**: 기존 언어 팩 자동 감지 및 덮어쓰기
- ⚡ **빠른 설치**: 몇 초 만에 설치 완료

### 🎯 호환 기기

- Supernote A5X/A6X/A5X2/A6X2

---

## 📥 다운로드 및 설치

### 앱 다운로드

[Releases](../../releases) 페이지에서 최신 버전의 `SupernoteTools.apk` 파일을 다운로드하세요.

### 기기에 설치

> ⚠️ **중요 안내**: Supernote 기기는 기본적으로 타사 APK 앱을 직접 설치할 수 없습니다. ADB(Android Debug Bridge) 도구를 사용하여 사이드로드해야 합니다.

#### 설치 단계 개요

**1단계: Supernote에서 사이드로드 기능 활성화**
1. Supernote의 **설정** 열기
2. **보안 및 개인정보** 이동
3. **사이드로드(Sideload)** 옵션 활성화

**2단계: 기기를 컴퓨터에 연결**
1. USB 데이터 케이블로 Supernote를 컴퓨터에 연결
2. 기기에 프롬프트가 표시되면 **확인**을 탭하여 연결 허용

**3단계: ADB를 사용하여 APK 설치**

운영 체제에 따라 해당 방법을 선택하세요:

<details>
<summary><b>Windows 사용자</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 프로젝트에서 `platform-tools-latest-windows.zip`을 다운로드하여 `C:\adb`에 압축 해제

2. `Win + R`을 누르고 `cmd`를 입력한 후 Enter를 눌러 명령 프롬프트 열기

3. ADB 디렉토리로 이동:
   ```bash
   cd C:\adb\platform-tools
   ```

4. 기기 연결 확인:
   ```bash
   adb devices
   ```
   기기 일련번호가 표시되면 연결 성공

5. APK 설치(APK 파일 경로로 교체):
   ```bash
   adb install "D:\Downloads\SupernoteTools.apk"
   ```

**빠른 방법**: `adb install `을 입력한 후 APK 파일을 명령 창으로 드래그하고 Enter를 누르세요.

</details>

<details>
<summary><b>Mac 사용자</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 프로젝트에서 `platform-tools-latest-darwin.zip`을 다운로드하여 압축 해제

2. 터미널을 열고 압축 해제된 디렉토리로 이동:
   ```bash
   cd ~/Downloads/platform-tools
   ```

3. 실행 권한 부여(처음만):
   ```bash
   chmod +x adb
   ```

4. 기기 연결 확인:
   ```bash
   ./adb devices
   ```

5. APK 설치:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

<details>
<summary><b>Linux 사용자</b></summary>

1. [Supernote-Install](https://github.com/qiaodenghui/Supernote-Install) 프로젝트에서 `platform-tools-latest-linux.zip`을 다운로드하여 압축 해제

2. 터미널을 열고 압축 해제된 디렉토리로 이동

3. 실행 권한 부여:
   ```bash
   chmod +x adb
   ```

4. 기기 연결 확인:
   ```bash
   ./adb devices
   ```

5. APK 설치:
   ```bash
   ./adb install ~/Downloads/SupernoteTools.apk
   ```

</details>

> 💡 **자세한 튜토리얼**: 더 자세한 ADB 설치 지침 및 문제 해결은 [Supernote APK 설치 도구](https://github.com/qiaodenghui/Supernote-Install) 프로젝트를 참조하세요.

✅ **설치 완료 후**, Supernote의 애플리케이션 목록에서 **Supernote Tools** 앱을 찾을 수 있습니다.

---

## 🚀 사용 가이드

### 1단계: 언어 팩 다운로드

1. MyScript 공식 웹사이트 방문:
   ```
   https://developer.myscript.com/support/recognition-assets
   ```

2. **Recognition Assets 3.2** 버전 찾기
3. 필요한 언어 팩 다운로드(ZIP 형식)

### 2단계: 언어 팩 전송

다운로드한 언어 팩 ZIP 파일을 Supernote 기기로 전송(`EXPORT` 또는 `Document` 폴더에 배치 권장)

### 3단계: 언어 팩 설치

1. **Supernote Tools** 앱 열기
2. **"언어 팩 파일 선택"** 버튼 탭
3. 다운로드한 언어 팩 ZIP 파일 선택
4. 언어 팩 유형 선택:
   - **Lite 버전**: 파일 크기 작음, 속도 빠름
   - **Standard 버전**: 정확도 높음
5. **"언어 팩 설치"** 버튼 탭
6. 설치 완료 대기

### 4단계: 언어 팩 활성화

Supernote의 필기 인식 설정에서 설치된 언어를 선택하여 사용할 수 있습니다.

---

## ⚙️ 기술 사양

### 언어 팩 버전
- **MyScript Recognition Assets 3.2 버전을 사용해야 합니다**

### 언어 팩 유형 비교

| 유형 | 파일 크기 | 인식 속도 | 인식 정확도 | 권장 기기 |
|------|---------|---------|---------|---------|
| Lite | 5-15 MB | 빠름 | 중간 | A5X/A6X |
| Standard | 20-50 MB | 중간 | 높음 | A5X2/A6X2 |

### 지원 언어

66개 언어 지원: 중국어, 영어, 일본어, 한국어, 프랑스어, 독일어 등

---

## ⚠️ 주의사항

1. ✅ 언어 팩은 **ZIP 형식**이어야 합니다
2. ✅ 충분한 저장 공간 확인
3. ✅ 재설치 시 자동 덮어쓰기
4. ✅ 설치 후 재시작 필요할 수 있음

---

## 🔍 자주 묻는 질문

<details>
<summary><b>Q: 설치 실패 시?</b></summary>

- 버전 3.2 확인
- ZIP 형식 확인
- 저장 공간 확인
</details>

<details>
<summary><b>Q: 여러 언어 팩 설치 가능?</b></summary>

예, 반복 설치 가능합니다.
</details>

---

## 🛠️ 기술 정보

- Android SDK
- Java
- MyScript Recognition SDK 3.2

---

## 📄 라이선스

학습 및 개인 사용 목적으로만 제공됩니다.

---

## 🤝 기여

Issue 및 Pull Request 환영!

---

## 📞 연락처

- 💬 [Issue](../../issues)
- 🌐 [Supernote 커뮤니티](https://www.reddit.com/r/Supernote/)

---

## 🔗 관련 프로젝트

- [Supernote APK 설치 도구](https://github.com/qiaodenghui/Supernote-Install)
- [MyScript 공식 문서](https://developer.myscript.com/)

---

## 🙏 감사

- [MyScript](https://www.myscript.com/)
- Supernote 커뮤니티

---

**⭐ Star를 눌러주세요!**
