---
title: Windows 10에서 Linux (WSL) 용 Windows 하위 시스템을 설치 합니다.
description: Windows 10에서 Linux 용 Windows 하위 시스템에 대 한 설치 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035055"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="1e358-104">Windows 10 용 Linux 설치 가이드 용 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="1e358-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="1e358-105">Linux 용 Windows 하위 시스템을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="1e358-106">WSL에 대 한 모든 Linux 배포판을 설치 하기 전에 "Windows 하위 시스템에 대 한 Linux" 선택적 기능을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="1e358-107">관리자 권한으로 PowerShell을 열고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="1e358-108">메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="1e358-109">선택한 Linux 배포를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="1e358-110">를 다운로드 하 여 기본 distro(s)를 설치 하는 세 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="1e358-111">(아래 참조) Windows 스토어에서 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="1e358-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="1e358-112">Command 명령줄/스크립트에서 다운로드 및 설치 ([수동 설치 지침을 읽고](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="1e358-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="1e358-113">다운로드 하 고 수동으로 풀고 설치 (Windows Server-에 대 한 [지침이](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="1e358-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="1e358-114">Windows 10 Fall Creators Update 이상: Microsoft Store 설치</span><span class="sxs-lookup"><span data-stu-id="1e358-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="1e358-115">이 섹션에서는 Windows 빌드 16215 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="1e358-116">다음이 단계를 수행 [빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="1e358-117">Microsoft Store 열고 원하는 Linux 배포판을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Windows 스토어에서 Linux 배포판의 보기](media/store.png)

    <span data-ttu-id="1e358-119">다음 링크는 각 배포에 대 한 Windows 스토어 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="1e358-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="1e358-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="1e358-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="1e358-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="1e358-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="1e358-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="1e358-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="1e358-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="1e358-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="1e358-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="1e358-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="1e358-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="1e358-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="1e358-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="1e358-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="1e358-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="1e358-128">WSL에 대 한 fedora Remix</span><span class="sxs-lookup"><span data-stu-id="1e358-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="1e358-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="1e358-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="1e358-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="1e358-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="1e358-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="1e358-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="1e358-132">배포판의 페이지에서 "Get"을 선택</span><span class="sxs-lookup"><span data-stu-id="1e358-132">From the distro's page, select "Get"</span></span>

    ![Windows 스토어에서 Linux 배포판의 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="1e358-134">배포의 초기화를 완료</span><span class="sxs-lookup"><span data-stu-id="1e358-134">Complete initialization of your distro</span></span>
<span data-ttu-id="1e358-135">이제 Linux 배포를 설치 해야 [새 배포판 인스턴스를 초기화](initialize-distro.md) 번 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e358-136">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="1e358-136">Troubleshooting:</span></span> 

<span data-ttu-id="1e358-137">다음은 관련된 오류 및 제안 된 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="1e358-138">참조 된 [WSL 문제 해결 페이지](troubleshooting.md) 다른 일반적인 오류 및 해결 방법에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="1e358-139">**설치 0x80070003 오류로 실패 합니다.**</span><span class="sxs-lookup"><span data-stu-id="1e358-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="1e358-140">Linux 용 Windows 하위 시스템은 시스템 드라이브에만 실행 됩니다 (이 일반적으로 프로그램 `C:` 드라이브).</span><span class="sxs-lookup"><span data-stu-id="1e358-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="1e358-141">배포판은 시스템 드라이브에 저장 되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="1e358-142">오픈 **설정을** -> **Storage** -> **더 많은 저장소 설정: 새 콘텐츠 저장 위치 변경**
    ![c: 드라이브에 앱을 설치 시스템 설정의 그림](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="1e358-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="1e358-143">**WslRegisterDistribution 0x8007019e 오류로 인해 실패 했습니다**</span><span class="sxs-lookup"><span data-stu-id="1e358-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="1e358-144">선택적 구성 요소 사용 가능 하지는 Linux 용 Windows 하위 시스템:</span><span class="sxs-lookup"><span data-stu-id="1e358-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="1e358-145">열기 **Control Panel** -> **프로그램 및 기능** -> \* \* Windows 기능 설정 또는 해제 \* \*-> **Linux 용 Windows 하위 시스템** 알거나는 이 문서의 시작 부분에서 언급 한 PowerShell cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
