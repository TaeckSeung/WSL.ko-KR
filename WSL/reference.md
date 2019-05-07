---
title: Linux 명령 참조에 대 한 Windows 하위 시스템
description: Linux 용 Windows 하위 시스템을 관리 하는 명령 목록
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem ubuntu 용 windows 하위 시스템
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063581"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에 대 한 명령 참조

> `lxrun.exe` Windows 10 1803부터 사용 되지 않는 이상 됩니다.

명령을 `lxrun.exe` 상호 작용에 사용할 수는 [Windows 하위 시스템에 대 한 WSL (Linux)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) 직접.  이러한 명령에 설치 되는 `\Windows\System32` 디렉터리 및 Windows 명령 프롬프트 내에서 또는 PowerShell에서 실행할 수 있습니다.

* `lxrun.exe` WSL를 관리에 사용 됩니다.  설치 또는 Ubuntu 이미지를 제거 하려면이 명령을 사용할 수 있습니다.


| Command                     | 설명                     |
|:----------------------------|:---------------------------|
| `bash`                      | 현재 디렉터리에서 Bash 셸을 시작합니다.  Bash 셸 자동으로 설치 되지 않은 경우 실행 `lxrun /install` |
| `bash ~`                    | 사용자의 Ubuntu에 대 한 홈 디렉터리에 bash 셸을 시작합니다.  Cd 실행 비슷합니다 ~            |
| `bash -c "<command>"`       | 명령을 실행 하 고 출력에 인쇄 다시 Windows 명령 프롬프트를 종료 합니다. <br/> <br/> 예: **-c "ls"의 bash** |

<p>

| Command                     | 설명                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 명령은 WSL 인스턴스 관리에 사용 됩니다. |
| `lxrun /install`            | 다운로드를 시작 하 고 프로세스를 설치 합니다. <br/> **/y** 모든 메시지를 표시 하지 않으려면 추가할 수 있습니다.  확인 프롬프트를 자동으로 적용 및 기본 사용자가 루트으로 설정 합니다.          |
| `lxrun /uninstall`          | 제거 되 고 Ubuntu 이미지를 삭제 합니다.  기본적으로이 사용자의 Ubuntu에 대 한 홈 디렉터리를 제거 되지 않습니다. <br/> **/y** 확인 프롬프트를 자동으로 적용할 추가할 수 있습니다 <br/>**전체/** 제거 되 고 사용자의 Ubuntu에 대 한 홈 디렉터리를 삭제 합니다.         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu 사용자의 기본 Bash를 설정합니다. 지정된 된 사용자가 없으면 암호를 묻는 됩니다.  자세한 내용은 참조: https://aka.ms/wslusers합니다. <br/> **/y** 암호 바이패스 promping 합니다.  사용자는 암호 없이 생성 됩니다.|
| `lxrun /update`            | 하위 시스템의 패키지 인덱스 업데이트          |
