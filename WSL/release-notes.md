---
title: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보
description: Linux 용 Windows 하위 시스템에 대 한 릴리스 정보입니다.  매주 업데이트 합니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem ubuntu 용 windows 하위 시스템
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988258"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에 대 한 릴리스 정보

## <a name="build-18890"></a>18890 빌드
일반 Windows에 대 한 18890 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)합니다.

### <a name="wsl"></a>WSL
* 비블로킹 소켓 누수 [GH 2913]
* EOF 입력 터미널에 후속 읽기 [GH 3421]를 차단할 수 있습니다.
* [GH 3928 설명] wsl.conf를 가리키도록 업데이트 하기 위해 resolv.conf 헤더
* Epoll의 교착 상태 [GH 3922] 코드를 삭제 합니다.
* -가져오고 내보내고-[GH 3932]에 대 한 인수에서 공백 처리
* Mmap 확장 파일은 제대로 작동 하지 않습니다 [GH 3939]
* ARM64를 사용 하 여 문제를 해결 \\wsl$ 액세스 제대로 작동 하지 않습니다
* 추가 wsl.exe에 대 한 더 나은 기본 아이콘

## <a name="build-18342"></a>18342 빌드
일반 Windows에 대 한 18342 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)합니다.

### <a name="wsl"></a>WSL
* Windows에서 Linux 파일 WSL 배포판에 액세스 하려면 사용자가 기능을 추가 했습니다. 명령줄 및 또한 파일 탐색기와 VSCode Windows 앱을 통해 이러한 파일에 액세스할 수 있습니다, 그리고 등 이러한 파일을 사용 하 여 상호 작용할 수 있습니다. 로 이동 하 여 파일에 액세스할 \\ \\wsl$\\< distro_name >로 이동 하 여 배포를 실행 중인 목록을 보거나 \\ \\wsl$
* CPU 정보 태그를 추가 하 고 [GH 2234] Cpus_allowed [목록 (_l)] 값 수정
* [GH 3800] 리더가 아닌 스레드에서 exec를 지원 합니다.
* 치명적이 지 않은 [GH 3785]으로 구성 업데이트 오류 처리
* 오프셋 [GH 3768]를 적절히 처리할 binfmt 업데이트
* 계획 9 [GH 3854]에 대 한 매핑 네트워크 드라이브를 사용 하도록 설정
* 지원 Windows Linux 및 Linux에 바인드 바 운 트에서 대 한 Windows 경로 번역->
* 읽기 전용으로 열려 있는 파일의 매핑에 대 한 읽기 전용 섹션 만들기

## <a name="build-18334"></a>18334 빌드
일반 Windows에 대 한 18334 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)합니다.

### <a name="wsl"></a>WSL
* Windows 표준 시간대 [GH 3747] Linux 표준 시간대로 매핑되는 방식을 다시 디자인
* 메모리 누수를 해결 하 고 새로운 문자열 변환 함수 [GH 3746]를 추가 합니다.
* threadgroup이 없는 스레드를 사용 하 여에서 SIGCONT가 no-op [GH 3741] 
* /Proc/self/fd에서 소켓 및 epoll 파일 설명자를 올바르게 표시

## <a name="build-18305"></a>18305 빌드
일반 Windows에 대 한 18305 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)합니다.

### <a name="wsl"></a>WSL
* 주 스레드가 종료 [GH 3589] pthread 파일에 대 한 액세스 권한을 상실합니다
* 필요한 경우에 TIOCSCTTY "force" 매개 변수를 무시 해야 [GH 3652]
* wsl.exe 명령줄 향상 된 기능 및 추가 가져오기/내보내기 기능.
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

## <a name="build-18277"></a>18277 빌드
일반 Windows에 대 한 18277 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)합니다.

### <a name="wsl"></a>WSL
* 빌드 [GH 3645] 18272에에서 도입 된 "인터페이스" 오류 해결
* Umount syscall [GH 3605]에 대 한 MNT_FORCE 플래그를 무시 합니다.
* WSL 공식 CreatePseudoConsole API를 사용 하는 interop 전환
* FUTEX_WAIT 다시 시작 될 때 시간 제한 값을 유지 관리

## <a name="build-18272"></a>18272 빌드
일반 Windows에 대 한 18272 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)합니다.

### <a name="wsl"></a>WSL
* **경고:** WSL 작동 하지 않습니다는이 빌드에는 문제가 없습니다. 배포를 시작 하려고 할 때 "인터페이스" 오류가 표시 됩니다. 문제가 해결 되었습니다 및 다음 주 Insider 빠른 빌드에 포함 됩니다. 이전에 설치한 경우 롤백할 수 있습니다 "이전 버전의 Windows 10으로 다시 이동"을 사용 하 여 이전 Windows 빌드 설정에서이 빌드에는 업데이트-> & 보안 복구-> 합니다.

## <a name="build-18267"></a>18267 빌드
일반 Windows에 대 한 18267 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)합니다.

### <a name="wsl"></a>WSL
* 좀비 프로세스 수 없습니다 수 했지만 누릴 수 있었습니다 않았고 무기한으로 문제를 해결 합니다.
* WslRegisterDistribution 오류 메시지 [GH 3592]는 최대 길이 초과 하는 경우 중단 됩니다.
* 읽기 전용 파일 DrvFs [GH 3556]에 대 한 성공 하려면 fsync 허용
* [GH 3584] 내부 symlink를 만들기 전에 /bin 및 /sbin 디렉터리가 존재 하는지 확인
* WSL 인스턴스에 대 한 인스턴스 종료 제한 시간 메커니즘을 추가 합니다. 제한 시간을 15 초로, 인스턴스가 15 초 마지막 WSL 프로세스가 종료 된 후 종료 됩니다 즉 현재 설정 됩니다. 배포를 즉시 종료 하려면 다음을 사용 합니다.
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>17763 빌드 (1809)
일반 Windows에 대 한 17763 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)합니다.

### <a name="wsl"></a>WSL
* 동일한 스레드 우선 순위 [GH 1838] 변경에 대 한 너무 엄격한 Setpriority syscall 권한 확인
* Clock_gettime(CLOCK_BOOTTIME) [GH 3434]에 대해 음수 값을 반환 하지 않으려면 비편향된 인터럽트 시간 비율 부팅 시간에 사용 되는지 확인
* WSL binfmt 인터프리터 [GH 3424]에서 symlink를 처리 합니다.
* Threadgroup이 리더 파일 설명자 정리 보다 효율적으로 처리 합니다.
* WSL 데 KeQueryInterruptTimePrecise KeQueryPerformanceCounter 대신 [GH 3252] 오버플로가 발생 하지 않도록 전환
* Ptrace 연결 월 [GH 1731] 시스템 호출에서 잘못 된 반환 값이 발생
* 여러 AF_UNIX 관련 된 수정 사항을 문제 [GH 3371]
* WSL interop 현재 작업 디렉터리를 5 대 미만의 자 [GH 3379] 이면 실패를 일으킬 수 있는 문제 해결
* 존재 하지 않는 포트 [GH 3286]에 대 한 루프백 연결 실패 한 두 번째 지연을 방지합니다
* /Proc/sys/fs/file-max 스텁 파일 [GH 2893]를 추가 합니다.
* 보다 정확 하 게 IPV6 범위 정보입니다.
* PR_SET_PTRACER 지원 [GH 3053]
* 실수로 epoll edge 트리거 이벤트 [GH 3276]의 선택을 취소 하는 파이프 파일 시스템
* Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.
* 향상 된 좀비 지원 [GH 1353]
* [GH 1493] Windows interop 동작을 제어 하기 위한 wsl.conf 항목 추가
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 항상 그렇지는 않음 UNIX 소켓 패밀리 형식을 [GH 1774]를 반환 하는 getsockname에 대 한 수정
* TIOCSTI [GH 1863]에 대 한 지원 추가
* 비블로킹 소켓 연결 중 쓰기 시도 [GH 2846] EAGAIN 반환할지
* 탑재 된 Vhd [GH 3246에 3291]에서 interop를 지원 합니다.
* 루트 폴더 [GH 3304]에서 문제를 확인 하는 사용 권한 수정
* TTY 키보드 ioctl KDGKBTYPE, KDGKBMODE 및 KDSKBMODE 제한적으로 지원 합니다.
* Windows UI 응용 프로그램은 백그라운드에서 시작 하는 경우에 실행 해야 합니다.
* Wsl-u 또는--사용자 옵션 [GH 1203] 추가
* 빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]
* Unix 소켓 연결이 끊긴된 피어 자격 증명 [GH 3183]를 유지 해야 합니다.
* EAGAIN [GH 3191]를 사용 하 여 무기한 실패 무중단 Unix 소켓
* 대/소문자 = off는 새 기본 drvfs 탑재 [GH 2937, 3212, 3328] 형식
    * 참조 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 자세한 내용은 합니다.
* 배포 실행을 중지 하려면 종료/wslconfig를 추가 합니다.
* 공간을 사용 하 여 경로 올바르게 처리 하지 않는 메뉴 항목 WSL 셸 컨텍스트를 사용 하 여 문제를 해결 합니다.
* 확장된 특성으로 단위 디렉터리에 대/소문자 구분. 노출
* ARM64: 캐시 유지 관리 작업을 에뮬레이트하십시오. 확인할 [dotnet 문제](https://github.com/dotnet/core/issues/1561)합니다.
* DrvFs: 개인 범위에 해당 하는 문자는 이스케이프 된 문자는 이스케이프을 해제 합니다.
* ELF 파서 인터프리터 길이 유효성 검사 [GH 3154]에서 해제-오류 해결
* 과거의 시간을 사용 하 여 WSL 절대 타이머 [GH 3091] 실행 안 함
* 새로 만든된 재분석 지점을 부모 디렉터리에 따라서 나와 확인 합니다.
* 원자 단위로 DrvFs에서 대/소문자 구분 디렉터리를 만듭니다.
* 추가 문제를 해결 하 고 다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 키를 누릅니다. [GH 2712]
* 고정된 WSL UMCI을 사용 하는 경우 오류를 시작 합니다. [GH 3020]
* WSL [GH 437 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다. 를 사용 하려면 shift 키를 누르고 및 탐색기 창에서 마우스 오른쪽 단추로 클릭 합니다.
* Unix 소켓 비차단 동작 [GH 2822, 3100] 수정
* GH 2026에 보고 된 NETLINK 명령을 중지를 수정 합니다.
* 탑재 전파 플래그 [GH 2911]에 대 한 지원을 추가 합니다.
* 자르기 유발 하지 inotify 이벤트 [GH 2978]를 사용 하 여 문제를 해결 합니다.
* 추가-셸 없이 단일 바이너리를 호출 하는 wsl.exe exec 옵션입니다.
* 추가-특정 배포판을 선택 하려면 wsl.exe에 대 한 배포 옵션입니다.
* Dmesg 제한적으로 지원 합니다. 응용 프로그램 dmesg를 로깅할 수 있습니다. WSL 드라이버 dmesg를 제한 된 정보를 기록합니다. 나중에이 드라이버에서 다른 정보/진단 전달할 확장할 수 있습니다.
    * 참고: dmesg를 통해 현재 지원 되는 `/dev/kmsg` 장치 인터페이스입니다. `syslog` syscall 인터페이스 아직 지원 되지 않습니다. 따라서 몇 가지는 `dmesg` 명령줄 옵션 등 `-S`, `-C` 작동 하지 않습니다.
* 기본 gid 및 네이티브 [GH 3042]에 맞게 직렬 장치 모드 변경
* 이제 DrvFs 확장 된 특성을 지원합니다.
    * 참고: DrvFs 확장 된 특성의 이름에 몇 가지 제한 사항이 있습니다. 일부 문자 (같은 '/', ':' 및 '\*') 허용 되지 않습니다 되며 확장 특성 이름은 대/소문자 구분 DrvFs에서 하지 않습니다.

## <a name="build-18252-skip-ahead"></a>빌드 18252 미리 건너 뛰 세요.
일반 Windows에 대 한 18252 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)합니다.

### <a name="wsl"></a>WSL
* Init 및 bsdtar 바이너리 lxssmanager dll를 별도 도구 폴더로 이동 합니다.
* 경합 CLONE_FILES를 사용 하는 경우 파일 설명자를 닫기 주위를 수정 합니다.
* DrvFs 경로 변환할 때 /proc/pid/mountinfo에 선택적 필드를 처리 합니다.
* S_IFREG에 대 한 메타 데이터 지원은 되려면 DrvFs mknod 허용
* DrvFs에 만들어진 읽기 전용 파일 [GH 3411]를 설정 하는 읽기 전용 특성이 있어야 합니다.
* /Sbin/mount.drvfs DrvFs 탑재를 처리 하는 도우미를 추가 합니다.
* DrvFs의 POSIX 이름을 사용 합니다.
* 볼륨 GUID 없는 볼륨에서 경로 번역을 허용 합니다.

## <a name="build-17738-fast"></a>17738 (Fast) 빌드
일반 Windows에 대 한 17738 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)합니다.

