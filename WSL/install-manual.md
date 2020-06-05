---
title: WSL(Linux용 Windows 하위 시스템) 배포판을 수동으로 다운로드
description: Linux용 Windows 하위 시스템 배포판을 수동으로 다운로드하는 방법에 대한 지침입니다.
keywords: wsl, linux 용 windows 하위 시스템, 수동 설치, 수동으로 설치, microsoft store, windows 10, curl, Add-AppxPackage, 장기 서비스, LTSC
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 621b2619d6c62e0b6c4e53f7791fc587c1c8f878
ms.sourcegitcommit: 09f5eb0f6062642e5c86deb1f34307ce3429163a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2020
ms.locfileid: "84211719"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Linux용 Windows 하위 시스템 배포판 패키지를 수동으로 다운로드

Microsoft Store를 통해 WSL Linux 배포판을 설치할 수 없는 몇 가지 시나리오가 있습니다. 구체적으로 말하자면, 사용자가 Microsoft Store를 지원하지 않는 Windows Server 또는 LTSC(장기 서비스) 데스크톱 OS SKU를 실행하고 있거나, 회사 네트워크 정책 및/또는 관리자가 사용자 환경에서 Microsoft Store 사용을 허용하지 않는 경우입니다.

이 경우 WSL 자체는 사용할 수 있는데 스토어에 액세스할 수 없다면 어떻게 WSL에서 Linux 배포판을 다운로드하고 설치할까요?

> 참고: **Cmd, PowerShell 및 Linux/WSL 배포판을 포함한 명령줄 셸 환경은 Windows 10 S 모드에서 실행할 수 없습니다.** 이러한 제한은 S 모드에서 제공하는 무결성 및 보안 목표를 보장하기 위한 것입니다. 자세한 내용은 [이 게시물](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)을 참조하세요.

## <a name="downloading-distros"></a>배포판 다운로드

Microsoft Store 앱을 사용할 수 없는 경우 다음 링크를 클릭하여 Linux 배포판을 다운로드하고 수동으로 설치할 수 있습니다.
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix for WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

이렇게 하면 `<distro>.appx` 패키지가 선택한 폴더에 다운로드됩니다. [설치 지침](#installing-your-distro)에 따라 다운로드한 배포판을 설치합니다.

## <a name="downloading-distros-via-the-command-line"></a>명령줄을 통해 배포판 다운로드
원하는 경우 명령줄을 통해 기본 배포판을 다운로드할 수도 있습니다.

 ### <a name="download-using-powershell"></a>PowerShell을 사용하여 다운로드
 PowerShell을 사용하여 배포판을 다운로드하려면 [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-5.1) cmdlet을 사용합니다. Ubuntu 16.04를 다운로드하는 샘플 명령은 다음과 같습니다.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 다운로드가 오래 걸릴 경우 `$ProgressPreference = 'SilentlyContinue'`를 설정하여 진행률 표시줄을 비활성화하세요.

### <a name="download-using-curl"></a>curl을 사용하여 다운로드
Windows 10 Spring 2018 업데이트(및 그 이상 버전)에는 명령줄에서 웹 요청(예: HTTP GET, POST, PUT 등)을 호출하는 데 사용할 수 있는 대중적인 [curl 명령줄 유틸리티](https://curl.haxx.se/)가 포함되어 있습니다. `curl.exe`를 사용하여 위의 배포판을 다운로드할 수 있습니다.

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

위의 예에서는 PowerShell에서 [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)의 PowerShell curl 별칭이 아닌 실제 curl 실행 파일이 호출되도록 `curl`이 아닌 `curl.exe`가 실행됩니다.

> 참고: Cmd 셸 및/또는 `.bat` / `.cmd` 스크립트를 사용하여 다운로드 단계를 호출/스크립팅해야 하는 경우 `curl`을 사용하는 것이 좋습니다.

## <a name="installing-your-distro"></a>배포판 설치
Windows 10을 사용하는 경우 PowerShell을 사용하여 배포판을 설치할 수 있습니다. 위에서 다운로드한 배포판이 포함된 폴더로 이동하고 해당 디렉터리에서 다음 명령을 실행합니다. 여기서 `app_name`은 배포판 .appx 파일의 이름입니다.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Windows Server를 사용하는 경우 [Windows Server](install-on-server.md) 설명서 페이지에서 설치 지침을 확인할 수 있습니다.

배포가 설치되면 일반 지침에 따라 [WSL 2로 업데이트](./install-win10.md#update-to-wsl-2)하거나 [새 사용자 계정 및 암호 작성](./user-support.md)을 수행하세요.
