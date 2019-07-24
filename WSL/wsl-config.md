---
title: Linux 배포 관리
description: Linux 용 Windows 하위 시스템에서 실행 되는 여러 Linux 배포를 나열 하 고 구성 하는 참조입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, wsl., wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499272"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="10957-104">Linux 용 Windows 하위 시스템 관리 및 구성</span><span class="sxs-lookup"><span data-stu-id="10957-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="10957-105">Windows 10로의 작성자 업데이트 이상에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="10957-106">새 관리 기능을 사용해 보고 Microsoft 스토어에서 여러 Linux 배포를 실행 하기 시작 하려면 업데이트 된 [설치 가이드](./install_guide.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="10957-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="10957-107">WSL 실행 방법</span><span class="sxs-lookup"><span data-stu-id="10957-107">Ways to run WSL</span></span>

<span data-ttu-id="10957-108">Linux 용 Windows 하위 시스템을 사용 하 여 Linux를 실행 하는 방법에는 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="10957-109">`[distro]`예를 들어`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="10957-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="10957-110">`wsl.exe` 또는 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="10957-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="10957-111">`wsl [command]` 또는 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="10957-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="10957-112">사용 해야 하는 방법은 수행 중인 작업에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="10957-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="10957-113">배포 별 WSL 시작</span><span class="sxs-lookup"><span data-stu-id="10957-113">Launch WSL by distribution</span></span>

<span data-ttu-id="10957-114">배포판 특정 응용 프로그램을 사용 하 여 배포를 실행 하면 자체 콘솔 창에서 해당 배포가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![시작 메뉴에서 WSL 시작](media/start-launch.png)

<span data-ttu-id="10957-116">Microsoft store에서 "시작"을 클릭 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft store에서 WSL 시작](media/store-launch.png)

<span data-ttu-id="10957-118">을 실행 `[distribution].exe`하 여 명령줄에서 배포를 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="10957-119">이러한 방식으로 명령줄에서 배포를 실행 하는 경우의 단점은 작업 디렉터리를 현재 디렉터리에서 배포의 홈 디렉터리로 자동으로 변경 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="10957-120">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="10957-121">wsl 및 wsl [명령]</span><span class="sxs-lookup"><span data-stu-id="10957-121">wsl and wsl [command]</span></span>

<span data-ttu-id="10957-122">명령줄에서 WSL을 실행 하는 가장 좋은 방법은를 사용 `wsl.exe`하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="10957-123">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="10957-124">현재 작업 디렉터리 `wsl` 를 그대로 유지할 수 있을 뿐 아니라 Windows 명령을 함께 사용 하 여 단일 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="10957-125">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-125">**Example:**</span></span>

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

<span data-ttu-id="10957-126">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="10957-127">여러 Linux 배포 관리</span><span class="sxs-lookup"><span data-stu-id="10957-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="10957-128">Windows 10 버전 1903 이상</span><span class="sxs-lookup"><span data-stu-id="10957-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="10957-129">를 사용 `wsl.exe` 하 여 Linux 용 Windows 하위 시스템 (wsl)의 배포를 관리할 수 있습니다. 여기에는 사용 가능한 배포 나열, 기본 배포 설정, 배포 제거 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="10957-130">각 Linux 배포판은 독립적으로 자체 구성을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="10957-131">배포 관련 명령을 보려면를 실행 `[distro.exe] /?`합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="10957-132">예를 들면 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="10957-133">배포 나열</span><span class="sxs-lookup"><span data-stu-id="10957-133">List distributions</span></span>

<span data-ttu-id="10957-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="10957-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="10957-135">WSL에서 사용할 수 있는 Linux 배포판을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="10957-136">배포가 나열 되 면 설치 되어 사용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="10957-137">현재 사용할 수 없는 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="10957-138">이러한 작업은 설치, 제거 또는 손상 된 상태에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="10957-139">현재 실행 중인 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="10957-140">기본 배포 설정</span><span class="sxs-lookup"><span data-stu-id="10957-140">Set a default distribution</span></span>

<span data-ttu-id="10957-141">기본 wsl 배포는 명령줄에서 실행할 `wsl` 때 실행 되는 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="10957-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="10957-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="10957-143">기본 분포를로 `<DistributionName>`설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="10957-144">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-144">**Example:**</span></span>  
<span data-ttu-id="10957-145">`wsl -s Ubuntu`기본 배포를 Ubuntu로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="10957-146">이제 실행 `wsl npm init` 하면 Ubuntu에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="10957-147">실행 `wsl` 하는 경우 Ubuntu 세션이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="10957-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="10957-148">배포 등록 취소 및 다시 설치</span><span class="sxs-lookup"><span data-stu-id="10957-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="10957-149">Linux 배포판은 Microsoft store를 통해 설치할 수 있지만 스토어에서는 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="10957-150">WSL Config를 사용 하면 배포를 등록 취소 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="10957-151">등록을 취소 하면 배포도 다시 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="10957-152">**주의:** 등록을 취소 하면 해당 배포와 관련 된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="10957-153">저장소에서 다시 설치 하면 배포의 정리 된 복사본을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="10957-154">설치 하거나 정리할 수 있도록 WSL에서 배포의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="10957-155">예를 들어 `wsl --unregister Ubuntu` 는 wsl에서 사용할 수 있는 배포에서 Ubuntu를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="10957-156">실행 `wsl --list` 하면 나열 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="10957-157">를 다시 설치 하려면 Microsoft 스토어에서 배포를 찾아 "시작"을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="10957-158">특정 사용자로 실행</span><span class="sxs-lookup"><span data-stu-id="10957-158">Run as a specific user</span></span>

<span data-ttu-id="10957-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="10957-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="10957-160">지정 된 사용자로 WSL을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-160">Run WSL as the specified user.</span></span> <span data-ttu-id="10957-161">사용자는 WSL 배포 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="10957-162">특정 배포 실행</span><span class="sxs-lookup"><span data-stu-id="10957-162">Run a specific distribution</span></span>

<span data-ttu-id="10957-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="10957-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="10957-164">WSL의 지정 된 배포를 실행 합니다. 기본값을 변경 하지 않고도 특정 배포에 명령을 보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="10957-165">Windows 10 버전 1903 이전 버전</span><span class="sxs-lookup"><span data-stu-id="10957-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="10957-166">Wsl Config (`wslconfig.exe`)는 wsl (linux 용 Windows 하위 시스템)에서 실행 되는 linux 배포를 관리 하기 위한 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="10957-167">사용 가능한 배포를 나열 하 고, 기본 배포를 설정 하 고, 배포를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="10957-168">WSL Config는 배포를 확장 하거나 조정 하는 설정에 유용 하지만 각 Linux 배포는 독립적으로 자체 구성을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="10957-169">배포 관련 명령을 보려면를 실행 `[distro.exe] /?`합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="10957-170">예를 들면 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="10957-171">Wslconfig에 사용할 수 있는 모든 옵션을 보려면 다음을 실행 합니다.`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="10957-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="10957-172">배포 나열</span><span class="sxs-lookup"><span data-stu-id="10957-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="10957-173">WSL에서 사용할 수 있는 Linux 배포판을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="10957-174">배포가 나열 되 면 설치 되어 사용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="10957-175">현재 사용할 수 없는 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="10957-176">이러한 작업은 설치, 제거 또는 손상 된 상태에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="10957-177">기본 배포 설정</span><span class="sxs-lookup"><span data-stu-id="10957-177">Set a default distribution</span></span>

<span data-ttu-id="10957-178">기본 wsl 배포는 명령줄에서 실행할 `wsl` 때 실행 되는 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="10957-179">기본 분포를로 `<DistributionName>`설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="10957-180">**예제:**</span><span class="sxs-lookup"><span data-stu-id="10957-180">**Example:**</span></span>  
<span data-ttu-id="10957-181">`wslconfig /setdefault Ubuntu`기본 배포를 Ubuntu로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="10957-182">이제 실행 `wsl npm init` 하면 Ubuntu에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="10957-183">실행 `wsl` 하는 경우 Ubuntu 세션이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="10957-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="10957-184">배포 등록 취소 및 다시 설치</span><span class="sxs-lookup"><span data-stu-id="10957-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="10957-185">Linux 배포판은 Microsoft store를 통해 설치할 수 있지만 스토어에서는 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="10957-186">WSL Config를 사용 하면 배포를 등록 취소 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="10957-187">등록을 취소 하면 배포도 다시 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="10957-188">**주의:** 등록을 취소 하면 해당 배포와 관련 된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="10957-189">저장소에서 다시 설치 하면 배포의 정리 된 복사본을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="10957-190">설치 하거나 정리할 수 있도록 WSL에서 배포의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="10957-191">예를 들어 `wslconfig /unregister Ubuntu` 는 wsl에서 사용할 수 있는 배포에서 Ubuntu를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="10957-192">실행 `wslconfig /list` 하면 나열 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="10957-193">를 다시 설치 하려면 Microsoft 스토어에서 배포를 찾아 "시작"을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="10957-194">WSL 시작 설정 설정</span><span class="sxs-lookup"><span data-stu-id="10957-194">Set WSL launch settings</span></span>

> <span data-ttu-id="10957-195">**Windows 참가자 빌드 17093 이상에서 사용 가능**</span><span class="sxs-lookup"><span data-stu-id="10957-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="10957-196">를 사용 하 여 `wsl.conf`하위 시스템을 시작할 때마다 적용 될 특정 기능을 wsl에서 자동으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="10957-197">현재 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="10957-198">`wsl.conf`는의 `/etc/wsl.conf`각 Linux 배포에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="10957-199">파일이 없으면 직접 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="10957-200">WSL에서 파일의 존재를 감지 하 고 해당 내용을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="10957-201">파일이 없거나 잘못 된 태그 서식 지정 인 경우 WSL은 계속 정상적으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="10957-202">다음은 배포판에 `wsl.conf` 추가할 수 있는 샘플 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="10957-203">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="10957-203">Configuration Options</span></span>

<span data-ttu-id="10957-204">.Ini 규칙을 유지 하는 경우 키가 섹션 아래에 선언 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="10957-205">Wsl은 및 라는 두 `automount` 개의 `network`섹션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="10957-206">자동 탑재</span><span class="sxs-lookup"><span data-stu-id="10957-206">automount</span></span>

<span data-ttu-id="10957-207">여기서`[automount]`</span><span class="sxs-lookup"><span data-stu-id="10957-207">Section: `[automount]`</span></span>


| <span data-ttu-id="10957-208">Key</span><span class="sxs-lookup"><span data-stu-id="10957-208">key</span></span>        | <span data-ttu-id="10957-209">value</span><span class="sxs-lookup"><span data-stu-id="10957-209">value</span></span>                          | <span data-ttu-id="10957-210">기본</span><span class="sxs-lookup"><span data-stu-id="10957-210">default</span></span>      | <span data-ttu-id="10957-211">메모란</span><span class="sxs-lookup"><span data-stu-id="10957-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10957-212">enabled</span><span class="sxs-lookup"><span data-stu-id="10957-212">enabled</span></span>    | <span data-ttu-id="10957-213">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-213">boolean</span></span>                        | <span data-ttu-id="10957-214">true</span><span class="sxs-lookup"><span data-stu-id="10957-214">true</span></span>         | <span data-ttu-id="10957-215">`true`고정 드라이브 (즉,</span><span class="sxs-lookup"><span data-stu-id="10957-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="10957-216">`C:/`또는 `D:/`)를 사용 하 여 자동으로 `/mnt`DrvFs에 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="10957-217">`false`는 드라이브가 자동으로 탑재 되지 않음을 의미 하지만 수동으로 또는를 통해 `fstab`탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="10957-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="10957-218">mountFsTab</span></span> | <span data-ttu-id="10957-219">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-219">boolean</span></span>                        | <span data-ttu-id="10957-220">true</span><span class="sxs-lookup"><span data-stu-id="10957-220">true</span></span>         | <span data-ttu-id="10957-221">`true`wsl start에서 처리할를 설정 `/etc/fstab` 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="10957-222">/etc/fstab는 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="10957-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="10957-223">따라서 시작 시 WSL에서 자동으로 이러한 파일 시스템를 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="10957-224">루트</span><span class="sxs-lookup"><span data-stu-id="10957-224">root</span></span>       | <span data-ttu-id="10957-225">문자열</span><span class="sxs-lookup"><span data-stu-id="10957-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="10957-226">고정 드라이브가 자동으로 탑재 되는 디렉터리를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="10957-227">예를 들어 wsl `/windir/` 에 디렉터리가 있고이를 루트로 지정 하는 경우 고정 드라이브가에 탑재 된 것을 볼 수 있습니다.`/windir/c`</span><span class="sxs-lookup"><span data-stu-id="10957-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="10957-228">옵션</span><span class="sxs-lookup"><span data-stu-id="10957-228">options</span></span>    | <span data-ttu-id="10957-229">쉼표로 구분 된 값 목록</span><span class="sxs-lookup"><span data-stu-id="10957-229">comma-separated list of values</span></span> | <span data-ttu-id="10957-230">빈 문자열</span><span class="sxs-lookup"><span data-stu-id="10957-230">empty string</span></span> | <span data-ttu-id="10957-231">이 값은 기본 DrvFs 탑재 옵션 문자열에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="10957-232">**DrvFs 옵션만 지정할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="10957-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="10957-233">탑재 이진이 일반적으로 플래그로 구문 분석 하는 옵션은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="10957-234">이러한 옵션을 명시적으로 지정 하려면/etc/fstab에서 수행 하려는 모든 드라이브를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="10957-235">기본적으로 WSL은 uid 및 gid를 기본 사용자의 값으로 설정 합니다 (Ubuntu 배포판에서 기본 사용자는 uid = 1000, gid = 1000으로 만들어짐).</span><span class="sxs-lookup"><span data-stu-id="10957-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="10957-236">사용자가이 키를 통해 gid 또는 uid 옵션을 명시적으로 지정 하면 연결 된 값이 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="10957-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="10957-237">그렇지 않으면 기본값이 항상 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="10957-238">**참고:** 이러한 옵션은 자동으로 탑재 된 모든 드라이브에 대 한 탑재 옵션으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="10957-239">특정 드라이브에 대 한 옵션만 변경 하려면 대신/etc/fstab를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="10957-240">network</span><span class="sxs-lookup"><span data-stu-id="10957-240">network</span></span>

