---
title: UX WSL 1 」 與 「 WSL 2 之間的變更
description: WSL 1 和 WSL 2 之間的使用者體驗變更
keywords: BashOnWindows、 bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038098"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="2ebea-104">WSL 1 和 WSL 2 之間的使用者體驗變更</span><span class="sxs-lookup"><span data-stu-id="2ebea-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="2ebea-105">此頁面會透過使用者體驗和之間的差異 WSL 1 WSL 2 預覽。</span><span class="sxs-lookup"><span data-stu-id="2ebea-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="2ebea-106">要注意的主要變更是：</span><span class="sxs-lookup"><span data-stu-id="2ebea-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="2ebea-107">放置您的 Linux 應用程式會存取 Linux 根檔案系統的效能速度檔案中的檔案</span><span class="sxs-lookup"><span data-stu-id="2ebea-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="2ebea-108">在 WSL 2 預覽的初始組建中，您將需要存取網路應用程式使用的 IP 位址與不使用 localhost</span><span class="sxs-lookup"><span data-stu-id="2ebea-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="2ebea-109">而以下是您可能會發現其他變更的完整清單：</span><span class="sxs-lookup"><span data-stu-id="2ebea-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="2ebea-110">WSL 2 使用 VHD 來儲存您的檔案，而且如果您達到其大小上限您可能需要將它展開</span><span class="sxs-lookup"><span data-stu-id="2ebea-110">WSL 2 uses a VHD to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="2ebea-111">啟動時，WSL 2 現在會使用記憶體的一小部分</span><span class="sxs-lookup"><span data-stu-id="2ebea-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="2ebea-112">跨 OS 檔案存取速度將會在初始的預覽版組建變慢</span><span class="sxs-lookup"><span data-stu-id="2ebea-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="2ebea-113">將您的 Linux 檔案放在您的 Linux 根檔案系統</span><span class="sxs-lookup"><span data-stu-id="2ebea-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="2ebea-114">請務必將您的 Linux 將經常存取的檔案放在您的 Linux 內的應用程式根目錄檔案系統，才能享有檔案效能優勢。</span><span class="sxs-lookup"><span data-stu-id="2ebea-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="2ebea-115">這些檔案一定要在 Linux 根檔案系統，以更快速的檔案系統存取。</span><span class="sxs-lookup"><span data-stu-id="2ebea-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="2ebea-116">我們也已可將 Windows 應用程式存取 Linux 根檔案系統 （例如檔案總管 中 ！</span><span class="sxs-lookup"><span data-stu-id="2ebea-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="2ebea-117">請嘗試執行：`explorer.exe /`中您 bash 殼層並查看) 這麼做會讓這項轉換更加方便。</span><span class="sxs-lookup"><span data-stu-id="2ebea-117">Try running: `explorer.exe /` in your bash shell and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="2ebea-118">存取網路的應用程式</span><span class="sxs-lookup"><span data-stu-id="2ebea-118">Accessing network applications</span></span>
<span data-ttu-id="2ebea-119">在 WSL 2 預覽的初始組建，您必須從 Windows 使用您的 Linux 散發版本，並從 Linux 使用主機電腦的 IP 位址的任何 Windows 伺服器的 IP 位址存取的任何 Linux 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2ebea-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="2ebea-120">這是暫時性的且若要修正我們的優先順序清單上非常高的項目。</span><span class="sxs-lookup"><span data-stu-id="2ebea-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="2ebea-121">從 Windows 存取 Linux 應用程式</span><span class="sxs-lookup"><span data-stu-id="2ebea-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="2ebea-122">如果您有伺服器在 WSL 散發版本，表示您要尋找加強您的散發版本的虛擬機器的 IP 位址，並使用該 IP 位址連線到它。</span><span class="sxs-lookup"><span data-stu-id="2ebea-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="2ebea-123">您可以依照下列步驟來這麼做：</span><span class="sxs-lookup"><span data-stu-id="2ebea-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="2ebea-124">執行命令來取得您的散發版本的 IP 位址`ip addr`內 WSL distro 並尋找下加以`inet`的值`eth0`介面。</span><span class="sxs-lookup"><span data-stu-id="2ebea-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="2ebea-125">您可以找到此更輕鬆地篩選使用 grep 命令的輸出如下： `ip addr | grep eth0`。</span><span class="sxs-lookup"><span data-stu-id="2ebea-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="2ebea-126">連接到您在上面找到您 Linux 伺服器使用的 IP。</span><span class="sxs-lookup"><span data-stu-id="2ebea-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="2ebea-127">下圖顯示這個範例藉由連接到使用 microsoft Edge 瀏覽器的 nodeJS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2ebea-127">The picture below shows an example of this by connecting to a nodeJS server using the Edge browser.</span></span>

