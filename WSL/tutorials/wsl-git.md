---
title: Linux 용 Windows 하위 시스템에서 Git 사용 시작
description: Linux 용 Windows 하위 시스템에서 버전 제어를 위해 Git를 설정 하는 방법에 대해 알아봅니다.
keywords: wsl, windows, windowssubsystem, gnu, linux, bash, git, github, 버전 제어
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 94166371fc0928d6be3b3cfd6cb595c6fac76608
ms.sourcegitcommit: d95bdbc2fea991ba14a4c9ec53ee0ec19d6bbdb4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/05/2020
ms.locfileid: "84457795"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에서 Git 사용 시작

Git은 가장 일반적으로 사용 되는 버전 제어 시스템입니다. Git를 사용 하면 파일에 대 한 변경 내용을 추적할 수 있으며,이를 통해 수행 된 작업에 대 한 기록이 제공 되며 필요한 경우 이전 버전의 파일로 되돌릴 수 있습니다. 또한 Git를 사용 하면 공동 작업을 더 쉽게 수행할 수 있으므로 여러 사람이 변경한 내용을 하나의 원본으로 병합할 수 있습니다.

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a>Git은 Windows 및 WSL에 설치할 수 있습니다.

중요 한 고려 사항: WSL을 사용 하도록 설정 하 고 Linux 배포를 설치 하는 경우 Windows NTFS C:\에서 분리 된 새 파일 시스템을 설치 하 게 됩니다. 컴퓨터의 드라이브입니다. Linux에서 드라이브에는 문자가 제공 되지 않습니다. 지정 된 탑재 지점이 있습니다. 파일 시스템의 루트는 `/` WSL의 경우 루트 파티션 또는 폴더의 탑재 지점입니다. 의 모든 항목이 `/` 동일한 드라이브는 아닙니다. 예를 들어 내 노트북에서 Debian 뿐만 아니라 Ubuntu (20.04 및 18.01)의 두 가지 버전을 설치 했습니다. 이러한 배포를 열고 명령을 사용 하 여 루트 디렉터리를 선택한 `cd ~` 후 명령을 입력 하면 `explorer.exe .` Windows 파일 탐색기가 열리고 해당 배포에 대 한 디렉터리 경로가 표시 됩니다.

| Linux 배포판 | 홈 폴더에 액세스 하기 위한 Windows 경로 |
| ----------- | ----------- |
| Ubuntu 20.04 | `\\wsl$\Ubuntu-20.04\home\username` |
| Ubuntu 18.01 | `\\wsl$\Ubuntu-18.04\home\username` |
| Debian | `\\wsl$\Debian\home\username` |
| Windows PowerShell | `C:\Users\username` |

> [!TIP]
> 를 사용 하 여 windows 파일 디렉터리에 액세스 하려는 경우에는 대신 `C:\Users\username` 를 사용 하 여 디렉터리에 액세스할 수 있습니다 `/mnt/c/Users/username` . Linux 배포에서는 windows 파일 시스템을 탑재 된 드라이브로 보기 때문입니다.

에서 사용 하려는 각 파일 시스템에 Git을 설치 해야 합니다.

![배포판 Git 버전 표시](../media/git-versions.gif)

## <a name="installing-git"></a>Git 설치

Git는 Linux 배포판에 대 한 대부분의 Windows 하위 시스템에 이미 설치 되어 있지만 최신 버전으로 업데이트 하는 것이 좋습니다. 그러면 git 구성 파일을 설정 해야 합니다.

