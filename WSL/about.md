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
ms.localizationpriority: High
ms.openlocfilehash: edff78b1447aa382253417d27df52fe497c58b08
ms.sourcegitcommit: e17038c166b69f73e593ae3ac351c9d66e2ba64b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67694623"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="0f3cf-104">Linux 용 Windows 하위 시스템 설명서</span><span class="sxs-lookup"><span data-stu-id="0f3cf-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="0f3cf-105">Linux 용 Windows 하위 시스템을 통해 개발자는 가상 컴퓨터의 오버 헤드 없이 대부분의 명령줄 도구, 유틸리티 및 응용 프로그램을 포함 하 여 Windows에서 직접 수정 되지 않은 GNU/Linux 환경을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="0f3cf-106">다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-106">You can:</span></span>

1. <span data-ttu-id="0f3cf-107">[Microsoft Store에서](https://aka.ms/wslstore)선호 하는 GNU/Linux 배포판을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="0f3cf-108">,, 또는 다른 ELF-64 이진 파일과 같은 `sed` 일반적인명령줄무료소프트웨어를실행합니다.`awk` `grep`</span><span class="sxs-lookup"><span data-stu-id="0f3cf-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="0f3cf-109">다음을 포함 하 여 Bash 셸 스크립트 및 GNU/Linux 명령줄 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="0f3cf-110">도구: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="0f3cf-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="0f3cf-111">언어들: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go 등</span><span class="sxs-lookup"><span data-stu-id="0f3cf-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="0f3cf-112">서비스: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="0f3cf-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="0f3cf-113">자체 GNU/Linux 배포 패키지 관리자를 사용 하 여 추가 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="0f3cf-114">Unix와 비슷한 명령줄 셸을 사용 하 여 Windows 응용 프로그램을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="0f3cf-115">Windows에서 GNU/Linux 응용 프로그램을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="0f3cf-116">시작하기</span><span class="sxs-lookup"><span data-stu-id="0f3cf-116">Getting Started</span></span>

* [<span data-ttu-id="0f3cf-117">Windows 10에 Linux 설치</span><span class="sxs-lookup"><span data-stu-id="0f3cf-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="0f3cf-118">명령 참조를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="0f3cf-119">질문과 대답 읽기</span><span class="sxs-lookup"><span data-stu-id="0f3cf-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="0f3cf-120">팀 블로그</span><span class="sxs-lookup"><span data-stu-id="0f3cf-120">Team Blogs</span></span>
*  [<span data-ttu-id="0f3cf-121">비디오 및 블로그의 컬렉션과 함께 게시</span><span class="sxs-lookup"><span data-stu-id="0f3cf-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="0f3cf-122">[명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/) Directory</span><span class="sxs-lookup"><span data-stu-id="0f3cf-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="0f3cf-123">[Linux 블로그의 Windows 하위 시스템](https://blogs.msdn.microsoft.com/wsl/) 이력</span><span class="sxs-lookup"><span data-stu-id="0f3cf-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="0f3cf-124">& 문서 게시</span><span class="sxs-lookup"><span data-stu-id="0f3cf-124">Posts & Articles</span></span>
* [<span data-ttu-id="0f3cf-125">Windows의 Ubuntu에서 Bash 실행</span><span class="sxs-lookup"><span data-stu-id="0f3cf-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="0f3cf-126">개발자는 Windows 10에서 Bash 및 Usermode Ubuntu Linux 이진 파일을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3cf-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="0f3cf-127">Windows의 ubuntu – Windows 개발자를 위한 Ubuntu Userspace</span><span class="sxs-lookup"><span data-stu-id="0f3cf-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="0f3cf-128">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="0f3cf-128">Provide Feedback</span></span>
* [<span data-ttu-id="0f3cf-129">GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="0f3cf-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="0f3cf-130">명령줄 UserVoice 포털</span><span class="sxs-lookup"><span data-stu-id="0f3cf-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
