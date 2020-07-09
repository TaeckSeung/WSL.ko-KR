---
title: MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server 또는 Redis를 사용 하 여 Linux 용 Windows 하위 시스템에서 데이터베이스 설정 시작
description: Linux 용 Windows 하위 시스템에서 MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server 또는 Redis를 설정 하는 방법에 대해 알아봅니다.
keywords: wsl, windows, windowssubsystem, MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server, Redis, windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8ffd40ef21e8fb8ece529157852ba5d8bb676076
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2020
ms.locfileid: "86160228"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템에서 데이터베이스 시작

이 단계별 가이드는 WSL의 프로젝트를 데이터베이스에 연결 하기 시작 하는 데 도움이 됩니다. MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server 또는 SQLite를 시작 하세요.

## <a name="prerequisites"></a>필수 구성 요소

- Windows 10 실행, [버전 2004로 업데이트](ms-settings:windowsupdate), **빌드 19041** 이상.
- [Wsl을 사용 및 설치 하 고 wsl 2로 업데이트 했습니다](https://docs.microsoft.com/windows/wsl/install-win10).
- [Linux 배포](https://docs.microsoft.com/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (이 예에서는 Ubuntu 18.04)가 설치 되어 있습니다.
- Ubuntu 18.04 배포가 [WSL 2 모드로 실행](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2)되 고 있는지 확인 합니다. WSL은 v1 또는 v2 모드에서 배포를 실행할 수 있습니다. PowerShell을 열고 다음을 입력 하 여이를 확인할 수 있습니다.`wsl -l -v`

## <a name="differences-between-database-systems"></a>데이터베이스 시스템의 차이점

데이터베이스 시스템에 가장 [많이 사용 되는 선택 항목](https://insights.stackoverflow.com/survey/2019#technology-_-databases) 은 다음과 같습니다.

- [MySQL](https://www.mysql.com/why-mysql/) (SQL)
- [PostgreSQL](https://www.postgresql.org/about/) (SQL)
- [Microsoft SQL Server](https://docs.microsoft.com/sql/?view=sql-server-ver15) (SQL)
- [SQLite](https://www.sqlite.org/about.html) (SQL)
- [MongoDB](https://www.mongodb.com/what-is-mongodb) (nosql)
- [Redis](https://redis.io/topics/introduction) (nosql)

**MySQL** 은 데이터 형식이 서로 관련 될 수 있는 하나 이상의 테이블로 데이터를 구성 하는 오픈 소스 SQL 관계형 데이터베이스입니다. 수직 확장 가능 합니다. 즉, 한 최종 컴퓨터에서 작업을 수행 합니다. 현재는 4 개의 데이터베이스 시스템에서 가장 널리 사용 되 고 있습니다.

**PostgreSQL** (Postgres 라고도 함)는 확장성 및 표준 준수를 강조 하는 오픈 소스 SQL 관계형 데이터베이스 이기도 합니다. 이제 JSON도 처리할 수 있지만, 일반적으로 정형 데이터, 수평적 크기 조정 및 전자 상거래 및 금융 거래와 같은 ACID 호환 요구에 더 적합합니다.

**Microsoft SQL Server** 에는 Azure의 Windows, SQL SERVER ON LINUX 및 SQL에 대 한 SQL Server 포함 되어 있습니다. 또한 소프트웨어 응용 프로그램에서 요청 하는 데이터를 저장 하 고 검색 하는 기본 기능을 사용 하 여 서버에 설정 된 관계형 데이터베이스 관리 시스템입니다.

**SQLite** 는 오픈 소스에 포함 된 파일 기반의 "서버를 사용 하지 않는" 데이터베이스 이며, 메모리 부족 환경 에서도 이식성, 안정성 및 뛰어난 성능에 대해 알려져 있습니다.

**MongoDB** 는 JSON을 사용 하 고 스키마 없는 데이터를 저장 하도록 설계 된 오픈 소스 nosql 문서 데이터베이스입니다. 수평 확장 가능 합니다. 즉, 여러 개의 작은 컴퓨터에서 작업을 수행 합니다. 유연 하 고 구조화 되지 않은 데이터에 적합 하며 실시간 분석을 캐싱합니다.

**Redis** 은 오픈 소스 nosql 메모리 내 데이터 구조 저장소입니다. 문서 대신 저장소에 대 한 키-값 쌍을 사용 합니다. Redis는 유연성, 성능 및 와이드 언어 지원에 대해 알려져 있습니다. 캐시 또는 메시지 브로커로 사용할 수 있을 정도로 유연 하며 목록, 집합 및 해시와 같은 데이터 구조를 사용할 수 있습니다.

선택한 데이터베이스의 종류는 데이터베이스와 함께 사용하는 애플리케이션의 유형에 따라 달라집니다. 정형 및 비정형 데이터베이스의 장점과 단점을 살펴보고 사용 사례에 따라 선택하는 것이 좋습니다.

## <a name="install-mysql"></a>MySQL 설치

WSL에 MySQL을 설치 하려면 (Ubuntu 18.04):

1. WSL 터미널을 엽니다(예: Ubuntu 18.04).
2. Ubuntu 패키지를 업데이트합니다. `sudo apt update`
3. 패키지가 업데이트 된 후 다음을 사용 하 여 MySQL을 설치 합니다.`sudo apt install mysql-server`
4. 설치를 확인하고 버전 번호(`mysql --version`)를 가져옵니다.

포함 된 보안 스크립트를 실행할 수도 있습니다. 이렇게 하면 원격 루트 로그인 및 샘플 사용자와 같은 항목에 대 한 보안 수준이 낮은 기본 옵션이 변경 됩니다. 보안 스크립트를 실행 하려면 다음을 수행 합니다.

1. MySQL 서버 시작:`sudo /etc/init.d/mysql start`
2. 보안 스크립트 프롬프트를 시작 합니다.`sudo mysql_secure_installation`
3. 첫 번째 메시지는 MySQL 암호의 강도를 테스트 하는 데 사용할 수 있는 암호 유효성 검사 플러그 인을 설정할지 여부를 묻는 메시지를 표시 합니다. 그런 다음 MySQL 루트 사용자에 대 한 암호를 설정 하 고, 익명 사용자를 제거할지 여부를 결정 하 고, 루트 사용자가 로컬 및 원격으로 로그인 할 수 있도록 허용할지 여부를 결정 하 고, 테스트 데이터베이스를 제거할지 여부를 결정 하 고, 마지막으로 권한 테이블을 즉시 다시 로드할지 여부를 결정 합니다.

MySQL 프롬프트를 열려면 다음을 입력 합니다.`sudo mysql`

사용 가능한 데이터베이스를 확인 하려면 MySQL 프롬프트에 다음을 입력 합니다.`SHOW DATABASES;`

새 데이터베이스를 만들려면 다음을 입력 합니다.`CREATE DATABASE database_name;`

데이터베이스를 삭제 하려면 다음을 입력 합니다.` DROP DATABASE database_name;`

MySQL 데이터베이스 작업에 대 한 자세한 내용은 [mysql 문서](https://dev.mysql.com/doc/mysql-getting-started/en/)를 참조 하세요.

VS Code에서 MySQL 데이터베이스로 작업 하려면 [mysql 확장](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2)을 시도 합니다.

## <a name="install-postgresql"></a>PostgreSQL 설치

WSL (Ubuntu 18.04)에 PostgreSQL를 설치 하려면 다음을 수행 합니다.

1. WSL 터미널을 엽니다(예: Ubuntu 18.04).
2. Ubuntu 패키지를 업데이트합니다. `sudo apt update`
3. 패키지가 업데이트된 후에는 PostgreSQL(몇 가지 유용한 유틸리티가 포함된 -contrib 패키지)을 설치합니다. `sudo apt install postgresql postgresql-contrib`
4. 설치를 확인하고 버전 번호(`psql --version`)를 가져옵니다.

PostgreSQL이 설치되면 다음 세 가지 명령을 알고 있어야 합니다.

- `sudo service postgresql status`: 데이터베이스의 상태 확인
- `sudo service postgresql start`: 데이터베이스 실행 시작
- `sudo service postgresql stop`: 데이터베이스 실행 중지

기본 관리자 사용자 `postgres`에는 데이터베이스에 연결하기 위해 할당된 암호가 필요합니다. 암호를 설정하려면 다음을 수행합니다.

1. `sudo passwd postgres` 명령을 입력합니다.
2. 새 암호를 입력하라는 메시지가 표시됩니다.
3. 터미널을 닫았다가 다시 엽니다.

[Psql](https://www.postgresql.org/docs/10/app-psql.html) shell을 사용 하 여 PostgreSQL를 실행 하려면:

1. Postgres 서비스를 시작합니다. `sudo service postgresql start`
2. Postgres 서비스에 연결하고 psql 셸을 엽니다. `sudo -u postgres psql`

psql 셸을 성공적으로 입력하면 명령줄 변경 내용이 다음과 같이 표시됩니다. `postgres=#`

> [!NOTE]
> 또는 `su - postgres`를 사용하여 postgres 사용자로 전환한 다음, `psql` 명령을 입력하여 psql 셸을 열 수 있습니다.

Postgres = # enter `\q` 키를 누르거나 바로 가기 키 (Ctrl + D)를 사용 합니다.

PostgreSQL 설치에 생성된 사용자 계정을 확인하려면 WSL 터미널에서 `psql -c "\du"`를 사용하거나 psql 셸이 열려 있는 경우 `\du`를 사용합니다. 이 명령은 계정 사용자 이름, 역할 특성 목록 및 역할 그룹의 멤버 열을 표시 합니다. 명령줄로 돌아가려면 `q`를 입력합니다.

PostgreSQL 데이터베이스 사용에 대 한 자세한 내용은 [PostgreSQL 문서](https://www.postgresql.org/docs/13/tutorial-createdb.html)를 참조 하세요.

VS Code에서 PostgreSQL 데이터베이스로 작업 하려면 [PostgreSQL 확장](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql)을 시도 합니다.

## <a name="install-mongodb"></a>MongoDB 설치

WSL (Ubuntu 18.04)에 MongoDB를 설치 하려면 다음을 수행 합니다.

1. WSL 터미널을 엽니다(예: Ubuntu 18.04).
2. Ubuntu 패키지를 업데이트합니다. `sudo apt update`
3. 패키지가 업데이트되면 `sudo apt-get install mongodb`를 사용하여 MongoDB를 설치합니다.
4. 설치를 확인하고 버전 번호(`mongod --version`)를 가져옵니다.

MongoDB가 설치되면 다음 세 가지 명령을 알고 있어야 합니다.

- `sudo service mongodb status`: 데이터베이스의 상태 확인
- `sudo service mongodb start`: 데이터베이스 실행 시작
- `sudo service mongodb stop`: 데이터베이스 실행 중지

> [!NOTE]
> 자습서 또는 문서에 사용된 `sudo systemctl status mongodb` 명령이 표시될 수 있습니다. WSL은 경량 상태를 유지하기 위해 `systemd`(Linux의 서비스 관리 시스템)를 포함하지 않습니다. 대신 SysVinit를 사용하여 머신에서 서비스를 시작합니다. 차이점은 볼 수 없지만 자습서에서 `sudo systemctl` 사용을 권장하는 경우 대신 `sudo /etc/init.d/`를 사용합니다. 예를 들어 WSL에 대한 `sudo systemctl status mongodb`는 `sudo /etc/inid.d/mongodb status`가 될 수 있습니다. 또는 `sudo service mongodb status`를 사용할 수도 있습니다.

로컬 서버에서 Mongo 데이터베이스를 실행 하려면 다음을 수행 합니다.

1. 데이터베이스 상태 확인: `sudo service mongodb status` 데이터베이스를 이미 시작한 경우를 제외 하 고 [Fail] 응답이 표시 되어야 합니다.

2. 데이터베이스 시작: `sudo service mongodb start` 이제 [OK] 응답이 표시 됩니다.

3. 데이터베이스 서버에 연결 하 고 진단 명령을 실행 하 여 확인 `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` 합니다. 그러면 현재 데이터베이스 버전, 서버 주소 및 포트, 상태 명령의 출력이 출력 됩니다. 응답의 “확인” 필드에 대한 `1` 값은 서버가 작동하고 있음을 나타냅니다.

4. MongoDB 서비스가 실행되는 것을 중지하려면 `sudo service mongodb stop`을 입력합니다.

> [!NOTE]
> MongoDB에는 데이터를 /data/db에 저장하고 포트 27017에서 실행하는 등의 몇 가지 기본 매개 변수가 있습니다. 또한 `mongod`는 디먼(데이터베이스에 대한 호스트 프로세스)이고 `mongo`는 `mongod`의 특정 인스턴스에 연결하는 명령줄 셸입니다.

[Azure CosmosDB 확장](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb)을 통해 MongoDB 데이터베이스 작업을 지원 VS Code VS Code 내에서 MongoDB 데이터베이스를 만들고 관리 하 고 쿼리할 수 있습니다. 자세히 알아보려면 [MongoDB 작업](https://code.visualstudio.com/docs/azure/mongodb): 문서를 VS Code 참조 하세요.

MongoDB 문서에서 자세히 알아보세요.

- [MongoDB 사용 소개](https://docs.mongodb.com/manual/introduction/)
- [사용자 만들기](https://docs.mongodb.com/manual/tutorial/create-users/)
- [원격 호스트에서 MongoDB 인스턴스에 연결](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [CRUD: 만들기, 읽기, 업데이트, 삭제](https://docs.mongodb.com/manual/crud/)
- [참조 문서](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a>Microsoft SQL Server 설치

WSL (Ubuntu 18.04)에 SQL Server를 설치 하려면이 빠른 시작: [ubuntu에 SQL Server 설치 및 데이터베이스 만들기](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15)를 따릅니다.

VS Code에서 Microsoft SQL Server 데이터베이스를 사용 하려면 [MSSQL 확장](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql)을 시도 합니다.

## <a name="install-sqlite"></a>SQLite 설치

WSL (Ubuntu 18.04)에 SQLite를 설치 하려면 다음을 수행 합니다.

1. WSL 터미널을 엽니다(예: Ubuntu 18.04).
2. Ubuntu 패키지를 업데이트합니다. `sudo apt update`
3. 패키지가 업데이트 된 후 다음을 사용 하 여 SQLite3를 설치 합니다.`sudo apt install sqlite3`
4. 설치를 확인하고 버전 번호(`sqlite3 --version`)를 가져옵니다.

"Example. db" 라는 테스트 데이터베이스를 만들려면 다음을 입력 합니다.`sqlite3 example.db`

SQLite 데이터베이스 목록을 보려면 다음을 입력 합니다.`.databases`

데이터베이스의 상태를 확인 하려면 다음을 입력 합니다.`.dbinfo ?DB?`

SQLite 프롬프트를 종료 하려면 다음을 입력 합니다.`.exit`

SQLite 데이터베이스 작업에 대 한 자세한 내용은 [sqlite 문서](https://www.sqlite.org/quickstart.html)를 참조 하세요.

VS Code에서 SQLite 데이터베이스를 사용 하려면 [sqlite 확장](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools)을 시도 합니다.

## <a name="install-redis"></a>Redis 설치

WSL (Ubuntu 18.04)에 Redis를 설치 하려면 다음을 수행 합니다.

1. WSL 터미널을 엽니다(예: Ubuntu 18.04).
2. Ubuntu 패키지를 업데이트합니다. `sudo apt update`
3. 패키지가 업데이트 된 후 다음을 사용 하 여 Redis를 설치 합니다.`sudo apt install redis-server`
4. 설치를 확인하고 버전 번호(`redis-server --version`)를 가져옵니다.

Redis 서버 실행을 시작 하려면 다음을 수행 합니다.`sudo service redis-server start`

Redis가 작동 하는지 확인 합니다 (redis은 Redis와 통신 하기 위한 명령줄 인터페이스 유틸리티). `redis-cli ping` "ping"의 회신을 반환 해야 합니다.

Redis 서버 실행을 중지 하려면:`sudo service redis-server stop`

Redis database 작업에 대 한 자세한 내용은 [Redis 문서](https://redis.io/topics/quickstart)를 참조 하세요.

VS Code에서 Redis 데이터베이스를 사용 하려면 [Redis 확장](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client)을 시도 합니다.

## <a name="see-services-running-and-set-up-profile-aliases"></a>서비스 실행 중 및 프로필 별칭 설정을 참조 하세요.

WSL 배포에서 현재 실행 중인 서비스를 확인 하려면 다음을 입력 합니다.`service --status-all`

`sudo service mongodb start` 또는 `sudo service postgres start` 및 `sudo -u postgrest psql`을 입력하는 것은 지루할 수 있습니다.  그러나 WSL의 `.profile` 파일에 별칭을 설정하면 이러한 명령으로 더 빠르게 사용하고 더 쉽게 기억할 수 있습니다.

이러한 명령 실행을 위한 사용자 지정 별칭 또는 바로 가기를 설정하려면 다음을 수행합니다.

1. WSL 터미널을 열고 루트 디렉터리에 있도록 `cd ~`를 입력합니다.
2. 터미널 텍스트 편집기인 Nano를 사용하여 터미널의 설정을 제어하는 `.profile` 파일을 엽니다. `sudo nano .profile`
3. 파일의 아래쪽에서(`# set PATH` 설정을 변경하지 않음) 다음을 추가합니다.

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    이렇게 하면 `start-pg`를 입력하여 postgresql 서비스 실행을 시작하고 `run-pg`를 입력하여 psql 셸을 열 수 있습니다. `start-pg` 및 `run-pg`를 원하는 이름으로 변경할 수 있습니다. postgres가 이미 사용하는 명령을 덮어쓰지 않도록 주의하세요.

4. 새 별칭을 추가한 후에는 **Ctrl+X**를 사용하여 Nano 텍스트 편집기를 종료합니다. 저장 및 Enter에 대한 메시지가 표시되면 `Y`(예)를 선택합니다(파일 이름을 `.profile`로 그대로 둠).
5. WSL 터미널을 닫았다가 다시 연 다음, 새 별칭 명령을 시도합니다.

## <a name="additional-resources"></a>추가 자료

- [Windows 10에서 개발 환경 설정](https://docs.microsoft.com/windows/dev-environment/)
