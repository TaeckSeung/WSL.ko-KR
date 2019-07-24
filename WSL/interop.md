---
title: Linux와 Windows의 상호 운용성
description: Linux 용 Windows 하위 시스템에서 실행 되는 Linux 배포판과의 Windows 상호 운용성에 대해 설명 합니다.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040822"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows와 Linux의 상호 운용성을 위한 windows 하위 시스템

> **업데이트를 업데이트 합니다.**  
작성자 업데이트 또는 기념일 업데이트를 실행 하는 경우 [작성자/기념일 업데이트 섹션](interop.md#creators-update-and-anniversary-update)으로 이동 합니다.

WSL (Linux 용 Windows 하위 시스템)은 지속적으로 Windows와 Linux 간의 통합을 개선 하 고 있습니다.  다음 작업을 수행할 수 있습니다.

1. Linux 콘솔에서 Windows 이진 파일을 호출 합니다.
1. Windows 콘솔에서 Linux 이진 파일을 호출 합니다.
1. **Windows 참가자는 17063 +를 빌드합니다** . Linux와 Windows 간의 환경 변수를 공유 합니다.

Windows와 WSL 간에 원활한 환경을 제공 합니다.  기술 세부 정보는 [Wsl 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)에 있습니다.

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows 명령줄에서 Linux 도구 실행

을 사용 하 여 `wsl.exe <command>`Windows 명령 프롬프트 (CMD 또는 PowerShell)에서 Linux 이진 파일을 실행 합니다.

이러한 방식으로 호출 되는 이진 파일은 다음과 같습니다.

1. 현재 CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용 합니다.
1. WSL 기본 사용자로 실행 합니다.
1. 호출 프로세스 및 터미널과 동일한 Windows 관리 권한이 있어야 합니다.

이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

다음 `wsl.exe` Linux 명령은 wsl에서 실행 되는 명령 처럼 처리 됩니다.  Sudo, 배관 및 파일 리디렉션과 같은 작업을 수행 합니다.

Sudo를 사용 하는 예제:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

WSL 및 Windows 명령의 혼합 예:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

에 `wsl.exe` 전달 된 명령은 수정 하지 않고 wsl 프로세스로 전달 됩니다.  파일 경로는 WSL 형식으로 지정 해야 합니다.

경로의 예:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL에서 Windows 도구 실행

WSL은를 사용 하 여 `[binary name].exe`wsl 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.  `notepad.exe` )을 입력합니다.  Windows 실행 파일을 더 쉽게 실행 하기 위해 windows 경로는 is is 크리에이터 `$PATH` 업데이트의 Linux에 포함 되어 있습니다.

이러한 방식으로 실행 되는 응용 프로그램에는 다음과 같은 속성이 있습니다.

1. 작업 디렉터리를 WSL 명령 프롬프트로 유지 합니다. 대부분의 경우 예외는 아래에 설명 되어 있습니다.
1. WSL 프로세스와 동일한 권한 권한을 갖습니다.
1. 활성 Windows 사용자로 실행 합니다.
1. CMD 프롬프트에서 직접 실행 한 것 처럼 Windows 작업 관리자에 표시 됩니다.

예:

``` BASH
$ notepad.exe
```

WSL에서 실행 되는 Windows 실행 파일은 기본 Linux 실행 파일 (파이프, 리디렉션 및 backgrounding 작업)과 유사 하 게 처리 됩니다.

파이프를 사용 하는 예제:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Mixed Windows 및 WSL 명령을 사용 하는 예제:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 바이너리는 파일 확장명을 포함 하 고, 파일 대 소문자와 일치 하며, 실행 파일 이어야 합니다.  일괄 처리 스크립트를 포함 하는 실행 파일입니다.  명령을 사용 하 여 `cmd.exe /C` 명령을 실행할 수있습니다.`dir`

예를 들면 다음과 같습니다.

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

매개 변수는 수정 되지 않은 상태로 Windows 이진에 전달 됩니다.

예를 들어 다음 명령은에서 `C:\temp\foo.txt` `notepad.exe`열립니다.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Windows 응용 프로그램을 사용 하 여 volfs ( `/mnt/<x>`아래에 있지 않은 파일)에 있는 파일을 수정 하는 것은 지원 되지 않습니다.

기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지 하려고 하지만 작업 디렉터리가 VolFs에 있는 경우에는 인스턴스 만들기 디렉터리를 대체 합니다.

예를 들어 는 처음에에서 `C:\temp` 시작 되 고 현재 wsl 디렉터리가 사용자의 홈으로 변경 됩니다. `wsl.exe`  사용자 `notepad.exe` 의 홈 디렉터리에서를 호출 하는 경우 wsl은 notepad.exe 작업 `C:\temp` 디렉터리로 자동으로 되돌아갑니다.

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows와 WSL 간에 환경 변수 공유

> Windows 참가자 빌드 17063 이상에서 사용할 수 있습니다.

17063 이전에는 wsl에서 액세스할 수 있는 Windows 환경 변수만이 `PATH` 에 액세스할 수 있습니다. 따라서 wsl에서 Win32 실행 파일을 시작할 수 있습니다.

17063부터 wsl 및 windows 공유 `WSLENV`에서 wsl에서 실행 되는 Windows 및 Linux 배포판을 연결 하기 위해 만든 특수 환경 변수입니다.

`WSLENV`속성:

