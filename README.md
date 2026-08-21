# 대웅그룹 PC 자산관리 프로그램

> Windows PC 스캐닝 · macOS 자산실사 — 시스템 정보/보안/설치 프로그램을 스캔하고 자산을 실사하는 통합 도구

## 📥 다운로드

**최신 버전**: [v2.2.1](https://github.com/qortmddbs33/windows_recreate/releases/tag/v2.2.1)

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

## 공용PC를 이름 규칙 대신 체크박스로 받습니다

지금까지 공용PC는 이름을 "용도_담당자이름_공용"(예: 회의실예약_홍길동_공용) 형식으로
적도록 안내했습니다. 사람 칸에 사람이 아닌 값이 들어가서, 실사 진행률의 조직도 명단
대조(이메일 → 법인+이름)에서 해당 제출이 어느 조직에도 붙지 않고 조용히 버려졌습니다.

이제 **[공용PC] 체크박스 + 용도/위치 입력**으로 받습니다. 이름·이메일은 관리 담당자의
것을 그대로 적으면 됩니다.

- 체크하면 용도/위치가 필수입니다 (겸직/쉐어드의 원소속법인과 같은 규칙)
- 겸직/쉐어드와는 다른 개념이라 별도 항목입니다 — 겸직은 사람이 두 법인 일을 겸하는
  것이고, 공용PC는 자산을 여럿이 함께 쓴다는 뜻입니다
- Windows·macOS 양쪽 적용

포털은 이 항목을 안 보내도 기본값으로 받으므로, 이 버전이 퍼지기 전의 구버전 제출도
그대로 동작합니다.

### UI 정리

- 체크박스 문구가 입력 영역을 넘겨 잘려 보이던 문제 수정 ("공용PC입니다." 로 단축)
- 안내문·진입 팝업의 버튼 표기를 실제 라벨과 일치시킴 ([공용PC])
- macOS 안내문에 옛 이름 규칙이 그대로 남아 있던 문제 수정, 누락 항목 추가
- macOS 창 세로 크기 확대 (항목이 늘어 하단이 잘렸음)

### 빌드

- 빌드 스크립트가 1종만 구울 때 다른 산출물을 지워버리던 문제 수정

---

이전 버전(v2.1.5)의 네트워크 미연결 시 MAC 주소 누락 수정도 포함되어 있습니다.


## 💬 문의하기

문제가 발생하거나 문의사항이 있으시면 [여기](https://assetify-desk.vercel.app/request)를 클릭해주세요.

---

**버전**: v2.2.1
**릴리즈 날짜**: 2026-08-21T06:14:51Z
**라이선스**: Proprietary
