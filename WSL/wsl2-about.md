---
title: WSL 2 정보
description: Linux 용 Windows 하위 시스템에 대 한 새 아키텍처 정보 WSL 2 정보
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9ed24b185ad6aef3589b23a114853b6f78b5899f
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269835"
---
# <a name="about-wsl-2"></a>WSL 2 정보

WSL 2는 Windows에서 ELF64 Linux 이진 파일을 실행하기 위해 Linux 용 Windows 하위 시스템을 지원하는 새 버전의 아키텍처입니다. 주요 목표는 전체 시스템 호출 호환성을 추가하는 것뿐만 아니라 파일 시스템 성능을 높이는 것입니다. 이 새로운 아키텍처는 이러한 Linux 이진 파일이 Windows 및 컴퓨터의 하드웨어와 상호 작용 하는 방식을 변경하지만 WSL 1 (현재 널리 사용 가능한 버전)에서와 동일한 사용자 환경을 제공합니다. 개별 Linux 배포판을 WSL 1 배포판 또는 WSL 2 배포판로 실행 하거나, 언제든지 업그레이드하거나 다운그레이드할 수 있으며, WSL 1과 WSL 2를 함께 실행할 수 있습니다. WSL 2는 실제 Linux 커널을 사용하는 완전히 새로운 아키텍처를 사용합니다.

## <a name="linux-kernel-in-wsl-2"></a>WSL 2의 Linux 커널

WSL 2의 Linux 커널은 kernel.org에서 제공되는 원본을 기반으로 하는 안정적인 최신 분기를 기반으로 합니다. 이 커널은 WSL 2에 대해 특별히 조정되었습니다. Windows에서 놀라운 Linux 환경을 제공하고 Windows 업데이트를 통해 서비스를 제공하는 크기와 성능에 맞게 최적화되었습니다. 즉, 사용자가 직접 관리할 필요 없이 최신 보안 수정과 커널 향상을 얻을 수 있습니다.

또한 이 커널은 오픈 소스가 됩니다. [여기](https://github.com/microsoft/WSL2-Linux-Kernel)에서 Linux 커널의 전체 소스 코드를 찾을 수 있습니다. 이 커널에 대해 자세히 알아보려면 이 블로그 게시물을 작성 한 팀이 작성 한 [이 블로그 게시물](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) 을 체크아웃할 수 있습니다.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 아키텍처에 대한 간략한 개요

WSL 2는 최신의 가상화 기술을 사용하여 경량 유틸리티 VM (가상 머신) 내에서 Linux 커널을 실행합니다. 그러나 WSL 2는 기존 VM 환경이 아닙니다. 기존 VM 환경을 부팅하고, 격리하고, 많은 리소스를 소비하고, 리소스를 관리하는 데 시간이 걸릴 수 있습니다. WSL 2에는 이러한 특성이 없습니다. WSL 1의 뛰어난 이점을 제공합니다. Windows와 Linux 간 높은 수준의 통합, 매우 빠른 부팅 시간, 작은 리소스 공간 및 가장 좋은 방법은 VM 구성 또는 관리가 필요하지 않습니다. WSL 2는 VM을 사용하지만 WSL 1과 동일한 사용자 환경을 유지 하면서 백그라운드에서 관리되고 실행됩니다.

## <a name="increased-file-io-performance"></a>파일 IO 성능 향상

Git clone, npm install, apt update, apt upgrade 등의 파일 집약적 작업은 모두 아주 빠르게 수행됩니다. 실제 속도 증가는 실행 중인 앱과 파일 시스템과 상호 작용 하는 방법에 따라 달라집니다. WSL 2의 초기 버전은 압축된 tarball의 압축을 푸는 경우 WSL 1에 비해 20x 더 빠르게 실행 되 고, git 클론을 사용하는 경우에는 2 ~ 5 배 더 빠르게 실행됩니다.

## <a name="full-system-call-compatibility"></a>전체 시스템 호출 호환성

Linux 이진 파일은 시스템 호출을 사용하여 파일 액세스, 메모리 요청, 프로세스 만들기 등의 여러 기능을 수행합니다. WSL 1은 WSL 팀에서 빌드된 번역 계층을 사용했지만 WSL 2에는 전체 시스템 호출 호환성이 있는 자체 Linux 커널이 포함되어 있습니다. 여기에는 Docker 등의 WSL 내에서 실행할 수 있는 완전히 새로운 앱 집합이 도입되었습니다. 또한 WSL 팀이 변경 내용을 구현하고 추가하기를 기다리는 대신 Linux 커널의 모든 업데이트를 컴퓨터에 즉시 추가할 수 있습니다.
