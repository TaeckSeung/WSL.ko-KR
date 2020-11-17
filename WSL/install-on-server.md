---
title: Windows Server에 Linux 하위 시스템 설치
description: Windows Server에 Linux 하위 시스템을 설치하는 방법을 알아봅니다. WSL은 Windows Server 2019(버전 1709) 이상에 설치할 수 있습니다.
keywords: BashOnWindows, bash, wsl, windows, linux용 windows 하위 시스템, windows 하위 시스템, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 501bbf78c2d9f59dad945af9c30571317240b79f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866143"
---
# <a name="windows-server-installation-guide"></a>Windows Server 설치 가이드

Linux용 Windows 하위 시스템은 Windows Server 2019(버전 1709) 이상에 설치할 수 있습니다. 이 가이드에서는 컴퓨터에서 WSL을 사용하는 단계를 안내합니다.

## <a name="enable-the-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 사용

Windows에서 Linux 배포판을 실행하려면 먼저 "Linux용 Windows 하위 시스템" 옵션 기능을 사용하도록 설정하고 다시 부팅해야 합니다.

PowerShell을 관리자 권한으로 열어 실행합니다.

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

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
