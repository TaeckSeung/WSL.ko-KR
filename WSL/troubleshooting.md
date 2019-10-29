---
title: Linux용 Windows 하위 시스템 문제 해결
description: Linux용 Windows 하위 시스템에서 Linux를 실행하는 동안 사용자에게 발생할 수 있는 일반적인 오류 및 문제에 대한 자세한 정보를 제공합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, Ubuntu
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 24a899df78e705630c6cb95f8719594aec340c5c
ms.sourcegitcommit: 600853005bd2b42d6e47bf36ebed4b868ff2af26
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2019
ms.locfileid: "72987521"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 문제 해결

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash가 VPN에 연결되면 네트워크 연결이 끊어짐

Windows에서 VPN에 연결한 후에 Bash에서 네트워크 연결이 끊어지면 Bash 내에서 다음 해결 방법을 시도해 보세요. 이 해결 방법을 사용하면 `/etc/resolv.conf`를 통해 DNS 확인을 수동으로 재정의할 수 있습니다.

1. `ipconfig.exe /all`을 수행하여 VPN의 DNS 서버를 적어 둡니다.
2. `sudo cp /etc/resolv.conf /etc/resolv.conf.new`를 수행하여 기존 resolv.conf의 복사본을 만듭니다.
3. `sudo unlink /etc/resolv.conf`를 수행하여 현재 resolv.conf의 연결을 해제합니다.
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. `/etc/resolv.conf`를 엽니다. <br/>
   a. "\# 이 파일은 WSL에서 자동으로 생성했습니다. 이 파일의 자동 생성을 중지하려면 이 줄을 제거하세요."라는 파일의 첫 번째 줄을 삭제합니다. <br/>
   b. 위 (1)의 DNS 항목을 DNS 서버 목록의 첫 번째 항목으로 추가합니다. <br/>
   c. 파일을 닫습니다. <br/>

VPN의 연결을 끊은 후에는 변경 내용을 `/etc/resolv.conf`로 되돌려야 합니다. 이렇게 하려면 다음을 수행합니다.
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>WSL을 시작하거나 배포를 설치하면 오류 코드가 반환됨

[이 지침](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)에 따라 자세한 로그를 수집하고 문제를 GitHub에 제출하세요.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Windows의 Ubuntu에 있는 Bash 업데이트

Windows의 Ubuntu에 있는 Bash에는 업데이트해야 할 수 있는 두 가지 구성 요소가 있습니다. 

1. Linux용 Windows 하위 시스템
  
   Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 [릴리스 정보](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)의 새로운 수정에 대한 개요가 활성화됩니다. Windows 참가자 프로그램을 구독하고 빌드가 최신 상태인지 확인하세요. Ubuntu 인스턴스 재설정을 포함하여 매우 자세히 제어하려면 [명령 참조 페이지](https://msdn.microsoft.com/en-us/commandline/wsl/reference)를 확인하세요.

2. Ubuntu 사용자 이진 파일 

   Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 apt-get을 통해 설치한 애플리케이션을 포함하여 Ubuntu 사용자 이진 파일에 대한 모든 업데이트가 설치됩니다. 업데이트하려면 Bash에서 다음 명령을 실행하세요.
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>apt-get upgrade 오류
일부 패키지는 아직 구현하지 않은 기능을 사용합니다. 예를 들어 `udev`는 아직 지원되지 않으므로 여러 `apt-get upgrade` 오류가 발생합니다.

`udev`와 관련된 문제를 해결하려면 다음 단계를 수행합니다.

1. 다음을 `/usr/sbin/policy-rc.d`에 작성하고 변경 내용을 저장합니다.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 실행 권한을 `/usr/sbin/policy-rc.d`에 추가합니다.
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 다음 명령을 실행합니다.
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306" - 설치 시
이 오류는 레거시 콘솔을 지원하지 않는다는 사실과 관련이 있습니다.
레거시 콘솔을 해제하려면 다음을 수행합니다.

1. cmd.exe를 엽니다.
1. 마우스 오른쪽 단추로 제목 표시줄-> 속성을 차례로 클릭하고, [레거시 콘솔 사용]의 선택을 취소합니다.
1. 확인을 클릭합니다.

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154" - Windows 업데이트 후
Windows 업데이트 중에 Linux용 Windows 하위 시스템 기능이 사용하지 않도록 설정될 수 있습니다. 이 문제가 발생하면 Windows 기능을 다시 사용하도록 설정해야 합니다. Linux용 Windows 하위 시스템을 사용하도록 설정하는 방법에 대한 지침은 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)에서 확인할 수 있습니다.

### <a name="changing-the-display-language"></a>표시 언어 변경
WSL 설치는 Windows 설치의 로캘과 일치하도록 Ubuntu 로캘을 자동으로 변경하려고 합니다.  이 동작을 원하지 않는 경우 설치가 완료된 후 다음 명령을 실행하여 Ubuntu 로캘을 변경할 수 있습니다.  이 변경 내용이 적용되려면 bash.exe를 다시 시작해야 합니다.

아래 예제에서는 로캘을 en-US로 변경합니다.
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 시스템 복원 후의 설치 문제
1.  `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` 폴더를 삭제합니다. <br/>
  **참고: 선택적 기능이 완전히 설치되어 작동하는 경우에는 이 작업을 수행하지 마세요.**
2.  선택적 WSL 기능을 사용하도록 설정합니다(아직 사용하지 않는 경우).
3.  다시 부팅
4.  lxrun /uninstall /full을 실행합니다
5.  Bash를 설치합니다.

