---
title: Windows 10에 Linux 용 Windows 하위 시스템 (WSL) 설치
description: Windows 10에서 Linux 용 Windows 하위 시스템에 대 한 설치 지침을 참조 하세요.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499290"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="5a203-104">Windows 10 용 windows 하위 시스템 설치 가이드</span><span class="sxs-lookup"><span data-stu-id="5a203-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="5a203-105">Linux 용 Windows 하위 시스템 설치</span><span class="sxs-lookup"><span data-stu-id="5a203-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="5a203-106">WSL 용 Linux 배포판을 설치 하기 전에 "Linux 용 Windows 하위 시스템" 옵션 기능이 사용 되도록 설정 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="5a203-107">관리자 권한으로 PowerShell을 열고 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="5a203-108">메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="5a203-109">선택한 Linux 배포를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="5a203-110">기본 배포판를 다운로드 하 고 설치 하려면 다음 세 가지 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="5a203-111">Microsoft Store에서 다운로드 하 여 설치 합니다 (아래 참조).</span><span class="sxs-lookup"><span data-stu-id="5a203-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="5a203-112">명령줄/스크립트에서 다운로드 및 설치 ([수동 설치 지침 참조](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="5a203-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="5a203-113">다운로드 및 수동으로 압축 풀기 및 설치 (Windows Server에 대 한 [지침](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="5a203-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="5a203-114">Windows 10의 작성자 업데이트 이상: Microsoft Store에서 설치</span><span class="sxs-lookup"><span data-stu-id="5a203-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="5a203-115">이 섹션은 Windows 빌드 16215 이상에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="5a203-116">[빌드를 확인](troubleshooting.md#check-your-build-number)하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="5a203-117">Microsoft Store를 열고 즐겨 사용 하는 Linux 배포를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store의 Linux 배포판 보기](media/store.png)

    <span data-ttu-id="5a203-119">다음 링크는 각 배포에 대 한 Microsoft store 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="5a203-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="5a203-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="5a203-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="5a203-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="5a203-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="5a203-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="5a203-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="5a203-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="5a203-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="5a203-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="5a203-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="5a203-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="5a203-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="5a203-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="5a203-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="5a203-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="5a203-128">WSL 용 Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="5a203-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="5a203-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="5a203-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="5a203-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="5a203-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="5a203-131">알파인 WSL</span><span class="sxs-lookup"><span data-stu-id="5a203-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="5a203-132">배포판의 페이지에서 "가져오기"를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-132">From the distro's page, select "Get"</span></span>

    ![Microsoft store의 Linux 배포판 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="5a203-134">배포판의 초기화를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-134">Complete initialization of your distro</span></span>
<span data-ttu-id="5a203-135">이제 Linux 배포판가 설치 되었으므로 [새 배포판 인스턴스](initialize-distro.md) 를 사용 하려면 먼저 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5a203-136">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="5a203-136">Troubleshooting:</span></span> 

<span data-ttu-id="5a203-137">관련 오류 및 권장 픽스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="5a203-138">다른 일반적인 오류 및 해결 방법에 대해서는 [Wsl 문제 해결 페이지](troubleshooting.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a203-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="5a203-139">**0x80070003 오류로 인해 설치 하지 못했습니다.**</span><span class="sxs-lookup"><span data-stu-id="5a203-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="5a203-140">Linux 용 Windows 하위 시스템은 시스템 드라이브 에서만 실행 됩니다 (일반적으로 `C:` 드라이브).</span><span class="sxs-lookup"><span data-stu-id="5a203-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="5a203-141">배포판가 시스템 드라이브에 저장 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="5a203-142">**설정** -> **저장소** 저장소 추가저장소->설정: \*\* 새 콘텐츠가 저장\*\*
    된위치를변경하여C:드라이브에앱을설치하는시스템설정그림![](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="5a203-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="5a203-143">**오류 0x8007019e를 사용 하 여 WslRegisterDistribution 실패**</span><span class="sxs-lookup"><span data-stu-id="5a203-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="5a203-144">Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="5a203-145">**제어판** -> **프로그램 및 기능** 을 엽니다.-> \* \* windows 기능 사용/사용 안 함 \* \*-> **Linux 용 windows 하위 시스템** 을 확인 하거나이 문서의 시작 부분에 설명 된 PowerShell cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a203-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
