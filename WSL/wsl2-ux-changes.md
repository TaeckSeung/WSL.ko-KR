---
title: WSL 1과 WSL 2 간의 UX 변경 내용
description: WSL 1과 WSL 2 간의 사용자 환경 변경 내용
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windows 하위 시스템, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256336"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1과 WSL 2 간의 사용자 환경 변경 내용

이 페이지에서는 WSL 1과 WSL 2 미리 보기의 사용자 환경이 어떻게 다른지 설명합니다. 주요 변경 내용은 다음과 같습니다.

- 파일 성능 속도 개선을 위해 Linux 앱이 액세스할 파일을 Linux 루트 파일 시스템에 배치합니다.
- WSL 2 미리 보기의 초기 빌드에서는 localhost를 사용하는 대신 IP 주소를 사용하여 네트워크 애플리케이션에 액세스해야 합니다.

다음은 다른 변경 내용의 전체 목록입니다.

- WSL 2는 VHD([가상 하드웨어 디스크](https://en.wikipedia.org/wiki/VHD_(file_format)))를 사용하여 파일을 저장합니다. 저장 용량이 최대 크기에 도달하면 VHD를 직접 확장해야 할 수 있습니다.
- WSL 2는 이제 시작할 때 소량의 메모리를 사용합니다.
- 초기 미리 보기 빌드에서는 OS 간 파일 액세스 속도가 느려짐

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux 루트 파일 시스템에 Linux 파일 배치
파일 성능 이점을 누리려면 Linux 애플리케이션을 사용하여 자주 액세스할 파일을 Linux 루트 파일 시스템 내부에 배치해야 합니다. 이러한 파일이 Linux 루트 파일 시스템 내부에 있어야 더 빠른 파일 시스템 액세스가 가능합니다. Windows 앱(예: 파일 탐색기)이 Linux 루트 파일 시스템에 액세스할 수도 있습니다. Linux 배포판의 홈 디렉터리에서 `explorer.exe .`를 실행하고 어떻게 되는지 확인하면 훨씬 더 쉽게 전환할 수 있습니다. 

## <a name="accessing-network-applications"></a>네트워크 애플리케이션 액세스
WSL 2 미리 보기의 초기 빌드에서는 호스트 머신의 IP 주소를 사용하여 Linux에서 Windows Server에 액세스해야 합니다.

### <a name="accessing-windows-applications-from-linux"></a>Linux에서 Windows 애플리케이션에 액세스
Windows 네트워크 애플리케이션에 액세스하려면 호스트 머신의 IP 주소를 사용해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

- `cat /etc/resolv.conf` 명령을 실행하고 `nameserver` 뒤에 있는 IP 주소를 복사하여 호스트 머신의 IP 주소를 가져옵니다. 
- 복사한 IP 주소를 사용하여 Windows Server에 연결합니다.

아래 그림은 curl을 통해 Windows에서 실행 중인 Node.js 서버에 연결하여 이에 대한 예를 보여줍니다. 

![Windows에서 Linux 네트워크 애플리케이션에 액세스](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Windows에서 Linux 애플리케이션에 액세스

사용 중인 Windows 버전에 따라 가상 머신의 IP 주소를 검색해야 할 수 있습니다. 빌드가 18945 이상인 경우 평상시처럼 `localhost`를 사용하면 됩니다. 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>[18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) 미만의 빌드에서 Linux에 액세스

WSL 배포판에 서버가 있는 경우 배포판이 실행 중인 가상 머신의 IP 주소를 찾고 해당 IP 주소를 사용하여 서버에 연결해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

- WSL 배포판 내에서 `ip addr` 명령을 실행하고 `eth0` 인터페이스의 `inet` 값 아래에 있는 배포판의 IP 주소를 가져옵니다.
   - `ip addr | grep eth0`처럼 grep를 사용하여 명령의 출력을 필터링하면 보다 쉽게 찾을 수 있습니다.
- 위에서 찾은 IP를 사용하여 Linux 서버에 연결합니다.

아래 그림은 Edge 브라우저를 통해 Node.js 서버에 연결하여 이에 대한 예를 보여줍니다.

![Windows에서 Linux 네트워크 애플리케이션에 액세스](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>기타 네트워킹 고려 사항

#### <a name="connecting-via-remote-ip-addresses"></a>원격 IP 주소를 통해 연결

원격 IP 주소를 사용하여 애플리케이션에 연결하는 경우 LAN(Local Area Network)에서 들어오는 연결로 취급됩니다. 따라서 애플리케이션에서 LAN 연결을 허용할 수 있는지 확인해야 합니다. 예를 들면 다음과 같습니다. 애플리케이션을 `127.0.0.1` 대신 `0.0.0.0`에 바인딩해야 할 수 있습니다. 예를 들어 flask를 사용하는 python에서는 `app.run(host='0.0.0.0')` 명령을 사용하여 이 작업을 수행할 수 있습니다. 이러한 변경을 수행하면 LAN에서 들어오는 연결이 허용되므로 보안에 유의하세요. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>LAN(Local Area Network)에서 WSL2 배포판에 액세스

WSL1 배포판을 사용할 때 LAN에서 들어오는 액세스를 허용하도록 컴퓨터를 설정한 경우 WSL에서 실행되는 애플리케이션을 LAN에서도 액세스할 수 있습니다. WSL2에는 자체 IP 주소가 있는 가상화된 이더넷 어댑터가 있기 때문에 이는 WSL2의 기본 사례가 아닙니다. 현재 이 워크플로를 사용하도록 설정하려면 일반 가상 머신과 동일한 단계를 진행해야 합니다. 이러한 환경을 개선하는 방법은 연구 중입니다.

#### <a name="ipv6-access"></a>IPv6 액세스

WSL2 배포판은 현재 IPv6 전용 주소에 연결할 수 없습니다. 이 기능을 추가하기 위한 작업이 진행 중입니다.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>WSL 2가 VHD를 사용하는 방식과 최대 크기에 도달할 경우 취해야 할 조치 이해
WSL 2는 ext4 파일 시스템을 사용하는 VHD 내부에 모든 Linux 파일을 저장합니다. 이 VHD는 스토리지 요구 사항에 맞게 자동으로 크기가 조정됩니다. 또한 이 VHD의 초기 최대 크기는 256GB입니다. 배포판 크기가 256GB보다 커지면 디스크 공간이 부족하다는 오류가 표시됩니다. VHD 크기를 확장하면 이러한 문제를 해결할 수 있습니다. 이 작업을 수행하는 방법에 대한 지침은 다음과 같습니다.

1. `wsl --shutdown` 명령을 사용하여 모든 WSL 인스턴스 종료
2. 배포판 설치 패키지 이름 'PackageFamilyName' 찾기
   - PowerShell 프롬프트에서 다음과 같이 입력(배포판 이름이 'distro'인 경우)
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. WSL 2 설치에 사용되는 VHD 파일의 전체 경로('pathToVHD') 찾기
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 다음 명령을 완료하여 WSL 2 VHD 크기 조정
   - 관리자 권한으로 명령 프롬프트 창을 열고 다음 명령 실행:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. WSL 배포판 시작
6. WSL에서 파일 시스템의 크기를 확장할 수 있음을 인식하도록 설정
   - WSL 배포판에서 다음 명령 실행:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - /dev/sdXX 같은 이 항목의 이름 복사(여기서 X는 다른 문자를 나타냄)
      - `sudo resize2fs /dev/sdXX`
         - 앞에서 복사한 값을 사용해야 하며 `apt install resize2fs`를 사용해야 할 수 있습니다.

참고: 일반적으로 Windows 도구 또는 편집기를 사용하여 AppData 폴더 내에 있는 WSL 관련 파일을 수정하거나 이동하거나 액세스해서는 안 됩니다. 그러면 Linux 배포판이 손상될 수 있습니다.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2는 시작 시 일부 메모리를 사용함
WSL 2는 실제 Linux 커널의 경량 유틸리티 VM을 사용하여 뛰어난 파일 시스템 성능 및 전체 시스템 호출 호환성을 제공하는 한편, WSL 1처럼 빠르고 가볍게 통합되고 반응합니다. 이 유틸리티 VM은 약간의 메모리 공간을 차지하며 시작 시 가상 주소 지원 메모리를 할당합니다. 총 메모리 중 소량의 메모리로 시작하도록 구성됩니다.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>초기 미리 보기 빌드에서는 OS 간 파일 속도가 느려짐
Linux 애플리케이션에서 Windows 파일에 액세스하거나 Windows 애플리케이션에서 Linux 파일에 액세스하는 경우 WSL 1보다 속도가 느리다는 것을 알 수 있습니다. 이는 WSL 2의 아키텍처가 변경되었기 때문이며, WSL 팀이 이 환경을 개선할 방법을 적극적으로 모색 중입니다.
