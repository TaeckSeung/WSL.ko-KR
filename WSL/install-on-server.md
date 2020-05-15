---
title: Windows Server에 Linux 하위 시스템 설치
description: Windows Server에 Linux 하위 시스템을 설치하는 방법에 대한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux용 windows 하위 시스템, windows 하위 시스템, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270887"
---
# <a name="windows-server-installation-guide"></a>Windows Server 설치 가이드

Linux용 Windows 하위 시스템은 Windows Server 2019(버전 1709) 이상에 설치할 수 있습니다. 이 가이드에서는 컴퓨터에서 WSL을 사용하는 단계를 안내합니다.

## <a name="enable-the-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 사용

Windows에서 Linux 배포판을 실행하려면 먼저 "Linux용 Windows 하위 시스템" 옵션 기능을 사용하도록 설정하고 다시 부팅해야 합니다.

PowerShell을 관리자 권한으로 열어 실행합니다.

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

**100% 시스템 호출 호환성과 더 빠른 IO 성능을 찾고 있는 경우 아래 내용을 참조하여 WSL 2를 설치합니다!**

WSL 2는 Windows 10, 버전 2004, 빌드 19041 이상에서만 사용할 수 있습니다. 5월 하순 공개 릴리스까지 [Windows 버전을 업데이트](ms-settings:windowsupdate)하고, "릴리스 미리 보기" 링의 [Windows 참가자 프로그램에 참여](https://insider.windows.com/insidersigninboth/)해야 합니다.

**WSL 1을 계속 진행하는 경우 메시지가 표시되면 컴퓨터를 다시 시작하고 [여기](./install-on-server.md#download-a-linux-distribution)에서 설치를 계속합니다.**

## <a name="enable-the-virtual-machine-platform-optional-component"></a>가상 머신 플랫폼 옵션 구성 요소 사용

‘가상 머신 플랫폼’ 옵션 구성 요소가 설치되어 있는지 확인합니다. PowerShell에서 다음 명령을 실행하면 확인할 수 있습니다.

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a>Linux 배포 다운로드

[이 지침](install-manual.md)을 따라 즐겨 사용하는 Linux 배포판을 다운로드하세요.

## <a name="extract-and-install-a-linux-distribution"></a>Linux 배포 추출 및 설치

Linux 배포를 다운로드했으므로 콘텐츠를 추출하고 수동으로 설치하기 위해 다음 단계를 수행합니다.

1. PowerShell을 사용하여 `<distro>.appx` 패키지의 콘텐츠를 추출합니다.

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. 대상 폴더에서 배포 시작 관리자 애플리케이션을 실행합니다. 시작 프로그램의 이름은 일반적으로 `<distro>.exe`입니다(예: `ubuntu.exe`).

    ![Windows Server의 확장된 Ubuntu 배포판](media/server-appx-expand.png)

> [!CAUTION]
> **0x8007007e 오류로 인한 설치 실패**: 이 오류가 발생하는 경우 시스템에서 WSL을 지원하지 않습니다. Windows 빌드 16215 이상을 실행하고 있는 확인합니다. [빌드를 확인](troubleshooting.md#check-your-build-number)하세요. 또한 [WSL를 사용하는지](troubleshooting.md#confirm-wsl-is-enabled) 그리고 기능이 활성화된 후 컴퓨터를 다시 시작했는지 확인합니다.  

3. PowerShell을 사용하여 Windows 환경 경로(이 예에서는 `C:\Users\Administrator\Ubuntu`)에 배포판 경로를 추가합니다.

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

이제 `<distro>.exe`를 입력하여 모든 경로에서 배포를 시작할 수 있습니다. 예를 들면 `ubuntu.exe`와 같습니다.

이제 배포가 설치되었으므로 이를 사용하기 전에 [새 배포 인스턴스를 초기화](initialize-distro.md)해야 합니다.
