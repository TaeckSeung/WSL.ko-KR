---
title: Linux 배포 관리
description: Linux용 Windows 하위 시스템에서 실행되는 여러 Linux 배포를 나열하고 구성하는 방법에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999396"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 관리 및 구성

> Windows 10 Fall Creators Update 이상에 적용됩니다.  업데이트된 [설치 가이드](./install_guide.md)를 참조하여 새 관리 기능을 사용해 보고 Microsoft Store에서 여러 Linux 배포의 실행을 시작합니다.

## <a name="ways-to-run-wsl"></a>WSL 실행 방법

Linux용 Windows 하위 시스템을 사용하여 Linux를 실행하는 여러 가지 방법이 있습니다.

1. `[distro]`(예: `ubuntu`)
1. `wsl.exe` 또는 `bash.exe`
1. `wsl [command]` 또는 `bash -c [command]`

사용해야 하는 방법은 수행하는 작업에 따라 다릅니다.

### <a name="launch-wsl-by-distribution"></a>배포별 WSL 시작

배포판 특정 애플리케이션을 사용하여 배포를 실행하면 자체 콘솔 창에서 해당 배포가 시작됩니다.

![시작 메뉴에서 WSL 시작](media/start-launch.png)

Microsoft Store에서 "시작"을 클릭하는 것과 같습니다.

![Microsoft Store에서 WSL 시작](media/store-launch.png)

`[distribution].exe`를 실행하여 명령줄에서 배포를 실행할 수도 있습니다.

명령줄에서 이 방식으로 배포를 실행하는 경우 작업 디렉터리가 현재 디렉터리에서 배포의 홈 디렉터리로 자동으로 변경된다는 단점이 있습니다.

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

명령줄에서 WSL을 실행하는 가장 좋은 방법은 `wsl.exe`를 사용하는 것입니다.

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

`wsl`은 현재 작업 디렉터리를 그대로 유지할 뿐만 아니라 Windows 명령과 함께 단일 명령을 실행할 수 있습니다.

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

배포는 WSL(Linux용 Windows 하위 시스템)에서 `wsl.exe`를 사용하여 관리할 수 있습니다. 여기에는 사용 가능한 배포 나열, 기본 배포 설정 및 배포 제거가 포함됩니다.

각 Linux 배포는 자체 구성을 독립적으로 관리합니다. 배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.  예를 들어 `ubuntu /?`입니다.

#### <a name="list-distributions"></a>배포 나열

`wsl -l`, `wsl --list`  
WSL에 사용할 수 있는 Linux 배포를 나열합니다.  배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.

`wsl --list --all`   
현재 사용할 수 없는 배포를 포함하여 모든 배포를 나열합니다.  이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.  

`wsl --list --running`   
현재 실행되고 있는 모든 배포를 나열합니다.

#### <a name="set-a-default-distribution"></a>기본 배포 설정

기본 WSL 배포는 명령줄에서 `wsl`을 실행할 때 실행되는 배포입니다.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

기본 배포를 `<DistributionName>`으로 설정합니다.

**예제:**  
`wsl -s Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.  이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.  `wsl`을 실행하면 Ubuntu 세션이 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>배포 등록 취소 및 다시 설치

Linux 배포는 Microsoft Store를 통해 설치할 수 있지만 이를 통해 제거할 수는 없습니다.  WSL Config를 사용하면 배포를 등록 취소/제거할 수 있습니다.

또한 등록을 취소하면 배포를 다시 설치할 수 있습니다.

> **주의:** 등록이 취소되면 해당 배포와 관련된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실됩니다.  스토어에서 다시 설치하면 배포의 새 복사본이 설치됩니다.

`wsl --unregister <DistributionName>`  
WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.

예를 들어 `wsl --unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.  `wsl --list`를 실행하면 나열되지 않습니다.

다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.

#### <a name="run-as-a-specific-user"></a>특정 사용자로 실행

`wsl -u <Username>`, `wsl --user <Username>`

