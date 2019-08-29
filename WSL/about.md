---
title: Linux 용 Windows 하위 시스템에 대 한 자세한 정보
description: Linux 용 Windows 하위 시스템이 작동 하는 방식에 대해 자세히 알아보세요.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122675"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Linux 용 Windows 하위 시스템 설명서

Linux 용 Windows 하위 시스템을 통해 개발자는 가상 컴퓨터의 오버 헤드 없이 대부분의 명령줄 도구, 유틸리티 및 응용 프로그램을 포함 하 여 Windows에서 직접 수정 되지 않은 GNU/Linux 환경을 실행할 수 있습니다.  

다음을 할 수 있습니다.

1. [Microsoft Store에서](https://aka.ms/wslstore)선호 하는 GNU/Linux 배포판을 선택 합니다.
1. ,, 또는 다른 ELF-64 이진 파일과 같은 `sed` 일반적인명령줄무료소프트웨어를실행합니다.`awk` `grep` 
1. 다음을 포함 하 여 Bash 셸 스크립트 및 GNU/Linux 명령줄 응용 프로그램을 실행 합니다.  
    * 도구: vim, emacs, tmux
    * 언어들: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go 등
    * 서비스: sshd, MySQL, Apache, lighttpd
1. 자체 GNU/Linux 배포 패키지 관리자를 사용 하 여 추가 소프트웨어를 설치 합니다.
1. Unix와 비슷한 명령줄 셸을 사용 하 여 Windows 응용 프로그램을 호출 합니다.
1. Windows에서 GNU/Linux 응용 프로그램을 호출 합니다.

## <a name="getting-started"></a>시작하기

* [Windows 10에 Linux 설치](install-win10.md)
* [명령 참조를 참조 하세요.](reference.md)
* [질문과 대답 읽기](faq.md)

## <a name="team-blogs"></a>팀 블로그
*  [비디오 및 블로그의 컬렉션과 함께 게시](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/) Directory
* [Linux 블로그의 Windows 하위 시스템](https://blogs.msdn.microsoft.com/wsl/) 이력

## <a name="posts--articles"></a>& 문서 게시
* [Windows의 Ubuntu에서 Bash 실행](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [개발자는 Windows 10에서 Bash 및 Usermode Ubuntu Linux 이진 파일을 실행할 수 있습니다.](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Windows의 ubuntu – Windows 개발자를 위한 Ubuntu Userspace](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>사용자 의견 제공
* [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
