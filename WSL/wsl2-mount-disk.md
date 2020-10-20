---
title: WSL 2에서 Linux 디스크 탑재 시작 (미리 보기)
description: WSL 2에서 디스크 탑재를 설정 하는 방법 및 액세스 하는 방법에 대해 알아봅니다.
keywords: wsl, windows, windowssubsystem, gnu, linux, bash, disk, ext4, filesystem, mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8c67b0f34dcde925bb91979e9153049fdd474db3
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211737"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a>WSL 2에서 Linux 디스크 탑재 시작 (미리 보기)

Windows에서 지원 되지 않는 Linux 디스크 형식에 액세스 하려는 경우 WSL 2를 사용 하 여 디스크를 탑재 하 고 해당 콘텐츠에 액세스할 수 있습니다.

이 자습서에서는 WSL2에 연결할 디스크와 파티션을 식별 하는 단계, 탑재 하는 방법 및 액세스 하는 방법을 설명 합니다.

> [!NOTE]
> WSL 2에 디스크를 연결 하려면 관리자 권한이 필요 합니다.

## <a name="identify-the-disk"></a>디스크 식별

Windows에서 사용 가능한 디스크를 나열 하려면 다음을 실행 합니다.

```powershell
wmic diskdrive list brief
```

디스크 경로는 ' DeviceID ' 열 아래에서 사용할 수 있습니다. 일반적으로 `\\.\PHYSICALDRIVE*` 형식입니다.

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a>WSL 2에 탑재할 파티션을 나열 하 고 선택 합니다.

디스크를 확인 한 후 다음을 실행 합니다.

```powershell
wsl --mount <DiskPath> --bare
```

그러면 WSL 2에서 디스크를 사용할 수 있게 됩니다.

연결 되 면 WSL 2 내에서 다음 명령을 실행 하 여 파티션을 나열할 수 있습니다.

```powershell
lsblk
```

사용 가능한 블록 장치 및 파티션이 표시 됩니다.

Linux 내에서 블록 장치는로 식별 됩니다  `/dev/<Device><Partition>` . 예를 들어,/dev/sdb3는 디스크의 파티션 번호 3입니다 `sdb` .

예제 출력:

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a>파일 시스템 유형 식별

디스크 또는 파티션의 파일 시스템 유형을 알 수 없는 경우 다음 명령을 사용할 수 있습니다.

```powershell
blkid <BlockDevice>
```

그러면 검색 된 파일 시스템 유형이 형식으로 출력 됩니다 `TYPE="<Filesystem>"` .

## <a name="mount-the-selected-partitions"></a>선택한 파티션 탑재

탑재 하려는 파티션을 식별 한 후에는 각 파티션에서 다음 명령을 실행 합니다. 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> 전체 디스크를 단일 볼륨으로 탑재 하려는 경우 (즉, 디스크가 분할 되지 않은 경우)에는를 `--partition` 생략할 수 있습니다.
> 
> 생략 하는 경우 기본 파일 시스템 유형은 "ext4"입니다.

## <a name="access-the-disk-content"></a>디스크 내용 액세스

탑재 된 후에는 구성 값이 가리키는 경로에서 디스크에 액세스할 수 `automount.root` 있습니다. 기본값은 `/mnt/wsl`입니다.

Windows에서 다음으로 이동 하 여 파일 탐색기에서 디스크에 액세스할 수 있습니다 `\\wsl$\\<Distro>\\<Mountpoint>` (Linux 배포 선택).

## <a name="unmount-the-disk"></a>디스크 분리

WSL 2에서 디스크를 분리 하 고 분리 하려면 다음을 실행 합니다.

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a>명령줄 참조

### <a name="mouting-a-specific-filesystem"></a>특정 파일 시스템 이전

기본적으로 WSL 2는 ext4으로 장치를 탑재 하려고 시도 합니다. 다른 파일 시스템을 지정 하려면 다음을 실행 합니다.

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

예를 들어 fat로 디스크를 탑재 하려면 다음을 실행 합니다.

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> WSL2에서 사용 가능한 파일 시스템를 나열 하려면 다음을 실행 합니다. `cat /proc/filesystems`

### <a name="mouting-a-specific-partition"></a>특정 파티션 이전

기본적으로 WSL 2는 전체 디스크를 탑재 하려고 시도 합니다. 특정 파티션을 탑재 하려면 다음을 실행 합니다.

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

디스크가 MBR (마스터 부트 레코드) 또는 GPT (GUID 파티션 테이블) 인 경우에만 작동 합니다. [파티션 스타일 (MBR 및 GPT)에 대해 읽어 보십시오](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).

### <a name="specifying-mount-options"></a>탑재 옵션 지정

탑재 옵션을 지정 하려면 다음을 실행 합니다.

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

예제:

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> 지금은 파일 시스템 전용 옵션만 지원 됩니다. 과 같은 일반 옵션 `ro, rw, noatime, ...` 은 지원 되지 않습니다.

### <a name="attaching-the-disk-without-mounting-it"></a>탑재 하지 않고 디스크 연결

위의 옵션 중 하나에서 디스크 구성표를 지원 하지 않는 경우 다음을 실행 하 여 탑재 하지 않고 WSL 2에 디스크를 연결할 수 있습니다.

```powershell
wsl --mount <DiskPath> --bare
```

그러면 WSL 2 내에서 블록 장치를 사용할 수 있게 되므로 해당 장치에서 수동으로 탑재할 수 있습니다. `lsblk`를 사용 하 여 WSL 2 내에서 사용 가능한 블록 장치를 나열 합니다.

### <a name="detaching-a-disk"></a>디스크 분리

WSL 2에서 디스크를 분리 하려면 다음을 실행 합니다.

```powershell
wsl --unmount [DiskPath]
```

`Diskpath`을 생략 하면 연결 된 모든 디스크가 분리 되어 분리 됩니다.

> [!NOTE]
> 한 디스크를 분리 하는 데 실패 한 경우 WSL 2는 디스크를 분리 하는를 실행 하 여 강제로 종료 될 수 있습니다 `wsl --shutdown` .

## <a name="limitations"></a>제한 사항

- 현재는 전체 디스크만 WSL 2에 연결 될 수 있습니다. 즉, 파티션만 연결할 수는 없습니다. 이는 구체적으로를 사용 하 여 부팅 장치에서 파티션을 읽을 수 없다는 것을 의미 합니다 `wsl --mount` .이 장치는 Windows에서 분리 될 수 없기 때문입니다.

- 지금은 USB 플래시 드라이브를 지원 하지 않으며 WSL 2에 연결 되지 않습니다. 그러나 USB 디스크는 지원 됩니다.

- 커널을 통해 기본적으로 지원 되는 파일 시스템만에 탑재할 수 있습니다 `wsl --mount` . 즉,을 호출 하 여 설치 된 파일 시스템 드라이버 (예: ntfs-3g)를 사용할 수 없습니다 `wsl --mount` .
