---
title: WSL 2에 대 한
description: WSL 2 Linux 용 Windows 하위 시스템에 대 한 새로운 아키텍처에 대 한
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038133"
---
WSL 2는 Windows에서 ELF64 Linux 이진 파일을 실행 하도록 Linux 용 Windows 하위 시스템을 구동 하는 아키텍처의 새 버전. 기본 목표는 전체 시스템 호출 호환성을 추가할 뿐 아니라 파일 시스템 성능을 향상 하는 것입니다. 이 새로운 아키텍처 이러한 Linux 바이너리 Windows 컴퓨터의 하드웨어와 상호 작용 하는 방법을 변경 하지만 여전히 WSL 1 (현재 널리 사용 가능한 버전)와 같이 동일한 사용자 환경을 제공 합니다. 개별 Linux 배포판 WSL 1 배포판을 또는 WSL 2 배포판을 실행할 수 있습니다 업그레이드 하거나 언제 든 지 다운 그레이드할 수 있으며 WSL 1-2 WSL 배포판 나란히 실행할 수 있습니다. WSL 2에는 실제 Linux 커널을 사용 하는 완전히 새로운 아키텍처를 사용 합니다.

## <a name="linux-kernel-in-wsl-2"></a>WSL 2에서 Linux 커널

WSL 2에서 Linux 커널에 사내 kernel.org에서 사용할 수 있는 원본을 기반으로 최신 안정적인 분기에서 빌드됩니다. 이 커널은 WSL 2에 대 한 특별 하 게 조정 되었습니다. 크기 및 성능 Windows에서 놀라운 Linux 경험을 제공 하기 위해 최적화 된 하 고 Windows 업데이트를 통해 처리 됩니다 의미를 직접 관리할 필요 하지 않고 최신 보안 픽스 및 향상 된 커널 기능을 얻을 수 있습니다.

또한이 커널은 오픈 소스 됩니다. Linux 커널에 대 한 전체 소스 코드를 찾을 수 있습니다 [여기](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip)합니다. 자세한 하려는 경우 체크 아웃할 수 있습니다이 커널에 대 한 [이 블로그 게시물](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) 빌드한 팀에서 작성 합니다.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 아키텍처의 간략 한 개요

WSL 2를 사용 하 여 최신 및 가상화 기술에 가장 간단한 유틸리티 가상 컴퓨터 (VM) 내에서 해당 Linux 커널을 실행 합니다. 그러나 WSL 2는 기존 VM 환경이 되지 않습니다. 기존의 VM 환경 부팅 속도가 느릴 수 있습니다, 격리 된, 다양 한 리소스를 사용 및 관리 하는 데에 시간이 필요 합니다. WSL 2에는 이러한 특성이 없습니다. 주목할 만한 이점은 WSL 1 계속 받습니다. 높은 수준의 Windows 및 Linux, 매우 빠른 부팅 시간, 작은 리소스 설치 공간이 및 무엇 보다 간의 통합에 없는 VM 구성 또는 관리 해야 합니다. WSL 2에서 VM을 사용 하는 동안 수 관리 하 고 동일한 사용자 환경을 WSL 1로으로 남게 백그라운드에서 실행 합니다.

## <a name="increased-file-io-performance"></a>향상 된 파일의 IO 성능

Git 복제 하는 것과 같은 파일 집약적인 작업, npm 설치, apt 업데이트, apt 업그레이드 등은 모두 빠르게 눈에 띄게 합니다. 실제 속도 증가 실행 되 고 파일 시스템 상호 작용 하는 방법을 하는 앱에 따라 달라 집니다. WSL 2의 초기 버전 실행 최대 20 배 더 빠르게 tarball을 압축된을 풀면와 WSL 1에 비해 다양 한 프로젝트에서 git clone, npm 설치 및 cmake를 사용 하는 경우 더 빠른 2-5 배입니다.

## <a name="full-system-call-compatibility"></a>전체 시스템 호출 호환성

Linux 이진 파일 시스템 호출을 사용 하 여 메모리를 요청, 생성 프로세스 등 파일에 액세스 등 많은 기능을 수행 하 합니다. WSL 1 WSL 팀에서 빌드된 변환 계층을 사용 하는 반면 WSL 2 전체 시스템 호출 호환성을 사용 하 여 Linux 커널 자체를 포함 합니다. 이 Docker 등과 같은 WSL 내에서 실행할 수 있는 앱의 완전히 새로운 집합을 소개 합니다. 또한 Linux 커널에 대 한 업데이트가 즉시 컴퓨터를 추가할 수 있습니다, 그리고 WSL 팀이 변경 내용을 구현 하 고을 대기 하는 대신 추가 합니다.