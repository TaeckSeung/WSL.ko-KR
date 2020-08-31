---
title: WSL 2와 WSL 1 비교
description: Linux용 Windows 하위 시스템의 버전 1과 버전 2를 비교합니다. WSL 2는 실제 Linux 커널을 실행하여 속도와 전체 시스템 호출 호환성을 높입니다. WSL 1은 Windows 및 Linux 파일 시스템 모두에서 작업하는 경우 더욱 효과적으로 작동합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, GNU, Linux, Ubuntu, Debian, Suse, Windows 10, UX 변경 내용, WSL 2, Linux 커널, 네트워크 애플리케이션, localhost, IPv6, 가상 하드웨어 디스크, VHD, VHD 제한, VHD 오류
ms.date: 07/22/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 15f1528332345f0bea829b9606372ed7346e6dff
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866021"
---
# <a name="comparing-wsl-1-and-wsl-2"></a>WSL 1과 WSL 2 비교

Linux용 Windows 하위 시스템을 새 버전으로 업데이트하는 기본 목표는 **파일 시스템 성능을 향상**시키고 **전체 시스템 호출 호환성**을 지원하는 것입니다. 

WSL 2는 가장 유용한 최신 가상화 기술을 사용하여 간단한 유틸리티 VM(가상 머신) 내에서 Linux 커널을 실행합니다. 그러나 WSL 2는 기존 VM 환경이 아닙니다. [WSL 2 아키텍처에 대해 자세히 알아보세요](#wsl-2-architecture).

## <a name="comparing-features"></a>기능 비교

기능 | WSL 1 | WSL 2
--- | --- | ---
 Windows와 Linux 통합| ✅|✅
 빠른 부팅 시간| ✅ | ✅
 작은 리소스 공간| ✅ |✅
 현재 버전의 VMWare 및 VirtualBox로 실행| ✅ | ✅
 관리 VM| ❌ | ✅
 전체 Linux 커널| ❌ |✅
 전체 시스템 호출 호환성| ❌ | ✅
 OS 파일 시스템 간 성능| ✅ | ❌

WSL 1을 이미 사용하고 있으며 WSL 2로 업그레이드하려고 하나요? 그러면 지침에 따라 [WSL 2로 업데이트](./install-win10.md#update-to-wsl-2)하세요!

WSL 2는 Windows 10, 버전 2004, 빌드 19041 이상에서만 사용할 수 있습니다. **Windows 로고 키 + R**을 선택하고 **winver**를 입력한 다음, **확인**을 선택하여 Windows 버전을 확인합니다. (또는 Windows 명령 프롬프트에서 `ver` 명령을 입력합니다.) [최신 Windows 버전을 업데이트](ms-settings:windowsupdate)해야 할 수도 있습니다. 19041보다 낮은 빌드의 경우 WSL은 전혀 지원되지 않습니다.

> [!NOTE]
> WSL 2는 [VMWare 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) 및 [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0)와 함께 작동합니다.

## <a name="use-the-linux-file-system-for-faster-performance"></a>더 빠른 성능을 위해 Linux 파일 시스템 사용

가장 빠른 성능 속도에 맞게 최적화하려면 프로젝트 파일을 Windows 파일 시스템이 아닌 Linux 파일 시스템에 저장해야 합니다.

예를 들어 WSL 프로젝트 파일을 저장하는 경우 다음과 같습니다.

* Linux 파일 시스템 루트 디렉터리(`\\wsl$\Ubuntu-18.04\home\<user name>\Project`)를 사용합니다.
* Windows 파일 시스템 루트 디렉터리(`C:\Users\<user name>\Project`)가 아닙니다.

더 빠른 파일 시스템 액세스를 활용하려면 WSL 배포(예: Ubuntu)를 사용하여 작업하는 프로젝트 파일이 Linux 루트 파일 시스템에 있어야 합니다.

Windows 앱 및 도구(예: 파일 탐색기)를 사용하여 Linux 루트 파일 시스템에 액세스할 수 있습니다. Linux 배포(예: Ubuntu)를 열어 보고, `cd ~` 명령을 입력하여 Linux 홈 디렉터리에 있는지 확인합니다. 그런 다음, `explorer.exe .` *(끝에 있는 마침표를 잊지 마세요)* 를 입력하여 파일 탐색기에서 Linux 파일 시스템을 엽니다.

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a>WSL 2가 아닌 WSL 1의 사용에 대한 예외

더 빠른 성능과 100% 시스템 호출 호환성을 제공하는 WSL 2를 사용하는 것이 좋습니다. 그러나 WSL 1을 사용하는 것이 더 나을 수 있는 몇 가지 특정 시나리오가 있습니다. 다음과 같은 경우 WSL 1을 사용하는 것이 좋습니다.

* 프로젝트 파일을 Windows 파일 시스템에 저장해야 합니다.
  * WSL Linux 배포를 사용하여 Windows 파일 시스템의 프로젝트 파일에 액세스하고 이러한 파일을 Linux 파일 시스템에 저장할 수 없는 경우 WSL 1을 사용하여 OS 파일 시스템에서 더 빠른 성능을 얻을 수 있습니다.
* Windows 및 Linux 도구를 모두 동일한 파일에 사용하여 크로스 컴파일해야 하는 프로젝트입니다.
  * Windows 및 Linux 운영 체제 전체의 파일 성능은 WSL 2보다 WSL 1에서 더 빠르므로 Windows 애플리케이션을 사용하여 Linux 파일에 액세스하는 경우 현재 WSL 1에서 더 빠른 성능을 얻을 수 있습니다.

> [!NOTE]
> VS Code [원격 WSL 확장](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)에서 Linux 명령줄 도구를 사용하여 프로젝트 파일을 Linux 파일 시스템에 저장하도록 시도하는 것을 고려할 수 있지만, Linux 및 Windows 간의 작업과 관련된 성능을 저하시키지 않고 Windows에서 VS Code를 사용하여 인터넷 브라우저에서 프로젝트를 작성, 편집, 디버그 또는 실행할 수도 있습니다. [자세한 정보를 알아보세요](https://code.visualstudio.com/docs/remote/wsl).

## <a name="wsl-2-architecture"></a>WSL 2 아키텍처

기존 VM 환경은 부팅 속도가 느리며, 격리되어 있고, 많은 리소스를 소비하며, 별도로 관리해야 합니다. WSL 2는 이러한 단점이 없습니다.

WSL 2는 Windows와 Linux 간의 원활한 통합, 빠른 부팅 시간, 작은 리소스 설치 공간을 포함하여 WSL 1의 이점을 제공하며 VM을 구성하거나 관리할 필요가 없습니다. WSL 2는 VM을 사용하지만 WSL 1과 동일한 사용자 환경을 유지하면서 백그라운드에서 관리되고 실행됩니다.

### <a name="full-linux-kernel"></a>전체 Linux 커널

WSL 2의 Linux 커널은 kernel.org에서 제공되는 원본을 기반으로 하여 Microsoft를 통해 안정적인 최신 분기에서 구축되었습니다. 이 커널은 WSL 2에 맞게 특별히 튜닝되어 크기와 성능을 최적화하여 Windows에서 놀라운 Linux 환경을 제공합니다. 커널은 Windows 업데이트를 통해 서비스를 제공하므로 직접 관리할 필요 없이 최신 보안 수정과 향상된 커널 기능을 얻을 수 있습니다.

[WSL 2 Linux 커널은 오픈 소스](https://github.com/microsoft/WSL2-Linux-Kernel)입니다. 자세히 알아보려면 구축한 팀에서 작성한 [Windows를 사용하여 Linux 커널 전달](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) 블로그 게시물을 확인하세요.

### <a name="increased-file-io-performance"></a>파일 IO 성능 향상

git clone, npm install, apt update, apt upgrade 등과 같은 파일 집약적 작업은 모두 WSL 2를 통해 훨씬 더 빠르게 수행됩니다.

실제 속도 증가는 실행되는 앱과 이 앱에서 파일 시스템과 상호 작용하는 방법에 따라 달라집니다. 압축된 tarball의 압축을 푸는 경우 WSL 2의 초기 버전은 WSL 1보다 최대 20배 더 빠르게 실행되며, 다양한 프로젝트에서 git clone, npm install 및 cmake를 사용하는 경우 약 2~5배 더 빠르게 실행됩니다.

### <a name="full-system-call-compatibility"></a>전체 시스템 호출 호환성

Linux 이진 파일은 시스템 호출을 사용하여 파일 액세스, 메모리 요청, 프로세스 만들기 등의 함수를 수행합니다. WSL 1은 WSL 팀에서 개발한 번역 계층을 사용했지만 WSL 2에는 전체 시스템 호출 호환성을 지원하는 자체 Linux 커널이 포함되어 있습니다. 이점은 다음과 같습니다.

* **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** 등과 같이 WSL 내에서 실행할 수 있는 새로운 앱의 전체 세트입니다.

* Linux 커널에 대한 모든 업데이트를 즉시 사용할 수 있습니다. (WSL 팀에서 업데이트를 구현하고 변경 내용을 추가할 때까지 기다릴 필요가 없습니다.)

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a>시작 시 더 적은 양의 메모리를 사용하는 WSL 2

WSL 2는 메모리 공간이 작은 실제 Linux 커널에서 간단한 유틸리티 VM을 사용합니다. 유틸리티는 시작 시 가상 주소 지원 메모리를 할당합니다. 이는 WSL 1에 필요했던 총 메모리 중 더 적은 비율로 시작하도록 구성되어 있습니다.

## <a name="accessing-network-applications"></a>네트워크 애플리케이션 액세스

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a>Windows에서 Linux 네트워킹 앱에 액세스(localhost)

네트워킹 앱(예: NodeJS 또는 SQL 서버에서 실행되는 앱)을 Linux 배포에 구축하는 경우 `localhost`를 사용하여 Windows 앱(예: Edge 또는 Chrome 인터넷 브라우저)에서 이 앱에 액세스할 수 있습니다(일반적인 방법과 동일함).

그러나 이전 버전의 Windows(빌드 18945 이하)를 실행하는 경우 Linux 호스트 VM의 IP 주소를 가져와야 합니다(또는 [최신 Windows 버전으로 업데이트](ms-settings:windowsupdate)).

Linux 배포를 작동하는 가상 머신의 IP 주소를 찾으려면 다음을 수행합니다.

* WSL 배포(즉, Ubuntu)에서 `ip addr` 명령을 실행합니다.
* `eth0` 인터페이스의 `inet` 값 아래에서 주소를 찾아 복사합니다.
* grep 도구가 설치되어 있는 경우 `ip addr | grep eth0` 명령을 사용하여 출력을 필터링하여 더 쉽게 찾을 수 있습니다.
* 이 IP 주소를 사용하여 Linux 서버에 연결합니다.

아래 그림은 Edge 브라우저를 통해 Node.js 서버에 연결하여 이에 대한 예를 보여줍니다.

![Windows에서 Linux 네트워크 애플리케이션에 액세스](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a>Linux에서 Windows 네트워킹 앱에 액세스(호스트 IP)

Linux 배포(즉, Ubuntu)에서 Windows에서 실행되는 네트워킹 앱(예: NodeJS 또는 SQL 서버에서 실행되는 앱)에 액세스하려면 호스트 머신의 IP 주소를 사용해야 합니다. 일반적인 시나리오는 아니지만 다음 단계에 따라 작업을 수행할 수 있습니다.
    - Linux 배포에서 `cat /etc/resolv.conf` 명령을 실행하여 호스트 머신의 IP 주소를 가져옵니다.
    - IP 주소를 `nameserver`라는 용어 뒤에 복사합니다.
    - 복사한 IP 주소를 사용하여 Windows Server에 연결합니다.

아래 그림은 curl을 통해 Windows에서 실행 중인 Node.js 서버에 연결하여 이에 대한 예를 보여줍니다.

![Windows에서 Linux 네트워크 애플리케이션에 액세스](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a>추가 네트워킹 고려 사항

#### <a name="connecting-via-remote-ip-addresses"></a>원격 IP 주소를 통해 연결

원격 IP 주소를 사용하여 애플리케이션에 연결하는 경우 LAN(Local Area Network)에서 들어오는 연결로 취급됩니다. 즉 애플리케이션에서 LAN 연결을 허용할 수 있는지 확인해야 합니다.

예를 들어 애플리케이션을 `127.0.0.1` 대신 `0.0.0.0`에 바인딩해야 할 수 있습니다. Flask를 사용하는 Python 앱의 예제에서는 `app.run(host='0.0.0.0')` 명령을 사용하여 이 작업을 수행할 수 있습니다. 이러한 변경을 수행하는 경우 LAN으로부터의 연결이 허용되므로 보안에 유의하세요.

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a>LAN(Local Area Network)에서 WSL 2 배포에 액세스

WSL 1 배포를 사용할 때 LAN에서 컴퓨터에 액세스하도록 설정된 경우 WSL에서 실행되는 애플리케이션도 LAN에서 액세스할 수 있습니다.

이는 WSL 2의 기본 사례가 아닙니다. WSL 2에는 고유한 IP 주소가 있는 가상화된 이더넷 어댑터가 있습니다. 현재 이 워크플로를 사용하도록 설정하려면 일반 가상 머신과 동일한 단계를 진행해야 합니다. (이 환경을 개선할 수 있는 방법을 찾고 있습니다.)

다음은 호스트의 포트 4000에서 수신 대기하고 포트 4000을 통해 IP 주소가 192.168.101.100인 WSL 2 VM에 연결하는 포트 프록시를 추가하는 PowerShell 명령의 예입니다.
```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a>IPv6 액세스

WSL 2 배포는 현재 IPv6 전용 주소에 연결할 수 없습니다. 이 기능을 추가하기 위한 작업이 진행 중입니다.

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a>WSL 2 가상 하드웨어 디스크의 크기 확장

WSL 2는 VHD(가상 하드웨어 디스크)를 사용하여 Linux 파일을 저장합니다. 최대 크기에 도달하면 확장해야 할 수도 있습니다.

WSL 2 VHD는 ext4 파일 시스템을 사용합니다. 이 VHD는 스토리지 요구 사항에 맞게 크기가 자동으로 조정되며 초기 최대 크기는 256GB입니다. 배포의 크기가 256GB보다 큰 경우 디스크 공간이 부족하다는 오류가 표시됩니다. 이 오류는 VHD 크기를 확장하여 해결할 수 있습니다.

최대 VHD 크기를 256GB 이상으로 확장하려면 다음을 수행합니다.

1. `wsl --shutdown` 명령을 사용하여 모든 WSL 인스턴스를 종료합니다.

2. 배포 설치 패키지 이름('PackageFamilyName')을 찾습니다.
    * PowerShell을 사용하여 다음 명령을 입력합니다(여기서 'distro'는 배포 이름임).
    * `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. WSL 2 설치에 사용된 VHD 파일 `fullpath`를 찾습니다. 이 경로는 `pathToVHD`가 됩니다.
     * `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. 다음 명령을 완료하여 WSL 2 VHD의 크기를 조정합니다.
   * 관리자 권한으로 Windows 명령 프롬프트를 열고 다음을 입력합니다.
      * `diskpart`
      * `Select vdisk file="<pathToVHD>"`
      * `expand vdisk maximum="<sizeInMegaBytes>"`

5. WSL 배포(예: Ubuntu)를 시작합니다.

6. Linux 배포 명령줄에서 다음 명령을 실행하여 WSL에서 파일 시스템의 크기를 확장할 수 있음을 알려줍니다.
    * `sudo mount -t devtmpfs none /dev`
    * `mount | grep ext4`
    * `/dev/sdXX`와 같은 이 항목의 이름을 복사합니다(여기서 X는 다른 문자를 나타냄).
    * `sudo resize2fs /dev/sdXX`
    * 이전에 복사한 값을 사용합니다. resize2fs를 설치해야 할 수도 있습니다(`apt install resize2fs`).

> [!NOTE]
> 일반적으로 Windows 도구 또는 편집기를 사용하여 AppData 폴더 내에 있는 WSL 관련 파일을 수정하거나 이동하거나 액세스해서는 안 됩니다. 이렇게 하면 Linux 배포가 손상될 수 있습니다.
