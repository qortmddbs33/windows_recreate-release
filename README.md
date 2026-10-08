# 대웅그룹 자산실사 프로그램

> Windows · macOS 자산실사 — 기기 정보와 설치 프로그램 목록을 수집해 자산관리 포털로 등록하는 도구

## 📥 다운로드

**최신 버전**: [v2.5.0](https://github.com/qortmddbs33/windows_recreate/releases/tag/v2.5.0)

### 🪟 Windows (자산실사)
[![Windows](https://img.shields.io/badge/다운로드-DW__IDS__AssetAudit.exe-blue?style=for-the-badge&logo=windows)](https://github.com/qortmddbs33/windows_recreate-release/releases/latest/download/DW_IDS_AssetAudit.exe)

### 🍎 macOS (자산실사, Apple Silicon)
[![macOS](https://img.shields.io/badge/다운로드-macOS_ARM64_.dmg-black?style=for-the-badge&logo=apple)](https://github.com/qortmddbs33/windows_recreate-release/releases/latest/download/DW_IDS_AssetAudit-macOS-arm64.dmg)

## ✨ 주요 기능

### 📋 자산실사 (Windows·macOS)
- 기기 정보 자동 수집 — 제조사·모델, 시리얼 번호, CPU·메모리·그래픽·저장장치, OS 버전, MAC 주소
- 설치된 프로그램 목록 수집 (이름·게시자·버전·설치일)
- 자산번호·법인·부서·이름·이메일 입력 후 자산관리 포털로 등록
- 겸직/쉐어드 근무 시 원소속법인 선택, 공용PC 용도 입력 지원

### 🔒 권한·수집 범위
- **관리자 권한이 필요 없습니다** (`asInvoker`) — 실행 시 UAC 창이 뜨지 않습니다
- 문서·파일의 내용, 웹 접속 기록, 키보드 입력은 **수집하지 않습니다**
- 수집 항목·이용 목적·전송처는 프로그램 실행 화면의 "수집·이용 안내"에서 확인할 수 있습니다

## 🚀 사용 방법

### Windows
1. **.NET 8 Desktop Runtime 설치** (미설치 시 실행 안 됨): [다운로드](https://dotnet.microsoft.com/download/dotnet/8.0/runtime) → "Desktop Runtime" 선택
2. 위 Windows 버튼으로 `DW_IDS_AssetAudit.exe` 다운로드 후 실행

### macOS (Apple Silicon)
1. 위 macOS 버튼으로 `.dmg` 다운로드 → 앱을 Applications 로 드래그
2. 첫 실행 시 "확인되지 않은 개발자" 경고가 뜨면, 터미널에서 아래 실행 후 다시 열기:
   `xattr -dr com.apple.quarantine "/Applications/대웅그룹 MAC OS 전용 자산실사 프로그램.app"`

> ⚠️ **주의**: 일부 백신에서 오탐이 발생할 수 있습니다. 안전한 파일이므로 예외 처리해주세요.

## 📦 시스템 요구사항

- **Windows**: Windows 10/11 (64비트), .NET 8 Desktop Runtime 별도 설치
- **macOS**: Apple Silicon(ARM64), macOS 11 이상

## 📝 릴리즈 노트

## 자산실사 전용 배포판 (정보보호 검토 반영)

- 관리자 권한 없이 실행됩니다 (UAC 창이 뜨지 않음)
- 자산실사 외 기능(프로세스 종료·복원 지점·이벤트 로그·파일 정리)은 실행 파일에 포함되지 않습니다
- 자동 업데이트 기능이 없습니다 — 새 버전은 공지로 다시 배포합니다
- 웹 접속 기록은 수집하지 않습니다
- 입력한 이름·이메일은 전송에 성공하면 PC에서 즉시 삭제됩니다
- 로그는 1MB·30일까지만 보관합니다

이 버전부터 이전 버전 프로그램으로는 전송할 수 없습니다.

SHA-256: 25675e5ce54f9b7871dda9eb70dbb799d9afaa026a249a26d2ec2ed738d7e5e8


## 💬 문의하기

문제가 발생하거나 문의사항이 있으시면 [여기](https://assetify-desk.vercel.app/request)를 클릭해주세요.

---

**버전**: v2.5.0
**릴리즈 날짜**: 2026-10-08T07:58:57Z
**라이선스**: Proprietary
