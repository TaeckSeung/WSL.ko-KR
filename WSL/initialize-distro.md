---
title: 새 WSL Linux 배포판을 초기화 합니다.
description: WSL에 대 한 Linux 배포판을 설치한 후 다음과 같은 간단한 단계에서 초기화를 완료
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902050"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="24bbb-104">새로 설치 된 배포판을 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="24bbb-105">배포를 다운로드 하 고 설치 된 후 새 배포판의 초기화를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="24bbb-106">배포판을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-106">Launch a distro</span></span>
<span data-ttu-id="24bbb-107">새로 설치 된 배포의 초기화를 완료 하려면 새 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="24bbb-108">Windows 스토어 앱의 경우 "시작" 단추를 클릭 하거나 시작 메뉴에서 배포판을 실행 하 여이 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="24bbb-109">팁:  사용자 가장 자주 사용 되는 배포판 하 여 시작 메뉴 및/또는 작업 표시줄에 고정할 수도 있습니다!</span><span class="sxs-lookup"><span data-stu-id="24bbb-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![시작 메뉴에서 배포를 시작 합니다.](media/start-menu.png)

> <span data-ttu-id="24bbb-111">Windows Server에서 실행 파일 배포의 시작 관리자를 시작할 수 있습니다 `<distro>.exe` 배포판 설치 폴더에서.</span><span class="sxs-lookup"><span data-stu-id="24bbb-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="24bbb-112">처음 새로 설치 된 배포판을 실행, 콘솔 창이 열리고 되며 설치가 완료에 대 일 분 정도 대기 하 라는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="24bbb-113">설치의이 최종 단계 동안 배포판의 파일 압축 해제 되어 pc에서는 사용할 수 있도록 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="24bbb-114">관련 저장소 장치를 PC의 성능에 따라 1 분 이상 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="24bbb-115">이 초기 설치 단계는만 정리-설치 됨-배포판을 때 필요한 모든 향후 출시 취해야 1 초 미만입니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="24bbb-116">새 Linux 사용자 계정 설정</span><span class="sxs-lookup"><span data-stu-id="24bbb-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="24bbb-117">설치가 완료 되 면 새 사용자 계정 (및 해당 암호)을 만들려면 묻는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows 콘솔에서 압축을 푼 Ubuntu](media/UbuntuInstall.png)

<span data-ttu-id="24bbb-119">이 사용자 계정은 수 있음을 기록 기능에서 기본적으로는 배포판을 시작할 때 관리자가 아닌 일반 사용자에 대 한입니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="24bbb-120">모든 사용자 이름 및 암호로 선택할 수 있습니다-Windows 사용자 이름을 관계가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="24bbb-121">새 배포판 인스턴스를 열면 않습니다 묻는 암호를 하지만 **를 사용 하 여 프로세스를 권한 상승 하는 경우 `sudo`, 암호를 입력 해야**쉽게 기억할 수 있는 암호 선택 해야 하므로,!</span><span class="sxs-lookup"><span data-stu-id="24bbb-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="24bbb-122">참조 된 [사용자 지원](user-support.md) 자세한 내용은 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="24bbb-123">업데이트 및 배포판의 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="24bbb-124">대부분의 배포판 빈/최소 패키지 카탈로그를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="24bbb-125">패키지 카탈로그를 정기적으로 업데이트 및 배포판의 기본 패키지 관리자를 사용 하 여 설치 된 패키지를 업그레이드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="24bbb-126">Debian/Ubuntu에 apt를 사용 하면:</span><span class="sxs-lookup"><span data-stu-id="24bbb-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="24bbb-127">Windows는 자동으로 업데이트 하거나 Linux distro(s) 프로그램 업그레이드: Linux 사용자 자체를 제어 하는 것을 선호 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="24bbb-128">모든 작업이 끝났습니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-128">You're done!</span></span> <span data-ttu-id="24bbb-129">WSL에서 새 Linux 배포를 사용 하 여을 즐겨보세요!</span><span class="sxs-lookup"><span data-stu-id="24bbb-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="24bbb-130">WSL에 대 한 자세한 내용은 다른 검토 [WSL docs](https://aka.ms/wsldocs), 또는 [학습 리소스 페이지 WSL](https://aka.ms/learnwsl)합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![WSL에서 Linux를 사용 하 여 이용할 수 있습니다.](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="24bbb-132">문제 해결</span><span class="sxs-lookup"><span data-stu-id="24bbb-132">Troubleshooting</span></span>

<span data-ttu-id="24bbb-133">다음은 관련된 오류 및 제안 된 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="24bbb-134">참조 된 [WSL 문제 해결 페이지](troubleshooting.md) 다른 일반적인 오류 및 해결 방법에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="24bbb-135">**0x8007007e 오류로 설치 하지 못했습니다.** 시스템 저장소에서 Linux를 지원 하지 않습니다 하는 경우이 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="24bbb-136">다음 사항을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="24bbb-136">Make sure that:</span></span>
> * <span data-ttu-id="24bbb-137">16215 이상 Windows 빌드를 실행 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="24bbb-138">[빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="24bbb-139">Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용 하도록 설정 하 고 컴퓨터 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="24bbb-140">[WSL를 사용할 수 있는지](troubleshooting.md#confirm-wsl-is-enabled)합니다.</span><span class="sxs-lookup"><span data-stu-id="24bbb-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
