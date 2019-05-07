---
title: 수동으로 Windows 하위 시스템 (WSL) Linux 배포판에 대 한 다운로드
description: Linux 배포판에 대 한 Windows 하위 시스템을 수동으로 다운로드 하는 방법에 대 한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, WSL, 용 windows 하위 시스템 배포판, windows 하위 시스템, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063571"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="23a3a-104">Linux 배포판의 패키지에 대 한 Windows 하위 시스템을 수동으로 다운로드</span><span class="sxs-lookup"><span data-stu-id="23a3a-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="23a3a-105">일부의 시나리오는 사용자 수 없습니다 수 (또는 원하는)을 설치 하려면 Microsoft Store 통해 WSL Linux 배포판입니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="23a3a-106">특히 있습니다 Windows Server 또는 장기 서비스 (LTSB/LTSC) 데스크톱 Microsoft Store 또는 사용자 회사 네트워크 정책 및/또는 관리자 환경에서 Microsoft Store 사용을 허용 하지 않으려면 지원 하지 않는 OS SKU를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="23a3a-107">이러한 경우에 WSL 자체를 사용할 수 있는, 어떻게 있습니다 다운로드 하 고 저장소에 액세스할 수 없으면 Linux 배포판 WSL 설치?</span><span class="sxs-lookup"><span data-stu-id="23a3a-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="23a3a-108">참고: **명령줄 셸 환경 Cmd, PowerShell 및/WSL Linux 배포판을 비롯 하 여 Windows 10 S 모드에서 실행 되도록 허용 되지 않습니다**합니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="23a3a-109">이 제한은 S 모드를 제공 하는 무결성 및 보안 목표를 보장 하기 위해 존재 합니다. 읽기 [이 게시물](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="23a3a-110">배포판을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-110">Downloading distros</span></span>

<span data-ttu-id="23a3a-111">Microsoft Store 앱을 사용할 수 없는 경우 다운로드 하 고 이러한 링크를 클릭 하 여 Linux 배포판을 수동으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="23a3a-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="23a3a-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="23a3a-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="23a3a-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="23a3a-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="23a3a-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="23a3a-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="23a3a-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="23a3a-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="23a3a-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="23a3a-117">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="23a3a-117">OpenSUSE</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="23a3a-118">SLES</span><span class="sxs-lookup"><span data-stu-id="23a3a-118">SLES</span></span>](https://aka.ms/wsl-sles-12)

<span data-ttu-id="23a3a-119">이렇게 하면는 `<distro>.appx` 선택한 폴더에 다운로드 하려면 패키지 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-119">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="23a3a-120">수행 합니다 [설치 지침](#installing-your-distro) 에 다운로드 한 distro(s) 설치.</span><span class="sxs-lookup"><span data-stu-id="23a3a-120">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="23a3a-121">명령줄을 통해 다운로드 배포판</span><span class="sxs-lookup"><span data-stu-id="23a3a-121">Downloading distros via the command line</span></span>
<span data-ttu-id="23a3a-122">원한다 면 명령줄을 통해 기본 distro(s)에도 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-122">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="23a3a-123">PowerShell을 사용 하 여 다운로드</span><span class="sxs-lookup"><span data-stu-id="23a3a-123">Download using PowerShell</span></span>
 <span data-ttu-id="23a3a-124">PowerShell을 사용 하는 배포판을 다운로드 하려면 사용 합니다 [Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a3a-124">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="23a3a-125">다음은 Ubuntu 16.04를 다운로드 하는 샘플 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-125">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="23a3a-126">다운로드 시간이 오래 걸리면, 설정 하 여 진행률 표시줄 해제 `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="23a3a-126">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="23a3a-127">Curl을 사용 하 여 다운로드</span><span class="sxs-lookup"><span data-stu-id="23a3a-127">Download using curl</span></span>
<span data-ttu-id="23a3a-128">Windows 10 Spring 2018 업데이트 (또는 이상)는 인기 있는 포함 [명령줄 유틸리티 curl](https://curl.haxx.se/) 는 사용 하 여 명령줄에서 웹 요청 (예: HTTP GET, POST, PUT, 명령 등)를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-128">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="23a3a-129">사용할 수 있습니다 `curl.exe` 위의 배포판을 다운로드 하려면:</span><span class="sxs-lookup"><span data-stu-id="23a3a-129">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="23a3a-130">위의 예에서 `curl.exe` 실행 됩니다 (뿐만 아니라 `curl`), PowerShell에서 실제 curl 실행 파일 인지 확인 호출 별칭 PowerShell curl 없습니다 [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="23a3a-130">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="23a3a-131">참고: 사용 하 여 `curl` Cmd 셸을 사용 하 여 다운로드 단계 호출/스크립트에 있는 경우에 좋을 수 있습니다 및/또는 `.bat`  /  `.cmd` 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-131">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="23a3a-132">배포를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="23a3a-132">Installing your distro</span></span>
<span data-ttu-id="23a3a-133">다운로드 한 distro(s) 프로그램을 설치 하는 방법에 지침을 참조 하십시오 합니다 [Windows 데스크톱](install-win10.md) 또는 [Windows Server](install-on-server.md) 설치 지침.</span><span class="sxs-lookup"><span data-stu-id="23a3a-133">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
