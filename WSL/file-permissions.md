---
title: 파일 사용 권한
description: WSL에서 Windows의 파일 사용 권한을 확인 하는 방법 이해
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10, 파일, 사용 권한에 대 한 windows 하위 시스템
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520862"
---
# <a name="file-permissions-for-wsl"></a>WSL에 대 한 파일 권한

이 페이지에서는 linux 용 Windows 하위 시스템에서 Linux 파일 사용 권한을 해석 하는 방법에 대해 자세히 설명 합니다. 특히 NT 파일 시스템의 Windows 내부 리소스에 액세스 하는 경우에 해당 합니다. 이 설명서에서는 [Linux 파일 시스템 권한 구조](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) 를 기본적으로 이해 하 고 있다고 가정 합니다. <!--TODO: Double check that it's okay to add these links--> [umask 명령](https://en.wikipedia.org/wiki/Umask)입니다.

WSL에서 Windows 파일에 액세스할 때 파일 권한은 Windows 사용 권한에서 계산 되거나 WSL에서 파일에 추가 된 메타 데이터에서 읽혀집니다. 이 메타 데이터는 기본적으로 사용 하도록 설정 되어 있지 않습니다. 

## <a name="wsl-metadata-on-windows-files"></a>Windows 파일의 WSL 메타 데이터

WSL의 탑재 옵션으로 메타 데이터를 사용 하는 경우 Windows NT 파일의 확장 된 특성을 추가 하 고 해석 하 여 Linux 파일 시스템 권한을 제공할 수 있습니다. 

WSL은 다음과 같은 네 가지 NTFS 확장 특성을 추가할 수 있습니다.

| 특성 이름 | 설명 |
| --- | --- |
| $LXUID | 사용자 소유자 ID |
| $LXGID | 그룹 소유자 ID |
| $LXMOD | 파일 모드 (파일 시스템 권한 octals 및 형식, 예: 0777) |
| $LXDEV | 장치 (장치 파일 인 경우) |

또한 일반 파일 또는 디렉터리가 아닌 파일 (예: symlink, FIFOs, 블록 장치, unix 소켓 및 문자 장치)에도 NTFS [재분석 지점이](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)있습니다. 이렇게 하면 확장 된 특성을 쿼리하지 않고도 지정 된 디렉터리의 파일 종류를 훨씬 빠르게 확인할 수 있습니다. 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a>파일 액세스 시나리오

다음은 Linux 용 Windows 하위 시스템을 사용 하 여 다양 한 방법으로 파일에 액세스할 때 사용 권한이 결정 되는 방법에 대 한 설명입니다.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Linux에서 DrvFS (Windows 드라이브 파일 시스템)의 파일 액세스

이러한 시나리오는 `/mnt/c`를 통해 WSL에서 Windows 파일에 액세스할 때 발생 합니다. 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>기존 Windows 파일에서 파일 사용 권한 읽기

이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.

##### <a name="the-file-does-not-have-metadata-default"></a>**파일에 메타 데이터가 없습니다 (기본값).**

파일에 연결 된 메타 데이터가 없으면 Windows 사용자의 유효 사용 권한을 읽기/쓰기/실행 비트로 변환 하 고이를 사용자, 그룹 및 기타에 대 한 동일한 값으로 설정 합니다. 예를 들어 Windows 사용자 계정에 읽기 및 실행 권한이 있지만 파일에 대 한 쓰기 권한이 없는 경우 사용자, 그룹 및 기타에 대 한 `r-x`으로 표시 됩니다. Windows에서 파일에 ' 읽기 전용 ' 특성이 설정 되어 있으면 Linux에서 쓰기 권한을 부여 하지 않습니다.

##### <a name="the-file-has-metadata"></a>파일에 메타 데이터가 있습니다.

파일에 메타 데이터가 있는 경우 Windows 사용자의 유효 사용 권한을 변환 하는 대신 해당 메타 데이터 값을 사용 합니다.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Chmod를 사용 하 여 기존 Windows 파일에 대 한 파일 사용 권한 변경

이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.

##### <a name="the-file-does-not-have-metadata-default"></a>**파일에 메타 데이터가 없습니다 (기본값).**

Chmod에는 하나의 효과만 있습니다. 파일의 모든 쓰기 특성을 제거 하면 Windows 파일의 ' 읽기 전용 ' 특성이 설정 됩니다 .이는 CIFS (Common Internet File System)와 Linux의 SMB (서버 메시지 블록) 클라이언트의 동작 이기 때문입니다.

