---
title: Windows 10에 WSL(Linux용 Windows 하위 시스템) 설치
description: Windows 10에 Linux용 Windows 하위 시스템을 설치하는 방법을 알아봅니다. Windows 10을 버전 2004, 빌드 19041 이상으로 업데이트해야 합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 설치, 사용, WSL 2, 버전 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 50b434e288ba90173875cf5e7cd5fe9e6c3d8a16
ms.sourcegitcommit: 498592fa4b09015be3ee9a8913e5e3cf755de24b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559293"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10에 Linux용 Windows 하위 시스템 설치 가이드

## <a name="install-the-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 설치

Windows에서 Linux 배포를 실행하기 전에 "Linux용 Windows 하위 시스템" 옵션 기능을 사용해야 합니다.

PowerShell을 관리자 권한으로 열어 실행합니다.

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

WSL 1만 설치하려면 지금 머신을 다시 시작하여 [선택한 Linux 배포 설치](./install-win10.md#install-your-linux-distribution-of-choice)로 이동해야 합니다. 그렇지 않으면 다시 시작될 때까지 기다렸다가 WSL 2로 업데이트로 이동합니다. [WSL 2와 WSL 1비교](./compare-versions.md)에 대해 자세히 알아보세요.

## <a name="update-to-wsl-2"></a>WSL 2로 업데이트

WSL 2로 업데이트하려면 다음 조건을 충족해야 합니다.

- Windows 10 실행, x64 시스템의 경우 [버전 1903 이상](ms-settings:windowsupdate), **빌드 18362** 이상으로 업데이트.
   - Windows 10 버전 1903 또는 1909를 사용하는 경우 부 빌드 번호가 1049 이상인지 확인합니다. [여기에서 전체 문제 해결 지침](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2)을 참조하세요.
- Windows 10 실행, ARM64 시스템의 경우 버전 2004 이상, **빌드 19041**로 업데이트.
- Windows 10 버전 1903 또는 1909를 사용할 경우 적절한 백포트가 있는지 확인해야 합니다. 지침은 [여기에서 확인](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it)할 수 있습니다. 

- **Windows 로고 키 + R**을 선택하고 **winver**를 입력한 다음, **확인**을 선택하여 Windows 버전을 확인합니다. (또는 Windows 명령 프롬프트에서 `ver` 명령을 입력합니다.) 빌드가 18361보다 낮은 경우 [최신 Windows 버전으로 업데이트합니다](ms-settings:windowsupdate). [Windows 업데이트 도우미를 가져옵니다](https://www.microsoft.com/software-download/windows10).

### <a name="enable-the-virtual-machine-platform-optional-component"></a>'가상 머신 플랫폼' 옵션 구성 요소 사용

WSL 2를 설치하기 전에 "가상 머신 플랫폼" 옵션 기능을 사용하도록 설정해야 합니다.

PowerShell을 관리자 권한으로 열어 실행합니다.

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

머신을 **다시 시작하여** WSL 설치를 완료하고 WSL 2로 업데이트합니다.

### <a name="set-wsl-2-as-your-default-version"></a>WSL 2를 기본 버전으로 설정

PowerShell을 관리자 권한으로 열고 이 명령을 실행하여 새 Linux 배포를 설치할 때 WSL 2를 기본 버전으로 설정합니다.

```powershell
wsl --set-default-version 2
```

`WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel` 명령을 실행한 후 이 메시지가 표시될 수 있습니다. 링크([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel))를 따라 이동한 다음, 설명서의 해당 페이지에서 MSI를 설치하여 머신에 WSL 2에서 사용할 Linux 커널을 설치합니다. 커널을 설치한 후 명령을 다시 실행합니다. 그러면 메시지가 표시되지 않고 성공적으로 완료될 것입니다. 

> [!NOTE]
> WSL 1에서 WSL 2로 업데이트는 대상 배포 크기에 따라 완료하는 데 몇 분이 걸릴 수 있습니다. Windows 10 1주년 업데이트 또는 Creators Update에서 이전 버전(레거시)의 WSL 1을 실행하는 경우 업데이트 오류가 발생할 수 있습니다. 다음 지침에 따라 [레거시 배포판을 제거](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro)하세요. 
>
> `wsl --set-default-version` 결과가 잘못된 명령이면 `wsl --help`를 입력하세요. `--set-default-version`이 나열되지 않은 경우 OS에서 해당 기능을 지원하지 않으며 버전 1903, 빌드 18362 이상으로 업데이트해야 함을 의미합니다.

## <a name="install-your-linux-distribution-of-choice"></a>선택한 Linux 배포 설치

1. [Microsoft Store](https://aka.ms/wslstore)를 열고 즐겨 찾는 Linux 배포를 선택합니다.

    ![Microsoft Store의 Linux 배포 보기](media/store.png)

    각 배포에 대한 Microsoft Store 페이지를 여는 링크는 다음과 같습니다.

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. 배포 페이지에서 "가져오기"를 선택합니다.

    ![Microsoft Store의 Linux 배포](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a>새 배포 설정

새로 설치된 Linux 배포를 처음 시작하면 콘솔 창이 열리고 파일이 압축 해제되어 PC에 저장될 때까지 1~2분 정도 기다려야 합니다. 이후의 모든 시작은 1초도 걸리지 않습니다.

[새 Linux 배포에 대한 사용자 계정 및 암호를 만들어야](./user-support.md) 합니다.

![Windows 콘솔에서 Ubuntu 압축 풀기](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>배포 버전을 WSL 1 또는 WSL 2로 설정

PowerShell 명령줄을 열고 `wsl -l -v` 명령을 입력([Windows 빌드 18362 이상에서만 사용 가능](ms-settings:windowsupdate))하면 설치한 각 Linux 배포에 할당된 WSL 버전을 확인할 수 있습니다.

```powershell
wsl --list --verbose
```

두 버전의 WSL에 의해 지원되도록 배포를 설정하려면 다음을 실행합니다.

```powershell
wsl --set-version <distribution name> <versionNumber>
```

`<distribution name>`을(를) 배포의 실제 이름으로, `<versionNumber>`을(를) 숫자 '1' 또는 '2'로 대체해야 합니다. 위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.

```powershell
wsl --set-default-version 2
```

이렇게 하면 WSL 2에 설치된 모든 새 배포 버전이 설정됩니다.

## <a name="troubleshooting-installation"></a>설치 문제 해결

관련 오류 및 제안된 수정 사항은 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

- **0x80070003 오류로 인한 설치 실패**
  - Linux용 Windows 하위 시스템은 시스템 드라이브(일반적으로 `C:` 드라이브)에서만 실행됩니다. 배포가 시스템 드라이브에 저장되어 있는지 확인합니다.  
  - **설정** -> **스토리지** -> **더 많은 스토리지 설정을 차례로 엽니다. 새 콘텐츠가 저장된 위치를 변경합니다.** 
    ![C: 드라이브에 앱을 설치하기 위한 시스템 설정에 대한 그림](media/AppStorage.png)

- **0x8007019e 오류로 인한 WslRegisterDistribution 실패**
  - 선택적인 Linux용 Windows 하위 시스템 구성 요소가 실행되지 않습니다.
  - **제어판** -> **프로그램 및 기능** -> **Windows 기능 사용/사용 안 함**을 차례로 열어 **Linux용 Windows 하위 시스템**을 선택하거나 이 문서의 시작 부분에서 설명한 PowerShell cmdlet을 사용합니다.

- **0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**
  - 컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다. 이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.

- **업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Linux용 Windows 하위 시스템을 사용하도록 설정했고 Windows 빌드 버전 18362 이상을 사용하고 있는지 확인합니다. WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 PowerShell 프롬프트에서 이 명령을 실행합니다.

- **가상 디스크 시스템 제한으로 인해 요청한 작업을 완료할 수 없습니다. 가상 하드 디스크 파일은 압축이 풀려 있는 상태이고 암호화되지 않아야 하며 스파스가 아니어야 합니다.**
  - Linux 배포판의 프로필 폴더를 열어서 "내용 압축"과 "내용 암호화"를 선택 취소합니다. 이는 Windows 파일 시스템의 `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...` 같은 폴더에 있을 것입니다.
  - 이 Linux 배포판 프로필에는 LocalState 폴더가 있을 것입니다. 이 폴더를 마우스 오른쪽 단추로 클릭하여 옵션 메뉴를 표시합니다. 속성 > 고급을 선택하고 "내용을 압축하여 디스크 공간 절약" 및 "데이터 보호를 위해 내용을 암호화" 확인란이 선택 취소되어 있는지 확인합니다(선택하지 않음). 이를 현재 폴더 또는 모든 하위 폴더와 파일에만 적용할지 묻는 메시지가 표시되면 압축 플래그만 지우도록 "이 폴더만"을 선택합니다. 그러면 `wsl --set-version` 명령이 작동할 것입니다.

![WSL 배포판 속성 설정의 스크린샷](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> 이 예에서는 Ubuntu 18.04 배포판의 LocalState 폴더가 C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc에 있습니다.
>
> 이 문제에 대한 업데이트된 정보를 추적할 수 있는 [WSL Docs GitHub 스레드 #4103](https://github.com/microsoft/WSL/issues/4103)을 확인하세요.

- **cmdlet, 함수, 스크립트 파일 또는 실행 프로그램의 이름에는 'wsl'이라는 단어가 들어갈 수 없습니다.**
  - [Linux용 Windows 하위 시스템 옵션 구성 요소가 설치되었는지](./install-win10.md#enable-the-virtual-machine-platform-optional-component) 확인하세요. 또는 ARM64 디바이스를 사용 중이고 PowerShell에서 이 명령을 실행하는 경우 이 오류가 표시됩니다. [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) 또는 명령 프롬프트에서 `wsl.exe`를 대신 실행하세요.
