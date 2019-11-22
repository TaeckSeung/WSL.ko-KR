---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309054"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2의 설치 지침

WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.

> WSL 2 is only available in Windows 10 builds 18917 or higher

- Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher
   - To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring. 
   - You can check your Windows version by opening Command Prompt and running the `ver` command.
- '가상 머신 플랫폼' 옵션 구성 요소 사용
- 명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정
- Distro가 사용 중인 WSL 버전 확인

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled

You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed. You can do that by running the following command in PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Please restart your machine to finish installing both components.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정

If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one. 

To set a distro please run: 

```
wsl --set-version <Distro> 2
```

`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다. (`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.) 위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.

```
wsl --set-default-version 2
```

이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.

To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):

`wsl --list --verbose` 또는 `wsl -l -v`

위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다. 이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다. 

## <a name="troubleshooting"></a>문제 해결: 

다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다. 기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

* **0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**
    * 컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다. 이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.
   
* **업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다. WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다. 전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.

* **The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**
    * Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.

* **The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.** 
    * Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error. Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt. 
