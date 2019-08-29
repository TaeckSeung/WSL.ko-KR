---
title: Linux 배포 관리
description: Linux 용 Windows 하위 시스템에서 실행 되는 여러 Linux 배포를 나열 하 고 구성 하는 참조입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, wsl., wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: ca65cf6fde3e0ba4750ffc44f5aec542be6cfabf
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122702"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템 관리 및 구성

> Windows 10로의 작성자 업데이트 이상에 적용 됩니다.  새 관리 기능을 사용해 보고 Microsoft 스토어에서 여러 Linux 배포를 실행 하기 시작 하려면 업데이트 된 [설치 가이드](./install_guide.md) 를 참조 하세요.

## <a name="ways-to-run-wsl"></a>WSL 실행 방법

Linux 용 Windows 하위 시스템을 사용 하 여 Linux를 실행 하는 방법에는 여러 가지가 있습니다.

1. `[distro]`예를 들어`ubuntu`
1. `wsl.exe` 또는 `bash.exe`
1. `wsl [command]` 또는 `bash -c [command]`

사용 해야 하는 방법은 수행 중인 작업에 따라 다릅니다.

### <a name="launch-wsl-by-distribution"></a>배포 별 WSL 시작

배포판 특정 응용 프로그램을 사용 하 여 배포를 실행 하면 자체 콘솔 창에서 해당 배포가 시작 됩니다.

![시작 메뉴에서 WSL 시작](media/start-launch.png)

Microsoft store에서 "시작"을 클릭 하는 것과 같습니다.

![Microsoft store에서 WSL 시작](media/store-launch.png)

을 실행 `[distribution].exe`하 여 명령줄에서 배포를 실행할 수도 있습니다.

이러한 방식으로 명령줄에서 배포를 실행 하는 경우의 단점은 작업 디렉터리를 현재 디렉터리에서 배포의 홈 디렉터리로 자동으로 변경 하는 것입니다.

**예제:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl 및 wsl [명령]

명령줄에서 WSL을 실행 하는 가장 좋은 방법은를 사용 `wsl.exe`하는 것입니다.

**예제:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

현재 작업 디렉터리 `wsl` 를 그대로 유지할 수 있을 뿐 아니라 Windows 명령을 함께 사용 하 여 단일 명령을 실행할 수 있습니다.

**예제:**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**예제:**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>여러 Linux 배포 관리

### <a name="windows-10-version-1903-and-later"></a>Windows 10 버전 1903 이상

를 사용 `wsl.exe` 하 여 Linux 용 Windows 하위 시스템 (wsl)의 배포를 관리할 수 있습니다. 여기에는 사용 가능한 배포 나열, 기본 배포 설정, 배포 제거 등이 포함 됩니다.

각 Linux 배포판은 독립적으로 자체 구성을 관리 합니다. 배포 관련 명령을 보려면를 실행 `[distro.exe] /?`합니다.  예를 들면 `ubuntu /?`입니다.

#### <a name="list-distributions"></a>배포 나열

`wsl -l`,`wsl --list`  
WSL에서 사용할 수 있는 Linux 배포판을 나열 합니다.  배포가 나열 되 면 설치 되어 사용할 준비가 된 것입니다.

`wsl --list --all`   
현재 사용할 수 없는 모든 배포를 나열 합니다.  이러한 작업은 설치, 제거 또는 손상 된 상태에 있을 수 있습니다.  

`wsl --list --running`   
현재 실행 중인 모든 배포를 나열 합니다.

#### <a name="set-a-default-distribution"></a>기본 배포 설정

기본 wsl 배포는 명령줄에서 실행할 `wsl` 때 실행 되는 배포입니다.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

기본 분포를로 `<DistributionName>`설정 합니다.

**예제:**  
`wsl -s Ubuntu`기본 배포를 Ubuntu로 설정 합니다.  이제 실행 `wsl npm init` 하면 Ubuntu에서 실행 됩니다.  실행 `wsl` 하는 경우 Ubuntu 세션이 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>배포 등록 취소 및 다시 설치

Linux 배포판은 Microsoft store를 통해 설치할 수 있지만 스토어에서는 제거할 수 없습니다.  WSL Config를 사용 하면 배포를 등록 취소 하거나 제거할 수 있습니다.

