---
title: 엔터프라이즈에 대한 Linux용 Windows 하위 시스템
description: 엔터프라이즈 환경에서 Linux용 Windows 하위 시스템을 가장 효율적으로 사용하는 방법에 대한 리소스 및 지침입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 엔터프라이즈, 배포, 오프라인, 패키징, 저장소, 배포, 설치, 설치
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ac0025257ae70547c5b20d89535510a8b8bb006c
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413104"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>회사를 위한 Linux용 Windows 하위 시스템 설정

비즈니스용 Microsoft Store는 WSL을 회사에 배포하려는 엔터프라이즈 환경에 다양한 솔루션을 제공합니다. [비즈니스 및 교육용 Microsoft Store 문서](/microsoft-store/)는 Store 환경에 대한 일반 정보를 확인하는 데 유용한 리소스입니다.

WSL 배포를 시작하도록 설정하려는 회사인 경우 다음 단계를 따릅니다.

* [비즈니스용 Microsoft Store에 가입하고 시작합니다](/microsoft-store/sign-up-microsoft-store-for-business-overview).
* [제품 및 서비스를 관리합니다(프라이빗 스토어에 있는 앱에 액세스할 수 있는 사용자 포함)](/microsoft-store/manage-apps-microsoft-store-for-business-overview). 여기서는 WSL 배포를 저장소에 추가하고, 설치할 수 있는 사용자를 제어할 수 있습니다.
* [선택한 배포 방법을 사용하여 소프트웨어를 회사에 배포합니다.](/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 다음 설명서 링크를 사용하여 WSL을 설치할 수 있다고 회사 직원에게 알려줍니다. [Linux용 Windows 하위 시스템 설치](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Windows 오프라인에서 Linux 배포를 배포하는 방법

회사의 컴퓨터에서 Microsoft Store 또는 비즈니스용 Microsoft Store에 액세스할 수 없는 경우 다음 단계에 따라 오프라인 라이선스가 있는 Linux 배포의 설치 관리자를 다운로드할 수 있습니다.

### <a name="set-up-an-azure-active-directory-account"></a>Azure Active Directory 계정 설정

Microsoft Store 앱의 설치 관리자를 얻으려면 [Azure AD 계정에 가입](/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner)해야 하고 조직의 글로벌 관리자여야 합니다. 계정이 이미 있는 경우 이 단계를 건너뛸 수 있습니다.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>비즈니스용 Microsoft Store 계정을 사용하여 WSL 설정

계정을 등록하는 방법에 대한 지침은 https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business 에서 찾을 수 있습니다.

1. 비즈니스용 Microsoft Store(https://www.microsoft.com/business-store )에 로그인하여 홈 페이지로 이동합니다.

    ![비즈니스용 MS Store 홈 페이지](media/offlineinstallscreens/1-screen.png)

2. 관리 > 설정으로 차례로 이동하여 '오프라인 앱 표시'를 사용하도록 설정합니다.

    ![비즈니스용 MS Store 설정 페이지](media/offlineinstallscreens/2-screen.png)

3. '내 그룹 쇼핑'을 선택하여 기본 페이지로 돌아갑니다.

    ![비즈니스용 MS Store 홈 페이지](media/offlineinstallscreens/1-screen.png)

4. 원하는 배포를 검색하여 선택합니다.

    ![활성 검색이 있는 비즈니스용 MS Store 홈 페이지](media/offlineinstallscreens/3-screen.png)

5. 라이선스 유형 드롭다운 메뉴에서 '오프라인' 라이선스를 선택하고, '앱 가져오기'를 선택합니다. (일부 Linux 배포에서는 오프라인 라이선스를 제공하지 않도록 선택할 수 있습니다.)

    ![비즈니스용 MS Store Ubuntu 선택 오프라인](media/offlineinstallscreens/4-screen.png)

6. '관리' 단추를 선택하여 앱의 제품 페이지로 이동합니다.

    ![비즈니스용 MS Store Ubuntu 선택 관리](media/offlineinstallscreens/5-screen.png)

7. 아키텍처를 선택하고, 오프라인에서 사용할 패키지를 다운로드합니다.

    ![비즈니스용 MS Store Ubuntu 선택 아키텍처](media/offlineinstallscreens/6-screen.png)

그러면 WSL을 설치하려는 모든 컴퓨터에 이 설치 관리자를 배포할 수 있습니다.
