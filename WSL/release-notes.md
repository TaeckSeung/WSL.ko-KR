---
title: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보
description: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보입니다.  매주 업데이트 합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem ubuntu 용 windows 하위 시스템
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988258"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="7bd1d-105">Linux 용 Windows 하위 시스템에 대 한 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="7bd1d-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="7bd1d-106">18890 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-106">Build 18890</span></span>
<span data-ttu-id="7bd1d-107">일반 Windows에 대 한 18890 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-108">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-108">WSL</span></span>
* <span data-ttu-id="7bd1d-109">비블로킹 소켓 누수 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="7bd1d-110">EOF 입력 터미널에 후속 읽기 [GH 3421]를 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="7bd1d-111">[GH 3928 설명] wsl.conf를 가리키도록 업데이트 하기 위해 resolv.conf 헤더</span><span class="sxs-lookup"><span data-stu-id="7bd1d-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="7bd1d-112">Epoll의 교착 상태 [GH 3922] 코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="7bd1d-113">-가져오고 내보내고-[GH 3932]에 대 한 인수에서 공백 처리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="7bd1d-114">Mmap 확장 파일은 제대로 작동 하지 않습니다 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="7bd1d-115">ARM64를 사용 하 여 문제를 해결 \\wsl$ 액세스 제대로 작동 하지 않습니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="7bd1d-116">추가 wsl.exe에 대 한 더 나은 기본 아이콘</span><span class="sxs-lookup"><span data-stu-id="7bd1d-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="7bd1d-117">18342 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-117">Build 18342</span></span>
<span data-ttu-id="7bd1d-118">일반 Windows에 대 한 18342 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-119">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-119">WSL</span></span>
* <span data-ttu-id="7bd1d-120">Windows에서 Linux 파일 WSL 배포판에 액세스 하려면 사용자가 기능을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="7bd1d-121">명령줄 및 또한 파일 탐색기와 VSCode Windows 앱을 통해 이러한 파일에 액세스할 수 있습니다, 그리고 등 이러한 파일을 사용 하 여 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="7bd1d-122">로 이동 하 여 파일에 액세스할 \\ \\wsl$\\< distro_name >로 이동 하 여 배포를 실행 중인 목록을 보거나 \\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="7bd1d-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="7bd1d-123">CPU 정보 태그를 추가 하 고 [GH 2234] Cpus_allowed [목록 (_l)] 값 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="7bd1d-124">[GH 3800] 리더가 아닌 스레드에서 exec를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="7bd1d-125">치명적이 지 않은 [GH 3785]으로 구성 업데이트 오류 처리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="7bd1d-126">오프셋 [GH 3768]를 적절히 처리할 binfmt 업데이트</span><span class="sxs-lookup"><span data-stu-id="7bd1d-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="7bd1d-127">계획 9 [GH 3854]에 대 한 매핑 네트워크 드라이브를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="7bd1d-128">지원 Windows Linux 및 Linux에 바인드 바 운 트에서 대 한 Windows 경로 번역-></span><span class="sxs-lookup"><span data-stu-id="7bd1d-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="7bd1d-129">읽기 전용으로 열려 있는 파일의 매핑에 대 한 읽기 전용 섹션 만들기</span><span class="sxs-lookup"><span data-stu-id="7bd1d-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="7bd1d-130">18334 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-130">Build 18334</span></span>
<span data-ttu-id="7bd1d-131">일반 Windows에 대 한 18334 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-132">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-132">WSL</span></span>
* <span data-ttu-id="7bd1d-133">Windows 표준 시간대 [GH 3747] Linux 표준 시간대로 매핑되는 방식을 다시 디자인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="7bd1d-134">메모리 누수를 해결 하 고 새로운 문자열 변환 함수 [GH 3746]를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="7bd1d-135">threadgroup이 없는 스레드를 사용 하 여에서 SIGCONT가 no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="7bd1d-136">/Proc/self/fd에서 소켓 및 epoll 파일 설명자를 올바르게 표시</span><span class="sxs-lookup"><span data-stu-id="7bd1d-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="7bd1d-137">18305 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-137">Build 18305</span></span>
<span data-ttu-id="7bd1d-138">일반 Windows에 대 한 18305 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-139">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-139">WSL</span></span>
* <span data-ttu-id="7bd1d-140">주 스레드가 종료 [GH 3589] pthread 파일에 대 한 액세스 권한을 상실합니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="7bd1d-141">필요한 경우에 TIOCSCTTY "force" 매개 변수를 무시 해야 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="7bd1d-142">wsl.exe 명령줄 향상 된 기능 및 추가 가져오기/내보내기 기능.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="7bd1d-143">18277 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-143">Build 18277</span></span>
<span data-ttu-id="7bd1d-144">일반 Windows에 대 한 18277 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-145">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-145">WSL</span></span>
* <span data-ttu-id="7bd1d-146">빌드 [GH 3645] 18272에에서 도입 된 "인터페이스" 오류 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="7bd1d-147">Umount syscall [GH 3605]에 대 한 MNT_FORCE 플래그를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="7bd1d-148">WSL 공식 CreatePseudoConsole API를 사용 하는 interop 전환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="7bd1d-149">FUTEX_WAIT 다시 시작 될 때 시간 제한 값을 유지 관리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="7bd1d-150">18272 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-150">Build 18272</span></span>
<span data-ttu-id="7bd1d-151">일반 Windows에 대 한 18272 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-152">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-152">WSL</span></span>
* <span data-ttu-id="7bd1d-153">**경고:** WSL 작동 하지 않습니다는이 빌드에는 문제가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="7bd1d-154">배포를 시작 하려고 할 때 "인터페이스" 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="7bd1d-155">문제가 해결 되었습니다 및 다음 주 Insider 빠른 빌드에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="7bd1d-156">이전에 설치한 경우 롤백할 수 있습니다 "이전 버전의 Windows 10으로 다시 이동"을 사용 하 여 이전 Windows 빌드 설정에서이 빌드에는 업데이트-> & 보안 복구-> 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="7bd1d-157">18267 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-157">Build 18267</span></span>
<span data-ttu-id="7bd1d-158">일반 Windows에 대 한 18267 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-159">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-159">WSL</span></span>
* <span data-ttu-id="7bd1d-160">좀비 프로세스 수 없습니다 수 했지만 누릴 수 있었습니다 않았고 무기한으로 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="7bd1d-161">WslRegisterDistribution 오류 메시지 [GH 3592]는 최대 길이 초과 하는 경우 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="7bd1d-162">읽기 전용 파일 DrvFs [GH 3556]에 대 한 성공 하려면 fsync 허용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="7bd1d-163">[GH 3584] 내부 symlink를 만들기 전에 /bin 및 /sbin 디렉터리가 존재 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="7bd1d-164">WSL 인스턴스에 대 한 인스턴스 종료 제한 시간 메커니즘을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="7bd1d-165">제한 시간을 15 초로, 인스턴스가 15 초 마지막 WSL 프로세스가 종료 된 후 종료 됩니다 즉 현재 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="7bd1d-166">배포를 즉시 종료 하려면 다음을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="7bd1d-167">17763 빌드 (1809)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-167">Build 17763 (1809)</span></span>
<span data-ttu-id="7bd1d-168">일반 Windows에 대 한 17763 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-169">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-169">WSL</span></span>
* <span data-ttu-id="7bd1d-170">동일한 스레드 우선 순위 [GH 1838] 변경에 대 한 너무 엄격한 Setpriority syscall 권한 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="7bd1d-171">Clock_gettime(CLOCK_BOOTTIME) [GH 3434]에 대해 음수 값을 반환 하지 않으려면 비편향된 인터럽트 시간 비율 부팅 시간에 사용 되는지 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="7bd1d-172">WSL binfmt 인터프리터 [GH 3424]에서 symlink를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="7bd1d-173">Threadgroup이 리더 파일 설명자 정리 보다 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="7bd1d-174">WSL 데 KeQueryInterruptTimePrecise KeQueryPerformanceCounter 대신 [GH 3252] 오버플로가 발생 하지 않도록 전환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="7bd1d-175">Ptrace 연결 월 [GH 1731] 시스템 호출에서 잘못 된 반환 값이 발생</span><span class="sxs-lookup"><span data-stu-id="7bd1d-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="7bd1d-176">여러 AF_UNIX 관련 된 수정 사항을 문제 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="7bd1d-177">WSL interop 현재 작업 디렉터리를 5 대 미만의 자 [GH 3379] 이면 실패를 일으킬 수 있는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="7bd1d-178">존재 하지 않는 포트 [GH 3286]에 대 한 루프백 연결 실패 한 두 번째 지연을 방지합니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="7bd1d-179">/Proc/sys/fs/file-max 스텁 파일 [GH 2893]를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="7bd1d-180">보다 정확 하 게 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="7bd1d-181">PR_SET_PTRACER 지원 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="7bd1d-182">실수로 epoll edge 트리거 이벤트 [GH 3276]의 선택을 취소 하는 파이프 파일 시스템</span><span class="sxs-lookup"><span data-stu-id="7bd1d-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7bd1d-183">Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="7bd1d-184">향상 된 좀비 지원 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="7bd1d-185">[GH 1493] Windows interop 동작을 제어 하기 위한 wsl.conf 항목 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="7bd1d-186">항상 그렇지는 않음 UNIX 소켓 패밀리 형식을 [GH 1774]를 반환 하는 getsockname에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="7bd1d-187">TIOCSTI [GH 1863]에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="7bd1d-188">비블로킹 소켓 연결 중 쓰기 시도 [GH 2846] EAGAIN 반환할지</span><span class="sxs-lookup"><span data-stu-id="7bd1d-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="7bd1d-189">탑재 된 Vhd [GH 3246에 3291]에서 interop를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="7bd1d-190">루트 폴더 [GH 3304]에서 문제를 확인 하는 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="7bd1d-191">TTY 키보드 ioctl KDGKBTYPE, KDGKBMODE 및 KDSKBMODE 제한적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="7bd1d-192">Windows UI 응용 프로그램은 백그라운드에서 시작 하는 경우에 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="7bd1d-193">Wsl-u 또는--사용자 옵션 [GH 1203] 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="7bd1d-194">빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="7bd1d-195">Unix 소켓 연결이 끊긴된 피어 자격 증명 [GH 3183]를 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="7bd1d-196">EAGAIN [GH 3191]를 사용 하 여 무기한 실패 무중단 Unix 소켓</span><span class="sxs-lookup"><span data-stu-id="7bd1d-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="7bd1d-197">대/소문자 = off는 새 기본 drvfs 탑재 [GH 2937, 3212, 3328] 형식</span><span class="sxs-lookup"><span data-stu-id="7bd1d-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="7bd1d-198">참조 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="7bd1d-199">배포 실행을 중지 하려면 종료/wslconfig를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="7bd1d-200">공간을 사용 하 여 경로 올바르게 처리 하지 않는 메뉴 항목 WSL 셸 컨텍스트를 사용 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="7bd1d-201">확장된 특성으로 단위 디렉터리에 대/소문자 구분. 노출</span><span class="sxs-lookup"><span data-stu-id="7bd1d-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="7bd1d-202">ARM64: 캐시 유지 관리 작업을 에뮬레이트하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="7bd1d-203">확인할 [dotnet 문제](https://github.com/dotnet/core/issues/1561)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="7bd1d-204">DrvFs: 개인 범위에 해당 하는 문자는 이스케이프 된 문자는 이스케이프을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="7bd1d-205">ELF 파서 인터프리터 길이 유효성 검사 [GH 3154]에서 해제-오류 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="7bd1d-206">과거의 시간을 사용 하 여 WSL 절대 타이머 [GH 3091] 실행 안 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="7bd1d-207">새로 만든된 재분석 지점을 부모 디렉터리에 따라서 나와 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="7bd1d-208">원자 단위로 DrvFs에서 대/소문자 구분 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="7bd1d-209">추가 문제를 해결 하 고 다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7bd1d-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-210">[GH 2712]</span></span>
* <span data-ttu-id="7bd1d-211">고정된 WSL UMCI을 사용 하는 경우 오류를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="7bd1d-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-212">[GH 3020]</span></span>
* <span data-ttu-id="7bd1d-213">WSL [GH 437 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="7bd1d-214">를 사용 하려면 shift 키를 누르고 및 탐색기 창에서 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="7bd1d-215">Unix 소켓 비차단 동작 [GH 2822, 3100] 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="7bd1d-216">GH 2026에 보고 된 NETLINK 명령을 중지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="7bd1d-217">탑재 전파 플래그 [GH 2911]에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="7bd1d-218">자르기 유발 하지 inotify 이벤트 [GH 2978]를 사용 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="7bd1d-219">추가-셸 없이 단일 바이너리를 호출 하는 wsl.exe exec 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="7bd1d-220">추가-특정 배포판을 선택 하려면 wsl.exe에 대 한 배포 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="7bd1d-221">Dmesg 제한적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-221">Limited support for dmesg.</span></span> <span data-ttu-id="7bd1d-222">응용 프로그램 dmesg를 로깅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="7bd1d-223">WSL 드라이버 dmesg를 제한 된 정보를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="7bd1d-224">나중에이 드라이버에서 다른 정보/진단 전달할 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="7bd1d-225">참고: dmesg를 통해 현재 지원 되는 `/dev/kmsg` 장치 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="7bd1d-226">`syslog` syscall 인터페이스 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="7bd1d-227">따라서 몇 가지는 `dmesg` 명령줄 옵션 등 `-S`, `-C` 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="7bd1d-228">기본 gid 및 네이티브 [GH 3042]에 맞게 직렬 장치 모드 변경</span><span class="sxs-lookup"><span data-stu-id="7bd1d-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="7bd1d-229">이제 DrvFs 확장 된 특성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="7bd1d-230">참고: DrvFs 확장 된 특성의 이름에 몇 가지 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="7bd1d-231">일부 문자 (같은 '/', ':' 및 '\*') 허용 되지 않습니다 되며 확장 특성 이름은 대/소문자 구분 DrvFs에서 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="7bd1d-232">빌드 18252 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-233">일반 Windows에 대 한 18252 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-234">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-234">WSL</span></span>
* <span data-ttu-id="7bd1d-235">Init 및 bsdtar 바이너리 lxssmanager dll를 별도 도구 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="7bd1d-236">경합 CLONE_FILES를 사용 하는 경우 파일 설명자를 닫기 주위를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="7bd1d-237">DrvFs 경로 변환할 때 /proc/pid/mountinfo에 선택적 필드를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="7bd1d-238">S_IFREG에 대 한 메타 데이터 지원은 되려면 DrvFs mknod 허용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="7bd1d-239">DrvFs에 만들어진 읽기 전용 파일 [GH 3411]를 설정 하는 읽기 전용 특성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="7bd1d-240">/Sbin/mount.drvfs DrvFs 탑재를 처리 하는 도우미를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="7bd1d-241">DrvFs의 POSIX 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="7bd1d-242">볼륨 GUID 없는 볼륨에서 경로 번역을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="7bd1d-243">17738 (Fast) 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="7bd1d-244">일반 Windows에 대 한 17738 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-245">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-245">WSL</span></span>
* <span data-ttu-id="7bd1d-246">동일한 스레드 우선 순위 [GH 1838] 변경에 대 한 너무 엄격한 Setpriority syscall 권한 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="7bd1d-247">Clock_gettime(CLOCK_BOOTTIME) [GH 3434]에 대해 음수 값을 반환 하지 않으려면 비편향된 인터럽트 시간 비율 부팅 시간에 사용 되는지 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="7bd1d-248">WSL binfmt 인터프리터 [GH 3424]에서 symlink를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="7bd1d-249">Threadgroup이 리더 파일 설명자 정리 보다 효율적으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="7bd1d-250">17728 (Fast) 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="7bd1d-251">일반 Windows에 대 한 17728 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-252">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-252">WSL</span></span>
* <span data-ttu-id="7bd1d-253">WSL 데 KeQueryInterruptTimePrecise KeQueryPerformanceCounter 대신 [GH 3252] 오버플로가 발생 하지 않도록 전환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="7bd1d-254">Ptrace 연결 월 [GH 1731] 시스템 호출에서 잘못 된 반환 값이 발생</span><span class="sxs-lookup"><span data-stu-id="7bd1d-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="7bd1d-255">다양 한 AF_UNIX 관련 된 수정 사항을 문제 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="7bd1d-256">WSL interop 현재 작업 디렉터리를 5 대 미만의 자 [GH 3379] 이면 실패를 일으킬 수 있는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="7bd1d-257">빌드 18204 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-258">일반 Windows에 대 한 18204 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-259">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-259">WSL</span></span>
* <span data-ttu-id="7bd1d-260">Edge 트리거 epoll 이벤트 [GH 3276]의 선택을 취소 하는 파일 시스템 inadvertenly을 파이프</span><span class="sxs-lookup"><span data-stu-id="7bd1d-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7bd1d-261">Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="7bd1d-262">17723 (Fast) 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="7bd1d-263">일반 Windows에 대 한 17723 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-264">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-264">WSL</span></span>
* <span data-ttu-id="7bd1d-265">존재 하지 않는 포트 [GH 3286]에 대 한 루프백 연결 실패 한 두 번째 지연을 방지합니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="7bd1d-266">/Proc/sys/fs/file-max 스텁 파일 [GH 2893]를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="7bd1d-267">보다 정확 하 게 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="7bd1d-268">PR_SET_PTRACER 지원 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="7bd1d-269">Edge 트리거 epoll 이벤트 [GH 3276]의 선택을 취소 하는 파일 시스템 inadvertenly을 파이프</span><span class="sxs-lookup"><span data-stu-id="7bd1d-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7bd1d-270">Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="7bd1d-271">17713 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-271">Build 17713</span></span>
<span data-ttu-id="7bd1d-272">일반 Windows에 대 한 17713 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-273">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-273">WSL</span></span>
* <span data-ttu-id="7bd1d-274">향상 된 좀비 지원 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="7bd1d-275">[GH 1493] Windows interop 동작을 제어 하기 위한 wsl.conf 항목 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="7bd1d-276">항상 그렇지는 않음 UNIX 소켓 패밀리 형식을 [GH 1774]를 반환 하는 getsockname에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="7bd1d-277">TIOCSTI [GH 1863]에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="7bd1d-278">비블로킹 소켓 연결 중 쓰기 시도 [GH 2846] EAGAIN 반환할지</span><span class="sxs-lookup"><span data-stu-id="7bd1d-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="7bd1d-279">탑재 된 Vhd [GH 3246에 3291]에서 interop를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="7bd1d-280">루트 폴더 [GH 3304]에서 문제를 확인 하는 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="7bd1d-281">TTY 키보드 ioctl KDGKBTYPE, KDGKBMODE 및 KDSKBMODE 제한적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="7bd1d-282">Windows UI 응용 프로그램은 백그라운드에서 시작 하는 경우에 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="7bd1d-283">17704 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-283">Build 17704</span></span>
<span data-ttu-id="7bd1d-284">일반 Windows에 대 한 17704 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-285">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-285">WSL</span></span>
* <span data-ttu-id="7bd1d-286">Wsl-u 또는--사용자 옵션 [GH 1203] 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="7bd1d-287">빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="7bd1d-288">Unix 소켓 연결이 끊긴된 피어 자격 증명 [GH 3183]를 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="7bd1d-289">EAGAIN [GH 3191]를 사용 하 여 무기한 실패 무중단 Unix 소켓</span><span class="sxs-lookup"><span data-stu-id="7bd1d-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="7bd1d-290">대/소문자 = off는 새 기본 drvfs 탑재 [GH 2937, 3212, 3328] 형식</span><span class="sxs-lookup"><span data-stu-id="7bd1d-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="7bd1d-291">참조 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="7bd1d-292">배포 실행을 중지 하려면 종료/wslconfig를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="7bd1d-293">빌드 17692</span><span class="sxs-lookup"><span data-stu-id="7bd1d-293">Build 17692</span></span>
<span data-ttu-id="7bd1d-294">일반 Windows에 대 한 17692 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-295">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-295">WSL</span></span>
* <span data-ttu-id="7bd1d-296">공간을 사용 하 여 경로 올바르게 처리 하지 않는 메뉴 항목 WSL 셸 컨텍스트를 사용 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="7bd1d-297">확장된 특성으로 단위 디렉터리에 대/소문자 구분. 노출</span><span class="sxs-lookup"><span data-stu-id="7bd1d-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="7bd1d-298">ARM64: 캐시 유지 관리 작업을 에뮬레이트하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="7bd1d-299">확인할 [dotnet 문제](https://github.com/dotnet/core/issues/1561)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="7bd1d-300">DrvFs: 개인 범위에 해당 하는 문자는 이스케이프 된 문자는 이스케이프을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="7bd1d-301">빌드 17686</span><span class="sxs-lookup"><span data-stu-id="7bd1d-301">Build 17686</span></span>
<span data-ttu-id="7bd1d-302">일반 Windows에 대 한 17686 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-303">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-303">WSL</span></span>
* <span data-ttu-id="7bd1d-304">ELF 파서 인터프리터 길이 유효성 검사 [GH 3154]에서 해제-오류 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="7bd1d-305">과거의 시간을 사용 하 여 WSL 절대 타이머 [GH 3091] 실행 안 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="7bd1d-306">새로 만든된 재분석 지점을 부모 디렉터리에 따라서 나와 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="7bd1d-307">원자 단위로 DrvFs에서 대/소문자 구분 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="7bd1d-308">17677 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-308">Build 17677</span></span>
<span data-ttu-id="7bd1d-309">일반 Windows에 대 한 17677 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-310">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-310">WSL</span></span>
* <span data-ttu-id="7bd1d-311">추가 문제를 해결 하 고 다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7bd1d-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-312">[GH 2712]</span></span>
* <span data-ttu-id="7bd1d-313">고정된 WSL UMCI을 사용 하는 경우 오류를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="7bd1d-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="7bd1d-315">17666 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-315">Build 17666</span></span>
<span data-ttu-id="7bd1d-316">일반 Windows에 대 한 17666 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-317">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="7bd1d-318">경고: WSL에서 일부 AMD 칩셋 [GH 3134] 실행 방지 하는 문제가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="7bd1d-319">해결 방법은 준비을 높일 해당 참가자 빌드 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="7bd1d-320">WSL [GH 437 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="7bd1d-321">사용 하려면 보류 shift 및 탐색기 창에서 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="7bd1d-322">Unix 소켓 비차단 동작 [GH 2822, 3100] 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="7bd1d-323">GH 2026에 보고 된 NETLINK 명령을 중지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="7bd1d-324">탑재 전파 플래그 [GH 2911]에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="7bd1d-325">자르기 유발 하지 inotify 이벤트 [GH 2978]를 사용 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="7bd1d-326">추가-셸 없이 단일 바이너리를 호출 하는 wsl.exe exec 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="7bd1d-327">추가-특정 배포판을 선택 하려면 wsl.exe에 대 한 배포 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="7bd1d-328">빌드 17655 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-329">일반 Windows에 대 한 17655 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-330">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-330">WSL</span></span>
* <span data-ttu-id="7bd1d-331">Dmesg 제한적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-331">Limited support for dmesg.</span></span> <span data-ttu-id="7bd1d-332">응용 프로그램 dmesg를 로깅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="7bd1d-333">WSL 드라이버 dmesg를 제한 된 정보를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="7bd1d-334">나중에이 드라이버에서 다른 정보/진단 전달할 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="7bd1d-335">참고: dmesg를 통해 현재 지원 되는 `/dev/kmsg` 장치 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="7bd1d-336">`syslog` sycall 인터페이스 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="7bd1d-337">따라서 몇 가지는 `dmesg` 명령줄 옵션 등 `-S`, `-C` 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="7bd1d-338">다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 있습니다 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7bd1d-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="7bd1d-340">빌드 17639 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-341">일반 Windows에 대 한 17639 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-342">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-342">WSL</span></span>
* <span data-ttu-id="7bd1d-343">기본 gid 및 네이티브 [GH 3042]에 맞게 직렬 장치 모드 변경</span><span class="sxs-lookup"><span data-stu-id="7bd1d-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="7bd1d-344">이제 DrvFs 확장 된 특성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="7bd1d-345">참고: DrvFs 확장 된 특성의 이름에 몇 가지 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="7bd1d-346">특히, 일부 문자 (같은 '/', ':' 및 '\*') 허용 되지 않습니다 되며 확장 특성 이름은 대/소문자 구분 DrvFs에서 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="7bd1d-347">17133 (Fast) 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="7bd1d-348">일반 Windows에 대 한 17133 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-349">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-349">WSL</span></span>
* <span data-ttu-id="7bd1d-350">WSL에서 중지를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-350">Fix for hang in WSL.</span></span> <span data-ttu-id="7bd1d-351">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="7bd1d-352">17128 (Fast) 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="7bd1d-353">일반 Windows에 대 한 17128 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-354">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-354">WSL</span></span>
* <span data-ttu-id="7bd1d-355">없음</span><span class="sxs-lookup"><span data-stu-id="7bd1d-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="7bd1d-356">빌드 17627 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-357">일반 Windows에 대 한 17627 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-358">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-358">WSL</span></span>
* <span data-ttu-id="7bd1d-359">Futex pi 인식 작업에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="7bd1d-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-360">[GH 1006]</span></span>
    * <span data-ttu-id="7bd1d-361">우선 순위는 현재 지원 되는 WSL 기능 제한 사항이 있지만 표준 사용을 차단 해야 하므로 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="7bd1d-362">WSL 프로세스에 대 한 Windows 방화벽 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="7bd1d-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-363">[GH 1852]</span></span>
    * <span data-ttu-id="7bd1d-364">예를 들어는 WSL 수 있도록 모든 포트에서 수신 대기를 관리자 권한 Windows cmd를 사용 하 여 python 처리: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="7bd1d-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="7bd1d-365">방화벽 규칙을 추가 하는 방법에 대 한 자세한 내용은 참조 하세요. [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="7bd1d-366">Wsl.exe를 사용 하는 경우 사용자의 기본 셸을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="7bd1d-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-367">[GH 2372]</span></span>
* <span data-ttu-id="7bd1d-368">모든 네트워크 인터페이스가 이더넷으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="7bd1d-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-369">[GH 2996]</span></span>
* <span data-ttu-id="7bd1d-370">/Etc/passwd 손상 된 파일의 향상 된 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="7bd1d-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-372">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-372">Console</span></span>
* <span data-ttu-id="7bd1d-373">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-374">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-374">LTP Results:</span></span>
<span data-ttu-id="7bd1d-375">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="7bd1d-376">빌드 17618 미리 건너 뛰 세요.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="7bd1d-377">일반 Windows에 대 한 17618 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-378">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-378">WSL</span></span>
* <span data-ttu-id="7bd1d-379">NT interop pseudoconsole 기능 소개 [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="7bd1d-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="7bd1d-380">레거시 설치 메커니즘 (lxrun.exe) 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="7bd1d-381">Microsoft Store 통해 배포를 설치 하기 위한 메커니즘을 지원 되는 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-382">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-382">Console</span></span>
* <span data-ttu-id="7bd1d-383">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-384">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-384">LTP Results:</span></span>
<span data-ttu-id="7bd1d-385">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="7bd1d-386">빌드 17110</span><span class="sxs-lookup"><span data-stu-id="7bd1d-386">Build 17110</span></span>
<span data-ttu-id="7bd1d-387">일반 Windows에 대 한 17110 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-388">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-388">WSL</span></span>
* <span data-ttu-id="7bd1d-389">/Init Windows [GH 2928]에서 종료 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="7bd1d-390">이제 DrvFs 기본적으로 디렉터리 당 대/소문자 구분을 사용 (해당 하는 "대/소문자 dir =" 탑재 옵션).</span><span class="sxs-lookup"><span data-stu-id="7bd1d-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="7bd1d-391">사용 하 여 "사례 force =" (이전 동작) 레지스트리 키를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="7bd1d-392">사용 하도록 설정 하려면 다음 명령을 실행 "대/소문자 force =" 사용 해야 할 경우: reg HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="7bd1d-393">WSL를 사용 하 여 대/소문자 구분 해야 하는 Windows의 이전 버전에서 만든 기존 디렉터리에 있는 fsutil.exe를 사용 하 여 표시할으로 대/소문자 구분: fsutil.exe 파일 setcasesensitiveinfo <path> 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="7bd1d-394">NULL 종료 uname syscall에서 반환 된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-395">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-395">Console</span></span>
* <span data-ttu-id="7bd1d-396">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-397">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-397">LTP Results:</span></span>
<span data-ttu-id="7bd1d-398">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="7bd1d-399">17107 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-399">Build 17107</span></span>
<span data-ttu-id="7bd1d-400">일반 Windows에 대 한 17107 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-401">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-401">WSL</span></span>
* <span data-ttu-id="7bd1d-402">마스터 pty 끝점 [GH 2552]에서 TCSETSF 및 TCSETSW를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="7bd1d-403">Interop 동시 프로세스를 시작 [GH 2813] EINVAL 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="7bd1d-404">PTRACE_ATTACH /proc/pid/status에서 적절 한 추적 상태를 표시 하도록 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="7bd1d-405">수정 경합 CLEARTID와 SETTID 플래그를 사용 하 여 단기 실행 프로세스를 복제 하는 위치는 TID 주소 선택을 취소 하지 않고 종료 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="7bd1d-406">사전 17093 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드할 때 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="7bd1d-407">17093 파일 시스템 변경 내용에 대 한 자세한 내용은 릴리스 정보 참조 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-408">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-408">Console</span></span>
* <span data-ttu-id="7bd1d-409">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-410">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-410">LTP Results:</span></span>
<span data-ttu-id="7bd1d-411">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="7bd1d-412">17101 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-412">Build 17101</span></span>
<span data-ttu-id="7bd1d-413">일반 Windows에 대 한 17101 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-414">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-414">WSL</span></span>
* <span data-ttu-id="7bd1d-415">Signalfd 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-415">Support for signalfd.</span></span> <span data-ttu-id="7bd1d-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-416">[GH 129]</span></span>
* <span data-ttu-id="7bd1d-417">파일 이름을 개인 유니코드 문자로 인코딩하여 NTFS의 잘못 된 문자가 포함 된 지원.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="7bd1d-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-418">[GH 1514]</span></span>
* <span data-ttu-id="7bd1d-419">자동 탑재 쓰기를 지원 하지 않는 경우 읽기 전용으로 대체가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="7bd1d-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-420">[GH 2603]</span></span>
* <span data-ttu-id="7bd1d-421">유니코드 서로게이트 쌍 (예:이 모 지 자)의 붙여넣기를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="7bd1d-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-422">[GH 2765]</span></span>
* <span data-ttu-id="7bd1d-423">/Proc /sys에 의사 (pseudo) 파일은 읽기 반환 쓰고 준비 선택, 폴링, epoll, et al [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="7bd1d-424">서비스 레지스트리 변조 또는 손상 된 경우 무한 루프로 이동 될 수 있는 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="7bd1d-425">Netlink iproute2의 최신 (업스트림 4.14) 버전을 사용 하는 메시지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-426">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-426">Console</span></span>
* <span data-ttu-id="7bd1d-427">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-428">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-428">LTP Results:</span></span>
<span data-ttu-id="7bd1d-429">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="7bd1d-430">17093 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-430">Build 17093</span></span>
<span data-ttu-id="7bd1d-431">일반 Windows에 대 한 17093 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="7bd1d-432">중요:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-432">Important:</span></span>
<span data-ttu-id="7bd1d-433">WSL이이 빌드로 업그레이드 후 처음으로 시작 하는 경우 Linux 파일 시스템 디렉터리를로 업그레이드 하는 일부 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="7bd1d-434">WSL 느리게 시작 하는 것 처럼 하므로 몇 분 정도 걸릴이 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="7bd1d-435">스토어에서 설치한 각 배포에 대 한 후에 발생 되어야이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="7bd1d-436">DrvFs에서 대/소문자 구분 지원을 개선.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="7bd1d-437">이제 DrvFs 디렉터리별 대/소문자 구분을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="7bd1d-438">새 플래그를 설정할 수 있는 해당 디렉터리에서 모든 작업을 처리 하도록 표시 하는 디렉터리와 대/소문자 구분, 대/소문자만 다른 파일 잘못 열려는 Windows 응용 프로그램을 허용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="7bd1d-439">DrvFs에 디렉터리 당 기준 대/소문자 구분을 제어 하는 새 탑재 옵션</span><span class="sxs-lookup"><span data-stu-id="7bd1d-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="7bd1d-440">대/소문자 force =: 모든 디렉터리와 대/소문자 구분 (드라이브 루트) 제외 하 고 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="7bd1d-441">WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="7bd1d-442">이 새 디렉터리를 대/소문자 구분 표시를 제외 하 고 레거시 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="7bd1d-443">대/소문자 = dir: 디렉터리별 대/소문자 구분 플래그를 사용 하 여 디렉터리만 대/소문자; 다른 디렉터리는 대/소문자 구분.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="7bd1d-444">WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="7bd1d-445">대/소문자 = off: 디렉터리별 대/소문자 구분 플래그를 사용 하 여 디렉터리만 대/소문자; 다른 디렉터리는 대/소문자 구분.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="7bd1d-446">WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="7bd1d-447">참고: 이전 릴리스에서 WSL에서 만든 디렉터리 없는 설정 처리 되지 것입니다 있도록으로 대/소문자 구분 사용 하는 경우이 플래그는 "사례 dir =" 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="7bd1d-448">기존 디렉터리에서이 플래그를 설정 하는 방법을 곧 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="7bd1d-449">이러한 옵션을 사용 하 여 탑재의 예 (기존 드라이브에서 먼저 탑재 해제 해야 다양 한 옵션을 사용 하 여 탑재할 수 전에): sudo mount-t drvfs c: mnt은 / c o 사례 dir =</span><span class="sxs-lookup"><span data-stu-id="7bd1d-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="7bd1d-450">지금은 경우 = 강제 여전히 기본 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="7bd1d-451">이 대/소문자를 변경할 수는 나중에 dir =.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="7bd1d-452">이제 사용할 수 있습니다 슬래시 Windows 경로 예: DrvFs, 탑재 하는 경우: sudo-t drvfs //server/share /mnt/share 탑재</span><span class="sxs-lookup"><span data-stu-id="7bd1d-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="7bd1d-453">이제 WSL 인스턴스 시작 [GH 2636] 중 /etc/fstab 파일을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="7bd1d-454">이 자동으로 DrvFs 드라이브를 탑재 하기 전에 작업 수행 fstab에서 이미 탑재 된 드라이브가 됩니다 하지 다시 탑재할 수 자동으로 특정 드라이브에 대 한 탑재 지점을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="7bd1d-455">이 동작은 해제할 수 있습니다 wsl.conf를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="7bd1d-456">/Proc의 탑재를 mountinfo mountstats 파일에 백슬래시 및 공백 [GH 2799]와 같은 특수 문자가 올바르게 이스케이프</span><span class="sxs-lookup"><span data-stu-id="7bd1d-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="7bd1d-457">이제 메타 데이터를 사용 하는 경우 WSL 기호화 된 링크 또는 fifos 및 소켓 같은 DrvFs를 사용 하 여 만든 특수 한 파일 복사 및 Windows에서 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="7bd1d-458">WSL은 wsl.conf를 사용 하 여 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="7bd1d-459">하위 시스템을 시작할 때마다 적용 되는 WSL에서 특정 기능을 자동으로 구성 하는 방법을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="7bd1d-460">자동 탑재 옵션 및 네트워크 구성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="7bd1d-461">자세한 정보에 대 한이 블로그 게시물에: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="7bd1d-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="7bd1d-462">WSL에서 Linux 프로세스와 Windows 네이티브 프로세스 사이의 소켓 연결을 허용 하는 AF_UNIX</span><span class="sxs-lookup"><span data-stu-id="7bd1d-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="7bd1d-463">WSL 및 Windows 응용 프로그램 이제 Unix 소켓을 통해 서로 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="7bd1d-464">Windows에서 서비스를 실행 하 여 WSL 및 Windows 앱에 사용할 수 있도록 하 려 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="7bd1d-465">이제 Unix 소켓을 사용 하 여 가능한입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="7bd1d-466">블로그에서 자세한 내용을 게시물 읽기 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="7bd1d-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-467">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-467">WSL</span></span>
* <span data-ttu-id="7bd1d-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="7bd1d-469">CLONE_PTRACE 및 CLONE_UNTRACED [GH 121, 2781] 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="7bd1d-470">복제 [GH 121, 2781]에서 비 SIGCHLD 종료 신호를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="7bd1d-471">스텁 /proc/sys/fs/inotify/max_user_instances 및 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="7bd1d-472">0이 아닌 오프셋 [GH 1884]를 사용 하 여 부하 헤더를 포함 하는 ELF 이진 파일을 로드 중 오류 발생</span><span class="sxs-lookup"><span data-stu-id="7bd1d-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="7bd1d-473">이미지를 로드할 때 후행 페이지 바이트 비워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="7bd1d-474">여기서 execve 프로세스를 자동으로 종료 하는 경우를 줄이려면</span><span class="sxs-lookup"><span data-stu-id="7bd1d-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-475">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-475">Console</span></span>
* <span data-ttu-id="7bd1d-476">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-477">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-477">LTP Results:</span></span>
<span data-ttu-id="7bd1d-478">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="7bd1d-479">빌드 17083</span><span class="sxs-lookup"><span data-stu-id="7bd1d-479">Build 17083</span></span>
<span data-ttu-id="7bd1d-480">일반 Windows에 대 한 17083 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-481">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-481">WSL</span></span>
* <span data-ttu-id="7bd1d-482">[GH 2798, 2801, 2857] epoll와 관련 된 고정된 버그 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="7bd1d-483">ASLR [GH 1185, 2870]을 해제 하는 경우 고정된 중지</span><span class="sxs-lookup"><span data-stu-id="7bd1d-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="7bd1d-484">Mmap 작업이 표시 원자성 [GH 2732] 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-485">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-485">Console</span></span>
* <span data-ttu-id="7bd1d-486">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-487">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-487">LTP Results:</span></span>
<span data-ttu-id="7bd1d-488">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="7bd1d-489">17074 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-489">Build 17074</span></span>
<span data-ttu-id="7bd1d-490">일반 Windows에 대 한 17074 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-491">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-491">WSL</span></span>
* <span data-ttu-id="7bd1d-492">고정 된 저장소 형식의 DrvFs 메타 데이터 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="7bd1d-493">**중요:** 이 빌드는 잘못 되거나 전혀 표시 되기 전의 DrvFs 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="7bd1d-494">영향을 받는 파일을 수정 하려면 메타 데이터를 다시 적용할 chmod 및 chown를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="7bd1d-495">여러 신호 및 다시 시작 가능한 syscall를 사용 하 여 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-496">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-496">Console</span></span>
* <span data-ttu-id="7bd1d-497">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-498">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-498">LTP Results:</span></span>
<span data-ttu-id="7bd1d-499">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="7bd1d-500">17063 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-500">Build 17063</span></span>
<span data-ttu-id="7bd1d-501">일반 Windows에 대 한 17063 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7bd1d-502">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-502">WSL</span></span>
* <span data-ttu-id="7bd1d-503">DrvFs 추가 Linux 메타 데이터를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="7bd1d-504">따라서, 소유자 및 chmod/chown 그리고 fifos, unix 소켓 및 장치 파일과 같은 특수 한 파일의 생성을 사용 하 여 파일의 모드를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="7bd1d-505">이 사용 되지 기본적으로 현재 여전히 실험적이 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="7bd1d-506">**참고:**  DrvFs에서 사용 하는 메타 데이터 형식에서 버그를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="7bd1d-507">메타 데이터 실험에 대 한이 빌드에 작동 하는 동안 이후 빌드 올바르게으로이 빌드에 의해 만들어진 메타 데이터를 읽지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="7bd1d-508">수정 된 파일의 소유자를 수동으로 업데이트 해야 하 고 사용자 지정 장치 ID 사용 하 여 장치를 다시 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="7bd1d-509">메타 데이터 옵션을 사용 하 여 탑재 DrvFs을 사용 하려면 (기존 탑재를 사용 하려면 먼저 탑재 해제 해야 해당):</span><span class="sxs-lookup"><span data-stu-id="7bd1d-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="7bd1d-510">Linux 권한은 파일에 추가 메타 데이터로 추가한 Windows 사용 권한에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="7bd1d-511">기억 메타 데이터를 제거할 수 있습니다 Windows 편집기를 사용 하 여 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="7bd1d-512">이 경우 파일의 기본 권한으로 되돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="7bd1d-513">메타 데이터 없이 제어 파일에 추가 탑재 옵션 DrvFs입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="7bd1d-514">uid: 모든 파일의 소유자에 사용 된 사용자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="7bd1d-515">gid: 모든 파일의 소유자에 사용 된 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="7bd1d-516">umask: 모든 파일 및 디렉터리를 제외 하려면 사용 권한 마스크를 8 진수입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="7bd1d-517">fmask: 제외할 모든 일반 파일에 대 한 사용 권한 마스크를 8 진수입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="7bd1d-518">dmask: 모든 디렉터리를 제외 하려면 사용 권한 마스크를 8 진수입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="7bd1d-519">예를 들어 다음과 같은 가치를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="7bd1d-520">메타 데이터 없이 파일에 대 한 기본 사용 권한을 지정 하는 메타 데이터 옵션을 사용 하 여 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="7bd1d-521">새 환경 변수를 도입 `WSLENV`를 환경 변수 WSL 및 Win32 간에 전달 되는 방식을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="7bd1d-522">이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="7bd1d-523">`WSLENV` Win32에서 WSL 프로세스 또는 WSL에서 Win32 프로세스를 시작할 때 포함할 수 있는 환경 변수의 콜론으로 구분 된 목록이입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="7bd1d-524">각 변수 슬래시 뒤에 변환 하는 방법을 지정 하는 플래그를 사용 하 여 접미사 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="7bd1d-525">p: 값은 Win32 경로 및 WSL 경로 간에 변환 해야 하는 경로.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="7bd1d-526">l: 값은 경로의 목록.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-526">l: The value is a list of paths.</span></span> <span data-ttu-id="7bd1d-527">WSL를에서 콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="7bd1d-528">Win32에서 세미콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="7bd1d-529">u: 값만 포함 해야 WSL Win32에서 호출 하는 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="7bd1d-530">w: 값만 포함 해야 WSL에서 Win32를 호출 하는 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="7bd1d-531">설정할 수 있습니다 `WSLENV` .bashrc 또는 사용자에 대 한 사용자 지정 Windows 환경에서.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="7bd1d-532">drvfs 탑재 tar에서 타임 스탬프를 올바르게 유지 cp-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="7bd1d-533">drvfs symlink (GH 2641) 정확한 크기를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="7bd1d-534">매우 큰 IO 크기 (GH 2653)에 대 한 작동에 대 한 읽기/쓰기</span><span class="sxs-lookup"><span data-stu-id="7bd1d-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="7bd1d-535">프로세스 그룹 (GH 2534) Id 사용 하 여 waitpid 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="7bd1d-536">향상 된 mmap 성능을 상당히 큰 예약 지역 선택 합니다. ghc 빨라집니다 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="7bd1d-537">READ_IMPLIES_EXEC;에 대 한 성격 지원 최대 및 clisp (GH 1185)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="7bd1d-538">mprotect PROT_GROWSDOWN; 지원 수정 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="7bd1d-539">모드를 과도 하 게 페이지 오류 수정 수정 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="7bd1d-540">복제는 많은 플래그 조합이 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="7bd1d-541">선택/epoll epoll 파일 (이전에 아무)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="7bd1d-542">구현 되지 않은 syscall의 ptrace를 알립니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="7bd1d-543">Resolv.conf 이름 서버 [GH 2694]을 생성 하는 경우 등록 되지 않은 인터페이스를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="7bd1d-544">실제 주소가 없는 네트워크 인터페이스를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="7bd1d-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-545">[GH 2685]</span></span>
* <span data-ttu-id="7bd1d-546">추가 버그 수정 및 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="7bd1d-547">Windows에서 개발자에 게 제공 되는 Linux 도구</span><span class="sxs-lookup"><span data-stu-id="7bd1d-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="7bd1d-548">Windows 명령줄 도구 체인에 bsdtar (tar) 및 넘기기가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="7bd1d-549">읽기 [이 블로그](https://aka.ms/tarcurlwindows) 이러한 두 가지 새로운 도구를 추가 하는 방법에 대 한 자세한 정보를 어떻게 개발자 환경에서 Windows 셰이핑 하는 이러한 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="7bd1d-550">`AF_UNIX` Windows Insider SDK (17061 이상)에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="7bd1d-551">읽기 [이 블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) 에 대해 자세히 알아보려면 `AF_UNIX` 개발자가 Windows에서 사용할 수 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="7bd1d-552">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-552">Console</span></span>
* <span data-ttu-id="7bd1d-553">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-554">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-554">LTP Results:</span></span>
<span data-ttu-id="7bd1d-555">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="7bd1d-556">17046 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-556">Build 17046</span></span>

<span data-ttu-id="7bd1d-557">일반 Windows에 대 한 17046 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-558">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-559">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-559">WSL</span></span>
- <span data-ttu-id="7bd1d-560">활성 터미널을 하지 않고 실행 하는 프로세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="7bd1d-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="7bd1d-562">CLONE_VFORK 및 CLONE_VM 더 나은 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="7bd1d-563">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="7bd1d-564">WSL 네트워킹 작업에 대 한 TDI 필터 드라이버를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="7bd1d-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-565">[GH 1554]</span></span>
- <span data-ttu-id="7bd1d-566">특정 조건이 충족 되 면 DrvFs NT symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="7bd1d-567">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="7bd1d-568">링크 대상 상대 이어야 하 고 모든 탑재 지점 또는 symlink를 넘지 않아야 합니다 하며 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="7bd1d-569">사용자는 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (일반적으로 해야 wsl.exe 권한 시작)에 있어야 합니다. 개발자 모드가 켜져 하지 않는 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="7bd1d-570">다른 모든 상황에서 DrvFs 여전히 WSL symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="7bd1d-571">관리자 권한 및 권한 상승 되지 않은 WSL 인스턴스를 동시에 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="7bd1d-572">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="7bd1d-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="7bd1d-573">WSL <>-Windows 경로 변환을 수행 하는 wslpath를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="7bd1d-574">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="7bd1d-575">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-575">Console</span></span>
- <span data-ttu-id="7bd1d-576">수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-577">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-577">LTP Results:</span></span>
<span data-ttu-id="7bd1d-578">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="7bd1d-579">17040 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-579">Build 17040</span></span>

<span data-ttu-id="7bd1d-580">일반 Windows에 대 한 빌드 17040에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-581">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-582">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-582">WSL</span></span>
- <span data-ttu-id="7bd1d-583">17035 이후 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-584">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-584">Console</span></span>
- <span data-ttu-id="7bd1d-585">17035 이후 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-586">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-586">LTP Results:</span></span>
<span data-ttu-id="7bd1d-587">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="7bd1d-588">17035 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-588">Build 17035</span></span>

<span data-ttu-id="7bd1d-589">일반 Windows에 대 한 17035 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-590">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-591">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-591">WSL</span></span>
- <span data-ttu-id="7bd1d-592">DrvFs에서 파일에 액세스할 경우에 따라 EINVAL를 사용 하 여 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="7bd1d-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-594">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-594">Console</span></span>
- <span data-ttu-id="7bd1d-595">VT 모드에서 줄 삽입/삭제 하는 경우 몇 가지 색 손실입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-596">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-596">LTP Results:</span></span>
<span data-ttu-id="7bd1d-597">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="7bd1d-598">빌드 17025</span><span class="sxs-lookup"><span data-stu-id="7bd1d-598">Build 17025</span></span>

<span data-ttu-id="7bd1d-599">일반 Windows에 대 한 빌드 17025에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-600">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-601">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-601">WSL</span></span>
- <span data-ttu-id="7bd1d-602">새 포그라운드 프로세스 그룹 [GH 1653, 2510]의 초기 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="7bd1d-603">SIGHUP 배달 [GH 2496] 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="7bd1d-604">[GH 2497] 아무 것도 제공 하는 경우 기본 가상 브리지 이름을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="7bd1d-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="7bd1d-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="7bd1d-606">더 interop stdout/stderr 파이프를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="7bd1d-607">스텁 syncfs 시스템 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-608">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-608">Console</span></span>
- <span data-ttu-id="7bd1d-609">제 3 자 콘솔 [GH 111]에 대 한 입력된 VT 번역 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-610">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-610">LTP Results:</span></span>
<span data-ttu-id="7bd1d-611">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="7bd1d-612">17017 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-612">Build 17017</span></span>

<span data-ttu-id="7bd1d-613">일반 Windows에 대 한 17017 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-614">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-615">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-615">WSL</span></span>
- <span data-ttu-id="7bd1d-616">빈 ELF 프로그램 헤더 [GH 330]를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="7bd1d-617">비 대화형 사용자에 대 한 WSL 인스턴스를 만드는 LxssManager 허용 (ssh 지원 작업을 예약 하 고) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="7bd1d-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="7bd1d-618">WSL 지원 Win32-> WSL ("초기") 시나리오 [GH 1228]-> 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="7bd1d-619">Interop [GH 1614]를 통해 호출 되는 콘솔 응용 프로그램 종료에 대 한 제한적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="7bd1d-620">Devpts [GH 1948]에 대 한 탑재 옵션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="7bd1d-621">Ptrace 자식 시작 [GH 2333]를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="7bd1d-622">누락 된 일부 이벤트 [GH 2462] EPOLLET 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="7bd1d-623">PTRACE_GETSIGINFO에 대 한 더 많은 데이터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="7bd1d-624">Lseek 사용 하 여 Getdents 잘못 된 결과 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="7bd1d-625">자세한 데이터가 없는 파이프에서 입력을 기다리는 일부 Win32 interop 응용 프로그램 중단을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="7bd1d-626">O_ASYNC는 tty/pty 파일에 대 한 지원.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="7bd1d-627">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-628">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-628">Console</span></span>
- <span data-ttu-id="7bd1d-629">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-630">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-630">LTP Results:</span></span>
<span data-ttu-id="7bd1d-631">진행 중인 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="7bd1d-632">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="7bd1d-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="7bd1d-633">16288 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-633">Build 16288</span></span>

<span data-ttu-id="7bd1d-634">일반 Windows에 대 한 16288 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-635">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-636">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-636">WSL</span></span>
- <span data-ttu-id="7bd1d-637">올바르게 초기화 하 고 보고서 uid, gid 및 소켓 파일 설명자 [GH 2490]에 대 한 모드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="7bd1d-638">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-639">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-639">Console</span></span>
- <span data-ttu-id="7bd1d-640">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-641">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-641">LTP Results:</span></span>
<span data-ttu-id="7bd1d-642">16273 이후 변경 되지 않았습니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="7bd1d-643">16278 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-643">Build 16278</span></span>

<span data-ttu-id="7bd1d-644">일반 Windows에 대 한 162738 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-645">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-646">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-646">WSL</span></span>
- <span data-ttu-id="7bd1d-647">LX MM 상태 [GH 2415]를 분해 하는 경우 명시적으로 매핑된 뷰 파일을 백업 섹션의 매핑을 해제합니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="7bd1d-648">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-649">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-649">Console</span></span>
- <span data-ttu-id="7bd1d-650">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-651">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-651">LTP Results:</span></span>
<span data-ttu-id="7bd1d-652">16273 이후 변경 되지 않았습니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="7bd1d-653">16275 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-653">Build 16275</span></span>

<span data-ttu-id="7bd1d-654">일반 Windows에 대 한 162735 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-655">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-656">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-656">WSL</span></span>
- <span data-ttu-id="7bd1d-657">없는 WSL 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-658">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-658">Console</span></span>
- <span data-ttu-id="7bd1d-659">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-660">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-660">LTP Results:</span></span>
<span data-ttu-id="7bd1d-661">16273 이후 변경 되지 않았습니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="7bd1d-662">16273 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-662">Build 16273</span></span>

<span data-ttu-id="7bd1d-663">일반 Windows에 대 한 16273 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-664">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-665">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-665">WSL</span></span>
- <span data-ttu-id="7bd1d-666">디렉터리 [GH 2392]에 대 한 잘못 된 파일 형식에 DrvFs 경우에 따라 보고 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="7bd1d-667">프로그램 차단을 해제 하려면 NETLINK_KOBJECT_UEVENT 소켓 만들기는 사용 하 여 uevent 허용 [GH 1121, 2293, 2242, 2295 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="7bd1d-668">비차단 연결에 대 한 지원을 추가 [GH 903, 1391, 1584 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="7bd1d-669">구현 CLONE_FS 복제 시스템 호출 플래그 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="7bd1d-670">탭 또는 따옴표 NT interop [GH 1625, 2164]에서 올바르게 처리 하지 못할 경우 관련 된 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="7bd1d-671">WSL를 다시 시작 하려고 하는 동안 오류가 발생 했습니다. [GH 651, 2095] 인스턴스 액세스 거부 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="7bd1d-672">Futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업 [GH 2242]를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="7bd1d-673">다양 한 SysFs 파일 [GH 2214]에 대 한 권한을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="7bd1d-674">설치 [GH 2290] 중 Haskell 스택 중단을 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="7bd1d-675">'C' binfmt_misc 구현 ' o ' 및 'P' 플래그 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="7bd1d-676">추가 /proc/sys/kernel /shmmax /shmmni /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="7bd1d-677">Ioprio_set 시스템 호출 [GH 498]에 대 한 부분 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="7bd1d-678">스텁 SO_REUSEPORT & SO_PASSCRED netlink 소켓 [GH 69]에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="7bd1d-679">배포를 현재 중이면 RegisterDistribuiton에서 다른 오류 코드를 반환 설치 또는 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="7bd1d-680">Wslconfig.exe 통해 부분적으로 설치 된 WSL 배포의 등록 취소 허용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="7bd1d-681">Udp::msg_peek에서 python 소켓 테스트 중지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="7bd1d-682">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-683">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-683">Console</span></span>
- <span data-ttu-id="7bd1d-684">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-685">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-685">LTP Results:</span></span>
<span data-ttu-id="7bd1d-686">총 테스트: 1904</span><span class="sxs-lookup"><span data-stu-id="7bd1d-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="7bd1d-687">총 건너뛴 테스트: 209</span><span class="sxs-lookup"><span data-stu-id="7bd1d-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="7bd1d-688">총 오류 횟수: 229</span><span class="sxs-lookup"><span data-stu-id="7bd1d-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="7bd1d-689">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="7bd1d-690">빌드 16257</span><span class="sxs-lookup"><span data-stu-id="7bd1d-690">Build 16257</span></span>

<span data-ttu-id="7bd1d-691">일반 Windows에 대 한 16257 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-692">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-693">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-693">WSL</span></span>
- <span data-ttu-id="7bd1d-694">구현 prlimit64 시스템 호출</span><span class="sxs-lookup"><span data-stu-id="7bd1d-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="7bd1d-695">Ulimit-n (setrlimit RLIMIT_NOFILE)에 대 한 지원을 추가 [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="7bd1d-696">TCP 소켓 [GH 2351]에 대 한 스텁을 MSG_MORE</span><span class="sxs-lookup"><span data-stu-id="7bd1d-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="7bd1d-697">잘못 된 AT_EXECFN 보조 벡터 동작 [GH 2133] 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="7bd1d-698">콘솔/tty에 대 한 복사/붙여넣기 동작을 수정 하 고 [GH 2204, 2131]를 처리 하는 더 나은 가득 찬 버퍼를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="7bd1d-699">집합-사용자 ID 및 집합-그룹-ID 프로그램 [GH 2031]에 대 한 보조 벡터에서 AT_SECURE 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="7bd1d-700">유사 터미널 마스터 엔드포인트 TIOCPGRP [GH 1063]를 처리 하지 못할 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="7bd1d-701">수정 lseek LxFs [GH 2310]의 디렉터리 부분까지 되 감아야 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="7bd1d-702">사용량이 [GH 1882] 후 /dev/ptmx 작동 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="7bd1d-703">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-704">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-704">Console</span></span>
- <span data-ttu-id="7bd1d-705">가로 줄/밑줄 Everywhere [GH 2168]에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="7bd1d-706">처리 순서를 닫으려면 [GH 2170] 어렵게 만드는 NPM 변경에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="7bd1d-707">이 새로운 색 구성표를 추가 합니다. https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="7bd1d-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-708">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-708">LTP Results:</span></span>
<span data-ttu-id="7bd1d-709">16251 이후 변경 되지 않았습니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-710">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-710">Syscall Support</span></span>
<span data-ttu-id="7bd1d-711">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-712">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="7bd1d-713">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="7bd1d-714">GitHub Issue 2392: Windows 폴더 WSL에서 인식할 수 없습니다...</span><span class="sxs-lookup"><span data-stu-id="7bd1d-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="7bd1d-715">빌드 16257 WSL에 문제를 통해 Windows 파일/폴더를 열거 하는 동안 `/mnt/c/...`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="7bd1d-716">이 문제는 해결 되었습니다 및에서 해제 되어야 참가자는 2017 년 8 월 14를 시작 하는 주 동안 빌드.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="7bd1d-717">16251 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-717">Build 16251</span></span>

<span data-ttu-id="7bd1d-718">일반 Windows에 대 한 16251 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-719">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-720">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-720">WSL</span></span>
- <span data-ttu-id="7bd1d-721">WSL 선택적 구성 요소에서 베타 태그 제거를 참조 하십시오 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) 세부 정보에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="7bd1d-722">저장 집합 uid 및 gid exec [GH 962, 1415, 2072]에서 집합-사용자 ID 및 집합-그룹-ID 바이너리를 제대로 초기화</span><span class="sxs-lookup"><span data-stu-id="7bd1d-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="7bd1d-723">ptrace PTRACE_O_TRACEEXIT [GH 555]에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="7bd1d-724">ptrace에 대 한 지원이 추가 되었습니다 PTRACE_GETFPREGS 및 PTRACE_GETREGSET NT_FPREGSET [GH 555]를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="7bd1d-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="7bd1d-725">무시 중지에 대해 ptrace를 고정 신호</span><span class="sxs-lookup"><span data-stu-id="7bd1d-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="7bd1d-726">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-727">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-727">Console</span></span>
- <span data-ttu-id="7bd1d-728">콘솔이 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-729">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-729">LTP Results:</span></span>
<span data-ttu-id="7bd1d-730">테스트 통과 수: 768</span><span class="sxs-lookup"><span data-stu-id="7bd1d-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="7bd1d-731">실패 한 테스트 수: 244</span><span class="sxs-lookup"><span data-stu-id="7bd1d-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="7bd1d-732">건너뛴된 테스트 수: 96</span><span class="sxs-lookup"><span data-stu-id="7bd1d-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="7bd1d-733">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="7bd1d-734">16241 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-734">Build 16241</span></span>

<span data-ttu-id="7bd1d-735">일반 Windows에 대 한 16241 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-736">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7bd1d-737">WSL</span><span class="sxs-lookup"><span data-stu-id="7bd1d-737">WSL</span></span>
- <span data-ttu-id="7bd1d-738">없는 WSL 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="7bd1d-739">콘솔</span><span class="sxs-lookup"><span data-stu-id="7bd1d-739">Console</span></span>
- <span data-ttu-id="7bd1d-740">원래 보고 교차 줄 dec 잘못 된 문자를 출력 하는 것에 대 한 수정 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="7bd1d-741">코드 페이지 65001 (utf8)에 표시 되는 출력 텍스트가 없습니다에 대 한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="7bd1d-742">선택 변경에서 색상표의 다른 부분에 하나의 색의 RGB 값에 대 한 변경 내용을 전송 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="7bd1d-743">이렇게 하면 콘솔 속성 시트를 사용 하 여 훨씬 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="7bd1d-744">Ctrl + S 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="7bd1d-745">굵게 표시 되지 않은 /-차원 없는 완전히 ANSI 이스케이프 코드 [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="7bd1d-746">콘솔 [GH 1706] Vim 색 테마를 올바르게 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="7bd1d-747">[GH 2149] 특정 문자를 붙여 넣을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="7bd1d-748">편집/명령줄 [GH ConEmu 1123]에 올려져 있는 경우 bash 창 크기 조정을 통한 리플로우 크기 조정 이상 하 게 상호 작용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="7bd1d-749">Ctrl-L 더티 화면 [GH 1978 년 5]을 떠날</span><span class="sxs-lookup"><span data-stu-id="7bd1d-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="7bd1d-750">HDPI [GH 1907]에서 VT를 표시할 때 콘솔 렌더링 버그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="7bd1d-751">Japansese 문자는 유니코드 문자 U + 30FB를 사용 하 여 생소할 [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="7bd1d-752">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="7bd1d-753">빌드 16237</span><span class="sxs-lookup"><span data-stu-id="7bd1d-753">Build 16237</span></span>

<span data-ttu-id="7bd1d-754">일반 Windows에 대 한 16237 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-755">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-755">Fixed</span></span>
- <span data-ttu-id="7bd1d-756">EAs 없이 파일 lxfs (루트, 루트, 0000)에 대 한 기본 특성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="7bd1d-757">확장 된 특성을 사용 하는 배포에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="7bd1d-758">Getdents getdents64로 반환 되는 항목에 대 한 안쪽 여백을 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="7bd1d-759">수정 [GH 2068] shmctl SHM_STAT 시스템 호출에 대 한 사용 권한 확인</span><span class="sxs-lookup"><span data-stu-id="7bd1d-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="7bd1d-760">Tty [GH 2231]에 대 한 잘못 된 초기 epoll 고정된 상태</span><span class="sxs-lookup"><span data-stu-id="7bd1d-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="7bd1d-761">모든 항목 [GH 2077]를 반환 하지 않는 DrvFs readdir 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="7bd1d-762">LxFs 해결 readdir 파일이 있는 경우 [GH 2077] 연결이 끊어진</span><span class="sxs-lookup"><span data-stu-id="7bd1d-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="7bd1d-763">연결 되지 않은 drvfs 파일은 procfs 통해 다시 열 수</span><span class="sxs-lookup"><span data-stu-id="7bd1d-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="7bd1d-764">WSL 기능을 사용 하지 않도록 설정 하는 것에 대 한 전역 레지스트리 키 재정의 추가 (interop / 탑재 드라이브)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="7bd1d-765">DrvFs (및 LxFs)에 대 한 "상태"에 잘못 된 블록 수를 수정 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="7bd1d-766">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="7bd1d-767">16232 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-767">Build 16232</span></span>

<span data-ttu-id="7bd1d-768">일반 Windows에 대 한 16232 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-769">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-769">Fixed</span></span>
- <span data-ttu-id="7bd1d-770">없는 WSL 관련이 릴리스의 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="7bd1d-771">16226 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-771">Build 16226</span></span>

<span data-ttu-id="7bd1d-772">일반 Windows에 대 한 16226 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-773">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-773">Fixed</span></span>
- <span data-ttu-id="7bd1d-774">xattr 관련 syscall 지원 (getxattr setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="7bd1d-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="7bd1d-775">security.capablity xattr 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="7bd1d-776">특정 파일 시스템 및 비 MS SMB 서버를 포함 하 여 필터를 사용 하 여 향상 된 호환성.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="7bd1d-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-777">[GH #1952]</span></span>
- <span data-ttu-id="7bd1d-778">OneDrive 자리 표시자, GVFS 자리 표시자 및 Compact OS에 대 한 향상 된 지원 파일을 압축 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="7bd1d-779">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="7bd1d-780">16215 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-780">Build 16215</span></span>

<span data-ttu-id="7bd1d-781">일반 Windows에 대 한 16215 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-782">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-782">Fixed</span></span>
- <span data-ttu-id="7bd1d-783">WSL은 개발자 모드를 더 이상 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="7bd1d-784">Drvfs에서 디렉터리 연결을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="7bd1d-785">WSL 배포 appx 패키지 제거를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="7bd1d-786">개인 표시할 procfs 업데이트 및 매핑을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="7bd1d-787">Wslconfig.exe 부분적으로 설치 되거나 제거 되는 배포를 정리 하는 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="7bd1d-788">TCP 소켓에 대 한 IP_MTU_DISCOVER에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="7bd1d-789">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="7bd1d-790">프로토콜 패밀리가 AF_INADDR에 대 한 경로 대 한 유추 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="7bd1d-791">직렬 장치 개선 [GH 1929]입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="7bd1d-792">16199 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-792">Build 16199</span></span>

<span data-ttu-id="7bd1d-793">일반 Windows에 대 한 16199 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-794">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-794">Fixed</span></span>
- <span data-ttu-id="7bd1d-795">없는 WSL의에서 관련 변경 내용을 이러한 릴리스 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="7bd1d-796">16193 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-796">Build 16193</span></span>

<span data-ttu-id="7bd1d-797">일반 Windows에 대 한 16193 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-798">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-798">Fixed</span></span>
- <span data-ttu-id="7bd1d-799">SIGCONT 및 [GH 1973] 종료는 threadgroup이 보내는 간격 사이의 경합 상태</span><span class="sxs-lookup"><span data-stu-id="7bd1d-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="7bd1d-800">보고서 [GH 1840] FILE_DEVICE_CONSOLE 대신 FILE_DEVICE_NAMED_PIPE tty 및 pty 장치 변경</span><span class="sxs-lookup"><span data-stu-id="7bd1d-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="7bd1d-801">IP_OPTIONS에 대 한 SSH 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="7bd1d-802">Init 디먼 DrvFs 탑재 이동할 [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="7bd1d-803">NT symlink 따라 하는 데 DrvFs에서 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="7bd1d-804">16184 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-804">Build 16184</span></span>

<span data-ttu-id="7bd1d-805">일반 Windows에 대 한 16184 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-806">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-806">Fixed</span></span>
- <span data-ttu-id="7bd1d-807">Apt 패키지 유지 관리 작업 (lxrun.exe /update)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="7bd1d-808">고정 된 출력에 표시 되지 node.js [GH 1840] Windows 프로세스에서</span><span class="sxs-lookup"><span data-stu-id="7bd1d-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="7bd1d-809">Lxcore [GH 1794]의 맞춤 요구 사항 완화</span><span class="sxs-lookup"><span data-stu-id="7bd1d-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="7bd1d-810">시스템 호출의 필드가에서 AT_EMPTY_PATH 플래그의 처리가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="7bd1d-811">여기서 열린 핸들로 DrvFs 파일을 삭제 하면 정의 되지 않은 동작이 [GH 544,966,1357,1535,1615] 파일의 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="7bd1d-812">/ 등 호스트에서 Windows 호스트 파일 (%windir%\system32\drivers\etc\hosts) 항목 상속 이제 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="7bd1d-813">16179 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-813">Build 16179</span></span>

<span data-ttu-id="7bd1d-814">일반 Windows에 대 한 16179 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-815">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-815">Fixed</span></span>
- <span data-ttu-id="7bd1d-816">없는 WSL 이번이 주를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="7bd1d-817">16176 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-817">Build 16176</span></span>

<span data-ttu-id="7bd1d-818">일반 Windows에 대 한 16176 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-819">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-819">Fixed</span></span>

- [<span data-ttu-id="7bd1d-820">직렬 지원 사용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="7bd1d-821">추가 IP 소켓 옵션 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="7bd1d-822">Nginx/PHP-FPM에 파일 업로드) 하는 것 (동안 pwritev 함수 구현 [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="7bd1d-823">추가 IP 소켓 옵션 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="7bd1d-824">IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP 소켓 옵션에 대 한 지원 [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="7bd1d-825">앱 노드의 traceroute, dig, nslookup 호스트에 대 한 추가 IP (V6) _MTU 소켓 옵션</span><span class="sxs-lookup"><span data-stu-id="7bd1d-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="7bd1d-826">추가 IP 소켓 옵션 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="7bd1d-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="7bd1d-827">파일 시스템 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="7bd1d-828">탑재 되는 UNC 경로 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="7bd1d-829">Drvfs에서 CDFS 지원을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="7bd1d-830">Drvfs에서 네트워크 파일 시스템에 대 한 사용 권한을 올바르게 처리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="7bd1d-831">Drvfs에 원격 드라이브에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="7bd1d-832">FAT 사용 drvfs 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="7bd1d-833">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-834">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="7bd1d-834">LTP Results</span></span>
<span data-ttu-id="7bd1d-835">15042 이후 변경 하지 않고</span><span class="sxs-lookup"><span data-stu-id="7bd1d-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="7bd1d-836">16170 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-836">Build 16170</span></span>

<span data-ttu-id="7bd1d-837">일반 Windows에 대 한 16170 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="7bd1d-838">새 출시 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) WSL를 테스트 하기 위한 우리의 노력에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-839">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-839">Fixed</span></span>

- <span data-ttu-id="7bd1d-840">지원 소켓 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP 옵션 [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="7bd1d-841">PTRACE_OLDSETOPTIONS 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="7bd1d-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-842">[GH 1692]</span></span>
- <span data-ttu-id="7bd1d-843">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-844">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="7bd1d-844">LTP Results</span></span>
<span data-ttu-id="7bd1d-845">15042 이후 변경 하지 않고</span><span class="sxs-lookup"><span data-stu-id="7bd1d-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="7bd1d-846">빌드 15046 windows 10 크리에이터 스 업데이트</span><span class="sxs-lookup"><span data-stu-id="7bd1d-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="7bd1d-847">WSL 수정 또는 Windows 10 크리에이터 스 업데이트에 포함 될 예정인 기능을 더 이상 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="7bd1d-848">WSL에 대 한 릴리스 정보는 다음 주요 Windows 업데이트를 대상으로 하는 추가 기능에 대 한 주간에 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="7bd1d-849">빌드 15046 및 향후 참가자에 대 한 정보를 일반 Windows에 대 한 방문을 해제 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="7bd1d-850">15042 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-850">Build 15042</span></span>

<span data-ttu-id="7bd1d-851">일반 Windows에 대 한 15042 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-852">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-852">Fixed</span></span>

- <span data-ttu-id="7bd1d-853">로 끝나는 경로 제거 하는 동안 교착 상태가 해결 "..."</span><span class="sxs-lookup"><span data-stu-id="7bd1d-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="7bd1d-854">문제를 해결 함 위치 [GH 1683] 성공 시 0을 반환 하지 않는 FIONBIO</span><span class="sxs-lookup"><span data-stu-id="7bd1d-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="7bd1d-855">길이가 0 인 읽기 inet 데이터 그램 소켓의 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="7bd1d-856">Drvfs inode 조회 [GH 1675] 경합으로 인해 가능한 교착 상태 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="7bd1d-857">Unix 소켓 보조 데이터에 대 한 지원 확장 SCM_CREDENTIALS 및 SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="7bd1d-858">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-859">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-859">LTP Results:</span></span>
<span data-ttu-id="7bd1d-860">통과 한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="7bd1d-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="7bd1d-861">불합격 개수 (실패, 건너뜀 등...): 255</span><span class="sxs-lookup"><span data-stu-id="7bd1d-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="7bd1d-862">15031 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-862">Build 15031</span></span>

<span data-ttu-id="7bd1d-863">일반 Windows에 대 한 15031 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-864">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-864">Fixed</span></span>

- <span data-ttu-id="7bd1d-865">여기서 time(2) 오동작 산발적는 버그가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="7bd1d-866">고정 및 where 발급 \* SIGPROCMASK syscall 신호 마스크 손상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="7bd1d-867">프로세스 만들기 알림 WSL에서에서 이제 전체 명령줄 길이 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="7bd1d-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-868">[GH 1632]</span></span>
- <span data-ttu-id="7bd1d-869">WSL은 GDB 중단에 ptrace 통해 스레드 종료를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="7bd1d-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-870">[GH 1196]</span></span>
- <span data-ttu-id="7bd1d-871">과도 한 tmux IO 후 ptys가 중단 되는 버그가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="7bd1d-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-872">[GH 1358]</span></span>
- <span data-ttu-id="7bd1d-873">많은 시스템 호출 (futex semtimedop, ppoll, sigtimedwait, itimer, timer_create)에서 고정 된 제한 시간 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="7bd1d-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="7bd1d-874">추가 eventfd EFD_SEMAPHORE 지원 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="7bd1d-875">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-876">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-876">LTP Results:</span></span>
<span data-ttu-id="7bd1d-877">통과 한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="7bd1d-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="7bd1d-878">불합격 개수 (실패, 건너뜀 등...): 255</span><span class="sxs-lookup"><span data-stu-id="7bd1d-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7bd1d-879">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="7bd1d-880">15025 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-880">Build 15025</span></span>

<span data-ttu-id="7bd1d-881">일반 Windows에 대 한 15025 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-882">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-882">Fixed</span></span>

- <span data-ttu-id="7bd1d-883">해당 고장 grep 2.27 [GH 1578] 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="7bd1d-884">Eventfd2 syscall [GH 452]에 대 한 구현된 EFD_SEMAPHORE 플래그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="7bd1d-885">[Pid] /proc//net ipv6_route 구현 [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="7bd1d-886">Unix 스트림 소켓 [GH 393를 68]에 대 한 IO 지원 기반 신호</span><span class="sxs-lookup"><span data-stu-id="7bd1d-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="7bd1d-887">F_GETPIPE_SZ 및 F_SETPIPE_SZ [GH 1012] 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="7bd1d-888">Implement recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="7bd1d-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="7bd1d-889">Epoll_wait() 되지 않은 대기 하는 [GH 1609] 버그가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="7bd1d-890">/Proc/version_signature 구현</span><span class="sxs-lookup"><span data-stu-id="7bd1d-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="7bd1d-891">동일한 파이프 파일 설명자 두 참조 하는 경우 이제 tee syscall 실패 반환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="7bd1d-892">Unix 소켓에 대 한 SO_PEERCRED에 대 한 올바른 구현 된 동작</span><span class="sxs-lookup"><span data-stu-id="7bd1d-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="7bd1d-893">고정된 tkill syscall 잘못 된 매개 변수 처리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="7bd1d-894">Drvfs의 preformace 높이기 위해 변경 내용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="7bd1d-895">Ruby IO 차단에 대해 사소한 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="7bd1d-896">고정된 recvmsg() EINVAL inet 소켓 [GH 1296] MSG_DONTWAIT 플래그에 대 한 반환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="7bd1d-897">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-898">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-898">LTP Results:</span></span>
<span data-ttu-id="7bd1d-899">통과 한 테스트 수: 732</span><span class="sxs-lookup"><span data-stu-id="7bd1d-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="7bd1d-900">불합격 개수 (실패, 건너뜀 등...): 255</span><span class="sxs-lookup"><span data-stu-id="7bd1d-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7bd1d-901">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="7bd1d-902">빌드 15019</span><span class="sxs-lookup"><span data-stu-id="7bd1d-902">Build 15019</span></span>

<span data-ttu-id="7bd1d-903">일반 Windows에 대 한 빌드 15019에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-904">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-904">Fixed</span></span>

- <span data-ttu-id="7bd1d-905">버그에서 CPU 사용량을 올바르게 보고 한다면 (GH 823 945, 971)와 같은 도구에 대 한 procfs</span><span class="sxs-lookup"><span data-stu-id="7bd1d-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="7bd1d-906">파일 inotify IN_OPEN 전에 IN_MODIFY 이제 생성 기존 O_TRUNC 사용 하 여 open ()를 호출 하는 경우</span><span class="sxs-lookup"><span data-stu-id="7bd1d-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="7bd1d-907">Unix 소켓 getsockopt SO_ERROR postgress [GH 61이 1354]를 사용 하도록 설정 하기 위한 수정 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="7bd1d-908">GO 언어에 대 한 구현 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="7bd1d-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="7bd1d-909">Apt get 패키지 업데이트 백그라운드 작업 지금 실행 숨겨진 뷰에서</span><span class="sxs-lookup"><span data-stu-id="7bd1d-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="7bd1d-910">Ipv6 localhost (Spring-Framework(Java) 실패)에 대 한 일반 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="7bd1d-911">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-912">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-912">LTP Results:</span></span>
<span data-ttu-id="7bd1d-913">통과 한 테스트 수: 714</span><span class="sxs-lookup"><span data-stu-id="7bd1d-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="7bd1d-914">불합격 개수 (실패, 건너뜀 등...): 249</span><span class="sxs-lookup"><span data-stu-id="7bd1d-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="7bd1d-915">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="7bd1d-916">15014 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-916">Build 15014</span></span>

<span data-ttu-id="7bd1d-917">일반 Windows에 대 한 15014 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-918">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-918">Fixed</span></span>

- <span data-ttu-id="7bd1d-919">Ctrl + C는 이제 의도 한 대로 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="7bd1d-920">htop 및 ps auxw 이제 표시 올바른 리소스 사용률 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="7bd1d-921">기본 신호 NT 예외 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="7bd1d-922">(#513 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-922">(GH #513)</span></span>
- <span data-ttu-id="7bd1d-923">fallocate 이제 실패 ENOSPC EINVAL (GH #1571) 대신 공간 부족</span><span class="sxs-lookup"><span data-stu-id="7bd1d-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="7bd1d-924">추가 /proc/sys/kernel/sem 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="7bd1d-925">구현 된 semop 및 semtimedop 시스템 호출</span><span class="sxs-lookup"><span data-stu-id="7bd1d-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="7bd1d-926">IP_RECVTOS & IPV6_RECVTCLASS 소켓 옵션 (GH 69)를 사용 하 여 고정된 nslookup 오류</span><span class="sxs-lookup"><span data-stu-id="7bd1d-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="7bd1d-927">IP_RECVTTL 및 IPV6_RECVHOPLIMIT 소켓 옵션에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="7bd1d-928">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-929">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-929">LTP Results:</span></span>
<span data-ttu-id="7bd1d-930">통과 한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="7bd1d-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="7bd1d-931">불합격 개수 (실패, 건너뜀 등...): 255</span><span class="sxs-lookup"><span data-stu-id="7bd1d-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7bd1d-932">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="7bd1d-933">Syscall 요약</span><span class="sxs-lookup"><span data-stu-id="7bd1d-933">Syscall Summary</span></span>
<span data-ttu-id="7bd1d-934">총 Syscall: 384</span><span class="sxs-lookup"><span data-stu-id="7bd1d-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="7bd1d-935">전체 구현: 235</span><span class="sxs-lookup"><span data-stu-id="7bd1d-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="7bd1d-936">스텁 합계: 22</span><span class="sxs-lookup"><span data-stu-id="7bd1d-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="7bd1d-937">구현 되지 않았으며 합계: 127</span><span class="sxs-lookup"><span data-stu-id="7bd1d-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="7bd1d-938">세부적인된 분석 결과</span><span class="sxs-lookup"><span data-stu-id="7bd1d-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="7bd1d-939">15007 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-939">Build 15007</span></span>

<span data-ttu-id="7bd1d-940">일반 Windows에 대 한 15007 빌드에 대 한 정보를 방문 합니다 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="7bd1d-941">알려진된 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-941">Known Issue</span></span>

- <span data-ttu-id="7bd1d-942">콘솔 일부 Ctrl 인식 하지 못하는 알려진 버그가 + <key> 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="7bd1d-943">일반 'c' keypress 역할을 할 ctrl + c 명령 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="7bd1d-944">해결 방법: Ctrl + C를 대체 키를 매핑하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="7bd1d-945">예를 들어, 매핑할 Ctrl + K Ctrl + C를 수행: `stty intr \^k`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="7bd1d-946">이 매핑은 터미널 당 이며 완료 해야 할 *마다* 시간 bash 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="7bd1d-947">사용자는이 포함 하는 옵션을 탐색할 수 있습니다는 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="7bd1d-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-948">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-948">Fixed</span></span>

- <span data-ttu-id="7bd1d-949">여기서 실행 WSL를 사용 하 게 CPU 코어의 100% 문제를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="7bd1d-950">소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO 이제 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="7bd1d-951">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-951">(GH #851, 987)</span></span>
- <span data-ttu-id="7bd1d-952">네트워크 인터페이스 물리적 주소 lxcore 16 바이트를 자르기 (1414, GH #1452, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="7bd1d-953">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-954">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-954">LTP Results:</span></span>
<span data-ttu-id="7bd1d-955">통과 한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="7bd1d-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="7bd1d-956">불합격 개수 (실패, 건너뜀 등...): 255</span><span class="sxs-lookup"><span data-stu-id="7bd1d-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7bd1d-957">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="7bd1d-958">빌드 15002</span><span class="sxs-lookup"><span data-stu-id="7bd1d-958">Build 15002</span></span>

<span data-ttu-id="7bd1d-959">일반 Windows 빌드 15002 방법은 참조를 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="7bd1d-960">알려진된 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-960">Known Issue</span></span>

<span data-ttu-id="7bd1d-961">두 가지 알려진된 문제:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-961">Two known issues:</span></span>
- <span data-ttu-id="7bd1d-962">콘솔 일부 Ctrl 인식 하지 못하는 알려진 버그가 + <key> 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="7bd1d-963">일반 'c' keypress 역할을 할 ctrl + c 명령 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="7bd1d-964">해결 방법: Ctrl + C를 대체 키를 매핑하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="7bd1d-965">예를 들어, 매핑할 Ctrl + K Ctrl + C를 수행: `stty intr \^k`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="7bd1d-966">이 매핑은 터미널 당 이며 완료 해야 할 *마다* 시간 bash 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="7bd1d-967">사용자는이 포함 하는 옵션을 탐색할 수 있습니다는 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="7bd1d-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="7bd1d-968">WSL에서 실행 되는 동안 시스템 스레드를 CPU 코어의 100%를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="7bd1d-969">근본 원인은 해결 되어 내부적으로 고정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-970">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-970">Fixed</span></span>

- <span data-ttu-id="7bd1d-971">이제 모든 bash 세션 같은 권한 수준에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="7bd1d-972">여러 수준에서 세션을 시작 하는 동안 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="7bd1d-973">즉, 관리자 및 비관리자 콘솔 동시에 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="7bd1d-974">(#626 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="7bd1d-975">다음 NETLINK_ROUTE 메시지 구현 (Windows 관리 해야 함)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="7bd1d-976">RTM_NEWADDR (지원 `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="7bd1d-977">RTM_NEWROUTE (지원 `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="7bd1d-978">RTM_DELADDR (지원 `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="7bd1d-979">RTM_DELROUTE (지원 `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="7bd1d-980">패키지 업데이트를 확인 하는 예약 된 작업 (GH #1371) 데이터 통신된 연결에서 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="7bd1d-981">고정 오류 가져옵니다 파이프 멈춘 즉, bash-c "ls alR /" | bash-c "고양이" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="7bd1d-982">구현 된 TCP_KEEPCNT 소켓 옵션 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="7bd1d-983">구현 된 IP_MTU_DISCOVER INET 소켓 옵션 (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="7bd1d-984">NT 경로 조회를 사용 하 여 초기화에서 NT 이진 파일을 실행 하는 레거시 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="7bd1d-985">(#1325 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-985">(GH #1325)</span></span>
- <span data-ttu-id="7bd1d-986">그룹 / 기타 읽기 (0644) (GH #1321) 액세스할 수 있도록/kmsg의 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="7bd1d-987">구현 된 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="7bd1d-988">프로세스 시작 시간 (GH #974) 2432 연도로 표시 되어 있는 오류를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="7bd1d-989">Xterm-256color (GH #1446)로 전환된 하는 기본 용어 환경 변수</span><span class="sxs-lookup"><span data-stu-id="7bd1d-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="7bd1d-990">수정 된 커밋을 처리 하는 방식으로 프로세스 분기 하는 동안 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="7bd1d-991">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-991">(GH #1286)</span></span>
- <span data-ttu-id="7bd1d-992">/Proc/sys/vm/overcommit_memory 구현된 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="7bd1d-993">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-993">(GH #1286)</span></span>
- <span data-ttu-id="7bd1d-994">구현 된 /proc/net/route 파일 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="7bd1d-995">바로 가기 이름이 올바르게 오류 수정된 했습니다 (GH #696) 지역화</span><span class="sxs-lookup"><span data-stu-id="7bd1d-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="7bd1d-996">프로그램 헤더를 올바르게 검사할 되는 논리를 구문 분석 하는 고정된 elf 작아야 (크거나 같음) PATH_MAX 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="7bd1d-997">(#1048 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-997">(GH #1048)</span></span>
- <span data-ttu-id="7bd1d-998">구현 된 statfs 콜백 procfs, sysfs, cgroupfs, 및 binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="7bd1d-999">(GH #1184, GH # 1193에 대해서도 설명)를 닫지는 고정 된 AptPackageIndexUpdate windows</span><span class="sxs-lookup"><span data-stu-id="7bd1d-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="7bd1d-1000">ADDR_NO_RANDOMIZE 지원 ASLR 성격을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="7bd1d-1001">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="7bd1d-1002">향상 된 PTRACE_GETSIGINFO, AV (GH #875) 하는 동안 적절 한 gdb 스택 추적에 대 한 SIGSEGV</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="7bd1d-1003">더 이상 구문 분석 elf patchelf 이진 파일에 대 한 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="7bd1d-1004">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1004">(GH #471)</span></span>
- <span data-ttu-id="7bd1d-1005">/Etc/resolv.conf (GH #416, 1350)를 VPN DNS 전파</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="7bd1d-1006">TCP의 향상 된 기능을 더 신뢰할 수 있는 데이터 전송에 대 한 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="7bd1d-1007">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="7bd1d-1008">이제 올바른 너무 많은 파일이 있는 경우 오류 코드 (EMFILE) 열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="7bd1d-1009">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="7bd1d-1010">프로세스의 이미지 이름을 Windows 감사 로그 이제 보고서는 감사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="7bd1d-1011">Bash 창 내에서 bash.exe 시작할 때 이제 정상적으로 실패</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="7bd1d-1012">추가 오류 메시지가 나타난다 interop LxFs (예: notepad.exe.bashrc)에서 작업 디렉터리에 액세스할 수 없는</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="7bd1d-1013">Windows 경로 WSL에서 잘린 여기서 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="7bd1d-1014">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1015">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1015">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1016">통과 한 테스트 수: 690</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="7bd1d-1017">불합격 개수 (실패, 건너뜀 등...): 274</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="7bd1d-1018">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1019">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1019">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1020">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1021">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="7bd1d-1022">14986 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1022">Build 14986</span></span>

<span data-ttu-id="7bd1d-1023">일반 Windows에 대 한 14986 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1024">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1024">Fixed</span></span>

- <span data-ttu-id="7bd1d-1025">Netlink Pty Ioctl와 고정된 버그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="7bd1d-1026">커널 버전에는 이제 4.4.0-43 Xenial와의 일관성에 대 한 보고</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="7bd1d-1027">Bash.exe 입력으로 전달 하는 경우 이제 시작 ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="7bd1d-1028">스레드 Id procfs (GH #967)에서 올바르게 이제 보고</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="7bd1d-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | 이제 inotify_add_watch() (GH #1280)에서 지원 되는 IN_ISDIR 플래그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="7bd1d-1030">구현 timer_create 및 관련된 시스템 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="7bd1d-1031">이렇게 하면 GHC 지원 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="7bd1d-1032">Ping 0.000ms (GH #1296)의 시간을 반환 하는 위치 하는 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="7bd1d-1033">너무 많은 파일이 열려 있는 경우 올바른 오류 코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="7bd1d-1034">인터페이스의 하드웨어 주소 (예: Teredo 인터페이스)를 32 바이트 이면 EINVAL를 사용 하 여 네트워크 인터페이스 데이터에 대 한 Netlink 요청 실패는 WSL에서 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="7bd1d-1035">Note Linux "ip" 유틸리티 WSL 32 비트 하드웨어 주소를 보고 하는 경우 충돌이 있는 버그를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="7bd1d-1036">WSL 없습니다 "ip"의 버그입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="7bd1d-1037">"ip" 유틸리티 하드 코드 길이 문자열 버퍼의 하드웨어 주소를 인쇄 하는 데 사용 하 고 32 비트 하드웨어 주소를 인쇄 하는 버퍼가 너무 작습니다.입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="7bd1d-1038">추가 수정 및 개선 사항</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1039">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1039">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1040">통과 한 테스트 수: 669</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="7bd1d-1041">불합격 개수 (실패, 건너뜀 등...): 258</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="7bd1d-1042">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1043">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1043">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1044">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1045">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="7bd1d-1046">14971 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1046">Build 14971</span></span>

<span data-ttu-id="7bd1d-1047">일반 Windows에 대 한 14971 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1048">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1048">Fixed</span></span>

 - <span data-ttu-id="7bd1d-1049">제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7bd1d-1050">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1051">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1051">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1052">14965에서 변경 되지 않음</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="7bd1d-1053">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7bd1d-1054">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1055">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="7bd1d-1056">14965 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1056">Build 14965</span></span>

<span data-ttu-id="7bd1d-1057">일반 Windows에 대 한 14965 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1058">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1058">Fixed</span></span>

- <span data-ttu-id="7bd1d-1059">Netlink 지원 소켓 NETLINK_ROUTE 프로토콜 RTM_GETLINK 및 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="7bd1d-1060">네트워크 열거형에 대 한 명령을 ifconfig 및 ip를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="7bd1d-1061">자세한 정보를 찾을 수 있습니다 우리의 [블로그 게시물 WSL 네트워킹](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="7bd1d-1062">기본적으로 사용자의 경로에 포함 되었습니다 /sbin</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="7bd1d-1063">NT 사용자 경로 (즉, 이제 입력할 있습니다 notepad.exe System32 Linux 경로에 추가 하지 않고) 기본적으로 이제 WSL 경로에 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="7bd1d-1064">/Proc/sys/kernel/cap_last_cap 지원 추가 됨된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="7bd1d-1065">현재 작업 디렉터리 (GH #1254) ansi 이외의 문자를 포함 하는 경우 NT 바이너리 WSL에서 시작할 수 이제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="7bd1d-1066">연결이 끊긴된 unix 스트림 소켓에서 종료를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="7bd1d-1067">PR_GET_PDEATHSIG 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="7bd1d-1068">CLONE_PARENT 지원 추가 됨된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="7bd1d-1069">고정 오류 가져옵니다 파이프 멈춘 즉, bash-c "ls alR /" | bash-c "고양이" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="7bd1d-1070">현재 터미널에 연결할 핸들 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="7bd1d-1071">/Proc/ 표시<pid>/oom_score_adj 쓰기 가능으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="7bd1d-1072">/Sys/fs/cgroup 폴더를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="7bd1d-1073">sched_setaffinity는 선호도 비트 마스크의 수를 반환 해야</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="7bd1d-1074">이 경우 올바르게 가정 하지 인터프리터 경로 보다 작거나 64 자 이어야 합니다. ELF 유효성 검사 논리를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="7bd1d-1075">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1075">(GH #743)</span></span>
- <span data-ttu-id="7bd1d-1076">열린 파일 설명자는 콘솔 창 열기 (GH #1187)를 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="7bd1d-1077">Rename () 뒤에 슬래시가 대상 이름 (GH #1008)에 실패 한 Fixeed 오류</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="7bd1d-1078">구현 /proc/net/dev 파일</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="7bd1d-1079">타이머 해상도 인해 고정된 0.000ms ping합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="7bd1d-1080">구현 된 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="7bd1d-1081">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1082">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1082">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1083">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7bd1d-1084">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1085">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="7bd1d-1086">14959 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1086">Build 14959</span></span>

<span data-ttu-id="7bd1d-1087">일반 Windows에 대 한 14959 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1088">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1088">Fixed</span></span>

- <span data-ttu-id="7bd1d-1089">Windows에 대 한 향상 된 Pico 프로세스 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="7bd1d-1090">추가 정보에는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="7bd1d-1091">Windows 상호 운용성을 사용 하 여 향상 된 안정성</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="7bd1d-1092">엔터프라이즈 데이터 보호 (EDP)을 사용 하는 경우 bash.exe를 시작할 때 0x80070057 오류가 수정 됨된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="7bd1d-1093">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1094">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1094">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1095">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7bd1d-1096">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1097">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="7bd1d-1098">14955 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1098">Build 14955</span></span>

<span data-ttu-id="7bd1d-1099">일반 Windows에 대 한 14955 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1100">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1100">Fixed</span></span>

 - <span data-ttu-id="7bd1d-1101">제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7bd1d-1102">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1103">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1103">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1104">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7bd1d-1105">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1106">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="7bd1d-1107">14951 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1107">Build 14951</span></span>

<span data-ttu-id="7bd1d-1108">일반 Windows에 대 한 14951 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="7bd1d-1109">새로운 기능: Windows / Ubuntu 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="7bd1d-1110">이제 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="7bd1d-1111">이렇게 하면 사용자는 Windows 환경 및 가능한 되지 않은 방식으로 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="7bd1d-1112">간단한 예제로 다음 명령을 실행 하는 사용자에 대 한 가능한 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="7bd1d-1113">자세한 내용은에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1113">More information can be found at:</span></span>

- [<span data-ttu-id="7bd1d-1114">Interop에 대 한 WSL 팀 블로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="7bd1d-1115">MSDN Interop 설명서</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1116">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1116">Fixed</span></span>

- <span data-ttu-id="7bd1d-1117">Ubuntu 16.04 (Xenial)는 이제 모든 새 WSL 인스턴스에 대 한 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="7bd1d-1118">기존 14.04 (믿음직한) 인스턴스를 사용 하 여 사용자가 자동으로 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="7bd1d-1119">설치 중에 설정 된 로캘을 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="7bd1d-1120">항상 그렇지는 않음 않습니다 WSL 프로세스 파일로 리디렉션하는 버그를 포함 하 여 터미널 향상 작업</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="7bd1d-1121">콘솔의 수명이 bash.exe 수명에 연결 해야</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="7bd1d-1122">콘솔 창 크기는 버퍼 크기가 아니라 표시 크기를 사용 해야</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="7bd1d-1123">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1124">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1124">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1125">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7bd1d-1126">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1127">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="7bd1d-1128">14946 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1128">Build 14946</span></span>

<span data-ttu-id="7bd1d-1129">일반 Windows에 대 한 14946 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1130">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1130">Fixed</span></span>

- <span data-ttu-id="7bd1d-1131">공백이 나 따옴표가 포함 된 NT 사용자 이름을 사용 하 여 사용자에 대 한 WSL 사용자 계정 만들기를 방해 하는 문제가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="7bd1d-1132">바뀌는 VolFs DrvFs stat에서 디렉터리의 링크 개수에 대 한 0을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="7bd1d-1133">IPV6_MULTICAST_HOPS 소켓 옵션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="7bd1d-1134">Tty 당 I/O 루프는 단일 콘솔을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="7bd1d-1135">예 명령을 불가능 합니다.:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="7bd1d-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="7bd1d-1137">공백은 /proc/cpuinfo (GH #1115) 탭으로 대체</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="7bd1d-1138">이제 탑재 된 Windows 볼륨을 일치 하는 이름의 mountinfo DrvFs에 나타납니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="7bd1d-1139">/home 및 /root 이제 올바른 이름의 mountinfo에 표시</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="7bd1d-1140">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1141">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1141">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1142">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7bd1d-1143">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1144">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="7bd1d-1145">14942 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1145">Build 14942</span></span>

<span data-ttu-id="7bd1d-1146">일반 Windows에 대 한 14942 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1147">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1147">Fixed</span></span>

- <span data-ttu-id="7bd1d-1148">다양 한 메모리를 포함 하는 "시도 실행의 NOEXECUTE" 네트워킹 SSH 차단 된 충돌 해결 버그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="7bd1d-1149">inotifiy DrvFs에서 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원은 이제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="7bd1d-1150">TCP_KEEPIDLE 및 TCP_KEEPINTVL mongod에 대 한 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="7bd1d-1151">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1151">(GH #695)</span></span>
- <span data-ttu-id="7bd1d-1152">Pivot_root 시스템 호출을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="7bd1d-1153">SO_DONTROUTE 소켓 옵션을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="7bd1d-1154">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1155">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1155">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1156">통과 한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7bd1d-1157">불합격 개수 (실패, 건너뜀 등...): 263</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7bd1d-1158">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1159">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1159">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1160">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1161">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="7bd1d-1162">14936 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1162">Build 14936</span></span>

<span data-ttu-id="7bd1d-1163">일반 Windows에 대 한 14936 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="7bd1d-1164">참고: WSL 예정 된 릴리스에서 Ubuntu 버전 16.04 (Xenial) 대신 Ubuntu 14.04 (신뢰할 수 있는)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="7bd1d-1165">이 변경 (lxrun.exe /install 또는 bash.exe의 첫 번째 실행)의 새 인스턴스를 설치 하는 참가자에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="7bd1d-1166">신뢰할 수 있는 사용 하 여 기존 인스턴스는 자동으로 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="7bd1d-1167">사용자 믿음직한 이미지 Xenial 수행 릴리스 업그레이드 명령을 사용 하 여 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="7bd1d-1168">알려진된 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1168">Known Issue</span></span>
<span data-ttu-id="7bd1d-1169">WSL에서 일부 소켓 구현 문제가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="7bd1d-1170">버그 확인 자체 명시 "시도 실행의 NOEXECUTE MEMORY" 오류와 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="7bd1d-1171">이 문제의 가장 일반적인 특성 충돌이 경우 ssh를 사용 하 여입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="7bd1d-1172">근본 원인을 내부 빌드에 고정 하 고 가능한 한 빨리 참가자에 밀어넣습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1173">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1173">Fixed</span></span>

- <span data-ttu-id="7bd1d-1174">Chroot 시스템 호출이 구현</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="7bd1d-1175">Inotify의 향상 된 기능 ~~DrvFs에서 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원을 비롯 하 여~~</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="7bd1d-1176">수정: Inotify 지금은 사용할 수 없는 Windows 응용 프로그램에서 시작 된 변경을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="7bd1d-1177">소켓을 IPV6 바인딩::<port n> IPV6_V6ONLY는 이제 (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="7bd1d-1178">Waitid systemcall 구현 (GH #638)에 대 한 WNOWAIT 동작</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="7bd1d-1179">IP_HDRINCL 및 IP_TTL IP 소켓 옵션에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="7bd1d-1180">길이가 0 인 read ()가 즉시 반환 하도록 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="7bd1d-1181">.Tar 파일에는 NULL 종결자를 포함 하지 않는 파일 이름 및 파일 이름 접두사를 올바르게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="7bd1d-1182">/dev/null epoll 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="7bd1d-1183">/Dev/alarm 시간 원본 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="7bd1d-1184">-C 파일을 리디렉션할 수 이제 bash</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="7bd1d-1185">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1186">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1186">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1187">통과 한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7bd1d-1188">불합격 개수 (실패, 건너뜀 등...): 264</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="7bd1d-1189">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1190">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1190">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1191">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1192">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="7bd1d-1193">14931 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1193">Build 14931</span></span>

<span data-ttu-id="7bd1d-1194">일반 Windows에 대 한 14931 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1195">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1195">Fixed</span></span>

 - <span data-ttu-id="7bd1d-1196">제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7bd1d-1197">정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="7bd1d-1198">14926 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1198">Build 14926</span></span>

<span data-ttu-id="7bd1d-1199">일반 Windows에 대 한 14926 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1200">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1200">Fixed</span></span>

- <span data-ttu-id="7bd1d-1201">Ping 이제 관리자 권한이 없는 콘솔에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="7bd1d-1202">이제 지원도 관리자 권한 없이 Ping6</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="7bd1d-1203">WSL를 통해 수정 된 파일에 대 한 Inotify 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="7bd1d-1204">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1204">(GH #216)</span></span>
  - <span data-ttu-id="7bd1d-1205">플래그를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1205">Flags supported:</span></span>
    - <span data-ttu-id="7bd1d-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="7bd1d-1207">inotify_add_watch 이벤트: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="7bd1d-1208">inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="7bd1d-1209">출력을 읽어보세요. LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="7bd1d-1210">알려진된 문제: 이벤트를 생성 하지 않는 Windows 응용 프로그램에서 파일 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="7bd1d-1211">Unix 소켓에 이제 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7bd1d-1212">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1212">LTP Results:</span></span>
<span data-ttu-id="7bd1d-1213">통과 한 테스트 수: 651</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="7bd1d-1214">불합격 개수 (실패, 건너뜀 등...): 258</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="7bd1d-1215">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="7bd1d-1216">14915 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1216">Build 14915</span></span>

<span data-ttu-id="7bd1d-1217">일반 Windows에 대 한 14915 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1218">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1218">Fixed</span></span>
-  <span data-ttu-id="7bd1d-1219">Unix 데이터 그램 소켓 (GH #262)에 대 한 Socketpair</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="7bd1d-1220">SO_REUSEADDR Unix 소켓 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="7bd1d-1221">UNIX 소켓 지원 SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="7bd1d-1222">Unix 소켓 지원 SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="7bd1d-1223">Unix 데이터 그램 소켓 전송, 수신 및 종료에 대 한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="7bd1d-1224">고정 되지 않은 주소에 대 한 잘못 된 mmap 매개 변수 유효성 검사로 인해 오류 검사를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="7bd1d-1225">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1225">(GH #847)</span></span>
- <span data-ttu-id="7bd1d-1226">일시 중단에 대 한 지원 / 터미널 상태는 다시 시작</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="7bd1d-1227">화면 유틸리티 (GH #774) 차단을 해제 하려면 TIOCPKT ioctl에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="7bd1d-1228">알려진된 문제: 기능 키 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="7bd1d-1229">해제 된 멤버 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814)에서 액세스 될 수 있는 TimerFd 경합이 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="7bd1d-1230">Futex, 설문 조사, 및 clock_nanosleep 다시 시작할 수 있는 시스템 호출 지원을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="7bd1d-1231">추가 바인딩 탑재 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1231">Added bind mount support</span></span>
- <span data-ttu-id="7bd1d-1232">탑재 네임 스페이스 지원에 대 한 공유 해제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="7bd1d-1233">알려진된 문제: 사용 하 여 새 탑재 네임 스페이스를 만들 때 `unshare(CLONE_NEWNS)` 현재 작업 디렉터리를 이전 네임 스페이스를 가리키도록 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="7bd1d-1234">추가 개선 사항 및 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="7bd1d-1235">14905 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1235">Build 14905</span></span>

<span data-ttu-id="7bd1d-1236">일반 Windows에 대 한 14905 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1237">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1237">Fixed</span></span>
- <span data-ttu-id="7bd1d-1238">다시 시작할 수 있는 시스템 호출 됩니다 (GH #349, GH #520) 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="7bd1d-1239">Symlink 디렉터리에 / 이제 작업 종료 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="7bd1d-1240">/Dev/random에 대 한 구현된 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="7bd1d-1241">[Pid] /proc/ 구현 / 탑재를 /proc/ [pid] / mountinfo 및 /proc/ [pid] / mountstats 파일</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="7bd1d-1242">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="7bd1d-1243">14901 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1243">Build 14901</span></span>
<span data-ttu-id="7bd1d-1244">Windows 10 1 주년 업데이트 릴리스 게시물에 대 한 첫 번째 참가자 빌드.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="7bd1d-1245">일반 Windows에 대 한 14901 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1246">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1246">Fixed</span></span>
- <span data-ttu-id="7bd1d-1247">후행 슬래시 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="7bd1d-1248">같은 명령 `$ mv a/c/ a/b/` 이제 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="7bd1d-1249">Ubuntu 로캘 Windows 로캘을 설정 해야 하는 경우 이제 프롬프트 설치</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="7bd1d-1250">Ns 폴더에 대 한 procfs 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="7bd1d-1251">탑재를 추가 및 tmpfs procfs 한 sysfs 파일 시스템 탑재 해제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="7bd1d-1252">[At] 32 비트 ABI 서명 mknod 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="7bd1d-1253">모델에 디스패치할 때 이동 하는 Unix 소켓</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="7bd1d-1254">INET 소켓 수신 버퍼 크기는 setsockopt를 사용 하 여 설정에 적용 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="7bd1d-1255">구현 MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="7bd1d-1256">Linux 프로세스 stdin/stdout 파이프 리디렉션 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="7bd1d-1257">명령줄에서 bash-c 명령의 파이핑 허용</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="7bd1d-1258">예: > dir | bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="7bd1d-1259">Bash은 이제 여러 사용량과 (GH #538, #358)를 사용 하 여 시스템에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="7bd1d-1260">기본 INET 소켓 버퍼 크기를 일치 해야 함을 기본 Ubuntu 설치</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="7bd1d-1261">Xattr syscall listxattr에 맞춤</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="7bd1d-1262">유효한 IPv4 주소를 사용 하 여 인터페이스 SIOCGIFCONF에서 반환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="7bd1d-1263">신호 ptrace에 의해 삽입 된 경우 기본 동작 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="7bd1d-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="7bd1d-1265">Sigreturn 컨텍스트를 복원 하는 경우 컴퓨터 컨텍스트 등록 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="7bd1d-1266">Java 및 javac 일부 사용자에 대 한 중지 된 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="7bd1d-1267">/Proc/sys/kernel/hostname 구현</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1268">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1268">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1269">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1270">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="7bd1d-1271">Windows 10 1 주년 업데이트에 14388 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="7bd1d-1272">일반 Windows에 대 한 14388 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/14388wip)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1273">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1273">Fixed</span></span>
- <span data-ttu-id="7bd1d-1274">8/2에서 Windows 10 1 주년 업데이트에 대 한 준비를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="7bd1d-1275">WSL 1 주년 업데이트에 대 한 자세한 내용은에서 확인할 수 있습니다이 [블로그](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="7bd1d-1276">14376 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1276">Build 14376</span></span>
<span data-ttu-id="7bd1d-1277">일반 Windows에 대 한 14376 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1278">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1278">Fixed</span></span>
- <span data-ttu-id="7bd1d-1279">Get apt (GH #493)를 중지 하는 되는 일부 인스턴스에서 제거</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="7bd1d-1280">빈 탑재 올바르게 처리 되지 않은 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="7bd1d-1281">Ramdisks 올바르게 탑재 되지 않은 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="7bd1d-1282">(부분 GH #451) 플래그를 지원 하기 위해 변경 unix 소켓 수락</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="7bd1d-1283">고정된 공용 네트워크 관련 블루 스크린</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="7bd1d-1284">블루 스크린 /proc/ [pid]에 액세스할 때 고정 (GH #523) 작업 /</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="7bd1d-1285">일부 pty 시나리오 (GH #488, #504)에 대 한 고정된 높은 CPU 사용률</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="7bd1d-1286">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="7bd1d-1287">14371 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1287">Build 14371</span></span>
<span data-ttu-id="7bd1d-1288">일반 Windows에 대 한 14371 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1289">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1289">Fixed</span></span>
- <span data-ttu-id="7bd1d-1290">SIGCHLD wait()와 타이밍 경합 ptrace를 사용 하는 경우 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="7bd1d-1291">경로 후행를 포함 하는 경우 몇 가지 동작을 수정 / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="7bd1d-1292">이름 바꾸기 끊고 열린 핸들을 자식으로 인해 실패 한 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="7bd1d-1293">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="7bd1d-1294">14366 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1294">Build 14366</span></span>
<span data-ttu-id="7bd1d-1295">일반 Windows에 대 한 14366 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1296">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1296">Fixed</span></span>
- <span data-ttu-id="7bd1d-1297">Symlink 통해 파일 생성에서 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="7bd1d-1298">Python (GH 385)에 대 한 추가 listxattr</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="7bd1d-1299">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1300">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1300">Syscall Support</span></span>
-   <span data-ttu-id="7bd1d-1301">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1302">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="7bd1d-1303">빌드 14361</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1303">Build 14361</span></span>
<span data-ttu-id="7bd1d-1304">일반 Windows에 대 한 빌드 14361에서 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14361)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1305">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1305">Fixed</span></span>
- <span data-ttu-id="7bd1d-1306">Windows에서 Ubuntu의 Bash에서 실행 중인 경우 DrvFs 대/소문자 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="7bd1d-1307">사용자가 월 case.txt 및 사례입니다. TXT 해당/mnt c 드라이브</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="7bd1d-1308">Windows에서 ubuntu의 Bash에서 대/소문자만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="7bd1d-1309">경우 NTFS Bash의 외부 파일을 올바르게 보고 됩니다 있지만 Windows에서 파일을 사용 하 여 상호 작용 예기치 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="7bd1d-1310">각 볼륨 (즉, /mnt/c)의 루트가 대/소문자 구분 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="7bd1d-1311">Windows에서 이러한 파일을 처리 하는 방법은 찾을 수 있습니다 [여기](https://support.microsoft.com/en-us/kb/100625)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="7bd1d-1312">크게 향상 pty / tty 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="7bd1d-1313">이제 지원 됩니다 (GH #40) TMUX와 같은 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="7bd1d-1314">사용자 계정이 항상 생성 하는 고정 된 설치 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="7bd1d-1315">매우 긴 인수 목록에 대 한 허용 하는 명령줄 인수 구조를 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="7bd1d-1316">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1316">(GH #153)</span></span>
- <span data-ttu-id="7bd1d-1317">DrvFs에서 삭제 및 chmod read_only 파일 이제 수</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="7bd1d-1318">일부 경우에서 터미널 중지 (GH #43)를 분리 하는 위치를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="7bd1d-1319">chmod 및 chown 이제 tty 장치에서 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="7bd1d-1320">0.0.0.0으로 연결을 허용 하 고:: localhost (#388 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="7bd1d-1321">Sendmsg/recvmsg의는 IO 벡터 길이 이제 처리할 > 1 (부분 GH #376)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="7bd1d-1322">사용자가 이제 옵트아웃할 수 자동으로 생성 된 호스트 파일 (GH #398)의</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="7bd1d-1323">자동으로 NT 로캘로 Linux 로캘 (GH #11) 설치 하는 동안 일치</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="7bd1d-1324">/Proc/sys/vm/swappiness 파일 (GH #306) 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="7bd1d-1325">strace 이제 올바르게 종료</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1325">strace now exits correctly</span></span>
- <span data-ttu-id="7bd1d-1326">파이프 /proc/self/fd (GH #222)를 통해 다시 열 수를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="7bd1d-1327">디렉터리가 %LOCALAPPDATA%\lxss DrvFs (GH #270)에서 숨기기</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="7bd1d-1328">Bash.exe 보다 효율적으로 처리 ~입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="7bd1d-1329">와 같은 명령도 "bash ~-c ls" (GH #467) 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="7bd1d-1330">소켓에는 이제 epoll 알림 (GH #271) 종료 하는 동안 사용할 수 있는 읽기</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="7bd1d-1331">lxrun / 제거는 더 효율적으로 파일 및 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="7bd1d-1332">수정 된 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="7bd1d-1333">X11 지원 개선 xEmacs (GH #481)와 같은 앱</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="7bd1d-1334">초기 스레드 스택 크기 기본값 Ubuntu 및 크기를 올바르게 보고 get_rlimit syscall (GH # 172를 #258)를 일치 시키는 업데이트</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="7bd1d-1335">Pico 프로세스 이미지 이름 (예: 감사) 보고 개선</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="7bd1d-1336">Df 명령에 대 한 구현된 /proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="7bd1d-1337">자식 이름에 대 한 고정된 symlink 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="7bd1d-1338">및...</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1338">and ..</span></span>
- <span data-ttu-id="7bd1d-1339">추가 개선 사항 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1340">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1340">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1341">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1342">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="7bd1d-1343">빌드 14352</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1343">Build 14352</span></span>
<span data-ttu-id="7bd1d-1344">일반 Windows에 대 한 빌드 14352에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14352)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1345">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1345">Fixed</span></span>
- <span data-ttu-id="7bd1d-1346">큰 파일 된 되지 않음 다운로드 / 올바르게 생성 문제를 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="7bd1d-1347">Npm 및 다른 시나리오 (GH 3, GH #313) 차단을 해제 해야이</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="7bd1d-1348">소켓의 중지 일부 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="7bd1d-1349">일부 ptrace 오류 수정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="7bd1d-1350">파일 이름이 255 자 보다 긴 허용 WSL 사용 하 여 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="7bd1d-1351">영어가 아닌 문자에 대 한 향상 된 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="7bd1d-1352">현재 Windows 표준 시간대 데이터를 추가 하 고 기본값으로 설정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="7bd1d-1353">고유한 장치 id의 각각에 대 한 탑재 지점 (jre 수정-GH #49)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="7bd1d-1354">포함 하는 경로 사용 하 여 문제를 해결 합니다. "."</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="7bd1d-1355">및 "..."</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1355">and “..”</span></span>
- <span data-ttu-id="7bd1d-1356">Fifo 지원이 추가 되었습니다 (#71 GH)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="7bd1d-1357">업데이트 된 형식의 기본 Ubuntu 형식과 일치 하도록 하기 위해 resolv.conf</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="7bd1d-1358">일부 procfs 정리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="7bd1d-1359">관리자 콘솔 (GH #18)에 대해 설정 된 ping</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1360">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1360">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1361">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1362">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="7bd1d-1363">14342 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1363">Build 14342</span></span>
<span data-ttu-id="7bd1d-1364">일반 Windows에 대 한 정보 빌드 14342 합니다 [Windows 블로그](https://aka.ms/wip14342)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="7bd1d-1365">VolFs 및 DriveFs에 대 한 정보를 확인할 수 있습니다 합니다 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1366">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1366">Fixed</span></span>
- <span data-ttu-id="7bd1d-1367">Windows 사용자 사용자 이름에 유니코드 문자가 있을 때에 설치 문제를 해결 함</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="7bd1d-1368">FAQ apt get 업데이트 udev 해결 방법은 첫 번째 실행에서 기본적으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="7bd1d-1369">DriveFs에 symlink를 사용 하도록 설정 (/mnt/<drive>) 디렉터리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="7bd1d-1370">Symlink은 DriveFs 사이의 VolFs 이제 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="7bd1d-1371">주소가 지정 된 상위 수준 경로 문제를 구문 분석: l s. / / 이제 정상적으로 작동 됩니다</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="7bd1d-1372">DriveFs에 npm 설치 하 고-g 옵션은 이제 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="7bd1d-1373">PHP 서버를 시작 하지 못하도록 방지 하는 문제 해결된</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="7bd1d-1374">네이티브 Ubuntu에 더 가깝게 맞게 $PATH 같은 업데이트 된 기본 환경 값</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="7bd1d-1375">Apt 패키지 캐시를 업데이트 하는 Windows에서 매주 유지 관리 작업을 추가</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="7bd1d-1376">ELF 헤더 유효성 검사를 사용 하 여 문제를 해결, WSL 이제 모든 Melkor 옵션</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="7bd1d-1377">Zsh shell은 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="7bd1d-1378">이동의 미리 컴파일된 이진 파일은 이제 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="7bd1d-1379">올바르게 이제 지역화 된 Bash.exe 첫 번째 실행에서 메시지를 표시</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="7bd1d-1380">/proc/meminfo 이제 올바른 정보를 반환</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="7bd1d-1381">이제 VFS에서 지원 되는 소켓</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="7bd1d-1382">사용 하기 위해 /dev 이제 tempfs로 탑재</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="7bd1d-1383">Fifo 이제 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1383">Fifo now supported</span></span>
- <span data-ttu-id="7bd1d-1384">이제/proc/cpuinfo에 올바르게 표시 하는 다중 코어 시스템</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="7bd1d-1385">추가 개선 사항 및 첫 번째 실행 동안 다운로드 하는 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="7bd1d-1386">Syscall 개선 사항 및 버그 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="7bd1d-1387">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="7bd1d-1388">추가 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="7bd1d-1389">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1389">Known Issues</span></span>
- <span data-ttu-id="7bd1d-1390">확인 하지 못하는 '..'</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1390">Not resolving ‘..’</span></span> <span data-ttu-id="7bd1d-1391">일부 경우에는 DriveFs에서 올바르게</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1392">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1392">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1393">다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1394">이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="7bd1d-1395">14332 빌드</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1395">Build 14332</span></span>

<span data-ttu-id="7bd1d-1396">일반 Windows에 대 한 14332 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14332)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="7bd1d-1397">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1397">Fixed</span></span>
- <span data-ttu-id="7bd1d-1398">DNS 항목을 우선 순위 지정을 비롯 한 효율적인 resolv.conf 생성</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="7bd1d-1399">/Mnt 사이 및 비 파일 및 디렉터리를 이동 하는 문제가-mnt 드라이브 /</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="7bd1d-1400">Tar 파일 symlink를 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="7bd1d-1401">인스턴스 만들기에서 추가 기본 /run/lock 디렉터리</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="7bd1d-1402">적절 한 상태 정보를 반환할 /dev/null 업데이트</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="7bd1d-1403">첫 번째 실행 동안 다운로드 하는 경우 추가 오류</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="7bd1d-1404">Syscall 개선 사항 및 버그 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="7bd1d-1405">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="7bd1d-1406">추가 개선 사항 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1407">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1407">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1408">다음은 WSL에서 구현 된 새 syscall입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="7bd1d-1409">Syscall이이 목록에는 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수가 지원 되지이 이번.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="7bd1d-1410">빌드 14328</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1410">Build 14328</span></span>

<span data-ttu-id="7bd1d-1411">일반 Windows에 대 한 14332 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14328)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="7bd1d-1412">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1412">New Features</span></span>
* <span data-ttu-id="7bd1d-1413">이제 Linux 사용자를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1413">Now support Linux users.</span></span>  <span data-ttu-id="7bd1d-1414">Windows에서 ubuntu의 Bash를 설치한 Linux 사용자를 만드는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="7bd1d-1415">자세한 내용은 참조 하세요. https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="7bd1d-1416">Hostname는 Windows 컴퓨터 이름에 더 이상 설정 되었습니다. @localhost</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="7bd1d-1417">빌드 14328 대 한 자세한 내용은 참조 하십시오. https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="7bd1d-1418">고정</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1418">Fixed</span></span>
* <span data-ttu-id="7bd1d-1419">비 /mnt/ Symlink 향상<drive> 파일</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="7bd1d-1420">npm 설치가 작동</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1420">npm install now works</span></span>
    * <span data-ttu-id="7bd1d-1421">jdk 지침을 사용 하 여 설치할 수 있는 이제 jre [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="7bd1d-1422">알려진 문제: Windows 탑재에 대 한 symlink 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="7bd1d-1423">기능을 이후 빌드에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="7bd1d-1424">위쪽과 htop 표시</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1424">top and htop now display</span></span>
* <span data-ttu-id="7bd1d-1425">추가 오류 메시지 일부에 대 한 설치 실패</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="7bd1d-1426">Syscall 개선 사항 및 버그 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="7bd1d-1427">아래 지원 되는 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="7bd1d-1428">추가 개선 사항 버그 수정 및 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7bd1d-1429">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1429">Syscall Support</span></span>
<span data-ttu-id="7bd1d-1430">다음은 syscall WSL 구현에 있는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="7bd1d-1431">Syscall이이 목록에 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.</span><span class="sxs-lookup"><span data-stu-id="7bd1d-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
