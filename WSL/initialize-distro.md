---
title: 새 WSL Linux 배포판을 초기화 합니다.
description: WSL에 대 한 Linux 배포판을 설치한 후 다음과 같은 간단한 단계에서 초기화를 완료
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902050"
---
# <a name="initializing-a-newly-installed-distro"></a>새로 설치 된 배포판을 초기화합니다.
배포를 다운로드 하 고 설치 된 후 새 배포판의 초기화를 완료 해야 합니다.

## <a name="launch-a-distro"></a>배포판을 시작 합니다.
새로 설치 된 배포의 초기화를 완료 하려면 새 인스턴스를 시작 합니다. Windows 스토어 앱의 경우 "시작" 단추를 클릭 하거나 시작 메뉴에서 배포판을 실행 하 여이 수행할 수 있습니다.

> 팁:  사용자 가장 자주 사용 되는 배포판 하 여 시작 메뉴 및/또는 작업 표시줄에 고정할 수도 있습니다!

![시작 메뉴에서 배포를 시작 합니다.](media/start-menu.png)

> Windows Server에서 실행 파일 배포의 시작 관리자를 시작할 수 있습니다 `<distro>.exe` 배포판 설치 폴더에서.

처음 새로 설치 된 배포판을 실행, 콘솔 창이 열리고 되며 설치가 완료에 대 일 분 정도 대기 하 라는 메시지가 나타납니다.

> 설치의이 최종 단계 동안 배포판의 파일 압축 해제 되어 pc에서는 사용할 수 있도록 저장 합니다. 관련 저장소 장치를 PC의 성능에 따라 1 분 이상 걸릴 수 있습니다. 이 초기 설치 단계는만 정리-설치 됨-배포판을 때 필요한 모든 향후 출시 취해야 1 초 미만입니다.

## <a name="setting-up-a-new-linux-user-account"></a>새 Linux 사용자 계정 설정

설치가 완료 되 면 새 사용자 계정 (및 해당 암호)을 만들려면 묻는 메시지가 나타납니다. 

![Windows 콘솔에서 압축을 푼 Ubuntu](media/UbuntuInstall.png)

이 사용자 계정은 수 있음을 기록 기능에서 기본적으로는 배포판을 시작할 때 관리자가 아닌 일반 사용자에 대 한입니다.

> 모든 사용자 이름 및 암호로 선택할 수 있습니다-Windows 사용자 이름을 관계가 없습니다. 

새 배포판 인스턴스를 열면 않습니다 묻는 암호를 하지만 **를 사용 하 여 프로세스를 권한 상승 하는 경우 `sudo`, 암호를 입력 해야**쉽게 기억할 수 있는 암호 선택 해야 하므로,! 참조 된 [사용자 지원](user-support.md) 자세한 내용은 페이지입니다.

## <a name="update--upgrade-your-distros-packages"></a>업데이트 및 배포판의 패키지를 업그레이드 합니다.

대부분의 배포판 빈/최소 패키지 카탈로그를 제공 합니다. 패키지 카탈로그를 정기적으로 업데이트 및 배포판의 기본 패키지 관리자를 사용 하 여 설치 된 패키지를 업그레이드는 것이 좋습니다. Debian/Ubuntu에 apt를 사용 하면:

```bash
sudo apt update && sudo apt upgrade
```

> Windows는 자동으로 업데이트 하거나 Linux distro(s) 프로그램 업그레이드: Linux 사용자 자체를 제어 하는 것을 선호 하는 작업입니다.

모든 작업이 끝났습니다. WSL에서 새 Linux 배포를 사용 하 여을 즐겨보세요! WSL에 대 한 자세한 내용은 다른 검토 [WSL docs](https://aka.ms/wsldocs), 또는 [학습 리소스 페이지 WSL](https://aka.ms/learnwsl)합니다.

![WSL에서 Linux를 사용 하 여 이용할 수 있습니다.](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>문제 해결

다음은 관련된 오류 및 제안 된 수정 합니다. 참조 된 [WSL 문제 해결 페이지](troubleshooting.md) 다른 일반적인 오류 및 해결 방법에 대 한 합니다.

> **0x8007007e 오류로 설치 하지 못했습니다.** 시스템 저장소에서 Linux를 지원 하지 않습니다 하는 경우이 오류가 발생 합니다.  다음 사항을 확인하세요.
> * 16215 이상 Windows 빌드를 실행 하는 합니다. [빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.
> * Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용 하도록 설정 하 고 컴퓨터 다시 시작 합니다.  [WSL를 사용할 수 있는지](troubleshooting.md#confirm-wsl-is-enabled)합니다.
