---
title: Windows의 Linux 상호 운용성
description: Linux 용 Windows 하위 시스템에서 실행 중인 Linux 배포를 사용 하 여 Windows 상호 운용성을 설명 합니다.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063251"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="4dd81-103">Windows와 Linux 상호 운용성에 대 한 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="4dd81-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="4dd81-104">**Fall Creators Update에 대 한 업데이트 합니다.**</span><span class="sxs-lookup"><span data-stu-id="4dd81-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="4dd81-105">크리에이터 스 업데이트 또는 1 주년 업데이트를 실행 하는 경우으로 이동 합니다 [작성자/1 주년 업데이트 섹션](interop.md#creators-update-and-anniversary-update)합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="4dd81-106">Windows 하위 시스템에 대 한 WSL (Linux)는 Windows와 Linux의 통합을 지속적으로 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="4dd81-107">다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-107">You can:</span></span>

1. <span data-ttu-id="4dd81-108">Linux 콘솔에서 Windows 이진 파일을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="4dd81-109">Windows 콘솔에서 Linux 이진 파일을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="4dd81-110">**Windows 참가자 빌드 17063 +** Linux와 Windows 간의 환경 변수를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="4dd81-111">이 Windows 및 WSL 간의 원활한 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="4dd81-112">기술 세부 정보에는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="4dd81-113">Windows 명령줄에서 Linux 도구를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="4dd81-114">Linux 이진 파일을 사용 하 여 Windows 명령 프롬프트 (CMD 또는 PowerShell)에서 실행 `wsl.exe <command>`합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="4dd81-115">이러한 방식으로 호출 하는 이진 파일:</span><span class="sxs-lookup"><span data-stu-id="4dd81-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="4dd81-116">현재 CMD 또는 PowerShell 프롬프트와 같은 작업 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="4dd81-117">WSL 기본 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="4dd81-118">터미널 호출 하는 프로세스와 동일한 Windows 관리자 권한이 있어야.</span><span class="sxs-lookup"><span data-stu-id="4dd81-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="4dd81-119">예를 들어 다음과 같은 가치를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="4dd81-120">다음 Linux 명령 `wsl.exe` WSL에서 실행할 명령 처럼 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="4dd81-121">Sudo, 파이핑 파일 리디렉션 등 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="4dd81-122">Sudo를 사용 하는 예제:</span><span class="sxs-lookup"><span data-stu-id="4dd81-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="4dd81-123">혼합 WSL 및 Windows 명령 예제:</span><span class="sxs-lookup"><span data-stu-id="4dd81-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="4dd81-124">에 전달 된 명령을 `wsl.exe` 수정 하지 않고 WSL 프로세스에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="4dd81-125">WSL 형식으로 파일 경로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="4dd81-126">예제 경로:</span><span class="sxs-lookup"><span data-stu-id="4dd81-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="4dd81-127">WSL에서 Windows 도구를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="4dd81-128">WSL 사용 하 여 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다 `[binary name].exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="4dd81-129">`notepad.exe`) 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="4dd81-130">Linux에서 Windows 실행 파일을 더 쉽게 실행 하려면 Windows 경로가 포함 되어 `$PATH` Fall Creators Update에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="4dd81-131">이러한 방식으로 실행 하는 응용 프로그램에 다음 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="4dd81-132">WSL 명령 프롬프트를 작업 디렉터리를 유지 합니다. 대부분의-예외는 아래에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="4dd81-133">WSL 프로세스와 동일한 권한 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="4dd81-134">현재 Windows 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="4dd81-135">Windows 작업 관리자에서 표시 CMD 프롬프트에서 직접 실행 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="4dd81-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="4dd81-136">예:</span><span class="sxs-lookup"><span data-stu-id="4dd81-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="4dd81-137">WSL에서 실행 되는 Windows 실행 파일에 네이티브 Linux 실행-리디렉션, 파이핑 및 예상 대로 작업을 backgrounding도 마찬가지로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="4dd81-138">파이프를 사용 하는 예제:</span><span class="sxs-lookup"><span data-stu-id="4dd81-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="4dd81-139">혼합 된 Windows 및 WSL 명령을 사용 하는 예제:</span><span class="sxs-lookup"><span data-stu-id="4dd81-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="4dd81-140">Windows 이진 파일 확장명을 포함 하 고 파일 대/소문자 구분 하 고 실행 가능 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="4dd81-141">비-실행 파일 포함 하 여 스크립트를 일괄 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="4dd81-142">와 같은 네이티브 명령도 CMD `dir` 실행할 수 있습니다 `cmd.exe /C` 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="4dd81-143">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="4dd81-144">매개 변수는 수정 되지 않은 Windows 이진에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="4dd81-145">예를 들어 다음 명령은 열립니다 `C:\temp\foo.txt` 에서 `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="4dd81-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="4dd81-146">VolFs에 있는 파일을 수정 (아래 하지 파일 `/mnt/<x>`)는 Windows WSL에서 응용 프로그램은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="4dd81-147">기본적으로 WSL는 Windows의 작업 디렉터리를 현재 WSL 디렉터리로 이진 상태를 유지 하려고 하지만 작업 디렉터리 VolFs 켜져 있으면 인스턴스 생성 디렉터리에 다시 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="4dd81-148">예를 들어; `wsl.exe` 에서 처음 시작 `C:\temp` 하며 현재 WSL 디렉터리 사용자의 홈으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="4dd81-149">때 `notepad.exe` 호출 되는 사용자의 홈 디렉터리에서 WSL 자동으로 되돌아갑니다 `C:\temp` notepad.exe 작업 디렉터리로:</span><span class="sxs-lookup"><span data-stu-id="4dd81-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="4dd81-150">Windows 및 WSL 간에 공유 환경 변수</span><span class="sxs-lookup"><span data-stu-id="4dd81-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="4dd81-151">Windows Insider 빌드 17063 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="4dd81-152">Windows 환경 변수 하나만 WSL 액세스할 수 있는 17063, 이전 `PATH` (따라서 WSL에서 Win32 실행 파일을 시작할 수 있습니다).</span><span class="sxs-lookup"><span data-stu-id="4dd81-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="4dd81-153">WSL 및 Windows 공유 17063부터 `WSLENV`, WSL에서 실행 되는 Windows 및 Linux 배포판을 생성 하는 특별 한 환경 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="4dd81-154">속성의 `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="4dd81-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="4dd81-155">공유 상태 Windows 및 WSL 환경 모두에 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="4dd81-156">WSL 및 Windows 간에 공유할 수 있는 환경 변수의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="4dd81-157">Windows 및 WSL에서 제대로 작동 하도록 환경 변수 형식을 지정할 수 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="4dd81-158">사용할 수 있는 네 개의 플래그는 `WSLENV` 해당 환경 변수는 변환 하는 방법에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="4dd81-159">`WSLENV` 플래그:</span><span class="sxs-lookup"><span data-stu-id="4dd81-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="4dd81-160">`/p` -Win32 및 WSL/Linux 스타일 경로 간의 경로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="4dd81-161">`/l` -환경 변수가 경로 목록을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="4dd81-162">`/u` -이 환경 변수만 포함 되어야 함을 WSL Win32에서 실행 하는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="4dd81-163">`/w` -이 환경 변수만 포함 되어야 함을 WSL에서 Win32를 실행 하는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="4dd81-164">필요에 따라 플래그를 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="4dd81-165">Interop을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="4dd81-165">Disable Interop</span></span>

