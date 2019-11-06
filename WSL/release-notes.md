---
title: Linux용 Windows 하위 시스템의 릴리스 정보
description: Linux용 Windows 하위 시스템의 릴리스 정보입니다.  매주 업데이트됩니다.
keywords: BashOnWindows, bash, wsl, windows, linux용 windows 하위 시스템, windows 하위 시스템, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 63c0e14dab73faf7f835e9ae1eb23eb490b13c44
ms.sourcegitcommit: 48ca05ce1ac8bf35408af3bc2a2b92a43adba0af
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166663"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템의 릴리스 정보

## <a name="build-19013"></a>빌드 19013
빌드 19013에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/)를 참조하세요.

* [WSL2] WSL 유틸리티 VM의 메모리 성능을 개선합니다. 더 이상 사용하지 않는 메모리는 호스트로 다시 해제됩니다.
* [WSL2] 커널 버전을 4.19.79로 업데이트합니다. (CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK 및 CONFIG_BRIDGE_VLAN_FILTERING 추가).
* [WSL2] stdin이 닫혀 있지 않은 파이프 핸들인 경우를 처리하기 위해 입력 릴레이를 수정합니다.[GH 4424]
* \\\\wsl$ 대/소문자를 구분하지 않는지 확인합니다.
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a>빌드 19002
빌드 19002에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/)를 참조하세요.

* [WSL] 일부 유니코드 문자 처리 이슈 해결: https://github.com/microsoft/terminal/issues/2770
* [WSL] 빌드 간 업그레이드 후 바로 시작할 경우 드물게 배포판이 등록 취소되는 사례를 수정합니다.
* [WSL] 인스턴스 유휴 타이머가 취소되지 않은 wsl.exe --shutdown의 사소한 이슈를 해결합니다.

## <a name="build-18995"></a>빌드 18995
빌드 18995에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)를 참조하세요.

* [WSL2] 작업이 중단된 후 DrvFs 탑재가 중지되는 문제 해결(예: ctrl-c) [GH 4377]
* [WSL2] 매우 큰 hvsocket 메시지 처리 문제 해결 [GH 4105]
* [WSL2] stdin이 파일인 경우 interop 문제 해결 [GH 4475]
* [WSL2] 예기치 않은 네트워크 상태가 발생한 경우 서비스 충돌 문제 해결 [GH 4474]
* [WSL2] 현재 프로세스에 환경 변수가 없는 경우 interop 서버에서 배포 이름 쿼리
* [WSL2] stdin이 파일인 경우 interop 문제 해결
* [WSL2] Linux 커널 버전을 4.19.72로 업데이트
* [WSL2] .wslconfig를 통해 추가 커널 명령줄 매개 변수를 지정하는 기능 추가
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a>빌드 18990
빌드 18990에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)를 참조하세요.

* \\\\wsl$의 디렉터리 목록의 성능 개선
* [WSL2] 추가 부팅 엔트로피를 주입합니다.[GH 4416]
* [WSL2] su/sudo를 사용할 때 Windows 인터럽트를 수정합니다.[GH 4465]

## <a name="build-18980"></a>빌드 18980
빌드 18980에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)를 참조하세요.

* FILE_READ_DATA를 거부하는 읽기 symlink를 수정했습니다. 여기에는 "C:\Document and Settings"처럼 이전 버전과의 호환성을 위해 Windows에서 만드는 모든 symlink와 사용자 프로필 디렉터리의 symlink가 포함됩니다.
* 예기치 않은 파일 시스템 상태를 심각하지 않은 상태로 표시합니다. [GH 4334, 4305]
* [WSL2] CPU/펌웨어가 가상화를 지원하는 경우 arm64에 대한 지원이 추가됩니다.
* [WSL2] 권한 없는 사용자가 커널 로그를 볼 수 있도록 허용합니다.
* [WSL2] stdout/stderr 소켓이 닫혀 있을 때 발생하는 출력 릴레이를 수정했습니다. [GH 4375]
* [WSL2] 배터리 및 AC 어댑터 통과를 지원합니다.
* [WSL2] Linux 커널을 4.19.67로 업데이트했습니다.
* 다음과 같이 /etc/wsl.conf에서 기본 사용자 이름을 설정하는 기능이 추가되었습니다.
```
[user]
default=<string>
```

## <a name="build-18975"></a>빌드 18975
빌드 18975에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)를 참조하세요.

* [WSL2] 여러 localhost 안정성 이슈를 해결했습니다. [GH 4340]

## <a name="build-18970"></a>빌드 18970
빌드 18970에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)를 참조하세요.

* [WSL2] 시스템이 절전 모드에서 다시 시작될 때 시간을 호스트 시간과 동기화합니다. [GH 4245]
* [WSL2] 가능한 경우 Windows 볼륨에 NT symlink를 만듭니다.
* [WSL2] UTS, IPC, PID 및 탑재 네임스페이스에서 배포판을 만듭니다.
* [WSL2] 서버가 localhost에 직접 바인딩할 때 localhost 포트 릴레이를 수정합니다. [GH 4353]
* [WSL2] 출력이 리디렉션될 때 interop를 수정합니다. [GH 4337]
* [WSL2] 절대 NT symlink 변환을 지원합니다.
* [WSL2] 커널을 4.19.59로 업데이트합니다.
* [WSL2] eth0에 대한 서브넷 마스크를 적절히 설정합니다.
* [WSL2] 종료 이벤트가 신호를 받으면 콘솔 작업자 루프를 중단하도록 논리를 변경합니다.
* [WSL2] 배포판이 실행되고 있지 않으면 배포용 vhd를 배출합니다.
* [WSL2] 빈 값을 올바르게 처리하도록 구성 구문 분석 라이브러리를 수정합니다.
* [WSL2] 교차 배포판 탑재를 만들어 Docker 데스크톱을 지원합니다. 다음 줄을 /etc/wsl.conf 파일에 추가하여 배포판에서 이 동작을 옵트인할 수 있습니다.
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a>빌드 18945
빌드 18945에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)를 참조하세요.

### <a name="wsl"></a>WSL
* [WSL2] localhost:port를 사용하여 호스트에서 액세스할 수 있도록 WSL2에서 수신 대기 tcp 소켓을 허용합니다.
* [WSL2] 향후 이슈를 추적하도록 설치/변환 오류 및 추가 진단을 수정합니다. [GH 4105] 
* [WSL2] WSL2 네트워크 이슈 진단 기능을 개선합니다.
* [WSL2] 커널 버전을 4.19.55로 업데이트합니다.
* [WSL2] docker에 필요한 구성 옵션으로 커널을 업데이트합니다. [GH 4165]
* [WSL2] 경량 유틸리티 VM에 할당된 CPU 수를 호스트와 동일하게 늘립니다(이전에는 커널 구성의 CONFIG_NR_CPUS에 의해 8로 제한). [GH 4137]
* [WSL2] WSL2 경량 VM에 대한 스왑 파일을 만듭니다.
* [WSL2] 사용자가 \\\\wsl$\\distro를 통해 탑재를 볼 수 있도록 허용합니다(예: sshfs). [GH 4172]
* [WSL2] 9p 파일 시스템 성능을 개선합니다.
* [WSL2] vhd ACL이 무한으로 확장되지 않도록 보장합니다. [GH 4126]
* [WSL2] squashfs 및 xt_conntrack을 지원하도록 커널 구성을 업데이트합니다. [GH 4107, 4123]
* [WSL2] interop.enabled /etc/wsl.conf 옵션을 수정합니다. [GH 4140]
* [WSL2] 파일 시스템에서 EA를 지원하지 않는 경우 ENOTSUP를 반환합니다.
* [WSL2] \\\\wsl$를 사용하여 CopyFile 중단을 수정합니다.
* 기본 umask를 0022로 전환하고 /etc/wsl.conf에 filesystem.umask 설정을 추가합니다.
* symlink를 적절하게 확인하도록 wslpath를 수정합니다.이것은 19h1에서 회귀되었습니다. [GH 4078]
* WSL2 설정을 수정하기 위한 %UserProfile%\\.wslconfig 파일을 도입합니다.
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a>빌드 18917
빌드 18917에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)를 참조하세요.

### <a name="wsl"></a>WSL
* 이제 WSL 2를 사용할 수 있습니다! 자세한 내용은 [블로그](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)를 참조하세요.
* symlink를 통해 Windows 프로세스를 시작하면 올바르게 작동하지 않는 성능 문제를 해결합니다. [GH 3999]
* wsl.exe에 wsl.exe --list --verbose, wsl.exe --list --quiet 및 wsl.exe --import --version 옵션을 추가합니다.
* wsl.exe --shutdown 옵션을 추가합니다.
* 플랜 9: 쓰기가 성공하도록 디렉터리 열기를 허용합니다.

## <a name="build-18890"></a>빌드 18890
빌드 18890에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)를 참조하세요.

### <a name="wsl"></a>WSL
* 비차단 소켓 유실 [GH 2913]
* 터미널의 EOF 입력이 후속 읽기를 차단할 수 있습니다. [GH 3421]
* wsl.conf를 참조하도록 resolv.conf 헤더를 업데이트합니다. [GH 3928에서 설명]
* epoll 삭제 코드의 교착 상태 [GH 3922]
* --import 및 –export에 대한 인수의 공백을 처리합니다. [GH 3932]
* mmap’d 파일을 확장하면 올바르게 작동하지 않습니다. [GH 3939]
* ARM64 \\\\wsl$ 액세스가 올바르게 작동하지 않는 문제 해결
* wsl.exe에 대한 개선된 기본 아이콘을 추가합니다.

## <a name="build-18342"></a>빌드 18342
빌드 18342에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)를 참조하세요.

### <a name="wsl"></a>WSL
* 사용자가 Windows에서 WSL 배포판의 Linux 파일에 액세스할 수 있는 기능을 추가했습니다. 이러한 파일은 명령줄을 통해 액세스할 수 있으며 파일 탐색기, VSCode 등의 Windows 앱에서도 이러한 파일과 상호 작용할 수 있습니다. \\\\wsl$\\<distro_name>으로 이동하여 파일에 액세스하거나, \\\\wsl$로 이동하여 실행 중인 배포판 목록을 확인하세요.
* 추가 CPU 정보 태그를 추가하고 Cpus_allowed[_list] 값을 수정합니다. [GH 2234]
* 리더가 아닌 스레드의 exec를 지원합니다. [GH 3800]
* 구성 업데이트 실패를 심각하지 않은 오류로 처리합니다. [GH 3785]
* 오프셋을 적절하게 처리하도록 binfmt를 업데이트합니다. [GH 3768]
* 플랜 9에 매핑 네트워크 드라이브를 사용합니다. [GH 3854]
* 바인딩 마운트를 위한 Windows > Linux 및 Linux > Windows 경로 변환을 지원합니다.
* 읽기 전용으로 열린 파일의 매핑에 대한 읽기 전용 섹션을 만듭니다.

## <a name="build-18334"></a>빌드 18334
빌드 18334에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)를 참조하세요.

### <a name="wsl"></a>WSL
* Windows 표준 시간대가 Linux 표준 시간대에 매핑되는 방식을 다시 디자인합니다. [GH 3747]
* 메모리 누수를 해결하고 새 문자열 변환 함수를 추가합니다. [GH 3746]
* 스레드 없는 threadgroup의 SIGCONT는 no-op입니다. [GH 3741] 
* /proc/self/fd에 소켓 및 epoll 파일 설명자를 올바르게 표시합니다.

## <a name="build-18305"></a>빌드 18305
빌드 18305에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)를 참조하세요.

### <a name="wsl"></a>WSL
* 주 스레드가 종료되면 pthread가 파일에 액세스할 수 없습니다. [GH 3589]
* TIOCSCTTY는 꼭 필요한 경우 외에는 "force" 매개 변수를 무시해야 합니다. [GH 3652]
* wsl.exe 명령줄 기능이 개선되고 가져오기/내보내기 함수가 추가되었습니다.
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a>빌드 18277
빌드 18277에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)를 참조하세요.

### <a name="wsl"></a>WSL
* 빌드 18272에서 발생하는 "해당 인터페이스를 지원하지 않습니다" 오류를 해결합니다. [GH 3645]
* umount syscall에 대한 MNT_FORCE 플래그를 무시합니다. [GH 3605]
* 공식 CreatePseudoConsole API를 사용하도록 WSL interop를 전환합니다.
* FUTEX_WAIT가 다시 시작할 때 시간 제한 값을 유지하지 않습니다.

