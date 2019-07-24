---
title: 엔터프라이즈에 대한 Linux용 Windows 하위 시스템
description: 엔터프라이즈 환경에서 Linux 용 Windows 하위 시스템을 가장 효과적으로 사용 하는 방법에 대 한 리소스 및 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, 배포, 오프 라인, 패키징, 스토어, 배포, 설치, 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063281"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="fb086-104">엔터프라이즈에 대한 Linux용 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="fb086-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="fb086-105">비즈니스 Microsoft Store는 WSL을 회사에 배포 하려는 기업에 게 다양 한 솔루션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="fb086-106">비즈니스용 Microsoft Store에 대 한 [온라인 문서](https://docs.microsoft.com/en-us/microsoft-store/) 는 매장 환경에 대 한 일반 정보를 확인 하는 데 유용한 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="fb086-107">WSL 배포를 시작 하도록 설정 하려는 회사 라면 다음 단계를 따를 수 있습니다 .이 단계는 Microsoft Store 문서 내에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="fb086-108">비즈니스용 Microsoft Store에 등록 하 고 시작 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb086-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="fb086-109">사용자의 [제품 및 서비스를 관리 합니다 (개인 저장소의 앱에 액세스할 수 있는 사용자 포함)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="fb086-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="fb086-110">여기에서 wsl 배포판를 저장소에 추가 하 고 해당 사용자를 설치할 수 있는 사용자를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="fb086-111">선택한 배포 방법을 사용 하 여 회사에 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="fb086-112">[이러한 단계를 사용](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 하 여 선택한 배포판 또는 배포판을 설치할 수 있는 wsl 배포판에 액세스할 수 있는 사용자와 의견을 교환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="fb086-113">배포판를 오프 라인으로 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="fb086-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="fb086-114">회사의 컴퓨터에서 Microsoft Store 또는 비즈니스용 Microsoft Store에 액세스할 수 없는 경우 다음 단계를 수행 하 여 오프 라인 라이선스가 있는 Linux 배포판의 설치 관리자를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="fb086-115">AD (Azure Active Directory) 계정 설정</span><span class="sxs-lookup"><span data-stu-id="fb086-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="fb086-116">Azure AD 계정이 있어야 하 고 Microsoft Store 앱의 설치 관리자를 얻기 위해 조직의 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="fb086-117">계정이 이미 있는 경우이 단계를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="fb086-118">계정을 등록 하는 지침은 여기에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="fb086-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="fb086-119">비즈니스용 스토어에 로그인 하 고 홈 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="fb086-120">로그인: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="fb086-120">Sign in here: www.microsoft.com/business-store</span></span>

![비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="fb086-122">관리 > 설정으로 이동 하 고 ' 오프 라인 앱 표시 '를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![비즈니스용 MS 스토어 설정 페이지](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="fb086-124">' 내 그룹에 대해 구입 '을 클릭 하 여 기본 페이지로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="fb086-126">원하는 배포판을 검색 하 고 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-126">Search for your desired distro and select it</span></span>

![활성 검색을 사용 하는 비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="fb086-128">라이선스 유형 드롭다운 메뉴에서 ' 오프 라인 ' 라이선스를 선택 하 고 ' 앱 다운로드 '를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![비즈니스 Ubuntu 용 MS 스토어 제품 페이지](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="fb086-130">참고: 일부 배포판은 오프 라인 라이선스를 사용 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="fb086-131">' 관리 ' 단추를 클릭 하 여 앱의 제품 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![비즈니스 Ubuntu 용 MS 스토어 제품 페이지](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="fb086-133">아키텍처를 선택 하 고 오프 라인에서 사용할 패키지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-133">Select your architecture and download the package for offline use</span></span>

![비즈니스 Ubuntu 용 MS 스토어 제품 세부 정보 페이지](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="fb086-135">그러면 WSL을 설치 하려는 모든 컴퓨터에이 설치 관리자를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb086-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>