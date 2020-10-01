---
title: FAQ(질문과 대답)
description: 'Linux용 Windows 하위 시스템에 대한 FAQ(예: WSL로 무엇을 할 수 있나요?)의 답변을 찾아보세요.'
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, FAQ
ms.date: 09/15/2020
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: f769261bab35619b034e2a84e4f308eeb0a93cb4
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413243"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템에 대한 질문과 대답

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>WSL(Linux용 Windows 하위 시스템)이란?

WSL(Linux용 Windows 하위 시스템)은 기존 Windows 데스크톱 및 최신 스토어 앱과 함께 Windows에서 네이티브 Linux 명령줄 도구를 직접 실행할 수 있는 새로운 Windows 10 기능입니다.

자세한 내용은 [정보 페이지](./about.md)를 참조하세요.

## <a name="who-is-wsl-for"></a>WSL은 누구를 위한 것인가요?

이는 주로 개발자, 특히 웹 개발자 및 오픈 소스 프로젝트에서 작업하는 사용자를 위한 도구입니다. 이 도구를 통해 Bash, 일반 Linux 도구(`sed`, `awk` 등) 및 많은 Linux 중심 도구(Ruby, Python 등)를 사용하려거나 사용해야 하는 사용자는 Windows에서 해당 도구 체인을 사용할 수 있습니다.

## <a name="what-can-i-do-with-wsl"></a>WSL로 무엇을 할 수 있나요?

WSL은 시작할 때 Bash 셸을 실행하는 Windows 콘솔을 여는 Bash.exe라는 애플리케이션을 제공합니다. Bash를 사용하면 Linux 명령줄 도구 및 앱을 실행할 수 있습니다. 예를 들어 `lsb_release -a`를 입력하고 Enter 키를 누릅니다. 그러면 현재 실행되고 있는 Linux 배포판의 세부 정보가 표시됩니다.

![배포판 세부 정보의 스크린샷](media/distro.png)

또한 Linux Bash 셸 내에서 로컬 머신의 파일 시스템에 액세스할 수 있습니다. 이 경우 로컬 드라이브는 `/mnt` 폴더 아래에 탑재되어 있습니다. 예를 들어 `C:` 드라이브가 `/mnt/c` 아래에 탑재되어 있습니다.  

![탑재된 C 드라이브의 스크린샷](media/ls.png)

## <a name="could-you-describe-a-typical-development-workflow-that-incorporates-wsl"></a>WSL이 통합된 일반적인 개발 워크플로를 설명할 수 있나요?

WSL은 내부 개발 루프의 일부로 사용하려는 개발자를 대상으로 합니다. Sam이 CI/CD 파이프라인(Continuous Integration & Continuous Delivery)을 만들고 있으며 클라우드에 배포하기 전에 로컬 머신(랩톱)에서 먼저 테스트하려 한다고 가정해 보겠습니다. Sam은 WSL(및 WSL 2)을 사용하여 속도와 성능을 향상시킨 다음, 원하는 Bash 명령어와 도구를 사용하여 로컬(랩톱 상의)에서 정품 Linux Ubuntu 인스턴스를 사용할 수 있습니다. 개발 파이프라인이 로컬에서 확인되면 Sam은 해당 CI/CD 파이프라인을 Docker 컨테이너로 만들고 프로덕션 준비가 된 Ubuntu VM에서 실행되는 클라우드 인스턴스로 푸시하여 이 컨테이너를 클라우드(예: Azure)까지 푸시할 수 있습니다.

## <a name="what-is-bash"></a>Bash란?

[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)는 널리 사용되는 텍스트 기반 셸 및 명령 언어입니다. 이는 Ubuntu, 기타 Linux 배포판 및 macOS에 포함된 기본 셸입니다. 사용자가 명령을 셸에 입력하여 스크립트를 실행하거나 명령과 도구를 실행하여 많은 작업을 수행합니다.

## <a name="how-does-this-work"></a>어떻게 작동하나요?

기본 기술에 대해 자세히 알아보려면 이 [블로그](/archive/blogs/wsl/)를 확인하세요.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>VM에서 Linux 대신 WSL을 사용하는 이유는 무엇인가요?

WSL에는 전체 가상 머신보다 적은 리소스(CPU, 메모리 및 스토리지)가 필요합니다. 또한 WSL을 사용하면 Windows 명령줄, 데스크톱 및 스토어 앱과 함께 Linux 명령줄 도구 및 앱을 실행하고 Linux 내에서 Windows 파일에 액세스할 수 있습니다. 이렇게 하면 원하는 경우 동일한 파일 세트에서 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>예를 들어 Windows 대신 Linux에서 Ruby를 사용하는 이유는 무엇인가요?

