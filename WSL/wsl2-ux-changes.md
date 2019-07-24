---
title: WSL 1과 WSL 2 간의 UX 변경 내용
description: WSL 1과 WSL 2 사이의 사용자 환경 변경
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a6c8f4fbbf21b4295e69fe3de2ecf0922ab20bbe
ms.sourcegitcommit: 6086126c35a5518a7110935fa13592b5ed9dd6b7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/15/2019
ms.locfileid: "67891781"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="8addd-104">WSL 1과 WSL 2 사이의 사용자 환경 변경</span><span class="sxs-lookup"><span data-stu-id="8addd-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="8addd-105">이 페이지에서는 WSL 1과 WSL 2 preview의 사용자 환경 차이를 모두 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="8addd-106">유의 해야 하는 주요 변경 내용은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="8addd-107">더 빠른 파일 성능 속도를 위해 linux 앱이 Linux 루트 파일 시스템에서 액세스할 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="8addd-108">WSL 2 preview의 초기 빌드에서는 localhost를 사용 하는 대신 IP 주소를 사용 하 여 네트워크 응용 프로그램에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="8addd-109">다음은 볼 수 있는 다른 변경 내용에 대 한 전체 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="8addd-110">WSL 2는 VHD ( [가상 하드웨어 디스크](https://en.wikipedia.org/wiki/VHD_(file_format)) )를 사용 하 여 파일을 저장 하 고 최대 크기에 도달 하면 확장 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="8addd-111">시작할 때 WSL 2는 이제 작은 메모리 비율을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="8addd-112">초기 미리 보기 빌드에서 OS 간 파일 액세스 속도가 느려집니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="8addd-113">Linux 루트 파일 시스템에 Linux 파일 저장</span><span class="sxs-lookup"><span data-stu-id="8addd-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="8addd-114">파일 성능 혜택을 누릴 수 있도록 Linux 루트 파일 시스템 내부의 Linux 응용 프로그램에 자주 액세스 하는 파일을 배치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="8addd-115">이러한 파일은 더 빠른 파일 시스템 액세스를 위해 Linux 루트 파일 시스템 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="8addd-116">Windows 앱이 Linux 루트 파일 시스템에 액세스할 수도 있습니다 (예: 파일 탐색기).</span><span class="sxs-lookup"><span data-stu-id="8addd-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="8addd-117">실행 시도: `explorer.exe .` Linux 배포판의 홈 디렉터리에서 수행 하는 작업을 확인 하 고이를 훨씬 쉽게 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="8addd-118">네트워크 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="8addd-118">Accessing network applications</span></span>
<span data-ttu-id="8addd-119">WSL 2 preview의 초기 빌드에서 Linux 배포판의 IP 주소와 호스트 컴퓨터의 IP 주소를 사용 하는 Linux의 모든 Windows server를 사용 하 여 Windows에서 Linux 서버에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="8addd-120">이는 일시적 이며 수정할 우선 순위 목록에 매우 높습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="8addd-121">Windows에서 Linux 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="8addd-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="8addd-122">WSL 배포판 서버를 사용 하는 경우 배포판를 켜는 가상 머신의 IP 주소를 찾아 해당 IP 주소를 사용 하 여 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="8addd-123">이렇게 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="8addd-124">Wsl 배포판 내에서 명령을 `ip addr` 실행 하 고 `eth0` 인터페이스의 `inet` 값에서 찾아 배포판의 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="8addd-125">다음과 `ip addr | grep eth0`같이 grep를 사용 하 여 명령의 출력을 필터링 하 여이를 보다 쉽게 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="8addd-126">위에서 찾은 IP를 사용 하 여 Linux 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="8addd-127">아래 그림에서는 Edge 브라우저를 사용 하 여 node.js 서버에 연결 하는 방법의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-127">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="8addd-129">Linux에서 Windows 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="8addd-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="8addd-130">Windows 네트워크 응용 프로그램에 액세스 하려면 호스트 컴퓨터의 IP 주소를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="8addd-131">이렇게 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-131">You can do so with these steps:</span></span>

- <span data-ttu-id="8addd-132">명령을 `cat /etc/resolv.conf` 실행 하 고 약관 `nameserver`에 따라 ip 주소를 복사 하 여 호스트 컴퓨터의 ip 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="8addd-133">복사한 IP 주소를 사용 하 여 Windows 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="8addd-134">아래 그림은 Windows에서 실행 되는 Windows에서 실행 되는 node.js 서버에 연결 하 여이에 대 한 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-134">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a><span data-ttu-id="8addd-136">기타 네트워킹 고려 사항</span><span class="sxs-lookup"><span data-stu-id="8addd-136">Other networking considerations</span></span>

