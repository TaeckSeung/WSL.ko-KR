---
title: Linux 용 Windows 하위 시스템 명령 참조
description: Linux 용 Windows 하위 시스템을 관리 하는 명령 목록
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307652"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="30f35-104">Linux 용 Windows 하위 시스템에 대 한 명령 참조</span><span class="sxs-lookup"><span data-stu-id="30f35-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="30f35-105">Linux 용 Windows 하위 시스템을 조작 하는 가장 좋은 방법은 `wsl.exe` 명령을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="30f35-106">다음은 Windows 버전 1903를 사용 하 `wsl.exe` 는 경우 모든 옵션을 포함 하는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="30f35-107">Linux 이진 파일을 실행 하기 위한 인수:</span><span class="sxs-lookup"><span data-stu-id="30f35-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="30f35-108">명령줄이 제공 되지 않은 경우 wsl .exe는 기본 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="30f35-109">--exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="30f35-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="30f35-110">기본 Linux 셸을 사용 하지 않고 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="30f35-111">나머지 명령줄을 있는 그대로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="30f35-112">옵션:</span><span class="sxs-lookup"><span data-stu-id="30f35-112">Options:</span></span>
    * <span data-ttu-id="30f35-113">--분포,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="30f35-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="30f35-114">지정 된 분포를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="30f35-115">--사용자,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="30f35-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="30f35-116">지정 된 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-116">Run as the specified user.</span></span>

