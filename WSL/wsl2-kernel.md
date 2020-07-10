---
title: WSL 2 Linux 커널 업데이트
description: WSL 2 Linux 커널을 수동으로 업데이트하는 방법에 대한 지침입니다.
keywords: wsl, windows, linux 커널, linux용 windows 하위 시스템, 커널
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: bef722f5653380d9f6d104f1a7c116a7599658c9
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033045"
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

## <a name="troubleshooting"></a>문제 해결

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a>이 업데이트는 Linux용 Windows 하위 시스템을 사용하는 머신에만 적용됩니다.
MSI 커널을 설치하려면 WSL이 필요하며 이를 먼저 사용하도록 설정해야 합니다. 실패하면 `This update only applies to machines with the Windows Subsytem for Linux` 메시지가 표시됩니다. 

이 메시지가 표시되는 세 가지 가능한 원인은 다음과 같습니다.

1. WSL 2를 지원하지 않는 이전 버전의 Windows를 아직 사용하고 있습니다. [WSL 2 요구 사항](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2)을 확인하고 WSL 2를 사용하도록 업그레이드하세요. 
2. `Windows Subsystem for Linux`를 사용할 수 없습니다. [Linux용 Windows 하위 시스템 설치 가이드](https://docs.microsoft.com/windows/wsl/install-win10)를 따르세요.
3. `Windows Subsystem for Linux`를 사용하도록 설정한 후 다시 부팅해야 적용됩니다. 머신을 다시 부팅한 후 다시 시도하세요.

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

%SystemRoot%\system32\lxss\tools\,에서 커널이 누락될 때마다 위의 오류가 발생할 수 있습니다.

가능한 해결 방법은 다음과 같습니다.

1. https://aka.ms/wsl2kernel 에 있는 지침에 따라 Linux 커널을 수동으로 설치하세요.
2. '프로그램 추가/제거'에서 MSI를 제거하고 다시 설치하세요.
