---
title: Linux 배포를 관리 합니다.
description: 목록 및 Linux 용 Windows 하위 시스템에서 실행 되는 여러 Linux 배포를 구성 참조 합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, wsl.conf, wslconfig 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063501"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="9f653-104">관리 및 Linux 용 Windows 하위 시스템 구성</span><span class="sxs-lookup"><span data-stu-id="9f653-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="9f653-105">이상 Windows 10 Fall Creators Update 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="9f653-106">이 업데이트 된 참조 [설치 가이드](./install_guide.md) 새로운 관리 기능을 시도 하 여 Windows 스토어에서 여러 Linux 배포판을 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="9f653-107">WSL를 실행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9f653-107">Ways to run WSL</span></span>

<span data-ttu-id="9f653-108">Linux 용 Windows 하위 시스템을 사용 하 여 Linux를 실행 하는 방법은 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="9f653-109">`[distro]` ie `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="9f653-109">`[distro]` ie `ubuntu`</span></span>
1. <span data-ttu-id="9f653-110">`wsl.exe` 또는 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="9f653-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="9f653-111">`wsl [command]` 또는 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="9f653-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="9f653-112">어떤 방법을 사용 해야 하는 일에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="9f653-113">WSL를 배포 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="9f653-113">Launch WSL by distribution</span></span>

<span data-ttu-id="9f653-114">자체 콘솔 창에서 해당 배포를 시작의 배포판 관련 응용 프로그램을 사용 하 여 배포를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![WSL 시작 메뉴에서 시작](media/start-launch.png)

<span data-ttu-id="9f653-116">패턴은 Windows 스토어에서 "시작"을 클릭 한 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![WSL Windows 스토어에서 시작](media/store-launch.png)

<span data-ttu-id="9f653-118">실행 하 여 명령줄에서 배포를 실행할 수도 있습니다 `[distribution].exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="9f653-119">이러한 방식으로 명령줄에서 배포를 실행 하는 단점은 자동으로 변경 됩니다 작업 디렉터리는 현재 디렉터리에서 분포의 홈 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="9f653-120">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="9f653-121">wsl 및 wsl [command]</span><span class="sxs-lookup"><span data-stu-id="9f653-121">wsl and wsl [command]</span></span>

<span data-ttu-id="9f653-122">WSL 명령줄에서 실행 하는 가장 좋은 방법은 사용 하 여 `wsl.exe`입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="9f653-123">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="9f653-124">뿐만 아니라 `wsl` 쪽 Windows 명령 함께 단일 명령을 실행 하면, 현재 작업 디렉터리를 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="9f653-125">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="9f653-126">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="9f653-127">여러 Linux 배포를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="9f653-128">Windows 10 버전이 1903 이상</span><span class="sxs-lookup"><span data-stu-id="9f653-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="9f653-129">사용할 수 있습니다 `wsl.exe` Windows 하위 시스템에 대 한 WSL (Linux)를 사용할 수 있는 배포를 나열, 기본 배포를 설정 및 배포를 제거를 포함 하 여 프로그램 배포를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="9f653-130">각 Linux 배포에서 자체 구성을 독립적으로 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="9f653-131">배포 관련 명령을 확인 하려면 실행 `[distro.exe] /?`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="9f653-132">예를 들면 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="9f653-133">목록 배포</span><span class="sxs-lookup"><span data-stu-id="9f653-133">List distributions</span></span>

<span data-ttu-id="9f653-134">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="9f653-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="9f653-135">WSL를 사용할 수 있는 사용 가능한 Linux 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="9f653-136">배포 되 면 설치 되 고 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="9f653-137">현재 사용할 수 없는 포함 하는 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="9f653-138">이러한 제거를 설치 하는 중일 수 있습니다 또는 손상 된 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="9f653-139">현재 실행 중인 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="9f653-140">기본 배포를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-140">Set a default distribution</span></span>