Git를 설치 하려면 [Linux 용 Git 다운로드](https://git-scm.com/download/linux) 사이트를 참조 하세요. 각 Linux 배포에는 자체 패키지 관리자와 install 명령이 있습니다. 예를 들어 알파인 배포에 Git을 설치 하려면를 사용 `apk add git` 합니다. 아직 없는 경우 [Windows 용 Git를 설치할](https://git-scm.com/download/win) 수도 있습니다.

## <a name="git-config-file-setup"></a>Git 구성 파일 설정

Git 구성 파일을 설정 하려면 작업 중인 배포에 대 한 명령줄을 열고를 입력 한 `git config --global user.name "Your Name"` 다음을 입력 `git config --global user.email "youremail@domain.com"` 합니다. 인용구의 콘텐츠를 Git 계정을 만드는 데 사용한 이름 및 전자 메일 주소로 바꿉니다.

> [!TIP]
> 아직 Git 계정이 없으면 [GitHub에서 가입](https://github.com/join)할 수 있습니다. 이전에 Git를 사용한 경험이 없는 경우 [GitHub 가이드](https://guides.github.com/)를 보면 시작하는 데 도움이 될 수 있습니다. git config를 편집해야 하는 경우 nano: `nano ~/.gitconfig`와 같은 기본 제공 텍스트 편집기를 사용하여 편집할 수 있습니다.

[2 단계 인증 (2FA)을 사용 하 여 계정을 보호](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)하는 것이 좋습니다.

## <a name="git-credential-manager-setup"></a>Git 자격 증명 관리자 설치

Git 자격 증명 관리자를 사용 하면 2 단계 인증, Azure Active Directory 등의 복잡 한 인증 패턴이 있거나 모든 git 푸시에 대해 SSH 키 암호가 필요한 SSH 원격 Url을 사용 하는 경우에도 원격 Git 서버를 인증할 수 있습니다. Git 자격 증명 관리자는 GitHub와 같은 서비스의 인증 흐름에 통합되며, 사용자가 호스팅 공급자에 인증되면 새 인증 토큰을 요청합니다. 그런 다음 [Windows 자격 증명 관리자](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager)에 안전 하 게 토큰을 저장 합니다. 처음 인증하고 나면 다시 인증할 필요 없이 Git을 사용하여 호스팅 공급자와 통신할 수 있습니다. Git이 Windows 자격 증명 관리자의 토큰에 액세스할 것입니다.

WSL 배포판과 함께 사용할 Git 자격 증명 관리자를 설정하려면 배포판을 열고 다음 명령을 입력합니다.

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

이제 사용자가 WSL 배포판 내에서 수행하는 모든 Git 작업에서 자격 증명 관리자를 사용합니다. 호스트용으로 캐시된 자격 증명이 이미 있는 경우 자격 증명 관리자에서 액세스됩니다. 그렇지 않다면 자격 증명을 요청하는 대화 상자 응답이 수신됩니다(Linux 콘솔에 있을 경우도).

## <a name="adding-a-git-ignore-file"></a>Git Ignore 파일 추가

프로젝트에 [.gitignore 파일](https://help.github.com/en/articles/ignoring-files) 을 추가 하는 것이 좋습니다. GitHub는 사용 사례에 따라 구성 된 .gitignore 파일 설정이 [.gitignore 템플릿 컬렉션을](https://github.com/github/gitignore) 제공 합니다.

[GitHub 웹 사이트를 사용 하 여 새 리포지토리를 만들도록](https://help.github.com/articles/create-a-repo)선택 하는 경우 특정 프로젝트 형식에 대 한 추가 정보 파일,. .gitignore 파일 및 필요한 경우 라이선스를 추가 하는 옵션을 사용 하 여 리포지토리를 초기화 하는 데 사용할 수 있는 확인란이 있습니다.

## <a name="git-and-vs-code"></a>Git 및 VS Code

Visual Studio Code에는 변경 내용을 표시 하 고 다양 한 git 명령을 처리 하는 소스 제어 탭을 비롯 하 여 Git에 대 한 기본 제공 지원이 제공 됩니다. [VS Code의 Git 지원](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)에 대해 자세히 알아보세요.

## <a name="git-line-endings"></a>Git 줄 끝

Windows, WSL 또는 컨테이너와 동일한 리포지토리 폴더를 사용 하 여 작업 하는 경우 일관성 있는 줄 끝을 설정 해야 합니다.

Windows 및 Linux는 서로 다른 기본 줄 끝을 사용 하기 때문에 Git은 줄 끝에서 차이가 없는 다 수의 수정 된 파일을 보고할 수 있습니다. 이 문제가 발생 하지 않도록 하려면 파일을 사용 하 여 줄 끝 변환을 사용 하지 않도록 설정 `.gitattributes` 하거나 Windows 쪽에서 전역적으로 변환을 사용 하지 않도록 설정할 수 있습니다. [Git 줄 종료 문제를 해결 하는 방법에 대 한이 VS Code 문서](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files)를 참조 하세요.

## <a name="additional-resources"></a>추가 리소스

* [WSL & VS Code](./wsl-vscode.md)
* [GitHub 학습 랩: 온라인 과정](https://lab.github.com/)
* [Git 시각화 도구](http://git-school.github.io/visualizing-git/)
* [Git 도구-자격 증명 저장소](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
