---
title: Windows 10에 WSL(Linux용 Windows 하위 시스템) 설치
description: Linux용 Windows 하위 시스템을 Windows 10에 설치하는 방법에 대한 지침입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 설치
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200238"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10에 Linux용 Windows 하위 시스템 설치 가이드

## <a name="install-the-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 설치

WSL용 Linux 배포판을 설치하려면 먼저 선택적인 "Linux용 Windows 하위 시스템" 기능을 사용하도록 설정해야 합니다.

1. PowerShell을 관리자 권한으로 열어 실행합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시되면 컴퓨터를 다시 시작합니다.

## <a name="install-your-linux-distribution-of-choice"></a>선택한 Linux 배포 설치
기본 설정 배포판을 다운로드하여 설치하려면 다음 세 가지 옵션 중에서 선택할 수 있습니다.
* Microsoft Store에서 다운로드 및 설치(아래 참조)
* 명령줄/스크립트에서 다운로드 및 설치([수동 설치 지침 참조](install-manual.md))
* 다운로드 및 수동으로 압축을 푼 후 설치(Windows Server의 경우 - [지침](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 이상: Microsoft Store에서 설치

> 이 섹션은 Windows 빌드 16215 이상에 적용됩니다.  다음 단계에 따라 [빌드를 확인](troubleshooting.md#check-your-build-number)하세요. 

1. Microsoft Store를 열고 즐겨찾는 Linux 배포를 선택합니다.

    ![Microsoft Store에서 Linux 배포판 보기](media/store.png)

    각 배포에 대한 Microsoft Store 페이지를 여는 링크는 다음과 같습니다.

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. 배포판의 페이지에서 "가져오기"를 선택합니다.

    ![Microsoft Store에서 Linux 배포판 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>배포판의 초기화 완료
이제 Linux 배포판이 설치되었으므로 새 배포판 인스턴스를 사용하려면 먼저 [초기화](initialize-distro.md)해야 합니다.

## <a name="troubleshooting"></a>문제 해결: 

관련 오류 및 제안된 수정 사항은 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

* **0x80070003 오류로 인한 설치 실패**
    * Linux용 Windows 하위 시스템은 시스템 드라이브(일반적으로 `C:` 드라이브)에서만 실행됩니다. 배포판이 시스템 드라이브에 저장되어 있는지 확인합니다.  
    * **설정** -> **스토리지** -> **더 많은 스토리지 설정을 차례로 엽니다. 새 콘텐츠가 저장된 위치를 변경합니다.** 
    ![C: 드라이브에 앱을 설치하기 위한 시스템 설정에 대한 그림](media/AppStorage.png)
    
    
 * **0x8007019e 오류로 인한 WslRegisterDistribution 실패**   
  * 선택적인 Linux용 Windows 하위 시스템 구성 요소가 실행되지 않습니다. 
   * **제어판** -> **프로그램 및 기능** -> **Windows 기능 사용/사용 안 함**을 차례로 열어 **Linux용 Windows 하위 시스템**을 선택하거나 이 문서의 시작 부분에서 설명한 PowerShell cmdlet을 사용합니다.