<span data-ttu-id="9f653-141">기본 WSL 배포를 실행할 때 실행 되는 것은 `wsl` 명령줄에서.</span><span class="sxs-lookup"><span data-stu-id="9f653-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="9f653-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="9f653-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="9f653-143">기본 배포 설정 하는 `<DistributionName>`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="9f653-144">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-144">**Example:**</span></span>  
<span data-ttu-id="9f653-145">`wsl -s Ubuntu` Ubuntu에 기본 배포 내 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="9f653-146">실행할 때 이제 `wsl npm init` Ubuntu에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="9f653-147">실행 하면 `wsl` Ubuntu 세션을 열립니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="9f653-148">등록을 취소 하 고 배포를 다시 설치</span><span class="sxs-lookup"><span data-stu-id="9f653-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="9f653-149">Linux 배포는 Windows를 통해 설치할 수 있습니다 하는 동안 저장, 저장소를 통해 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="9f653-150">WSL 구성 배포를 등록 취소/제거를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="9f653-151">등록 취소 하면 배포를를 다시 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="9f653-152">**주의:** 등록 취소 되 면 모든 데이터, 설정 및 해당 배포와 관련 된 소프트웨어 영구적으로 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="9f653-153">저장소에서 다시 설치 하면 배포의 깨끗 한 사본이 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="9f653-154">다시 설치 하거나 정리할 수 있도록 WSL에서 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="9f653-155">예를 들어: `wsl -unregister Ubuntu` Ubuntu WSL에서 사용할 수 있는 배포에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="9f653-156">실행할 때 `wsl --list` 나열 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="9f653-157">을 다시 설치 하려면 Windows 스토어에서 배포를 찾아 "시작"을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="9f653-158">특정 사용자로 실행</span><span class="sxs-lookup"><span data-stu-id="9f653-158">Run as a specific user</span></span>

<span data-ttu-id="9f653-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="9f653-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="9f653-160">WSL 지정된 된 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-160">Run WSL as the specified user.</span></span> <span data-ttu-id="9f653-161">해당 사용자는 WSL 배포 내에 있어야 합니다. note 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9f653-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="9f653-162">또한 특정 분포를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-162">Run a specific distribution</span></span>

<span data-ttu-id="9f653-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="9f653-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="9f653-164">WSL의 지정된 된 배포를 실행, 기본 변경 하지 않고도 특정 배포에 명령을 보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="9f653-165">Windows 10 버전 1903 보다 이전 버전</span><span class="sxs-lookup"><span data-stu-id="9f653-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="9f653-166">WSL 구성 (`wslconfig.exe`) Linux (WSL) 용 Windows 하위 시스템에서 실행 중인 Linux 배포를 관리 하기 위한 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="9f653-167">사용할 수 있는 배포 목록를 기본 배포를 설정 하 고 배포를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="9f653-168">WSL 구성에 걸쳐 하거나 배포를 조정 하는 설정에 대 한 유용한 상태인 각 Linux 배포 독립적으로 관리 하지 자체 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="9f653-169">배포 관련 명령을 확인 하려면 실행 `[distro.exe] /?`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="9f653-170">예를 들면 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="9f653-171">Wslconfig에 대 한 모든 사용 가능한 옵션을 보려면 다음을 실행 합니다.  `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="9f653-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="9f653-172">목록 배포</span><span class="sxs-lookup"><span data-stu-id="9f653-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="9f653-173">WSL를 사용할 수 있는 사용 가능한 Linux 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="9f653-174">배포 되 면 설치 되 고 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="9f653-175">현재 사용할 수 없는 포함 하는 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="9f653-176">이러한 제거를 설치 하는 중일 수 있습니다 또는 손상 된 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="9f653-177">기본 배포를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-177">Set a default distribution</span></span>

<span data-ttu-id="9f653-178">기본 WSL 배포를 실행할 때 실행 되는 것은 `wsl` 명령줄에서.</span><span class="sxs-lookup"><span data-stu-id="9f653-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="9f653-179">기본 배포 설정 하는 `<DistributionName>`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="9f653-180">**예:**</span><span class="sxs-lookup"><span data-stu-id="9f653-180">**Example:**</span></span>  
<span data-ttu-id="9f653-181">`wslconfig /setdefault Ubuntu` Ubuntu에 기본 배포 내 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="9f653-182">실행할 때 이제 `wsl npm init` Ubuntu에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="9f653-183">실행 하면 `wsl` Ubuntu 세션을 열립니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="9f653-184">등록을 취소 하 고 배포를 다시 설치</span><span class="sxs-lookup"><span data-stu-id="9f653-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="9f653-185">Linux 배포는 Windows를 통해 설치할 수 있습니다 하는 동안 저장, 저장소를 통해 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="9f653-186">WSL 구성 배포를 등록 취소/제거를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="9f653-187">등록 취소 하면 배포를를 다시 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="9f653-188">**주의:** 등록 취소 되 면 모든 데이터, 설정 및 해당 배포와 관련 된 소프트웨어 영구적으로 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="9f653-189">저장소에서 다시 설치 하면 배포의 깨끗 한 사본이 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="9f653-190">다시 설치 하거나 정리할 수 있도록 WSL에서 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="9f653-191">예를 들어: `wslconfig /unregister Ubuntu` Ubuntu WSL에서 사용할 수 있는 배포에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="9f653-192">실행할 때 `wslconfig /list` 나열 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="9f653-193">을 다시 설치 하려면 Windows 스토어에서 배포를 찾아 "시작"을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="9f653-194">WSL 시작 설정</span><span class="sxs-lookup"><span data-stu-id="9f653-194">Set WSL launch settings</span></span>

