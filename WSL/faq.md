---
title: FAQ(질문과 대답)
description: 질문과 대답 Windows 하위 시스템에 대 한 Linux 용입니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063271"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="053db-104">Linux 용 Windows 하위 시스템에 대 한 질문 질문과</span><span class="sxs-lookup"><span data-stu-id="053db-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="053db-105">Windows 하위 시스템에 대 한 WSL (Linux) 란?</span><span class="sxs-lookup"><span data-stu-id="053db-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="053db-106">Linux (WSL) 용 Windows 하위 시스템에 함께 기존 Windows 데스크톱 및 최신 스토어 앱, Windows에서 직접 네이티브 Linux 명령줄 도구를 실행할 수 있는 새 Windows 10 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="053db-107">참조 된 [페이지에 대 한](./about.md) 대 한 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="053db-108">에 대 한 WSL는 누구 인가요?</span><span class="sxs-lookup"><span data-stu-id="053db-108">Who is WSL for?</span></span>
<span data-ttu-id="053db-109">이것이 기본적으로 개발자가-특히 웹 개발자 또는 오픈 소스 프로젝트를 사용 하 여 작업 하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="053db-110">이 사용자에 게 원하는/Bash, 일반적인 Linux 도구를 사용 해야 합니다. (`sed`, `awk`등) 및 (Ruby, Python 등) Windows에서 해당 도구 체인을 사용 하려면 여러 Linux 중심 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="053db-111">WSL를 사용 하 여 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-111">What can I do with WSL?</span></span>
<span data-ttu-id="053db-112">WSL은 프로그램이 Bash.exe는 시작 될 때 호출, 열립니다 Bash 셸을 실행 하는 Windows 콘솔을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="053db-113">Bash를 사용 하는 명령줄 Linux 도구 및 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="053db-114">예를 들어 입력 `lsb_release -a` enter 키를 누릅니다 하 고 현재 실행 중인 Linux 배포판의 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![배포 세부 정보 스크린샷](media/distro.png)

