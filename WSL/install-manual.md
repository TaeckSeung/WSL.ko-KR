---
title: Linux 용 Windows 하위 시스템 (WSL) Distros를 수동으로 다운로드 합니다.
description: Linux 배포판에 대 한 Windows 하위 시스템을 수동으로 다운로드 하는 방법에 대 한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, WSL, windows 하위 시스템, 배포판, ubuntu, openSUSE, SLES, debian, kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: df47e656cf83e0b13aa8eb3f210e010d6a85bfd8
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269788"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Linux 배포판 패키지에 대 한 Windows 하위 시스템 수동으로 다운로드

Microsoft Store를 통해 WSL Linux 배포판을 설치 하거나 원하지 않는 몇 가지 시나리오가 있습니다. 특히 사용자 환경에서 Microsoft Store 사용을 허용 하지 않는 Microsoft Store 또는 회사 네트워크 정책 및/또는 관리자를 지원 하지 않는 Windows Server 또는 LTSC (장기 서비스) 데스크톱 OS SKU를 실행 하 고 있을 수 있습니다.

이러한 경우 WSL 자체를 사용할 수 있는 동안 스토어에 액세스할 수 없는 경우 WSL에서 Linux 배포판을 다운로드 하 여 설치 하는 방법

> 참고: **Cmd, PowerShell 및 Linux/WSL 배포판을 포함 하는 명령줄 셸 환경은 Windows 10 S 모드에서 실행할 수 없습니다**. 이러한 제한은 S 모드에서 제공 하는 무결성 및 보안 목표를 보장 하기 위해 존재 합니다. 자세한 내용은 [이 게시물](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) 을 참조 하세요.

## <a name="downloading-distros"></a>배포판 다운로드 중

Microsoft Store 앱을 사용할 수 없는 경우 다음 링크를 클릭 하 여 Linux 배포판을 다운로드 하 고 수동으로 설치할 수 있습니다.
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL 용 Fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

이렇게 하면 `<distro>.appx` 패키지가 선택한 폴더로 다운로드 됩니다. [설치 지침](#installing-your-distro) 에 따라 다운로드 한 배포판를 설치 합니다.

## <a name="downloading-distros-via-the-command-line"></a>명령줄을 통해 배포판 다운로드
원하는 경우 명령줄을 통해 기본 설정 배포판를 다운로드할 수도 있습니다.

 ### <a name="download-using-powershell"></a>PowerShell을 사용 하 여 다운로드
 PowerShell을 사용 하 여 배포판를 다운로드 하려면 [호출 WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet을 사용 합니다. Ubuntu 16.04을 다운로드 하는 샘플 지침은 다음과 같습니다.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 다운로드 시간이 오래 걸리는 경우을 설정 하 여 진행률 표시줄을 해제 합니다.`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>말아를 사용 하 여 다운로드
Windows 10 스프링 2018 업데이트 (이상)에는 명령줄에서 웹 요청 (예: HTTP GET, POST, PUT 등)을 호출할 수 있는 인기 있는 [말아 명령줄 유틸리티가](https://curl.haxx.se/) 포함 되어 있습니다. 를 사용 `curl.exe` 하 여 위의 배포판을 다운로드할 수 있습니다.

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

위의 예에서를 실행 하 `curl.exe` 는 것이 아니라, `curl`powershell에서 실제 말아 실행 파일을 호출 하 여 [호출-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) 에 대 한 powershell 말아 앨리어스가 아닌를 실행 하도록 합니다.

> 참고: Cmd `curl` shell 및/또는 `.bat`  /  스크립트를 사용 하 여 다운로드 단계를 호출/스크립팅 해야 하는 경우를 사용 하는 것이 좋습니다. `.cmd`

## <a name="installing-your-distro"></a>배포판 설치
Windows 10을 사용 하는 경우 PowerShell을 사용 하 여 배포판를 설치할 수 있습니다. 위에서 다운로드 한 배포판이 포함 된 폴더로 이동 하 고 해당 디렉터리에서 다음 명령을 실행 합니다. 여기서 `app_name` 는 배포판 파일의 이름입니다.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Windows server를 사용 하는 경우 [Windows server](install-on-server.md) 설명서 페이지에서 설치 지침을 찾을 수 있습니다.

배포판가 설치 되 면 [Intilization 단계](initialize-distro.md) 페이지를 참조 하 여 새 배포판를 초기화 합니다.