> <span data-ttu-id="9f653-195">**Windows Insider 빌드 17093 이상 사용할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="9f653-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="9f653-196">특정 기능을 사용 하 여 하위 시스템을 시작할 때마다 적용 되는 WSL에서 자동으로 구성 `wsl.conf`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="9f653-197">오른쪽 이제 여기에 자동 탑재 옵션 및 네트워크 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="9f653-198">`wsl.conf` 각 Linux 배포에 위치한 `/etc/wsl.conf`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="9f653-199">파일이 없는, 만들 직접 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="9f653-200">WSL는 파일의 존재 여부 감지 및 해당 내용을 읽는 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="9f653-201">파일이 없거나 형식이 잘못 된 경우 (즉, 잘못 된 태그 형식), WSL는 계속 정상적으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="9f653-202">다음은 샘플 `wsl.conf` 파일에 배포판에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="9f653-203">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="9f653-203">Configuration Options</span></span>

<span data-ttu-id="9f653-204">.Ini 규칙에 따라 키 섹션에서 선언 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="9f653-205">WSL 두 섹션을 지원 합니다. `automount` 및 `network`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="9f653-206">자동 탑재</span><span class="sxs-lookup"><span data-stu-id="9f653-206">automount</span></span>

<span data-ttu-id="9f653-207">섹션: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="9f653-207">Section: `[automount]`</span></span>


