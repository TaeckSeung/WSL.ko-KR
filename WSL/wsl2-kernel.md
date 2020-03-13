---
title: WSL 2 Linux 커널 업데이트
description: WSL 2 Linux 커널을 수동으로 업데이트 하는 방법에 대 한 지침
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138192"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>WSL 2 Linux 커널 업데이트

WSL 2 내에서 Linux 커널을 수동으로 업데이트 하려면 다음 단계를 수행 하세요. 

## <a name="download-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 다운로드

[이 링크](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) 를 클릭 하 여 AMD64 컴퓨터용 최신 WSL2 Linux 커널 업데이트 패키지를 다운로드 하세요.

> [!NOTE] ARM64 컴퓨터를 사용 하는 경우 대신 [이 패키지](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) 를 다운로드 하세요.

## <a name="install-the-linux-kernel-update-package"></a>Linux 커널 업데이트 패키지 설치

Linux 커널 업데이트 패키지를 설치 하려면:
    1. 이전 단계에서 다운로드 한 업데이트 패키지를 실행 합니다.
    2. 상승 된 권한을 요청 하는 메시지가 표시 됩니다 .이 설치를 승인 하려면 ' 예 '를 선택 합니다.
    3. 설치가 완료 되 면 WSL2 사용을 시작할 준비가 된 것입니다.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>WSL2 Linux 커널을 업데이트 하기 위한 향후 계획

이러한 변경 내용에 대 한 자세한 내용은 [Windows 명령줄 블로그의](https://aka.ms/cliblog) [이 블로그 게시물](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) 을 참조 하세요.