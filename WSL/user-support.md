---
title: Linux 사용자 계정 및 권한
description: Linux용 Windows 하위 시스템의 사용자 계정 및 권한 관리에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, 사용자 계정
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d8434283e459ae25637fac0c0b1877ca07d9a255
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269707"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템에 대한 사용자 계정 및 권한

WSL에서 새 Linux 배포를 설정하는 첫 번째 단계는 Linux 사용자를 만드는 것입니다.  처음 만든 사용자 계정은 다음과 같은 몇 가지 특수 특성을 사용하여 자동으로 구성됩니다.

1. 기본 사용자이며, 시작할 때 자동으로 로그인됩니다.
1. 기본적으로 Linux 관리자(sudo 그룹의 멤버)입니다.

Linux용 Windows 하위 시스템에서 실행되는 각 Linux 배포에는 고유한 Linux 사용자 계정과 암호가 있습니다.  배포를 추가하거나, 다시 설치하거나, 다시 설정할 때마다 Linux 사용자 계정을 구성해야 합니다.  Linux 사용자 계정은 배포마다 독립적일 뿐만 아니라 Windows 사용자 계정과도 독립적입니다.

## <a name="resetting-your-linux-password"></a>Linux 암호 재설정

Linux 사용자 계정에 대한 액세스 권한이 있고 현재 암호를 알고 있는 경우 해당 배포의 Linux 암호 재설정 도구(대부분 `passwd`)를 사용하여 암호를 변경합니다.

이 도구가 옵션이 아닌 경우 배포에 따라 기본 사용자를 다시 설정하여 암호를 다시 설정하면 됩니다.

WSL에서는 WSL을 시작할 때 자동으로 로그인되는 사용자 계정을 식별하는 기본 사용자 태그를 제공합니다.  대부분의 배포에는 기본 사용자를 루트로 설정하고 암호가 설정되지 않은 루트 사용자도 설정하는 명령이 포함되어 있으므로 기본 사용자를 루트로 변경하는 것은 암호 재설정과 같은 작업에 유용한 도구입니다.

### <a name="for-creators-update-and-earlier"></a>크리에이터스 업데이트 및 이전 버전의 경우
Windows 10 크리에이터스 업데이트를 실행하는 경우 다음 명령을 실행하여 기본 Bash 사용자를 변경할 수 있습니다.

1. 기본 사용자를 `root`로 변경합니다.

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 지금 `bash.exe`를 실행하여 `root`로 로그인합니다.

    ```console
    C:\> bash.exe
    ```

1. 배포의 암호 명령을 사용하여 암호를 다시 설정하고 Linux 콘솔을 닫습니다.

    ```BASH
    $ passwd username
    $ exit
    ```

1. Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update 및 이후 버전의 경우
특정 배포에 사용할 수 있는 명령을 확인하려면 `[distro.exe] /?`를 실행합니다.
    
예를 들어 Ubuntu가 설치된 경우 다음과 같습니다.

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

Ubuntu를 사용한 단계별 지침은 다음과 같습니다.

1. CMD를 엽니다.
1. 기본 Linux 사용자를 `root`로 설정합니다.

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Linux 배포(`ubuntu`)를 시작합니다.  자동으로 `root`로 로그인됩니다.

1. `passwd` 명령을 사용하여 암호를 다시 설정합니다.

    ```BASH
    $ passwd username
    ```

1. Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>권한

WSL의 권한과 관련하여 다음 두 가지 중요한 개념을 명심해야 합니다.

1. Windows 권한 모델은 Windows 리소스에 대한 프로세스의 권한을 제어합니다.
2. Linux 권한 모델은 Linux 리소스에 대한 프로세스의 권한을 제어합니다.

WSL에서 Linux를 실행하는 경우 Linux는 이를 시작하는 프로세스와 동일한 Windows 권한을 갖습니다. Linux는 다음 두 가지 권한 수준 중 하나로 시작할 수 있습니다.

* 보통(관리자 권한 없음): Linux가 로그인한 사용자의 권한으로 실행됩니다.
* 관리자 권한/관리자: Linux가 관리자 권한/관리자 Windows 권한으로 실행됩니다.

> 관리자 권한으로 실행되는 프로세스는 시스템 수준 설정 및 시스템 수준의 보호된 데이터에 액세스하여 수정할 수 있으므로(이에 따라 손상시킬 수 있음) Windows 또는 Linux 애플리케이션/도구/셸인지 여부와 관계없이 반드시 필요한 경우가 아니면 관리자 권한으로 실행되는 프로세스를 **시작하지 마세요**!

위의 Windows 권한은 Linux 인스턴스 내의 권한과는 독립적입니다. Linux "루트 권한"은 Linux 환경 및 파일 시스템 내의 사용자의 권한에만 영향을 주며, 부여된 Windows 권한에는 영향을 주지 않습니다. 따라서 Linux 프로세스를 루트로(예: `sudo`를 통해) 실행하면 Linux 환경 내에서 해당 프로세스 관리자 권한만 부여됩니다.

**예제:**     
Windows 관리자 권한이 있는 Bash 세션은 `cd /mnt/c/Users/Administrator`에 액세스할 수 있지만, 관리자 권한이 없는 Bash 세션은 "권한 거부" 오류를 표시할 수 있습니다.

Windows 내의 권한은 Windows에서 관리하므로 Linux에서 `sudo cd /mnt/c/Users/Administrator`를 입력하더라도 관리자의 디렉터리에 대한 액세스 권한이 부여되지 않습니다.

Linux 권한 모델은 사용자에게 현재 Linux 사용자 기반의 권한이 있는 Linux 환경 내에서 중요합니다.

**예제:**  
sudo 그룹의 사용자가 `sudo apt update`를 실행할 수 있습니다.
