---
title: 엔터프라이즈에 대한 Linux용 Windows 하위 시스템
description: 리소스 및 최상의 방법에 대 한 지침 엔터프라이즈 환경에서 Linux 용 Windows 하위 시스템을 사용합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, 배포, 오프 라인 패키지, 저장소, 배포, 설치, 용 windows 하위 시스템에 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063281"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>엔터프라이즈에 대한 Linux용 Windows 하위 시스템

비즈니스용 Microsoft Store WSL 회사에 배포 하려는 기업에 다양 한 솔루션을 제공 합니다. 합니다 [온라인 문서의](https://docs.microsoft.com/en-us/microsoft-store/) 비즈니스용 Microsoft Store 대 한 저장소 환경에 대 한 일반 정보를 확인할 수 있는 훌륭한 리소스 됩니다.

회사를 가져와서 설정 검색만 하는 경우 등록 WSL 배포를 시작 하기 따르면 Microsoft Store 문서 내에서 설명 된이 단계:

* [비즈니스용 Microsoft Store 대 한 등록 및 시작](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [제품 및 서비스 등 개인 저장소에 있는 앱에 액세스할 수 있는 사용자 관리](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)합니다. 여기 WSL 배포판 저장소 및 설치할 수 있는 사용자 제어에 추가할 수 있습니다.
* [선택한 배포 메서드를 사용 하 여 회사 소프트웨어를 배포 하려면](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 수 있도록 WSL 배포판에 대 한 액세스 권한이 사용자에 게 알릴 [이 단계를 사용 하 여](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 배포판 또는 선택한 배포판 설치 

## <a name="how-to-distribute-a-distro-offline"></a>오프 라인 배포판을 배포 하는 방법

회사에서 컴퓨터 비즈니스용 Microsoft Store 또는 Microsoft Store 대 한 액세스에 없는 경우 다음이 단계를 수행 하 여 오프 라인 라이선스를 보유 하는 Linux 배포판의 설치 관리자를 다운로드할 수 있습니다. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Azure Active Directory (AD) 계정 설정 

해야 Azure AD 계정이 있고 Microsoft Store 앱의 설치 관리자 다운로드 하려면 조직에 대 한 전역 관리자 여야 합니다. 계정이 이미 있는 경우이 단계를 건너뛸 수 있습니다.

계정을 등록 하는 지침은 여기에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>비즈니스용 스토어에 로그인 하 고 홈 페이지로 이동 합니다.
여기에서에서 로그인: www.microsoft.com/business-store

![MS 스토어 비즈니스 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>관리로 이동-> 설정 하 고 '오프 라인 앱 표시'를 사용 하도록 설정

![MS 스토어 비즈니스 설정 페이지](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>'내 그룹에 대 한 상점'를 클릭 하 여 기본 페이지로 돌아가서

![MS 스토어 비즈니스 홈 페이지](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>원하는 배포에 대 한 검색 하 고 선택

![MS 스토어 활성 검색을 사용 하 여 비즈니스 홈 페이지](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>라이선스 유형 드롭다운 메뉴에서 '오프 라인' 라이선스를 선택 하 고 앱 가져오기'를 클릭 합니다.

![MS 스토어 비즈니스 Ubuntu 제품 페이지](media/offlineinstallscreens/4-screen.png)

참고: 일부 배포판 오프 라인 라이선스를 유지할 필요가 없으며 선택할 수 있습니다

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>앱의 제품 페이지를 표시 하려면 '관리' 단추를 클릭 합니다.

![MS 스토어 비즈니스 Ubuntu 제품 페이지](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>아키텍처를 선택 하 고 오프 라인 패키지를 다운로드 합니다.

![MS 스토어 비즈니스 Ubuntu 제품 정보 페이지](media/offlineinstallscreens/6-screen.png)

이 설치 관리자 WSL 설치 하려는 컴퓨터에 배포할 수 있습니다.