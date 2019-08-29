---
title: 새 WSL Linux 배포판 초기화
description: WSL 용 Linux 배포판를 설치한 후 다음과 같은 간단한 단계에 따라 초기화를 완료 합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122711"
---
# <a name="initializing-a-newly-installed-distro"></a>새로 설치 된 배포판 초기화
배포판를 다운로드 하 여 설치한 후에는 새 배포판의 초기화를 완료 해야 합니다.

## <a name="launch-a-distro"></a>배포판 시작
새로 설치한 배포판의 초기화를 완료 하려면 새 인스턴스를 시작 합니다. Microsoft Store 앱에서 "시작" 단추를 클릭 하거나 시작 메뉴에서 배포판를 시작 하 여이 작업을 수행할 수 있습니다.

> 팁: 가장 자주 사용 되는 배포판을 시작 메뉴에 고정 하거나 작업 표시줄에 고정 하는 것이 좋습니다.

![시작 메뉴에서 배포판 시작](media/start-menu.png)

> Windows Server의 배포판 설치 폴더에서 배포판의 시작 관리자 실행 `<distro>.exe` 파일을 시작할 수 있습니다.

새로 설치 된 배포판를 처음 실행 하는 경우 콘솔 창이 열리고 1 분 또는 2 분 동안 기다렸다가 설치를 완료 하 라는 메시지가 표시 됩니다.

> 이 마지막 설치 단계에서 배포판의 파일은 압축 해제 되 고 PC에 저장 되며 사용할 준비가 됩니다. PC의 저장소 장치 성능에 따라 1 분 이상 걸릴 수 있습니다. 이 초기 설치 단계는 배포판을 새로 설치 하는 경우에만 필요 합니다. 이후의 모든 시작은 1 초 미만 소요 됩니다.

## <a name="setting-up-a-new-linux-user-account"></a>새 Linux 사용자 계정 설정

설치가 완료 되 면 새 사용자 계정 및 암호를 만들라는 메시지가 표시 됩니다. 

![Windows 콘솔의 Ubuntu 압축 풀기](media/UbuntuInstall.png)

이 사용자 계정은 배포판를 시작할 때 기본적으로 로그인 되는 관리자가 아닌 정규 사용자를 위한 것입니다.

> 원하는 사용자 이름 및 암호를 선택할 수 있습니다. Windows 사용자 이름에는 관계가 없습니다. 

새 배포판 인스턴스를 열 때 암호를 묻는 메시지가 표시 되지 않지만을 **사용 하 여 `sudo`프로세스를 승격 하는 경우 암호를 입력 해야**하므로 쉽게 기억할 수 있는 암호를 선택 해야 합니다. 자세한 내용은 [사용자 지원](user-support.md) 페이지를 참조 하세요.

## <a name="update--upgrade-your-distros-packages"></a>배포판 패키지 업데이트 & 업그레이드

대부분의 배포판은 빈/최소 패키지 카탈로그와 함께 제공 됩니다. 패키지 카탈로그를 정기적으로 업데이트 하 고 배포판의 기본 패키지 관리자를 사용 하 여 설치 된 패키지를 업그레이드 하는 것이 좋습니다. Debian/Ubuntu에서는 apt을 사용 합니다.

```bash
sudo apt update && sudo apt upgrade
```

> Windows는 Linux 배포판을 자동으로 업데이트 하거나 업그레이드 하지 않습니다. 이 작업은 Linux 사용자가 자신을 제어 하는 데 선호 하는 작업입니다.

모든 작업이 끝났습니다. WSL에서 새로운 Linux 배포판을 사용해 보세요! WSL에 대해 자세히 알아보려면 기타 [wsl 문서](https://aka.ms/wsldocs)또는 [wsl 학습 리소스 페이지](https://aka.ms/learnwsl)를 검토 합니다.

![WSL에서 Linux를 사용 하 여 이용](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>문제 해결

관련 오류 및 권장 픽스는 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [Wsl 문제 해결 페이지](troubleshooting.md) 를 참조 하세요.

> **0x8007007e 등 오류로 인해 설치 하지 못했습니다.** 시스템이 스토어에서 Linux를 지원 하지 않는 경우이 오류가 발생 합니다.  다음 사항을 확인합니다
> * Windows 빌드 16215 이상을 실행 하 고 있습니다. [빌드를 확인](troubleshooting.md#check-your-build-number)합니다.
> * Linux 용 Windows 하위 시스템 옵션 구성 요소가 사용 하도록 설정 되어 있고 컴퓨터가 다시 시작 되었습니다.  [WSL이 사용 하도록 설정 되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)합니다.
