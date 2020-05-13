---
title: Linux 배포 관리
description: Linux용 Windows 하위 시스템에서 실행되는 여러 Linux 배포를 나열하고 구성하는 방법에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: 59419919be138a20ab57e1a6d26a411e1531bf9f
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235899"
---
# <a name="wsl-commands-and-launch-configurations"></a>WSL 명령 및 시작 구성

## <a name="ways-to-run-wsl"></a>WSL 실행 방법

[설치](install-win10.md)된 후에는 wsl을 사용 하 여 Linux 배포를 실행 하는 여러 가지 방법이 있습니다.

1. Windows 시작 메뉴를 방문 하 고 설치 된 배포의 이름을 입력 하 여 Linux 배포를 엽니다. 예: "Ubuntu".
2. Windows 명령 프롬프트 또는 PowerShell에서 설치 된 배포의 이름을 입력 합니다. 예: `ubuntu`
3. Windows 명령 프롬프트 또는 PowerShell에서 현재 명령줄 내에서 기본 Linux 배포를 열려면 다음을 입력 `wsl.exe` 합니다.
4. Windows 명령 프롬프트 또는 PowerShell에서 현재 명령줄 내에서 기본 Linux 배포를 열려면 다음을 입력 `wsl [command]` 합니다.

사용해야 하는 방법은 수행하는 작업에 따라 다릅니다. Windows 프롬프트 또는 PowerShell 창에서 WSL 명령줄을 열고 종료 하려면 명령을 입력 `exit` 합니다.

## <a name="launch-wsl-by-distribution"></a>배포별 WSL 시작

배포판 특정 애플리케이션을 사용하여 배포를 실행하면 자체 콘솔 창에서 해당 배포가 시작됩니다.

![시작 메뉴에서 WSL 시작](media/start-launch.png)

Microsoft Store에서 "시작"을 클릭하는 것과 같습니다.

![Microsoft Store에서 WSL 시작](media/store-launch.png)

`[distribution].exe`를 실행하여 명령줄에서 배포를 실행할 수도 있습니다.

명령줄에서 이 방식으로 배포를 실행하는 경우 작업 디렉터리가 현재 디렉터리에서 배포의 홈 디렉터리로 자동으로 변경된다는 단점이 있습니다.

**예: (PowerShell 사용)**

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

**예: (PowerShell 사용)**

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

**예: (PowerShell 사용)**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

**예: (PowerShell 사용)**

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

Windows 10 버전 1903 [이상](ms-settings:windowsupdate)에서는를 사용 `wsl.exe` 하 여 Linux 용 Windows 하위 시스템 (wsl)의 배포를 관리할 수 있습니다. 여기에는 사용 가능한 배포 나열, 기본 배포 설정, 배포 제거 등이 포함 됩니다.

각 Linux 배포는 자체 구성을 독립적으로 관리합니다. 배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.  예: `ubuntu /?`.

## <a name="list-distributions"></a>배포 나열

`wsl -l` , `wsl --list`  
WSL에 사용할 수 있는 Linux 배포를 나열합니다.  배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.

`wsl --list --all`현재 사용할 수 없는 모든 배포를 나열 합니다.  이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.  

`wsl --list --running`현재 실행 중인 모든 배포를 나열 합니다.

## <a name="set-a-default-distribution"></a>기본 배포 설정

기본 WSL 배포는 명령줄에서 `wsl`을 실행할 때 실행되는 배포입니다.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

기본 배포를 `<DistributionName>`으로 설정합니다.

**예: (PowerShell 사용)**  
`wsl -s Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.  이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.  `wsl`을 실행하면 Ubuntu 세션이 열립니다.

## <a name="unregister-and-reinstall-a-distribution"></a>배포 등록 취소 및 다시 설치

Linux 배포는 Microsoft Store를 통해 설치할 수 있지만 이를 통해 제거할 수는 없습니다.  WSL Config를 사용하면 배포를 등록 취소/제거할 수 있습니다.

또한 등록을 취소하면 배포를 다시 설치할 수 있습니다.

> **주의:** 등록을 취소 하면 해당 배포와 관련 된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실 됩니다.  스토어에서 다시 설치하면 배포의 새 복사본이 설치됩니다.

`wsl --unregister <DistributionName>`  
WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.

예를 들어 `wsl --unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.  `wsl --list`를 실행하면 나열되지 않습니다.

다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.

## <a name="run-as-a-specific-user"></a>특정 사용자로 실행

`wsl -u <Username>`, `wsl --user <Username>`

WSL을 지정된 사용자로 실행합니다. 사용자는 WSL 배포 내에 있어야 합니다.

## <a name="run-a-specific-distribution"></a>특정 배포 실행

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

WSL의 지정된 배포를 실행합니다. 기본값을 변경하지 않고도 명령을 특정 배포로 보내는 데 사용할 수 있습니다.

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a>이전 Windows 버전에서 여러 Linux 배포 관리