## <a name="build-18272"></a>빌드 18272
빌드 18272에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)를 참조하세요.

### <a name="wsl"></a>WSL
* **경고:** 이 빌드에는 WSL이 작동하지 않는 문제가 있습니다. 배포를 시작하려고 하면 "해당 인터페이스를 지원하지 않습니다" 오류가 표시됩니다. 이 이슈는 해결되었으며 다음 주의 초기 참가자 빌드에 포함될 예정입니다. 이 빌드를 설치한 경우 설정->업데이트 & 보안->복구에서 "이전 버전의 Windows 10으로 되돌리기"를 사용하여 이전 Windows 빌드로 롤백할 수 있습니다.

## <a name="build-18267"></a>빌드 18267
빌드 18267에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)를 참조하세요.

### <a name="wsl"></a>WSL
* 좀비 프로세스가 제거되지 않고 무기한으로 유지되는 문제를 해결합니다.
* 오류 메시지가 최대 길이를 초과하는 경우 WslRegisterDistribution이 중지됩니다. [GH 3592]
* DrvFs에서 읽기 전용 파일에 대해 fsync가 성공하도록 허용합니다. [GH 3556]
* symlink를 만들기 전에 /bin 및 /sbin 디렉터리가 존재하는지 확인합니다. [GH 3584]
* WSL 인스턴스에 대한 인스턴스 종료 시간 제한 메커니즘이 추가되었습니다. 현재 시간 제한은 15초로 설정되어 있습니다. 즉, 마지막 WSL 프로세스가 종료된 후 15초 후에 인스턴스가 종료됩니다. 배포를 즉시 종료하려면 다음을 사용합니다.
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>빌드 17763(1809)
빌드 17763에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)를 참조하세요.

### <a name="wsl"></a>WSL
* 동일한 스레드 우선 순위를 변경하기 위한 Setpriority syscall 권한 검사가 너무 엄격합니다. [GH 1838]
* clock_gettime(CLOCK_BOOTTIME)에 대한 음수 값이 반환되지 않도록, 부팅 시간에 비편향 인터럽트 시간을 사용하도록 확인합니다. [GH 3434]
* WSL binfmt 인터프리터의 symlink를 처리합니다. [GH 3424]
* threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리합니다.
* 오버플로를 방지하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용하도록 WSL을 전환합니다. [GH 3252]
* Ptrace attach로 인해 시스템 호출에서 잘못된 값이 반환될 수 있습니다. [GH 1731]
* 여러 AF_UNIX 관련 이슈를 해결합니다. [GH 3371]
* 현재 작업 디렉터리 길이가 5자 미만인 경우 WSL interop가 실패할 수 있는 이슈를 해결합니다. [GH 3379]
* 존재하지 않는 포트에 대한 루프백 연결이 실패하지 않도록 1초 지연을 방지합니다. [GH 3286]
* /proc/sys/fs/file-max 스텁 파일을 추가합니다. [GH 2893]
* 보다 정확한 IPV6 범위 정보입니다.
* PR_SET_PTRACER를 지원합니다. [GH 3053]
* 파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]
* NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]
* 좀비 지원이 개선되었습니다. [GH 1353]
* Windows interop 동작을 제어하기 위한 wsl.conf 항목을 추가합니다. [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* getsockname이 경우에 따라 UNIX 소켓 패밀리 유형을 반환하지 않는 문제를 해결합니다. [GH 1774]
* TIOCSTI 지원이 추가됩니다. [GH 1863]
* 연결 중인 비차단 소켓은 쓰기 시도에 대한 EAGAIN을 반환해야 합니다. [GH 2846]
* 탑재된 VHD에서 interop를 지원합니다. [GH 3246, 3291]
* 루트 폴더에 대한 권한 확인 이슈를 해결합니다. [GH 3304]
* TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대한 지원이 제한됩니다.
* Windows UI 앱은 백그라운드에서 시작된 경우에도 실행되어야 합니다.
* wsl -u 또는 --user 옵션이 추가됩니다. [GH 1203]
* 빠른 시작을 사용하는 경우 WSL 시작 이슈를 해결합니다. [GH 2576]
* Unix 소켓은 연결 해제된 피어 자격 증명을 유지해야 합니다. [GH 3183]
* 비차단 Unix 소켓이 EAGAIN과 함께 무기한 실패합니다. [GH 3191]
* case=off는 새로운 기본 drvfs 탑재 유형입니다. [GH 2937, 3212, 3328]
    * 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)를 참조하세요.
* 실행 중인 배포를 중지하려면 wslconfig /terminate를 추가합니다.
* 공백이 포함된 경로를 올바르게 처리하지 않는 WSL 셸 팝업 메뉴 항목의 이슈를 해결합니다.
* 디렉터리별 대/소문자 구분을 확장 특성으로 노출합니다.
* ARM64: 캐시 유지 관리 작업을 에뮬레이트합니다. [dotnet 이슈](https://github.com/dotnet/core/issues/1561)를 해결합니다.
* DrvFs: 프라이빗 범위에서 이스케이프된 문자에 해당하는 문자만 unescape합니다.
* ELF 파서 인터프리터 길이 유효성 검사의 OB1 오류를 수정합니다. [GH 3154]
* 과거 시간이 포함된 WSL 절대 타이머가 시작되지 않습니다. [GH 3091]
* 새로 만든 재분석 지점이 부모 디렉터리에 표시되는지 확인합니다.
* DrvFs에 대/소문자를 구분하는 디렉터리를 원자 단위로 만듭니다.
* 파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 추가 이슈를 해결했습니다. [GH 2712]
* UMCI를 사용하는 경우 WSL 시작이 실패하는 문제가 해결되었습니다. [GH 3020]
* WSL을 시작하는 탐색기 팝업 메뉴를 추가합니다. [GH 437, 603, 1836]. 사용하려면 탐색기 창에서 Shift 키를 누른 상태로 마우스 오른쪽 단추를 클릭합니다.
* Unix 소켓 비차단 동작을 수정합니다. [GH 2822, 3100]
* GH 2026에 보고된 것처럼 NETLINK 명령이 중지되는 문제를 해결합니다.
* 탑재 전파 플래그에 대한 지원이 추가됩니다. [GH 2911]
* 자르기가 Inotify 이벤트를 발생시키지 않는 이슈를 해결합니다. [GH 2978]
* wsl.exe가 셸 없이 단일 이진 파일을 호출하는 --exec 옵션이 추가됩니다.
* wsl.exe가 특정 배포판을 선택하는 --distribution 옵션이 추가됩니다.
* dmesg에 대한 지원이 제한됩니다. 이제 애플리케이션에서 dmesg에 기록할 수 있습니다. WSL 드라이버는 제한된 정보를 dmesg에 기록합니다. 이후에 드라이버의 다른 정보/진단을 수행하도록 이 기능이 확장될 수 있습니다.
    * 참고: dmesg는 현재 `/dev/kmsg` 디바이스 인터페이스를 통해 지원됩니다. `syslog` syscall 인터페이스는 아직 지원되지 않습니다. 따라서 `-S`, `-C` 같은 `dmesg` 명령줄 옵션 중 일부는 작동하지 않습니다.
* 네이티브와 일치하도록 직렬 디바이스의 기본 그리드 및 모드를 변경합니다. [GH 3042]
* DrvFs는 이제 확장된 특성을 지원합니다.
    * 참고: DrvFs는 확장 특성의 이름에 대한 몇 가지 제한이 있습니다. 일부 문자(예: '/', ':' 및 '\*')는 허용되지 않으며, 확장 특성 이름은 DrvFs에서 대/소문자를 구분하지 않습니다.

## <a name="build-18252-skip-ahead"></a>빌드 18252(앞으로 건너뛰기)
빌드 18252에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)를 참조하세요.

### <a name="wsl"></a>WSL
* lxssmanager dll에서 init 및 bsdtar 이진 파일을 별도의 도구 폴더로 이동합니다.
* CLONE_FILES를 사용할 때 파일 설명자를 닫는 동안 경합을 해결합니다.
* DrvFs 경로를 변환할 때 /proc/pid/mountinfo의 선택적 필드를 처리합니다.
* S_IFREG에 대한 메타데이터 지원 없이 DrvFs mknod가 성공하도록 허용합니다.
* DrvFs에서 만든 읽기 전용 파일에는 readonly 특성 세트가 있어야 합니다. [GH 3411]
* DrvFs 탑재를 처리하는 /sbin/mount.drvfs 도우미가 추가됩니다.
* DrvFs에서 POSIX rename을 사용합니다.
* 볼륨 GUID 없이 볼륨의 경로 변환을 허용합니다.

## <a name="build-17738-fast"></a>빌드 17738(패스트)
빌드 17738에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)를 참조하세요.

### <a name="wsl"></a>WSL
* 동일한 스레드 우선 순위를 변경하기 위한 Setpriority syscall 권한 검사가 너무 엄격합니다. [GH 1838]
* clock_gettime(CLOCK_BOOTTIME)에 대한 음수 값이 반환되지 않도록, 부팅 시간에 비편향 인터럽트 시간을 사용하도록 확인합니다. [GH 3434]
* WSL binfmt 인터프리터의 symlink를 처리합니다. [GH 3424]
* threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리합니다.

## <a name="build-17728-fast"></a>빌드 17728(패스트)
빌드 17728에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)를 참조하세요.

### <a name="wsl"></a>WSL
* 오버플로를 방지하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용하도록 WSL을 전환합니다. [GH 3252]
* Ptrace attach로 인해 시스템 호출에서 잘못된 값이 반환될 수 있습니다. [GH 1731]
* 여러 AF_UNIX 관련 이슈를 해결합니다. [GH 3371]
* 현재 작업 디렉터리 길이가 5자 미만인 경우 WSL interop가 실패할 수 있는 이슈를 해결합니다. [GH 3379]

## <a name="build-18204-skip-ahead"></a>빌드 18204(앞으로 건너뛰기)
빌드 18204에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조하세요.

### <a name="wsl"></a>WSL
* 파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]
* NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]

## <a name="build-17723-fast"></a>빌드 17723(패스트)
빌드 17723에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조하세요.

### <a name="wsl"></a>WSL
* 존재하지 않는 포트에 대한 루프백 연결이 실패하지 않도록 1초 지연을 방지합니다. [GH 3286]
* /proc/sys/fs/file-max 스텁 파일을 추가합니다. [GH 2893]
* 보다 정확한 IPV6 범위 정보입니다.
* PR_SET_PTRACER를 지원합니다. [GH 3053]
* 파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]
* NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]

## <a name="build-17713"></a>빌드 17713
빌드 17713에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)를 참조하세요.

### <a name="wsl"></a>WSL
* 좀비 지원이 개선되었습니다. [GH 1353]
* Windows interop 동작을 제어하기 위한 wsl.conf 항목을 추가합니다. [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* getsockname이 경우에 따라 UNIX 소켓 패밀리 유형을 반환하지 않는 문제를 해결합니다. [GH 1774]
* TIOCSTI 지원이 추가됩니다. [GH 1863]
* 연결 중인 비차단 소켓은 쓰기 시도에 대한 EAGAIN을 반환해야 합니다. [GH 2846]
* 탑재된 VHD에서 interop를 지원합니다. [GH 3246, 3291]
* 루트 폴더에 대한 권한 확인 이슈를 해결합니다. [GH 3304]
* TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대한 지원이 제한됩니다.
* Windows UI 앱은 백그라운드에서 시작된 경우에도 실행되어야 합니다.

## <a name="build-17704"></a>빌드 17704
빌드 17704에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)를 참조하세요.

### <a name="wsl"></a>WSL
* wsl -u 또는 --user 옵션이 추가됩니다. [GH 1203]
* 빠른 시작을 사용하는 경우 WSL 시작 이슈를 해결합니다. [GH 2576]
* Unix 소켓은 연결 해제된 피어 자격 증명을 유지해야 합니다. [GH 3183]
* 비차단 Unix 소켓이 EAGAIN과 함께 무기한 실패합니다. [GH 3191]
* case=off는 새로운 기본 drvfs 탑재 유형입니다. [GH 2937, 3212, 3328]
    * 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)를 참조하세요.
* 실행 중인 배포를 중지하려면 wslconfig /terminate를 추가합니다.

## <a name="build-17692"></a>빌드 17692
빌드 17692에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)를 참조하세요.

