# 대웅그룹 PC 자산관리 프로그램

> Windows PC 스캐닝 · macOS 자산실사 — 시스템 정보/보안/설치 프로그램을 스캔하고 자산을 실사하는 통합 도구

## 📥 다운로드

**최신 버전**: [v2.1.5](https://github.com/qortmddbs33/windows_recreate/releases/tag/v2.1.5)

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

## 네트워크 미연결 시 MAC 주소가 빈 채로 등록되던 문제 수정

랜선이 연결되지 않았거나 Wi-Fi에 접속되지 않은 상태로 프로그램을 실행하면
MAC 주소가 수집되지 않고 빈 값으로 등록되던 문제를 수정했습니다.
Windows·macOS 자산실사 양쪽 모두 적용됩니다.

### MAC 주소 수집 3단 폴백

앞 단계에서 못 찾으면 다음 단계로 넘어갑니다.

**Windows**
1. IP가 구성된 어댑터 (실사용 중인 NIC)
2. 물리 어댑터 — 연결 여부와 무관하게 읽힘 (VMware/Hyper-V 등 가상 NIC 제외)
3. NetworkInterface — 보안 SW로 WMI 자체가 막힌 경우의 최후 수단

**macOS**
1. IP가 할당된 인터페이스
2. en* 물리 인터페이스 (주 인터페이스 en0을 첫 항목으로 정렬)
3. 가상 인터페이스만 제외한 전부

### 그 외

- 표기를 AA:BB:CC:DD:EE:FF 로 통일, 중복·무의미 값 제거
- 등록 직전 MAC이 비어 있으면 재수집하고, 그래도 없으면 사용자에게 확인 후 진행
- MAC 미수집 시 화면에 공란 대신 "(확인 불가 — 네트워크 연결 후 다시 실행 필요)" 표시
- 운영 포털 도메인 변경 (assetify-desk.vercel.app) — 기존 배포본도 리다이렉트로 계속 동작
- 앱과 포털 사이 공유키를 소스 코드에서 제거하고 빌드 시 실행 파일에 내장하는 방식으로 전환


## 💬 문의하기

문제가 발생하거나 문의사항이 있으시면 [여기](https://assetify-desk.vercel.app/request)를 클릭해주세요.

---

**버전**: v2.1.5
**릴리즈 날짜**: 2026-08-21T04:19:14Z
**라이선스**: Proprietary