### <a name="wsl"></a>WSL
* 동일한 스레드 우선 순위 [GH 1838] 변경에 대 한 너무 엄격한 Setpriority syscall 권한 확인
* Clock_gettime(CLOCK_BOOTTIME) [GH 3434]에 대해 음수 값을 반환 하지 않으려면 비편향된 인터럽트 시간 비율 부팅 시간에 사용 되는지 확인
* WSL binfmt 인터프리터 [GH 3424]에서 symlink를 처리 합니다.
* Threadgroup이 리더 파일 설명자 정리 보다 효율적으로 처리 합니다.

## <a name="build-17728-fast"></a>17728 (Fast) 빌드
일반 Windows에 대 한 17728 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)합니다.

### <a name="wsl"></a>WSL
* WSL 데 KeQueryInterruptTimePrecise KeQueryPerformanceCounter 대신 [GH 3252] 오버플로가 발생 하지 않도록 전환
* Ptrace 연결 월 [GH 1731] 시스템 호출에서 잘못 된 반환 값이 발생
* 다양 한 AF_UNIX 관련 된 수정 사항을 문제 [GH 3371]
* WSL interop 현재 작업 디렉터리를 5 대 미만의 자 [GH 3379] 이면 실패를 일으킬 수 있는 문제 해결

## <a name="build-18204-skip-ahead"></a>빌드 18204 미리 건너 뛰 세요.
일반 Windows에 대 한 18204 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)합니다.

### <a name="wsl"></a>WSL
* Edge 트리거 epoll 이벤트 [GH 3276]의 선택을 취소 하는 파일 시스템 inadvertenly을 파이프
* Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.

## <a name="build-17723-fast"></a>17723 (Fast) 빌드
일반 Windows에 대 한 17723 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)합니다.

### <a name="wsl"></a>WSL
* 존재 하지 않는 포트 [GH 3286]에 대 한 루프백 연결 실패 한 두 번째 지연을 방지합니다
* /Proc/sys/fs/file-max 스텁 파일 [GH 2893]를 추가 합니다.
* 보다 정확 하 게 IPV6 범위 정보입니다.
* PR_SET_PTRACER 지원 [GH 3053]
* Edge 트리거 epoll 이벤트 [GH 3276]의 선택을 취소 하는 파일 시스템 inadvertenly을 파이프
* Win32 실행 파일은 NTFS symlink를 통해 시작 symlink 이름 [GH 2909]을 따르지 않습니다.

## <a name="build-17713"></a>17713 빌드
일반 Windows에 대 한 17713 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)합니다.

### <a name="wsl"></a>WSL
* 향상 된 좀비 지원 [GH 1353]
* [GH 1493] Windows interop 동작을 제어 하기 위한 wsl.conf 항목 추가
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 항상 그렇지는 않음 UNIX 소켓 패밀리 형식을 [GH 1774]를 반환 하는 getsockname에 대 한 수정
* TIOCSTI [GH 1863]에 대 한 지원 추가
* 비블로킹 소켓 연결 중 쓰기 시도 [GH 2846] EAGAIN 반환할지
* 탑재 된 Vhd [GH 3246에 3291]에서 interop를 지원 합니다.
* 루트 폴더 [GH 3304]에서 문제를 확인 하는 사용 권한 수정
* TTY 키보드 ioctl KDGKBTYPE, KDGKBMODE 및 KDSKBMODE 제한적으로 지원 합니다.
* Windows UI 응용 프로그램은 백그라운드에서 시작 하는 경우에 실행 해야 합니다.

## <a name="build-17704"></a>17704 빌드
일반 Windows에 대 한 17704 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)합니다.

### <a name="wsl"></a>WSL
* Wsl-u 또는--사용자 옵션 [GH 1203] 추가
* 빠른 시작을 사용 하는 경우 WSL 시작 문제 해결 [GH 2576]
* Unix 소켓 연결이 끊긴된 피어 자격 증명 [GH 3183]를 유지 해야 합니다.
* EAGAIN [GH 3191]를 사용 하 여 무기한 실패 무중단 Unix 소켓
* 대/소문자 = off는 새 기본 drvfs 탑재 [GH 2937, 3212, 3328] 형식
    * 참조 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 자세한 내용은 합니다.
* 배포 실행을 중지 하려면 종료/wslconfig를 추가 합니다.

## <a name="build-17692"></a>빌드 17692
일반 Windows에 대 한 17692 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)합니다.

### <a name="wsl"></a>WSL
* 공간을 사용 하 여 경로 올바르게 처리 하지 않는 메뉴 항목 WSL 셸 컨텍스트를 사용 하 여 문제를 해결 합니다.
* 확장된 특성으로 단위 디렉터리에 대/소문자 구분. 노출
* ARM64: 캐시 유지 관리 작업을 에뮬레이트하십시오. 확인할 [dotnet 문제](https://github.com/dotnet/core/issues/1561)합니다.
* DrvFs: 개인 범위에 해당 하는 문자는 이스케이프 된 문자는 이스케이프을 해제 합니다.

## <a name="build-17686"></a>빌드 17686
일반 Windows에 대 한 17686 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)합니다.

### <a name="wsl"></a>WSL
* ELF 파서 인터프리터 길이 유효성 검사 [GH 3154]에서 해제-오류 해결
* 과거의 시간을 사용 하 여 WSL 절대 타이머 [GH 3091] 실행 안 함
* 새로 만든된 재분석 지점을 부모 디렉터리에 따라서 나와 확인 합니다.
* 원자 단위로 DrvFs에서 대/소문자 구분 디렉터리를 만듭니다.

## <a name="build-17677"></a>17677 빌드
일반 Windows에 대 한 17677 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)합니다.

### <a name="wsl"></a>WSL
* 추가 문제를 해결 하 고 다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 키를 누릅니다. [GH 2712]
* 고정된 WSL UMCI을 사용 하는 경우 오류를 시작 합니다. [GH 3020]

## <a name="build-17666"></a>17666 빌드
일반 Windows에 대 한 17666 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)합니다.

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>경고: WSL에서 일부 AMD 칩셋 [GH 3134] 실행 방지 하는 문제가 없습니다. 해결 방법은 준비을 높일 해당 참가자 빌드 분기입니다.
* WSL [GH 437 603, 1836]를 시작 하려면 탐색기 상황에 맞는 메뉴를 추가 합니다. 사용 하려면 보류 shift 및 탐색기 창에서 마우스 오른쪽 단추로 클릭 합니다.
* Unix 소켓 비차단 동작 [GH 2822, 3100] 수정
* GH 2026에 보고 된 NETLINK 명령을 중지를 수정 합니다.
* 탑재 전파 플래그 [GH 2911]에 대 한 지원을 추가 합니다.
* 자르기 유발 하지 inotify 이벤트 [GH 2978]를 사용 하 여 문제를 해결 합니다.
* 추가-셸 없이 단일 바이너리를 호출 하는 wsl.exe exec 옵션입니다.
* 추가-특정 배포판을 선택 하려면 wsl.exe에 대 한 배포 옵션입니다.

## <a name="build-17655-skip-ahead"></a>빌드 17655 미리 건너 뛰 세요.
일반 Windows에 대 한 17655 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)합니다.

### <a name="wsl"></a>WSL
* Dmesg 제한적으로 지원 합니다. 응용 프로그램 dmesg를 로깅할 수 있습니다. WSL 드라이버 dmesg를 제한 된 정보를 기록합니다. 나중에이 드라이버에서 다른 정보/진단 전달할 확장할 수 있습니다.
    * 참고: dmesg를 통해 현재 지원 되는 `/dev/kmsg` 장치 인터페이스입니다. `syslog` sycall 인터페이스 아직 지원 되지 않습니다. 따라서 몇 가지는 `dmesg` 명령줄 옵션 등 `-S`, `-C` 작동 하지 않습니다.
* 다중 스레드 작업 파일에 있는 경우에 ENOENT를 반환할 수 있습니다 문제를 해결 했습니다. [GH 2712]

## <a name="build-17639-skip-ahead"></a>빌드 17639 미리 건너 뛰 세요.
일반 Windows에 대 한 17639 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)합니다.

### <a name="wsl"></a>WSL
* 기본 gid 및 네이티브 [GH 3042]에 맞게 직렬 장치 모드 변경
* 이제 DrvFs 확장 된 특성을 지원합니다.
    * 참고: DrvFs 확장 된 특성의 이름에 몇 가지 제한 사항이 있습니다. 특히, 일부 문자 (같은 '/', ':' 및 '\*') 허용 되지 않습니다 되며 확장 특성 이름은 대/소문자 구분 DrvFs에서 하지 않습니다.

## <a name="build-17133-fast"></a>17133 (Fast) 빌드
일반 Windows에 대 한 17133 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)합니다.

### <a name="wsl"></a>WSL
* WSL에서 중지를 해결 합니다. [GH 3039, 3034]

## <a name="build-17128-fast"></a>17128 (Fast) 빌드
일반 Windows에 대 한 17128 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)합니다.

### <a name="wsl"></a>WSL
* 없음

## <a name="build-17627-skip-ahead"></a>빌드 17627 미리 건너 뛰 세요.
일반 Windows에 대 한 17627 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)합니다.

### <a name="wsl"></a>WSL
* Futex pi 인식 작업에 대 한 지원을 추가 합니다. [GH 1006]
    * 우선 순위는 현재 지원 되는 WSL 기능 제한 사항이 있지만 표준 사용을 차단 해야 하므로 note 합니다.
* WSL 프로세스에 대 한 Windows 방화벽 지원 합니다. [GH 1852]
    * 예를 들어는 WSL 수 있도록 모든 포트에서 수신 대기를 관리자 권한 Windows cmd를 사용 하 여 python 처리: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 방화벽 규칙을 추가 하는 방법에 대 한 자세한 내용은 참조 하세요. [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Wsl.exe를 사용 하는 경우 사용자의 기본 셸을 따릅니다. [GH 2372]
* 모든 네트워크 인터페이스가 이더넷으로 보고 합니다. [GH 2996]
* /Etc/passwd 손상 된 파일의 향상 된 처리 합니다. [GH 3001]

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17618-skip-ahead"></a>빌드 17618 미리 건너 뛰 세요.
일반 Windows에 대 한 17618 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)합니다.

### <a name="wsl"></a>WSL
* NT interop pseudoconsole 기능 소개 [GH 988, 1366, 1433, 1542, 2370, 2406].
* 레거시 설치 메커니즘 (lxrun.exe) 더 이상 사용 되지 않습니다. Microsoft Store 통해 배포를 설치 하기 위한 메커니즘을 지원 되는 경우

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17110"></a>빌드 17110
일반 Windows에 대 한 17110 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)합니다.

