---
title: Linux 배포를 관리 합니다.
description: 목록 및 Linux 용 Windows 하위 시스템에서 실행 되는 여러 Linux 배포를 구성 참조 합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, wsl.conf, wslconfig 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063501"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>관리 및 Linux 용 Windows 하위 시스템 구성

> 이상 Windows 10 Fall Creators Update 적용 됩니다.  이 업데이트 된 참조 [설치 가이드](./install_guide.md) 새로운 관리 기능을 시도 하 여 Windows 스토어에서 여러 Linux 배포판을 실행을 시작 합니다.

## <a name="ways-to-run-wsl"></a>WSL를 실행 하는 방법

Linux 용 Windows 하위 시스템을 사용 하 여 Linux를 실행 하는 방법은 여러 가지가 있습니다.

1. `[distro]` ie `ubuntu`
1. `wsl.exe` 또는 `bash.exe`
1. `wsl [command]` 또는 `bash -c [command]`

어떤 방법을 사용 해야 하는 일에 따라 달라 집니다.

### <a name="launch-wsl-by-distribution"></a>WSL를 배포 하 여 시작

자체 콘솔 창에서 해당 배포를 시작의 배포판 관련 응용 프로그램을 사용 하 여 배포를 실행 합니다.

![WSL 시작 메뉴에서 시작](media/start-launch.png)

패턴은 Windows 스토어에서 "시작"을 클릭 한 것과 같습니다.

![WSL Windows 스토어에서 시작](media/store-launch.png)

실행 하 여 명령줄에서 배포를 실행할 수도 있습니다 `[distribution].exe`합니다.

이러한 방식으로 명령줄에서 배포를 실행 하는 단점은 자동으로 변경 됩니다 작업 디렉터리는 현재 디렉터리에서 분포의 홈 디렉터리입니다.

**예:**

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

### <a name="wsl-and-wsl-command"></a>wsl 및 wsl [command]

WSL 명령줄에서 실행 하는 가장 좋은 방법은 사용 하 여 `wsl.exe`입니다.

**예:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

뿐만 아니라 `wsl` 쪽 Windows 명령 함께 단일 명령을 실행 하면, 현재 작업 디렉터리를 그대로 유지 합니다.

**예:**

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

**예:**

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


## <a name="managing-multiple-linux-distributions"></a>여러 Linux 배포를 관리합니다.

### <a name="windows-10-version-1903-and-later"></a>Windows 10 버전이 1903 이상

사용할 수 있습니다 `wsl.exe` Windows 하위 시스템에 대 한 WSL (Linux)를 사용할 수 있는 배포를 나열, 기본 배포를 설정 및 배포를 제거를 포함 하 여 프로그램 배포를 관리할 수 있습니다.

각 Linux 배포에서 자체 구성을 독립적으로 관리 합니다. 배포 관련 명령을 확인 하려면 실행 `[distro.exe] /?`합니다.  예를 들면 `ubuntu /?`입니다.

#### <a name="list-distributions"></a>목록 배포

`wsl -l` , `wsl --list`  
WSL를 사용할 수 있는 사용 가능한 Linux 배포를 나열합니다.  배포 되 면 설치 되 고 사용할 준비가 되었습니다.

`wsl --list --all`   
현재 사용할 수 없는 포함 하는 모든 배포를 나열 합니다.  이러한 제거를 설치 하는 중일 수 있습니다 또는 손상 된 상태입니다.  

`wsl --list --running`   
현재 실행 중인 모든 배포를 나열 합니다.

#### <a name="set-a-default-distribution"></a>기본 배포를 설정 합니다.

기본 WSL 배포를 실행할 때 실행 되는 것은 `wsl` 명령줄에서.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

기본 배포 설정 하는 `<DistributionName>`합니다.

**예:**  
`wsl -s Ubuntu` Ubuntu에 기본 배포 내 설정 합니다.  실행할 때 이제 `wsl npm init` Ubuntu에서 실행 됩니다.  실행 하면 `wsl` Ubuntu 세션을 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>등록을 취소 하 고 배포를 다시 설치

Linux 배포는 Windows를 통해 설치할 수 있습니다 하는 동안 저장, 저장소를 통해 제거할 수 없습니다.  WSL 구성 배포를 등록 취소/제거를 허용 합니다.

등록 취소 하면 배포를를 다시 설치할 수도 있습니다.

