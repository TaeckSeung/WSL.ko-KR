---
title: WSL 1과 WSL 2 간의 UX 변경 내용
description: WSL 1과 WSL 2 사이의 사용자 환경 변경
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3addfd27d777731bf92efab42c6bcd4be415779b
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020968"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1과 WSL 2 사이의 사용자 환경 변경

이 페이지에서는 WSL 1과 WSL 2 preview의 사용자 환경 차이를 모두 제공 합니다. 유의 해야 하는 주요 변경 내용은 다음과 같습니다.

- 더 빠른 파일 성능 속도를 위해 linux 앱이 Linux 루트 파일 시스템에서 액세스할 파일을 저장 합니다.
- WSL 2 preview의 초기 빌드에서는 localhost를 사용 하는 대신 IP 주소를 사용 하 여 네트워크 응용 프로그램에 액세스 해야 합니다.

다음은 볼 수 있는 다른 변경 내용에 대 한 전체 목록입니다.

- WSL 2는 VHD ( [가상 하드웨어 디스크](https://en.wikipedia.org/wiki/VHD_(file_format)) )를 사용 하 여 파일을 저장 하 고 최대 크기에 도달 하면 확장 해야 할 수 있습니다.
- 시작할 때 WSL 2는 이제 작은 메모리 비율을 사용 합니다.
- 초기 미리 보기 빌드에서 OS 간 파일 액세스 속도가 느려집니다.

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux 루트 파일 시스템에 Linux 파일 저장
파일 성능 혜택을 누릴 수 있도록 Linux 루트 파일 시스템 내부의 Linux 응용 프로그램에 자주 액세스 하는 파일을 배치 해야 합니다. 이러한 파일은 더 빠른 파일 시스템 액세스를 위해 Linux 루트 파일 시스템 내에 있어야 합니다. Windows 앱이 Linux 루트 파일 시스템에 액세스할 수도 있습니다 (예: 파일 탐색기). 실행 시도: `explorer.exe .` Linux 배포판의 홈 디렉터리에서 수행 하는 작업을 확인 하 고이를 훨씬 쉽게 전환할 수 있습니다. 

## <a name="accessing-network-applications"></a>네트워크 응용 프로그램 액세스
WSL 2 preview의 초기 빌드에서 Linux 배포판의 IP 주소와 호스트 컴퓨터의 IP 주소를 사용 하는 Linux의 모든 Windows server를 사용 하 여 Windows에서 Linux 서버에 액세스 해야 합니다. 이는 일시적 이며 수정할 우선 순위 목록에 매우 높습니다.

### <a name="accessing-linux-applications-from-windows"></a>Windows에서 Linux 응용 프로그램 액세스
WSL 배포판 서버를 사용 하는 경우 배포판를 켜는 가상 머신의 IP 주소를 찾아 해당 IP 주소를 사용 하 여 연결 해야 합니다. 이렇게 하려면 다음 단계를 수행 합니다.

- Wsl 배포판 내에서 명령을 `ip addr` 실행 하 고 `eth0` 인터페이스의 `inet` 값에서 찾아 배포판의 IP 주소를 가져옵니다.
   - 다음과 `ip addr | grep eth0`같이 grep를 사용 하 여 명령의 출력을 필터링 하 여이를 보다 쉽게 찾을 수 있습니다.
- 위에서 찾은 IP를 사용 하 여 Linux 서버에 연결 합니다.

아래 그림에서는 Edge 브라우저를 사용 하 여 node.js 서버에 연결 하는 방법의 예를 보여 줍니다.

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Linux에서 Windows 응용 프로그램 액세스
Windows 네트워크 응용 프로그램에 액세스 하려면 호스트 컴퓨터의 IP 주소를 사용 해야 합니다. 이렇게 하려면 다음 단계를 수행 합니다.

- 명령을 `cat /etc/resolv.conf` 실행 하 고 약관 `nameserver`에 따라 ip 주소를 복사 하 여 호스트 컴퓨터의 ip 주소를 가져옵니다. 
- 복사한 IP 주소를 사용 하 여 Windows 서버에 연결 합니다.

아래 그림은 Windows에서 실행 되는 Windows에서 실행 되는 node.js 서버에 연결 하 여이에 대 한 예를 보여 줍니다. 

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a>기타 네트워킹 고려 사항

원격 IP 주소를 사용 하 여 응용 프로그램에 연결 하는 경우 LAN (Local Area Network)의 연결로 처리 됩니다. 즉, 응용 프로그램에서 LAN 연결을 허용할 수 있는지 확인 해야 합니다. 예를 들면 다음과 같습니다. 대신 응용 프로그램을에 `0.0.0.0` 바인딩해야 할 수도 있습니다. `127.0.0.1` 예를 들어 flask를 사용 하는 python에서는 명령을 `app.run(host='0.0.0.0')`사용 하 여이 작업을 수행할 수 있습니다. 이러한 변경을 수행 하는 경우 LAN 으로부터의 연결을 허용 하므로 보안을 염두에 두십시오. 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>WSL 2는 VHD를 사용 하 고 최대 크기에 도달 하는 경우 수행할 작업을 이해 합니다.
WSL 2는 ext4 파일 시스템을 사용 하는 VHD 내에 모든 Linux 파일을 저장 합니다. 이 VHD는 저장소 요구에 맞게 자동으로 크기가 조정 됩니다. 또한이 VHD의 초기 최대 크기는 256GB입니다. 배포판 크기가 256GB 보다 큰 경우 디스크 공간이 부족 하다는 오류가 표시 됩니다. VHD 크기를 확장 하 여 이러한 문제를 해결할 수 있습니다. 이 작업을 수행 하는 방법에 대 한 지침은 다음과 같습니다.

1. `wsl --shutdown` 명령을 사용 하 여 모든 wsl 인스턴스를 종료 합니다.
2. 배포판 설치 패키지 이름 ' PackageFamilyName ' 찾기
   - Powershell 프롬프트에서 (' 배포판 '이 (가) 배포 이름인 경우)를 입력 합니다.
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. WSL 2 설치에서 사용 되는 VHD 파일 fullpath를 찾습니다 .이 파일은 ' pathToVHD '입니다.
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 다음 명령을 완료 하 여 WSL 2 VHD 크기를 조정 합니다.
   - 관리자 권한으로 명령 프롬프트 창을 열고 다음 명령을 실행 합니다.
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. WSL 배포판 시작
6. WSL에서 파일 시스템의 크기를 확장할 수 있음을 인식 하도록 설정
   - WSL 배포판에서 다음 명령을 실행 합니다.
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 이 항목의 이름을 복사 합니다. 예를 들어/Hv/sdxx (X는 다른 문자를 나타냄)와 같습니다.
      - `sudo resize2fs /dev/sdXX`
         - 앞에서 복사한 값을 사용 하 고를 사용 `apt install resize2fs`해야 할 수도 있습니다.

참고: 일반적으로 Windows 도구 또는 편집기를 사용 하 여 AppData 폴더 내에 있는 WSL 관련 파일을 수정 하거나 이동 하거나 액세스 하지 않습니다. 이렇게 하면 Linux 배포판 손상 될 수 있습니다.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2는 시작 시 일부 메모리를 사용 합니다.
WSL 2는 실제 Linux 커널의 경량 유틸리티 VM을 사용 하 여 뛰어난 파일 시스템 성능 및 전체 시스템 호출 호환성을 제공 하는 동시에 WSL 1로 신속 하 고 신속 하 게 통합 되 고 응답성을 제공 합니다. 이 유틸리티 VM에는 작은 메모리 공간이 있으며 시작 시 가상 주소 지원 메모리를 할당 합니다. 총 메모리의 작은 부분으로 시작 되도록 구성 됩니다.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>초기 미리 보기 빌드에서 OS 파일 속도가 느립니다.
Linux 응용 프로그램에서 Windows 파일에 액세스 하거나 Windows 응용 프로그램에서 Linux 파일에 액세스 하는 경우 WSL 1과 비교 하 여 파일 속도가 느려지는 것을 알 수 있습니다. 이는 WSL 2의 아키텍처 변경의 결과 이며, WSL 팀이이 환경을 개선할 수 있는 방법에 대해 적극적으로 조사 하 고 있습니다.