<span data-ttu-id="10957-241">섹션 레이블:`[network]`</span><span class="sxs-lookup"><span data-stu-id="10957-241">Section label: `[network]`</span></span>

| <span data-ttu-id="10957-242">Key</span><span class="sxs-lookup"><span data-stu-id="10957-242">key</span></span> | <span data-ttu-id="10957-243">value</span><span class="sxs-lookup"><span data-stu-id="10957-243">value</span></span> | <span data-ttu-id="10957-244">기본</span><span class="sxs-lookup"><span data-stu-id="10957-244">default</span></span> | <span data-ttu-id="10957-245">메모란</span><span class="sxs-lookup"><span data-stu-id="10957-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="10957-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="10957-246">generateHosts</span></span> | <span data-ttu-id="10957-247">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-247">boolean</span></span> | `true` | <span data-ttu-id="10957-248">`true`생성할 `/etc/hosts`wsl을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="10957-249">이 `hosts` 파일에는 해당 IP 주소에 해당 하는 호스트 이름에 대 한 정적 맵이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="10957-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="10957-250">generateResolvConf</span></span> | <span data-ttu-id="10957-251">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-251">boolean</span></span> | `true` | <span data-ttu-id="10957-252">`true`WSL을 생성 `/etc/resolv.conf`하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="10957-253">에 `resolv.conf` 는 IP 주소에 대해 지정 된 호스트 이름을 확인할 수 있는 DNS 목록이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="10957-254">rop</span><span class="sxs-lookup"><span data-stu-id="10957-254">interop</span></span>