> **주의:** 등록 취소 되 면 모든 데이터, 설정 및 해당 배포와 관련 된 소프트웨어 영구적으로 손실 됩니다.  저장소에서 다시 설치 하면 배포의 깨끗 한 사본이 설치 됩니다.

`wsl --unregister <DistributionName>`  
다시 설치 하거나 정리할 수 있도록 WSL에서 배포를 취소 합니다.

예를 들어: `wsl -unregister Ubuntu` Ubuntu WSL에서 사용할 수 있는 배포에서 제거 됩니다.  실행할 때 `wsl --list` 나열 되지 것입니다.

을 다시 설치 하려면 Windows 스토어에서 배포를 찾아 "시작"을 선택 합니다.

#### <a name="run-as-a-specific-user"></a>특정 사용자로 실행

`wsl -u <Username>`, `wsl --user <Username>`

WSL 지정된 된 사용자로 실행 합니다. 해당 사용자는 WSL 배포 내에 있어야 합니다. note 하십시오.

#### <a name="run-a-specific-distribution"></a>또한 특정 분포를 실행 합니다.

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

WSL의 지정된 된 배포를 실행, 기본 변경 하지 않고도 특정 배포에 명령을 보내는 데 사용할 수 있습니다.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 버전 1903 보다 이전 버전

WSL 구성 (`wslconfig.exe`) Linux (WSL) 용 Windows 하위 시스템에서 실행 중인 Linux 배포를 관리 하기 위한 명령줄 도구입니다.  사용할 수 있는 배포 목록를 기본 배포를 설정 하 고 배포를 제거할 수 있습니다.

WSL 구성에 걸쳐 하거나 배포를 조정 하는 설정에 대 한 유용한 상태인 각 Linux 배포 독립적으로 관리 하지 자체 구성 합니다.  배포 관련 명령을 확인 하려면 실행 `[distro.exe] /?`합니다.  예를 들면 `ubuntu /?`입니다.

Wslconfig에 대 한 모든 사용 가능한 옵션을 보려면 다음을 실행 합니다.  `wslconfig /?`

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

#### <a name="list-distributions"></a>목록 배포

`wslconfig /list`  
WSL를 사용할 수 있는 사용 가능한 Linux 배포를 나열합니다.  배포 되 면 설치 되 고 사용할 준비가 되었습니다.

`wslconfig /list /all`  
현재 사용할 수 없는 포함 하는 모든 배포를 나열 합니다.  이러한 제거를 설치 하는 중일 수 있습니다 또는 손상 된 상태입니다.  

#### <a name="set-a-default-distribution"></a>기본 배포를 설정 합니다.

기본 WSL 배포를 실행할 때 실행 되는 것은 `wsl` 명령줄에서.

`wslconfig /setdefault <DistributionName>`

기본 배포 설정 하는 `<DistributionName>`합니다.

**예:**  
`wslconfig /setdefault Ubuntu` Ubuntu에 기본 배포 내 설정 합니다.  실행할 때 이제 `wsl npm init` Ubuntu에서 실행 됩니다.  실행 하면 `wsl` Ubuntu 세션을 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>등록을 취소 하 고 배포를 다시 설치

Linux 배포는 Windows를 통해 설치할 수 있습니다 하는 동안 저장, 저장소를 통해 제거할 수 없습니다.  WSL 구성 배포를 등록 취소/제거를 허용 합니다.

등록 취소 하면 배포를를 다시 설치할 수도 있습니다.

> **주의:** 등록 취소 되 면 모든 데이터, 설정 및 해당 배포와 관련 된 소프트웨어 영구적으로 손실 됩니다.  저장소에서 다시 설치 하면 배포의 깨끗 한 사본이 설치 됩니다.

`wslconfig /unregister <DistributionName>`  
다시 설치 하거나 정리할 수 있도록 WSL에서 배포를 취소 합니다.

예를 들어: `wslconfig /unregister Ubuntu` Ubuntu WSL에서 사용할 수 있는 배포에서 제거 됩니다.  실행할 때 `wslconfig /list` 나열 되지 것입니다.

을 다시 설치 하려면 Windows 스토어에서 배포를 찾아 "시작"을 선택 합니다.

## <a name="set-wsl-launch-settings"></a>WSL 시작 설정

> **Windows Insider 빌드 17093 이상 사용할 수 있습니다.**