등록을 취소 하면 배포도 다시 설치할 수 있습니다.

> **주의:** 등록을 취소 하면 해당 배포와 관련 된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실 됩니다.  저장소에서 다시 설치 하면 배포의 정리 된 복사본을 설치 합니다.

`wsl --unregister <DistributionName>`  
설치 하거나 정리할 수 있도록 WSL에서 배포의 등록을 취소 합니다.

예를 들어 `wsl --unregister Ubuntu` 는 wsl에서 사용할 수 있는 배포에서 Ubuntu를 제거 합니다.  실행 `wsl --list` 하면 나열 되지 않습니다.

를 다시 설치 하려면 Microsoft 스토어에서 배포를 찾아 "시작"을 선택 합니다.

#### <a name="run-as-a-specific-user"></a>특정 사용자로 실행

`wsl -u <Username>`, `wsl --user <Username>`

지정 된 사용자로 WSL을 실행 합니다. 사용자는 WSL 배포 내에 있어야 합니다.

#### <a name="run-a-specific-distribution"></a>특정 배포 실행

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

WSL의 지정 된 배포를 실행 합니다. 기본값을 변경 하지 않고도 특정 배포에 명령을 보내는 데 사용할 수 있습니다.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 버전 1903 이전 버전

Wsl Config (`wslconfig.exe`)는 wsl (linux 용 Windows 하위 시스템)에서 실행 되는 linux 배포를 관리 하기 위한 명령줄 도구입니다.  사용 가능한 배포를 나열 하 고, 기본 배포를 설정 하 고, 배포를 제거할 수 있습니다.

WSL Config는 배포를 확장 하거나 조정 하는 설정에 유용 하지만 각 Linux 배포는 독립적으로 자체 구성을 관리 합니다.  배포 관련 명령을 보려면를 실행 `[distro.exe] /?`합니다.  예를 들면 `ubuntu /?`입니다.

