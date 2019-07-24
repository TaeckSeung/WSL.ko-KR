---
title: FAQ(질문과 대답)
description: Linux 용 Windows 하위 시스템에 대 한 질문과 대답입니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237390"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="d71a8-104">Linux 용 Windows 하위 시스템에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="d71a8-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="d71a8-105">WSL (Linux 용 Windows 하위 시스템) 이란?</span><span class="sxs-lookup"><span data-stu-id="d71a8-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="d71a8-106">WSL (Linux 용 Windows 하위 시스템)은 기존 Windows 데스크톱 및 최신 스토어 앱과 함께 Windows에서 직접 기본 Linux 명령줄 도구를 실행할 수 있도록 하는 새로운 Windows 10 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="d71a8-107">자세한 내용은 [정보 페이지](./about.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d71a8-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="d71a8-108">WSL은 누구 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-108">Who is WSL for?</span></span>
<span data-ttu-id="d71a8-109">주로 개발자를 위한 도구입니다. 특히 웹 개발자와 오픈 소스 프로젝트에서 작업 하는 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="d71a8-110">이를 통해 Bash, 일반적인 linux 도구 (`sed`, `awk`등) 및 많은 Linux 중심 도구 (Ruby, Python 등)를 사용 해야 하는 사용자와 Windows에서 도구 체인를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="d71a8-111">WSL로 무엇을 할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-111">What can I do with WSL?</span></span>
<span data-ttu-id="d71a8-112">WSL은 bash 라는 응용 프로그램을 제공 합니다 .이 응용 프로그램은 시작 될 때 Bash 셸을 실행 하는 Windows 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="d71a8-113">Bash를 사용 하 여 명령줄 Linux 도구 및 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="d71a8-114">예를 들어를 `lsb_release -a` 입력 하 고 enter 키를 누르면 현재 실행 중인 Linux 배포판의 세부 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![배포판 세부 정보 스크린샷](media/distro.png)

