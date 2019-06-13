---
title: Linux 용 Windows 하위 시스템에 알아봅니다
description: Linux 용 Windows 하위 시스템의 작동 원리에 대해 알아봅니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040812"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Linux 설명서 용 Windows 하위 시스템

Linux 용 Windows 하위 시스템, 가상 컴퓨터의 오버 헤드 없이 수정 되지 않은 Windows에서 직접-대부분의 명령줄 도구, 유틸리티 및 응용 프로그램을 포함 하 여-GNU/Linux 환경을 실행 하는 개발자를 수 있습니다.  

다음 작업을 수행할 수 있습니다.

1. 즐겨 사용 GNU/Linux 배포를 선택 [Windows 스토어에서](https://aka.ms/wslstore)합니다.
1. 와 같은 일반적인 명령줄 사용 가능한 소프트웨어를 실행할 `grep`, `sed`, `awk`, 또는 다른 ELF-64 이진 파일. 
1. Bash 셸 스크립트 및 GNU/Linux 명령줄 응용 프로그램을 실행 합니다.  
    * 도구: vim, emacs, tmux
    * 언어들: Javascript/node.js, Ruby, Python, C /C++, C# & F#, Rust, Go 등입니다.
    * 서비스: sshd, MySQL, Apache, lighttpd
1. 자체 GNU/Linux 배포 패키지 관리자를 사용 하 여 추가 소프트웨어를 설치 합니다.
1. Unix 유사 명령줄 셸을 사용 하 여 Windows 응용 프로그램을 호출 합니다.
1. Windows에서 GNU/Linux 응용 프로그램을 호출 합니다.

## <a name="getting-started"></a>시작하기

* [Windows 10에서 Linux 설치](install-win10.md)
* [명령 참조를 참조 하세요.](reference.md)
* [읽기에 대 한 질문과 대답](faq.md)

## <a name="team-blogs"></a>팀 블로그
*  [개요 컬렉션 비디오 및 블로그 게시물](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/) (활성)
* [Linux 블로그에 대 한 Windows 하위 시스템](https://blogs.msdn.microsoft.com/wsl/) (기록)

## <a name="posts--articles"></a>게시물 및 문서
* [Windows의 Ubuntu에서 Bash 실행](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [개발자는 Windows 10의 Bash 및 Usermode Ubuntu Linux 이진 파일을 실행할 수 있습니다.](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Windows 개발자를 위한 Ubuntu Userspace – Windows에서 Ubuntu](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>사용자 의견 제공
* [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
