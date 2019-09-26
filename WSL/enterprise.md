---
title: 엔터프라이즈에 대한 Linux용 Windows 하위 시스템
description: 엔터프라이즈 환경에서 Linux 용 Windows 하위 시스템을 가장 효과적으로 사용 하는 방법에 대 한 리소스 및 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, 배포, 오프 라인, 패키징, 스토어, 배포, 설치, 설치
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269857"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>엔터프라이즈에 대한 Linux용 Windows 하위 시스템

비즈니스 Microsoft Store는 WSL을 회사에 배포 하려는 기업에 게 다양 한 솔루션을 제공 합니다. 비즈니스용 Microsoft Store에 대 한 [온라인 문서](https://docs.microsoft.com/en-us/microsoft-store/) 는 매장 환경에 대 한 일반 정보를 확인 하는 데 유용한 리소스입니다.

WSL 배포를 시작 하도록 설정 하려는 회사 라면 다음 단계를 따를 수 있습니다 .이 단계는 Microsoft Store 문서 내에서 설명 합니다.

* [비즈니스용 Microsoft Store에 등록 하 고 시작 하세요.](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* 사용자의 [제품 및 서비스를 관리 합니다 (개인 저장소의 앱에 액세스할 수 있는 사용자 포함)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). 여기에서 wsl 배포판를 저장소에 추가 하 고 해당 사용자를 설치할 수 있는 사용자를 제어할 수 있습니다.
* [선택한 배포 방법을 사용 하 여 회사에 소프트웨어를 배포 합니다.](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* [이러한 단계를 사용](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 하 여 선택한 배포판 또는 배포판을 설치할 수 있는 wsl 배포판에 액세스할 수 있는 사용자와 의견을 교환 합니다. 

## <a name="how-to-distribute-a-distro-offline"></a>배포판를 오프 라인으로 배포 하는 방법

회사의 컴퓨터에서 Microsoft Store 또는 비즈니스용 Microsoft Store에 액세스할 수 없는 경우 다음 단계를 수행 하 여 오프 라인 라이선스가 있는 Linux 배포판의 설치 관리자를 다운로드할 수 있습니다. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>AD (Azure Active Directory) 계정 설정 

Azure AD 계정이 있어야 하 고 Microsoft Store 앱의 설치 관리자를 얻기 위해 조직의 전역 관리자 여야 합니다. 계정이 이미 있는 경우이 단계를 건너뛸 수 있습니다.

계정을 등록 하는 지침은 여기에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>비즈니스용 스토어에 로그인 하 고 홈 페이지로 이동 합니다.
로그인: www.microsoft.com/business-store

![비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>관리 > 설정으로 이동 하 고 ' 오프 라인 앱 표시 '를 사용 하도록 설정 합니다.

![비즈니스용 MS 스토어 설정 페이지](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>' 내 그룹에 대해 구입 '을 클릭 하 여 기본 페이지로 돌아갑니다.

![비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>원하는 배포판을 검색 하 고 선택 합니다.

![활성 검색을 사용 하는 비즈니스용 MS 스토어 홈 페이지](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>라이선스 유형 드롭다운 메뉴에서 ' 오프 라인 ' 라이선스를 선택 하 고 ' 앱 다운로드 '를 클릭 합니다.

![비즈니스 Ubuntu 용 MS 스토어 제품 페이지](media/offlineinstallscreens/4-screen.png)

참고: 일부 배포판은 오프 라인 라이선스를 사용 하지 않도록 선택할 수 있습니다.

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>' 관리 ' 단추를 클릭 하 여 앱의 제품 페이지로 이동 합니다.

![비즈니스 Ubuntu 용 MS 스토어 제품 페이지](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>아키텍처를 선택 하 고 오프 라인에서 사용할 패키지를 다운로드 합니다.

![비즈니스 Ubuntu 용 MS 스토어 제품 세부 정보 페이지](media/offlineinstallscreens/6-screen.png)

그러면 WSL을 설치 하려는 모든 컴퓨터에이 설치 관리자를 배포할 수 있습니다.