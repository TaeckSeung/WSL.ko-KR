---
title: 설치 또는 Windows 10 1 주년 업데이트 또는 크리에이터 스 업데이트에서 제거
description: 레거시, Windows 10 1 주년 업데이트 또는 크리에이터 스 업데이트에서 베타 배포판에 대 한 지침을 설치 및 제거
keywords: 설치, 제거, 취소-설치, 제거 BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10, 레거시, 베타, 용 windows 하위 시스템 삭제에 사용 되지 않음
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040841"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="a200a-104">설치 또는 Windows 10 1 주년 업데이트 및 크리에이터 업데이트의 Linux 용 Windows 하위 시스템을 제거 하는 가이드</span><span class="sxs-lookup"><span data-stu-id="a200a-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="a200a-105">Windows 10 크리에이터 스 업데이트를 실행 하는 하거나 나중에 하세요 [Windows 10 설치 지침을 따릅니다](install-win10.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="a200a-106"><strong><em><span style="color: #f28014">다음 지침은 Windows 10 1 주년 업데이트 또는 Windows 10 크리에이터 스 업데이트를 실행 하는 사용자에 대 한</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="a200a-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="a200a-107">Windows 10 Fall Creators Update (버전 1709), WSL 베타 기능으로 릴리스된 전과 "Bash에서 Ubuntu의 Windows" (또는 Bash.exe)를 처음 실행할 때 단일 Ubuntu 인스턴스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="a200a-108">WSL를 사용 하 여 이전 Windows 10 버전에이 베타 "레거시 배포판" 이제 사용 되지 않는 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="a200a-109">사용 가능한 Windows 10의 최신 버전을 실행 하려면 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="a200a-110">각각의 새 Windows 10 릴리스 WSL 단독으로 Linux 도구 및 WSL에서 올바르게 실행 되도록 앱을 더 수정 및 개선 사항에 수백 개의 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="a200a-111">Fall Creators Update 이상을 업그레이드할 수 없는 경우, 설정 및 WSL를 사용 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="a200a-112">개발자 모드에서 실행 되도록 WSL Creators Update 또는 Windows 10 1 주년 업데이트 설정, 개발자 모드가 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="a200a-113">오픈 **설정을** -> **업데이트 및 보안** -> **개발자를 위한**</span><span class="sxs-lookup"><span data-stu-id="a200a-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="a200a-114">개발자 모드 라디오 단추를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-114">Select the Developer Mode radio button</span></span>  
    ![개발자 모드 사용](media/updateAndSecurity.png)

    > <span data-ttu-id="a200a-116">개발자 모드를 사용 하도록 설정 하는 요구 사항이 된 [Windows 10 Fall Creators Update 제거](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="a200a-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="a200a-117">명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-117">Open a command prompt.</span></span>  <span data-ttu-id="a200a-118">형식 `bash` 하 고 enter 키를 누릅니다</span><span class="sxs-lookup"><span data-stu-id="a200a-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="a200a-119">처음에 Windows, Ubuntu에서 Bash를 실행 Canonical의 라이선스에 동의 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="a200a-120">WSL 다운로드 되 고 컴퓨터에 Ubuntu 인스턴스 설치에 동의 하 고 "Bash에서 Ubuntu의 Windows" 바로 가기를 시작 메뉴에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Ubuntu를 설치 하 라는 메시지가](media/bashShellInstall.png)

    <span data-ttu-id="a200a-122">처음에 Windows, Ubuntu에서 Bash를 실행 UNIX 사용자 이름 및 암호를 만들려고 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="a200a-123">수행 합니다 [새 배포판 인스턴스 지침](initialize-distro.md) 설치를 완료 하려면</span><span class="sxs-lookup"><span data-stu-id="a200a-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="a200a-124">새 Ubuntu 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="a200a-125">실행 `bash` 명령 프롬프트에서</span><span class="sxs-lookup"><span data-stu-id="a200a-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="a200a-126">시작 메뉴 "Bash에서 Ubuntu의 Windows" 바로 가기를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="a200a-127">레거시 배포판 제거/제거</span><span class="sxs-lookup"><span data-stu-id="a200a-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="a200a-128">WSL 설치는 이전 Windows 10 버전의 Windows 10 Fall Creators Update 업그레이드 하면 기존 배포는 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="a200a-129">그러나 강력한 새 저장소 제공 배포판 ASAP를 설치 하는 것이 좋습니다 하 고 레거시 배포에서 모든 필요한 파일, 데이터 등을 새 배포로 마이그레이션.</span><span class="sxs-lookup"><span data-stu-id="a200a-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="a200a-130">컴퓨터에서 레거시 배포판을 제거 하려면 다음 명령줄 또는 PowerShell 인스턴스에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="a200a-131">레거시 배포판을 수동으로 삭제</span><span class="sxs-lookup"><span data-stu-id="a200a-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="a200a-132">원한다 면 기존 인스턴스를 수동으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="a200a-133">사용 하 여 레거시 배포판 제거 하는 문제가 발생 하는 경우 필요할 수 있습니다 `lxrun.exe`, 또는 Windows 10 Spring 2018 업데이트를 실행 하는 (또는 이상)와 함께 제공 되지 않는 `lxrun.exe`합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="a200a-134">레거시 WSL 배포를 강제로 삭제 하려면 삭제 된 `%localappdata%\lxss\` 폴더 (및 모든 하위 콘텐츠의) Windows의 파일 탐색기 또는 명령줄을 사용 하 여:</span><span class="sxs-lookup"><span data-stu-id="a200a-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="a200a-135">PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="a200a-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="a200a-136">Cmd를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a200a-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
