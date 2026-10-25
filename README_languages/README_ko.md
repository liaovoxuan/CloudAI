# CloudAI

CloudAI는 크로스 플랫폼 AI 어시스턴트입니다.

> **버전 1.0.1 상태:** Agent 모드는 여러 단계의 작업을 지원하며 애플리케이션 패키지는 기본적으로 ZIP 형식을 사용합니다. 이전 1.0.0 패키지는 [이전 버전 보관소](../Releases/Legacy/v1.0.0/)에 보관됩니다. [Agent 모드](../docs/AGENT_MODE.md)와 [HarmonyOS 제한 사항](../docs/HARMONYOS.md)을 참조하세요.

> **macOS:** 버전 1.0.1은 Intel과 Apple Silicon을 모두 지원하는 Universal 빌드를 사용하며, 보관된 1.0.0 패키지는 Apple Silicon(`arm64`)만 지원합니다.

## 기능

-   AI 대화
-   여러 단계 작업을 위한 Agent 모드
-   클라우드 AI API 연동
-   멀티 플랫폼 데스크톱 애플리케이션
-   다중 아키텍처 빌드
-   그래픽 인터페이스
-   다국어 지원

## Agent 모드

Agent 모드는 목표를 여러 단계로 나누고, 사용자가 활성화한 도구를 사용하며, 허용된 범위에서 변경을 수행하고 가능한 경우 결과를 검증할 수 있습니다. 이 모드 자체로 추가 권한이 부여되지는 않으며, 민감하거나 파괴적인 작업을 수행하기 전에 확인을 요청해야 합니다. 자세한 내용은 [Agent 모드 안내](../docs/AGENT_MODE.md)를 참조하세요.

## 지원 플랫폼

### 데스크톱

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### 기타 플랫폼

-   HarmonyOS
-   OpenHarmony

## 플랫폼 상세 정보

| 플랫폼 | 아키텍처 및 패키지 상태 | 설치 방법 및 제한 사항 |
| --- | --- | --- |
| Windows | 1.0.1은 x64와 ARM64를 대상으로 하며 기본적으로 ZIP을 사용합니다. 보관소에는 이전 1.0.0 x64 ZIP이 있습니다. | 실행 전에 ZIP을 완전히 압축 해제하세요. |
| Linux | 1.0.1은 x86_64와 ARM64를 대상으로 하며 기본적으로 ZIP을 사용합니다. 두 아키텍처의 1.0.0 패키지가 보관되어 있습니다. | ZIP에는 AppImage, DEB, RPM 또는 TAR.GZ가 포함될 수 있습니다. AppImage에는 실행 권한이 필요하며 DEB와 RPM은 패키지 관리자로 설치합니다. |
| macOS | 1.0.1은 Intel과 Apple Silicon용 Universal 빌드이며 기본적으로 ZIP으로 배포됩니다. 1.0.0은 Apple Silicon(`arm64`)만 지원합니다. | ZIP을 풀어 애플리케이션을 얻습니다. 서명되지 않아 macOS에서 직접 허용해야 할 수 있습니다. |
| HarmonyOS | 1.0.1은 기본적으로 ZIP으로 배포되며 안의 호환되는 서명된 HAP을 설치합니다. 보관된 1.0.0 HAP은 `2in1` 전용 debug 빌드입니다. | 이전 HAP은 API `60101024`를 대상으로 합니다. 호환 시스템과 유효한 서명이 필요합니다. [HarmonyOS 참고 사항](../docs/HARMONYOS.md)을 확인하세요. |
| OpenHarmony | 1.0.1은 기본적으로 ZIP으로 배포되며 안의 OpenHarmony 호환 HAP을 설치합니다. | 호환 서명과 실제 기기 테스트가 필요합니다. 보관된 HarmonyOS 1.0.0 HAP을 OpenHarmony 패키지로 사용하지 마세요. |

## 설치

### Linux

AppImage:

1.  기본 Linux ZIP 패키지를 다운로드하여 압축을 푼 다음 아키텍처에 맞는 AppImage를 선택합니다.
2.  실행 권한을 추가합니다:

``` bash
chmod +x CloudAI.AppImage
```

3.  애플리케이션을 실행합니다:

``` bash
./CloudAI.AppImage
```

Deb 패키지는 다음 명령으로 설치할 수 있습니다:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS 버전은 현재 Apple Developer 인증서로 서명되어 있지 않습니다.

처음 실행할 때 사용자는 macOS 보안 설정에서 애플리케이션을 직접 허용해야 할 수 있습니다.

### HarmonyOS

HarmonyOS 버전은 공식 HarmonyOS 개발 툴체인으로 빌드되었습니다.

개발과 패키징에는 DevEco Studio를 사용합니다. HarmonyOS 애플리케이션은 HAP/App 패키지로 빌드되며 배포 전에 적절한 서명 구성이 필요합니다.

## 라이선스

[MIT 라이선스](../LICENSE).

## 오픈 소스 프로젝트 파일

라이선스, 소스 코드 공개 상태, 기여 안내 및 프로젝트 정책은 [오픈 소스 프로젝트 정보](../docs/OPEN_SOURCE.md)를 참조하세요.

CloudAI 1.0.1 소스 트리 사본이 [`Source/CloudAI`](../Source/CloudAI/)에 추가되었습니다. 데스크톱 애플리케이션, Agent 및 플러그인 지원, 패키징 리소스와 HarmonyOS 프로젝트가 포함됩니다. 별도의 OpenHarmony HAP 프로젝트, 릴리스 산출물과 소스의 연결 정보, 잠긴 종속성 버전, 검증된 재현 가능 패키징 절차는 아직 제공되지 않습니다. 자세한 내용은 [오픈 소스 상태 검토](../docs/OPEN_SOURCE_STATUS.md)를 참조하세요.

## 개발자

Liao Boxuan

## 날짜

2026-09-13
