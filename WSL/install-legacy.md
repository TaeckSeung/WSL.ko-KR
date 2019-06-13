---
title: 설치 또는 Windows 10 1 주년 업데이트 또는 크리에이터 스 업데이트에서 제거
description: 레거시, Windows 10 1 주년 업데이트 또는 크리에이터 스 업데이트에서 베타 배포판에 대 한 지침을 설치 및 제거
keywords: 설치, 제거, 취소-설치, 제거 BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10, 레거시, 베타, 용 windows 하위 시스템 삭제에 사용 되지 않음
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040841"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>설치 또는 Windows 10 1 주년 업데이트 및 크리에이터 업데이트의 Linux 용 Windows 하위 시스템을 제거 하는 가이드 

Windows 10 크리에이터 스 업데이트를 실행 하는 하거나 나중에 하세요 [Windows 10 설치 지침을 따릅니다](install-win10.md)합니다.

<strong><em><span style="color: #f28014">다음 지침은 Windows 10 1 주년 업데이트 또는 Windows 10 크리에이터 스 업데이트를 실행 하는 사용자에 대 한</span></em></strong>

Windows 10 Fall Creators Update (버전 1709), WSL 베타 기능으로 릴리스된 전과 "Bash에서 Ubuntu의 Windows" (또는 Bash.exe)를 처음 실행할 때 단일 Ubuntu 인스턴스를 설치 합니다.

> WSL를 사용 하 여 이전 Windows 10 버전에이 베타 "레거시 배포판" 이제 사용 되지 않는 간주 됩니다. 사용 가능한 Windows 10의 최신 버전을 실행 하려면 좋습니다. 각각의 새 Windows 10 릴리스 WSL 단독으로 Linux 도구 및 WSL에서 올바르게 실행 되도록 앱을 더 수정 및 개선 사항에 수백 개의 포함 합니다.

Fall Creators Update 이상을 업그레이드할 수 없는 경우, 설정 및 WSL를 사용 하려면 다음 단계를 수행 합니다.

1. 개발자 모드에서 실행 되도록 WSL Creators Update 또는 Windows 10 1 주년 업데이트 설정, 개발자 모드가 사용 하도록 설정 해야 합니다.

    오픈 **설정을** -> **업데이트 및 보안** -> **개발자를 위한**

    개발자 모드 라디오 단추를 선택 합니다.  
    ![개발자 모드 사용](media/updateAndSecurity.png)

    > 개발자 모드를 사용 하도록 설정 하는 요구 사항이 된 [Windows 10 Fall Creators Update 제거](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. 명령 프롬프트를 엽니다.  형식 `bash` 하 고 enter 키를 누릅니다

    처음에 Windows, Ubuntu에서 Bash를 실행 Canonical의 라이선스에 동의 하 라는 메시지가 표시 됩니다. WSL 다운로드 되 고 컴퓨터에 Ubuntu 인스턴스 설치에 동의 하 고 "Bash에서 Ubuntu의 Windows" 바로 가기를 시작 메뉴에 추가 됩니다.

    ![Ubuntu를 설치 하 라는 메시지가](media/bashShellInstall.png)

    처음에 Windows, Ubuntu에서 Bash를 실행 UNIX 사용자 이름 및 암호를 만들려고 라는 메시지가 표시 됩니다. 수행 합니다 [새 배포판 인스턴스 지침](initialize-distro.md) 설치를 완료 하려면

1. 새 Ubuntu 셸을 시작 합니다.
    * 실행 `bash` 명령 프롬프트에서
    * 시작 메뉴 "Bash에서 Ubuntu의 Windows" 바로 가기를 클릭합니다.

    
## <a name="uninstallingremoving-the-legacy-distro"></a>레거시 배포판 제거/제거
WSL 설치는 이전 Windows 10 버전의 Windows 10 Fall Creators Update 업그레이드 하면 기존 배포는 그대로 유지 됩니다. 그러나 강력한 새 저장소 제공 배포판 ASAP를 설치 하는 것이 좋습니다 하 고 레거시 배포에서 모든 필요한 파일, 데이터 등을 새 배포로 마이그레이션.

컴퓨터에서 레거시 배포판을 제거 하려면 다음 명령줄 또는 PowerShell 인스턴스에서 실행 합니다.

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>레거시 배포판을 수동으로 삭제
원한다 면 기존 인스턴스를 수동으로 삭제할 수 있습니다. 사용 하 여 레거시 배포판 제거 하는 문제가 발생 하는 경우 필요할 수 있습니다 `lxrun.exe`, 또는 Windows 10 Spring 2018 업데이트를 실행 하는 (또는 이상)와 함께 제공 되지 않는 `lxrun.exe`합니다.

레거시 WSL 배포를 강제로 삭제 하려면 삭제 된 `%localappdata%\lxss\` 폴더 (및 모든 하위 콘텐츠의) Windows의 파일 탐색기 또는 명령줄을 사용 하 여:

PowerShell 사용
```powershell
rm -Recurse $env:localappdata/lxss/
```

Cmd를 사용합니다.
```console
DEL /S %localappdata%\lxss\
```
