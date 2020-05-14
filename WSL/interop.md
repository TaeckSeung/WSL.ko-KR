---
title: Linux와 Windows의 상호 운용성
description: Linux용 Windows 하위 시스템에서 실행되는 Linux 배포와의 Windows 상호 운용성에 대해 설명합니다.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: b1c7a64a86cf088159d1abee3b341328151428f6
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270847"
---
# <a name="windows-interoperability-with-linux"></a>Linux와 Windows의 상호 운용성

WSL(Linux용 Windows 하위 시스템)은 Windows와 Linux 간의 통합을 지속적으로 향상시키고 있습니다.  다음을 수행할 수 있습니다.

* Linux 명령줄(즉, Ubuntu)에서 Windows 도구(즉, notepad.exe)를 실행합니다.
* Windows 명령줄(즉, PowerShell)에서 Linux 도구(즉, grep)를 실행합니다.
* Linux와 Windows 간에 환경 변수를 공유합니다. (빌드 17063 이상)

> [!NOTE]
> 크리에이터스 업데이트(2017년 10월 빌드 16299) 또는 1주년 업데이트(2016년 8월 빌드 14393)를 실행하는 경우 [이전 버전의 Windows 10](#earlier-versions-of-windows-10)으로 이동합니다.

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows 명령줄에서 Linux 도구 실행

`wsl <command>`(또는 `wsl.exe <command>`)를 사용하여 CMD(Windows 명령 프롬프트) 또는 PowerShell에서 Linux 이진 파일을 실행합니다.

예:

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

이진 파일은 다음과 같은 방식으로 호출됩니다.

* 현재 CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용합니다.
* WSL 기본 사용자로 실행합니다.
* 호출 프로세스 및 터미널과 동일한 Windows 관리 권한을 사용합니다.

`wsl`(또는 `wsl.exe`) 뒤의 Linux 명령은 WSL에서 실행되는 명령처럼 처리됩니다.  sudo, 파이핑, 파일 리디렉션과 같은 작업이 작동합니다.

sudo를 사용하여 기본 Linux 배포를 업데이트하는 예제:

```powershell
C:\temp> wsl sudo apt-get update
```

이 명령을 실행하면 기본 Linux 배포 사용자 이름이 나열되고 암호를 입력하라는 메시지가 표시됩니다. 암호가 올바르게 입력되면 배포에서 업데이트를 다운로드합니다.

## <a name="mixing-linux-and-windows-commands"></a>Linux 및 Windows 명령 혼합

PowerShell을 사용하여 Linux와 Windows 명령을 혼합하는 몇 가지 예제는 다음과 같습니다.

`ls -la` Linux 명령을 사용하여 파일을 나열하고 `findstr` PowerShell 명령을 사용하여 "git"이 포함된 단어에 대한 결과를 필터링하려면 명령을 다음과 같이 결합합니다.

```powershell
wsl ls -la | findstr "git"
```

`dir` PowerShell 명령을 사용하여 파일을 나열하고 `grep` Linux 명령을 사용하여 "git"이 포함된 단어에 대한 결과를 필터링하려면 명령을 다음과 같이 결합합니다.

```powershell
C:\temp> dir | wsl grep git
```

`ls -la` Linux 명령을 사용하여 파일을 나열하고 `> out.txt` PowerShell 명령을 사용하여 해당 목록을 "out.txt"라는 텍스트 파일로 출력하려면 명령을 다음과 같이 결합합니다.

```powershell
C:\temp> wsl ls -la > out.txt
```

`wsl.exe`에 전달된 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.  파일 경로는 WSL 형식으로 지정해야 합니다.

`ls -la` Linux 명령을 사용하여 `/proc/cpuinfo` Linux 파일 시스템 경로에 있는 파일을 나열하려면 PowerShell을 다음과 같이 사용합니다.

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

`ls -la` Linux 명령을 사용하여 `C:\Program Files` Windows 파일 시스템 경로에 있는 파일을 나열하려면 PowerShell을 다음과 같이 사용합니다.

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a>Linux에서 Windows 도구 실행

WSL에서 `[tool-name].exe`를 사용하여 WSL 명령줄에서 Windows 도구를 직접 실행할 수 있습니다.  정의합니다(예: `notepad.exe`).

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

이 방식으로 실행되는 애플리케이션에는 다음과 같은 속성이 있습니다.

* 작업 디렉터리를 WSL 명령 프롬프트로 유지합니다(대부분의 경우에 해당, 예외는 아래에 설명되어 있음).
* WSL 프로세스와 동일한 권한을 갖습니다.
* 활성 Windows 사용자로 실행합니다.
* CMD 프롬프트에서 직접 실행한 것처럼 Windows 작업 관리자에 표시됩니다.

WSL에서 실행되는 Windows 실행 파일은 네이티브 Linux 실행 파일과 비슷하게 처리됩니다(파이핑, 리디렉션 및 백그라운드 작업이 예상대로 작동).

`ipconfig.exe` Windows 도구를 실행하려면 `grep` Linux 도구를 사용하여 "IPv4" 결과를 필터링하고 `cut` Linux 도구를 사용하여 Linux 배포(예: Ubuntu)에서 열 필드를 제거합니다.

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Windows와 Linux 명령이 혼합된 예제를 사용해 보겠습니다. Linux 배포(즉, Ubuntu)를 열고, `touch foo.txt`라는 텍스트 파일을 만듭니다. 이제 `ls -la` Linux 명령을 사용하여 파일 및 해당 만들기 세부 정보를 직접 나열하고 `findstr.exe` Windows PowerShell 도구를 사용하여 결과를 필터링하여 `foo.txt` 파일만 결과에 표시합니다.

```bash
ls -la | findstr.exe foo.txt
```

Windows 도구는 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.  일괄 처리 스크립트가 포함된 비실행 파일이 있습니다.  `dir`과 같은 CMD 기본 명령은 `cmd.exe /C` 명령을 사용하여 실행할 수 있습니다.

예를 들어 다음을 입력하여 Windows 파일 시스템의 C:\ 디렉터리에 있는 콘텐츠를 나열합니다.

```bash
cmd.exe /C dir
```

또는 `ping` 명령을 사용하여 에코 요청을 microsoft.com 웹 사이트에 보냅니다.

```bash
ping.exe www.microsoft.com
```

매개 변수는 수정되지 않은 Windows 이진 파일에 전달됩니다. 예를 들어 다음 명령은 `notepad.exe`에서 `C:\temp\foo.txt`를 엽니다.

```bash
notepad.exe "C:\temp\foo.txt"
```

또한 다음과 같은 작업도 수행합니다.

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows와 WSL 간의 환경 변수 공유

WSL 및 Windows는 WSL에서 실행되는 Windows 및 Linux 배포를 연결하기 위해 만든 `WSLENV`라는 특수 환경 변수를 공유합니다.

`WSLENV` 변수의 속성은 다음과 같습니다.

* 공유되며, Windows 및 WSL 환경 모두에 있습니다.
* Windows와 WSL 간에 공유할 환경 변수의 목록입니다.
* Windows 및 WSL에서 제대로 작동하도록 환경 변수의 형식을 지정할 수 있습니다.

> [!NOTE]
> 17063 이전에서는 `PATH`만 WSL에서 액세스할 수 있는 Windows 환경 변수였습니다(이를 통해 WSL 아래에서 Win32 실행 파일을 시작할 수 있었음). `WSLENV`는 17063부터 지원됩니다.

## <a name="wslenv-flags"></a>WSLENV 플래그

`WSLENV`에서 4개의 플래그를 사용하여 환경 변수가 변환되는 방법에 영향을 줄 수 있습니다.

`WSLENV` 플래그:

* `/p` - WSL/Linux 스타일 경로 및 Win32 경로 간의 경로를 변환합니다.
* `/l` - 환경 변수가 경로 목록임을 나타냅니다.
* `/u` - Win32에서 WSL을 실행하는 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.
* `/w` - WSL에서 Win32를 실행할 때만 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.

플래그는 필요에 따라 결합할 수 있습니다.

## <a name="disable-interoperability"></a>상호 운용성 사용 안 함

사용자는 다음 명령을 루트로 실행하여 단일 WSL 세션에 대해 Windows 도구를 실행하는 기능을 사용하지 않도록 설정할 수 있습니다.

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows 이진 파일을 다시 사용하도록 설정하려면 모든 WSL 세션을 종료하고 bash.exe를 다시 실행하거나 다음 명령을 루트로 실행합니다.

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

interop를 사용하지 않도록 설정하는 것은 WSL 세션 간에 유지되지 않습니다. 새 세션이 시작되면 interop가 사용하도록 다시 설정됩니다.

## <a name="earlier-versions-of-windows-10"></a>이전 버전의 Windows 10

이전 Windows 10 버전의 상호 운용성 명령에는 몇 가지 차이점이 있습니다. 크리에이터스 업데이트(2017년 10월 빌드 16299) 또는 1주년 업데이트(2016년 8월 빌드 14393) 버전의 Windows 10을 실행하는 경우 [최신 Windows 버전으로 업데이트](ms-settings:windowsupdate)하는 것이 좋습니다. 그러나 최신 버전으로 업데이트할 수 없는 경우 아래에 몇 가지 interop 차이점에 대해 간략히 설명했습니다.

요약:

* `bash.exe`가 `wsl.exe`로 바뀌었습니다.
* `wsl.exe`에는 단일 명령을 실행하기 위한 `-c` 옵션이 필요하지 않습니다.
* Windows 경로가 WSL `$PATH`에 포함됩니다.
* interop를 사용하지 않도록 설정하는 프로세스는 변경되지 않습니다.

Linux 명령은 Windows 명령 프롬프트 또는 PowerShell에서 실행할 수 있지만, 초기 Windows 버전의 경우 `bash` 명령을 사용해야 합니다. 예:

```powershell
C:\temp> bash -c "ls -la"
```

입력, 파이핑, 파일 리디렉션과 같은 작업이 예상대로 작동합니다.

`bash -c`에 전달된 WSL 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.  파일 경로는 WSL 형식으로 지정해야 하며, 관련 문자를 이스케이프 방식으로 처리해야 합니다. 예제:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

또는...

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

이전 버전의 Windows 10에서 WSL 배포를 통해 Windows 도구를 호출하는 경우 디렉터리 경로를 지정해야 합니다. 예를 들어 WSL 명령줄에서 다음을 입력합니다.

```bash
/mnt/c/Windows/System32/notepad.exe
```

WSL에서는 이러한 실행 파일이 네이티브 Linux 실행 파일과 비슷한 방식으로 처리됩니다.  즉, 디렉터리를 Linux 경로에 추가하고 명령 간의 파이프가 예상대로 작동합니다.  예:

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
또는

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Windows 이진 파일은 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.  일괄 처리 스크립트 및 `dir`과 같은 명령이 포함된 비실행 파일은 `/mnt/c/Windows/System32/cmd.exe /C` 명령을 사용하여 실행할 수 있습니다. 예:

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a>추가 리소스

* [2016의 상호 운용성에 대한 WSL 블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
