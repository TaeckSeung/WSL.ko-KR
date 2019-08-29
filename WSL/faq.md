---
title: FAQ(질문과 대답)
description: Linux 용 Windows 하위 시스템에 대 한 질문과 대답입니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122759"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에 대 한 질문과 대답

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>WSL (Linux 용 Windows 하위 시스템) 이란?
WSL (Linux 용 Windows 하위 시스템)은 기존 Windows 데스크톱 및 최신 스토어 앱과 함께 Windows에서 직접 기본 Linux 명령줄 도구를 실행할 수 있도록 하는 새로운 Windows 10 기능입니다.

자세한 내용은 [정보 페이지](./about.md) 를 참조 하세요.

## <a name="who-is-wsl-for"></a>WSL은 누구 인가요?
주로 개발자를 위한 도구입니다. 특히 웹 개발자와 오픈 소스 프로젝트에서 작업 하는 사용자입니다. 이를 통해 Bash, 일반적인 linux 도구 (`sed`, `awk`등) 및 많은 Linux 중심 도구 (Ruby, Python 등)를 사용 해야 하는 사용자와 Windows에서 도구 체인를 사용할 수 있습니다.

## <a name="what-can-i-do-with-wsl"></a>WSL로 무엇을 할 수 있나요?
WSL은 bash 라는 응용 프로그램을 제공 합니다 .이 응용 프로그램은 시작 될 때 Bash 셸을 실행 하는 Windows 콘솔을 엽니다. Bash를 사용 하 여 명령줄 Linux 도구 및 앱을 실행할 수 있습니다. 예를 들어를 `lsb_release -a` 입력 하 고 enter 키를 누르면 현재 실행 중인 Linux 배포판의 세부 정보가 표시 됩니다.

![배포판 세부 정보 스크린샷](media/distro.png)

Linux Bash 셸 내에서 로컬 컴퓨터의 파일 시스템에 액세스할 수도 있습니다. 그러면 해당 폴더에 탑재 된 `/mnt` 로컬 드라이브를 찾을 수 있습니다. 예를 `C:` 들어 드라이브가 `/mnt/c`탑재 된 위치는 다음과 같습니다.  

![탑재 된 C 드라이브의 스크린샷](media/ls.png)

## <a name="what-is-bash"></a>Bash 란?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 는 널리 사용 되는 텍스트 기반 셸 및 명령 언어입니다. Ubuntu 및 기타 Linux 배포판 및 macOS 내에 포함 된 기본 셸입니다. 사용자는 셸에서 명령을 입력 하 여 스크립트를 실행 하거나 명령 및 도구를 실행 하 여 많은 작업을 수행 합니다.

