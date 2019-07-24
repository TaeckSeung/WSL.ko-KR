---
title: Linux 용 Windows 하위 시스템 명령 참조
description: Linux 용 Windows 하위 시스템을 관리 하는 명령 목록
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307652"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에 대 한 명령 참조

Linux 용 Windows 하위 시스템을 조작 하는 가장 좋은 방법은 `wsl.exe` 명령을 사용 하는 것입니다. 

## `wsl.exe` 

다음은 Windows 버전 1903를 사용 하 `wsl.exe` 는 경우 모든 옵션을 포함 하는 목록입니다.

* Linux 이진 파일을 실행 하기 위한 인수:

    * 명령줄이 제공 되지 않은 경우 wsl .exe는 기본 셸을 시작 합니다.

    * --exec,-e<CommandLine>
        * 기본 Linux 셸을 사용 하지 않고 지정 된 명령을 실행 합니다.

    * --
        * 나머지 명령줄을 있는 그대로 전달 합니다.

* 옵션:
    * --분포,-d<Distro>
        * 지정 된 분포를 실행 합니다.

    * --사용자,-u<UserName>
        * 지정 된 사용자로 실행 합니다.

* Linux 용 Windows 하위 시스템을 관리 하기 위한 인수:

    * --내보내기 <Distro><FileName>
        * 배포를 tar 파일로 내보냅니다.
        표준 출력의 경우 파일 이름으로 지정할 수 있습니다.

    * --import <Distro> <InstallLocation>[Options <FileName> ]
        * 지정 된 tar 파일을 새 배포로 가져옵니다.
        표준 입력의 경우 파일 이름으로 지정할 수 있습니다.

        * 옵션:
            * --version <Version> 새 배포에 사용할 버전을 지정 합니다.

    * --list,-l [Options]
        * 분포를 나열 합니다.

        * 옵션:
            * --모두
                * 현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.

            * --실행 중
                * 현재 실행 중인 배포만 나열 합니다.

    * --set-기본값,-s<Distro>
        * 분포를 기본값으로 설정 합니다.

    * --set-기본값-버전<Version>
        * 새 배포에 대 한 기본 설치 버전을 변경 합니다.

    * --set-version <Distro><Version>
        * 지정 된 분포의 버전을 변경 합니다.

    * --terminate,-t<Distro>
        * 지정 된 분포를 종료 합니다.

    * --등록 취소<Distro>
        * 배포를 등록 취소 합니다.

    * --help
        * 사용법 정보를 표시합니다.

## <a name="additional-commands"></a>추가 명령

또한 Linux 용 Windows 하위 시스템을 조작 하는 기록 명령도 있습니다. 해당 기능은에 포함 `wsl.exe`되어 있지만 여전히 사용할 수 있습니다. 

### `wslconfig.exe`

이 명령을 사용 하 여 WSL 배포를 구성할 수 있습니다. 다음은 해당 옵션의 목록입니다.

* /l,/list [Option]
    * 등록 된 배포를 나열 합니다.
        * /all-필요에 따라 현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.

        * /실행 중-현재 실행 중인 배포만 나열 합니다.

* /s,/setdefault<DistributionName>
    * 분포를 기본값으로 설정 합니다.

* /t,/종료<DistributionName>
    * 분포를 종료 합니다.

* /u,/unregister<DistributionName>
    * 배포를 등록 취소 합니다.

### `bash.exe`

이 명령은 bash 셸을 시작 하는 데 사용 됩니다. 다음은이 명령에서 사용할 수 있는 옵션입니다.

* 지정 된 옵션이 없습니다.
    * 현재 디렉터리에서 Bash 셸을 시작 합니다. Bash 셸이 설치 되어 있지 않으면 자동으로 실행 됩니다.`lxrun /install`

* bash ~
    * 사용자의 홈 디렉터리에 bash 셸을 시작 합니다.  실행과 `cd ~`비슷합니다.

* bash-c "&lt;명령&gt;"
    * 명령을 실행 하 고 출력을 출력 한 다음 Windows 명령 프롬프트로 다시 종료 합니다. <br/> <br/> 예 들어`bash -c "ls"`

## <a name="deprecated-commands"></a>사용 되지 않는 명령

는 `lxrun.exe` Linux 용 Windows 하위 시스템을 설치 하 고 관리 하는 데 사용 되는 첫 번째 명령입니다. Windows 10 1803 이상에서 사용 되지 않습니다.

명령을 `lxrun.exe` 사용 하 여 [Linux 용 Windows 하위 시스템 (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) 을 직접 조작할 수 있습니다.  이러한 명령은 `\Windows\System32` 디렉터리에 설치 되며, Windows 명령 프롬프트 또는 PowerShell 내에서 실행할 수 있습니다.

| Command                     | 설명                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 명령은 WSL 인스턴스를 관리 하는 데 사용 됩니다. |
| `lxrun /install`            | 다운로드 및 설치 프로세스를 시작 합니다. <br/> 모든 프롬프트를 무시 하도록 **/y** 를 추가할 수 있습니다.  확인 메시지가 자동으로 수락 되 고 기본 사용자가 root로 설정 됩니다.          |
| `lxrun /uninstall`          | Ubuntu 이미지를 제거 하 고 삭제 합니다.  기본적으로 사용자의 Ubuntu 홈 디렉터리는 제거 되지 않습니다. <br/> 자동으로 확인 메시지를 수락 하도록 **/y** 를 추가할 수 있습니다. <br/>**/full** 사용자의 Ubuntu 홈 디렉터리를 제거 하 고 삭제 합니다.         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu 사용자에 대 한 기본 Bash를 설정 합니다. 지정 된 사용자가 없는 경우 암호를 입력 하 라는 메시지가 표시 됩니다.  자세한 내용은을 참조 https://aka.ms/wslusers 하세요. <br/> **/y** 암호에 대 한 promping를 무시 합니다.  사용자가 암호 없이 만들어집니다.|
| `lxrun /update`            | 하위 시스템의 패키지 인덱스를 업데이트 합니다.          |