![從 Windows 存取 Linux 的網路應用程式](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="2ebea-129">從 Linux 存取 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="2ebea-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="2ebea-130">若要存取 Windows 網路應用程式，您必須使用主機電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2ebea-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="2ebea-131">您可以執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2ebea-131">You can do so with these steps:</span></span>

- <span data-ttu-id="2ebea-132">執行命令來取得您的主機電腦的 IP 位址`cat /etc/resolv.conf`並複製下列詞彙的 IP 位址`nameserver`。</span><span class="sxs-lookup"><span data-stu-id="2ebea-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="2ebea-133">連線至任何使用複製的 IP 位址的 Windows 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2ebea-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="2ebea-134">下圖顯示這個範例藉由連線到透過 curl 在 Windows 中執行的 python 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2ebea-134">The picture below shows an example of this by connecting to a python server running in Windows via curl.</span></span> 

![從 Windows 存取 Linux 的網路應用程式](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="2ebea-136">了解 WSL 2 使用 VHD，而如果您達到其大小上限，該怎麼辦</span><span class="sxs-lookup"><span data-stu-id="2ebea-136">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="2ebea-137">WSL 2 會儲存您所有的 Linux 檔案內使用 ext4 檔案系統的 VHD。</span><span class="sxs-lookup"><span data-stu-id="2ebea-137">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="2ebea-138">此 VHD 自動調整大小以符合您的儲存體需求。</span><span class="sxs-lookup"><span data-stu-id="2ebea-138">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="2ebea-139">此 VHD 也具有初始大小上限為 256 GB。</span><span class="sxs-lookup"><span data-stu-id="2ebea-139">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="2ebea-140">如果您的散發版本成長的大小必須大於 256 GB，您會看到錯誤指出您已用盡磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="2ebea-140">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="2ebea-141">您可以修正這些方法是展開的 VHD 大小。</span><span class="sxs-lookup"><span data-stu-id="2ebea-141">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="2ebea-142">有關如何執行這項操作的指示如下：</span><span class="sxs-lookup"><span data-stu-id="2ebea-142">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="2ebea-143">終止所有 WSL 執行個體使用`wsl --shutdown`命令</span><span class="sxs-lookup"><span data-stu-id="2ebea-143">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="2ebea-144">完成下列命令來調整大小 WSL 2 VHD</span><span class="sxs-lookup"><span data-stu-id="2ebea-144">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="2ebea-145">以系統管理員權限開啟命令提示字元 視窗，然後執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="2ebea-145">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. <span data-ttu-id="2ebea-146">啟動您的 WSL 散發套件</span><span class="sxs-lookup"><span data-stu-id="2ebea-146">Launch your WSL distro</span></span>
4. <span data-ttu-id="2ebea-147">請注意，它可以展開其檔案系統的大小 WSL</span><span class="sxs-lookup"><span data-stu-id="2ebea-147">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="2ebea-148">在 WSL distro 中，執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="2ebea-148">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="2ebea-149">複製此項目，看起來就像的名稱: / sdXX (具有 X 表示任何其他字元)</span><span class="sxs-lookup"><span data-stu-id="2ebea-149">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="2ebea-150">請確定使用的值之前，複製，而且您可能需要使用： `apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="2ebea-150">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="2ebea-151">WSL 2 會使用一些記憶體，在啟動</span><span class="sxs-lookup"><span data-stu-id="2ebea-151">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="2ebea-152">WSL 2 會使用輕量級的公用程式 VM 上實際的 Linux 核心提供絕佳的檔案系統的效能和完整的系統呼叫仍正在執行時的相容性，就如同光線，快速、 整合和回應以 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="2ebea-152">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="2ebea-153">此公用程式 VM 會具有較小的記憶體耗用量，並將備份的虛擬位址上配置的記憶體啟動。</span><span class="sxs-lookup"><span data-stu-id="2ebea-153">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="2ebea-154">它會設定為啟動與您的總記憶體的一小部分。</span><span class="sxs-lookup"><span data-stu-id="2ebea-154">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="2ebea-155">跨作業系統檔案的速度將會在初始的預覽版組建變慢</span><span class="sxs-lookup"><span data-stu-id="2ebea-155">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="2ebea-156">您會發現檔案上的速度比 WSL 1 時從 Linux 應用程式，或從 Windows 應用程式存取 Linux 檔案存取 Windows 檔案。</span><span class="sxs-lookup"><span data-stu-id="2ebea-156">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="2ebea-157">這是在 WSL 2 的架構變更的結果，是指 WSL 小組正在調查上如何改善這項體驗。</span><span class="sxs-lookup"><span data-stu-id="2ebea-157">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>