일부 플랫폼 간 도구는 이러한 도구가 실행되는 환경이 Linux처럼 동작한다고 가정하여 구축되었습니다. 예를 들어 일부 도구에서는 매우 긴 파일 경로에 액세스할 수 있거나 특정 파일/폴더가 있다고 가정합니다. 이로 인해 Windows에서 Linux와 다르게 동작하는 문제가 발생하는 경우가 많습니다.

Ruby 및 Node와 같은 많은 언어는 Windows에서 이식되고 매우 효율적으로 실행되는 경우가 많습니다. 그러나 일부 Ruby Gem 또는 Node/NPM 라이브러리 소유자는 Windows를 지원하기 위해 라이브러리를 이식하지 않으며 많은 소유자가 Linux 관련 종속성을 사용하고 있습니다. 이로 인해 이러한 도구와 라이브러리를 사용하여 빌드된 시스템의 Windows에서 빌드 및 때로는 런타임 오류 또는 원치 않는 동작이 발생하는 경우가 많습니다.

이러한 문제 중 일부는 Windows의 명령줄 도구를 개선하도록 많은 사용자가 Microsoft에 요청하게 하였으며, Windows에서 네이티브 Bash 및 Linux 명령줄 도구를 실행할 수 있도록 하기 위해 Microsoft에서 Canonical과 파트너 관계를 맺게 하였습니다.

## <a name="what-does-this-mean-for-powershell"></a>PowerShell에서 의미하는 것은 무엇인가요?

OSS 프로젝트에서 작업하는 동안 PowerShell 프롬프트에서 Bash를 사용하는 것이 매우 유용한 시나리오가 많이 있습니다. Bash 지원은 보완적이며 Windows에서 명령줄의 가치를 강화하여 PowerShell 및 PowerShell 커뮤니티에서 널리 사용되는 다른 기술을 활용할 수 있도록 합니다.

자세한 내용은 [Windows용 Bash: 뛰어난 기능 및 PowerShell에 대한 의미는 무엇일까요?](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)라는 PowerShell 팀 블로그를 참조하세요.

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL에서 모든 Linux 앱을 실행할 수 있나요?

아니요! WSL은 필요한 사용자가 Windows에서 Bash 및 핵심 Linux 명령줄 도구를 실행할 수 있도록 설정하기 위한 도구입니다.

WSL은 GUI 데스크톱 또는 애플리케이션(예: Gnome, KDE 등)을 지원하지 **않습니다**.  

또한 널리 사용되는 여러 서버 애플리케이션(예: Redis)을 실행할 수 있지만 프로덕션 서비스 호스팅에는 WSL을 추천하지 않습니다. Microsoft는 Azure, Hyper-V 및 Docker에서 프로덕션 Linux 워크로드를 실행하는 다양한 솔루션을 제공합니다. 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL이 포함된 Windows SKU는 무엇인가요?

Linux용 Windows 하위 시스템은 Windows 10 1주년 및 크리에이터스 업데이트 이상의 Windows 데스크톱 버전에서 사용할 수 있습니다.

Fall Creators Update부터 WSL은 Windows의 데스크톱 및 서버 SKU에서 모두 사용할 수 있습니다.

## <a name="what-processors-does-wsl-support"></a>WSL에서 지원하는 프로세서는 무엇인가요?

WSL은 x64 및 ARM CPU를 지원합니다.

## <a name="how-do-i-access-my-c-drive"></a>내 C: 드라이브에는 어떻게 액세스하나요?

로컬 머신의 하드 드라이브에 대한 탑재 지점이 자동으로 만들어져 Windows 파일 시스템에 쉽게 액세스할 수 있습니다.

