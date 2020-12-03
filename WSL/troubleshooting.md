---
title: Linux용 Windows 하위 시스템 문제 해결
description: Linux용 Windows 하위 시스템에서 Linux를 실행하는 동안 사용자에게 발생할 수 있는 일반적인 오류 및 문제에 대한 자세한 정보를 제공합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, Ubuntu
ms.date: 09/28/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f4040cbe9faf5d55324b56974dd5677052224dd1
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443752"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Linux용 Windows 하위 시스템 문제 해결

WSL 관련 문제에 대한 지원은 [GitHub의 WSL 제품 리포지토리](https://github.com/Microsoft/wsl/issues)를 참조하세요.

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>문제와 관련된 기존 문제 검색

기술 문제를 해결하려면 [제품 리포지토리](https://github.com/Microsoft/wsl/issues)를 사용합니다.

이 설명서의 내용과 관련된 문제는 [문서 리포지토리](https://github.com/MicrosoftDocs/wsl/issues)를 사용합니다.

## <a name="submit-a-bug-report"></a>버그 보고서 제출

WSL 함수 또는 기능과 관련된 버그는 해당 문제를 https://github.com/Microsoft/wsl/issues 제품 리포지토리에 제출합니다.

## <a name="submit-a-feature-request"></a>기능 요청 제출

WSL 기능 또는 호환성과 관련된 새로운 기능을 요청하려면 [해당 문제를 제품 리포지토리에 제출합니다](https://github.com/Microsoft/wsl/issues).

## <a name="contribute-to-the-docs"></a>문서 작성에 참여

WSL 설명서에 기여하려면 끌어오기 요청을 https://github.com/MicrosoftDocs/wsl/issues 문서 리포지토리에 제출합니다.

## <a name="terminal-or-command-line"></a>터미널 또는 명령줄

마지막으로, Windows 터미널, Windows 콘솔 또는 명령줄 UI와 관련된 문제가 있는 경우 https://github.com/microsoft/terminal Windows 터미널 리포지토리를 사용합니다.

## <a name="common-issues"></a>일반적인 문제

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a>Windows 10 버전 1903을 사용하고 있는데 WSL 2에 대한 옵션이 아직 보이지 않음

이는 머신이 아직 WSL 2의 백포트를 가져오지 않았기 때문일 수 있습니다. 이를 해결하는 가장 간단한 방법은 Windows 설정으로 이동하여 '업데이트 확인'을 클릭하여 시스템에 최신 업데이트를 설치하는 것입니다. [백포트에 대한 전체 지침](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it)을 확인하세요.

'업데이트 확인'을 눌렀는데도 업데이트를 아직 받지 못한 경우 [KB KB4566116을 수동으로 설치](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116)할 수 있습니다.  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a>오류: `wsl --set-default-version 2`인 경우 0x1bc

'표시 언어' 또는 '시스템 로캘' 설정이 영어가 아닌 경우 발생할 수 있습니다.

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

`0x1bc`의 실제 오류는 다음과 같습니다.

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

자세한 내용은 문제 [5749](https://github.com/microsoft/WSL/issues/5749)를 참조하십시오.

### <a name="cannot-access-wsl-files-from-windows"></a>Windows에서 WSL 파일에 액세스할 수 없음

9p 프로토콜 파일 서버는 Linux 쪽에서 서비스를 제공하여 Windows가 Linux 파일 시스템에 액세스할 수 있도록 합니다. Windows에서 `\\wsl$`를 사용하여 WSL에 액세스할 수 없는 경우 9P가 제대로 시작되지 않았기 때문일 수 있습니다.

이를 확인하려면 `dmesg |grep 9p`를 사용하여 시작 로그를 확인할 수 있습니다. 그러면 오류가 표시됩니다. 성공적인 출력은 다음과 같습니다.

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

이 문제에 대한 자세한 내용은 [이 Github 스레드](https://github.com/microsoft/wsl/issues/5307)를 참조하세요.

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a>WSL 2 배포를 시작할 수 없으며 출력에 'WSL 2'만 표시됨

표시 언어가 영어가 아닌 경우 오류 텍스트가 잘려서 표시될 수 있습니다.

```powershell
C:\Users\me>wsl
WSL 2
```

이 문제를 해결하려면 `https://aka.ms/wsl2kernel`을 방문하여 해당 문서 페이지의 지침에 따라 수동으로 커널을 설치하세요. 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a>Linux에서 windows.exe를 실행하는 경우 `command not found`

사용자는 Linux에서 직접 notepad.exe와 같은 Windows 실행 파일을 실행할 수 있습니다. 경우에 따라 다음과 같이 "명령을 찾을 수 없음" 오류가 발생할 수 있습니다. 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

$PATH에 win32 경로가 없는 경우 interop에서 .exe를 찾지 못합니다.
Linux에서 `echo $PATH`를 실행하여 이를 확인할 수 있습니다. 출력에 win32 경로(예: /mnt/c/Windows)가 표시되어야 합니다.
Windows 경로가 표시되지 않는 경우 Linux 셸에서 PATH를 덮어쓸 가능성이 높습니다. 

다음은 Debian의 /etc/profile로 인해 문제가 발생한 예입니다.

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

Debian에서 올바른 방법은 위의 줄을 제거하는 것입니다.
아래와 같이 할당 시 $PATH를 추가할 수도 있지만 이 경우에는 WSL 및 VSCode와 관련한 [몇 가지 다른 문제](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6)가 발생합니다.

자세한 내용은 문제 [5296](https://github.com/microsoft/WSL/issues/5296) 및 [5779](https://github.com/microsoft/WSL/issues/5779)를 참조하세요.

### <a name="error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed"></a>"Error: 0x80370102 필요한 기능이 설치되어 있지 않아 가상 머신을 시작할 수 없습니다."

가상 머신 플랫폼 Windows 기능을 활성화하고 BIOS에서 가상화가 사용되고 있는지 확인하세요.

1. [Hyper-V 시스템 요구 사항](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)을 확인합니다.

2. 머신이 VM인 경우 [중첩된 가상화](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine)를 수동으로 사용하도록 설정하세요. 관리자로 powershell을 시작하고 다음을 실행합니다.

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. 가상화를 사용하도록 설정하는 방법에 대한 자세한 지침은 PC 제조업체의 지침을 따르세요. 일반적으로 이는 시스템 BIOS를 사용하여 이러한 기능이 CPU에서 활성화되도록 할 수 있습니다. 이 프로세스에 대한 지침은 머신마다 다를 수 있습니다. 예는 Bleeping Computer의 [이 문서](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/)를 참조하세요.

4. `Virtual Machine Platform` 선택적 구성 요소를 사용하도록 설정한 후 머신을 다시 시작합니다.

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
  
   Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 [릴리스 정보](./release-notes.md)의 새로운 수정에 대한 개요가 활성화됩니다. Windows 참가자 프로그램을 구독하고 빌드가 최신 상태인지 확인하세요. Ubuntu 인스턴스 재설정을 포함하여 매우 자세히 제어하려면 [명령 참조 페이지](./reference.md)를 확인하세요.

2. Ubuntu 사용자 이진 파일

   Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 apt-get을 통해 설치한 애플리케이션을 포함하여 Ubuntu 사용자 이진 파일에 대한 모든 업데이트가 설치됩니다. 업데이트하려면 Bash에서 다음 명령을 실행하세요.
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>apt-get upgrade 오류

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
  
3. 다음 명령을 실행 합니다.

   ```bash
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

Windows 업데이트 중에 Linux용 Windows 하위 시스템 기능이 사용하지 않도록 설정될 수 있습니다. 이 문제가 발생하면 Windows 기능을 다시 사용하도록 설정해야 합니다. Linux용 Windows 하위 시스템을 사용하도록 설정하는 방법에 대한 지침은 [설치 가이드](./install-win10.md)에서 확인할 수 있습니다.

### <a name="changing-the-display-language"></a>표시 언어 변경

WSL 설치는 Windows 설치의 로캘과 일치하도록 Ubuntu 로캘을 자동으로 변경하려고 합니다.  이 동작을 원하지 않는 경우 설치가 완료된 후 다음 명령을 실행하여 Ubuntu 로캘을 변경할 수 있습니다.  이 변경 내용이 적용되려면 bash.exe를 다시 시작해야 합니다.

아래 예제에서는 로캘을 en-US로 변경합니다.

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 시스템 복원 후의 설치 문제

1. `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` 폴더를 삭제합니다. <br/>
  **참고: 선택적 기능이 완전히 설치되어 작동하는 경우에는 이 작업을 수행하지 마세요.**
2. 선택적 WSL 기능을 사용하도록 설정합니다(아직 사용하지 않는 경우).
3. 다시 부팅
4. lxrun /uninstall /full을 실행합니다
5. Bash를 설치합니다.

### <a name="no-internet-access-in-wsl"></a>WSL에서 인터넷에 액세스할 수 없음

일부 사용자가 WSL에서 인터넷 액세스를 차단하는 특정 방화벽 애플리케이션의 문제를 보고했습니다.  보고된 방화벽은 다음과 같습니다.

1. Kaspersky
2. AVG
3. Avast

방화벽을 해제하면 액세스가 허용되는 경우도 있습니다.  단순히 방화벽을 설치하면 경우에 따라 액세스가 차단되는 것처럼 보입니다.

### <a name="permission-denied-error-when-using-ping"></a>ping 사용 시의 권한 거부 오류

[Windows 1주년 업데이트, 버전 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update)의 경우 WSL에서 ping을 실행하려면 Windows의 **관리자 권한** 이 필요합니다.  ping을 실행하려면 Windows의 Ubuntu에서 관리자 권한으로 Bash를 실행하거나 CMD/PowerShell 프롬프트에서 관리자 권한으로 bash.exe를 실행합니다.

이후 버전의 Windows인 [빌드 14926 이상](./release-notes.md#build-14926)의 경우 관리자 권한이 더 이상 필요하지 않습니다.

### <a name="bash-is-hung"></a>Bash가 중지됨

Bash로 작업하는 동안 Bash가 중지되거나 교착 상태가 되어 입력에 응답하지 않는 경우 메모리 덤프를 수집하고 보고하여 문제를 진단하는 데 도움이 됩니다. 다음 단계를 수행하면 시스템의 작동이 중단됩니다. 편안하지 않으면 이 작업을 수행하지 않거나 해당 작업을 저장한 후에 수행하세요.

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
**설정** > **시스템** > **정보** 를 차례로 엽니다.

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

   ```bash
   sudo service ssh status
   ```

   그리고 https://ubuntu.com/server/docs/service-openssh 자습서를 수행했습니다.

2. sshd 서비스를 중지한 다음, 디버그 모드에서 sshd를 시작합니다.

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. 시작 로그를 확인하고, HostKeys를 사용할 수 있고 다음과 같은 로그 메시지가 표시되지 않는지 확인합니다.

   ```BASH
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

- PowerShell에서 WSL 기능 사용 명령을 실행하는 경우 [시작] 메뉴를 열고, 'Windows 기능 사용/사용 안 함'을 검색하여 GUI를 대신 사용해 본 다음, 목록에서 선택적 구성 요소를 설치할 'Linux용 Windows 하위 시스템'을 선택합니다.

- [설정], [업데이트]로 차례로 이동하고, '업데이트 확인'을 클릭하여 Windows 버전을 업데이트합니다.

- 두 단계가 모두 실패하고 WSL에 액세스해야 하는 경우 설치 미디어를 사용하여 Windows 10을 다시 설치하고 '모두 유지'를 선택하여 앱과 파일이 유지되도록 하는 방식으로 업그레이드하는 것이 좋습니다. 이 작업을 수행하는 방법에 대한 지침은 [Windows 10 다시 설치](https://support.microsoft.com/help/4000735/windows-10-reinstall) 페이지에서 확인할 수 있습니다.

### <a name="correct-ssh-related-permission-errors"></a>(SSH 관련) 권한 오류 해결

이 오류가 표시되는 경우:

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

이 문제를 해결하려면 다음을 ```/etc/wsl.conf``` 파일에 추가합니다.

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

이 명령을 추가하면 메타데이터가 포함되고 WSL에서 보이는 Windows 파일에 대한 파일 권한이 수정됩니다. 자세한 내용은 [파일 시스템 권한](./file-permissions.md)에서 확인하세요.

### <a name="running-windows-commands-fails-inside-a-distribution"></a>배포 내에서 Windows 명령 실행 실패

[Microsoft Store에서 제공되는](install-win10.md#step-6---install-your-linux-distribution-of-choice) 일부 배포는 아직 완전히 호환되지 않아서 기본적으로 [터미널](https://en.wikipedia.org/wiki/Linux_console)에서 Windows 명령을 실행할 수 없습니다. `powershell.exe /c start .` 또는 다른 Windows 명령을 실행할 때 `-bash: powershell.exe: command not found` 오류가 발생하면 다음 단계를 수행하여 해결할 수 있습니다.

1. WSL 배포에서 `echo $PATH`를 실행합니다.  
   `/mnt/c/Windows/system32`를 포함하지 않는 경우 무언가 표준 PATH 변수를 다시 정의하는 것입니다.
2. `cat /etc/profile`을 사용하여 프로필 설정을 확인하세요.  
   PATH 변수 할당을 포함하는 경우에는 파일을 편집하여 **#** 문자로 PATH 할당 블록을 주석 처리합니다.
3. wsl.conf가 있는지 확인하고(`cat /etc/wsl.conf`) `appendWindowsPath=false`가 없는지 확인합니다. 있는 경우에는 주석 처리합니다.
4. `wsl -t ` 다음에 배포 이름을 입력하여 배포를 다시 시작하거나 cmd 또는 PowerShell에서 `wsl --shutdown`을 실행합니다.

### <a name="unable-to-boot-after-installing-wsl-2"></a>WSL 2를 설치한 후 부팅할 수 없음

사용자가 WSL 2를 설치한 후 부팅할 수 없는 문제에 대해 알고 있습니다. 현재 이러한 문제를 철저하게 진단하고 있으며, [버퍼 크기를 변경](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363)하거나 [적절한 드라이버를 설치](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244)하면 이 문제를 해결하는 데 도움이 된다는 사용자들의 제보가 있었습니다. [Github 문제](https://github.com/microsoft/WSL/issues/4784)에서 이 문제에 대한 최신 업데이트를 확인하세요. 
