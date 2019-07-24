---
title: Linux 용 Windows 하위 시스템의 릴리스 정보
description: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보입니다.  매주 업데이트 됩니다.
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042429"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템의 릴리스 정보


## <a name="build-18917"></a>빌드 18917
빌드 18917에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 이제 WSL 2를 사용할 수 있습니다. 자세한 내용은 [블로그](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) 를 참조 하세요.
* Symlink를 통한 Windows 프로세스 시작이 올바르게 작동 하지 않는 재발 문제 해결 [GH 3999]
* Wsl .exe--list--verbose, wsl .exe--list--quiet 및 wsl .exe--import--version 옵션을 wsl .exe에 추가 합니다.
* Wsl .exe--shutdown 옵션 추가
* 계획 9: 쓰기에 대 한 디렉터리 열기가 성공 하도록 허용

## <a name="build-18890"></a>빌드 18890
빌드 18890에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 비 블로킹 소켓 누수 [GH 2913]
* 터미널의 EOF 입력은 후속 읽기를 차단할 수 있습니다 [GH 3421]
* Resolv.conf를 참조 하도록 헤더를 업데이트 합니다. [GH 3928]에 설명 되어 있습니다.
* Epoll delete 코드의 교착 상태 [GH 3922]
* 인수에서--import 및 – export에 대 한 공백 처리 [GH 3932]
* Mmap 파일 확장은 제대로 작동 하지 않습니다 [GH 3939]
* ARM64 \\wsl의 문제 해결 $ access가 제대로 작동 하지 않음
* Wsl .exe에 대해 더 나은 기본 아이콘 추가

## <a name="build-18342"></a>빌드 18342
빌드 18342에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 사용자가 Windows에서 WSL 배포판의 Linux 파일에 액세스할 수 있는 기능을 추가 했습니다. 이러한 파일은 명령줄을 통해 액세스할 수 있으며 파일 탐색기, VSCode 등의 Windows 앱 에서도 이러한 파일과 상호 작용할 수 있습니다. Wsl \\$ \\ \\ \\< distro_name >로 이동 하 여 파일에 액세스 하거나 wsl $으로 이동 하 여 실행 중인 배포의 목록을 확인 합니다.\\
* 추가 CPU 정보 태그 추가 및 Cpus_allowed [_list] 값 수정 [GH 2234]
* 비-리더 스레드의 exec 지원 [GH 3800]
* 구성 업데이트 실패를 심각 하지 않은 것으로 처리 [GH 3785]
* 적절 한 오프셋을 적절 하 게 처리 하도록 binfmt 업데이트 [GH 3768]
* 계획 9에 대 한 네트워크 드라이브 매핑 사용 [GH 3854]
* Bind 탑재를 위한 Windows > Linux 및 Linux > Windows 경로 변환 지원
* 읽기 전용으로 열린 파일의 매핑에 대 한 읽기 전용 섹션 만들기

## <a name="build-18334"></a>빌드 18334
빌드 18334에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Windows 표준 시간대가 Linux 표준 시간대에 매핑되는 방식 다시 디자인 [GH 3747]
* 메모리 누수 수정 및 새 문자열 변환 함수 추가 [GH 3746]
* 스레드가 없는 threadgroup의 SIGCONT가 no op [GH 3741] 
* /Proc/self/fd에 소켓 및 epoll 파일 설명자를 올바르게 표시 합니다.

## <a name="build-18305"></a>빌드 18305
빌드 18305에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 주 스레드가 종료 되 면 pthread가 파일에 액세스할 수 없게 됩니다. [GH 3589]
* 필요한 경우가 아니면 TIOCSCTTY는 "force" 매개 변수를 무시 해야 합니다. [GH 3652]
* wsl .exe 명령줄 기능을 개선 하 고 가져오기/내보내기 기능을 추가 합니다.
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
빌드 18277에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 빌드 18272에 도입 된 "해당 인터페이스를 지원 하지 않습니다." 오류 해결 [GH 3645]
* 분리할 syscall에 대 한 MNT_FORCE 플래그 무시 [GH 3605]
* 공식 CreatePseudoConsole API를 사용 하도록 WSL interop 전환
* FUTEX_WAIT를 다시 시작할 때 시간 제한 값을 유지 하지 않습니다.

## <a name="build-18272"></a>빌드 18272
빌드 18272에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* **내용의** 이 빌드에는 WSL이 작동 하지 않는 문제가 있습니다. 배포를 시작 하려고 하면 "해당 인터페이스가 지원 되지 않습니다." 오류가 표시 됩니다. 이 문제는 해결 되었으며 다음 주의 Insider Fast 빌드에 포함 될 예정입니다. 이 빌드를 설치한 경우 설정-> 업데이트 & 보안-> 복구에서 "이전 버전의 Windows 10으로 돌아가기"를 사용 하 여 이전 Windows 빌드로 롤백할 수 있습니다.

## <a name="build-18267"></a>빌드 18267
빌드 18267에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 좀비 프로세스가 reaped 수 없는 문제를 해결 하 고 무기한으로 유지 합니다.
* 오류 메시지가 최대 길이를 초과 하는 경우 WslRegisterDistribution이 중지 됨 [GH 3592]
* DrvFs에서 읽기 전용 파일에 대해 fsync가 성공 하도록 허용 [GH 3556]
* Symlink를 만들기 전에/sbin 및 디렉터리가 존재 하는지 확인 합니다. [GH 3584]
* WSL 인스턴스에 대 한 인스턴스 종료 시간 제한 메커니즘을 추가 했습니다. 현재 시간 제한은 15 초로 설정 되어 있습니다. 즉, 인스턴스는 마지막 WSL 프로세스가 종료 된 후 15 초 후에 종료 됩니다. 배포를 즉시 종료 하려면 다음을 사용 합니다.
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>빌드 17763 (1809)
빌드 17763에 대 한 일반적인 Windows 정보는 [windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Setpriority syscall permission check가 같은 스레드 우선 순위 변경에 대해 너무 엄격 하 게 [GH 1838]
* Clock_gettime (CLOCK_BOOTTIME)에 대해 음수 값을 반환 하지 않도록 하기 위해 비편향 interrupt time이 부팅 시간에 사용 되는지 확인 [GH 3434]
* WSL binfmt 인터프리터의 symlink 처리 [GH 3424]
* Threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리 합니다.
* 오버플로를 방지 하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용 하도록 WSL 전환 [GH 3252]
* Ptrace attach로 인해 시스템 호출에서 잘못 된 반환 값이 발생 하는 경우 [GH 1731]
* 여러 AF_UNIX 관련 문제 해결 [GH 3371]
* 현재 작업 디렉터리가 5 자 미만인 경우 WSL interop가 실패할 수 있는 문제 해결 [GH 3379]
* 존재 하지 않는 포트에 대 한 두 번째 지연 지연의 루프백 연결 방지 [GH 3286]
* ////> 추가/f i d/최대 스텁 파일 추가 [GH 2893]
* 더 정확한 IPV6 범위 정보입니다.
* PR_SET_PTRACER 지원 [GH 3053]
* 파이프 파일 시스템 실수로 edge에서 트리거된 epoll 이벤트 지우기 [GH 3276]
* NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.
* 향상 된 좀비 지원 [GH 1353]
* Windows interop 동작을 제어 하기 위한 wsl. c 항목 추가 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 항상 UNIX 소켓 패밀리 유형을 반환 하지 않는 getsockname에 대 한 수정 [GH 1774]
* TIOCSTI에 대 한 지원 추가 [GH 1863]
* 연결 프로세스의 비차단 소켓이 쓰기 시도에 대해 EAGAIN 반환 되어야 함 [GH 2846]
* 탑재 된 Vhd에 대 한 interop 지원 [GH 3246, 3291]
* 루트 폴더에 대 한 사용 권한 확인 문제 해결 [GH 3304]
* TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대 한 지원이 제한적입니다.
* Windows UI 앱은 백그라운드에서 실행 되는 경우에도 실행 해야 합니다.
* Wsl-u 또는--user 옵션 추가 [GH 1203]
* 빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]
* Unix 소켓이 연결 되지 않은 피어 자격 증명을 유지 해야 하는 경우 [GH 3183]
* 비 블로킹 Unix 소켓이 EAGAIN로 무기한 실패 하는 경우 [GH 3191]
* case = off는 새로운 기본 drvfs 탑재 유형 [GH 2937, 3212, 3328]입니다.
    * 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 를 참조 하세요.
