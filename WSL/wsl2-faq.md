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
# <a name="wsl-2-faq"></a>WSL 2 FAQ

질문과 대답 (FAQ)는 Windows 하위 시스템에 대 한 Linux 2의 목록은 다음과 같습니다.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2에서 Hyper-v를 사용 하나요? 사용할 수 있으므로 Windows 10 Home에서?

WSL를 Windows 10 Home 비롯 하 여 현재 사용할 수 있는 WSL 2 모든 Sku에서 사용할 수 있습니다.

WSL의 최신 버전의 가상화를 사용 하도록 Hyper-v 아키텍처를 사용 합니다. 이 아키텍처는 Hyper-v 기능 하위 집합에는 선택적 구성 요소에서 사용할 수 있습니다. 이 선택적 구성 요소는 모든 Sku에서 사용할 수 있습니다. WSL 2 출시가 확정 될 때 곧이 환경에 대 한 자세한 내용을 보려면 예상할 수 있습니다.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1은 어떻게 됩니까? 다음을 중단 되 고 있습니까?

현재 계획이 없습니다 WSL 1의 사용을 중단 했습니다. 수 WSL 1-2 WSL 배포판 나란히 실행 하 고 업그레이드를 언제 든 지 모든 배포판을 다운 그레이드 합니다. 새 아키텍처와 WSL 2 추가 WSL 팀 WSL Windows에서 Linux 환경을 실행 하는 훌륭한 방법을 확인 하는 기능을 제공 하는 더 나은 플랫폼을 제공 합니다.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>WSL 2 및 VMware, VirtualBox 등 타사 가상화 도구를 실행 하는 일을 할 수 있나요?

일부 타사 응용 프로그램에는 Hyper-v WSL 2가 설정 된 경우 실행할 수 없습니다 의미는 사용 중인 경우 작동할 수 없습니다. 아쉽게도이 VMware 및 VirtualBox VirtualBox 6 이전 버전 (2018 년 12 월에에서 릴리스된 6.0.0 VirtualBox [대체 (fallback) 실행 핵심 Windows 호스트에서 Hyper-v는 이제] [ 1]!)

이 문제를 해결 하는 방법을 조사 하는 것입니다. 예를 들어, 호출 되는 Api 집합을 노출 [하이퍼바이저 플랫폼] [ 2] 제 virtualization 공급자가 소프트웨어를 Hyper-v와 호환 되도록 하는 데 사용할 수 있는 그러면 같은 해당 에뮬레이션에 대 한 Hyper-v 아키텍처를 사용 하는 응용 프로그램 [Google Android Emulator][3], 6 및 기준이 VirtualBox 이제 Hyper-v와 호환 되며.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2에서 GPU를 액세스할 수 있나요? 하드웨어 지원 향상 계획이 있습니까?

WSL 2 하드웨어 액세스의 초기 릴리스에서 지원 제한 됩니다 (예:): GPU, 직렬 액세스 또는 Usb 할 수는 있습니다. 그러나 더 나은 장치 지원을 추가 백로그, 높은 이러한 장치와 상호 작용할 수 있는 개발자를 위한 더 많은 사용 사례가 열립니다. 그 동안에 직렬 포트와 USB 액세스 WSL 1를 항상 사용할 수 있습니다. 이 블로그 및 WSL 팀원 내부자에 최신 기능에 대 한 최신 Twitter에 주목 하세요. 작성 하 고 상호 작용 하려는 장치에 대 한 의견을 연락 하세요!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 네트워킹 응용 프로그램을 사용할 수 있습니까?

예, 응용 프로그램을 일반적인 네트워킹 더 빠를 수를 전체 시스템 호환성을 호출 했기 때문에 더 잘 작동 합니다. 그러나 새 아키텍처는 가상화 된 네트워킹 구성 요소를 사용합니다. 이 즉, 초기 미리 보기에서 WSL 2를 작성 하는 가상 컴퓨터를 더 비슷하게 작동 합니다 (예:): WSL 2에는 호스트 컴퓨터와 다른 IP 주소를 갖습니다. WSL 1로 뻐 WSL 2 하기 위해 노력할 것입니다 및를 포함 하는 네트워킹 이야기를 개선 합니다. 향상 된 기능을 Linux 또는 localhost를 사용 하 여 Windows에서 모든 네트워킹 앱에 액세스 하는 등, 수 만큼 빠르게 추가할 예정입니다. WSL 2 릴리스를 접근 하는 것으로 네트워킹 스토리 및 향상 된 기능에 대 한 자세한 내용은 드리며 했습니다.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>WSL 2 가상 컴퓨터에서 실행할 수 있습니까?

예! 가상 컴퓨터에 중첩 된 가상화를 사용 하 고 있는지 확인 해야 합니다. 이 관리자 권한으로 PowerShell 창에서 다음 명령을 실행 하 여 Hyper-v에서 활성화할 수 있습니다.

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

바꿔야 '&lt;VMName&gt;' 가상 컴퓨터의 이름입니다.

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/