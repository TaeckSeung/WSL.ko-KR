---
title: Linux 용 Windows 하위 시스템 문제 해결
description: Linux 용 Windows 하위 시스템에서 Linux를 실행 하는 동안 사용자가 실행 하는 일반적인 오류 및 문제에 대 한 자세한 정보를 제공 합니다.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6a5fec8b8e054b4d3399ee9bcd903acebca7aace
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122689"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템 문제 해결

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash는 VPN에 연결 된 후 네트워크 연결을 손실 합니다.

Windows에서 VPN에 연결한 후 bash에서 네트워크 연결이 끊어지면 bash 내에서이 해결 방법을 시도해 보세요. 이 해결 방법에서는를 통해 `/etc/resolv.conf`DNS 확인을 수동으로 재정의할 수 있습니다.

1. 이 작업을 수행 하는 데 VPN의 DNS 서버를 적어 둡니다.`ipconfig.exe /all`
2. 기존 resolv.conf의 복사본 만들기`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 현재 resolv.conf의 연결을 해제 합니다.`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 및 `/etc/resolv.conf` 열기 <br/>
   a. 파일에서 첫 번째 줄을 삭제 합니다. 즉,\# "이 파일은 wsl에 의해 자동으로 생성 되었습니다. 이 파일의 자동 생성을 중지 하려면이 줄을 제거 하십시오. " <br/>
   b. (1)의 DNS 항목을 DNS 서버 목록의 첫 번째 항목으로 추가 합니다. <br/>
   c. 파일을 닫습니다. <br/>

VPN의 연결을 끊은 후에는 변경 내용을로 `/etc/resolv.conf`되돌려야 합니다. 이렇게 하려면 다음을 수행 합니다.
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>WSL을 시작 하거나 배포를 설치 하면 오류 코드가 반환 됩니다.

자세한 로그를 수집 하 고 GitHub에서 문제를 파일 하려면 [다음 지침](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) 을 따르세요.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Windows에서 Ubuntu의 Bash 업데이트

업데이트 해야 할 수 있는 Windows의 Ubuntu에는 Bash의 두 구성 요소가 있습니다. 

