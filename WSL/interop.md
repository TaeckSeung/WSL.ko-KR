---
title: Windows의 Linux 상호 운용성
description: Linux 용 Windows 하위 시스템에서 실행 중인 Linux 배포를 사용 하 여 Windows 상호 운용성을 설명 합니다.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063251"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows와 Linux 상호 운용성에 대 한 Windows 하위 시스템

> **Fall Creators Update에 대 한 업데이트 합니다.**  
크리에이터 스 업데이트 또는 1 주년 업데이트를 실행 하는 경우으로 이동 합니다 [작성자/1 주년 업데이트 섹션](interop.md#creators-update-and-anniversary-update)합니다.

Windows 하위 시스템에 대 한 WSL (Linux)는 Windows와 Linux의 통합을 지속적으로 개선 합니다.  다음 작업을 수행할 수 있습니다.

1. Linux 콘솔에서 Windows 이진 파일을 호출 합니다.
1. Windows 콘솔에서 Linux 이진 파일을 호출 합니다.
1. **Windows 참가자 빌드 17063 +** Linux와 Windows 간의 환경 변수를 공유 합니다.

이 Windows 및 WSL 간의 원활한 환경을 제공합니다.  기술 세부 정보에는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)합니다.

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows 명령줄에서 Linux 도구를 실행 합니다.

Linux 이진 파일을 사용 하 여 Windows 명령 프롬프트 (CMD 또는 PowerShell)에서 실행 `wsl.exe <command>`합니다.

이러한 방식으로 호출 하는 이진 파일:

1. 현재 CMD 또는 PowerShell 프롬프트와 같은 작업 디렉터리를 사용 합니다.
1. WSL 기본 사용자로 실행 합니다.
1. 터미널 호출 하는 프로세스와 동일한 Windows 관리자 권한이 있어야.

예를 들어 다음과 같은 가치를 제공해야 합니다.

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

다음 Linux 명령 `wsl.exe` WSL에서 실행할 명령 처럼 처리 됩니다.  Sudo, 파이핑 파일 리디렉션 등 작동 합니다.

Sudo를 사용 하는 예제:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

혼합 WSL 및 Windows 명령 예제:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

에 전달 된 명령을 `wsl.exe` 수정 하지 않고 WSL 프로세스에 전달 됩니다.  WSL 형식으로 파일 경로 지정 해야 합니다.

예제 경로:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL에서 Windows 도구를 실행 합니다.

WSL 사용 하 여 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다 `[binary name].exe`합니다.  `notepad.exe`) 을 입력합니다.  Linux에서 Windows 실행 파일을 더 쉽게 실행 하려면 Windows 경로가 포함 되어 `$PATH` Fall Creators Update에 있습니다.

이러한 방식으로 실행 하는 응용 프로그램에 다음 속성이 있습니다.

1. WSL 명령 프롬프트를 작업 디렉터리를 유지 합니다. 대부분의-예외는 아래에서 설명 합니다.
1. WSL 프로세스와 동일한 권한 권한을 갖습니다.
1. 현재 Windows 사용자로 실행 합니다.
1. Windows 작업 관리자에서 표시 CMD 프롬프트에서 직접 실행 하는 경우.

예:

``` BASH
$ notepad.exe
```

WSL에서 실행 되는 Windows 실행 파일에 네이티브 Linux 실행-리디렉션, 파이핑 및 예상 대로 작업을 backgrounding도 마찬가지로 처리 됩니다.

파이프를 사용 하는 예제:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

혼합 된 Windows 및 WSL 명령을 사용 하는 예제:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 이진 파일 확장명을 포함 하 고 파일 대/소문자 구분 하 고 실행 가능 해야 합니다.  비-실행 파일 포함 하 여 스크립트를 일괄 처리 합니다.  와 같은 네이티브 명령도 CMD `dir` 실행할 수 있습니다 `cmd.exe /C` 명령입니다.

예를 들면 다음과 같습니다.

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

매개 변수는 수정 되지 않은 Windows 이진에 전달 됩니다.