### <a name="no-internet-access-in-wsl"></a>WSL에서 인터넷에 액세스할 수 없음
일부 사용자가 WSL에서 인터넷 액세스를 차단하는 특정 방화벽 애플리케이션의 문제를 보고했습니다.  보고된 방화벽은 다음과 같습니다.

1. Kaspersky
1. AVG
1. Avast

방화벽을 해제하면 액세스가 허용되는 경우도 있습니다.  단순히 방화벽을 설치하면 경우에 따라 액세스가 차단되는 것처럼 보입니다.

### <a name="permission-denied-error-when-using-ping"></a>ping 사용 시의 권한 거부 오류
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[1주년 업데이트](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

WSL에서 ping을 실행하려면 Windows의 관리자 권한이 필요합니다.  ping을 실행하려면 Windows의 Ubuntu에서 관리자 권한으로 Bash를 실행하거나 CMD/PowerShell 프롬프트에서 관리자 권한으로 bash.exe를 실행합니다.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[빌드 14926 이상](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  관리자 권한이 더 이상 필요하지 않습니다.

### <a name="bash-is-hung"></a>Bash가 중지됨
Bash로 작업하는 동안 Bash가 중지되거나 교착 상태가 되어 입력에 응답하지 않는 경우 메모리 덤프를 수집하고 보고하여 문제를 진단하는 데 도움이 됩니다. 다음 단계를 수행하면 시스템의 작동이 중단됩니다. 편안하지 않으면 이 작업을 수행하지 않거나 해당 작업을 저장한 후에 수행하세요.  <br/>
메모리 덤프를 수집하려면 다음을 수행합니다.
1. 메모리 덤프 유형을 "전체 메모리 덤프"로 변경합니다. 덤프 유형을 변경하는 동안 현재 유형을 적어 둡니다.
2. 이 [단계](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809)를 사용하여 키보드 컨트롤을 사용하는 시스템 작동 중단을 구성합니다.
3. 중지 또는 교착 상태를 재현합니다.
4. (2)의 키 시퀀스를 사용하여 시스템의 작동을 중단시킵니다.
5. 시스템의 작동이 중단되고 메모리 덤프가 수집됩니다.
6. 시스템이 다시 부팅되면 memory.dmp를 secure@microsoft.com에 보고합니다. 덤프 파일의 기본 위치는 %SystemRoot%\memory.dmp 또는 C:\Windows\memory.dmp(C:가 시스템 드라이브인 경우)입니다. 이메일에서 덤프는 Windows 팀의 WSL 또는 Bash에 대한 것입니다.
7. 메모리 덤프 유형을 원래 설정으로 복원합니다.

### <a name="check-your-build-number"></a>빌드 번호 확인

PC의 아키텍처 및 Windows 빌드 번호를 확인하려면  
**설정** > **시스템** > **정보**를 차례로 엽니다.

**OS 빌드** 및 **시스템 종류** 필드를 찾습니다.  
    ![빌드 및 시스템 종류 필드의 스크린샷](media/system.png) 


Windows Server 빌드 번호를 확인하려면 PowerShell에서 다음을 실행합니다.  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>WSL이 사용하도록 설정되었는지 확인
PowerShell에서 다음을 실행하여 Linux용 Windows 하위 시스템을 사용하도록 설정했는지 확인할 수 있습니다.  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH 서버 연결 문제
SSH 서버를 연결하려고 하면 "127.0.0.1 포트 22에 의해 연결이 닫혔습니다." 오류로 인해 실패합니다.
1. OpenSSH 서버가 실행되고 있는지 확인합니다.
   ``` BASH
   sudo service ssh status
   ```
   그리고 https://help.ubuntu.com/lts/serverguide/openssh-server.html.en 자습서를 수행했습니다.
2. sshd 서비스를 중지한 다음, 디버그 모드에서 sshd를 시작합니다.
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 시작 로그를 확인하고, HostKeys를 사용할 수 있고 다음과 같은 로그 메시지가 표시되지 않는지 확인합니다.
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

이러한 메시지가 표시되고 키가 `/etc/ssh/` 아래에 없으면 해당 키를 다시 생성하거나 OpenSSH 서버를 제거 후 설치해야 합니다.
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a>WSL 선택적 기능을 사용하도록 설정할 때 "참조된 어셈블리를 찾을 수 없습니다." 오류가 발생함

이 오류는 잘못된 설치 상태와 관련이 있습니다. 이 문제를 시도해 보고 해결하려면 다음 단계를 수행하세요.

* PowerShell에서 WSL 기능 사용 명령을 실행하는 경우 [시작] 메뉴를 열고, 'Windows 기능 사용/사용 안 함'을 검색하여 GUI를 대신 사용해 본 다음, 목록에서 선택적 구성 요소를 설치할 'Linux용 Windows 하위 시스템'을 선택합니다.
* [설정], [업데이트]로 차례로 이동하고, '업데이트 확인'을 클릭하여 Windows 버전을 업데이트합니다.
* 두 단계가 모두 실패하고 WSL에 액세스해야 하는 경우 설치 미디어를 사용하여 Windows 10을 다시 설치하고 '모두 유지'를 선택하여 앱과 파일이 유지되도록 하는 방식으로 업그레이드하는 것이 좋습니다. 이 작업을 수행하는 방법에 대한 지침은 [Windows 10 다시 설치](https://support.microsoft.com/en-us/help/4000735/windows-10-reinstall) 페이지에서 확인할 수 있습니다.