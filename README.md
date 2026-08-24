# 대웅그룹 PC 자산관리 프로그램

> Windows PC 스캐닝 · macOS 자산실사 — 시스템 정보/보안/설치 프로그램을 스캔하고 자산을 실사하는 통합 도구

## 📥 다운로드

**최신 버전**: [v2.3.0](https://github.com/qortmddbs33/windows_recreate/releases/tag/v2.3.0)

### 🪟 Windows (PC 스캐닝 프로그램)
[![Windows](https://img.shields.io/badge/다운로드-DW__IDS__PCSCAN.exe-blue?style=for-the-badge&logo=windows)](https://github.com/qortmddbs33/windows_recreate-release/releases/latest/download/DW_IDS_PCSCAN.exe)

### 🍎 macOS (자산실사, Apple Silicon)
[![macOS](https://img.shields.io/badge/다운로드-macOS_ARM64_.dmg-black?style=for-the-badge&logo=apple)](https://github.com/qortmddbs33/windows_recreate-release/releases/latest/download/DW_IDS_AssetAudit-macOS-arm64.dmg)

## ✨ 주요 기능

### 🖥 시스템 모니터 (Windows)
- **CPU**: 코어별 점유율 + 실시간 클럭 표시
- **GPU**: 엔진별 점유율 (3D, VideoEncode, VideoDecode, Compute, Copy)
- **메모리**: 사용량 및 여유 공간 실시간 모니터링
- **스토리지**: 드라이브별 사용량 + 모델명 표시
- **네트워크**: 실시간 업로드/다운로드 속도
- **배터리**: 수명, 사이클 수, 설계/최대충전 용량 비교

### ⚡ 프로세스 관리 (Windows)
- 실행 중인 프로세스 목록 및 리소스 사용량 확인
- 프로세스 종료 기능

### 💾 RAM 사용량 분석 (Windows)
- 프로세스별 메모리 사용량 상세 분석
- 메모리 최적화 제안

### 🗑 불필요 파일 제거 (Windows)
- 임시 파일, 캐시 파일 자동 탐지 및 안전한 삭제

### 🛡 설치된 프로그램 관리 (Windows·macOS)
- 설치된 프로그램 목록 표시 및 화이트리스트 기반 보안 검사
- 보안 제품 설치 여부 확인

### 📋 자산실사 (Windows·macOS)
- 하드웨어 정보 자동 수집 + 사용자 정보 입력 후 포털로 등록
- 겸직/쉐어드 근무 시 원소속법인 선택 지원

## 🚀 사용 방법

### Windows
1. **.NET 8 Desktop Runtime 설치** (미설치 시 실행 안 됨): [다운로드](https://dotnet.microsoft.com/download/dotnet/8.0/runtime) → "Desktop Runtime" 선택
2. 위 Windows 버튼으로 `DW_IDS_PCSCAN.exe` 다운로드 후 실행

### macOS (Apple Silicon)
1. 위 macOS 버튼으로 `.dmg` 다운로드 → 앱을 Applications 로 드래그
2. 첫 실행 시 "확인되지 않은 개발자" 경고가 뜨면, 터미널에서 아래 실행 후 다시 열기:
   `xattr -dr com.apple.quarantine "/Applications/대웅그룹 MAC OS 전용 자산실사 프로그램.app"`

> ⚠️ **주의**: 일부 백신에서 오탐이 발생할 수 있습니다. 안전한 파일이므로 예외 처리해주세요.

## 📦 시스템 요구사항

- **Windows**: Windows 10/11 (64비트), .NET 8 Desktop Runtime 별도 설치
- **macOS**: Apple Silicon(ARM64), macOS 11 이상

## 📝 릴리즈 노트

## SW 정책을 포털에서 직접 받고, 자동 설치 프로그램을 판정에서 뺍니다

### SW 정책 출처가 바뀌었습니다 (Notion CSV → 포털)

지금까지 PC 화면의 프로그램 판정은 Notion 에 올려둔 CSV 를 받아 썼고, 포털의 설치 SW
감사는 별개의 정책 목록을 봤습니다. 같은 프로그램이 PC 에서는 "사용자 임의 설치"인데
포털에서는 "승인"으로 나오면 둘 중 하나는 반드시 틀린 답입니다.

이제 양쪽이 **같은 정책**을 봅니다. 정책을 고칠 곳도 포털 관리 페이지 한 곳입니다.

- 상단 문구가 `SW 정책 기준일: YYYY-MM-DD` 로 바뀝니다
- 포털을 못 받으면 마지막으로 받은 정책(캐시)을 쓰고, 그것도 없으면 내장 목록으로
  내려갑니다 — 이때는 `SW 정책: 내장 CSV(포털 연결 실패)` 로 표시됩니다
- 금지 표기가 두 가지 섞여 있던 것도 함께 잡습니다. 실제 데이터의 금지 27종이
  이전에는 판정에서 조용히 빠지고 있었습니다

### "판정 제외" 가 생겼습니다

은행·공공기관 접속 시 자동으로 깔리는 보안모듈, OS 런타임, 드라이버는 사용자가 골라
설치한 프로그램이 아닙니다. 그런데도 지금까지 **"사용자가 임의로 설치한 프로그램입니다"**
배지가 붙어, 관리자가 매번 같은 판단을 반복해야 했습니다.

이런 항목에는 이제 파란 배지가 붙고 "임의 설치" 로 세지 않습니다:

> 자동 설치되는 프로그램입니다 (승인/금지 판정 대상 아님)

- 예: Visual C++ 재배포 패키지, .NET 런타임, Edge WebView2, AhnLab Safe Transaction,
  TouchEn, INISAFE, Veraport, nProtect, Intel·NVIDIA·Realtek 드라이버
- 필터에 **판정 제외(자동 설치)** 체크박스가 추가됐고, 상태줄에 `· 판정 제외 N개` 로
  몇 개가 빠졌는지 보입니다
- 정책 목록에 등록된 예외 항목과, 이름·게시자로 자동 인식한 것 둘 다 잡습니다.
  드라이버·보안모듈은 버전·모델마다 이름이 달라 목록만으로는 커버할 수 없습니다

⚠️ Intel·NVIDIA·Realtek 은 게시자로 걸러서, 그 회사가 만든 사용자 선택 프로그램
(예: GeForce Experience)도 함께 판정에서 빠집니다. 드라이버를 잡기 위한 선택입니다.
백신처럼 일반 사용자용 제품도 파는 회사는 게시자로 걸지 않습니다 — V3 Endpoint
Security 는 그대로 판정 대상입니다.

### macOS 자산실사

기능 변경은 없습니다. 버전만 Windows 와 맞췄습니다.


## 💬 문의하기

문제가 발생하거나 문의사항이 있으시면 [여기](https://assetify-desk.vercel.app/request)를 클릭해주세요.

---

**버전**: v2.3.0
**릴리즈 날짜**: 2026-08-24T08:49:06Z
**라이선스**: Proprietary
