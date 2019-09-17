---
title: WSL 2 질문과 대답
description: Linux 2 용 Windows 하위 시스템에 대 한 질문과 대답
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: ea6a1e4fc813ec80393a0c4e2beb89e9a40fb68e
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020919"
---
# <a name="wsl-2-faq"></a>WSL 2 FAQ

다음은 Linux 2 용 Windows 하위 시스템에 대 한 FAQ (질문과 대답) 목록입니다.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2는 Hyper-v를 사용 하나요? Windows 10 Home에서 사용할 수 있나요?

WSL 2는 Windows 10 Home을 포함 하 여 WSL을 현재 사용할 수 있는 모든 Sku에서 사용할 수 있습니다.

최신 버전의 WSL은 Hyper-v 아키텍처를 사용 하 여 가상화를 사용 하도록 설정 합니다. 이 아키텍처는 ' 가상 컴퓨터 플랫폼 ' 옵션 구성 요소에서 사용할 수 있습니다. 이 선택적 구성 요소는 모든 Sku에서 사용할 수 있습니다. 이 환경에 대 한 자세한 내용은 WSL 2 릴리스와 함께 제공 될 예정입니다.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1은 어떻게 되나요? 중단 될 예정 인가요?

현재 사용 중단 WSL 1에 대 한 계획은 없습니다. WSL 1과 WSL 2를 나란히 실행 하 고 언제 든 지 배포판를 업그레이드 하 고 다운 그레이드할 수 있습니다. Wsl 2를 새 아키텍처로 추가 하면 wsl 팀이 Windows에서 Linux 환경을 실행 하는 뛰어난 방법을 제공 하는 기능을 제공 하는 데 더 나은 플랫폼이 제공 됩니다.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>WSL 2 및 기타 타사 가상화 도구 (예: VMware 또는 VirtualBox)를 실행할 수 있나요?

Hyper-v를 사용 하는 경우 일부 타사 응용 프로그램은 작동할 수 없습니다. 즉, WSL 2를 사용 하도록 설정한 경우에는 실행할 수 없습니다. 아쉽게도 VirtualBox 6 (2018 년 12 월에 출시 된 VirtualBox 6.0.0는 [이제 Windows 호스트에서 대체 실행 코어로 hyper-v를 지원함][1]) 이전에 VMware 및 버전의 virtualbox를 포함 합니다.

이 문제를 해결 하는 데 도움이 되는 방법을 조사 하 고 있습니다. 예를 들어 타사 가상화 공급자가 Hyper-v와 호환 되는 소프트웨어를 만드는 데 사용할 수 있는 [하이퍼바이저 플랫폼][2] 이라는 api 집합을 노출 합니다. 이를 통해 응용 프로그램은 [Google Android Emulator][3]와 같은 에뮬레이션에 hyper-v 아키텍처를 사용 하 고 현재 hyper-v와 호환 되는 virtualbox 6 이상을 사용할 수 있습니다.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2의 GPU에 액세스할 수 있나요? 하드웨어 지원을 높일 계획이 있나요?

WSL 2의 초기 릴리스에서 하드웨어 액세스 지원은 제한 됩니다. 예를 들어 GPU, 직렬 또는 USBs에 액세스할 수 없습니다. 그러나 백로그에서 더 나은 장치 지원을 추가 하는 것이 좋습니다. 이렇게 하면 이러한 장치와 상호 작용 하려는 개발자에 게 더 많은 사용 사례가 열립니다. 그 동안에는 항상 직렬 포트 및 USB 액세스 권한이 있는 WSL 1을 사용할 수 있습니다. 이 블로그 및 WSL 팀 구성원에 게 문의 하 여 참가자 빌드에 제공 되는 최신 기능에 대 한 정보를 확인 하 고, 상호 작용 하려는 장치에 대 한 피드백을 제공 해 주시기 바랍니다.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2는 네트워킹 응용 프로그램을 사용할 수 있나요?

예, 일반적인 네트워킹 응용 프로그램은 전체 시스템 호출 호환성이 있으므로 더 빠르게 작동 합니다. 그러나 새 아키텍처는 가상화 된 네트워킹 구성 요소를 사용 합니다. 즉, 초기 미리 보기 빌드 WSL 2는 가상 컴퓨터와 유사 하 게 동작 합니다. 예를 들면 다음과 같습니다. WSL 2는 호스트 컴퓨터와 다른 IP 주소를 갖게 됩니다. Microsoft는 wsl 2를 WSL 1과 동일 하 게 만들기 위해 노력 하 고 있으며,이는 네트워킹 사례를 개선 하는 것을 포함 합니다. Localhost를 사용 하 여 Linux 또는 Windows에서 모든 네트워킹 앱에 액세스 하는 것과 같이 최대한 빠르게 향상 된 기능을 추가할 예정입니다. WSL 2의 릴리스를 사용 하는 것 처럼 네트워킹 사례 및 개선 사항에 대 한 자세한 내용을 게시할 예정입니다.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>가상 머신에서 WSL 2를 실행할 수 있나요?

예! 가상 머신에서 중첩 된 가상화를 사용 하도록 설정 했는지 확인 해야 합니다. 관리자 권한으로 PowerShell 창에서 다음 명령을 실행 하 여 부모 Hyper-v 호스트에서이 기능을 사용 하도록 설정할 수 있습니다.

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

'&lt;VMName&gt;'을 가상 머신의 이름으로 바꾸어야 합니다.

## <a name="can-i-use-wslconf-in-wsl-2"></a>WSL 2에서 wsl를 사용할 수 있나요?

WSL 2는 WSL 1에서 사용 하는 것과 동일한 wsl. 파일을 지원 합니다. 즉, WSL 1 배포판에서 설정한 모든 구성 옵션 (예: Windows 드라이브 automounting, interop 사용 또는 사용 안 함, Windows 드라이브가 탑재 되는 디렉터리 변경 등)이 WSL 2 내에서 모두 작동 합니다. [배포판 관리](./wsl-config.md) 페이지에서 wsl의 구성 옵션에 대해 자세히 알아볼 수 있습니다. 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