### <a name="wsl"></a>WSL
* 공백이 포함된 경로를 올바르게 처리하지 않는 WSL 셸 팝업 메뉴 항목의 이슈를 해결합니다.
* 디렉터리별 대/소문자 구분을 확장 특성으로 노출합니다.
* ARM64: 캐시 유지 관리 작업을 에뮬레이트합니다. [dotnet 이슈](https://github.com/dotnet/core/issues/1561)를 해결합니다.
* DrvFs: 프라이빗 범위에서 이스케이프된 문자에 해당하는 문자만 unescape합니다.

## <a name="build-17686"></a>빌드 17686
빌드 17686에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)를 참조하세요.

### <a name="wsl"></a>WSL
* ELF 파서 인터프리터 길이 유효성 검사의 OB1 오류를 수정합니다. [GH 3154]
* 과거 시간이 포함된 WSL 절대 타이머가 시작되지 않습니다. [GH 3091]
* 새로 만든 재분석 지점이 부모 디렉터리에 표시되는지 확인합니다.
* DrvFs에 대/소문자를 구분하는 디렉터리를 원자 단위로 만듭니다.

## <a name="build-17677"></a>빌드 17677
빌드 17677에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)를 참조하세요.

### <a name="wsl"></a>WSL
* 파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 추가 이슈를 해결했습니다. [GH 2712]
* UMCI를 사용하는 경우 WSL 시작이 실패하는 문제가 해결되었습니다. [GH 3020]

## <a name="build-17666"></a>빌드 17666
빌드 17666에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)를 참조하세요.

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>경고: 일부 AMD 칩셋에서 WSL이 실행되지 않는 이슈가 있습니다 [GH 3134]. 해결 방법이 준비되어 있으며 참가자 빌드 분기에 적용 중입니다.
* WSL을 시작하는 탐색기 팝업 메뉴를 추가합니다. [GH 437, 603, 1836]. 사용하려면 탐색기 창에서 Shift 키를 누른 상태로 마우스 오른쪽 단추를 클릭합니다.
* Unix 소켓 비차단 동작을 수정합니다. [GH 2822, 3100]
* GH 2026에 보고된 것처럼 NETLINK 명령이 중지되는 문제를 해결합니다.
* 탑재 전파 플래그에 대한 지원이 추가됩니다. [GH 2911]
* 자르기가 Inotify 이벤트를 발생시키지 않는 이슈를 해결합니다. [GH 2978]
* wsl.exe가 셸 없이 단일 이진 파일을 호출하는 --exec 옵션이 추가됩니다.
* wsl.exe가 특정 배포판을 선택하는 --distribution 옵션이 추가됩니다.

## <a name="build-17655-skip-ahead"></a>빌드 17655(앞으로 건너뛰기)
빌드 17655에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)를 참조하세요.

### <a name="wsl"></a>WSL
* dmesg에 대한 지원이 제한됩니다. 이제 애플리케이션에서 dmesg에 기록할 수 있습니다. WSL 드라이버는 제한된 정보를 dmesg에 기록합니다. 이후에 드라이버의 다른 정보/진단을 수행하도록 이 기능이 확장될 수 있습니다.
    * 참고: dmesg는 현재 `/dev/kmsg` 디바이스 인터페이스를 통해 지원됩니다. `syslog` syscall 인터페이스는 아직 지원되지 않습니다. 따라서 `-S`, `-C` 같은 `dmesg` 명령줄 옵션 중 일부는 작동하지 않습니다.
* 파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 이슈를 해결했습니다. [GH 2712]

## <a name="build-17639-skip-ahead"></a>빌드 17639(앞으로 건너뛰기)
빌드 17639에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)를 참조하세요.

### <a name="wsl"></a>WSL
* 네이티브와 일치하도록 직렬 디바이스의 기본 그리드 및 모드를 변경합니다. [GH 3042]
* DrvFs는 이제 확장된 특성을 지원합니다.
    * 참고: DrvFs는 확장 특성의 이름에 대한 몇 가지 제한이 있습니다. 특히 일부 문자(예: '/', ':' 및 '\*')는 허용되지 않으며, 확장 특성 이름은 DrvFs에서 대/소문자를 구분하지 않습니다.

## <a name="build-17133-fast"></a>빌드 17133(패스트)
빌드 17133에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)를 참조하세요.

### <a name="wsl"></a>WSL
* WSL의 중단 문제를 해결합니다. [GH 3039, 3034]

## <a name="build-17128-fast"></a>빌드 17128(패스트)
빌드 17128에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)를 참조하세요.

### <a name="wsl"></a>WSL
* 없음

## <a name="build-17627-skip-ahead"></a>빌드 17627(앞으로 건너뛰기)
빌드 17627에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)를 참조하세요.

### <a name="wsl"></a>WSL
* futex pi 인식 작업에 대한 지원이 추가됩니다. [GH 1006]
    * 우선 순위는 현재 지원되는 WSL 기능이 아니므로 제한이 있지만, 표준 사용의 차단을 해제해야 합니다.
* Windows 방화벽은 WSL 프로세스를 지원합니다. [GH 1852]
    * 예를 들어 WSL python 프로세스가 모든 포트에서 수신 대기하도록 허용하려면 관리자 권한 Windows cmd ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```를 사용합니다.
    * 방화벽 규칙을 추가하는 방법에 대한 자세한 내용은 [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)를 참조하세요.
* wsl.exe를 사용할 때 사용자의 기본 셸을 준수합니다. [GH 2372]
* 모든 네트워크 인터페이스를 이더넷으로 보고합니다. [GH 2996]
* 손상된 /etc/passwd 파일을 보다 효율적으로 처리합니다. [GH 3001]

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17618-skip-ahead"></a>빌드 17618(앞으로 건너뛰기)
빌드 17618에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)를 참조하세요.

### <a name="wsl"></a>WSL
* NT interop에 대한 pseudoconsole 기능을 도입합니다. [GH 988, 1366, 1433, 1542, 2370, 2406]
* 레거시 설치 메커니즘(lxrun.exe)은 더 이상 사용되지 않습니다. 배포판 설치를 위한 메커니즘은 Microsoft Store를 통해 지원됩니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17110"></a>빌드 17110
빌드 17110에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)를 참조하세요.

### <a name="wsl"></a>WSL
* Windows에서 /init를 종료할 수 있습니다. [GH 2928]
* 이제 DrvFs는 기본적으로 디렉터리 단위 대/소문자 구분을 사용합니다(“case=dir” 탑재 옵션과 동일).
    * “case=force”(이전 동작)를 사용하려면 레지스트리 키를 설정해야 합니다. "case=force"를 사용해야 하는 경우 reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1 명령을 실행하여 "case=force"를 설정합니다.
    * 이전 버전의 Windows에서 WSL을 사용하여 만든 기존 디렉터리가 있고 대/소문자를 구분해야 하는 경우 다음 fsutil.exe를 사용하여 대/소문자를 구분하도록 설정합니다. fsutil.exe file setcasesensitiveinfo <path> enable
* NULL은 uname syscall에서 반환된 문자열을 종료합니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17107"></a>빌드 17107
빌드 17107에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)를 참조하세요.

### <a name="wsl"></a>WSL
* 마스터 pty 엔드포인트에서 TCSETSF 및 TCSETSW를 지원합니다. [GH 2552]
* 동시 interop 프로세스를 시작하면 EINVAL이 발생할 수 있습니다. [GH 2813]
* /proc/pid/status에서 적절한 추적 상태를 표시하도록 PTRACE_ATTACH를 수정합니다.
* CLEARTID 및 SETTID 플래그를 모두 사용하여 복제된 단기 프로세스가 TID 주소를 지우지 않고 종료될 수 있는 경합을 수정합니다.
* 17093 이전 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드하는 동안 메시지를 표시합니다. 17093 파일 시스템 변경 내용에 대한 자세한 내용은 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 릴리스 정보를 참조하세요.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17101"></a>빌드 17101
빌드 17101에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)를 참조하세요.

### <a name="wsl"></a>WSL
* signalfd를 지원합니다. [GH 129]
* 지원되지 않는 NTFS 문자가 포함된 파일 이름을 프라이빗 유니코드 문자로 인코딩하여 지원합니다. [GH 1514]
* 쓰기가 지원되지 않는 경우 자동 탑재는 읽기 전용으로 대체됩니다. [GH 2603]
* 유니코드 서로게이트 쌍(예:이모지 문자)을 붙여넣을 수 있습니다. [GH 2765]
* /proc 및 /sys의 의사 파일은 select, poll, epoll 등에서 read and write ready를 반환해야 합니다. [GH 2838]
* 레지스트리가 변조되거나 손상된 경우 서비스가 무한 루프에 빠질 수 있는 이슈를 해결합니다.
* 최신 버전의 iproute2(업스트림 4.14)를 사용하도록 netlink 메시지를 수정합니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17093"></a>빌드 17093
빌드 17093에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)를 참조하세요.

#### <a name="important"></a>중요:
이 빌드로 업그레이드한 후 처음으로 WSL을 시작할 때 Linux 파일 시스템 디렉터리를 업그레이드하는 작업을 수행해야 합니다. 이 작업은 몇 분 정도 걸릴 수 있으므로 WSL이 느리게 시작되는 것처럼 보일 수 있습니다. 이 작업은 스토어에서 설치한 배포판마다 한 번씩만 수행됩니다.
* DrvFs의 대/소문자 구분 지원이 개선되었습니다.
    * 이제 DrvFs는 디렉터리 단위 대/소문자 구분을 지원합니다. 이 새로운 플래그를 디렉터리에 설정하여 해당 디렉터리의 모든 작업을 대/소문자 구분으로 나타낼 수 있으며, 이렇게 하면 Windows 애플리케이션에서도 대/소문자만 다른 파일을 올바르게 열 수 있습니다.
    * DrvFs에는 디렉터리 단위로 대/소문자 구분을 제어하는 다음과 같은 새로운 탑재 옵션이 있습니다.
        * case=force: 모든 디렉터리가 대/소문자 구분으로 처리됩니다(드라이브 루트 제외). WSL에서 만든 새 디렉터리는 대/소문자를 구분하는 것으로 표시됩니다. 새 디렉터리를 대/소문자 구분으로 표시하는 것만 제외하면 레거시 동작입니다.
        * case=dir: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리되고, 다른 디렉터리는 대/소문자를 구분하지 않습니다. WSL에서 만든 새 디렉터리는 대/소문자를 구분하는 것으로 표시됩니다.
        * case=off: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리되고, 다른 디렉터리는 대/소문자를 구분하지 않습니다. WSL로 만든 새 디렉터리는 대/소문자를 구분하지 않는 것으로 표시됩니다.
    * 참고: 이전 릴리스의 WSL에서 만든 디렉터리는 이 플래그가 설정되지 않았으므로 "case=dir" 옵션을 사용하는 경우 대/소문자를 구분하는 것으로 간주되지 않습니다. 기존 디렉터리에 이 플래그를 설정하는 방법이 곧 제공될 예정입니다.
    * 이러한 옵션을 사용하는 탑재 예제로는 sudo mount -t drvfs C: /mnt/c -o case=dir이 있습니다(기존 드라이브의 경우 먼저 탑재 해제해야만 다른 옵션으로 탑재 가능).
    * 현재는 case=force가 여전히 기본 옵션입니다. 향후 case=dir로 변경될 것입니다.
* 이제 DrvFs를 탑재할 때 Windows 경로에 슬래시를 사용할 수 있습니다(예: sudo mount -t drvfs //server/share /mnt/share).
* 이제 인스턴스를 시작하는 동안 WSL에서 /etc/fstab 파일을 처리합니다. [GH 2636]
    * 이 작업은 DrvFs 드라이브를 자동으로 탑재하기 전에 수행됩니다. fstab을 통해 이미 탑재된 드라이브는 자동으로 다시 탑재되지 않으므로 특정 드라이브의 탑재 지점을 변경할 수 있습니다.
    * 이 동작은 wsl.conf를 사용하여 해제할 수 있습니다.
* /proc의 mount, mountinfo 및 mountstats 파일은 백슬래시 및 공백과 같은 특수 문자를 적절히 이스케이프합니다. [GH 2799]
* DrvFs를 사용하여 만든 특수 파일(예: WSL 기호화된 링크) 또는 메타데이터를 사용하는 경우 fifos 및 소켓을 이제 Windows에서 복사하여 이동할 수 있습니다.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>wsl.conf를 사용하여 보다 유연하게 WSL 구성 가능
하위 시스템을 시작할 때마다 적용되는 WSL의 특정 기능을 자동으로 구성하는 방법이 추가되었습니다. 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함됩니다. 블로그 게시물 https://aka.ms/wslconf 에서 자세히 알아보세요.

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX를 사용하면 WSL의 Linux 프로세스와 Windows 네이티브 프로세스 간에 소켓 연결이 가능합니다.
WSL 및 Windows 애플리케이션은 이제 Unix 소켓을 통해 서로 통신할 수 있습니다. Windows에서 서비스를 실행하고 Windows 및 WSL 앱 모두에서 이 서비스를 제공하려 한다고 가정해 보겠습니다. 이제 Unix 소켓을 사용하면 가능합니다. 블로그 게시물 https://aka.ms/afunixinterop 에서 자세히 알아보세요.

### <a name="wsl"></a>WSL
* MAP_NORESERVE를 통해 mmap() 지원 [GH 121, 2784]
* CLONE_PTRACE 및 CLONE_UNTRACED 지원 [GH 121, 2781]
* 복제 시 비-SIGCHLD 종료 신호 처리 [GH 121, 2781]
* /proc/sys/fs/inotify/max_user_instances 및 /proc/sys/fs/inotify/max_user_watches를 스텁합니다. [GH 1705]
* 0이 아닌 오프셋이 있는 로드 헤더가 포함된 ELF 이진 파일을 로드하는 동안 오류 발생 [GH 1884]
* 이미지를 로드할 때 후행 페이지 바이트 삭제
* execve가 자동으로 프로세스를 종료하는 사례 감소

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17083"></a>빌드 17083
빌드 17083에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)를 참조하세요.

### <a name="wsl"></a>WSL
* epoll 관련 버그 검사 수정 [GH 2798, 2801, 2857]
* ASLR을 끄면 중단되는 문제 해결 [GH 1185, 2870]
* mmap 작업이 원자성으로 표시되는지 확인 [GH 2732]

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17074"></a>빌드 17074
빌드 17074에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)를 참조하세요.

### <a name="wsl"></a>WSL
* DrvFs 메타데이터의 스토리지 형식 수정 [GH 2777] </br>
**중요:** 이 빌드 전에 만들어진 DrvFs 메타데이터는 잘못 표시되거나 전혀 표시되지 않습니다. 영향을 받는 파일을 수정하려면 chmod 및 chown을 사용하여 메타데이터를 다시 적용합니다.
* 여러 신호 및 다시 시작 가능한 syscall 관련 이슈 해결

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17063"></a>빌드 17063
빌드 17063에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)를 참조하세요.

### <a name="wsl"></a>WSL
* DrvFs는 추가 Linux 메타데이터를 지원합니다. 따라서 chmod/chown을 사용하여 파일의 소유자와 모드를 설정할 수 있으며, fifos, unix 소켓, 디바이스 파일 등의 특수 파일을 만들 수 있습니다. 이 기능은 아직 실험 중이므로 지금은 기본적으로 사용되지 않습니다.
**참고:**  DrvFs에서 사용하는 메타데이터 형식의 버그를 수정했습니다. 메타데이터는 이 빌드에서 실험에 사용되지만, 향후 빌드는 이 빌드에서 생성된 메타데이터를 올바르게 읽을 수 없습니다.  수정된 파일의 소유자를 수동으로 업데이트하고 사용자 지정 디바이스 ID를 사용하는 디바이스를 다시 만들어야 할 수도 있습니다.

  DrvFs를 사용하려면 다음과 같이 메타데이터 옵션으로 DrvFs를 탑재합니다(기존 탑재에서 DrvFs를 사용하려면 먼저 DrvFs를 분리해야 함).

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 권한은 파일에 추가 메타데이터로 추가되며, Windows 권한에 영향을 주지 않습니다.  Windows 편집기를 사용하여 파일을 편집하면 메타데이터가 제거될 수 있습니다. 이 경우 파일이 기본 권한으로 되돌아갑니다.

* 메타데이터를 사용하지 않고 파일을 제어하는 탑재 옵션이 DrvFs에 추가되었습니다.
  * uid: 모든 파일의 소유자에게 사용되는 사용자 ID입니다.
  * gid: 모든 파일의 소유자에게 사용되는 그룹 ID입니다.
  * umask: 모든 파일과 디렉터리에서 제외할 권한의 8진수 마스크입니다.
  * fmask: 모든 일반 파일에서 제외할 권한의 8진수 마스크입니다.
  * dmask: 모든 디렉터리에서 제외할 권한의 8진수 마스크입니다.

  예를 들어 다음과 같은 가치를 제공해야 합니다.
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  메타데이터 없이 파일에 대한 기본 권한을 지정하려면 메타데이터 옵션과 결합합니다.

* WSL과 Win32 간에 환경 변수가 어떻게 흐르는지 구성하는 새 환경 변수 `WSLENV`가 도입되었습니다.

  예를 들어 다음과 같은 가치를 제공해야 합니다.

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`는 WSL의 Win32 또는 Win32 프로세스에서 WSL 프로세스를 시작할 때 포함할 수 있는 콜론으로 구분된 환경 변수 목록입니다.  각 변수에 슬래시를 접미사로 붙이고 그 뒤에 플래그를 사용하여 변환 방식을 지정할 수 있습니다.
  * p: 이 값은 WSL 경로와 Win32 경로 간에 변환해야 하는 경로입니다.
  * l: 이 값은 경로 목록입니다. WSL에서는 콜론으로 구분된 목록입니다. Win32에서는 세미콜론으로 구분된 목록입니다.
  * u: 이 값은 Win32에서 WSL을 호출할 때만 포함되어야 합니다.
  * w: 이 값은 WSL에서 Win32를 호출할 때만 포함되어야 합니다.

  .bashrc 또는 사용자 지정 Windows 환경에서 사용자에 대한 `WSLENV`를 설정할 수 있습니다.

