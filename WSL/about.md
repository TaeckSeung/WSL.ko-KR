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
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="308a0-104">Linux 설명서 용 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="308a0-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="308a0-105">Linux 용 Windows 하위 시스템, 가상 컴퓨터의 오버 헤드 없이 수정 되지 않은 Windows에서 직접-대부분의 명령줄 도구, 유틸리티 및 응용 프로그램을 포함 하 여-GNU/Linux 환경을 실행 하는 개발자를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="308a0-106">다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-106">You can:</span></span>

1. <span data-ttu-id="308a0-107">즐겨 사용 GNU/Linux 배포를 선택 [Windows 스토어에서](https://aka.ms/wslstore)합니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="308a0-108">와 같은 일반적인 명령줄 사용 가능한 소프트웨어를 실행할 `grep`, `sed`, `awk`, 또는 다른 ELF-64 이진 파일.</span><span class="sxs-lookup"><span data-stu-id="308a0-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="308a0-109">Bash 셸 스크립트 및 GNU/Linux 명령줄 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="308a0-110">도구: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="308a0-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="308a0-111">언어들: Javascript/node.js, Ruby, Python, C /C++, C# & F#, Rust, Go 등입니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="308a0-112">서비스: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="308a0-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="308a0-113">자체 GNU/Linux 배포 패키지 관리자를 사용 하 여 추가 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="308a0-114">Unix 유사 명령줄 셸을 사용 하 여 Windows 응용 프로그램을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="308a0-115">Windows에서 GNU/Linux 응용 프로그램을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="308a0-116">시작하기</span><span class="sxs-lookup"><span data-stu-id="308a0-116">Getting Started</span></span>

* [<span data-ttu-id="308a0-117">Windows 10에서 Linux 설치</span><span class="sxs-lookup"><span data-stu-id="308a0-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="308a0-118">명령 참조를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="308a0-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="308a0-119">읽기에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="308a0-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="308a0-120">팀 블로그</span><span class="sxs-lookup"><span data-stu-id="308a0-120">Team Blogs</span></span>
*  [<span data-ttu-id="308a0-121">개요 컬렉션 비디오 및 블로그 게시물</span><span class="sxs-lookup"><span data-stu-id="308a0-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="308a0-122">[명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/) (활성)</span><span class="sxs-lookup"><span data-stu-id="308a0-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="308a0-123">[Linux 블로그에 대 한 Windows 하위 시스템](https://blogs.msdn.microsoft.com/wsl/) (기록)</span><span class="sxs-lookup"><span data-stu-id="308a0-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="308a0-124">게시물 및 문서</span><span class="sxs-lookup"><span data-stu-id="308a0-124">Posts & Articles</span></span>
* [<span data-ttu-id="308a0-125">Windows의 Ubuntu에서 Bash 실행</span><span class="sxs-lookup"><span data-stu-id="308a0-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="308a0-126">개발자는 Windows 10의 Bash 및 Usermode Ubuntu Linux 이진 파일을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308a0-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="308a0-127">Windows 개발자를 위한 Ubuntu Userspace – Windows에서 Ubuntu</span><span class="sxs-lookup"><span data-stu-id="308a0-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="308a0-128">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="308a0-128">Provide Feedback</span></span>
* [<span data-ttu-id="308a0-129">GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="308a0-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="308a0-130">명령줄 UserVoice 포털</span><span class="sxs-lookup"><span data-stu-id="308a0-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
