---
title: Linux 용 Windows 하위 시스템에서 Docker 컨테이너 사용 시작
description: Linux 용 Windows 하위 시스템에서 Docker 컨테이너를 설정 하는 방법에 대해 알아봅니다.
keywords: wsl, windows, windowssubsystem, windows 10, docker, 컨테이너
ms.date: 08/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: cca53f2079e026fbe765ad13cc67722457f83c23
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211787"
---
# <a name="get-started-with-docker-remote-containers-on-wsl-2"></a>WSL 2에서 Docker 원격 컨테이너 시작

이 단계별 가이드는 WSL 2 (Linux 용 windows 하위 시스템, 버전 2) **를 사용 하 여 windows 용 Docker Desktop을 설정** 하 여 원격 컨테이너를 사용 하 여 개발을 시작 하는 데 도움이 됩니다.

Windows 용 Docker Desktop은 무료로 제공 되며 dockerized 앱을 빌드, 배송 및 실행 하기 위한 개발 환경을 제공 합니다. WSL 2 기반 엔진을 사용 하도록 설정 하 여 동일한 컴퓨터에서 Docker Desktop의 Linux 및 Windows 컨테이너를 모두 실행할 수 있습니다.

## <a name="overview-of-docker-containers"></a>Docker 컨테이너 개요

Docker는 컨테이너를 사용하여 애플리케이션을 만들고, 배포하고, 실행하는 데 사용되는 도구입니다. 개발자는 컨테이너를 사용하여 필요한 모든 파트(라이브러리, 프레임워크, 종속성 등)와 함께 앱을 패키징하여 하나의 패키지로 제공할 수 있습니다. 컨테이너를 사용하면 앱을 실행하는 컴퓨터(코드를 작성하고 테스트하는 데 사용된 머신과 다를 수도 있음)의 사용자 지정된 설정 또는 이전에 설치한 라이브러리와 상관없이 앱이 동일하게 실행됩니다. 따라서 개발자는 코드가 실행될 시스템에 대해 신경 쓰지 않고 코드 작성에 집중할 수 있습니다.

Docker 컨테이너는 가상 머신과 비슷하지만 전체 가상 운영 체제를 만들지는 않습니다. 대신 Docker를 사용하면 앱이 실행 중인 시스템과 동일한 Linux 커널을 사용할 수 있습니다. 따라서 호스트 컴퓨터에 아직 없는 파트만 앱 패키지에 필요하므로 패키지 크기를 줄이고 성능을 높일 수 있습니다.

컨테이너가 인기 있는 또 다른 이유는 [Kubernetes](/azure/aks/) 같은 도구와 함께 Docker 컨테이너를 사용하면 지속적인 가용성을 얻을 수 있다는 점입니다. 이렇게 하면 여러 버전의 앱 컨테이너를 서로 다른 시간에 만들 수 있습니다. 업데이트 또는 유지 관리를 위해 전체 시스템을 중단하는 대신, 각 컨테이너(및 해당 마이크로서비스)를 필요할 때 바꿀 수 있습니다. 모든 업데이트가 포함된 새 컨테이너를 준비하고, 프로덕션용 컨테이너를 설정하고, 준비가 되면 새 컨테이너를 가리킬 수 있습니다. 컨테이너를 사용하여 여러 버전의 앱을 보관하고, 필요한 경우 안전 대비책으로 앱을 계속 실행할 수도 있습니다.

자세히 알아보려면 Microsoft Learn에서 [Docker 컨테이너 소개](/learn/modules/intro-to-docker-containers/) 를 확인 하세요.

## <a name="prerequisites"></a>필수 구성 요소