* drvfs 탑재는 tar, cp-p의 타임스탬프를 올바르게 유지합니다. (GH 1939)
* drvfs symlink는 올바른 크기를 보고합니다. (GH 2641)
* 매우 큰 IO 크기에 대한 읽기/쓰기가 작동합니다. (GH 2653)
* waitpid는 프로세스 그룹 ID와 함께 작동합니다. (GH 2534)
* 큰 예약 영역에 대한 mmap 성능이 크게 향상되었습니다. ghc 성능이 향상됩니다. (GH 1671)
* 퍼스낼리티에서 READ_IMPLIES_EXEC를 지원합니다. maxima 및 clisp를 수정합니다. (GH 1185)
* mprotect에서 PROT_GROWSDOWN을 지원합니다. clisp를 수정합니다. (GH 1128)
* 오버커밋 모드의 페이지 오류를 수정합니다. sbcl을 수정합니다. (GH 1128)
* 복제에서 더 많은 플래그 조합을 지원합니다.
* epoll 파일의 select/epoll을 지원합니다(이전에는 no-op).
* ptrace에 구현되지 않은 syscall을 알립니다.
* resolv.conf 이름 서버를 생성할 때 작동하지 않는 인터페이스를 무시합니다. [GH 2694]
* 실제 주소가 없는 네트워크 인터페이스를 열거합니다. [GH 2685]
* 추가로 버그를 수정하고 기능을 개선했습니다.

### <a name="linux-tools-available-to-developers-on-windows"></a>Windows 기반 개발자가 사용할 수 있는 Linux 도구

* Windows 명령줄 도구 체인에는 bsdtar(tar) 및 curl이 포함되어 있습니다.
  이 [블로그](https://aka.ms/tarcurlwindows)를 읽고 새로 추가된 이 두 가지 도구에 대해 자세히 살펴보고 두 도구가 Windows에서 어떤 개발자 환경을 제공하는지 알아보세요.

*   `AF_UNIX`는 Windows 참가자 SDK(17061+)에서 사용할 수 있습니다.
  이 [블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)를 읽고 `AF_UNIX`에 대해 자세히 살펴보고 Windows 기반의 개발자가 어떻게 사용할 수 있는지 알아보세요.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.


## <a name="build-17046"></a>빌드 17046

빌드 17046에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)를 참조하세요.

### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 활성 터미널 없이 프로세스를 실행할 수 있습니다. [GH 709, 1007, 1511, 2252, 2391 등]
- CLONE_VFORK 및 CLONE_VM에 대한 지원이 향상되었습니다. [GH 1878, 2615]
- WSL 네트워킹 작업을 위한 TDI 필터 드라이버를 건너뜁니다. [GH 1554]
- 특정 조건이 충족되면 DrvFs에서 NT symlink를 만듭니다. [GH 353, 1475, 2602]
    - 연결 대상은 상대 경로여야 하고, 탑재 지점이나 symlink와 교차해서는 안 되며, 존재해야 합니다.
    - 개발자 모드가 켜져 있지 않으면 사용자에게 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE가 있어야 합니다(일반적으로 관리자 권한으로 wsl.exe를 실행해야 함).
    - 그 외의 상황에서는 DrvFs가 여전히 WSL symlink를 만듭니다.
