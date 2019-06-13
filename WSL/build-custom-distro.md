---
title: WSL에 대 한 사용자 지정 Linux 배포판으로 빌드
description: Linux 용 Windows 하위 시스템에 대 한 사용자 지정 Linux 배포를 만드는 방법에 알아봅니다.
keywords: BashOnWindows, bash, wsl, windows, windows 하위 시스템, 배포, 사용자 지정
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040779"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>WSL에 대 한 사용자 지정 Linux 배포판으로 만들기

Microsoft Store 대 한 WSL 배포판의 패키지를 빌드 및/또는 테스트용 로드에 대 한 사용자 지정 Linux 배포판 패키지를 만들려면 오픈 소스 WSL 샘플을 사용 합니다. 찾을 수 있습니다 합니다 [배포판 launcher 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) github입니다.

이 프로젝트는 다음 작업을 사용 하도록 설정 합니다.
* 패키지 및 WSL에서 실행 되는 appx로 Linux 배포를 제출 하려면 Linux 배포 유지 관리자
* 개발자는 자신의 개발 컴퓨터에 테스트용으로 로드 될 수 있습니다. 있는 사용자 지정 Linux 배포를 만들 수

## <a name="background"></a>배경
Microsoft Store 통해 UWP 응용 프로그램으로 WSL에 대 한 Linux 배포판을 배포 했습니다. WSL-Windows 커널에 있는 하위 시스템에 실행 한 다음 해당 응용 프로그램을 설치할 수 있습니다. 이 배달 메커니즘에서 설명한 것 처럼 많은 이점이 있습니다는 [이전 블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)합니다.

## <a name="sideloading-a-custom-linux-distro-package"></a>사용자 지정 Linux 배포판의 패키지를 테스트용으로 로드
개인 컴퓨터에 테스트용으로 로드 하려면 응용 프로그램으로 사용자 지정 Linux 배포판 패키지를 만들 수 있습니다. 사용자 지정 패키지는 배포 되지 Microsoft Store 통해 배포 유지 관리자는으로 제출 하지 않는 한 note 하십시오.
앱 사이드 로드 하기 위해 컴퓨터를 설정 하려면 "For Developers" 시스템 설정에서이 기능을 사용 해야 합니다.  개발자 모드 또는 테스트용 로드 앱을 선택한 포함 해야 합니다.

## <a name="for-linux-distro-maintainers"></a>Linux 배포판 유지 관리자에 대 한
스토어에 제출 하려면 게시 승인을 사용 해야 합니다. Microsoft Store 배포 추가 원하는 Linux 배포 소유자 인 경우 문의 wslpartners@microsoft.com합니다.

## <a name="getting-started"></a>시작하기
지침에 따라 합니다 [배포판 Launcher GitHub 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) 사용자 지정 Linux 배포판 패키지를 만듭니다.

 
## <a name="team-blogs"></a>팀 블로그
*  [Linux 배포 유지 관리자 및 테스트용으로 로드할 사용자 지정 Linux 배포에 대 한 WSL 샘플 소싱 열기](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>사용자 의견 제공
* [배포판 Launcher GitHub 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher)
* [WSL에 대 한 GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
