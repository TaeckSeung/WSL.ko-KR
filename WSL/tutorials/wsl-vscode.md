---
title: Linux 용 Windows 하위 시스템을 사용 하 여 VS Code 시작
description: Linux 용 Windows 하위 시스템을 사용 하 여 코드를 작성 하 고 디버그 하 VS Code를 설정 하는 방법에 대해 알아봅니다.
keywords: wsl, windows, windowssubsystem, gnu, linux, bash, vs code, 원격 확장, 디버그, 경로, visual studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 528c2b040136518f9c7d04d8572cd0f08bb68385
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443757"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템을 사용 하 여 Visual Studio Code 시작

원격 WSL 확장과 함께 Visual Studio Code를 사용 하면 VS Code에서 직접 WSL을 전체 시간 개발 환경으로 사용할 수 있습니다. 다음 작업을 수행할 수 있습니다.

* Linux 기반 환경에서 개발
* Linux 특정 도구 체인 및 유틸리티 사용
* Outlook 및 Office와 같은 생산성 도구에 대 한 액세스를 유지 하면서 Windows에서 편안하게 Linux 기반 응용 프로그램을 실행하고 디버그 합니다.
* VS Code 기본 제공 터미널을 사용 하 여 선택한 Linux 배포를 실행 합니다.
* [Intellisense 코드 완성](https://code.visualstudio.com/docs/editor/intellisense), [lint](https://code.visualstudio.com/docs/python/linting), [디버그 지원](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), [코드 조각](https://code.visualstudio.com/docs/editor/userdefinedsnippets)및 [유닛 테스트](https://code.visualstudio.com/docs/python/testing) 와 같은 VS Code 기능 활용
* VS Code의 기본 제공 [Git 지원](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support) 으로 손쉽게 버전 제어 관리
* WSL 프로젝트에서 직접 명령 및 VS Code 확장 실행
* pathing 문제, 이진 호환성 또는 기타 OS 간 문제를 걱정 하지 않고 Linux 또는 탑재 된 Windows 파일 시스템 (예:/mnt/c)에서 파일을 편집 합니다.

## <a name="install-vs-code-and-the-remote-wsl-extension"></a>VS Code 및 원격 WSL 확장 설치

* [VS Code 설치 페이지](https://code.visualstudio.com/download) 를 방문하여 32 또는 64 비트 설치 관리자를 선택 합니다. Windows에 Visual Studio Code를 설치 합니다 (WSL 파일 시스템이 아님).

* 설치 하는 동안 **추가 작업을 선택** 하 라는 메시지가 표시 되는 경우 코드 명령을 사용하여 wsl에서 폴더를 쉽게 열 수 있도록 **경로에 추가** 옵션을 선택 해야 합니다.

* [원격 개발 확장 팩](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)을 설치 합니다. 이 확장 팩은 원격-SSH 및 원격 컨테이너 확장 외에도 원격-WSL 확장을 포함하여 컨테이너, 원격 컴퓨터 또는 WSL의 모든 폴더를 열 수 있도록 합니다.

> [!IMPORTANT]
> 원격 WSL 확장을 설치 하려면 VS Code의 [1.35](https://code.visualstudio.com/updates/v1_35) 버전 이상이 필요 합니다. 자동 완성, 디버깅, lint 등에 대한 지원이 손실 될 것 이므로, 원격-WSL 확장이 없으면 VS Code에서 WSL을 사용 하지 않는 것이 좋습니다. 흥미로운 사실:이 WSL 확장은 $HOME/확장명 (PowerShell에서 명령을 입력)에 설치 됩니다 `ls $HOME\.vscode\extensions\` .

## <a name="update-your-linux-distribution"></a>Linux 배포 업데이트

일부 WSL Linux 배포판에는 VS Code 서버에서 시작 하는 데 필요한 라이브러리가 부족 합니다. 패키지 관리자를 사용하여 Linux 배포에 라이브러리를 더 추가할 수 있습니다.

예를 들어 Debian 또는 Ubuntu를 업데이트 하려면 다음을 사용 합니다.

```bash
sudo apt-get update
```

Wget (웹 서버에서 콘텐츠 검색) 및 ca 인증서 (SSL 기반 응용 프로그램에서 SSL 연결의 신뢰성을 확인할 수 있도록 하려면)를 추가 하려면 다음을 입력 합니다.

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a>Visual Studio Code에서 WSL 프로젝트를 엽니다.

### <a name="from-the-command-line"></a>명령줄에서

WSL 배포에서 프로젝트를 열려면 분포의 명령줄을 열고 다음을 입력 합니다. `code .`

![VS Code 원격 서버를 사용 하 여 WSL 프로젝트 열기](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a>VS Code에서

바로 가기를 사용하여 추가 VS Code 원격 옵션에 액세스할 수도 있습니다. `CTRL+SHIFT+P` VS Code에서 명령 팔레트를 표시 합니다. 그런 다음을 입력 하면 `VSCODE-REMOTE` 사용 가능한 VS Code 모든 원격 옵션을 볼 수 있습니다. 이 옵션을 사용 하면 원격 세션에서 폴더를 다시 열고 어떤 배포에서 열것인지 등의 작업을 지정할 수 있습니다.

![VS Code의 명령 팔레트](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a>VS Code 원격 내의 확장

원격 WSL 확장은 Windows 컴퓨터에서 실행되는 클라이언트 (사용자 인터페이스)와 원격으로 실행되는 서버 (코드, Git, 플러그 인 등)를 사용하여 "클라이언트 서버" 아키텍처로 VS Code 분할 합니다.

원격 VS Code를 실행 하는 경우 '확장' 탭을 선택하면 로컬 컴퓨터와 WSL 배포 간에 분할 된 확장의 목록이 표시 됩니다.

[테마](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs)와 같이 로컬 확장을 설치 하는 경우에는 한 번만 설치하면 됩니다.

[Python 확장](https://marketplace.visualstudio.com/items?itemName=ms-python.python) 또는 lint 또는 디버깅과 같은 항목을 처리 하는 것과 같은 일부 확장은 각 원격 wsl 배포에 별도로 설치 되어야 합니다. ⚠Wsl 원격에 설치 되지 않은 확장을 로컬로 설치하는 경우 VS Code에는 녹색 "wsl에 설치" 단추가 표시 됩니다.

![원격-WSL 확장 및 로컬 확장을 사용하여 VS Code](../media/vscode-remote-wsl-extensions.png)

자세한 내용은 VS Code 문서를 참조 하세요.

* WSL에서 원격 VS Code 시작 하면 셸 시작 스크립트가 실행되지 않습니다. 추가 명령을 실행 하거나 환경을 수정 하는 방법에 대한 자세한 내용은이 [고급 환경 설정 스크립트 문서](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) 를 참조 하세요.

* WSL 명령줄에서 VS Code를 시작 하는데 문제가 있나요? 이 [문제 해결 가이드](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) 에는 경로 변수를 변경 하 고, 누락된 종속성에 대한 확장 오류를 해결하고, Git 줄 문제를 해결하고, 원격 컴퓨터에 로컬 VSIX를 설치 하고, 브라우저 창을 시작하고, 웹 소켓이 작동 하지 않거나, 확장 데이터를 저장 하는 오류 등의 팁이 포함 됩니다

## <a name="install-git-optional"></a>Git 설치(선택 사항)

다른 사람과 협업할 계획이거나 GitHub 같은 오픈 소스 사이트에 프로젝트를 호스팅할 계획인 분들을 위해 VS Code는 [Git을 사용한 버전 제어](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)를 지원합니다. VS Code의 소스 제어 탭은 모든 변경 내용을 추적하며, UI에 바로 빌드된 일반적인 Git 명령(추가, 커밋, 푸시, 끌어오기)를 포함하고 있습니다.

Git를 설치 하려면 [Linux 용 Windows 하위 시스템을 사용 하도록 git 설정](./wsl-git.md)을 참조 하세요.

## <a name="install-windows-terminal-optional"></a>Windows 터미널 설치(선택 사항)

새 Windows 터미널을 사용 하면 여러 탭 (명령 프롬프트, PowerShell 또는 여러 Linux 배포 간을 신속 하 게 전환), 사용자 지정 키 바인딩 (열기 또는 닫기 탭에 대한 사용자 고유의 바로 가기 키 만들기, 복사 + 붙여넣기 등),이모지 ☺ 및 사용자 지정 테마 (색 구성표, 글꼴 스타일 및 크기, 배경 이미지/흐림/투명도)를 사용할 수 있습니다. 자세한 내용은 [Windows 터미널 문서](/windows/terminal)를 확인 하세요.

1. 다음과 같이 [Microsoft Store에서 Windows 터미널](https://www.microsoft.com/store/apps/9n0dx20hk701)을 받습니다. Microsoft Store를 통해 설치하면 업데이트가 자동으로 처리됩니다.

2. 설치가 완료되면 Windows 터미널을 열고 **설정** 을 선택한 다음, `profile.json` 파일을 사용하여 터미널을 사용자 지정합니다.

## <a name="additional-resources"></a>추가 리소스

* [원격 개발 VS Code](https://code.visualstudio.com/docs/remote/remote-overview)
* [원격 개발 팁 및 요령](https://code.visualstudio.com/docs/remote/troubleshooting)
* [WSL 자습서를 사용한 원격 개발 자습서](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [WSL 2 및 VS Code에서 Docker 사용](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [VS Code에서 c + + 및 WSL 사용](https://code.visualstudio.com/docs/cpp/config-wsl)
* [Linux용 원격 R 서비스](/visualstudio/rtvs/setting-up-remote-r-service-on-linux)

다음과 같은 몇 가지 추가 확장도 고려해 볼 수 있습니다.

* [다른 편집기의 키맵](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads): Atom, Sublime, Vim, eMacs, 메모장++ 등의 다른 텍스트 편집기에서 전환할 때 이러한 확장을 사용하여 익숙한 환경을 만들 수 있습니다.
* [설정 동기화](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync): GitHub를 사용하는 여러 설치에서 VS Code 설정을 동기화할 수 있습니다. 여러 머신에서 작업하는 경우 이렇게 하면 여러 머신의 환경을 일관되게 유지할 수 있습니다.
* [Chrome 용 디버거](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): Linux를 사용하여 서버 쪽에서 개발을 마친 후에는 클라이언트 쪽을 개발하고 테스트 해야 합니다. 이 확장은 VS Code 편집기를 Chrome 브라우저 디버깅 서비스와 통합하여 효율성을 높입니다.
