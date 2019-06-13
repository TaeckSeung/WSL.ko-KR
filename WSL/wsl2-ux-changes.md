---
title: WSL 1 및 2 WSL UX 차이점
description: WSL 1 및 2 WSL 간의 사용자 환경 변경 내용
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038103"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 및 2 WSL 간의 사용자 환경 변경 내용

이 페이지의 사용자 환경 차이점 WSL 1 및 WSL 2 미리 보기를 초과 합니다. 알아야 할 주요 변경 됩니다.

- Linux 앱 파일 성능 속도 더 빠르게 Linux 루트 파일 시스템에 액세스 하는 파일 배치
- WSL 2 미리 보기의 초기 빌드에 IP 주소를 사용 하 고 localhost를 사용 하지 않는 네트워크 응용 프로그램에 액세스 해야 합니다.

및 다음은 나타날 수 있는 기타 변경의 전체 목록:

- WSL 2 VHD를 사용 하 여 파일을 저장 하 고 확장 해야 해당 최대 크기에 도달 하면
- WSL 2는 이제 메모리의 작은 비율을 사용을 시작할 때
- OS 간 파일 액세스 속도 느려집니다 초기 미리 보기 빌드에서

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux 루트 파일 시스템에서 Linux 파일을 저장 합니다.
Linux를 사용 하 여 자주 액세스 수는 파일을 배치 해야 합니다. Linux 내부의 응용 프로그램 루트 파일 시스템 파일 성능 이점을 누리고 있습니다. 이러한 파일 내 Linux 루트 파일 시스템에 더 빠르게 파일 시스템 액세스 권한이 있어야 합니다. 또한 했습니다 (예: 파일 탐색기 Linux 루트 파일 시스템에 액세스 하려면 Windows 앱! 실행 해 보세요: `explorer.exe /` bash 셸 및 일어나는지 볼)를 활용 하는이 전환 훨씬 수 월 합니다. 

## <a name="accessing-network-applications"></a>네트워크 응용 프로그램에 액세스
WSL 2 미리 보기 빌드의 초기 Linux 배포판에 및 모든 Windows server 호스트 컴퓨터의 IP 주소를 사용 하 여 Linux에서의 IP 주소를 사용 하 여 Windows에서 모든 Linux 서버에 액세스 해야 합니다. 임시 및 문제를 해결 하려면 우선 순위 목록에서 매우 높은 있다는 것입니다.

### <a name="accessing-linux-applications-from-windows"></a>Windows에서 Linux 응용 프로그램에 액세스
WSL 배포판을 서버에 있는 경우에 배포를 구동 하는 가상 컴퓨터의 IP 주소를 찾으려면 해당 IP 주소에 연결 하는 것이 해야 합니다. 다음 단계를 수행할 수 있습니다.

- 명령을 실행 하 여 배포의 IP 주소를 가져옵니다 `ip addr` WSL 배포 및에서 찾아 내부를 `inet` 의 값을 `eth0` 인터페이스.
   - Grep를 사용 하 여 명령의 출력을 필터링 하 여이 작업을 더 쉽게 찾을 수 있습니다 같이: `ip addr | grep eth0`합니다.
- 위에서 찾은 IP를 사용 하 여 Linux 서버에 연결 합니다.

아래 그림은 Edge 브라우저를 사용 하는 nodeJS 서버에 연결 하 여이 예제를 보여줍니다.

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Linux에서 Windows 응용 프로그램에 액세스
Windows 네트워크 응용 프로그램에 액세스할 호스트 컴퓨터의 IP 주소를 사용 해야 합니다. 다음이 단계를 사용 하 여 수행할 수 있습니다.

- 명령을 실행 하 여 호스트 컴퓨터의 IP 주소를 가져옵니다 `cat /etc/resolv.conf` 용어를 다음 IP 주소를 복사 하 고 `nameserver`입니다. 
- 복사 된 IP 주소를 사용 하 여 모든 Windows 서버에 연결 합니다.

아래 그림은 curl을 통해 Windows에서 실행 하는 python 서버에 연결 하 여이 예제를 보여줍니다. 

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>VHD 및 해당 최대 크기에 도달 하면 수행할 작업을 사용 하 여 WSL 2 이해
WSL 2 ext4 파일 시스템을 사용 하는 VHD 내의 모든 Linux 파일을 저장 합니다. 이 VHD는 저장소 요구 사항에 맞게 자동으로 크기가 조정 됩니다. 이 VHD의 초기 최대 크기는 256GB 있습니다. 크기가 256GB를 초과할 수 증가 함에 따라 배포 하는 경우 디스크 공간이 부족 실행 한 것을 알리는 오류가 표시 됩니다. VHD 크기를 확장 하 여이 해결할 수 있습니다. 이렇게 하는 방법에 대 한 지침은 아래와 같습니다.

1. 사용 하 여 모든 WSL 인스턴스 종료는 `wsl --shutdown` 명령
2. 다음 명령을 완료 하 여 WSL 2 VHD를 크기 조정
   - 관리자 권한으로 명령 프롬프트 창을 열고 다음 명령을 실행:
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. WSL 배포를 시작 합니다.
4. 해당 파일 시스템의 크기를 확장할 수 있는 인식 WSL 확인
   - WSL 배포에서 이러한 명령을 실행 합니다.
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 와이 항목의 이름을 복사 합니다. / sdXX (X가 있는 다른 모든 문자를 나타내는)
      - `sudo resize2fs /dev/sdXX`
         - 값을 사용 하 여 앞에서 복사한 및 사용 해야 하는지 확인: `apt install resize2fs`합니다.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2는 시작 시 일부 메모리를 사용 하는
WSL 2에서 사용 하 여 간단한 유틸리티 VM 실제 Linux 커널을 뛰어난 파일 시스템 성능 및 전체 시스템 호출 신호등에서와 마찬가지로 계속 되는 동안 호환성 빠르고 통합 및 WSL 1로 응답을 제공 합니다. VM이이 유틸리티는 작은 메모리 공간이 하 고 시작 시 메모리 지원 가상 주소를 할당 합니다. 총 메모리의 작은 비율을 시작 하도록 구성 됩니다.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>OS 간 파일 속도 느려집니다 초기 미리 보기 빌드에서
Windows 응용 프로그램에서 Linux 파일을 액세스 하거나 Linux 응용 프로그램을 Windows 파일에 액세스할 때 WSL 1에 비해 속도가 파일을 확인할 수 있습니다. WSL 2 아키텍처 변경의 결과 이며 WSL 팀이 적극적으로 하는 것이 환경을 개선할 방법에 대 한 조사 합니다.