**/mnt/\<drive letter>/**

예를 들어 c:\에 액세스하려면 `cd /mnt/c`를 사용합니다.

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a>Git 자격 증명 관리자는 어떻게 설정하나요? (WSL에서 내 Windows Git 권한을 어떻게 사용하나요?) 

Git 자격 증명 관리자를 사용하면 Azure Active Directory 또는 2단계 인증과 같은 복잡한 인증 패턴이 있는 경우에도 원격 Git 서버를 인증할 수 있습니다. Git 자격 증명 관리자는 GitHub와 같은 서비스의 인증 흐름에 통합되며, 사용자가 호스팅 공급자에 인증되면 새 인증 토큰을 요청합니다. 그런 다음, Windows 자격 증명 관리자에 토큰을 안전하게 저장합니다. 처음 인증하고 나면 다시 인증할 필요 없이 Git을 사용하여 호스팅 공급자와 통신할 수 있습니다. Git이 Windows 자격 증명 관리자의 토큰에 액세스할 것입니다.

WSL 배포판과 함께 사용할 Git 자격 증명 관리자를 설정하려면 배포판을 열고 다음 명령을 입력합니다.

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

이제 사용자가 WSL 배포판 내에서 수행하는 모든 Git 작업에서 자격 증명 관리자를 사용합니다. 호스트용으로 캐시된 자격 증명이 이미 있는 경우 자격 증명 관리자에서 액세스됩니다. 그렇지 않다면 자격 증명을 요청하는 대화 상자 응답이 수신됩니다(Linux 콘솔에 있을 경우도).

이 지원은 [Linux 및 Windows 자체의 Windows 하위 시스템 간의 상호 운용성](./interop.md)을 기반으로 합니다.

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux 앱에서 Windows 파일을 사용하려면 어떻게 하나요?

WSL의 이점 중 하나는 Windows 및 Linux 앱 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다. 

WSL은 머신의 고정 드라이브를 Linux 배포판의 `/mnt/<drive>` 폴더 아래에 탑재합니다. 예를 들어 `C:` 드라이브는 `/mnt/c/` 아래에 탑재됩니다.

탑재된 드라이브를 사용하면 [Visual Studio](https://visualstudio.microsoft.com/vs/) 또는 [VS Code](https://code.visualstudio.com/)를 사용하여 `C:\dev\myproj\`에서 코드를 편집하고, `/mnt/c/dev/myproj`를 통해 동일한 파일에 액세스하여 Linux에서 해당 코드를 빌드/테스트할 수 있습니다.

> **중요 참고 사항**: WSL을 사용하는 경우의 주요 제한 사항 중 하나는 Windows 앱 또는 도구를 사용하여 Linux 배포판의 파일 시스템에 있는 파일에 직접 액세스하여 변경할 수 없다는 것입니다. 다음을 참조하세요. [Windows 앱 및 도구를 사용하여 Linux 파일 변경 안 함](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux 드라이브의 파일이 탑재된 Windows 드라이브와 다른가요?

1. Linux 루트(예: `/`) 아래의 파일은 다음을 포함하지만 이에 국한되지 않는 Linux 특정 동작을 모방하는 WSL에서 제어합니다.
   * 잘못된 Windows 파일 이름 문자가 포함된 파일
   * 관리자가 아닌 사용자에 대해 만들어진 symlink
   * chmod 및 chown을 통한 파일 특성 변경
   * 파일/폴더 대/소문자 구분

2. 탑재된 드라이브의 파일은 Windows에서 제어하며 다음과 같은 동작을 수행합니다.
   * 대/소문자 구분 지원
   * 모든 권한이 Windows 권한을 가장 잘 반영하도록 설정됨

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>apt-get upgrade를 실행할 때 많은 오류가 발생하는 이유는 무엇인가요?

일부 패키지는 아직 구현하지 않은 기능을 사용합니다. 예를 들어 `udev`는 아직 지원되지 않으므로 여러 `apt-get upgrade` 오류가 발생합니다.

`udev`와 관련된 문제를 해결하려면 다음 단계를 수행합니다.

1. 다음을 `/usr/sbin/policy-rc.d`에 작성하고 변경 내용을 저장합니다.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 실행 권한을 `/usr/sbin/policy-rc.d`에 추가합니다.

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. 다음 명령을 실행합니다.

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL 배포를 제거하려면 어떻게 하나요?

1709(16299) 이전의 빌드에서 명령 프롬프트를 열고 다음을 실행합니다.

  ```batchfile
  lxrun /uninstall /full
  ```
  
스토어에서 설치된 WSL 배포는 다른 Windows 앱처럼 마우스 오른쪽 단추로 앱 타일을 클릭하고 [제거]를 클릭하거나 [`Remove-AppxPackage` cmdlet](/previous-versions//hh856038(v=technet.10))을 사용하여 PowerShell을 통해 제거할 수 있습니다.

## <a name="why-does-ping-generate-permission-denied-errors"></a>ping에서 권한 거부 오류가 생성되는 이유는 무엇인가요?

14926 이전의 WSL 빌드에서 ping은 WSL이 관리자 권한으로 실행되는 콘솔을 통해 실행되도록 요구했습니다. 이 문제는 14926 빌드 이상에서 해결되었습니다.

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH 서버를 실행하려면 어떻게 하나요?

WSL에서 OpenSSH를 실행하려면 Windows의 관리자 권한이 필요합니다. OpenSSH 서버를 실행하려면 Windows의 Ubuntu에서 관리자 권한으로 Bash를 실행하거나 CMD/PowerShell 프롬프트에서 관리자 권한으로 bash.exe를 실행합니다.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>설치하려고 하면 "오류: 0x80040306"이 발생하는 이유는 무엇인가요?

WSL은 레거시 콘솔에서 실행할 수 없습니다. 레거시 콘솔을 해제하려면 다음을 수행합니다.

1. WSL, PowerShell 또는 Cmd를 엽니다.
1. 마우스 오른쪽 단추로 제목 표시줄-> 속성을 차례로 클릭하고, "레거시 콘솔 사용"의 선택을 취소합니다.
1. 확인을 클릭합니다.

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Windows를 업그레이드한 후 bash.exe를 실행하면 "오류: 0x80040154"가 발생하는 이유는 무엇인가요?

Windows 업데이트 중에 "Linux용 Windows 하위 시스템" 기능이 사용하지 않도록 설정될 수 있습니다. 이 문제가 발생하면 Windows 기능을 다시 사용하도록 설정해야 합니다. "Linux용 Windows 하위 시스템" 기능을 사용하도록 설정하는 방법에 대한 지침은 [설치 가이드](./install-win10.md)에서 확인할 수 있습니다.

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL의 표시 언어를 변경하려면 어떻게 하나요?

WSL 설치는 Windows 설치의 로캘과 일치하도록 Ubuntu 로캘을 자동으로 변경하려고 합니다. 이 동작을 원하지 않는 경우 설치가 완료된 후 다음 명령을 실행하여 Ubuntu 로캘을 변경할 수 있습니다. 이 변경 내용이 적용되려면 bash.exe를 다시 시작해야 합니다.

아래 예제에서는 로캘을 en-US로 변경합니다.

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>WSL에서 인터넷에 액세스할 수 없는 이유는 무엇인가요?

일부 사용자가 WSL에서 인터넷 액세스를 차단하는 특정 방화벽 애플리케이션의 문제를 보고했습니다. 보고된 방화벽은 다음과 같습니다.

1. Kaspersky
1. AVG
1. Avast

방화벽을 해제하면 액세스가 허용되는 경우도 있습니다. 단순히 방화벽을 설치하면 경우에 따라 액세스가 차단되는 것처럼 보입니다.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Windows의 WSL에서 포트에 액세스하려면 어떻게 하나요?
WSL은 Windows에서 실행되는 Windows의 IP 주소를 공유합니다. 따라서 localhost의 모든 포트에 액세스할 수 있습니다. 예를 들어 1234 포트에 웹 콘텐츠가 있는 경우 https://localhost:1234 를 Windows 브라우저에 연결할 수 있습니다.

## <a name="how-can-i-back-up-my-wsl-distros-or-move-them-from-one-drive-to-another"></a>내 WSL 배포판을 백업하거나 한 드라이브에서 다른 드라이브로 이동할 수 있나요?

배포판을 백업하거나 이동하는 가장 좋은 방법은 Windows 버전 1809 이상에서 사용할 수 있는 export/import 명령을 통하는 것입니다. `wsl --export` 명령을 사용하여 전체 배포를 tarball로 내보낼 수 있습니다. 그런 다음, `wsl --import` 명령을 사용하여 이 배포판을 WSL로 다시 가져올 수 있습니다. 이 명령을 사용하면 가져올 새 드라이브 위치의 이름을 지정할 수 있으므로 WSL 배포 상태를 백업 및 저장하거나 이동할 수 있습니다. 

Appdata 폴더의 파일을 백업하는 기존 백업 서비스(예: Windows Backup)는 Linux 파일을 손상시키지 않습니다.

## <a name="where-can-i-provide-feedback"></a>피드백을 어디에 제공할 수 있나요?

여러 채널을 통해 피드백을 공유하고 질문할 수 있습니다.

기술적인 문제가 있거나 새로운 기능을 요청하려면 Github 문제 추적기로 이동하세요.

* [GitHub 문제 추적기](https://github.com/Microsoft/BashOnWindows/issues)

최신 WSL 뉴스를 최신 상태로 유지하려면 다음을 수행하세요.

* [명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)
* Twitter. Twitter에서 [@craigaloewen](https://twitter.com/craigaloewen)를 팔로우하여 뉴스, 업데이트 등에 대해 알아보세요.