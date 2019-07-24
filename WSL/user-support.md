---
title: Linux 사용자 계정 및 사용 권한
description: Linux 용 Windows 하위 시스템을 사용 하 여 사용자 계정 및 사용 권한 관리를 참조 하세요.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, 사용자 계정
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040827"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="fe314-104">Linux 용 Windows 하위 시스템에 대 한 사용자 계정 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="fe314-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="fe314-105">WSL에서 새 Linux 배포를 설정 하는 첫 번째 단계는 Linux 사용자를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="fe314-106">만든 첫 번째 사용자 계정은 다음과 같은 몇 가지 특수 특성으로 자동으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="fe314-107">기본 사용자입니다. 시작 시 자동으로 로그인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="fe314-108">기본적으로 Linux 관리자 (sudo 그룹의 구성원)입니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="fe314-109">Linux 용 Windows 하위 시스템에서 실행 되는 각 Linux 배포에는 고유한 Linux 사용자 계정 및 암호가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="fe314-110">배포를 추가, 다시 설치 또는 다시 설정 하는 경우 언제 든 지 Linux 사용자 계정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="fe314-111">Linux 사용자 계정은 배포 마다 독립적이 지 않으며 Windows 사용자 계정과 독립적입니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="fe314-112">Linux 암호 재설정</span><span class="sxs-lookup"><span data-stu-id="fe314-112">Resetting your Linux password</span></span>

<span data-ttu-id="fe314-113">Linux 사용자 계정에 대 한 액세스 권한이 있고 현재 암호를 알고 있는 경우 해당 배포 `passwd`의 linux 암호 재설정 도구를 사용 하 여 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="fe314-114">배포에 따라 옵션이 아닌 경우 기본 사용자를 다시 설정 하 여 암호를 다시 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="fe314-115">WSL은 WSL을 시작할 때 자동으로 로그인 하는 사용자 계정을 식별 하는 기본 사용자 태그를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="fe314-116">대부분의 배포에는 기본 사용자를 루트로 설정 하는 명령과 암호를 설정 하지 않은 루트 사용자를 설정 하는 명령이 포함 되어 있으므로, 기본 사용자를 root로 변경 하면 암호 재설정과 같은 작업을 수행 하는 데 유용한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="fe314-117">작성자 업데이트 및 이전 버전</span><span class="sxs-lookup"><span data-stu-id="fe314-117">For Creators Update and earlier</span></span>
<span data-ttu-id="fe314-118">Windows 10 크리에이터 업데이트 또는 이전 버전을 실행 하는 경우 다음 명령을 실행 하 여 기본 Bash 사용자를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="fe314-119">기본 사용자를 `root`다음과 같이 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="fe314-120">지금 `bash.exe` 다음으로 `root`로그인 하려면 실행:</span><span class="sxs-lookup"><span data-stu-id="fe314-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="fe314-121">배포의 암호 명령을 사용 하 여 암호를 재설정 하 고 Linux 콘솔을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="fe314-122">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="fe314-123">적합 하지 않은 작성자 업데이트 이상</span><span class="sxs-lookup"><span data-stu-id="fe314-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="fe314-124">특정 배포에 사용할 수 있는 명령을 확인 하려면를 실행 `[distro.exe] /?`합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="fe314-125">예: Ubuntu가 설치 된 경우:</span><span class="sxs-lookup"><span data-stu-id="fe314-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="fe314-126">Ubuntu를 사용 하는 단계별 지침:</span><span class="sxs-lookup"><span data-stu-id="fe314-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="fe314-127">CMD 열기</span><span class="sxs-lookup"><span data-stu-id="fe314-127">Open CMD</span></span>
1. <span data-ttu-id="fe314-128">기본 Linux 사용자를 다음으로 `root`설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="fe314-129">Linux 배포 (`ubuntu`)를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="fe314-130">자동으로 로그인 `root`합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="fe314-131">다음 `passwd` 명령을 사용 하 여 암호를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="fe314-132">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="fe314-133">사용 권한</span><span class="sxs-lookup"><span data-stu-id="fe314-133">Permissions</span></span>

<span data-ttu-id="fe314-134">WSL의 사용 권한과 관련 하 여 다음 두 가지 중요 한 개념을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="fe314-135">Windows 사용 권한 모델은 Windows 리소스에 대 한 프로세스의 권한을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="fe314-136">Linux 권한 모델은 Linux 리소스에 대 한 프로세스의 권한을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="fe314-137">WSL에서 Linux를 실행 하는 경우 Linux는이를 시작 하는 프로세스와 동일한 Windows 사용 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="fe314-138">Linux는 다음 두 가지 권한 수준 중 하나로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="fe314-139">보통 (권한 없음): Linux는 로그인 한 사용자의 권한으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="fe314-140">관리자 권한/관리자: 관리자 권한으로 실행 되는 Linux 및 Windows 권한</span><span class="sxs-lookup"><span data-stu-id="fe314-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="fe314-141">상승 된 프로세스는 시스템 수준 설정과 시스템 차원의/보호 된 데이터에 액세스/수정 (따라서 손상) 할 수 있기 때문에 Windows 또는 Linux 응용 프로그램/도구 인지 여부에 관계 없이 상승 된 프로세스를 시작 **하지 않습니다** . 셸에!</span><span class="sxs-lookup"><span data-stu-id="fe314-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="fe314-142">위의 Windows 권한은 Linux 인스턴스 내의 권한과는 독립적입니다. Linux "루트 권한"은 Linux 환경 & filesystem에서 사용자의 권한에만 영향을 줍니다. 부여 된 Windows 권한에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="fe314-143">따라서 linux 프로세스를 루트 (예: via `sudo`)로 실행 하면 linux 환경 내에서 해당 프로세스 관리자 권한만 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="fe314-144">**예제:**   </span><span class="sxs-lookup"><span data-stu-id="fe314-144">**Example:**  </span></span>  
<span data-ttu-id="fe314-145">관리자 권한이 없는 bash 세션이 "권한 거부" `cd /mnt/c/Users/Administrator` 오류를 표시 하는 동안 Windows 관리자 권한이 있는 bash 세션에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="fe314-146">Linux에서는 windows 내의 `sudo cd /mnt/c/Users/Administrator` 권한이 windows에서 관리 되기 때문에를 입력 하면 관리자 디렉터리에 대 한 액세스 권한이 부여 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="fe314-147">Linux 권한 모델은 사용자에 게 현재 Linux 사용자에 따라 사용 권한이 있는 Linux 환경 내에서 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="fe314-148">**예제:**</span><span class="sxs-lookup"><span data-stu-id="fe314-148">**Example:**</span></span>  
<span data-ttu-id="fe314-149">Sudo 그룹의 사용자가 실행 `sudo apt update`될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe314-149">A user in the sudo group may run `sudo apt update`.</span></span>