## <a name="how-does-this-work"></a>어떻게 작동합니까?
기본 기술에 대해 자세히 설명 하는 [블로그](https://blogs.msdn.microsoft.com/wsl/) 를 확인 하세요.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>VM에서 Linux가 아닌 WSL을 사용 하는 이유는 무엇 인가요?
WSL은 전체 가상 컴퓨터 보다 많은 리소스 (CPU, 메모리 및 저장소)가 필요 합니다. 또한 WSL에서는 Windows 명령줄, 데스크톱 및 스토어 앱과 함께 Linux 명령줄 도구 및 앱을 실행 하 고 Linux 내에서 Windows 파일에 액세스할 수 있습니다. 이렇게 하면 원하는 경우 동일한 파일 집합에서 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>예를 들어 Windows 대신 Linux에서 Ruby를 사용 하는 이유는 무엇 인가요?
일부 플랫폼 간 도구는 이러한 도구가 실행 되는 환경이 Linux와 같이 동작 한다고 가정 하 여 구축 되었습니다. 예를 들어, 일부 도구는 매우 긴 파일 경로에 액세스할 수 있거나 특정 파일/폴더가 존재 한다고 가정 합니다. 이 경우 종종 Linux와 다르게 동작 하는 Windows에서 문제가 발생 합니다.

Ruby 및 노드와 같은 많은 언어는 Windows에서 자주 이식 되 고 실행 됩니다. 그러나 일부 Ruby 보석 또는 node/NPM library 소유자는 Windows를 지원 하기 위해 라이브러리를 이식 하는 것이 아니라 많은 Linux 관련 종속성이 있습니다. 이러한 도구 및 라이브러리를 사용 하 여 빌드한 시스템이 빌드 및 경우에 따라 Windows의 런타임 오류나 원치 않는 동작에서 발생 하는 경우가 많습니다.

이러한 문제 중 일부는 Windows의 명령줄 도구를 개선 하기 위해 Microsoft에 문의 하 고, 기본 Bash 및 Linux 명령줄 도구를 Windows에서 실행할 수 있도록 하기 위해 정식 파트너와 협력 하는 것입니다.

## <a name="what-does-this-mean-for-powershell"></a>PowerShell의 의미는 무엇 인가요?
OSS 프로젝트를 사용 하는 동안 PowerShell 프롬프트에서 Bash로 끌어 놓는 데 매우 유용한 여러 가지 시나리오가 있습니다. Bash 지원은 Windows에서 명령줄의 값을 보완 하며 PowerShell 및 PowerShell 커뮤니티에서 다른 인기 기술을 활용할 수 있도록 합니다.

PowerShell 팀 블로그- [Windows 용 Bash에서 자세히 알아보세요. 훌륭한 기능 및 PowerShell에 대 한 의미](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL에서 모든 Linux 앱을 실행할 수 있나요?
아니요! WSL은 Windows에서 Bash 및 핵심 Linux 명령줄 도구를 실행 하는 데 필요한 사용자를 사용 하도록 설정 하기 위한 도구입니다. 

WSL은 GUI 데스크톱 또는 응용 프로그램 (예: Gnome, KDE 등)을 지원 **하지** 않습니다.  

또한 널리 사용 되는 여러 서버 응용 프로그램 (예: Redis)을 실행할 수 있는 경우에도 프로덕션 서비스를 호스팅하기 위해 WSL을 사용 하지 않는 것이 좋습니다. Microsoft는 Azure, Hyper-v 및 Docker에서 프로덕션 Linux 워크 로드를 실행 하기 위한 다양 한 솔루션을 제공 합니다. 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL이 포함 된 Windows Sku는 무엇 인가요?
Windows 용 windows 하위 시스템은 windows 10 기념일 및 크리에이터 업데이트 이상용 Windows 데스크톱 버전에서 사용할 수 있습니다.

이 하 버전에서 시작 하 여 Windows의 데스크톱 및 서버 Sku에서 업데이트 WSL을 사용할 수 있습니다.

## <a name="what-processors-does-wsl-support"></a>WSL에서 지 원하는 프로세서는 무엇 인가요?
WSL은 x64 및 ARM Cpu를 지원 합니다.

## <a name="how-do-i-access-my-c-drive"></a>C: 드라이브에 액세스 어떻게 할까요??
로컬 컴퓨터의 하드 드라이브에 대 한 탑재 지점이 자동으로 만들어지고 Windows 파일 시스템에 쉽게 액세스할 수 있습니다. 
 
**/mnt/\<드라이브 문자 >/**
 
예제 사용법은 c:\ `cd /mnt/c` 에 액세스 하는 것입니다.

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux 앱과 함께 Windows 파일을 사용 어떻게 할까요??

WSL의 이점 중 하나는 Windows 및 Linux 앱 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다. 

Wsl은 Linux 배포판의 `/mnt/<drive>` 폴더에 컴퓨터의 고정 드라이브를 탑재 합니다. 예를 `C:` 들어 드라이브가`/mnt/c/` 

탑재 된 드라이브를 사용 하 `C:\dev\myproj\` 여 [Visual Studio](https://visualstudio.microsoft.com/vs/) /또는 [VS Code](https://code.visualstudio.com/)를 사용 하는 등의 코드를 편집 하 고를 통해 `/mnt/c/dev/myproj`동일한 파일에 액세스 하 여 Linux에서 해당 코드를 빌드/테스트할 수 있습니다.

> **중요 정보**: WSL을 사용 하는 경우의 주요 제한 사항 중 하나는 Windows 앱 또는 도구를 사용 하 여 Linux 배포판의 파일 시스템에서 직접 액세스/변경 하는 것입니다. 참조 [Windows 앱 및 도구를 사용 하 여 Linux 파일 변경 안 함](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux 드라이브의 파일이 탑재 된 Windows 드라이브와 다른 가요?

1. Linux 루트 (예 `/`:)에 있는 파일은 다음을 비롯 하 여 linux 특정 동작을 모방 하는 wsl에 의해 제어 됩니다.
   * 잘못 된 Windows 파일 이름 문자를 포함 하는 파일
   * 관리자가 아닌 사용자에 대해 생성 되는 symlink
   * Chmod 및 chown를 통해 파일 특성 변경
   * 파일/폴더 대/소문자 구분

2. 탑재 된 드라이브의 파일은 Windows에 의해 제어 되며 다음과 같은 동작을 수행 합니다.
   * 대/소문자 구분 지원
   * 모든 사용 권한은 Windows 사용 권한을 가장 잘 반영 하도록 설정 됩니다.

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Apt를 실행할 때 많은 오류가 발생 하는 이유는 무엇 인가요?
일부 패키지는 아직 구현 하지 않은 기능을 사용 합니다. `udev`예를 들어,는 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류가 발생 합니다.

와 관련 된 `udev`문제를 해결 하려면 다음 단계를 수행 합니다.

1. 에 다음을 `/usr/sbin/policy-rc.d` 작성 하 고 변경 내용을 저장 합니다.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 실행 권한 추가`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 다음 명령을 실행 합니다.

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL 배포를 제거할 어떻게 할까요? 있나요?

1709 이전의 빌드 (16299)에서 명령 프롬프트를 열고 다음을 실행 합니다.
  ```batchfile
  lxrun /uninstall /full
  ```
  
앱 타일을 마우스 오른쪽 단추로 클릭 하 고 제거를 클릭 하거나 [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)을 사용 하 여 PowerShell을 통해 저장소에서 설치 된 wsl 배포를 제거할 수 있습니다.

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping이 권한 거부 오류를 생성 하는 이유는 무엇 인가요?
WSL에서 14926 < 빌드는 관리자 권한 콘솔을 통해 실행 하는 데 필요한 WSL을 ping 합니다. 이 문제는 빌드 14926 이상에서 해결 되었습니다.

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH 서버를 실행할 어떻게 할까요? 있나요?
WSL에서 OpenSSH를 실행 하려면 Windows의 관리자 권한이 필요 합니다. OpenSSH 서버를 실행 하려면 관리자 권한으로 Windows의 Ubuntu에서 Bash를 실행 하거나 관리자 권한으로 CMD/PowerShell 프롬프트에서 bash를 실행 합니다.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>"오류: 0x80040306 "를 설치 하려고 하면
WSL은 레거시 콘솔에서 실행을 지원 하지 않습니다. 레거시 콘솔을 해제 하려면:

1. WSL, PowerShell 또는 Cmd를 엽니다.
1. 제목 표시줄-> 속성을 마우스 오른쪽 단추로 클릭 > "레거시 콘솔 사용" 선택을 취소 합니다.
1. 확인을 클릭합니다.

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>"오류: 0x80040154 "Windows를 업그레이드 한 후 bash를 실행 하는 경우
Windows 업데이트 중에 "Linux 용 Windows 하위 시스템" 기능이 사용 하지 않도록 설정 될 수 있습니다. 이 문제가 발생 하면 Windows 기능을 다시 사용 하도록 설정 해야 합니다. "Linux 용 Windows 하위 시스템" 기능을 사용 하도록 설정 하는 방법에 대 한 지침은 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)에서 찾을 수 있습니다.

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL의 표시 언어를 변경 어떻게 할까요?
WSL install은 Windows 설치의 로캘과 일치 하도록 Ubuntu 로캘을 자동으로 변경 하려고 합니다. 이 동작을 원하지 않는 경우 설치가 완료 된 후이 명령을 실행 하 여 Ubuntu 로캘을 변경할 수 있습니다. 이 변경 내용이 적용 되려면 bash를 다시 실행 해야 합니다.

아래 예제에서는 로캘을 en-us로 변경 합니다.
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>WSL에서 인터넷에 액세스할 수 없는 이유는 무엇입니까?
일부 사용자가 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램의 문제를 보고 했습니다. 보고 된 방화벽은 다음과 같습니다.

1. Kaspersky
1. 매출
1. Avast

방화벽을 해제 하면 액세스가 허용 되는 경우도 있습니다. 경우에 따라 방화벽을 설치 하면 액세스를 차단 하는 것으로 보입니다.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Windows의 WSL에서 포트에 액세스 어떻게 할까요??
WSL은 windows에서 실행 되는 Windows의 IP 주소를 공유 합니다. 따라서 localhost의 모든 포트 (예: 포트 1234 https://localhost:1234 에 웹 콘텐츠가 있는 경우)에 액세스할 수 있습니다.

## <a name="how-can-i-back-up-my-wsl-distros"></a>내 WSL 배포판을 백업 하려면 어떻게 해야 하나요?

배포판을 백업 하는 가장 좋은 방법은 Windows 버전 1809 이상에서 사용할 수 있습니다. `wsl --export` 명령을 사용 하 여 전체 배포를 tarball로 내보낼 수 있습니다. 그런 다음 `wsl --import` 명령을 사용 하 여이 배포판을 wsl로 다시 가져올 수 있으므로 wsl 배포판의 상태를 백업 하 고 저장할 수 있습니다. 

Appdata 폴더 (예: Windows 백업)의 파일을 백업 하는 기존 백업 서비스는 Linux 파일을 손상 하지 않습니다. 



## <a name="where-can-i-provide-feedback"></a>어디에서 피드백을 제공할 수 있나요?

여러 채널을 통해 피드백을 공유 하 고 질문할 수 있습니다. 사용자 의견 및 질문을 다음으로 전달 해야 합니다.
* [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)
* [명령줄 UserVoice 포털](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Microsoft [명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)
* Twitter를 통해. Twitter를 [@richturn_ms](https://twitter.com/richturn_MS) 따라 뉴스, 업데이트 등에 대해 알아보세요.
