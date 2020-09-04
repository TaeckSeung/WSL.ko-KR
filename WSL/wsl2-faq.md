---
title: WSL 2 관련 질문과 대답
description: 'Linux용 Windows 하위 시스템 2에 대한 FAQ(예: 가상 머신에서 WSL 2를 실행할 수 있나요?)의 답변을 찾아보세요.'
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: a021dc3c6c3c2a14fea631f2733d2b846c6fe3ad
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058488"
---
# <a name="wsl-2-faqs"></a>WSL 2 FAQ

다음은 Linux용 Windows 하위 시스템 2에 대한 FAQ(질문과 대답) 목록입니다.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2가 Hyper-V를 사용하나요? Windows 10 Home에 제공될 예정인가요?

WSL 2는 Windows 10 Home을 포함하여 WSL이 현재 제공되는 모든 SKU에서 사용할 수 있습니다.

최신 버전의 WSL은 Hyper-V 아키텍처를 사용하여 가상화를 지원합니다. 이 아키텍처는 'Virtual Machine 플랫폼' 옵션 구성 요소에서 사용할 수 있습니다. 이 옵션 구성 요소는 모든 SKU에서 사용할 수 있습니다. 이 환경에 대한 자세한 내용은 WSL 2 릴리스를 앞두고 제공될 예정입니다.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1은 어떻게 되나요? 중단되나요?

현재 WSL 1을 사용 중단할 계획은 없습니다. WSL 1과 WSL 2 배포판을 함께 실행하고 원하는 배포판을 언제든지 업그레이드하고 다운그레이드할 수 있습니다. WSL 2를 새 아키텍처로 추가하면 WSL 팀이 더 나은 플랫폼을 통해 Windows에서 Linux 환경을 원활하게 실행하는 데 필요한 기능을 제공할 수 있습니다.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>WSL 2 및 기타 타사 가상화 도구(예: VMware 또는 VirtualBox)를 실행할 수 있나요?

Hyper-V를 사용 중인 경우 일부 타사 애플리케이션을 작동할 수 없습니다. 즉, VMware 및 VirtualBox와 같이 WSL 2를 사용하도록 설정된 경우에는 일부 타사 애플리케이션이 실행되지 않습니다. 그러나 최근 VirtualBox와 VMware는 모두 Hyper-V와 WSL2를 지원하는 버전을 릴리스했습니다! [VirtualBox의 변경 내용은 여기][1] 그리고 [VMware의 변경 내용은 여기][4]에서 자세히 알아볼 수 있습니다.

저희는 타사의 Hyper-V 통합을 지원하기 위해 지속적으로 솔루션을 개발하고 있습니다. 예를 들어 타사 가상화 공급자가 Hyper-V와 호환되는 소프트웨어를 만드는 데 사용할 수 있는 [하이퍼바이저 플랫폼][2]이라는 API 세트를 제공합니다. 이를 통해 애플리케이션은 현재 Hyper-V와 호환되는 VirtualBox 6 이상 버전과 [Google Android Emulator][3] 같은 에뮬레이션에 Hyper-V 아키텍처를 사용할 수 있습니다.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2의 GPU에 액세스할 수 있나요? 하드웨어 지원을 늘릴 계획이 있나요?

WSL 2 배포판 내부의 GPU 액세스 지원을 릴리스했습니다. 즉, 이제 빅 데이터 세트가 관련될 때 기계 학습, AI 및 데이터 과학 시나리오에 대해 WSL을 더 쉽게 사용할 수 있습니다. [여기에서 GPU 지원을 시작하기 위한](./tutorials/gpu-compute) 자습서를 찾을 수 있습니다. 현재 WSL 2에는 직렬 지원 또는 USB 디바이스 지원이 포함되어 있지 않습니다. 이러한 기능을 추가하는 가장 좋은 방법을 찾고 있습니다.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2가 네트워킹 애플리케이션을 사용할 수 있나요?

예, 전체 시스템 호출 호환성이 지원되므로 일반적으로 네트워킹 애플리케이션이 더 빠르게, 더 효율적으로 작동합니다. 그러나 새 아키텍처는 가상화된 네트워킹 구성 요소를 사용합니다. 따라서 WSL 2의 초기 미리 보기 빌드는 가상 머신과 유사하게 동작합니다. 예를 들면 다음과 같습니다. WSL 2는 호스트 머신과 다른 IP 주소를 갖게 됩니다. Microsoft는 WSL 2를 WSL 1과 동일한 느낌으로 만들기 위해 노력하고 있으며, 이를 위해 네트워킹 사례를 개선하고 있습니다. 

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>가상 머신에서 WSL 2를 실행할 수 있나요?

예! 가상 머신에 중첩된 가상화가 사용 설정되었는지 확인해야 합니다. PowerShell 창에서 관리자 권한으로 다음 명령을 실행하면 부모 Hyper-V 호스트에서 이를 사용하도록 설정할 수 있습니다.

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

'&lt;VMName&gt;'을 가상 머신 이름으로 바꾸세요.

## <a name="can-i-use-wslconf-in-wsl-2"></a>WSL 2에서 wsl.conf를 사용할 수 있나요?

WSL 2는 WSL 1에서 사용하는 것과 동일한 wsl. 파일을 지원합니다. 즉, WSL 1 배포판에서 설정한 모든 구성 옵션(예: Windows 드라이브 자동 탑재, interop 사용 또는 사용 안 함, Windows 드라이브가 탑재될 디렉터리 변경 등)이 모두 WSL 2 내에서 작동합니다. [배포판 관리](./wsl-config.md) 페이지에서 WSL의 구성 옵션에 대해 자세히 알아볼 수 있습니다.

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html