<span data-ttu-id="4dd81-166">사용자는 루트로 다음 명령을 실행 하 여 단일 WSL 세션에 대 한 Windows 이진 파일을 실행 하는 기능을 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="4dd81-167">Windows를 다시 사용 하도록 설정 하려면 이진 파일 모든 WSL 세션을 종료 및 bash.exe를 다시 실행 하거나 루트로 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="4dd81-168">Interop을 사용 하지 않도록 설정 WSL 세션 간에 유지 되지 않습니다. 즉 interop 새 세션을 시작할 때 다시 사용할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="4dd81-169">크리에이터 업데이트 및 1 주년 업데이트</span><span class="sxs-lookup"><span data-stu-id="4dd81-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="4dd81-170">Interop 환경 사전 Fall Creators Update는 최신 interop 환경을 비슷하지만 주요 차이점 중 handfull 가지 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handfull of major differences.</span></span>

<span data-ttu-id="4dd81-171">요약:</span><span class="sxs-lookup"><span data-stu-id="4dd81-171">To summarize:</span></span>

* <span data-ttu-id="4dd81-172">`bash.exe` 더 이상 사용 되지 않으며로 대체 되었습니다 `wsl.exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="4dd81-173">`-c` 필요 하지 않습니다 단일 명령 실행에 대 한 옵션 `wsl.exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="4dd81-174">Windows 경로 WSL에 포함 된 `$PATH`</span><span class="sxs-lookup"><span data-stu-id="4dd81-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="4dd81-175">Interop을 사용 하지 않도록 설정 하는 것에 대 한 프로세스 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="4dd81-176">Windows 명령줄에서 호출 WSL</span><span class="sxs-lookup"><span data-stu-id="4dd81-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="4dd81-177">Windows 명령 프롬프트에서 또는 PowerShell에서 Linux 이진 파일을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="4dd81-178">이러한 방식으로 호출 하는 이진 파일에 다음 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="4dd81-179">CMD 또는 PowerShell 프롬프트와 같은 작업 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="4dd81-180">WSL 기본 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="4dd81-181">터미널 호출 하는 프로세스와 동일한 Windows 관리자 권한이 있어야.</span><span class="sxs-lookup"><span data-stu-id="4dd81-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="4dd81-182">예:</span><span class="sxs-lookup"><span data-stu-id="4dd81-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="4dd81-183">이러한 방식으로 호출 하는 Linux 명령은 다른 Windows 응용 프로그램과 마찬가지로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="4dd81-184">입력, 파이핑 및 파일 리디렉션 등 예상 대로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="4dd81-185">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-185">Examples:</span></span>

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

