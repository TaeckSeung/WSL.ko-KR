---
title: Linux 용 Windows 하위 시스템의 릴리스 정보
description: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보입니다.  매주 업데이트 됩니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: d2d91db24c12fc674d695ccffc79eb5781a0721d
ms.sourcegitcommit: be00abbb170aa569e008b804f15949344b378999
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68501578"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="6e861-105">Linux 용 Windows 하위 시스템의 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="6e861-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18947"></a><span data-ttu-id="6e861-106">빌드 18947</span><span class="sxs-lookup"><span data-stu-id="6e861-106">Build 18947</span></span>
<span data-ttu-id="6e861-107">빌드 18947에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18947/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-107">For general Windows information on build 18947 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18947/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-108">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-108">WSL</span></span>
* <span data-ttu-id="6e861-109">[WSL2] Localhost: port를 사용 하 여 호스트에서 WSL2의 수신 대기 tcp 소켓에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-109">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="6e861-110">[WSL2] 향후 문제를 추적 하기 위한 설치/변환 오류 및 추가 진단 수정 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="6e861-110">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="6e861-111">[WSL2] 진단 가능 WSL2 네트워크 문제 개선</span><span class="sxs-lookup"><span data-stu-id="6e861-111">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="6e861-112">[WSL2] 4.19.55에 커널 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e861-112">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="6e861-113">[WSL2] Docker에 필요한 구성 옵션을 사용 하 여 커널 업데이트 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="6e861-113">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="6e861-114">[WSL2] 경량 유틸리티 VM에 할당 된 Cpu 수를 호스트와 동일 하 게 늘립니다 (이전에는 커널 구성의 CONFIG_NR_CPUS에서 8 번 이상). [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="6e861-114">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="6e861-115">[WSL2] WSL2 경량 VM에 대 한 스왑 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="6e861-115">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="6e861-116">[WSL2] Wsl $ \\ \\배포판를통해사용자탑재를표시할수있습니다(예:sshfs)[GH4172]\\</span><span class="sxs-lookup"><span data-stu-id="6e861-116">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="6e861-117">[WSL2] 9p 파일 시스템 성능 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-117">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="6e861-118">[WSL2] Vhd ACL이 무제한으로 확장 되지 않았는지 확인 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="6e861-118">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="6e861-119">[WSL2] Squashfs 및 xt_conntrack를 지원 하도록 커널 구성 업데이트 [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="6e861-119">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="6e861-120">[WSL2] Interop에 대 한 수정. enabled/etc/wsl.conf 옵션 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="6e861-120">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="6e861-121">[WSL2] 파일 시스템에서 EAs를 지원 하지 않는 경우 ENOTSUP 반환</span><span class="sxs-lookup"><span data-stu-id="6e861-121">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="6e861-122">[WSL2] Wsl $를 \\사용 하 여 \\CopyFile 중단 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-122">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="6e861-123">기본 umask를 0022로 전환 하 고 umask 설정을/etc/wsl.conf에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-123">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="6e861-124">Symlink를 적절 하 게 확인 하기 위해 wslpath를 수정 합니다 .이는 19h1에서 회귀 되었습니다 [GH 4078].</span><span class="sxs-lookup"><span data-stu-id="6e861-124">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="6e861-125">트윅 WSL2 설정에\.대 한% UserProfile% wslconfig 파일 소개</span><span class="sxs-lookup"><span data-stu-id="6e861-125">Introduce %UserProfile%\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="6e861-126">빌드 18917</span><span class="sxs-lookup"><span data-stu-id="6e861-126">Build 18917</span></span>
<span data-ttu-id="6e861-127">빌드 18917에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-127">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-128">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-128">WSL</span></span>
* <span data-ttu-id="6e861-129">이제 WSL 2를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-129">WSL 2 is now available!</span></span> <span data-ttu-id="6e861-130">자세한 내용은 [블로그](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-130">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="6e861-131">Symlink를 통한 Windows 프로세스 시작이 올바르게 작동 하지 않는 재발 문제 해결 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="6e861-131">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="6e861-132">Wsl .exe--list--verbose, wsl .exe--list--quiet 및 wsl .exe--import--version 옵션을 wsl .exe에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-132">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="6e861-133">Wsl .exe--shutdown 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-133">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="6e861-134">계획 9: 쓰기에 대 한 디렉터리 열기가 성공 하도록 허용</span><span class="sxs-lookup"><span data-stu-id="6e861-134">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="6e861-135">빌드 18890</span><span class="sxs-lookup"><span data-stu-id="6e861-135">Build 18890</span></span>
<span data-ttu-id="6e861-136">빌드 18890에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-136">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-137">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-137">WSL</span></span>
* <span data-ttu-id="6e861-138">비 블로킹 소켓 누수 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="6e861-138">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="6e861-139">터미널의 EOF 입력은 후속 읽기를 차단할 수 있습니다 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="6e861-139">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="6e861-140">Resolv.conf를 참조 하도록 헤더를 업데이트 합니다. [GH 3928]에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-140">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="6e861-141">Epoll delete 코드의 교착 상태 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="6e861-141">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="6e861-142">인수에서--import 및 – export에 대 한 공백 처리 [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="6e861-142">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="6e861-143">Mmap 파일 확장은 제대로 작동 하지 않습니다 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="6e861-143">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="6e861-144">ARM64 \\wsl의 문제 해결 $ access가 제대로 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="6e861-144">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="6e861-145">Wsl .exe에 대해 더 나은 기본 아이콘 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-145">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="6e861-146">빌드 18342</span><span class="sxs-lookup"><span data-stu-id="6e861-146">Build 18342</span></span>
<span data-ttu-id="6e861-147">빌드 18342에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-147">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-148">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-148">WSL</span></span>
* <span data-ttu-id="6e861-149">사용자가 Windows에서 WSL 배포판의 Linux 파일에 액세스할 수 있는 기능을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-149">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="6e861-150">이러한 파일은 명령줄을 통해 액세스할 수 있으며 파일 탐색기, VSCode 등의 Windows 앱 에서도 이러한 파일과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-150">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="6e861-151">Wsl \\$ \\ \\ \\< distro_name >로 이동 하 여 파일에 액세스 하거나 wsl $으로 이동 하 여 실행 중인 배포의 목록을 확인 합니다.\\</span><span class="sxs-lookup"><span data-stu-id="6e861-151">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="6e861-152">추가 CPU 정보 태그 추가 및 Cpus_allowed [_list] 값 수정 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="6e861-152">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="6e861-153">비-리더 스레드의 exec 지원 [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="6e861-153">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="6e861-154">구성 업데이트 실패를 심각 하지 않은 것으로 처리 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="6e861-154">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="6e861-155">적절 한 오프셋을 적절 하 게 처리 하도록 binfmt 업데이트 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="6e861-155">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="6e861-156">계획 9에 대 한 네트워크 드라이브 매핑 사용 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="6e861-156">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="6e861-157">Bind 탑재를 위한 Windows > Linux 및 Linux > Windows 경로 변환 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-157">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="6e861-158">읽기 전용으로 열린 파일의 매핑에 대 한 읽기 전용 섹션 만들기</span><span class="sxs-lookup"><span data-stu-id="6e861-158">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="6e861-159">빌드 18334</span><span class="sxs-lookup"><span data-stu-id="6e861-159">Build 18334</span></span>
<span data-ttu-id="6e861-160">빌드 18334에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-160">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-161">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-161">WSL</span></span>
* <span data-ttu-id="6e861-162">Windows 표준 시간대가 Linux 표준 시간대에 매핑되는 방식 다시 디자인 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="6e861-162">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="6e861-163">메모리 누수 수정 및 새 문자열 변환 함수 추가 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="6e861-163">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="6e861-164">스레드가 없는 threadgroup의 SIGCONT가 no op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="6e861-164">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="6e861-165">/Proc/self/fd에 소켓 및 epoll 파일 설명자를 올바르게 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-165">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="6e861-166">빌드 18305</span><span class="sxs-lookup"><span data-stu-id="6e861-166">Build 18305</span></span>
<span data-ttu-id="6e861-167">빌드 18305에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-167">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-168">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-168">WSL</span></span>
* <span data-ttu-id="6e861-169">주 스레드가 종료 되 면 pthread가 파일에 액세스할 수 없게 됩니다. [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="6e861-169">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="6e861-170">필요한 경우가 아니면 TIOCSCTTY는 "force" 매개 변수를 무시 해야 합니다. [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="6e861-170">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="6e861-171">wsl .exe 명령줄 기능을 개선 하 고 가져오기/내보내기 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-171">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="6e861-172">빌드 18277</span><span class="sxs-lookup"><span data-stu-id="6e861-172">Build 18277</span></span>
<span data-ttu-id="6e861-173">빌드 18277에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-173">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-174">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-174">WSL</span></span>
* <span data-ttu-id="6e861-175">빌드 18272에 도입 된 "해당 인터페이스를 지원 하지 않습니다." 오류 해결 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="6e861-175">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="6e861-176">분리할 syscall에 대 한 MNT_FORCE 플래그 무시 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="6e861-176">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="6e861-177">공식 CreatePseudoConsole API를 사용 하도록 WSL interop 전환</span><span class="sxs-lookup"><span data-stu-id="6e861-177">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="6e861-178">FUTEX_WAIT를 다시 시작할 때 시간 제한 값을 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-178">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="6e861-179">빌드 18272</span><span class="sxs-lookup"><span data-stu-id="6e861-179">Build 18272</span></span>
<span data-ttu-id="6e861-180">빌드 18272에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-180">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-181">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-181">WSL</span></span>
* <span data-ttu-id="6e861-182">**내용의** 이 빌드에는 WSL이 작동 하지 않는 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-182">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="6e861-183">배포를 시작 하려고 하면 "해당 인터페이스가 지원 되지 않습니다." 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-183">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="6e861-184">이 문제는 해결 되었으며 다음 주의 Insider Fast 빌드에 포함 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-184">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="6e861-185">이 빌드를 설치한 경우 설정-> 업데이트 & 보안-> 복구에서 "이전 버전의 Windows 10으로 돌아가기"를 사용 하 여 이전 Windows 빌드로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-185">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="6e861-186">빌드 18267</span><span class="sxs-lookup"><span data-stu-id="6e861-186">Build 18267</span></span>
<span data-ttu-id="6e861-187">빌드 18267에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-187">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-188">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-188">WSL</span></span>
* <span data-ttu-id="6e861-189">좀비 프로세스가 reaped 수 없는 문제를 해결 하 고 무기한으로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-189">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="6e861-190">오류 메시지가 최대 길이를 초과 하는 경우 WslRegisterDistribution이 중지 됨 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="6e861-190">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="6e861-191">DrvFs에서 읽기 전용 파일에 대해 fsync가 성공 하도록 허용 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="6e861-191">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="6e861-192">Symlink를 만들기 전에/sbin 및 디렉터리가 존재 하는지 확인 합니다. [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="6e861-192">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="6e861-193">WSL 인스턴스에 대 한 인스턴스 종료 시간 제한 메커니즘을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-193">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="6e861-194">현재 시간 제한은 15 초로 설정 되어 있습니다. 즉, 인스턴스는 마지막 WSL 프로세스가 종료 된 후 15 초 후에 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-194">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="6e861-195">배포를 즉시 종료 하려면 다음을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-195">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="6e861-196">빌드 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="6e861-196">Build 17763 (1809)</span></span>
<span data-ttu-id="6e861-197">빌드 17763에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-197">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-198">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-198">WSL</span></span>
* <span data-ttu-id="6e861-199">Setpriority syscall permission check가 같은 스레드 우선 순위 변경에 대해 너무 엄격 하 게 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="6e861-199">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="6e861-200">Clock_gettime (CLOCK_BOOTTIME)에 대해 음수 값을 반환 하지 않도록 하기 위해 비편향 interrupt time이 부팅 시간에 사용 되는지 확인 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="6e861-200">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="6e861-201">WSL binfmt 인터프리터의 symlink 처리 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="6e861-201">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="6e861-202">Threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-202">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="6e861-203">오버플로를 방지 하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용 하도록 WSL 전환 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="6e861-203">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="6e861-204">Ptrace attach로 인해 시스템 호출에서 잘못 된 반환 값이 발생 하는 경우 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="6e861-204">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="6e861-205">여러 AF_UNIX 관련 문제 해결 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="6e861-205">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="6e861-206">현재 작업 디렉터리가 5 자 미만인 경우 WSL interop가 실패할 수 있는 문제 해결 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="6e861-206">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="6e861-207">존재 하지 않는 포트에 대 한 두 번째 지연 지연의 루프백 연결 방지 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="6e861-207">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="6e861-208">////> 추가/f i d/최대 스텁 파일 추가 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="6e861-208">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="6e861-209">더 정확한 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-209">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="6e861-210">PR_SET_PTRACER 지원 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="6e861-210">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="6e861-211">파이프 파일 시스템 실수로 edge에서 트리거된 epoll 이벤트 지우기 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6e861-211">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6e861-212">NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-212">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="6e861-213">향상 된 좀비 지원 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="6e861-213">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="6e861-214">Windows interop 동작을 제어 하기 위한 wsl. c 항목 추가 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="6e861-214">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="6e861-215">항상 UNIX 소켓 패밀리 유형을 반환 하지 않는 getsockname에 대 한 수정 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="6e861-215">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="6e861-216">TIOCSTI에 대 한 지원 추가 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="6e861-216">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="6e861-217">연결 프로세스의 비차단 소켓이 쓰기 시도에 대해 EAGAIN 반환 되어야 함 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="6e861-217">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="6e861-218">탑재 된 Vhd에 대 한 interop 지원 [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="6e861-218">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="6e861-219">루트 폴더에 대 한 사용 권한 확인 문제 해결 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="6e861-219">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="6e861-220">TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대 한 지원이 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-220">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="6e861-221">Windows UI 앱은 백그라운드에서 실행 되는 경우에도 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-221">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="6e861-222">Wsl-u 또는--user 옵션 추가 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="6e861-222">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="6e861-223">빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="6e861-223">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="6e861-224">Unix 소켓이 연결 되지 않은 피어 자격 증명을 유지 해야 하는 경우 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="6e861-224">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="6e861-225">비 블로킹 Unix 소켓이 EAGAIN로 무기한 실패 하는 경우 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="6e861-225">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="6e861-226">case = off는 새로운 기본 drvfs 탑재 유형 [GH 2937, 3212, 3328]입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-226">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="6e861-227">자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-227">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="6e861-228">배포 실행을 중지 하려면 wslconfig/terminate를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-228">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="6e861-229">공백으로 경로를 올바르게 처리 하지 않는 WSL shell 상황에 맞는 메뉴 항목의 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-229">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="6e861-230">디렉터리 단위 대/소문자 구분을 확장 특성으로 노출</span><span class="sxs-lookup"><span data-stu-id="6e861-230">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="6e861-231">ARM64 캐시 유지 관리 작업을 에뮬레이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-231">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="6e861-232">[Dotnet 문제](https://github.com/dotnet/core/issues/1561)를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-232">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="6e861-233">DrvFs: 전용 범위에서 이스케이프 된 문자에 해당 하는 문자만 unescape 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-233">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="6e861-234">ELF 파서 인터프리터 길이 유효성 검사에서 한 번 이상 오류 수정 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="6e861-234">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="6e861-235">WSL 과거 시간을 사용한 절대 타이머 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="6e861-235">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="6e861-236">새로 만든 재분석 지점이 부모 디렉터리에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-236">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="6e861-237">DrvFs에서 대/소문자를 구분 하는 디렉터리를 원자 단위로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-237">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="6e861-238">파일이 존재 하더라도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 추가 문제를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-238">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6e861-239">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6e861-239">[GH 2712]</span></span>
* <span data-ttu-id="6e861-240">UMCI를 사용 하는 경우 WSL 시작 실패가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-240">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="6e861-241">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="6e861-241">[GH 3020]</span></span>
* <span data-ttu-id="6e861-242">WSL [GH 437, 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-242">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="6e861-243">를 사용 하려면 shift 키를 누른 상태에서 탐색기 창에서 마우스 오른쪽 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-243">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="6e861-244">Unix 소켓이 차단 되지 않는 동작 수정 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="6e861-244">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="6e861-245">GH 2026에 보고 된 대로 NETLINK 명령을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-245">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="6e861-246">탑재 전파 플래그에 대 한 지원 추가 [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="6e861-246">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="6e861-247">Inotify 이벤트를 발생 시 키 지 않는 자르기 문제를 해결 합니다 [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="6e861-247">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="6e861-248">Wsl .exe를 추가 하 여 셸이 없는 단일 이진 파일을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-248">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="6e861-249">특정 배포판를 선택 하기 위해 wsl .exe의 추가--배포 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-249">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="6e861-250">Dmesg에 대 한 지원이 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-250">Limited support for dmesg.</span></span> <span data-ttu-id="6e861-251">이제 응용 프로그램이 dmesg에 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-251">Applications can now log to dmesg.</span></span> <span data-ttu-id="6e861-252">WSL 드라이버는 제한 된 정보를 dmesg로 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-252">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="6e861-253">나중에이를 확장 하 여 드라이버에서 다른 정보/진단을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-253">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="6e861-254">참고: dmesg는 현재 장치 인터페이스를 `/dev/kmsg` 통해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-254">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="6e861-255">`syslog`syscall 인터페이스는 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-255">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="6e861-256">따라서와 `dmesg` `-S`같은 명령줄옵션중일부는작동하지않습니다.`-C`</span><span class="sxs-lookup"><span data-stu-id="6e861-256">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="6e861-257">네이티브와 일치 하도록 직렬 장치의 기본 gid 및 모드 변경 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="6e861-257">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="6e861-258">DrvFs는 이제 확장 된 특성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-258">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="6e861-259">참고: DrvFs에는 확장 특성의 이름에 대 한 몇 가지 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-259">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="6e861-260">일부 문자 (예: '/', ': ' 및\*' ')는 허용 되지 않으며 확장 특성 이름은 DrvFs에서 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-260">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="6e861-261">빌드 18252 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-261">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-262">빌드 18252에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-262">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-263">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-263">WSL</span></span>
* <span data-ttu-id="6e861-264">Lxssmanager dll과 별도의 도구 폴더로 init 및 bsdtar 이진 파일을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-264">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="6e861-265">CLONE_FILES를 사용할 때 파일 설명자를 닫는 동안 경합 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-265">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="6e861-266">DrvFs 경로를 변환할 때/proc/pid/mountinfo의 선택적 필드를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-266">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="6e861-267">S_IFREG에 대 한 메타 데이터를 지원 하지 않고 DrvFs mknod가 성공 하도록 허용</span><span class="sxs-lookup"><span data-stu-id="6e861-267">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="6e861-268">DrvFs에서 만든 읽기 전용 파일에는 readonly 특성 집합이 있어야 합니다. [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="6e861-268">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="6e861-269">DrvFs 탑재를 처리 하는/sbin/mount.drvfs 도우미 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-269">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="6e861-270">DrvFs에서 POSIX rename을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-270">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="6e861-271">볼륨 GUID가 없는 볼륨에 대 한 경로 변환을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-271">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="6e861-272">빌드 17738 (빠름)</span><span class="sxs-lookup"><span data-stu-id="6e861-272">Build 17738 (Fast)</span></span>
<span data-ttu-id="6e861-273">빌드 17738에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-273">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-274">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-274">WSL</span></span>
* <span data-ttu-id="6e861-275">Setpriority syscall permission check가 같은 스레드 우선 순위 변경에 대해 너무 엄격 하 게 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="6e861-275">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="6e861-276">Clock_gettime (CLOCK_BOOTTIME)에 대해 음수 값을 반환 하지 않도록 하기 위해 비편향 interrupt time이 부팅 시간에 사용 되는지 확인 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="6e861-276">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="6e861-277">WSL binfmt 인터프리터의 symlink 처리 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="6e861-277">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="6e861-278">Threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-278">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="6e861-279">빌드 17728 (빠름)</span><span class="sxs-lookup"><span data-stu-id="6e861-279">Build 17728 (Fast)</span></span>
<span data-ttu-id="6e861-280">빌드 17728에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-280">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-281">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-281">WSL</span></span>
* <span data-ttu-id="6e861-282">오버플로를 방지 하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용 하도록 WSL 전환 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="6e861-282">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="6e861-283">Ptrace attach로 인해 시스템 호출에서 잘못 된 반환 값이 발생 하는 경우 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="6e861-283">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="6e861-284">여러 AF_UNIX 관련 문제 해결 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="6e861-284">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="6e861-285">현재 작업 디렉터리가 5 자 미만인 경우 WSL interop가 실패할 수 있는 문제 해결 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="6e861-285">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="6e861-286">빌드 18204 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-286">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-287">빌드 18204에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-287">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-288">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-288">WSL</span></span>
* <span data-ttu-id="6e861-289">파이프 파일 시스템 inadvertenly 지우기 edge-트리거된 epoll 이벤트 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6e861-289">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6e861-290">NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-290">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="6e861-291">빌드 17723 (빠름)</span><span class="sxs-lookup"><span data-stu-id="6e861-291">Build 17723 (Fast)</span></span>
<span data-ttu-id="6e861-292">빌드 17723에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-292">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-293">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-293">WSL</span></span>
* <span data-ttu-id="6e861-294">존재 하지 않는 포트에 대 한 두 번째 지연 지연의 루프백 연결 방지 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="6e861-294">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="6e861-295">////> 추가/f i d/최대 스텁 파일 추가 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="6e861-295">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="6e861-296">더 정확한 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-296">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="6e861-297">PR_SET_PTRACER 지원 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="6e861-297">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="6e861-298">파이프 파일 시스템 inadvertenly 지우기 edge-트리거된 epoll 이벤트 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6e861-298">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6e861-299">NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-299">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="6e861-300">빌드 17713</span><span class="sxs-lookup"><span data-stu-id="6e861-300">Build 17713</span></span>
<span data-ttu-id="6e861-301">빌드 17713에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-301">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-302">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-302">WSL</span></span>
* <span data-ttu-id="6e861-303">향상 된 좀비 지원 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="6e861-303">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="6e861-304">Windows interop 동작을 제어 하기 위한 wsl. c 항목 추가 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="6e861-304">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="6e861-305">항상 UNIX 소켓 패밀리 유형을 반환 하지 않는 getsockname에 대 한 수정 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="6e861-305">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="6e861-306">TIOCSTI에 대 한 지원 추가 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="6e861-306">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="6e861-307">연결 프로세스의 비차단 소켓이 쓰기 시도에 대해 EAGAIN 반환 되어야 함 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="6e861-307">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="6e861-308">탑재 된 Vhd에 대 한 interop 지원 [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="6e861-308">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="6e861-309">루트 폴더에 대 한 사용 권한 확인 문제 해결 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="6e861-309">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="6e861-310">TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대 한 지원이 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-310">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="6e861-311">Windows UI 앱은 백그라운드에서 실행 되는 경우에도 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-311">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="6e861-312">빌드 17704</span><span class="sxs-lookup"><span data-stu-id="6e861-312">Build 17704</span></span>
<span data-ttu-id="6e861-313">빌드 17704에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-313">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-314">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-314">WSL</span></span>
* <span data-ttu-id="6e861-315">Wsl-u 또는--user 옵션 추가 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="6e861-315">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="6e861-316">빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="6e861-316">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="6e861-317">Unix 소켓이 연결 되지 않은 피어 자격 증명을 유지 해야 하는 경우 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="6e861-317">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="6e861-318">비 블로킹 Unix 소켓이 EAGAIN로 무기한 실패 하는 경우 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="6e861-318">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="6e861-319">case = off는 새로운 기본 drvfs 탑재 유형 [GH 2937, 3212, 3328]입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-319">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="6e861-320">자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-320">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="6e861-321">배포 실행을 중지 하려면 wslconfig/terminate를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-321">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="6e861-322">빌드 17692</span><span class="sxs-lookup"><span data-stu-id="6e861-322">Build 17692</span></span>
<span data-ttu-id="6e861-323">빌드 17692에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-323">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-324">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-324">WSL</span></span>
* <span data-ttu-id="6e861-325">공백으로 경로를 올바르게 처리 하지 않는 WSL shell 상황에 맞는 메뉴 항목의 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-325">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="6e861-326">디렉터리 단위 대/소문자 구분을 확장 특성으로 노출</span><span class="sxs-lookup"><span data-stu-id="6e861-326">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="6e861-327">ARM64 캐시 유지 관리 작업을 에뮬레이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-327">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="6e861-328">[Dotnet 문제](https://github.com/dotnet/core/issues/1561)를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-328">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="6e861-329">DrvFs: 전용 범위에서 이스케이프 된 문자에 해당 하는 문자만 unescape 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-329">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="6e861-330">빌드 17686</span><span class="sxs-lookup"><span data-stu-id="6e861-330">Build 17686</span></span>
<span data-ttu-id="6e861-331">빌드 17686에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-331">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-332">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-332">WSL</span></span>
* <span data-ttu-id="6e861-333">ELF 파서 인터프리터 길이 유효성 검사에서 한 번 이상 오류 수정 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="6e861-333">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="6e861-334">WSL 과거 시간을 사용한 절대 타이머 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="6e861-334">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="6e861-335">새로 만든 재분석 지점이 부모 디렉터리에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-335">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="6e861-336">DrvFs에서 대/소문자를 구분 하는 디렉터리를 원자 단위로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-336">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="6e861-337">빌드 17677</span><span class="sxs-lookup"><span data-stu-id="6e861-337">Build 17677</span></span>
<span data-ttu-id="6e861-338">빌드 17677에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-338">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-339">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-339">WSL</span></span>
* <span data-ttu-id="6e861-340">파일이 존재 하더라도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 추가 문제를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-340">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6e861-341">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6e861-341">[GH 2712]</span></span>
* <span data-ttu-id="6e861-342">UMCI를 사용 하는 경우 WSL 시작 실패가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-342">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="6e861-343">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="6e861-343">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="6e861-344">빌드 17666</span><span class="sxs-lookup"><span data-stu-id="6e861-344">Build 17666</span></span>
<span data-ttu-id="6e861-345">빌드 17666에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-345">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-346">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-346">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="6e861-347">경고: 일부 AMD 칩셋에서 WSL이 실행 되지 않도록 하는 문제가 있습니다 [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="6e861-347">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="6e861-348">수정이 준비 되 고 참가자 빌드 분기에 대 한 방법이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-348">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="6e861-349">WSL [GH 437, 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-349">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="6e861-350">Shift 키를 누른 상태에서 탐색기 창에서 마우스 오른쪽 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-350">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="6e861-351">Unix 소켓이 차단 되지 않는 동작 수정 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="6e861-351">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="6e861-352">GH 2026에 보고 된 대로 NETLINK 명령을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-352">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="6e861-353">탑재 전파 플래그에 대 한 지원 추가 [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="6e861-353">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="6e861-354">Inotify 이벤트를 발생 시 키 지 않는 자르기 문제를 해결 합니다 [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="6e861-354">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="6e861-355">Wsl .exe를 추가 하 여 셸이 없는 단일 이진 파일을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-355">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="6e861-356">특정 배포판를 선택 하기 위해 wsl .exe의 추가--배포 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-356">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="6e861-357">빌드 17655 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-357">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-358">빌드 17655에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-358">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-359">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-359">WSL</span></span>
* <span data-ttu-id="6e861-360">Dmesg에 대 한 지원이 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-360">Limited support for dmesg.</span></span> <span data-ttu-id="6e861-361">이제 응용 프로그램이 dmesg에 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-361">Applications can now log to dmesg.</span></span> <span data-ttu-id="6e861-362">WSL 드라이버는 제한 된 정보를 dmesg로 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-362">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="6e861-363">나중에이를 확장 하 여 드라이버에서 다른 정보/진단을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-363">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="6e861-364">참고: dmesg는 현재 장치 인터페이스를 `/dev/kmsg` 통해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-364">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="6e861-365">`syslog`sycall 인터페이스는 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-365">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="6e861-366">따라서와 `dmesg` `-S`같은 명령줄옵션중일부는작동하지않습니다.`-C`</span><span class="sxs-lookup"><span data-stu-id="6e861-366">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="6e861-367">파일이 있는 경우에도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-367">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6e861-368">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6e861-368">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="6e861-369">빌드 17639 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-369">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-370">빌드 17639에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-370">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-371">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-371">WSL</span></span>
* <span data-ttu-id="6e861-372">네이티브와 일치 하도록 직렬 장치의 기본 gid 및 모드 변경 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="6e861-372">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="6e861-373">DrvFs는 이제 확장 된 특성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-373">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="6e861-374">참고: DrvFs에는 확장 특성의 이름에 대 한 몇 가지 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-374">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="6e861-375">특히, 일부 문자 (예: '/', ': ' 및 '\*')는 허용 되지 않으며 확장 특성 이름은 DrvFs에서 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-375">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="6e861-376">빌드 17133 (빠름)</span><span class="sxs-lookup"><span data-stu-id="6e861-376">Build 17133 (Fast)</span></span>
<span data-ttu-id="6e861-377">빌드 17133에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-377">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-378">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-378">WSL</span></span>
* <span data-ttu-id="6e861-379">WSL에서 중단에 대 한 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-379">Fix for hang in WSL.</span></span> <span data-ttu-id="6e861-380">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="6e861-380">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="6e861-381">빌드 17128 (빠름)</span><span class="sxs-lookup"><span data-stu-id="6e861-381">Build 17128 (Fast)</span></span>
<span data-ttu-id="6e861-382">빌드 17128에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-382">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-383">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-383">WSL</span></span>
* <span data-ttu-id="6e861-384">없음</span><span class="sxs-lookup"><span data-stu-id="6e861-384">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="6e861-385">빌드 17627 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-385">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-386">빌드 17627에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-386">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-387">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-387">WSL</span></span>
* <span data-ttu-id="6e861-388">Futex pi 인식 작업에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-388">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="6e861-389">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="6e861-389">[GH 1006]</span></span>
    * <span data-ttu-id="6e861-390">우선 순위는 현재 지원 되는 WSL 기능이 아니므로 제한이 있지만 표준 사용을 차단 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-390">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="6e861-391">WSL 프로세스에 대 한 Windows 방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-391">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="6e861-392">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="6e861-392">[GH 1852]</span></span>
    * <span data-ttu-id="6e861-393">예를 들어 WSL python 프로세스가 모든 포트에서 수신 대기 하도록 허용 하려면 관리자 권한 Windows cmd를 사용 합니다.```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="6e861-393">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="6e861-394">방화벽 규칙을 추가 하는 방법에 대 한 자세한 내용은 [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-394">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="6e861-395">Wsl .exe를 사용할 때 사용자의 기본 셸을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-395">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="6e861-396">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="6e861-396">[GH 2372]</span></span>
* <span data-ttu-id="6e861-397">모든 네트워크 인터페이스를 이더넷으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-397">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="6e861-398">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="6e861-398">[GH 2996]</span></span>
* <span data-ttu-id="6e861-399">손상 된/etc/passwd 파일을 보다 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-399">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="6e861-400">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="6e861-400">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="6e861-401">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-401">Console</span></span>
* <span data-ttu-id="6e861-402">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-402">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-403">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-403">LTP Results:</span></span>
<span data-ttu-id="6e861-404">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-404">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="6e861-405">빌드 17618 (앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="6e861-405">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="6e861-406">빌드 17618에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-406">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-407">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-407">WSL</span></span>
* <span data-ttu-id="6e861-408">NT interop [GH 988, 1366, 1433, 1542, 2370, 2406]에 대 한 pseudoconsole 기능을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-408">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="6e861-409">레거시 설치 메커니즘 (lxrun)은 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-409">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="6e861-410">배포를 설치 하는 데 지원 되는 메커니즘은 Microsoft Store입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-410">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="6e861-411">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-411">Console</span></span>
* <span data-ttu-id="6e861-412">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-412">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-413">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-413">LTP Results:</span></span>
<span data-ttu-id="6e861-414">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-414">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="6e861-415">빌드 17110</span><span class="sxs-lookup"><span data-stu-id="6e861-415">Build 17110</span></span>
<span data-ttu-id="6e861-416">빌드 17110에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-416">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-417">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-417">WSL</span></span>
* <span data-ttu-id="6e861-418">Windows [GH 2928]에서/serers를 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-418">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="6e861-419">이제 DrvFs는 기본적으로 디렉터리 대/소문자 구분을 사용 합니다 ("case = dir" 탑재 옵션과 동일).</span><span class="sxs-lookup"><span data-stu-id="6e861-419">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="6e861-420">"Case = force" (이전 동작)를 사용 하려면 레지스트리 키를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-420">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="6e861-421">사용 해야 하는 경우 "case = force"를 사용 하도록 설정 하려면 다음 명령을 실행 합니다. reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="6e861-421">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="6e861-422">대/소문자를 구분 해야 하는 이전 버전의 Windows에서 wsl로 만든 기존 디렉터리를 사용 하는 경우에는 cmd.exe를 사용 하 여 대/소문자를 구분 합니다 <path> . 즉, fsutil .exe 파일 setcasesensitiveinfo enable을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-422">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="6e861-423">NULL은 uname syscall에서 반환 된 문자열을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-423">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="6e861-424">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-424">Console</span></span>
* <span data-ttu-id="6e861-425">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-425">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-426">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-426">LTP Results:</span></span>
<span data-ttu-id="6e861-427">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-427">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="6e861-428">빌드 17107</span><span class="sxs-lookup"><span data-stu-id="6e861-428">Build 17107</span></span>
<span data-ttu-id="6e861-429">빌드 17107에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-429">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-430">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-430">WSL</span></span>
* <span data-ttu-id="6e861-431">TCSETSF 및 TCSETSW on master 인 pty 끝점 [GH 2552]을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-431">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="6e861-432">동시 interop 프로세스를 시작 하면 EINVAL [GH 2813]이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-432">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="6e861-433">/Proc/pid/status.에서 적절 한 추적 상태를 표시 하도록 PTRACE_ATTACH 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-433">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="6e861-434">CLEARTID 및 SETTID 플래그 모두로 복제 된 단기 프로세스가 TID 주소를 지우지 않고 종료 되는 경합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-434">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="6e861-435">17093 이전 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드할 때 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-435">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="6e861-436">17093 파일 시스템 변경 내용에 대 한 자세한 내용은 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)의 릴리스 정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-436">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="6e861-437">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-437">Console</span></span>
* <span data-ttu-id="6e861-438">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-438">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-439">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-439">LTP Results:</span></span>
<span data-ttu-id="6e861-440">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-440">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="6e861-441">빌드 17101</span><span class="sxs-lookup"><span data-stu-id="6e861-441">Build 17101</span></span>
<span data-ttu-id="6e861-442">빌드 17101에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-442">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-443">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-443">WSL</span></span>
* <span data-ttu-id="6e861-444">Signalfd에 대 한 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-444">Support for signalfd.</span></span> <span data-ttu-id="6e861-445">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="6e861-445">[GH 129]</span></span>
* <span data-ttu-id="6e861-446">지원 되지 않는 NTFS 문자를 포함 하는 파일 이름을 개인 유니코드 문자로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-446">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="6e861-447">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="6e861-447">[GH 1514]</span></span>
* <span data-ttu-id="6e861-448">자동 탑재는 쓰기가 지원 되지 않는 경우 읽기 전용으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-448">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="6e861-449">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="6e861-449">[GH 2603]</span></span>
* <span data-ttu-id="6e861-450">유니코드 서로게이트 쌍 (예:이 모 지 문자)을 붙여 넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-450">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="6e861-451">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="6e861-451">[GH 2765]</span></span>
* <span data-ttu-id="6e861-452">/Sproc 및/tsys의 의사 (Pseudo) 파일은 select, 폴링합니다, epoll, et al에서 준비 된 읽기 및 쓰기를 반환 해야 합니다. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="6e861-452">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="6e861-453">레지스트리가 변조 되거나 손상 된 경우 서비스가 무한 루프로 전환 될 수 있는 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-453">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="6e861-454">Netlink 메시지를 수정 하 여 최신 (업스트림 4.14) 버전의 iproute2를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-454">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="6e861-455">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-455">Console</span></span>
* <span data-ttu-id="6e861-456">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-457">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-457">LTP Results:</span></span>
<span data-ttu-id="6e861-458">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-458">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="6e861-459">빌드 17093</span><span class="sxs-lookup"><span data-stu-id="6e861-459">Build 17093</span></span>
<span data-ttu-id="6e861-460">빌드 17093에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-460">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="6e861-461">중요:</span><span class="sxs-lookup"><span data-stu-id="6e861-461">Important:</span></span>
<span data-ttu-id="6e861-462">이 빌드로 업그레이드 한 후 처음으로 WSL을 시작할 때 Linux 파일 시스템 디렉터리를 업그레이드 하는 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-462">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="6e861-463">이 작업은 몇 분 정도 걸릴 수 있으므로 WSL이 느리게 시작 하는 것 처럼 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-463">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="6e861-464">저장소에서 설치한 각 배포에 대해 한 번만 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-464">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="6e861-465">DrvFs에서 대/소문자 구분 지원이 개선 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-465">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="6e861-466">이제 DrvFs는 디렉터리 단위 대/소문자 구분을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-466">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="6e861-467">이 플래그는 디렉터리에 대해 설정 하 여 해당 디렉터리의 모든 작업이 대/소문자만 다른 파일을 열 수 있도록 하는 대/소문자 구분으로 처리 되어야 함을 나타내는 새로운 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-467">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="6e861-468">DrvFs에는 디렉터리 별로 대/소문자 구분을 제어 하는 새로운 탑재 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-468">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="6e861-469">case = force: 모든 디렉터리는 대/소문자를 구분 합니다 (드라이브 루트 제외).</span><span class="sxs-lookup"><span data-stu-id="6e861-469">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="6e861-470">WSL로 만든 새 디렉터리는 대/소문자를 구분 하 여 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-470">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="6e861-471">이는 새 디렉터리의 대/소문자 구분을 표시 하는 것을 제외 하 고 레거시 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-471">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="6e861-472">case = dir: 디렉터리 단위 대/소문자 구분 플래그를 사용 하는 디렉터리만 대/소문자를 구분 합니다. 다른 디렉터리는 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-472">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="6e861-473">WSL로 만든 새 디렉터리는 대/소문자를 구분 하 여 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-473">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="6e861-474">case = off: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리 됩니다. 다른 디렉터리는 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-474">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="6e861-475">WSL로 만든 새 디렉터리는 대/소문자를 구분 하지 않는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-475">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="6e861-476">참고: 이전 릴리스의 WSL에서 만든 디렉터리는이 플래그를 설정 하지 않았으므로 "case = dir" 옵션을 사용 하는 경우 대/소문자를 구분 하는 것으로 간주 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-476">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="6e861-477">기존 디렉터리에이 플래그를 설정 하는 방법은 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-477">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="6e861-478">이러한 옵션을 사용 하 여 탑재 하는 예 (기존 드라이브의 경우 다른 옵션을 사용 하 여 탑재 하려면 먼저 분리 해야 함): sudo mount-t drvfs C:/mnt/c-o case = dir</span><span class="sxs-lookup"><span data-stu-id="6e861-478">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="6e861-479">지금은 case = force가 여전히 기본 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-479">For now, case=force is still the default option.</span></span> <span data-ttu-id="6e861-480">이는 나중에 case = dir로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-480">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="6e861-481">이제 DrvFs을 탑재할 때 Windows 경로에서 슬래시를 사용할 수 있습니다 (예: sudo mount-t DrvFs/server/share/mnt/share).</span><span class="sxs-lookup"><span data-stu-id="6e861-481">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="6e861-482">이제 WSL에서 인스턴스를 시작 하는 동안/etc/fstab 파일 [GH 2636]을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-482">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="6e861-483">DrvFs 드라이브를 자동으로 탑재 하기 전에 수행 됩니다. fstab에 의해 이미 탑재 된 모든 드라이브는 자동으로 탑재 되지 않으므로 특정 드라이브의 탑재 지점을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-483">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="6e861-484">이 동작은 wsl를 사용 하 여 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-484">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="6e861-485">/Proc의 mount, mountinfo 및 mountstats 파일은 백슬래시 및 공백과 같은 특수 문자를 적절히 이스케이프 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="6e861-485">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="6e861-486">DrvFs를 사용 하 여 만든 특수 파일 (예: WSL 기호화 된 링크, 메타 데이터를 사용 하는 경우 fifos 및 소켓)을 이제 Windows에서 복사 하 여 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-486">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="6e861-487">WSL은 wsl.</span><span class="sxs-lookup"><span data-stu-id="6e861-487">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="6e861-488">사용자가 하위 시스템을 시작할 때마다 적용 되는 WSL의 특정 기능을 자동으로 구성 하는 메서드를 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-488">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="6e861-489">여기에는 자동 탑재 옵션 및 네트워크 구성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-489">This includes automount options and network configuration.</span></span> <span data-ttu-id="6e861-490">이에 대 한 자세한 내용은 다음 블로그 게시물을 살펴보세요. https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="6e861-490">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="6e861-491">AF_UNIX를 사용 하면 WSL 및 Windows 네이티브 프로세스의 Linux 프로세스 간 소켓 연결을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-491">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="6e861-492">WSL 및 Windows 응용 프로그램은 이제 Unix 소켓을 통해 서로 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-492">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="6e861-493">Windows에서 서비스를 실행 하 고 Windows 및 WSL 앱 모두에서 서비스를 사용할 수 있게 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-493">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="6e861-494">이제는 Unix 소켓에서 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-494">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="6e861-495">블로그 게시물에서 자세한 내용을 알아보세요. https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="6e861-495">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-496">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-496">WSL</span></span>
* <span data-ttu-id="6e861-497">MAP_NORESERVE를 사용 하 여 mmap () 지원 [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="6e861-497">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="6e861-498">지원 CLONE_PTRACE 및 CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="6e861-498">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="6e861-499">복제에서 비 SIGCHLD 종료 신호 처리 [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="6e861-499">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="6e861-500">스텁/proc/sys/fs/inotify/max_user_instances 및/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="6e861-500">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="6e861-501">0이 아닌 오프셋을 포함 하는 로드 헤더가 포함 된 ELF 이진 파일을 로드 하는 동안 오류 발생 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="6e861-501">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="6e861-502">이미지를 로드할 때 후행 페이지 바이트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-502">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="6e861-503">Execve가 자동으로 프로세스를 종료 하는 사례 줄이기</span><span class="sxs-lookup"><span data-stu-id="6e861-503">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="6e861-504">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-504">Console</span></span>
* <span data-ttu-id="6e861-505">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-505">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-506">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-506">LTP Results:</span></span>
<span data-ttu-id="6e861-507">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-507">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="6e861-508">빌드 17083</span><span class="sxs-lookup"><span data-stu-id="6e861-508">Build 17083</span></span>
<span data-ttu-id="6e861-509">빌드 17083에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-509">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-510">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-510">WSL</span></span>
* <span data-ttu-id="6e861-511">Epoll [GH 2798, 2801, 2857]와 관련 된 버그를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-511">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="6e861-512">ASLR을 끄면 중단 문제가 해결 됨 [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="6e861-512">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="6e861-513">Mmap 작업이 원자성으로 표시 되는지 확인 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="6e861-513">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="6e861-514">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-514">Console</span></span>
* <span data-ttu-id="6e861-515">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-515">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-516">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-516">LTP Results:</span></span>
<span data-ttu-id="6e861-517">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-517">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="6e861-518">빌드 17074</span><span class="sxs-lookup"><span data-stu-id="6e861-518">Build 17074</span></span>
<span data-ttu-id="6e861-519">빌드 17074에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-519">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-520">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-520">WSL</span></span>
* <span data-ttu-id="6e861-521">DrvFs 메타 데이터의 고정 저장소 형식 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="6e861-521">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="6e861-522">**중요:** 이 빌드 전에 만든 DrvFs 메타 데이터는 잘못 표시 되거나 전혀 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-522">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="6e861-523">영향을 받는 파일을 수정 하려면 chmod 및 chown를 사용 하 여 메타 데이터를 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-523">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="6e861-524">여러 신호 및 다시 시작 가능한 syscall 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-524">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="6e861-525">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-525">Console</span></span>
* <span data-ttu-id="6e861-526">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-526">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-527">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-527">LTP Results:</span></span>
<span data-ttu-id="6e861-528">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-528">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="6e861-529">빌드 17063</span><span class="sxs-lookup"><span data-stu-id="6e861-529">Build 17063</span></span>
<span data-ttu-id="6e861-530">빌드 17063에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-530">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6e861-531">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-531">WSL</span></span>
* <span data-ttu-id="6e861-532">DrvFs는 추가 Linux 메타 데이터를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-532">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="6e861-533">이렇게 하면 chmod/chown를 사용 하 여 파일의 소유자와 모드를 설정할 수 있으며 fifos, unix 소켓 및 장치 파일과 같은 특수 파일을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-533">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="6e861-534">이는 아직 실험적 이기 때문에 지금은 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-534">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="6e861-535">**참고:**  DrvFs에서 사용 하는 메타 데이터 형식의 버그를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-535">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="6e861-536">메타 데이터는 실험을 위해이 빌드에서 작동 하지만 향후 빌드는이 빌드에서 생성 된 메타 데이터를 올바르게 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-536">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="6e861-537">수정 된 파일의 소유자를 수동으로 업데이트 하 고 사용자 지정 장치 ID를 사용 하는 장치를 다시 만들어야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-537">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="6e861-538">을 사용 하도록 설정 하려면 메타 데이터 옵션을 사용 하 여 DrvFs를 탑재 합니다 (기존 탑재에서 사용 하도록 설정 하려면 먼저 분리 해야 함).</span><span class="sxs-lookup"><span data-stu-id="6e861-538">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="6e861-539">Linux 권한은 파일에 추가 메타 데이터로 추가 됩니다. Windows 사용 권한에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-539">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="6e861-540">Windows 편집기를 사용 하 여 파일을 편집 하면 메타 데이터가 제거 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-540">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="6e861-541">이 경우 파일은 기본 권한으로 되돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-541">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="6e861-542">메타 데이터를 사용 하지 않고 파일을 제어 하는 탑재 옵션이 DrvFs에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-542">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="6e861-543">uid: 모든 파일의 소유자에 게 사용 되는 사용자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-543">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="6e861-544">gid: 모든 파일의 소유자에 사용 되는 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-544">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="6e861-545">umask: 모든 파일 및 디렉터리에 대해 제외할 8 진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-545">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="6e861-546">fmask: 모든 일반 파일에 대해 제외할 8 진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-546">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="6e861-547">6mask: 모든 디렉터리에 대해 제외할 8 진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-547">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="6e861-548">이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-548">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="6e861-549">메타 데이터 없이 파일에 대 한 기본 권한을 지정 하려면 메타 데이터 옵션과 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-549">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="6e861-550">는 새 환경 변수 `WSLENV`를 도입 하 여 환경 변수가 wsl과 Win32 사이에서 흐르는 방식을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-550">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="6e861-551">이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-551">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="6e861-552">`WSLENV`는 WSL의 Win32 또는 Win32 프로세스에서 WSL 프로세스를 시작할 때 포함할 수 있는 환경 변수의 콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-552">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="6e861-553">각 변수에는 슬래시 뒤에 플래그를 사용 하 여 변환 방법을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-553">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="6e861-554">® 값은 WSL 경로와 Win32 경로 간에 변환 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-554">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="6e861-555">l-value 값은 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-555">l: The value is a list of paths.</span></span> <span data-ttu-id="6e861-556">WSL에서는 콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-556">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="6e861-557">Win32에서 세미콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-557">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="6e861-558">나무 Win32에서 WSL을 호출할 때에만 값이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-558">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="6e861-559">w WSL에서 Win32를 호출할 때에만 값이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-559">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="6e861-560">사용자를 위해 `WSLENV` .bashrc 또는 사용자 지정 Windows 환경에서를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-560">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="6e861-561">drvfs 탑재는 tar, cp-p의 타임 스탬프를 올바르게 유지 합니다 (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="6e861-561">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="6e861-562">drvfs symlink 올바른 크기를 보고 합니다 (GH 2641).</span><span class="sxs-lookup"><span data-stu-id="6e861-562">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="6e861-563">매우 큰 IO 크기에 대 한 읽기/쓰기 작동 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="6e861-563">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="6e861-564">waitpid는 프로세스 그룹 Id와 함께 작동 합니다 (GH 2534).</span><span class="sxs-lookup"><span data-stu-id="6e861-564">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="6e861-565">큰 예약 영역에 대 한 mmap 성능이 크게 향상 되었습니다. GH c 성능 향상 (1671)</span><span class="sxs-lookup"><span data-stu-id="6e861-565">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="6e861-566">READ_IMPLIES_EXEC에 대 한 개성 지원 최대 및 clisp 수정 (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="6e861-566">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="6e861-567">mprotect는 PROT_GROWSDOWN을 지원 합니다. clisp 수정 (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="6e861-567">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="6e861-568">과도 한 커밋 모드의 페이지 폴트 수정 sbcl (GH 1128)을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-568">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="6e861-569">클론은 더 많은 플래그 조합을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-569">clone supports more flags combinations</span></span>
* <span data-ttu-id="6e861-570">Epoll 파일의 select/epoll (이전에는 작동 하지 않음)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-570">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="6e861-571">구현 되지 않은 syscall에 대 한 ptrace를 알립니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-571">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="6e861-572">Resolv.conf 이름 서버를 생성할 때 작동 하지 않는 인터페이스 무시 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="6e861-572">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="6e861-573">실제 주소가 없는 네트워크 인터페이스를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-573">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="6e861-574">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="6e861-574">[GH 2685]</span></span>
* <span data-ttu-id="6e861-575">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-575">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="6e861-576">Windows의 개발자가 사용할 수 있는 Linux 도구</span><span class="sxs-lookup"><span data-stu-id="6e861-576">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="6e861-577">Windows 명령줄 도구 체인는 bsdtar (tar) 및 말아를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-577">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="6e861-578">[이 블로그](https://aka.ms/tarcurlwindows) 를 읽고 이러한 두 가지 도구를 추가 하는 방법에 대해 자세히 알아보고 Windows에서 개발자 환경에 어떻게 셰이핑 하는지 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-578">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="6e861-579">`AF_UNIX`는 Windows 참가자 SDK (17061 +)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-579">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="6e861-580">[이 블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) 를 읽고 Windows의 개발자 `AF_UNIX` 가 사용할 수 있는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-580">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="6e861-581">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-581">Console</span></span>
* <span data-ttu-id="6e861-582">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-582">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-583">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-583">LTP Results:</span></span>
<span data-ttu-id="6e861-584">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-584">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="6e861-585">빌드 17046</span><span class="sxs-lookup"><span data-stu-id="6e861-585">Build 17046</span></span>

<span data-ttu-id="6e861-586">빌드 17046에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-586">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-587">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-587">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-588">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-588">WSL</span></span>
- <span data-ttu-id="6e861-589">활성 터미널 없이 프로세스를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-589">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="6e861-590">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="6e861-590">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="6e861-591">CLONE_VFORK 및 CLONE_VM에 대 한 지원이 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-591">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="6e861-592">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="6e861-592">[GH 1878, 2615]</span></span>
- <span data-ttu-id="6e861-593">WSL 네트워킹 작업을 위한 TDI 필터 드라이버를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-593">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="6e861-594">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="6e861-594">[GH 1554]</span></span>
- <span data-ttu-id="6e861-595">특정 조건이 충족 되 면 DrvFs에서 NT symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-595">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="6e861-596">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="6e861-596">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="6e861-597">링크 대상은 상대 경로 여야 하 고, 탑재 지점이 나 symlink를 교차 해서는 안 되며, 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-597">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="6e861-598">개발자 모드가 설정 되어 있지 않으면 사용자에 게 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (일반적으로 wsl .exe를 실행 해야 함)가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-598">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="6e861-599">다른 모든 상황에서 DrvFs는 여전히 WSL symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-599">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="6e861-600">상승 된 권한 및 비관리자 WSL 인스턴스를 동시에 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-600">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="6e861-601">/Proc/sys/kernel/yama/ptrace_scope 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-601">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="6e861-602">Wslpath를 추가 하 여 WSL <-> Windows 경로 변환을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-602">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="6e861-603">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="6e861-603">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="6e861-604">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-604">Console</span></span>
- <span data-ttu-id="6e861-605">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-605">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-606">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-606">LTP Results:</span></span>
<span data-ttu-id="6e861-607">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-607">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="6e861-608">빌드 17040</span><span class="sxs-lookup"><span data-stu-id="6e861-608">Build 17040</span></span>

<span data-ttu-id="6e861-609">빌드 17040에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-609">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-610">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-610">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-611">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-611">WSL</span></span>
- <span data-ttu-id="6e861-612">17035 이후의 수정 사항은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-612">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-613">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-613">Console</span></span>
- <span data-ttu-id="6e861-614">17035 이후의 수정 사항은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-614">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-615">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-615">LTP Results:</span></span>
<span data-ttu-id="6e861-616">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-616">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="6e861-617">빌드 17035</span><span class="sxs-lookup"><span data-stu-id="6e861-617">Build 17035</span></span>

<span data-ttu-id="6e861-618">빌드 17035에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-618">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-619">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-619">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-620">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-620">WSL</span></span>
- <span data-ttu-id="6e861-621">DrvFs의 파일에 액세스 하는 경우 EINVAL와 함께 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-621">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="6e861-622">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="6e861-622">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-623">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-623">Console</span></span>
- <span data-ttu-id="6e861-624">VT 모드에서 줄을 삽입/삭제할 때 일부 색이 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-624">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-625">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-625">LTP Results:</span></span>
<span data-ttu-id="6e861-626">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-626">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="6e861-627">빌드 17025</span><span class="sxs-lookup"><span data-stu-id="6e861-627">Build 17025</span></span>

<span data-ttu-id="6e861-628">빌드 17025에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-628">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-629">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-629">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-630">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-630">WSL</span></span>
- <span data-ttu-id="6e861-631">새 포그라운드 프로세스 그룹 [GH 1653, 2510]에서 초기 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-631">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="6e861-632">SIDELIVERY UP 배달 수정 [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="6e861-632">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="6e861-633">제공 된 [GH 2497]이 없으면 기본 가상 브리지 이름을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-633">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="6e861-634">/Proc/sys/kernel/random/boot_id [GH 2518]을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-634">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="6e861-635">더 많은 interop stdout/stderr 파이프 수정.</span><span class="sxs-lookup"><span data-stu-id="6e861-635">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="6e861-636">스텁 syncfs 시스템 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-636">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-637">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-637">Console</span></span>
- <span data-ttu-id="6e861-638">타사 콘솔에 대 한 입력 VT 번역 수정 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="6e861-638">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-639">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-639">LTP Results:</span></span>
<span data-ttu-id="6e861-640">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-640">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="6e861-641">빌드 17017</span><span class="sxs-lookup"><span data-stu-id="6e861-641">Build 17017</span></span>

<span data-ttu-id="6e861-642">빌드 17017에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-642">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-643">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-643">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-644">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-644">WSL</span></span>
- <span data-ttu-id="6e861-645">빈 ELF program headers [GH 330]을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-645">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="6e861-646">LxssManager가 비 대화형 사용자 (ssh 및 예약 된 작업 지원) [GH 777, 1602]에 대해 WSL 인스턴스를 만들도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-646">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="6e861-647">WSL-> Win32 > WSL ("개시") 시나리오 [GH 1228]을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-647">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="6e861-648">Interop [GH 1614]를 통해 호출 되는 콘솔 앱의 종료에 대 한 제한 된 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-648">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="6e861-649">Devpts [GH 1948]에 대 한 탑재 옵션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-649">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="6e861-650">Ptrace 차단 자식 시작 [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="6e861-650">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="6e861-651">EPOLLET에 일부 이벤트가 없습니다 [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="6e861-651">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="6e861-652">PTRACE_GETSIGINFO에 대 한 추가 데이터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-652">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="6e861-653">Lseek를 사용한 Getdents는 잘못 된 결과를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-653">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="6e861-654">일부 Win32 interop 앱이 중단 되 고, 더 이상 데이터가 없는 파이프의 입력을 기다리는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-654">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="6e861-655">Tty/인 pty 파일에 대 한 O_ASYNC 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-655">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="6e861-656">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-656">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-657">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-657">Console</span></span>
- <span data-ttu-id="6e861-658">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-658">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-659">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-659">LTP Results:</span></span>
<span data-ttu-id="6e861-660">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-660">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="6e861-661">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="6e861-661">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="6e861-662">빌드 16288</span><span class="sxs-lookup"><span data-stu-id="6e861-662">Build 16288</span></span>

<span data-ttu-id="6e861-663">빌드 16288에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-663">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-664">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-665">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-665">WSL</span></span>
- <span data-ttu-id="6e861-666">소켓 파일 설명자에 대해 uid, gid 및 모드를 올바르게 초기화 및 보고 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="6e861-666">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="6e861-667">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-667">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-668">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-668">Console</span></span>
- <span data-ttu-id="6e861-669">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-669">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-670">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-670">LTP Results:</span></span>
<span data-ttu-id="6e861-671">16273 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-671">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="6e861-672">빌드 16278</span><span class="sxs-lookup"><span data-stu-id="6e861-672">Build 16278</span></span>

<span data-ttu-id="6e861-673">빌드 162738에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-673">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-674">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-674">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-675">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-675">WSL</span></span>
- <span data-ttu-id="6e861-676">LX MM 상태를 해제할 때 파일 지원 섹션의 매핑된 뷰를 명시적으로 매핑 해제 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="6e861-676">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="6e861-677">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-677">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-678">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-678">Console</span></span>
- <span data-ttu-id="6e861-679">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-679">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-680">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-680">LTP Results:</span></span>
<span data-ttu-id="6e861-681">16273 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-681">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="6e861-682">빌드 16275</span><span class="sxs-lookup"><span data-stu-id="6e861-682">Build 16275</span></span>

<span data-ttu-id="6e861-683">빌드 162735에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-683">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-684">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-684">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-685">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-685">WSL</span></span>
- <span data-ttu-id="6e861-686">이 릴리스에서는 WSL 관련 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-686">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-687">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-687">Console</span></span>
- <span data-ttu-id="6e861-688">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-688">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-689">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-689">LTP Results:</span></span>
<span data-ttu-id="6e861-690">16273 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-690">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="6e861-691">빌드 16273</span><span class="sxs-lookup"><span data-stu-id="6e861-691">Build 16273</span></span>

<span data-ttu-id="6e861-692">빌드 16273에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-692">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-693">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-694">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-694">WSL</span></span>
- <span data-ttu-id="6e861-695">DrvFs에서 디렉터리에 대해 잘못 된 파일 형식을 보고 하는 문제 해결 [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="6e861-695">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="6e861-696">Uevent를 사용 하는 프로그램의 차단을 해제 하는 NETLINK_KOBJECT_UEVENT 소켓 만들기 허용 [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="6e861-696">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="6e861-697">비차단 연결에 대 한 지원 추가 [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="6e861-697">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="6e861-698">CLONE_FS CLONE 시스템 호출 플래그 구현 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="6e861-698">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="6e861-699">NT interop에서 탭 또는 따옴표를 올바르게 처리 하지 않는 문제 해결 [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="6e861-699">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="6e861-700">WSL 인스턴스를 다시 시작 하려고 할 때 액세스 거부 오류 해결 [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="6e861-700">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="6e861-701">Futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업 구현 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="6e861-701">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="6e861-702">여러 SysFs 파일에 대 한 사용 권한 수정 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="6e861-702">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="6e861-703">설치 하는 동안 Haskell stack 중단 수정 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="6e861-703">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="6e861-704">Binfmt_misc ' C ' ' O ' 및 ' P ' 플래그 구현 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="6e861-704">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="6e861-705">Add/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="6e861-705">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="6e861-706">Ioprio_set 시스템 호출에 대 한 부분 지원 추가 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="6e861-706">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="6e861-707">스텁 SO_REUSEPORT & netlink 소켓 SO_PASSCRED에 대 한 지원을 추가 하는 중 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="6e861-707">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="6e861-708">배포를 현재 설치 하거나 제거 하는 경우 RegisterDistribuiton의 다른 오류 코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-708">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="6e861-709">Wslconfig .exe를 통해 부분적으로 설치 된 WSL 배포의 등록 취소 허용</span><span class="sxs-lookup"><span data-stu-id="6e861-709">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="6e861-710">Udp:: msg_peek에서 python 소켓 테스트 중단 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-710">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="6e861-711">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-712">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-712">Console</span></span>
- <span data-ttu-id="6e861-713">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-714">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-714">LTP Results:</span></span>
<span data-ttu-id="6e861-715">총 테스트: 1904</span><span class="sxs-lookup"><span data-stu-id="6e861-715">Total Tests: 1904</span></span><br/>
<span data-ttu-id="6e861-716">건너뛴 총 테스트: 209</span><span class="sxs-lookup"><span data-stu-id="6e861-716">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="6e861-717">총 실패 횟수: 229</span><span class="sxs-lookup"><span data-stu-id="6e861-717">Total Failures: 229</span></span><br/>
[<span data-ttu-id="6e861-718">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-718">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="6e861-719">빌드 16257</span><span class="sxs-lookup"><span data-stu-id="6e861-719">Build 16257</span></span>

<span data-ttu-id="6e861-720">빌드 16257에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-720">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-721">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-721">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-722">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-722">WSL</span></span>
- <span data-ttu-id="6e861-723">Prlimit64 시스템 호출 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-723">Implement prlimit64 system call</span></span>
- <span data-ttu-id="6e861-724">Ulimit에 대 한 지원 추가 (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="6e861-724">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="6e861-725">TCP 소켓용 스텁 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="6e861-725">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="6e861-726">잘못 된 AT_EXECFN 보조 벡터 동작 수정 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="6e861-726">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="6e861-727">콘솔/tty의 복사/붙여넣기 동작을 수정 하 고 더 나은 전체 버퍼 처리를 추가 합니다 [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="6e861-727">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="6e861-728">AT_SECURE 및 GH 프로그램에 대 한 보조 vector에서 set [2031]</span><span class="sxs-lookup"><span data-stu-id="6e861-728">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="6e861-729">유사-터미널 마스터 끝점이 TIOCPGRP를 처리 하지 않습니다 [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="6e861-729">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="6e861-730">Fix lseek에서 LxFs의 디렉터리 되감기 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="6e861-730">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="6e861-731">사용량이 많은 후에/cv/ptmx 잠금 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="6e861-731">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="6e861-732">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-732">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-733">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-733">Console</span></span>
- <span data-ttu-id="6e861-734">모든 곳에서 가로 선/밑줄 수정 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="6e861-734">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="6e861-735">NPM을 닫기 위해 프로세스 순서 변경 수정 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="6e861-735">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="6e861-736">새 색 구성표를 추가 했습니다. https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="6e861-736">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-737">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-737">LTP Results:</span></span>
<span data-ttu-id="6e861-738">16251 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-738">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-739">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-739">Syscall Support</span></span>
<span data-ttu-id="6e861-740">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-740">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-741">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-741">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="6e861-742">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-742">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="6e861-743">GitHub 문제 2392: WSL에서 인식할 수 없는 Windows 폴더 ...</span><span class="sxs-lookup"><span data-stu-id="6e861-743">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="6e861-744">빌드 16257에서 WSL에는를 통해 `/mnt/c/...`Windows 파일/폴더를 열거 하는 동안 문제가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-744">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="6e861-745">이 문제는 해결 되었으며, 8/14/2017를 시작 하는 동안에는 참가자 빌드에서 릴리스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-745">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="6e861-746">빌드 16251</span><span class="sxs-lookup"><span data-stu-id="6e861-746">Build 16251</span></span>

<span data-ttu-id="6e861-747">빌드 16251에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-747">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-748">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-748">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-749">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-749">WSL</span></span>
- <span data-ttu-id="6e861-750">WSL 선택적 구성 요소에서 베타 태그 제거에 대 한 자세한 내용은 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-750">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="6e861-751">Exec [GH 962, 1415, 2072]에서 집합-사용자 ID 및 집합 그룹 ID 바이너리에 대해 저장 된 설정 uid 및 gid를 올바르게 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-751">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="6e861-752">Ptrace PTRACE_O_TRACEEXIT에 대 한 지원 추가 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="6e861-752">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="6e861-753">NT_FPREGSET에서 ptrace PTRACE_GETFPREGS 및 PTRACE_GETREGSET에 대 한 지원이 추가 됨 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="6e861-753">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="6e861-754">무시 된 신호를 중지 하도록 ptrace 고정</span><span class="sxs-lookup"><span data-stu-id="6e861-754">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="6e861-755">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-756">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-756">Console</span></span>
- <span data-ttu-id="6e861-757">이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-758">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-758">LTP Results:</span></span>
<span data-ttu-id="6e861-759">통과 한 테스트 수: 768</span><span class="sxs-lookup"><span data-stu-id="6e861-759">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="6e861-760">실패 한 테스트 수: 244</span><span class="sxs-lookup"><span data-stu-id="6e861-760">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="6e861-761">건너뛴 테스트 수: 96</span><span class="sxs-lookup"><span data-stu-id="6e861-761">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="6e861-762">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="6e861-763">빌드 16241</span><span class="sxs-lookup"><span data-stu-id="6e861-763">Build 16241</span></span>

<span data-ttu-id="6e861-764">빌드 16241에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-764">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-765">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6e861-766">WSL</span><span class="sxs-lookup"><span data-stu-id="6e861-766">WSL</span></span>
- <span data-ttu-id="6e861-767">이 릴리스에서는 WSL 관련 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-767">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="6e861-768">콘솔</span><span class="sxs-lookup"><span data-stu-id="6e861-768">Console</span></span>
- <span data-ttu-id="6e861-769">원래 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) 에 보고 된 교차 선 DEC에 대해 잘못 된 문자를 출력 하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-769">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="6e861-770">코드 페이지 65001 (utf8)에 표시 되는 출력 텍스트를 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-770">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="6e861-771">한 색의 RGB 값에 적용 한 변경 내용을 선택 변경 시 색상표의 다른 부분으로 전송 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-771">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="6e861-772">이렇게 하면 콘솔 속성 시트를 훨씬 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-772">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="6e861-773">Ctrl + S가 제대로 작동 하지 않는 것 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-773">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="6e861-774">ANSI 이스케이프 코드에서 굵게 표시 되지 않은/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="6e861-774">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="6e861-775">콘솔이 Vim color 테마를 올바르게 지원 하지 않음 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="6e861-775">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="6e861-776">특정 문자를 붙여 넣을 수 없습니다 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="6e861-776">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="6e861-777">편집/명령줄에 있는 경우 bash 창의 크기를 조정 하 여 리플로우 크기를 조정할 수 있습니다. [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="6e861-777">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="6e861-778">Ctrl + L에서 화면을 더티 상태로 둡니다 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="6e861-778">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="6e861-779">HDPI에서 VT를 표시할 때 콘솔 렌더링 버그 [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="6e861-779">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="6e861-780">Japansese 문자는 유니코드 문자 U + 30FB [GH 2146]와 이상한 모양으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-780">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="6e861-781">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-781">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="6e861-782">빌드 16237</span><span class="sxs-lookup"><span data-stu-id="6e861-782">Build 16237</span></span>

<span data-ttu-id="6e861-783">빌드 16237에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-783">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-784">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-784">Fixed</span></span>
- <span data-ttu-id="6e861-785">Lxfs (root, root, 0000)에서 EAs가 없는 파일에 대 한 기본 특성 사용</span><span class="sxs-lookup"><span data-stu-id="6e861-785">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="6e861-786">확장 된 특성을 사용 하는 배포에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-786">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="6e861-787">Getdents 및 getdents64에서 반환 된 항목의 패딩 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-787">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="6e861-788">Shmctl SHM_STAT 시스템 호출에 대 한 권한 확인 수정 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="6e861-788">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="6e861-789">Tty에 대 한 잘못 된 초기 epoll 상태 수정 됨 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="6e861-789">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="6e861-790">모든 항목을 반환 하지 않는 DrvFs readdir 수정 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="6e861-790">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="6e861-791">파일의 연결을 끊을 때 LxFs readdir 수정 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="6e861-791">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="6e861-792">연결 되지 않은 drvfs 파일을 procfs를 통해 다시 열 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="6e861-792">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="6e861-793">WSL 기능을 사용 하지 않도록 설정 하기 위한 전역 레지스트리 키 재정의 추가 (상호 운용성/드라이브 탑재)</span><span class="sxs-lookup"><span data-stu-id="6e861-793">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="6e861-794">DrvFs (및 LxFs)에 대해 "stat"의 잘못 된 블록 수 수정 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="6e861-794">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="6e861-795">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-795">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="6e861-796">빌드 16232</span><span class="sxs-lookup"><span data-stu-id="6e861-796">Build 16232</span></span>

<span data-ttu-id="6e861-797">빌드 16232에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-797">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-798">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-798">Fixed</span></span>
- <span data-ttu-id="6e861-799">이 릴리스에서는 WSL 관련 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-799">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="6e861-800">빌드 16226</span><span class="sxs-lookup"><span data-stu-id="6e861-800">Build 16226</span></span>

<span data-ttu-id="6e861-801">빌드 16226에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-801">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-802">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-802">Fixed</span></span>
- <span data-ttu-id="6e861-803">xattr 관련 syscall 지원 (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="6e861-803">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="6e861-804">capablity xattr 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-804">security.capablity xattr support.</span></span>
- <span data-ttu-id="6e861-805">비-MS SMB 서버를 비롯 한 특정 파일 시스템 및 필터와의 호환성이 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-805">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="6e861-806">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="6e861-806">[GH #1952]</span></span>
- <span data-ttu-id="6e861-807">OneDrive 자리 표시자, GVFS 자리 표시자 및 압축 OS 압축 파일에 대 한 지원이 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-807">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="6e861-808">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-808">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="6e861-809">빌드 16215</span><span class="sxs-lookup"><span data-stu-id="6e861-809">Build 16215</span></span>

<span data-ttu-id="6e861-810">빌드 16215에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-810">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-811">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-811">Fixed</span></span>
- <span data-ttu-id="6e861-812">WSL에서 더 이상 개발자 모드를 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-812">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="6e861-813">Drvfs에서 디렉터리 연결점을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-813">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="6e861-814">WSL 배포 appx 패키지의 제거를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-814">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="6e861-815">개인 및 공유 매핑을 표시 하도록 procfs를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-815">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="6e861-816">구성에서 부분적으로 설치 또는 제거 되는 배포를 정리 하는 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-816">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="6e861-817">TCP 소켓에 대해 IP_MTU_DISCOVER에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-817">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="6e861-818">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="6e861-818">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="6e861-819">AF_INADDR에 대 한 경로에 대 한 프로토콜 패밀리를 유추 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-819">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="6e861-820">직렬 장치 개선 [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="6e861-820">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="6e861-821">빌드 16199</span><span class="sxs-lookup"><span data-stu-id="6e861-821">Build 16199</span></span>

<span data-ttu-id="6e861-822">빌드 16199에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-822">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-823">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-823">Fixed</span></span>
- <span data-ttu-id="6e861-824">이러한 릴리스에서는 WSL 관련 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-824">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="6e861-825">빌드 16193</span><span class="sxs-lookup"><span data-stu-id="6e861-825">Build 16193</span></span>

<span data-ttu-id="6e861-826">빌드 16193에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-826">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-827">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-827">Fixed</span></span>
- <span data-ttu-id="6e861-828">SIGCONT 및 threadgroup을 종료 하는 경합 상태 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="6e861-828">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="6e861-829">FILE_DEVICE_CONSOLE 대신 tty 및 인 pty 장치를 report FILE_DEVICE_NAMED_PIPE로 변경 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="6e861-829">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="6e861-830">IP_OPTIONS에 대 한 SSH 픽스</span><span class="sxs-lookup"><span data-stu-id="6e861-830">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="6e861-831">Init daemon로 이동 DrvFs 탑재 [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="6e861-831">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="6e861-832">DrvFs에서 다음 NT symlink에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-832">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="6e861-833">빌드 16184</span><span class="sxs-lookup"><span data-stu-id="6e861-833">Build 16184</span></span>

<span data-ttu-id="6e861-834">빌드 16184에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-834">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-835">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-835">Fixed</span></span>
- <span data-ttu-id="6e861-836">Apt 패키지 유지 관리 작업 제거 (lxrun/update)</span><span class="sxs-lookup"><span data-stu-id="6e861-836">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="6e861-837">Node.js의 Windows 프로세스에서 표시 되지 않는 고정 출력 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="6e861-837">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="6e861-838">Lxcore의 완화 맞춤 요구 사항 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="6e861-838">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="6e861-839">숫자로 시스템 호출에서 AT_EMPTY_PATH 플래그의 처리 문제를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-839">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="6e861-840">열린 핸들로 DrvFs 파일을 삭제 하면 파일이 정의 되지 않은 동작 [GH 544, 966, 1357, 1535, 1615]을 나타내도록 하는 문제가 해결 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-840">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="6e861-841">이제/etc/hosts가 Windows 호스트 파일 (%windir%\system32\drivers\etc\hosts)에서 항목을 상속 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="6e861-841">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="6e861-842">빌드 16179</span><span class="sxs-lookup"><span data-stu-id="6e861-842">Build 16179</span></span>

<span data-ttu-id="6e861-843">빌드 16179에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-843">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-844">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-844">Fixed</span></span>
- <span data-ttu-id="6e861-845">이번 주에는 WSL이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-845">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="6e861-846">빌드 16176</span><span class="sxs-lookup"><span data-stu-id="6e861-846">Build 16176</span></span>

<span data-ttu-id="6e861-847">빌드 16176에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-847">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-848">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-848">Fixed</span></span>

- [<span data-ttu-id="6e861-849">직렬 지원 사용</span><span class="sxs-lookup"><span data-stu-id="6e861-849">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="6e861-850">추가 된 IP 소켓 옵션 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="6e861-850">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="6e861-851">Pwritev 함수 구현 (파일을 nginx/PHP로 업로드 하는 동안) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="6e861-851">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="6e861-852">추가 된 IP 소켓 옵션 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="6e861-852">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="6e861-853">IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP 소켓 옵션에 대 한 지원 [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="6e861-853">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="6e861-854">앱 노드에 대 한 IP (V6) _MTU 소켓 옵션 추가 됨, 경로 추적, 방법, nslookup, 호스트</span><span class="sxs-lookup"><span data-stu-id="6e861-854">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="6e861-855">추가 된 IP 소켓 옵션 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="6e861-855">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="6e861-856">파일 시스템 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-856">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="6e861-857">UNC 경로 탑재 허용</span><span class="sxs-lookup"><span data-stu-id="6e861-857">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="6e861-858">Drvfs에서 CDFS 지원 사용</span><span class="sxs-lookup"><span data-stu-id="6e861-858">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="6e861-859">Drvfs의 네트워크 파일 시스템에 대 한 사용 권한을 올바르게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-859">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="6e861-860">Drvfs에 원격 드라이브에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-860">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="6e861-861">Drvfs에서 FAT 지원 사용</span><span class="sxs-lookup"><span data-stu-id="6e861-861">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="6e861-862">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-862">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-863">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="6e861-863">LTP Results</span></span>
<span data-ttu-id="6e861-864">15042 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-864">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="6e861-865">빌드 16170</span><span class="sxs-lookup"><span data-stu-id="6e861-865">Build 16170</span></span>

<span data-ttu-id="6e861-866">빌드 16170에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-866">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="6e861-867">WSL 테스트를 위한 새로운 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) 을 발표 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-867">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-868">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-868">Fixed</span></span>

- <span data-ttu-id="6e861-869">지원 소켓 옵션 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="6e861-869">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="6e861-870">PTRACE_OLDSETOPTIONS에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-870">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="6e861-871">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="6e861-871">[GH 1692]</span></span>
- <span data-ttu-id="6e861-872">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-872">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-873">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="6e861-873">LTP Results</span></span>
<span data-ttu-id="6e861-874">15042 이후 변경 내용 없음</span><span class="sxs-lookup"><span data-stu-id="6e861-874">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="6e861-875">Windows 10 크리에이터 스 업데이트에 15046 빌드</span><span class="sxs-lookup"><span data-stu-id="6e861-875">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="6e861-876">Windows 10에 대 한 작성자 업데이트에 포함 하기 위해 계획 된 WSL 수정 사항이 나 기능이 더 이상 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-876">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="6e861-877">WSL의 릴리스 정보는 다음 주 Windows 업데이트을 대상으로 하는 추가를 위해 향후 몇 주 이내에 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-877">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="6e861-878">빌드 15046 및 향후 Insider 릴리스에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-878">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="6e861-879">빌드 15042</span><span class="sxs-lookup"><span data-stu-id="6e861-879">Build 15042</span></span>

<span data-ttu-id="6e861-880">빌드 15042에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-880">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-881">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-881">Fixed</span></span>

- <span data-ttu-id="6e861-882">"..."로 끝나는 경로를 제거할 때 교착 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-882">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="6e861-883">성공 시 FIONBIO에서 0을 반환 하지 않는 문제 해결 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="6e861-883">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="6e861-884">Inet 데이터 그램 소켓의 길이가 0 인 읽기와 관련 된 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-884">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="6e861-885">Drvfs inode lookup의 경합 상태 때문에 가능한 교착 상태 수정 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="6e861-885">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="6e861-886">Unix 소켓 보조 데이터에 대 한 확장 된 지원 SCM_CREDENTIALS 및 SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="6e861-886">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="6e861-887">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-887">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-888">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-888">LTP Results:</span></span>
<span data-ttu-id="6e861-889">통과 한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="6e861-889">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="6e861-890">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255</span><span class="sxs-lookup"><span data-stu-id="6e861-890">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="6e861-891">빌드 15031</span><span class="sxs-lookup"><span data-stu-id="6e861-891">Build 15031</span></span>

<span data-ttu-id="6e861-892">빌드 15031에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-892">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-893">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-893">Fixed</span></span>

- <span data-ttu-id="6e861-894">시간 (2)이 산발적으로 동작 하는 버그를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-894">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="6e861-895">\* SIGPROCMASK syscall에서 신호 마스크를 손상 시킬 수 있는 문제를 해결 하 고 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-895">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="6e861-896">이제 WSL 프로세스 만들기 알림에서 전체 명령줄 길이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-896">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="6e861-897">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="6e861-897">[GH 1632]</span></span>
- <span data-ttu-id="6e861-898">이제 WSL은 GDB 정지에 대해 ptrace를 통해 스레드 종료를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-898">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="6e861-899">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="6e861-899">[GH 1196]</span></span>
- <span data-ttu-id="6e861-900">많은 tmux IO 후에 ptys 중단 하는 버그를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-900">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="6e861-901">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="6e861-901">[GH 1358]</span></span>
- <span data-ttu-id="6e861-902">많은 시스템 호출 (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)에서 시간 제한 확인이 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-902">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="6e861-903">추가 된 eventfd EFD_SEMAPHORE 지원 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="6e861-903">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="6e861-904">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-904">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-905">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-905">LTP Results:</span></span>
<span data-ttu-id="6e861-906">통과 한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="6e861-906">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="6e861-907">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255</span><span class="sxs-lookup"><span data-stu-id="6e861-907">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6e861-908">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-908">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="6e861-909">빌드 15025</span><span class="sxs-lookup"><span data-stu-id="6e861-909">Build 15025</span></span>

<span data-ttu-id="6e861-910">빌드 15025에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-910">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-911">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-911">Fixed</span></span>

- <span data-ttu-id="6e861-912">Grep 2.27을 중단 한 버그 수정 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="6e861-912">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="6e861-913">Eventfd2 syscall에 대해 구현 된 EFD_SEMAPHORE 플래그 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="6e861-913">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="6e861-914">구현 됨/proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="6e861-914">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="6e861-915">Unix 스트림 소켓에 대 한 신호 구동 IO 지원 [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="6e861-915">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="6e861-916">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="6e861-916">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="6e861-917">Syscall () 구현 구현 [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="6e861-917">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="6e861-918">Epoll_wait ()가 대기 하지 않는 버그 수정 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="6e861-918">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="6e861-919">/Proc\version_siu 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-919">Implement /proc/version_signature</span></span>
- <span data-ttu-id="6e861-920">이제 두 파일 설명자가 같은 파이프를 참조 하는 경우 티 syscall에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-920">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="6e861-921">SO_PEERCRED for Unix 소켓의 올바른 동작을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-921">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="6e861-922">Tkill syscall 잘못 된 매개 변수 처리를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-922">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="6e861-923">Drvfs의 preformace를 늘리기 위한 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6e861-923">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="6e861-924">Ruby IO 차단에 대 한 사소한 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-924">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="6e861-925">Inet 소켓에 대 한 MSG_DONTWAIT 플래그의 EINVAL을 반환 하는 Fixed recvmsg () [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="6e861-925">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="6e861-926">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-926">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-927">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-927">LTP Results:</span></span>
<span data-ttu-id="6e861-928">통과 한 테스트 수: 732</span><span class="sxs-lookup"><span data-stu-id="6e861-928">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="6e861-929">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255</span><span class="sxs-lookup"><span data-stu-id="6e861-929">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6e861-930">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-930">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="6e861-931">빌드 15019</span><span class="sxs-lookup"><span data-stu-id="6e861-931">Build 15019</span></span>

<span data-ttu-id="6e861-932">빌드 15019에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-932">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-933">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-933">Fixed</span></span>

- <span data-ttu-id="6e861-934">Htop (GH 823, 945, 971)와 같은 도구에 대해 procfs에서 CPU 사용량을 잘못 보고 하는 버그가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-934">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="6e861-935">기존 파일에 대해 O_TRUNC를 사용 하 여 open ()을 호출 하면 inotify 앞에 IN_MODIFY가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-935">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="6e861-936">Postgress를 사용 하도록 설정 하는 unix socket getsockopt SO_ERROR에 대 한 수정 [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="6e861-936">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="6e861-937">GO 언어에 대해/proc/sys/net/core/somaxconn 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-937">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="6e861-938">Apt-패키지 업데이트 배경 가져오기 작업이 이제 뷰에서 숨겨진 상태로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-938">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="6e861-939">Ipv6 localhost (스프링 프레임 워크 (Java) 실패)의 범위를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-939">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="6e861-940">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-940">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-941">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-941">LTP Results:</span></span>
<span data-ttu-id="6e861-942">통과 한 테스트 수: 714</span><span class="sxs-lookup"><span data-stu-id="6e861-942">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="6e861-943">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 249</span><span class="sxs-lookup"><span data-stu-id="6e861-943">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="6e861-944">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-944">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="6e861-945">빌드 15014</span><span class="sxs-lookup"><span data-stu-id="6e861-945">Build 15014</span></span>

<span data-ttu-id="6e861-946">빌드 15014에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-946">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-947">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-947">Fixed</span></span>

- <span data-ttu-id="6e861-948">이제 Ctrl + C는 의도 한 대로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-948">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="6e861-949">이제 htop 및 ps auxw에 올바른 리소스 사용률 (GH #516)이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-949">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="6e861-950">신호로 NT 예외를 기본으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-950">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="6e861-951">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="6e861-951">(GH #513)</span></span>
- <span data-ttu-id="6e861-952">EINVAL (GH #1571) 대신 공간이 부족 하 게 되 면 ENOSPC가 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-952">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="6e861-953">/Proc/sys/kernel/sem. 추가 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-953">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="6e861-954">구현 된 semop 및 semtimedop 시스템 호출</span><span class="sxs-lookup"><span data-stu-id="6e861-954">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="6e861-955">IP_RECVTOS & IPV6_RECVTCLASS socket 옵션을 사용 하 여 nslookup 오류 수정 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="6e861-955">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="6e861-956">IP_RECVTTL 및 IPV6_RECVHOPLIMIT 소켓 옵션에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-956">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="6e861-957">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-957">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-958">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-958">LTP Results:</span></span>
<span data-ttu-id="6e861-959">통과 한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="6e861-959">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="6e861-960">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255</span><span class="sxs-lookup"><span data-stu-id="6e861-960">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6e861-961">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-961">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="6e861-962">Syscall 요약</span><span class="sxs-lookup"><span data-stu-id="6e861-962">Syscall Summary</span></span>
<span data-ttu-id="6e861-963">총 Syscall: 384</span><span class="sxs-lookup"><span data-stu-id="6e861-963">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="6e861-964">총 구현: 235</span><span class="sxs-lookup"><span data-stu-id="6e861-964">Total Implemented: 235</span></span> </br>
<span data-ttu-id="6e861-965">총 스텁: 22</span><span class="sxs-lookup"><span data-stu-id="6e861-965">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="6e861-966">구현 되지 않은 총: 127</span><span class="sxs-lookup"><span data-stu-id="6e861-966">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="6e861-967">자세한 분석</span><span class="sxs-lookup"><span data-stu-id="6e861-967">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="6e861-968">빌드 15007</span><span class="sxs-lookup"><span data-stu-id="6e861-968">Build 15007</span></span>

<span data-ttu-id="6e861-969">빌드 15007에 대 한 일반적인 Windows 정보는 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-969">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="6e861-970">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-970">Known Issue</span></span>

- <span data-ttu-id="6e861-971">콘솔에서 일부 Ctrl + <key> input을 인식 하지 못하는 알려진 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="6e861-972">여기에는 일반 ' c ' 키의 역할을 하는 ctrl + c 명령이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="6e861-973">해결 방법: 대체 키를 Ctrl + C에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="6e861-974">예를 들어 Ctrl + K를 Ctrl + C로 매핑하려면: `stty intr \^k`를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="6e861-975">이 매핑은 터미널 당 이며 bash를 시작할 *때마다* 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="6e861-976">사용자는이를 포함 하는 옵션을 탐색할 수 있습니다.`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="6e861-976">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-977">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-977">Fixed</span></span>

- <span data-ttu-id="6e861-978">WSL을 실행 하면 CPU 코어의 100%를 사용 하는 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-978">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="6e861-979">소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO 이제 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-979">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="6e861-980">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="6e861-980">(GH #851, 987)</span></span>
- <span data-ttu-id="6e861-981">Lxcore (GH #1452, 1414, 1343, 468, 308)에서 네트워크 인터페이스 실제 주소를 16 바이트로 자릅니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-981">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="6e861-982">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-982">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-983">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-983">LTP Results:</span></span>
<span data-ttu-id="6e861-984">통과 한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="6e861-984">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="6e861-985">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255</span><span class="sxs-lookup"><span data-stu-id="6e861-985">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6e861-986">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-986">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="6e861-987">빌드 15002</span><span class="sxs-lookup"><span data-stu-id="6e861-987">Build 15002</span></span>

<span data-ttu-id="6e861-988">빌드 15002에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-988">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="6e861-989">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-989">Known Issue</span></span>

<span data-ttu-id="6e861-990">다음과 같은 두 가지 알려진 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-990">Two known issues:</span></span>
- <span data-ttu-id="6e861-991">콘솔에서 일부 Ctrl + <key> input을 인식 하지 못하는 알려진 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-991">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="6e861-992">여기에는 일반 ' c ' 키의 역할을 하는 ctrl + c 명령이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-992">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="6e861-993">해결 방법: 대체 키를 Ctrl + C에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-993">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="6e861-994">예를 들어 Ctrl + K를 Ctrl + C로 매핑하려면: `stty intr \^k`를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-994">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="6e861-995">이 매핑은 터미널 당 이며 bash를 시작할 *때마다* 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-995">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="6e861-996">사용자는이를 포함 하는 옵션을 탐색할 수 있습니다.`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="6e861-996">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="6e861-997">WSL은 시스템 스레드를 실행 하는 동안 CPU 코어의 100%를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-997">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="6e861-998">근본 원인을 내부적으로 해결 하 고 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-998">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-999">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-999">Fixed</span></span>

- <span data-ttu-id="6e861-1000">이제 모든 bash 세션을 동일한 권한 수준에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1000">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="6e861-1001">다른 수준에서 세션을 시작 하려고 하면 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1001">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="6e861-1002">즉, 관리자 및 비관리자 콘솔을 동시에 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1002">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="6e861-1003">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="6e861-1003">(GH #626)</span></span>
<br/>
- <span data-ttu-id="6e861-1004">다음 NETLINK_ROUTE 메시지를 구현 함 (Windows 관리자 필요)</span><span class="sxs-lookup"><span data-stu-id="6e861-1004">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="6e861-1005">RTM_NEWADDR (지원 `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="6e861-1005">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="6e861-1006">RTM_NEWROUTE (지원 `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="6e861-1006">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="6e861-1007">RTM_DELADDR (지원 `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="6e861-1007">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="6e861-1008">RTM_DELROUTE (지원 `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="6e861-1008">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="6e861-1009">업데이트할 패키지의 예약 된 작업 확인은 더 이상 요금제 연결 (GH #1371)에서 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1009">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="6e861-1010">파이프가 중단 되는 오류 (예: bash-c "ls-alR/" |)를 수정 했습니다. bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="6e861-1010">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="6e861-1011">구현 된 TCP_KEEPCNT socket 옵션 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="6e861-1011">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="6e861-1012">구현 된 IP_MTU_DISCOVER INET socket 옵션 (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="6e861-1012">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="6e861-1013">Nt 경로 조회를 사용 하 여 init에서 NT 이진 파일을 실행 하는 레거시 기능을 제거 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1013">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="6e861-1014">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="6e861-1014">(GH #1325)</span></span>
- <span data-ttu-id="6e861-1015">그룹/기타 읽기 액세스 (0644) (GH #1321)를 허용 하는/dev/kmsg의 수정 모드</span><span class="sxs-lookup"><span data-stu-id="6e861-1015">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="6e861-1016">구현 된/proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="6e861-1016">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="6e861-1017">프로세스 시작 시간이 2432 년 (GH #974)으로 표시 된 오류를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1017">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="6e861-1018">기본 용어 환경 변수를 xterm-256color (GH #1446)로 전환 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1018">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="6e861-1019">프로세스 포크 중에 프로세스 커밋이 계산 되는 방식이 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1019">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="6e861-1020">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="6e861-1020">(GH #1286)</span></span>
- <span data-ttu-id="6e861-1021">구현 된/proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="6e861-1021">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="6e861-1022">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="6e861-1022">(GH #1286)</span></span>
- <span data-ttu-id="6e861-1023">GH (#69)를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1023">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="6e861-1024">바로 가기 이름이 잘못 지역화 된 오류 (GH #696)를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1024">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="6e861-1025">프로그램 헤더의 유효성을 올바르게 검사 하지 않는 elf 구문 분석 논리는 PATH_MAX 보다 작거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1025">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="6e861-1026">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="6e861-1026">(GH #1048)</span></span>
- <span data-ttu-id="6e861-1027">Procfs, sysfs, cgroupfs 및 binfmtfs (GH #1378)에 대 한 statfs 콜백을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1027">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="6e861-1028">닫히지 않는 AptPackageIndexUpdate 창이 수정 됨 (GH #1184 GH #1193에도 설명 됨)</span><span class="sxs-lookup"><span data-stu-id="6e861-1028">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="6e861-1029">ASLR 개성 ADDR_NO_RANDOMIZE 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1029">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="6e861-1030">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="6e861-1030">(GH #1148, 1128)</span></span>
- <span data-ttu-id="6e861-1031">PTRACE_GETSIGINFO, SIGSEGV, AV 중 적절 한 gdb 스택 추적을 위한 향상 된 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="6e861-1031">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="6e861-1032">Patchelf 이진 파일에 대해 Elf 구문 분석이 더 이상 실패 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1032">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="6e861-1033">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="6e861-1033">(GH #471)</span></span>
- <span data-ttu-id="6e861-1034">/Etc/resolv.conf에 전파 되는 VPN DNS (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="6e861-1034">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="6e861-1035">보다 안정적인 데이터 전송을 위해 TCP가 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1035">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="6e861-1036">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="6e861-1036">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="6e861-1037">이제 너무 많은 파일이 열려 있으면 (EMFILE) 올바른 오류 코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1037">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="6e861-1038">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="6e861-1038">(GH #1126, 2090)</span></span>
- <span data-ttu-id="6e861-1039">이제 Windows 감사 로그가 프로세스 만들기 감사에서 이미지 이름을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1039">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="6e861-1040">이제 bash 창 내에서 bash를 시작할 때 정상적으로 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1040">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="6e861-1041">Interop가 LxFs 아래의 작업 디렉터리에 액세스할 수 없는 경우 오류 메시지가 추가 되었습니다 (예: .bashrc).</span><span class="sxs-lookup"><span data-stu-id="6e861-1041">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="6e861-1042">WSL에서 Windows 경로가 잘린 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-1042">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="6e861-1043">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-1043">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1044">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1044">LTP Results:</span></span>
<span data-ttu-id="6e861-1045">통과 한 테스트 수: 690</span><span class="sxs-lookup"><span data-stu-id="6e861-1045">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="6e861-1046">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 274</span><span class="sxs-lookup"><span data-stu-id="6e861-1046">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="6e861-1047">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1047">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1048">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1048">Syscall Support</span></span>
<span data-ttu-id="6e861-1049">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1049">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1050">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1050">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="6e861-1051">빌드 14986</span><span class="sxs-lookup"><span data-stu-id="6e861-1051">Build 14986</span></span>

<span data-ttu-id="6e861-1052">빌드 14986에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1052">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1053">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1053">Fixed</span></span>

- <span data-ttu-id="6e861-1054">Netlink 및 인 pty IOCTLs를 사용 하 여 버그 검사 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1054">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="6e861-1055">이제 커널 버전은 4.4.0를 보고 합니다. Xenial를 사용 하 여 일관성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1055">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="6e861-1056">이제 Bash가 ' nul: ' (GH #1259)으로 전달 되 면 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1056">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="6e861-1057">이제 스레드 Id가 procfs에서 올바르게 보고 됨 (GH #967)</span><span class="sxs-lookup"><span data-stu-id="6e861-1057">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="6e861-1058">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 플래그는 이제 inotify_add_watch () (GH #1280)에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1058">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="6e861-1059">Timer_create 및 관련 시스템 호출을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1059">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="6e861-1060">이를 통해 GH (#307)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1060">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="6e861-1061">Ping이 0.000 m 시간을 반환 하는 문제 해결 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="6e861-1061">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="6e861-1062">너무 많은 파일이 열려 있으면 올바른 오류 코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1062">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="6e861-1063">인터페이스의 하드웨어 주소가 32 바이트 (예: Teredo 인터페이스) 인 경우 EINVAL를 사용 하 여 네트워크 인터페이스 데이터에 대 한 Netlink 요청이 실패 하는 WSL의 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="6e861-1063">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="6e861-1064">Linux "ip" 유틸리티에는 WSL에서 32 바이트 하드웨어 주소를 보고 하는 경우 충돌 하는 버그가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1064">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="6e861-1065">이는 WSL이 아니라 "ip"의 버그입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1065">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="6e861-1066">"Ip" 유틸리티는 하드웨어 주소를 인쇄 하는 데 사용 되는 문자열 버퍼의 길이를 하드 코딩 하 고, 버퍼가 너무 작아서 32 바이트 하드웨어 주소를 인쇄할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1066">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="6e861-1067">추가 수정 사항 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-1067">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1068">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1068">LTP Results:</span></span>
<span data-ttu-id="6e861-1069">통과 한 테스트 수: 669</span><span class="sxs-lookup"><span data-stu-id="6e861-1069">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="6e861-1070">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 258</span><span class="sxs-lookup"><span data-stu-id="6e861-1070">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="6e861-1071">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1071">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1072">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1072">Syscall Support</span></span>
<span data-ttu-id="6e861-1073">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1073">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1074">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1074">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="6e861-1075">빌드 14971</span><span class="sxs-lookup"><span data-stu-id="6e861-1075">Build 14971</span></span>

<span data-ttu-id="6e861-1076">빌드 14971에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1076">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1077">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1077">Fixed</span></span>

 - <span data-ttu-id="6e861-1078">이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1078">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6e861-1079">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1079">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1080">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1080">LTP Results:</span></span>
<span data-ttu-id="6e861-1081">14965에서 변경 되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e861-1081">Unchanged from 14965</span></span> </br>
<span data-ttu-id="6e861-1082">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="6e861-1082">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6e861-1083">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1083">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1084">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1084">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="6e861-1085">빌드 14965</span><span class="sxs-lookup"><span data-stu-id="6e861-1085">Build 14965</span></span>

<span data-ttu-id="6e861-1086">빌드 14965에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1086">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1087">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1087">Fixed</span></span>

- <span data-ttu-id="6e861-1088">Netlink sockets NETLINK_ROUTE 프로토콜의 RTM_GETLINK 및 RTM_GETADDR에 대 한 지원 (GH #468)</span><span class="sxs-lookup"><span data-stu-id="6e861-1088">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="6e861-1089">네트워크 열거에 대해 ifconfig 및 ip 명령을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1089">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="6e861-1090">자세한 내용은 [Wsl 네트워킹 블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1090">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="6e861-1091">/sbin는 이제 기본적으로 사용자의 경로에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1091">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="6e861-1092">이제 NT 사용자 경로가 기본적으로 WSL 경로에 추가 됩니다. 즉, Linux 경로에 System32를 추가 하지 않고 notepad.exe를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1092">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="6e861-1093">/Proc/sys/kernel/cap_last_cap에 대 한 지원이 추가 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1093">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="6e861-1094">현재 작업 디렉터리에 비 ansi 문자 (GH #1254)가 포함 되어 있으면 이제 WSL에서 NT 이진 파일을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1094">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="6e861-1095">연결 되지 않은 unix 스트림 소켓에서 종료를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1095">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="6e861-1096">PR_GET_PDEATHSIG에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1096">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="6e861-1097">CLONE_PARENT에 대 한 지원이 추가 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1097">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="6e861-1098">파이프가 중단 되는 오류 (예: bash-c "ls-alR/" |)를 수정 했습니다. bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="6e861-1098">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="6e861-1099">현재 터미널에 연결 하는 요청을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1099">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="6e861-1100">/Proc/<pid>/oom_score_adj을 쓰기 가능으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1100">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="6e861-1101">/Sys/fs/cgroup 폴더를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1101">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="6e861-1102">sched_setaffinity은 선호도 비트 마스크의 수를 반환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1102">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="6e861-1103">인터프리터 경로를 잘못 가정 하는 ELF 유효성 검사 논리는 64 자 미만 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1103">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="6e861-1104">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="6e861-1104">(GH #743)</span></span>
- <span data-ttu-id="6e861-1105">Open file 설명자는 콘솔 창을 열어 둘 수 있습니다 (GH #1187).</span><span class="sxs-lookup"><span data-stu-id="6e861-1105">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="6e861-1106">Fixeed ()가 대상 이름에 후행 슬래시를 사용 하 여 실패 한 경우 오류 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="6e861-1106">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="6e861-1107">/Proc/net/dev 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-1107">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="6e861-1108">타이머 해상도로 인해 0.000 ms ping을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1108">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="6e861-1109">구현 된/proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="6e861-1109">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="6e861-1110">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1110">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1111">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1111">LTP Results:</span></span>
<span data-ttu-id="6e861-1112">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="6e861-1112">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6e861-1113">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1113">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1114">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1114">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="6e861-1115">빌드 14959</span><span class="sxs-lookup"><span data-stu-id="6e861-1115">Build 14959</span></span>

<span data-ttu-id="6e861-1116">빌드 14959에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1116">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1117">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1117">Fixed</span></span>

- <span data-ttu-id="6e861-1118">Windows에 대 한 Pico 프로세스 알림이 개선 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1118">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="6e861-1119">[Wsl 블로그에서](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)추가 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1119">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="6e861-1120">Windows 상호 운용성으로 향상 된 안정성</span><span class="sxs-lookup"><span data-stu-id="6e861-1120">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="6e861-1121">EDP (엔터프라이즈 데이터 보호)를 사용 하는 경우 bash를 시작할 때 0x80070057 오류 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-1121">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="6e861-1122">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1122">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1123">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1123">LTP Results:</span></span>
<span data-ttu-id="6e861-1124">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="6e861-1124">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6e861-1125">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1125">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1126">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1126">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="6e861-1127">빌드 14955</span><span class="sxs-lookup"><span data-stu-id="6e861-1127">Build 14955</span></span>

<span data-ttu-id="6e861-1128">빌드 14955에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1128">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1129">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1129">Fixed</span></span>

 - <span data-ttu-id="6e861-1130">이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1130">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6e861-1131">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1131">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1132">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1132">LTP Results:</span></span>
<span data-ttu-id="6e861-1133">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="6e861-1133">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6e861-1134">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1134">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1135">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1135">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="6e861-1136">빌드 14951</span><span class="sxs-lookup"><span data-stu-id="6e861-1136">Build 14951</span></span>

<span data-ttu-id="6e861-1137">빌드 14951에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1137">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="6e861-1138">새 기능: Windows/Ubuntu 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="6e861-1138">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="6e861-1139">이제 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1139">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="6e861-1140">이렇게 하면 사용자에 게 Windows 환경 및 시스템과 상호 작용할 수 있는 방법이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1140">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="6e861-1141">이제 사용자가 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1141">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="6e861-1142">자세한 내용은 다음 위치에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1142">More information can be found at:</span></span>

- [<span data-ttu-id="6e861-1143">Interop 용 WSL 팀 블로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1143">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="6e861-1144">MSDN Interop 설명서</span><span class="sxs-lookup"><span data-stu-id="6e861-1144">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1145">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1145">Fixed</span></span>

- <span data-ttu-id="6e861-1146">이제 모든 새 WSL 인스턴스에 Ubuntu 16.04 (Xenial)이 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1146">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="6e861-1147">T (기존 14.04) 인스턴스가 있는 사용자는 자동으로 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1147">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="6e861-1148">설치 중에 설정 된 로캘이 이제 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1148">Locale set during install is now displayed</span></span>
- <span data-ttu-id="6e861-1149">WSL 프로세스를 파일로 리디렉션하는 버그를 포함 하 여 터미널의 향상 된 기능은 항상 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1149">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="6e861-1150">콘솔 수명은 bash 수명에 연결 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1150">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="6e861-1151">콘솔 창 크기는 버퍼 크기가 아닌 표시 크기를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1151">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="6e861-1152">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1152">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1153">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1153">LTP Results:</span></span>
<span data-ttu-id="6e861-1154">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="6e861-1154">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6e861-1155">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1155">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1156">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1156">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="6e861-1157">빌드 14946</span><span class="sxs-lookup"><span data-stu-id="6e861-1157">Build 14946</span></span>

<span data-ttu-id="6e861-1158">빌드 14946에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1158">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1159">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1159">Fixed</span></span>

- <span data-ttu-id="6e861-1160">공백이 나 따옴표를 포함 하는 NT 사용자 이름을 가진 사용자에 대해 WSL 사용자 계정을 만들지 못하게 하는 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1160">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="6e861-1161">상태에서 디렉터리의 링크 수에 대해 0을 반환 하도록 VolFs 및 DrvFs를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1161">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="6e861-1162">IPV6_MULTICAST_HOPS socket 옵션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1162">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="6e861-1163">Tty 당 단일 콘솔 i/o 루프로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1163">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="6e861-1164">예: 다음과 같은 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1164">Example: the following command is possible:</span></span>
  - <span data-ttu-id="6e861-1165">bash-c "echo data" | bash-c "ssh user@example.com ' cat > foo .txt '"</span><span class="sxs-lookup"><span data-stu-id="6e861-1165">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="6e861-1166">/proc/cpuinfo (GH #1115)에서 공백을 탭으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1166">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="6e861-1167">이제 DrvFs이 탑재 된 Windows 볼륨과 일치 하는 이름으로 mountinfo에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1167">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="6e861-1168">이제/home 및/root가 올바른 이름의 mountinfo에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1168">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="6e861-1169">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1169">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1170">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1170">LTP Results:</span></span>
<span data-ttu-id="6e861-1171">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="6e861-1171">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6e861-1172">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1172">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1173">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1173">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="6e861-1174">빌드 14942</span><span class="sxs-lookup"><span data-stu-id="6e861-1174">Build 14942</span></span>

<span data-ttu-id="6e861-1175">빌드 14942에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1175">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1176">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1176">Fixed</span></span>

- <span data-ttu-id="6e861-1177">SSH를 차단 하는 "NOEXECUTE 메모리의 실행을 시도 했습니다." 라는 네트워킹 충돌을 포함 하 여 해결 된 많은 버그 검사</span><span class="sxs-lookup"><span data-stu-id="6e861-1177">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="6e861-1178">DrvFs의 Windows 응용 프로그램에서 생성 된 알림에 대 한 inotifiy 지원은 현재</span><span class="sxs-lookup"><span data-stu-id="6e861-1178">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="6e861-1179">Mongod에 대해 TCP_KEEPIDLE 및 TCP_KEEPINTVL를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1179">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="6e861-1180">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="6e861-1180">(GH #695)</span></span>
- <span data-ttu-id="6e861-1181">Pivot_root 시스템 호출을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1181">Implement the pivot_root system call</span></span>
- <span data-ttu-id="6e861-1182">SO_DONTROUTE에 대 한 소켓 옵션 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-1182">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="6e861-1183">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1183">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="6e861-1184">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1184">LTP Results:</span></span>
<span data-ttu-id="6e861-1185">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="6e861-1185">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6e861-1186">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263</span><span class="sxs-lookup"><span data-stu-id="6e861-1186">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6e861-1187">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1187">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1188">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1188">Syscall Support</span></span>
<span data-ttu-id="6e861-1189">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1189">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1190">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1190">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="6e861-1191">빌드 14936</span><span class="sxs-lookup"><span data-stu-id="6e861-1191">Build 14936</span></span>

<span data-ttu-id="6e861-1192">빌드 14936에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1192">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="6e861-1193">참고: WSL은 향후 릴리스에서 Ubuntu 14.04 (t) 대신 Ubuntu 16.04 (Xenial)을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1193">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="6e861-1194">이 변경 내용은 새 인스턴스 (lxrun/install 또는 먼저 bash를 실행)를 설치 하는 참가자에 게 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1194">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="6e861-1195">T를 사용 하는 기존 인스턴스는 자동으로 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1195">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="6e861-1196">사용자는 릴리스-업그레이드 명령을 사용 하 여 t 이미지를 Xenial로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1196">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="6e861-1197">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-1197">Known Issue</span></span>
<span data-ttu-id="6e861-1198">WSL에서 일부 소켓 구현에 문제가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1198">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="6e861-1199">버그 확인은 "NOEXECUTE 메모리의 실행을 시도 했습니다." 라는 오류와 함께 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1199">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="6e861-1200">이 문제의 가장 일반적인 노력 ssh를 사용할 때 발생 하는 충돌입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1200">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="6e861-1201">근본 원인은 내부 빌드에서 고정 되 고, 가장 빠른 기회에서 참가자에 게 푸시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1201">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-1202">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1202">Fixed</span></span>

- <span data-ttu-id="6e861-1203">Chroot 시스템 호출을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1203">Implemented the chroot system call</span></span>
- <span data-ttu-id="6e861-1204">~~DrvFs의 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원을 포함 하는~~ inotify의 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-1204">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="6e861-1205">수정 지금은 Windows 응용 프로그램에서 시작 되는 변경 내용에 대 한 Inotify 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1205">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="6e861-1206">I p v 6에 대<port n> 한 소켓 바인딩: 이제 IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1206">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="6e861-1207">Waitid systemcall의 WNOWAIT 동작 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="6e861-1207">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="6e861-1208">IP_HDRINCL 및 IP_TTL IP 소켓 옵션에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1208">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="6e861-1209">길이가 0 인 읽기 ()는 즉시 반환 되어야 합니다 (GH #975).</span><span class="sxs-lookup"><span data-stu-id="6e861-1209">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="6e861-1210">Tar 파일에 NULL 종결자를 포함 하지 않는 파일 이름 및 파일 이름 접두사를 올바르게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1210">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="6e861-1211">/dev/snull에 대 한 epoll 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1211">epoll support for /dev/null</span></span>
- <span data-ttu-id="6e861-1212">Fix/vrhtime 원본 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1212">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="6e861-1213">Bash-c 이제 파일로 리디렉션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1213">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="6e861-1214">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1214">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1215">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1215">LTP Results:</span></span>
<span data-ttu-id="6e861-1216">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="6e861-1216">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6e861-1217">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 264</span><span class="sxs-lookup"><span data-stu-id="6e861-1217">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="6e861-1218">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1219">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1219">Syscall Support</span></span>
<span data-ttu-id="6e861-1220">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1220">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1221">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1221">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="6e861-1222">빌드 14931</span><span class="sxs-lookup"><span data-stu-id="6e861-1222">Build 14931</span></span>

<span data-ttu-id="6e861-1223">빌드 14931에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1223">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1224">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1224">Fixed</span></span>

 - <span data-ttu-id="6e861-1225">이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1225">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6e861-1226">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1226">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="6e861-1227">빌드 14926</span><span class="sxs-lookup"><span data-stu-id="6e861-1227">Build 14926</span></span>

<span data-ttu-id="6e861-1228">빌드 14926에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1228">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1229">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1229">Fixed</span></span>

- <span data-ttu-id="6e861-1230">이제 Ping은 관리자 권한이 없는 콘솔에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1230">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="6e861-1231">이제 Ping6이 지원 됩니다 (관리자 권한 없음).</span><span class="sxs-lookup"><span data-stu-id="6e861-1231">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="6e861-1232">WSL을 통해 수정 된 파일에 대 한 Inotify 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-1232">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="6e861-1233">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="6e861-1233">(GH #216)</span></span>
  - <span data-ttu-id="6e861-1234">지원 되는 플래그:</span><span class="sxs-lookup"><span data-stu-id="6e861-1234">Flags supported:</span></span>
    - <span data-ttu-id="6e861-1235">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="6e861-1235">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="6e861-1236">이벤트 inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="6e861-1236">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="6e861-1237">inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="6e861-1237">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="6e861-1238">출력 읽기: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="6e861-1238">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="6e861-1239">알려진 문제: Windows 응용 프로그램에서 파일을 수정 해도 이벤트가 생성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="6e861-1239">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="6e861-1240">이제 Unix 소켓이 SCM_CREDENTIALS을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1240">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6e861-1241">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="6e861-1241">LTP Results:</span></span>
<span data-ttu-id="6e861-1242">통과 한 테스트 수: 651</span><span class="sxs-lookup"><span data-stu-id="6e861-1242">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="6e861-1243">전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 258</span><span class="sxs-lookup"><span data-stu-id="6e861-1243">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="6e861-1244">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="6e861-1244">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="6e861-1245">빌드 14915</span><span class="sxs-lookup"><span data-stu-id="6e861-1245">Build 14915</span></span>

<span data-ttu-id="6e861-1246">빌드 14915에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1246">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1247">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1247">Fixed</span></span>
-  <span data-ttu-id="6e861-1248">GH #262 (unix 데이터 그램 소켓) 용 socketpair</span><span class="sxs-lookup"><span data-stu-id="6e861-1248">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="6e861-1249">SO_REUSEADDR에 대 한 Unix 소켓 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1249">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="6e861-1250">SO_BROADCAST에 대 한 UNIX 소켓 지원 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="6e861-1250">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="6e861-1251">SOCK_SEQPACKET에 대 한 Unix 소켓 지원 (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="6e861-1251">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="6e861-1252">Unix 데이터 그램 소켓 전송, 수신 및 종료에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-1252">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="6e861-1253">고정 되지 않은 주소에 대 한 잘못 된 mmap 매개 변수 유효성 검사로 인해 버그 확인을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1253">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="6e861-1254">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="6e861-1254">(GH #847)</span></span>
- <span data-ttu-id="6e861-1255">터미널 상태의 일시 중단/다시 시작에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1255">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="6e861-1256">화면 유틸리티 (GH #774)의 차단을 해제 하는 TIOCPKT ioctl 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1256">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="6e861-1257">알려진 문제: 작동 하지 않는 기능 키</span><span class="sxs-lookup"><span data-stu-id="6e861-1257">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="6e861-1258">LxpTimerFdWorkerRoutine (GH #814)에서 해제 된 멤버 ' ReaderReady '에 액세스할 수 있는 타이머를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1258">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="6e861-1259">Futex, 설문 조사 및 clock_nanosleep에 대 한 다시 시작 가능한 시스템 호출 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1259">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="6e861-1260">추가 된 바인드 탑재 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1260">Added bind mount support</span></span>
- <span data-ttu-id="6e861-1261">탑재 네임 스페이스 지원에 대 한 공유 해제</span><span class="sxs-lookup"><span data-stu-id="6e861-1261">unshare for mount namespace support</span></span>
    - <span data-ttu-id="6e861-1262">알려진 문제: 현재 작업 디렉터리로 새 탑재 네임 스페이스 `unshare(CLONE_NEWNS)` 를 만들 때 이전 네임 스페이스를 계속 가리키도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1262">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="6e861-1263">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1263">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="6e861-1264">빌드 14905</span><span class="sxs-lookup"><span data-stu-id="6e861-1264">Build 14905</span></span>

<span data-ttu-id="6e861-1265">빌드 14905에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1265">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1266">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1266">Fixed</span></span>
- <span data-ttu-id="6e861-1267">이제 다시 시작 가능한 시스템 호출이 지원 됩니다 (GH #349, GH #520).</span><span class="sxs-lookup"><span data-stu-id="6e861-1267">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="6e861-1268">Symlink (GH #650)로 끝나는 디렉터리</span><span class="sxs-lookup"><span data-stu-id="6e861-1268">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="6e861-1269">/Sv/svvvvvhu에 대해 구현 된 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="6e861-1269">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="6e861-1270">/Proc/[pid]/탑재,/proc/[pid]/mountinfo 및/proc/[pid]/mountstats 파일을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1270">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="6e861-1271">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1271">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="6e861-1272">빌드 14901</span><span class="sxs-lookup"><span data-stu-id="6e861-1272">Build 14901</span></span>
<span data-ttu-id="6e861-1273">사후 Windows 10 기념일 업데이트 릴리스에 대 한 첫 번째 Insider build.</span><span class="sxs-lookup"><span data-stu-id="6e861-1273">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="6e861-1274">빌드 14901에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1274">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1275">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1275">Fixed</span></span>
- <span data-ttu-id="6e861-1276">후행 슬래시 문제를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1276">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="6e861-1277">이제와 `$ mv a/c/ a/b/` 같은 명령이 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1277">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="6e861-1278">이제 Ubuntu 로캘을 Windows 로캘로 설정 해야 하는지 여부를 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1278">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="6e861-1279">Ns 폴더에 대 한 procfs 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1279">Procfs support for ns folder</span></span>
- <span data-ttu-id="6e861-1280">Tmpfs, procfs 및 sysfs 파일 시스템에 대 한 탑재 및 탑재 해제 추가 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1280">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="6e861-1281">Fix mknod [at] 32 비트 ABI 서명</span><span class="sxs-lookup"><span data-stu-id="6e861-1281">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="6e861-1282">발송 모델로 이동 하는 Unix 소켓</span><span class="sxs-lookup"><span data-stu-id="6e861-1282">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="6e861-1283">Setsockopt를 사용 하 여 설정 된 INET 소켓 수신 버퍼 크기를 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1283">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="6e861-1284">MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-1284">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="6e861-1285">Linux process stdin/stdout 파이프 리디렉션 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="6e861-1285">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="6e861-1286">CMD에서 bash-c 명령의 파이프를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1286">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="6e861-1287">예: > dir | bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="6e861-1287">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="6e861-1288">이제 여러 개의 탭이 있는 시스템에 Bash를 설치할 수 있습니다 (GH #538, #358).</span><span class="sxs-lookup"><span data-stu-id="6e861-1288">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="6e861-1289">기본 INET 소켓 버퍼 크기는 기본 Ubuntu 설정의 크기와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1289">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="6e861-1290">Xattr syscall을 listxattr에 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1290">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="6e861-1291">SIOC.GIF 회의의 유효한 IPv4 주소가 있는 인터페이스만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1291">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="6e861-1292">Ptrace에서 삽입 하는 경우 신호 기본 작업 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1292">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="6e861-1293">/proc/sys/vm/min_free_kbytes 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-1293">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="6e861-1294">Sigreturn에서 컨텍스트를 복원 하는 경우 컴퓨터 컨텍스트 레지스터 값 사용</span><span class="sxs-lookup"><span data-stu-id="6e861-1294">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="6e861-1295">이는 일부 사용자에 대해 java 및 javac이 중단 된 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1295">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="6e861-1296">/Proc/sys/kernel/hostname 구현</span><span class="sxs-lookup"><span data-stu-id="6e861-1296">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1297">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1297">Syscall Support</span></span>
<span data-ttu-id="6e861-1298">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1298">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1299">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1299">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="6e861-1300">Windows 10 기념일 업데이트에 14388 빌드</span><span class="sxs-lookup"><span data-stu-id="6e861-1300">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="6e861-1301">빌드 14388에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/14388wip)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1301">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1302">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1302">Fixed</span></span>
- <span data-ttu-id="6e861-1303">8/2에 대 한 Windows 10 기념일 업데이트 준비에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1303">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="6e861-1304">기념일 업데이트의 WSL에 대 한 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/wsl/) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-1304">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="6e861-1305">빌드 14376</span><span class="sxs-lookup"><span data-stu-id="6e861-1305">Build 14376</span></span>
<span data-ttu-id="6e861-1306">빌드 14376에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1306">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1307">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1307">Fixed</span></span>
- <span data-ttu-id="6e861-1308">Apt-get이 중단 되는 일부 인스턴스 제거 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="6e861-1308">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="6e861-1309">빈 탑재를 올바르게 처리 하지 않는 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="6e861-1309">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="6e861-1310">지 각 디스크가 올바르게 탑재 되지 않은 문제를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1310">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="6e861-1311">지원 되는 unix 소켓 수락 플래그 (부분 GH #451)</span><span class="sxs-lookup"><span data-stu-id="6e861-1311">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="6e861-1312">일반적인 네트워크 관련 블루 스크린 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1312">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="6e861-1313">/Proc/[pid]/task (GH #523)에 액세스할 때 블루 스크린을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1313">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="6e861-1314">일부 인 pty 시나리오에 대 한 높은 CPU 사용률 (GH #488, #504)을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1314">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="6e861-1315">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1315">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="6e861-1316">빌드 14371</span><span class="sxs-lookup"><span data-stu-id="6e861-1316">Build 14371</span></span>
<span data-ttu-id="6e861-1317">빌드 14371에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1317">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1318">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1318">Fixed</span></span>
- <span data-ttu-id="6e861-1319">Ptrace를 사용 하는 경우 SIGCHLD 및 wait ()로 타이밍 경합을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1319">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="6e861-1320">경로에 후행/(GH #432)가 있는 경우 몇 가지 동작을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1320">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="6e861-1321">자식에 대 한 열린 핸들로 인해 이름 바꾸기/연결 해제 실패 문제가 해결 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1321">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="6e861-1322">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1322">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="6e861-1323">빌드 14366</span><span class="sxs-lookup"><span data-stu-id="6e861-1323">Build 14366</span></span>
<span data-ttu-id="6e861-1324">빌드 14366에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1324">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1325">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1325">Fixed</span></span>
- <span data-ttu-id="6e861-1326">Symlink를 통한 파일 생성 수정</span><span class="sxs-lookup"><span data-stu-id="6e861-1326">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="6e861-1327">Python에 대 한 listxattr 추가 (GH 385)</span><span class="sxs-lookup"><span data-stu-id="6e861-1327">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="6e861-1328">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1328">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1329">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1329">Syscall Support</span></span>
-   <span data-ttu-id="6e861-1330">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1331">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="6e861-1332">빌드 14361</span><span class="sxs-lookup"><span data-stu-id="6e861-1332">Build 14361</span></span>
<span data-ttu-id="6e861-1333">빌드 14361에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14361)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1333">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1334">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1334">Fixed</span></span>
- <span data-ttu-id="6e861-1335">DrvFs는 Windows의 Ubuntu에서 Bash로 실행 될 때 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1335">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="6e861-1336">사용자는 .txt와 CASE를 입력할 수 있습니다. /Mnt/c 드라이브의 TXT</span><span class="sxs-lookup"><span data-stu-id="6e861-1336">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="6e861-1337">대/소문자 구분은 Windows의 Ubuntu에 있는 Bash 내 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1337">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="6e861-1338">Bash를 벗어난 NTFS에서 파일을 올바르게 보고 하지만 Windows의 파일과 상호 작용 하는 경우 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1338">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="6e861-1339">각 볼륨의 루트 (예:/mnt/c)는 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1339">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="6e861-1340">Windows에서 이러한 파일을 처리 하는 방법에 대 한 자세한 내용은 [여기](https://support.microsoft.com/en-us/kb/100625)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e861-1340">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="6e861-1341">매우 향상 된 인 pty/tty 지원.</span><span class="sxs-lookup"><span data-stu-id="6e861-1341">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="6e861-1342">현재 TMUX와 같은 응용 프로그램 지원 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="6e861-1342">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="6e861-1343">사용자 계정이 항상 만들어지지 않는 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1343">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="6e861-1344">매우 긴 인수 목록을 허용 하는 최적화 된 명령줄 인수 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1344">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="6e861-1345">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="6e861-1345">(GH #153)</span></span>
- <span data-ttu-id="6e861-1346">이제 DrvFs에서 삭제할 수 있고 chmod read_only 파일</span><span class="sxs-lookup"><span data-stu-id="6e861-1346">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="6e861-1347">연결이 끊어질 때 터미널이 중단 되는 일부 인스턴스 (GH #43)를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1347">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="6e861-1348">chmod 및 chown가 이제 tty 장치에서 작동</span><span class="sxs-lookup"><span data-stu-id="6e861-1348">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="6e861-1349">0\.0.0.0 및::에서 localhost로 연결 허용 (GH #388)</span><span class="sxs-lookup"><span data-stu-id="6e861-1349">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="6e861-1350">Sendmsg/recvmsg는 이제 > 1 (부분 GH #376)의 IO 벡터 길이를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1350">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="6e861-1351">사용자는 이제 자동 생성 된 호스트 파일 (GH #398)을 옵트아웃 (opt out) 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1351">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="6e861-1352">설치 하는 동안 자동으로 Linux 로캘을 NT 로캘로 일치 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="6e861-1352">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="6e861-1353">/Proc/sys/vm/swappiness 파일 (GH #306)을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1353">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="6e861-1354">이제 strace가 제대로 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1354">strace now exits correctly</span></span>
- <span data-ttu-id="6e861-1355">/Proc/self/fd를 통해 파이프를 다시 열 수 있도록 허용 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="6e861-1355">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="6e861-1356">DrvFs에서%LOCALAPPDATA%\lxss 아래의 디렉터리 숨기기 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="6e861-1356">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="6e861-1357">Bash ~를 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1357">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="6e861-1358">"Bash ~-c ls"와 같은 명령이 지원 됩니다 (GH #467).</span><span class="sxs-lookup"><span data-stu-id="6e861-1358">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="6e861-1359">이제 소켓에서 종료 하는 동안 epoll 읽기를 사용할 수 있음을 알립니다 (GH #271).</span><span class="sxs-lookup"><span data-stu-id="6e861-1359">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="6e861-1360">lxrun/uninstall은 파일 및 폴더를 삭제 하는 작업을 더 효율적으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1360">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="6e861-1361">GH (#246)를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1361">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="6e861-1362">XEmacs (GH #481)와 같은 x11 앱에 대 한 지원 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-1362">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="6e861-1363">기본 Ubuntu 설정과 일치 하도록 초기 스레드 스택 크기를 업데이트 하 고 get_rlimit syscall (GH #172, #258)에 대 한 크기를 올바르게 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1363">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="6e861-1364">Pico 프로세스 이미지 이름 (예: 감사)의 보고 기능 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-1364">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="6e861-1365">Df 명령에 대해/proc/mountinfo 구현 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1365">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="6e861-1366">자식 이름에 대 한 symlink 오류 코드를 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1366">Fixed symlink error code for child name .</span></span> <span data-ttu-id="6e861-1367">및입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1367">and ..</span></span>
- <span data-ttu-id="6e861-1368">추가 개선 사항에 대 한 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1368">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1369">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1369">Syscall Support</span></span>
<span data-ttu-id="6e861-1370">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1371">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="6e861-1372">빌드 14352</span><span class="sxs-lookup"><span data-stu-id="6e861-1372">Build 14352</span></span>
<span data-ttu-id="6e861-1373">빌드 14352에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14352)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1373">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1374">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1374">Fixed</span></span>
- <span data-ttu-id="6e861-1375">대량 파일이 다운로드/생성 되지 않은 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1375">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="6e861-1376">Npm 및 기타 시나리오를 차단 해제 해야 합니다 (GH #3, GH #313).</span><span class="sxs-lookup"><span data-stu-id="6e861-1376">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="6e861-1377">소켓이 중단 된 일부 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="6e861-1377">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="6e861-1378">일부 ptrace 오류 수정 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1378">Corrected some ptrace errors</span></span>
- <span data-ttu-id="6e861-1379">255 자 보다 긴 파일 이름을 허용 하는 WSL의 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="6e861-1379">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="6e861-1380">영어가 아닌 문자에 대 한 지원 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-1380">Improved support for non-English characters</span></span>
- <span data-ttu-id="6e861-1381">현재 Windows 표준 시간대 데이터를 추가 하 고 기본값으로 설정</span><span class="sxs-lookup"><span data-stu-id="6e861-1381">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="6e861-1382">각 탑재 지점에 대 한 고유한 장치 id (jre fix – GH #49)</span><span class="sxs-lookup"><span data-stu-id="6e861-1382">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="6e861-1383">"."를 포함 하는 경로에 대 한 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1383">Correct issue with paths containing “.”</span></span> <span data-ttu-id="6e861-1384">및 "."</span><span class="sxs-lookup"><span data-stu-id="6e861-1384">and “..”</span></span>
- <span data-ttu-id="6e861-1385">Fifo 지원 추가 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="6e861-1385">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="6e861-1386">네이티브 Ubuntu 형식에 맞게 resolv.conf의 업데이트 된 형식</span><span class="sxs-lookup"><span data-stu-id="6e861-1386">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="6e861-1387">일부 procfs 정리</span><span class="sxs-lookup"><span data-stu-id="6e861-1387">Some procfs cleanup</span></span>
- <span data-ttu-id="6e861-1388">관리자 콘솔에 대해 ping을 사용 하도록 설정 (GH #18)</span><span class="sxs-lookup"><span data-stu-id="6e861-1388">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1389">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1389">Syscall Support</span></span>
<span data-ttu-id="6e861-1390">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1390">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1391">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1391">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="6e861-1392">빌드 14342</span><span class="sxs-lookup"><span data-stu-id="6e861-1392">Build 14342</span></span>
<span data-ttu-id="6e861-1393">빌드 14342에 대 한 일반 Windows 정보는 [Windows 블로그](https://aka.ms/wip14342)를 통해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1393">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="6e861-1394">VolFs 및 드라이브 Fs에 대 한 정보는 [Wsl 블로그](https://blogs.msdn.microsoft.com/wsl)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1394">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6e861-1395">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1395">Fixed</span></span>
- <span data-ttu-id="6e861-1396">Windows 사용자 이름에 유니코드 문자가 있는 경우의 설치 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-1396">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="6e861-1397">이제 FAQ의 apt 업데이트 udev 해결 방법이 기본적으로 처음 실행 될 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1397">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="6e861-1398">Symlink fs (/mnt/<drive>) 디렉터리에서 사용 하도록 설정 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1398">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="6e861-1399">이제 symlink fs와 VolFs 간에 작업</span><span class="sxs-lookup"><span data-stu-id="6e861-1399">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="6e861-1400">주소가 지정 된 최상위 경로 구문 분석 문제가 발생 했습니다.//이제 정상적으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1400">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="6e861-1401">드라이브의 npm 설치 및-g 옵션이 이제 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1401">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="6e861-1402">PHP 서버가 시작 되지 않도록 하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e861-1402">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="6e861-1403">네이티브 Ubuntu와 더 가까운 일치를 위해 $PATH와 같은 업데이트 된 기본 환경 값</span><span class="sxs-lookup"><span data-stu-id="6e861-1403">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="6e861-1404">Windows에서 apt 패키지 캐시를 업데이트 하기 위한 주간 유지 관리 작업 추가</span><span class="sxs-lookup"><span data-stu-id="6e861-1404">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="6e861-1405">ELF 헤더 유효성 검사와 관련 된 문제가 해결 되었습니다. 이제 WSL은 모든 Melkor 옵션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1405">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="6e861-1406">Zsh shell이 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1406">Zsh shell is functional</span></span>
- <span data-ttu-id="6e861-1407">미리 컴파일된 이동 이진 파일이 이제 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1407">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="6e861-1408">Bash에 대 한 확인 메시지가 이제 올바르게 지역화 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1408">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="6e861-1409">/proc/meminfo는 이제 올바른 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1409">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="6e861-1410">이제 지원 되는 소켓이 VFS에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1410">Sockets now supported in VFS</span></span>
- <span data-ttu-id="6e861-1411">/sdev는 이제 tempfs로 탑재 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1411">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="6e861-1412">이제 Fifo 지원 됨</span><span class="sxs-lookup"><span data-stu-id="6e861-1412">Fifo now supported</span></span>
- <span data-ttu-id="6e861-1413">이제 다중 코어 시스템이/proc/cpuinfo에서 올바르게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1413">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="6e861-1414">처음 실행 하는 동안 다운로드 한 추가 개선 사항 및 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="6e861-1414">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="6e861-1415">향상 된 기능 및 버그 수정을 Syscall.</span><span class="sxs-lookup"><span data-stu-id="6e861-1415">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="6e861-1416">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1416">Supported syscall list below.</span></span>
- <span data-ttu-id="6e861-1417">추가 버그 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1417">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="6e861-1418">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-1418">Known Issues</span></span>
- <span data-ttu-id="6e861-1419">'.. '을 (를) 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1419">Not resolving ‘..’</span></span> <span data-ttu-id="6e861-1420">일부 경우에는 드라이브에서 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="6e861-1420">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1421">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1421">Syscall Support</span></span>
<span data-ttu-id="6e861-1422">다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1422">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6e861-1423">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1423">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="6e861-1424">빌드 14332</span><span class="sxs-lookup"><span data-stu-id="6e861-1424">Build 14332</span></span>

<span data-ttu-id="6e861-1425">빌드 14332에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14332)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1425">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="6e861-1426">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1426">Fixed</span></span>
- <span data-ttu-id="6e861-1427">DNS 항목 우선 순위를 포함 하는 resolv.conf 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-1427">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="6e861-1428">/Mnt 및 비/mnt 드라이브 간에 파일 및 디렉터리를 이동 하는 문제</span><span class="sxs-lookup"><span data-stu-id="6e861-1428">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="6e861-1429">이제 symlink를 사용 하 여 Tar 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1429">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="6e861-1430">인스턴스를 만들 때 기본/run/lock 디렉터리를 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1430">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="6e861-1431">적절 한 상태 정보를 반환 하기 위해/sv/svnull 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e861-1431">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="6e861-1432">처음 실행 하는 동안 다운로드할 때 추가 오류 발생</span><span class="sxs-lookup"><span data-stu-id="6e861-1432">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="6e861-1433">향상 된 기능 및 버그 수정을 Syscall.</span><span class="sxs-lookup"><span data-stu-id="6e861-1433">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="6e861-1434">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1434">Supported syscall list below.</span></span>
- <span data-ttu-id="6e861-1435">추가 개선 사항에 대 한 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1435">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1436">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1436">Syscall Support</span></span>
<span data-ttu-id="6e861-1437">다음은 WSL에서 일부 구현을 포함 하는 새 syscall.</span><span class="sxs-lookup"><span data-stu-id="6e861-1437">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="6e861-1438">이 목록에 있는 syscall는 하나 이상의 시나리오에서 지원 되지만 지금은 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1438">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="6e861-1439">빌드 14328</span><span class="sxs-lookup"><span data-stu-id="6e861-1439">Build 14328</span></span>

<span data-ttu-id="6e861-1440">빌드 14332에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14328)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6e861-1440">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="6e861-1441">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="6e861-1441">New Features</span></span>
* <span data-ttu-id="6e861-1442">이제 Linux 사용자를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1442">Now support Linux users.</span></span>  <span data-ttu-id="6e861-1443">Windows에서 Ubuntu에 Bash를 설치 하면 Linux 사용자를 만들라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1443">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="6e861-1444">자세한 내용은 다음을 참조 하세요. https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="6e861-1444">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="6e861-1445">이제 호스트 이름이 Windows 컴퓨터 이름으로 설정 되어 있습니다.@localhost</span><span class="sxs-lookup"><span data-stu-id="6e861-1445">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="6e861-1446">빌드 14328에 대 한 자세한 내용은 다음을 참조 하세요. https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="6e861-1446">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="6e861-1447">고정</span><span class="sxs-lookup"><span data-stu-id="6e861-1447">Fixed</span></span>
* <span data-ttu-id="6e861-1448">비/mnt/<drive> 파일에 대 한 Symlink 향상</span><span class="sxs-lookup"><span data-stu-id="6e861-1448">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="6e861-1449">npm 설치 이제 작동</span><span class="sxs-lookup"><span data-stu-id="6e861-1449">npm install now works</span></span>
    * <span data-ttu-id="6e861-1450">이제 jdk/jre에서 [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)에 있는 지침을 사용 하 여 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1450">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="6e861-1451">알려진 문제: Windows 탑재에 대해 symlink가 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1451">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="6e861-1452">이후 빌드에서 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1452">Functionality will be available in a later build</span></span>
* <span data-ttu-id="6e861-1453">위쪽 및 htop 이제 표시</span><span class="sxs-lookup"><span data-stu-id="6e861-1453">top and htop now display</span></span>
* <span data-ttu-id="6e861-1454">일부 설치 오류에 대 한 추가 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="6e861-1454">Additional error messages for some install failures</span></span>
* <span data-ttu-id="6e861-1455">향상 된 기능 및 버그 수정을 Syscall.</span><span class="sxs-lookup"><span data-stu-id="6e861-1455">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="6e861-1456">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1456">Supported syscall list below.</span></span>
* <span data-ttu-id="6e861-1457">추가 개선 사항에 대 한 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="6e861-1457">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6e861-1458">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="6e861-1458">Syscall Support</span></span>
<span data-ttu-id="6e861-1459">다음은 WSL에서 일부 구현을 포함 하는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1459">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="6e861-1460">이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e861-1460">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