<span data-ttu-id="8addd-137">원격 IP 주소를 사용 하 여 응용 프로그램에 연결 하는 경우 LAN (Local Area Network)의 연결로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-137">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="8addd-138">즉, 응용 프로그램에서 LAN 연결을 허용할 수 있는지 확인 해야 합니다. 예를 들면 다음과 같습니다. 대신 응용 프로그램을에 `0.0.0.0` 바인딩해야 할 수도 있습니다. `127.0.0.1`</span><span class="sxs-lookup"><span data-stu-id="8addd-138">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="8addd-139">예를 들어 flask를 사용 하는 python에서는 명령을 `app.run(host='0.0.0.0')`사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-139">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="8addd-140">이러한 변경을 수행 하는 경우 LAN 으로부터의 연결을 허용 하므로 보안을 염두에 두십시오.</span><span class="sxs-lookup"><span data-stu-id="8addd-140">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="8addd-141">WSL 2는 VHD를 사용 하 고 최대 크기에 도달 하는 경우 수행할 작업을 이해 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-141">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="8addd-142">WSL 2는 ext4 파일 시스템을 사용 하는 VHD 내에 모든 Linux 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-142">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="8addd-143">이 VHD는 저장소 요구에 맞게 자동으로 크기가 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-143">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="8addd-144">또한이 VHD의 초기 최대 크기는 256GB입니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-144">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="8addd-145">배포판 크기가 256GB 보다 큰 경우 디스크 공간이 부족 하다는 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-145">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="8addd-146">VHD 크기를 확장 하 여 이러한 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-146">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="8addd-147">이 작업을 수행 하는 방법에 대 한 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-147">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="8addd-148">`wsl --shutdown` 명령을 사용 하 여 모든 wsl 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-148">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="8addd-149">배포판 설치 패키지 이름 ' PackageFamilyName ' 찾기</span><span class="sxs-lookup"><span data-stu-id="8addd-149">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="8addd-150">Powershell 프롬프트에서 (' 배포판 '이 (가) 배포 이름인 경우)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-150">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="8addd-151">WSL 2 설치에서 사용 되는 VHD 파일 fullpath를 찾습니다 .이 파일은 ' pathToVHD '입니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-151">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="8addd-152">다음 명령을 완료 하 여 WSL 2 VHD 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-152">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="8addd-153">관리자 권한으로 명령 프롬프트 창을 열고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-153">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="8addd-154">WSL 배포판 시작</span><span class="sxs-lookup"><span data-stu-id="8addd-154">Launch your WSL distro</span></span>
6. <span data-ttu-id="8addd-155">WSL에서 파일 시스템의 크기를 확장할 수 있음을 인식 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8addd-155">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="8addd-156">WSL 배포판에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-156">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="8addd-157">이 항목의 이름을 복사 합니다. 예를 들어/Hv/sdxx (X는 다른 문자를 나타냄)와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-157">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="8addd-158">앞에서 복사한 값을 사용 하 고를 사용 `apt install resize2fs`해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-158">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="8addd-159">참고: 일반적으로 Windows 도구 또는 편집기를 사용 하 여 AppData 폴더 내에 있는 WSL 관련 파일을 수정 하거나 이동 하거나 액세스 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-159">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="8addd-160">이렇게 하면 Linux 배포판 손상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-160">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="8addd-161">WSL 2는 시작 시 일부 메모리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-161">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="8addd-162">WSL 2는 실제 Linux 커널의 경량 유틸리티 VM을 사용 하 여 뛰어난 파일 시스템 성능 및 전체 시스템 호출 호환성을 제공 하는 동시에 WSL 1로 신속 하 고 신속 하 게 통합 되 고 응답성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-162">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="8addd-163">이 유틸리티 VM에는 작은 메모리 공간이 있으며 시작 시 가상 주소 지원 메모리를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-163">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="8addd-164">총 메모리의 작은 부분으로 시작 되도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-164">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="8addd-165">초기 미리 보기 빌드에서 OS 파일 속도가 느립니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-165">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="8addd-166">Linux 응용 프로그램에서 Windows 파일에 액세스 하거나 Windows 응용 프로그램에서 Linux 파일에 액세스 하는 경우 WSL 1과 비교 하 여 파일 속도가 느려지는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-166">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="8addd-167">이는 WSL 2의 아키텍처 변경의 결과 이며, WSL 팀이이 환경을 개선할 수 있는 방법에 대해 적극적으로 조사 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8addd-167">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