WSL을 지정된 사용자로 실행합니다. 사용자는 WSL 배포 내에 있어야 합니다.

#### <a name="run-a-specific-distribution"></a>특정 배포 실행

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

WSL의 지정된 배포를 실행합니다. 기본값을 변경하지 않고도 명령을 특정 배포로 보내는 데 사용할 수 있습니다.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 버전 1903의 이전 버전

WSL Config(`wslconfig.exe`)는 WSL(Linux용 Windows 하위 시스템)에서 실행되는 Linux 배포를 관리하기 위한 명령줄 도구입니다.  사용 가능한 배포를 나열하고, 기본 배포를 설정하고, 배포를 제거할 수 있습니다.

WSL Config는 배포를 확장하거나 조정하는 설정에 유용하지만, 각 Linux 배포는 자체 구성을 독립적으로 관리합니다.  배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.  예를 들어 `ubuntu /?`입니다.

wslconfig에 사용할 수 있는 모든 옵션을 보려면 `wslconfig /?`를 실행합니다.

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
WSL에 사용할 수 있는 Linux 배포를 나열합니다.  배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.

`wslconfig /list /all`  
현재 사용할 수 없는 배포를 포함하여 모든 배포를 나열합니다.  이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.  

#### <a name="set-a-default-distribution"></a>기본 배포 설정

기본 WSL 배포는 명령줄에서 `wsl`을 실행할 때 실행되는 배포입니다.

`wslconfig /setdefault <DistributionName>`

기본 배포를 `<DistributionName>`으로 설정합니다.

**예제:**  
`wslconfig /setdefault Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.  이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.  `wsl`을 실행하면 Ubuntu 세션이 열립니다.

#### <a name="unregister-and-reinstall-a-distribution"></a>배포 등록 취소 및 다시 설치

Linux 배포는 Microsoft Store를 통해 설치할 수 있지만 이를 통해 제거할 수는 없습니다.  WSL Config를 사용하면 배포를 등록 취소/제거할 수 있습니다.

또한 등록을 취소하면 배포를 다시 설치할 수 있습니다.

> **주의:** 등록이 취소되면 해당 배포와 관련된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실됩니다.  스토어에서 다시 설치하면 배포의 새 복사본이 설치됩니다.

`wslconfig /unregister <DistributionName>`  
WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.

예를 들어 `wslconfig /unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.  `wslconfig /list`를 실행하면 나열되지 않습니다.

다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.

## <a name="set-wsl-launch-settings"></a>WSL 시작 설정 지정

> **Windows 참가자 빌드 17093 이상에서 사용할 수 있음**

`wsl.conf`를 사용하여 하위 시스템을 시작할 때마다 적용되는 WSL의 특정 기능을 자동으로 구성합니다. 

현재 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함됩니다.

`wsl.conf`는 `/etc/wsl.conf`의 각 Linux 배포에 있습니다. 여기에 파일이 없으면 해당 파일을 직접 만들 수 있습니다. WSL은 파일의 존재 여부를 검색하고 해당 내용을 읽습니다. 파일이 없거나 형식이 잘못된(즉, 잘못된 태그 형식 지정) 경우에도 WSL은 정상적으로 계속 시작됩니다.

다음은 배포판에 추가할 수 있는 `wsl.conf` 파일 샘플입니다.

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

.ini 규칙에 따라 키는 섹션 아래에 선언됩니다. 

WSL은 `automount` 및 `network`의 두 가지 섹션을 지원합니다.

#### <a name="automount"></a>automount

섹션: `[automount]`


