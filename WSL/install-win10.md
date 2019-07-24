---
title: Windows 10에 Linux 용 Windows 하위 시스템 (WSL) 설치
description: Windows 10에서 Linux 용 Windows 하위 시스템에 대 한 설치 지침을 참조 하세요.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499290"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 용 windows 하위 시스템 설치 가이드

## <a name="install-the-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템 설치

WSL 용 Linux 배포판을 설치 하기 전에 "Linux 용 Windows 하위 시스템" 옵션 기능이 사용 되도록 설정 되어 있는지 확인 해야 합니다.

1. 관리자 권한으로 PowerShell을 열고 다음을 실행 합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.

## <a name="install-your-linux-distribution-of-choice"></a>선택한 Linux 배포를 설치 합니다.
기본 배포판를 다운로드 하 고 설치 하려면 다음 세 가지 옵션을 선택할 수 있습니다.
1. Microsoft Store에서 다운로드 하 여 설치 합니다 (아래 참조).
1. 명령줄/스크립트에서 다운로드 및 설치 ([수동 설치 지침 참조](install-manual.md))
1. 다운로드 및 수동으로 압축 풀기 및 설치 (Windows Server에 대 한 [지침](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10의 작성자 업데이트 이상: Microsoft Store에서 설치

> 이 섹션은 Windows 빌드 16215 이상에 대 한 것입니다.  [빌드를 확인](troubleshooting.md#check-your-build-number)하려면 다음 단계를 수행 합니다. 

1. Microsoft Store를 열고 즐겨 사용 하는 Linux 배포를 선택 합니다.

    ![Microsoft Store의 Linux 배포판 보기](media/store.png)

    다음 링크는 각 배포에 대 한 Microsoft store 페이지를 엽니다.

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [WSL 용 Fedora Remix](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [알파인 WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. 배포판의 페이지에서 "가져오기"를 선택 합니다.

    ![Microsoft store의 Linux 배포판 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>배포판의 초기화를 완료 합니다.
이제 Linux 배포판가 설치 되었으므로 [새 배포판 인스턴스](initialize-distro.md) 를 사용 하려면 먼저 초기화 해야 합니다.

## <a name="troubleshooting"></a>문제 해결: 

관련 오류 및 권장 픽스는 다음과 같습니다. 다른 일반적인 오류 및 해결 방법에 대해서는 [Wsl 문제 해결 페이지](troubleshooting.md) 를 참조 하세요.

* **0x80070003 오류로 인해 설치 하지 못했습니다.**
    * Linux 용 Windows 하위 시스템은 시스템 드라이브 에서만 실행 됩니다 (일반적으로 `C:` 드라이브). 배포판가 시스템 드라이브에 저장 되어 있는지 확인 합니다.  
    * **설정** -> **저장소** 저장소 추가저장소->설정: ** 새 콘텐츠가 저장**
    된위치를변경하여C:드라이브에앱을설치하는시스템설정그림![](media/AppStorage.png)
    
    
 * **오류 0x8007019e를 사용 하 여 WslRegisterDistribution 실패**   
  * Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용할 수 없습니다. 
   * **제어판** -> **프로그램 및 기능** 을 엽니다.-> * * windows 기능 사용/사용 안 함 * *-> **Linux 용 windows 하위 시스템** 을 확인 하거나이 문서의 시작 부분에 설명 된 PowerShell cmdlet을 사용 합니다.
