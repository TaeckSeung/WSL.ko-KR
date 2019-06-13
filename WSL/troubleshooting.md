---
title: Linux 용 Windows Susbystem 문제 해결
description: 실행 하는 사용자 문제 및 일반적인 오류에 대 한 자세한 정보를 제공 Linux 용 Windows Susbystem에서 Linux를 실행 하는 동안.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: feb9e25da73eeb0d7f0cef4014221a42e2ca179b
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040848"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템 문제 해결

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash의 VPN에 연결 되 면 네트워크 연결이 끊어지는

Windows에서 VPN에 연결한 후 bash 네트워크 연결이 끊어지는 경우 bash 내에서이 해결 방법을 시도 합니다. 이 해결 방법은 직접을 통해 DNS 확인을 재정의할 수 있습니다 `/etc/resolv.conf`합니다.

1. 작업과에서 vpn DNS 서버의 기록 `ipconfig.exe /all`
2. 기존 resolv.conf의 복사본 `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 현재 resolv.con 연결 해제 `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 열기 `/etc/resolv.conf` 및 <br/>
   a. 파일에서 첫 번째 줄을 삭제 "\# WSL에서이 파일 자동으로 생성 되었습니다. 이 파일의 자동 생성을 중지 하려면이 줄을 제거 합니다. "입니다. <br/>
   b. DNS 서버 목록에서 첫 번째 항목으로 위에서 (1)에서 DNS 항목을 추가 합니다. <br/>
   c. 파일을 닫습니다. <br/>

VPN 연결을 끊 었는 후 변경 내용이 되돌리려면 `/etc/resolv.conf`합니다. 이렇게 하려면 다음을 수행 합니다.
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>WSL를 시작 하거나 배포를 설치 하는 오류 코드를 반환 합니다.

따릅니다 [이러한 지침](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) 자세한 로그를 수집 하 여 GitHub에서 문제를 제출 합니다.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Windows에서 ubuntu의 Bash를 업데이트 하는 중

업데이트 필요할 수 있는 Windows에서 ubuntu의 Bash의 두 구성 요소가 있습니다. 

