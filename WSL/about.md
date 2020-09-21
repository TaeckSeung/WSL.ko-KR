---
title: Linux용 Windows 하위 시스템 정보
description: 다양한 버전 및 이를 사용하는 방법을 포함하여 Linux용 Windows 하위 시스템에 대해 알아봅니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, GNU, Linux
ms.date: 07/21/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 2b79473f620c39084bc9b7a385d4e16e3fe34d77
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818675"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템이란?

Linux용 Windows 하위 시스템을 사용하면 개발자가 기존 가상 머신의 오버헤드 또는 듀얼 부팅 설정 없이 대부분의 명령줄 도구, 유틸리티 및 애플리케이션을 비롯한 GNU/Linux 환경을 수정하지 않고 Windows에서 직접 실행할 수 있습니다.

다음을 수행할 수 있습니다.

* [Microsoft Store](https://aka.ms/wslstore)에서 즐겨찾는 GNU/Linux 배포를 선택합니다.
* `grep`, `sed`, `awk` 또는 다른 ELF-64 이진 파일과 같은 일반적인 명령줄 도구를 실행합니다.
* 다음을 포함하여 Bash 셸 스크립트 및 GNU/Linux 명령줄 애플리케이션을 실행합니다.  
    * 도구: vim, emacs, tmux
    * 언어: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# 및 F#, Rust, Go 등
    * 서비스: SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).
* 자체 GNU/Linux 배포 패키지 관리자를 사용하여 추가 소프트웨어를 설치합니다.
* Unix와 같은 명령줄 셸을 사용하여 Windows 애플리케이션을 호출합니다.
* Windows에서 GNU/Linux 애플리케이션을 호출합니다.

> [!div class="nextstepaction"]
> [WSL 설치](install-win10.md)

<br>

> [!VIDEO https://www.youtube.com/embed/48k317kOxqg]

## <a name="what-is-wsl-2"></a>WSL 2란?

WSL 2는 Linux용 Windows 하위 시스템 아키텍처의 새로운 버전으로, Linux용 Windows 하위 시스템이 Windows에서 ELF64 Linux 이진 파일을 실행할 수 있게 해줍니다. WSL 2의 주 목표는 **파일 시스템 성능을 높이고** **전체 시스템 호출 호환성**을 추가하는 것입니다.

이 새 아키텍처는 이러한 Linux 이진 파일이 Windows 및 컴퓨터의 하드웨어와 상호 작용하는 방식을 변경하되, WSL 1(현재 널리 사용 가능한 버전)과 동일한 사용자 환경을 제공합니다.

개별 Linux 배포는 WSL 1 또는 WSL 2 아키텍처를 사용하여 실행할 수 있습니다. 언제든지 각 배포를 업그레이드하거나 다운그레이드할 수 있으며 WSL 1 및 WSL 2 배포를 함께 실행할 수 있습니다. WSL 2는 실제 Linux 커널을 실행하는 이점을 제공하는 완전히 새로운 아키텍처를 사용합니다.

<br>

> [!VIDEO https://www.youtube.com/embed/MrZolfGm8Zk]

## <a name="next-steps"></a>다음 단계

* [WSL 1 설치 및 WSL 2로 업데이트](./install-win10.md)

* [WSL 2와 WSL 1 비교](./compare-versions.md)

* [새 Linux 배포에 대한 사용자 계정 및 암호 만들기](./user-support.md)

* [질문과 대답 참조](./faq.md)

* [WSL 2에 대한 질문과 대답 읽기](./wsl2-faq.md)

* [문제 해결](./troubleshooting.md)

* [Windows와 Linux 간의 상호 운용성 명령 실행](./interop.md)

* [실행 명령 및 구성 실행](./wsl-config.md)

* [파일 권한 설정](./file-permissions.md)

* [Enterprise용 WSL 설정](./enterprise.md)

* [참조 WSL 명령](./reference.md)

* [사용자 지정 배포 빌드](./build-custom-distro.md)

* [WSL 릴리스 정보 읽기](./release-notes.md)
