---
title: Windows 10에서 Linux (WSL) 용 Windows 하위 시스템을 설치
description: Windows 10에서 Linux 용 Windows 하위 시스템에 대 한 설치 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063291"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="a4a7f-104">Windows 10 용 Linux 설치 가이드 용 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="a4a7f-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="a4a7f-105">Linux 용 Windows 하위 시스템을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="a4a7f-106">WSL에 대 한 모든 Linux 배포판을 설치 하기 전에 "Windows 하위 시스템에 대 한 Linux" 선택적 기능을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="a4a7f-107">관리자 권한으로 PowerShell을 열고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="a4a7f-108">메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="a4a7f-109">선택한 Linux 배포를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="a4a7f-110">를 다운로드 하 여 기본 distro(s)를 설치 하는 세 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="a4a7f-111">(아래 참조) Windows 스토어에서 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="a4a7f-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="a4a7f-112">Command 명령줄/스크립트에서 다운로드 및 설치 ([수동 설치 지침을 읽고](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="a4a7f-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="a4a7f-113">다운로드 하 고 수동으로 풀고 설치 (Windows Server-에 대 한 [지침이](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="a4a7f-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="a4a7f-114">Windows 10 Fall Creators Update 이상: Microsoft Store 설치</span><span class="sxs-lookup"><span data-stu-id="a4a7f-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="a4a7f-115">이 섹션에서는 Windows 빌드 16215 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="a4a7f-116">다음이 단계를 수행 [빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="a4a7f-117">Microsoft Store 열고 원하는 Linux 배포판을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Windows 스토어에서 Linux 배포판의 보기](media/store.png)

    <span data-ttu-id="a4a7f-119">다음 링크는 각 배포에 대 한 Windows 스토어 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="a4a7f-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="a4a7f-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="a4a7f-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="a4a7f-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="a4a7f-122">SLES</span><span class="sxs-lookup"><span data-stu-id="a4a7f-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="a4a7f-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="a4a7f-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="a4a7f-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="a4a7f-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="a4a7f-125">배포판의 페이지에서 "Get"을 선택</span><span class="sxs-lookup"><span data-stu-id="a4a7f-125">From the distro's page, select "Get"</span></span>

    ![Windows 스토어에서 Linux 배포판의 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="a4a7f-127">배포의 초기화를 완료</span><span class="sxs-lookup"><span data-stu-id="a4a7f-127">Complete initialization of your distro</span></span>
<span data-ttu-id="a4a7f-128">이제 Linux 배포를 설치 해야 [새 배포판 인스턴스를 초기화](initialize-distro.md) 번 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a4a7f-129">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="a4a7f-129">Troubleshooting:</span></span> 

<span data-ttu-id="a4a7f-130">다음은 관련된 오류 및 제안 된 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="a4a7f-131">참조 된 [WSL 문제 해결 페이지](troubleshooting.md) 다른 일반적인 오류 및 해결 방법에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="a4a7f-132">**설치 0x80070003 오류로 실패 합니다.**</span><span class="sxs-lookup"><span data-stu-id="a4a7f-132">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="a4a7f-133">Linux 용 Windows 하위 시스템은 시스템 드라이브에만 실행 됩니다 (이 일반적으로 프로그램 `C:` 드라이브).</span><span class="sxs-lookup"><span data-stu-id="a4a7f-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="a4a7f-134">배포판은 시스템 드라이브에 저장 되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a7f-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="a4a7f-135">오픈 **설정을** -> **Storage** -> **더 많은 저장소 설정: 새 콘텐츠 저장 위치 변경**
    ![c: 드라이브에 앱을 설치 시스템 설정의 그림](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="a4a7f-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