<span data-ttu-id="053db-116">Linux Bash 셸 내에서 로컬 컴퓨터의 파일 시스템에 액세스할 수도 있습니다 – 아래의 탑재 된 로컬 드라이브를 찾을 수 있습니다는 `/mnt` 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="053db-117">예를 들어 프로그램 `C:` 아래에서 드라이브를 탑재 `/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="053db-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![탑재 된 C 드라이브의 스크린샷](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="053db-119">Bash 란?</span><span class="sxs-lookup"><span data-stu-id="053db-119">What is Bash?</span></span>
<span data-ttu-id="053db-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 은 인기 있는 텍스트를 기반으로 셸 및 명령 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="053db-121">MacOS에 Ubuntu 및 다른 Linux 배포판 내에 포함 된 기본 셸을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="053db-122">사용자는 스크립트를 실행 하거나 여러 작업을 수행 하는 명령 및 도구를 실행 하는 shell에 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="053db-123">어떻게 작동합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-123">How does this work?</span></span>
<span data-ttu-id="053db-124">체크 아웃 우리의 [블로그](https://blogs.msdn.microsoft.com/wsl/) 기본 기술에 대 한 세부 정보로 이동 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="053db-125">VM의 Linux 대신 WSL 사용은 이유</span><span class="sxs-lookup"><span data-stu-id="053db-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="053db-126">WSL를 전체 가상 머신 보다 더 적은 리소스 (CPU, 메모리 및 저장소)에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="053db-127">WSL를 사용 하면 Linux 명령줄 도구 및 앱과 함께 Windows 명령줄에서 바탕 화면 및 스토어에서 앱을 실행 하 고 linux에서 Windows 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="053db-128">이 옵션을 사용 하면 원하는 경우 파일의 동일한 집합에 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="053db-129">왜 사용 해야 합니까, 예를 들어 Windows 대신 Linux에서 Ruby?</span><span class="sxs-lookup"><span data-stu-id="053db-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="053db-130">일부 플랫폼 간 도구를 실행 하는 환경 Linux 처럼 가정 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="053db-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="053db-131">예를 들어, 일부 도구는 매우 긴 파일 경로 액세스할 수 있는지 또는 특정 파일/폴더가 있음을 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="053db-132">이 문제의 원인이 되기도 종종 동작 하는 Windows에서 다르게 Linux에서.</span><span class="sxs-lookup"><span data-stu-id="053db-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="053db-133">종종 Ruby 노드와 같은 많은 언어에 이식 되며, Windows에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="053db-134">그러나 Windows를 지원 하기 위해 해당 라이브러리를 포트 Ruby 보석 또는 노드/NPM 라이브러리 소유자의 일부 Linux 관련 종속성이 있는 여러 하며</span><span class="sxs-lookup"><span data-stu-id="053db-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="053db-135">이 이러한 도구 및 라이브러리 빌드 및 경우에 따라 런타임 오류 또는 Windows에서 원치 않는 동작에서 포괄적으로 구축 된 시스템에서 자주 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="053db-136">이들은 많은 사람들이 Windows' 명령줄 도구 및 canonical 네이티브 Bash 및 Linux 명령줄 도구를 Windows에서 실행할 수 있도록 파트너을 이끌기도 무엇을 개선 하기 위해 Microsoft에 게 발생 시킨 문제 중 일부에 불과합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="053db-137">PowerShell에 대 한 무슨 뜻인가요?</span><span class="sxs-lookup"><span data-stu-id="053db-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="053db-138">OSS 프로젝트를 사용 하는 동안 시나리오가 많은 것이 매우 유용한 PowerShell에서 Bash를 삭제 하려면 프롬프트입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="053db-139">Bash 지원을 보완 되며 Windows, 다른 인기 있는 기술을 활용 하 여 PowerShell 및 PowerShell 커뮤니티에서 명령줄의 값을 강화 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="053db-140">자세한 내용은 PowerShell 팀 블로그- [Bash에 대 한 Windows: 멋진 하는 이유 및 PowerShell에 끼치는 의미](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="053db-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="053db-141">WSL에서 모든 Linux 앱을 실행할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="053db-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="053db-142">아니요!</span><span class="sxs-lookup"><span data-stu-id="053db-142">No!</span></span> <span data-ttu-id="053db-143">WSL에 Bash를 실행 하 고 Windows에서 Linux 명령줄 도구를 코어 수 필요한 사용자 수 있도록 하기 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="053db-144">WSL 않습니다 **되지** GUI 데스크톱 또는 응용 프로그램 (예: Gnome, KDE 등)를 지원 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="053db-145">또한도 수 많은 인기 있는 서버 응용 프로그램 (예: Redis) WSL 프로덕션 서비스를 호스팅하기 위한 권장 하지는 않습니다 – Microsoft는 다양 한 프로덕션을 Azure에서 Linux 워크 로드 실행에 대 한 솔루션을 제공 합니다. Hyper-v 및 Docker.</span><span class="sxs-lookup"><span data-stu-id="053db-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="053db-146">에 WSL에서 포함 되어 Windows Sku는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="053db-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="053db-147">Linux 용 Windows 하위 시스템은 데스크톱 버전의 Windows 10 Anniversary Windows 및 크리에이터 스 업데이트 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="053db-148">부터 Fall Creators update WSL 데스크톱과 서버 Sku의 Windows에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="053db-149">WSL에서 어떤 프로세서를 지원 하나요?</span><span class="sxs-lookup"><span data-stu-id="053db-149">What processors does WSL support?</span></span>
<span data-ttu-id="053db-150">WSL은 x64 및 ARM Cpu를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="053db-151">C: 드라이브에 액세스 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-151">How do I access my C: drive?</span></span>
<span data-ttu-id="053db-152">로컬 컴퓨터의 하드 드라이브에 대 한 탑재 지점을 자동으로 생성 됩니다 및 Windows 파일 시스템에 대 한 쉬운 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="053db-153">**/mnt/\<드라이브 문자 > /**</span><span class="sxs-lookup"><span data-stu-id="053db-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="053db-154">사용 예 `cd /mnt/c` c:\ 액세스 하려면</span><span class="sxs-lookup"><span data-stu-id="053db-154">Example usage would be `cd /mnt/c` to access c:\\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="053db-155">Linux 앱을 사용 하 여 Windows 파일을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="053db-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="053db-156">WSL의 이점 중 하나는 Windows 및 Linux 응용 프로그램 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="053db-157">WSL에서 컴퓨터의 고정된 드라이브를 탑재 합니다 `/mnt/<drive>` 에 Linux 배포판에 대 한 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="053db-158">예를 들어 프로그램 `C:` 드라이브 아래에 탑재 됩니다 `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="053db-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="053db-159">탑재 된 드라이브를 사용 하 여 편집할 수 있습니다, 코드 예를 들어 `C:\dev\myproj\` 를 사용 하 여 [Visual Studio](https://visualstudio.microsoft.com/vs/) / 또는 [VS Code](https://code.visualstudio.com/), 및 Linux에서 해당 코드를 통해 동일한 파일에 액세스 하 여 빌드/테스트 `\mnt\c\dev\myproj`합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `\mnt\c\dev\myproj`.</span></span>

