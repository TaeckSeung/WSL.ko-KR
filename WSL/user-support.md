---
title: Linux 배포를 위한 사용자 계정 만들기 및 업데이트
description: Linux용 Windows 하위 시스템의 사용자 계정 및 권한 관리에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, 사용자 계정
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235915"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>새 Linux 배포에 대한 사용자 계정 및 암호 만들기

[WSL을 사용하도록 설정하고 Microsoft Store에서 Linux 배포를 설치](./install-win10.md)하면, 새로 설치된 Linux 배포를 열 때 완료해야 하는 첫 번째 단계는 **사용자 이름** 및 **암호**를 포함하여 계정을 만드는 것입니다.

- 이 **사용자 이름** 및 **암호**는 Linux 배포에만 적용되며, Windows 사용자 이름에는 적용되지 않습니다.

- 이 **사용자 이름** 및 **암호**를 만들면 해당 계정이 배포의 기본 사용자가 되고 시작 시 자동으로 로그인됩니다.

- 이 계정은 `sudo`(슈퍼 사용자 작업) 관리 명령을 실행할 수 있는 Linux 관리자로 간주됩니다.

- Linux용 Windows 하위 시스템에서 실행되는 각 Linux 배포에는 고유한 Linux 사용자 계정과 암호가 있습니다.  배포를 추가하거나, 다시 설치하거나, 다시 설정할 때마다 Linux 사용자 계정을 구성해야 합니다.

![Windows 콘솔에서 Ubuntu 압축 풀기](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>패키지 업데이트 및 업그레이드

대부분의 배포는 비어 있거나 최소한의 패키지 카탈로그와 함께 제공됩니다. 배포의 기본 설정 패키지 관리자를 사용하여 정기적으로 패키지 카탈로그를 업데이트하고 설치된 패키지를 업그레이드하는 것이 좋습니다. Debian/Ubuntu의 경우 apt를 사용합니다.

```bash
sudo apt update && sudo apt upgrade
```

Windows는 Linux 배포를 자동으로 업데이트하거나 업그레이드하지 않습니다. 이는 대부분의 Linux 사용자가 직접 제어하는 것을 선호하는 작업입니다.

## <a name="reset-your-linux-password"></a>Linux 암호 재설정

암호를 변경하려면 Linux 배포(예: Ubuntu)를 열고 `passwd` 명령을 입력합니다.

현재 암호를 입력하고 새 암호를 입력하라는 메시지가 표시된 다음, 새 암호를 확인하라는 메시지가 표시됩니다.

## <a name="forgot-your-password"></a>암호 잊음

Linux 배포용 암호를 잊은 경우 다음을 수행합니다.

1. PowerShell을 열고, `wsl -u root` 명령을 사용하여 기본 WSL 배포의 루트를 입력합니다.

    > 기본값이 아닌 배포에서 잊어버린 암호를 업데이트해야 하는 경우 `Debian`을 대상 배포의 이름으로 바꾼 `wsl -d Debian -u root` 명령을 사용합니다.

2. WSL 배포가 PowerShell 내의 루트 수준에서 열리면 `passwd` 명령을 사용하여 암호를 업데이트할 수 있습니다.

3. 새 UNIX 암호를 입력한 다음, 해당 암호를 확인하라는 메시지가 표시됩니다. 암호가 성공적으로 업데이트되었다는 메시지가 표시되면 `exit` 명령을 사용하여 PowerShell 내에서 WSL을 닫습니다.

> [!NOTE]
> 1703(크리에이터스 업데이트) 또는 1709(Fall Creators Update)와 같은 초기 버전의 Windows 운영 체제를 실행하는 경우 [이 사용자 계정 업데이트 문서의 보관 버전](./user-support-archived.md)을 확인하세요.