* 공유 됩니다. Windows 및 WSL 환경에 모두 있습니다.
* Windows와 WSL 간에 공유할 환경 변수의 목록입니다.
* Windows 및 WSL에서 잘 작동 하도록 환경 변수의 형식을 지정할 수 있습니다.

에서 `WSLENV` 사용할 수 있는 네 가지 플래그는 환경 변수를 변환 하는 방법에 영향을 줍니다.

`WSLENV`flags

* `/p`-WSL/Linux 스타일 경로와 Win32 경로 간의 경로를 변환 합니다.
* `/l`-환경 변수가 경로 목록 임을 나타냅니다.
* `/u`-이 환경 변수는 Win32에서 WSL을 실행할 때만 포함 되어야 함을 나타냅니다.
* `/w`-이 환경 변수는 WSL에서 Win32를 실행할 때만 포함 되어야 함을 나타냅니다.

필요에 따라 플래그를 결합할 수 있습니다.

## <a name="disable-interop"></a>Interop 사용 안 함

사용자는 루트로 다음 명령을 실행 하 여 단일 WSL 세션에 대해 Windows 이진 파일을 실행 하는 기능을 사용 하지 않도록 설정할 수 있습니다.

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows 이진 파일을 다시 활성화 하려면 모든 WSL 세션을 종료 하 고 bash를 다시 실행 하거나 다음 명령을 루트로 실행 합니다.

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Interop를 사용 하지 않도록 설정 하는 것은 WSL 세션 간에 유지 되지 않습니다. 새 세션이 시작 되 면 interop가 다시 활성화 됩니다.

## <a name="creators-update-and-anniversary-update"></a>작성자 업데이트 및 기념일 업데이트

Interop 환경 이전 버전의 작성자 업데이트는 최신 interop 환경과 유사 하지만 몇 가지 주요 차이점이 있습니다.

요약하면 다음과 같습니다.

* `bash.exe`는 더 이상 사용 되지 않으며 `wsl.exe`로 대체 되었습니다.
* `-c`에서 단일 명령을 실행 하 `wsl.exe`는 옵션은 필요 하지 않습니다.
* Windows 경로는 WSL에 포함 되어 있습니다.`$PATH`

Interop를 사용 하지 않도록 설정 하는 프로세스는 변경 되지 않습니다.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Windows 명령줄에서 WSL 호출

Linux 이진 파일은 Windows 명령 프롬프트 또는 PowerShell에서 호출할 수 있습니다.  이러한 방식으로 호출 되는 이진 파일에는 다음과 같은 속성이 있습니다.

1. CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용 합니다.
1. WSL 기본 사용자로 실행 합니다.
1. 호출 프로세스 및 터미널과 동일한 Windows 관리 권한이 있어야 합니다.

예:

```console
C:\temp> bash -c "ls -la"
```

이러한 방식으로 호출 되는 Linux 명령은 다른 Windows 응용 프로그램과 마찬가지로 처리 됩니다.  입력, 파이프 및 파일 리디렉션과 같은 항목은 예상 대로 작동 합니다.

예를 들면 다음과 같습니다.

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

에 `bash -c` 전달 된 wsl 명령은 수정 하지 않고 wsl 프로세스로 전달 됩니다.  파일 경로는 WSL 형식으로 지정 해야 하며 관련 문자를 이스케이프 처리 하는 데 필요 합니다. 예:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL에서 Windows 이진 파일 호출

Linux 용 Windows 하위 시스템은 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.  이러한 방식으로 실행 되는 응용 프로그램에는 다음과 같은 속성이 있습니다.

1. 아래에 설명 된 시나리오를 제외 하 고 작업 디렉터리를 WSL 명령 프롬프트로 유지 합니다.
1. `bash.exe` 프로세스와 동일한 권한 권한을 갖습니다. 
1. 활성 Windows 사용자로 실행 합니다.
1. CMD 프롬프트에서 직접 실행 한 것 처럼 Windows 작업 관리자에 표시 됩니다.

예:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL에서 이러한 실행 파일은 네이티브 Linux 실행 파일과 유사 하 게 처리 됩니다.  즉, Linux 경로에 디렉터리를 추가 하 고 명령 사이에 있는 파이핑을 정상적으로 작동 합니다.  예를 들면 다음과 같습니다.

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 바이너리는 파일 확장명을 포함 하 고, 파일 케이스와 일치 하며, 실행 파일 이어야 합니다.  명령을 사용 `dir` `/mnt/c/Windows/System32/cmd.exe /C` 하 여 실행 될 수 있는 것과 같은 일괄 처리 스크립트 및 명령을 포함 하는 실행 파일입니다.

예를 들면 다음과 같습니다.

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

매개 변수는 수정 되지 않은 상태로 Windows 이진에 전달 됩니다.  

예를 들어 다음 명령은에서 `C:\temp\foo.txt` `notepad.exe`열립니다.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Windows 응용 프로그램을 사용 하 여 volfs ( `/mnt/<x>`아래에 있지 않은 파일)에 있는 파일은 수정할 수 없습니다.  기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지 하려고 하지만 작업 디렉터리가 VolFs에 있는 경우에는 인스턴스 만들기 디렉터리를 대체 합니다.

예를 들어 는 처음에에서 `C:\temp` 시작 되 고 현재 wsl 디렉터리가 사용자의 홈으로 변경 됩니다. `bash.exe`  사용자 `notepad.exe` 의 홈 디렉터리에서를 호출 하는 경우 wsl은 notepad.exe 작업 `C:\temp` 디렉터리로 자동으로 되돌아갑니다.

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
