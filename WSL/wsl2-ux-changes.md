---
title: WSL 1 和 WSL 2 之間的 UX 變更
description: WSL 1 與 WSL 2 之間的使用者體驗變更
keywords: BashOnWindows, bash, wsl, wsl2, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a6c8f4fbbf21b4295e69fe3de2ecf0922ab20bbe
ms.sourcegitcommit: 6086126c35a5518a7110935fa13592b5ed9dd6b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/15/2019
ms.locfileid: "67891780"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="3b973-104">WSL 1 與 WSL 2 之間的使用者體驗變更</span><span class="sxs-lookup"><span data-stu-id="3b973-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="3b973-105">此頁面會超越 WSL 1 與 WSL 2 preview 之間的使用者體驗差異。</span><span class="sxs-lookup"><span data-stu-id="3b973-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="3b973-106">要注意的關鍵變更如下:</span><span class="sxs-lookup"><span data-stu-id="3b973-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="3b973-107">將您的 Linux 應用程式將在 Linux 根檔案系統中存取的檔案放在一起, 以加快檔案效能速度</span><span class="sxs-lookup"><span data-stu-id="3b973-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="3b973-108">在 WSL 2 preview 的初始組建中, 您將需要使用 IP 位址存取網路應用程式, 而不使用 localhost</span><span class="sxs-lookup"><span data-stu-id="3b973-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="3b973-109">以下是您可能會注意到的其他變更的完整清單:</span><span class="sxs-lookup"><span data-stu-id="3b973-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="3b973-110">WSL 2 使用[虛擬硬體磁片](https://en.wikipedia.org/wiki/VHD_(file_format))(VHD) 來儲存您的檔案, 如果您達到其大小上限, 您可能需要將它展開</span><span class="sxs-lookup"><span data-stu-id="3b973-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="3b973-111">啟動時, WSL 2 現在會使用一小部分的記憶體</span><span class="sxs-lookup"><span data-stu-id="3b973-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="3b973-112">初次預覽組建中的跨 OS 檔案存取速度會變慢</span><span class="sxs-lookup"><span data-stu-id="3b973-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="3b973-113">將您的 Linux 檔案放在 Linux 根檔案系統中</span><span class="sxs-lookup"><span data-stu-id="3b973-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="3b973-114">請務必將您將經常存取的檔案, 放在 Linux 根檔案系統內的 Linux 應用程式, 以享有檔案效能優勢。</span><span class="sxs-lookup"><span data-stu-id="3b973-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="3b973-115">這些檔案必須位於 Linux 根檔案系統內, 才能加快檔案系統存取的速度。</span><span class="sxs-lookup"><span data-stu-id="3b973-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="3b973-116">我們也可以讓 Windows 應用程式存取 Linux 根檔案系統 (例如 File Explorer!</span><span class="sxs-lookup"><span data-stu-id="3b973-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="3b973-117">請嘗試執行`explorer.exe .` : 在 Linux 散發版本的主目錄中, 並查看發生什麼事), 這將會大幅簡化此轉換。</span><span class="sxs-lookup"><span data-stu-id="3b973-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="3b973-118">存取網路應用程式</span><span class="sxs-lookup"><span data-stu-id="3b973-118">Accessing network applications</span></span>
<span data-ttu-id="3b973-119">在 WSL 2 preview 的初始組建中, 您必須使用您的 Linux 散發版本的 IP 位址, 以及使用您主機電腦 IP 位址的 Linux 中的任何 Windows 伺服器, 從 Windows 存取任何 Linux 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3b973-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="3b973-120">這是暫時性的專案, 而且在我們的優先順序清單上會非常高, 以修正此問題。</span><span class="sxs-lookup"><span data-stu-id="3b973-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="3b973-121">從 Windows 存取 Linux 應用程式</span><span class="sxs-lookup"><span data-stu-id="3b973-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="3b973-122">如果您在 WSL 散發版本中有一部伺服器, 您將需要尋找虛擬機器的 IP 位址, 並使用該 IP 位址來連線到您的散發版本。</span><span class="sxs-lookup"><span data-stu-id="3b973-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="3b973-123">您可以遵循下列步驟來執行此動作:</span><span class="sxs-lookup"><span data-stu-id="3b973-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="3b973-124">在您的 WSL 散發版本內執行命令`ip addr` , 並在`eth0`介面的`inet`值底下尋找, 以取得散發版本的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b973-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="3b973-125">使用 grep 篩選命令的輸出 (如下所示), 可以更輕鬆地找到此`ip addr | grep eth0`程式:。</span><span class="sxs-lookup"><span data-stu-id="3b973-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="3b973-126">使用您在上面找到的 IP 連接到 Linux 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3b973-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="3b973-127">下圖顯示使用 Edge 瀏覽器連接到 node.js 伺服器的範例。</span><span class="sxs-lookup"><span data-stu-id="3b973-127">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![從 Windows 存取 Linux 網路應用程式](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="3b973-129">從 Linux 存取 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="3b973-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="3b973-130">若要存取 Windows 網路應用程式, 您必須使用主機電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b973-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="3b973-131">您可以使用下列步驟來執行此動作:</span><span class="sxs-lookup"><span data-stu-id="3b973-131">You can do so with these steps:</span></span>

- <span data-ttu-id="3b973-132">執行命令`cat /etc/resolv.conf`並複製該字詞`nameserver`之後的 ip 位址, 以取得主機電腦的 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="3b973-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="3b973-133">使用複製的 IP 位址連接到任何 Windows 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3b973-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="3b973-134">下圖顯示這種情況的範例, 其方式是連接到在 Windows 中執行的 node.js 伺服器 (透過捲曲)。</span><span class="sxs-lookup"><span data-stu-id="3b973-134">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![從 Windows 存取 Linux 網路應用程式](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a><span data-ttu-id="3b973-136">其他網路功能考慮</span><span class="sxs-lookup"><span data-stu-id="3b973-136">Other networking considerations</span></span>

<span data-ttu-id="3b973-137">使用遠端 IP 位址連線到您的應用程式時, 系統會將其視為來自區域網路 (LAN) 的連線。</span><span class="sxs-lookup"><span data-stu-id="3b973-137">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="3b973-138">這表示您必須確定您的應用程式可以接受 LAN 連線, 也就是:您可能需要將您的`0.0.0.0` `127.0.0.1`應用程式系結至, 而不是。</span><span class="sxs-lookup"><span data-stu-id="3b973-138">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="3b973-139">例如, 在使用 flask 的 python 中, 可以使用下列命令來`app.run(host='0.0.0.0')`完成此作業:。</span><span class="sxs-lookup"><span data-stu-id="3b973-139">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="3b973-140">在進行這些變更時, 請記住安全性, 因為這會允許來自您 LAN 的連接。</span><span class="sxs-lookup"><span data-stu-id="3b973-140">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="3b973-141">瞭解 WSL 2 會使用 VHD, 以及當您達到其大小上限時該怎麼辦</span><span class="sxs-lookup"><span data-stu-id="3b973-141">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="3b973-142">WSL 2 會將您所有的 Linux 檔案儲存在使用 ext4 檔案系統的 VHD 內。</span><span class="sxs-lookup"><span data-stu-id="3b973-142">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="3b973-143">此 VHD 會自動調整大小以符合您的儲存需求。</span><span class="sxs-lookup"><span data-stu-id="3b973-143">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="3b973-144">此 VHD 也具有256GB 的初始大小上限。</span><span class="sxs-lookup"><span data-stu-id="3b973-144">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="3b973-145">如果您的散發版本大小成長得大於 256GB, 您將會看到錯誤, 指出您已用盡磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="3b973-145">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="3b973-146">您可以藉由擴充 VHD 大小來修正這些問題。</span><span class="sxs-lookup"><span data-stu-id="3b973-146">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="3b973-147">有關如何執行此動作的指示如下:</span><span class="sxs-lookup"><span data-stu-id="3b973-147">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="3b973-148">使用`wsl --shutdown`命令終止所有 WSL 實例</span><span class="sxs-lookup"><span data-stu-id="3b973-148">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="3b973-149">尋找您的散發版本安裝套件名稱 ' PackageFamilyName '</span><span class="sxs-lookup"><span data-stu-id="3b973-149">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="3b973-150">在 powershell 提示字元中 (其中 ' 散發版本 ' 是您的發佈名稱), 請輸入:</span><span class="sxs-lookup"><span data-stu-id="3b973-150">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="3b973-151">找出 WSL 2 安裝所使用的 VHD 檔案 fullpath, 這會是您的 ' pathToVHD ':</span><span class="sxs-lookup"><span data-stu-id="3b973-151">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="3b973-152">完成下列命令以調整您的 WSL 2 VHD 大小</span><span class="sxs-lookup"><span data-stu-id="3b973-152">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="3b973-153">以系統管理員許可權開啟 [命令提示字元] 視窗, 然後執行下列命令:</span><span class="sxs-lookup"><span data-stu-id="3b973-153">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="3b973-154">啟動您的 WSL 散發版本</span><span class="sxs-lookup"><span data-stu-id="3b973-154">Launch your WSL distro</span></span>
6. <span data-ttu-id="3b973-155">讓 WSL 知道它可以擴充其檔案系統的大小</span><span class="sxs-lookup"><span data-stu-id="3b973-155">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="3b973-156">在您的 WSL 散發版本中執行下列命令:</span><span class="sxs-lookup"><span data-stu-id="3b973-156">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="3b973-157">複製此專案的名稱, 如下所示:/dev/sdXX (X 代表任何其他字元)</span><span class="sxs-lookup"><span data-stu-id="3b973-157">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="3b973-158">請務必使用您稍早複製的值, 您可能需要使用: `apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="3b973-158">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="3b973-159">請注意：一般來說, 請不要使用 Windows 工具或編輯器修改、移動或存取位於 AppData 資料夾內的 WSL 相關檔案。</span><span class="sxs-lookup"><span data-stu-id="3b973-159">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="3b973-160">這麼做可能會導致您的 Linux 散發版本損毀。</span><span class="sxs-lookup"><span data-stu-id="3b973-160">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="3b973-161">WSL 2 會在啟動時使用一些記憶體</span><span class="sxs-lookup"><span data-stu-id="3b973-161">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="3b973-162">WSL 2 會在實際的 Linux 核心上使用輕量公用程式 VM, 以提供絕佳的檔案系統效能和完整的系統呼叫相容性, 同時仍能以 WSL 1 的速度快速、整合和回應。</span><span class="sxs-lookup"><span data-stu-id="3b973-162">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="3b973-163">此公用程式 VM 具有小型的記憶體使用量, 並會在啟動時配置虛擬位址支援的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3b973-163">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="3b973-164">它會設定為從您總記憶體的一小部分開始。</span><span class="sxs-lookup"><span data-stu-id="3b973-164">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="3b973-165">初次預覽組建中的跨 OS 檔案速度會較慢</span><span class="sxs-lookup"><span data-stu-id="3b973-165">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="3b973-166">從 Linux 應用程式存取 Windows 檔案, 或從 Windows 應用程式存取 Linux 檔案時, 您會發現相較于 WSL 1 的檔案速度比較慢。</span><span class="sxs-lookup"><span data-stu-id="3b973-166">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="3b973-167">這是 WSL 2 中架構變更的結果, 而 WSL 小組會主動調查如何改善這項體驗。</span><span class="sxs-lookup"><span data-stu-id="3b973-167">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
