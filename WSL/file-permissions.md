---
title: 파일 권한
description: WSL에서 Windows의 파일 권한을 결정하는 방법을 살펴봅니다.
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 파일, 권한
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 81d4cfa1ae57cdd077ba8cbd614111881724718a
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336076"
---
# <a name="file-permissions-for-wsl"></a>WSL에 대한 파일 권한

이 페이지에서는 Linux용 Windows 하위 시스템에서, 특히 NT 파일 시스템에서 Windows 내의 리소스에 액세스할 때 Linux 파일 권한을 해석하는 방법에 대해 자세히 설명합니다. 이 설명서에서는 [Linux 파일 시스템 권한 구조](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) 및 [umask 명령](https://en.wikipedia.org/wiki/Umask)을 기본적으로 이해하고 있다고 가정합니다.

WSL에서 Windows 파일에 액세스할 때 파일 권한은 Windows 권한에서 계산되거나 WSL에서 파일에 추가한 메타데이터로부터 읽어들입니다. 이 메타데이터는 기본적으로 사용하도록 설정되어 있지 않습니다.

## <a name="wsl-metadata-on-windows-files"></a>Windows 파일의 WSL 메타데이터

WSL에서 메타데이터를 탑재 옵션으로 사용하도록 설정된 경우 Windows NT 파일에 대한 확장 특성을 추가하고 해석하여 Linux 파일 시스템 권한을 제공할 수 있습니다.

WSL에서 추가할 수 있는 네 가지 NTFS 확장 특성은 다음과 같습니다.

| 특성 이름 | 설명 |
| --- | --- |
| $LXUID | 사용자 소유자 ID |
| $LXGID | 그룹 소유자 ID |
| $LXMOD | 파일 모드(파일 시스템 권한 8진수 및 형식(예: 0777)) |
| $LXDEV | 디바이스(디바이스 파일인 경우) |

또한 일반 파일 또는 디렉터리가 아닌 파일(예: symlinks, FIFO, 블록 디바이스, Unix 소켓 및 문자 디바이스)에는 NTFS [재분석 지점](https://docs.microsoft.com/windows/win32/fileio/reparse-points)도 있습니다. 이렇게 하면 확장 특성을 쿼리하지 않고도 지정된 디렉터리에서 파일 종류를 더 빨리 확인할 수 있습니다.

## <a name="file-access-scenarios"></a>파일 액세스 시나리오

다음은 Linux용 Windows 하위 시스템을 사용하여 다양한 방법으로 파일에 액세스할 때 권한이 결정되는 방법에 대해 설명합니다.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Linux에서 Windows DrvFS(드라이브 파일 시스템)의 파일 액세스

이러한 시나리오는 대부분 `/mnt/c`를 통해 WSL에서 Windows 파일에 액세스할 때 발생합니다.

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>기존 Windows 파일에서 파일 권한 읽기

기존 메타데이터가 파일에 이미 있는지 여부에 따라 결과가 달라집니다.

##### <a name="drvfs-file-does-not-have-metadata-default"></a>DrvFS 파일에 메타데이터가 없음(기본값)

메타데이터가 파일에 연결되어 있지 않으면 유효한 Windows 사용자 권한을 비트 읽기/쓰기/실행 권한으로 변환하여 이를 사용자, 그룹 및 기타에 대한 동일한 값으로 설정합니다. 예를 들어 파일에 대한 읽기 및 실행 액세스 권한은 Windows 사용자 계정에 있지만 쓰기 액세스 권한이 없는 경우 이는 사용자, 그룹 및 기타에 대해 `r-x`로 표시됩니다. Windows에서 '읽기 전용' 특성이 파일에 설정되어 있으면 Linux에서 쓰기 액세스 권한이 부여되지 않습니다.

##### <a name="the-file-has-metadata"></a>파일에 메타데이터가 있음

메타데이터가 파일에 있는 경우 유효한 Windows 사용자 권한을 변환하는 대신 해당 메타데이터 값을 사용합니다.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>chmod를 사용하여 기존 Windows 파일에 대한 파일 권한 변경

기존 메타데이터가 파일에 이미 있는지 여부에 따라 결과가 달라집니다.

##### <a name="chmod-file-does-not-have-metadata-default"></a>메타데이터가 chmod 파일에 없음(기본값)

chmod에는 하나의 효과만 있습니다. 파일의 쓰기 특성을 모두 제거하면 Windows 파일의 '읽기 전용' 특성이 설정됩니다. 이는 Linux의 SMB(서버 메시지 블록) 클라이언트인 CIFS(일반 인터넷 파일 시스템)의 동작과 동일하기 때문입니다.

##### <a name="chmod-file-has-metadata"></a>메타데이터가 chmod 파일에 있음

chmod는 파일의 기존 메타데이터에 따라 메타데이터를 변경하거나 추가합니다. 

메타데이터에 해당하는 경우에도 Windows에 있는 것보다 더 많은 액세스 권한을 부여할 수 없습니다. 예를 들어 `chmod 777`을 사용하여 파일에 대한 쓰기 권한이 있음을 표시하도록 메타데이터를 설정할 수 있지만, 해당 파일에 액세스하려고 하는 경우 여전히 파일에 쓸 수 없습니다. 이는 Windows 파일에 대한 읽기 또는 쓰기 명령이 Windows 사용자 권한을 통해 라우팅되는 상호 운용성 때문입니다.

#### <a name="creating-a-file-in-drivefs"></a>DriveFS에서 파일 만들기

메타데이터를 사용하도록 설정되었는지 여부에 따라 결과가 달라집니다.

##### <a name="metadata-is-not-enabled-default"></a>메타데이터를 사용할 수 없음(기본값)

새로 만든 파일의 Windows 권한은 특정 보안 설명자 없이 Windows에서 파일을 만든 경우와 동일하며 부모의 권한을 상속합니다.

##### <a name="metadata-is-enabled"></a>메타데이터를 사용할 수 있음

파일의 권한 비트는 Linux umask를 따르도록 설정되고, 파일은 메타데이터와 함께 저장됩니다.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>어떤 Linux 사용자 및 Linux 그룹에서 파일을 소유하나요? 

기존 메타데이터가 파일에 이미 있는지 여부에 따라 결과가 달라집니다.

##### <a name="user-file-does-not-have-metadata-default"></a>메타데이터가 사용자 파일에 없음(기본값)

기본 시나리오에서는 Windows 드라이브를 자동으로 탑재할 때 파일에 대한 UID(사용자 ID)가 WSL 사용자의 사용자 ID로 설정되고 GID(그룹 ID)가 WSL 사용자의 주 그룹 ID로 설정되도록 지정합니다.

##### <a name="user-file-has-metadata"></a>메타데이터가 사용자 파일에 있음

메타데이터에 지정된 UID와 GID가 파일의 사용자 소유자 및 그룹 소유자로 적용됩니다.

### <a name="accessing-linux-files-from-windows-using-wsl"></a>`\\wsl$`을 사용하여 Windows에서 Linux 파일에 액세스

`\\wsl$`을 통해 Linux 파일에 액세스하면 WSL 배포의 기본 사용자가 사용됩니다. 따라서 Linux 파일에 액세스하는 모든 Windows 앱은 기본 사용자와 동일한 권한을 갖습니다.

#### <a name="creating-a-new-file"></a>새 파일 만들기

Windows에서 WSL 배포 내에 새 파일을 만들 때 기본 umask가 적용됩니다. 기본 umask는 `022`입니다. 즉 그룹 및 기타에 대한 쓰기 권한을 제외한 모든 권한을 허용합니다. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Linux에서 Linux 루트 파일 시스템의 파일 액세스

Linux 루트 파일 시스템에서 만들거나 수정하거나 액세스하는 모든 파일은 umask를 새로 만든 파일에 적용하는 것과 같은 표준 Linux 규칙을 따릅니다.

## <a name="configuring-file-permissions"></a>파일 권한 구성

wsl.conf의 탑재 옵션을 사용하여 Windows 드라이브 내에서 파일 권한을 구성할 수 있습니다. 탑재 옵션을 사용하면 `umask`, `dmask` 및 `fmask` 권한 마스크를 설정할 수 있습니다. `umask`는 모든 파일에 적용되고, `dmask`는 디렉터리에만 적용되며, `fmask`는 파일에만 적용됩니다. 그런 다음, 이러한 권한 마스크는 파일에 적용될 때 논리 OR 연산을 수행합니다. 예를 들어 `umask` 값이 `023`이고 `fmask` 값이 `022`인 경우 파일에 대한 결과 권한 마스크는 `023`이 됩니다.

이 작업을 수행하는 방법에 대한 지침은 [wslconf를 사용하여 배포판별 시작 설정 구성](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf) 문서를 참조하세요.