- 컴퓨터에 Windows 10이 실행 되 고 있는지 확인 하 고 버전 2004, **빌드 18362** 이상 [으로 업데이트](ms-settings:windowsupdate)합니다.
- [WSL을 사용 하도록 설정 하 고, Linux 배포를 설치 하 고, wsl 2로 업데이트](../install-win10.md)합니다.
- [Linux 커널 업데이트 패키지를 다운로드 하 여 설치](../install-win10.md#step-4---download-the-linux-kernel-update-package)합니다.
- [Visual Studio Code를 설치](https://code.visualstudio.com/download) 합니다 *(선택 사항)*. 이렇게 하면 원격 Docker 컨테이너 내에서 코딩 및 디버깅 하 고 Linux 배포에 연결 하는 기능을 포함 하 여 최상의 환경을 제공 합니다.
- [Windows 터미널을 설치](/windows/terminal/get-started) 합니다 *(선택 사항)*. 이렇게 하면 동일한 인터페이스에서 여러 터미널을 사용자 지정 하 고 여는 기능 (Ubuntu, Debian, PowerShell, Azure CLI 또는 선호 하는 항목 포함)을 비롯 하 여 최상의 환경을 제공 합니다.
- Docker [허브에서 DOCKER ID에 등록](https://hub.docker.com/signup) 합니다 *(선택 사항)*.

> [!NOTE]
> WSL은 WSL 버전 1 또는 WSL 2 모드에서 배포를 실행할 수 있습니다. PowerShell을 열고 다음을 입력 하 여이를 확인할 수 있습니다 `wsl -l -v` . 다음을 입력 하 여 분포가 WSL 2를 사용 하도록 설정 되어 있는지 확인 `wsl --set-version  <distro> 2` 합니다. `<distro>`배포판 이름으로 대체 합니다 (예: Ubuntu 18.04).
> 
> WSL 버전 1에서 Windows와 Linux의 기본적인 차이로 인해 Docker 엔진은 WSL 내에서 직접 실행할 수 없으므로 Docker 팀은 Hyper-v Vm 및 LinuxKit를 사용 하 여 대체 솔루션을 개발 했습니다. 그러나 이제 WSL 2는 전체 시스템 호출 용량의 Linux 커널에서 실행 되므로 Docker는 WSL 2에서 완전 하 게 실행할 수 있습니다. 즉, Linux 컨테이너가 에뮬레이션 없이 기본적으로 실행 될 수 있으므로 Windows 및 Linux 도구 간의 성능 및 상호 운용성이 향상 됩니다.

## <a name="install-docker-desktop"></a>Docker Desktop 설치

Windows 용 Docker Desktop에서 WSL 2 백 엔드를 지 원하는 경우 Linux 기반 개발 환경에서 작업 하 고, 코드 편집 및 디버깅을 위해 Visual Studio Code를 사용 하 고, Windows의 Microsoft Edge 브라우저에서 컨테이너를 실행 하는 동안 linux 기반 개발 환경에서 작업을 수행할 수 있습니다.

Docker를 설치 하려면 ( [WSL 2](../install-win10.md)를 이미 설치한 후):

1. [Docker Desktop](https://docs.docker.com/docker-for-windows/wsl/#download) 을 다운로드 하 고 설치 지침을 따릅니다.

2. 설치가 완료 되 면 Windows 시작 메뉴에서 Docker Desktop을 시작 하 고 작업 표시줄의 숨겨진 아이콘 메뉴에서 Docker 아이콘을 선택 합니다. 아이콘을 마우스 오른쪽 단추로 클릭 하 여 Docker 명령 메뉴를 표시 하 고 "설정"을 선택 합니다.
    ![Docker 데스크톱 대시보드 아이콘](../media/docker-starting.png)

3. **설정**일반에서 "wsl 2 기반 엔진 사용"이 선택 되어 있는지 확인  >  **General**합니다.
    ![Docker 데스크톱 일반 설정](../media/docker-running.png)

4. **설정**  >  **리소스**  >  **wsl 통합**으로 이동 하 여 Docker 통합을 사용 하도록 설정 하려는 설치 된 wsl 2 배포판에서 선택 합니다.
    ![Docker 데스크톱 리소스 설정](../media/docker-dashboard.png)

5. Docker가 설치 되었는지 확인 하려면 WSL 배포 (예: Ubuntu)를 열고 다음을 입력 하 여 버전 및 빌드 번호를 표시 합니다. `docker --version`

6. 다음을 사용 하 여 간단한 기본 제공 Docker 이미지를 실행 하 여 설치가 제대로 작동 하는지 테스트 합니다. `docker run hello-world`

> [!TIP]
> 다음은 몇 가지 유용한 Docker 명령입니다.
>
> - Docker CLI에서 사용할 수 있는 명령 나열: `docker`
> - 특정 명령에 대한 정보 나열: `docker <COMMAND> --help`
> - 머신의 docker 이미지 나열(현재는 hello-world 이미지만 나열됨): `docker image ls --all`
> - 다음을 사용 하 여 컴퓨터에 컨테이너 나열: `docker container ls --all` 또는 `docker ps -a` (-a show all 플래그를 사용 하지 않고 실행 중인 컨테이너만 표시 됨)
> - 다음을 사용 하 여 WSL 2 컨텍스트에서 사용할 수 있는 통계 및 리소스 (CPU & 메모리)를 비롯 하 여 Docker 설치와 관련 된 시스템 차원의 정보를 나열 합니다. `docker info`

## <a name="develop-in-remote-containers-using-vs-code"></a>VS Code를 사용 하 여 원격 컨테이너에서 개발

WSL 2에서 Docker를 사용 하 여 앱 개발을 시작 하려면 원격 WSL 확장 및 Docker 확장과 함께 VS Code를 사용 하는 것이 좋습니다.

- [VS Code 원격-WSL 확장을 설치](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)합니다. 이 확장을 사용 하면 VS Code의 WSL에서 실행 되는 Linux 프로젝트를 열 수 있습니다 (pathing 문제, 이진 호환성 또는 기타 OS 간 문제에 대해 걱정 하지 않아도 됩니다).

- [VS code Remote-Containers 확장을 설치](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)합니다. 이 확장을 사용 하면 컨테이너 내에서 프로젝트 폴더 또는 리포지토리를 열고 Visual Studio Code의 전체 기능 집합을 활용 하 여 컨테이너 내에서 개발 작업을 수행할 수 있습니다.

- [VS Code Docker 확장을 설치](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)합니다. 이 확장은 VS Code 내에서 컨테이너 화 된 응용 프로그램을 빌드, 관리 및 배포 하는 기능을 추가 합니다. (실제로는 컨테이너를 개발 환경으로 사용 하기 위해 Remote-Container 확장이 필요 합니다.)

Docker를 사용 하 여 기존 앱 프로젝트에 대 한 개발 컨테이너를 만들어 보겠습니다.

1. 이 예제에서는 Python 개발 환경에서 [Django에 대 한 내 Hello World 자습서](/windows/python/web-frameworks#hello-world-tutorial-for-django) 의 소스 코드를 사용 하 여 문서를 설정 합니다. 사용자 고유의 프로젝트 소스 코드를 사용 하려는 경우이 단계를 건너뛸 수 있습니다. GitHub에서 내 HelloWorld-Django 웹 앱을 다운로드 하려면 WSL 터미널 (예: Ubuntu)을 열고 다음을 입력 합니다. `git clone https://github.com/mattwojo/helloworld-django.git`

    > [!NOTE]
    > 에서 도구를 사용 하는 것과 동일한 파일 시스템에 항상 코드를 저장 합니다. 이로 인해 파일 액세스 성능이 더 빨라집니다. 이 예제에서는 Ubuntu (Linux 배포판)를 사용 하며, 프로젝트 파일을 WSL 파일 시스템에 저장 하려고 합니다 `\\wsl\` . Windows 파일 시스템에 프로젝트 파일을 저장 하면 WSL에서 Linux 도구를 사용 하 여 해당 파일에 액세스할 때 성능이 크게 저하 됩니다.

2. WSL terminal에서이 프로젝트에 대 한 소스 코드 폴더로 디렉터리를 변경 합니다.

    ```bash
    cd helloworld-django
    ```

3. 다음을 입력 하 여 로컬 원격 WSL 확장 서버에서 실행 중인 VS Code에서 프로젝트를 엽니다.

    ```bash
    code .
    ```

    VS Code 인스턴스의 왼쪽 아래 모서리에 있는 녹색 원격 표시기를 선택 하 여 WSL Linux 배포판에 연결 되어 있는지 확인 합니다.

    ![VS Code WSL 원격 표시기](../media/vscode-remote-indicator.png)

4. VS Code 명령 팔레트 (Ctrl + Shift + P)에서 다음을 입력 합니다. **원격-컨테이너: 컨테이너에서 폴더 열기** ... 입력 하기 시작할 때이 명령이 표시 되지 않으면 위에 링크 된 원격 컨테이너 확장을 설치 했는지 확인 합니다.

    ![VS Code 원격 컨테이너 명령](../media/docker-extension.png)

5. 컨테이너 화 프로젝트 폴더를 선택 합니다. 이 경우는 다음과 같습니다. `\\wsl\Ubuntu-20.04\home\mattwojo\repos\helloworld-django\`

    ![원격 컨테이너 폴더 VS Code](../media/docker-extension2.png)

6. 프로젝트 폴더 (리포지토리)에 DevContainer 구성이 아직 없기 때문에 컨테이너 정의 목록이 표시 됩니다. 표시 되는 컨테이너 구성 정의 목록은 프로젝트 형식에 따라 필터링 됩니다. 내 Django 프로젝트의 경우 Python 3을 선택 합니다.

    ![원격 컨테이너 구성 정의 VS Code](../media/docker-extension3.png)

7. 새 VS Code 인스턴스가 열리고 새 이미지 빌드를 시작 하 고 빌드가 완료 되 면 컨테이너가 시작 됩니다. `.devcontainer`및 파일 내에 컨테이너 구성 정보를 포함 하는 새 폴더가 표시 됩니다 `Dockerfile` `devcontainer.json` .  

    ![VS Code devcontainer 폴더](../media/docker-extension4.png)

8. 프로젝트가 아직 WSL과 컨테이너 내에 모두 연결 되어 있는지 확인 하려면 VS Code 통합 터미널 (Ctrl + Shift + ~)을 엽니다. : 및를 사용 하 여 Python 버전을 입력 하 여 운영 체제를 확인 `uname` `python3 --version` 합니다. Uname이 "Linux"로 다시 표시 되는 것을 확인할 수 있습니다 .이는 WSL 2 엔진에 계속 연결 되어 있으며, Python 버전 번호는 WSL 배포에 설치 된 Python 버전과 다를 수 있는 컨테이너 구성을 기반으로 합니다.

9. Visual Studio Code를 사용 하 여 컨테이너 내에서 응용 프로그램을 실행 하 고 디버깅 하려면 먼저 **실행** 메뉴를 열거나 (Ctrl + Shift + D), 맨 왼쪽 메뉴 모음에서 탭을 선택 합니다. 그런 다음 **실행 및 디버그** 를 선택 하 여 디버그 구성을 선택 하 고 프로젝트에 가장 적합 한 구성을 선택 합니다 (이 예에서는 "Django"이 됨). 그러면 `launch.json` `.vscode` 응용 프로그램을 실행 하는 방법에 대 한 지침이 포함 된 파일이 프로젝트의 폴더에 생성 됩니다.

    ![디버그 구성 실행 VS Code](../media/vscode-run-config.png)

10. VS Code 내에서 **Run**  >  **디버깅 시작** 실행을 선택 하거나 **f5** 키를 누르기만 하면 됩니다. 그러면 VS Code 내에서 터미널이 열리고 " http://127.0.0.1:8000/ 제어를 사용 하 여 서버 종료에서 개발 서버 시작"과 같은 결과가 표시 됩니다. Ctrl 키를 누른 상태에서 표시 되는 주소를 선택 하 여 기본 웹 브라우저에서 앱을 열고 해당 컨테이너 내부에서 실행 중인 프로젝트를 확인 합니다.

    ![Docker 컨테이너를 실행 하는 VS Code](../media/vscode-running-in-container.png)

이제 VS Code를 사용 하 여 코딩, 빌드, 실행, 배포 또는 디버그할 수 있는 Docker Desktop을 사용 하 여 원격 개발 컨테이너를 성공적으로 구성 했습니다.

## <a name="troubleshooting"></a>문제 해결

### <a name="wsl-docker-context-deprecated"></a>WSL docker 컨텍스트 사용 되지 않음

WSL 용 Docker의 초기 Tech Preview를 사용 하는 경우, 이제는 사용 되지 않으며 더 이상 사용 되지 않는 "wsl" 이라는 Docker 컨텍스트가 있을 수 있습니다. 명령을 사용 하 여 확인할 수 있습니다 `docker context ls` . `docker context rm wsl`Windows 및 WSL2에 대 한 기본 컨텍스트를 사용 하는 것과 같이 명령을 사용 하 여 오류를 방지 하기 위해이 "wsl" 컨텍스트를 제거할 수 있습니다.

사용 되지 않는 wsl 컨텍스트를 사용 하는 경우 발생할 수 있는 오류는 다음과 같습니다. `docker wsl open //./pipe/docker_wsl: The system cannot find the file specified.` 또는 `error during connect: Get http://%2F%2F.%2Fpipe%2Fdocker_wsl/v1.40/images/json?all=1: open //./pipe/docker_wsl: The system cannot find the file specified.`

이 문제에 대 한 자세한 내용은 [windows 10의 Windows System For Linux 내에서 Docker를 설정 하는 방법 (WSL2)](https://www.hanselman.com/blog/HowToSetUpDockerWithinWindowsSystemForLinuxWSL2OnWindows10.aspx)을 참조 하십시오.

### <a name="trouble-finding-docker-image-storage-folder"></a>Docker 이미지 저장소 폴더를 찾는 데 문제가 있습니다.

Docker는 데이터를 저장 하는 두 개의 배포판 폴더를 만듭니다.
- \\wsl $ \docker-desktop
- \\wsl $ \docker-m-m-m-m-m-m-

WSL Linux 배포를 열고 다음을 입력 하 여 이러한 폴더를 찾을 수 있습니다. `explorer.exe .` Windows 파일 탐색기에서 폴더를 확인 합니다. Enter: `\\wsl\<distro name>\mnt\wsl` `<distro name>` 를 배포 이름으로 바꿉니다 (ie. Ubuntu-20.04)를 참조 하세요.

WSL에서 docker 저장소 위치 찾기에 대 한 자세한 내용은 [wsl 리포지토리](https://github.com/microsoft/WSL/issues/4176) 또는이 [StackOverlow 게시물](https://stackoverflow.com/questions/62380124/where-docker-image-is-stored-with-docker-desktop-for-windows)에서이 문제를 참조 하세요.

WSL의 일반적인 문제 해결에 대 한 자세한 도움말은 [문제 해결](../troubleshooting.md) 문서를 참조 하세요.

## <a name="additional-resources"></a>추가 리소스

- [Docker docs: WSL 2를 사용 하는 Docker Desktop에 대 한 모범 사례](https://docs.docker.com/docker-for-windows/wsl/#best-practices)
- [Windows 용 Docker Desktop에 대 한 피드백: 문제 파일](https://github.com/docker/for-win/issues)
- [VS Code 블로그: 개발 환경 선택 지침](https://code.visualstudio.com/docs/containers/choosing-dev-environment#_guidelines-for-choosing-a-development-environment)
- [VS Code 블로그: WSL 2에서 Docker 사용](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
- [VS Code 블로그: WSL 2에서 원격 컨테이너 사용](https://code.visualstudio.com/blogs/2020/07/01/containers-wsl)
- [Hanselminutes 포드캐스트: 개발자를 위한 Simon Ferquel를 위한 Docker 만들기](https://hanselminutes.com/736/making-docker-lovely-for-developers-with-simon-ferquel)