Windows 10 버전 1903 이전에서는 wsl `wslconfig.exe` (linux 용 Windows 하위 시스템)에서 실행 되는 linux 배포를 관리 하는 데 Wsl Config () 명령줄 도구를 사용 해야 합니다.  사용 가능한 배포를 나열하고, 기본 배포를 설정하고, 배포를 제거할 수 있습니다.

WSL Config는 배포를 확장하거나 조정하는 설정에 유용하지만, 각 Linux 배포는 자체 구성을 독립적으로 관리합니다.  배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.  예: `ubuntu /?`.

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

배포를 나열 하려면 다음을 사용 합니다.

`wslconfig /list`  
WSL에 사용할 수 있는 Linux 배포를 나열합니다.  배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.

`wslconfig /list /all`  
현재 사용할 수 없는 배포를 포함하여 모든 배포를 나열합니다.  이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.  

명령줄에서를 실행할 때 실행 되는 기본 배포를 설정 하려면 `wsl` 다음을 수행 합니다.

`wslconfig /setdefault <DistributionName>`기본 분포를로 설정 `<DistributionName>` 합니다.

**예: (PowerShell 사용)**  
`wslconfig /setdefault Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.  이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.  `wsl`을 실행하면 Ubuntu 세션이 열립니다.

배포 등록을 취소 하 고 다시 설치 하려면:

`wslconfig /unregister <DistributionName>`  
WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.

예를 들어 `wslconfig /unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.  `wslconfig /list`를 실행하면 나열되지 않습니다.

다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.

## <a name="configure-per-distro-launch-settings-with-wslconf"></a>Wslconf를 사용 하 여 각 시작 설정 구성

> **Windows 빌드 17093 이상에서 사용 가능**

`wsl.conf`를 사용하여 하위 시스템을 시작할 때마다 적용되는 WSL의 특정 기능을 자동으로 구성합니다.

현재 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함됩니다.

`wsl.conf`는 `/etc/wsl.conf`의 각 Linux 배포에 있습니다. 여기에 파일이 없으면 해당 파일을 직접 만들 수 있습니다. WSL은 파일의 존재 여부를 검색하고 해당 내용을 읽습니다. 파일이 없거나 형식이 잘못된(즉, 잘못된 태그 형식 지정) 경우에도 WSL은 정상적으로 계속 시작됩니다.

다음은 `wsl.conf` 배포에 추가할 수 있는 샘플 파일입니다.

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>구성 옵션

.ini 규칙에 따라 키는 섹션 아래에 선언됩니다. 

WSL은 `automount` 및 `network`의 두 가지 섹션을 지원합니다.

#### <a name="automount"></a>automount

섹션: `[automount]`

| key        | 값                          | default      | 정보                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 사용    | boolean                        | true         | `true`를 사용하면 고정 드라이브(즉, `C:/` 또는 `D:/`)가 `/mnt` 아래의 DrvFs에 자동으로 탑재됩니다.  `false`는 드라이브가 자동으로 탑재 되지 않음을 의미 하지만 수동으로 또는를 통해 탑재할 수 있습니다 `fstab` .                                                                                                             |
| mountFsTab | boolean                        | true         | `true`는 WSL 시작 시 `/etc/fstab`가 처리되도록 설정합니다. /etc/fstab는 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다. 따라서 시작 시 이러한 파일 시스템을 WSL에 자동으로 탑재할 수 있습니다.                                                                                                                |
| root       | String                         | `/mnt/`      | 고정 드라이브가 자동으로 탑재될 디렉터리를 설정합니다. 예를 들어 WSL의 `/windir/`에 디렉터리가 있고 이 디렉터리를 루트로 지정하면 고정 드라이브가 `/windir/c`에 탑재됩니다.                                                                                              |
| 옵션    | 쉼표로 구분된 값 목록 | 빈 문자열 | 이 값은 기본 DrvFs 탑재 옵션 문자열에 추가됩니다. **DrvFs별 옵션만 지정할 수 있습니다.** 탑재 이진 파일이 일반적으로 플래그로 구문 분석되는 옵션은 지원되지 않습니다. 이러한 옵션을 명시적으로 지정하려면 원하는 모든 드라이브를 /etc/fstab에 포함시켜야 합니다. |

기본적으로 WSL은 uid와 gid를 기본 사용자의 값으로 설정합니다(Ubuntu 배포판에서 기본 사용자는 uid=1000, gid=1000으로 만들어짐). 사용자가 이 키를 통해 gid 또는 uid 옵션을 명시적으로 지정하면 연결된 값이 덮어쓰입니다. 그렇지 않으면 항상 기본값이 추가됩니다.

**참고:** 이러한 옵션은 자동으로 탑재 된 모든 드라이브에 대 한 탑재 옵션으로 적용 됩니다. 특정 드라이브에 대한 옵션만 변경하려면 /etc/fstab를 대신 사용합니다.

#### <a name="mount-options"></a>탑재 옵션