* 배포 실행을 중지 하려면 wslconfig/terminate를 추가 합니다.
* 공백으로 경로를 올바르게 처리 하지 않는 WSL shell 상황에 맞는 메뉴 항목의 문제를 해결 합니다.
* 디렉터리 단위 대/소문자 구분을 확장 특성으로 노출
* ARM64 캐시 유지 관리 작업을 에뮬레이트합니다. [Dotnet 문제](https://github.com/dotnet/core/issues/1561)를 해결 합니다.
* DrvFs: 전용 범위에서 이스케이프 된 문자에 해당 하는 문자만 unescape 합니다.
* ELF 파서 인터프리터 길이 유효성 검사에서 한 번 이상 오류 수정 [GH 3154]
* WSL 과거 시간을 사용한 절대 타이머 [GH 3091]
* 새로 만든 재분석 지점이 부모 디렉터리에 표시 되는지 확인 합니다.
* DrvFs에서 대/소문자를 구분 하는 디렉터리를 원자 단위로 만듭니다.
* 파일이 존재 하더라도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 추가 문제를 수정 했습니다. [GH 2712]
* UMCI를 사용 하는 경우 WSL 시작 실패가 수정 되었습니다. [GH 3020]
* WSL [GH 437, 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다. 를 사용 하려면 shift 키를 누른 상태에서 탐색기 창에서 마우스 오른쪽 단추를 클릭 합니다.
* Unix 소켓이 차단 되지 않는 동작 수정 [GH 2822, 3100]
* GH 2026에 보고 된 대로 NETLINK 명령을 수정 합니다.
* 탑재 전파 플래그에 대 한 지원 추가 [GH 2911].
* Inotify 이벤트를 발생 시 키 지 않는 자르기 문제를 해결 합니다 [GH 2978].
* Wsl .exe를 추가 하 여 셸이 없는 단일 이진 파일을 호출 합니다.
* 특정 배포판를 선택 하기 위해 wsl .exe의 추가--배포 옵션입니다.
* Dmesg에 대 한 지원이 제한적입니다. 이제 응용 프로그램이 dmesg에 로그인 할 수 있습니다. WSL 드라이버는 제한 된 정보를 dmesg로 기록 합니다. 나중에이를 확장 하 여 드라이버에서 다른 정보/진단을 수행할 수 있습니다.
    * 참고: dmesg는 현재 장치 인터페이스를 `/dev/kmsg` 통해 지원 됩니다. `syslog`syscall 인터페이스는 아직 지원 되지 않습니다. 따라서와 `dmesg` `-S`같은 명령줄옵션중일부는작동하지않습니다.`-C`
* 네이티브와 일치 하도록 직렬 장치의 기본 gid 및 모드 변경 [GH 3042]
* DrvFs는 이제 확장 된 특성을 지원 합니다.
    * 참고: DrvFs에는 확장 특성의 이름에 대 한 몇 가지 제한이 있습니다. 일부 문자 (예: '/', ': ' 및\*' ')는 허용 되지 않으며 확장 특성 이름은 DrvFs에서 대/소문자를 구분 하지 않습니다.

## <a name="build-18252-skip-ahead"></a>빌드 18252 (앞으로 건너뛰기)
빌드 18252에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Lxssmanager dll과 별도의 도구 폴더로 init 및 bsdtar 이진 파일을 이동 합니다.
* CLONE_FILES를 사용할 때 파일 설명자를 닫는 동안 경합 해결
* DrvFs 경로를 변환할 때/proc/pid/mountinfo의 선택적 필드를 처리 합니다.
* S_IFREG에 대 한 메타 데이터를 지원 하지 않고 DrvFs mknod가 성공 하도록 허용
* DrvFs에서 만든 읽기 전용 파일에는 readonly 특성 집합이 있어야 합니다. [GH 3411]
* DrvFs 탑재를 처리 하는/sbin/mount.drvfs 도우미 추가
* DrvFs에서 POSIX rename을 사용 합니다.
* 볼륨 GUID가 없는 볼륨에 대 한 경로 변환을 허용 합니다.

## <a name="build-17738-fast"></a>빌드 17738 (빠름)
빌드 17738에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Setpriority syscall permission check가 같은 스레드 우선 순위 변경에 대해 너무 엄격 하 게 [GH 1838]
* Clock_gettime (CLOCK_BOOTTIME)에 대해 음수 값을 반환 하지 않도록 하기 위해 비편향 interrupt time이 부팅 시간에 사용 되는지 확인 [GH 3434]
* WSL binfmt 인터프리터의 symlink 처리 [GH 3424]
* Threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리 합니다.

## <a name="build-17728-fast"></a>빌드 17728 (빠름)
빌드 17728에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 오버플로를 방지 하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용 하도록 WSL 전환 [GH 3252]
* Ptrace attach로 인해 시스템 호출에서 잘못 된 반환 값이 발생 하는 경우 [GH 1731]
* 여러 AF_UNIX 관련 문제 해결 [GH 3371]
* 현재 작업 디렉터리가 5 자 미만인 경우 WSL interop가 실패할 수 있는 문제 해결 [GH 3379]

## <a name="build-18204-skip-ahead"></a>빌드 18204 (앞으로 건너뛰기)
빌드 18204에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 파이프 파일 시스템 inadvertenly 지우기 edge-트리거된 epoll 이벤트 [GH 3276]
* NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.

## <a name="build-17723-fast"></a>빌드 17723 (빠름)
빌드 17723에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 존재 하지 않는 포트에 대 한 두 번째 지연 지연의 루프백 연결 방지 [GH 3286]
* ////> 추가/f i d/최대 스텁 파일 추가 [GH 2893]
* 더 정확한 IPV6 범위 정보입니다.
* PR_SET_PTRACER 지원 [GH 3053]
* 파이프 파일 시스템 inadvertenly 지우기 edge-트리거된 epoll 이벤트 [GH 3276]
* NTFS symlink를 통해 시작 되는 Win32 실행 파일은 symlink 이름 [GH 2909]을 준수 하지 않습니다.

## <a name="build-17713"></a>빌드 17713
빌드 17713에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 향상 된 좀비 지원 [GH 1353]
* Windows interop 동작을 제어 하기 위한 wsl. c 항목 추가 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 항상 UNIX 소켓 패밀리 유형을 반환 하지 않는 getsockname에 대 한 수정 [GH 1774]
* TIOCSTI에 대 한 지원 추가 [GH 1863]
* 연결 프로세스의 비차단 소켓이 쓰기 시도에 대해 EAGAIN 반환 되어야 함 [GH 2846]
* 탑재 된 Vhd에 대 한 interop 지원 [GH 3246, 3291]
* 루트 폴더에 대 한 사용 권한 확인 문제 해결 [GH 3304]
* TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대 한 지원이 제한적입니다.
* Windows UI 앱은 백그라운드에서 실행 되는 경우에도 실행 해야 합니다.

## <a name="build-17704"></a>빌드 17704
빌드 17704에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Wsl-u 또는--user 옵션 추가 [GH 1203]
* 빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]
* Unix 소켓이 연결 되지 않은 피어 자격 증명을 유지 해야 하는 경우 [GH 3183]
* 비 블로킹 Unix 소켓이 EAGAIN로 무기한 실패 하는 경우 [GH 3191]
* case = off는 새로운 기본 drvfs 탑재 유형 [GH 2937, 3212, 3328]입니다.
    * 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 를 참조 하세요.
* 배포 실행을 중지 하려면 wslconfig/terminate를 추가 합니다.

## <a name="build-17692"></a>빌드 17692
빌드 17692에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 공백으로 경로를 올바르게 처리 하지 않는 WSL shell 상황에 맞는 메뉴 항목의 문제를 해결 합니다.
* 디렉터리 단위 대/소문자 구분을 확장 특성으로 노출
* ARM64 캐시 유지 관리 작업을 에뮬레이트합니다. [Dotnet 문제](https://github.com/dotnet/core/issues/1561)를 해결 합니다.
* DrvFs: 전용 범위에서 이스케이프 된 문자에 해당 하는 문자만 unescape 합니다.

## <a name="build-17686"></a>빌드 17686
빌드 17686에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)를 참조 하십시오.

### <a name="wsl"></a>WSL
* ELF 파서 인터프리터 길이 유효성 검사에서 한 번 이상 오류 수정 [GH 3154]
* WSL 과거 시간을 사용한 절대 타이머 [GH 3091]
* 새로 만든 재분석 지점이 부모 디렉터리에 표시 되는지 확인 합니다.
* DrvFs에서 대/소문자를 구분 하는 디렉터리를 원자 단위로 만듭니다.

## <a name="build-17677"></a>빌드 17677
빌드 17677에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 파일이 존재 하더라도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 추가 문제를 수정 했습니다. [GH 2712]
* UMCI를 사용 하는 경우 WSL 시작 실패가 수정 되었습니다. [GH 3020]

## <a name="build-17666"></a>빌드 17666
빌드 17666에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)를 참조 하십시오.

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>경고: 일부 AMD 칩셋에서 WSL이 실행 되지 않도록 하는 문제가 있습니다 [GH 3134]. 수정이 준비 되 고 참가자 빌드 분기에 대 한 방법이 됩니다.
* WSL [GH 437, 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다. Shift 키를 누른 상태에서 탐색기 창에서 마우스 오른쪽 단추를 클릭 합니다.
* Unix 소켓이 차단 되지 않는 동작 수정 [GH 2822, 3100]
* GH 2026에 보고 된 대로 NETLINK 명령을 수정 합니다.
* 탑재 전파 플래그에 대 한 지원 추가 [GH 2911].
* Inotify 이벤트를 발생 시 키 지 않는 자르기 문제를 해결 합니다 [GH 2978].
* Wsl .exe를 추가 하 여 셸이 없는 단일 이진 파일을 호출 합니다.
* 특정 배포판를 선택 하기 위해 wsl .exe의 추가--배포 옵션입니다.

## <a name="build-17655-skip-ahead"></a>빌드 17655 (앞으로 건너뛰기)
빌드 17655에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Dmesg에 대 한 지원이 제한적입니다. 이제 응용 프로그램이 dmesg에 로그인 할 수 있습니다. WSL 드라이버는 제한 된 정보를 dmesg로 기록 합니다. 나중에이를 확장 하 여 드라이버에서 다른 정보/진단을 수행할 수 있습니다.
    * 참고: dmesg는 현재 장치 인터페이스를 `/dev/kmsg` 통해 지원 됩니다. `syslog`sycall 인터페이스는 아직 지원 되지 않습니다. 따라서와 `dmesg` `-S`같은 명령줄옵션중일부는작동하지않습니다.`-C`
* 파일이 있는 경우에도 다중 스레드 작업에서 ENOENT (를 반환할 수 있는 문제를 해결 했습니다. [GH 2712]

## <a name="build-17639-skip-ahead"></a>빌드 17639 (앞으로 건너뛰기)
빌드 17639에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 네이티브와 일치 하도록 직렬 장치의 기본 gid 및 모드 변경 [GH 3042]
* DrvFs는 이제 확장 된 특성을 지원 합니다.
    * 참고: DrvFs에는 확장 특성의 이름에 대 한 몇 가지 제한이 있습니다. 특히, 일부 문자 (예: '/', ': ' 및 '\*')는 허용 되지 않으며 확장 특성 이름은 DrvFs에서 대/소문자를 구분 하지 않습니다.

## <a name="build-17133-fast"></a>빌드 17133 (빠름)
빌드 17133에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* WSL에서 중단에 대 한 수정입니다. [GH 3039, 3034]

## <a name="build-17128-fast"></a>빌드 17128 (빠름)
빌드 17128에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* 없음

## <a name="build-17627-skip-ahead"></a>빌드 17627 (앞으로 건너뛰기)
빌드 17627에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Futex pi 인식 작업에 대 한 지원을 추가 합니다. [GH 1006]
    * 우선 순위는 현재 지원 되는 WSL 기능이 아니므로 제한이 있지만 표준 사용을 차단 해제 해야 합니다.
* WSL 프로세스에 대 한 Windows 방화벽 지원. [GH 1852]
    * 예를 들어 WSL python 프로세스가 모든 포트에서 수신 대기 하도록 허용 하려면 관리자 권한 Windows cmd를 사용 합니다.```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 방화벽 규칙을 추가 하는 방법에 대 한 자세한 내용은 [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh) 를 참조 하세요.
* Wsl .exe를 사용할 때 사용자의 기본 셸을 준수 합니다. [GH 2372]
* 모든 네트워크 인터페이스를 이더넷으로 보고 합니다. [GH 2996]
* 손상 된/etc/passwd 파일을 보다 효율적으로 처리 합니다. [GH 3001]

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17618-skip-ahead"></a>빌드 17618 (앞으로 건너뛰기)
빌드 17618에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* NT interop [GH 988, 1366, 1433, 1542, 2370, 2406]에 대 한 pseudoconsole 기능을 소개 합니다.
* 레거시 설치 메커니즘 (lxrun)은 더 이상 사용 되지 않습니다. 배포를 설치 하는 데 지원 되는 메커니즘은 Microsoft Store입니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17110"></a>빌드 17110
빌드 17110에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Windows [GH 2928]에서/serers를 종료할 수 있습니다.
* 이제 DrvFs는 기본적으로 디렉터리 대/소문자 구분을 사용 합니다 ("case = dir" 탑재 옵션과 동일).
    * "Case = force" (이전 동작)를 사용 하려면 레지스트리 키를 설정 해야 합니다. 사용 해야 하는 경우 "case = force"를 사용 하도록 설정 하려면 다음 명령을 실행 합니다. reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * 대/소문자를 구분 해야 하는 이전 버전의 Windows에서 wsl로 만든 기존 디렉터리를 사용 하는 경우에는 cmd.exe를 사용 하 여 대/소문자를 구분 합니다 <path> . 즉, fsutil .exe 파일 setcasesensitiveinfo enable을 사용 합니다.
* NULL은 uname syscall에서 반환 된 문자열을 종료 합니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17107"></a>빌드 17107
빌드 17107에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* TCSETSF 및 TCSETSW on master 인 pty 끝점 [GH 2552]을 지원 합니다.
* 동시 interop 프로세스를 시작 하면 EINVAL [GH 2813]이 발생할 수 있습니다.
* /Proc/pid/status.에서 적절 한 추적 상태를 표시 하도록 PTRACE_ATTACH 수정
* CLEARTID 및 SETTID 플래그 모두로 복제 된 단기 프로세스가 TID 주소를 지우지 않고 종료 되는 경합을 수정 합니다.
* 17093 이전 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드할 때 메시지를 표시 합니다. 17093 파일 시스템 변경 내용에 대 한 자세한 내용은 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)의 릴리스 정보를 참조 하세요.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17101"></a>빌드 17101
빌드 17101에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Signalfd에 대 한 지원. [GH 129]
* 지원 되지 않는 NTFS 문자를 포함 하는 파일 이름을 개인 유니코드 문자로 인코딩합니다. [GH 1514]
* 자동 탑재는 쓰기가 지원 되지 않는 경우 읽기 전용으로 대체 됩니다. [GH 2603]
* 유니코드 서로게이트 쌍 (예:이 모 지 문자)을 붙여 넣을 수 있습니다. [GH 2765]
* /Sproc 및/tsys의 의사 (Pseudo) 파일은 select, 폴링합니다, epoll, et al에서 준비 된 읽기 및 쓰기를 반환 해야 합니다. [GH 2838]
* 레지스트리가 변조 되거나 손상 된 경우 서비스가 무한 루프로 전환 될 수 있는 문제를 해결 합니다.
* Netlink 메시지를 수정 하 여 최신 (업스트림 4.14) 버전의 iproute2를 사용 합니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17093"></a>빌드 17093
빌드 17093에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)를 참조 하십시오.

#### <a name="important"></a>중요:
이 빌드로 업그레이드 한 후 처음으로 WSL을 시작할 때 Linux 파일 시스템 디렉터리를 업그레이드 하는 작업을 수행 해야 합니다. 이 작업은 몇 분 정도 걸릴 수 있으므로 WSL이 느리게 시작 하는 것 처럼 보일 수 있습니다. 저장소에서 설치한 각 배포에 대해 한 번만 수행 해야 합니다.
* DrvFs에서 대/소문자 구분 지원이 개선 되었습니다.
    * 이제 DrvFs는 디렉터리 단위 대/소문자 구분을 지원 합니다. 이 플래그는 디렉터리에 대해 설정 하 여 해당 디렉터리의 모든 작업이 대/소문자만 다른 파일을 열 수 있도록 하는 대/소문자 구분으로 처리 되어야 함을 나타내는 새로운 플래그입니다.
    * DrvFs에는 디렉터리 별로 대/소문자 구분을 제어 하는 새로운 탑재 옵션이 있습니다.
        * case = force: 모든 디렉터리는 대/소문자를 구분 합니다 (드라이브 루트 제외). WSL로 만든 새 디렉터리는 대/소문자를 구분 하 여 표시 됩니다. 이는 새 디렉터리의 대/소문자 구분을 표시 하는 것을 제외 하 고 레거시 동작입니다.
        * case = dir: 디렉터리 단위 대/소문자 구분 플래그를 사용 하는 디렉터리만 대/소문자를 구분 합니다. 다른 디렉터리는 대/소문자를 구분 하지 않습니다. WSL로 만든 새 디렉터리는 대/소문자를 구분 하 여 표시 됩니다.
        * case = off: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리 됩니다. 다른 디렉터리는 대/소문자를 구분 하지 않습니다. WSL로 만든 새 디렉터리는 대/소문자를 구분 하지 않는 것으로 표시 됩니다.
    * 참고: 이전 릴리스의 WSL에서 만든 디렉터리는이 플래그를 설정 하지 않았으므로 "case = dir" 옵션을 사용 하는 경우 대/소문자를 구분 하는 것으로 간주 되지 않습니다. 기존 디렉터리에이 플래그를 설정 하는 방법은 곧 제공 될 예정입니다.
    * 이러한 옵션을 사용 하 여 탑재 하는 예 (기존 드라이브의 경우 다른 옵션을 사용 하 여 탑재 하려면 먼저 분리 해야 함): sudo mount-t drvfs C:/mnt/c-o case = dir
    * 지금은 case = force가 여전히 기본 옵션입니다. 이는 나중에 case = dir로 변경 됩니다.
* 이제 DrvFs을 탑재할 때 Windows 경로에서 슬래시를 사용할 수 있습니다 (예: sudo mount-t DrvFs/server/share/mnt/share).
* 이제 WSL에서 인스턴스를 시작 하는 동안/etc/fstab 파일 [GH 2636]을 처리 합니다.
    * DrvFs 드라이브를 자동으로 탑재 하기 전에 수행 됩니다. fstab에 의해 이미 탑재 된 모든 드라이브는 자동으로 탑재 되지 않으므로 특정 드라이브의 탑재 지점을 변경할 수 있습니다.
    * 이 동작은 wsl를 사용 하 여 해제할 수 있습니다.
* /Proc의 mount, mountinfo 및 mountstats 파일은 백슬래시 및 공백과 같은 특수 문자를 적절히 이스케이프 [GH 2799]
* DrvFs를 사용 하 여 만든 특수 파일 (예: WSL 기호화 된 링크, 메타 데이터를 사용 하는 경우 fifos 및 소켓)을 이제 Windows에서 복사 하 여 이동할 수 있습니다.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL은 wsl.
사용자가 하위 시스템을 시작할 때마다 적용 되는 WSL의 특정 기능을 자동으로 구성 하는 메서드를 추가 했습니다. 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함 됩니다. 이에 대 한 자세한 내용은 다음 블로그 게시물을 살펴보세요. https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX를 사용 하면 WSL 및 Windows 네이티브 프로세스의 Linux 프로세스 간 소켓 연결을 허용 합니다.
WSL 및 Windows 응용 프로그램은 이제 Unix 소켓을 통해 서로 통신할 수 있습니다. Windows에서 서비스를 실행 하 고 Windows 및 WSL 앱 모두에서 서비스를 사용할 수 있게 하려는 경우를 가정해 보겠습니다. 이제는 Unix 소켓에서 가능 합니다. 블로그 게시물에서 자세한 내용을 알아보세요. https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* MAP_NORESERVE를 사용 하 여 mmap () 지원 [GH 121, 2784]
* 지원 CLONE_PTRACE 및 CLONE_UNTRACED [GH 121, 2781]
* 복제에서 비 SIGCHLD 종료 신호 처리 [GH 121, 2781]
* 스텁/proc/sys/fs/inotify/max_user_instances 및/proc/sys/fs/inotify/max_user_watches [GH 1705]
* 0이 아닌 오프셋을 포함 하는 로드 헤더가 포함 된 ELF 이진 파일을 로드 하는 동안 오류 발생 [GH 1884]
* 이미지를 로드할 때 후행 페이지 바이트를 반환 합니다.
* Execve가 자동으로 프로세스를 종료 하는 사례 줄이기

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17083"></a>빌드 17083
빌드 17083에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* Epoll [GH 2798, 2801, 2857]와 관련 된 버그를 수정 했습니다.
* ASLR을 끄면 중단 문제가 해결 됨 [GH 1185, 2870]
* Mmap 작업이 원자성으로 표시 되는지 확인 [GH 2732]

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17074"></a>빌드 17074
빌드 17074에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* DrvFs 메타 데이터의 고정 저장소 형식 [GH 2777] </br>
**중요:** 이 빌드 전에 만든 DrvFs 메타 데이터는 잘못 표시 되거나 전혀 표시 되지 않습니다. 영향을 받는 파일을 수정 하려면 chmod 및 chown를 사용 하 여 메타 데이터를 다시 적용 합니다.
* 여러 신호 및 다시 시작 가능한 syscall 문제를 해결 했습니다.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17063"></a>빌드 17063
빌드 17063에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)를 참조 하십시오.

### <a name="wsl"></a>WSL
* DrvFs는 추가 Linux 메타 데이터를 지원 합니다. 이렇게 하면 chmod/chown를 사용 하 여 파일의 소유자와 모드를 설정할 수 있으며 fifos, unix 소켓 및 장치 파일과 같은 특수 파일을 만들 수도 있습니다. 이는 아직 실험적 이기 때문에 지금은 기본적으로 사용 되지 않습니다.
**참고:**  DrvFs에서 사용 하는 메타 데이터 형식의 버그를 수정 했습니다. 메타 데이터는 실험을 위해이 빌드에서 작동 하지만 향후 빌드는이 빌드에서 생성 된 메타 데이터를 올바르게 읽을 수 없습니다.  수정 된 파일의 소유자를 수동으로 업데이트 하 고 사용자 지정 장치 ID를 사용 하는 장치를 다시 만들어야 할 수도 있습니다.

  을 사용 하도록 설정 하려면 메타 데이터 옵션을 사용 하 여 DrvFs를 탑재 합니다 (기존 탑재에서 사용 하도록 설정 하려면 먼저 분리 해야 함).

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 권한은 파일에 추가 메타 데이터로 추가 됩니다. Windows 사용 권한에는 영향을 주지 않습니다.  Windows 편집기를 사용 하 여 파일을 편집 하면 메타 데이터가 제거 될 수 있습니다. 이 경우 파일은 기본 권한으로 되돌아갑니다.

* 메타 데이터를 사용 하지 않고 파일을 제어 하는 탑재 옵션이 DrvFs에 추가 되었습니다.
  * uid: 모든 파일의 소유자에 게 사용 되는 사용자 ID입니다.
  * gid: 모든 파일의 소유자에 사용 되는 그룹 ID입니다.
  * umask: 모든 파일 및 디렉터리에 대해 제외할 8 진수 마스크입니다.
  * fmask: 모든 일반 파일에 대해 제외할 8 진수 마스크입니다.
  * 6mask: 모든 디렉터리에 대해 제외할 8 진수 마스크입니다.

  이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  메타 데이터 없이 파일에 대 한 기본 권한을 지정 하려면 메타 데이터 옵션과 결합 합니다.

* 는 새 환경 변수 `WSLENV`를 도입 하 여 환경 변수가 wsl과 Win32 사이에서 흐르는 방식을 구성 합니다.

  이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`는 WSL의 Win32 또는 Win32 프로세스에서 WSL 프로세스를 시작할 때 포함할 수 있는 환경 변수의 콜론으로 구분 된 목록입니다.  각 변수에는 슬래시 뒤에 플래그를 사용 하 여 변환 방법을 지정할 수 있습니다.
  * ® 값은 WSL 경로와 Win32 경로 간에 변환 해야 하는 경로입니다.
  * l-value 값은 경로 목록입니다. WSL에서는 콜론으로 구분 된 목록입니다. Win32에서 세미콜론으로 구분 된 목록입니다.
  * 나무 Win32에서 WSL을 호출할 때에만 값이 포함 되어야 합니다.
  * w WSL에서 Win32를 호출할 때에만 값이 포함 되어야 합니다.

  사용자를 위해 `WSLENV` .bashrc 또는 사용자 지정 Windows 환경에서를 설정할 수 있습니다.

* drvfs 탑재는 tar, cp-p의 타임 스탬프를 올바르게 유지 합니다 (GH 1939).
* drvfs symlink 올바른 크기를 보고 합니다 (GH 2641).
* 매우 큰 IO 크기에 대 한 읽기/쓰기 작동 (GH 2653)
* waitpid는 프로세스 그룹 Id와 함께 작동 합니다 (GH 2534).
* 큰 예약 영역에 대 한 mmap 성능이 크게 향상 되었습니다. GH c 성능 향상 (1671)
* READ_IMPLIES_EXEC에 대 한 개성 지원 최대 및 clisp 수정 (GH 1185)
* mprotect는 PROT_GROWSDOWN을 지원 합니다. clisp 수정 (GH 1128)
* 과도 한 커밋 모드의 페이지 폴트 수정 sbcl (GH 1128)을 수정 합니다.
* 클론은 더 많은 플래그 조합을 지원 합니다.
* Epoll 파일의 select/epoll (이전에는 작동 하지 않음)를 지원 합니다.
* 구현 되지 않은 syscall에 대 한 ptrace를 알립니다.
* Resolv.conf 이름 서버를 생성할 때 작동 하지 않는 인터페이스 무시 [GH 2694]
* 실제 주소가 없는 네트워크 인터페이스를 열거 합니다. [GH 2685]
* 추가 버그 수정 및 개선 사항

### <a name="linux-tools-available-to-developers-on-windows"></a>Windows의 개발자가 사용할 수 있는 Linux 도구

* Windows 명령줄 도구 체인는 bsdtar (tar) 및 말아를 포함 합니다.
  [이 블로그](https://aka.ms/tarcurlwindows) 를 읽고 이러한 두 가지 도구를 추가 하는 방법에 대해 자세히 알아보고 Windows에서 개발자 환경에 어떻게 셰이핑 하는지 알아보세요.

*   `AF_UNIX`는 Windows 참가자 SDK (17061 +)에서 사용할 수 있습니다.
  [이 블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) 를 읽고 Windows의 개발자 `AF_UNIX` 가 사용할 수 있는 방법에 대해 자세히 알아보세요.

### <a name="console"></a>콘솔
* 수정 사항이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.


## <a name="build-17046"></a>빌드 17046

빌드 17046에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)를 참조 하십시오.

### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 활성 터미널 없이 프로세스를 실행할 수 있습니다. [GH 709, 1007, 1511, 2252, 2391, et al.]
- CLONE_VFORK 및 CLONE_VM에 대 한 지원이 향상 되었습니다. [GH 1878, 2615]
- WSL 네트워킹 작업을 위한 TDI 필터 드라이버를 건너뜁니다. [GH 1554]
- 특정 조건이 충족 되 면 DrvFs에서 NT symlink를 만듭니다. [GH 353, 1475, 2602]
    - 링크 대상은 상대 경로 여야 하 고, 탑재 지점이 나 symlink를 교차 해서는 안 되며, 존재 해야 합니다.
    - 개발자 모드가 설정 되어 있지 않으면 사용자에 게 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (일반적으로 wsl .exe를 실행 해야 함)가 있어야 합니다.
    - 다른 모든 상황에서 DrvFs는 여전히 WSL symlink를 만듭니다.
- 상승 된 권한 및 비관리자 WSL 인스턴스를 동시에 실행할 수 있습니다.
- /Proc/sys/kernel/yama/ptrace_scope 지원
- Wslpath를 추가 하 여 WSL <-> Windows 경로 변환을 수행 합니다. [GH 522, 1243, 1834, 2327, et al.]
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

빌드 17040에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 17035 이후의 수정 사항은 없습니다.

#### <a name="console"></a>콘솔
- 17035 이후의 수정 사항은 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17035"></a>빌드 17035

빌드 17035에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- DrvFs의 파일에 액세스 하는 경우 EINVAL와 함께 실패할 수 있습니다. [GH 2448]

#### <a name="console"></a>콘솔
- VT 모드에서 줄을 삽입/삭제할 때 일부 색이 손실 됩니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17025"></a>빌드 17025

빌드 17025에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 새 포그라운드 프로세스 그룹 [GH 1653, 2510]에서 초기 프로세스를 시작 합니다.
- SIDELIVERY UP 배달 수정 [GH 2496].
- 제공 된 [GH 2497]이 없으면 기본 가상 브리지 이름을 생성 합니다.
- /Proc/sys/kernel/random/boot_id [GH 2518]을 구현 합니다.
- 더 많은 interop stdout/stderr 파이프 수정.
- 스텁 syncfs 시스템 호출입니다.

#### <a name="console"></a>콘솔
- 타사 콘솔에 대 한 입력 VT 번역 수정 [GH 111]

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="build-17017"></a>빌드 17017

빌드 17017에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 빈 ELF program headers [GH 330]을 무시 합니다.
- LxssManager가 비 대화형 사용자 (ssh 및 예약 된 작업 지원) [GH 777, 1602]에 대해 WSL 인스턴스를 만들도록 허용 합니다.
- WSL-> Win32 > WSL ("개시") 시나리오 [GH 1228]을 지원 합니다.
- Interop [GH 1614]를 통해 호출 되는 콘솔 앱의 종료에 대 한 제한 된 지원.
- Devpts [GH 1948]에 대 한 탑재 옵션을 지원 합니다.
- Ptrace 차단 자식 시작 [GH 2333].
- EPOLLET에 일부 이벤트가 없습니다 [GH 2462].
- PTRACE_GETSIGINFO에 대 한 추가 데이터를 반환 합니다.
- Lseek를 사용한 Getdents는 잘못 된 결과를 제공 합니다.
- 일부 Win32 interop 앱이 중단 되 고, 더 이상 데이터가 없는 파이프의 입력을 기다리는 중입니다.
- Tty/인 pty 파일에 대 한 O_ASYNC 지원.
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
테스트를 진행 중입니다.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>빌드 16288

빌드 16288에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 소켓 파일 설명자에 대해 uid, gid 및 모드를 올바르게 초기화 및 보고 [GH 2490]
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 내용 없음

## <a name="build-16278"></a>빌드 16278

빌드 162738에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- LX MM 상태를 해제할 때 파일 지원 섹션의 매핑된 뷰를 명시적으로 매핑 해제 [GH 2415]
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 내용 없음

## <a name="build-16275"></a>빌드 16275

빌드 162735에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 이 릴리스에서는 WSL 관련 변경 내용이 없습니다.

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 내용 없음

## <a name="build-16273"></a>빌드 16273

빌드 16273에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- DrvFs에서 디렉터리에 대해 잘못 된 파일 형식을 보고 하는 문제 해결 [GH 2392]
- Uevent를 사용 하는 프로그램의 차단을 해제 하는 NETLINK_KOBJECT_UEVENT 소켓 만들기 허용 [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- 비차단 연결에 대 한 지원 추가 [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- CLONE_FS CLONE 시스템 호출 플래그 구현 [GH 2242]
- NT interop에서 탭 또는 따옴표를 올바르게 처리 하지 않는 문제 해결 [GH 1625, 2164]
- WSL 인스턴스를 다시 시작 하려고 할 때 액세스 거부 오류 해결 [GH 651, 2095]
- Futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업 구현 [GH 2242]
- 여러 SysFs 파일에 대 한 사용 권한 수정 [GH 2214]
- 설치 하는 동안 Haskell stack 중단 수정 [GH 2290]
- Binfmt_misc ' C ' ' O ' 및 ' P ' 플래그 구현 [GH 2103]
- Add/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]
- Ioprio_set 시스템 호출에 대 한 부분 지원 추가 [GH 498]
- 스텁 SO_REUSEPORT & netlink 소켓 SO_PASSCRED에 대 한 지원을 추가 하는 중 [GH 69]
- 배포를 현재 설치 하거나 제거 하는 경우 RegisterDistribuiton의 다른 오류 코드를 반환 합니다.
- Wslconfig .exe를 통해 부분적으로 설치 된 WSL 배포의 등록 취소 허용
- Udp:: msg_peek에서 python 소켓 테스트 중단 수정
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
총 테스트: 1904<br/>
건너뛴 총 테스트: 209<br/>
총 실패 횟수: 229<br/>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>빌드 16257

빌드 16257에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- Prlimit64 시스템 호출 구현
- Ulimit에 대 한 지원 추가 (setrlimit RLIMIT_NOFILE) [GH 1688]
- TCP 소켓용 스텁 MSG_MORE [GH 2351]
- 잘못 된 AT_EXECFN 보조 벡터 동작 수정 [GH 2133]
- 콘솔/tty의 복사/붙여넣기 동작을 수정 하 고 더 나은 전체 버퍼 처리를 추가 합니다 [GH 2204, 2131]
- AT_SECURE 및 GH 프로그램에 대 한 보조 vector에서 set [2031]
- 유사-터미널 마스터 끝점이 TIOCPGRP를 처리 하지 않습니다 [GH 1063]
- Fix lseek에서 LxFs의 디렉터리 되감기 [GH 2310]
- 사용량이 많은 후에/cv/ptmx 잠금 [GH 1882]
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 모든 곳에서 가로 선/밑줄 수정 [GH 2168]
- NPM을 닫기 위해 프로세스 순서 변경 수정 [GH 2170]
- 새 색 구성표를 추가 했습니다. https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 결과:
16251 이후 변경 내용 없음

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`prlimit64`<br/>

### <a name="known-issues"></a>알려진 문제
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub 문제 2392: WSL에서 인식할 수 없는 Windows 폴더 ...](https://github.com/Microsoft/BashOnWindows/issues/2392)
빌드 16257에서 WSL에는를 통해 `/mnt/c/...`Windows 파일/폴더를 열거 하는 동안 문제가 발생 했습니다.
이 문제는 해결 되었으며, 8/14/2017를 시작 하는 동안에는 참가자 빌드에서 릴리스 해야 합니다.

<br/>

## <a name="build-16251"></a>빌드 16251

빌드 16251에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- WSL 선택적 구성 요소에서 베타 태그 제거에 대 한 자세한 내용은 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) 을 참조 하세요.
- Exec [GH 962, 1415, 2072]에서 집합-사용자 ID 및 집합 그룹 ID 바이너리에 대해 저장 된 설정 uid 및 gid를 올바르게 초기화 합니다.
- Ptrace PTRACE_O_TRACEEXIT에 대 한 지원 추가 [GH 555]
- NT_FPREGSET에서 ptrace PTRACE_GETFPREGS 및 PTRACE_GETREGSET에 대 한 지원이 추가 됨 [GH 555]
- 무시 된 신호를 중지 하도록 ptrace 고정
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 이 릴리스에서는 콘솔과 관련 된 변경 내용이 없습니다.

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 768</br>
실패 한 테스트 수: 244</br>
건너뛴 테스트 수: 96</br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>빌드 16241

빌드 16241에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 이 릴리스에서는 WSL 관련 변경 내용이 없습니다.

#### <a name="console"></a>콘솔
- 원래 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) 에 보고 된 교차 선 DEC에 대해 잘못 된 문자를 출력 하는 문제 해결
- 코드 페이지 65001 (utf8)에 표시 되는 출력 텍스트를 수정 하지 않습니다.
- 한 색의 RGB 값에 적용 한 변경 내용을 선택 변경 시 색상표의 다른 부분으로 전송 하지 않습니다. 이렇게 하면 콘솔 속성 시트를 훨씬 쉽게 사용할 수 있습니다.
- Ctrl + S가 제대로 작동 하지 않는 것 같습니다.
- ANSI 이스케이프 코드에서 굵게 표시 되지 않은/-Dim [GH 2174]
- 콘솔이 Vim color 테마를 올바르게 지원 하지 않음 [GH 1706]
- 특정 문자를 붙여 넣을 수 없습니다 [GH 2149]
- 편집/명령줄에 있는 경우 bash 창의 크기를 조정 하 여 리플로우 크기를 조정할 수 있습니다. [GH ConEmu 1123]
- Ctrl + L에서 화면을 더티 상태로 둡니다 [GH 1978]
- HDPI에서 VT를 표시할 때 콘솔 렌더링 버그 [GH 1907]
- Japansese 문자는 유니코드 문자 U + 30FB [GH 2146]와 이상한 모양으로 표시 됩니다.
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16237"></a>빌드 16237

빌드 16237에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- Lxfs (root, root, 0000)에서 EAs가 없는 파일에 대 한 기본 특성 사용
- 확장 된 특성을 사용 하는 배포에 대 한 지원 추가
- Getdents 및 getdents64에서 반환 된 항목의 패딩 수정
- Shmctl SHM_STAT 시스템 호출에 대 한 권한 확인 수정 [GH 2068]
- Tty에 대 한 잘못 된 초기 epoll 상태 수정 됨 [GH 2231]
- 모든 항목을 반환 하지 않는 DrvFs readdir 수정 [GH 2077]
- 파일의 연결을 끊을 때 LxFs readdir 수정 [GH 2077]
- 연결 되지 않은 drvfs 파일을 procfs를 통해 다시 열 수 있도록 허용
- WSL 기능을 사용 하지 않도록 설정 하기 위한 전역 레지스트리 키 재정의 추가 (상호 운용성/드라이브 탑재)
- DrvFs (및 LxFs)에 대해 "stat"의 잘못 된 블록 수 수정 [GH 1894]
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16232"></a>빌드 16232

빌드 16232에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 이 릴리스에서는 WSL 관련 변경 내용이 없습니다.

</br>

## <a name="build-16226"></a>빌드 16226

빌드 16226에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- xattr 관련 syscall 지원 (getxattr, setxattr, listxattr, removexattr).
- capablity xattr 지원.
- 비-MS SMB 서버를 비롯 한 특정 파일 시스템 및 필터와의 호환성이 향상 되었습니다. [GH #1952]
- OneDrive 자리 표시자, GVFS 자리 표시자 및 압축 OS 압축 파일에 대 한 지원이 향상 되었습니다.
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16215"></a>빌드 16215

빌드 16215에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- WSL에서 더 이상 개발자 모드를 요구 하지 않습니다.
- Drvfs에서 디렉터리 연결점을 지원 합니다.
- WSL 배포 appx 패키지의 제거를 처리 합니다.
- 개인 및 공유 매핑을 표시 하도록 procfs를 업데이트 합니다.
- 구성에서 부분적으로 설치 또는 제거 되는 배포를 정리 하는 기능을 추가 합니다.
- TCP 소켓에 대해 IP_MTU_DISCOVER에 대 한 지원이 추가 되었습니다. [GH 1639, 2115, 2205]
- AF_INADDR에 대 한 경로에 대 한 프로토콜 패밀리를 유추 합니다.
- 직렬 장치 개선 [GH 1929].

</br>

## <a name="build-16199"></a>빌드 16199

빌드 16199에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 이러한 릴리스에서는 WSL 관련 변경 내용이 없습니다.

</br>

## <a name="build-16193"></a>빌드 16193

빌드 16193에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- SIGCONT 및 threadgroup을 종료 하는 경합 상태 [GH 1973]
- FILE_DEVICE_CONSOLE 대신 tty 및 인 pty 장치를 report FILE_DEVICE_NAMED_PIPE로 변경 [GH 1840]
- IP_OPTIONS에 대 한 SSH 픽스
- Init daemon로 이동 DrvFs 탑재 [GH 1862, 1968, 1767, 1933]
- DrvFs에서 다음 NT symlink에 대 한 지원이 추가 되었습니다.

</br>

## <a name="build-16184"></a>빌드 16184

빌드 16184에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- Apt 패키지 유지 관리 작업 제거 (lxrun/update)
- Node.js의 Windows 프로세스에서 표시 되지 않는 고정 출력 [GH 1840]
- Lxcore의 완화 맞춤 요구 사항 [GH 1794]
- 숫자로 시스템 호출에서 AT_EMPTY_PATH 플래그의 처리 문제를 수정 했습니다.
- 열린 핸들로 DrvFs 파일을 삭제 하면 파일이 정의 되지 않은 동작 [GH 544, 966, 1357, 1535, 1615]을 나타내도록 하는 문제가 해결 되었습니다.
- 이제/etc/hosts가 Windows 호스트 파일 (%windir%\system32\drivers\etc\hosts)에서 항목을 상속 [GH 1495]

</br>

## <a name="build-16179"></a>빌드 16179

빌드 16179에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 이번 주에는 WSL이 변경 되지 않습니다.

</br>

## <a name="build-16176"></a>빌드 16176

빌드 16176에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- [직렬 지원 사용](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 추가 된 IP 소켓 옵션 IP_OPTIONS [GH 1116]
- Pwritev 함수 구현 (파일을 nginx/PHP로 업로드 하는 동안) [GH 1506]
- 추가 된 IP 소켓 옵션 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP 소켓 옵션에 대 한 지원 [GH 1678]
- 앱 노드에 대 한 IP (V6) _MTU 소켓 옵션 추가 됨, 경로 추적, 방법, nslookup, 호스트
- 추가 된 IP 소켓 옵션 IPV6_UNICAST_HOPS
- [파일 시스템 향상](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * UNC 경로 탑재 허용
    * Drvfs에서 CDFS 지원 사용
    * Drvfs의 네트워크 파일 시스템에 대 한 사용 권한을 올바르게 처리 합니다.
    * Drvfs에 원격 드라이브에 대 한 지원 추가
    * Drvfs에서 FAT 지원 사용
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과
15042 이후 변경 내용 없음

</br>

## <a name="build-16170"></a>빌드 16170

빌드 16170에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)를 참조 하십시오.<br/>

WSL 테스트를 위한 새로운 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) 을 발표 했습니다.

### <a name="fixed"></a>고정

- 지원 소켓 옵션 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- PTRACE_OLDSETOPTIONS에 대 한 지원을 추가 합니다. [GH 1692]
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과
15042 이후 변경 내용 없음

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Windows 10 크리에이터 스 업데이트에 15046 빌드
Windows 10에 대 한 작성자 업데이트에 포함 하기 위해 계획 된 WSL 수정 사항이 나 기능이 더 이상 없습니다. WSL의 릴리스 정보는 다음 주 Windows 업데이트을 대상으로 하는 추가를 위해 향후 몇 주 이내에 다시 시작 됩니다. 빌드 15046 및 향후 Insider 릴리스에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)를 참조 하세요. <br/><br/>
 <br/>

## <a name="build-15042"></a>빌드 15042

빌드 15042에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- "..."로 끝나는 경로를 제거할 때 교착 상태를 수정 합니다.
- 성공 시 FIONBIO에서 0을 반환 하지 않는 문제 해결 [GH 1683]
- Inet 데이터 그램 소켓의 길이가 0 인 읽기와 관련 된 문제 해결
- Drvfs inode lookup의 경합 상태 때문에 가능한 교착 상태 수정 [GH 1675]
- Unix 소켓 보조 데이터에 대 한 확장 된 지원 SCM_CREDENTIALS 및 SCM_RIGHTS [GH 514, 613, 1326]
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 737</br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255

</br>

## <a name="build-15031"></a>빌드 15031

빌드 15031에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- 시간 (2)이 산발적으로 동작 하는 버그를 수정 했습니다.
- \* SIGPROCMASK syscall에서 신호 마스크를 손상 시킬 수 있는 문제를 해결 하 고 문제를 해결 합니다.
- 이제 WSL 프로세스 만들기 알림에서 전체 명령줄 길이를 반환 합니다. [GH 1632]
- 이제 WSL은 GDB 정지에 대해 ptrace를 통해 스레드 종료를 보고 합니다. [GH 1196]
- 많은 tmux IO 후에 ptys 중단 하는 버그를 수정 했습니다. [GH 1358]
- 많은 시스템 호출 (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)에서 시간 제한 확인이 수정 되었습니다.
- 추가 된 eventfd EFD_SEMAPHORE 지원 [GH 452]
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 737</br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>빌드 15025

빌드 15025에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- Grep 2.27을 중단 한 버그 수정 [GH 1578]
- Eventfd2 syscall에 대해 구현 된 EFD_SEMAPHORE 플래그 [GH 452]
- 구현 됨/proc/[pid]/net/ipv6_route [GH 1608]
- Unix 스트림 소켓에 대 한 신호 구동 IO 지원 [GH 393, 68]
- Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]
- Syscall () 구현 구현 [GH 1531]
- Epoll_wait ()가 대기 하지 않는 버그 수정 [GH 1609]
- /Proc\version_siu 구현
- 이제 두 파일 설명자가 같은 파이프를 참조 하는 경우 티 syscall에서 오류를 반환 합니다.
- SO_PEERCRED for Unix 소켓의 올바른 동작을 구현 합니다.
- Tkill syscall 잘못 된 매개 변수 처리를 수정 했습니다.
- Drvfs의 preformace를 늘리기 위한 변경 내용
- Ruby IO 차단에 대 한 사소한 수정
- Inet 소켓에 대 한 MSG_DONTWAIT 플래그의 EINVAL을 반환 하는 Fixed recvmsg () [GH 1296]
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 732</br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>빌드 15019

