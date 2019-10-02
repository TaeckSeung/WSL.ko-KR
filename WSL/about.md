---
title: Linux용 Windows 하위 시스템 알아보기
description: Linux용 Windows 하위 시스템이 작동하는 방법에 대해 자세히 알아봅니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, GNU, Linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 4e63fd186f11545937a4ce0a0fbd6071a4bf268d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269725"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Linux용 Windows 하위 시스템 설명서

Linux용 Windows 하위 시스템을 사용하면 개발자가 가상 머신의 오버헤드 없이 대부분의 명령줄 도구, 유틸리티 및 애플리케이션이 포함된 수정되지 않은 GNU/Linux 환경을 Windows에서 직접 실행할 수 있습니다.  

다음을 수행할 수 있습니다.

1. [Microsoft Store](https://aka.ms/wslstore)에서 즐겨찾는 GNU/Linux 배포를 선택합니다.
1. `grep`, `sed`, `awk` 또는 다른 ELF-64 이진 파일과 같은 일반적인 무료 명령줄 소프트웨어를 실행합니다. 
1. 다음을 포함하여 Bash 셸 스크립트 및 GNU/Linux 명령줄 애플리케이션을 실행합니다.  
    * 도구: vim, emacs, tmux
    * 언어: Javascript/node.js, Ruby, Python, C/C++, C# 및 F#, Rust, Go 등
    * 서비스: sshd, MySQL, Apache, lighttpd
1. 자체 GNU/Linux 배포 패키지 관리자를 사용하여 추가 소프트웨어를 설치합니다.
1. Unix와 같은 명령줄 셸을 사용하여 Windows 애플리케이션을 호출합니다.
1. Windows에서 GNU/Linux 애플리케이션을 호출합니다.

## <a name="getting-started"></a>시작

* [Windows 10에 Linux 설치](install-win10.md)
* [명령 참조 살펴보기](reference.md)
* [질문과 대답 참조](faq.md)

## <a name="team-blogs"></a>팀 블로그
*  [비디오 및 블로그 모음이 포함된 게시물에 대한 개요](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/)(활성)
* [Linux용 Windows 하위 시스템 블로그](https://blogs.msdn.microsoft.com/wsl/)(기록)

## <a name="posts--articles"></a>게시물 및 문서
* [Windows에서 Ubuntu 기반 Bash 실행](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [개발자가 Windows 10에서 Bash 및 사용자 모드 Ubuntu Linux 이진 파일을 실행할 수 있음](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Windows의 Ubuntu – Windows 개발자를 위한 Ubuntu 사용자 공간](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>사용자 의견 제공
* [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