예를 들어 다음 명령은 열립니다 `C:\temp\foo.txt` 에서 `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs에 있는 파일을 수정 (아래 하지 파일 `/mnt/<x>`)는 Windows WSL에서 응용 프로그램은 지원 되지 않습니다.

기본적으로 WSL는 Windows의 작업 디렉터리를 현재 WSL 디렉터리로 이진 상태를 유지 하려고 하지만 작업 디렉터리 VolFs 켜져 있으면 인스턴스 생성 디렉터리에 다시 대체 됩니다.

예를 들어; `wsl.exe` 에서 처음 시작 `C:\temp` 하며 현재 WSL 디렉터리 사용자의 홈으로 변경 됩니다.  때 `notepad.exe` 호출 되는 사용자의 홈 디렉터리에서 WSL 자동으로 되돌아갑니다 `C:\temp` notepad.exe 작업 디렉터리로:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows 및 WSL 간에 공유 환경 변수

> Windows Insider 빌드 17063 이상에서 사용할 수 있습니다.

Windows 환경 변수 하나만 WSL 액세스할 수 있는 17063, 이전 `PATH` (따라서 WSL에서 Win32 실행 파일을 시작할 수 있습니다).

WSL 및 Windows 공유 17063부터 `WSLENV`, WSL에서 실행 되는 Windows 및 Linux 배포판을 생성 하는 특별 한 환경 변수입니다.

속성의 `WSLENV`:

* 공유 상태 Windows 및 WSL 환경 모두에 존재 합니다.
* WSL 및 Windows 간에 공유할 수 있는 환경 변수의 목록입니다.
* Windows 및 WSL에서 제대로 작동 하도록 환경 변수 형식을 지정할 수 것입니다.

사용할 수 있는 네 개의 플래그는 `WSLENV` 해당 환경 변수는 변환 하는 방법에 영향을 줍니다.

`WSLENV` 플래그:

* `/p` -Win32 및 WSL/Linux 스타일 경로 간의 경로 변환 합니다.
* `/l` -환경 변수가 경로 목록을 나타냅니다.
* `/u` -이 환경 변수만 포함 되어야 함을 WSL Win32에서 실행 하는 경우를 나타냅니다.
* `/w` -이 환경 변수만 포함 되어야 함을 WSL에서 Win32를 실행 하는 경우를 나타냅니다.

필요에 따라 플래그를 결합할 수 있습니다.

## <a name="disable-interop"></a>Interop을 사용 하지 않도록 설정

사용자는 루트로 다음 명령을 실행 하 여 단일 WSL 세션에 대 한 Windows 이진 파일을 실행 하는 기능을 비활성화할 수 있습니다.

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows를 다시 사용 하도록 설정 하려면 이진 파일 모든 WSL 세션을 종료 및 bash.exe를 다시 실행 하거나 루트로 다음 명령을 실행 합니다.

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Interop을 사용 하지 않도록 설정 WSL 세션 간에 유지 되지 않습니다. 즉 interop 새 세션을 시작할 때 다시 사용할 수는 있습니다.

## <a name="creators-update-and-anniversary-update"></a>크리에이터 업데이트 및 1 주년 업데이트

Interop 환경 사전 Fall Creators Update는 최신 interop 환경을 비슷하지만 주요 차이점 중 handfull 가지 있습니다.

요약:

* `bash.exe` 더 이상 사용 되지 않으며로 대체 되었습니다 `wsl.exe`합니다.
* `-c` 필요 하지 않습니다 단일 명령 실행에 대 한 옵션 `wsl.exe`합니다.
* Windows 경로 WSL에 포함 된 `$PATH`

Interop을 사용 하지 않도록 설정 하는 것에 대 한 프로세스 변경 되지 않습니다.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Windows 명령줄에서 호출 WSL

Windows 명령 프롬프트에서 또는 PowerShell에서 Linux 이진 파일을 호출할 수 있습니다.  이러한 방식으로 호출 하는 이진 파일에 다음 속성이 있습니다.

1. CMD 또는 PowerShell 프롬프트와 같은 작업 디렉터리를 사용 합니다.
1. WSL 기본 사용자로 실행 합니다.
1. 터미널 호출 하는 프로세스와 동일한 Windows 관리자 권한이 있어야.

예:

```console
C:\temp> bash -c "ls -la"
```

이러한 방식으로 호출 하는 Linux 명령은 다른 Windows 응용 프로그램과 마찬가지로 처리 됩니다.  입력, 파이핑 및 파일 리디렉션 등 예상 대로 작동 합니다.

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

WSL 명령을 전달할 `bash -c` 수정 하지 않고 WSL 프로세스에 전달 됩니다.  WSL 형식으로 파일 경로 지정 해야 합니다 및 관련 문자 이스케이프에 주의 해야 합니다. 예:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL에서 Windows 바이너리를 호출합니다.

Linux 용 Windows 하위 시스템에는 Windows 이진 WSL 명령줄에서 직접 호출할 수 있습니다.  이러한 방식으로 실행 하는 응용 프로그램에 다음 속성이 있습니다.

1. 아래에 설명 된 시나리오에서 제외 하 고 WSL 명령 프롬프트를 작업 디렉터리를 유지 합니다.
1. 와 동일한 권한 권한이 `bash.exe` 프로세스입니다. 
1. 현재 Windows 사용자로 실행 합니다.
1. Windows 작업 관리자에서 표시 CMD 프롬프트에서 직접 실행 하는 경우.

예:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL를 이러한 실행 파일 네이티브 Linux 실행 파일을 비슷하게 처리 됩니다.  즉, Linux 경로에 디렉터리를 추가 하 고 예상 대로 명령이 작동 간의 파이핑 합니다.  예를 들면 다음과 같습니다.

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 이진 파일 확장명을 포함 하 고 파일 대/소문자 구분 하 고 실행 가능 해야 합니다.  비-실행 파일 포함 하 여 일괄 처리 스크립트 및와 같은 명령을 `dir` 실행할 수 있습니다 `/mnt/c/Windows/System32/cmd.exe /C` 명령입니다.

예를 들면 다음과 같습니다.

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

매개 변수는 수정 되지 않은 Windows 이진에 전달 됩니다.  

예를 들어 다음 명령은 열립니다 `C:\temp\foo.txt` 에서 `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs에 있는 파일을 수정 (아래 하지 파일 `/mnt/<x>`)는 Windows 응용 프로그램은 지원 되지 않습니다.  기본적으로 WSL 현재 WSL 디렉터리로 이진을 Windows의 작업 디렉터리를 유지 하려고 하지만 작업 디렉터리 VolFs 켜져 있으면 인스턴스 생성 디렉터리에 다시 대체 됩니다.

예를 들어; `bash.exe` 에서 처음 시작 `C:\temp` 하며 현재 WSL 디렉터리 사용자의 홈으로 변경 됩니다.  때 `notepad.exe` 호출 되는 사용자의 홈 디렉터리에서 WSL 자동으로 되돌아갑니다 `C:\temp` notepad.exe 작업 디렉터리로:

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