### <a name="wsl"></a>WSL
* /Init Windows [GH 2928]에서 종료 될 수 있습니다.
* 이제 DrvFs 기본적으로 디렉터리 당 대/소문자 구분을 사용 (해당 하는 "대/소문자 dir =" 탑재 옵션).
    * 사용 하 여 "사례 force =" (이전 동작) 레지스트리 키를 설정 해야 합니다. 사용 하도록 설정 하려면 다음 명령을 실행 "대/소문자 force =" 사용 해야 할 경우: reg HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1 추가
    * WSL를 사용 하 여 대/소문자 구분 해야 하는 Windows의 이전 버전에서 만든 기존 디렉터리에 있는 fsutil.exe를 사용 하 여 표시할으로 대/소문자 구분: fsutil.exe 파일 setcasesensitiveinfo <path> 사용 하도록 설정
* NULL 종료 uname syscall에서 반환 된 문자열입니다.

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17107"></a>17107 빌드
일반 Windows에 대 한 17107 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)합니다.

### <a name="wsl"></a>WSL
* 마스터 pty 끝점 [GH 2552]에서 TCSETSF 및 TCSETSW를 지원 합니다.
* Interop 동시 프로세스를 시작 [GH 2813] EINVAL 발생할 수 있습니다.
* PTRACE_ATTACH /proc/pid/status에서 적절 한 추적 상태를 표시 하도록 수정 합니다.
* 수정 경합 CLEARTID와 SETTID 플래그를 사용 하 여 단기 실행 프로세스를 복제 하는 위치는 TID 주소 선택을 취소 하지 않고 종료 수 없습니다.
* 사전 17093 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드할 때 메시지를 표시 합니다. 17093 파일 시스템 변경 내용에 대 한 자세한 내용은 릴리스 정보 참조 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)합니다.

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17101"></a>17101 빌드
일반 Windows에 대 한 17101 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)합니다.

### <a name="wsl"></a>WSL
* Signalfd 지원 합니다. [GH 129]
* 파일 이름을 개인 유니코드 문자로 인코딩하여 NTFS의 잘못 된 문자가 포함 된 지원. [GH 1514]
* 자동 탑재 쓰기를 지원 하지 않는 경우 읽기 전용으로 대체가 됩니다. [GH 2603]
* 유니코드 서로게이트 쌍 (예:이 모 지 자)의 붙여넣기를 허용 합니다. [GH 2765]
* /Proc /sys에 의사 (pseudo) 파일은 읽기 반환 쓰고 준비 선택, 폴링, epoll, et al [GH 2838]
* 서비스 레지스트리 변조 또는 손상 된 경우 무한 루프로 이동 될 수 있는 문제를 해결 합니다.
* Netlink iproute2의 최신 (업스트림 4.14) 버전을 사용 하는 메시지를 수정 합니다.

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17093"></a>17093 빌드
일반 Windows에 대 한 17093 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)합니다.

#### <a name="important"></a>중요:
WSL이이 빌드로 업그레이드 후 처음으로 시작 하는 경우 Linux 파일 시스템 디렉터리를로 업그레이드 하는 일부 작업을 수행 해야 합니다. WSL 느리게 시작 하는 것 처럼 하므로 몇 분 정도 걸릴이 수 있습니다. 스토어에서 설치한 각 배포에 대 한 후에 발생 되어야이 있습니다.
* DrvFs에서 대/소문자 구분 지원을 개선.
    * 이제 DrvFs 디렉터리별 대/소문자 구분을 지원합니다. 새 플래그를 설정할 수 있는 해당 디렉터리에서 모든 작업을 처리 하도록 표시 하는 디렉터리와 대/소문자 구분, 대/소문자만 다른 파일 잘못 열려는 Windows 응용 프로그램을 허용 하는 경우
    * DrvFs에 디렉터리 당 기준 대/소문자 구분을 제어 하는 새 탑재 옵션
        * 대/소문자 force =: 모든 디렉터리와 대/소문자 구분 (드라이브 루트) 제외 하 고 처리 됩니다. WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다. 이 새 디렉터리를 대/소문자 구분 표시를 제외 하 고 레거시 동작입니다.
        * 대/소문자 = dir: 디렉터리별 대/소문자 구분 플래그를 사용 하 여 디렉터리만 대/소문자; 다른 디렉터리는 대/소문자 구분. WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다.
        * 대/소문자 = off: 디렉터리별 대/소문자 구분 플래그를 사용 하 여 디렉터리만 대/소문자; 다른 디렉터리는 대/소문자 구분. WSL를 사용 하 여 만든 새 디렉터리는 대/소문자 구분으로 표시 됩니다.
    * 참고: 이전 릴리스에서 WSL에서 만든 디렉터리 없는 설정 처리 되지 것입니다 있도록으로 대/소문자 구분 사용 하는 경우이 플래그는 "사례 dir =" 옵션입니다. 기존 디렉터리에서이 플래그를 설정 하는 방법을 곧 제공 됩니다.
    * 이러한 옵션을 사용 하 여 탑재의 예 (기존 드라이브에서 먼저 탑재 해제 해야 다양 한 옵션을 사용 하 여 탑재할 수 전에): sudo mount-t drvfs c: mnt은 / c o 사례 dir =
    * 지금은 경우 = 강제 여전히 기본 옵션입니다. 이 대/소문자를 변경할 수는 나중에 dir =.
* 이제 사용할 수 있습니다 슬래시 Windows 경로 예: DrvFs, 탑재 하는 경우: sudo-t drvfs //server/share /mnt/share 탑재
* 이제 WSL 인스턴스 시작 [GH 2636] 중 /etc/fstab 파일을 처리합니다.
    * 이 자동으로 DrvFs 드라이브를 탑재 하기 전에 작업 수행 fstab에서 이미 탑재 된 드라이브가 됩니다 하지 다시 탑재할 수 자동으로 특정 드라이브에 대 한 탑재 지점을 변경할 수 있습니다.
    * 이 동작은 해제할 수 있습니다 wsl.conf를 사용 하 여 합니다.
* /Proc의 탑재를 mountinfo mountstats 파일에 백슬래시 및 공백 [GH 2799]와 같은 특수 문자가 올바르게 이스케이프
* 이제 메타 데이터를 사용 하는 경우 WSL 기호화 된 링크 또는 fifos 및 소켓 같은 DrvFs를 사용 하 여 만든 특수 한 파일 복사 및 Windows에서 이동할 수 있습니다.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL은 wsl.conf를 사용 하 여 구성 됩니다.
하위 시스템을 시작할 때마다 적용 되는 WSL에서 특정 기능을 자동으로 구성 하는 방법을 추가 했습니다. 자동 탑재 옵션 및 네트워크 구성이 포함 됩니다. 자세한 정보에 대 한이 블로그 게시물에: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>WSL에서 Linux 프로세스와 Windows 네이티브 프로세스 사이의 소켓 연결을 허용 하는 AF_UNIX
WSL 및 Windows 응용 프로그램 이제 Unix 소켓을 통해 서로 통신할 수 있습니다. Windows에서 서비스를 실행 하 여 WSL 및 Windows 앱에 사용할 수 있도록 하 려 한다고 가정 합니다. 이제 Unix 소켓을 사용 하 여 가능한입니다. 블로그에서 자세한 내용을 게시물 읽기 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Support mmap() with MAP_NORESERVE [GH 121, 2784]
* CLONE_PTRACE 및 CLONE_UNTRACED [GH 121, 2781] 지원
* 복제 [GH 121, 2781]에서 비 SIGCHLD 종료 신호를 처리 합니다.
* 스텁 /proc/sys/fs/inotify/max_user_instances 및 /proc/sys/fs/inotify/max_user_watches [GH 1705]
* 0이 아닌 오프셋 [GH 1884]를 사용 하 여 부하 헤더를 포함 하는 ELF 이진 파일을 로드 중 오류 발생
* 이미지를 로드할 때 후행 페이지 바이트 비워야 합니다.
* 여기서 execve 프로세스를 자동으로 종료 하는 경우를 줄이려면

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17083"></a>빌드 17083
일반 Windows에 대 한 17083 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)합니다.

### <a name="wsl"></a>WSL
* [GH 2798, 2801, 2857] epoll와 관련 된 고정된 버그 확인
* ASLR [GH 1185, 2870]을 해제 하는 경우 고정된 중지
* Mmap 작업이 표시 원자성 [GH 2732] 확인

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17074"></a>17074 빌드
일반 Windows에 대 한 17074 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)합니다.

### <a name="wsl"></a>WSL
* 고정 된 저장소 형식의 DrvFs 메타 데이터 [GH 2777] </br>
**중요:** 이 빌드는 잘못 되거나 전혀 표시 되기 전의 DrvFs 메타 데이터입니다. 영향을 받는 파일을 수정 하려면 메타 데이터를 다시 적용할 chmod 및 chown를 사용 합니다.
* 여러 신호 및 다시 시작 가능한 syscall를 사용 하 여 문제를 해결 했습니다.

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17063"></a>17063 빌드
일반 Windows에 대 한 17063 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)합니다.

### <a name="wsl"></a>WSL
* DrvFs 추가 Linux 메타 데이터를 지원합니다. 따라서, 소유자 및 chmod/chown 그리고 fifos, unix 소켓 및 장치 파일과 같은 특수 한 파일의 생성을 사용 하 여 파일의 모드를 설정 합니다. 이 사용 되지 기본적으로 현재 여전히 실험적이 이기 때문입니다.
**참고:**  DrvFs에서 사용 하는 메타 데이터 형식에서 버그를 해결 했습니다. 메타 데이터 실험에 대 한이 빌드에 작동 하는 동안 이후 빌드 올바르게으로이 빌드에 의해 만들어진 메타 데이터를 읽지 못합니다.  수정 된 파일의 소유자를 수동으로 업데이트 해야 하 고 사용자 지정 장치 ID 사용 하 여 장치를 다시 생성 해야 합니다.

  메타 데이터 옵션을 사용 하 여 탑재 DrvFs을 사용 하려면 (기존 탑재를 사용 하려면 먼저 탑재 해제 해야 해당):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 권한은 파일에 추가 메타 데이터로 추가한 Windows 사용 권한에 영향을 주지 않습니다.  기억 메타 데이터를 제거할 수 있습니다 Windows 편집기를 사용 하 여 파일을 편집 합니다. 이 경우 파일의 기본 권한으로 되돌아갑니다.

* 메타 데이터 없이 제어 파일에 추가 탑재 옵션 DrvFs입니다.
  * uid: 모든 파일의 소유자에 사용 된 사용자 ID입니다.
  * gid: 모든 파일의 소유자에 사용 된 그룹 ID입니다.
  * umask: 모든 파일 및 디렉터리를 제외 하려면 사용 권한 마스크를 8 진수입니다.
  * fmask: 제외할 모든 일반 파일에 대 한 사용 권한 마스크를 8 진수입니다.
  * dmask: 모든 디렉터리를 제외 하려면 사용 권한 마스크를 8 진수입니다.

  예를 들어 다음과 같은 가치를 제공해야 합니다.
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  메타 데이터 없이 파일에 대 한 기본 사용 권한을 지정 하는 메타 데이터 옵션을 사용 하 여 결합 합니다.

