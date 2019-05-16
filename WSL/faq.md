---
title: FAQ(질문과 대답)
description: 질문과 대답 Windows 하위 시스템에 대 한 Linux 용입니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063271"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에 대 한 질문 질문과

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Windows 하위 시스템에 대 한 WSL (Linux) 란?
Linux (WSL) 용 Windows 하위 시스템에 함께 기존 Windows 데스크톱 및 최신 스토어 앱, Windows에서 직접 네이티브 Linux 명령줄 도구를 실행할 수 있는 새 Windows 10 기능입니다.

참조 된 [페이지에 대 한](./about.md) 대 한 자세한 내용은 합니다.

## <a name="who-is-wsl-for"></a>에 대 한 WSL는 누구 인가요?
이것이 기본적으로 개발자가-특히 웹 개발자 또는 오픈 소스 프로젝트를 사용 하 여 작업 하는 도구입니다. 이 사용자에 게 원하는/Bash, 일반적인 Linux 도구를 사용 해야 합니다. (`sed`, `awk`등) 및 (Ruby, Python 등) Windows에서 해당 도구 체인을 사용 하려면 여러 Linux 중심 도구입니다.

## <a name="what-can-i-do-with-wsl"></a>WSL를 사용 하 여 어떻게 해야 합니까?
WSL은 프로그램이 Bash.exe는 시작 될 때 호출, 열립니다 Bash 셸을 실행 하는 Windows 콘솔을 제공 합니다. Bash를 사용 하는 명령줄 Linux 도구 및 앱을 실행할 수 있습니다. 예를 들어 입력 `lsb_release -a` enter 키를 누릅니다 하 고 현재 실행 중인 Linux 배포판의 자세한 정보를 표시 합니다.

![배포 세부 정보 스크린샷](media/distro.png)

Linux Bash 셸 내에서 로컬 컴퓨터의 파일 시스템에 액세스할 수도 있습니다 – 아래의 탑재 된 로컬 드라이브를 찾을 수 있습니다는 `/mnt` 폴더입니다. 예를 들어 프로그램 `C:` 아래에서 드라이브를 탑재 `/mnt/c`:  

![탑재 된 C 드라이브의 스크린샷](media/ls.png)

## <a name="what-is-bash"></a>Bash 란?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 은 인기 있는 텍스트를 기반으로 셸 및 명령 언어입니다. MacOS에 Ubuntu 및 다른 Linux 배포판 내에 포함 된 기본 셸을 것입니다. 사용자는 스크립트를 실행 하거나 여러 작업을 수행 하는 명령 및 도구를 실행 하는 shell에 명령을 입력 합니다.

