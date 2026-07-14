# 대웅그룹 PC 자산관리 프로그램

> Windows PC 스캐닝 · macOS 자산실사 — 시스템 정보/보안/설치 프로그램을 스캔하고 자산을 실사하는 통합 도구

## 📥 다운로드

**최신 버전**: [v2.1.4](https://github.com/qortmddbs33/windows_recreate/releases/tag/v2.1.4)

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

## 변경사항
- **macOS**: 부서·이름 등 입력란에 한글을 입력할 때 조합 중인 **마지막 글자가 잘리던 문제 수정**
  - 원인: Avalonia의 TwoWay 텍스트 바인딩이 매 입력(keystroke)마다 소스로 값을 되돌려 쓰면서(write-back) macOS IME 조합(preedit) 세션을 리셋 → 아직 확정되지 않은 마지막 글자가 유실
  - 조치: 입력란(자산번호·부서·이름·이메일) 바인딩을 `UpdateSourceTrigger=LostFocus`로 변경(포커스 이탈, 즉 조합 확정 후에만 반영). 등록 버튼은 항상 활성 + 클릭 시 검증으로 변경해 마지막 필드 입력 직후에도 정상 동작.
- **Windows**: 변경 없음 (2.1.3 유지)

## 첨부 파일
- `Daewoong_AssetAudit-macOS-arm64-v2.1.4.dmg` — **macOS 자산실사** (Apple Silicon/ARM64 전용) · 운영 포털 전송본
  - ad-hoc 서명이라 첫 실행 시 Gatekeeper 경고가 뜹니다. DMG 안의 **"❗️먼저 읽어주세요 — 실행 방법.txt"** 안내(터미널 `xattr` / 우클릭→열기 / 시스템 설정)에 따라 실행해 주세요.
- `Daewoong_PC_Scan-v2.1.3.exe` — **Windows PC 스캐닝 프로그램** (v2.1.3, 이번 릴리즈에서 변경 없음)


## 💬 문의하기

문제가 발생하거나 문의사항이 있으시면 [여기](https://swportal.vercel.app/request)를 클릭해주세요.

---

**버전**: v2.1.4
**릴리즈 날짜**: 2026-07-14T07:44:10Z
**라이선스**: Proprietary
