---
title: Linux와 Windows의 상호 운용성
description: Linux용 Windows 하위 시스템에서 실행되는 Linux 배포와의 Windows 상호 운용성에 대해 설명합니다.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122729"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows와 Linux용 Windows 하위 시스템의 상호 운용성

> **Fall Creators Update로 업데이트되었습니다.**  
크리에이터스 업데이트 또는 1주년 업데이트를 실행하는 경우 [크리에이터스/1주년 업데이트 섹션](interop.md#creators-update-and-anniversary-update)으로 이동합니다.

WSL(Linux용 Windows 하위 시스템)은 Windows와 Linux 간의 통합을 지속적으로 향상시키고 있습니다.  다음을 수행할 수 있습니다.

1. Linux 콘솔에서 Windows 이진 파일을 호출합니다.
1. Windows 콘솔에서 Linux 이진 파일을 호출합니다.
1. **Windows 참가자 빌드 17063 이상** Linux와 Windows 간에 환경 변수를 공유합니다.

이렇게 하면 Windows와 WSL 간에 원활한 환경이 제공됩니다.  기술 세부 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)에 있습니다.

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows 명령줄에서 Linux 도구 실행

`wsl.exe <command>`를 사용하여 Windows 명령 프롬프트(CMD 또는 PowerShell)에서 Linux 이진 파일을 실행합니다.

이진 파일은 다음과 같은 방식으로 호출됩니다.

1. 현재 CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용합니다.
1. WSL 기본 사용자로 실행합니다.
1. 호출 프로세스 및 터미널과 동일한 Windows 관리 권한을 사용합니다.

예를 들어 다음과 같은 가치를 제공해야 합니다.

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

`wsl.exe` 뒤에 나오는 Linux 명령은 WSL에서 실행되는 명령처럼 처리됩니다.  sudo, 파이핑, 파일 리디렉션과 같은 작업이 작동합니다.

sudo를 사용하는 예제:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

WSL 및 Windows 명령을 혼합한 예제:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

`wsl.exe`에 전달된 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.  파일 경로는 WSL 형식으로 지정해야 합니다.

경로가 포함된 예제:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL에서 Windows 도구 실행

WSL은 `[binary name].exe`를 사용하여 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.  예를 들면 `notepad.exe`입니다.  Windows 실행 파일을 더 쉽게 실행하기 위해 Windows 경로가 Fall Creators Update의 Linux `$PATH`에 포함됩니다.

이 방식으로 실행되는 애플리케이션에는 다음과 같은 속성이 있습니다.

1. 작업 디렉터리를 WSL 명령 프롬프트로 유지합니다(대부분의 경우에 해당, 예외는 아래에 설명되어 있음).
1. WSL 프로세스와 동일한 권한을 갖습니다.
1. 활성 Windows 사용자로 실행합니다.
1. CMD 프롬프트에서 직접 실행한 것처럼 Windows 작업 관리자에 표시됩니다.

예제:

``` BASH
$ notepad.exe
```

WSL에서 실행되는 Windows 실행 파일은 네이티브 Linux 실행 파일과 비슷하게 처리됩니다(파이핑, 리디렉션 및 백그라운드 작업이 예상대로 작동).

파이프를 사용하는 예제:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

혼합된 Windows와 WSL 명령을 사용하는 예제:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 이진 파일은 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.  일괄 처리 스크립트가 포함된 비실행 파일이 있습니다.  `dir`과 같은 CMD 기본 명령은 `cmd.exe /C` 명령을 사용하여 실행할 수 있습니다.

예제:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

매개 변수는 수정되지 않은 Windows 이진 파일에 전달됩니다.

예를 들어 다음 명령은 `notepad.exe`에서 `C:\temp\foo.txt`를 엽니다.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs에 있는 파일(`/mnt/<x>` 아래에 없는 파일)은 WSL에서 Windows 애플리케이션을 사용하여 수정할 수 없습니다.

기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지하려고 하지만, 작업 디렉터리가 VolFs에 있는 경우 인스턴스 만들기 디렉터리로 대체됩니다.

예를 들어 `wsl.exe`가 처음에는 `C:\temp`에서 시작되고, 현재 WSL 디렉터리가 사용자의 홈으로 변경됩니다.  사용자의 홈 디렉터리에서 `notepad.exe`를 호출하면 WSL이 자동으로 notepad.exe의 작업 디렉터리인 `C:\temp`로 되돌아갑니다.

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows와 WSL 간의 환경 변수 공유

> Windows 참가자 빌드 17063 이상에서 사용할 수 있습니다.

17063 이전에서는 `PATH`만 WSL에서 액세스할 수 있는 Windows 환경 변수였습니다(이를 통해 WSL 아래에서 Win32 실행 파일을 시작할 수 있었음).

17063부터 WSL 및 Windows는 WSL에서 실행되는 Windows 및 Linux 배포판을 연결하기 위해 만든 특수 환경 변수인 `WSLENV`를 공유합니다.

`WSLENV`의 속성:

* 공유되며, Windows 및 WSL 환경 모두에 있습니다.
* Windows와 WSL 간에 공유할 환경 변수의 목록입니다.
* Windows 및 WSL에서 제대로 작동하도록 환경 변수의 형식을 지정할 수 있습니다.

`WSLENV`에는 해당 환경 변수가 변환되는 방법에 영향을 주는 4개의 플래그를 사용할 수 있습니다.

`WSLENV` 플래그:

* `/p` - WSL/Linux 스타일 경로 및 Win32 경로 간의 경로를 변환합니다.
* `/l` - 환경 변수가 경로 목록임을 나타냅니다.
* `/u` - Win32에서 WSL을 실행하는 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.
* `/w` - WSL에서 Win32를 실행할 때만 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.

플래그는 필요에 따라 결합할 수 있습니다.

## <a name="disable-interop"></a>Interop 사용 안 함

사용자는 다음 명령을 루트로 실행하여 단일 WSL 세션에서 Windows 이진 파일을 실행하는 기능을 사용하지 않도록 설정할 수 있습니다.

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows 이진 파일을 다시 사용하도록 설정하려면 모든 WSL 세션을 종료하고 bash.exe를 다시 실행하거나 다음 명령을 루트로 실행합니다.

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

interop를 사용하지 않도록 설정하는 것은 WSL 세션 간에 유지되지 않습니다. 새 세션이 시작되면 interop가 사용하도록 다시 설정됩니다.

## <a name="creators-update-and-anniversary-update"></a>크리에이터스 업데이트 및 1주년 업데이트

Fall Creators Update 이전의 interop 환경은 최신 interop 환경과 비슷하지만 몇 가지 주요 차이점이 있습니다.

요약하면 다음과 같습니다.

* `bash.exe`가 더 이상 사용되지 않으며 `wsl.exe`로 대체되었습니다.
* `wsl.exe`에는 단일 명령을 실행하기 위한 `-c` 옵션이 필요하지 않습니다.
* Windows 경로가 WSL `$PATH`에 포함됩니다.

interop를 사용하지 않도록 설정하는 프로세스는 변경되지 않습니다.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Windows 명령줄에서 WSL 호출

Linux 이진 파일은 Windows 명령 프롬프트 또는 PowerShell에서 호출할 수 있습니다.  이 방식으로 호출되는 이진 파일에는 다음과 같은 속성이 있습니다.

1. CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용합니다.
1. WSL 기본 사용자로 실행합니다.
1. 호출 프로세스 및 터미널과 동일한 Windows 관리 권한을 사용합니다.

예제:

```console
C:\temp> bash -c "ls -la"
```

이 방식으로 호출되는 Linux 명령은 다른 Windows 애플리케이션처럼 처리됩니다.  입력, 파이핑, 파일 리디렉션과 같은 작업이 예상대로 작동합니다.

예제:

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

`bash -c`에 전달된 WSL 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.  파일 경로는 WSL 형식으로 지정해야 하며, 관련 문자를 이스케이프 방식으로 처리해야 합니다. 예제:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL에서 Windows 이진 파일 호출

Linux용 Windows 하위 시스템은 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.  이 방식으로 실행되는 애플리케이션에는 다음과 같은 속성이 있습니다.

1. 아래에 설명된 시나리오를 제외하고는 작업 디렉터리를 WSL 명령 프롬프트로 유지합니다.
1. `bash.exe` 프로세스와 동일한 권한을 갖습니다. 
1. 활성 Windows 사용자로 실행합니다.
1. CMD 프롬프트에서 직접 실행한 것처럼 Windows 작업 관리자에 표시됩니다.

예제:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL에서는 이러한 실행 파일이 네이티브 Linux 실행 파일과 비슷한 방식으로 처리됩니다.  즉, 디렉터리를 Linux 경로에 추가하고 명령 간의 파이프가 예상대로 작동합니다.  예제:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 이진 파일은 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.  일괄 처리 스크립트 및 `dir`과 같은 명령이 포함된 비실행 파일은 `/mnt/c/Windows/System32/cmd.exe /C` 명령을 사용하여 실행할 수 있습니다.

예제:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

매개 변수는 수정되지 않은 Windows 이진 파일에 전달됩니다.  

예를 들어 다음 명령은 `notepad.exe`에서 `C:\temp\foo.txt`를 엽니다.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs에 있는 파일(`/mnt/<x>` 아래에 없는 파일)은 Windows 애플리케이션을 사용하여 수정할 수 없습니다.  기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지하려고 하지만, 작업 디렉터리가 VolFs에 있는 경우 인스턴스 만들기 디렉터리로 대체됩니다.

예를 들어 `bash.exe`가 처음에는 `C:\temp`에서 시작되고, 현재 WSL 디렉터리가 사용자의 홈으로 변경됩니다.  사용자의 홈 디렉터리에서 `notepad.exe`를 호출하면 WSL이 자동으로 notepad.exe의 작업 디렉터리인 `C:\temp`로 되돌아갑니다.

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