빌드 15019에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- Htop (GH 823, 945, 971)와 같은 도구에 대해 procfs에서 CPU 사용량을 잘못 보고 하는 버그가 수정 되었습니다.
- 기존 파일에 대해 O_TRUNC를 사용 하 여 open ()을 호출 하면 inotify 앞에 IN_MODIFY가 생성 됩니다.
- Postgress를 사용 하도록 설정 하는 unix socket getsockopt SO_ERROR에 대 한 수정 [GH 61, 1354]
- GO 언어에 대해/proc/sys/net/core/somaxconn 구현
- Apt-패키지 업데이트 배경 가져오기 작업이 이제 뷰에서 숨겨진 상태로 실행 됩니다.
- Ipv6 localhost (스프링 프레임 워크 (Java) 실패)의 범위를 지웁니다.
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 714 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 249 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>빌드 15014

빌드 15014에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- 이제 Ctrl + C는 의도 한 대로 작동 합니다.
- 이제 htop 및 ps auxw에 올바른 리소스 사용률 (GH #516)이 표시 됩니다.
- 신호로 NT 예외를 기본으로 변환 합니다. (GH #513)
- EINVAL (GH #1571) 대신 공간이 부족 하 게 되 면 ENOSPC가 실패 하 게 됩니다.
- /Proc/sys/kernel/sem. 추가 됨
- 구현 된 semop 및 semtimedop 시스템 호출
- IP_RECVTOS & IPV6_RECVTCLASS socket 옵션을 사용 하 여 nslookup 오류 수정 (GH 69)
- IP_RECVTTL 및 IPV6_RECVHOPLIMIT 소켓 옵션에 대 한 지원
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 709 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 요약
총 Syscall: 384 </br>
총 구현: 235 </br>
총 스텁: 22 </br>
구현 되지 않은 총: 127 </br>
[자세한 분석](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>빌드 15007

빌드 15007에 대 한 일반적인 Windows 정보는 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)를 참조 하십시오.<br/>


### <a name="known-issue"></a>알려진 문제

- 콘솔에서 일부 Ctrl + <key> input을 인식 하지 못하는 알려진 버그가 있습니다.  여기에는 일반 ' c ' 키의 역할을 하는 ctrl + c 명령이 포함 됩니다.

  - 해결 방법: 대체 키를 Ctrl + C에 매핑합니다. 예를 들어 Ctrl + K를 Ctrl + C로 매핑하려면: `stty intr \^k`를 추가 합니다.  이 매핑은 터미널 당 이며 bash를 시작할 *때마다* 수행 해야 합니다. 사용자는이를 포함 하는 옵션을 탐색할 수 있습니다.`.bashrc`

### <a name="fixed"></a>고정

- WSL을 실행 하면 CPU 코어의 100%를 사용 하는 문제를 해결 했습니다.
- 소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO 이제 지원 됩니다. (GH #851, 987)
- Lxcore (GH #1452, 1414, 1343, 468, 308)에서 네트워크 인터페이스 실제 주소를 16 바이트로 자릅니다.
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 709 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>빌드 15002

빌드 15002에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)를 참조 하십시오.<br/>


### <a name="known-issue"></a>알려진 문제

다음과 같은 두 가지 알려진 문제가 있습니다.
- 콘솔에서 일부 Ctrl + <key> input을 인식 하지 못하는 알려진 버그가 있습니다.  여기에는 일반 ' c ' 키의 역할을 하는 ctrl + c 명령이 포함 됩니다.

  - 해결 방법: 대체 키를 Ctrl + C에 매핑합니다. 예를 들어 Ctrl + K를 Ctrl + C로 매핑하려면: `stty intr \^k`를 추가 합니다.  이 매핑은 터미널 당 이며 bash를 시작할 *때마다* 수행 해야 합니다. 사용자는이를 포함 하는 옵션을 탐색할 수 있습니다.`.bashrc`

- WSL은 시스템 스레드를 실행 하는 동안 CPU 코어의 100%를 사용 합니다.  근본 원인을 내부적으로 해결 하 고 해결 했습니다.

### <a name="fixed"></a>고정

- 이제 모든 bash 세션을 동일한 권한 수준에서 만들어야 합니다.  다른 수준에서 세션을 시작 하려고 하면 차단 됩니다.  즉, 관리자 및 비관리자 콘솔을 동시에 실행할 수 없습니다. (GH #626)
<br/>
- 다음 NETLINK_ROUTE 메시지를 구현 함 (Windows 관리자 필요)
     - RTM_NEWADDR (지원 `ip addr add`)
     - RTM_NEWROUTE (지원 `ip route add`)
     - RTM_DELADDR (지원 `ip addr del`)
     - RTM_DELROUTE (지원 `ip route del`)
- 업데이트할 패키지의 예약 된 작업 확인은 더 이상 요금제 연결 (GH #1371)에서 실행 되지 않습니다.
- 파이프가 중단 되는 오류 (예: bash-c "ls-alR/" |)를 수정 했습니다. bash-c "cat" (GH #1214)
- 구현 된 TCP_KEEPCNT socket 옵션 (GH #843)
- 구현 된 IP_MTU_DISCOVER INET socket 옵션 (GH #720, 717, 170, 69)
- Nt 경로 조회를 사용 하 여 init에서 NT 이진 파일을 실행 하는 레거시 기능을 제거 했습니다. (GH #1325)
- 그룹/기타 읽기 액세스 (0644) (GH #1321)를 허용 하는/dev/kmsg의 수정 모드
- 구현 된/proc/sys/kernel/random/uuid (GH #1092)
- 프로세스 시작 시간이 2432 년 (GH #974)으로 표시 된 오류를 수정 했습니다.
- 기본 용어 환경 변수를 xterm-256color (GH #1446)로 전환 했습니다.
- 프로세스 포크 중에 프로세스 커밋이 계산 되는 방식이 수정 되었습니다. (GH #1286)
- 구현 된/proc/sys/vm/overcommit_memory. (GH #1286)
- GH (#69)를 구현 합니다.
- 바로 가기 이름이 잘못 지역화 된 오류 (GH #696)를 수정 했습니다.
- 프로그램 헤더의 유효성을 올바르게 검사 하지 않는 elf 구문 분석 논리는 PATH_MAX 보다 작거나 같아야 합니다. (GH #1048)
- Procfs, sysfs, cgroupfs 및 binfmtfs (GH #1378)에 대 한 statfs 콜백을 구현 합니다.
- 닫히지 않는 AptPackageIndexUpdate 창이 수정 됨 (GH #1184 GH #1193에도 설명 됨)
- ASLR 개성 ADDR_NO_RANDOMIZE 지원이 추가 되었습니다. (GH #1148, 1128)
- PTRACE_GETSIGINFO, SIGSEGV, AV 중 적절 한 gdb 스택 추적을 위한 향상 된 (GH #875)
- Patchelf 이진 파일에 대해 Elf 구문 분석이 더 이상 실패 하지 않습니다. (GH #471)
- /Etc/resolv.conf에 전파 되는 VPN DNS (GH #416, 1350)
- 보다 안정적인 데이터 전송을 위해 TCP가 향상 되었습니다. (GH #610, 616, 1025, 1335)
- 이제 너무 많은 파일이 열려 있으면 (EMFILE) 올바른 오류 코드를 반환 합니다. (GH #1126, 2090)
- 이제 Windows 감사 로그가 프로세스 만들기 감사에서 이미지 이름을 보고 합니다.
- 이제 bash 창 내에서 bash를 시작할 때 정상적으로 실패 합니다.
- Interop가 LxFs 아래의 작업 디렉터리에 액세스할 수 없는 경우 오류 메시지가 추가 되었습니다 (예: .bashrc).
- WSL에서 Windows 경로가 잘린 문제 해결
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 690 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 274 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>빌드 14986

빌드 14986에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- Netlink 및 인 pty IOCTLs를 사용 하 여 버그 검사 수정
- 이제 커널 버전은 4.4.0를 보고 합니다. Xenial를 사용 하 여 일관성을 유지 합니다.
- 이제 Bash가 ' nul: ' (GH #1259)으로 전달 되 면 시작 됩니다.
- 이제 스레드 Id가 procfs에서 올바르게 보고 됨 (GH #967)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 플래그는 이제 inotify_add_watch () (GH #1280)에서 지원 됩니다.
- Timer_create 및 관련 시스템 호출을 구현 합니다.  이를 통해 GH (#307)를 지원 합니다.
- Ping이 0.000 m 시간을 반환 하는 문제 해결 (GH #1296)
- 너무 많은 파일이 열려 있으면 올바른 오류 코드를 반환 합니다.
- 인터페이스의 하드웨어 주소가 32 바이트 (예: Teredo 인터페이스) 인 경우 EINVAL를 사용 하 여 네트워크 인터페이스 데이터에 대 한 Netlink 요청이 실패 하는 WSL의 문제를 해결 함
   - Linux "ip" 유틸리티에는 WSL에서 32 바이트 하드웨어 주소를 보고 하는 경우 충돌 하는 버그가 포함 되어 있습니다. 이는 WSL이 아니라 "ip"의 버그입니다. "Ip" 유틸리티는 하드웨어 주소를 인쇄 하는 데 사용 되는 문자열 버퍼의 길이를 하드 코딩 하 고, 버퍼가 너무 작아서 32 바이트 하드웨어 주소를 인쇄할 수 없습니다.
- 추가 수정 사항 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 669 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>빌드 14971

빌드 14971에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

 - 이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

### <a name="ltp-results"></a>LTP 결과:
14965에서 변경 되지 않음 </br>
통과 한 테스트 수: 664 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>빌드 14965

빌드 14965에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- Netlink sockets NETLINK_ROUTE 프로토콜의 RTM_GETLINK 및 RTM_GETADDR에 대 한 지원 (GH #468)
  - 네트워크 열거에 대해 ifconfig 및 ip 명령을 사용 하도록 설정 합니다.
  - 자세한 내용은 [Wsl 네트워킹 블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)에서 찾을 수 있습니다.

- /sbin는 이제 기본적으로 사용자의 경로에 있습니다.
- 이제 NT 사용자 경로가 기본적으로 WSL 경로에 추가 됩니다. 즉, Linux 경로에 System32를 추가 하지 않고 notepad.exe를 입력할 수 있습니다.
- /Proc/sys/kernel/cap_last_cap에 대 한 지원이 추가 됨
- 현재 작업 디렉터리에 비 ansi 문자 (GH #1254)가 포함 되어 있으면 이제 WSL에서 NT 이진 파일을 시작할 수 있습니다.
- 연결 되지 않은 unix 스트림 소켓에서 종료를 허용 합니다.
- PR_GET_PDEATHSIG에 대 한 지원이 추가 되었습니다.
- CLONE_PARENT에 대 한 지원이 추가 됨
- 파이프가 중단 되는 오류 (예: bash-c "ls-alR/" |)를 수정 했습니다. bash-c "cat" (GH #1214)
- 현재 터미널에 연결 하는 요청을 처리 합니다.
- /Proc/<pid>/oom_score_adj을 쓰기 가능으로 표시 합니다.
- /Sys/fs/cgroup 폴더를 추가 합니다.
- sched_setaffinity은 선호도 비트 마스크의 수를 반환 해야 합니다.
- 인터프리터 경로를 잘못 가정 하는 ELF 유효성 검사 논리는 64 자 미만 이어야 합니다. (GH #743)
- Open file 설명자는 콘솔 창을 열어 둘 수 있습니다 (GH #1187).
- Fixeed ()가 대상 이름에 후행 슬래시를 사용 하 여 실패 한 경우 오류 (GH #1008)
- /Proc/net/dev 구현
- 타이머 해상도로 인해 0.000 ms ping을 수정 했습니다.
- 구현 된/proc/self/environ (GH #730)
- 추가 버그 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 664 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>빌드 14959

빌드 14959에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- Windows에 대 한 Pico 프로세스 알림이 개선 되었습니다.  [Wsl 블로그에서](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)추가 정보를 찾을 수 있습니다.
- Windows 상호 운용성으로 향상 된 안정성
- EDP (엔터프라이즈 데이터 보호)를 사용 하는 경우 bash를 시작할 때 0x80070057 오류 해결
- 추가 버그 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>빌드 14955

빌드 14955에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

 - 이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>빌드 14951

빌드 14951에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)를 참조 하십시오.<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>새 기능: Windows/Ubuntu 상호 운용성
이제 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.  이렇게 하면 사용자에 게 Windows 환경 및 시스템과 상호 작용할 수 있는 방법이 제공 되지 않습니다.  이제 사용자가 다음 명령을 실행할 수 있습니다.

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

자세한 내용은 다음 위치에서 찾을 수 있습니다.

- [Interop 용 WSL 팀 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop 설명서](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>고정

- 이제 모든 새 WSL 인스턴스에 Ubuntu 16.04 (Xenial)이 설치 됩니다.  T (기존 14.04) 인스턴스가 있는 사용자는 자동으로 업그레이드 되지 않습니다.
- 설치 중에 설정 된 로캘이 이제 표시 됩니다.
- WSL 프로세스를 파일로 리디렉션하는 버그를 포함 하 여 터미널의 향상 된 기능은 항상 작동 하지 않습니다.
- 콘솔 수명은 bash 수명에 연결 되어야 합니다.
- 콘솔 창 크기는 버퍼 크기가 아닌 표시 크기를 사용 해야 합니다.
- 추가 버그 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>빌드 14946

빌드 14946에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- 공백이 나 따옴표를 포함 하는 NT 사용자 이름을 가진 사용자에 대해 WSL 사용자 계정을 만들지 못하게 하는 문제를 해결 했습니다. 
- 상태에서 디렉터리의 링크 수에 대해 0을 반환 하도록 VolFs 및 DrvFs를 변경 합니다.
- IPV6_MULTICAST_HOPS socket 옵션을 지원 합니다.
- Tty 당 단일 콘솔 i/o 루프로 제한 합니다. 예: 다음과 같은 명령을 사용할 수 있습니다.
  - bash-c "echo data" | bash-c "ssh user@example.com ' cat > foo .txt '"

- /proc/cpuinfo (GH #1115)에서 공백을 탭으로 바꿉니다.
- 이제 DrvFs이 탑재 된 Windows 볼륨과 일치 하는 이름으로 mountinfo에 표시 됩니다.
- 이제/home 및/root가 올바른 이름의 mountinfo에 표시 됩니다.
- 추가 버그 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>빌드 14942

빌드 14942에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- SSH를 차단 하는 "NOEXECUTE 메모리의 실행을 시도 했습니다." 라는 네트워킹 충돌을 포함 하 여 해결 된 많은 버그 검사
- DrvFs의 Windows 응용 프로그램에서 생성 된 알림에 대 한 inotifiy 지원은 현재
- Mongod에 대해 TCP_KEEPIDLE 및 TCP_KEEPINTVL를 구현 합니다. (GH #695)
- Pivot_root 시스템 호출을 구현 합니다.
- SO_DONTROUTE에 대 한 소켓 옵션 구현
- 추가 버그 수정 및 개선 사항


### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>빌드 14936

빌드 14936에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)를 참조 하십시오.<br/>


참고: WSL은 향후 릴리스에서 Ubuntu 14.04 (t) 대신 Ubuntu 16.04 (Xenial)을 설치 합니다.  이 변경 내용은 새 인스턴스 (lxrun/install 또는 먼저 bash를 실행)를 설치 하는 참가자에 게 적용 됩니다.  T를 사용 하는 기존 인스턴스는 자동으로 업그레이드 되지 않습니다. 사용자는 릴리스-업그레이드 명령을 사용 하 여 t 이미지를 Xenial로 업그레이드할 수 있습니다.

### <a name="known-issue"></a>알려진 문제
WSL에서 일부 소켓 구현에 문제가 발생 했습니다.  버그 확인은 "NOEXECUTE 메모리의 실행을 시도 했습니다." 라는 오류와 함께 중단 됩니다.  이 문제의 가장 일반적인 노력 ssh를 사용할 때 발생 하는 충돌입니다.  근본 원인은 내부 빌드에서 고정 되 고, 가장 빠른 기회에서 참가자에 게 푸시됩니다.

### <a name="fixed"></a>고정

- Chroot 시스템 호출을 구현 합니다.
- ~~DrvFs의 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원을 포함 하는~~ inotify의 향상 된 기능
  - 수정 지금은 Windows 응용 프로그램에서 시작 되는 변경 내용에 대 한 Inotify 지원 되지 않습니다.
- I p v 6에 대<port n> 한 소켓 바인딩: 이제 IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)를 지원 합니다.
- Waitid systemcall의 WNOWAIT 동작 (GH #638)
- IP_HDRINCL 및 IP_TTL IP 소켓 옵션에 대 한 지원
- 길이가 0 인 읽기 ()는 즉시 반환 되어야 합니다 (GH #975).
- Tar 파일에 NULL 종결자를 포함 하지 않는 파일 이름 및 파일 이름 접두사를 올바르게 처리 합니다.
- /dev/snull에 대 한 epoll 지원
- Fix/vrhtime 원본 수정
- Bash-c 이제 파일로 리디렉션할 수 있습니다.
- 추가 버그 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 664 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 264 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>빌드 14931

빌드 14931에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

 - 이러한 상황 때문에 Linux 용 Windows 하위 시스템에 대 한이 빌드에 업데이트가 없습니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

<br/>

## <a name="build-14926"></a>빌드 14926

빌드 14926에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정

- 이제 Ping은 관리자 권한이 없는 콘솔에서 작동 합니다.
- 이제 Ping6이 지원 됩니다 (관리자 권한 없음).
- WSL을 통해 수정 된 파일에 대 한 Inotify 지원. (GH #216)
  - 지원 되는 플래그:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - 이벤트 inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 출력 읽기: LX_IN_ISDIR, LX_IN_IGNORED
  - 알려진 문제: Windows 응용 프로그램에서 파일을 수정 해도 이벤트가 생성 되지 않음
- 이제 Unix 소켓이 SCM_CREDENTIALS을 지원 합니다.

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 651 </br>
전달 되지 않는 (실패, 건너뜀 등)의 수입니다. 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>빌드 14915

빌드 14915에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
-  GH #262 (unix 데이터 그램 소켓) 용 socketpair
- SO_REUSEADDR에 대 한 Unix 소켓 지원
- SO_BROADCAST에 대 한 UNIX 소켓 지원 (GH #568)
- SOCK_SEQPACKET에 대 한 Unix 소켓 지원 (GH #758, #546)
- Unix 데이터 그램 소켓 전송, 수신 및 종료에 대 한 지원 추가
- 고정 되지 않은 주소에 대 한 잘못 된 mmap 매개 변수 유효성 검사로 인해 버그 확인을 수정 합니다. (GH #847)
- 터미널 상태의 일시 중단/다시 시작에 대 한 지원
- 화면 유틸리티 (GH #774)의 차단을 해제 하는 TIOCPKT ioctl 지원
    - 알려진 문제: 작동 하지 않는 기능 키
- LxpTimerFdWorkerRoutine (GH #814)에서 해제 된 멤버 ' ReaderReady '에 액세스할 수 있는 타이머를 수정 했습니다.
- Futex, 설문 조사 및 clock_nanosleep에 대 한 다시 시작 가능한 시스템 호출 지원
- 추가 된 바인드 탑재 지원
- 탑재 네임 스페이스 지원에 대 한 공유 해제
    - 알려진 문제: 현재 작업 디렉터리로 새 탑재 네임 스페이스 `unshare(CLONE_NEWNS)` 를 만들 때 이전 네임 스페이스를 계속 가리키도록 합니다.
- 추가 개선 사항 및 버그 수정

<br/>

## <a name="build-14905"></a>빌드 14905

빌드 14905에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 이제 다시 시작 가능한 시스템 호출이 지원 됩니다 (GH #349, GH #520).
- Symlink (GH #650)로 끝나는 디렉터리
- /Sv/svvvvvhu에 대해 구현 된 RNDGETENTCNT ioctl
- /Proc/[pid]/탑재,/proc/[pid]/mountinfo 및/proc/[pid]/mountstats 파일을 구현 합니다.
- 추가 버그 수정 및 개선 사항

</br>

## <a name="build-14901"></a>빌드 14901
사후 Windows 10 기념일 업데이트 릴리스에 대 한 첫 번째 Insider build.

빌드 14901에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 후행 슬래시 문제를 수정 했습니다.
    - 이제와 `$ mv a/c/ a/b/` 같은 명령이 작동 합니다.
- 이제 Ubuntu 로캘을 Windows 로캘로 설정 해야 하는지 여부를 묻는 메시지가 표시 됩니다.
- Ns 폴더에 대 한 procfs 지원
- Tmpfs, procfs 및 sysfs 파일 시스템에 대 한 탑재 및 탑재 해제 추가 됨
- Fix mknod [at] 32 비트 ABI 서명
- 발송 모델로 이동 하는 Unix 소켓
- Setsockopt를 사용 하 여 설정 된 INET 소켓 수신 버퍼 크기를 적용 해야 합니다.
- MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그 구현
- Linux process stdin/stdout 파이프 리디렉션 (GH #2)
    - CMD에서 bash-c 명령의 파이프를 허용 합니다.  예: > dir | bash-c "grep foo"
- 이제 여러 개의 탭이 있는 시스템에 Bash를 설치할 수 있습니다 (GH #538, #358).
- 기본 INET 소켓 버퍼 크기는 기본 Ubuntu 설정의 크기와 일치 해야 합니다.
- Xattr syscall을 listxattr에 맞춥니다.
- SIOC.GIF 회의의 유효한 IPv4 주소가 있는 인터페이스만 반환 합니다.
- Ptrace에서 삽입 하는 경우 신호 기본 작업 수정
- /proc/sys/vm/min_free_kbytes 구현
- Sigreturn에서 컨텍스트를 복원 하는 경우 컴퓨터 컨텍스트 레지스터 값 사용
    - 이는 일부 사용자에 대해 java 및 javac이 중단 된 문제를 해결 합니다.
- /Proc/sys/kernel/hostname 구현

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Windows 10 기념일 업데이트에 14388 빌드
빌드 14388에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/14388wip)를 참조 하십시오. <br/>

### <a name="fixed"></a>고정
- 8/2에 대 한 Windows 10 기념일 업데이트 준비에 대 한 수정
  - 기념일 업데이트의 WSL에 대 한 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/wsl/) 를 참조 하세요.

<br/>

## <a name="build-14376"></a>빌드 14376
빌드 14376에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)를 참조 하십시오. <br/>

### <a name="fixed"></a>고정
- Apt-get이 중단 되는 일부 인스턴스 제거 (GH #493)
- 빈 탑재를 올바르게 처리 하지 않는 문제를 해결 함
- 지 각 디스크가 올바르게 탑재 되지 않은 문제를 수정 했습니다.
- 지원 되는 unix 소켓 수락 플래그 (부분 GH #451)
- 일반적인 네트워크 관련 블루 스크린 수정
- /Proc/[pid]/task (GH #523)에 액세스할 때 블루 스크린을 수정 했습니다.
- 일부 인 pty 시나리오에 대 한 높은 CPU 사용률 (GH #488, #504)을 수정 했습니다.
- 추가 버그 수정 및 개선 사항

<br/>

## <a name="build-14371"></a>빌드 14371
빌드 14371에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)를 참조 하십시오. <br/>

### <a name="fixed"></a>고정
- Ptrace를 사용 하는 경우 SIGCHLD 및 wait ()로 타이밍 경합을 수정 했습니다.
- 경로에 후행/(GH #432)가 있는 경우 몇 가지 동작을 수정 했습니다.
- 자식에 대 한 열린 핸들로 인해 이름 바꾸기/연결 해제 실패 문제가 해결 됨
- 추가 버그 수정 및 개선 사항

<br/>

## <a name="build-14366"></a>빌드 14366
빌드 14366에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)를 참조 하십시오. <br/>

### <a name="fixed"></a>고정
- Symlink를 통한 파일 생성 수정
-   Python에 대 한 listxattr 추가 (GH 385)
-   추가 버그 수정 및 개선 사항

### <a name="syscall-support"></a>Syscall 지원
-   다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>빌드 14361
빌드 14361에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14361)를 참조 하십시오. <br/>

### <a name="fixed"></a>고정
- DrvFs는 Windows의 Ubuntu에서 Bash로 실행 될 때 대/소문자를 구분 합니다.
  - 사용자는 .txt와 CASE를 입력할 수 있습니다. /Mnt/c 드라이브의 TXT
  - 대/소문자 구분은 Windows의 Ubuntu에 있는 Bash 내 에서만 지원 됩니다. Bash를 벗어난 NTFS에서 파일을 올바르게 보고 하지만 Windows의 파일과 상호 작용 하는 경우 예기치 않은 동작이 발생할 수 있습니다.
  - 각 볼륨의 루트 (예:/mnt/c)는 대/소문자를 구분 하지 않습니다.
  - Windows에서 이러한 파일을 처리 하는 방법에 대 한 자세한 내용은 [여기](https://support.microsoft.com/en-us/kb/100625)를 참조 하세요.
- 매우 향상 된 인 pty/tty 지원.  현재 TMUX와 같은 응용 프로그램 지원 (GH #40)
- 사용자 계정이 항상 만들어지지 않는 문제를 해결 했습니다.
- 매우 긴 인수 목록을 허용 하는 최적화 된 명령줄 인수 구조입니다. (GH #153)
- 이제 DrvFs에서 삭제할 수 있고 chmod read_only 파일
- 연결이 끊어질 때 터미널이 중단 되는 일부 인스턴스 (GH #43)를 수정 했습니다.
- chmod 및 chown가 이제 tty 장치에서 작동
- 0\.0.0.0 및::에서 localhost로 연결 허용 (GH #388)
- Sendmsg/recvmsg는 이제 > 1 (부분 GH #376)의 IO 벡터 길이를 처리 합니다.
- 사용자는 이제 자동 생성 된 호스트 파일 (GH #398)을 옵트아웃 (opt out) 할 수 있습니다.
- 설치 하는 동안 자동으로 Linux 로캘을 NT 로캘로 일치 (GH #11)
- /Proc/sys/vm/swappiness 파일 (GH #306)을 추가 했습니다.
- 이제 strace가 제대로 종료 됩니다.
- /Proc/self/fd를 통해 파이프를 다시 열 수 있도록 허용 (GH #222)
- DrvFs에서%LOCALAPPDATA%\lxss 아래의 디렉터리 숨기기 (GH #270)
- Bash ~를 효율적으로 처리 합니다.  "Bash ~-c ls"와 같은 명령이 지원 됩니다 (GH #467).
- 이제 소켓에서 종료 하는 동안 epoll 읽기를 사용할 수 있음을 알립니다 (GH #271).
- lxrun/uninstall은 파일 및 폴더를 삭제 하는 작업을 더 효율적으로 수행 합니다.
- GH (#246)를 수정 했습니다.
- XEmacs (GH #481)와 같은 x11 앱에 대 한 지원 향상
- 기본 Ubuntu 설정과 일치 하도록 초기 스레드 스택 크기를 업데이트 하 고 get_rlimit syscall (GH #172, #258)에 대 한 크기를 올바르게 보고 합니다.
- Pico 프로세스 이미지 이름 (예: 감사)의 보고 기능 향상
- Df 명령에 대해/proc/mountinfo 구현 됨
- 자식 이름에 대 한 symlink 오류 코드를 수정 했습니다. 및입니다.
- 추가 개선 사항에 대 한 수정 및 개선 사항

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>빌드 14352
빌드 14352에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14352)를 참조 하십시오.<br/>


### <a name="fixed"></a>고정
- 대량 파일이 다운로드/생성 되지 않은 문제를 해결 했습니다.  Npm 및 기타 시나리오를 차단 해제 해야 합니다 (GH #3, GH #313).
- 소켓이 중단 된 일부 인스턴스 제거
- 일부 ptrace 오류 수정 됨
- 255 자 보다 긴 파일 이름을 허용 하는 WSL의 문제를 해결 함
- 영어가 아닌 문자에 대 한 지원 향상
- 현재 Windows 표준 시간대 데이터를 추가 하 고 기본값으로 설정
- 각 탑재 지점에 대 한 고유한 장치 id (jre fix – GH #49)
- "."를 포함 하는 경로에 대 한 문제를 해결 합니다. 및 "."
- Fifo 지원 추가 (GH #71)
- 네이티브 Ubuntu 형식에 맞게 resolv.conf의 업데이트 된 형식
- 일부 procfs 정리
- 관리자 콘솔에 대해 ping을 사용 하도록 설정 (GH #18)

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>빌드 14342
빌드 14342에 대 한 일반 Windows 정보는 [Windows 블로그](https://aka.ms/wip14342)를 통해 설명 합니다. <br/>

VolFs 및 드라이브 Fs에 대 한 정보는 [Wsl 블로그](https://blogs.msdn.microsoft.com/wsl)에서 찾을 수 있습니다. <br/>

### <a name="fixed"></a>고정
- Windows 사용자 이름에 유니코드 문자가 있는 경우의 설치 문제 해결
- 이제 FAQ의 apt 업데이트 udev 해결 방법이 기본적으로 처음 실행 될 때 제공 됩니다.
- Symlink fs (/mnt/<drive>) 디렉터리에서 사용 하도록 설정 됨
- 이제 symlink fs와 VolFs 간에 작업
- 주소가 지정 된 최상위 경로 구문 분석 문제가 발생 했습니다.//이제 정상적으로 작동 합니다.
- 드라이브의 npm 설치 및-g 옵션이 이제 작동 합니다.
- PHP 서버가 시작 되지 않도록 하는 문제 해결
- 네이티브 Ubuntu와 더 가까운 일치를 위해 $PATH와 같은 업데이트 된 기본 환경 값
- Windows에서 apt 패키지 캐시를 업데이트 하기 위한 주간 유지 관리 작업 추가
- ELF 헤더 유효성 검사와 관련 된 문제가 해결 되었습니다. 이제 WSL은 모든 Melkor 옵션을 지원 합니다.
- Zsh shell이 작동 합니다.
- 미리 컴파일된 이동 이진 파일이 이제 지원 됩니다.
- Bash에 대 한 확인 메시지가 이제 올바르게 지역화 됨
- /proc/meminfo는 이제 올바른 정보를 반환 합니다.
- 이제 지원 되는 소켓이 VFS에서 지원 됩니다.
- /sdev는 이제 tempfs로 탑재 되었습니다.
- 이제 Fifo 지원 됨
- 이제 다중 코어 시스템이/proc/cpuinfo에서 올바르게 표시 됩니다.
- 처음 실행 하는 동안 다운로드 한 추가 개선 사항 및 오류 메시지
- 향상 된 기능 및 버그 수정을 Syscall. 아래 지원 되는 syscall 목록입니다.
- 추가 버그 수정 및 개선 사항

### <a name="known-issues"></a>알려진 문제
- '.. '을 (를) 확인 하지 않습니다. 일부 경우에는 드라이브에서 올바르게 설정

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새로운 또는 향상 된 syscall의 목록입니다. 이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

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

빌드 14332에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14332)를 참조 하십시오. <br/>


### <a name="fixed"></a>고정
- DNS 항목 우선 순위를 포함 하는 resolv.conf 향상
- /Mnt 및 비/mnt 드라이브 간에 파일 및 디렉터리를 이동 하는 문제
- 이제 symlink를 사용 하 여 Tar 파일을 만들 수 있습니다.
- 인스턴스를 만들 때 기본/run/lock 디렉터리를 추가 했습니다.
- 적절 한 상태 정보를 반환 하기 위해/sv/svnull 업데이트
- 처음 실행 하는 동안 다운로드할 때 추가 오류 발생
- 향상 된 기능 및 버그 수정을 Syscall. 아래 지원 되는 syscall 목록입니다.
- 추가 개선 사항에 대 한 수정 및 개선 사항

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 새 syscall. 이 목록에 있는 syscall는 하나 이상의 시나리오에서 지원 되지만 지금은 지원 되는 매개 변수가 없을 수 있습니다.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>빌드 14328

빌드 14332에 대 한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14328)를 참조 하십시오. <br/>


### <a name="new-features"></a>새로운 기능
* 이제 Linux 사용자를 지원 합니다.  Windows에서 Ubuntu에 Bash를 설치 하면 Linux 사용자를 만들라는 메시지가 표시 됩니다.  자세한 내용은 다음을 참조 하세요. https://aka.ms/wslusers
* 이제 호스트 이름이 Windows 컴퓨터 이름으로 설정 되어 있습니다.@localhost
* 빌드 14328에 대 한 자세한 내용은 다음을 참조 하세요. https://aka.ms/wip14328

### <a name="fixed"></a>고정
* 비/mnt/<drive> 파일에 대 한 Symlink 향상
    * npm 설치 이제 작동
    * 이제 jdk/jre에서 [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)에 있는 지침을 사용 하 여 설치할 수 있습니다.
    * 알려진 문제: Windows 탑재에 대해 symlink가 작동 하지 않습니다.  이후 빌드에서 기능을 사용할 수 있습니다.
* 위쪽 및 htop 이제 표시
* 일부 설치 오류에 대 한 추가 오류 메시지
* 향상 된 기능 및 버그 수정을 Syscall.  아래 지원 되는 syscall 목록입니다.
* 추가 개선 사항에 대 한 수정 및 개선 사항

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 일부 구현을 포함 하는 syscall 목록입니다.  이 목록의 syscall는 하나 이상의 시나리오에서 지원 되지만 현재 지원 되는 매개 변수가 없을 수 있습니다.

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
