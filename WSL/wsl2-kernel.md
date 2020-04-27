---
title: WSL 2 Linux 커널 업데이트
description: WSL 2 Linux 커널을 수동으로 업데이트하는 방법에 대한 지침입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/24/2020
ms.locfileid: "79447747"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>WSL 2 Linux 커널 업데이트

WSL 2 내에서 Linux 커널을 수동으로 업데이트하려면 다음 단계를 따르세요. 

## <a name="download-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 다운로드

x64 머신에 대한 최신 WSL2 Linux 커널 업데이트 패키지를 다운로드하려면 [이 링크](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)를 클릭하세요.

> [!NOTE] 
> ARM64 머신을 사용하는 경우 [이 패키지](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)를 대신 다운로드하세요.

## <a name="install-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 설치

Linux 커널 업데이트 패키지를 설치하려면 다음을 수행합니다.

    1. 이전 단계에서 다운로드한 업데이트 패키지를 실행합니다.
    2. 관리자 권한을 요구하는 메시지가 표시되면 '예'를 선택하여 이 설치를 승인합니다.
    3. 설치가 완료되면 WSL2를 사용할 준비가 되었습니다!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>향후의 WSL2 Linux 커널 업데이트 계획

이러한 변경 내용에 대한 자세한 내용은 [Windows 명령줄 블로그](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)에서 [이 블로그 게시물](https://aka.ms/cliblog)을 참조하세요.