* <span data-ttu-id="30f35-117">Linux 용 Windows 하위 시스템을 관리 하기 위한 인수:</span><span class="sxs-lookup"><span data-stu-id="30f35-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="30f35-118">--내보내기 <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="30f35-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="30f35-119">배포를 tar 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="30f35-120">표준 출력의 경우 파일 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="30f35-121">--import <Distro> <InstallLocation>[Options <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="30f35-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="30f35-122">지정 된 tar 파일을 새 배포로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="30f35-123">표준 입력의 경우 파일 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="30f35-124">옵션:</span><span class="sxs-lookup"><span data-stu-id="30f35-124">Options:</span></span>
            * <span data-ttu-id="30f35-125">--version <Version> 새 배포에 사용할 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="30f35-126">--list,-l [Options]</span><span class="sxs-lookup"><span data-stu-id="30f35-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="30f35-127">분포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-127">Lists distributions.</span></span>

        * <span data-ttu-id="30f35-128">옵션:</span><span class="sxs-lookup"><span data-stu-id="30f35-128">Options:</span></span>
            * <span data-ttu-id="30f35-129">--모두</span><span class="sxs-lookup"><span data-stu-id="30f35-129">--all</span></span>
                * <span data-ttu-id="30f35-130">현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="30f35-131">--실행 중</span><span class="sxs-lookup"><span data-stu-id="30f35-131">--running</span></span>
                * <span data-ttu-id="30f35-132">현재 실행 중인 배포만 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="30f35-133">--set-기본값,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="30f35-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="30f35-134">분포를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="30f35-135">--set-기본값-버전<Version></span><span class="sxs-lookup"><span data-stu-id="30f35-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="30f35-136">새 배포에 대 한 기본 설치 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="30f35-137">--set-version <Distro><Version></span><span class="sxs-lookup"><span data-stu-id="30f35-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="30f35-138">지정 된 분포의 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="30f35-139">--terminate,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="30f35-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="30f35-140">지정 된 분포를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="30f35-141">--등록 취소<Distro></span><span class="sxs-lookup"><span data-stu-id="30f35-141">--unregister <Distro></span></span>
        * <span data-ttu-id="30f35-142">배포를 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="30f35-143">--help</span><span class="sxs-lookup"><span data-stu-id="30f35-143">--help</span></span>
        * <span data-ttu-id="30f35-144">사용법 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="30f35-145">추가 명령</span><span class="sxs-lookup"><span data-stu-id="30f35-145">Additional Commands</span></span>

<span data-ttu-id="30f35-146">또한 Linux 용 Windows 하위 시스템을 조작 하는 기록 명령도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="30f35-147">해당 기능은에 포함 `wsl.exe`되어 있지만 여전히 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="30f35-148">이 명령을 사용 하 여 WSL 배포를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="30f35-149">다음은 해당 옵션의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-149">Below is a list of its options.</span></span>

* <span data-ttu-id="30f35-150">/l,/list [Option]</span><span class="sxs-lookup"><span data-stu-id="30f35-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="30f35-151">등록 된 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="30f35-152">/all-필요에 따라 현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="30f35-153">/실행 중-현재 실행 중인 배포만 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="30f35-154">/s,/setdefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="30f35-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="30f35-155">분포를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="30f35-156">/t,/종료<DistributionName></span><span class="sxs-lookup"><span data-stu-id="30f35-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="30f35-157">분포를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-157">Terminates the distribution.</span></span>

* <span data-ttu-id="30f35-158">/u,/unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="30f35-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="30f35-159">배포를 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="30f35-160">이 명령은 bash 셸을 시작 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="30f35-161">다음은이 명령에서 사용할 수 있는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="30f35-162">지정 된 옵션이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-162">No Option given</span></span>
    * <span data-ttu-id="30f35-163">현재 디렉터리에서 Bash 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="30f35-164">Bash 셸이 설치 되어 있지 않으면 자동으로 실행 됩니다.`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="30f35-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="30f35-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="30f35-165">bash ~</span></span>
    * <span data-ttu-id="30f35-166">사용자의 홈 디렉터리에 bash 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="30f35-167">실행과 `cd ~`비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="30f35-168">bash-c "&lt;명령&gt;"</span><span class="sxs-lookup"><span data-stu-id="30f35-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="30f35-169">명령을 실행 하 고 출력을 출력 한 다음 Windows 명령 프롬프트로 다시 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="30f35-170">예 들어`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="30f35-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="30f35-171">사용 되지 않는 명령</span><span class="sxs-lookup"><span data-stu-id="30f35-171">Deprecated Commands</span></span>

<span data-ttu-id="30f35-172">는 `lxrun.exe` Linux 용 Windows 하위 시스템을 설치 하 고 관리 하는 데 사용 되는 첫 번째 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="30f35-173">Windows 10 1803 이상에서 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="30f35-174">명령을 `lxrun.exe` 사용 하 여 [Linux 용 Windows 하위 시스템 (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) 을 직접 조작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="30f35-175">이러한 명령은 `\Windows\System32` 디렉터리에 설치 되며, Windows 명령 프롬프트 또는 PowerShell 내에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="30f35-176">Command</span><span class="sxs-lookup"><span data-stu-id="30f35-176">Command</span></span>                     | <span data-ttu-id="30f35-177">설명</span><span class="sxs-lookup"><span data-stu-id="30f35-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="30f35-178">Lxrun 명령은 WSL 인스턴스를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="30f35-179">다운로드 및 설치 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="30f35-180">모든 프롬프트를 무시 하도록 **/y** 를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="30f35-181">확인 메시지가 자동으로 수락 되 고 기본 사용자가 root로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="30f35-182">Ubuntu 이미지를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="30f35-183">기본적으로 사용자의 Ubuntu 홈 디렉터리는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="30f35-184">자동으로 확인 메시지를 수락 하도록 **/y** 를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="30f35-185">**/full** 사용자의 Ubuntu 홈 디렉터리를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="30f35-186">Ubuntu 사용자에 대 한 기본 Bash를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="30f35-187">지정 된 사용자가 없는 경우 암호를 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="30f35-188">자세한 내용은을 참조 https://aka.ms/wslusers 하세요.</span><span class="sxs-lookup"><span data-stu-id="30f35-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="30f35-189">**/y** 암호에 대 한 promping를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="30f35-190">사용자가 암호 없이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="30f35-191">하위 시스템의 패키지 인덱스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f35-191">Updates the subsystem's package index</span></span>          |