<span data-ttu-id="4dd81-186">WSL 명령을 전달할 `bash -c` 수정 하지 않고 WSL 프로세스에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="4dd81-187">WSL 형식으로 파일 경로 지정 해야 합니다 및 관련 문자 이스케이프에 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="4dd81-188">예:</span><span class="sxs-lookup"><span data-stu-id="4dd81-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="4dd81-189">WSL에서 Windows 바이너리를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="4dd81-190">Linux 용 Windows 하위 시스템에는 Windows 이진 WSL 명령줄에서 직접 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="4dd81-191">이러한 방식으로 실행 하는 응용 프로그램에 다음 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="4dd81-192">아래에 설명 된 시나리오에서 제외 하 고 WSL 명령 프롬프트를 작업 디렉터리를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="4dd81-193">와 동일한 권한 권한이 `bash.exe` 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="4dd81-194">현재 Windows 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="4dd81-195">Windows 작업 관리자에서 표시 CMD 프롬프트에서 직접 실행 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="4dd81-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="4dd81-196">예:</span><span class="sxs-lookup"><span data-stu-id="4dd81-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="4dd81-197">WSL를 이러한 실행 파일 네이티브 Linux 실행 파일을 비슷하게 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="4dd81-198">즉, Linux 경로에 디렉터리를 추가 하 고 예상 대로 명령이 작동 간의 파이핑 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="4dd81-199">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="4dd81-200">Windows 이진 파일 확장명을 포함 하 고 파일 대/소문자 구분 하 고 실행 가능 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="4dd81-201">비-실행 파일 포함 하 여 일괄 처리 스크립트 및와 같은 명령을 `dir` 실행할 수 있습니다 `/mnt/c/Windows/System32/cmd.exe /C` 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="4dd81-202">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="4dd81-203">매개 변수는 수정 되지 않은 Windows 이진에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="4dd81-204">예를 들어 다음 명령은 열립니다 `C:\temp\foo.txt` 에서 `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="4dd81-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="4dd81-205">VolFs에 있는 파일을 수정 (아래 하지 파일 `/mnt/<x>`)는 Windows 응용 프로그램은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="4dd81-206">기본적으로 WSL 현재 WSL 디렉터리로 이진을 Windows의 작업 디렉터리를 유지 하려고 하지만 작업 디렉터리 VolFs 켜져 있으면 인스턴스 생성 디렉터리에 다시 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="4dd81-207">예를 들어; `bash.exe` 에서 처음 시작 `C:\temp` 하며 현재 WSL 디렉터리 사용자의 홈으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd81-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="4dd81-208">때 `notepad.exe` 호출 되는 사용자의 홈 디렉터리에서 WSL 자동으로 되돌아갑니다 `C:\temp` notepad.exe 작업 디렉터리로:</span><span class="sxs-lookup"><span data-stu-id="4dd81-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
