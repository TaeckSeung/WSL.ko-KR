---
title: WSL 2를 설치 합니다.
description: WSL 2에 대 한 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038083"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2에 대 한 설치 지침

설치 하 고 사용 하 여 시작 WSL 2는 다음 단계를 완료 합니다.

- ' 가상 컴퓨터 플랫폼 ' 선택적 구성 요소를 사용 하도록 설정
- WSL 2 명령줄을 사용 하 여 지원 되는 배포판 설정
- 사용할 WSL에 배포판의 버전 확인

## <a name="enable-the-virtual-machine-platform-optional-component"></a>' 가상 컴퓨터 플랫폼 ' 선택적 구성 요소를 사용 하도록 설정

관리자 권한으로 PowerShell을 열고 실행 합니다.

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

이러한 변경 내용을 사용 하도록 설정 된 후 컴퓨터를 다시 시작 해야 합니다.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>WSL 2 명령줄을 사용 하 여 지원 되는 배포판 설정

Powershell을 실행 합니다.

`wsl --set-version <Distro> 2`

바꿔야 및 `<Distro>` 배포의 실제 이름입니다. (이러한 명령을 사용 하 여 찾을 수 있습니다: `wsl -l`). 위와 동일한 명령을 실행 하지만 ' 2'와 ' 1'을 대체 하 여 언제 든 지에서 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2 기본 아키텍처를 확인 하려면이 명령을 사용 하 여 수행할 수 있습니다.

`wsl --set-default-version 2`

모든 이렇게 하면 설치 하는 새 배포판 WSL 2 배포판으로 초기화 되어야 합니다.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>사용할 WSL 배포의 버전 확인 완료

확인 하려면 다음 명령을 사용 하는 각 배포판을 사용 하는 WSL의 어떤 버전:

`wsl --list --verbose` 또는 `wsl -l -v`

위에서 선택한 배포판 'version' 열 아래에 있는 '2'를 이제 표시 됩니다. 이 과정을 완료 했으므로 자유롭게 WSL 2 배포를 사용 하 여 시작 하십시오! 