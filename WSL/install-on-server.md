---
title: Windows Server에 Linux 하위 시스템 설치
description: Windows Server에 Linux 하위 시스템을 설치하는 방법에 대한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux용 windows 하위 시스템, windows 하위 시스템, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256396"
---
# <a name="windows-server-installation-guide"></a>Windows Server 설치 가이드

> 적용 대상: Windows Server 2019 이상

Microsoft는 Build 2017에서 Linux용 Windows 하위 시스템을 [Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)에서 사용할 수 있게 될 것이라고 발표했습니다.  이 지침에서는 Windows Server 1709 이상에서 Linux용 Windows 하위 시스템을 실행하는 과정을 안내합니다.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Linux용 Windows 하위 시스템 사용(WSL)

Windows에서 Linux 배포판을 실행하려면 먼저 "Linux용 Windows 하위 시스템" 옵션 기능을 사용하도록 설정하고 다시 부팅해야 합니다.

1. PowerShell을 관리자 권한으로 열어 실행합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시되면 컴퓨터를 다시 시작합니다. WSL이 신뢰할 수 있는 실행 환경을 시작할 수 있도록 하려면 **시스템을 다시 부팅해야 합니다**.

## <a name="download-a-linux-distro"></a>Linux 배포판 다운로드

[이 지침](install-manual.md)을 따라 즐겨 사용하는 Linux 배포판을 다운로드하세요.

## <a name="extract-and-install-a-linux-distro"></a>Linux 배포판 추출 및 설치
배포판을 다운로드했으므로 이제 콘텐츠를 추출하고 배포판을 수동으로 설치합니다.

1. `<distro>.appx` 패키지의 콘텐츠를 추출합니다. PowerShell을 사용한 예는 다음과 같습니다.

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. 배포판 시작 관리자를 실행합니다. 설치를 완료하려면 `<distro>.exe`라는 대상 폴더에서 배포판 시작 관리자 애플리케이션을 실행합니다. 예를 들어 `ubuntu.exe` 등이 있습니다.

    ![Windows Server의 확장된 Ubuntu 배포판](media/server-appx-expand.png)

    > **문제 해결**
    > * **0x8007007e 오류로 인한 설치 실패**: 이 오류는 시스템에서 WSL을 지원하지 않을 때 발생합니다. 다음 사항을 확인하세요.
    >   * Windows 빌드 16215 이상을 실행하고 있습니다. [빌드를 확인](troubleshooting.md#check-your-build-number)하세요.
    >   * Linux용 Windows 하위 시스템의 선택적 구성 요소가 사용하도록 설정되어 있고 컴퓨터가 다시 시작되었습니다.  [WSL이 사용하도록 설정되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)하세요.
    
3. Windows 환경 경로(이 예에서는 `C:\Users\Administrator\Ubuntu`)에 배포판 경로를 추가합니다. PowerShell을 사용한 예는 다음과 같습니다.
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    이제 `<distro>.exe`를 입력하여 모든 경로에서 배포판을 시작할 수 있습니다. 예를 들면 다음과 같습니다. `ubuntu.exe`

이제 Linux 배포판이 설치되었으므로 배포판을 사용하기 전에 [새 배포판 인스턴스를 초기화](initialize-distro.md)해야 합니다.
