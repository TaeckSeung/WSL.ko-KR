---
title: WSL 2에 대 한 질문과 대답
description: Frequently Asked Questions about Windows 하위 시스템에 대 한 Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038093"
---
# <a name="wsl-2-faq"></a><span data-ttu-id="55530-104">WSL 2 FAQ</span><span class="sxs-lookup"><span data-stu-id="55530-104">WSL 2 FAQ</span></span>

<span data-ttu-id="55530-105">질문과 대답 (FAQ)는 Windows 하위 시스템에 대 한 Linux 2의 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="55530-106">WSL 2에서 Hyper-v를 사용 하나요?</span><span class="sxs-lookup"><span data-stu-id="55530-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="55530-107">사용할 수 있으므로 Windows 10 Home에서?</span><span class="sxs-lookup"><span data-stu-id="55530-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="55530-108">WSL를 Windows 10 Home 비롯 하 여 현재 사용할 수 있는 WSL 2 모든 Sku에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-108">WSL 2 will be available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="55530-109">WSL의 최신 버전의 가상화를 사용 하도록 Hyper-v 아키텍처를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="55530-110">이 아키텍처는 Hyper-v 기능 하위 집합에는 선택적 구성 요소에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-110">This architecture will be available in an optional component that is a subset of the Hyper-V feature.</span></span> <span data-ttu-id="55530-111">이 선택적 구성 요소는 모든 Sku에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="55530-112">WSL 2 출시가 확정 될 때 곧이 환경에 대 한 자세한 내용을 보려면 예상할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="55530-113">WSL 1은 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="55530-113">What will happen to WSL 1?</span></span> <span data-ttu-id="55530-114">다음을 중단 되 고 있습니까?</span><span class="sxs-lookup"><span data-stu-id="55530-114">Will it be abandoned?</span></span>

<span data-ttu-id="55530-115">현재 계획이 없습니다 WSL 1의 사용을 중단 했습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="55530-116">수 WSL 1-2 WSL 배포판 나란히 실행 하 고 업그레이드를 언제 든 지 모든 배포판을 다운 그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="55530-117">새 아키텍처와 WSL 2 추가 WSL 팀 WSL Windows에서 Linux 환경을 실행 하는 훌륭한 방법을 확인 하는 기능을 제공 하는 더 나은 플랫폼을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="55530-118">WSL 2 및 VMware, VirtualBox 등 타사 가상화 도구를 실행 하는 일을 할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="55530-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="55530-119">일부 타사 응용 프로그램에는 Hyper-v WSL 2가 설정 된 경우 실행할 수 없습니다 의미는 사용 중인 경우 작동할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled.</span></span> <span data-ttu-id="55530-120">아쉽게도이 VMware 및 VirtualBox VirtualBox 6 이전 버전 (2018 년 12 월에에서 릴리스된 6.0.0 VirtualBox [대체 (fallback) 실행 핵심 Windows 호스트에서 Hyper-v는 이제] [ 1]!)</span><span class="sxs-lookup"><span data-stu-id="55530-120">Unfortunately, this does include VMware, and versions of VirtualBox before VirtualBox 6 (VirtualBox 6.0.0 released in December 2018 [now supports Hyper-V as a fallback execution core on a Windows host][1]!)</span></span>

<span data-ttu-id="55530-121">이 문제를 해결 하는 방법을 조사 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="55530-121">We are investigating ways to help resolve this issue.</span></span> <span data-ttu-id="55530-122">예를 들어, 호출 되는 Api 집합을 노출 [하이퍼바이저 플랫폼] [ 2] 제 virtualization 공급자가 소프트웨어를 Hyper-v와 호환 되도록 하는 데 사용할 수 있는</span><span class="sxs-lookup"><span data-stu-id="55530-122">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s.</span></span> <span data-ttu-id="55530-123">그러면 같은 해당 에뮬레이션에 대 한 Hyper-v 아키텍처를 사용 하는 응용 프로그램 [Google Android Emulator][3], 6 및 기준이 VirtualBox 이제 Hyper-v와 호환 되며.</span><span class="sxs-lookup"><span data-stu-id="55530-123">This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="55530-124">WSL 2에서 GPU를 액세스할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="55530-124">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="55530-125">하드웨어 지원 향상 계획이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="55530-125">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="55530-126">WSL 2 하드웨어 액세스의 초기 릴리스에서 지원 제한 됩니다 (예:): GPU, 직렬 액세스 또는 Usb 할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-126">In initial releases of WSL 2 hardware access support will be limited, e.g: you will be unable to access the GPU, serial or USBs .</span></span> <span data-ttu-id="55530-127">그러나 더 나은 장치 지원을 추가 백로그, 높은 이러한 장치와 상호 작용할 수 있는 개발자를 위한 더 많은 사용 사례가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="55530-127">However, adding better device support is high on our backlog, as this opens many more use cases for developers that wish to interact with these devices.</span></span> <span data-ttu-id="55530-128">그 동안에 직렬 포트와 USB 액세스 WSL 1를 항상 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-128">In the meantime, you can always use WSL 1 which has serial port and USB access.</span></span> <span data-ttu-id="55530-129">이 블로그 및 WSL 팀원 내부자에 최신 기능에 대 한 최신 Twitter에 주목 하세요. 작성 하 고 상호 작용 하려는 장치에 대 한 의견을 연락 하세요!</span><span class="sxs-lookup"><span data-stu-id="55530-129">Please stay tuned to this blog and WSL team members on Twitter to stay informed about the latest features coming to insider builds and reach out to give us feedback on what devices you’d like to interact with!</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="55530-130">WSL 2 네트워킹 응용 프로그램을 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="55530-130">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="55530-131">예, 응용 프로그램을 일반적인 네트워킹 더 빠를 수를 전체 시스템 호환성을 호출 했기 때문에 더 잘 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-131">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="55530-132">그러나 새 아키텍처는 가상화 된 네트워킹 구성 요소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-132">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="55530-133">이 즉, 초기 미리 보기에서 WSL 2를 작성 하는 가상 컴퓨터를 더 비슷하게 작동 합니다 (예:): WSL 2에는 호스트 컴퓨터와 다른 IP 주소를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-133">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="55530-134">WSL 1로 뻐 WSL 2 하기 위해 노력할 것입니다 및를 포함 하는 네트워킹 이야기를 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-134">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> <span data-ttu-id="55530-135">향상 된 기능을 Linux 또는 localhost를 사용 하 여 Windows에서 모든 네트워킹 앱에 액세스 하는 등, 수 만큼 빠르게 추가할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="55530-135">We expect to add improvements as quickly as we are able to, such as accessing all networking apps from Linux or Windows using localhost.</span></span> <span data-ttu-id="55530-136">WSL 2 릴리스를 접근 하는 것으로 네트워킹 스토리 및 향상 된 기능에 대 한 자세한 내용은 드리며 했습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-136">We will be posting more details about our networking story and improvements as we approach the release of WSL 2.</span></span>

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="55530-137">WSL 2 가상 컴퓨터에서 실행할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="55530-137">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="55530-138">예!</span><span class="sxs-lookup"><span data-stu-id="55530-138">Yes!</span></span> <span data-ttu-id="55530-139">가상 컴퓨터에 중첩 된 가상화를 사용 하 고 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55530-139">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="55530-140">이 관리자 권한으로 PowerShell 창에서 다음 명령을 실행 하 여 Hyper-v에서 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55530-140">This can be enabled in Hyper-V by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="55530-141">바꿔야 '&lt;VMName&gt;' 가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55530-141">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/