1. Linux 용 Windows 하위 시스템
  
   Windows의 Ubuntu에 있는 Bash의이 부분을 업그레이드 하면 [릴리스 정보](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)에서 새로운 수정 개요가 활성화 됩니다. Windows 참가자 프로그램을 구독 하 고 빌드가 최신 상태 인지 확인 합니다. Ubuntu 인스턴스를 다시 설정 하는 등의 미세 제어를 위해 [명령 참조 페이지](https://msdn.microsoft.com/en-us/commandline/wsl/reference)를 확인 합니다.

2. Ubuntu 사용자 이진 파일 

   Windows의 Ubuntu에 있는 Bash의이 부분을 업그레이드 하면 apt-get을 통해 설치한 응용 프로그램을 포함 하 여 Ubuntu 사용자 이진 파일에 대 한 업데이트를 설치 합니다. 업데이트 하려면 Bash에서 다음 명령을 실행 합니다.
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-업그레이드 오류 가져오기
일부 패키지는 아직 구현 하지 않은 기능을 사용 합니다. `udev`예를 들어,는 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류가 발생 합니다.

와 관련 된 `udev`문제를 해결 하려면 다음 단계를 수행 합니다.

1. 에 다음을 `/usr/sbin/policy-rc.d` 작성 하 고 변경 내용을 저장 합니다.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 실행 권한 추가`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 다음 명령을 실행 합니다.
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306 "설치 시
레거시 콘솔을 지원 하지 않기 때문에이 작업을 수행 해야 합니다.
레거시 콘솔을 해제 하려면:

1. Cmd.exe를 엽니다.
1. 제목 표시줄-> 속성을 마우스 오른쪽 단추로 클릭 > 기존 콘솔 사용 선택 취소
1. 확인을 클릭합니다.

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154 "Windows 업데이트 후
Windows 업데이트를 실행 하는 동안 Linux 용 Windows 하위 시스템 기능을 사용 하지 못할 수 있습니다. 이 문제가 발생 하면 Windows 기능을 다시 사용 하도록 설정 해야 합니다. Linux 용 Windows 하위 시스템을 사용 하도록 설정 하는 방법에 대 한 지침은 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)에서 찾을 수 있습니다.

### <a name="changing-the-display-language"></a>표시 언어 변경
WSL install은 Windows 설치의 로캘과 일치 하도록 Ubuntu 로캘을 자동으로 변경 하려고 합니다.  이 동작을 원하지 않는 경우 설치가 완료 된 후이 명령을 실행 하 여 Ubuntu 로캘을 변경할 수 있습니다.  이 변경 내용이 적용 되려면 bash를 다시 실행 해야 합니다.

아래 예제에서는 로캘을 en-us로 변경 합니다.
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 시스템 복원 후의 설치 문제
1.  폴더를 `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` 삭제 합니다. <br/>
  **참고: 선택적 기능이 완전히 설치 되 고 작동 하는 경우에는이 작업을 수행 하지 마십시오.**
2.  WSL 선택적 기능 사용 (아직 없는 경우)
3.  다시 부팅
4.  lxrun/uninstall/full
5.  Bash 설치

### <a name="no-internet-access-in-wsl"></a>WSL에서 인터넷에 액세스할 필요가 없습니다.
일부 사용자가 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램의 문제를 보고 했습니다.  보고 된 방화벽은 다음과 같습니다.

1. Kaspersky
1. 매출
1. Avast

방화벽을 해제 하면 액세스가 허용 되는 경우도 있습니다.  경우에 따라 방화벽을 설치 하면 액세스를 차단 하는 것으로 보입니다.

### <a name="permission-denied-error-when-using-ping"></a>Ping을 사용 하는 경우 사용 권한 거부 오류
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[기념일 업데이트](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

WSL에서 ping을 실행 하려면 Windows의 관리자 권한이 필요 합니다.  Ping을 실행 하려면 관리자 권한으로 Windows의 Ubuntu에서 Bash를 실행 하거나 관리자 권한으로 CMD/PowerShell 프롬프트에서 bash를 실행 합니다.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[14926 + 빌드](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  더 이상 관리자 권한이 필요 하지 않습니다.

### <a name="bash-is-hung"></a>Bash가 중지 되었습니다.
Bash로 작업 하는 동안 bash가 중지 (또는 교착 상태) 상태 이며 입력에 응답 하지 않는 것을 발견 하면 메모리 덤프를 수집 하 고 보고 하 여 문제를 진단 하는 데 도움이 됩니다. 이러한 단계를 수행 하면 시스템이 중단 됩니다. 이 작업을 수행 하기 전에이 작업을 수행 하기 전에 작업을 저장 하는 것이 좋습니다.  <br/>
메모리 덤프를 수집 하려면:
1. 메모리 덤프 유형을 "전체 메모리 덤프"로 변경 합니다. 덤프 유형을 변경 하는 동안 현재 유형을 기록해 둡니다.
2. 키보드 컨트롤을 사용 하 여 충돌을 구성 하는 [단계](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) 를 사용 합니다.
3. 중지 또는 교착 상태를 재현 합니다.
4. (2)의 키 시퀀스를 사용 하 여 시스템의 작동이 중단 됩니다.
5. 시스템 작동이 중단 되 고 메모리 덤프가 수집 됩니다.
6. 시스템이 다시 부팅 되 면 memory.dmp를에 secure@microsoft.com보고 합니다. 덤프 파일의 기본 위치는%SystemRoot%\memory.dmp 또는 C:가 시스템 드라이브인 경우에 한 합니다. 전자 메일에서 덤프는 Windows 팀의 WSL 또는 Bash에 대 한 것입니다.
7. 메모리 덤프 유형을 원래 설정으로 복원 합니다.

### <a name="check-your-build-number"></a>빌드 번호 확인

PC의 아키텍처 및 Windows 빌드 번호를 찾으려면를 엽니다.  
**설정** > **시스템** 정보 > 

**OS 빌드** 및 **시스템 유형** 필드를 찾습니다.  
    ![빌드 및 시스템 유형 필드의 스크린샷](media/system.png) 


Windows Server 빌드 번호를 찾으려면 PowerShell에서 다음을 실행 합니다.  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>WSL이 사용 하도록 설정 되었는지 확인
PowerShell에서 다음을 실행 하 여 Linux 용 Windows 하위 시스템을 사용할 수 있는지 확인할 수 있습니다.  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH-서버 연결 문제
다음 오류로 인해 SSH 서버를 연결 하지 못했습니다. "연결을 127.0.0.1 포트 22"로 닫았습니다.
1. OpenSSH 서버가 실행 중인지 확인 합니다.
   ``` BASH
   sudo service ssh status
   ```
   그리고 다음 자습서를 수행 했습니다. https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Sshd 서비스를 중지 하 고 디버그 모드에서 sshd를 시작 합니다.
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 시작 로그를 확인 하 고 호스트 키를 사용할 수 있는지 확인 하 고 다음과 같은 로그 메시지가 표시 되지 않는지 확인 합니다.
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

이러한 메시지가 표시 되 고 아래 `/etc/ssh/`에 키가 없는 경우 키를 다시 생성 하거나 openssh를 제거 & 설치 해야 합니다.
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

