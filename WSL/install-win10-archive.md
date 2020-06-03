---
title: Windows 10에 WSL(Linux용 Windows 하위 시스템) 설치
description: Linux용 Windows 하위 시스템을 Windows 10에 설치하는 방법에 대한 지침입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 설치
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301204"
---
# <a name="install-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 설치

다음 가이드는 Windows 10을 실행하는 컴퓨터에 WSL(Linux용 Windows 하위 시스템)을 설치하는 데 필요한 단계를 안내합니다.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Linux용 Windows 하위 시스템 옵션 기능 사용

Linux 배포를 실행하기 전에 Windows 10의 "Linux용 Windows 하위 시스템" 옵션 기능을 사용해야 합니다.

1. PowerShell을 관리자 권한으로 열고 이 스크립트를 엽니다.

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. 메시지가 표시되면 컴퓨터를 다시 시작합니다.

## <a name="install-a-linux-distribution"></a>Linux 배포 설치

기본 Linux 배포를 다운로드하고 설치하는 방법에는 세 가지가 있습니다.

- Microsoft Store에서 다운로드 및 설치(아래 참조)
- [명령줄에서 다운로드하여 수동으로 설치](install-manual.md)
- [Windows Server에 설치](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>Microsoft Store에서 설치

Linux 배포는 Windows 10의 Microsoft Store(빌드 16215 +)에서 설치할 수 있습니다.

> [!NOTE]
> 이 단계를 따라 [Windows 10 빌드 번호를 확인](troubleshooting.md#check-your-build-number)하세요.

1. Microsoft Store를 열고 즐겨찾는 Linux 배포를 선택합니다.

    ![Microsoft Store에서 Linux 배포판 보기](media/store.png)

    각 배포에 대한 Microsoft Store 페이지를 여는 링크는 다음과 같습니다.

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. "가져오기"를 선택하고 배포 다운로드가 완료되면 "시작"을 선택합니다.

    ![Microsoft Store에서 Linux 배포판 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>배포판의 초기화 완료

Linux 배포를 시작한 후 화면 지침에 따라 배포판을 초기화합니다.

> [!NOTE]
> Windows Server의 경우 설치 폴더에서 실행 파일 `<distro>.exe`를 사용하여 배포를 시작합니다.

새로 설치한 배포가 처음 실행되면 콘솔 창이 열리고, 설치가 완료될 때까지 1~2분 정도 기다리라는 메시지가 표시됩니다. 이 설치의 마지막 단계에서 배포판의 파일이 압축 해제되고 PC에 저장되어 사용할 준비가 됩니다. 이 경우 PC의 스토리지 디바이스 성능에 따라 약 1분 이상이 걸릴 수 있습니다. 이 초기 설치 단계는 배포판을 새로 설치하는 경우에만 필요하며, 이후의 모든 시작에는 1초 미만이 걸립니다.

## <a name="set-up-a-new-linux-user-account"></a>새 Linux 사용자 계정 설정

설치가 완료되면 새 사용자 계정(및 해당 암호)을 만들라는 메시지가 표시됩니다.

![Windows 콘솔에서 Ubuntu 압축 풀기](media/UbuntuInstall.png)

이 사용자 계정은 배포를 시작할 때 기본적으로 로그인되는 관리자가 아닌 일반 사용자를 위한 것입니다. 원하는 사용자 이름과 암호를 선택할 수 있으며, Windows 사용자 이름과는 관련이 없습니다.

새 배포판 인스턴스를 열면 암호를 입력하라는 메시지가 표시되지 않지만, **`sudo`를 사용하여 프로세스를 관리자 권한으로 실행하는 경우** 암호를 입력해야 하므로 쉽게 기억할 수 있는 암호를 선택해야 합니다! 자세한 내용은 [사용자 지원](user-support.md) 페이지를 참조하세요.

## <a name="update--upgrade-packages"></a>패키지 업데이트 및 업그레이드

대부분의 배포는 비어 있거나 최소한의 패키지 카탈로그와 함께 제공됩니다. 배포판의 기본 설정 패키지 관리자를 사용하여 정기적으로 패키지 카탈로그를 업데이트하고 설치된 패키지를 업그레이드하는 것이 좋습니다. Debian/Ubuntu의 경우 apt를 사용합니다.

```bash
sudo apt update && sudo apt upgrade
```

Windows에서는 Linux 배포판을 자동으로 업데이트하거나 업그레이드하지 않습니다. 이는 대부분의 Linux 사용자가 직접 제어하는 것을 선호하는 작업입니다.

WSL에서 새 Linux 배포판을 사용해 보세요!

## <a name="troubleshooting"></a>문제 해결

관련 설치 오류 및 제안된 수정 사항은 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

### <a name="installation-failed-with-error-0x8007007e"></a>0x8007007e 오류로 인한 설치 실패

이 오류는 시스템이 스토어의 Linux를 지원하지 않을 때 발생합니다.  다음 사항을 확인하세요.

- Windows 빌드 16215 이상을 실행하고 있습니다. [빌드를 확인](troubleshooting.md#check-your-build-number)하세요.
- Linux용 Windows 하위 시스템의 선택적 구성 요소가 사용하도록 설정되어 있고 컴퓨터가 다시 시작되었습니다.  [WSL이 사용하도록 설정되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)하세요.

### <a name="installation-failed-with-error-0x80070003"></a>0x80070003 오류로 인한 설치 실패

Linux용 Windows 하위 시스템은 시스템 드라이브(일반적으로 `C:` 드라이브)에서만 실행됩니다. 배포판이 시스템 드라이브에 저장되어 있는지 확인합니다.

- **설정** -> **스토리지** -> **더 많은 스토리지 설정을 차례로 엽니다. 새 콘텐츠가 저장되는 위치 변경**
  
    ![C: 드라이브에 앱을 설치하기 위한 시스템 설정에 대한 그림](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>0x8007019e 오류로 인한 WslRegisterDistribution 실패

선택적인 Linux용 Windows 하위 시스템 구성 요소가 실행되지 않습니다.

- **제어판** -> **프로그램 및 기능** -> **Windows 기능 사용/사용 안 함**을 차례로 열어 **Linux용 Windows 하위 시스템**을 선택하거나 이 문서의 시작 부분에서 설명한 PowerShell cmdlet을 사용합니다.