* 새 환경 변수를 도입 `WSLENV`를 환경 변수 WSL 및 Win32 간에 전달 되는 방식을 구성 합니다.

  이는 아래와 같이 함수의 반환값을 데이터 프레임으로 바로 변환하는 데 사용할 수 있음을 나타냅니다.

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` Win32에서 WSL 프로세스 또는 WSL에서 Win32 프로세스를 시작할 때 포함할 수 있는 환경 변수의 콜론으로 구분 된 목록이입니다.  각 변수 슬래시 뒤에 변환 하는 방법을 지정 하는 플래그를 사용 하 여 접미사 수 있습니다.
  * p: 값은 Win32 경로 및 WSL 경로 간에 변환 해야 하는 경로.
  * l: 값은 경로의 목록. WSL를에서 콜론으로 구분 된 목록입니다. Win32에서 세미콜론으로 구분 된 목록입니다.
  * u: 값만 포함 해야 WSL Win32에서 호출 하는 경우
  * w: 값만 포함 해야 WSL에서 Win32를 호출 하는 경우

  설정할 수 있습니다 `WSLENV` .bashrc 또는 사용자에 대 한 사용자 지정 Windows 환경에서.

* drvfs 탑재 tar에서 타임 스탬프를 올바르게 유지 cp-p (GH 1939)
* drvfs symlink (GH 2641) 정확한 크기를 보고합니다.
* 매우 큰 IO 크기 (GH 2653)에 대 한 작동에 대 한 읽기/쓰기
* 프로세스 그룹 (GH 2534) Id 사용 하 여 waitpid 작동
* 향상 된 mmap 성능을 상당히 큰 예약 지역 선택 합니다. ghc 빨라집니다 (GH 1671)
* READ_IMPLIES_EXEC;에 대 한 성격 지원 최대 및 clisp (GH 1185)를 수정합니다.
* mprotect PROT_GROWSDOWN; 지원 수정 clisp (GH 1128)
* 모드를 과도 하 게 페이지 오류 수정 수정 sbcl (GH 1128)
* 복제는 많은 플래그 조합이 지원
* 선택/epoll epoll 파일 (이전에 아무)를 지원 합니다.
* 구현 되지 않은 syscall의 ptrace를 알립니다.
* Resolv.conf 이름 서버 [GH 2694]을 생성 하는 경우 등록 되지 않은 인터페이스를 무시 합니다.
* 실제 주소가 없는 네트워크 인터페이스를 열거 합니다. [GH 2685]
* 추가 버그 수정 및 개선 합니다.

### <a name="linux-tools-available-to-developers-on-windows"></a>Windows에서 개발자에 게 제공 되는 Linux 도구

* Windows 명령줄 도구 체인에 bsdtar (tar) 및 넘기기가 포함 됩니다.
  읽기 [이 블로그](https://aka.ms/tarcurlwindows) 이러한 두 가지 새로운 도구를 추가 하는 방법에 대 한 자세한 정보를 어떻게 개발자 환경에서 Windows 셰이핑 하는 이러한 참조 합니다.

*   `AF_UNIX` Windows Insider SDK (17061 이상)에서 제공 됩니다.
  읽기 [이 블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) 에 대해 자세히 알아보려면 `AF_UNIX` 개발자가 Windows에서 사용할 수 하는 방법입니다.

### <a name="console"></a>콘솔
* 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.


## <a name="build-17046"></a>17046 빌드

일반 Windows에 대 한 17046 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)합니다.

### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 활성 터미널을 하지 않고 실행 하는 프로세스를 허용 합니다. [GH 709, 1007, 1511, 2252, 2391, et al.]
- CLONE_VFORK 및 CLONE_VM 더 나은 지원 합니다. [GH 1878, 2615]
- WSL 네트워킹 작업에 대 한 TDI 필터 드라이버를 건너뜁니다. [GH 1554]
- 특정 조건이 충족 되 면 DrvFs NT symlink를 만듭니다. [GH 353, 1475, 2602]
    - 링크 대상 상대 이어야 하 고 모든 탑재 지점 또는 symlink를 넘지 않아야 합니다 하며 존재 해야 합니다.
    - 사용자는 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (일반적으로 해야 wsl.exe 권한 시작)에 있어야 합니다. 개발자 모드가 켜져 하지 않는 한 합니다.
    - 다른 모든 상황에서 DrvFs 여전히 WSL symlink를 만듭니다.
- 관리자 권한 및 권한 상승 되지 않은 WSL 인스턴스를 동시에 실행할 수 있습니다.
- Support /proc/sys/kernel/yama/ptrace_scope
- WSL <>-Windows 경로 변환을 수행 하는 wslpath를 추가 합니다. [GH 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>콘솔
- 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.


## <a name="build-17040"></a>17040 빌드

일반 Windows에 대 한 빌드 17040에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 17035 이후 수정 되지 않습니다.

#### <a name="console"></a>콘솔
- 17035 이후 수정 되지 않습니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17035"></a>17035 빌드

일반 Windows에 대 한 17035 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- DrvFs에서 파일에 액세스할 경우에 따라 EINVAL를 사용 하 여 실패할 수 있습니다. [GH 2448]

#### <a name="console"></a>콘솔
- VT 모드에서 줄 삽입/삭제 하는 경우 몇 가지 색 손실입니다.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17025"></a>빌드 17025

일반 Windows에 대 한 빌드 17025에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 새 포그라운드 프로세스 그룹 [GH 1653, 2510]의 초기 프로세스를 시작 합니다.
- SIGHUP 배달 [GH 2496] 수정합니다.
- [GH 2497] 아무 것도 제공 하는 경우 기본 가상 브리지 이름을 생성 합니다.
- Implement /proc/sys/kernel/random/boot_id [GH 2518].
- 더 interop stdout/stderr 파이프를 수정합니다.
- 스텁 syncfs 시스템 호출 합니다.

#### <a name="console"></a>콘솔
- 제 3 자 콘솔 [GH 111]에 대 한 입력된 VT 번역 수정

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="build-17017"></a>17017 빌드

일반 Windows에 대 한 17017 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 빈 ELF 프로그램 헤더 [GH 330]를 무시 합니다.
- 비 대화형 사용자에 대 한 WSL 인스턴스를 만드는 LxssManager 허용 (ssh 지원 작업을 예약 하 고) [GH 777, 1602].
- WSL 지원 Win32-> WSL ("초기") 시나리오 [GH 1228]-> 합니다.
- Interop [GH 1614]를 통해 호출 되는 콘솔 응용 프로그램 종료에 대 한 제한적으로 지원 합니다.
- Devpts [GH 1948]에 대 한 탑재 옵션을 지원 합니다.
- Ptrace 자식 시작 [GH 2333]를 차단 합니다.
- 누락 된 일부 이벤트 [GH 2462] EPOLLET 합니다.
- PTRACE_GETSIGINFO에 대 한 더 많은 데이터를 반환 합니다.
- Lseek 사용 하 여 Getdents 잘못 된 결과 제공합니다.
- 자세한 데이터가 없는 파이프에서 입력을 기다리는 일부 Win32 interop 응용 프로그램 중단을 수정 합니다.
- O_ASYNC는 tty/pty 파일에 대 한 지원.
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
진행 중인 테스트 합니다.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>16288 빌드

일반 Windows에 대 한 16288 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 올바르게 초기화 하 고 보고서 uid, gid 및 소켓 파일 설명자 [GH 2490]에 대 한 모드
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 되지 않았습니다

## <a name="build-16278"></a>16278 빌드

일반 Windows에 대 한 162738 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- LX MM 상태 [GH 2415]를 분해 하는 경우 명시적으로 매핑된 뷰 파일을 백업 섹션의 매핑을 해제합니다
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 되지 않았습니다

## <a name="build-16275"></a>16275 빌드

일반 Windows에 대 한 162735 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 없는 WSL 관련이 릴리스의 변경 내용.

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
16273 이후 변경 되지 않았습니다

## <a name="build-16273"></a>16273 빌드

일반 Windows에 대 한 16273 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 디렉터리 [GH 2392]에 대 한 잘못 된 파일 형식에 DrvFs 경우에 따라 보고 문제를 해결 함
- 프로그램 차단을 해제 하려면 NETLINK_KOBJECT_UEVENT 소켓 만들기는 사용 하 여 uevent 허용 [GH 1121, 2293, 2242, 2295 2235, 648, 637]
- 비차단 연결에 대 한 지원을 추가 [GH 903, 1391, 1584 1585, 1829, 2290, 2314]
- 구현 CLONE_FS 복제 시스템 호출 플래그 [GH 2242]
- 탭 또는 따옴표 NT interop [GH 1625, 2164]에서 올바르게 처리 하지 못할 경우 관련 된 문제를 해결 합니다.
- WSL를 다시 시작 하려고 하는 동안 오류가 발생 했습니다. [GH 651, 2095] 인스턴스 액세스 거부 해결
- Futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업 [GH 2242]를 구현 합니다.
- 다양 한 SysFs 파일 [GH 2214]에 대 한 권한을 수정 합니다.
- 설치 [GH 2290] 중 Haskell 스택 중단을 수정
- 'C' binfmt_misc 구현 ' o ' 및 'P' 플래그 [GH 2103]
- 추가 /proc/sys/kernel /shmmax /shmmni /threads-max [GH 1753]
- Ioprio_set 시스템 호출 [GH 498]에 대 한 부분 지원 추가
- 스텁 SO_REUSEPORT & SO_PASSCRED netlink 소켓 [GH 69]에 대 한 지원 추가
- 배포를 현재 중이면 RegisterDistribuiton에서 다른 오류 코드를 반환 설치 또는 제거 합니다.
- Wslconfig.exe 통해 부분적으로 설치 된 WSL 배포의 등록 취소 허용
- Udp::msg_peek에서 python 소켓 테스트 중지를 수정 합니다.
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
총 테스트: 1904<br/>
총 건너뛴 테스트: 209<br/>
총 오류 횟수: 229<br/>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>빌드 16257

일반 Windows에 대 한 16257 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 구현 prlimit64 시스템 호출
- Ulimit-n (setrlimit RLIMIT_NOFILE)에 대 한 지원을 추가 [GH 1688]
- TCP 소켓 [GH 2351]에 대 한 스텁을 MSG_MORE
- 잘못 된 AT_EXECFN 보조 벡터 동작 [GH 2133] 수정
- 콘솔/tty에 대 한 복사/붙여넣기 동작을 수정 하 고 [GH 2204, 2131]를 처리 하는 더 나은 가득 찬 버퍼를 추가 합니다.
- 집합-사용자 ID 및 집합-그룹-ID 프로그램 [GH 2031]에 대 한 보조 벡터에서 AT_SECURE 설정
- 유사 터미널 마스터 엔드포인트 TIOCPGRP [GH 1063]를 처리 하지 못할 경우
- 수정 lseek LxFs [GH 2310]의 디렉터리 부분까지 되 감아야 않습니다.
- 사용량이 [GH 1882] 후 /dev/ptmx 작동 중지 됩니다.
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 가로 줄/밑줄 Everywhere [GH 2168]에 대 한 수정
- 처리 순서를 닫으려면 [GH 2170] 어렵게 만드는 NPM 변경에 대 한 수정
- 이 새로운 색 구성표를 추가 합니다. https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 결과:
16251 이후 변경 되지 않았습니다

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`prlimit64`<br/>

### <a name="known-issues"></a>알려진 문제
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub Issue 2392: Windows 폴더 WSL에서 인식할 수 없습니다...](https://github.com/Microsoft/BashOnWindows/issues/2392)
빌드 16257 WSL에 문제를 통해 Windows 파일/폴더를 열거 하는 동안 `/mnt/c/...`합니다.
이 문제는 해결 되었습니다 및에서 해제 되어야 참가자는 2017 년 8 월 14를 시작 하는 주 동안 빌드.

<br/>

## <a name="build-16251"></a>16251 빌드

일반 Windows에 대 한 16251 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- WSL 선택적 구성 요소에서 베타 태그 제거를 참조 하십시오 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) 세부 정보에 대 한 합니다.
- 저장 집합 uid 및 gid exec [GH 962, 1415, 2072]에서 집합-사용자 ID 및 집합-그룹-ID 바이너리를 제대로 초기화
- ptrace PTRACE_O_TRACEEXIT [GH 555]에 대 한 지원 추가
- ptrace에 대 한 지원이 추가 되었습니다 PTRACE_GETFPREGS 및 PTRACE_GETREGSET NT_FPREGSET [GH 555]를 사용 하 여
- 무시 중지에 대해 ptrace를 고정 신호
- 추가 개선 사항 및 버그 수정

#### <a name="console"></a>콘솔
- 콘솔이 관련이 릴리스의 변경 내용.

### <a name="ltp-results"></a>LTP 결과:
테스트 통과 수: 768</br>
실패 한 테스트 수: 244</br>
건너뛴된 테스트 수: 96</br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>16241 빌드

일반 Windows에 대 한 16241 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
#### <a name="wsl"></a>WSL
- 없는 WSL 관련이 릴리스의 변경 내용.

#### <a name="console"></a>콘솔
- 원래 보고 교차 줄 dec 잘못 된 문자를 출력 하는 것에 대 한 수정 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- 코드 페이지 65001 (utf8)에 표시 되는 출력 텍스트가 없습니다에 대 한 수정
- 선택 변경에서 색상표의 다른 부분에 하나의 색의 RGB 값에 대 한 변경 내용을 전송 하지 않습니다. 이렇게 하면 콘솔 속성 시트를 사용 하 여 훨씬 더 쉽습니다.
- Ctrl + S 제대로 작동 하지 않습니다.
- 굵게 표시 되지 않은 /-차원 없는 완전히 ANSI 이스케이프 코드 [GH 2174]
- 콘솔 [GH 1706] Vim 색 테마를 올바르게 지원 하지 않습니다.
- [GH 2149] 특정 문자를 붙여 넣을 수 없습니다.
- 편집/명령줄 [GH ConEmu 1123]에 올려져 있는 경우 bash 창 크기 조정을 통한 리플로우 크기 조정 이상 하 게 상호 작용
- Ctrl-L 더티 화면 [GH 1978 년 5]을 떠날
- HDPI [GH 1907]에서 VT를 표시할 때 콘솔 렌더링 버그
- Japansese 문자는 유니코드 문자 U + 30FB를 사용 하 여 생소할 [GH 2146]
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16237"></a>빌드 16237

일반 Windows에 대 한 16237 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)합니다.<br/>


### <a name="fixed"></a>고정
- EAs 없이 파일 lxfs (루트, 루트, 0000)에 대 한 기본 특성을 사용 합니다.
- 확장 된 특성을 사용 하는 배포에 대 한 지원 추가
- Getdents getdents64로 반환 되는 항목에 대 한 안쪽 여백을 수정
- 수정 [GH 2068] shmctl SHM_STAT 시스템 호출에 대 한 사용 권한 확인
- Tty [GH 2231]에 대 한 잘못 된 초기 epoll 고정된 상태
- 모든 항목 [GH 2077]를 반환 하지 않는 DrvFs readdir 수정
- LxFs 해결 readdir 파일이 있는 경우 [GH 2077] 연결이 끊어진
- 연결 되지 않은 drvfs 파일은 procfs 통해 다시 열 수
- WSL 기능을 사용 하지 않도록 설정 하는 것에 대 한 전역 레지스트리 키 재정의 추가 (interop / 탑재 드라이브)
- DrvFs (및 LxFs)에 대 한 "상태"에 잘못 된 블록 수를 수정 [GH 1894]
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16232"></a>16232 빌드

일반 Windows에 대 한 16232 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- 없는 WSL 관련이 릴리스의 변경 내용.

</br>

## <a name="build-16226"></a>16226 빌드

일반 Windows에 대 한 16226 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)합니다.<br/>


### <a name="fixed"></a>고정
- xattr 관련 syscall 지원 (getxattr setxattr, listxattr, removexattr).
- security.capablity xattr 지원 합니다.
- 특정 파일 시스템 및 비 MS SMB 서버를 포함 하 여 필터를 사용 하 여 향상 된 호환성. [GH #1952]
- OneDrive 자리 표시자, GVFS 자리 표시자 및 Compact OS에 대 한 향상 된 지원 파일을 압축 합니다.
- 추가 개선 사항 및 버그 수정

</br>

## <a name="build-16215"></a>16215 빌드

일반 Windows에 대 한 16215 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- WSL은 개발자 모드를 더 이상 필요합니다.
- Drvfs에서 디렉터리 연결을 지원 합니다.
- WSL 배포 appx 패키지 제거를 처리 합니다.
- 개인 표시할 procfs 업데이트 및 매핑을 공유 합니다.
- Wslconfig.exe 부분적으로 설치 되거나 제거 되는 배포를 정리 하는 기능을 추가 합니다.
- TCP 소켓에 대 한 IP_MTU_DISCOVER에 대 한 지원이 추가 되었습니다. [GH 1639, 2115, 2205]
- 프로토콜 패밀리가 AF_INADDR에 대 한 경로 대 한 유추 합니다.
- 직렬 장치 개선 [GH 1929]입니다.

</br>

## <a name="build-16199"></a>16199 빌드

일반 Windows에 대 한 16199 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- 없는 WSL의에서 관련 변경 내용을 이러한 릴리스 합니다.

</br>

## <a name="build-16193"></a>16193 빌드

일반 Windows에 대 한 16193 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- SIGCONT 및 [GH 1973] 종료는 threadgroup이 보내는 간격 사이의 경합 상태
- 보고서 [GH 1840] FILE_DEVICE_CONSOLE 대신 FILE_DEVICE_NAMED_PIPE tty 및 pty 장치 변경
- IP_OPTIONS에 대 한 SSH 수정
- Init 디먼 DrvFs 탑재 이동할 [GH 1862, 1968, 1767, 1933]
- NT symlink 따라 하는 데 DrvFs에서 지원이 추가 되었습니다.

</br>

## <a name="build-16184"></a>16184 빌드

일반 Windows에 대 한 16184 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- Apt 패키지 유지 관리 작업 (lxrun.exe /update)를 제거합니다.
- 고정 된 출력에 표시 되지 node.js [GH 1840] Windows 프로세스에서
- Lxcore [GH 1794]의 맞춤 요구 사항 완화
- 시스템 호출의 필드가에서 AT_EMPTY_PATH 플래그의 처리가 수정 되었습니다.
- 여기서 열린 핸들로 DrvFs 파일을 삭제 하면 정의 되지 않은 동작이 [GH 544,966,1357,1535,1615] 파일의 문제 해결된
- / 등 호스트에서 Windows 호스트 파일 (%windir%\system32\drivers\etc\hosts) 항목 상속 이제 [GH 1495]

</br>

## <a name="build-16179"></a>16179 빌드

일반 Windows에 대 한 16179 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- 없는 WSL 이번이 주를 변경합니다.

</br>

## <a name="build-16176"></a>16176 빌드

일반 Windows에 대 한 16176 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)합니다.<br/>


### <a name="fixed"></a>고정

- [직렬 지원 사용](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 추가 IP 소켓 옵션 IP_OPTIONS [GH 1116]
- Nginx/PHP-FPM에 파일 업로드) 하는 것 (동안 pwritev 함수 구현 [GH 1506]
- 추가 IP 소켓 옵션 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP 소켓 옵션에 대 한 지원 [GH 1678]
- 앱 노드의 traceroute, dig, nslookup 호스트에 대 한 추가 IP (V6) _MTU 소켓 옵션
- 추가 IP 소켓 옵션 IPV6_UNICAST_HOPS
- [파일 시스템 개선 사항](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * 탑재 되는 UNC 경로 허용 합니다.
    * Drvfs에서 CDFS 지원을 사용 하도록 설정
    * Drvfs에서 네트워크 파일 시스템에 대 한 사용 권한을 올바르게 처리
    * Drvfs에 원격 드라이브에 대 한 지원 추가
    * FAT 사용 drvfs 지원
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과
15042 이후 변경 하지 않고

</br>

## <a name="build-16170"></a>16170 빌드

일반 Windows에 대 한 16170 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)합니다.<br/>

새 출시 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) WSL를 테스트 하기 위한 우리의 노력에 설명 합니다.

### <a name="fixed"></a>고정

- 지원 소켓 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP 옵션 [GH 1678]
- PTRACE_OLDSETOPTIONS 지원을 추가 합니다. [GH 1692]
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과
15042 이후 변경 하지 않고

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>빌드 15046 windows 10 크리에이터 스 업데이트
WSL 수정 또는 Windows 10 크리에이터 스 업데이트에 포함 될 예정인 기능을 더 이상 있습니다. WSL에 대 한 릴리스 정보는 다음 주요 Windows 업데이트를 대상으로 하는 추가 기능에 대 한 주간에 다시 시작 됩니다. 빌드 15046 및 향후 참가자에 대 한 정보를 일반 Windows에 대 한 방문을 해제 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)합니다. <br/><br/>
 <br/>

## <a name="build-15042"></a>15042 빌드

일반 Windows에 대 한 15042 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)합니다.<br/>


### <a name="fixed"></a>고정

- 로 끝나는 경로 제거 하는 동안 교착 상태가 해결 "..."
- 문제를 해결 함 위치 [GH 1683] 성공 시 0을 반환 하지 않는 FIONBIO
- 길이가 0 인 읽기 inet 데이터 그램 소켓의 문제 해결된
- Drvfs inode 조회 [GH 1675] 경합으로 인해 가능한 교착 상태 해결
- Unix 소켓 보조 데이터에 대 한 지원 확장 SCM_CREDENTIALS 및 SCM_RIGHTS [GH 514, 613, 1326]
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 737</br>
불합격 개수 (실패, 건너뜀 등...): 255

</br>

## <a name="build-15031"></a>15031 빌드

일반 Windows에 대 한 15031 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)합니다.<br/>


### <a name="fixed"></a>고정

- 여기서 time(2) 오동작 산발적는 버그가 수정 되었습니다.
- 고정 및 where 발급 * SIGPROCMASK syscall 신호 마스크 손상 될 수 있습니다.
- 프로세스 만들기 알림 WSL에서에서 이제 전체 명령줄 길이 반환 합니다. [GH 1632]
- WSL은 GDB 중단에 ptrace 통해 스레드 종료를 보고합니다. [GH 1196]
- 과도 한 tmux IO 후 ptys가 중단 되는 버그가 수정 되었습니다. [GH 1358]
- 많은 시스템 호출 (futex semtimedop, ppoll, sigtimedwait, itimer, timer_create)에서 고정 된 제한 시간 유효성 검사
- 추가 eventfd EFD_SEMAPHORE 지원 [GH 452]
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 737</br>
불합격 개수 (실패, 건너뜀 등...): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>15025 빌드

일반 Windows에 대 한 15025 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)합니다.<br/>


### <a name="fixed"></a>고정

- 해당 고장 grep 2.27 [GH 1578] 버그 수정
- Eventfd2 syscall [GH 452]에 대 한 구현된 EFD_SEMAPHORE 플래그
- [Pid] /proc//net ipv6_route 구현 [GH 1608]
- Unix 스트림 소켓 [GH 393를 68]에 대 한 IO 지원 기반 신호
- F_GETPIPE_SZ 및 F_SETPIPE_SZ [GH 1012] 지원
- Implement recvmmsg() syscall [GH 1531]
- Epoll_wait() 되지 않은 대기 하는 [GH 1609] 버그가 수정 되었습니다.
- /Proc/version_signature 구현
- 동일한 파이프 파일 설명자 두 참조 하는 경우 이제 tee syscall 실패 반환
- Unix 소켓에 대 한 SO_PEERCRED에 대 한 올바른 구현 된 동작
- 고정된 tkill syscall 잘못 된 매개 변수 처리
- Drvfs의 preformace 높이기 위해 변경 내용
- Ruby IO 차단에 대해 사소한 수정
- 고정된 recvmsg() EINVAL inet 소켓 [GH 1296] MSG_DONTWAIT 플래그에 대 한 반환
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 732</br>
불합격 개수 (실패, 건너뜀 등...): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>빌드 15019

일반 Windows에 대 한 빌드 15019에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)합니다.<br/>


### <a name="fixed"></a>고정

- 버그에서 CPU 사용량을 올바르게 보고 한다면 (GH 823 945, 971)와 같은 도구에 대 한 procfs
- 파일 inotify IN_OPEN 전에 IN_MODIFY 이제 생성 기존 O_TRUNC 사용 하 여 open ()를 호출 하는 경우
- Unix 소켓 getsockopt SO_ERROR postgress [GH 61이 1354]를 사용 하도록 설정 하기 위한 수정 사항
- GO 언어에 대 한 구현 /proc/sys/net/core/somaxconn
- Apt get 패키지 업데이트 백그라운드 작업 지금 실행 숨겨진 뷰에서
- Ipv6 localhost (Spring-Framework(Java) 실패)에 대 한 일반 범위입니다.
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 714 </br>
불합격 개수 (실패, 건너뜀 등...): 249 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>15014 빌드

일반 Windows에 대 한 15014 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)합니다.<br/>


### <a name="fixed"></a>고정

- Ctrl + C는 이제 의도 한 대로 작동
- htop 및 ps auxw 이제 표시 올바른 리소스 사용률 (GH #516)
- 기본 신호 NT 예외 변환 합니다. (#513 GH)
- fallocate 이제 실패 ENOSPC EINVAL (GH #1571) 대신 공간 부족
- 추가 /proc/sys/kernel/sem 합니다.
- 구현 된 semop 및 semtimedop 시스템 호출
- IP_RECVTOS & IPV6_RECVTCLASS 소켓 옵션 (GH 69)를 사용 하 여 고정된 nslookup 오류
- IP_RECVTTL 및 IPV6_RECVHOPLIMIT 소켓 옵션에 대 한 지원
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 709 </br>
불합격 개수 (실패, 건너뜀 등...): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 요약
총 Syscall: 384 </br>
전체 구현: 235 </br>
스텁 합계: 22 </br>
구현 되지 않았으며 합계: 127 </br>
[세부적인된 분석 결과](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>15007 빌드

일반 Windows에 대 한 15007 빌드에 대 한 정보를 방문 합니다 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)합니다.<br/>


### <a name="known-issue"></a>알려진된 문제

- 콘솔 일부 Ctrl 인식 하지 못하는 알려진 버그가 + <key> 입력 합니다.  일반 'c' keypress 역할을 할 ctrl + c 명령 포함 됩니다.

  - 해결 방법: Ctrl + C를 대체 키를 매핑하십시오. 예를 들어, 매핑할 Ctrl + K Ctrl + C를 수행: `stty intr \^k`합니다.  이 매핑은 터미널 당 이며 완료 해야 할 *마다* 시간 bash 시작 됩니다. 사용자는이 포함 하는 옵션을 탐색할 수 있습니다는 `.bashrc`

### <a name="fixed"></a>고정

- 여기서 실행 WSL를 사용 하 게 CPU 코어의 100% 문제를 수정 합니다.
- 소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO 이제 지원 됩니다. (GH #851, 987)
- 네트워크 인터페이스 물리적 주소 lxcore 16 바이트를 자르기 (1414, GH #1452, 1343, 468, 308)
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 709 </br>
불합격 개수 (실패, 건너뜀 등...): 255 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>빌드 15002

일반 Windows 빌드 15002 방법은 참조를 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)합니다.<br/>


### <a name="known-issue"></a>알려진된 문제

두 가지 알려진된 문제:
- 콘솔 일부 Ctrl 인식 하지 못하는 알려진 버그가 + <key> 입력 합니다.  일반 'c' keypress 역할을 할 ctrl + c 명령 포함 됩니다.

  - 해결 방법: Ctrl + C를 대체 키를 매핑하십시오. 예를 들어, 매핑할 Ctrl + K Ctrl + C를 수행: `stty intr \^k`합니다.  이 매핑은 터미널 당 이며 완료 해야 할 *마다* 시간 bash 시작 됩니다. 사용자는이 포함 하는 옵션을 탐색할 수 있습니다는 `.bashrc`

- WSL에서 실행 되는 동안 시스템 스레드를 CPU 코어의 100%를 사용 합니다.  근본 원인은 해결 되어 내부적으로 고정 합니다.

### <a name="fixed"></a>고정

- 이제 모든 bash 세션 같은 권한 수준에서 만들어야 합니다.  여러 수준에서 세션을 시작 하는 동안 차단 됩니다.  즉, 관리자 및 비관리자 콘솔 동시에 실행할 수 없습니다. (#626 GH)
<br/>
- 다음 NETLINK_ROUTE 메시지 구현 (Windows 관리 해야 함)
     - RTM_NEWADDR (지원 `ip addr add`)
     - RTM_NEWROUTE (지원 `ip route add`)
     - RTM_DELADDR (지원 `ip addr del`)
     - RTM_DELROUTE (지원 `ip route del`)
- 패키지 업데이트를 확인 하는 예약 된 작업 (GH #1371) 데이터 통신된 연결에서 수행 되지 않습니다.
- 고정 오류 가져옵니다 파이프 멈춘 즉, bash-c "ls alR /" | bash-c "고양이" (GH #1214)
- 구현 된 TCP_KEEPCNT 소켓 옵션 (GH #843)
- 구현 된 IP_MTU_DISCOVER INET 소켓 옵션 (GH #720, 717, 170, 69)
- NT 경로 조회를 사용 하 여 초기화에서 NT 이진 파일을 실행 하는 레거시 기능을 제거 합니다. (#1325 GH)
- 그룹 / 기타 읽기 (0644) (GH #1321) 액세스할 수 있도록/kmsg의 모드를 수정 합니다.
- 구현 된 /proc/sys/kernel/random/uuid (GH #1092)
- 프로세스 시작 시간 (GH #974) 2432 연도로 표시 되어 있는 오류를 수정 합니다.
- Xterm-256color (GH #1446)로 전환된 하는 기본 용어 환경 변수
- 수정 된 커밋을 처리 하는 방식으로 프로세스 분기 하는 동안 계산 됩니다. (GH #1286)
- /Proc/sys/vm/overcommit_memory 구현된 합니다. (GH #1286)
- 구현 된 /proc/net/route 파일 (GH #69)
- 바로 가기 이름이 올바르게 오류 수정된 했습니다 (GH #696) 지역화
- 프로그램 헤더를 올바르게 검사할 되는 논리를 구문 분석 하는 고정된 elf 작아야 (크거나 같음) PATH_MAX 합니다. (#1048 GH)
- 구현 된 statfs 콜백 procfs, sysfs, cgroupfs, 및 binfmtfs (GH #1378)
- (GH #1184, GH # 1193에 대해서도 설명)를 닫지는 고정 된 AptPackageIndexUpdate windows
- ADDR_NO_RANDOMIZE 지원 ASLR 성격을 추가 합니다. (GH #1148, 1128)
- 향상 된 PTRACE_GETSIGINFO, AV (GH #875) 하는 동안 적절 한 gdb 스택 추적에 대 한 SIGSEGV
- 더 이상 구문 분석 elf patchelf 이진 파일에 대 한 실패 합니다. (GH #471)
- /Etc/resolv.conf (GH #416, 1350)를 VPN DNS 전파
- TCP의 향상 된 기능을 더 신뢰할 수 있는 데이터 전송에 대 한 닫습니다. (GH #610, 616, 1025, 1335)
- 이제 올바른 너무 많은 파일이 있는 경우 오류 코드 (EMFILE) 열을 반환 합니다. (GH #1126, 2090)
- 프로세스의 이미지 이름을 Windows 감사 로그 이제 보고서는 감사를 만듭니다.
- Bash 창 내에서 bash.exe 시작할 때 이제 정상적으로 실패
- 추가 오류 메시지가 나타난다 interop LxFs (예: notepad.exe.bashrc)에서 작업 디렉터리에 액세스할 수 없는
- Windows 경로 WSL에서 잘린 여기서 문제 해결된
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 690 </br>
불합격 개수 (실패, 건너뜀 등...): 274 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>14986 빌드

일반 Windows에 대 한 14986 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)합니다.<br/>


### <a name="fixed"></a>고정

- Netlink Pty Ioctl와 고정된 버그
- 커널 버전에는 이제 4.4.0-43 Xenial와의 일관성에 대 한 보고
- Bash.exe 입력으로 전달 하는 경우 이제 시작 ' nul:' (GH #1259)
- 스레드 Id procfs (GH #967)에서 올바르게 이제 보고
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | 이제 inotify_add_watch() (GH #1280)에서 지원 되는 IN_ISDIR 플래그
- 구현 timer_create 및 관련된 시스템 호출 합니다.  이렇게 하면 GHC 지원 (GH #307)
- Ping 0.000ms (GH #1296)의 시간을 반환 하는 위치 하는 문제 해결된
- 너무 많은 파일이 열려 있는 경우 올바른 오류 코드를 반환 합니다.
- 인터페이스의 하드웨어 주소 (예: Teredo 인터페이스)를 32 바이트 이면 EINVAL를 사용 하 여 네트워크 인터페이스 데이터에 대 한 Netlink 요청 실패는 WSL에서 문제 해결된
   - Note Linux "ip" 유틸리티 WSL 32 비트 하드웨어 주소를 보고 하는 경우 충돌이 있는 버그를 포함 합니다. WSL 없습니다 "ip"의 버그입니다. "ip" 유틸리티 하드 코드 길이 문자열 버퍼의 하드웨어 주소를 인쇄 하는 데 사용 하 고 32 비트 하드웨어 주소를 인쇄 하는 버퍼가 너무 작습니다.입니다.
- 추가 수정 및 개선 사항

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 669 </br>
불합격 개수 (실패, 건너뜀 등...): 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>14971 빌드

일반 Windows에 대 한 14971 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)합니다.<br/>


### <a name="fixed"></a>고정

 - 제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

### <a name="ltp-results"></a>LTP 결과:
14965에서 변경 되지 않음 </br>
통과 한 테스트 수: 664 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>14965 빌드

일반 Windows에 대 한 14965 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)합니다.<br/>


### <a name="fixed"></a>고정

- Netlink 지원 소켓 NETLINK_ROUTE 프로토콜 RTM_GETLINK 및 RTM_GETADDR (GH #468)
  - 네트워크 열거형에 대 한 명령을 ifconfig 및 ip를 사용 하도록 설정
  - 자세한 정보를 찾을 수 있습니다 우리의 [블로그 게시물 WSL 네트워킹](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)합니다.

- 기본적으로 사용자의 경로에 포함 되었습니다 /sbin
- NT 사용자 경로 (즉, 이제 입력할 있습니다 notepad.exe System32 Linux 경로에 추가 하지 않고) 기본적으로 이제 WSL 경로에 추가
- /Proc/sys/kernel/cap_last_cap 지원 추가 됨된
- 현재 작업 디렉터리 (GH #1254) ansi 이외의 문자를 포함 하는 경우 NT 바이너리 WSL에서 시작할 수 이제
- 연결이 끊긴된 unix 스트림 소켓에서 종료를 허용 합니다.
- PR_GET_PDEATHSIG 지원이 추가 되었습니다.
- CLONE_PARENT 지원 추가 됨된
- 고정 오류 가져옵니다 파이프 멈춘 즉, bash-c "ls alR /" | bash-c "고양이" (GH #1214)
- 현재 터미널에 연결할 핸들 요청 합니다.
- /Proc/ 표시<pid>/oom_score_adj 쓰기 가능으로 합니다.
- /Sys/fs/cgroup 폴더를 추가 합니다.
- sched_setaffinity는 선호도 비트 마스크의 수를 반환 해야
- 이 경우 올바르게 가정 하지 인터프리터 경로 보다 작거나 64 자 이어야 합니다. ELF 유효성 검사 논리를 수정 합니다. (GH #743)
- 열린 파일 설명자는 콘솔 창 열기 (GH #1187)를 유지할 수 있습니다.
- Rename () 뒤에 슬래시가 대상 이름 (GH #1008)에 실패 한 Fixeed 오류
- 구현 /proc/net/dev 파일
- 타이머 해상도 인해 고정된 0.000ms ping합니다.
- 구현 된 /proc/self/environ (GH #730)
- 추가 버그 수정 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 664 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>14959 빌드

일반 Windows에 대 한 14959 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)합니다.<br/>


### <a name="fixed"></a>고정

- Windows에 대 한 향상 된 Pico 프로세스 알림입니다.  추가 정보에는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)합니다.
- Windows 상호 운용성을 사용 하 여 향상 된 안정성
- 엔터프라이즈 데이터 보호 (EDP)을 사용 하는 경우 bash.exe를 시작할 때 0x80070057 오류가 수정 됨된
- 추가 버그 수정 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>14955 빌드

일반 Windows에 대 한 14955 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)합니다.<br/>


### <a name="fixed"></a>고정

 - 제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>14951 빌드

일반 Windows에 대 한 14951 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)합니다.<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>새로운 기능: Windows / Ubuntu 상호 운용성
이제 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.  이렇게 하면 사용자는 Windows 환경 및 가능한 되지 않은 방식으로 상호 작용할 수 있습니다.  간단한 예제로 다음 명령을 실행 하는 사용자에 대 한 가능한 되었습니다.

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

자세한 내용은에서 찾을 수 있습니다.

- [Interop에 대 한 WSL 팀 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop 설명서](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>고정

- Ubuntu 16.04 (Xenial)는 이제 모든 새 WSL 인스턴스에 대 한 설치 됩니다.  기존 14.04 (믿음직한) 인스턴스를 사용 하 여 사용자가 자동으로 업그레이드 되지 않습니다.
- 설치 중에 설정 된 로캘을 표시 됩니다.
- 항상 그렇지는 않음 않습니다 WSL 프로세스 파일로 리디렉션하는 버그를 포함 하 여 터미널 향상 작업
- 콘솔의 수명이 bash.exe 수명에 연결 해야
- 콘솔 창 크기는 버퍼 크기가 아니라 표시 크기를 사용 해야
- 추가 버그 수정 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>14946 빌드

일반 Windows에 대 한 14946 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)합니다.<br/>


### <a name="fixed"></a>고정

- 공백이 나 따옴표가 포함 된 NT 사용자 이름을 사용 하 여 사용자에 대 한 WSL 사용자 계정 만들기를 방해 하는 문제가 수정 되었습니다. 
- 바뀌는 VolFs DrvFs stat에서 디렉터리의 링크 개수에 대 한 0을 반환 합니다.
- IPV6_MULTICAST_HOPS 소켓 옵션을 지원 합니다.
- Tty 당 I/O 루프는 단일 콘솔을 제한 합니다. 예 명령을 불가능 합니다.:
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- 공백은 /proc/cpuinfo (GH #1115) 탭으로 대체
- 이제 탑재 된 Windows 볼륨을 일치 하는 이름의 mountinfo DrvFs에 나타납니다
- /home 및 /root 이제 올바른 이름의 mountinfo에 표시
- 추가 버그 수정 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>14942 빌드

일반 Windows에 대 한 14942 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)합니다.<br/>


### <a name="fixed"></a>고정

- 다양 한 메모리를 포함 하는 "시도 실행의 NOEXECUTE" 네트워킹 SSH 차단 된 충돌 해결 버그
- inotifiy DrvFs에서 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원은 이제
- TCP_KEEPIDLE 및 TCP_KEEPINTVL mongod에 대 한 구현 합니다. (GH #695)
- Pivot_root 시스템 호출을 구현 합니다.
- SO_DONTROUTE 소켓 옵션을 구현 합니다.
- 추가 버그 수정 및 향상 된 기능


### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 665 </br>
불합격 개수 (실패, 건너뜀 등...): 263 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>14936 빌드

일반 Windows에 대 한 14936 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)합니다.<br/>


참고: WSL 예정 된 릴리스에서 Ubuntu 버전 16.04 (Xenial) 대신 Ubuntu 14.04 (신뢰할 수 있는)를 설치 합니다.  이 변경 (lxrun.exe /install 또는 bash.exe의 첫 번째 실행)의 새 인스턴스를 설치 하는 참가자에 적용 됩니다.  신뢰할 수 있는 사용 하 여 기존 인스턴스는 자동으로 업그레이드 되지 않습니다. 사용자 믿음직한 이미지 Xenial 수행 릴리스 업그레이드 명령을 사용 하 여 업그레이드할 수 있습니다.

### <a name="known-issue"></a>알려진된 문제
WSL에서 일부 소켓 구현 문제가 발생 했습니다.  버그 확인 자체 명시 "시도 실행의 NOEXECUTE MEMORY" 오류와 충돌 합니다.  이 문제의 가장 일반적인 특성 충돌이 경우 ssh를 사용 하 여입니다.  근본 원인을 내부 빌드에 고정 하 고 가능한 한 빨리 참가자에 밀어넣습니다.

### <a name="fixed"></a>고정

- Chroot 시스템 호출이 구현
- Inotify의 향상 된 기능 ~~DrvFs에서 Windows 응용 프로그램에서 생성 된 알림에 대 한 지원을 비롯 하 여~~
  - 수정: Inotify 지금은 사용할 수 없는 Windows 응용 프로그램에서 시작 된 변경을 지원 합니다.
- 소켓을 IPV6 바인딩::<port n> IPV6_V6ONLY는 이제 (GH #68, #157, #393, #460, #674, #740, #982, #996)
- Waitid systemcall 구현 (GH #638)에 대 한 WNOWAIT 동작
- IP_HDRINCL 및 IP_TTL IP 소켓 옵션에 대 한 지원
- 길이가 0 인 read ()가 즉시 반환 하도록 (GH #975)
- .Tar 파일에는 NULL 종결자를 포함 하지 않는 파일 이름 및 파일 이름 접두사를 올바르게 처리 합니다.
- /dev/null epoll 지원
- /Dev/alarm 시간 원본 수정
- -C 파일을 리디렉션할 수 이제 bash
- 추가 버그 수정 및 향상 된 기능

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 664 </br>
불합격 개수 (실패, 건너뜀 등...): 264 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>14931 빌드

일반 Windows에 대 한 14931 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)합니다.<br/>


### <a name="fixed"></a>고정

 - 제어권 초과 상황으로 인해 업데이트가 없는 Linux 용 Windows 하위 시스템에 대 한이 빌드 에입니다.  정기적으로 예약 된 업데이트는 다음 릴리스에서 다시 시작 됩니다.

<br/>

## <a name="build-14926"></a>14926 빌드

일반 Windows에 대 한 14926 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)합니다.<br/>


### <a name="fixed"></a>고정

- Ping 이제 관리자 권한이 없는 콘솔에서 작동 합니다.
- 이제 지원도 관리자 권한 없이 Ping6
- WSL를 통해 수정 된 파일에 대 한 Inotify 지원 합니다. (GH #216)
  - 플래그를 지원 합니다.
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch 이벤트: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 출력을 읽어보세요. LX_IN_ISDIR, LX_IN_IGNORED
  - 알려진된 문제: 이벤트를 생성 하지 않는 Windows 응용 프로그램에서 파일 수정
- Unix 소켓에 이제 SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP 결과:
통과 한 테스트 수: 651 </br>
불합격 개수 (실패, 건너뜀 등...): 258 </br>
[LTP 테스트 실행 로그](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>14915 빌드

일반 Windows에 대 한 14915 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)합니다.<br/>


### <a name="fixed"></a>고정
-  Unix 데이터 그램 소켓 (GH #262)에 대 한 Socketpair
- SO_REUSEADDR Unix 소켓 지원
- UNIX 소켓 지원 SO_BROADCAST (GH #568)
- Unix 소켓 지원 SOCK_SEQPACKET (GH #758, #546)
- Unix 데이터 그램 소켓 전송, 수신 및 종료에 대 한 지원 추가
- 고정 되지 않은 주소에 대 한 잘못 된 mmap 매개 변수 유효성 검사로 인해 오류 검사를 수정 합니다. (GH #847)
- 일시 중단에 대 한 지원 / 터미널 상태는 다시 시작
- 화면 유틸리티 (GH #774) 차단을 해제 하려면 TIOCPKT ioctl에 대 한 지원
    - 알려진된 문제: 기능 키 작동 하지 않음
- 해제 된 멤버 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814)에서 액세스 될 수 있는 TimerFd 경합이 수정
- Futex, 설문 조사, 및 clock_nanosleep 다시 시작할 수 있는 시스템 호출 지원을 사용 하도록 설정
- 추가 바인딩 탑재 지원
- 탑재 네임 스페이스 지원에 대 한 공유 해제
    - 알려진된 문제: 사용 하 여 새 탑재 네임 스페이스를 만들 때 `unshare(CLONE_NEWNS)` 현재 작업 디렉터리를 이전 네임 스페이스를 가리키도록 계속 합니다.
- 추가 개선 사항 및 버그 수정

<br/>

## <a name="build-14905"></a>14905 빌드

일반 Windows에 대 한 14905 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)합니다.<br/>


### <a name="fixed"></a>고정
- 다시 시작할 수 있는 시스템 호출 됩니다 (GH #349, GH #520) 지원
- Symlink 디렉터리에 / 이제 작업 종료 (GH #650)
- /Dev/random에 대 한 구현된 RNDGETENTCNT ioctl
- [Pid] /proc/ 구현 / 탑재를 /proc/ [pid] / mountinfo 및 /proc/ [pid] / mountstats 파일
- 추가 버그 수정 및 향상 된 기능

</br>

## <a name="build-14901"></a>14901 빌드
Windows 10 1 주년 업데이트 릴리스 게시물에 대 한 첫 번째 참가자 빌드.

일반 Windows에 대 한 14901 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)합니다.<br/>


### <a name="fixed"></a>고정
- 후행 슬래시 문제 해결된
    - 같은 명령 `$ mv a/c/ a/b/` 이제 작동
- Ubuntu 로캘 Windows 로캘을 설정 해야 하는 경우 이제 프롬프트 설치
- Ns 폴더에 대 한 procfs 지원
- 탑재를 추가 및 tmpfs procfs 한 sysfs 파일 시스템 탑재 해제
- [At] 32 비트 ABI 서명 mknod 수정
- 모델에 디스패치할 때 이동 하는 Unix 소켓
- INET 소켓 수신 버퍼 크기는 setsockopt를 사용 하 여 설정에 적용 되어야 합니다.
- 구현 MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그
- Linux 프로세스 stdin/stdout 파이프 리디렉션 (GH #2)
    - 명령줄에서 bash-c 명령의 파이핑 허용  예: > dir | bash-c "grep foo"
- Bash은 이제 여러 사용량과 (GH #538, #358)를 사용 하 여 시스템에 설치할 수 있습니다.
- 기본 INET 소켓 버퍼 크기를 일치 해야 함을 기본 Ubuntu 설치
- Xattr syscall listxattr에 맞춤
- 유효한 IPv4 주소를 사용 하 여 인터페이스 SIOCGIFCONF에서 반환
- 신호 ptrace에 의해 삽입 된 경우 기본 동작 수정
- implement /proc/sys/vm/min_free_kbytes
- Sigreturn 컨텍스트를 복원 하는 경우 컴퓨터 컨텍스트 등록 값을 사용 합니다.
    - Java 및 javac 일부 사용자에 대 한 중지 된 문제 해결
- /Proc/sys/kernel/hostname 구현

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Windows 10 1 주년 업데이트에 14388 빌드
일반 Windows에 대 한 14388 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/14388wip)합니다. <br/>

### <a name="fixed"></a>고정
- 8/2에서 Windows 10 1 주년 업데이트에 대 한 준비를 수정 합니다.
  - WSL 1 주년 업데이트에 대 한 자세한 내용은에서 확인할 수 있습니다이 [블로그](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>14376 빌드
일반 Windows에 대 한 14376 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)합니다. <br/>

### <a name="fixed"></a>고정
- Get apt (GH #493)를 중지 하는 되는 일부 인스턴스에서 제거
- 빈 탑재 올바르게 처리 되지 않은 문제를 해결 함
- Ramdisks 올바르게 탑재 되지 않은 문제를 해결 함
- (부분 GH #451) 플래그를 지원 하기 위해 변경 unix 소켓 수락
- 고정된 공용 네트워크 관련 블루 스크린
- 블루 스크린 /proc/ [pid]에 액세스할 때 고정 (GH #523) 작업 /
- 일부 pty 시나리오 (GH #488, #504)에 대 한 고정된 높은 CPU 사용률
- 추가 버그 수정 및 향상 된 기능

<br/>

## <a name="build-14371"></a>14371 빌드
일반 Windows에 대 한 14371 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)합니다. <br/>

### <a name="fixed"></a>고정
- SIGCHLD wait()와 타이밍 경합 ptrace를 사용 하는 경우 수정
- 경로 후행를 포함 하는 경우 몇 가지 동작을 수정 / (GH #432)
- 이름 바꾸기 끊고 열린 핸들을 자식으로 인해 실패 한 문제 해결된
- 추가 버그 수정 및 향상 된 기능

<br/>

## <a name="build-14366"></a>14366 빌드
일반 Windows에 대 한 14366 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)합니다. <br/>

### <a name="fixed"></a>고정
- Symlink 통해 파일 생성에서 수정
-   Python (GH 385)에 대 한 추가 listxattr
-   추가 버그 수정 및 향상 된 기능

### <a name="syscall-support"></a>Syscall 지원
-   다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>빌드 14361
일반 Windows에 대 한 빌드 14361에서 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14361)합니다. <br/>

### <a name="fixed"></a>고정
- Windows에서 Ubuntu의 Bash에서 실행 중인 경우 DrvFs 대/소문자 구분 됩니다.
  - 사용자가 월 case.txt 및 사례입니다. TXT 해당/mnt c 드라이브
  - Windows에서 ubuntu의 Bash에서 대/소문자만 지원 됩니다. 경우 NTFS Bash의 외부 파일을 올바르게 보고 됩니다 있지만 Windows에서 파일을 사용 하 여 상호 작용 예기치 않은 동작이 발생할 수 있습니다.
  - 각 볼륨 (즉, /mnt/c)의 루트가 대/소문자 구분 되지 않습니다.
  - Windows에서 이러한 파일을 처리 하는 방법은 찾을 수 있습니다 [여기](https://support.microsoft.com/en-us/kb/100625)합니다.
- 크게 향상 pty / tty 지원 합니다.  이제 지원 됩니다 (GH #40) TMUX와 같은 응용 프로그램
- 사용자 계정이 항상 생성 하는 고정 된 설치 문제
- 매우 긴 인수 목록에 대 한 허용 하는 명령줄 인수 구조를 최적화 합니다. (GH #153)
- DrvFs에서 삭제 및 chmod read_only 파일 이제 수
- 일부 경우에서 터미널 중지 (GH #43)를 분리 하는 위치를 수정 합니다.
- chmod 및 chown 이제 tty 장치에서 작동
- 0.0.0.0으로 연결을 허용 하 고:: localhost (#388 GH)
- Sendmsg/recvmsg의는 IO 벡터 길이 이제 처리할 > 1 (부분 GH #376)
- 사용자가 이제 옵트아웃할 수 자동으로 생성 된 호스트 파일 (GH #398)의
- 자동으로 NT 로캘로 Linux 로캘 (GH #11) 설치 하는 동안 일치
- /Proc/sys/vm/swappiness 파일 (GH #306) 추가
- strace 이제 올바르게 종료
- 파이프 /proc/self/fd (GH #222)를 통해 다시 열 수를 허용 합니다.
- 디렉터리가 %LOCALAPPDATA%\lxss DrvFs (GH #270)에서 숨기기
- Bash.exe 보다 효율적으로 처리 ~입니다.  와 같은 명령도 "bash ~-c ls" (GH #467) 지원
- 소켓에는 이제 epoll 알림 (GH #271) 종료 하는 동안 사용할 수 있는 읽기
- lxrun / 제거는 더 효율적으로 파일 및 폴더를 삭제 합니다.
- 수정 된 ps-f (GH #246)
- X11 지원 개선 xEmacs (GH #481)와 같은 앱
- 초기 스레드 스택 크기 기본값 Ubuntu 및 크기를 올바르게 보고 get_rlimit syscall (GH # 172를 #258)를 일치 시키는 업데이트
- Pico 프로세스 이미지 이름 (예: 감사) 보고 개선
- Df 명령에 대 한 구현된 /proc/mountinfo
- 자식 이름에 대 한 고정된 symlink 오류 코드입니다. 및...
- 추가 개선 사항 버그 수정 및 향상 된 기능

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>빌드 14352
일반 Windows에 대 한 빌드 14352에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14352)합니다.<br/>


### <a name="fixed"></a>고정
- 큰 파일 된 되지 않음 다운로드 / 올바르게 생성 문제를 해결 했습니다.  Npm 및 다른 시나리오 (GH 3, GH #313) 차단을 해제 해야이
- 소켓의 중지 일부 인스턴스를 제거 합니다.
- 일부 ptrace 오류 수정
- 파일 이름이 255 자 보다 긴 허용 WSL 사용 하 여 문제 해결된
- 영어가 아닌 문자에 대 한 향상 된 지원
- 현재 Windows 표준 시간대 데이터를 추가 하 고 기본값으로 설정
- 고유한 장치 id의 각각에 대 한 탑재 지점 (jre 수정-GH #49)
- 포함 하는 경로 사용 하 여 문제를 해결 합니다. "." 및 "..."
- Fifo 지원이 추가 되었습니다 (#71 GH)
- 업데이트 된 형식의 기본 Ubuntu 형식과 일치 하도록 하기 위해 resolv.conf
- 일부 procfs 정리
- 관리자 콘솔 (GH #18)에 대해 설정 된 ping

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>14342 빌드
일반 Windows에 대 한 정보 빌드 14342 합니다 [Windows 블로그](https://aka.ms/wip14342)합니다. <br/>

VolFs 및 DriveFs에 대 한 정보를 확인할 수 있습니다 합니다 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl)합니다. <br/>

### <a name="fixed"></a>고정
- Windows 사용자 사용자 이름에 유니코드 문자가 있을 때에 설치 문제를 해결 함
- FAQ apt get 업데이트 udev 해결 방법은 첫 번째 실행에서 기본적으로 제공 됩니다.
- DriveFs에 symlink를 사용 하도록 설정 (/mnt/<drive>) 디렉터리
- Symlink은 DriveFs 사이의 VolFs 이제 작동
- 주소가 지정 된 상위 수준 경로 문제를 구문 분석: l s. / / 이제 정상적으로 작동 됩니다
- DriveFs에 npm 설치 하 고-g 옵션은 이제 작동
- PHP 서버를 시작 하지 못하도록 방지 하는 문제 해결된
- 네이티브 Ubuntu에 더 가깝게 맞게 $PATH 같은 업데이트 된 기본 환경 값
- Apt 패키지 캐시를 업데이트 하는 Windows에서 매주 유지 관리 작업을 추가
- ELF 헤더 유효성 검사를 사용 하 여 문제를 해결, WSL 이제 모든 Melkor 옵션
- Zsh shell은 기능
- 이동의 미리 컴파일된 이진 파일은 이제 지원
- 올바르게 이제 지역화 된 Bash.exe 첫 번째 실행에서 메시지를 표시
- /proc/meminfo 이제 올바른 정보를 반환
- 이제 VFS에서 지원 되는 소켓
- 사용 하기 위해 /dev 이제 tempfs로 탑재
- Fifo 이제 지원
- 이제/proc/cpuinfo에 올바르게 표시 하는 다중 코어 시스템
- 추가 개선 사항 및 첫 번째 실행 동안 다운로드 하는 오류 메시지
- Syscall 개선 사항 및 버그 수정입니다. 아래 지원 되는 syscall 목록입니다.
- 추가 버그 수정 및 향상 된 기능

### <a name="known-issues"></a>알려진 문제
- 확인 하지 못하는 '..' 일부 경우에는 DriveFs에서 올바르게

### <a name="syscall-support"></a>Syscall 지원
다음은 새롭거나 향상 된 syscall WSL 구현에 있는 목록입니다. 이 목록에 syscall 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

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

## <a name="build-14332"></a>14332 빌드

일반 Windows에 대 한 14332 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14332)합니다. <br/>


### <a name="fixed"></a>고정
- DNS 항목을 우선 순위 지정을 비롯 한 효율적인 resolv.conf 생성
- /Mnt 사이 및 비 파일 및 디렉터리를 이동 하는 문제가-mnt 드라이브 /
- Tar 파일 symlink를 사용 하 여 만들 수 있습니다.
- 인스턴스 만들기에서 추가 기본 /run/lock 디렉터리
- 적절 한 상태 정보를 반환할 /dev/null 업데이트
- 첫 번째 실행 동안 다운로드 하는 경우 추가 오류
- Syscall 개선 사항 및 버그 수정입니다. 아래 지원 되는 syscall 목록입니다.
- 추가 개선 사항 버그 수정 및 향상 된 기능

### <a name="syscall-support"></a>Syscall 지원
다음은 WSL에서 구현 된 새 syscall입니다. Syscall이이 목록에는 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수가 지원 되지이 이번.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>빌드 14328

일반 Windows에 대 한 14332 빌드에 대 한 정보를 방문 합니다 [Windows 블로그](https://aka.ms/wip14328)합니다. <br/>


### <a name="new-features"></a>새로운 기능
* 이제 Linux 사용자를 지원 합니다.  Windows에서 ubuntu의 Bash를 설치한 Linux 사용자를 만드는 메시지가 나타납니다.  자세한 내용은 참조 하세요. https://aka.ms/wslusers
* Hostname는 Windows 컴퓨터 이름에 더 이상 설정 되었습니다. @localhost
* 빌드 14328 대 한 자세한 내용은 참조 하십시오. https://aka.ms/wip14328

### <a name="fixed"></a>고정
* 비 /mnt/ Symlink 향상<drive> 파일
    * npm 설치가 작동
    * jdk 지침을 사용 하 여 설치할 수 있는 이제 jre [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)합니다.
    * 알려진 문제: Windows 탑재에 대 한 symlink 작동 하지 않습니다.  기능을 이후 빌드에서 사용할 수 있습니다.
* 위쪽과 htop 표시
* 추가 오류 메시지 일부에 대 한 설치 실패
* Syscall 개선 사항 및 버그 수정입니다.  아래 지원 되는 syscall 목록입니다.
* 추가 개선 사항 버그 수정 및 향상 된 기능

### <a name="syscall-support"></a>Syscall 지원
다음은 syscall WSL 구현에 있는 목록입니다.  Syscall이이 목록에 하나 이상의 시나리오에서 지원 되지만 수 있는 모든 매개 변수에서 지원 되지 않습니다이 시간.

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
