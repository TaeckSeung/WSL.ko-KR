---
title: Linux 사용자 계정 및 사용 권한
description: Linux 용 Windows 하위 시스템을 사용 하 여 사용자 계정 및 사용 권한 관리에 대 한 참조입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, 사용자 계정에 대 한 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063601"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>사용자 계정 및 Linux 용 Windows 하위 시스템에 대 한 권한

WSL에서 새 Linux 배포를 설정 하는 첫 번째 단계는 Linux 사용자를 만들기.  사용자가 만든 첫 번째 사용자 계정에 몇 가지 특수 한 특성을 사용 하 여 자동으로 구성 됩니다.

1. 기본 사용자 것-해당 로그인 자동으로 시작 합니다.
1. 기본적으로 Linux 관리자 (sudo 그룹의 구성원)는 것입니다.

Linux 용 Windows 하위 시스템에서 실행 중인 각 Linux 배포에는 자체 Linux 사용자 계정 및 암호.  언제 든 지 추가 배포를 다시 설치 또는 다시 설정 Linux 사용자 계정을 구성 해야 합니다.  와 별개의 Windows 사용자 계정에도, Linux 사용자 계정 에서만 배포당 독립 받지 않습니다.

## <a name="resetting-your-linux-password"></a>Linux 암호를 다시 설정

변경할 현재 암호를 알고 있고 Linux 사용자 계정에 액세스할 경우 Linux를 사용 하 여 암호 재설정 해당 배포-가장 가능성이 높은 도구 `passwd`합니다.

배포에 따라 옵션 하지 않은 경우에 기본 사용자를 다시 설정 하 여 암호를 재설정할 수 있습니다.

WSL은 사용자 계정을 자동으로 식별 하는 기본 사용자 태그는 WSL 시작할 때 로그인을 제공 합니다.  대부분의 배포 루트 및 루트 사용자로 설정 된 암호가 없거나를 사용 하 여 기본 사용자를 설정 하는 명령을 포함 하므로 기본 사용자 루트 변경은 등 암호 재설정에 대 한 유용한 도구입니다.

### <a name="for-creators-update-and-earlier"></a>크리에이터 스 업데이트 이상
실행 중인 경우 Windows 10 크리에이터 스 업데이트 하거나 이전에 다음 명령을 실행 하 여 기본 Bash 사용자를 변경할 수 있습니다.

1. 기본 사용자 변경 `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 실행할 `bash.exe` 지금 로그인으로 `root`:

    ```console
    C:\> bash.exe
    ```

1. 분포의 암호 명령을 사용 하 여 암호를 재설정 하 고 Linux 콘솔을 닫습니다.

    ```BASH
    $ passwd username
    $ exit
    ```

1. Windows CMD에서 일반적인 Linux 사용자 계정으로 다시 기본 사용자를 다시 설정 합니다.

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update에 대 한 이상
특정 배포에 사용할 수 있는 명령을 확인 하려면 `[distro.exe] /?`합니다.
    
예를 들어, Ubuntu를 사용 하 여 설치 합니다.

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Ubuntu를 사용 하는 단계별 지침 단계:

1. 열기 CMD
1. 기본 Linux 사용자로 `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Linux 배포를 시작 (`ubuntu`).  자동으로로 로그인 `root`:

1. 사용 하 여 암호 재설정을 `passwd` 명령:

    ```BASH
    $ passwd username
    ```

1. Windows CMD에서 일반적인 Linux 사용자 계정으로 다시 기본 사용자를 다시 설정 합니다.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>사용 권한

WSL에서 사용 권한을 제공 하는 경우 염두에 두 가지 중요 한 개념이 있습니다.

1. Windows 권한 모델을 Windows 리소스에 대 한 프로세스의 권한을 제어합니다
2. Linux 권한 모델에는 Linux 리소스에 대 한 프로세스의 권한을 제어합니다

WSL에서 Linux를 실행 하는 경우 Linux는 프로세스와 동일한 Windows 권한을 갖습니다. 두 사용 권한 수준 중 하나로 Linux는 시작할 수 있습니다.

* 일반 (권한이 상승 되지 않은): Linux에서 로그인 한 사용자의 권한으로 실행
* 관리자 권한/관리자: 관리자 권한/관리자 Windows 권한으로 실행 되는 Linux

> 상승 된 때문에 프로세스 수 변경/시스템 차원의 설정 및 데이터 손상과 보호 파일 및 폴더 액세스/수정 **하지 말고** Windows 있는지 여부에 반드시 필요한 경우가 아니면 관리자 권한 프로세스를 시작 하거나 Linux 응용 프로그램/도구/셸!

위의 Windows 권한은 Linux 인스턴스 내에서 사용 권한을 무관 다음과 같습니다. "루트 권한" Linux Linux 환경 및 파일 시스템 내에서 사용자의 권한에 영향을 줍니다. 영향을 미치지 않습니다 Windows 권한 부여에 있습니다. 따라서 루트로 Linux 프로세스를 실행 (예: 통해 `sudo`) Linux 환경 내에서 권한 관리를 처리 하는 유일한 부여 합니다.

**예:**    
Windows 관리자 권한으로 Bash 세션에 액세스할 수 있습니다 `cd /mnt/c/Users/Administrator` 관리자 권한이 사용 권한 거부 "오류를 볼 수 없는 Bash 세션 동안.

Linux에서 입력 `sudo cd /mnt/c/Users/Administrator` Windows 내에서 사용 권한을 Windows에서 관리 되므로 관리자의 디렉터리에 대 한 액세스 권한을 부여 하지 됩니다.

Linux 권한 모델이 사용자에 게 현재 Linux 사용자를 기반으로 하는 권한이 있는 Linux 환경 내에 있을 때 중요 합니다.

**예:**  
Sudo 그룹에 사용자가 실행할 수 있습니다 `sudo apt update`합니다.
