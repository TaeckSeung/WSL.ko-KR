---
title: Linux용 Windows 하위 시스템에 대한 명령 참조
description: Linux용 Windows 하위 시스템을 관리하는 명령의 목록입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 72b78a73bf68b28dd14b4826943a0c81ea04bbad
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270877"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템에 대한 명령 참조

Linux용 Windows 하위 시스템과 상호 작용하는 가장 좋은 방법은 `wsl.exe` 명령을 사용하는 것입니다.

## <a name="set-wsl-2-as-your-default-version"></a>WSL 2를 기본 버전으로 설정

새 Linux 배포를 설치할 때 Powershell에서 다음 명령을 실행하여 WSL 2를 기본 버전으로 설정합니다.

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>배포 버전을 WSL 1 또는 WSL 2로 설정

PowerShell 명령줄을 열고 `wsl -l -v` 명령을 입력([Windows 빌드 19041 이상에서만 사용 가능](ms-settings:windowsupdate))하면 설치한 각 Linux 배포에 할당된 WSL 버전을 확인할 수 있습니다.

```bash
wsl --list --verbose
```

두 버전의 WSL에 의해 지원되도록 배포를 설정하려면 다음을 실행합니다.

```bash
wsl --set-version <distribution name> <versionNumber>
```

`<distribution name>`을(를) 배포의 실제 이름으로, `<versionNumber>`을(를) 숫자 '1' 또는 '2'로 대체해야 합니다. 위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.

```bash
wsl --set-default-version 2
```

이렇게 하면 WSL 2에 설치된 모든 새 배포 버전이 설정됩니다.

## `wsl.exe`

Windows 버전 1903에서 `wsl.exe`를 사용하는 경우의 모든 옵션이 포함된 목록은 다음과 같습니다.

사용: `wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-commands"></a>Linux 명령을 실행하기 위한 인수

* **인수 없음**

  명령줄이 제공되지 않으면 wsl.exe에서 기본 셸을 시작합니다.

* **--exec, -e \<CommandLine>**
  
  기본 Linux 셸을 사용하지 않고 지정된 명령을 실행합니다.

* **--**
  
  나머지 명령줄을 있는 그대로 전달합니다.

또한 위의 명령에는 다음 옵션도 사용할 수 있습니다.

* **--distribution, -d \<Distro>**

  지정된 배포를 실행합니다.

* **--user, -u \<UserName>**

  지정된 사용자로 실행합니다.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템을 관리하기 위한 인수

* **--export \<Distro> \<FileName>**
  
  배포를 tar 파일로 내보냅니다. 파일 이름은 표준 출력을 위한 것입니다.

* **--import \<Distro> \<InstallLocation> \<FileName>**
  
  지정된 tar 파일을 새 배포로 가져옵니다. 파일 이름은 표준 입력을 위한 것입니다.

* **--list, -l [옵션]**
  
  배포를 나열합니다.

  옵션:
  * **--all**

    현재 설치 또는 제거 중인 배포를 포함하여 모든 배포를 나열합니다.

  * **--running**

    현재 실행 중인 배포만 나열합니다.

* **--set-default, -s \<Distro>**
  
  배포를 기본값으로 설정합니다.

* **--terminate, -t \<Distro>**
  
  지정된 배포를 종료합니다.

* **--unregister \<Distro>**
  
  배포 등록을 취소합니다.

* **--help** 사용법 정보를 표시합니다.

## <a name="additional-commands"></a>추가 명령

Linux용 Windows 하위 시스템과 상호 작용하는 기록 명령도 있습니다. 이러한 기능은 `wsl.exe`에 포함되어 있지만 여전히 사용할 수 있습니다.

### `wslconfig.exe`

다음 명령을 사용하여 WSL 배포를 구성할 수 있습니다. 해당 옵션의 목록은 다음과 같습니다.

사용: `wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>인수

* **/l, /list [옵션]**
  
  등록된 배포를 나열합니다.
  
옵션:

* **/all** 필요에 따라 현재 설치 또는 제거 중인 배포를 포함하여 모든 배포를 나열합니다.

* **/running** 현재 실행 중인 배포만 나열합니다.

* **/s, /setdefault \<Distro>** 배포를 기본값으로 설정합니다.

* **/t, /terminate \<Distro>** 배포를 종료합니다.

* **/u, /unregister \<Distro>** 배포 등록을 취소합니다.

* **/upgrade \<Distro>** 배포를 WslFs 파일 시스템 형식으로 업그레이드합니다.

### `bash.exe`

이 명령은 Bash 셸을 시작하는 데 사용됩니다. 이 명령에서 사용할 수 있는 옵션은 다음과 같습니다.

사용: `bash [Options...]`

* **지정된 옵션 없음**
  
  현재 디렉터리에서 Bash 셸을 시작합니다. Bash 셸이 설치되어 있지 않으면 `lxrun /install`이 자동으로 실행됩니다.

* **~**
  
  `bash ~`는 Bash 셸을 사용자의 홈 디렉터리에 시작합니다.  `cd ~`를 실행하는 것과 비슷합니다.

* **-c "\<command>"**
  
  명령을 실행하고, 출력한 다음, Windows 명령 프롬프트로 다시 종료합니다.

  예제: `bash -c "ls"`

## <a name="deprecated-commands"></a>사용되지 않는 명령

`lxrun.exe`는 Linux용 Windows 하위 시스템을 설치하고 관리하는 데 처음으로 사용된 명령이었습니다. Windows 10 1803 이상에서는 더 이상 사용되지 않습니다.

`lxrun.exe` 명령은 [WSL(Linux용 Windows 하위 시스템)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)과 직접 상호 작용하는 데 사용할 수 있습니다.  이러한 명령은 `\Windows\System32` 디렉터리에 설치되며 Windows 명령 프롬프트 내에서 또는 PowerShell에서 실행할 수 있습니다.

| 명령                     | 설명                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | lxrun 명령은 WSL 인스턴스를 관리하는 데 사용됩니다. |
| `lxrun /install`            | 다운로드 및 설치 프로세스를 시작합니다. <br/> 모든 프롬프트를 무시하려면 **/y**를 추가할 수 있습니다.  확인 메시지가 자동으로 수락되고 기본 사용자가 루트로 설정됩니다.          |
| `lxrun /uninstall`          | Ubuntu 이미지를 제거하고 삭제합니다.  이 명령은 기본적으로 사용자의 Ubuntu 홈 디렉터리를 제거하지 않습니다. <br/> 확인 메시지가 자동으로 수락되도록 하려면 **/y**를 추가할 수 있습니다. <br/>**/full**은 사용자의 Ubuntu 홈 디렉터리를 제거하고 삭제합니다.         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu 사용자에 대한 기본 Bash를 설정합니다. 지정된 사용자가 없는 경우 암호를 입력하라는 메시지가 표시됩니다.  자세한 내용은 https://aka.ms/wslusers를 참조하세요. <br/> **/y**는 암호를 입력하라는 메시지를 무시합니다.  사용자가 암호 없이 만들어집니다.|
| `lxrun /update`            | 하위 시스템의 패키지 인덱스를 업데이트합니다.          |
