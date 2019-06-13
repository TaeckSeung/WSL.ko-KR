---
title: 수동으로 Windows 하위 시스템 (WSL) Linux 배포판에 대 한 다운로드
description: Linux 배포판에 대 한 Windows 하위 시스템을 수동으로 다운로드 하는 방법에 대 한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, WSL, 용 windows 하위 시스템 배포판, windows 하위 시스템, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 669c017c97aba70c107484b32acd99296265d84a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035029"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Linux 배포판의 패키지에 대 한 Windows 하위 시스템을 수동으로 다운로드

일부의 시나리오는 사용자 수 없습니다 수 (또는 원하는)을 설치 하려면 Microsoft Store 통해 WSL Linux 배포판입니다. 특히 있습니다 Windows Server 또는 장기 서비스 (LTSB/LTSC) 데스크톱 Microsoft Store 또는 사용자 회사 네트워크 정책 및/또는 관리자 환경에서 Microsoft Store 사용을 허용 하지 않으려면 지원 하지 않는 OS SKU를 실행할 수 있습니다.

이러한 경우에 WSL 자체를 사용할 수 있는, 어떻게 있습니다 다운로드 하 고 저장소에 액세스할 수 없으면 Linux 배포판 WSL 설치?

> 참고: **명령줄 셸 환경 Cmd, PowerShell 및/WSL Linux 배포판을 비롯 하 여 Windows 10 S 모드에서 실행 되도록 허용 되지 않습니다**합니다. 이 제한은 S 모드를 제공 하는 무결성 및 보안 목표를 보장 하기 위해 존재 합니다. 읽기 [이 게시물](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) 자세한 내용은 합니다.

## <a name="downloading-distros"></a>배포판을 다운로드합니다.

Microsoft Store 앱을 사용할 수 없는 경우 다운로드 하 고 이러한 링크를 클릭 하 여 Linux 배포판을 수동으로 설치할 수 있습니다.
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL에 대 한 fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

이렇게 하면는 `<distro>.appx` 선택한 폴더에 다운로드 하려면 패키지 있습니다. 수행 합니다 [설치 지침](#installing-your-distro) 에 다운로드 한 distro(s) 설치.

## <a name="downloading-distros-via-the-command-line"></a>명령줄을 통해 다운로드 배포판
원한다 면 명령줄을 통해 기본 distro(s)에도 다운로드할 수 있습니다.

 ### <a name="download-using-powershell"></a>PowerShell을 사용 하 여 다운로드
 PowerShell을 사용 하는 배포판을 다운로드 하려면 사용 합니다 [Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet. 다음은 Ubuntu 16.04를 다운로드 하는 샘플 명령입니다.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 다운로드 시간이 오래 걸리면, 설정 하 여 진행률 표시줄 해제 `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Curl을 사용 하 여 다운로드
Windows 10 Spring 2018 업데이트 (또는 이상)는 인기 있는 포함 [명령줄 유틸리티 curl](https://curl.haxx.se/) 는 사용 하 여 명령줄에서 웹 요청 (예: HTTP GET, POST, PUT, 명령 등)를 호출할 수 있습니다. 사용할 수 있습니다 `curl.exe` 위의 배포판을 다운로드 하려면:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

위의 예에서 `curl.exe` 실행 됩니다 (뿐만 아니라 `curl`), PowerShell에서 실제 curl 실행 파일 인지 확인 호출 별칭 PowerShell curl 없습니다 [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> 참고: 사용 하 여 `curl` Cmd 셸을 사용 하 여 다운로드 단계 호출/스크립트에 있는 경우에 좋을 수 있습니다 및/또는 `.bat`  /  `.cmd` 스크립트입니다.

## <a name="installing-your-distro"></a>배포를 설치합니다.
다운로드 한 distro(s) 프로그램을 설치 하는 방법에 지침을 참조 하십시오 합니다 [Windows 데스크톱](install-win10.md) 또는 [Windows Server](install-on-server.md) 설치 지침.
