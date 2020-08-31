---
title: WSL 2 정보
description: Linux용 Windows 하위 시스템의 새 아키텍처인 WSL 2에 대해 알아봅니다. 아키텍처 개요 및 Linux 커널에 대한 정보를 참조하세요.
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: bfb0e14ce53d3022dba06340630cc97a1286a13f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866128"
---
# <a name="about-wsl-2"></a>WSL 2 정보

WSL 2는 새 아키텍처 버전으로, Linux용 Windows 하위 시스템이 Windows에서 ELF64 Linux 이진 파일을 실행할 수 있게 해줍니다. WSL 2의 주 목표는 파일 시스템 성능을 높이고 전체 시스템 호출 호환성을 추가하는 것입니다. 이 새 아키텍처는 이러한 Linux 이진 파일이 Windows 및 컴퓨터의 하드웨어와 상호 작용하는 방식을 변경하되, WSL 1(현재 널리 사용 가능한 버전)과 동일한 사용자 환경을 제공합니다. 개별 Linux 배포판을 WSL 1 배포판 또는 WSL 2 배포판으로 실행할 수 있고, 언제든지 업그레이드하거나 다운그레이드할 수 있으며, WSL 1과 WSL 2 배포판을 함께 실행할 수 있습니다. WSL 2는 실제 Linux 커널을 사용하는 완전히 새로운 아키텍처를 사용합니다.

## <a name="linux-kernel-in-wsl-2"></a>WSL 2의 Linux 커널

WSL 2의 Linux 커널은 kernel.org에서 제공되는 소스를 기반으로 하는 안정적인 최신 분기를 통해 사내에 구축됩니다. 이 커널은 WSL 2용으로 특별히 조정되었습니다. Windows에서 놀라운 Linux 환경을 제공하도록 크기와 성능이 최적화되었으며, Windows 업데이트를 통해 관리되므로 사용자가 직접 관리할 필요 없이 최신 보안 수정과 커널 개선 기능을 받을 수 있습니다.

또한 이 커널은 오픈 소스입니다. Linux 커널의 전체 소스 코드를 [여기](https://github.com/microsoft/WSL2-Linux-Kernel)에서 확인할 수 있습니다. 이 커널에 대한 자세한 내용을 읽어보려면 이 커널을 개발한 팀이 작성한 [이 블로그 게시물](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)을 확인해 보세요.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 아키텍처에 대한 간략한 개요

WSL 2는 가장 유용한 최신 가상화 기술을 사용하여 경량 유틸리티 VM(가상 머신) 내부에서 Linux 커널을 실행합니다. 그러나 WSL 2는 기존 VM 환경과 다릅니다. 기존 VM 환경은 부팅 속도가 느리며, 격리되어 있고, 많은 리소스를 소비하며, 별도로 관리해야 합니다. WSL 2는 이러한 단점이 없습니다. 하지만 WSL 1의 뛰어난 장점을 그대로 제공합니다. Windows와 Linux 간의 긴밀한 통합, 매우 빠른 부팅 시간, 적은 리소스 사용량 등이 장점이며, 최대 장점은 VM 구성 또는 관리가 필요 없다는 점입니다. WSL 2는 VM을 사용하지만 WSL 1과 동일한 사용자 환경을 유지하면서 백그라운드에서 관리되고 실행됩니다.

## <a name="increased-file-io-performance"></a>파일 IO 성능 향상

`git clone`, `npm install`, `apt update`, `apt upgrade` 등의 파일 집약적 작업이 모두 아주 빠르게 수행됩니다. 실제 속도 증가량은 실행 중인 앱과 앱이 파일 시스템과 상호 작용하는 방법에 따라 달라집니다. WSL 2의 초기 버전은 압축된 tarball의 압축을 풀 경우 WSL 1보다 최대 20배 더 빠르게 실행되고, 다양한 프로젝트에서 `git clone`, `npm install` 및 `cmake`를 사용할 경우 약 2~5배 더 빠르게 실행됩니다.

## <a name="full-system-call-compatibility"></a>전체 시스템 호출 호환성

Linux 이진 파일은 시스템 호출을 사용하여 파일 액세스, 메모리 요청, 프로세스 생성 등의 여러 기능을 수행합니다. WSL 1은 WSL 팀에서 개발한 번역 계층을 사용했지만 WSL 2에는 전체 시스템 호출 호환성을 지원하는 자체 Linux 커널이 포함되어 있습니다. 여기에는 WSL 내에서 실행할 수 있는 Docker 등의 완전히 새로운 앱 세트가 도입되었습니다. 또한 WSL 팀이 변경 내용을 구현하고 추가하기를 기다리는 대신 Linux 커널에 대한 모든 업데이트를 컴퓨터에 즉시 추가할 수 있습니다.
