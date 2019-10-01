---
title: 새 WSL Linux 배포판 초기화
description: WSL용 Linux 배포판이 설치되면 여기에 나와 있는 간단한 단계에 따라 초기화를 완료합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122711"
---
# <a name="initializing-a-newly-installed-distro"></a>새로 설치된 배포판 초기화
배포판을 다운로드하여 설치한 후에는 새 배포판의 초기화를 완료해야 합니다.

## <a name="launch-a-distro"></a>배포판 시작
새로 설치한 배포판의 초기화를 완료하려면 새 인스턴스를 시작합니다. 이 작업은 Microsoft Store 앱에서 "시작" 단추를 클릭하거나 시작 메뉴에서 배포판을 시작하여 수행할 수 있습니다.

> 팁: 가장 자주 사용하는 배포판을 시작 메뉴 및/또는 작업 표시줄에 고정하는 것이 좋습니다!

![시작 메뉴에서 배포판 시작](media/start-menu.png)

> Windows 서버의 경우 배포판의 설치 폴더에서 배포판의 시작 관리자 실행 파일인 `<distro>.exe`를 시작할 수 있습니다.

새로 설치한 배포판이 처음 실행되면 콘솔 창이 열리고, 설치가 완료될 때까지 1~2분 정도 기다리라는 메시지가 표시됩니다.

> 이 설치의 마지막 단계에서 배포판의 파일이 압축 해제되고 PC에 저장되어 사용할 준비가 됩니다. 이 경우 PC의 스토리지 디바이스 성능에 따라 약 1분 이상이 걸릴 수 있습니다. 이 초기 설치 단계는 배포판을 새로 설치하는 경우에만 필요하며, 이후의 모든 시작에는 1초 미만이 걸립니다.

## <a name="setting-up-a-new-linux-user-account"></a>새 Linux 사용자 계정 설정

설치가 완료되면 새 사용자 계정(및 해당 암호)을 만들라는 메시지가 표시됩니다. 

![Windows 콘솔에서 Ubuntu 압축 풀기](media/UbuntuInstall.png)

이 사용자 계정은 배포판을 시작할 때 기본적으로 로그인되는 관리자가 아닌 일반 사용자를 위한 것입니다.

> 원하는 사용자 이름과 암호를 선택할 수 있으며, Windows 사용자 이름과는 관련이 없습니다. 

새 배포판 인스턴스를 열면 암호를 입력하라는 메시지가 표시되지 않지만, **`sudo`를 사용하여 프로세스를 관리자 권한으로 실행하는 경우** 암호를 입력해야 하므로 쉽게 기억할 수 있는 암호를 선택해야 합니다! 자세한 내용은 [사용자 지원](user-support.md) 페이지를 참조하세요.

## <a name="update--upgrade-your-distros-packages"></a>배포판 패키지 업데이트 및 업그레이드

대부분의 배포판에는 비어 있거나 최소한의 패키지 카탈로그가 제공됩니다. 배포판의 기본 설정 패키지 관리자를 사용하여 정기적으로 패키지 카탈로그를 업데이트하고 설치된 패키지를 업그레이드하는 것이 좋습니다. Debian/Ubuntu에서는 apt를 사용합니다.

```bash
sudo apt update && sudo apt upgrade
```

> Windows에서는 Linux 배포판을 자동으로 업데이트하거나 업그레이드하지 않습니다. 이는 Linux 사용자가 직접 제어하는 것을 선호하는 작업입니다.

작업을 완료했습니다. WSL에서 새 Linux 배포판을 사용해 보세요! WSL에 대해 자세히 알아보려면 다른 [WSL 문서](https://aka.ms/wsldocs) 또는 [WSL 학습 리소스 페이지](https://aka.ms/learnwsl)를 검토하세요.

![WSL에서 Linux 사용](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>문제 해결

관련 오류 및 제안된 수정 사항은 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

> **0x8007007e 오류로 인한 설치 실패** 이 오류는 시스템에서 스토어의 Linux를 지원하지 않을 때 발생합니다.  다음 사항을 확인하세요.
> * Windows 빌드 16215 이상을 실행하고 있습니다. [빌드를 확인](troubleshooting.md#check-your-build-number)하세요.
> * Linux용 Windows 하위 시스템의 선택적 구성 요소가 사용하도록 설정되어 있고 컴퓨터가 다시 시작되었습니다.  [WSL이 사용하도록 설정되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)하세요.