Windows 드라이브(DrvFs)에 다른 탑재 옵션을 설정하면 Windows 파일에 대한 파일 사용 권한이 계산되는 방법을 제어할 수 있습니다. 다음 옵션을 사용할 수 있습니다.

| 키 | Description | 기본값 |
|:----|:----|:----|
|uid| 모든 파일의 소유자에게 사용되는 사용자 ID | WSL 배포판의 기본 사용자 ID(처음 설치할 때 기본값은 1000으로 설정됨)
|gid| 모든 파일의 소유자에게 사용되는 그룹 ID | WSL 배포판의 기본 그룹 ID(처음 설치할 때 기본값은 1000으로 설정됨)
|umask | 모든 파일 및 디렉터리에서 제외할 권한의 8진수 마스크 | 000
|fmask | 모든 파일에서 제외할 권한의 8진수 마스크 | 000
|dmask | 모든 디렉터리에서 제외할 권한의 8진수 마스크 | 000

**참고:** 권한 마스크는 파일이 나 디렉터리에 적용 되기 전에 논리적 OR 작업을 통해 배치 됩니다. 

#### <a name="network"></a>네트워크

섹션 레이블: `[network]`

| key | 값 | default | 정보|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`는 WSL에서 `/etc/hosts`를 생성하도록 설정합니다. `hosts` 파일에는 IP 주소에 해당하는 호스트 이름의 정적 맵이 포함됩니다. |
| generateResolvConf | boolean | `true` | `true`는 WSL에서 `/etc/resolv.conf`를 생성하도록 설정합니다. `resolv.conf`에는 지정된 호스트 이름을 해당 IP 주소로 확인할 수 있는 DNS 목록이 포함됩니다. | 

#### <a name="interop"></a>interop

섹션 레이블: `[interop]`

다음 옵션은 참가자 빌드 17713 이상에서 사용할 수 있습니다.

| key | 값 | default | 정보|
|:----|:----|:----|:----|
| 사용 | boolean | `true` | 이 키를 설정하면 WSL에서 Windows 프로세스 시작을 지원하는지 여부가 결정됩니다. |
| appendWindowsPath | boolean | `true` | 이 키를 설정하면 WSL에서 Windows 경로 요소를 $PATH 환경 변수에 추가할지 여부가 결정됩니다. |

#### <a name="user"></a>사용자

섹션 레이블: `[user]`

이러한 옵션은 빌드 18980 이상에서 사용할 수 있습니다.

| key | 값 | default | 정보|
|:----|:----|:----|:----|
| default | 문자열 | 처음 실행할 때 생성 된 초기 사용자 이름입니다. | 이 키를 설정 하면 먼저 WSL 세션을 시작할 때 실행할 사용자를 지정 합니다. |

## <a name="configure-global-options-with-wslconfig"></a>. Wslconfig를 사용 하 여 전역 옵션 구성

> **Windows 빌드 19041 이상에서 사용 가능**

`.wslconfig`사용자 폴더의 루트 디렉터리에 파일을 배치 하 여 global WSL 옵션을 구성할 수 있습니다 `C:\Users\<yourUserName>\.wslconfig` . 이 파일에는 다음 옵션이 포함 될 수 있습니다.

### <a name="wsl-2-settings"></a>WSL 2 설정

이러한 설정은 모든 WSL 2 배포를 지 원하는 VM에 영향을 줍니다. 

| key | 값 | default | 정보|
|:----|:----|:----|:----|
| 커널(kernel) | 문자열 | Microsoft에서 빌드된 커널을 제공 받은 수신함 | 사용자 지정 Linux 커널의 절대 Windows 경로입니다. |
| 메모리 | 크기 | Windows에서 총 메모리의 80% | WSL 2 VM에 할당할 메모리의 양입니다. |
| 프로세서 | number | Windows에서 동일한 수의 프로세서 | WSL 2 VM에 할당할 프로세서 수입니다. |
| localhostForwarding | boolean | `true` | WSL 2 VM의 와일드 카드 또는 localhost에 바인딩된 포트를 localhost: port를 통해 호스트에서 연결할 수 있는지 여부를 지정 하는 부울입니다. |
| kernelCommandLine | 문자열 | 비어 있음 | 추가 커널 명령줄 인수입니다. |
| swap | 크기 | Windows에서 메모리 크기의 25%가 가장 가까운 GB로 반올림 됨 | WSL 2 VM에 추가할 스왑 공간의 크기 이며, 스왑 파일이 없는 경우 0입니다. |
| 스왑 파일 | 크기 | %USERPROFILE%\AppData\Local\Temp\swap.vhdx | 스왑 가상 하드 디스크에 대 한 절대 Windows 경로입니다. |

값이 인 항목은 `path` 이스케이프 된 백슬래시가 포함 된 Windows 경로 여야 합니다. 예:`C:\\Temp\\myCustomKernel`

값이 인 항목은 `size` 크기와 그 뒤에 단위를 사용 해야 합니다 (예: `8GB` 또는) `512MB` .