특정 기능을 사용 하 여 하위 시스템을 시작할 때마다 적용 되는 WSL에서 자동으로 구성 `wsl.conf`합니다. 

오른쪽 이제 여기에 자동 탑재 옵션 및 네트워크 구성 합니다.

`wsl.conf` 각 Linux 배포에 위치한 `/etc/wsl.conf`합니다. 파일이 없는, 만들 직접 열 수 있습니다. WSL는 파일의 존재 여부 감지 및 해당 내용을 읽는 됩니다. 파일이 없거나 형식이 잘못 된 경우 (즉, 잘못 된 태그 형식), WSL는 계속 정상적으로 시작 합니다.

다음은 샘플 `wsl.conf` 파일에 배포판에 추가할 수 있습니다.

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

.Ini 규칙에 따라 키 섹션에서 선언 됩니다. 

WSL 두 섹션을 지원 합니다. `automount` 및 `network`합니다.

#### <a name="automount"></a>자동 탑재

섹션: `[automount]`


| Key        | value                          | 기본      | 참고 사항                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` 고정 드라이브 (즉, 원인 `C:/` 또는 `D:/`)에서 DrvFs를 사용 하 여 자동으로 탑재할 `/mnt`합니다.  `false` 드라이브를 자동으로 탑재할 수 없습니다 하지만 수 여전히 탑재할 하 수동으로 또는 통해 `fstab`합니다.                                                                                                             |
| mountFsTab | boolean                        | true         | `true` 설정 `/etc/fstab` 처리할 WSL 시작 합니다. /etc/fstab에 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다. 따라서 시작 시 WSL에서 자동으로 이러한 파일 시스템을 탑재할 수 있습니다.                                                                                                                |
| 루트       | 문자열                         | `/mnt/`      | 고정된 드라이브는 자동으로 탑재 디렉터리를 설정 합니다. 예를 들어 WSL에서 디렉터리에 `/windir/` 를 루트로 예상 되는 고정된 드라이브에 탑재를 지정 하 고 `/windir/c`                                                                                              |
| 옵션    | 값의 쉼표로 구분 된 목록 | 빈 문자열 | 이 값은 기본 DrvFs 탑재 옵션 문자열에 추가 됩니다. **DrvFs 별 옵션 으로만 지정할 수 있습니다.** 이진 탑재는 일반적으로 플래그를 구문 분석 하는 옵션이 지원 되지 않습니다. 해당 옵션을 명시적으로 지정 하려는 경우에 /etc/fstab에 이렇게 하려면 모든 드라이브를 포함 해야 합니다. |

기본적으로 WSL uid 및 gid 값으로 설정 된 기본 사용자 (uid를 사용 하 여 Ubuntu 배포판에 기본 사용자를 만들면 1000 = gid = 1000)입니다. 이 키를 통해 명시적으로 gid 또는 uid 옵션을 지정 하는 사용자, 관련된 값을 덮어씁니다. 그렇지 않은 경우 기본값 추가 항상 됩니다.

**참고:** 이러한 옵션은 모두 자동으로 탑재 된 드라이브에 대 한 탑재 옵션으로 적용 됩니다. 특정 드라이브에 대 한 옵션을 변경 하려면 /etc/fstab을 대신 사용 합니다.

#### <a name="network"></a>네트워크

섹션 레이블: `[network]`

| Key | value | 기본 | 참고 사항|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` WSL 생성 설정 `/etc/hosts`합니다. `hosts` 파일 호스트 이름 해당 IP 주소의 정적 맵이 포함 되어 있습니다. |
| generateResolvConf | boolean | `true` | `true` WSL 생성 설정 `/etc/resolv.conf`합니다. `resolv.conf` 지정된 된 호스트 이름을 해당 IP 주소로 확인할 수 있는 DNS 목록을 포함 합니다. | 

#### <a name="interop"></a>Interop

섹션 레이블: `[interop]`

이러한 옵션에는 참가자 빌드 17713에서 사용할 수 있는 이상입니다.

| Key | value | 기본 | 참고 사항|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 이 키 설정을 WSL는 시작 Windows 프로세스를 지원 하는지 여부를 결정 됩니다. |
| appendWindowsPath | boolean | `true` | 이 키 설정을 WSL $PATH 환경 변수의에 Windows 경로 요소를 추가 하는지 여부를 결정 합니다. | 
