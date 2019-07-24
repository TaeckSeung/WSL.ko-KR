---
title: Linux 용 Windows 하위 시스템 (WSL) Distros를 수동으로 다운로드 합니다.
description: Linux 배포판에 대 한 Windows 하위 시스템을 수동으로 다운로드 하는 방법에 대 한 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, WSL, windows 하위 시스템, 배포판, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 55cea2c4b7087f3dd8a29986aaddc8c313763448
ms.sourcegitcommit: b07769a3140db9ac63e42c7d7d1290c0bad8c40d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467557"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="9aa8f-104">Linux 배포판 패키지에 대 한 Windows 하위 시스템 수동으로 다운로드</span><span class="sxs-lookup"><span data-stu-id="9aa8f-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="9aa8f-105">Microsoft Store를 통해 WSL Linux 배포판을 설치 하거나 원하지 않는 몇 가지 시나리오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="9aa8f-106">특히 Microsoft Store을 지원 하지 않는 LTSB/LTSC (장기 서비스) 데스크톱 OS SKU 또는 사용자 환경에서 Microsoft Store 사용을 허용 하지 않는 회사 네트워크 정책 및/또는 관리자를 실행 하 고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="9aa8f-107">이러한 경우 WSL 자체를 사용할 수 있는 동안 스토어에 액세스할 수 없는 경우 WSL에서 Linux 배포판을 다운로드 하 여 설치 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9aa8f-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="9aa8f-108">참고: **Cmd, PowerShell 및 Linux/WSL 배포판을 포함 하는 명령줄 셸 환경은 Windows 10 S 모드에서 실행할 수 없습니다**.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="9aa8f-109">이러한 제한은 S 모드에서 제공 하는 무결성 및 보안 목표를 보장 하기 위해 존재 합니다. 자세한 내용은 [이 게시물](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="9aa8f-110">배포판 다운로드 중</span><span class="sxs-lookup"><span data-stu-id="9aa8f-110">Downloading distros</span></span>

<span data-ttu-id="9aa8f-111">Microsoft Store 앱을 사용할 수 없는 경우 다음 링크를 클릭 하 여 Linux 배포판을 다운로드 하 고 수동으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="9aa8f-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="9aa8f-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="9aa8f-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="9aa8f-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="9aa8f-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="9aa8f-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="9aa8f-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="9aa8f-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="9aa8f-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="9aa8f-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="9aa8f-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="9aa8f-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="9aa8f-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="9aa8f-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="9aa8f-119">WSL 용 Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="9aa8f-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="9aa8f-120">이렇게 하면 `<distro>.appx` 패키지가 선택한 폴더로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="9aa8f-121">[설치 지침](#Installing-your-distro) 에 따라 다운로드 한 배포판를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-121">Follow the [installation instructions](#Installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="9aa8f-122">명령줄을 통해 배포판 다운로드</span><span class="sxs-lookup"><span data-stu-id="9aa8f-122">Downloading distros via the command line</span></span>
<span data-ttu-id="9aa8f-123">원하는 경우 명령줄을 통해 기본 설정 배포판를 다운로드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="9aa8f-124">PowerShell을 사용 하 여 다운로드</span><span class="sxs-lookup"><span data-stu-id="9aa8f-124">Download using PowerShell</span></span>
 <span data-ttu-id="9aa8f-125">PowerShell을 사용 하 여 배포판를 다운로드 하려면 [호출 WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="9aa8f-126">Ubuntu 16.04을 다운로드 하는 샘플 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="9aa8f-127">다운로드 시간이 오래 걸리는 경우을 설정 하 여 진행률 표시줄을 해제 합니다.`$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="9aa8f-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="9aa8f-128">말아를 사용 하 여 다운로드</span><span class="sxs-lookup"><span data-stu-id="9aa8f-128">Download using curl</span></span>
<span data-ttu-id="9aa8f-129">Windows 10 스프링 2018 업데이트 (이상)에는 명령줄에서 웹 요청 (예: HTTP GET, POST, PUT 등)을 호출할 수 있는 인기 있는 [말아 명령줄 유틸리티가](https://curl.haxx.se/) 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="9aa8f-130">를 사용 `curl.exe` 하 여 위의 배포판을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="9aa8f-131">위의 예에서를 실행 하 `curl.exe` 는 것이 아니라, `curl`powershell에서 실제 말아 실행 파일을 호출 하 여 [호출-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) 에 대 한 powershell 말아 앨리어스가 아닌를 실행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="9aa8f-132">참고: Cmd `curl` shell 및/또는 `.bat`  /  스크립트를 사용 하 여 다운로드 단계를 호출/스크립팅 해야 하는 경우를 사용 하는 것이 좋습니다. `.cmd`</span><span class="sxs-lookup"><span data-stu-id="9aa8f-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="9aa8f-133">배포판 설치</span><span class="sxs-lookup"><span data-stu-id="9aa8f-133">Installing your distro</span></span>
<span data-ttu-id="9aa8f-134">Windows 10을 사용 하는 경우 PowerShell을 사용 하 여 배포판를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="9aa8f-135">위에서 다운로드 한 배포판이 포함 된 폴더로 이동 하 고 해당 디렉터리에서 다음 명령을 실행 합니다. 여기서 `app_name` 는 배포판 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="9aa8f-136">Windows server를 사용 하는 경우 [Windows server](install-on-server.md) 설명서 페이지에서 설치 지침을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="9aa8f-137">배포판가 설치 되 면 [Intilization 단계](initialize-distro.md) 페이지를 참조 하 여 새 배포판를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa8f-137">Once your distro is installed please refer to the [Intilization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