Wslconfig에 사용할 수 있는 모든 옵션을 보려면 다음을 실행 합니다.`wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>배포 나열

`wslconfig /list`  
WSL에서 사용할 수 있는 Linux 배포판을 나열 합니다.  배포가 나열 되 면 설치 되어 사용할 준비가 된 것입니다.

`wslconfig /list /all`  
현재 사용할 수 없는 모든 배포를 나열 합니다.  이러한 작업은 설치, 제거 또는 손상 된 상태에 있을 수 있습니다.  

#### <a name="set-a-default-distribution"></a>기본 배포 설정

기본 wsl 배포는 명령줄에서 실행할 `wsl` 때 실행 되는 배포입니다.

`wslconfig /setdefault <DistributionName>`

기본 분포를로 `<DistributionName>`설정 합니다.

**예제:**  
`wslconfig /setdefault Ubuntu`기본 배포를 Ubuntu로 설정 합니다.  이제 실행 `wsl npm init` 하면 Ubuntu에서 실행 됩니다.  실행 `wsl` 하는 경우 Ubuntu 세션이 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>배포 등록 취소 및 다시 설치

Linux 배포판은 Microsoft store를 통해 설치할 수 있지만 스토어에서는 제거할 수 없습니다.  WSL Config를 사용 하면 배포를 등록 취소 하거나 제거할 수 있습니다.

등록을 취소 하면 배포도 다시 설치할 수 있습니다.

> **주의:** 등록을 취소 하면 해당 배포와 관련 된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실 됩니다.  저장소에서 다시 설치 하면 배포의 정리 된 복사본을 설치 합니다.

`wslconfig /unregister <DistributionName>`  
설치 하거나 정리할 수 있도록 WSL에서 배포의 등록을 취소 합니다.

예를 들어 `wslconfig /unregister Ubuntu` 는 wsl에서 사용할 수 있는 배포에서 Ubuntu를 제거 합니다.  실행 `wslconfig /list` 하면 나열 되지 않습니다.

를 다시 설치 하려면 Microsoft 스토어에서 배포를 찾아 "시작"을 선택 합니다.

## <a name="set-wsl-launch-settings"></a>WSL 시작 설정 설정

> **Windows 참가자 빌드 17093 이상에서 사용 가능**

를 사용 하 여 `wsl.conf`하위 시스템을 시작할 때마다 적용 될 특정 기능을 wsl에서 자동으로 구성 합니다. 

현재 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함 됩니다.

`wsl.conf`는의 `/etc/wsl.conf`각 Linux 배포에 있습니다. 파일이 없으면 직접 만들 수 있습니다. WSL에서 파일의 존재를 감지 하 고 해당 내용을 읽습니다. 파일이 없거나 잘못 된 태그 서식 지정 인 경우 WSL은 계속 정상적으로 시작 됩니다.

다음은 배포판에 `wsl.conf` 추가할 수 있는 샘플 파일입니다.

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>구성 옵션

.Ini 규칙을 유지 하는 경우 키가 섹션 아래에 선언 됩니다. 

Wsl은 및 라는 두 `automount` 개의 `network`섹션을 지원 합니다.

#### <a name="automount"></a>자동 탑재

여기서`[automount]`


| Key        | value                          | 기본      | 메모란                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`고정 드라이브 (즉, `C:/`또는 `D:/`)를 사용 하 여 자동으로 `/mnt`DrvFs에 탑재할 수 있습니다.  `false`는 드라이브가 자동으로 탑재 되지 않음을 의미 하지만 수동으로 또는를 통해 `fstab`탑재할 수 있습니다.                                                                                                             |
| mountFsTab | boolean                        | true         | `true`wsl start에서 처리할를 설정 `/etc/fstab` 합니다. /etc/fstab는 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다. 따라서 시작 시 WSL에서 자동으로 이러한 파일 시스템를 탑재할 수 있습니다.                                                                                                                |
| 루트       | String                         | `/mnt/`      | 고정 드라이브가 자동으로 탑재 되는 디렉터리를 설정 합니다. 예를 들어 wsl `/windir/` 에 디렉터리가 있고이를 루트로 지정 하는 경우 고정 드라이브가에 탑재 된 것을 볼 수 있습니다.`/windir/c`                                                                                              |
| 옵션    | 쉼표로 구분 된 값 목록 | 빈 문자열 | 이 값은 기본 DrvFs 탑재 옵션 문자열에 추가 됩니다. **DrvFs 옵션만 지정할 수 있습니다.** 탑재 이진이 일반적으로 플래그로 구문 분석 하는 옵션은 지원 되지 않습니다. 이러한 옵션을 명시적으로 지정 하려면/etc/fstab에서 수행 하려는 모든 드라이브를 포함 해야 합니다. |

기본적으로 WSL은 uid 및 gid를 기본 사용자의 값으로 설정 합니다 (Ubuntu 배포판에서 기본 사용자는 uid = 1000, gid = 1000으로 만들어짐). 사용자가이 키를 통해 gid 또는 uid 옵션을 명시적으로 지정 하면 연결 된 값이 덮어쓰여집니다. 그렇지 않으면 기본값이 항상 추가 됩니다.

**참고:** 이러한 옵션은 자동으로 탑재 된 모든 드라이브에 대 한 탑재 옵션으로 적용 됩니다. 특정 드라이브에 대 한 옵션만 변경 하려면 대신/etc/fstab를 사용 합니다.

#### <a name="network"></a>network

섹션 레이블:`[network]`

| Key | value | 기본 | 메모란|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`생성할 `/etc/hosts`wsl을 설정 합니다. 이 `hosts` 파일에는 해당 IP 주소에 해당 하는 호스트 이름에 대 한 정적 맵이 포함 됩니다. |
| generateResolvConf | boolean | `true` | `true`WSL을 생성 `/etc/resolv.conf`하도록 설정 합니다. 에 `resolv.conf` 는 IP 주소에 대해 지정 된 호스트 이름을 확인할 수 있는 DNS 목록이 포함 되어 있습니다. | 

#### <a name="interop"></a>rop

섹션 레이블:`[interop]`

이러한 옵션은 Insider Build 17713 이상에서 사용할 수 있습니다.

| Key | value | 기본 | 메모란|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 이 키를 설정 하면 WSL에서 Windows 프로세스 시작을 지원 하는지 여부가 결정 됩니다. |
| appendWindowsPath | boolean | `true` | 이 키를 설정 하면 WSL에서 $PATH 환경 변수에 Windows 경로 요소를 추가할지 여부를 결정 합니다. | 
