---
title: WSL에 대 한 사용자 지정 Linux 배포판으로 빌드
description: Linux 용 Windows 하위 시스템에 대 한 사용자 지정 Linux 배포를 만드는 방법에 알아봅니다.
keywords: BashOnWindows, bash, wsl, windows, windows 하위 시스템, 배포, 사용자 지정
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040779"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="3ea42-104">WSL에 대 한 사용자 지정 Linux 배포판으로 만들기</span><span class="sxs-lookup"><span data-stu-id="3ea42-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="3ea42-105">Microsoft Store 대 한 WSL 배포판의 패키지를 빌드 및/또는 테스트용 로드에 대 한 사용자 지정 Linux 배포판 패키지를 만들려면 오픈 소스 WSL 샘플을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="3ea42-106">찾을 수 있습니다 합니다 [배포판 launcher 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) github입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="3ea42-107">이 프로젝트는 다음 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-107">This project enables:</span></span>
* <span data-ttu-id="3ea42-108">패키지 및 WSL에서 실행 되는 appx로 Linux 배포를 제출 하려면 Linux 배포 유지 관리자</span><span class="sxs-lookup"><span data-stu-id="3ea42-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="3ea42-109">개발자는 자신의 개발 컴퓨터에 테스트용으로 로드 될 수 있습니다. 있는 사용자 지정 Linux 배포를 만들 수</span><span class="sxs-lookup"><span data-stu-id="3ea42-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="3ea42-110">배경</span><span class="sxs-lookup"><span data-stu-id="3ea42-110">Background</span></span>
<span data-ttu-id="3ea42-111">Microsoft Store 통해 UWP 응용 프로그램으로 WSL에 대 한 Linux 배포판을 배포 했습니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="3ea42-112">WSL-Windows 커널에 있는 하위 시스템에 실행 한 다음 해당 응용 프로그램을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="3ea42-113">이 배달 메커니즘에서 설명한 것 처럼 많은 이점이 있습니다는 [이전 블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="3ea42-114">사용자 지정 Linux 배포판의 패키지를 테스트용으로 로드</span><span class="sxs-lookup"><span data-stu-id="3ea42-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="3ea42-115">개인 컴퓨터에 테스트용으로 로드 하려면 응용 프로그램으로 사용자 지정 Linux 배포판 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="3ea42-116">사용자 지정 패키지는 배포 되지 Microsoft Store 통해 배포 유지 관리자는으로 제출 하지 않는 한 note 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3ea42-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="3ea42-117">앱 사이드 로드 하기 위해 컴퓨터를 설정 하려면 "For Developers" 시스템 설정에서이 기능을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="3ea42-118">개발자 모드 또는 테스트용 로드 앱을 선택한 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="3ea42-119">Linux 배포판 유지 관리자에 대 한</span><span class="sxs-lookup"><span data-stu-id="3ea42-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="3ea42-120">스토어에 제출 하려면 게시 승인을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="3ea42-121">Microsoft Store 배포 추가 원하는 Linux 배포 소유자 인 경우 문의 wslpartners@microsoft.com합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="3ea42-122">시작하기</span><span class="sxs-lookup"><span data-stu-id="3ea42-122">Getting Started</span></span>
<span data-ttu-id="3ea42-123">지침에 따라 합니다 [배포판 Launcher GitHub 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) 사용자 지정 Linux 배포판 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ea42-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="3ea42-124">팀 블로그</span><span class="sxs-lookup"><span data-stu-id="3ea42-124">Team Blogs</span></span>
*  [<span data-ttu-id="3ea42-125">Linux 배포 유지 관리자 및 테스트용으로 로드할 사용자 지정 Linux 배포에 대 한 WSL 샘플 소싱 열기</span><span class="sxs-lookup"><span data-stu-id="3ea42-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="3ea42-126">명령줄 블로그</span><span class="sxs-lookup"><span data-stu-id="3ea42-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="3ea42-127">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="3ea42-127">Provide Feedback</span></span>
* [<span data-ttu-id="3ea42-128">배포판 Launcher GitHub 리포지토리</span><span class="sxs-lookup"><span data-stu-id="3ea42-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="3ea42-129">WSL에 대 한 GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="3ea42-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="3ea42-130">명령줄 UserVoice 포털</span><span class="sxs-lookup"><span data-stu-id="3ea42-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