| <span data-ttu-id="9f653-208">Key</span><span class="sxs-lookup"><span data-stu-id="9f653-208">key</span></span>        | <span data-ttu-id="9f653-209">value</span><span class="sxs-lookup"><span data-stu-id="9f653-209">value</span></span>                          | <span data-ttu-id="9f653-210">기본</span><span class="sxs-lookup"><span data-stu-id="9f653-210">default</span></span>      | <span data-ttu-id="9f653-211">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f653-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f653-212">enabled</span><span class="sxs-lookup"><span data-stu-id="9f653-212">enabled</span></span>    | <span data-ttu-id="9f653-213">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-213">boolean</span></span>                        | <span data-ttu-id="9f653-214">true</span><span class="sxs-lookup"><span data-stu-id="9f653-214">true</span></span>         | <span data-ttu-id="9f653-215">`true` 고정 드라이브 (즉, 원인</span><span class="sxs-lookup"><span data-stu-id="9f653-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="9f653-216">`C:/` 또는 `D:/`)에서 DrvFs를 사용 하 여 자동으로 탑재할 `/mnt`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="9f653-217">`false` 드라이브를 자동으로 탑재할 수 없습니다 하지만 수 여전히 탑재할 하 수동으로 또는 통해 `fstab`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="9f653-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="9f653-218">mountFsTab</span></span> | <span data-ttu-id="9f653-219">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-219">boolean</span></span>                        | <span data-ttu-id="9f653-220">true</span><span class="sxs-lookup"><span data-stu-id="9f653-220">true</span></span>         | <span data-ttu-id="9f653-221">`true` 설정 `/etc/fstab` 처리할 WSL 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="9f653-222">/etc/fstab에 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="9f653-223">따라서 시작 시 WSL에서 자동으로 이러한 파일 시스템을 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="9f653-224">루트</span><span class="sxs-lookup"><span data-stu-id="9f653-224">root</span></span>       | <span data-ttu-id="9f653-225">문자열</span><span class="sxs-lookup"><span data-stu-id="9f653-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="9f653-226">고정된 드라이브는 자동으로 탑재 디렉터리를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="9f653-227">예를 들어 WSL에서 디렉터리에 `/windir/` 를 루트로 예상 되는 고정된 드라이브에 탑재를 지정 하 고 `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="9f653-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="9f653-228">옵션</span><span class="sxs-lookup"><span data-stu-id="9f653-228">options</span></span>    | <span data-ttu-id="9f653-229">값의 쉼표로 구분 된 목록</span><span class="sxs-lookup"><span data-stu-id="9f653-229">comma-separated list of values</span></span> | <span data-ttu-id="9f653-230">빈 문자열</span><span class="sxs-lookup"><span data-stu-id="9f653-230">empty string</span></span> | <span data-ttu-id="9f653-231">이 값은 기본 DrvFs 탑재 옵션 문자열에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="9f653-232">**DrvFs 별 옵션 으로만 지정할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="9f653-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="9f653-233">이진 탑재는 일반적으로 플래그를 구문 분석 하는 옵션이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="9f653-234">해당 옵션을 명시적으로 지정 하려는 경우에 /etc/fstab에 이렇게 하려면 모든 드라이브를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="9f653-235">기본적으로 WSL uid 및 gid 값으로 설정 된 기본 사용자 (uid를 사용 하 여 Ubuntu 배포판에 기본 사용자를 만들면 1000 = gid = 1000)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="9f653-236">이 키를 통해 명시적으로 gid 또는 uid 옵션을 지정 하는 사용자, 관련된 값을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="9f653-237">그렇지 않은 경우 기본값 추가 항상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="9f653-238">**참고:** 이러한 옵션은 모두 자동으로 탑재 된 드라이브에 대 한 탑재 옵션으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="9f653-239">특정 드라이브에 대 한 옵션을 변경 하려면 /etc/fstab을 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="9f653-240">네트워크</span><span class="sxs-lookup"><span data-stu-id="9f653-240">network</span></span>

<span data-ttu-id="9f653-241">섹션 레이블: `[network]`</span><span class="sxs-lookup"><span data-stu-id="9f653-241">Section label: `[network]`</span></span>

| <span data-ttu-id="9f653-242">Key</span><span class="sxs-lookup"><span data-stu-id="9f653-242">key</span></span> | <span data-ttu-id="9f653-243">value</span><span class="sxs-lookup"><span data-stu-id="9f653-243">value</span></span> | <span data-ttu-id="9f653-244">기본</span><span class="sxs-lookup"><span data-stu-id="9f653-244">default</span></span> | <span data-ttu-id="9f653-245">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f653-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="9f653-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="9f653-246">generateHosts</span></span> | <span data-ttu-id="9f653-247">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-247">boolean</span></span> | `true` | <span data-ttu-id="9f653-248">`true` WSL 생성 설정 `/etc/hosts`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="9f653-249">`hosts` 파일 호스트 이름 해당 IP 주소의 정적 맵이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="9f653-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="9f653-250">generateResolvConf</span></span> | <span data-ttu-id="9f653-251">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-251">boolean</span></span> | `true` | <span data-ttu-id="9f653-252">`true` WSL 생성 설정 `/etc/resolv.conf`합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="9f653-253">`resolv.conf` 지정된 된 호스트 이름을 해당 IP 주소로 확인할 수 있는 DNS 목록을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="9f653-254">Interop</span><span class="sxs-lookup"><span data-stu-id="9f653-254">interop</span></span>

<span data-ttu-id="9f653-255">섹션 레이블: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="9f653-255">Section label: `[interop]`</span></span>

<span data-ttu-id="9f653-256">이러한 옵션에는 참가자 빌드 17713에서 사용할 수 있는 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="9f653-257">Key</span><span class="sxs-lookup"><span data-stu-id="9f653-257">key</span></span> | <span data-ttu-id="9f653-258">value</span><span class="sxs-lookup"><span data-stu-id="9f653-258">value</span></span> | <span data-ttu-id="9f653-259">기본</span><span class="sxs-lookup"><span data-stu-id="9f653-259">default</span></span> | <span data-ttu-id="9f653-260">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f653-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="9f653-261">enabled</span><span class="sxs-lookup"><span data-stu-id="9f653-261">enabled</span></span> | <span data-ttu-id="9f653-262">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-262">boolean</span></span> | `true` | <span data-ttu-id="9f653-263">이 키 설정을 WSL는 시작 Windows 프로세스를 지원 하는지 여부를 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="9f653-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="9f653-264">appendWindowsPath</span></span> | <span data-ttu-id="9f653-265">boolean</span><span class="sxs-lookup"><span data-stu-id="9f653-265">boolean</span></span> | `true` | <span data-ttu-id="9f653-266">이 키 설정을 WSL $PATH 환경 변수의에 Windows 경로 요소를 추가 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f653-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