## <a name="how-does-this-work"></a>어떻게 작동합니까?
체크 아웃 우리의 [블로그](https://blogs.msdn.microsoft.com/wsl/) 기본 기술에 대 한 세부 정보로 이동 위치 합니다.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>VM의 Linux 대신 WSL 사용은 이유
WSL를 전체 가상 머신 보다 더 적은 리소스 (CPU, 메모리 및 저장소)에 필요합니다. WSL를 사용 하면 Linux 명령줄 도구 및 앱과 함께 Windows 명령줄에서 바탕 화면 및 스토어에서 앱을 실행 하 고 linux에서 Windows 파일에 액세스할 수 있습니다. 이 옵션을 사용 하면 원하는 경우 파일의 동일한 집합에 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>왜 사용 해야 합니까, 예를 들어 Windows 대신 Linux에서 Ruby?
일부 플랫폼 간 도구를 실행 하는 환경 Linux 처럼 가정 빌드됩니다. 예를 들어, 일부 도구는 매우 긴 파일 경로 액세스할 수 있는지 또는 특정 파일/폴더가 있음을 가정 합니다. 이 문제의 원인이 되기도 종종 동작 하는 Windows에서 다르게 Linux에서.

종종 Ruby 노드와 같은 많은 언어에 이식 되며, Windows에서 실행 합니다. 그러나 Windows를 지원 하기 위해 해당 라이브러리를 포트 Ruby 보석 또는 노드/NPM 라이브러리 소유자의 일부 Linux 관련 종속성이 있는 여러 하며 이 이러한 도구 및 라이브러리 빌드 및 경우에 따라 런타임 오류 또는 Windows에서 원치 않는 동작에서 포괄적으로 구축 된 시스템에서 자주 발생할 수 있습니다.

이들은 많은 사람들이 Windows' 명령줄 도구 및 canonical 네이티브 Bash 및 Linux 명령줄 도구를 Windows에서 실행할 수 있도록 파트너을 이끌기도 무엇을 개선 하기 위해 Microsoft에 게 발생 시킨 문제 중 일부에 불과합니다.

## <a name="what-does-this-mean-for-powershell"></a>PowerShell에 대 한 무슨 뜻인가요?
OSS 프로젝트를 사용 하는 동안 시나리오가 많은 것이 매우 유용한 PowerShell에서 Bash를 삭제 하려면 프롬프트입니다. Bash 지원을 보완 되며 Windows, 다른 인기 있는 기술을 활용 하 여 PowerShell 및 PowerShell 커뮤니티에서 명령줄의 값을 강화 합니다.

자세한 내용은 PowerShell 팀 블로그- [Bash에 대 한 Windows: 멋진 하는 이유 및 PowerShell에 끼치는 의미](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL에서 모든 Linux 앱을 실행할 수 있습니까?
아니요! WSL에 Bash를 실행 하 고 Windows에서 Linux 명령줄 도구를 코어 수 필요한 사용자 수 있도록 하기 위한 도구입니다. 

WSL 않습니다 **되지** GUI 데스크톱 또는 응용 프로그램 (예: Gnome, KDE 등)를 지원 하려고 합니다.  

또한도 수 많은 인기 있는 서버 응용 프로그램 (예: Redis) WSL 프로덕션 서비스를 호스팅하기 위한 권장 하지는 않습니다 – Microsoft는 다양 한 프로덕션을 Azure에서 Linux 워크 로드 실행에 대 한 솔루션을 제공 합니다. Hyper-v 및 Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>에 WSL에서 포함 되어 Windows Sku는 무엇입니까?
Linux 용 Windows 하위 시스템은 데스크톱 버전의 Windows 10 Anniversary Windows 및 크리에이터 스 업데이트 이상에서 사용할 수 있습니다.

부터 Fall Creators update WSL 데스크톱과 서버 Sku의 Windows에서 사용할 수 있습니다.

## <a name="what-processors-does-wsl-support"></a>WSL에서 어떤 프로세서를 지원 하나요?
WSL은 x64 및 ARM Cpu를 지원합니다.

## <a name="how-do-i-access-my-c-drive"></a>C: 드라이브에 액세스 하려면 어떻게 해야 합니까?
로컬 컴퓨터의 하드 드라이브에 대 한 탑재 지점을 자동으로 생성 됩니다 및 Windows 파일 시스템에 대 한 쉬운 액세스를 제공 합니다. 
 
**/mnt/\<드라이브 문자 > /**
 
사용 예 `cd /mnt/c` c:\ 액세스 하려면

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux 앱을 사용 하 여 Windows 파일을 사용 하는 방법

WSL의 이점 중 하나는 Windows 및 Linux 응용 프로그램 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다. 

WSL에서 컴퓨터의 고정된 드라이브를 탑재 합니다 `/mnt/<drive>` 에 Linux 배포판에 대 한 폴더입니다. 예를 들어 프로그램 `C:` 드라이브 아래에 탑재 됩니다 `/mnt/c/` 

탑재 된 드라이브를 사용 하 여 편집할 수 있습니다, 코드 예를 들어 `C:\dev\myproj\` 를 사용 하 여 [Visual Studio](https://visualstudio.microsoft.com/vs/) / 또는 [VS Code](https://code.visualstudio.com/), 및 Linux에서 해당 코드를 통해 동일한 파일에 액세스 하 여 빌드/테스트 `\mnt\c\dev\myproj`합니다.

> **중요 참고**: WSL를 사용 하는 주요 제한 사항 중 하나입니다는 직접 액세스/변경은 Windows 응용 프로그램 또는 도구를 사용 하 여 Linux 배포판의 파일 시스템에 파일이 지원 되지 않습니다. 참조 [Windows 앱 및 도구를 사용 하 여 Linux 파일을 변경 하지 마세요](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>탑재 된 Windows 드라이브에서 다양 한 Linux 드라이브의 파일은 있나요?

1. Linux 루트 아래에 있는 파일 (예: `/`) Linux 특정 동작을 포함 하지만에 제한 되지 않는 유사한 WSL에 의해 제어 됩니다.
   * 잘못 된 Windows 파일 이름 문자가 포함 된 파일
   * 관리자가 아닌 사용자를 위해 만든 Symlink
   * Chmod 및 chown를 통해 파일 특성 변경
   * 파일/폴더 대/소문자 구분

2. 탑재 된 드라이브의 Windows에 의해 제어 되는 파일과 다음과 같은 결과:
   * 대/소문자 구분을 지원 합니다.
   * 모든 권한은 가장 Windows 권한을 나타내도록 설정 됩니다.

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>이유는 무엇입니까 많은 오류 apt get 업그레이드를 실행할 때?
일부 패키지는 아직 구현 되지 않은 기능을 사용 합니다. `udev`예를 들어, 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류입니다.

관련 된 문제를 해결 하려면 `udev`, 다음 단계를 수행 합니다.

1. 다음을 작성 `/usr/sbin/policy-rc.d` 변경 내용을 저장 합니다.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 추가 권한을 실행 `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 다음 명령을 실행 합니다.

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL 배포를 제거 하려면 어떻게 해야 합니까?

1709 (16299) 열기 전에 명령 프롬프트를 빌드하고 실행 합니다.
  ```batchfile
  lxrun /uninstall /full
  ```
  
앱 타일을 마우스 오른쪽 단추로 클릭 하 고 제거를 클릭 하거나 사용 하 여 PowerShell을 통해 다른 Windows 앱 처럼 스토어에서 설치한 WSL 배포를 제거할 수 있습니다 합니다 [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)합니다.

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping 사용 권한 거부 오류를 생성 하는 이유
WSL 구축 < 14926, ping WSL 상승 된 콘솔을 통해 실행 하려면 필요 합니다. 빌드 14926 이상이 문제가 수정 되었습니다.

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH 서버를 실행 하려면 어떻게 해야 하나요?
WSL에서 OpenSSH를 실행 하려면 Windows에서 관리자 권한이 필요 합니다. OpenSSH 서버를를 실행 하려면 관리자로 서 Windows에서 Ubuntu의 Bash를 실행 하거나 bash.exe 관리자 권한으로 CMD/PowerShell 프롬프트에서 실행 합니다.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>왜 "오류: 0x80040306 "설치 하려고 하나요?
WSL 레거시 콘솔을 실행 하는 것을 지원 하지 않습니다. 레거시 콘솔 사용 하지 않으려면:

1. WSL, PowerShell 또는 Cmd를 열으십시오
1. 제목을 마우스 오른쪽 단추로 클릭-> 모음 속성의 선택을 취소 "레거시 콘솔 사용 하 여"->
1. 확인을 클릭합니다.

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>왜 "오류: 0x80040154 "Windows를 업그레이드 한 후 bash.exe를 실행 하나요?
"Windows 하위 시스템에 대 한 Linux" 기능을 비활성화할 수 있습니다 Windows 업데이트 중입니다. 이 경우 Windows 기능을 다시 사용 하도록 설정 해야 합니다. "Windows 하위 시스템에 대 한 Linux" 기능을 사용 하는 것에 대 한 지침을 찾을 수 있습니다 합니다 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)합니다.

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL의 표시 언어를 변경 하려면 어떻게 해야 합니까?
WSL 설치는 Windows 설치의 로캘이 일치 하는 Ubuntu 로캘을 자동으로 변경 하려고 합니다. 이 문제를 원하지 않는 경우 설치가 완료 되 면 Ubuntu 로캘을 변경 하려면이 명령을 실행할 수 있습니다. 이 변경 내용을 적용 하려면 bash.exe를 다시 시작 해야 합니다.

아래 예제에서는 EN-US 로캘 변경 합니다.
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>왜 없습니다 있습니까 WSL에서 인터넷 액세스?
일부 사용자에 게 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램을 사용 하 여 문제를 보고 했습니다. 보고 하는 방화벽은 다음과 같습니다.

1. Kaspersky
1. AVG
1. Avast

일부 경우에 대 한 액세스 허용 방화벽을 해제 합니다. 일부 경우에 대 한 액세스 차단 보일 방화벽이 설치 되어 있는 하기만 하면 됩니다.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>포트를 Windows에서 WSL에서 액세스 하려면 어떻게 해야 합니까?
WSL은 Windows에서 실행 되는 Windows에서의 IP 주소를 공유 합니다. 예: localhost에서 모든 포트에 액세스할 수 있습니다 따라서 1234 할 수 있습니다. 포트에서 웹 콘텐츠 했다면 https://localhost:1234 Windows 브라우저에 합니다.

## <a name="where-can-i-provide-feedback"></a>피드백을 제공할 수는 있는

피드백을 공유 하 고 여러 채널을 통해 궁금한 사항을 문의할 수 있습니다. 사용자 의견 및 질문을 전달 되어야 합니다.
* 우리의 [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* 우리의 [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* 우리의 [명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)
* Twitter를 통해. 따르세요 [ @richturn_ms ](https://twitter.com/richturn_MS) 뉴스, 업데이트를 파악 하는 Twitter에서 등입니다.
