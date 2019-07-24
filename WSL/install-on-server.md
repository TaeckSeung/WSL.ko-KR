---
title: Windows Server에 Linux 하위 시스템 설치
description: Windows Server의 Linux 하위 시스템에 대 한 설치 지침
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, windows server 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308796"
---
# <a name="windows-server-installation-guide"></a>Windows Server 설치 가이드

> Windows Server 2019 이상에 적용 됩니다.

Build2017에서 Microsoft는 [Windows Server에서](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)Linux 용 Windows 하위 시스템을 사용할 수 있다고 발표 했습니다.  이 지침에서는 Windows Server 1709 이상에서 Linux 용 Windows 하위 시스템을 실행 하는 과정을 안내 합니다.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Linux 용 Windows 하위 시스템 (WSL) 사용

Windows에서 Linux 배포판을 실행 하려면 먼저 "Linux 용 Windows 하위 시스템" 옵션 기능을 사용 하도록 설정 하 고 다시 부팅 해야 합니다.

1. 관리자 권한으로 PowerShell을 열고 다음을 실행 합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시 되 면 컴퓨터를 다시 시작 합니다. **이 다시 부팅은** wsl에서 신뢰할 수 있는 실행 환경을 시작할 수 있도록 하기 위해 필요 합니다.

## <a name="download-a-linux-distro"></a>Linux 배포판 다운로드

[다음 지침](install-manual.md) 에 따라 즐겨 사용 하는 Linux 배포를 다운로드 합니다.

## <a name="extract-and-install-a-linux-distro"></a>Linux 배포판 추출 및 설치
배포판를 다운로드 했으므로 이제 콘텐츠를 추출 하 고 배포판를 수동으로 설치 합니다.

1. `<distro>.appx` 패키지의 콘텐츠를 추출 합니다 (예: PowerShell 사용).

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. 배포판 시작 관리자를 실행 하 여 설치를 완료 하 고 라는 `<distro>.exe`대상 폴더에서 배포판 시작 관리자 응용 프로그램을 실행 합니다. 예: `ubuntu.exe`등

    ![Windows Server의 확장 된 Ubuntu 배포판](media/server-appx-expand.png)

    > **문제 해결**
    > * **0x8007007e 등 오류로 인해 설치 하지 못했습니다**. 이 오류는 시스템에서 WSL을 지원 하지 않을 때 발생 합니다. 다음 사항을 확인합니다
    >   * Windows 빌드 16215 이상을 실행 하 고 있습니다. [빌드를 확인](troubleshooting.md#check-your-build-number)합니다.
    >   * Linux 용 Windows 하위 시스템 옵션 구성 요소가 사용 하도록 설정 되어 있고 컴퓨터가 다시 시작 되었습니다.  [WSL이 사용 하도록 설정 되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)합니다.
    
3. Windows 환경 경로 (이 예에서는)에 배포판`C:\Users\Administrator\Ubuntu` 경로를 추가 합니다 (예: Powershell 사용).
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    이제를 입력 `<distro>.exe`하 여 모든 경로에서 배포판을 시작할 수 있습니다. 예: `ubuntu.exe`

이제 Linux 배포판가 설치 되었으므로 배포판를 사용 하기 전에 [새 배포판 인스턴스를 초기화](initialize-distro.md) 해야 합니다.
