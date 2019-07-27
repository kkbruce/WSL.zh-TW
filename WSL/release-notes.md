---
title: 適用于 Linux 的 Windows 子系統版本資訊
description: 適用于 Linux 的 Windows 子系統版本資訊。  每週更新。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: c262ddb359507c1654f0089050bfd15ec16402f9
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523788"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="b3d62-105">適用于 Linux 的 Windows 子系統版本資訊</span><span class="sxs-lookup"><span data-stu-id="b3d62-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18945"></a><span data-ttu-id="b3d62-106">組建18945</span><span class="sxs-lookup"><span data-stu-id="b3d62-106">Build 18945</span></span>
<span data-ttu-id="b3d62-107">如需組建18945的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-107">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-108">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-108">WSL</span></span>
* <span data-ttu-id="b3d62-109">[WSL2]允許使用 localhost: port 從主機存取 WSL2 中的接聽 tcp 通訊端</span><span class="sxs-lookup"><span data-stu-id="b3d62-109">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="b3d62-110">[WSL2]修正安裝/轉換失敗和其他診斷以追蹤未來問題 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="b3d62-110">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="b3d62-111">[WSL2]改善 WSL2 網路問題的診斷</span><span class="sxs-lookup"><span data-stu-id="b3d62-111">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="b3d62-112">[WSL2]將核心版本更新為4.19.55</span><span class="sxs-lookup"><span data-stu-id="b3d62-112">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="b3d62-113">[WSL2]使用 docker 所需的設定選項更新核心 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="b3d62-113">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="b3d62-114">[WSL2]增加指派給輕量公用程式 VM 的 Cpu 數目, 使其與主機相同 (之前在核心設定中 CONFIG_NR_CPUS 的上限為 8) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="b3d62-114">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="b3d62-115">[WSL2]建立 WSL2 輕量 VM 的交換檔</span><span class="sxs-lookup"><span data-stu-id="b3d62-115">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="b3d62-116">[WSL2]允許透過\\ \\wsl $\\散發版本顯示使用者裝載 (例如 sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="b3d62-116">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="b3d62-117">[WSL2]改善9p 檔案系統效能</span><span class="sxs-lookup"><span data-stu-id="b3d62-117">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="b3d62-118">[WSL2]確保 vhd ACL 沒有無限成長 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="b3d62-118">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="b3d62-119">[WSL2]更新核心設定以支援 squashfs 和 xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="b3d62-119">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="b3d62-120">[WSL2]修正 interop. enabled/etc/wsl.conf 選項 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="b3d62-120">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="b3d62-121">[WSL2]如果檔案系統不支援 EAs, 則傳回 ENOTSUP</span><span class="sxs-lookup"><span data-stu-id="b3d62-121">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="b3d62-122">[WSL2]修正具有 wsl $ \\的\\CopyFile 停止回應</span><span class="sxs-lookup"><span data-stu-id="b3d62-122">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="b3d62-123">將預設 umask 切換至 0022, 並將 filesystem. umask 設定新增至/etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="b3d62-123">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="b3d62-124">修正 wslpath 以適當地解決符號連結, 這是回歸在 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="b3d62-124">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="b3d62-125">引進% UserProfile%\.wslconfig 檔案以調整 WSL2 設定</span><span class="sxs-lookup"><span data-stu-id="b3d62-125">Introduce %UserProfile%\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="b3d62-126">組建18917</span><span class="sxs-lookup"><span data-stu-id="b3d62-126">Build 18917</span></span>
<span data-ttu-id="b3d62-127">如需組建18917的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-127">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-128">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-128">WSL</span></span>
* <span data-ttu-id="b3d62-129">WSL 2 現已推出!</span><span class="sxs-lookup"><span data-stu-id="b3d62-129">WSL 2 is now available!</span></span> <span data-ttu-id="b3d62-130">如需詳細資訊, 請參閱[blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) 。</span><span class="sxs-lookup"><span data-stu-id="b3d62-130">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="b3d62-131">修正透過符號連結啟動 Windows 進程的回歸無法正常運作 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="b3d62-131">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="b3d62-132">將 wsl--list--verbose、wsl--list--quiet 和 wsl--import--version 選項新增至 wsl</span><span class="sxs-lookup"><span data-stu-id="b3d62-132">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="b3d62-133">新增 wsl--shutdown 選項</span><span class="sxs-lookup"><span data-stu-id="b3d62-133">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="b3d62-134">方案 9:允許開啟目錄以供寫入成功</span><span class="sxs-lookup"><span data-stu-id="b3d62-134">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="b3d62-135">組建18890</span><span class="sxs-lookup"><span data-stu-id="b3d62-135">Build 18890</span></span>
<span data-ttu-id="b3d62-136">如需組建18890的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-136">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-137">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-137">WSL</span></span>
* <span data-ttu-id="b3d62-138">非封鎖通訊端洩漏 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="b3d62-138">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="b3d62-139">對終端機的 EOF 輸入可以封鎖後續讀取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="b3d62-139">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="b3d62-140">更新 resolv.conf 的標頭以參考 wsl [在 GH 3928 中討論]</span><span class="sxs-lookup"><span data-stu-id="b3d62-140">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="b3d62-141">Epoll 刪除程式碼中的鎖死 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="b3d62-141">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="b3d62-142">處理引數中的空格--import 和– export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="b3d62-142">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="b3d62-143">擴充 mmap 的檔案無法正常運作 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="b3d62-143">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="b3d62-144">修正 ARM64 \\wsl $ access 無法正常運作的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-144">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="b3d62-145">為 wsl 新增更好的預設圖示</span><span class="sxs-lookup"><span data-stu-id="b3d62-145">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="b3d62-146">組建18342</span><span class="sxs-lookup"><span data-stu-id="b3d62-146">Build 18342</span></span>
<span data-ttu-id="b3d62-147">如需組建18342的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-147">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-148">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-148">WSL</span></span>
* <span data-ttu-id="b3d62-149">我們新增了一項功能, 讓使用者從 Windows 存取 WSL 散發版本中的 Linux 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-149">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="b3d62-150">這些檔案可透過命令列存取, 而 Windows 應用程式 (例如檔案瀏覽器、VSCode 等) 則可以與這些檔案互動。</span><span class="sxs-lookup"><span data-stu-id="b3d62-150">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="b3d62-151">流覽至 wsl \\$ \\ \\ \\< distro_name > 以存取您的檔案, 或流覽至\\wsl $ 來查看執行中的發行版本清單</span><span class="sxs-lookup"><span data-stu-id="b3d62-151">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="b3d62-152">新增額外的 CPU 資訊標記並修正 Cpus_allowed [_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="b3d62-152">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="b3d62-153">從非領導者執行緒支援 exec [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="b3d62-153">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="b3d62-154">將設定更新失敗視為非嚴重的 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="b3d62-154">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="b3d62-155">更新 binfmt 以適當地處理位移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="b3d62-155">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="b3d62-156">啟用對應規劃9的網路磁碟機 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="b3d62-156">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="b3d62-157">支援 Windows > Linux 和 Linux > 適用于系結裝載的 Windows 路徑轉譯</span><span class="sxs-lookup"><span data-stu-id="b3d62-157">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="b3d62-158">在以唯讀狀態開啟的檔案上建立對應的唯讀區段</span><span class="sxs-lookup"><span data-stu-id="b3d62-158">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="b3d62-159">組建18334</span><span class="sxs-lookup"><span data-stu-id="b3d62-159">Build 18334</span></span>
<span data-ttu-id="b3d62-160">如需組建18334的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-160">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-161">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-161">WSL</span></span>
* <span data-ttu-id="b3d62-162">重新設計 Windows 時區對應到 Linux 時區的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="b3d62-162">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="b3d62-163">修正記憶體流失並加入新的字串轉譯函數 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="b3d62-163">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="b3d62-164">不含執行緒的 threadgroup 上的 SIGCONT 不是「GH 3741」</span><span class="sxs-lookup"><span data-stu-id="b3d62-164">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="b3d62-165">在/proc/self/fd 中正確顯示通訊端和 epoll 檔案描述項</span><span class="sxs-lookup"><span data-stu-id="b3d62-165">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="b3d62-166">組建18305</span><span class="sxs-lookup"><span data-stu-id="b3d62-166">Build 18305</span></span>
<span data-ttu-id="b3d62-167">如需組建18305的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-167">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-168">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-168">WSL</span></span>
* <span data-ttu-id="b3d62-169">pthreads 在主要執行緒結束時遺失檔案的存取權 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="b3d62-169">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="b3d62-170">TIOCSCTTY 應該忽略 "force" 參數, 除非它是必要的 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="b3d62-170">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="b3d62-171">wsl 的命令列改進和匯入/匯出功能的新增。</span><span class="sxs-lookup"><span data-stu-id="b3d62-171">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="b3d62-172">組建18277</span><span class="sxs-lookup"><span data-stu-id="b3d62-172">Build 18277</span></span>
<span data-ttu-id="b3d62-173">如需組建18277的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-173">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-174">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-174">WSL</span></span>
* <span data-ttu-id="b3d62-175">修正組建18272中引進的「不支援這類介面」錯誤 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="b3d62-175">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="b3d62-176">忽略 umount syscall 的 MNT_FORCE 旗標 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="b3d62-176">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="b3d62-177">切換 WSL interop 以使用官方 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="b3d62-177">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="b3d62-178">FUTEX_WAIT 重新開機時維持無超時值</span><span class="sxs-lookup"><span data-stu-id="b3d62-178">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="b3d62-179">組建18272</span><span class="sxs-lookup"><span data-stu-id="b3d62-179">Build 18272</span></span>
<span data-ttu-id="b3d62-180">如需組建18272的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-180">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-181">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-181">WSL</span></span>
* <span data-ttu-id="b3d62-182">**WARNING**此組建中的問題導致 WSL 無法運作。</span><span class="sxs-lookup"><span data-stu-id="b3d62-182">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="b3d62-183">嘗試啟動您的散發套件時, 您會看到「不支援這種介面」錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3d62-183">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="b3d62-184">已修正此問題, 並將于下一周的 Insider 快速組建中提供。</span><span class="sxs-lookup"><span data-stu-id="b3d62-184">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="b3d62-185">如果您已安裝此組建, 您可以使用 [設定] 中的 [回到先前的 Windows 10 版本] 復原到先前的 Windows 組建, > 更新 & 安全性 > 復原。</span><span class="sxs-lookup"><span data-stu-id="b3d62-185">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="b3d62-186">組建18267</span><span class="sxs-lookup"><span data-stu-id="b3d62-186">Build 18267</span></span>
<span data-ttu-id="b3d62-187">如需組建18267的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-187">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-188">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-188">WSL</span></span>
* <span data-ttu-id="b3d62-189">修正無法 reaped 或無限期地維持廢止進程的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-189">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="b3d62-190">如果錯誤訊息超過最大長度 [GH 3592], WslRegisterDistribution 就會停止回應</span><span class="sxs-lookup"><span data-stu-id="b3d62-190">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="b3d62-191">允許 fsync 在 DrvFs 上成功執行唯讀檔案 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="b3d62-191">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="b3d62-192">在 [GH 3584] 內建立符號連結之前, 請先確認/bin 和/sbin 目錄是否存在</span><span class="sxs-lookup"><span data-stu-id="b3d62-192">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="b3d62-193">已新增 WSL 實例的實例終止超時機制。</span><span class="sxs-lookup"><span data-stu-id="b3d62-193">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="b3d62-194">Timeout 目前設定為15秒, 表示實例會在最後一個 WSL 進程結束後的15秒後終止。</span><span class="sxs-lookup"><span data-stu-id="b3d62-194">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="b3d62-195">若要立即終止散發, 請使用:</span><span class="sxs-lookup"><span data-stu-id="b3d62-195">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="b3d62-196">組建 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="b3d62-196">Build 17763 (1809)</span></span>
<span data-ttu-id="b3d62-197">如需組建17763的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-197">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-198">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-198">WSL</span></span>
* <span data-ttu-id="b3d62-199">Setpriority syscall 許可權檢查太嚴格, 無法變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b3d62-199">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b3d62-200">確保開機時間使用非偏誤停機時間, 以避免傳回 clock_gettime (CLOCK_BOOTTIME) [GH 3434] 的負值</span><span class="sxs-lookup"><span data-stu-id="b3d62-200">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b3d62-201">在 WSL binfmt 解譯器中處理符號連結 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b3d62-201">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b3d62-202">較佳的 threadgroup 領導者檔案描述項清除處理。</span><span class="sxs-lookup"><span data-stu-id="b3d62-202">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="b3d62-203">將 WSL 切換為使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter, 以避免溢位 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b3d62-203">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b3d62-204">Ptrace attach 可能會造成系統呼叫的錯誤傳回值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b3d62-204">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b3d62-205">修正數個 AF_UNIX 相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b3d62-205">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b3d62-206">修正當目前的工作目錄長度少於5個字元時, 可能導致 WSL interop 失敗的問題 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b3d62-206">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="b3d62-207">避免一秒延遲失敗的回送連線到不存在的埠 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b3d62-207">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b3d62-208">新增/proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b3d62-208">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b3d62-209">更精確的 IPV6 領域資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d62-209">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b3d62-210">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b3d62-210">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b3d62-211">管道檔案系統不小心清除邊緣觸發的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b3d62-211">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3d62-212">透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b3d62-212">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="b3d62-213">改良的僵支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b3d62-213">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b3d62-214">新增用於控制 Windows interop 行為的 wsl 專案 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b3d62-214">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b3d62-215">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b3d62-215">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b3d62-216">新增對 TIOCSTI 的支援 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b3d62-216">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b3d62-217">連接過程中的非封鎖通訊端應該會傳回 EAGAIN 進行寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b3d62-217">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b3d62-218">支援掛接的 Vhd 上的 interop [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="b3d62-218">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b3d62-219">修正根資料夾 [GH 3304] 的許可權檢查問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-219">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b3d62-220">對 TTY 鍵盤 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的支援有限。</span><span class="sxs-lookup"><span data-stu-id="b3d62-220">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b3d62-221">即使是在背景中啟動, Windows UI 應用程式也應該執行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-221">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="b3d62-222">新增 wsl-u 或--user 選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b3d62-222">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b3d62-223">修正啟用快速啟動時的 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b3d62-223">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b3d62-224">Unix 通訊端需要保留中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b3d62-224">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b3d62-225">非封鎖的 Unix 通訊端使用 EAGAIN 無限期失敗 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b3d62-225">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b3d62-226">case = off 是新的預設 drvfs 掛接類型 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="b3d62-226">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b3d62-227">如需詳細資訊, 請參閱[blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 。</span><span class="sxs-lookup"><span data-stu-id="b3d62-227">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b3d62-228">新增 wslconfig/terminate 以停止執行散發套件。</span><span class="sxs-lookup"><span data-stu-id="b3d62-228">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="b3d62-229">修正未正確處理具有空格之路徑的 WSL shell 內容功能表項目問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-229">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b3d62-230">以擴充屬性的形式公開每個目錄的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b3d62-230">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b3d62-231">ARM64模擬快取維護作業。</span><span class="sxs-lookup"><span data-stu-id="b3d62-231">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b3d62-232">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-232">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b3d62-233">DrvFs: 僅 unescape 與逸出字元對應之私用範圍中的字元。</span><span class="sxs-lookup"><span data-stu-id="b3d62-233">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="b3d62-234">修正 ELF parser 解譯器長度驗證中的逐一錯誤 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b3d62-234">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b3d62-235">WSL 過去時間的絕對計時器不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b3d62-235">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b3d62-236">確保新建立的重新分析點在上層目錄中列為。</span><span class="sxs-lookup"><span data-stu-id="b3d62-236">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b3d62-237">以原子方式在 DrvFs 中建立區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="b3d62-237">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="b3d62-238">已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的其他問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-238">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3d62-239">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3d62-239">[GH 2712]</span></span>
* <span data-ttu-id="b3d62-240">已修正啟用 UMCI 時的 WSL 啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="b3d62-240">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b3d62-241">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b3d62-241">[GH 3020]</span></span>
* <span data-ttu-id="b3d62-242">[新增 explorer] 操作功能表以啟動 WSL [GH 437, 603, 1836]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-242">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b3d62-243">若要使用, 請按住 shift 鍵, 並在 explorer 視窗中按一下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="b3d62-243">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b3d62-244">修正 Unix 通訊端未封鎖的行為 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="b3d62-244">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b3d62-245">修正 GH 2026 中所報告的懸掛 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="b3d62-245">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b3d62-246">新增對掛接傳播旗標的支援 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-246">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b3d62-247">修正不會造成 inotifypropertychanged 事件的截斷問題 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-247">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b3d62-248">Add--wsl 的 exec 選項, 可在不使用 shell 的情況下叫用單一二進位檔。</span><span class="sxs-lookup"><span data-stu-id="b3d62-248">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b3d62-249">新增--wsl 的散發選項, 以選取特定的散發版本。</span><span class="sxs-lookup"><span data-stu-id="b3d62-249">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="b3d62-250">有限的 dmesg 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-250">Limited support for dmesg.</span></span> <span data-ttu-id="b3d62-251">應用程式現在可以登入 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-251">Applications can now log to dmesg.</span></span> <span data-ttu-id="b3d62-252">WSL 驅動程式會將有限的資訊記錄到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-252">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b3d62-253">未來, 您可以擴充此功能, 以從驅動程式中攜帶其他資訊/診斷。</span><span class="sxs-lookup"><span data-stu-id="b3d62-253">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b3d62-254">注意: 目前透過`/dev/kmsg`裝置介面支援 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-254">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b3d62-255">`syslog`尚不支援 syscall 介面。</span><span class="sxs-lookup"><span data-stu-id="b3d62-255">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="b3d62-256">因此, 某些`dmesg`命令列選項`-S`(例如) `-C`無法使用。</span><span class="sxs-lookup"><span data-stu-id="b3d62-256">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b3d62-257">變更序列裝置的預設 gid 和模式以符合原生 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b3d62-257">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b3d62-258">DrvFs 現在支援擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d62-258">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b3d62-259">注意:DrvFs 在擴充屬性的名稱上有一些限制。</span><span class="sxs-lookup"><span data-stu-id="b3d62-259">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b3d62-260">不允許某些字元 (例如 '/'、': '\*和 ' '), 而且擴充屬性名稱在 DrvFs 上不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b3d62-260">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="b3d62-261">組建 18252 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-261">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-262">如需組建18252的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-262">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-263">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-263">WSL</span></span>
* <span data-ttu-id="b3d62-264">將 init 和 bsdtar 二進位檔從 lxssmanager dll 移到另一個工具資料夾</span><span class="sxs-lookup"><span data-stu-id="b3d62-264">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="b3d62-265">修正使用 CLONE_FILES 時有關關閉檔案描述項的競爭</span><span class="sxs-lookup"><span data-stu-id="b3d62-265">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="b3d62-266">轉換 DrvFs 路徑時, 處理/proc/pid/mountinfo 中的選擇性欄位</span><span class="sxs-lookup"><span data-stu-id="b3d62-266">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="b3d62-267">允許 DrvFs mknod 成功, 但不支援 S_IFREG 的中繼資料</span><span class="sxs-lookup"><span data-stu-id="b3d62-267">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="b3d62-268">在 DrvFs 上建立的 readonly 檔案應具有 readonly 屬性集 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="b3d62-268">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="b3d62-269">新增/sbin/mount.drvfs helper 以處理 DrvFs 裝載</span><span class="sxs-lookup"><span data-stu-id="b3d62-269">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="b3d62-270">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="b3d62-270">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="b3d62-271">允許磁片區上沒有磁片區 GUID 的路徑轉譯。</span><span class="sxs-lookup"><span data-stu-id="b3d62-271">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="b3d62-272">組建 17738 (快速)</span><span class="sxs-lookup"><span data-stu-id="b3d62-272">Build 17738 (Fast)</span></span>
<span data-ttu-id="b3d62-273">如需組建17738的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-273">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-274">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-274">WSL</span></span>
* <span data-ttu-id="b3d62-275">Setpriority syscall 許可權檢查太嚴格, 無法變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b3d62-275">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b3d62-276">確保開機時間使用非偏誤停機時間, 以避免傳回 clock_gettime (CLOCK_BOOTTIME) [GH 3434] 的負值</span><span class="sxs-lookup"><span data-stu-id="b3d62-276">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b3d62-277">在 WSL binfmt 解譯器中處理符號連結 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b3d62-277">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b3d62-278">較佳的 threadgroup 領導者檔案描述項清除處理。</span><span class="sxs-lookup"><span data-stu-id="b3d62-278">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="b3d62-279">組建 17728 (快速)</span><span class="sxs-lookup"><span data-stu-id="b3d62-279">Build 17728 (Fast)</span></span>
<span data-ttu-id="b3d62-280">如需組建17728的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-280">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-281">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-281">WSL</span></span>
* <span data-ttu-id="b3d62-282">將 WSL 切換為使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter, 以避免溢位 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b3d62-282">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b3d62-283">Ptrace attach 可能會造成系統呼叫的錯誤傳回值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b3d62-283">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b3d62-284">修正一些 AF_UNIX 相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b3d62-284">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b3d62-285">修正當目前的工作目錄長度少於5個字元時, 可能導致 WSL interop 失敗的問題 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b3d62-285">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="b3d62-286">組建 18204 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-286">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-287">如需組建18204的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-287">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-288">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-288">WSL</span></span>
* <span data-ttu-id="b3d62-289">管道檔案系統 inadvertenly 清除邊緣觸發的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b3d62-289">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3d62-290">透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b3d62-290">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="b3d62-291">組建 17723 (快速)</span><span class="sxs-lookup"><span data-stu-id="b3d62-291">Build 17723 (Fast)</span></span>
<span data-ttu-id="b3d62-292">如需組建17723的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-292">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-293">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-293">WSL</span></span>
* <span data-ttu-id="b3d62-294">避免一秒延遲失敗的回送連線到不存在的埠 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b3d62-294">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b3d62-295">新增/proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b3d62-295">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b3d62-296">更精確的 IPV6 領域資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d62-296">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b3d62-297">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b3d62-297">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b3d62-298">管道檔案系統 inadvertenly 清除邊緣觸發的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b3d62-298">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3d62-299">透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b3d62-299">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="b3d62-300">組建17713</span><span class="sxs-lookup"><span data-stu-id="b3d62-300">Build 17713</span></span>
<span data-ttu-id="b3d62-301">如需組建17713的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-301">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-302">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-302">WSL</span></span>
* <span data-ttu-id="b3d62-303">改良的僵支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b3d62-303">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b3d62-304">新增用於控制 Windows interop 行為的 wsl 專案 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b3d62-304">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b3d62-305">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b3d62-305">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b3d62-306">新增對 TIOCSTI 的支援 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b3d62-306">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b3d62-307">連接過程中的非封鎖通訊端應該會傳回 EAGAIN 進行寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b3d62-307">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b3d62-308">支援掛接的 Vhd 上的 interop [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="b3d62-308">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b3d62-309">修正根資料夾 [GH 3304] 的許可權檢查問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-309">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b3d62-310">對 TTY 鍵盤 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的支援有限。</span><span class="sxs-lookup"><span data-stu-id="b3d62-310">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b3d62-311">即使是在背景中啟動, Windows UI 應用程式也應該執行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-311">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="b3d62-312">組建17704</span><span class="sxs-lookup"><span data-stu-id="b3d62-312">Build 17704</span></span>
<span data-ttu-id="b3d62-313">如需組建17704的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-313">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-314">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-314">WSL</span></span>
* <span data-ttu-id="b3d62-315">新增 wsl-u 或--user 選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b3d62-315">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b3d62-316">修正啟用快速啟動時的 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b3d62-316">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b3d62-317">Unix 通訊端需要保留中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b3d62-317">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b3d62-318">非封鎖的 Unix 通訊端使用 EAGAIN 無限期失敗 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b3d62-318">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b3d62-319">case = off 是新的預設 drvfs 掛接類型 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="b3d62-319">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b3d62-320">如需詳細資訊, 請參閱[blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 。</span><span class="sxs-lookup"><span data-stu-id="b3d62-320">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b3d62-321">新增 wslconfig/terminate 以停止執行散發套件。</span><span class="sxs-lookup"><span data-stu-id="b3d62-321">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="b3d62-322">組建 17692</span><span class="sxs-lookup"><span data-stu-id="b3d62-322">Build 17692</span></span>
<span data-ttu-id="b3d62-323">如需組建17692的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-323">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-324">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-324">WSL</span></span>
* <span data-ttu-id="b3d62-325">修正未正確處理具有空格之路徑的 WSL shell 內容功能表項目問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-325">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b3d62-326">以擴充屬性的形式公開每個目錄的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b3d62-326">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b3d62-327">ARM64模擬快取維護作業。</span><span class="sxs-lookup"><span data-stu-id="b3d62-327">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b3d62-328">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-328">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b3d62-329">DrvFs: 僅 unescape 與逸出字元對應之私用範圍中的字元。</span><span class="sxs-lookup"><span data-stu-id="b3d62-329">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="b3d62-330">組建 17686</span><span class="sxs-lookup"><span data-stu-id="b3d62-330">Build 17686</span></span>
<span data-ttu-id="b3d62-331">如需組建17686的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-331">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-332">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-332">WSL</span></span>
* <span data-ttu-id="b3d62-333">修正 ELF parser 解譯器長度驗證中的逐一錯誤 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b3d62-333">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b3d62-334">WSL 過去時間的絕對計時器不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b3d62-334">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b3d62-335">確保新建立的重新分析點在上層目錄中列為。</span><span class="sxs-lookup"><span data-stu-id="b3d62-335">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b3d62-336">以原子方式在 DrvFs 中建立區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="b3d62-336">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="b3d62-337">組建17677</span><span class="sxs-lookup"><span data-stu-id="b3d62-337">Build 17677</span></span>
<span data-ttu-id="b3d62-338">如需組建17677的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-338">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-339">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-339">WSL</span></span>
* <span data-ttu-id="b3d62-340">已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的其他問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-340">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3d62-341">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3d62-341">[GH 2712]</span></span>
* <span data-ttu-id="b3d62-342">已修正啟用 UMCI 時的 WSL 啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="b3d62-342">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b3d62-343">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b3d62-343">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="b3d62-344">組建17666</span><span class="sxs-lookup"><span data-stu-id="b3d62-344">Build 17666</span></span>
<span data-ttu-id="b3d62-345">如需組建17666的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-345">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-346">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-346">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="b3d62-347">警告：有一個問題導致 WSL 無法在某些 AMD 晶片組上執行 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-347">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="b3d62-348">修正已準備就緒, 可對 Insider Build 分支進行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-348">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="b3d62-349">[新增 explorer] 操作功能表以啟動 WSL [GH 437, 603, 1836]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-349">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b3d62-350">在 explorer 視窗中, 使用按住 shift 並以滑鼠右鍵按一下。</span><span class="sxs-lookup"><span data-stu-id="b3d62-350">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b3d62-351">修正 unix 通訊端未封鎖的行為 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="b3d62-351">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b3d62-352">修正 GH 2026 中所報告的懸掛 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="b3d62-352">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b3d62-353">新增對掛接傳播旗標的支援 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-353">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b3d62-354">修正不會造成 inotifypropertychanged 事件的截斷問題 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-354">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b3d62-355">Add--wsl 的 exec 選項, 可在不使用 shell 的情況下叫用單一二進位檔。</span><span class="sxs-lookup"><span data-stu-id="b3d62-355">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b3d62-356">新增--wsl 的散發選項, 以選取特定的散發版本。</span><span class="sxs-lookup"><span data-stu-id="b3d62-356">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="b3d62-357">組建 17655 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-357">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-358">如需組建17655的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-358">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-359">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-359">WSL</span></span>
* <span data-ttu-id="b3d62-360">有限的 dmesg 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-360">Limited support for dmesg.</span></span> <span data-ttu-id="b3d62-361">應用程式現在可以登入 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-361">Applications can now log to dmesg.</span></span> <span data-ttu-id="b3d62-362">WSL 驅動程式會將有限的資訊記錄到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-362">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b3d62-363">未來, 您可以擴充此功能, 以從驅動程式中攜帶其他資訊/診斷。</span><span class="sxs-lookup"><span data-stu-id="b3d62-363">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b3d62-364">注意: 目前透過`/dev/kmsg`裝置介面支援 dmesg。</span><span class="sxs-lookup"><span data-stu-id="b3d62-364">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b3d62-365">`syslog`尚不支援 sycall 介面。</span><span class="sxs-lookup"><span data-stu-id="b3d62-365">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="b3d62-366">因此, 某些`dmesg`命令列選項`-S`(例如) `-C`無法使用。</span><span class="sxs-lookup"><span data-stu-id="b3d62-366">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b3d62-367">已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-367">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3d62-368">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3d62-368">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="b3d62-369">組建 17639 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-369">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-370">如需組建17639的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-370">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-371">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-371">WSL</span></span>
* <span data-ttu-id="b3d62-372">變更序列裝置的預設 gid 和模式以符合原生 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b3d62-372">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b3d62-373">DrvFs 現在支援擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d62-373">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b3d62-374">注意:DrvFs 在擴充屬性的名稱上有一些限制。</span><span class="sxs-lookup"><span data-stu-id="b3d62-374">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b3d62-375">特別的是, 不允許某些字元 (例如 '/'、':\*' 和 ' '), 而且擴充屬性名稱在 DrvFs 上不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-375">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="b3d62-376">組建 17133 (快速)</span><span class="sxs-lookup"><span data-stu-id="b3d62-376">Build 17133 (Fast)</span></span>
<span data-ttu-id="b3d62-377">如需組建17133的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-377">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-378">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-378">WSL</span></span>
* <span data-ttu-id="b3d62-379">修正 WSL 中的停止回應。</span><span class="sxs-lookup"><span data-stu-id="b3d62-379">Fix for hang in WSL.</span></span> <span data-ttu-id="b3d62-380">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="b3d62-380">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="b3d62-381">組建 17128 (快速)</span><span class="sxs-lookup"><span data-stu-id="b3d62-381">Build 17128 (Fast)</span></span>
<span data-ttu-id="b3d62-382">如需組建17128的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-382">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-383">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-383">WSL</span></span>
* <span data-ttu-id="b3d62-384">None</span><span class="sxs-lookup"><span data-stu-id="b3d62-384">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="b3d62-385">組建 17627 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-385">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-386">如需組建17627的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-386">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-387">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-387">WSL</span></span>
* <span data-ttu-id="b3d62-388">新增對 futex pi 感知作業的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-388">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="b3d62-389">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="b3d62-389">[GH 1006]</span></span>
    * <span data-ttu-id="b3d62-390">請注意, 優先順序目前不是支援的 WSL 功能, 因此有一些限制, 但應該解除封鎖標準使用方式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-390">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="b3d62-391">適用于 WSL 進程的 Windows 防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-391">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="b3d62-392">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="b3d62-392">[GH 1852]</span></span>
    * <span data-ttu-id="b3d62-393">例如, 若要允許 WSL python 進程在任何埠上接聽, 請使用提升許可權的 Windows cmd:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="b3d62-393">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="b3d62-394">如需如何新增防火牆規則的其他詳細資料, 請參閱[連結](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="b3d62-394">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="b3d62-395">使用 wsl 時, 請遵循使用者的預設 shell。</span><span class="sxs-lookup"><span data-stu-id="b3d62-395">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="b3d62-396">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="b3d62-396">[GH 2372]</span></span>
* <span data-ttu-id="b3d62-397">將所有網路介面報告為 ethernet。</span><span class="sxs-lookup"><span data-stu-id="b3d62-397">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="b3d62-398">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="b3d62-398">[GH 2996]</span></span>
* <span data-ttu-id="b3d62-399">更好的處理損毀的/etc/passwd 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-399">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="b3d62-400">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="b3d62-400">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-401">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-401">Console</span></span>
* <span data-ttu-id="b3d62-402">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-402">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-403">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-403">LTP Results:</span></span>
<span data-ttu-id="b3d62-404">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-404">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="b3d62-405">組建 17618 (向前跳過)</span><span class="sxs-lookup"><span data-stu-id="b3d62-405">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="b3d62-406">如需組建17618的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-406">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-407">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-407">WSL</span></span>
* <span data-ttu-id="b3d62-408">引進 NT interop 的 pseudoconsole 功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-408">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="b3d62-409">舊版安裝機制 (lxrun) 已被取代。</span><span class="sxs-lookup"><span data-stu-id="b3d62-409">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="b3d62-410">安裝發行版本的支援機制是透過 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="b3d62-410">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-411">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-411">Console</span></span>
* <span data-ttu-id="b3d62-412">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-412">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-413">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-413">LTP Results:</span></span>
<span data-ttu-id="b3d62-414">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-414">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="b3d62-415">組建 17110</span><span class="sxs-lookup"><span data-stu-id="b3d62-415">Build 17110</span></span>
<span data-ttu-id="b3d62-416">如需組建17110的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-416">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-417">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-417">WSL</span></span>
* <span data-ttu-id="b3d62-418">允許從 Windows 終止/init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-418">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="b3d62-419">根據預設, DrvFs 現在會使用每個目錄的區分大小寫 (相當於 "case = dir" 掛接選項)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-419">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="b3d62-420">使用 "case = force" (舊行為) 需要設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-420">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="b3d62-421">執行下列命令, 以在您需要使用「案例 = 強制」時啟用它: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="b3d62-421">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="b3d62-422">如果您在舊版 Windows 中使用 WSL 建立的現有目錄需要區分大小寫, 請使用 fsutil 將它們標示為區分大小寫: fsutil file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="b3d62-422">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="b3d62-423">從 uname syscall 傳回的 Null 終止字串。</span><span class="sxs-lookup"><span data-stu-id="b3d62-423">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-424">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-424">Console</span></span>
* <span data-ttu-id="b3d62-425">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-425">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-426">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-426">LTP Results:</span></span>
<span data-ttu-id="b3d62-427">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-427">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="b3d62-428">組建17107</span><span class="sxs-lookup"><span data-stu-id="b3d62-428">Build 17107</span></span>
<span data-ttu-id="b3d62-429">如需組建17107的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-429">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-430">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-430">WSL</span></span>
* <span data-ttu-id="b3d62-431">支援主要 pty 端點上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-431">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="b3d62-432">啟動同步 interop 進程可能會導致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-432">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="b3d62-433">修正 PTRACE_ATTACH 以在/proc/pid/status. 中顯示適當的追蹤狀態</span><span class="sxs-lookup"><span data-stu-id="b3d62-433">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="b3d62-434">修正使用 CLEARTID 和 SETTID 旗標複製短期進程的競爭情形, 而不需要清除 TID 位址即可結束。</span><span class="sxs-lookup"><span data-stu-id="b3d62-434">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="b3d62-435">從17093前版本的組建進行升級時, 顯示一則訊息。</span><span class="sxs-lookup"><span data-stu-id="b3d62-435">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="b3d62-436">如需17093檔案系統變更的詳細資料, 請參閱[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)版的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d62-436">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-437">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-437">Console</span></span>
* <span data-ttu-id="b3d62-438">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-438">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-439">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-439">LTP Results:</span></span>
<span data-ttu-id="b3d62-440">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-440">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="b3d62-441">組建17101</span><span class="sxs-lookup"><span data-stu-id="b3d62-441">Build 17101</span></span>
<span data-ttu-id="b3d62-442">如需組建17101的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-442">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-443">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-443">WSL</span></span>
* <span data-ttu-id="b3d62-444">支援 signalfd。</span><span class="sxs-lookup"><span data-stu-id="b3d62-444">Support for signalfd.</span></span> <span data-ttu-id="b3d62-445">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="b3d62-445">[GH 129]</span></span>
* <span data-ttu-id="b3d62-446">支援包含不合法 NTFS 字元的檔案名, 方法是將它們編碼為私用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="b3d62-446">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="b3d62-447">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="b3d62-447">[GH 1514]</span></span>
* <span data-ttu-id="b3d62-448">當不支援寫入時, 自動掛接將會回復為唯讀。</span><span class="sxs-lookup"><span data-stu-id="b3d62-448">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="b3d62-449">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="b3d62-449">[GH 2603]</span></span>
* <span data-ttu-id="b3d62-450">允許貼上 Unicode 代理配對 (如表情字元)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-450">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="b3d62-451">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="b3d62-451">[GH 2765]</span></span>
* <span data-ttu-id="b3d62-452">/Proc 和/sys 中的虛擬檔案應該會從 select、輪詢、epoll、et al 傳回讀取和寫入準備就緒。 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="b3d62-452">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="b3d62-453">修正可能導致服務在登錄遭篡改或損毀時進入無限迴圈的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-453">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="b3d62-454">修正 netlink 訊息, 以使用較新的 (上游 4.14) 版本的 iproute2。</span><span class="sxs-lookup"><span data-stu-id="b3d62-454">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-455">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-455">Console</span></span>
* <span data-ttu-id="b3d62-456">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-457">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-457">LTP Results:</span></span>
<span data-ttu-id="b3d62-458">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-458">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="b3d62-459">組建17093</span><span class="sxs-lookup"><span data-stu-id="b3d62-459">Build 17093</span></span>
<span data-ttu-id="b3d62-460">如需組建17093的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-460">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="b3d62-461">重要事項：</span><span class="sxs-lookup"><span data-stu-id="b3d62-461">Important:</span></span>
<span data-ttu-id="b3d62-462">升級至這個組建之後, 第一次啟動 WSL 時, 它需要執行一些工作來升級 Linux 檔案系統目錄。</span><span class="sxs-lookup"><span data-stu-id="b3d62-462">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="b3d62-463">這可能需要幾分鐘的時間, 因此 WSL 的啟動速度可能會變慢。</span><span class="sxs-lookup"><span data-stu-id="b3d62-463">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="b3d62-464">這應該只會針對您從存放區安裝的每個發佈執行一次。</span><span class="sxs-lookup"><span data-stu-id="b3d62-464">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="b3d62-465">改善 DrvFs 中的區分大小寫支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-465">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="b3d62-466">DrvFs 現在支援每個目錄區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-466">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="b3d62-467">這是可以在目錄上設定的新旗標, 以指出這些目錄中的所有作業都應該視為區分大小寫, 這可讓 Windows 應用程式能夠正確開啟只有大小寫不同的檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-467">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="b3d62-468">DrvFs 有新的掛接選項, 可控制以每個目錄為基礎的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b3d62-468">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="b3d62-469">case = force: 將所有目錄視為區分大小寫 (磁片磁碟機根目錄除外)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-469">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="b3d62-470">使用 WSL 建立的新目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-470">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="b3d62-471">這是舊版的行為, 但會將新的目錄標記為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-471">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="b3d62-472">case = dir: 只有具有每個目錄的區分大小寫旗標的目錄會被視為區分大小寫;其他目錄則不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-472">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b3d62-473">使用 WSL 建立的新目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-473">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="b3d62-474">案例 = 關閉: 只有具有每個目錄區分大小寫旗標的目錄會被視為區分大小寫;其他目錄則不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-474">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b3d62-475">使用 WSL 建立的新目錄會標示為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-475">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="b3d62-476">注意: 在舊版中, WSL 所建立的目錄並不會設定此旗標, 因此如果您使用 "case = dir" 選項, 則不會將其視為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-476">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="b3d62-477">即將推出在現有目錄上設定此旗標的方法。</span><span class="sxs-lookup"><span data-stu-id="b3d62-477">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="b3d62-478">使用這些選項掛接的範例 (針對現有的磁片磁碟機, 您必須先卸載, 才可以使用不同的選項進行掛接): sudo mount-t drvfs C:/mnt/c-o case = dir</span><span class="sxs-lookup"><span data-stu-id="b3d62-478">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="b3d62-479">目前, case = force 仍然是預設選項。</span><span class="sxs-lookup"><span data-stu-id="b3d62-479">For now, case=force is still the default option.</span></span> <span data-ttu-id="b3d62-480">未來將會變更為案例 = dir。</span><span class="sxs-lookup"><span data-stu-id="b3d62-480">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="b3d62-481">在裝載 DrvFs 時, 您現在可以在 Windows 路徑中使用正斜線, 例如: sudo mount-t DrvFs//server/share/mnt/share</span><span class="sxs-lookup"><span data-stu-id="b3d62-481">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="b3d62-482">WSL 現在會在實例開始 [GH 2636] 期間處理/etc/fstab 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-482">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="b3d62-483">這會在自動掛接 DrvFs 磁片磁碟機之前完成。fstab 已掛接的任何磁片磁碟機將不會自動重新掛接, 可讓您變更特定磁片磁碟機的掛接點。</span><span class="sxs-lookup"><span data-stu-id="b3d62-483">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="b3d62-484">您可以使用 wsl 來關閉此行為。</span><span class="sxs-lookup"><span data-stu-id="b3d62-484">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="b3d62-485">/Proc 中的 mount、mountinfo 和 mountstats 檔案會適當地轉義特殊字元, 例如反斜線和空格 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="b3d62-485">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="b3d62-486">在啟用中繼資料時, 使用 DrvFs 建立的特殊檔案 (例如 WSL 符號連結, 或 fifos 和通訊端), 現在可以從 Windows 複製和移動。</span><span class="sxs-lookup"><span data-stu-id="b3d62-486">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="b3d62-487">WSL 可透過 WSL 更容易設定</span><span class="sxs-lookup"><span data-stu-id="b3d62-487">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="b3d62-488">我們新增了一種方法, 讓您在每次啟動子系統時, 自動設定 WSL 中的特定功能。</span><span class="sxs-lookup"><span data-stu-id="b3d62-488">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="b3d62-489">這包括自動掛接選項和網路設定。</span><span class="sxs-lookup"><span data-stu-id="b3d62-489">This includes automount options and network configuration.</span></span> <span data-ttu-id="b3d62-490">在我們的 blog 文章中深入瞭解它, 網址為: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="b3d62-490">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="b3d62-491">AF_UNIX 允許 WSL 和 Windows 原生進程上 Linux 進程之間的通訊端連線</span><span class="sxs-lookup"><span data-stu-id="b3d62-491">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="b3d62-492">WSL 和 Windows 應用程式現在可以透過 Unix 通訊端彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="b3d62-492">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="b3d62-493">假設您想要在 Windows 中執行服務, 並讓 Windows 和 WSL 應用程式都能使用它。</span><span class="sxs-lookup"><span data-stu-id="b3d62-493">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="b3d62-494">現在, 您可以使用 Unix 通訊端來做到這一點。</span><span class="sxs-lookup"><span data-stu-id="b3d62-494">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="b3d62-495">在我們的 blog 文章中閱讀更多資訊, 網址為 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="b3d62-495">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-496">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-496">WSL</span></span>
* <span data-ttu-id="b3d62-497">支援 mmap () 與 MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="b3d62-497">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="b3d62-498">支援 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="b3d62-498">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="b3d62-499">處理複製中的非 SIGCHLD 終止信號 [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="b3d62-499">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="b3d62-500">Stub/proc/sys/fs/inotify/max_user_instances 和/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="b3d62-500">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="b3d62-501">載入包含具有非零位移之載入標頭的 ELF 二進位檔時發生錯誤 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="b3d62-501">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="b3d62-502">載入影像時, 有零的尾端分頁位元組。</span><span class="sxs-lookup"><span data-stu-id="b3d62-502">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="b3d62-503">減少 execve 以無訊息方式終止進程的情況</span><span class="sxs-lookup"><span data-stu-id="b3d62-503">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-504">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-504">Console</span></span>
* <span data-ttu-id="b3d62-505">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-505">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-506">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-506">LTP Results:</span></span>
<span data-ttu-id="b3d62-507">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-507">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="b3d62-508">組建 17083</span><span class="sxs-lookup"><span data-stu-id="b3d62-508">Build 17083</span></span>
<span data-ttu-id="b3d62-509">如需組建17083的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-509">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-510">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-510">WSL</span></span>
* <span data-ttu-id="b3d62-511">已修正與 epoll 相關的錯誤檢查 [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="b3d62-511">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="b3d62-512">已修正關閉 ASLR 時的停止回應 [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="b3d62-512">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="b3d62-513">確保 mmap 作業看起來不可部分完成 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="b3d62-513">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-514">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-514">Console</span></span>
* <span data-ttu-id="b3d62-515">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-515">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-516">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-516">LTP Results:</span></span>
<span data-ttu-id="b3d62-517">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-517">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="b3d62-518">組建17074</span><span class="sxs-lookup"><span data-stu-id="b3d62-518">Build 17074</span></span>
<span data-ttu-id="b3d62-519">如需組建17074的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-519">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-520">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-520">WSL</span></span>
* <span data-ttu-id="b3d62-521">已修正 DrvFs 中繼資料的儲存格式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="b3d62-521">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="b3d62-522">**重要事項：** 在此組建之前建立的 DrvFs 中繼資料將不會正確地顯示, 或根本不會出現。</span><span class="sxs-lookup"><span data-stu-id="b3d62-522">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="b3d62-523">若要修正受影響的檔案, 請使用 chmod 和 chown 來重新套用中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3d62-523">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="b3d62-524">已修正多個信號和可重新開機 syscalls 的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-524">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-525">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-525">Console</span></span>
* <span data-ttu-id="b3d62-526">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-526">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-527">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-527">LTP Results:</span></span>
<span data-ttu-id="b3d62-528">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-528">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="b3d62-529">組建17063</span><span class="sxs-lookup"><span data-stu-id="b3d62-529">Build 17063</span></span>
<span data-ttu-id="b3d62-530">如需組建17063的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-530">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3d62-531">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-531">WSL</span></span>
* <span data-ttu-id="b3d62-532">DrvFs 支援其他 Linux 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3d62-532">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="b3d62-533">這可讓您使用 chmod/chown 來設定檔案的擁有者和模式, 以及建立特殊檔案 (例如 fifos、unix 通訊端和裝置檔案)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-533">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="b3d62-534">預設會停用這項功能, 因為它仍然是實驗性。</span><span class="sxs-lookup"><span data-stu-id="b3d62-534">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="b3d62-535">**注意：** 我們已修正 DrvFs 所使用之元資料格式的 bug。</span><span class="sxs-lookup"><span data-stu-id="b3d62-535">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="b3d62-536">雖然中繼資料適用于實驗的此組建, 但未來的組建將無法正確讀取此組建所建立的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3d62-536">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="b3d62-537">您可能需要手動更新已修改檔案的擁有者, 而且必須重新建立具有自訂裝置識別碼的裝置。</span><span class="sxs-lookup"><span data-stu-id="b3d62-537">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="b3d62-538">若要啟用, 請使用中繼資料選項掛接 DrvFs (若要在現有的掛接上啟用, 您必須先將它卸載):</span><span class="sxs-lookup"><span data-stu-id="b3d62-538">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="b3d62-539">Linux 許可權會當做額外的中繼資料新增至檔案;它們不會影響 Windows 許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-539">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="b3d62-540">請記住, 使用 Windows 編輯器編輯檔案可能會移除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3d62-540">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="b3d62-541">在此情況下, 檔案將會還原為其預設許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-541">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="b3d62-542">已將掛接選項新增至 DrvFs, 以控制沒有中繼資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-542">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="b3d62-543">uid: 用於所有檔案之擁有者的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-543">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b3d62-544">gid: 用於所有檔案之擁有者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-544">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b3d62-545">umask: 要針對所有檔案和目錄排除的八進位遮罩許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-545">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="b3d62-546">fmask: 要針對所有一般檔案排除的八進位遮罩許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-546">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="b3d62-547">dmask: 要針對所有目錄排除的八進位遮罩許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-547">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="b3d62-548">例如:</span><span class="sxs-lookup"><span data-stu-id="b3d62-548">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="b3d62-549">結合中繼資料選項來指定沒有中繼資料之檔案的預設許可權。</span><span class="sxs-lookup"><span data-stu-id="b3d62-549">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="b3d62-550">引進新的環境變數, `WSLENV`以設定環境變數在 WSL 與 Win32 之間的流動方式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-550">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="b3d62-551">例如:</span><span class="sxs-lookup"><span data-stu-id="b3d62-551">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="b3d62-552">`WSLENV`這是以冒號分隔的環境變數清單, 可在從 WSL 啟動 Win32 或 Win32 進程中的 WSL 進程時包含。</span><span class="sxs-lookup"><span data-stu-id="b3d62-552">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="b3d62-553">每個變數都可以加上斜線, 後面接著旗標, 以指定翻譯的方式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-553">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="b3d62-554">p&id此值是應該在 WSL 路徑和 Win32 路徑之間轉譯的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3d62-554">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="b3d62-555">l值是路徑的清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-555">l: The value is a list of paths.</span></span> <span data-ttu-id="b3d62-556">在 WSL 中, 它是以冒號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-556">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="b3d62-557">在 Win32 中, 它是以分號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-557">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="b3d62-558">那麼從 Win32 叫用 WSL 時, 應該只包含此值</span><span class="sxs-lookup"><span data-stu-id="b3d62-558">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="b3d62-559">寬從 WSL 叫用 Win32 時, 應該只包含此值</span><span class="sxs-lookup"><span data-stu-id="b3d62-559">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="b3d62-560">您可以在`WSLENV` .bashrc 或在自訂 Windows 環境中, 為您的使用者設定。</span><span class="sxs-lookup"><span data-stu-id="b3d62-560">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="b3d62-561">drvfs 裝載會正確保留 tar、cp-p 的時間戳記 (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="b3d62-561">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="b3d62-562">drvfs 符號連結報告正確的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="b3d62-562">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="b3d62-563">讀取/寫入適用于非常大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="b3d62-563">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="b3d62-564">waitpid 適用于進程群組識別碼 (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="b3d62-564">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="b3d62-565">大幅改善大型保留區域的 mmap 效能;改善 ghc 效能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="b3d62-565">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="b3d62-566">特性支援 READ_IMPLIES_EXEC;修正 maxima 和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="b3d62-566">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="b3d62-567">mprotect 支援 PROT_GROWSDOWN;修正 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b3d62-567">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="b3d62-568">過量使用模式中的分頁錯誤修正;修正 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b3d62-568">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="b3d62-569">複製支援更多旗標組合</span><span class="sxs-lookup"><span data-stu-id="b3d62-569">clone supports more flags combinations</span></span>
* <span data-ttu-id="b3d62-570">支援 epoll 檔案的 select/epoll (先前為無 op)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-570">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="b3d62-571">通知 ptrace 未實現的 syscalls。</span><span class="sxs-lookup"><span data-stu-id="b3d62-571">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="b3d62-572">忽略產生 resolv.conf 時未啟動的介面 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="b3d62-572">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="b3d62-573">列舉沒有實體位址的網路介面。</span><span class="sxs-lookup"><span data-stu-id="b3d62-573">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="b3d62-574">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="b3d62-574">[GH 2685]</span></span>
* <span data-ttu-id="b3d62-575">其他錯誤修正和改善。</span><span class="sxs-lookup"><span data-stu-id="b3d62-575">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="b3d62-576">適用于 Windows 開發人員的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="b3d62-576">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="b3d62-577">Windows 命令列工具鏈包括 bsdtar (tar) 和捲曲。</span><span class="sxs-lookup"><span data-stu-id="b3d62-577">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="b3d62-578">閱讀[這篇 blog](https://aka.ms/tarcurlwindows)以深入瞭解如何新增這兩項新工具, 並查看其如何塑造 Windows 上的開發人員經驗。</span><span class="sxs-lookup"><span data-stu-id="b3d62-578">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="b3d62-579">`AF_UNIX`可在 Windows 測試人員 SDK (17061 +) 中取得。</span><span class="sxs-lookup"><span data-stu-id="b3d62-579">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="b3d62-580">閱讀[這篇 blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)以深入瞭解`AF_UNIX` , 以及 Windows 上的開發人員可以如何使用它。</span><span class="sxs-lookup"><span data-stu-id="b3d62-580">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="b3d62-581">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-581">Console</span></span>
* <span data-ttu-id="b3d62-582">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-582">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-583">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-583">LTP Results:</span></span>
<span data-ttu-id="b3d62-584">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-584">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="b3d62-585">組建17046</span><span class="sxs-lookup"><span data-stu-id="b3d62-585">Build 17046</span></span>

<span data-ttu-id="b3d62-586">如需組建17046的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-586">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-587">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-587">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-588">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-588">WSL</span></span>
- <span data-ttu-id="b3d62-589">允許進程在沒有使用中的終端機的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-589">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="b3d62-590">[GH 709, 1007, 1511, 2252, 2391, et al。]</span><span class="sxs-lookup"><span data-stu-id="b3d62-590">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="b3d62-591">更好的 CLONE_VFORK 和 CLONE_VM 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-591">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="b3d62-592">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="b3d62-592">[GH 1878, 2615]</span></span>
- <span data-ttu-id="b3d62-593">略過 WSL 網路作業的 TDI 篩選器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-593">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="b3d62-594">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="b3d62-594">[GH 1554]</span></span>
- <span data-ttu-id="b3d62-595">DrvFs 會在符合特定條件時建立 NT 符號連結。</span><span class="sxs-lookup"><span data-stu-id="b3d62-595">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="b3d62-596">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="b3d62-596">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="b3d62-597">連結目標必須是相對的, 而且不能跨越任何掛接點或符號連結, 而且必須存在。</span><span class="sxs-lookup"><span data-stu-id="b3d62-597">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="b3d62-598">除非已開啟開發人員模式, 否則使用者必須具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (這通常會要求您啟動 wsl 提升許可權)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-598">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="b3d62-599">在所有其他情況下, DrvFs 仍然會建立 WSL 符號連結。</span><span class="sxs-lookup"><span data-stu-id="b3d62-599">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="b3d62-600">允許同時執行提高許可權和未提高許可權的 WSL 實例。</span><span class="sxs-lookup"><span data-stu-id="b3d62-600">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="b3d62-601">支援/proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="b3d62-601">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="b3d62-602">新增 wslpath 以執行 WSL <-> Windows 路徑轉換。</span><span class="sxs-lookup"><span data-stu-id="b3d62-602">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="b3d62-603">[GH 522、1243、1834、2327、et al。]</span><span class="sxs-lookup"><span data-stu-id="b3d62-603">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="b3d62-604">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-604">Console</span></span>
- <span data-ttu-id="b3d62-605">沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-605">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-606">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-606">LTP Results:</span></span>
<span data-ttu-id="b3d62-607">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-607">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="b3d62-608">組建17040</span><span class="sxs-lookup"><span data-stu-id="b3d62-608">Build 17040</span></span>

<span data-ttu-id="b3d62-609">如需組建17040的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-609">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-610">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-610">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-611">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-611">WSL</span></span>
- <span data-ttu-id="b3d62-612">17035之後沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-612">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-613">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-613">Console</span></span>
- <span data-ttu-id="b3d62-614">17035之後沒有任何修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-614">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-615">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-615">LTP Results:</span></span>
<span data-ttu-id="b3d62-616">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-616">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="b3d62-617">組建17035</span><span class="sxs-lookup"><span data-stu-id="b3d62-617">Build 17035</span></span>

<span data-ttu-id="b3d62-618">如需組建17035的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-618">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-619">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-619">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-620">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-620">WSL</span></span>
- <span data-ttu-id="b3d62-621">在 DrvFs 上存取檔案時, 偶爾會發生 EINVAL 失敗。</span><span class="sxs-lookup"><span data-stu-id="b3d62-621">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="b3d62-622">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="b3d62-622">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-623">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-623">Console</span></span>
- <span data-ttu-id="b3d62-624">在 VT 模式下插入/刪除線條時, 某些色彩會遺失。</span><span class="sxs-lookup"><span data-stu-id="b3d62-624">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-625">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-625">LTP Results:</span></span>
<span data-ttu-id="b3d62-626">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-626">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="b3d62-627">組建17025</span><span class="sxs-lookup"><span data-stu-id="b3d62-627">Build 17025</span></span>

<span data-ttu-id="b3d62-628">如需組建17025的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-628">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-629">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-629">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-630">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-630">WSL</span></span>
- <span data-ttu-id="b3d62-631">在新的前景進程群組中啟動初始進程 [GH 1653, 2510]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-631">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="b3d62-632">SIGHUP 傳遞修正 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-632">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="b3d62-633">如果未提供 [GH 2497], 則產生預設虛擬橋接器名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d62-633">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="b3d62-634">執行/proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-634">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="b3d62-635">更多 interop stdout/stderr 管線修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-635">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="b3d62-636">存根 syncfs 系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-636">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-637">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-637">Console</span></span>
- <span data-ttu-id="b3d62-638">修正協力廠商主控台的輸入 VT 轉譯 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="b3d62-638">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-639">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-639">LTP Results:</span></span>
<span data-ttu-id="b3d62-640">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-640">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="b3d62-641">組建17017</span><span class="sxs-lookup"><span data-stu-id="b3d62-641">Build 17017</span></span>

<span data-ttu-id="b3d62-642">如需組建17017的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-642">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-643">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-643">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-644">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-644">WSL</span></span>
- <span data-ttu-id="b3d62-645">忽略空的 ELF 程式標頭 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-645">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="b3d62-646">允許 LxssManager 建立非互動式使用者的 WSL 實例 (ssh 和排程的工作支援) [GH 777, 1602]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-646">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="b3d62-647">支援 WSL-> Win32 > WSL (「開始」) 案例 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-647">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="b3d62-648">限制終止透過 interop [GH 1614] 叫用的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-648">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="b3d62-649">支援 devpts 的掛接選項 [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-649">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="b3d62-650">Ptrace 封鎖子啟動 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-650">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="b3d62-651">EPOLLET 遺漏某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-651">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="b3d62-652">傳回 PTRACE_GETSIGINFO 的更多資料。</span><span class="sxs-lookup"><span data-stu-id="b3d62-652">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="b3d62-653">具有 lseek 的 Getdents 會提供不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="b3d62-653">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="b3d62-654">修正某些 Win32 interop 應用程式當機, 等候沒有其他資料的管道上的輸入。</span><span class="sxs-lookup"><span data-stu-id="b3d62-654">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="b3d62-655">O_ASYNC 對 tty/pty 檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-655">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="b3d62-656">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-656">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-657">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-657">Console</span></span>
- <span data-ttu-id="b3d62-658">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-658">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-659">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-659">LTP Results:</span></span>
<span data-ttu-id="b3d62-660">正在進行測試。</span><span class="sxs-lookup"><span data-stu-id="b3d62-660">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="b3d62-661">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="b3d62-661">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="b3d62-662">組建16288</span><span class="sxs-lookup"><span data-stu-id="b3d62-662">Build 16288</span></span>

<span data-ttu-id="b3d62-663">如需組建16288的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-663">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-664">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-665">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-665">WSL</span></span>
- <span data-ttu-id="b3d62-666">正確初始化和報告通訊端檔案描述項的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="b3d62-666">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="b3d62-667">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-667">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-668">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-668">Console</span></span>
- <span data-ttu-id="b3d62-669">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-669">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-670">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-670">LTP Results:</span></span>
<span data-ttu-id="b3d62-671">自16273開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-671">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="b3d62-672">組建16278</span><span class="sxs-lookup"><span data-stu-id="b3d62-672">Build 16278</span></span>

<span data-ttu-id="b3d62-673">如需組建162738的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-673">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-674">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-674">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-675">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-675">WSL</span></span>
- <span data-ttu-id="b3d62-676">卸載 LX MM 狀態時, 明確取消對應檔案支援區段的對應視圖 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="b3d62-676">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="b3d62-677">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-677">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-678">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-678">Console</span></span>
- <span data-ttu-id="b3d62-679">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-679">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-680">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-680">LTP Results:</span></span>
<span data-ttu-id="b3d62-681">自16273開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-681">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="b3d62-682">組建16275</span><span class="sxs-lookup"><span data-stu-id="b3d62-682">Build 16275</span></span>

<span data-ttu-id="b3d62-683">如需組建162735的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-683">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-684">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-684">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-685">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-685">WSL</span></span>
- <span data-ttu-id="b3d62-686">此版本中沒有任何 WSL 相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-686">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-687">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-687">Console</span></span>
- <span data-ttu-id="b3d62-688">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-688">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-689">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-689">LTP Results:</span></span>
<span data-ttu-id="b3d62-690">自16273開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-690">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="b3d62-691">組建16273</span><span class="sxs-lookup"><span data-stu-id="b3d62-691">Build 16273</span></span>

<span data-ttu-id="b3d62-692">如需組建16273的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-692">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-693">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-694">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-694">WSL</span></span>
- <span data-ttu-id="b3d62-695">已修正 DrvFs 有時會回報錯誤的目錄檔案類型 [GH 2392] 的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-695">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="b3d62-696">允許建立 NETLINK_KOBJECT_UEVENT 通訊端來解除封鎖使用 UEVENT 的程式 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="b3d62-696">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="b3d62-697">新增對非封鎖型連接的支援 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="b3d62-697">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="b3d62-698">執行 CLONE_FS 複製系統呼叫旗標 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b3d62-698">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="b3d62-699">修正不會在 NT interop 中正確處理索引標籤或引號的問題 [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="b3d62-699">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="b3d62-700">解決嘗試重新開機 WSL 實例時發生的拒絕存取錯誤 [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="b3d62-700">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="b3d62-701">執行 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 作業 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b3d62-701">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="b3d62-702">修正各種 SysFs 檔案的許可權 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="b3d62-702">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="b3d62-703">修正安裝期間的 Haskell 堆疊停止回應 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="b3d62-703">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="b3d62-704">執行 binfmt_misc ' C ' ' O ' 與 ' P ' 旗標 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="b3d62-704">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="b3d62-705">新增/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="b3d62-705">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="b3d62-706">新增 ioprio_set 系統呼叫的部分支援 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="b3d62-706">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="b3d62-707">存根 SO_REUSEPORT & 新增 netlink 通訊端的 SO_PASSCRED 支援 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="b3d62-707">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="b3d62-708">如果目前正在安裝或卸載散發, 則會從 RegisterDistribuiton 傳回不同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-708">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="b3d62-709">允許透過 wslconfig 取消註冊部分安裝的 WSL 散發套件</span><span class="sxs-lookup"><span data-stu-id="b3d62-709">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="b3d62-710">從 udp:: msg_peek 修正 python 通訊端測試停止回應</span><span class="sxs-lookup"><span data-stu-id="b3d62-710">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="b3d62-711">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-712">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-712">Console</span></span>
- <span data-ttu-id="b3d62-713">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-714">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-714">LTP Results:</span></span>
<span data-ttu-id="b3d62-715">測試總計:1904</span><span class="sxs-lookup"><span data-stu-id="b3d62-715">Total Tests: 1904</span></span><br/>
<span data-ttu-id="b3d62-716">已略過的測試總數:209</span><span class="sxs-lookup"><span data-stu-id="b3d62-716">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="b3d62-717">失敗總計:229</span><span class="sxs-lookup"><span data-stu-id="b3d62-717">Total Failures: 229</span></span><br/>
[<span data-ttu-id="b3d62-718">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-718">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="b3d62-719">組建 16257</span><span class="sxs-lookup"><span data-stu-id="b3d62-719">Build 16257</span></span>

<span data-ttu-id="b3d62-720">如需組建16257的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-720">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-721">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-721">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-722">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-722">WSL</span></span>
- <span data-ttu-id="b3d62-723">執行 prlimit64 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="b3d62-723">Implement prlimit64 system call</span></span>
- <span data-ttu-id="b3d62-724">新增對 ulimit 的支援-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="b3d62-724">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="b3d62-725">TCP 通訊端的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="b3d62-725">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="b3d62-726">修正不正確 AT_EXECFN 輔助向量行為 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="b3d62-726">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="b3d62-727">修正主控台/tty 的複製/貼上行為, 並新增更好的完整緩衝區處理 [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="b3d62-727">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="b3d62-728">設定 AT_SECURE 在輔助向量中用於設定使用者識別碼和設定群組識別碼程式 [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="b3d62-728">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="b3d62-729">虛擬-終端機主要端點未處理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="b3d62-729">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="b3d62-730">修正 lseek 在 LxFs 中倒轉目錄 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="b3d62-730">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="b3d62-731">/dev/ptmx 在高使用量之後鎖定 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="b3d62-731">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="b3d62-732">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-732">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-733">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-733">Console</span></span>
- <span data-ttu-id="b3d62-734">修正所有位置的水平線/底線 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="b3d62-734">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="b3d62-735">修正程式順序變更, 使 NPM 難以關閉 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="b3d62-735">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="b3d62-736">已新增新的色彩配置: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="b3d62-736">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-737">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-737">LTP Results:</span></span>
<span data-ttu-id="b3d62-738">自16251開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-738">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-739">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-739">Syscall Support</span></span>
<span data-ttu-id="b3d62-740">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-740">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-741">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-741">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="b3d62-742">已知問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-742">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="b3d62-743">GitHub 問題 2392:WSL 無法辨識的 Windows 資料夾 .。。</span><span class="sxs-lookup"><span data-stu-id="b3d62-743">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="b3d62-744">在組建16257中, WSL 在透過列舉 Windows 檔案/資料夾`/mnt/c/...`時發生問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-744">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="b3d62-745">此問題已獲得修正, 應在一周開始8/14/2017 期間, 于內部人員組建中發行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-745">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="b3d62-746">組建16251</span><span class="sxs-lookup"><span data-stu-id="b3d62-746">Build 16251</span></span>

<span data-ttu-id="b3d62-747">如需組建16251的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-747">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-748">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-748">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-749">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-749">WSL</span></span>
- <span data-ttu-id="b3d62-750">從 WSL 選用元件移除 Beta 標記, 如需詳細資訊, 請參閱[blog 文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-750">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="b3d62-751">在 exec [GH 962, 1415, 2072] 上正確初始化已儲存集的 uid 和 gid, 用於設定使用者識別碼和集合群組識別碼二進位檔</span><span class="sxs-lookup"><span data-stu-id="b3d62-751">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="b3d62-752">已新增對 ptrace PTRACE_O_TRACEEXIT 的支援 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b3d62-752">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="b3d62-753">已新增使用 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支援 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b3d62-753">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="b3d62-754">已修正 ptrace 以停止忽略的信號</span><span class="sxs-lookup"><span data-stu-id="b3d62-754">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="b3d62-755">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-756">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-756">Console</span></span>
- <span data-ttu-id="b3d62-757">此版本中沒有任何與主控台相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-758">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-758">LTP Results:</span></span>
<span data-ttu-id="b3d62-759">通過測試的數目:768</span><span class="sxs-lookup"><span data-stu-id="b3d62-759">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="b3d62-760">失敗的測試數目:244</span><span class="sxs-lookup"><span data-stu-id="b3d62-760">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="b3d62-761">略過的測試數目:96</span><span class="sxs-lookup"><span data-stu-id="b3d62-761">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="b3d62-762">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="b3d62-763">組建16241</span><span class="sxs-lookup"><span data-stu-id="b3d62-763">Build 16241</span></span>

<span data-ttu-id="b3d62-764">如需組建16241的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-764">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-765">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3d62-766">WSL</span><span class="sxs-lookup"><span data-stu-id="b3d62-766">WSL</span></span>
- <span data-ttu-id="b3d62-767">此版本中沒有任何 WSL 相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-767">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b3d62-768">Console</span><span class="sxs-lookup"><span data-stu-id="b3d62-768">Console</span></span>
- <span data-ttu-id="b3d62-769">修正輸出中的跨行不正確的字元, 原先在[此](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)報告</span><span class="sxs-lookup"><span data-stu-id="b3d62-769">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="b3d62-770">修正字碼頁 65001 (utf8) 中沒有顯示的輸出文字</span><span class="sxs-lookup"><span data-stu-id="b3d62-770">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="b3d62-771">在選取範圍變更時, 請勿將對某個色彩的 RGB 值所做的變更傳送到調色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="b3d62-771">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="b3d62-772">這會讓主控台屬性工作表的使用變得更容易。</span><span class="sxs-lookup"><span data-stu-id="b3d62-772">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="b3d62-773">Ctrl + S 似乎無法正常運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-773">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="b3d62-774">ANSI 轉義碼中的非粗體/-Dim 完全不存在 [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="b3d62-774">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="b3d62-775">主控台未正確支援 Vim 色彩主題 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="b3d62-775">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="b3d62-776">無法貼上特定字元 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="b3d62-776">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="b3d62-777">重新調整大小會互動奇怪, 並在編輯/命令列上有內容時調整 bash 視窗的大小 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="b3d62-777">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="b3d62-778">Ctrl-L 讓螢幕保持不變 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="b3d62-778">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="b3d62-779">在 HDPI 上顯示 VT 時的主控台呈現錯誤 [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="b3d62-779">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="b3d62-780">Unicode 字元 U + 30FB 的 Japansese 字元看起來很奇怪 [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="b3d62-780">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="b3d62-781">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-781">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="b3d62-782">組建 16237</span><span class="sxs-lookup"><span data-stu-id="b3d62-782">Build 16237</span></span>

<span data-ttu-id="b3d62-783">如需組建16237的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-783">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-784">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-784">Fixed</span></span>
- <span data-ttu-id="b3d62-785">在 lxfs 中使用不含 EAs 的檔案的預設屬性 (root、root、0000)</span><span class="sxs-lookup"><span data-stu-id="b3d62-785">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="b3d62-786">已新增使用擴充屬性之散發的支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-786">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="b3d62-787">修正 getdents 和 getdents64 所傳回之專案的填補</span><span class="sxs-lookup"><span data-stu-id="b3d62-787">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="b3d62-788">修正 shmctl SHM_STAT 系統呼叫的許可權檢查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="b3d62-788">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="b3d62-789">已修正 ttys 的初始 epoll 狀態不正確 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="b3d62-789">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="b3d62-790">修正 DrvFs readdir 未傳回所有專案 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b3d62-790">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="b3d62-791">修正檔案未連結時的 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b3d62-791">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="b3d62-792">允許透過 procfs 重新開啟未連結的 drvfs 檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-792">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="b3d62-793">已新增用來停用 WSL 功能的全域登錄機碼覆寫 (interop/磁片磁碟機裝載)</span><span class="sxs-lookup"><span data-stu-id="b3d62-793">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="b3d62-794">針對 DrvFs (和 LxFs) 的 "stat" 修正不正確的區塊計數 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="b3d62-794">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="b3d62-795">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-795">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="b3d62-796">組建16232</span><span class="sxs-lookup"><span data-stu-id="b3d62-796">Build 16232</span></span>

<span data-ttu-id="b3d62-797">如需組建16232的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-797">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-798">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-798">Fixed</span></span>
- <span data-ttu-id="b3d62-799">此版本中沒有任何 WSL 相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-799">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="b3d62-800">組建16226</span><span class="sxs-lookup"><span data-stu-id="b3d62-800">Build 16226</span></span>

<span data-ttu-id="b3d62-801">如需組建16226的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-801">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-802">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-802">Fixed</span></span>
- <span data-ttu-id="b3d62-803">xattr 相關的 syscalls 支援 (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-803">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="b3d62-804">capablity xattr 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-804">security.capablity xattr support.</span></span>
- <span data-ttu-id="b3d62-805">改善與特定檔案系統和篩選器的相容性, 包括非 MS SMB 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b3d62-805">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="b3d62-806">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="b3d62-806">[GH #1952]</span></span>
- <span data-ttu-id="b3d62-807">改善對 OneDrive 預留位置、GVFS 預留位置和 Compact OS 壓縮檔的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-807">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="b3d62-808">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-808">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="b3d62-809">組建16215</span><span class="sxs-lookup"><span data-stu-id="b3d62-809">Build 16215</span></span>

<span data-ttu-id="b3d62-810">如需組建16215的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-810">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-811">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-811">Fixed</span></span>
- <span data-ttu-id="b3d62-812">WSL 不再需要開發人員模式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-812">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="b3d62-813">支援 drvfs 中的目錄聯接。</span><span class="sxs-lookup"><span data-stu-id="b3d62-813">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="b3d62-814">處理 WSL 散發 appx 套件的卸載。</span><span class="sxs-lookup"><span data-stu-id="b3d62-814">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="b3d62-815">更新 procfs 以顯示私用和共用對應。</span><span class="sxs-lookup"><span data-stu-id="b3d62-815">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="b3d62-816">新增 wslconfig 的功能, 以清除部分安裝或卸載的散發套件。</span><span class="sxs-lookup"><span data-stu-id="b3d62-816">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="b3d62-817">已針對 TCP 通訊端新增 IP_MTU_DISCOVER 的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-817">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="b3d62-818">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="b3d62-818">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="b3d62-819">推斷通訊協定系列以取得 AF_INADDR 的路由。</span><span class="sxs-lookup"><span data-stu-id="b3d62-819">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="b3d62-820">序列裝置改善 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="b3d62-820">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="b3d62-821">組建16199</span><span class="sxs-lookup"><span data-stu-id="b3d62-821">Build 16199</span></span>

<span data-ttu-id="b3d62-822">如需組建16199的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-822">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-823">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-823">Fixed</span></span>
- <span data-ttu-id="b3d62-824">這些版本中沒有任何 WSL 相關的變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-824">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="b3d62-825">組建16193</span><span class="sxs-lookup"><span data-stu-id="b3d62-825">Build 16193</span></span>

<span data-ttu-id="b3d62-826">如需組建16193的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-826">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-827">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-827">Fixed</span></span>
- <span data-ttu-id="b3d62-828">傳送 SIGCONT 與 threadgroup 終止之間的競爭條件 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="b3d62-828">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="b3d62-829">將 tty 和 pty 裝置變更為報告 FILE_DEVICE_NAMED_PIPE, 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b3d62-829">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="b3d62-830">IP_OPTIONS 的 SSH 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-830">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="b3d62-831">已將 DrvFs 裝載移至 init daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="b3d62-831">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="b3d62-832">已在 DrvFs 中新增下列 NT 符號連結的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-832">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="b3d62-833">組建16184</span><span class="sxs-lookup"><span data-stu-id="b3d62-833">Build 16184</span></span>

<span data-ttu-id="b3d62-834">如需組建16184的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-834">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-835">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-835">Fixed</span></span>
- <span data-ttu-id="b3d62-836">已移除 apt 套件維護工作 (lxrun .exe/update)</span><span class="sxs-lookup"><span data-stu-id="b3d62-836">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="b3d62-837">已修正的輸出不會顯示在 node.js 中的 Windows 進程 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b3d62-837">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="b3d62-838">放寬 lxcore 中的對齊需求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="b3d62-838">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="b3d62-839">已修正系統呼叫推中的 AT_EMPTY_PATH 旗標處理。</span><span class="sxs-lookup"><span data-stu-id="b3d62-839">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="b3d62-840">已修正使用開啟的控制碼刪除 DrvFs 檔案將導致檔案出現未定義的行為 [GH 544、966、1357、1535、1615] 的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-840">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="b3d62-841">/etc/hosts 現在會繼承 Windows hosts 檔案中的專案 (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="b3d62-841">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="b3d62-842">組建16179</span><span class="sxs-lookup"><span data-stu-id="b3d62-842">Build 16179</span></span>

<span data-ttu-id="b3d62-843">如需組建16179的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-843">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-844">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-844">Fixed</span></span>
- <span data-ttu-id="b3d62-845">本周沒有任何 WSL 變更。</span><span class="sxs-lookup"><span data-stu-id="b3d62-845">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="b3d62-846">組建16176</span><span class="sxs-lookup"><span data-stu-id="b3d62-846">Build 16176</span></span>

<span data-ttu-id="b3d62-847">如需組建16176的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-847">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-848">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-848">Fixed</span></span>

- [<span data-ttu-id="b3d62-849">啟用的序列支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-849">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="b3d62-850">已新增 IP 通訊端選項 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="b3d62-850">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="b3d62-851">實 pwritev 函式 (在上傳檔案至 nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="b3d62-851">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="b3d62-852">已新增 IP 通訊端選項 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="b3d62-852">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="b3d62-853">支援通訊端選項 IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b3d62-853">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="b3d62-854">已新增適用于應用程式節點、追蹤路由、發掘、nslookup、主機的 IP (V6) _MTU 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="b3d62-854">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="b3d62-855">已新增 IP 通訊端選項 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="b3d62-855">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="b3d62-856">檔案系統改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-856">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="b3d62-857">允許裝載 UNC 路徑</span><span class="sxs-lookup"><span data-stu-id="b3d62-857">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="b3d62-858">在 drvfs 中啟用 CDFS.SYS 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-858">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="b3d62-859">在 drvfs 中正確處理網路檔案系統的許可權</span><span class="sxs-lookup"><span data-stu-id="b3d62-859">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="b3d62-860">將遠端磁片磁碟機的支援新增至 drvfs</span><span class="sxs-lookup"><span data-stu-id="b3d62-860">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="b3d62-861">在 drvfs 中啟用 FAT 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-861">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="b3d62-862">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-862">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-863">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="b3d62-863">LTP Results</span></span>
<span data-ttu-id="b3d62-864">自15042開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-864">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="b3d62-865">組建16170</span><span class="sxs-lookup"><span data-stu-id="b3d62-865">Build 16170</span></span>

<span data-ttu-id="b3d62-866">如需組建16170的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-866">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="b3d62-867">我們發行了新的[blog 文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), 討論我們對測試 WSL 的努力。</span><span class="sxs-lookup"><span data-stu-id="b3d62-867">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-868">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-868">Fixed</span></span>

- <span data-ttu-id="b3d62-869">支援通訊端選項 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b3d62-869">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="b3d62-870">新增對 PTRACE_OLDSETOPTIONS 的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-870">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="b3d62-871">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="b3d62-871">[GH 1692]</span></span>
- <span data-ttu-id="b3d62-872">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-872">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-873">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="b3d62-873">LTP Results</span></span>
<span data-ttu-id="b3d62-874">自15042開始沒有任何變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-874">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="b3d62-875">組建15046至 Windows 10 建立者更新</span><span class="sxs-lookup"><span data-stu-id="b3d62-875">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="b3d62-876">尚未規劃要加入 Windows 10 的建立者更新中的 WSL 修正或功能。</span><span class="sxs-lookup"><span data-stu-id="b3d62-876">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="b3d62-877">WSL 的版本資訊將會在接下來的幾周內繼續, 以供下一個主要 Windows Update 的新增目標。</span><span class="sxs-lookup"><span data-stu-id="b3d62-877">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="b3d62-878">如需組建15046和未來 Insider 版本的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-878">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="b3d62-879">組建15042</span><span class="sxs-lookup"><span data-stu-id="b3d62-879">Build 15042</span></span>

<span data-ttu-id="b3d62-880">如需組建15042的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-880">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-881">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-881">Fixed</span></span>

- <span data-ttu-id="b3d62-882">修正移除結尾為 "..." 的路徑時的鎖死</span><span class="sxs-lookup"><span data-stu-id="b3d62-882">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="b3d62-883">已修正 FIONBIO 未在成功時傳回0的問題 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="b3d62-883">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="b3d62-884">已修正長度為零的 inet 資料包通訊端讀取的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-884">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="b3d62-885">修正因 drvfs inode 查閱中的競爭條件而造成的可能鎖死 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="b3d62-885">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="b3d62-886">擴充對 unix 通訊端輔助資料的支援;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="b3d62-886">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="b3d62-887">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-887">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-888">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-888">LTP Results:</span></span>
<span data-ttu-id="b3d62-889">通過測試的數目:737</span><span class="sxs-lookup"><span data-stu-id="b3d62-889">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b3d62-890">非通過的數字 (失敗，所以已略過等等...):255</span><span class="sxs-lookup"><span data-stu-id="b3d62-890">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="b3d62-891">組建15031</span><span class="sxs-lookup"><span data-stu-id="b3d62-891">Build 15031</span></span>

<span data-ttu-id="b3d62-892">如需組建15031的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-892">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-893">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-893">Fixed</span></span>

- <span data-ttu-id="b3d62-894">已修正時間 (2) 偶爾會行為失常的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3d62-894">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="b3d62-895">已修正併發出 \* SIGPROCMASK syscalls 可能會損毀信號遮罩的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-895">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="b3d62-896">現在, 在 WSL 進程建立通知中傳回完整的命令列長度。</span><span class="sxs-lookup"><span data-stu-id="b3d62-896">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="b3d62-897">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="b3d62-897">[GH 1632]</span></span>
- <span data-ttu-id="b3d62-898">WSL 現在會透過 ptrace 來報告執行緒結束, 以 GDB 停止回應。</span><span class="sxs-lookup"><span data-stu-id="b3d62-898">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="b3d62-899">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="b3d62-899">[GH 1196]</span></span>
- <span data-ttu-id="b3d62-900">已修正 ptys 在大量 tmux IO 後停止回應的 bug。</span><span class="sxs-lookup"><span data-stu-id="b3d62-900">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="b3d62-901">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="b3d62-901">[GH 1358]</span></span>
- <span data-ttu-id="b3d62-902">已修正許多系統呼叫中的超時驗證 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)</span><span class="sxs-lookup"><span data-stu-id="b3d62-902">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="b3d62-903">已新增 eventfd EFD_SEMAPHORE 支援 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b3d62-903">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="b3d62-904">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-904">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-905">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-905">LTP Results:</span></span>
<span data-ttu-id="b3d62-906">通過測試的數目:737</span><span class="sxs-lookup"><span data-stu-id="b3d62-906">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b3d62-907">非通過的數字 (失敗，所以已略過等等...):255</span><span class="sxs-lookup"><span data-stu-id="b3d62-907">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3d62-908">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-908">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="b3d62-909">組建15025</span><span class="sxs-lookup"><span data-stu-id="b3d62-909">Build 15025</span></span>

<span data-ttu-id="b3d62-910">如需組建15025的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-910">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-911">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-911">Fixed</span></span>

- <span data-ttu-id="b3d62-912">修正中斷 grep 2.27 [GH 1578] 的 bug</span><span class="sxs-lookup"><span data-stu-id="b3d62-912">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="b3d62-913">Eventfd2 syscall 的實 EFD_SEMAPHORE 旗標 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b3d62-913">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="b3d62-914">實/proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="b3d62-914">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="b3d62-915">Unix 串流通訊端的信號驅動 IO 支援 [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="b3d62-915">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="b3d62-916">支援 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="b3d62-916">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="b3d62-917">執行 recvmmsg () syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="b3d62-917">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="b3d62-918">已修正 epoll_wait () 未等候的錯誤 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="b3d62-918">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="b3d62-919">執行/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="b3d62-919">Implement /proc/version_signature</span></span>
- <span data-ttu-id="b3d62-920">如果兩個檔案描述元都參考相同的管道, 則 t a syscall 現在會傳回失敗</span><span class="sxs-lookup"><span data-stu-id="b3d62-920">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="b3d62-921">已為 Unix 通訊端的 SO_PEERCRED 實作為正確行為</span><span class="sxs-lookup"><span data-stu-id="b3d62-921">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="b3d62-922">已修正 tkill syscall 不正確參數處理</span><span class="sxs-lookup"><span data-stu-id="b3d62-922">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="b3d62-923">增加 drvfs preformace 的變更</span><span class="sxs-lookup"><span data-stu-id="b3d62-923">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="b3d62-924">Ruby IO 封鎖的次要修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-924">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="b3d62-925">已修正 recvmsg () 針對 inet 通訊端的 MSG_DONTWAIT 旗標傳回 EINVAL [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="b3d62-925">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="b3d62-926">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-926">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-927">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-927">LTP Results:</span></span>
<span data-ttu-id="b3d62-928">通過測試的數目:732</span><span class="sxs-lookup"><span data-stu-id="b3d62-928">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="b3d62-929">非通過的數字 (失敗，所以已略過等等...):255</span><span class="sxs-lookup"><span data-stu-id="b3d62-929">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3d62-930">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-930">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="b3d62-931">組建15019</span><span class="sxs-lookup"><span data-stu-id="b3d62-931">Build 15019</span></span>

<span data-ttu-id="b3d62-932">如需組建15019的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-932">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-933">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-933">Fixed</span></span>

- <span data-ttu-id="b3d62-934">已修正不正確回報 procfs for htop (GH 823, 945, 971) 等工具的 CPU 使用量錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d62-934">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="b3d62-935">在現有檔案上以 O_TRUNC 呼叫 open () 時, inotifypropertychanged 現在會在 IN_OPEN 之前產生 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b3d62-935">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="b3d62-936">修正 unix 通訊端 getsockopt SO_ERROR 以啟用 postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="b3d62-936">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="b3d62-937">執行 GO 語言的/proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="b3d62-937">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="b3d62-938">Apt-取得套件更新背景工作現在會從 view 隱藏執行</span><span class="sxs-lookup"><span data-stu-id="b3d62-938">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="b3d62-939">清除 ipv6 localhost (春季 (JAVA) 失敗) 的範圍。</span><span class="sxs-lookup"><span data-stu-id="b3d62-939">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="b3d62-940">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-940">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-941">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-941">LTP Results:</span></span>
<span data-ttu-id="b3d62-942">通過測試的數目:714</span><span class="sxs-lookup"><span data-stu-id="b3d62-942">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="b3d62-943">非通過的數字 (失敗，所以已略過等等...):249</span><span class="sxs-lookup"><span data-stu-id="b3d62-943">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="b3d62-944">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-944">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="b3d62-945">組建15014</span><span class="sxs-lookup"><span data-stu-id="b3d62-945">Build 15014</span></span>

<span data-ttu-id="b3d62-946">如需組建15014的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-946">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-947">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-947">Fixed</span></span>

- <span data-ttu-id="b3d62-948">Ctrl + C 現在可如預期運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-948">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="b3d62-949">htop 和 ps auxw 現在會顯示正確的資源使用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="b3d62-949">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="b3d62-950">NT 例外狀況與信號的基本轉譯。</span><span class="sxs-lookup"><span data-stu-id="b3d62-950">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="b3d62-951">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="b3d62-951">(GH #513)</span></span>
- <span data-ttu-id="b3d62-952">fallocate 現在會在空間用盡 (而非 EINVAL (GH #1571) 時失敗, 並出現 ENOSPC</span><span class="sxs-lookup"><span data-stu-id="b3d62-952">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="b3d62-953">已新增/proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="b3d62-953">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="b3d62-954">執行 semop 和 semtimedop 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="b3d62-954">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="b3d62-955">已修正使用 IP_RECVTOS & IPV6_RECVTCLASS 通訊端選項 (GH 69) 的 nslookup 錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d62-955">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="b3d62-956">支援通訊端選項 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="b3d62-956">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="b3d62-957">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-957">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-958">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-958">LTP Results:</span></span>
<span data-ttu-id="b3d62-959">通過測試的數目:709</span><span class="sxs-lookup"><span data-stu-id="b3d62-959">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b3d62-960">非通過的數字 (失敗，所以已略過等等...):255</span><span class="sxs-lookup"><span data-stu-id="b3d62-960">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3d62-961">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-961">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="b3d62-962">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="b3d62-962">Syscall Summary</span></span>
<span data-ttu-id="b3d62-963">總 Syscalls:384</span><span class="sxs-lookup"><span data-stu-id="b3d62-963">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="b3d62-964">已實行總數:235</span><span class="sxs-lookup"><span data-stu-id="b3d62-964">Total Implemented: 235</span></span> </br>
<span data-ttu-id="b3d62-965">總 Stub:22</span><span class="sxs-lookup"><span data-stu-id="b3d62-965">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="b3d62-966">未實現的總計:127</span><span class="sxs-lookup"><span data-stu-id="b3d62-966">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="b3d62-967">詳細細目</span><span class="sxs-lookup"><span data-stu-id="b3d62-967">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="b3d62-968">組建15007</span><span class="sxs-lookup"><span data-stu-id="b3d62-968">Build 15007</span></span>

<span data-ttu-id="b3d62-969">如需組建15007的一般 Windows 資訊, 請造訪[Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-969">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b3d62-970">已知問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-970">Known Issue</span></span>

- <span data-ttu-id="b3d62-971">有一個已知的錯誤, 主控台無法辨識某些 Ctrl + <key>輸入。</span><span class="sxs-lookup"><span data-stu-id="b3d62-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b3d62-972">這包括將做為一般 ' c ' 按鍵動作的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="b3d62-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b3d62-973">因應措施：將其他索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="b3d62-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b3d62-974">例如, 若要將 Ctrl + K 對應到 Ctrl + C, `stty intr \^k`請執行:。</span><span class="sxs-lookup"><span data-stu-id="b3d62-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b3d62-975">這是每個終端機的對應, 必須在*每*次啟動 bash 時完成。</span><span class="sxs-lookup"><span data-stu-id="b3d62-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b3d62-976">使用者可以流覽選項, 將此包含在其`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="b3d62-976">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-977">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-977">Fixed</span></span>

- <span data-ttu-id="b3d62-978">已更正執行 WSL 耗用 100% CPU 核心的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-978">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="b3d62-979">通訊端選項 IP_PKTINFO, 現在支援 IPV6_RECVPKTINFO。</span><span class="sxs-lookup"><span data-stu-id="b3d62-979">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="b3d62-980">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="b3d62-980">(GH #851, 987)</span></span>
- <span data-ttu-id="b3d62-981">在 lxcore 中截斷網路介面實體位址為16個位元組 (GH #1452、1414、1343、468、308)</span><span class="sxs-lookup"><span data-stu-id="b3d62-981">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="b3d62-982">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-982">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-983">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-983">LTP Results:</span></span>
<span data-ttu-id="b3d62-984">通過測試的數目:709</span><span class="sxs-lookup"><span data-stu-id="b3d62-984">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b3d62-985">非通過的數字 (失敗，所以已略過等等...):255</span><span class="sxs-lookup"><span data-stu-id="b3d62-985">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3d62-986">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-986">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="b3d62-987">組建15002</span><span class="sxs-lookup"><span data-stu-id="b3d62-987">Build 15002</span></span>

<span data-ttu-id="b3d62-988">如需組建15002的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-988">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b3d62-989">已知問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-989">Known Issue</span></span>

<span data-ttu-id="b3d62-990">兩個已知問題:</span><span class="sxs-lookup"><span data-stu-id="b3d62-990">Two known issues:</span></span>
- <span data-ttu-id="b3d62-991">有一個已知的錯誤, 主控台無法辨識某些 Ctrl + <key>輸入。</span><span class="sxs-lookup"><span data-stu-id="b3d62-991">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b3d62-992">這包括將做為一般 ' c ' 按鍵動作的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="b3d62-992">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b3d62-993">因應措施：將其他索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="b3d62-993">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b3d62-994">例如, 若要將 Ctrl + K 對應到 Ctrl + C, `stty intr \^k`請執行:。</span><span class="sxs-lookup"><span data-stu-id="b3d62-994">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b3d62-995">這是每個終端機的對應, 必須在*每*次啟動 bash 時完成。</span><span class="sxs-lookup"><span data-stu-id="b3d62-995">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b3d62-996">使用者可以流覽選項, 將此包含在其`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="b3d62-996">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="b3d62-997">當 WSL 正在執行時, 系統執行緒會耗用 100% 的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="b3d62-997">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="b3d62-998">根本原因已于內部解決和修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-998">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-999">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-999">Fixed</span></span>

- <span data-ttu-id="b3d62-1000">所有 bash 會話現在都必須在相同的許可權層級建立。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1000">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="b3d62-1001">嘗試在不同層級啟動會話將會遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1001">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="b3d62-1002">這表示系統管理員和非系統管理員的主控台無法同時執行。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1002">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="b3d62-1003">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1003">(GH #626)</span></span>
<br/>
- <span data-ttu-id="b3d62-1004">已執行下列 NETLINK_ROUTE 訊息 (需要 Windows 系統管理員)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1004">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="b3d62-1005">RTM_NEWADDR (支援`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1005">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="b3d62-1006">RTM_NEWROUTE (支援`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1006">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="b3d62-1007">RTM_DELADDR (支援`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1007">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="b3d62-1008">RTM_DELROUTE (支援`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1008">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="b3d62-1009">針對要更新的套件, 已排程的工作檢查將不再于計量付費連線上執行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1009">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="b3d62-1010">已修正管道停滯的錯誤, 亦即 bash-c "ls-alR/" |bash-c 「cat」 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1010">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b3d62-1011">已執行 TCP_KEEPCNT 通訊端選項 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1011">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="b3d62-1012">已實 IP_MTU_DISCOVER INET 通訊端選項 (GH #720、717、170、69)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1012">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="b3d62-1013">已移除舊版功能, 以使用 NT 路徑查閱從 init 執行 NT 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1013">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="b3d62-1014">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1014">(GH #1325)</span></span>
- <span data-ttu-id="b3d62-1015">/Dev/kmsg 的修正模式, 允許群組/其他讀取權限 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1015">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="b3d62-1016">實/proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1016">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="b3d62-1017">已更正處理開始時間顯示為年2432的錯誤 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1017">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="b3d62-1018">已將預設詞彙環境變數切換為 xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1018">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="b3d62-1019">修改處理常式分叉期間計算進程認可的方式。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1019">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="b3d62-1020">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1020">(GH #1286)</span></span>
- <span data-ttu-id="b3d62-1021">實/proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1021">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="b3d62-1022">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1022">(GH #1286)</span></span>
- <span data-ttu-id="b3d62-1023">已執行的/proc/net/route 檔案 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1023">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="b3d62-1024">已修正快捷方式名稱未正確當地語系化的錯誤 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1024">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="b3d62-1025">已修正不正確地驗證程式標頭的 elf 剖析邏輯必須小於 (或等於) PATH_MAX。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1025">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="b3d62-1026">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1026">(GH #1048)</span></span>
- <span data-ttu-id="b3d62-1027">已針對 procfs、sysfs、cgroupfs 和 binfmtfs 實 statfs 回呼 (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1027">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="b3d62-1028">已修正不會關閉的 AptPackageIndexUpdate 視窗 (GH #1184 也會在 GH #1193 中討論)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1028">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="b3d62-1029">已新增 ASLR 個性 ADDR_NO_RANDOMIZE 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1029">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="b3d62-1030">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1030">(GH #1148, 1128)</span></span>
- <span data-ttu-id="b3d62-1031">改善 PTRACE_GETSIGINFO (SIGSEGV), 以在 AV 期間適當的 gdb 堆疊追蹤 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1031">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="b3d62-1032">Patchelf 二進位檔的 Elf 剖析不會再失敗。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1032">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="b3d62-1033">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1033">(GH #471)</span></span>
- <span data-ttu-id="b3d62-1034">VPN DNS 已傳播至/etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1034">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="b3d62-1035">已改善 TCP 關閉以提供更可靠的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1035">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="b3d62-1036">(GH #610、616、1025、1335)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1036">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="b3d62-1037">當開啟太多檔案時, 現在會傳回正確的錯誤碼 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1037">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="b3d62-1038">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1038">(GH #1126, 2090)</span></span>
- <span data-ttu-id="b3d62-1039">Windows Audit 記錄現在會報告進程建立 Audit 中的映射名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1039">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="b3d62-1040">現在, 從 bash 視窗內啟動 bash 時, 正常地失敗</span><span class="sxs-lookup"><span data-stu-id="b3d62-1040">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="b3d62-1041">當 interop 無法存取 LxFs 下的工作目錄 (亦即 notepad.exe. .bashrc) 時, 新增錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b3d62-1041">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="b3d62-1042">已修正在 WSL 中截斷 Windows 路徑的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1042">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="b3d62-1043">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-1043">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1044">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1044">LTP Results:</span></span>
<span data-ttu-id="b3d62-1045">通過測試的數目:690</span><span class="sxs-lookup"><span data-stu-id="b3d62-1045">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="b3d62-1046">非通過的數字 (失敗，所以已略過等等...):274</span><span class="sxs-lookup"><span data-stu-id="b3d62-1046">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="b3d62-1047">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1047">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1048">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1048">Syscall Support</span></span>
<span data-ttu-id="b3d62-1049">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1049">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1050">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1050">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="b3d62-1051">組建14986</span><span class="sxs-lookup"><span data-stu-id="b3d62-1051">Build 14986</span></span>

<span data-ttu-id="b3d62-1052">如需組建14986的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1052">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1053">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1053">Fixed</span></span>

- <span data-ttu-id="b3d62-1054">已修正 Netlink 和 Pty Ioctl 的錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="b3d62-1054">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="b3d62-1055">核心版本現在會報告 4.4.0-43, 以與 Xenial 一致</span><span class="sxs-lookup"><span data-stu-id="b3d62-1055">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="b3d62-1056">當輸入導向 ' nul: ' (GH #1259) 時, Bash 現在會啟動</span><span class="sxs-lookup"><span data-stu-id="b3d62-1056">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="b3d62-1057">執行緒識別碼現在在 procfs 中正確地回報 (GH #967)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1057">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="b3d62-1058">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |Inotify_add_watch () 中現在支援 IN_ISDIR 旗標 () (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1058">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="b3d62-1059">執行 timer_create 和相關的系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1059">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="b3d62-1060">這會啟用 GHC 支援 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1060">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="b3d62-1061">已修正 ping 傳回 0.000 ms 時間的問題 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1061">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="b3d62-1062">開啟太多檔案時, 傳回正確的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1062">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="b3d62-1063">已修正 WSL 中的問題, 其中如果介面的硬體位址為 32-位元組 (例如 Teredo 介面), 則網路介面資料的 Netlink 要求會失敗, 並 EINVAL</span><span class="sxs-lookup"><span data-stu-id="b3d62-1063">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="b3d62-1064">請注意, Linux 「ip」公用程式包含一個 bug, 如果 WSL 報告32位元組的硬體位址, 它會損毀。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1064">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="b3d62-1065">這是「ip」中的錯誤 (bug), 而不是 WSL。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1065">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="b3d62-1066">「Ip」公用程式用來硬式編碼用來列印硬體位址的字串緩衝區長度, 而該緩衝區太小, 無法列印32位元組的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1066">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="b3d62-1067">其他修正和改善</span><span class="sxs-lookup"><span data-stu-id="b3d62-1067">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1068">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1068">LTP Results:</span></span>
<span data-ttu-id="b3d62-1069">通過測試的數目:669</span><span class="sxs-lookup"><span data-stu-id="b3d62-1069">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="b3d62-1070">非通過的數字 (失敗，所以已略過等等...):258</span><span class="sxs-lookup"><span data-stu-id="b3d62-1070">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b3d62-1071">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1071">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1072">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1072">Syscall Support</span></span>
<span data-ttu-id="b3d62-1073">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1073">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1074">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1074">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="b3d62-1075">組建14971</span><span class="sxs-lookup"><span data-stu-id="b3d62-1075">Build 14971</span></span>

<span data-ttu-id="b3d62-1076">如需組建14971的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1076">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1077">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1077">Fixed</span></span>

 - <span data-ttu-id="b3d62-1078">由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1078">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3d62-1079">定期排程的更新將會在下一版中繼續。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1079">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1080">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1080">LTP Results:</span></span>
<span data-ttu-id="b3d62-1081">不變更自14965</span><span class="sxs-lookup"><span data-stu-id="b3d62-1081">Unchanged from 14965</span></span> </br>
<span data-ttu-id="b3d62-1082">通過測試的數目:664</span><span class="sxs-lookup"><span data-stu-id="b3d62-1082">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3d62-1083">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1083">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1084">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1084">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="b3d62-1085">組建14965</span><span class="sxs-lookup"><span data-stu-id="b3d62-1085">Build 14965</span></span>

<span data-ttu-id="b3d62-1086">如需組建14965的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1086">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1087">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1087">Fixed</span></span>

- <span data-ttu-id="b3d62-1088">支援 Netlink 通訊端 NETLINK_ROUTE 通訊協定的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1088">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="b3d62-1089">啟用網路列舉的 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="b3d62-1089">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="b3d62-1090">如需詳細資訊, 請參閱我們的[WSL 網路功能 blog 文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1090">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="b3d62-1091">根據預設,/sbin 現在位於使用者的路徑中</span><span class="sxs-lookup"><span data-stu-id="b3d62-1091">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="b3d62-1092">NT 使用者路徑預設會附加至 WSL 路徑 (也就是您現在可以輸入 notepad.exe, 而不需要將 System32 新增至 Linux 路徑)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1092">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="b3d62-1093">已新增對/proc/sys/kernel/cap_last_cap 的支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1093">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="b3d62-1094">當目前的工作目錄包含非 ansi 字元 (GH #1254) 時, 現在可以從 WSL 啟動 NT 二進位檔</span><span class="sxs-lookup"><span data-stu-id="b3d62-1094">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="b3d62-1095">允許在中斷連線的 unix 資料流程通訊端上關機。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1095">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="b3d62-1096">已新增對 PR_GET_PDEATHSIG 的支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1096">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="b3d62-1097">已新增對 CLONE_PARENT 的支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1097">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="b3d62-1098">已修正管道停滯的錯誤, 亦即 bash-c "ls-alR/" |bash-c 「cat」 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1098">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b3d62-1099">處理要求以連接到目前的終端機。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1099">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="b3d62-1100">將/proc/<pid>/oom_score_adj 標記為可寫入。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1100">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="b3d62-1101">新增形式/sys/fs/cgroup 掛接資料夾。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1101">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="b3d62-1102">sched_setaffinity 應該傳回相似性位元遮罩的數目</span><span class="sxs-lookup"><span data-stu-id="b3d62-1102">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="b3d62-1103">修正不正確假設解譯器路徑長度不能超過64個字元的 ELF 驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1103">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="b3d62-1104">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1104">(GH #743)</span></span>
- <span data-ttu-id="b3d62-1105">開啟檔案描述元可以保持主控台視窗開啟 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1105">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="b3d62-1106">Fixeed 錯誤, 其中在目標名稱上以尾端斜線結尾的重新命名 () 失敗 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1106">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="b3d62-1107">執行/proc/net/dev 檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-1107">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="b3d62-1108">已修正 0.000 ms ping, 因為計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1108">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="b3d62-1109">實/proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1109">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="b3d62-1110">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1110">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1111">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1111">LTP Results:</span></span>
<span data-ttu-id="b3d62-1112">通過測試的數目:664</span><span class="sxs-lookup"><span data-stu-id="b3d62-1112">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3d62-1113">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1113">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1114">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1114">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="b3d62-1115">組建14959</span><span class="sxs-lookup"><span data-stu-id="b3d62-1115">Build 14959</span></span>

<span data-ttu-id="b3d62-1116">如需組建14959的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1116">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1117">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1117">Fixed</span></span>

- <span data-ttu-id="b3d62-1118">改善 Windows 的 Pico 流程通知。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1118">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="b3d62-1119">在[WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)上找到的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1119">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="b3d62-1120">改善 Windows 互通性的穩定性</span><span class="sxs-lookup"><span data-stu-id="b3d62-1120">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="b3d62-1121">已修正在啟用企業資料保護 (EDP) 時啟動 bash 時的錯誤0x80070057</span><span class="sxs-lookup"><span data-stu-id="b3d62-1121">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="b3d62-1122">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1122">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1123">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1123">LTP Results:</span></span>
<span data-ttu-id="b3d62-1124">通過測試的數目:665</span><span class="sxs-lookup"><span data-stu-id="b3d62-1124">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3d62-1125">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1125">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1126">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1126">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="b3d62-1127">組建14955</span><span class="sxs-lookup"><span data-stu-id="b3d62-1127">Build 14955</span></span>

<span data-ttu-id="b3d62-1128">如需組建14955的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1128">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1129">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1129">Fixed</span></span>

 - <span data-ttu-id="b3d62-1130">由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1130">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3d62-1131">定期排程的更新將會在下一版中繼續。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1131">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1132">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1132">LTP Results:</span></span>
<span data-ttu-id="b3d62-1133">通過測試的數目:665</span><span class="sxs-lookup"><span data-stu-id="b3d62-1133">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3d62-1134">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1134">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1135">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1135">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="b3d62-1136">組建14951</span><span class="sxs-lookup"><span data-stu-id="b3d62-1136">Build 14951</span></span>

<span data-ttu-id="b3d62-1137">如需組建14951的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1137">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="b3d62-1138">新功能:Windows/Ubuntu 互通性</span><span class="sxs-lookup"><span data-stu-id="b3d62-1138">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="b3d62-1139">現在可以直接從 WSL 命令列叫用 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1139">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="b3d62-1140">這讓使用者能夠以不可行的方式與其 Windows 環境和系統互動。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1140">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="b3d62-1141">作為快速範例, 使用者現在可以執行下列命令:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1141">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="b3d62-1142">如需詳細資訊, 請參閱:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1142">More information can be found at:</span></span>

- [<span data-ttu-id="b3d62-1143">WSL 適用于 Interop 的小組 Blog</span><span class="sxs-lookup"><span data-stu-id="b3d62-1143">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="b3d62-1144">MSDN Interop 檔</span><span class="sxs-lookup"><span data-stu-id="b3d62-1144">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1145">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1145">Fixed</span></span>

- <span data-ttu-id="b3d62-1146">現在已針對所有新的 WSL 實例安裝 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1146">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="b3d62-1147">將不會自動升級具有現有 14.04 (Trusty) 實例的使用者。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1147">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="b3d62-1148">現在會顯示在安裝期間設定的地區設定</span><span class="sxs-lookup"><span data-stu-id="b3d62-1148">Locale set during install is now displayed</span></span>
- <span data-ttu-id="b3d62-1149">終端機改善, 包括將 WSL 程式重新導向至檔案的 bug, 不一定都能運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1149">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="b3d62-1150">主控台存留期應該系結至 bash 存留期</span><span class="sxs-lookup"><span data-stu-id="b3d62-1150">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="b3d62-1151">主控台視窗大小應使用可見大小, 而不是緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="b3d62-1151">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="b3d62-1152">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1152">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1153">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1153">LTP Results:</span></span>
<span data-ttu-id="b3d62-1154">通過測試的數目:665</span><span class="sxs-lookup"><span data-stu-id="b3d62-1154">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3d62-1155">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1155">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1156">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1156">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="b3d62-1157">組建14946</span><span class="sxs-lookup"><span data-stu-id="b3d62-1157">Build 14946</span></span>

<span data-ttu-id="b3d62-1158">如需組建14946的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1158">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1159">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1159">Fixed</span></span>

- <span data-ttu-id="b3d62-1160">已修正無法為包含空格或引號的 NT 使用者名稱建立 WSL 使用者帳戶的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1160">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="b3d62-1161">變更 VolFs 和 DrvFs, 使其在 stat 中針對目錄的連結計數傳回0</span><span class="sxs-lookup"><span data-stu-id="b3d62-1161">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="b3d62-1162">支援 IPV6_MULTICAST_HOPS 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1162">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="b3d62-1163">限制每個 tty 的單一主控台 i/o 迴圈。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1163">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="b3d62-1164">範例: 以下是可能的命令:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1164">Example: the following command is possible:</span></span>
  - <span data-ttu-id="b3d62-1165">bash-c "echo data" |bash-c "ssh user@example.com ' cat > foo .txt '"</span><span class="sxs-lookup"><span data-stu-id="b3d62-1165">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="b3d62-1166">以/proc/cpuinfo 中的索引標籤取代空格 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1166">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="b3d62-1167">DrvFs 現在會出現在 mountinfo 中, 名稱符合已掛接的 Windows 磁片區</span><span class="sxs-lookup"><span data-stu-id="b3d62-1167">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="b3d62-1168">/home 和/root 現在會以正確的名稱出現在 mountinfo 中</span><span class="sxs-lookup"><span data-stu-id="b3d62-1168">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="b3d62-1169">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1169">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1170">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1170">LTP Results:</span></span>
<span data-ttu-id="b3d62-1171">通過測試的數目:665</span><span class="sxs-lookup"><span data-stu-id="b3d62-1171">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3d62-1172">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1172">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1173">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1173">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="b3d62-1174">組建14942</span><span class="sxs-lookup"><span data-stu-id="b3d62-1174">Build 14942</span></span>

<span data-ttu-id="b3d62-1175">如需組建14942的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1175">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1176">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1176">Fixed</span></span>

- <span data-ttu-id="b3d62-1177">有一些錯誤的錯誤處理, 包括「嘗試執行 NOEXECUTE 記憶體」網路損毀, 但封鎖了 SSH</span><span class="sxs-lookup"><span data-stu-id="b3d62-1177">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="b3d62-1178">DrvFs 上 Windows 應用程式所產生之通知的 inotifiy 支援現已推出</span><span class="sxs-lookup"><span data-stu-id="b3d62-1178">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="b3d62-1179">執行 mongod.exe 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1179">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="b3d62-1180">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1180">(GH #695)</span></span>
- <span data-ttu-id="b3d62-1181">執行 pivot_root 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="b3d62-1181">Implement the pivot_root system call</span></span>
- <span data-ttu-id="b3d62-1182">SO_DONTROUTE 的執行通訊端選項</span><span class="sxs-lookup"><span data-stu-id="b3d62-1182">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="b3d62-1183">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1183">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="b3d62-1184">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1184">LTP Results:</span></span>
<span data-ttu-id="b3d62-1185">通過測試的數目:665</span><span class="sxs-lookup"><span data-stu-id="b3d62-1185">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3d62-1186">非通過的數字 (失敗，所以已略過等等...):263</span><span class="sxs-lookup"><span data-stu-id="b3d62-1186">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3d62-1187">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1187">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1188">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1188">Syscall Support</span></span>
<span data-ttu-id="b3d62-1189">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1189">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1190">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1190">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="b3d62-1191">組建14936</span><span class="sxs-lookup"><span data-stu-id="b3d62-1191">Build 14936</span></span>

<span data-ttu-id="b3d62-1192">如需組建14936的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1192">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="b3d62-1193">注意:WSL 將會在即將推出的版本中安裝 Ubuntu 版本 16.04 (Xenial), 而不是 Ubuntu 14.04 (Trusty)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1193">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="b3d62-1194">這項變更將適用于安裝新實例 (lxrun/install 或第一次執行 bash) 的內部人員。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1194">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="b3d62-1195">具有 Trusty 的現有實例將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1195">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="b3d62-1196">使用者可以使用 [發行-升級] 命令, 將其 Trusty 映射升級至 Xenial。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1196">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="b3d62-1197">已知問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1197">Known Issue</span></span>
<span data-ttu-id="b3d62-1198">WSL 遇到一些通訊端執行問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1198">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="b3d62-1199">檢查錯誤會將本身視為損毀, 並出現「嘗試執行 NOEXECUTE 記憶體」錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1199">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="b3d62-1200">此問題最常見的表現是使用 ssh 時的損毀。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1200">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="b3d62-1201">內部組建已修正根本原因, 並會以最早的機會將其推送給內部人員。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1201">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-1202">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1202">Fixed</span></span>

- <span data-ttu-id="b3d62-1203">執行 chroot 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="b3d62-1203">Implemented the chroot system call</span></span>
- <span data-ttu-id="b3d62-1204">Inotifypropertychanged 的改良功能~~, 包括支援 DrvFs 上的 Windows 應用程式所產生的通知~~</span><span class="sxs-lookup"><span data-stu-id="b3d62-1204">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="b3d62-1205">更正Inotifypropertychanged 對於源自 Windows 應用程式的變更, 目前不提供支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1205">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="b3d62-1206">通訊端系結至 IPV6<port n> :: 現在支援 IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1206">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="b3d62-1207">已實 WNOWAIT waitid systemcall 的行為 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1207">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="b3d62-1208">支援 IP 通訊端選項 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="b3d62-1208">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="b3d62-1209">長度為零的讀取 () 應立即傳回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1209">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="b3d62-1210">正確處理檔案名和檔案名前置詞, 這些前置詞不會在. tar 檔案中包含 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1210">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="b3d62-1211">/dev/null 的 epoll 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1211">epoll support for /dev/null</span></span>
- <span data-ttu-id="b3d62-1212">修正/dev/alarm 時間來源</span><span class="sxs-lookup"><span data-stu-id="b3d62-1212">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="b3d62-1213">Bash-c 現在可以重新導向至檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-1213">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="b3d62-1214">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1214">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1215">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1215">LTP Results:</span></span>
<span data-ttu-id="b3d62-1216">通過測試的數目:664</span><span class="sxs-lookup"><span data-stu-id="b3d62-1216">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3d62-1217">非通過的數字 (失敗，所以已略過等等...):264</span><span class="sxs-lookup"><span data-stu-id="b3d62-1217">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="b3d62-1218">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1219">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1219">Syscall Support</span></span>
<span data-ttu-id="b3d62-1220">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1220">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1221">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1221">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="b3d62-1222">組建14931</span><span class="sxs-lookup"><span data-stu-id="b3d62-1222">Build 14931</span></span>

<span data-ttu-id="b3d62-1223">如需組建14931的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1223">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1224">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1224">Fixed</span></span>

 - <span data-ttu-id="b3d62-1225">由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1225">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3d62-1226">定期排程的更新將會在下一版中繼續。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1226">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="b3d62-1227">組建14926</span><span class="sxs-lookup"><span data-stu-id="b3d62-1227">Build 14926</span></span>

<span data-ttu-id="b3d62-1228">如需組建14926的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1228">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1229">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1229">Fixed</span></span>

- <span data-ttu-id="b3d62-1230">Ping 現在適用于沒有系統管理員許可權的主控台</span><span class="sxs-lookup"><span data-stu-id="b3d62-1230">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="b3d62-1231">現在也支援 Ping6, 而且沒有系統管理員許可權</span><span class="sxs-lookup"><span data-stu-id="b3d62-1231">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="b3d62-1232">Inotifypropertychanged 支援透過 WSL 修改的檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1232">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="b3d62-1233">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1233">(GH #216)</span></span>
  - <span data-ttu-id="b3d62-1234">支援的旗標:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1234">Flags supported:</span></span>
    - <span data-ttu-id="b3d62-1235">inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="b3d62-1235">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="b3d62-1236">inotify_add_watch 事件:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="b3d62-1236">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="b3d62-1237">inotify_add_watch 屬性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="b3d62-1237">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="b3d62-1238">讀取輸出:LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="b3d62-1238">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="b3d62-1239">已知問題:從 Windows 應用程式修改檔案並不會產生任何事件</span><span class="sxs-lookup"><span data-stu-id="b3d62-1239">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="b3d62-1240">Unix 通訊端現在支援 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="b3d62-1240">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3d62-1241">LTP 結果:</span><span class="sxs-lookup"><span data-stu-id="b3d62-1241">LTP Results:</span></span>
<span data-ttu-id="b3d62-1242">通過測試的數目:651</span><span class="sxs-lookup"><span data-stu-id="b3d62-1242">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="b3d62-1243">非通過的數字 (失敗，所以已略過等等...):258</span><span class="sxs-lookup"><span data-stu-id="b3d62-1243">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b3d62-1244">LTP 測試回合記錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1244">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="b3d62-1245">組建14915</span><span class="sxs-lookup"><span data-stu-id="b3d62-1245">Build 14915</span></span>

<span data-ttu-id="b3d62-1246">如需組建14915的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1246">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1247">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1247">Fixed</span></span>
-  <span data-ttu-id="b3d62-1248">Socketpair for unix 資料包通訊端 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1248">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="b3d62-1249">適用于 SO_REUSEADDR 的 Unix 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1249">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="b3d62-1250">適用于 SO_BROADCAST 的 UNIX 通訊端支援 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1250">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="b3d62-1251">適用于 SOCK_SEQPACKET 的 Unix 通訊端支援 (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1251">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="b3d62-1252">新增對 unix 資料包通訊端傳送、接收和關閉的支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1252">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="b3d62-1253">修正錯誤檢查, 因為非固定位址的 mmap 參數驗證無效。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1253">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="b3d62-1254">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1254">(GH #847)</span></span>
- <span data-ttu-id="b3d62-1255">支援終止/繼續終端機狀態</span><span class="sxs-lookup"><span data-stu-id="b3d62-1255">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="b3d62-1256">支援 TIOCPKT ioctl 來解除封鎖螢幕公用程式 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1256">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="b3d62-1257">已知問題:功能鍵無法運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1257">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="b3d62-1258">已更正 TimerFd 中可能造成 LxpTimerFdWorkerRoutine (GH #814) 存取已釋放成員 ' ReaderReady ' 的競爭</span><span class="sxs-lookup"><span data-stu-id="b3d62-1258">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="b3d62-1259">啟用 futex、輪詢和 clock_nanosleep 的可重新開機系統呼叫支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1259">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="b3d62-1260">已新增 bind 掛接支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1260">Added bind mount support</span></span>
- <span data-ttu-id="b3d62-1261">掛接命名空間支援的取消共用</span><span class="sxs-lookup"><span data-stu-id="b3d62-1261">unshare for mount namespace support</span></span>
    - <span data-ttu-id="b3d62-1262">已知問題:使用`unshare(CLONE_NEWNS)`目前的工作目錄建立新的掛接命名空間時, 將會繼續指向舊的命名空間</span><span class="sxs-lookup"><span data-stu-id="b3d62-1262">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="b3d62-1263">其他改良功能和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-1263">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="b3d62-1264">組建14905</span><span class="sxs-lookup"><span data-stu-id="b3d62-1264">Build 14905</span></span>

<span data-ttu-id="b3d62-1265">如需組建14905的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1265">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1266">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1266">Fixed</span></span>
- <span data-ttu-id="b3d62-1267">現在支援可重新開機的系統呼叫 (GH #349、GH #520)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1267">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="b3d62-1268">符號連結至結尾為/現在可運作的目錄 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1268">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="b3d62-1269">已針對/dev/random 執行 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="b3d62-1269">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="b3d62-1270">執行/proc/[pid]/mounts,/proc/[pid]/mountinfo 和/proc/[pid]/mountstats 檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-1270">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="b3d62-1271">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1271">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="b3d62-1272">組建14901</span><span class="sxs-lookup"><span data-stu-id="b3d62-1272">Build 14901</span></span>
<span data-ttu-id="b3d62-1273">Windows 10 年度更新版文章的第一個 Insider 組建。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1273">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="b3d62-1274">如需組建14901的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1274">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1275">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1275">Fixed</span></span>
- <span data-ttu-id="b3d62-1276">已修正結尾斜線問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1276">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="b3d62-1277">現在可以使用`$ mv a/c/ a/b/`的命令</span><span class="sxs-lookup"><span data-stu-id="b3d62-1277">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="b3d62-1278">如果 Ubuntu 地區設定應設為 Windows locale, 現在安裝會提示</span><span class="sxs-lookup"><span data-stu-id="b3d62-1278">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="b3d62-1279">Ns 資料夾的 Procfs 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1279">Procfs support for ns folder</span></span>
- <span data-ttu-id="b3d62-1280">新增 tmpfs、procfs 和 sysfs 檔案系統的掛接和卸載</span><span class="sxs-lookup"><span data-stu-id="b3d62-1280">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="b3d62-1281">修正 mknod [at] 32 位 ABI 簽名</span><span class="sxs-lookup"><span data-stu-id="b3d62-1281">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="b3d62-1282">Unix 通訊端已移至分派模型</span><span class="sxs-lookup"><span data-stu-id="b3d62-1282">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="b3d62-1283">應接受使用 setsockopt 設定的 INET 通訊端接收緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="b3d62-1283">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="b3d62-1284">執行 MSG_CMSG_CLOEXEC unix 通訊端接收訊息旗標</span><span class="sxs-lookup"><span data-stu-id="b3d62-1284">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="b3d62-1285">Linux 進程 stdin/stdout 管道重新導向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1285">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="b3d62-1286">允許在 CMD 中進行 bash-c 命令的管線。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1286">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="b3d62-1287">範例: > dir |bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="b3d62-1287">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="b3d62-1288">Bash 現在可以安裝在具有多個頁面的系統上 (GH #538、#358)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1288">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="b3d62-1289">預設 INET 通訊端緩衝區大小應符合預設 Ubuntu 安裝程式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1289">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="b3d62-1290">將 xattr syscalls 對齊 listxattr</span><span class="sxs-lookup"><span data-stu-id="b3d62-1290">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="b3d62-1291">僅從 SIOCGIFCONF 傳回具有有效 IPv4 位址的介面</span><span class="sxs-lookup"><span data-stu-id="b3d62-1291">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="b3d62-1292">修正 ptrace 插入時的信號預設動作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1292">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="b3d62-1293">執行/proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="b3d62-1293">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="b3d62-1294">還原 sigreturn 中的內容時使用機器內容暫存器值</span><span class="sxs-lookup"><span data-stu-id="b3d62-1294">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="b3d62-1295">這可解決某些使用者的 java 和 javac 已懸掛的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1295">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="b3d62-1296">執行/proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="b3d62-1296">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1297">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1297">Syscall Support</span></span>
<span data-ttu-id="b3d62-1298">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1298">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1299">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1299">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="b3d62-1300">組建14388至 Windows 10 年度更新版</span><span class="sxs-lookup"><span data-stu-id="b3d62-1300">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="b3d62-1301">如需組建14388的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1301">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1302">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1302">Fixed</span></span>
- <span data-ttu-id="b3d62-1303">修正在8/2 上準備 Windows 10 年度更新版</span><span class="sxs-lookup"><span data-stu-id="b3d62-1303">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="b3d62-1304">如需有關 WSL 的詳細資訊, 請參閱我們的[blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1304">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="b3d62-1305">組建14376</span><span class="sxs-lookup"><span data-stu-id="b3d62-1305">Build 14376</span></span>
<span data-ttu-id="b3d62-1306">如需組建14376的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1306">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1307">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1307">Fixed</span></span>
- <span data-ttu-id="b3d62-1308">移除某些 apt-get 停止回應的實例 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1308">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="b3d62-1309">已修正未正確處理空白裝載的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1309">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="b3d62-1310">已修正未正確裝載 ramdisks 的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1310">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="b3d62-1311">變更 unix 通訊端接受以支援旗標 (部分 GH #451)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1311">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="b3d62-1312">已修正一般網路相關的藍屏</span><span class="sxs-lookup"><span data-stu-id="b3d62-1312">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="b3d62-1313">已修正存取/proc/[pid]/task (GH #523) 時的藍屏</span><span class="sxs-lookup"><span data-stu-id="b3d62-1313">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="b3d62-1314">已針對某些 pty 案例 (GH #488、#504) 修正高 CPU 使用率</span><span class="sxs-lookup"><span data-stu-id="b3d62-1314">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="b3d62-1315">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1315">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="b3d62-1316">組建14371</span><span class="sxs-lookup"><span data-stu-id="b3d62-1316">Build 14371</span></span>
<span data-ttu-id="b3d62-1317">如需組建14371的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1317">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1318">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1318">Fixed</span></span>
- <span data-ttu-id="b3d62-1319">使用 ptrace 時, 以 SIGCHLD 和 wait () 更正計時競賽</span><span class="sxs-lookup"><span data-stu-id="b3d62-1319">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="b3d62-1320">已更正路徑具有尾端/(GH #432) 時的部分行為</span><span class="sxs-lookup"><span data-stu-id="b3d62-1320">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="b3d62-1321">已修正因為開啟子系的控制碼而導致重新命名/取消連結失敗的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1321">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="b3d62-1322">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1322">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="b3d62-1323">組建14366</span><span class="sxs-lookup"><span data-stu-id="b3d62-1323">Build 14366</span></span>
<span data-ttu-id="b3d62-1324">如需組建14366的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1324">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1325">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1325">Fixed</span></span>
- <span data-ttu-id="b3d62-1326">透過符號連結在檔案建立時修正</span><span class="sxs-lookup"><span data-stu-id="b3d62-1326">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="b3d62-1327">已新增 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1327">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="b3d62-1328">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1328">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1329">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1329">Syscall Support</span></span>
-   <span data-ttu-id="b3d62-1330">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1331">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="b3d62-1332">組建14361</span><span class="sxs-lookup"><span data-stu-id="b3d62-1332">Build 14361</span></span>
<span data-ttu-id="b3d62-1333">如需組建14361的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1333">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1334">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1334">Fixed</span></span>
- <span data-ttu-id="b3d62-1335">在 Windows 上 Ubuntu 的 Bash 中執行時, DrvFs 現在會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1335">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="b3d62-1336">使用者可能會有 .txt 和大小寫。/Mnt/c 磁片磁碟機上的 TXT</span><span class="sxs-lookup"><span data-stu-id="b3d62-1336">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="b3d62-1337">只有在 Windows 上 Ubuntu 的 Bash 中才支援區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1337">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="b3d62-1338">在 Bash NTFS 以外的地方, 會正確地報告檔案, 但是可能會發生非預期的行為, 與 Windows 中的檔案互動。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1338">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="b3d62-1339">每個磁片區的根目錄 (亦即/mnt/c) 不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b3d62-1339">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="b3d62-1340">如需如何在 Windows 中處理這些檔案的詳細資訊, 請參閱[這裡](https://support.microsoft.com/en-us/kb/100625)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1340">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="b3d62-1341">大幅增強的 pty/tty 支援。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1341">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="b3d62-1342">現在支援 TMUX 之類的應用程式 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1342">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="b3d62-1343">已修正不一定會建立使用者帳戶的安裝問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1343">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="b3d62-1344">優化的命令列 arg 結構, 允許非常長的引數清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1344">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="b3d62-1345">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1345">(GH #153)</span></span>
- <span data-ttu-id="b3d62-1346">現在可以從 DrvFs 刪除和 chmod read_only 檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-1346">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="b3d62-1347">已修正終端機在中斷連線時停止回應的某些實例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1347">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="b3d62-1348">chmod 和 chown 現在可以在 tty 裝置上執行</span><span class="sxs-lookup"><span data-stu-id="b3d62-1348">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="b3d62-1349">允許連接到0.0.0.0 和:: 作為 localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1349">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="b3d62-1350">Sendmsg/recvmsg 現在會處理 > 1 的 IO 向量長度 (部分 GH #376)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1350">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="b3d62-1351">使用者現在可以退出宣告自動產生的主機檔案 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1351">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="b3d62-1352">在安裝期間, 自動將 Linux 地區設定與 NT 地區設定進行比對 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1352">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="b3d62-1353">已新增/proc/sys/vm/swappiness 檔案 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1353">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="b3d62-1354">strace 現在已正確結束</span><span class="sxs-lookup"><span data-stu-id="b3d62-1354">strace now exits correctly</span></span>
- <span data-ttu-id="b3d62-1355">允許透過/proc/self/fd 重新開啟管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1355">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="b3d62-1356">隱藏%LOCALAPPDATA%\lxss from DrvFs 下的目錄 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1356">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="b3d62-1357">更好的 bash 處理。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1357">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="b3d62-1358">現在支援 "bash ~-c ls" 之類的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1358">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="b3d62-1359">通訊端現在會在關機期間通知 epoll 讀取可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1359">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="b3d62-1360">lxrun/uninstall 有更好的工作刪除檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="b3d62-1360">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="b3d62-1361">已更正 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1361">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="b3d62-1362">改良的 x11 應用程式支援, 例如 xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1362">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="b3d62-1363">已更新初始執行緒堆疊大小以符合預設 Ubuntu 設定, 並將大小正確地報告給 get_rlimit syscall (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1363">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="b3d62-1364">已改善 pico 進程映射名稱的報告 (例如, 用於審核)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1364">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="b3d62-1365">已針對 df 命令執行/proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="b3d62-1365">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="b3d62-1366">已修正子系名稱的符號式錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1366">Fixed symlink error code for child name .</span></span> <span data-ttu-id="b3d62-1367">和。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1367">and ..</span></span>
- <span data-ttu-id="b3d62-1368">其他改良功能的錯誤修正和改進</span><span class="sxs-lookup"><span data-stu-id="b3d62-1368">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1369">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1369">Syscall Support</span></span>
<span data-ttu-id="b3d62-1370">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1371">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="b3d62-1372">組建14352</span><span class="sxs-lookup"><span data-stu-id="b3d62-1372">Build 14352</span></span>
<span data-ttu-id="b3d62-1373">如需組建14352的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1373">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1374">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1374">Fixed</span></span>
- <span data-ttu-id="b3d62-1375">已修正未正確下載/建立大型檔案的問題。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1375">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="b3d62-1376">這應該會解除封鎖 npm 和其他案例 (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1376">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="b3d62-1377">移除通訊端停止回應的部分實例</span><span class="sxs-lookup"><span data-stu-id="b3d62-1377">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="b3d62-1378">已更正某些 ptrace 錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d62-1378">Corrected some ptrace errors</span></span>
- <span data-ttu-id="b3d62-1379">已修正 WSL 允許檔案名長度超過255個字元的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1379">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="b3d62-1380">改善非英文字元的支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1380">Improved support for non-English characters</span></span>
- <span data-ttu-id="b3d62-1381">新增目前的 Windows 時區資料並設定為預設值</span><span class="sxs-lookup"><span data-stu-id="b3d62-1381">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="b3d62-1382">每個掛接點的唯一裝置識別碼 (jre 修正程式– GH #49)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1382">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="b3d62-1383">更正包含 "." 之路徑的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1383">Correct issue with paths containing “.”</span></span> <span data-ttu-id="b3d62-1384">和 "..."</span><span class="sxs-lookup"><span data-stu-id="b3d62-1384">and “..”</span></span>
- <span data-ttu-id="b3d62-1385">已新增 Fifo 支援 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1385">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="b3d62-1386">已更新 resolv.conf 格式以符合原生 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1386">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="b3d62-1387">某些 procfs 清除</span><span class="sxs-lookup"><span data-stu-id="b3d62-1387">Some procfs cleanup</span></span>
- <span data-ttu-id="b3d62-1388">已啟用系統管理員主控台的 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="b3d62-1388">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1389">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1389">Syscall Support</span></span>
<span data-ttu-id="b3d62-1390">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1390">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1391">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1391">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="b3d62-1392">組建14342</span><span class="sxs-lookup"><span data-stu-id="b3d62-1392">Build 14342</span></span>
<span data-ttu-id="b3d62-1393">如需組建14342的一般 Windows 資訊, 請查看[Windows Blog](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1393">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="b3d62-1394">如需 VolFs 和 DriveFs 的資訊, 請參閱[WSL Blog](https://blogs.msdn.microsoft.com/wsl)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1394">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3d62-1395">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1395">Fixed</span></span>
- <span data-ttu-id="b3d62-1396">已修正 Windows 使用者在使用者名稱中具有 Unicode 字元時的安裝問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1396">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="b3d62-1397">常見問題中的 apt-get update udev 因應措施現在預設會在第一次執行時提供</span><span class="sxs-lookup"><span data-stu-id="b3d62-1397">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="b3d62-1398">已在 DriveFs (于/mnt/<drive>) 目錄中啟用符號連結</span><span class="sxs-lookup"><span data-stu-id="b3d62-1398">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="b3d62-1399">符號連結現在可在 DriveFs 和 VolFs 之間工作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1399">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="b3d62-1400">已解決最上層路徑剖析問題: ls.//現在會如預期般運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1400">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="b3d62-1401">DriveFs 上的 npm install 和-g 選項現在正在運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1401">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="b3d62-1402">已修正導致 PHP 伺服器無法啟動的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1402">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="b3d62-1403">已更新預設的環境值, 例如 $PATH 更接近原生 Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b3d62-1403">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="b3d62-1404">在 Windows 中新增每週維護工作以更新 apt 套件快取</span><span class="sxs-lookup"><span data-stu-id="b3d62-1404">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="b3d62-1405">已修正 ELF 標頭驗證的問題, WSL 現在支援所有 Melkor 選項</span><span class="sxs-lookup"><span data-stu-id="b3d62-1405">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="b3d62-1406">Zsh shell 功能正常</span><span class="sxs-lookup"><span data-stu-id="b3d62-1406">Zsh shell is functional</span></span>
- <span data-ttu-id="b3d62-1407">現在支援先行編譯的 Go 二進位檔</span><span class="sxs-lookup"><span data-stu-id="b3d62-1407">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="b3d62-1408">在 Bash 第一次執行時提示現在已正確當地語系化</span><span class="sxs-lookup"><span data-stu-id="b3d62-1408">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="b3d62-1409">/proc/meminfo 現在會傳回正確的資訊</span><span class="sxs-lookup"><span data-stu-id="b3d62-1409">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="b3d62-1410">VFS 現在支援的通訊端</span><span class="sxs-lookup"><span data-stu-id="b3d62-1410">Sockets now supported in VFS</span></span>
- <span data-ttu-id="b3d62-1411">/dev 現在掛接為 tempfs</span><span class="sxs-lookup"><span data-stu-id="b3d62-1411">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="b3d62-1412">現在支援 Fifo</span><span class="sxs-lookup"><span data-stu-id="b3d62-1412">Fifo now supported</span></span>
- <span data-ttu-id="b3d62-1413">多核心系統現在已正確地顯示在/proc/cpuinfo 中</span><span class="sxs-lookup"><span data-stu-id="b3d62-1413">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="b3d62-1414">第一次執行期間下載的其他改良功能和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b3d62-1414">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="b3d62-1415">Syscall 改良功能與錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1415">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b3d62-1416">支援的 syscall 清單如下。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1416">Supported syscall list below.</span></span>
- <span data-ttu-id="b3d62-1417">其他錯誤修正與改良功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1417">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="b3d62-1418">已知問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1418">Known Issues</span></span>
- <span data-ttu-id="b3d62-1419">未解析 ' ... '</span><span class="sxs-lookup"><span data-stu-id="b3d62-1419">Not resolving ‘..’</span></span> <span data-ttu-id="b3d62-1420">在某些情況下, 于 DriveFs 上正確運作</span><span class="sxs-lookup"><span data-stu-id="b3d62-1420">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1421">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1421">Syscall Support</span></span>
<span data-ttu-id="b3d62-1422">以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1422">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1423">這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1423">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="b3d62-1424">組建14332</span><span class="sxs-lookup"><span data-stu-id="b3d62-1424">Build 14332</span></span>

<span data-ttu-id="b3d62-1425">如需組建14332的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1425">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="b3d62-1426">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1426">Fixed</span></span>
- <span data-ttu-id="b3d62-1427">更好的 resolv.conf, 包括排列 DNS 專案的優先順序</span><span class="sxs-lookup"><span data-stu-id="b3d62-1427">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="b3d62-1428">在/mnt 與非/mnt 磁片磁碟機之間移動檔案和目錄的問題</span><span class="sxs-lookup"><span data-stu-id="b3d62-1428">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="b3d62-1429">現在可以使用符號連結來建立 Tar 檔案</span><span class="sxs-lookup"><span data-stu-id="b3d62-1429">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="b3d62-1430">已在建立實例時新增預設/run/lock 目錄</span><span class="sxs-lookup"><span data-stu-id="b3d62-1430">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="b3d62-1431">更新/dev/null 以傳回適當的 stat 資訊</span><span class="sxs-lookup"><span data-stu-id="b3d62-1431">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="b3d62-1432">第一次執行時下載的其他錯誤</span><span class="sxs-lookup"><span data-stu-id="b3d62-1432">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="b3d62-1433">Syscall 改良功能與錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1433">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b3d62-1434">支援的 syscall 清單如下。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1434">Supported syscall list below.</span></span>
- <span data-ttu-id="b3d62-1435">其他改良功能的錯誤修正和改進</span><span class="sxs-lookup"><span data-stu-id="b3d62-1435">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1436">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1436">Syscall Support</span></span>
<span data-ttu-id="b3d62-1437">以下是在 WSL 中有一些實作為的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1437">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="b3d62-1438">至少有一個案例支援此清單上的 syscall, 但目前不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1438">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="b3d62-1439">組建14328</span><span class="sxs-lookup"><span data-stu-id="b3d62-1439">Build 14328</span></span>

<span data-ttu-id="b3d62-1440">如需組建14332的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1440">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="b3d62-1441">新功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1441">New Features</span></span>
* <span data-ttu-id="b3d62-1442">現在支援 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1442">Now support Linux users.</span></span>  <span data-ttu-id="b3d62-1443">在 Windows 上的 Ubuntu 上安裝 Bash 時, 將會提示您建立 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1443">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="b3d62-1444">如需詳細資訊, 請造訪 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="b3d62-1444">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="b3d62-1445">主機名稱現在已設定為 Windows 電腦名稱稱, 不再有@localhost</span><span class="sxs-lookup"><span data-stu-id="b3d62-1445">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="b3d62-1446">如需組建14328的詳細資訊, 請造訪: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="b3d62-1446">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="b3d62-1447">固定式</span><span class="sxs-lookup"><span data-stu-id="b3d62-1447">Fixed</span></span>
* <span data-ttu-id="b3d62-1448">非于/mnt/<drive>檔案的符號的增強功能</span><span class="sxs-lookup"><span data-stu-id="b3d62-1448">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="b3d62-1449">npm install now works</span><span class="sxs-lookup"><span data-stu-id="b3d62-1449">npm install now works</span></span>
    * <span data-ttu-id="b3d62-1450">jdk/jre 現在可使用[這裡](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)找到的指示來安裝。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1450">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="b3d62-1451">已知問題: 符號連結不適用於 Windows 裝載。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1451">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="b3d62-1452">功能將在稍後的組建中提供</span><span class="sxs-lookup"><span data-stu-id="b3d62-1452">Functionality will be available in a later build</span></span>
* <span data-ttu-id="b3d62-1453">頂端和 htop 現在顯示</span><span class="sxs-lookup"><span data-stu-id="b3d62-1453">top and htop now display</span></span>
* <span data-ttu-id="b3d62-1454">某些安裝失敗的其他錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b3d62-1454">Additional error messages for some install failures</span></span>
* <span data-ttu-id="b3d62-1455">Syscall 改良功能與錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1455">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="b3d62-1456">支援的 syscall 清單如下。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1456">Supported syscall list below.</span></span>
* <span data-ttu-id="b3d62-1457">其他改良功能的錯誤修正和改進</span><span class="sxs-lookup"><span data-stu-id="b3d62-1457">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3d62-1458">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="b3d62-1458">Syscall Support</span></span>
<span data-ttu-id="b3d62-1459">以下是在 WSL 中有一些實作為 syscalls 的清單。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1459">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="b3d62-1460">至少有一個案例支援此清單上的 Syscalls, 但目前可能不支援所有參數。</span><span class="sxs-lookup"><span data-stu-id="b3d62-1460">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