<span data-ttu-id="d71a8-116">Linux Bash 셸 내에서 로컬 컴퓨터의 파일 시스템에 액세스할 수도 있습니다. 그러면 해당 폴더에 탑재 된 `/mnt` 로컬 드라이브를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="d71a8-117">예를 `C:` 들어 드라이브가 `/mnt/c`탑재 된 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![탑재 된 C 드라이브의 스크린샷](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="d71a8-119">Bash 란?</span><span class="sxs-lookup"><span data-stu-id="d71a8-119">What is Bash?</span></span>
<span data-ttu-id="d71a8-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 는 널리 사용 되는 텍스트 기반 셸 및 명령 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="d71a8-121">Ubuntu 및 기타 Linux 배포판 및 macOS 내에 포함 된 기본 셸입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="d71a8-122">사용자는 셸에서 명령을 입력 하 여 스크립트를 실행 하거나 명령 및 도구를 실행 하 여 많은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="d71a8-123">어떻게 작동합니까?</span><span class="sxs-lookup"><span data-stu-id="d71a8-123">How does this work?</span></span>
<span data-ttu-id="d71a8-124">기본 기술에 대해 자세히 설명 하는 [블로그](https://blogs.msdn.microsoft.com/wsl/) 를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="d71a8-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="d71a8-125">VM에서 Linux가 아닌 WSL을 사용 하는 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="d71a8-126">WSL은 전체 가상 컴퓨터 보다 많은 리소스 (CPU, 메모리 및 저장소)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="d71a8-127">또한 WSL에서는 Windows 명령줄, 데스크톱 및 스토어 앱과 함께 Linux 명령줄 도구 및 앱을 실행 하 고 Linux 내에서 Windows 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="d71a8-128">이렇게 하면 원하는 경우 동일한 파일 집합에서 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="d71a8-129">예를 들어 Windows 대신 Linux에서 Ruby를 사용 하는 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="d71a8-130">일부 플랫폼 간 도구는 이러한 도구가 실행 되는 환경이 Linux와 같이 동작 한다고 가정 하 여 구축 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="d71a8-131">예를 들어, 일부 도구는 매우 긴 파일 경로에 액세스할 수 있거나 특정 파일/폴더가 존재 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="d71a8-132">이 경우 종종 Linux와 다르게 동작 하는 Windows에서 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="d71a8-133">Ruby 및 노드와 같은 많은 언어는 Windows에서 자주 이식 되 고 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="d71a8-134">그러나 일부 Ruby 보석 또는 node/NPM library 소유자는 Windows를 지원 하기 위해 라이브러리를 이식 하는 것이 아니라 많은 Linux 관련 종속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="d71a8-135">이러한 도구 및 라이브러리를 사용 하 여 빌드한 시스템이 빌드 및 경우에 따라 Windows의 런타임 오류나 원치 않는 동작에서 발생 하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="d71a8-136">이러한 문제 중 일부는 Windows의 명령줄 도구를 개선 하기 위해 Microsoft에 문의 하 고, 기본 Bash 및 Linux 명령줄 도구를 Windows에서 실행할 수 있도록 하기 위해 정식 파트너와 협력 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="d71a8-137">PowerShell의 의미는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="d71a8-138">OSS 프로젝트를 사용 하는 동안 PowerShell 프롬프트에서 Bash로 끌어 놓는 데 매우 유용한 여러 가지 시나리오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="d71a8-139">Bash 지원은 Windows에서 명령줄의 값을 보완 하며 PowerShell 및 PowerShell 커뮤니티에서 다른 인기 기술을 활용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="d71a8-140">PowerShell 팀 블로그- [Windows 용 Bash에서 자세히 알아보세요. 훌륭한 기능 및 PowerShell에 대 한 의미](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="d71a8-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="d71a8-141">WSL에서 모든 Linux 앱을 실행할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="d71a8-142">아니요!</span><span class="sxs-lookup"><span data-stu-id="d71a8-142">No!</span></span> <span data-ttu-id="d71a8-143">WSL은 Windows에서 Bash 및 핵심 Linux 명령줄 도구를 실행 하는 데 필요한 사용자를 사용 하도록 설정 하기 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="d71a8-144">WSL은 GUI 데스크톱 또는 응용 프로그램 (예: Gnome, KDE 등)을 지원 **하지** 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="d71a8-145">또한 널리 사용 되는 여러 서버 응용 프로그램 (예: Redis)을 실행할 수 있는 경우에도 프로덕션 서비스를 호스팅하기 위해 WSL을 사용 하지 않는 것이 좋습니다. Microsoft는 Azure, Hyper-v 및 Docker에서 프로덕션 Linux 워크 로드를 실행 하기 위한 다양 한 솔루션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="d71a8-146">WSL이 포함 된 Windows Sku는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="d71a8-147">Windows 용 windows 하위 시스템은 windows 10 기념일 및 크리에이터 업데이트 이상용 Windows 데스크톱 버전에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="d71a8-148">이 하 버전에서 시작 하 여 Windows의 데스크톱 및 서버 Sku에서 업데이트 WSL을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="d71a8-149">WSL에서 지 원하는 프로세서는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-149">What processors does WSL support?</span></span>
<span data-ttu-id="d71a8-150">WSL은 x64 및 ARM Cpu를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="d71a8-151">C: 드라이브에 액세스 어떻게 할까요??</span><span class="sxs-lookup"><span data-stu-id="d71a8-151">How do I access my C: drive?</span></span>
<span data-ttu-id="d71a8-152">로컬 컴퓨터의 하드 드라이브에 대 한 탑재 지점이 자동으로 만들어지고 Windows 파일 시스템에 쉽게 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="d71a8-153">**/mnt/\<드라이브 문자 >/**</span><span class="sxs-lookup"><span data-stu-id="d71a8-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="d71a8-154">예제 사용법은 c:\ `cd /mnt/c` 에 액세스 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-154">Example usage would be `cd /mnt/c` to access c:\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="d71a8-155">Linux 앱과 함께 Windows 파일을 사용 어떻게 할까요??</span><span class="sxs-lookup"><span data-stu-id="d71a8-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="d71a8-156">WSL의 이점 중 하나는 Windows 및 Linux 앱 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="d71a8-157">Wsl은 Linux 배포판의 `/mnt/<drive>` 폴더에 컴퓨터의 고정 드라이브를 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="d71a8-158">예를 `C:` 들어 드라이브가`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="d71a8-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="d71a8-159">탑재 된 드라이브를 사용 하 `C:\dev\myproj\` 여 [Visual Studio](https://visualstudio.microsoft.com/vs/) /또는 [VS Code](https://code.visualstudio.com/)를 사용 하는 등의 코드를 편집 하 고를 통해 `/mnt/c/dev/myproj`동일한 파일에 액세스 하 여 Linux에서 해당 코드를 빌드/테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="d71a8-160">**중요 정보**: WSL을 사용 하는 경우의 주요 제한 사항 중 하나는 Windows 앱 또는 도구를 사용 하 여 Linux 배포판의 파일 시스템에서 직접 액세스/변경 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="d71a8-161">참조 [Windows 앱 및 도구를 사용 하 여 Linux 파일 변경 안 함](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="d71a8-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="d71a8-162">Linux 드라이브의 파일이 탑재 된 Windows 드라이브와 다른 가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="d71a8-163">Linux 루트 (예 `/`:)에 있는 파일은 다음을 비롯 하 여 linux 특정 동작을 모방 하는 wsl에 의해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="d71a8-164">잘못 된 Windows 파일 이름 문자를 포함 하는 파일</span><span class="sxs-lookup"><span data-stu-id="d71a8-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="d71a8-165">관리자가 아닌 사용자에 대해 생성 되는 symlink</span><span class="sxs-lookup"><span data-stu-id="d71a8-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="d71a8-166">Chmod 및 chown를 통해 파일 특성 변경</span><span class="sxs-lookup"><span data-stu-id="d71a8-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="d71a8-167">파일/폴더 대/소문자 구분</span><span class="sxs-lookup"><span data-stu-id="d71a8-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="d71a8-168">탑재 된 드라이브의 파일은 Windows에 의해 제어 되며 다음과 같은 동작을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="d71a8-169">대/소문자 구분 지원</span><span class="sxs-lookup"><span data-stu-id="d71a8-169">Support case sensitivity</span></span>
   * <span data-ttu-id="d71a8-170">모든 사용 권한은 Windows 사용 권한을 가장 잘 반영 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="d71a8-171">Apt를 실행할 때 많은 오류가 발생 하는 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="d71a8-172">일부 패키지는 아직 구현 하지 않은 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="d71a8-173">`udev`예를 들어,는 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="d71a8-174">와 관련 된 `udev`문제를 해결 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="d71a8-175">에 다음을 `/usr/sbin/policy-rc.d` 작성 하 고 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="d71a8-176">실행 권한 추가`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="d71a8-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="d71a8-177">다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="d71a8-178">WSL 배포를 제거할 어떻게 할까요? 있나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="d71a8-179">1709 이전의 빌드 (16299)에서 명령 프롬프트를 열고 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="d71a8-180">앱 타일을 마우스 오른쪽 단추로 클릭 하 고 제거를 클릭 하거나 [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)을 사용 하 여 PowerShell을 통해 저장소에서 설치 된 wsl 배포를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="d71a8-181">Ping이 권한 거부 오류를 생성 하는 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="d71a8-182">WSL에서 14926 < 빌드는 관리자 권한 콘솔을 통해 실행 하는 데 필요한 WSL을 ping 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="d71a8-183">이 문제는 빌드 14926 이상에서 해결 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="d71a8-184">OpenSSH 서버를 실행할 어떻게 할까요? 있나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="d71a8-185">WSL에서 OpenSSH를 실행 하려면 Windows의 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="d71a8-186">OpenSSH 서버를 실행 하려면 관리자 권한으로 Windows의 Ubuntu에서 Bash를 실행 하거나 관리자 권한으로 CMD/PowerShell 프롬프트에서 bash를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="d71a8-187">"오류: 0x80040306 "를 설치 하려고 하면</span><span class="sxs-lookup"><span data-stu-id="d71a8-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="d71a8-188">WSL은 레거시 콘솔에서 실행을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="d71a8-189">레거시 콘솔을 해제 하려면:</span><span class="sxs-lookup"><span data-stu-id="d71a8-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="d71a8-190">WSL, PowerShell 또는 Cmd를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="d71a8-191">제목 표시줄-> 속성을 마우스 오른쪽 단추로 클릭 > "레거시 콘솔 사용" 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="d71a8-192">확인을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="d71a8-193">"오류: 0x80040154 "Windows를 업그레이드 한 후 bash를 실행 하는 경우</span><span class="sxs-lookup"><span data-stu-id="d71a8-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="d71a8-194">Windows 업데이트 중에 "Linux 용 Windows 하위 시스템" 기능이 사용 하지 않도록 설정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="d71a8-195">이 문제가 발생 하면 Windows 기능을 다시 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="d71a8-196">"Linux 용 Windows 하위 시스템" 기능을 사용 하도록 설정 하는 방법에 대 한 지침은 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="d71a8-197">WSL의 표시 언어를 변경 어떻게 할까요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="d71a8-198">WSL install은 Windows 설치의 로캘과 일치 하도록 Ubuntu 로캘을 자동으로 변경 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="d71a8-199">이 동작을 원하지 않는 경우 설치가 완료 된 후이 명령을 실행 하 여 Ubuntu 로캘을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="d71a8-200">이 변경 내용이 적용 되려면 bash를 다시 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="d71a8-201">아래 예제에서는 로캘을 en-us로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="d71a8-202">WSL에서 인터넷에 액세스할 수 없는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="d71a8-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="d71a8-203">일부 사용자가 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램의 문제를 보고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="d71a8-204">보고 된 방화벽은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="d71a8-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="d71a8-205">Kaspersky</span></span>
1. <span data-ttu-id="d71a8-206">매출</span><span class="sxs-lookup"><span data-stu-id="d71a8-206">AVG</span></span>
1. <span data-ttu-id="d71a8-207">Avast</span><span class="sxs-lookup"><span data-stu-id="d71a8-207">Avast</span></span>

<span data-ttu-id="d71a8-208">방화벽을 해제 하면 액세스가 허용 되는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="d71a8-209">경우에 따라 방화벽을 설치 하면 액세스를 차단 하는 것으로 보입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="d71a8-210">Windows의 WSL에서 포트에 액세스 어떻게 할까요??</span><span class="sxs-lookup"><span data-stu-id="d71a8-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="d71a8-211">WSL은 windows에서 실행 되는 Windows의 IP 주소를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="d71a8-212">따라서 localhost의 모든 포트 (예: 포트 1234 https://localhost:1234 에 웹 콘텐츠가 있는 경우)에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="d71a8-213">내 WSL 배포판을 백업 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="d71a8-214">배포판을 백업 하는 가장 좋은 방법은 Windows 버전 1809 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="d71a8-215">`wsl --export` 명령을 사용 하 여 전체 배포를 tarball로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="d71a8-216">그런 다음 `wsl --import` 명령을 사용 하 여이 배포판을 wsl로 다시 가져올 수 있으므로 wsl 배포판의 상태를 백업 하 고 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="d71a8-217">Appdata 폴더 (예: Windows 백업)의 파일을 백업 하는 기존 백업 서비스는 Linux 파일을 손상 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="d71a8-218">어디에서 피드백을 제공할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="d71a8-218">Where can I provide feedback?</span></span>

<span data-ttu-id="d71a8-219">여러 채널을 통해 피드백을 공유 하 고 질문할 수 있습니다. 사용자 의견 및 질문을 다음으로 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a8-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="d71a8-220">[GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="d71a8-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="d71a8-221">[명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="d71a8-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="d71a8-222">Microsoft [명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="d71a8-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="d71a8-223">Twitter를 통해.</span><span class="sxs-lookup"><span data-stu-id="d71a8-223">Via Twitter.</span></span> <span data-ttu-id="d71a8-224">Twitter를 [@richturn_ms](https://twitter.com/richturn_MS) 따라 뉴스, 업데이트 등에 대해 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="d71a8-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