- 관리자 권한 및 비관리자 권한 WSL 인스턴스를 동시에 실행할 수 있습니다.
- /proc/sys/kernel/yama/ptrace_scope를 지원합니다.
- WSL<->Windows 경로를 변환하는 wslpath가 추가됩니다. [GH 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>콘솔
- 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.


## <a name="build-17040"></a>빌드 17040

빌드 17040에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 17035 이후로는 수정 사항이 없습니다.

#### <a name="console"></a>콘솔
- 17035 이후로는 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17035"></a>빌드 17035

빌드 17035에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- DrvFs의 파일에 액세스할 때 가끔 EINVAL과 함께 액세스가 실패할 수 있습니다. [GH 2448]

#### <a name="console"></a>콘솔
- VT 모드에서 줄을 삽입/삭제할 때 일부 색이 손실됩니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17025"></a>빌드 17025

빌드 17025에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 새 포그라운드 프로세스 그룹에서 초기 프로세스를 시작합니다. [GH 1653, 2510]
- SIGHUP 전송 픽스 [GH 2496]
- 제공된 이름이 없으면 기본 가상 브리지 이름을 생성합니다. [GH 2497]
- /proc/sys/kernel/random/boot_id를 구현합니다. [GH 2518]
- 더 많은 interop stdout/stderr 파이프 픽스를 제공합니다.
- syncfs 시스템 호출을 스텁합니다.

#### <a name="console"></a>콘솔
- 타사 콘솔에 대한 입력 VT 변환을 수정합니다. [GH 111]

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17017"></a>빌드 17017

빌드 17017에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 빈 ELF 프로그램 헤더를 무시합니다. [GH 330]
- LxssManager가 비 대화형 사용자에 대한 WSL 인스턴스를 만들도록 허용합니다(ssh 및 예약된 작업 지원). [GH 777, 1602]
- WSL->Win32>WSL("개시") 시나리오를 지원합니다. [GH 1228]
- Interop를 통해 호출되는 콘솔 앱의 종료를 제한적으로 지원합니다. [GH 1614]
- devpts에 대한 탑재 옵션을 지원합니다. [GH 1948]
- Ptrace가 자식 시작을 차단합니다. [GH 2333]
- EPOLLET에 일부 이벤트가 없습니다. [GH 2462]
- PTRACE_GETSIGINFO에 대한 더 많은 데이터를 반환합니다.
- lseek를 사용하는 Getdents가 잘못된 결과를 제공합니다.
- 일부 Win32 interop 앱이 중단되고, 더 이상 데이터가 없는 파이프에서 입력을 기다립니다.
- tty/pty 파일에 O_ASYNC가 지원됩니다.
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>빌드 16288

빌드 16288에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 소켓 파일 설명자에 대한 uid, gid 및 모드를 올바르게 초기화하고 보고합니다. [GH 2490]
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후로 변경된 내용이 없습니다.

## <a name="build-16278"></a>빌드 16278

빌드 162738에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- LX MM 상태를 해제할 때 파일 지원 섹션의 매핑된 보기를 명시적으로 매핑 해제합니다. [GH 2415]
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후로 변경된 내용이 없습니다.

## <a name="build-16275"></a>빌드 16275

빌드 162735에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후로 변경된 내용이 없습니다.

## <a name="build-16273"></a>빌드 16273

빌드 16273에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- DrvFs에서 가끔 디렉터리의 파일 형식을 잘못 보고하는 이슈가 해결되었습니다. [GH 2392]
- uevent를 사용하는 프로그램의 차단을 해제하는 NETLINK_KOBJECT_UEVENT 소켓을 만들 수 있습니다. [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- 비차단 연결에 대한 지원이 추가되었습니다. [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- CLONE_FS 복제 시스템 호출 플래그를 구현했습니다. [GH 2242]
- NT interop에서 탭 또는 따옴표를 올바르게 처리하지 않는 이슈를 해결했습니다. [GH 1625, 2164]
- WSL 인스턴스를 다시 시작하려고 할 때 발생하는 액세스 거부 오류를 해결했습니다. [GH 651, 2095]
- futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업을 구현했습니다. [GH 2242]
- 다양한 SysFs 파일에 대한 권한을 수정했습니다. [GH 2214]
- 설치하는 동안 Haskell 스택이 중단되는 오류를 수정했습니다. [GH 2290]
- binfmt_misc 'C' 'O' 및 'P' 플래그를 구현했습니다. [GH 2103]
- /proc/sys/kernel /shmmax /shmmni 및 /threads-max를 추가했습니다. [GH 1753]
- ioprio_set 시스템 호출에 대한 부분 지원을 추가했습니다. [GH 498]
- SO_REUSEPORT를 스텁하고 netlink 소켓에 대한 SO_PASSCRED 지원이 추가되었습니다. [GH 69]
- 현재 배포판을 설치 중이거나 제거 중일 때 RegisterDistribuiton에서 다른 오류 코드를 반환합니다.
- wslconfig.exe를 통해 부분적으로 설치된 WSL 배포판을 등록 취소할 수 있습니다.
- udp::msg_peek에서 python 소켓 테스트가 중단되는 오류를 수정했습니다.
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
총 테스트: 1904<br/>
건너뛴 총 테스트: 209<br/>
총 실패 횟수: 229<br/>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>빌드 16257

빌드 16257에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- prlimit64 시스템 호출을 구현했습니다.
- ulimit -n에 대한 지원이 추가되었습니다(setrlimit RLIMIT_NOFILE). [GH 1688]
- TCP 소켓에 대한 MSG_MORE를 스텁합니다. [GH 2351]
- 잘못된 AT_EXECFN 보조 벡터 동작을 수정합니다. [GH 2133]
- 콘솔/tty의 복사/붙여넣기 동작을 수정하고, 보다 효율적인 전체 버퍼 처리를 추가합니다. [GH 2204, 2131]
- set-user-ID 및 set-group-ID 프로그램의 보조 벡터에서 AT_SECURE를 설정합니다. [GH 2031]
- Psuedo-terminal 마스터 엔드포인트에서 TIOCPGRP를 처리하지 않습니다. [GH 1063]
- lseek가 LxFs의 디렉터리를 되감는 오류를 수정했습니다. [GH 2310]
- 사용량이 많은 후 /dev/ptmx가 잠깁니다. [GH 1882]
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 모든 곳에서 가로 선/밑줄을 수정했습니다. [GH 2168]
- 프로세스 순서가 변경되면 NPM을 닫기 어려워지는 문제를 수정했습니다. [GH 2170]
- 새로운 색 구성표를 추가했습니다(https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/ ).

### <a name="ltp-results"></a>LTP 결과:
16251 이후로 변경된 내용이 없습니다.

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`prlimit64`<br/>

### <a name="known-issues"></a>알려진 문제
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub 이슈 2392: WSL에서 Windows 폴더를 인식할 수 없음...](https://github.com/Microsoft/BashOnWindows/issues/2392)
빌드 16257의 경우 WSL에서 `/mnt/c/...` 명령을 통해 Windows 파일/폴더를 열거할 때 이슈가 있습니다.
이 이슈가 해결되었으며, 2017년 8월 14일부터 일주일 동안 참가자 빌드에서 릴리스해야 합니다.

<br/>

## <a name="build-16251"></a>빌드 16251

빌드 16251에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- WSL 선택적 구성 요소에서 베타 태그를 제거했습니다. 자세한 내용은 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)을 참조하세요.
- exec의 set-user-ID 및 set-group-ID 이진 파일에 대한 saved-set uid 및 gid를 올바르게 초기화합니다. [GH 962, 1415, 2072]
- ptrace PTRACE_O_TRACEEXIT에 대한 지원이 추가되었습니다. [GH 555]
- NT_FPREGSET를 사용하는 ptrace PTRACE_GETFPREGS 및 PTRACE_GETREGSET에 대한 지원이 추가되었습니다. [GH 555]
- 무시된 신호에서 중지하도록 ptrace를 수정했습니다.
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 768</br>
실패한 테스트 수: 244</br>
건너뛴 테스트 수: 96</br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>빌드 16241

빌드 16241에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.

#### <a name="console"></a>콘솔
- 교차 줄 DEC에 대해 잘못된 문자를 출력하는 문제가 해결되었으며, 이 문제는 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)에 처음 보고되었습니다.
- 코드 페이지 65001(utf8)에 출력 텍스트가 표시되지 않는 문제를 해결했습니다.
- 선택 변경 시 한 색의 RGB 값에 적용한 변경 내용을 색상표의 다른 부분으로 전송하지 마세요. 이렇게 하면 콘솔 속성 시트를 훨씬 쉽게 사용할 수 있습니다.
- Ctrl+S가 제대로 작동하지 않는 것 같습니다.
- ANSI 이스케이프 코드에서 Un-Bold/-Dim이 완전히 없어졌습니다. [GH 2174]
- 콘솔이 Vim 컬러 테마를 올바르게 지원하지 않습니다. [GH 1706]
- 특정 문자를 붙여넣을 수 없습니다. [GH 2149]
- 항목이 편집/명령줄에 있는 경우 재배치 크기 조정이 bash 창 크기 조정과 이상하게 상호 작용합니다. [GH ConEmu 1123]
- Ctrl-L 키를 누르면 화면이 더티 상태로 유지됩니다. [GH 1978]
- HDPI에서 VT를 표시할 때 콘솔 렌더링 버그가 있습니다. [GH 1907]
- 유니코드 문자 U+30FB를 사용할 때 일본어 문자가 이상하게 보입니다. [GH 2146]
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

</br>

## <a name="build-16237"></a>빌드 16237

빌드 16237에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- lxfs에서 EA가 없는 파일에는 기본 특성을 사용합니다(root, root, 0000).
- 확장된 특성을 사용하는 배포에 대한 지원이 추가되었습니다.
- getdents 및 getdents64에서 반환된 항목의 여백이 수정되었습니다.
- shmctl SHM_STAT 시스템 호출에 대한 권한 확인이 수정되었습니다. [GH 2068]
- ttys에 대한 잘못된 초기 epoll 상태가 수정되었습니다. [GH 2231]
- DrvFs readdir이 일부 항목을 반환하지 않는 문제가 수정되었습니다. [GH 2077]
- 파일의 연결이 끊어질 때 발생하는 LxFs readdir 문제가 수정되었습니다. [GH 2077]
- 연결되지 않은 drvfs 파일을 procfs를 통해 다시 열 수 있습니다.
- WSL 기능을 사용하지 않도록 설정하기 위한 글로벌 레지스트리 키 재정의가 추가되었습니다(interop/드라이브 탑재).
- DrvFs(및 LxFs)에 대한 "통계"의 잘못된 블록 수를 수정했습니다. [GH 1894]
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

</br>

## <a name="build-16232"></a>빌드 16232

빌드 16232에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.

</br>

## <a name="build-16226"></a>빌드 16226

빌드 16226에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- xattr 관련 syscall 지원이 추가되었습니다(getxattr, setxattr, listxattr, removexattr).
- security.capablity xattr 지원이 추가되었습니다.
- 비-MS SMB 서버를 비롯한 특정 파일 시스템 및 필터와의 호환성이 향상되었습니다. [GH #1952]
- OneDrive 자리 표시자, GVFS 자리 표시자 및 컴팩트 OS 압축 파일에 대한 지원이 향상되었습니다.
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

</br>

## <a name="build-16215"></a>빌드 16215

빌드 16215에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- WSL에서 더 이상 개발자 모드를 요구하지 않습니다.
- drvfs에서 디렉터리 연결을 지원합니다.
- WSL 배포 appx 패키지의 제거를 처리합니다.
- 프라이빗 및 공유 매핑을 표시하도록 procfs를 업데이트합니다.
- 부분적으로 설치 또는 제거된 배포판을 정리하는 wslconfig.exe 기능을 추가합니다.
- TCP 소켓에 대한 IP_MTU_DISCOVER 지원이 추가되었습니다. [GH 1639, 2115, 2205]
- AF_INADDR 경로에 대한 프로토콜 패밀리를 유추합니다.
- 직렬 디바이스가 개선되었습니다. [GH 1929]

</br>

## <a name="build-16199"></a>빌드 16199

빌드 16199에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.

</br>

## <a name="build-16193"></a>빌드 16193

빌드 16193에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- SIGCONT 전송과 threadgroup 종료 간의 경합 상태 [GH 1973]
- FILE_DEVICE_CONSOLE 대신 FILE_DEVICE_NAMED_PIPE를 보고하도록 tty 및 pty 디바이스를 변경합니다. [GH 1840]
- IP_OPTIONS에 대한 SSH 픽스
- DrvFs 탑재를 Init daemon으로 이동했습니다. [GH 1862, 1968, 1767, 1933]
- DrvFs에 다음 NT symlink에 대한 지원이 추가되었습니다.

</br>

## <a name="build-16184"></a>빌드 16184

빌드 16184에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- apt 패키지 유지 관리 작업(lxrun.exe/update)을 제거했습니다.
- node.js의 Windows 프로세스에서 출력이 표시되지 않는 문제를 해결했습니다. [GH 1840]
- lxcore의 맞춤 요구 사항이 완화됩니다. [GH 1794]
- 여러 시스템 호출에서 AT_EMPTY_PATH 플래그 처리가 수정되었습니다.
- 열린 핸들로 DrvFs 파일을 삭제하면 파일이 정의되지 않은 동작을 보이는 이슈가 수정되었습니다. [GH 544,966,1357,1535,1615]
- 이제 /etc/hosts는 Windows 호스트 파일(%windir%\system32\drivers\etc\hosts)의 항목을 상속합니다. [GH 1495]

</br>

## <a name="build-16179"></a>빌드 16179

빌드 16179에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 이번 주에는 WSL이 변경되지 않았습니다.

</br>

## <a name="build-16176"></a>빌드 16176

빌드 16176에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- [직렬 지원을 사용합니다.](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- IP 소켓 옵션 IP_OPTIONS가 추가되었습니다. [GH 1116]
- pwritev 함수를 구현했습니다(파일을 nginx/PHP-FPM으로 업로드하는 동안). [GH 1506]
- IP 소켓 옵션 IP_MULTICAST_IF 및 IPV6_MULTICAST_IF가 추가되었습니다. [GH 990]
- 소켓 옵션 IP_MULTICAST_LOOP 및 IPV6_MULTICAST_LOOP에 대한 지원이 추가되었습니다. [GH 1678]
- 앱 노드, traceroute, dig, nslookup, host에 대한 IP(V6)_MTU 소켓 옵션이 추가되었습니다.
- IP 소켓 옵션 IPV6_UNICAST_HOPS가 추가되었습니다.
- [파일 시스템이 향상되었습니다.](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * UNC 경로 탑재 허용
    * drvfs에서 CDFS 지원 사용
    * drvfs의 네트워크 파일 시스템에 대한 권한을 올바르게 처리
    * drvfs에 원격 드라이브에 대한 지원 추가
    * drvfs에서 FAT 지원 사용
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과
15042 이후에는 변경된 내용이 없습니다.

</br>

## <a name="build-16170"></a>빌드 16170

빌드 16170에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)를 참조하세요.<br/>

WSL 테스트에 대해 설명하는 새로운 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)을 발표했습니다.

### <a name="fixed"></a>고정

- 소켓 옵션 IP_ADD_MEMBERSHIP 및 IPV6_ADD_MEMBERSHIP를 지원합니다. [GH 1678]
- PTRACE_OLDSETOPTIONS에 대한 지원이 추가되었습니다. [GH 1692]
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과
15042 이후에는 변경된 내용이 없습니다.

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>빌드 15046에서 Windows 10 크리에이터스 업데이트로 변경
Windows 10 크리에이터스 업데이트에 포함하기로 계획된 WSL 수정 사항 또는 기능이 더 이상 없습니다. WSL 릴리스 정보는 그 다음 주요 Windows 업데이트를 대상으로 하는 추가 기능을 위해 향후 몇 주 이내에 다시 시작될 예정입니다. 빌드 15046 및 향후 참가자 릴리스에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)를 참조하세요. <br/><br/>
 <br/>

## <a name="build-15042"></a>빌드 15042

빌드 15042에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- "..."로 끝나는 경로를 제거할 때 발생하는 교착 상태를 해결했습니다.
- 성공 시 FIONBIO에서 0을 반환하지 않는 이슈를 해결했습니다. [GH 1683]
- inet 데이터 그램 소켓의 길이가 0인 읽기와 관련된 이슈를 해결했습니다.
- drvfs inode lookup의 경합 상태 때문에 발생 가능한 교착 상태를 수정했습니다. [GH 1675]
- unix 소켓 보조 데이터에 대한 지원이 확장되었습니다(SCM_CREDENTIALS 및 SCM_RIGHTS). [GH 514, 613, 1326]
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 737</br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 255

</br>

## <a name="build-15031"></a>빌드 15031

빌드 15031에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- 시간(2)이 우발적으로 오작동하는 버그를 수정했습니다.
- *SIGPROCMASK syscall이 신호 마스크를 손상시킬 수 있는 이슈를 해결했습니다.
- 이제 WSL 프로세스 만들기 알림에서 전체 명령줄 길이를 반환합니다. [GH 1632]
- 이제 WSL은 GDB 정지에 대해 ptrace를 통해 스레드 종료를 보고합니다. [GH 1196]
- 많은 tmux IO 후에 ptys가 중단되는 버그를 수정했습니다. [GH 1358]
- 여러 시스템 호출(futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)의 시간 제한 유효성 검사를 수정했습니다.
- eventfd EFD_SEMAPHORE 지원이 추가되었습니다. [GH 452]
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 737</br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>빌드 15025

빌드 15025에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- grep 2.27을 손상시킨 버그를 수정했습니다. [GH 1578]
- eventfd2 syscall에 대한 EFD_SEMAPHORE 플래그를 구현했습니다. [GH 452]
- /proc/[pid]/net/ipv6_route를 구현했습니다. [GH 1608]
- unix 스트림 소켓에 대한 신호 구동 IO 지원이 추가되었습니다. [GH 393, 68]
- F_GETPIPE_SZ 및 F_SETPIPE_SZ를 지원합니다. [GH 1012]
- recvmmsg() syscall을 구현했습니다. [GH 1531]
- epoll_wait()가 대기하지 않는 버그를 수정했습니다. [GH 1609]
- /proc/version_signature를 구현했습니다.
- 두 파일 설명자가 같은 파이프를 참조하는 경우 이제 syscall에서 오류를 반환합니다.
- Unix 소켓에 대한 SO_PEERCRED의 올바른 동작을 구현했습니다.
- tkill syscall 잘못된 매개 변수 처리를 수정했습니다.
- drvfs의 성능을 높이기 위한 변경 작업을 수행했습니다.
- Ruby IO 차단에 대한 사소한 수정 사항이 있습니다.
- recvmsg()에서 inet 소켓의 MSG_DONTWAIT 플래그에 대해 EINVAL을 반환하는 문제를 수정했습니다. [GH 1296]
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 732</br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>빌드 15019

빌드 15019에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- htop 같은 도구에 대한 procfs에서 CPU 사용량을 잘못 보고하는 버그가 수정되었습니다. (GH 823, 945, 971)
- 기존 파일에서 O_TRUNC를 사용하여 open()을 호출하면 이제 inotify가 IN_MODIFY를 IN_OPEN보다 먼저 생성합니다.
- postgress를 사용하도록 unix 소켓 getsockopt SO_ERROR가 수정되었습니다. [GH 61, 1354]
- GO 언어에 대한 /proc/sys/net/core/somaxconn이 구현되었습니다.
- 이제 Apt-get 패키지 업데이트 백그라운드 작업이 보기에서 숨겨진 상태로 실행됩니다.
- ipv6 localhost의 범위를 지웁니다(Spring-Framework(Java) 오류).
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 714 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 249 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>빌드 15014

빌드 15014에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- 이제 Ctrl+C가 의도한 대로 작동합니다.
- 이제 htop 및 ps auxw가 올바른 리소스 사용률을 표시합니다. (GH #516)
- 기본적으로 NT 예외를 신호로 변환합니다. (GH #513)
- 이제 공간이 부족하면 fallocate가 EINVAL 대신 ENOSPC와 함께 실패합니다. (GH #1571)
- /proc/sys/kernel/sem이 추가되었습니다.
- semop 및 semtimedop 시스템 호출이 구현되었습니다.
- IP_RECVTOS & IPV6_RECVTCLASS 소켓 옵션을 사용하여 nslookup 오류를 수정했습니다. (GH 69)
- 소켓 옵션 IP_RECVTTL 및 IPV6_RECVHOPLIMIT에 대한 지원이 추가되었습니다.
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 709 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 요약
총 Syscall: 384 </br>
총 구현: 235 </br>
총 스텁: 22 </br>
총 미구현: 127 </br>
[자세한 분석](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>빌드 15007

빌드 15007에 대한 일반적인 Windows 정보는 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)를 참조하세요.<br/>


### <a name="known-issue"></a>알려진 이슈

- 콘솔에서 일부 Ctrl + <key> 입력을 인식하지 못하는 알려진 버그가 있습니다.  여기에는 일반적인 'c' 키누름 역할을 하는 ctrl-c 명령이 포함됩니다.

  - 해결 방법: 대체 키를 Ctrl+C에 매핑합니다. 예를 들어 Ctrl+K를 Ctrl+C에 매핑하려면 `stty intr \^k`를 사용합니다.  이 매핑은 터미널 단위로 수행되며 bash가 시작될 *때마다* 수행해야 합니다. 사용자는 옵션을 살펴보고 `.bashrc`에 포함시킬 수 있습니다.

### <a name="fixed"></a>고정

- WSL을 실행하면 CPU 코어를 100% 사용하는 이슈를 해결했습니다.
- 소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO가 이제 지원됩니다. (GH #851, 987)
- lxcore에서 네트워크 인터페이스 실제 주소를 16바이트로 자릅니다. (GH #1452, 1414, 1343, 468, 308)
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 709 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>빌드 15002

빌드 15002에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)를 참조하세요.<br/>


### <a name="known-issue"></a>알려진 이슈

알려진 두 가지 이슈:
- 콘솔에서 일부 Ctrl + <key> 입력을 인식하지 못하는 알려진 버그가 있습니다.  여기에는 일반적인 'c' 키누름 역할을 하는 ctrl-c 명령이 포함됩니다.

  - 해결 방법: 대체 키를 Ctrl+C에 매핑합니다. 예를 들어 Ctrl+K를 Ctrl+C에 매핑하려면 `stty intr \^k`를 사용합니다.  이 매핑은 터미널 단위로 수행되며 bash가 시작될 *때마다* 수행해야 합니다. 사용자는 옵션을 살펴보고 `.bashrc`에 포함시킬 수 있습니다.

- WSL이 실행되는 동안 시스템 스레드에서 CPU 코어를 100% 사용합니다.  내부적으로 근본 원인을 찾아 해결했습니다.

### <a name="fixed"></a>고정

- 이제 모든 bash 세션을 동일한 권한 수준에서 만들어야 합니다.  다른 수준에서 세션을 시작하려고 하면 차단됩니다.  즉, 관리자 콘솔과 비관리자 콘솔을 동시에 실행할 수 없습니다. (GH #626)
<br/>
- 다음 NETLINK_ROUTE 메시지를 구현했습니다(Windows 관리자 필요).
     - RTM_NEWADDR(`ip addr add` 지원)
     - RTM_NEWROUTE(`ip route add` 지원)
     - RTM_DELADDR(`ip addr del` 지원)
     - RTM_DELROUTE(`ip route del` 지원)
- 업데이트할 패키지의 예약된 작업 확인이 더 이상 요금제 연결에서 실행되지 않습니다. (GH #1371)
- 파이핑이 중단되는 오류(예: bash -c "ls -alR /" | bash -c "cat")를 수정했습니다. (GH #1214)
- TCP_KEEPCNT 소켓 옵션을 구현했습니다. (GH #843)
- IP_MTU_DISCOVER INET 소켓 옵션을 구현했습니다. (GH #720, 717, 170, 69)
- NT 경로 조회를 사용하여 init에서 NT 이진 파일을 실행하는 레거시 기능을 제거했습니다. (GH #1325)
- 그룹/기타 읽기 액세스(0644)를 허용하도록 /dev/kmsg 모드를 수정했습니다. (GH #1321)
- /proc/sys/kernel/random/uuid를 구현했습니다. (GH #1092)
- 프로세스 시작 시간이 2432년으로 표시되는 오류를 수정했습니다. (GH #974)
- 기본 TERM 환경 변수를 xterm-256color로 전환했습니다. (GH #1446)
- 프로세스 포크 중에 프로세스 커밋이 계산되는 방식이 수정되었습니다. (GH #1286)
- /proc/sys/vm/overcommit_memory를 구현했습니다. (GH #1286)
- /proc/net/route 파일을 구현했습니다. (GH #69)
- 바로 가기 이름이 잘못 번역된 오류를 수정했습니다. (GH #696)
- 프로그램 헤더의 유효성을 잘못 검사하는 elf 구문 분석 논리는 PATH_MAX보다 작거나 같아야 하도록 수정했습니다. (GH #1048)
- procfs, sysfs, cgroupfs 및 binfmtfs에 대한 statfs 콜백을 구현했습니다. (GH #1378)
- 닫히지 않는 AptPackageIndexUpdate 창을 수정했습니다. (GH #1184, GH #1193에서도 설명)
- ASLR 퍼스낼리티 ADDR_NO_RANDOMIZE 지원이 추가되었습니다. (GH #1148, 1128)
- AV 중에 gdb 스택을 적절하게 추적하도록 PTRACE_GETSIGINFO, SIGSEGV를 개선했습니다. (GH #875)
- patchelf 이진 파일에 대한 Elf 구문 분석이 더 이상 실패하지 않습니다. (GH #471)
- VPN DNS가 /etc/resolv.conf로 전파되었습니다. (GH #416, 1350)
- 보다 안정적인 데이터 전송을 위해 TCP 닫기가 향상되었습니다. (GH #610, 616, 1025, 1335)
- 이제 파일을 너무 많이 열었을 때 올바른 오류 코드가 반환됩니다(EMFILE). (GH #1126, 2090)
- 이제 Windows 감사 로그가 프로세스 만들기 감사에서 이미지 이름을 보고합니다.
- 이제 bash 창 내에서 bash.exe를 시작할 때 정상적으로 실패합니다.
- interop가 LxFs 아래의 작업 디렉터리(예: notepad.exe .bashrc)에 액세스할 수 없는 경우에 표시되는 오류 메시지가 추가되었습니다.
- WSL에서 Windows 경로가 잘리는 문제를 해결했습니다.
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 690 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 274 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>빌드 14986

빌드 14986에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- Netlink 및 Pty IOCTL의 버그 검사를 수정했습니다.
- 이제 커널 버전은 Xenial과의 일관성 때문에 4.4.0-43을 보고합니다.
- 이제 입력이 'nul:'로 전달되면 Bash.exe가 시작됩니다. (GH #1259)
- 이제 스레드 ID가 procfs에서 올바르게 보고됩니다. (GH #967)
- 이제 inotify_add_watch()에서 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 플래그가 지원됩니다. (GH #1280)
- timer_create 및 관련 시스템 호출이 구현되었습니다.  따라서 GHC가 지원됩니다. (GH #307)
- ping이 0.000ms 시간을 반환하는 이슈를 해결했습니다. (GH #1296)
- 파일을 너무 많이 열었을 때 올바른 오류 코드가 반환됩니다.
- 인터페이스의 하드웨어 주소가 32바이트인 경우(예: Teredo 인터페이스) 네트워크 인터페이스 데이터에 대한 Netlink 요청이 EINVAL과 함께 실패하는 WSL 이슈를 해결했습니다.
   - Linux "ip" 유틸리티에는 WSL에서 32바이트 하드웨어 주소를 보고하면 충돌하는 버그가 있습니다. 이것은 WSL이 아니라 "ip"의 버그입니다. “ip” 유틸리티는 하드웨어 주소를 인쇄하는 데 사용되는 문자열 버퍼의 길이를 하드 코딩하는데, 이 버퍼가 너무 작아서 32바이트 하드웨어 주소를 인쇄할 수 없습니다.
- 그 외에도 여러 문제를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 669 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>빌드 14971

빌드 14971에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

 - Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.  정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.

### <a name="ltp-results"></a>LTP 결과:
14965에서 변한 것이 없습니다. </br>
통과한 테스트 수: 664 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>빌드 14965

빌드 14965에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- Netlink 소켓 NETLINK_ROUTE 프로토콜의 RTM_GETLINK 및 RTM_GETADDR에 대한 지원이 추가되었습니다. (GH #468)
  - 네트워크 열거에 ifconfig 및 ip 명령을 사용할 수 있습니다.
  - 자세한 내용은 [WSL 네트워킹 블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)에서 찾을 수 있습니다.

- /sbin은 이제 기본적으로 사용자의 경로에 있습니다.
- 이제 NT 사용자 경로가 기본적으로 WSL 경로에 추가됩니다. 즉, Linux 경로에 System32를 추가하지 않고 notepad.exe를 입력할 수 있습니다.
- /proc/sys/kernel/cap_last_cap에 대한 지원이 추가되었습니다.
- 현재 작업 디렉터리에 비 ansi 문자가 포함되어 있으면 이제 WSL에서 NT 이진 파일을 시작할 수 있습니다. (GH #1254)
- 연결되지 않은 unix 스트림 소켓에서 종료할 수 있습니다.
- PR_GET_PDEATHSIG에 대한 지원이 추가되었습니다.
- CLONE_PARENT에 대한 지원이 추가되었습니다.
- 파이핑이 중단되는 오류(예: bash -c "ls -alR /" | bash -c "cat")를 수정했습니다. (GH #1214)
- 현재 터미널에 연결하라는 요청을 처리합니다.
- /proc/<pid>/oom_score_adj를 쓰기 가능으로 표시합니다.
- /sys/fs/cgroup 폴더를 추가합니다.
- sched_setaffinity는 선호도 비트 마스크 수를 반환해야 합니다.
- 인터프리터 경로를 잘못 가정하는 ELF 유효성 검사 논리는 64자 미만이어야 하도록 수정했습니다. (GH #743)
- Open file 설명자는 콘솔 창을 열어 둘 수 있습니다. (GH #1187)
- rename()이 대상 이름에 후행 슬래시를 사용하여 실패하는 오류를 수정했습니다. (GH #1008)
- /proc/net/dev 파일을 구현했습니다.
- 타이머 해상도로 인한 0.000ms ping을 수정했습니다.
- /proc/self/environ을 구현했습니다. (GH #730)
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 664 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>빌드 14959

빌드 14959에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- Windows에 대한 Pico 프로세스 알림이 개선되었습니다.  추가 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)에서 찾을 수 있습니다.
- Windows 상호 운용성 덕분에 안정성이 향상되었습니다.
- EDP(엔터프라이즈 데이터 보호)를 사용하는 경우 bash.exe를 시작할 때 발생하는 0x80070057 오류를 해결했습니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 665 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>빌드 14955

빌드 14955에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)를 참조하세요.<br/>


### <a name="fixed"></a>고정

 - Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.  정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 665 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>빌드 14951

빌드 14951에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)를 참조하세요.<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>새 기능: Windows/Ubuntu 상호 운용성
이제 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.  덕분에 사용자는 이전에는 불가능하던 방식으로 Windows 환경 및 시스템과 상호 작용할 수 있게 되었습니다.  간단한 예제로, 이제 사용자가 다음 명령을 실행할 수 있습니다.

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

자세한 내용은 아래에서 찾을 수 있습니다.

- [Interop에 대한 WSL 팀 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop 설명서](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>고정

- 이제 모든 새 WSL 인스턴스에 대해 Ubuntu 16.04(Xenial)가 설치됩니다.  기존 14.04(Trusty) 인스턴스를 사용하는 사용자는 자동으로 업그레이드되지 않습니다.
- 이제 설치 중에 설정된 로캘이 표시됩니다.
- WSL 프로세스를 파일로 리디렉션하는 기능이 가끔 작동하지 않는 버그를 포함하여 터미널이 개선되었습니다.
- 콘솔 수명은 bash.exe 수명에 연결되어야 합니다.
- 콘솔 창 크기는 버퍼 크기가 아닌 가시 크기를 사용해야 합니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 665 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>빌드 14946

빌드 14946에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- NT 사용자 이름에 공백이나 따옴표가 포함된 사용자에 대한 WSL 사용자 계정을 만들 수 없는 이슈를 해결했습니다. 
- 통계에서 디렉터리의 링크 수로 0을 반환하도록 VolFs 및 DrvFs를 변경합니다.
- IPV6_MULTICAST_HOPS 소켓 옵션을 지원합니다.
- tty당 단일 콘솔 I/O 루프로 제한합니다. 예: 다음 명령을 사용할 수 있습니다.
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- 공백을 /proc/cpuinfo의 탭으로 바꿉니다. (GH #1115)
- 이제 DrvFs는 탑재된 Windows 볼륨과 일치하는 이름으로 mountinfo에 표시됩니다.
- 이제 /home 및 /root가 올바른 이름으로 mountinfo에 표시됩니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 665 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>빌드 14942

빌드 14942에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- SSH를 차단하는 “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” 네트워킹 충돌을 포함하여 여러 버그 검사가 수정되었습니다.
- 현재 DrvFs가 있는 Windows 애플리케이션에서 생성된 알림에 inotifiy가 지원됩니다.
- mongod에 대한 TCP_KEEPIDLE 및 TCP_KEEPINTVL이 구현되었습니다. (GH #695)
- pivot_root 시스템 호출이 구현되었습니다.
- SO_DONTROUTE에 대한 소켓 옵션이 구현되었습니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.


### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 665 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>빌드 14936

빌드 14936에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)를 참조하세요.<br/>


참고: 향후 릴리스에서 WSL은 Ubuntu 14.04(Trusty) 대신 Ubuntu 16.04(Xenial)를 설치할 것입니다.  이 변경 내용은 새 인스턴스를 설치하는(lxrun.exe /install 또는 bash.exe를 처음으로 실행) 참가자에게 적용됩니다.  Trusty를 사용하는 기존 인스턴스는 자동으로 업그레이드되지 않습니다. 사용자는 do-release-upgrade 명령을 사용하여 Trusty 이미지를 Xenial로 업그레이드할 수 있습니다.

### <a name="known-issue"></a>알려진 이슈
WSL에서 일부 소켓 구현에 이슈가 있습니다.  버그 검사는 “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” 오류와 함께 자신을 충돌로 나타냅니다.  이 이슈의 가장 일반적인 징후는 ssh를 사용할 때 발생하는 충돌입니다.  근본 원인은 내부 빌드에서 수정되었으며, 기회가 되는 대로 참가자에게 푸시할 예정입니다.

### <a name="fixed"></a>고정

- chroot 시스템 호출이 구현되었습니다.
- 현재 ~~DrvFs의 Windows 애플리케이션에서 생성된 알림에 대한 지원을 포함하여~~ inotifiy가 개선되었습니다.
  - 수정 사항: Windows 애플리케이션에서 시작된 변경 내용에 대한 Inotify 지원은 현재 제공되지 않습니다.
- IPV6에 대한 소켓 바인딩:<port n> 이제 IPV6_V6ONLY를 지원합니다. (GH #68, #157, #393, #460, #674, #740, #982, #996)
- waitid systemcall에 대한 WNOWAIT 동작이 구현되었습니다. (GH #638)
- IP 소켓 옵션 IP_HDRINCL 및 IP_TTL에 대한 지원이 추가되었습니다.
- 길이가 0인 read()는 즉시 반환되어야 합니다. (GH #975).
- .tar 파일에 NULL 종결자가 포함되지 않은 파일 이름 및 파일 이름 접두사를 올바르게 처리합니다.
- /dev/snull에 epoll이 지원됩니다.
- /dev/alarm 시간 원본이 수정되었습니다.
- 이제 Bash -c가 파일로 리디렉션할 수 있습니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 664 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 264 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>빌드 14931

빌드 14931에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

 - Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.  정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.

<br/>

## <a name="build-14926"></a>빌드 14926

빌드 14926에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정

- 이제 Ping은 관리자 권한이 없는 콘솔에서 작동합니다.
- 이제 Ping6가 지원되며, 관리자 권한이 없습니다.
- WSL을 통해 수정된 파일에 Inotify가 지원됩니다. (GH #216)
  - 지원되는 플래그:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch 이벤트: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 출력 읽기: LX_IN_ISDIR, LX_IN_IGNORED
  - 알려진 이슈: Windows 애플리케이션의 파일을 수정해도 이벤트가 생성되지 않습니다.
- 이제 Unix 소켓이 SCM_CREDENTIALS를 지원합니다.

### <a name="ltp-results"></a>LTP 결과:
통과한 테스트 수: 651 </br>
통과하지 못한 테스트 수(실패, 건너뜀 등): 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>빌드 14915

빌드 14915에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)를 참조하세요.<br/>


### <a name="fixed"></a>고정
-  unix 데이터 그램 소켓용 Socketpair가 제공됩니다. (GH #262)
- SO_REUSEADDR에 Unix 소켓이 지원됩니다.
- SO_BROADCAST에 UNIX 소켓이 지원됩니다. (GH #568)
- SOCK_SEQPACKET에 Unix 소켓이 지원됩니다. (GH #758, #546)
- unix 데이터 그램 전송, 수신 및 종료에 대한 지원이 추가되었습니다.
- 고정되지 않은 주소에 대한 잘못된 mmap 매개 변수 유효성 검사로 인한 버그 검사를 수정했습니다. (GH #847)
- 터미널 상태의 일시 중단/다시 시작을 지원합니다.
- 화면 유틸리티의 차단을 해제하는 TIOCPKT ioctl을 지원합니다. (GH #774)
    - 알려진 이슈: 기능 키가 작동하지 않습니다.
- 해제된 멤버 'ReaderReady'에 LxpTimerFdWorkerRoutine이 액세스할 수 있게 되는 원인인 TimerFd의 경합을 수정했습니다. (GH #814)
- futex, poll 및 clock_nanosleep에 대한 다시 시작 가능한 시스템 호출을 지원합니다.
- 바인드 탑재 지원이 추가되었습니다.
- 탑재 네임스페이스 지원에 대한 공유가 해제되었습니다.
    - 알려진 이슈: `unshare(CLONE_NEWNS)`를 사용하여 새 탑재 네임스페이스를 만들 때 현재 작업 디렉터리는 이전 네임스페이스를 계속 가리킵니다.
- 추가적으로 기능이 개선되고 버그가 수정되었습니다.

<br/>

## <a name="build-14905"></a>빌드 14905

빌드 14905에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 다시 시작 가능한 시스템 호출이 이제 지원됩니다. (GH #349, GH #520).
- /로 끝나는 디렉터리에 대한 Symlink가 이제 작동합니다. (GH #650)
- /dev/random에 대한 RNDGETENTCNT ioctl이 구현되었습니다.
- /proc/[pid]/mounts, /proc/[pid]/mountinfo 및 /proc/[pid]/mountstats 파일이 구현되었습니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

</br>

## <a name="build-14901"></a>빌드 14901
Windows 10 1주년 업데이트 이후에 출시된 첫 번째 참가자 빌드입니다.

빌드 14901에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 후행 슬래시 이슈를 수정했습니다.
    - 이제 `$ mv a/c/ a/b/` 같은 명령이 작동합니다.
- 이제 설치 시 Ubuntu 로캘을 Windows 로캘로 설정해야 하는지 여부를 묻는 메시지가 표시됩니다.
- ns 폴더에 procfs가 지원됩니다.
- tmpfs, procfs 및 sysfs 파일 시스템에 탑재 및 탑재 해제가 추가되었습니다.
- mknod[at] 32비트 ABI 서명이 수정되었습니다.
- Unix 소켓이 디스패치 모델로 전환되었습니다.
- setsockopt를 사용하여 설정된 INET 소켓 수신 버퍼 크기를 준수해야 합니다.
- MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그가 구현되었습니다.
- Linux 프로세스 stdin/stdout 파이프 리디렉션 (GH #2)
    - CMD에서 bash -c 명령을 파이핑할 수 있습니다.  예:  >dir | bash -c "grep foo"
- 이제 여러 개의 페이지 파일이 있는 시스템에 Bash를 설치할 수 있습니다. (GH #538, #358).
- 기본 INET 소켓 버퍼 크기가 기본 Ubuntu 설정의 크기와 일치해야 합니다.
- xattr syscall을 listxattr에 맞춥니다.
- SIOCGIFCONF의 유효한 IPv4 주소가 있는 인터페이스만 반환합니다.
- ptrace에서 삽입할 때 신호 기본 작업을 수정합니다.
- /proc/sys/vm/min_free_kbytes가 구현되었습니다.
- sigreturn에서 컨텍스트를 복원할 때 머신 컨텍스트 레지스터 값을 사용합니다.
    - 이렇게 하면 일부 사용자의 java 및 javac가 중단되는 이슈를 해결할 수 있습니다.
- /proc/sys/kernel/hostname이 구현되었습니다.

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>빌드 14388에서 Windows 10 1주년 업데이트로 전환
빌드 14388에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/14388wip)를 참조하세요. <br/>

### <a name="fixed"></a>고정
- 8월 2일에 Windows 10 1주년 업데이트를 준비하도록 수정되었습니다.
  - 1주년 업데이트의 WSL에 대한 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/wsl/)에서 찾을 수 있습니다.

<br/>

## <a name="build-14376"></a>빌드 14376
빌드 14376에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)를 참조하세요. <br/>

### <a name="fixed"></a>고정
- apt-get이 중단되는 일부 인스턴스를 제거했습니다. (GH #493)
- 빈 탑재가 올바르게 처리되지 않는 이슈를 해결했습니다.
- ramdisks가 올바르게 탑재되지 않는 이슈를 해결했습니다.
- 플래그를 지원하도록 unix 소켓 수용이 변경되었습니다. (부분 GH #451)
- 일반적인 네트워크 관련 블루스크린이 해결되었습니다.
- /proc/[pid]/task에 액세스할 때 블루스크린이 발생하는 문제를 해결했습니다. (GH #523)
- 일부 pty 시나리오에서 CPU 사용률이 높은 문제를 해결했습니다. (GH #488, #504)
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

<br/>

## <a name="build-14371"></a>빌드 14371
빌드 14371에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)를 참조하세요. <br/>

### <a name="fixed"></a>고정
- ptrace를 사용할 때 SIGCHLD 및 wait()를 사용하여 타이밍 경합을 수정했습니다.
- 경로에 후행 /가 있을 때 발생하는 몇 가지 동작을 수정했습니다. (GH #432)
- 자식에 대한 열린 핸들로 인해 이름 바꾸기/연결 해제가 실패하는 이슈를 해결했습니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

<br/>

## <a name="build-14366"></a>빌드 14366
빌드 14366에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)를 참조하세요. <br/>

### <a name="fixed"></a>고정
- symlink를 통한 파일 만들기를 수정했습니다.
-   Python에 대한 listxattr을 추가했습니다. (GH 385)
-   그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="syscall-support"></a>Syscall 지원
-   아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>빌드 14361
빌드 14361에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14361)를 참조하세요. <br/>

### <a name="fixed"></a>고정
- 이제 DrvFs는 Windows 기반의 Ubuntu에서 Bash로 실행될 때 대/소문자를 구분합니다.
  - 사용자는 /mnt/c 드라이브에서 case.txt 및 CASE.TXT를 입력할 수 있습니다.
  - 대/소문자 구분은 Windows 기반 Ubuntu의 Bash 내에서만 지원됩니다. Bash 외부에 있는 경우 NTFS가 파일을 올바르게 보고하지만, 예기치 않은 동작이 발생하여 Windows의 파일과 상호 작용할 수 있습니다.
  - 각 볼륨의 루트(/mnt/c)는 대/소문자를 구분하지 않습니다.
  - Windows에서 이러한 파일을 처리하는 방법에 대한 자세한 내용은 [여기](https://support.microsoft.com/en-us/kb/100625)에서 확인할 수 있습니다.
- pty/tty 지원이 대폭 개선되었습니다.  이제 TMUX 같은 애플리케이션이 지원됩니다. (GH #40)
- 가끔 사용자 계정이 만들어지지 않는 이슈를 해결했습니다.
- 매우 긴 인수 목록을 허용하도록 명령줄 인수 구조를 최적화했습니다. (GH #153)
- 이제 DrvFs의 read_only 파일을 삭제하고 chmod할 수 있습니다.
- 연결이 끊어질 때 터미널이 중단되는 일부 인스턴스를 수정했습니다. (GH #43)
- 이제 chmod 및 chown이 tty 디바이스에서 작동합니다.
- 0\.0.0.0 및 ::에 localhost로 연결할 수 있습니다. (GH #388)
- 이제 Sendmsg/recvmsg는 1보다 큰 IO 벡터 길이를 처리합니다. (부분 GH #376)
- 이제 사용자는 자동 생성된 호스트 파일을 옵트아웃할 수 있습니다. (GH #398)
- 설치하는 동안 자동으로 Linux 로캘을 NT 로캘에 연결합니다. (GH #11)
- /proc/sys/vm/swappiness 파일이 추가되었습니다. (GH #306)
- 이제 strace가 올바르게 종료됩니다.
- /proc/self/fd를 통해 파이프를 다시 열 수 있습니다. (GH #222)
- DrvFs에서 %LOCALAPPDATA%\lxss 아래에 디렉터리를 숨깁니다. (GH #270)
- bash.exe ~를 보다 효율적으로 처리합니다.  이제 “bash ~ -c ls” 같은 명령이 지원됩니다. (GH #467)
- 이제 종료하는 동안 소켓이 epoll 읽기를 사용할 수 있음을 알립니다. (GH #271).
- lxrun /uninstall이 파일 및 폴더 삭제를 보다 효율적으로 수행합니다.
- ps -f를 수정했습니다. (GH #246)
- xEmacs 같은 x11 앱에 대한 지원이 개선되었습니다. (GH #481)
- 기본 Ubuntu 설정과 일치하고 get_rlimit syscall에 올바른 크기를 보고하도록 초기 스레드 스택 크기를 업데이트했습니다. (GH #172, #258)
- pico 프로세스 이미지 이름의 보고 기능을 개선했습니다(예: 감사).
- df 명령에 대한 /proc/mountinfo를 구현했습니다.
- 자식 이름에 대한 symlink 오류 코드를 수정했습니다. 그리고 ...
- 버그 및 기능이 추가로 개선되었습니다.

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>빌드 14352
빌드 14352에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14352)를 참조하세요.<br/>


### <a name="fixed"></a>고정
- 대용량 파일이 올바르게 다운로드/생성되지 않는 이슈를 해결했습니다.  이제 npm 및 기타 시나리오의 차단을 해제해도 됩니다. (GH #3, GH #313)
- 소켓이 중단되는 일부 인스턴스를 제거했습니다.
- 일부 ptrace 오류를 수정했습니다.
- 255자보다 긴 파일 이름을 허용하는 WSL 이슈를 수정했습니다.
- 영어가 아닌 문자에 대한 지원이 개선되었습니다.
- 현재 Windows 표준 시간대 데이터를 추가하고 기본값으로 설정했습니다.
- 각 탑재 지점에 대한 고유한 디바이스 id (jre 픽스 – GH #49)
- "." 및 “..”가 포함된 경로 이슈를 수정했습니다.
- Fifo 지원이 추가되었습니다. (GH #71)
- 네이티브 Ubuntu 형식과 일치하도록 resolv.conf 형식을 업데이트했습니다.
- 일부 procfs를 정리했습니다.
- 관리자 콘솔에 ping을 사용합니다. (GH #18)

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>빌드 14342
빌드 14342에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14342)를 참조하세요. <br/>

VolFs 및 DriveFs에 대한 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl)에서 찾을 수 있습니다. <br/>

### <a name="fixed"></a>고정
- Windows 사용자의 사용자 이름에 유니코드 문자가 있을 때 발생하는 설치 이슈를 해결했습니다.
- 이제 FAQ의 apt-get update udev 해결 방법이 첫 번째 실행 시 기본적으로 제공됩니다.
- DriveFs(/mnt/<drive>) 디렉터리에서 symlink를 사용합니다.
- 이제 symlink가 DriveFs와 VolFs 간에 작동합니다.
- 최상위 경로 구문 분석 이슈를 해결했습니다. 이제 ls .//가 예상대로 작동합니다.
- 이제 DriveFs의 npm 설치와 -g 옵션이 작동합니다.
- PHP 서버가 시작되지 않는 이슈를 해결했습니다.
- 네이티브 Ubuntu와 보다 가깝게 일치하도록 $PATH 같은 기본 환경 변수를 업데이트했습니다.
- apt 패키지 캐시를 업데이트하기 위한 주간 유지 관리 작업이 Windows에 추가되었습니다.
- ELF 헤더 유효성 검사와 관련된 이슈를 해결했습니다. 이제 WSL은 모든 Melkor 옵션을 지원합니다.
- Zsh 셸이 작동합니다.
- 미리 컴파일된 Go 이진 파일이 이제 지원됩니다.
- Bash.exe 첫 실행에 대한 메시지가 이제 올바르게 번역되었습니다.
- 이제 /proc/meminfo에서 올바른 정보를 반환합니다.
- 이제 VFS에서 소켓이 지원됩니다.
- 이제 /dev가 tempfs로 탑재됩니다.
- 이제 Fifo가 지원됩니다.
- 이제 다중 코어 시스템이 /proc/cpuinfo에 올바르게 표시됩니다.
- 첫 번째 실행에서 다운로드와 관련된 기능이 개선되고 오류 메시지가 추가되었습니다.
- Syscall 및 버그 픽스가 개선되었습니다. 아래 syscall 목록이 지원됩니다.
- 그 외에도 여러 버그를 수정하고 기능을 개선했습니다.

### <a name="known-issues"></a>알려진 문제
- 경우에 따라 DriveFs에서 ‘..’가 올바르게 확인되지 않습니다.

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a>빌드 14332

빌드 14332에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14332)를 참조하세요. <br/>


### <a name="fixed"></a>고정
- DNS 항목 우선 순위 지정을 포함하여 resolv.conf 생성이 개선되었습니다.
- /mnt 드라이브와 비-/mnt 드라이브 간에 파일 및 디렉터리를 이동할 때 발생하는 이슈
- 이제 symlink를 사용하여 Tar 파일을 만들 수 있습니다.
- 인스턴스를 만들 때 기본 /run/lock 디렉터리가 추가됩니다.
- 적절한 통계 정보를 반환하도록 /dev/null이 업데이트되었습니다.
- 처음 실행하는 동안 다운로드할 때 추가 오류가 발생합니다.
- Syscall 및 버그 픽스가 개선되었습니다. 아래 syscall 목록이 지원됩니다.
- 버그 및 기능이 추가로 개선되었습니다.

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부가 구현된 새 syscall입니다. 이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>빌드 14328

빌드 14332에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14328)를 참조하세요. <br/>


### <a name="new-features"></a>새로운 기능
* 이제 Linux 사용자를 지원합니다.  Windows 기반의 Ubuntu에 Bash를 설치하면 Linux 사용자를 만들라는 메시지가 표시됩니다.  자세한 내용은 https://aka.ms/wslusers 에서 확인할 수 있습니다.
* 이제 호스트 이름이 Windows 컴퓨터 이름으로 설정됩니다. 더 이상 @localhost는 없습니다.
* 빌드 14328에 대한 자세한 내용은 https://aka.ms/wip14328 에서 확인할 수 있습니다.

### <a name="fixed"></a>고정
* 비 /mnt/<drive> 파일에 대한 Symlink가 개선되었습니다.
    * 이제 npm 설치가 작동합니다.
    * 이제 [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)에 제공된 지침에 따라 jdk/jre를 설치할 수 있습니다.
    * 알려진 이슈: symlink가 Windows 탑재에 대해 작동하지 않습니다.  이 기능은 이후 빌드에서 사용할 수 있습니다.
* 이제 top 및 htop이 표시됩니다.
* 일부 설치 오류에 대한 오류 메시지가 추가되었습니다.
* Syscall 및 버그 픽스가 개선되었습니다.  아래 syscall 목록이 지원됩니다.
* 버그 및 기능이 추가로 개선되었습니다.

### <a name="syscall-support"></a>Syscall 지원
아래는 WSL에서 일부가 구현된 syscall 목록입니다.  이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