1. Linux 용 Windows 하위 시스템
  
   에 모든 새 수정 설명 하면 Windows에서 ubuntu의 Bash의이 부분을 업그레이드 합니다 [릴리스](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)합니다. Windows 참가자 프로그램에 구독 하 고 최신 빌드 인지 확인 합니다. 재설정에 Ubuntu를 포함 하 여 세밀 하 게 세분화 제어 체크 아웃 인스턴스를 [명령 참조 페이지](https://msdn.microsoft.com/en-us/commandline/wsl/reference)합니다.

2. Ubuntu 사용자 이진 파일 

   Windows에서 ubuntu의 Bash의이 부분을 업그레이드 apt get을 통해 설치 된 응용 프로그램을 포함 하 여 Ubuntu 사용자 바이너리에 포함 된 업데이트 설치 됩니다. Bash에서 다음 명령을 실행을 업데이트 하려면:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt get 업그레이드 오류
일부 패키지는 아직 구현 되지 않은 기능을 사용 합니다. `udev`예를 들어, 아직 지원 되지 않으며 여러 `apt-get upgrade` 오류입니다.

관련 된 문제를 해결 하려면 `udev`, 다음 단계를 수행 합니다.

1. 다음을 작성 `/usr/sbin/policy-rc.d` 변경 내용을 저장 합니다.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 추가 권한을 실행 `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 다음 명령을 실행 합니다.
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306 "설치
이 레거시 콘솔을 지원 하지 않습니다는 팩트와 관련이 있습니다.
레거시 콘솔 사용 하지 않으려면:

1. Cmd.exe를 열으십시오
1. 제목을 마우스 오른쪽 단추로 클릭 모음-> 속성에는 레거시 콘솔 사용의 선택을 취소->
1. 확인을 클릭합니다.

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154 "Windows 업데이트 후
Linux 기능에 대 한 Windows 하위 시스템을 비활성화할 수 있습니다 Windows 업데이트 중입니다. 이 경우 Windows 기능을 다시 사용 하도록 설정 해야 합니다. Linux에서 찾을 수 있습니다 Windows 하위 시스템을 사용 하도록 설정 하는 것에 대 한 지침을 [설치 가이드](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)합니다.

### <a name="changing-the-display-language"></a>표시 언어 변경
WSL 설치는 Windows 설치의 로캘이 일치 하는 Ubuntu 로캘을 자동으로 변경 하려고 합니다.  이 문제를 원하지 않는 경우 설치가 완료 되 면 Ubuntu 로캘을 변경 하려면이 명령을 실행할 수 있습니다.  이 변경 내용을 적용 하려면 bash.exe를 다시 시작 해야 합니다.

아래 예제에서는 EN-US 로캘 변경 합니다.
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 시스템 복원 후 설치 문제
1.  삭제 된 `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` 폴더입니다. <br/>
  **참고: 이렇게 하지 않으면 선택적 기능에 완전히 설치 된 경우 및 작업.**
2.  WSL 선택적 기능 사용 (경우 아직)
3.  다시 부팅
4.  lxrun 제거/전체
5.  Bash를 설치 합니다.

### <a name="no-internet-access-in-wsl"></a>WSL에서 인터넷 액세스가 불가능
일부 사용자에 게 WSL에서 인터넷 액세스를 차단 하는 특정 방화벽 응용 프로그램을 사용 하 여 문제를 보고 했습니다.  보고 하는 방화벽은 다음과 같습니다.

1. Kaspersky
1. AVG
1. Avast

일부 경우에 대 한 액세스 허용 방화벽을 해제 합니다.  일부 경우에 대 한 액세스 차단 보일 방화벽이 설치 되어 있는 하기만 하면 됩니다.

### <a name="permission-denied-error-when-using-ping"></a>Ping을 사용 하는 경우 사용 권한 거부 오류
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[1 주년 업데이트](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

WSL에서 ping을 실행 하려면 Windows에서 관리자 권한이 필요 합니다.  Ping을 실행 하려면 관리자 권한으로 Windows에서 Ubuntu의 Bash를 실행 하거나 bash.exe 관리자 권한으로 CMD/PowerShell 프롬프트에서 실행 합니다.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[빌드 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  관리자 권한이 더 이상 필요 합니다.

### <a name="bash-is-hung"></a>Bash가 중지 되었습니다.
찾을 bash를 사용 하는 동안 해당 bash 중지 (또는 교착 상태)을 수집 및 메모리 덤프를 보고 하 여 문제를 진단 하는 데 도움이 입력에 응답 하지. 참고이 단계 시스템 작동이 중단 됩니다. 이 작업을 수행 하기 전에 작업을 저장 하거나 된 익숙하지 않은 경우에 이렇게 하지 마십시오.  <br/>
메모리 덤프를 수집 합니다.
1. "전체 메모리 덤프" 메모리 덤프 유형을 변경 합니다. 덤프 형식을 변경 하는 동안 현재 컴퓨터 종류를 적어둡니다.
2. 사용 된 [단계](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) 크래시를 구성 하려면 키보드 컨트롤을 사용 하 여 합니다.
3. 교착 상태를 중단을 재현 합니다.
4. 키 시퀀스 (2)를에서 사용 하 여 시스템을 충돌 합니다.
5. 시스템 크래시를 메모리 덤프를 수집 합니다.
6. 시스템이 다시 부팅 되 면 보고서를 memory.dmp secure@microsoft.com합니다. 시스템 드라이브 c: 경우 덤프 파일의 기본 위치는 %SystemRoot%\memory.dmp 또는 C:\Windows\memory.dmp 합니다. WSL 또는 Bash에 대 한 덤프 인지 확인 메일의 Windows 팀입니다.
7. 메모리 덤프 형식을 원래 설정으로 복원 합니다.

### <a name="check-your-build-number"></a>빌드 번호 확인

PC의 아키텍처 및 Windows에 대 한 빌드 번호를 찾으려면 열기  
**설정을** > **System** > **에 대 한**

검색할 합니다 **OS 빌드** 하 고 **시스템 형식** 필드입니다.  
    ![빌드 스크린샷 및 시스템 형식 필드](media/system.png) 


사용자의 Windows Server 빌드 번호를 찾으려면 다음 PowerShell에서 실행 합니다.  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>WSL 사용 하도록 설정할지 확인 합니다.
PowerShell에서 다음을 실행 하 여 Linux 용 Windows 하위 시스템 활성화 되어 있는지 확인할 수 있습니다.  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH 서버 연결 문제
다음 오류로 인해 실패 했습니다는 SSH 서버를 연결 하려고 합니다. "127.0.0.1에 의해 연결이 닫혔습니다 22 포트"입니다.
1. OpenSSH 서버에서 실행 해야 합니다.
   ``` BASH
   sudo service ssh status
   ```
   이 자습서를 수행 했다면을 https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Sshd 서비스를 중지 하 고 디버그 모드에서 sshd를 시작 합니다.
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 시작 로그를 확인 하 고 HostKeys 제공 되며 같은 로그 메시지가 표시 되지 않는 확인 합니다.
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

이러한 메시지를 보이지 키 아래에서 누락 된 경우 `/etc/ssh/`, 키를 다시 생성 하거나만 제거 및 openssh 서버를 설치 해야 합니다.
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

