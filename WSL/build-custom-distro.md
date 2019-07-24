---
title: WSL 용 사용자 지정 Linux 배포판 빌드
description: Linux 용 Windows 하위 시스템에 대 한 사용자 지정 Linux 배포를 만드는 방법에 대해 알아봅니다.
keywords: BashOnWindows, bash, wsl, windows, windows 하위 시스템, 배포판, 사용자 지정
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040779"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="5bf91-104">WSL 용 사용자 지정 Linux 배포판 만들기</span><span class="sxs-lookup"><span data-stu-id="5bf91-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="5bf91-105">오픈 소스 WSL 샘플을 사용 하 여 Microsoft Store에 대 한 WSL 배포판 패키지를 작성 하거나 테스트용 로드에 대 한 사용자 지정 Linux 배포판 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="5bf91-106">GitHub에서 [배포판 시작 관리자 리포지토리](https://github.com/Microsoft/WSL-DistroLauncher) 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="5bf91-107">이 프로젝트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-107">This project enables:</span></span>
* <span data-ttu-id="5bf91-108">WSL에서 실행 되는 appx로 Linux 배포를 패키지 하 고 제출 하는 linux 배포 유지 관리자</span><span class="sxs-lookup"><span data-stu-id="5bf91-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="5bf91-109">개발자는 자신의 개발 컴퓨터에 테스트용으로 로드 수 있는 사용자 지정 Linux 배포를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="5bf91-110">배경</span><span class="sxs-lookup"><span data-stu-id="5bf91-110">Background</span></span>
<span data-ttu-id="5bf91-111">Microsoft Store를 통해 WSL 용 Linux 배포판을 UWP 응용 프로그램으로 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="5bf91-112">WSL에서 실행 되는 응용 프로그램을 설치할 수 있습니다-Windows 커널에 상주 하는 하위 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="5bf91-113">이 전달 메커니즘에는 [이전 블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)에 설명 된 것 처럼 많은 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="5bf91-114">사용자 지정 Linux 배포판 패키지를 테스트용 로드</span><span class="sxs-lookup"><span data-stu-id="5bf91-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="5bf91-115">사용자 지정 Linux 배포판 패키지를 개인용 컴퓨터의 테스트용으로 로드에 대 한 응용 프로그램으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="5bf91-116">배포 유지 관리자로 제출 하지 않으면 사용자 지정 패키지는 Microsoft Store를 통해 배포 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="5bf91-117">테스트용으로 로드 apps에 대 한 컴퓨터를 설정 하려면 "개발자 용"의 시스템 설정에서 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="5bf91-118">개발자 모드 또는 테스트용으로 로드 apps가 선택 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="5bf91-119">Linux 배포판 유지 관리자</span><span class="sxs-lookup"><span data-stu-id="5bf91-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="5bf91-120">스토어에 제출 하려면 microsoft와 협력 하 여 게시 승인을 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="5bf91-121">Microsoft Store에 배포를 추가 하는 데 관심이 있는 Linux 배포 소유자 인 경우에 게 문의 wslpartners@microsoft.com하세요.</span><span class="sxs-lookup"><span data-stu-id="5bf91-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="5bf91-122">시작하기</span><span class="sxs-lookup"><span data-stu-id="5bf91-122">Getting Started</span></span>
<span data-ttu-id="5bf91-123">[배포판 시작 관리자 GitHub 리포지토리의](https://github.com/Microsoft/WSL-DistroLauncher) 지침에 따라 사용자 지정 Linux 배포판 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5bf91-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="5bf91-124">팀 블로그</span><span class="sxs-lookup"><span data-stu-id="5bf91-124">Team Blogs</span></span>
*  [<span data-ttu-id="5bf91-125">Linux 배포 유지 관리자 및 테스트용 로드 사용자 지정 Linux 배포에 대 한 WSL 샘플 열기</span><span class="sxs-lookup"><span data-stu-id="5bf91-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="5bf91-126">명령줄 블로그</span><span class="sxs-lookup"><span data-stu-id="5bf91-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="5bf91-127">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="5bf91-127">Provide Feedback</span></span>
* [<span data-ttu-id="5bf91-128">배포판 시작 관리자 GitHub 리포지토리</span><span class="sxs-lookup"><span data-stu-id="5bf91-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="5bf91-129">WSL 용 GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="5bf91-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="5bf91-130">명령줄 UserVoice 포털</span><span class="sxs-lookup"><span data-stu-id="5bf91-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