<span data-ttu-id="10957-255">섹션 레이블:`[interop]`</span><span class="sxs-lookup"><span data-stu-id="10957-255">Section label: `[interop]`</span></span>

<span data-ttu-id="10957-256">이러한 옵션은 Insider Build 17713 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10957-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="10957-257">Key</span><span class="sxs-lookup"><span data-stu-id="10957-257">key</span></span> | <span data-ttu-id="10957-258">value</span><span class="sxs-lookup"><span data-stu-id="10957-258">value</span></span> | <span data-ttu-id="10957-259">기본</span><span class="sxs-lookup"><span data-stu-id="10957-259">default</span></span> | <span data-ttu-id="10957-260">메모란</span><span class="sxs-lookup"><span data-stu-id="10957-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="10957-261">enabled</span><span class="sxs-lookup"><span data-stu-id="10957-261">enabled</span></span> | <span data-ttu-id="10957-262">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-262">boolean</span></span> | `true` | <span data-ttu-id="10957-263">이 키를 설정 하면 WSL에서 Windows 프로세스 시작을 지원 하는지 여부가 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10957-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="10957-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="10957-264">appendWindowsPath</span></span> | <span data-ttu-id="10957-265">boolean</span><span class="sxs-lookup"><span data-stu-id="10957-265">boolean</span></span> | `true` | <span data-ttu-id="10957-266">이 키를 설정 하면 WSL에서 $PATH 환경 변수에 Windows 경로 요소를 추가할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10957-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
