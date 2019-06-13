---
title: Windows Server에서 Linux 하위 시스템을 설치
description: Windows Server에서 Linux 하위 시스템에 대 한 설치 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, windows server 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 25723395212575f8fe2dcbfbd30b59de9431816a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035070"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="6db49-104">Windows Server 설치 가이드</span><span class="sxs-lookup"><span data-stu-id="6db49-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="6db49-105">이상 Windows Server 2019에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="6db49-106">/ / Linux 용 Windows 하위 시스템 되도록 Build2017, Microsoft 발표 [Windows Server에서 사용할 수 있는](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="6db49-107">이러한 지침은 Windows Server 1709 이상 Linux 용 Windows 하위 시스템을 실행 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="6db49-108">Linux (WSL) 용 Windows 하위 시스템을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="6db49-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="6db49-109">Windows에서 Linux 배포판을 실행할 수 있습니다, 전에 "Windows 하위 시스템에 대 한 Linux" 선택적 기능을 사용 하도록 설정 하 고 다시 부팅 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="6db49-110">관리자 권한으로 PowerShell을 열고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="6db49-111">메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-111">Restart your computer when prompted.</span></span> <span data-ttu-id="6db49-112">**이 다시 부팅 해야** WSL 신뢰할 수 있는 실행 환경을 시작할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="6db49-113">Linux 배포판을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-113">Download a Linux distro</span></span>

<span data-ttu-id="6db49-114">따릅니다 [이러한 지침](install-manual.md) 원하는 Linux 배포를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="6db49-115">압축을 풀고 Linux 배포판을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="6db49-116">배포판을를 다운로드 한 했으므로 해당 내용을 추출 하 고 수동으로 배포판을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="6db49-117">추출 된 `<distro>.appx` 예: PowerShell을 사용 하 여 패키지의 내용:</span><span class="sxs-lookup"><span data-stu-id="6db49-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="6db49-118">명명 된 설치를 완료 하려면 대상 폴더에서 배포판 시작 관리자 응용 프로그램을 실행 배포판 시작 관리자를 실행 `<distro>.exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="6db49-119">예를 들어: `ubuntu.exe`등입니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server에서 확장 된 Ubuntu 배포판](media/server-appx-expand.png)

    > <span data-ttu-id="6db49-121">**문제 해결**</span><span class="sxs-lookup"><span data-stu-id="6db49-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="6db49-122">**0x8007007e 오류로 설치 하지 못했습니다.** : 이 오류는 시스템 WSL를 지원 하지 않습니다 하는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="6db49-123">다음 사항을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="6db49-123">Make sure that:</span></span>
    >   * <span data-ttu-id="6db49-124">16215 이상 Windows 빌드를 실행 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="6db49-125">[빌드를 확인할](troubleshooting.md#check-your-build-number)합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="6db49-126">Linux 선택적 구성 요소에 대 한 Windows 하위 시스템을 사용 하도록 설정 하 고 컴퓨터 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="6db49-127">[WSL를 사용할 수 있는지](troubleshooting.md#confirm-wsl-is-enabled)합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="6db49-128">Windows 환경 경로에 배포판 경로 추가 (`C:\Users\Administrator\Ubuntu` 이 예제의), 예: Powershell을 사용 하 여:</span><span class="sxs-lookup"><span data-stu-id="6db49-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="6db49-129">입력 하 여 이제 모든 경로에서 배포를 시작할 수 있습니다 `<distro>.exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="6db49-130">예: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="6db49-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="6db49-131">이제 Linux 배포를 설치 해야 [새 배포판 인스턴스를 초기화](initialize-distro.md) 배포를 사용 하기 전에 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db49-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
