<div align="right">

[English](./README.md) · **한국어**

</div>

<div align="center">


**실제로 사용할 수 있는 데스크톱 애플리케이션과 AI 비서, 개발 도구를 만들고 검증합니다.**

C# / .NET · Python · Avalonia · PySide6 · Windows 및 크로스플랫폼 개발

[![GitHub](https://img.shields.io/badge/GitHub-DO0OG-181717?style=flat-square&logo=github)](https://github.com/DO0OG)
[![이메일](https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:laleme@naver.com)

[Ari](#대표-프로젝트) · [프로젝트](#주요-프로젝트) · [기술 구현](#기술-구현-및-검증) · [기술 스택](#기술-스택) · [연락처](#연락처-및-github-활동)

</div>

---

## 대표 프로젝트

Ari는 음성 상호작용과 PC 자동화를 결합한 Windows용 AI 데스크톱 비서로, 현재 가장 중점적으로 소개하는 오픈소스 프로젝트입니다.

### [Ari — AI 음성 비서 및 자율 데스크톱 에이전트](https://github.com/DO0OG/Ari-VoiceCommand)

**음성으로 PC와 대화하고 일상적인 작업을 처리하도록 만든 AI 비서입니다.**

**음성 상호작용, 로컬·원격 언어 모델, Windows 자동화와 도구 기반 작업 처리를 결합한 오픈소스 Windows 음성 비서입니다.**

`Python` `PySide6` `Ollama` `MCP` `STT/TTS` `AI Agent`

- 호출어 인식, 다국어 음성 인식과 음성 응답, 상호작용 가능한 데스크톱 캐릭터를 제공합니다.
- 로컬 LLM, 기억 기능, 플러그인, `SKILL.md` 스킬, Model Context Protocol(MCP) 연동을 지원합니다.
- 도구를 활용한 데스크톱 작업을 계획·실행·검증하고 진행 중인 작업을 중단할 수 있습니다.

[![Ari 최근 커밋](https://img.shields.io/github/last-commit/DO0OG/Ari-VoiceCommand?style=flat-square&label=updated)](https://github.com/DO0OG/Ari-VoiceCommand/commits/main)
[![Ari 릴리스](https://img.shields.io/github/v/release/DO0OG/Ari-VoiceCommand?style=flat-square&label=release)](https://github.com/DO0OG/Ari-VoiceCommand/releases/latest)
[![Ari 스타](https://img.shields.io/github/stars/DO0OG/Ari-VoiceCommand?style=flat-square)](https://github.com/DO0OG/Ari-VoiceCommand/stargazers)

**기술적 구현:** 음성 입력부터 명령 처리, 다단계 도구 실행, 선택 가능한 언어 모델과 MCP·플러그인 연동까지 연결했습니다. 로컬 모델을 지원하지만, 모든 설정이 완전한 오프라인 동작을 의미하는 것은 아닙니다.

**상세 문서:** [에이전트 작업 흐름](https://github.com/DO0OG/Ari-VoiceCommand/blob/main/docs/AGENT_ADVANCED.md) · [로컬 판단 엔진](https://github.com/DO0OG/Ari-VoiceCommand/blob/main/docs/LOCAL_DECISION_ENGINE.md) · [보안 안내](https://github.com/DO0OG/Ari-VoiceCommand/blob/main/docs/SECURITY.md)

[프로젝트 홈페이지](https://ari-voice-command.vercel.app) · [최신 릴리스 다운로드](https://github.com/DO0OG/Ari-VoiceCommand/releases/latest) · [사용 및 설치 안내](https://github.com/DO0OG/Ari-VoiceCommand#install)

<br/>

## 주요 프로젝트

다른 공개 프로젝트도 해결하려는 문제, 구현 방식, 확인 가능한 자료를 함께 정리했습니다.

### [AsterCache — HDD 게임 로딩 최적화](https://github.com/DO0OG/AsterCache)

**게임 전체를 SSD로 옮기지 않고, HDD에 설치된 게임을 반복 실행할 때 발생하는 디스크 탐색 부담을 줄이기 위해 개발 중인 Windows 11용 실험적 유틸리티입니다.**

`C#` `.NET 10` `Windows` `NTFS` `ETW` `RAM Cache`

- Windows 이벤트 추적(ETW)을 이용해 게임 실행 중 파일을 읽는 순서와 위치를 기록합니다.
- NTFS 데이터 재배치, 접근 순서 기반 미리 읽기(prefetch), RAM 프리워밍을 통해 이후 실행에서 데이터 접근 효율을 높이도록 설계했습니다.
- 게임 자동 탐지, 백그라운드 동작, 안전장치와 [공유 읽기 순서 프로필](https://github.com/DO0OG/AsterCache-profiles)을 지원합니다.

**문제와 접근 방식:** HDD에서 분산된 데이터 접근에 따른 탐색 부담을 줄이기 위해 ETW로 읽기 패턴을 수집하고, 제한적인 NTFS 재배치와 순서 기반 미리 읽기, RAM 프리워밍을 조합했습니다.

**검증 범위:** 기록된 디스크 I/O 재생 실험이며, 실제 게임 전체 로딩 시간 단축이 입증된 것은 아닙니다. 재배치 시 디스크 쓰기가 발생하므로 사용 전 중요한 데이터를 백업해야 합니다. [실험 결과와 한계](https://github.com/DO0OG/AsterCache/blob/main/docs/RESULTS_SUMMARY.ko.md) · [안티치트 주의사항](https://github.com/DO0OG/AsterCache/blob/main/docs/ANTICHEAT.ko.md)

[![AsterCache 최근 커밋](https://img.shields.io/github/last-commit/DO0OG/AsterCache?style=flat-square&label=updated)](https://github.com/DO0OG/AsterCache/commits/main)
[![AsterCache 릴리스](https://img.shields.io/github/v/release/DO0OG/AsterCache?style=flat-square&label=release)](https://github.com/DO0OG/AsterCache/releases/latest)
[![AsterCache 라이선스](https://img.shields.io/github/license/DO0OG/AsterCache?style=flat-square)](https://github.com/DO0OG/AsterCache/blob/main/LICENSE)

<sub>실험 단계의 성능 개선 프로젝트입니다. 기록된 디스크 읽기 패턴을 재생한 측정값만으로 실제 게임의 로딩 시간 단축이 입증되는 것은 아닙니다. 데이터 재배치 과정에서 HDD에 쓰기가 발생하므로, 중요한 데이터는 백업하고 호환성 및 주의사항을 먼저 확인해야 합니다.</sub>

<br/>

### [agk75-tool — AGK75 키보드 비공식 설정 도구](https://github.com/DO0OG/agk75-tool)

**Antgamer AGK75의 USB HID 통신 프로토콜을 분석해 개발한 비공식 데스크톱 설정 프로그램입니다.**

`Python` `PySide6` `HID API` `Device Configuration`

- 키 재배치, Fn 레이어, 프로필, 조명, 래피드 트리거 및 폴링레이트 설정을 지원합니다.
- 기기에서 설정값을 다시 읽어 적용 여부를 확인하며, 설정 백업·복원과 USB 폴링레이트 측정 기능을 제공합니다.
- 한국어·영어·중국어 간체 UI를 제공하며, 프로그램 사용에 네트워크 연결이 필요하지 않습니다.

**문제와 접근 방식:** 하드웨어 설정값을 안정적으로 변경할 수 있도록 AGK75의 USB HID 명령을 분석해 독립적으로 구현했습니다. 변경 후 기기에서 값을 다시 읽어 실제 적용 여부를 확인합니다.

**확인 가능한 자료:** 실제 설정 화면과 [설정·폴링레이트 측정 기록](https://github.com/DO0OG/agk75-tool/blob/main/README.md). 측정 결과는 유선 연결로 시험한 조건에 한정되며 모든 환경에서의 동작을 보장하지 않습니다.

[![AGK75 최근 커밋](https://img.shields.io/github/last-commit/DO0OG/agk75-tool?style=flat-square&label=updated)](https://github.com/DO0OG/agk75-tool/commits/main)
[![AGK75 라이선스](https://img.shields.io/github/license/DO0OG/agk75-tool?style=flat-square)](https://github.com/DO0OG/agk75-tool/blob/main/LICENSE)

<sub>Antgamer와 제휴하지 않은 비공식 프로젝트입니다. USB로 연결한 호환 AGK75 기기를 대상으로 합니다.</sub>

---

## 다른 프로젝트

### [CustomLauncher — 크로스플랫폼 Minecraft 런처](https://github.com/DO0OG/CustomLaucncher)

`C#`, `.NET 8`, `Avalonia`로 개발한 **Windows·macOS·Linux용 Minecraft 서버 런처 및 콘텐츠 배포 클라이언트**입니다.

- Microsoft/Xbox 계정 로그인 및 계정 관리
- 무결성을 검사하는 변경 파일 다운로드, 복구, 롤백, 모드·리소스팩 관리
- 다중 서버 설정, Forge/Fabric/NeoForge/Quilt 지원, 업데이트 기능

**기술적 구현:** Microsoft 인증, 무결성 검사 기반 변경 파일 다운로드, 파일 복구·롤백, 모드 로더 처리, 운영체제별 배포 흐름을 다룹니다. [운영자 가이드](https://github.com/DO0OG/CustomLaucncher/blob/main/docs/OPERATOR_GUIDE.ko.md) · [QA 검증 항목](https://github.com/DO0OG/CustomLaucncher/blob/main/docs/QA_MATRIX.ko.md)

[![CustomLauncher 최근 커밋](https://img.shields.io/github/last-commit/DO0OG/CustomLaucncher?style=flat-square&label=updated)](https://github.com/DO0OG/CustomLaucncher/commits/main)

<br/>

### [yttStudio — YouTube 자막 시각 편집기](https://github.com/DO0OG/yttStudio)

`C#`, `.NET 10`, `Avalonia` 기반의 크로스플랫폼 **YTT/SRV3 자막 WYSIWYG 편집기**입니다.

- 영상 미리보기 화면에서 자막의 위치와 스타일을 직접 편집
- 타임라인, 가라오케 타이밍, 다중 키프레임 애니메이션과 효과 지원
- YouTube 자막 포맷의 제약 조건 검사 및 스타일 자막 내보내기

**문제와 접근 방식:** 복잡한 YouTube 스타일 자막을 파일 내부 구조만으로 편집하기 어렵다는 문제를 영상 위 직접 편집, 타임라인, 가라오케 타이밍, 키프레임 효과로 해결하도록 설계했습니다.

**확인 가능한 자료:** [사용자 가이드](https://github.com/DO0OG/yttStudio/blob/main/docs/USER_GUIDE.md) · [포맷 검증 기록](https://github.com/DO0OG/yttStudio/blob/main/docs/YTT-VERIFICATION.md). 편집 미리보기는 실제 YouTube 렌더링과 차이가 있을 수 있습니다.

[![yttStudio 최근 커밋](https://img.shields.io/github/last-commit/DO0OG/yttStudio?style=flat-square&label=updated)](https://github.com/DO0OG/yttStudio/commits/main)
[![yttStudio 릴리스](https://img.shields.io/github/v/release/DO0OG/yttStudio?style=flat-square&label=release)](https://github.com/DO0OG/yttStudio/releases/latest)

---

## 기술 구현 및 검증

프로젝트별로 **어떤 문제를 해결하려 했고, 어떤 방식으로 구현했으며, 어디까지 검증했는지**를 확인할 수 있도록 정리했습니다.

| 기술 분야 | 저장소에서 확인할 수 있는 내용 |
| :--- | :--- |
| AI 및 도구 기반 에이전트 | Ari의 음성 입출력, 로컬·원격 언어 모델, MCP·도구 연동, 작업 결과 확인 |
| 운영체제 및 장치 I/O | AsterCache의 ETW·NTFS·Windows 파일 캐시 / agk75-tool의 USB HID와 설정값 재확인 |
| 크로스플랫폼 데스크톱 | yttStudio·CustomLauncher의 C#/.NET·Avalonia / Ari·agk75-tool의 Python·PySide6 |
| 안정성 및 복구 | AsterCache의 데이터 재배치 안전장치 / CustomLauncher의 무결성 검사·파일 복구·롤백 |
| 테스트 및 문서 | 프로젝트별 테스트, CI, 릴리스 배포, 사용 가이드와 검증 한계 기록 |

**검증 결과는 범위를 구분해 설명합니다.** 디스크 읽기 패턴을 재생한 실험 결과를 실제 게임 로딩 시간 개선으로 단정하지 않는 것처럼, 구현한 기능과 측정 결과, 추가 확인이 필요한 사항을 구분했습니다.

---

## 기술 스택

<div align="center">

**프로그래밍 언어**

![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

**데스크톱 및 인터랙티브 개발**

![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Avalonia](https://img.shields.io/badge/Avalonia-8B44AC?style=for-the-badge)
![PySide6](https://img.shields.io/badge/PySide6-41CD52?style=for-the-badge&logo=qt&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)

**개발 도구 및 시스템**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

## 관심 및 개발 분야

- **AI 비서와 에이전트 작업 흐름:** 음성 인터페이스, 로컬 모델, 도구 연동, 데스크톱 자동화
- **데스크톱 애플리케이션 개발:** 네이티브 UI, 크로스플랫폼 프로그램, 유지보수하기 쉬운 구조
- **성능 및 시스템:** 병목 측정, 디스크 I/O 개선, 효율적인 처리 방식 연구
- **소프트웨어 배포 및 품질:** 자동화 테스트, CI/CD, 설치 프로그램, 릴리스·업데이트·복구 흐름

---

## 이력

**서원대학교** · 컴퓨터공학 전공  
**대한상공회의소** · Unity 부트캠프

---

## 연락처 및 GitHub 활동

프로젝트 문의 및 협업 연락: **[이메일](mailto:laleme@naver.com)** · [GitHub](https://github.com/DO0OG)


<div align="center">

<a href="https://github.com/stats-organization/github-stats-extended">
  <img height="180" src="https://github-stats-extended.vercel.app/api?username=DO0OG&show_icons=true&hide_border=true&theme=transparent&include_all_commits=true&rank_icon=github" alt="DO0OG GitHub 활동 통계" />
</a>

</div>

---

<div align="center">

<sub>실용적인 소프트웨어를 만들고, 검증하고, 꾸준히 개선합니다.</sub>

</div>
