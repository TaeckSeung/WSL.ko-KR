---
title: Windows Server에서 Linux 하위 시스템을 설치
description: Windows Server에서 Linux 하위 시스템에 대 한 설치 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, windows server 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 25723395212575f8fe2dcbfbd30b59de9431816a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035070"
---
# <a name="windows-server-installation-guide"></a>Windows Server 설치 가이드

> 이상 Windows Server 2019에 적용 됩니다.

/ / Linux 용 Windows 하위 시스템 되도록 Build2017, Microsoft 발표 [Windows Server에서 사용할 수 있는](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)합니다.  이러한 지침은 Windows Server 1709 이상 Linux 용 Windows 하위 시스템을 실행 안내 합니다.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Linux (WSL) 용 Windows 하위 시스템을 사용 하도록 설정

Windows에서 Linux 배포판을 실행할 수 있습니다, 전에 "Windows 하위 시스템에 대 한 Linux" 선택적 기능을 사용 하도록 설정 하 고 다시 부팅 해야 합니다.

1. 관리자 권한으로 PowerShell을 열고 실행 합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시 되 면 컴퓨터를 다시 시작 합니다. **이 다시 부팅 해야** WSL 신뢰할 수 있는 실행 환경을 시작할 수 있도록 합니다.

## <a name="download-a-linux-distro"></a>Linux 배포판을 다운로드 합니다.

따릅니다 [이러한 지침](install-manual.md) 원하는 Linux 배포를 다운로드 합니다.

## <a name="extract-and-install-a-linux-distro"></a>압축을 풀고 Linux 배포판을 설치 합니다.
배포판을를 다운로드 한 했으므로 해당 내용을 추출 하 고 수동으로 배포판을 설치 합니다.

1. 추출 된 `<distro>.appx` 예: PowerShell을 사용 하 여 패키지의 내용:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. 명명 된 설치를 완료 하려면 대상 폴더에서 배포판 시작 관리자 응용 프로그램을 실행 배포판 시작 관리자를 실행 `<distro>.exe`합니다. 예를 들어: `ubuntu.exe`등입니다.

    ![Windows Server에서 확장 된 Ubuntu 배포판](media/server-appx-expand.png)

    > **문제 해결**
    > * **0x8007007e 오류로 설치 하지 못했습니다.** : 이 오류는 시스템 WSL를 지원 하지 않습니다 하는 경우에 발생 합니다. 다음 사항을 확인하세요.
    >   * 16215 이상 Windows 빌드를 실행 하는 합니다. [빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.
    >   * Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용 하도록 설정 하 고 컴퓨터 다시 시작 합니다.  [WSL를 사용할 수 있는지](troubleshooting.md#confirm-wsl-is-enabled)합니다.
    
3. Windows 환경 경로에 배포판 경로 추가 (`C:\Users\Administrator\Ubuntu` 이 예제의), 예: Powershell을 사용 하 여:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    입력 하 여 이제 모든 경로에서 배포를 시작할 수 있습니다 `<distro>.exe`합니다. 예: `ubuntu.exe`

이제 Linux 배포를 설치 해야 [새 배포판 인스턴스를 초기화](initialize-distro.md) 배포를 사용 하기 전에 합니다.
