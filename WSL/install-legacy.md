---
title: Windows 10 기념일 업데이트 또는 작성자 업데이트에서 설치 또는 제거
description: 레거시, beta 배포판 on Windows 10 기념일 업데이트 또는 작성자 업데이트에 대 한 설치 및 설치 취소 지침
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 레거시, 베타, 설치, 제거, 제거, 설치 취소, 삭제, 사용 되지 않음
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499268"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Windows 10 기념일 업데이트 및 작성자 업데이트에서 Linux 용 Windows 하위 시스템을 설치 또는 제거 하는 방법에 대 한 가이드 

Windows 10 크리에이터 업데이트 이상을 실행 하 [는 경우 windows 10 설치 지침을 따르세요](install-win10.md).

<strong><em><span style="color: #f28014">다음 지침은 Windows 10 기념일 업데이트 또는 Windows 10 크리에이터 스 업데이트를 실행 하는 사용자를 위한 것입니다.</span></em></strong>

Windows 10 구성 작성자 업데이트 (버전 1709) 이전에는 WSL이 베타 기능으로 출시 되었으며 "Windows의 Bash에서 Bash" (또는 Bash)가 처음 실행 될 때 단일 Ubuntu 인스턴스가 설치 되었습니다.

> 이전 Windows 10 릴리스에서는 WSL을 사용할 수 있지만이 베타 "legacy 배포판"는 이제 사용 되지 않는 것으로 간주 됩니다. 사용 가능한 Windows 10의 최신 버전을 실행 하는 것이 좋습니다. 각각의 새로운 Windows 10 릴리스에는 WSL의 수많은 수정 및 향상 기능이 포함 되어 있으므로 WSL에서 더 많은 Linux 도구와 앱을 제대로 실행할 수 있습니다.

을 (를) 작성자 업데이트 이상으로 업그레이드할 수 없는 경우 다음 단계에 따라 WSL을 사용 하도록 설정 하 고 사용 합니다.

1. 개발자 모드를 사용 하 여 Windows 10 기념일 업데이트 또는 작성자 업데이트에서 WSL 실행: 개발자 모드를 사용 하도록 설정 해야 합니다.

    **개발자를 위한** 개방형 **설정** -> **업데이트 및 보안** -> 

    개발자 모드 라디오 단추를 선택 합니다.  
    ![개발자 모드 사용](media/updateAndSecurity.png)

    > 개발자 모드를 사용 하도록 설정 해야 하는 요구 사항이 [Windows 10의 작성자 업데이트에서 제거](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/) 되었습니다.

1. 명령 프롬프트를 엽니다.  을 `bash` 입력 하 고 enter 키를 누릅니다.

    Windows에서 Ubuntu의 Bash를 처음 실행 하면 정식 라이선스를 허용 하 라는 메시지가 표시 됩니다. 동의 하면 WSL에서 Ubuntu 인스턴스를 다운로드 하 여 컴퓨터에 설치 합니다. 그러면 "Windows의 Bash에서 Bash" 바로 가기가 시작 메뉴에 추가 됩니다.

    ![Ubuntu 설치 확인](media/bashShellInstall.png)

    Windows에서 Ubuntu의 Bash를 처음 실행 하면 UNIX 사용자 이름 및 암호를 만들라는 메시지가 표시 됩니다. [새 배포판 인스턴스 지침](initialize-distro.md) 에 따라 설치를 완료 합니다.

1. 다음 중 하나를 수행 하 여 새 Ubuntu 셸을 시작 합니다.
    * 명령 `bash` 프롬프트에서 실행
    * 시작 메뉴 "Windows의 Ubuntu에서 Bash" 바로 가기를 클릭 합니다.

    
## <a name="uninstallingremoving-the-legacy-distro"></a>레거시 배포판 제거/제거
WSL을 설치한 이전 버전의 Windows 10에서 Windows 10의 손상 작성자 업데이트로 업그레이드 하는 경우 기존 배포판는 그대로 유지 됩니다. 그러나 새로운 매장 제공 배포판 ASAP를 설치 하 고 필요한 파일, 데이터 등을 레거시 배포판에서 새 배포판로 마이그레이션해야 합니다.

컴퓨터에서 레거시 배포판을 제거 하려면 명령줄 또는 PowerShell 인스턴스에서 다음을 실행 합니다.

```console
wsl --unregister Legacy
```

Windows 버전 1903 이상을 사용 하지 않는 경우 또는 `wslconfig /u Legacy` `lxrun /uninstall /full` 를 대신 실행 해야 할 수 있습니다. 

### <a name="manually-deleting-the-legacy-distro"></a>레거시 배포판 수동 삭제
원하는 경우 레거시 인스턴스를 수동으로 삭제할 수 있습니다. 이는를 사용 하 여 레거시 배포판을 제거 하 `lxrun.exe`는 데 문제가 발생 하거나와 함께 `lxrun.exe`제공 되지 않는 Windows 10 스프링 2018 업데이트 (이상)를 실행 하는 경우에 필요할 수 있습니다.

레거시 wsl 배포판을 강제로 삭제 하려면 Windows의 파일 `%localappdata%\lxss\` 탐색기 또는 명령줄을 사용 하 여 폴더 및 모든 하위 콘텐츠를 삭제 합니다.

PowerShell 사용
```powershell
rm -Recurse $env:localappdata/lxss/
```

Cmd 사용:
```console
DEL /S %localappdata%\lxss\
```