| 키        | value                          | 기본      | 참고                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`를 사용하면 고정 드라이브(즉, `C:/` 또는 `D:/`)가 `/mnt` 아래의 DrvFs에 자동으로 탑재됩니다.  `false`는 드라이브가 자동으로 탑재되지 않음을 의미하지만, 수동으로 또는 `fstab`를 통해 탑재할 수 있습니다.                                                                                                             |
| mountFsTab | boolean                        | true         | `true`는 WSL 시작 시 `/etc/fstab`가 처리되도록 설정합니다. /etc/fstab는 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다. 따라서 시작 시 이러한 파일 시스템을 WSL에 자동으로 탑재할 수 있습니다.                                                                                                                |
| root       | 문자열                         | `/mnt/`      | 고정 드라이브가 자동으로 탑재될 디렉터리를 설정합니다. 예를 들어 WSL의 `/windir/`에 디렉터리가 있고 이 디렉터리를 루트로 지정하면 고정 드라이브가 `/windir/c`에 탑재됩니다.                                                                                              |
| 옵션    | 쉼표로 구분된 값 목록 | 빈 문자열 | 이 값은 기본 DrvFs 탑재 옵션 문자열에 추가됩니다. **DrvFs별 옵션만 지정할 수 있습니다.** 탑재 이진 파일이 일반적으로 플래그로 구문 분석되는 옵션은 지원되지 않습니다. 이러한 옵션을 명시적으로 지정하려면 원하는 모든 드라이브를 /etc/fstab에 포함시켜야 합니다. |

기본적으로 WSL은 uid와 gid를 기본 사용자의 값으로 설정합니다(Ubuntu 배포판에서 기본 사용자는 uid=1000, gid=1000으로 만들어짐). 사용자가 이 키를 통해 gid 또는 uid 옵션을 명시적으로 지정하면 연결된 값이 덮어쓰입니다. 그렇지 않으면 항상 기본값이 추가됩니다.

**참고:** 이러한 옵션은 자동으로 탑재된 모든 드라이브에 대한 탑재 옵션으로 적용됩니다. 특정 드라이브에 대한 옵션만 변경하려면 /etc/fstab를 대신 사용합니다.

##### <a name="mount-options"></a>탑재 옵션

Windows 드라이브(DrvFs)에 다른 탑재 옵션을 설정하면 Windows 파일에 대한 파일 사용 권한이 계산되는 방법을 제어할 수 있습니다. 다음 옵션을 사용할 수 있습니다.

| 키 | 설명 | Default |
|:----|:----|:----|
|uid| 모든 파일의 소유자에게 사용되는 사용자 ID | WSL 배포판의 기본 사용자 ID(처음 설치할 때 기본값은 1000으로 설정됨)
|gid| 모든 파일의 소유자에게 사용되는 그룹 ID | WSL 배포판의 기본 그룹 ID(처음 설치할 때 기본값은 1000으로 설정됨)
|umask | 모든 파일 및 디렉터리에서 제외할 권한의 8진수 마스크 | 000
|fmask | 모든 파일에서 제외할 권한의 8진수 마스크 | 000
|dmask | 모든 디렉터리에서 제외할 권한의 8진수 마스크 | 000

**참고:** 권한 마스크는 파일 또는 디렉터리에 적용되기 전에 논리 OR 연산을 거칩니다. 

#### <a name="network"></a>네트워크

섹션 레이블: `[network]`

| 키 | value | 기본 | 참고|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`는 WSL에서 `/etc/hosts`를 생성하도록 설정합니다. `hosts` 파일에는 IP 주소에 해당하는 호스트 이름의 정적 맵이 포함됩니다. |
| generateResolvConf | boolean | `true` | `true`는 WSL에서 `/etc/resolv.conf`를 생성하도록 설정합니다. `resolv.conf`에는 지정된 호스트 이름을 해당 IP 주소로 확인할 수 있는 DNS 목록이 포함됩니다. | 

#### <a name="interop"></a>interop

섹션 레이블: `[interop]`

다음 옵션은 참가자 빌드 17713 이상에서 사용할 수 있습니다.

| 키 | value | 기본 | 참고|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 이 키를 설정하면 WSL에서 Windows 프로세스 시작을 지원하는지 여부가 결정됩니다. |
| appendWindowsPath | boolean | `true` | 이 키를 설정하면 WSL에서 Windows 경로 요소를 $PATH 환경 변수에 추가할지 여부가 결정됩니다. | 
