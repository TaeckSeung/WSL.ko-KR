---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0220d642854f9fc7fe2a85357ad2e70e0b888ed8
ms.sourcegitcommit: f878e88921d36e01e32624a9c60ee9de3d706a2e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69620094"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2의 설치 지침

WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.

- WSL이 설치 되어 있는지 확인 하 고 ( [여기](./install-win10.md)에서 작업을 수행 하기 위한 지침을 찾을 수 있음) Windows 10 빌드 18917 이상을 실행 하 고 있는지 확인 합니다.
- '가상 머신 플랫폼' 옵션 구성 요소 사용
- 명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정
- Distro가 사용 중인 WSL 버전 확인

## <a name="enable-the-virtual-machine-platform-optional-component"></a>'가상 머신 플랫폼' 옵션 구성 요소 사용

관리자 권한으로 PowerShell을 열어 실행합니다.

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

이러한 변경 내용을 사용한 후에는 컴퓨터를 다시 시작해야 합니다.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정

PowerShell에서 실행하고

`wsl --set-version <Distro> 2`

`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다. (`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.) 위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.

`wsl --set-default-version 2`

이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.

Distro가 사용 중인 WSL의 버전을 확인하려면 다음 명령을 사용합니다.

`wsl --list --verbose` 또는 `wsl -l -v`

위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다. 이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다. 

## <a name="troubleshooting"></a>문제 해결: 

다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다. 기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

* **0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**
    * 컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다. 이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.
   
* **업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다. WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다. 전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.