##### <a name="the-file-has-metadata"></a>파일에 메타 데이터가 있습니다.

Chmod는 파일의 기존 메타 데이터에 따라 메타 데이터를 변경 하거나 추가 합니다. 

메타 데이터에 해당 하는 경우에도 Windows에서 사용 하는 것 보다 더 많은 액세스 권한을 부여할 수 없다는 점에 유의 하세요. 예를 들어 `chmod 777`를 사용 하 여 파일에 대 한 쓰기 권한이 있지만 해당 파일에 대 한 액세스를 시도한 경우에는 해당 파일에 쓸 수 없도록 메타 데이터를 설정할 수 있습니다. Windows 파일에 대 한 읽기 또는 쓰기 명령이 Windows 사용자 권한을 통해 라우팅되도록 interopability.

#### <a name="creating-a-file-in-drivefs"></a>드라이브에서 파일 만들기

메타 데이터를 사용할 수 있는지 여부에 따라 결과가 달라 집니다.

##### <a name="metadata-is-not-enabled-default"></a>메타 데이터를 사용할 수 없습니다 (기본값).

새로 만든 파일의 Windows 권한은 특정 보안 설명자 없이 Windows에서 파일을 만든 경우와 동일 합니다 .이는 부모의 권한을 상속 합니다. 

##### <a name="metadata-is-enabled"></a>메타 데이터를 사용할 수 있습니다.

파일의 사용 권한 비트는 Linux umask을 따르도록 설정 되며 파일은 메타 데이터와 함께 저장 됩니다.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>어떤 Linux 사용자 및 Linux 그룹이 파일을 소유 하나요? 

이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.

##### <a name="the-file-does-not-have-metadata-default"></a>**파일에 메타 데이터가 없습니다 (기본값).**
기본 시나리오에서 Windows 드라이브를 automounting 때 모든 파일에 대 한 UID (사용자 ID)가 WSL 사용자의 사용자 ID로 설정 되 고 GID (그룹 ID)가 WSL 사용자의 주 그룹 ID로 설정 되도록 지정 합니다. 

##### <a name="the-file-has-metadata"></a>파일에 메타 데이터가 있습니다.

메타 데이터에 지정 된 UID 및 GID는 파일의 사용자 소유자 및 그룹 소유자로 적용 됩니다. 

### <a name="accessing-linux-files-from-windows-using-wsl"></a>`\\wsl$`를 사용 하 여 Windows에서 Linux 파일 액세스

`\\wsl$`를 통해 Linux 파일에 액세스 하면 WSL 배포판의 기본 사용자가 사용 됩니다. 따라서 Linux 파일에 액세스 하는 모든 Windows 앱은 기본 사용자와 동일한 권한을 갖습니다.

#### <a name="creating-a-new-file"></a>새 파일 만들기

Windows에서 WSL 배포판 내에 새 파일을 만들 때 기본 umask 적용 됩니다. 기본 umask은 `022`, 즉 그룹 및 기타에 대 한 쓰기 권한을 제외한 모든 사용 권한을 허용 합니다. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Linux에서 Linux 루트 파일 시스템의 파일에 액세스

Linux 루트 파일 시스템에서 생성, 수정 또는 액세스 되는 모든 파일은 umask를 새로 만든 파일에 적용 하는 것과 같은 표준 Linux 규칙을 따릅니다.

## <a name="configuring-file-permissions"></a>파일 사용 권한 구성

Wsl의 탑재 옵션을 사용 하 여 Windows 드라이브 내에서 파일 사용 권한을 구성할 수 있습니다. 탑재 옵션을 사용 하 여 `umask`, `dmask` 및 `fmask` 사용 권한 마스크를 설정할 수 있습니다. `umask` 모든 파일에 적용 되며 `dmask` 디렉터리에만 적용 되 고 `fmask` 파일에만 적용 됩니다. 이러한 권한 마스크는 파일에 적용 될 때 논리적 OR 작업을 통해 배치 됩니다. 예를 들어 `umask` 값이 `023`이 고 `fmask` 값이 `022` 이면 파일에 대 한 결과 권한 마스크는 `023`됩니다. 

이 작업을 수행 하는 방법에 대 한 지침은 [' Linux 배포판 관리 '](./wsl-config.md) 문서 페이지를 참조 하세요.
<!-- TODO: Add # to the link-->

