---
title: WSL 1 및 2 WSL UX 차이점
description: WSL 1 및 2 WSL 간의 사용자 환경 변경 내용
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038103"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="ada93-104">WSL 1 및 2 WSL 간의 사용자 환경 변경 내용</span><span class="sxs-lookup"><span data-stu-id="ada93-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="ada93-105">이 페이지의 사용자 환경 차이점 WSL 1 및 WSL 2 미리 보기를 초과 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="ada93-106">알아야 할 주요 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="ada93-107">Linux 앱 파일 성능 속도 더 빠르게 Linux 루트 파일 시스템에 액세스 하는 파일 배치</span><span class="sxs-lookup"><span data-stu-id="ada93-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="ada93-108">WSL 2 미리 보기의 초기 빌드에 IP 주소를 사용 하 고 localhost를 사용 하지 않는 네트워크 응용 프로그램에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="ada93-109">및 다음은 나타날 수 있는 기타 변경의 전체 목록:</span><span class="sxs-lookup"><span data-stu-id="ada93-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="ada93-110">WSL 2 VHD를 사용 하 여 파일을 저장 하 고 확장 해야 해당 최대 크기에 도달 하면</span><span class="sxs-lookup"><span data-stu-id="ada93-110">WSL 2 uses a VHD to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="ada93-111">WSL 2는 이제 메모리의 작은 비율을 사용을 시작할 때</span><span class="sxs-lookup"><span data-stu-id="ada93-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="ada93-112">OS 간 파일 액세스 속도 느려집니다 초기 미리 보기 빌드에서</span><span class="sxs-lookup"><span data-stu-id="ada93-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="ada93-113">Linux 루트 파일 시스템에서 Linux 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="ada93-114">Linux를 사용 하 여 자주 액세스 수는 파일을 배치 해야 합니다. Linux 내부의 응용 프로그램 루트 파일 시스템 파일 성능 이점을 누리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="ada93-115">이러한 파일 내 Linux 루트 파일 시스템에 더 빠르게 파일 시스템 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="ada93-116">또한 했습니다 (예: 파일 탐색기 Linux 루트 파일 시스템에 액세스 하려면 Windows 앱!</span><span class="sxs-lookup"><span data-stu-id="ada93-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="ada93-117">실행 해 보세요: `explorer.exe /` bash 셸 및 일어나는지 볼)를 활용 하는이 전환 훨씬 수 월 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-117">Try running: `explorer.exe /` in your bash shell and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="ada93-118">네트워크 응용 프로그램에 액세스</span><span class="sxs-lookup"><span data-stu-id="ada93-118">Accessing network applications</span></span>
<span data-ttu-id="ada93-119">WSL 2 미리 보기 빌드의 초기 Linux 배포판에 및 모든 Windows server 호스트 컴퓨터의 IP 주소를 사용 하 여 Linux에서의 IP 주소를 사용 하 여 Windows에서 모든 Linux 서버에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="ada93-120">임시 및 문제를 해결 하려면 우선 순위 목록에서 매우 높은 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="ada93-121">Windows에서 Linux 응용 프로그램에 액세스</span><span class="sxs-lookup"><span data-stu-id="ada93-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="ada93-122">WSL 배포판을 서버에 있는 경우에 배포를 구동 하는 가상 컴퓨터의 IP 주소를 찾으려면 해당 IP 주소에 연결 하는 것이 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="ada93-123">다음 단계를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="ada93-124">명령을 실행 하 여 배포의 IP 주소를 가져옵니다 `ip addr` WSL 배포 및에서 찾아 내부를 `inet` 의 값을 `eth0` 인터페이스.</span><span class="sxs-lookup"><span data-stu-id="ada93-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="ada93-125">Grep를 사용 하 여 명령의 출력을 필터링 하 여이 작업을 더 쉽게 찾을 수 있습니다 같이: `ip addr | grep eth0`합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="ada93-126">위에서 찾은 IP를 사용 하 여 Linux 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="ada93-127">아래 그림은 Edge 브라우저를 사용 하는 nodeJS 서버에 연결 하 여이 예제를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-127">The picture below shows an example of this by connecting to a nodeJS server using the Edge browser.</span></span>

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="ada93-129">Linux에서 Windows 응용 프로그램에 액세스</span><span class="sxs-lookup"><span data-stu-id="ada93-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="ada93-130">Windows 네트워크 응용 프로그램에 액세스할 호스트 컴퓨터의 IP 주소를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="ada93-131">다음이 단계를 사용 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-131">You can do so with these steps:</span></span>

- <span data-ttu-id="ada93-132">명령을 실행 하 여 호스트 컴퓨터의 IP 주소를 가져옵니다 `cat /etc/resolv.conf` 용어를 다음 IP 주소를 복사 하 고 `nameserver`입니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="ada93-133">복사 된 IP 주소를 사용 하 여 모든 Windows 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="ada93-134">아래 그림은 curl을 통해 Windows에서 실행 하는 python 서버에 연결 하 여이 예제를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-134">The picture below shows an example of this by connecting to a python server running in Windows via curl.</span></span> 

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="ada93-136">VHD 및 해당 최대 크기에 도달 하면 수행할 작업을 사용 하 여 WSL 2 이해</span><span class="sxs-lookup"><span data-stu-id="ada93-136">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="ada93-137">WSL 2 ext4 파일 시스템을 사용 하는 VHD 내의 모든 Linux 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-137">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="ada93-138">이 VHD는 저장소 요구 사항에 맞게 자동으로 크기가 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-138">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="ada93-139">이 VHD의 초기 최대 크기는 256GB 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-139">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="ada93-140">크기가 256GB를 초과할 수 증가 함에 따라 배포 하는 경우 디스크 공간이 부족 실행 한 것을 알리는 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-140">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="ada93-141">VHD 크기를 확장 하 여이 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-141">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="ada93-142">이렇게 하는 방법에 대 한 지침은 아래와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-142">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="ada93-143">사용 하 여 모든 WSL 인스턴스 종료는 `wsl --shutdown` 명령</span><span class="sxs-lookup"><span data-stu-id="ada93-143">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="ada93-144">다음 명령을 완료 하 여 WSL 2 VHD를 크기 조정</span><span class="sxs-lookup"><span data-stu-id="ada93-144">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="ada93-145">관리자 권한으로 명령 프롬프트 창을 열고 다음 명령을 실행:</span><span class="sxs-lookup"><span data-stu-id="ada93-145">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. <span data-ttu-id="ada93-146">WSL 배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-146">Launch your WSL distro</span></span>
4. <span data-ttu-id="ada93-147">해당 파일 시스템의 크기를 확장할 수 있는 인식 WSL 확인</span><span class="sxs-lookup"><span data-stu-id="ada93-147">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="ada93-148">WSL 배포에서 이러한 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-148">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="ada93-149">와이 항목의 이름을 복사 합니다. / sdXX (X가 있는 다른 모든 문자를 나타내는)</span><span class="sxs-lookup"><span data-stu-id="ada93-149">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="ada93-150">값을 사용 하 여 앞에서 복사한 및 사용 해야 하는지 확인: `apt install resize2fs`합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-150">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="ada93-151">WSL 2는 시작 시 일부 메모리를 사용 하는</span><span class="sxs-lookup"><span data-stu-id="ada93-151">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="ada93-152">WSL 2에서 사용 하 여 간단한 유틸리티 VM 실제 Linux 커널을 뛰어난 파일 시스템 성능 및 전체 시스템 호출 신호등에서와 마찬가지로 계속 되는 동안 호환성 빠르고 통합 및 WSL 1로 응답을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-152">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="ada93-153">VM이이 유틸리티는 작은 메모리 공간이 하 고 시작 시 메모리 지원 가상 주소를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-153">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="ada93-154">총 메모리의 작은 비율을 시작 하도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-154">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="ada93-155">OS 간 파일 속도 느려집니다 초기 미리 보기 빌드에서</span><span class="sxs-lookup"><span data-stu-id="ada93-155">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="ada93-156">Windows 응용 프로그램에서 Linux 파일을 액세스 하거나 Linux 응용 프로그램을 Windows 파일에 액세스할 때 WSL 1에 비해 속도가 파일을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-156">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="ada93-157">WSL 2 아키텍처 변경의 결과 이며 WSL 팀이 적극적으로 하는 것이 환경을 개선할 방법에 대 한 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada93-157">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>