---
title: WSL 2 Linux 커널 업데이트
description: WSL 2 Linux 커널을 수동으로 업데이트하는 방법에 대한 지침입니다.
keywords: wsl, windows, linux 커널, linux용 windows 하위 시스템, 커널
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153048"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>WSL 2 Linux 커널 업데이트

WSL 2 내에서 Linux 커널을 수동으로 업데이트하려면 다음 단계를 따르세요.

> [!NOTE] 
> 설치 관리자가 WSL 1을 찾지 못하면 Linux 커널 업데이트 설치 관리자를 마우스 오른쪽 단추로 클릭하고 "제거"를 누른 후 설치 관리자를 다시 실행합니다.

## <a name="download-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 다운로드

x64 머신용 [최신 WSL2 Linux 커널 업데이트 패키지를 다운로드](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)하세요.

> [!NOTE]
> ARM64 머신을 사용하는 경우 [ARM64 패키지](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)를 대신 다운로드하세요.

## <a name="install-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 설치

Linux 커널 업데이트 패키지를 설치하려면 다음을 수행합니다.

  1. 이전 단계에서 다운로드한 업데이트 패키지를 실행합니다.

  2. 관리자 권한을 요구하는 메시지가 표시되면 '예'를 선택하여 이 설치를 승인합니다.

  3. 설치가 완료되면 WSL2를 사용할 준비가 되었습니다!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>향후의 WSL2 Linux 커널 업데이트 계획

자세한 내용은 [Windows 명령줄 블로그](https://aka.ms/cliblog)에서 사용할 수 있는 [WSL2 Linux 커널업데이트 변경](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) 문서를 참조하세요.