> <span data-ttu-id="053db-160">**중요 참고**: WSL를 사용 하는 주요 제한 사항 중 하나입니다는 직접 액세스/변경은 Windows 응용 프로그램 또는 도구를 사용 하 여 Linux 배포판의 파일 시스템에 파일이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="053db-161">참조 [Windows 앱 및 도구를 사용 하 여 Linux 파일을 변경 하지 마세요](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="053db-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="053db-162">탑재 된 Windows 드라이브에서 다양 한 Linux 드라이브의 파일은 있나요?</span><span class="sxs-lookup"><span data-stu-id="053db-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="053db-163">Linux 루트 아래에 있는 파일 (예: `/`) Linux 특정 동작을 포함 하지만에 제한 되지 않는 유사한 WSL에 의해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="053db-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="053db-164">잘못 된 Windows 파일 이름 문자가 포함 된 파일</span><span class="sxs-lookup"><span data-stu-id="053db-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="053db-165">관리자가 아닌 사용자를 위해 만든 Symlink</span><span class="sxs-lookup"><span data-stu-id="053db-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="053db-166">Chmod 및 chown를 통해 파일 특성 변경</span><span class="sxs-lookup"><span data-stu-id="053db-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="053db-167">파일/폴더 대/소문자 구분</span><span class="sxs-lookup"><span data-stu-id="053db-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="053db-168">탑재 된 드라이브의 Windows에 의해 제어 되는 파일과 다음과 같은 결과:</span><span class="sxs-lookup"><span data-stu-id="053db-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="053db-169">대/소문자 구분을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-169">Support case sensitivity</span></span>
   * <span data-ttu-id="053db-170">모든 권한은 가장 Windows 권한을 나타내도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="053db-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="053db-171">이유는 무엇입니까 많은 오류 apt get 업그레이드를 실행할 때?</span><span class="sxs-lookup"><span data-stu-id="053db-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="053db-172">일부 패키지는 아직 구현 되지 않은 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="053db-173">`udev`예를 들어, 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="053db-174">관련 된 문제를 해결 하려면 `udev`, 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="053db-175">다음을 작성 `/usr/sbin/policy-rc.d` 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="053db-176">추가 권한을 실행 `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="053db-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="053db-177">다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="053db-178">WSL 배포를 제거 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="053db-179">1709 (16299) 열기 전에 명령 프롬프트를 빌드하고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="053db-180">앱 타일을 마우스 오른쪽 단추로 클릭 하 고 제거를 클릭 하거나 사용 하 여 PowerShell을 통해 다른 Windows 앱 처럼 스토어에서 설치한 WSL 배포를 제거할 수 있습니다 합니다 [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="053db-181">Ping 사용 권한 거부 오류를 생성 하는 이유</span><span class="sxs-lookup"><span data-stu-id="053db-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="053db-182">WSL 구축 < 14926, ping WSL 상승 된 콘솔을 통해 실행 하려면 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="053db-183">빌드 14926 이상이 문제가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="053db-184">OpenSSH 서버를 실행 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="053db-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="053db-185">WSL에서 OpenSSH를 실행 하려면 Windows에서 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="053db-186">OpenSSH 서버를를 실행 하려면 관리자로 서 Windows에서 Ubuntu의 Bash를 실행 하거나 bash.exe 관리자 권한으로 CMD/PowerShell 프롬프트에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="053db-187">왜 "오류: 0x80040306 "설치 하려고 하나요?</span><span class="sxs-lookup"><span data-stu-id="053db-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="053db-188">WSL 레거시 콘솔을 실행 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="053db-189">레거시 콘솔 사용 하지 않으려면:</span><span class="sxs-lookup"><span data-stu-id="053db-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="053db-190">WSL, PowerShell 또는 Cmd를 열으십시오</span><span class="sxs-lookup"><span data-stu-id="053db-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="053db-191">제목을 마우스 오른쪽 단추로 클릭-> 모음 속성의 선택을 취소 "레거시 콘솔 사용 하 여"-></span><span class="sxs-lookup"><span data-stu-id="053db-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="053db-192">확인을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="053db-193">왜 "오류: 0x80040154 "Windows를 업그레이드 한 후 bash.exe를 실행 하나요?</span><span class="sxs-lookup"><span data-stu-id="053db-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="053db-194">"Windows 하위 시스템에 대 한 Linux" 기능을 비활성화할 수 있습니다 Windows 업데이트 중입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="053db-195">이 경우 Windows 기능을 다시 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="053db-196">"Windows 하위 시스템에 대 한 Linux" 기능을 사용 하는 것에 대 한 지침을 찾을 수 있습니다 합니다 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="053db-197">WSL의 표시 언어를 변경 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="053db-198">WSL 설치는 Windows 설치의 로캘이 일치 하는 Ubuntu 로캘을 자동으로 변경 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="053db-199">이 문제를 원하지 않는 경우 설치가 완료 되 면 Ubuntu 로캘을 변경 하려면이 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="053db-200">이 변경 내용을 적용 하려면 bash.exe를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="053db-201">아래 예제에서는 EN-US 로캘 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="053db-202">왜 없습니다 있습니까 WSL에서 인터넷 액세스?</span><span class="sxs-lookup"><span data-stu-id="053db-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="053db-203">일부 사용자에 게 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램을 사용 하 여 문제를 보고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="053db-204">보고 하는 방화벽은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="053db-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="053db-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="053db-205">Kaspersky</span></span>
1. <span data-ttu-id="053db-206">AVG</span><span class="sxs-lookup"><span data-stu-id="053db-206">AVG</span></span>
1. <span data-ttu-id="053db-207">Avast</span><span class="sxs-lookup"><span data-stu-id="053db-207">Avast</span></span>

<span data-ttu-id="053db-208">일부 경우에 대 한 액세스 허용 방화벽을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="053db-209">일부 경우에 대 한 액세스 차단 보일 방화벽이 설치 되어 있는 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="053db-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="053db-210">포트를 Windows에서 WSL에서 액세스 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="053db-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="053db-211">WSL은 Windows에서 실행 되는 Windows에서의 IP 주소를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="053db-212">예: localhost에서 모든 포트에 액세스할 수 있습니다 따라서 1234 할 수 있습니다. 포트에서 웹 콘텐츠 했다면 https://localhost:1234 Windows 브라우저에 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="053db-213">피드백을 제공할 수는 있는</span><span class="sxs-lookup"><span data-stu-id="053db-213">Where can I provide feedback?</span></span>

<span data-ttu-id="053db-214">피드백을 공유 하 고 여러 채널을 통해 궁금한 사항을 문의할 수 있습니다. 사용자 의견 및 질문을 전달 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="053db-214">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="053db-215">우리의 [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="053db-215">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="053db-216">우리의 [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="053db-216">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="053db-217">우리의 [명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="053db-217">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="053db-218">Twitter를 통해.</span><span class="sxs-lookup"><span data-stu-id="053db-218">Via Twitter.</span></span> <span data-ttu-id="053db-219">따르세요 [ @richturn_ms ](https://twitter.com/richturn_MS) 뉴스, 업데이트를 파악 하는 Twitter에서 등입니다.</span><span class="sxs-lookup"><span data-stu-id="053db-219">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
