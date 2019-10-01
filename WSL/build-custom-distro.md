---
title: WSL 용 사용자 지정 Linux 배포판 빌드
description: Linux 용 Windows 하위 시스템에 대 한 사용자 지정 Linux 배포를 만드는 방법에 대해 알아봅니다.
keywords: BashOnWindows, bash, wsl, windows, windows 하위 시스템, 배포판, 사용자 지정
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269701"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>WSL 용 사용자 지정 Linux 배포판 만들기

오픈 소스 WSL 샘플을 사용 하 여 Microsoft Store에 대 한 WSL 배포판 패키지를 작성 하거나 테스트용 로드에 대 한 사용자 지정 Linux 배포판 패키지를 만듭니다. GitHub에서 [배포판 시작 관리자 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) 를 찾을 수 있습니다.

이 프로젝트를 사용할 수 있습니다.
* WSL에서 실행 되는 appx로 Linux 배포를 패키지 하 고 제출 하는 linux 배포 유지 관리자
* 개발자는 자신의 개발 컴퓨터에 테스트용으로 로드 수 있는 사용자 지정 Linux 배포를 만들 수 있습니다.

## <a name="background"></a>배경
Microsoft Store를 통해 WSL 용 Linux 배포판을 UWP 응용 프로그램으로 배포 합니다. WSL에서 실행 되는 응용 프로그램을 설치할 수 있습니다-Windows 커널에 상주 하는 하위 시스템입니다. 이 전달 메커니즘에는 [이전 블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)에 설명 된 것 처럼 많은 이점이 있습니다.

## <a name="sideloading-a-custom-linux-distro-package"></a>사용자 지정 Linux 배포판 패키지를 테스트용 로드
사용자 지정 Linux 배포판 패키지를 개인용 컴퓨터의 테스트용으로 로드에 대 한 응용 프로그램으로 만들 수 있습니다. 배포 유지 관리자로 제출 하지 않으면 사용자 지정 패키지는 Microsoft Store를 통해 배포 되지 않습니다.
테스트용으로 로드 apps에 대 한 컴퓨터를 설정 하려면 "개발자 용"의 시스템 설정에서 사용 하도록 설정 해야 합니다.  개발자 모드 또는 테스트용으로 로드 apps가 선택 되어 있어야 합니다.

## <a name="for-linux-distro-maintainers"></a>Linux 배포판 유지 관리자
스토어에 제출 하려면 microsoft와 협력 하 여 게시 승인을 받아야 합니다. Microsoft Store에 배포를 추가 하는 데 관심이 있는 Linux 배포 소유자 인 경우에 게 문의 wslpartners@microsoft.com하세요.

## <a name="getting-started"></a>시작하기
[배포판 시작 관리자 GitHub 리포지토리의](https://github.com/Microsoft/WSL-DistroLauncher) 지침에 따라 사용자 지정 Linux 배포판 패키지를 만듭니다.

 
## <a name="team-blogs"></a>팀 블로그
*  [Linux 배포 유지 관리자 및 테스트용 로드 사용자 지정 Linux 배포에 대 한 WSL 샘플 열기](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>사용자 의견 제공
* [배포판 시작 관리자 GitHub 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher)
* [WSL 용 GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
