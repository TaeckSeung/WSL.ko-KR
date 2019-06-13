---
title: WSL 2를 설치 합니다.
description: WSL 2에 대 한 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038083"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="9f271-104">WSL 2에 대 한 설치 지침</span><span class="sxs-lookup"><span data-stu-id="9f271-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="9f271-105">설치 하 고 사용 하 여 시작 WSL 2는 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="9f271-106">' 가상 컴퓨터 플랫폼 ' 선택적 구성 요소를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="9f271-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="9f271-107">WSL 2 명령줄을 사용 하 여 지원 되는 배포판 설정</span><span class="sxs-lookup"><span data-stu-id="9f271-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="9f271-108">사용할 WSL에 배포판의 버전 확인</span><span class="sxs-lookup"><span data-stu-id="9f271-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="9f271-109">' 가상 컴퓨터 플랫폼 ' 선택적 구성 요소를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="9f271-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="9f271-110">관리자 권한으로 PowerShell을 열고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="9f271-111">이러한 변경 내용을 사용 하도록 설정 된 후 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="9f271-112">WSL 2 명령줄을 사용 하 여 지원 되는 배포판 설정</span><span class="sxs-lookup"><span data-stu-id="9f271-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="9f271-113">Powershell을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="9f271-114">바꿔야 및 `<Distro>` 배포의 실제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="9f271-115">(이러한 명령을 사용 하 여 찾을 수 있습니다: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="9f271-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="9f271-116">위와 동일한 명령을 실행 하지만 ' 2'와 ' 1'을 대체 하 여 언제 든 지에서 WSL 1로 다시 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="9f271-117">또한 WSL 2 기본 아키텍처를 확인 하려면이 명령을 사용 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="9f271-118">모든 이렇게 하면 설치 하는 새 배포판 WSL 2 배포판으로 초기화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="9f271-119">사용할 WSL 배포의 버전 확인 완료</span><span class="sxs-lookup"><span data-stu-id="9f271-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="9f271-120">확인 하려면 다음 명령을 사용 하는 각 배포판을 사용 하는 WSL의 어떤 버전:</span><span class="sxs-lookup"><span data-stu-id="9f271-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="9f271-121">`wsl --list --verbose` 또는 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="9f271-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="9f271-122">위에서 선택한 배포판 'version' 열 아래에 있는 '2'를 이제 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f271-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="9f271-123">이 과정을 완료 했으므로 자유롭게 WSL 2 배포를 사용 하 여 시작 하십시오!</span><span class="sxs-lookup"><span data-stu-id="9f271-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 