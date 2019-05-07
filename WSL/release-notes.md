---
title: 適用於 Linux 的 Windows 子系統的版本資訊
description: 適用於 Linux 的 Windows 子系統的版本資訊。  每週更新。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu 的 windows 子系統
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988256"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="19dda-105">適用於 Linux 的 Windows 子系統的版本資訊</span><span class="sxs-lookup"><span data-stu-id="19dda-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="19dda-106">建置 18890</span><span class="sxs-lookup"><span data-stu-id="19dda-106">Build 18890</span></span>
<span data-ttu-id="19dda-107">一般 Windows 組建 18890 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-108">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-108">WSL</span></span>
* <span data-ttu-id="19dda-109">非封鎖通訊端遺漏 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="19dda-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="19dda-110">終端機 EOF 輸入可能會封鎖後續的讀取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="19dda-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="19dda-111">更新 resolv.conf 標頭，指向 [述 GH 3928] wsl.conf</span><span class="sxs-lookup"><span data-stu-id="19dda-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="19dda-112">Epoll 刪除程式碼 [GH 3922] 中的死結</span><span class="sxs-lookup"><span data-stu-id="19dda-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="19dda-113">處理中的引數-匯入和 – 匯出 [GH 3932] 空間</span><span class="sxs-lookup"><span data-stu-id="19dda-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="19dda-114">擴充 mmap 會檔案無法正常運作 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="19dda-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="19dda-115">修正問題 ARM64 \\wsl$ 存取未正常運作</span><span class="sxs-lookup"><span data-stu-id="19dda-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="19dda-116">新增 wsl.exe 更好的預設圖示</span><span class="sxs-lookup"><span data-stu-id="19dda-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="19dda-117">建置 18342</span><span class="sxs-lookup"><span data-stu-id="19dda-117">Build 18342</span></span>
<span data-ttu-id="19dda-118">一般 Windows 組建 18342 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-119">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-119">WSL</span></span>
* <span data-ttu-id="19dda-120">我們已新增可讓使用者從 Windows 存取在 WSL 散發版本的 Linux 檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="19dda-121">這些檔案可以透過命令列，以及 Windows 應用程式，例如 [檔案總管] 中，VSCode，等等，都可以與這些檔案互動。</span><span class="sxs-lookup"><span data-stu-id="19dda-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="19dda-122">存取檔案，請瀏覽至\\ \\wsl$\\< distro_name >，或看到一份瀏覽至執行散發套件\\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="19dda-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="19dda-123">新增額外的 CPU 資訊標記，並修正 Cpus_allowed [清單 （_l)] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="19dda-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="19dda-124">支援從非領導者執行緒 [GH 3800] exec</span><span class="sxs-lookup"><span data-stu-id="19dda-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="19dda-125">設定更新失敗視為非嚴重 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="19dda-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="19dda-126">更新 binfmt 可正確處理位移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="19dda-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="19dda-127">計劃 9 [GH 3854] 啟用對應網路磁碟機</span><span class="sxs-lookup"><span data-stu-id="19dda-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="19dda-128">支援 Windows]-> [Linux 和 Linux]-> [繫結掛接的 Windows 路徑轉譯</span><span class="sxs-lookup"><span data-stu-id="19dda-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="19dda-129">建立唯讀的區段，對應上開啟的檔案唯讀</span><span class="sxs-lookup"><span data-stu-id="19dda-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="19dda-130">建置 18334</span><span class="sxs-lookup"><span data-stu-id="19dda-130">Build 18334</span></span>
<span data-ttu-id="19dda-131">一般 Windows 組建 18334 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-132">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-132">WSL</span></span>
* <span data-ttu-id="19dda-133">重新設計 Windows 時區會對應至 Linux 時間的時區 [GH 3747] 的方式</span><span class="sxs-lookup"><span data-stu-id="19dda-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="19dda-134">修正記憶體流失並新增新的字串翻譯函式 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="19dda-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="19dda-135">在任何執行緒的 threadgroup SIGCONT 是無作業 [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="19dda-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="19dda-136">正確地顯示 /proc/self/fd 中的 通訊端與 epoll 檔案描述項</span><span class="sxs-lookup"><span data-stu-id="19dda-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="19dda-137">建置 18305</span><span class="sxs-lookup"><span data-stu-id="19dda-137">Build 18305</span></span>
<span data-ttu-id="19dda-138">一般 Windows 組建 18305 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-139">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-139">WSL</span></span>
* <span data-ttu-id="19dda-140">pthreads 主執行緒結束 [GH 3589] 時，遺失檔案的存取權</span><span class="sxs-lookup"><span data-stu-id="19dda-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="19dda-141">TIOCSCTTY 應該略過 「 強制 」 參數，除非必要，否則 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="19dda-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="19dda-142">wsl.exe 命令列改進功能和新增匯入/匯出功能。</span><span class="sxs-lookup"><span data-stu-id="19dda-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="19dda-143">建置 18277</span><span class="sxs-lookup"><span data-stu-id="19dda-143">Build 18277</span></span>
<span data-ttu-id="19dda-144">一般 Windows 組建 18277 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-145">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-145">WSL</span></span>
* <span data-ttu-id="19dda-146">修正組建 18272 [GH 3645] 中所引進的 「 沒有這類介面支援 」 錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="19dda-147">忽略 umount syscall [GH 3605] MNT_FORCE 旗標</span><span class="sxs-lookup"><span data-stu-id="19dda-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="19dda-148">切換以使用官方 CreatePseudoConsole API WSL interop</span><span class="sxs-lookup"><span data-stu-id="19dda-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="19dda-149">FUTEX_WAIT 重新啟動時，維護任何逾時值</span><span class="sxs-lookup"><span data-stu-id="19dda-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="19dda-150">建置 18272</span><span class="sxs-lookup"><span data-stu-id="19dda-150">Build 18272</span></span>
<span data-ttu-id="19dda-151">一般 Windows 組建 18272 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-152">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-152">WSL</span></span>
* <span data-ttu-id="19dda-153">**警告：** 讓 WSL 無法運作的這個組建中沒有問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="19dda-154">嘗試啟動您的散發套件時，您會看到 「 沒有這類介面支援 」 錯誤。</span><span class="sxs-lookup"><span data-stu-id="19dda-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="19dda-155">此問題已修正，而且會在下一週的測試人員快速建置。</span><span class="sxs-lookup"><span data-stu-id="19dda-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="19dda-156">如果您已安裝此組建，您可以回復至先前的 Windows 組建使用 [執行回舊版的 Windows 10] 在 [設定]-> [更新與安全性]-> 復原。</span><span class="sxs-lookup"><span data-stu-id="19dda-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="19dda-157">建置 18267</span><span class="sxs-lookup"><span data-stu-id="19dda-157">Build 18267</span></span>
<span data-ttu-id="19dda-158">一般 Windows 組建 18267 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-159">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-159">WSL</span></span>
* <span data-ttu-id="19dda-160">修正的問題廢止程序可能會不 reaped 而無限期保留。</span><span class="sxs-lookup"><span data-stu-id="19dda-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="19dda-161">如果錯誤訊息超過最大長度 [GH 3592] WslRegisterDistribution 停止回應</span><span class="sxs-lookup"><span data-stu-id="19dda-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="19dda-162">允許 fsync DrvFs [GH 3556] 上的唯讀檔案順利完成</span><span class="sxs-lookup"><span data-stu-id="19dda-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="19dda-163">請確定 [/bin] 和 [/sbin 目錄存在，才能建立 [GH 3584] 內的符號連結</span><span class="sxs-lookup"><span data-stu-id="19dda-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="19dda-164">新增 WSL 執行個體的執行個體終止逾時機制。</span><span class="sxs-lookup"><span data-stu-id="19dda-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="19dda-165">逾時是目前設定為 15 秒，這表示執行個體將會終止在最後一個 WSL 程序結束之後的 15 秒。</span><span class="sxs-lookup"><span data-stu-id="19dda-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="19dda-166">若要立即終止發佈，請使用：</span><span class="sxs-lookup"><span data-stu-id="19dda-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="19dda-167">建置 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="19dda-167">Build 17763 (1809)</span></span>
<span data-ttu-id="19dda-168">一般 Windows 組建 17763 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-169">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-169">WSL</span></span>
* <span data-ttu-id="19dda-170">Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="19dda-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="19dda-171">確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="19dda-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="19dda-172">處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結</span><span class="sxs-lookup"><span data-stu-id="19dda-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="19dda-173">更妥善地處理的 threadgroup 領導者檔案描述元清除。</span><span class="sxs-lookup"><span data-stu-id="19dda-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="19dda-174">切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="19dda-175">Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="19dda-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="19dda-176">修正數個 AF_UNIX 相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="19dda-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="19dda-177">修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop</span><span class="sxs-lookup"><span data-stu-id="19dda-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="19dda-178">避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲</span><span class="sxs-lookup"><span data-stu-id="19dda-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="19dda-179">新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="19dda-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="19dda-180">更精確的 IPV6 範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="19dda-181">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="19dda-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="19dda-182">使用管線傳送不小心清除 edge 觸發 epoll 事件 [GH 3276] 的檔案系統</span><span class="sxs-lookup"><span data-stu-id="19dda-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="19dda-183">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="19dda-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="19dda-184">改善的殭屍支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="19dda-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="19dda-185">加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目</span><span class="sxs-lookup"><span data-stu-id="19dda-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="19dda-186">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="19dda-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="19dda-187">新增支援 TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="19dda-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="19dda-188">連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="19dda-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="19dda-189">支援在掛接的 Vhd [GH 3246，3291] 上的 interop</span><span class="sxs-lookup"><span data-stu-id="19dda-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="19dda-190">修正權限檢查在根資料夾 [GH 3304] 上的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="19dda-191">TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="19dda-192">Windows UI 應用程式應該執行，即使是在背景中啟動。</span><span class="sxs-lookup"><span data-stu-id="19dda-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="19dda-193">新增 wsl-u 或--使用者選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="19dda-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="19dda-194">啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="19dda-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="19dda-195">Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="19dda-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="19dda-196">非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="19dda-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="19dda-197">案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="19dda-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="19dda-198">請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="19dda-199">新增 wslconfig/終止停止執行的散發套件。</span><span class="sxs-lookup"><span data-stu-id="19dda-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="19dda-200">修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。</span><span class="sxs-lookup"><span data-stu-id="19dda-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="19dda-201">每個目錄區分大小寫做為擴充屬性公開 （expose)</span><span class="sxs-lookup"><span data-stu-id="19dda-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="19dda-202">ARM64:模擬快取的維護作業。</span><span class="sxs-lookup"><span data-stu-id="19dda-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="19dda-203">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="19dda-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="19dda-204">DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。</span><span class="sxs-lookup"><span data-stu-id="19dda-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="19dda-205">修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="19dda-206">WSL 絕對計時器與過去的時間不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="19dda-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="19dda-207">確定新建立的重新分析點將因此列出父目錄中。</span><span class="sxs-lookup"><span data-stu-id="19dda-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="19dda-208">以不可分割方式在 DrvFs 區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="19dda-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="19dda-209">已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="19dda-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="19dda-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="19dda-210">[GH 2712]</span></span>
* <span data-ttu-id="19dda-211">固定的 WSL UMCI 啟用時，啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="19dda-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="19dda-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="19dda-212">[GH 3020]</span></span>
* <span data-ttu-id="19dda-213">新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。</span><span class="sxs-lookup"><span data-stu-id="19dda-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="19dda-214">若要使用，請按住 shift 鍵，以滑鼠右鍵按一下 [在檔案總管] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="19dda-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="19dda-215">修正 Unix 通訊端非封鎖行為 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="19dda-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="19dda-216">當掉 NETLINK 命令，GH 2026 中所報告的修正程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="19dda-217">新增支援掛接傳用旗標 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="19dda-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="19dda-218">截斷而造成不 inotify 事件 [GH 2978] 修正問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="19dda-219">新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="19dda-220">新增--wsl.exe 來選取特定的散發版本的散發選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="19dda-221">Dmesg 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-221">Limited support for dmesg.</span></span> <span data-ttu-id="19dda-222">應用程式現在可以 dmesg 來記錄。</span><span class="sxs-lookup"><span data-stu-id="19dda-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="19dda-223">WSL 驅動程式會記錄到 dmesg 的有限的資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="19dda-224">在將來，這可以延伸到包含其他資訊/診斷的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="19dda-225">注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="19dda-226">`syslog` 尚未支援 syscall 介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="19dda-227">以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。</span><span class="sxs-lookup"><span data-stu-id="19dda-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="19dda-228">變更預設 gid 和模式比對原生 [GH 3042] 序列裝置</span><span class="sxs-lookup"><span data-stu-id="19dda-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="19dda-229">DrvFs 現在支援擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="19dda-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="19dda-230">注意：DrvFs 的擴充屬性名稱有一些限制。</span><span class="sxs-lookup"><span data-stu-id="19dda-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="19dda-231">某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="19dda-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="19dda-232">建置 18252 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-233">一般 Windows 組建 18252 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-234">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-234">WSL</span></span>
* <span data-ttu-id="19dda-235">移動 init 和 bsdtar 二進位檔出 lxssmanager dll 並進入不同的工具資料夾</span><span class="sxs-lookup"><span data-stu-id="19dda-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="19dda-236">修正競爭周圍使用 CLONE_FILES 時關閉檔案描述元</span><span class="sxs-lookup"><span data-stu-id="19dda-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="19dda-237">翻譯 DrvFs 路徑時，處理 /proc/pid/mountinfo 中的選擇性欄位</span><span class="sxs-lookup"><span data-stu-id="19dda-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="19dda-238">允許 DrvFs mknod 不用 S_IFREG 的中繼資料支援成功</span><span class="sxs-lookup"><span data-stu-id="19dda-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="19dda-239">DrvFs 上建立的唯讀檔案應該有設定 [GH 3411] 中的 readonly 屬性</span><span class="sxs-lookup"><span data-stu-id="19dda-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="19dda-240">新增處理 DrvFs 掛接 /sbin/mount.drvfs 協助程式</span><span class="sxs-lookup"><span data-stu-id="19dda-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="19dda-241">用於 DrvFs POSIX 重新命名。</span><span class="sxs-lookup"><span data-stu-id="19dda-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="19dda-242">允許在不含磁碟區 GUID 的磁碟區上的路徑轉譯。</span><span class="sxs-lookup"><span data-stu-id="19dda-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="19dda-243">建置 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="19dda-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="19dda-244">一般 Windows 組建 17738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-245">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-245">WSL</span></span>
* <span data-ttu-id="19dda-246">Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="19dda-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="19dda-247">確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="19dda-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="19dda-248">處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結</span><span class="sxs-lookup"><span data-stu-id="19dda-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="19dda-249">更妥善地處理的 threadgroup 領導者檔案描述元清除。</span><span class="sxs-lookup"><span data-stu-id="19dda-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="19dda-250">建置 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="19dda-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="19dda-251">一般 Windows 組建 17728 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-252">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-252">WSL</span></span>
* <span data-ttu-id="19dda-253">切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="19dda-254">Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="19dda-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="19dda-255">修正幾個 AF_UNIX 的相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="19dda-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="19dda-256">修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop</span><span class="sxs-lookup"><span data-stu-id="19dda-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="19dda-257">建置 18204 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-258">一般 Windows 組建 18204 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-259">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-259">WSL</span></span>
* <span data-ttu-id="19dda-260">使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="19dda-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="19dda-261">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="19dda-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="19dda-262">建置 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="19dda-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="19dda-263">一般 Windows 組建 17723 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-264">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-264">WSL</span></span>
* <span data-ttu-id="19dda-265">避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲</span><span class="sxs-lookup"><span data-stu-id="19dda-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="19dda-266">新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="19dda-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="19dda-267">更精確的 IPV6 範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="19dda-268">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="19dda-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="19dda-269">使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="19dda-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="19dda-270">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="19dda-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="19dda-271">建置 17713</span><span class="sxs-lookup"><span data-stu-id="19dda-271">Build 17713</span></span>
<span data-ttu-id="19dda-272">一般 Windows 組建 17713 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-273">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-273">WSL</span></span>
* <span data-ttu-id="19dda-274">改善的殭屍支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="19dda-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="19dda-275">加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目</span><span class="sxs-lookup"><span data-stu-id="19dda-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="19dda-276">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="19dda-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="19dda-277">新增支援 TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="19dda-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="19dda-278">連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="19dda-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="19dda-279">支援在掛接的 Vhd [GH 3246，3291] 上的 interop</span><span class="sxs-lookup"><span data-stu-id="19dda-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="19dda-280">修正權限檢查在根資料夾 [GH 3304] 上的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="19dda-281">TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="19dda-282">Windows UI 應用程式應該執行，即使是在背景中啟動。</span><span class="sxs-lookup"><span data-stu-id="19dda-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="19dda-283">建置 17704</span><span class="sxs-lookup"><span data-stu-id="19dda-283">Build 17704</span></span>
<span data-ttu-id="19dda-284">一般 Windows 組建 17704 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-285">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-285">WSL</span></span>
* <span data-ttu-id="19dda-286">新增 wsl-u 或--使用者選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="19dda-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="19dda-287">啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="19dda-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="19dda-288">Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="19dda-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="19dda-289">非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="19dda-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="19dda-290">案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="19dda-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="19dda-291">請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="19dda-292">新增 wslconfig/終止停止執行的散發套件。</span><span class="sxs-lookup"><span data-stu-id="19dda-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="19dda-293">組建 17692</span><span class="sxs-lookup"><span data-stu-id="19dda-293">Build 17692</span></span>
<span data-ttu-id="19dda-294">一般 Windows 組建 17692 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="19dda-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-295">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-295">WSL</span></span>
* <span data-ttu-id="19dda-296">修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。</span><span class="sxs-lookup"><span data-stu-id="19dda-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="19dda-297">每個目錄區分大小寫做為擴充屬性公開 （expose)</span><span class="sxs-lookup"><span data-stu-id="19dda-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="19dda-298">ARM64:模擬快取的維護作業。</span><span class="sxs-lookup"><span data-stu-id="19dda-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="19dda-299">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="19dda-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="19dda-300">DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。</span><span class="sxs-lookup"><span data-stu-id="19dda-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="19dda-301">組建 17686</span><span class="sxs-lookup"><span data-stu-id="19dda-301">Build 17686</span></span>
<span data-ttu-id="19dda-302">一般 Windows 組建 17686 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="19dda-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-303">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-303">WSL</span></span>
* <span data-ttu-id="19dda-304">修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="19dda-305">WSL 絕對計時器與過去的時間不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="19dda-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="19dda-306">確定新建立的重新分析點將因此列出父目錄中。</span><span class="sxs-lookup"><span data-stu-id="19dda-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="19dda-307">以不可分割方式在 DrvFs 區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="19dda-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="19dda-308">建置 17677</span><span class="sxs-lookup"><span data-stu-id="19dda-308">Build 17677</span></span>
<span data-ttu-id="19dda-309">一般 Windows 組建 17677 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-310">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-310">WSL</span></span>
* <span data-ttu-id="19dda-311">已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="19dda-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="19dda-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="19dda-312">[GH 2712]</span></span>
* <span data-ttu-id="19dda-313">固定的 WSL UMCI 啟用時，啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="19dda-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="19dda-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="19dda-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="19dda-315">建置 17666</span><span class="sxs-lookup"><span data-stu-id="19dda-315">Build 17666</span></span>
<span data-ttu-id="19dda-316">一般 Windows 組建 17666 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-317">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="19dda-318">警告：還有一些 AMD 晶片 [GH 3134] 上執行時，防止 WSL 問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="19dda-319">修正程式是準備好讓測試人員組建分支及其方式。</span><span class="sxs-lookup"><span data-stu-id="19dda-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="19dda-320">新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。</span><span class="sxs-lookup"><span data-stu-id="19dda-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="19dda-321">若要使用按住 shift 鍵並以滑鼠右鍵按一下在檔案總管 視窗中。</span><span class="sxs-lookup"><span data-stu-id="19dda-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="19dda-322">修正 unix 通訊端非封鎖行為 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="19dda-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="19dda-323">當掉 NETLINK 命令，GH 2026 中所報告的修正程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="19dda-324">新增支援掛接傳用旗標 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="19dda-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="19dda-325">截斷而造成不 inotify 事件 [GH 2978] 修正問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="19dda-326">新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="19dda-327">新增--wsl.exe 來選取特定的散發版本的散發選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="19dda-328">建置 17655 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-329">一般 Windows 組建 17655 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-330">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-330">WSL</span></span>
* <span data-ttu-id="19dda-331">Dmesg 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-331">Limited support for dmesg.</span></span> <span data-ttu-id="19dda-332">應用程式現在可以 dmesg 來記錄。</span><span class="sxs-lookup"><span data-stu-id="19dda-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="19dda-333">WSL 驅動程式會記錄到 dmesg 的有限的資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="19dda-334">在將來，這可以延伸到包含其他資訊/診斷的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="19dda-335">注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="19dda-336">`syslog` 尚未支援 sycall 介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="19dda-337">以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。</span><span class="sxs-lookup"><span data-stu-id="19dda-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="19dda-338">已修正的問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="19dda-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="19dda-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="19dda-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="19dda-340">建置 17639 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-341">一般 Windows 組建 17639 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-342">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-342">WSL</span></span>
* <span data-ttu-id="19dda-343">變更預設 gid 和模式比對原生 [GH 3042] 序列裝置</span><span class="sxs-lookup"><span data-stu-id="19dda-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="19dda-344">DrvFs 現在支援擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="19dda-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="19dda-345">注意：DrvFs 的擴充屬性名稱有一些限制。</span><span class="sxs-lookup"><span data-stu-id="19dda-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="19dda-346">特別是，某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="19dda-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="19dda-347">建置 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="19dda-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="19dda-348">一般 Windows 組建 17133 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-349">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-349">WSL</span></span>
* <span data-ttu-id="19dda-350">修正在 WSL 的停止回應。</span><span class="sxs-lookup"><span data-stu-id="19dda-350">Fix for hang in WSL.</span></span> <span data-ttu-id="19dda-351">[GH 3039，3034]</span><span class="sxs-lookup"><span data-stu-id="19dda-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="19dda-352">建置 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="19dda-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="19dda-353">一般 Windows 組建 17128 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-354">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-354">WSL</span></span>
* <span data-ttu-id="19dda-355">None</span><span class="sxs-lookup"><span data-stu-id="19dda-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="19dda-356">建置 17627 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-357">一般 Windows 組建 17627 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-358">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-358">WSL</span></span>
* <span data-ttu-id="19dda-359">新增支援 futex 感知 pi 的作業。</span><span class="sxs-lookup"><span data-stu-id="19dda-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="19dda-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="19dda-360">[GH 1006]</span></span>
    * <span data-ttu-id="19dda-361">請注意，優先順序而不是目前支援的 WSL 功能因此有一些限制，但標準使用量應該要解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="19dda-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="19dda-362">WSL 程序的 Windows 防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="19dda-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="19dda-363">[GH 1852]</span></span>
    * <span data-ttu-id="19dda-364">比方說，若要允許 WSL python 則會接聽任何通訊埠，請使用提高權限的 Windows cmd 處理： ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="19dda-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="19dda-365">如需有關如何新增防火牆規則的詳細資訊，請參閱[連結](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="19dda-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="19dda-366">使用 wsl.exe 時，請採用使用者的預設殼層。</span><span class="sxs-lookup"><span data-stu-id="19dda-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="19dda-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="19dda-367">[GH 2372]</span></span>
* <span data-ttu-id="19dda-368">報告為乙太網路的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="19dda-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="19dda-369">[GH 2996]</span></span>
* <span data-ttu-id="19dda-370">更妥善地處理的損毀 /etc/passwd 檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="19dda-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="19dda-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="19dda-372">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-372">Console</span></span>
* <span data-ttu-id="19dda-373">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-374">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-374">LTP Results:</span></span>
<span data-ttu-id="19dda-375">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="19dda-376">建置 17618 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="19dda-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="19dda-377">一般 Windows 組建 17618 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-378">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-378">WSL</span></span>
* <span data-ttu-id="19dda-379">引入 NT interop pseudoconsole 功能 [GH 988，1366，1433年、 1542年、 2370年、 2406年]。</span><span class="sxs-lookup"><span data-stu-id="19dda-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="19dda-380">舊版安裝機制 (lxrun.exe) 已被取代。</span><span class="sxs-lookup"><span data-stu-id="19dda-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="19dda-381">安裝散發套件支援的機制是透過 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="19dda-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="19dda-382">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-382">Console</span></span>
* <span data-ttu-id="19dda-383">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-384">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-384">LTP Results:</span></span>
<span data-ttu-id="19dda-385">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="19dda-386">組建 17110</span><span class="sxs-lookup"><span data-stu-id="19dda-386">Build 17110</span></span>
<span data-ttu-id="19dda-387">一般 Windows 組建 17110 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-388">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-388">WSL</span></span>
* <span data-ttu-id="19dda-389">允許從 Windows [GH 2928] 終止 /init。</span><span class="sxs-lookup"><span data-stu-id="19dda-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="19dda-390">DrvFs 現在預設會使用每個目錄是否區分大小寫 (相當於"案例 = dir 」 掛接選項)。</span><span class="sxs-lookup"><span data-stu-id="19dda-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="19dda-391">使用 「 案例 = force"（舊的行為） 需要設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="19dda-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="19dda-392">執行下列命令，以啟用 「 案例 = 強制 「 如果您需要使用它： reg 新增 HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="19dda-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="19dda-393">如果您有現有的目錄建立 WSL 與 Windows 所需區分大小寫的舊版本中，會使用 fsutil.exe 來將它們標示為區分大小寫： fsutil.exe 檔案 setcasesensitiveinfo<path>啟用</span><span class="sxs-lookup"><span data-stu-id="19dda-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="19dda-394">以 NULL 結尾的 uname syscall 從傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="19dda-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="19dda-395">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-395">Console</span></span>
* <span data-ttu-id="19dda-396">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-397">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-397">LTP Results:</span></span>
<span data-ttu-id="19dda-398">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="19dda-399">建置 17107</span><span class="sxs-lookup"><span data-stu-id="19dda-399">Build 17107</span></span>
<span data-ttu-id="19dda-400">一般 Windows 組建 17107 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-401">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-401">WSL</span></span>
* <span data-ttu-id="19dda-402">支援 TCSETSF 和 TCSETSW 主要 pty 端點 [GH 2552] 上。</span><span class="sxs-lookup"><span data-stu-id="19dda-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="19dda-403">啟動同時 interop 的程序，可能會導致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="19dda-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="19dda-404">修正 PTRACE_ATTACH 在 /proc/pid/status 中顯示適當的追蹤狀態。</span><span class="sxs-lookup"><span data-stu-id="19dda-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="19dda-405">修正競爭短期處理序使用 CLEARTID 和 SETTID 旗標已複製的儲存無法結束而不清除 TID 位址。</span><span class="sxs-lookup"><span data-stu-id="19dda-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="19dda-406">移動從 pre 17093 組建時升級 Linux 檔案系統目錄時，顯示一則訊息。</span><span class="sxs-lookup"><span data-stu-id="19dda-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="19dda-407">如需 17093 檔案系統變更的詳細資訊，請參閱版本資訊[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)。</span><span class="sxs-lookup"><span data-stu-id="19dda-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="19dda-408">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-408">Console</span></span>
* <span data-ttu-id="19dda-409">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-410">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-410">LTP Results:</span></span>
<span data-ttu-id="19dda-411">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="19dda-412">建置 17101</span><span class="sxs-lookup"><span data-stu-id="19dda-412">Build 17101</span></span>
<span data-ttu-id="19dda-413">一般 Windows 組建 17101 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-414">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-414">WSL</span></span>
* <span data-ttu-id="19dda-415">Signalfd 支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-415">Support for signalfd.</span></span> <span data-ttu-id="19dda-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="19dda-416">[GH 129]</span></span>
* <span data-ttu-id="19dda-417">支援的檔案名稱包含不合法的 NTFS 字元加以編碼為私用的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="19dda-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="19dda-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="19dda-418">[GH 1514]</span></span>
* <span data-ttu-id="19dda-419">不支援寫入時，自動掛接會將恢復為唯讀。</span><span class="sxs-lookup"><span data-stu-id="19dda-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="19dda-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="19dda-420">[GH 2603]</span></span>
* <span data-ttu-id="19dda-421">允許貼上的 Unicode surrogate 字組 （例如 emoji 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="19dda-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="19dda-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="19dda-422">[GH 2765]</span></span>
* <span data-ttu-id="19dda-423">/Proc 和 /sys 中的虛擬檔案應該會傳回讀取和寫入已準備好從 select、 投票、 epoll，要是 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="19dda-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="19dda-424">修正問題，可能會導致服務登錄已遭竄改，或已損毀時進入無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="19dda-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="19dda-425">修正使用較新版本 (4.14 上游) iproute2 netlink 訊息。</span><span class="sxs-lookup"><span data-stu-id="19dda-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="19dda-426">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-426">Console</span></span>
* <span data-ttu-id="19dda-427">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-428">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-428">LTP Results:</span></span>
<span data-ttu-id="19dda-429">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="19dda-430">建置 17093</span><span class="sxs-lookup"><span data-stu-id="19dda-430">Build 17093</span></span>
<span data-ttu-id="19dda-431">一般 Windows 組建 17093 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="19dda-432">重要事項：</span><span class="sxs-lookup"><span data-stu-id="19dda-432">Important:</span></span>
<span data-ttu-id="19dda-433">當從 WSL 開始第一次升級至此組建之後，它必須執行一些工作升級 Linux 檔案系統目錄。</span><span class="sxs-lookup"><span data-stu-id="19dda-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="19dda-434">這可能需要幾分鐘的時間，因此 WSL 似乎較慢啟動。</span><span class="sxs-lookup"><span data-stu-id="19dda-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="19dda-435">這只應該發生之後的每個散發中，您已安裝從存放區。</span><span class="sxs-lookup"><span data-stu-id="19dda-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="19dda-436">已改善 DrvFs 中的區分大小寫支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="19dda-437">DrvFs 現在支援每個目錄區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="19dda-438">這是新旗標，可以設定目錄，以指出在這些目錄中的所有作業應都視為區分大小寫，如此即使 Windows 應用程式正確地開啟只有大小寫不同的檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="19dda-439">DrvFs 具備新的掛接選項，控制每個目錄為基礎的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="19dda-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="19dda-440">案例 = 強制： 所有目錄都區分大小寫 （除了磁碟機根目錄中）。</span><span class="sxs-lookup"><span data-stu-id="19dda-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="19dda-441">WSL 以建立新的目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="19dda-442">這是除了標示新的目錄的區分大小寫的舊行為。</span><span class="sxs-lookup"><span data-stu-id="19dda-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="19dda-443">案例 = dir： 只有透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="19dda-444">WSL 以建立新的目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="19dda-445">案例 = 關閉： 只透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="19dda-446">WSL 以建立新的目錄會標示為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="19dda-447">注意： 在舊版中建立的 WSL 目錄沒有設定，因此將不被視為區分大小寫如果您使用這個旗標 」 案例 = dir"選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="19dda-448">即將推出的方式，若要在現有的目錄上設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="19dda-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="19dda-449">裝載這些選項的範例 （現有的磁碟機，您必須先卸載之前，您可以掛上使用不同的選項）： sudo mount-t drvfs c: / /mnt/c o 案例 = dir</span><span class="sxs-lookup"><span data-stu-id="19dda-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="19dda-450">現在，寫 = 強制仍是預設選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="19dda-451">這將會變更為案例未來 = dir。</span><span class="sxs-lookup"><span data-stu-id="19dda-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="19dda-452">您現在可以使用正斜線 Windows 路徑中時，裝載 DrvFs，例如： sudo 掛接-t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="19dda-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="19dda-453">現在，WSL 會在執行個體啟動 [GH 2636] 處理 /etc/fstab 檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="19dda-454">這是之前自動掛接 DrvFs 磁碟機;任何已經 fstab 已掛接的磁碟機將不會自動重新掛接，可讓您變更特定磁碟機的掛接點。</span><span class="sxs-lookup"><span data-stu-id="19dda-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="19dda-455">此行為可以關閉使用 wsl.conf。</span><span class="sxs-lookup"><span data-stu-id="19dda-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="19dda-456">掛接、 mountinfo 和 mountstats 檔案中 /proc 正確逸出特殊字元，例如反斜線和空格 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="19dda-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="19dda-457">可以複製和移動從 Windows 建立 DrvFs WSL 符號連結，或 fifos 等通訊端啟用中繼資料時，特殊的檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="19dda-458">WSL 會與 wsl.conf 更易設定</span><span class="sxs-lookup"><span data-stu-id="19dda-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="19dda-459">我們已新增為您自動設定會套用每次您啟動子系統的 WSL 中的 特定功能的方法。</span><span class="sxs-lookup"><span data-stu-id="19dda-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="19dda-460">這包括自動掛接選項和網路設定。</span><span class="sxs-lookup"><span data-stu-id="19dda-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="19dda-461">深入了解在我們的部落格文章，網址： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="19dda-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="19dda-462">AF_UNIX 可讓 Linux 處理序在 WSL 與 Windows 原生程序之間的通訊端連線</span><span class="sxs-lookup"><span data-stu-id="19dda-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="19dda-463">WSL 與 Windows 應用程式現在可以透過 Unix 通訊端通訊彼此。</span><span class="sxs-lookup"><span data-stu-id="19dda-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="19dda-464">假設您想要在 Windows 中執行的服務，並使其可供 Windows 和 WSL 應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="19dda-465">現在，這可能與 Unix 通訊端。</span><span class="sxs-lookup"><span data-stu-id="19dda-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="19dda-466">如需我們的部落格文章，讀取 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="19dda-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-467">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-467">WSL</span></span>
* <span data-ttu-id="19dda-468">支援使用 MAP_NORESERVE [GH 121，2784年] mmap()</span><span class="sxs-lookup"><span data-stu-id="19dda-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="19dda-469">支援 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121，2781年]</span><span class="sxs-lookup"><span data-stu-id="19dda-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="19dda-470">處理非 SIGCHLD 終止訊號中複製 [GH 121，2781年]</span><span class="sxs-lookup"><span data-stu-id="19dda-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="19dda-471">虛設常式 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="19dda-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="19dda-472">載入 ELF 二進位碼檔案包含具有非零位移 [GH 1884] 的負載標頭時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="19dda-473">會全面清除載入影像時後, 置頁面位元組。</span><span class="sxs-lookup"><span data-stu-id="19dda-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="19dda-474">減少 execve 以無訊息方式結束處理序的情況下</span><span class="sxs-lookup"><span data-stu-id="19dda-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="19dda-475">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-475">Console</span></span>
* <span data-ttu-id="19dda-476">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-477">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-477">LTP Results:</span></span>
<span data-ttu-id="19dda-478">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="19dda-479">組建 17083</span><span class="sxs-lookup"><span data-stu-id="19dda-479">Build 17083</span></span>
<span data-ttu-id="19dda-480">一般 Windows 組建 17083 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-481">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-481">WSL</span></span>
* <span data-ttu-id="19dda-482">固定的 epoll [GH 2798，2801，2857年] 相關的錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="19dda-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="19dda-483">固定的停止回應時關閉 ASLR [GH 1185，2870年]</span><span class="sxs-lookup"><span data-stu-id="19dda-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="19dda-484">請確定 mmap 作業出現不可部分完成 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="19dda-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="19dda-485">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-485">Console</span></span>
* <span data-ttu-id="19dda-486">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-487">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-487">LTP Results:</span></span>
<span data-ttu-id="19dda-488">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="19dda-489">建置 17074</span><span class="sxs-lookup"><span data-stu-id="19dda-489">Build 17074</span></span>
<span data-ttu-id="19dda-490">一般 Windows 組建 17074 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-491">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-491">WSL</span></span>
* <span data-ttu-id="19dda-492">DrvFs 中繼資料 [GH 2777] 固定的儲存體格式</span><span class="sxs-lookup"><span data-stu-id="19dda-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="19dda-493">**重要事項：** 這個組建不正確，或完全不會出現之前建立的 DrvFs 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="19dda-494">若要修正受影響的檔案，請使用 chmod 和 chown 來重新套用中繼資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="19dda-495">與多個訊號可重新啟動 syscall 修正的問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="19dda-496">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-496">Console</span></span>
* <span data-ttu-id="19dda-497">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-498">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-498">LTP Results:</span></span>
<span data-ttu-id="19dda-499">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="19dda-500">建置 17063</span><span class="sxs-lookup"><span data-stu-id="19dda-500">Build 17063</span></span>
<span data-ttu-id="19dda-501">一般 Windows 組建 17063 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="19dda-502">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-502">WSL</span></span>
* <span data-ttu-id="19dda-503">DrvFs 支援 Linux 的其他中繼資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="19dda-504">這可讓設定擁有者和使用 chmod/chown，以及建立特殊的檔案，例如 fifos、 unix 通訊端和裝置檔案的檔案模式。</span><span class="sxs-lookup"><span data-stu-id="19dda-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="19dda-505">這預設會停用目前因為它是仍屬實驗性質。</span><span class="sxs-lookup"><span data-stu-id="19dda-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="19dda-506">**注意：** 我們修正了在 DrvFs 所使用的中繼資料格式。</span><span class="sxs-lookup"><span data-stu-id="19dda-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="19dda-507">而中繼資料則適用於此組建進行實驗，未來的組建將不會正確地讀取此組建所建立的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="19dda-508">您可能需要手動更新已修改檔案的擁有者，就必須重新建立自訂裝置識別碼的裝置。</span><span class="sxs-lookup"><span data-stu-id="19dda-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="19dda-509">若要啟用，請使用 [中繼資料] 選項掛接 DrvFs （現有的裝載上啟用此功能，您必須先取消掛接）：</span><span class="sxs-lookup"><span data-stu-id="19dda-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="19dda-510">Linux 的權限會新增為額外的中繼資料檔案，它們不會影響 Windows 權限。</span><span class="sxs-lookup"><span data-stu-id="19dda-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="19dda-511">請記住，編輯檔案，使用 Windows 編輯器可能會移除的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="19dda-512">在此情況下，檔案將還原為其預設權限。</span><span class="sxs-lookup"><span data-stu-id="19dda-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="19dda-513">已新增的掛接選項 DrvFs 以不含中繼資料的控制檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="19dda-514">uid： 使用的所有檔案擁有者的使用者 ID。</span><span class="sxs-lookup"><span data-stu-id="19dda-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="19dda-515">gid： 使用的所有檔案擁有者的群組 ID。</span><span class="sxs-lookup"><span data-stu-id="19dda-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="19dda-516">umask： 排除所有的檔案和目錄的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="19dda-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="19dda-517">fmask： 排除所有的一般檔案的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="19dda-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="19dda-518">dmask： 排除所有目錄的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="19dda-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="19dda-519">例如: </span><span class="sxs-lookup"><span data-stu-id="19dda-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="19dda-520">結合指定不含中繼資料檔案的預設權限的 [中繼資料] 選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="19dda-521">導入新的環境變數， `WSLENV`，來設定環境變數 WSL 和 Win32 之間流動的方式。</span><span class="sxs-lookup"><span data-stu-id="19dda-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="19dda-522">例如: </span><span class="sxs-lookup"><span data-stu-id="19dda-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="19dda-523">`WSLENV` 是以冒號分隔的清單時啟動 WSL 程序，從 Win32 或從 WSL 的 Win32 處理序可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="19dda-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="19dda-524">每個變數都可以加斜線，後面接著旗標，以指定在轉譯的方式。</span><span class="sxs-lookup"><span data-stu-id="19dda-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="19dda-525">p:值為應轉譯 WSL 路徑與 Win32 路徑之間的路徑。</span><span class="sxs-lookup"><span data-stu-id="19dda-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="19dda-526">L:值是路徑的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-526">l: The value is a list of paths.</span></span> <span data-ttu-id="19dda-527">在 WSL，它是以冒號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="19dda-528">在 Win32 中，它是以分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="19dda-529">U:值只能包含時叫用從 Win32 WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="19dda-530">寫入：值只能包含時叫用 Win32 從 WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="19dda-531">您可以設定`WSLENV`.bashrc 或自訂的 Windows 環境，為您的使用者。</span><span class="sxs-lookup"><span data-stu-id="19dda-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="19dda-532">drvfs 掛接正確保留時間戳記的 tar 檔案解壓縮，cp-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="19dda-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="19dda-533">drvfs 符號連結報告正確的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="19dda-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="19dda-534">讀取/寫入適用於非常大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="19dda-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="19dda-535">waitpid 搭配處理序群組識別碼 (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="19dda-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="19dda-536">大型的保留區域，大幅改善的 mmap 效能改善 ghc 效能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="19dda-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="19dda-537">READ_IMPLIES_EXEC; 的人格支援修正行程最長和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="19dda-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="19dda-538">mprotect 支援 PROT_GROWSDOWN;修正 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="19dda-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="19dda-539">頁面中的錯誤修正程式過量使用模式;修正 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="19dda-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="19dda-540">複製支援多個旗標的組合</span><span class="sxs-lookup"><span data-stu-id="19dda-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="19dda-541">支援選取/epoll 的 epoll 檔案 （之前執行任何作業）。</span><span class="sxs-lookup"><span data-stu-id="19dda-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="19dda-542">通知未實作 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="19dda-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="19dda-543">忽略都未運作時產生 resolv.conf nameservers [GH 2694] 的介面</span><span class="sxs-lookup"><span data-stu-id="19dda-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="19dda-544">列舉沒有實體位址的網路介面。</span><span class="sxs-lookup"><span data-stu-id="19dda-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="19dda-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="19dda-545">[GH 2685]</span></span>
* <span data-ttu-id="19dda-546">其他錯誤修正和改進功能。</span><span class="sxs-lookup"><span data-stu-id="19dda-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="19dda-547">在 Windows 上的開發人員可使用的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="19dda-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="19dda-548">Windows 命令列工具鏈包含 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="19dda-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="19dda-549">讀取[這篇部落格](https://aka.ms/tarcurlwindows)深入了解這兩個新工具加入，並查看如何它們塑造在 Windows 上的開發人員體驗。</span><span class="sxs-lookup"><span data-stu-id="19dda-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="19dda-550">`AF_UNIX` 提供 Windows Insider SDK 中 （17061 +）。</span><span class="sxs-lookup"><span data-stu-id="19dda-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="19dda-551">讀取[這篇部落格](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)若要深入了解`AF_UNIX`以及如何在 Windows 上的開發人員可以使用它。</span><span class="sxs-lookup"><span data-stu-id="19dda-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="19dda-552">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-552">Console</span></span>
* <span data-ttu-id="19dda-553">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-554">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-554">LTP Results:</span></span>
<span data-ttu-id="19dda-555">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="19dda-556">建置 17046</span><span class="sxs-lookup"><span data-stu-id="19dda-556">Build 17046</span></span>

<span data-ttu-id="19dda-557">一般 Windows 組建 17046 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="19dda-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-558">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-559">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-559">WSL</span></span>
- <span data-ttu-id="19dda-560">允許在沒有使用中的終端機的情況下執行的處理序。</span><span class="sxs-lookup"><span data-stu-id="19dda-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="19dda-561">[GH 709、 1007、 1511年、 2252年 2391，et al。]</span><span class="sxs-lookup"><span data-stu-id="19dda-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="19dda-562">CLONE_VFORK 和 CLONE_VM 更佳的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="19dda-563">[GH 1878，2615年]</span><span class="sxs-lookup"><span data-stu-id="19dda-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="19dda-564">略過網路作業的 WSL TDI 篩選器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="19dda-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="19dda-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="19dda-565">[GH 1554]</span></span>
- <span data-ttu-id="19dda-566">DrvFs 會在符合特定條件時，建立 NT 符號連結。</span><span class="sxs-lookup"><span data-stu-id="19dda-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="19dda-567">[GH 353，1475，2602年]</span><span class="sxs-lookup"><span data-stu-id="19dda-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="19dda-568">連結目標必須是相對的不能跨越任何掛接點或符號連結，而且必須存在。</span><span class="sxs-lookup"><span data-stu-id="19dda-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="19dda-569">使用者必須擁有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE （這通常需要您啟動 wsl.exe 提升權限），除非開發人員模式下開啟。</span><span class="sxs-lookup"><span data-stu-id="19dda-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="19dda-570">在其他情況下，DrvFs 仍會建立 WSL 符號連結。</span><span class="sxs-lookup"><span data-stu-id="19dda-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="19dda-571">允許同時執行提高權限和非提高權限的 WSL 執行個體。</span><span class="sxs-lookup"><span data-stu-id="19dda-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="19dda-572">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="19dda-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="19dda-573">新增 wslpath 執行 WSL <>-Windows 路徑的轉換。</span><span class="sxs-lookup"><span data-stu-id="19dda-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="19dda-574">[GH 522，1243，1834年、 2327，et al。]</span><span class="sxs-lookup"><span data-stu-id="19dda-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="19dda-575">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-575">Console</span></span>
- <span data-ttu-id="19dda-576">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-577">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-577">LTP Results:</span></span>
<span data-ttu-id="19dda-578">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="19dda-579">建置 17040</span><span class="sxs-lookup"><span data-stu-id="19dda-579">Build 17040</span></span>

<span data-ttu-id="19dda-580">一般 Windows 組建 17040 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="19dda-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-581">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-582">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-582">WSL</span></span>
- <span data-ttu-id="19dda-583">因為 17035 任何修正。</span><span class="sxs-lookup"><span data-stu-id="19dda-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-584">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-584">Console</span></span>
- <span data-ttu-id="19dda-585">因為 17035 任何修正。</span><span class="sxs-lookup"><span data-stu-id="19dda-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-586">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-586">LTP Results:</span></span>
<span data-ttu-id="19dda-587">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="19dda-588">建置 17035</span><span class="sxs-lookup"><span data-stu-id="19dda-588">Build 17035</span></span>

<span data-ttu-id="19dda-589">一般 Windows 組建 17035 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="19dda-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-590">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-591">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-591">WSL</span></span>
- <span data-ttu-id="19dda-592">偶爾會失敗，但是 EINVAL 存取 DrvFs 上的檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="19dda-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="19dda-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-594">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-594">Console</span></span>
- <span data-ttu-id="19dda-595">色彩遺失部分插入/刪除 VT 模式中的行時。</span><span class="sxs-lookup"><span data-stu-id="19dda-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-596">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-596">LTP Results:</span></span>
<span data-ttu-id="19dda-597">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="19dda-598">組建 17025</span><span class="sxs-lookup"><span data-stu-id="19dda-598">Build 17025</span></span>

<span data-ttu-id="19dda-599">一般 Windows 組建 17025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="19dda-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-600">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-601">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-601">WSL</span></span>
- <span data-ttu-id="19dda-602">在新的前景處理程序群組 [GH 1653，2510年] 開始初始程序。</span><span class="sxs-lookup"><span data-stu-id="19dda-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="19dda-603">SIGHUP 傳遞修正 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="19dda-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="19dda-604">若無提供 [GH 2497]，則產生預設虛擬橋接器的名稱。</span><span class="sxs-lookup"><span data-stu-id="19dda-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="19dda-605">實作 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="19dda-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="19dda-606">修正了更 interop 的 stdout/stderr 管道。</span><span class="sxs-lookup"><span data-stu-id="19dda-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="19dda-607">虛設常式 syncfs 系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="19dda-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-608">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-608">Console</span></span>
- <span data-ttu-id="19dda-609">修正輸入的 VT 翻譯的協力廠商主控台 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="19dda-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-610">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-610">LTP Results:</span></span>
<span data-ttu-id="19dda-611">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="19dda-612">建置 17017</span><span class="sxs-lookup"><span data-stu-id="19dda-612">Build 17017</span></span>

<span data-ttu-id="19dda-613">一般 Windows 組建 17017 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="19dda-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-614">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-615">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-615">WSL</span></span>
- <span data-ttu-id="19dda-616">忽略空白 ELF 程式標頭 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="19dda-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="19dda-617">允許建立非互動式使用者的 WSL 執行個體的 LxssManager (ssh 和排程的工作支援) [GH 777 1602年]。</span><span class="sxs-lookup"><span data-stu-id="19dda-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="19dda-618">支援 WSL]-> [Win32]-> [WSL （「 開始 」） 案例 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="19dda-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="19dda-619">終止透過 interop [GH 1614] 叫用的主控台應用程式的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="19dda-620">支援掛接 devpts [GH 1948] 選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="19dda-621">Ptrace 封鎖子啟動 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="19dda-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="19dda-622">EPOLLET 遺漏某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="19dda-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="19dda-623">傳回 PTRACE_GETSIGINFO 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="19dda-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="19dda-624">使用 lseek Getdents 提供不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="19dda-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="19dda-625">修正一些 Win32 interop 應用程式停止回應，有沒有更多的資料管道上等候輸入。</span><span class="sxs-lookup"><span data-stu-id="19dda-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="19dda-626">O_ASYNC 支援 tty/pty 檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="19dda-627">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-628">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-628">Console</span></span>
- <span data-ttu-id="19dda-629">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-630">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-630">LTP Results:</span></span>
<span data-ttu-id="19dda-631">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="19dda-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="19dda-632">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="19dda-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="19dda-633">建置 16288</span><span class="sxs-lookup"><span data-stu-id="19dda-633">Build 16288</span></span>

<span data-ttu-id="19dda-634">一般 Windows 組建 16288 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-635">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-636">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-636">WSL</span></span>
- <span data-ttu-id="19dda-637">正確初始化，並報告 uid、 gid 和通訊端檔案描述元 [GH 2490] 模式</span><span class="sxs-lookup"><span data-stu-id="19dda-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="19dda-638">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-639">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-639">Console</span></span>
- <span data-ttu-id="19dda-640">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-641">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-641">LTP Results:</span></span>
<span data-ttu-id="19dda-642">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="19dda-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="19dda-643">建置 16278</span><span class="sxs-lookup"><span data-stu-id="19dda-643">Build 16278</span></span>

<span data-ttu-id="19dda-644">一般 Windows 組建 162738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-645">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-646">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-646">WSL</span></span>
- <span data-ttu-id="19dda-647">卸除 LX MM 狀態 [GH 2415] 時，明確地取消對應支援的檔案區段的對應的檢視</span><span class="sxs-lookup"><span data-stu-id="19dda-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="19dda-648">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-649">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-649">Console</span></span>
- <span data-ttu-id="19dda-650">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-651">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-651">LTP Results:</span></span>
<span data-ttu-id="19dda-652">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="19dda-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="19dda-653">建置 16275</span><span class="sxs-lookup"><span data-stu-id="19dda-653">Build 16275</span></span>

<span data-ttu-id="19dda-654">一般 Windows 組建 162735 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-655">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-656">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-656">WSL</span></span>
- <span data-ttu-id="19dda-657">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-658">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-658">Console</span></span>
- <span data-ttu-id="19dda-659">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-660">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-660">LTP Results:</span></span>
<span data-ttu-id="19dda-661">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="19dda-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="19dda-662">建置 16273</span><span class="sxs-lookup"><span data-stu-id="19dda-662">Build 16273</span></span>

<span data-ttu-id="19dda-663">一般 Windows 組建 16273 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-664">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-665">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-665">WSL</span></span>
- <span data-ttu-id="19dda-666">已修正的問題 DrvFs 有時報告目錄 [GH 2392] 錯誤的檔案類型</span><span class="sxs-lookup"><span data-stu-id="19dda-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="19dda-667">允許建立 NETLINK_KOBJECT_UEVENT 通訊端，若要解除封鎖程式，使用 uevent [GH 1121，2293，2242年、 2295年 2235，648、 637]</span><span class="sxs-lookup"><span data-stu-id="19dda-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="19dda-668">新增支援非封鎖連線 [GH 903，1391，1584年、 1585年、 1829年、 2290年、 2314年]</span><span class="sxs-lookup"><span data-stu-id="19dda-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="19dda-669">實作 CLONE_FS 複製系統呼叫旗標 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="19dda-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="19dda-670">修正問題不會處理索引標籤或 NT interop [GH 1625，2164年] 中正確的引號</span><span class="sxs-lookup"><span data-stu-id="19dda-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="19dda-671">解決錯誤時嘗試重新啟動 WSL 執行個體 [GH 651、 2095年] 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="19dda-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="19dda-672">實作 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 作業 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="19dda-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="19dda-673">修正各種 SysFs 檔案 [GH 2214] 的權限</span><span class="sxs-lookup"><span data-stu-id="19dda-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="19dda-674">在安裝 [GH 2290] 期間修正 Haskell 堆疊停止回應</span><span class="sxs-lookup"><span data-stu-id="19dda-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="19dda-675">實作 binfmt_misc 'C' 'o' 和 'P' 旗標 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="19dda-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="19dda-676">加入 /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="19dda-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="19dda-677">新增部分支援 ioprio_set 系統呼叫 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="19dda-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="19dda-678">虛設常式 SO_REUSEPORT & 新增支援 SO_PASSCRED netlink 通訊端 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="19dda-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="19dda-679">從 RegisterDistribuiton 傳回不同的錯誤碼，如果目前正在發佈安裝或解除安裝。</span><span class="sxs-lookup"><span data-stu-id="19dda-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="19dda-680">允許部分安裝 WSL 散發 wslconfig.exe 透過取消的註冊</span><span class="sxs-lookup"><span data-stu-id="19dda-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="19dda-681">修正從 udp::msg_peek python 通訊端測試停止回應</span><span class="sxs-lookup"><span data-stu-id="19dda-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="19dda-682">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-683">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-683">Console</span></span>
- <span data-ttu-id="19dda-684">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-685">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-685">LTP Results:</span></span>
<span data-ttu-id="19dda-686">測試總計：1904</span><span class="sxs-lookup"><span data-stu-id="19dda-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="19dda-687">總略過測試：209</span><span class="sxs-lookup"><span data-stu-id="19dda-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="19dda-688">失敗總數：229</span><span class="sxs-lookup"><span data-stu-id="19dda-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="19dda-689">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="19dda-690">組建 16257</span><span class="sxs-lookup"><span data-stu-id="19dda-690">Build 16257</span></span>

<span data-ttu-id="19dda-691">一般 Windows 組建 16257 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-692">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-693">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-693">WSL</span></span>
- <span data-ttu-id="19dda-694">實作 prlimit64 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="19dda-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="19dda-695">新增支援 ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="19dda-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="19dda-696">虛設常式 MSG_MORE 針對 TCP 通訊端 [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="19dda-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="19dda-697">修正無效的 AT_EXECFN 輔助向量行為 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="19dda-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="19dda-698">修正主控台/tty，複製/貼上的行為並新增更好的完整緩衝處理 [GH 2204，2131年]</span><span class="sxs-lookup"><span data-stu-id="19dda-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="19dda-699">設定使用者識別碼和設定群組識別碼程式 [GH 2031] 的輔助向量中設定 AT_SECURE</span><span class="sxs-lookup"><span data-stu-id="19dda-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="19dda-700">虛擬終端機主要端點不會處理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="19dda-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="19dda-701">修正 lseek 會更新，以倒轉 LxFs [GH 2310] 中的目錄</span><span class="sxs-lookup"><span data-stu-id="19dda-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="19dda-702">/dev/ptmx 鎖之後的繁重使用量 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="19dda-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="19dda-703">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-704">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-704">Console</span></span>
- <span data-ttu-id="19dda-705">針對水平列/底線 Everywhere [GH 2168] 修正程式</span><span class="sxs-lookup"><span data-stu-id="19dda-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="19dda-706">修正程序順序變更並關閉 [GH 2170] 的工作變得更難的 NPM</span><span class="sxs-lookup"><span data-stu-id="19dda-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="19dda-707">加入我們新的色彩配置： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="19dda-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-708">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-708">LTP Results:</span></span>
<span data-ttu-id="19dda-709">16251 後並無變更</span><span class="sxs-lookup"><span data-stu-id="19dda-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-710">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-710">Syscall Support</span></span>
<span data-ttu-id="19dda-711">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-712">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="19dda-713">已知問題</span><span class="sxs-lookup"><span data-stu-id="19dda-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="19dda-714">GitHub 問題 2392年:無法辨識的 WSL Windows 資料夾...</span><span class="sxs-lookup"><span data-stu-id="19dda-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="19dda-715">在組建中 16257，WSL 有問題時列舉 Windows 檔案/資料夾透過`/mnt/c/...`。</span><span class="sxs-lookup"><span data-stu-id="19dda-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="19dda-716">已修正此問題，因此應該在發行測試人員組建開始時間 2017 年 8 月 14 日一週內。</span><span class="sxs-lookup"><span data-stu-id="19dda-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="19dda-717">建置 16251</span><span class="sxs-lookup"><span data-stu-id="19dda-717">Build 16251</span></span>

<span data-ttu-id="19dda-718">一般 Windows 組建 16251 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-719">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-720">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-720">WSL</span></span>
- <span data-ttu-id="19dda-721">Beta 標記移除 WSL 選用元件，請參閱 <<c0> [ 部落格文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="19dda-722">正確初始化儲存組 uid 與 gid exec [GH 962，1415，2072年] 上設定使用者識別碼和設定群組識別碼的二進位檔</span><span class="sxs-lookup"><span data-stu-id="19dda-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="19dda-723">已新增的支援 ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="19dda-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="19dda-724">已新增支援 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET NT_FPREGSET [GH 555] 與</span><span class="sxs-lookup"><span data-stu-id="19dda-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="19dda-725">已修正 ptrace 若要停止忽略訊號</span><span class="sxs-lookup"><span data-stu-id="19dda-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="19dda-726">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-727">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-727">Console</span></span>
- <span data-ttu-id="19dda-728">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="19dda-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-729">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-729">LTP Results:</span></span>
<span data-ttu-id="19dda-730">成功的測試數目：768</span><span class="sxs-lookup"><span data-stu-id="19dda-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="19dda-731">失敗的測試數目：244</span><span class="sxs-lookup"><span data-stu-id="19dda-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="19dda-732">已略過的測試數目：96</span><span class="sxs-lookup"><span data-stu-id="19dda-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="19dda-733">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="19dda-734">建置 16241</span><span class="sxs-lookup"><span data-stu-id="19dda-734">Build 16241</span></span>

<span data-ttu-id="19dda-735">一般 Windows 組建 16241 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-736">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="19dda-737">WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-737">WSL</span></span>
- <span data-ttu-id="19dda-738">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="19dda-739">Console</span><span class="sxs-lookup"><span data-stu-id="19dda-739">Console</span></span>
- <span data-ttu-id="19dda-740">修正錯誤的字元輸出的交叉線年 12 月原本報告[這裡](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="19dda-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="19dda-741">不修正在字碼頁 65001 (utf-8) 中顯示任何輸出文字</span><span class="sxs-lookup"><span data-stu-id="19dda-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="19dda-742">不會傳送至選取範圍變更調色盤的其他部分的一種色彩的 RGB 值所做的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="19dda-743">這會讓主控台內容工作表頁更容易使用。</span><span class="sxs-lookup"><span data-stu-id="19dda-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="19dda-744">Ctrl + S 似乎未正確運作</span><span class="sxs-lookup"><span data-stu-id="19dda-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="19dda-745">非粗體 /-維度沒有完全從 ANSI 逸出程式碼 [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="19dda-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="19dda-746">主控台不會正確支援 Vim 色彩佈景主題 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="19dda-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="19dda-747">無法貼上的特定字元 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="19dda-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="19dda-748">自動重排調整互動奇怪調整 bash 視窗的大小，在 [編輯] / [命令列 [GH ConEmu 1123] 上的東西時</span><span class="sxs-lookup"><span data-stu-id="19dda-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="19dda-749">Ctrl-L 離開畫面已變更 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="19dda-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="19dda-750">HDPI [GH 1907] 上顯示 VT 時，主控台轉譯 bug</span><span class="sxs-lookup"><span data-stu-id="19dda-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="19dda-751">Japansese 字元很陌生與 Unicode 字元 U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="19dda-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="19dda-752">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="19dda-753">組建 16237</span><span class="sxs-lookup"><span data-stu-id="19dda-753">Build 16237</span></span>

<span data-ttu-id="19dda-754">一般 Windows 組建 16237 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-755">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-755">Fixed</span></span>
- <span data-ttu-id="19dda-756">使用預設屬性，而不需要 EAs lxfs （根目錄、 根目錄，0000） 中的檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="19dda-757">已新增的支援使用擴充的屬性的散發套件</span><span class="sxs-lookup"><span data-stu-id="19dda-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="19dda-758">修正填補 getdents 和 getdents64 所傳回的項目</span><span class="sxs-lookup"><span data-stu-id="19dda-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="19dda-759">修正 shmctl SHM_STAT 系統呼叫 [GH 2068] 的權限檢查</span><span class="sxs-lookup"><span data-stu-id="19dda-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="19dda-760">已修正不正確的初始 epoll tty [GH 2231] 狀態</span><span class="sxs-lookup"><span data-stu-id="19dda-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="19dda-761">修正 DrvFs readdir 不會傳回所有項目 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="19dda-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="19dda-762">修正 LxFs readdir 檔案時已取消連結 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="19dda-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="19dda-763">允許透過 procfs 重新開啟的檔案未連結的 drvfs</span><span class="sxs-lookup"><span data-stu-id="19dda-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="19dda-764">新增全域登錄金鑰覆寫停用 WSL 功能 (interop / 磁碟機掛接)</span><span class="sxs-lookup"><span data-stu-id="19dda-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="19dda-765">修正 「 狀態 」 中的不正確的區塊計數 DrvFs （以及 LxFs） [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="19dda-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="19dda-766">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="19dda-767">建置 16232</span><span class="sxs-lookup"><span data-stu-id="19dda-767">Build 16232</span></span>

<span data-ttu-id="19dda-768">一般 Windows 組建 16232 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-769">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-769">Fixed</span></span>
- <span data-ttu-id="19dda-770">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="19dda-771">建置 16226</span><span class="sxs-lookup"><span data-stu-id="19dda-771">Build 16226</span></span>

<span data-ttu-id="19dda-772">一般 Windows 組建 16226 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-773">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-773">Fixed</span></span>
- <span data-ttu-id="19dda-774">xattr 相關 syscall 支援 （getxattr、 setxattr、 listxattr、 removexattr）。</span><span class="sxs-lookup"><span data-stu-id="19dda-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="19dda-775">security.capablity xattr 支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="19dda-776">改進的相容性與特定的檔案系統篩選器，包括非 MS SMB 伺服器。</span><span class="sxs-lookup"><span data-stu-id="19dda-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="19dda-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="19dda-777">[GH #1952]</span></span>
- <span data-ttu-id="19dda-778">改善對 OneDrive 預留位置、 GVFS 預留位置和精簡的 OS 支援壓縮的檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="19dda-779">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="19dda-780">建置 16215</span><span class="sxs-lookup"><span data-stu-id="19dda-780">Build 16215</span></span>

<span data-ttu-id="19dda-781">一般 Windows 組建 16215 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-782">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-782">Fixed</span></span>
- <span data-ttu-id="19dda-783">WSL 不再需要開發人員模式。</span><span class="sxs-lookup"><span data-stu-id="19dda-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="19dda-784">支援 drvfs 目錄連接。</span><span class="sxs-lookup"><span data-stu-id="19dda-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="19dda-785">處理的 WSL 發佈 appx 套件解除安裝。</span><span class="sxs-lookup"><span data-stu-id="19dda-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="19dda-786">更新 procfs 顯示私用和共用對應。</span><span class="sxs-lookup"><span data-stu-id="19dda-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="19dda-787">新增 wslconfig.exe 清除部分安裝或解除安裝的散發套件的能力。</span><span class="sxs-lookup"><span data-stu-id="19dda-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="19dda-788">已新增的支援 IP_MTU_DISCOVER 針對 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="19dda-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="19dda-789">[GH 1639，2115，2205年]</span><span class="sxs-lookup"><span data-stu-id="19dda-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="19dda-790">推斷 AF_INADDR 路由通訊協定家族。</span><span class="sxs-lookup"><span data-stu-id="19dda-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="19dda-791">序列裝置的功能改進 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="19dda-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="19dda-792">建置 16199</span><span class="sxs-lookup"><span data-stu-id="19dda-792">Build 16199</span></span>

<span data-ttu-id="19dda-793">一般 Windows 組建 16199 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-794">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-794">Fixed</span></span>
- <span data-ttu-id="19dda-795">沒有 WSL 相關的這些版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="19dda-796">建置 16193</span><span class="sxs-lookup"><span data-stu-id="19dda-796">Build 16193</span></span>

<span data-ttu-id="19dda-797">一般 Windows 組建 16193 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-798">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-798">Fixed</span></span>
- <span data-ttu-id="19dda-799">傳送 SIGCONT 以及終止 [GH 1973] threadgroup 之間的競爭情形</span><span class="sxs-lookup"><span data-stu-id="19dda-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="19dda-800">將報表而不是 [GH 1840] FILE_DEVICE_CONSOLE FILE_DEVICE_NAMED_PIPE tty 和 pty 裝置</span><span class="sxs-lookup"><span data-stu-id="19dda-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="19dda-801">SSH IP_OPTIONS 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="19dda-802">移動 DrvFs 掛接至 init 精靈 [GH 1862，1968 年，1767年、 1933年]</span><span class="sxs-lookup"><span data-stu-id="19dda-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="19dda-803">已新增的支援在 DrvFs 遵循 NT 符號連結。</span><span class="sxs-lookup"><span data-stu-id="19dda-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="19dda-804">建置 16184</span><span class="sxs-lookup"><span data-stu-id="19dda-804">Build 16184</span></span>

<span data-ttu-id="19dda-805">一般 Windows 組建 16184 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-806">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-806">Fixed</span></span>
- <span data-ttu-id="19dda-807">已移除的 apt 套件維護工作 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="19dda-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="19dda-808">已修正未出現在從 node.js [GH 1840] 中的 Windows 處理序的輸出</span><span class="sxs-lookup"><span data-stu-id="19dda-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="19dda-809">放寬 lxcore [GH 1794] 中的對齊需求</span><span class="sxs-lookup"><span data-stu-id="19dda-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="19dda-810">已修正的數系統呼叫的 AT_EMPTY_PATH 旗標的處理。</span><span class="sxs-lookup"><span data-stu-id="19dda-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="19dda-811">已修正的問題，其中刪除 DrvFs 檔案含有開啟控制代碼，會導致檔案出現未定義的行為 [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="19dda-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="19dda-812">eg /etc/ 主機現在將會從 Windows hosts 檔案 (%windir%\system32\drivers\etc\hosts) 繼承項目 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="19dda-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="19dda-813">建置 16179</span><span class="sxs-lookup"><span data-stu-id="19dda-813">Build 16179</span></span>

<span data-ttu-id="19dda-814">一般 Windows 組建 16179 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-815">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-815">Fixed</span></span>
- <span data-ttu-id="19dda-816">沒有 WSL 變更本週。</span><span class="sxs-lookup"><span data-stu-id="19dda-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="19dda-817">建置 16176</span><span class="sxs-lookup"><span data-stu-id="19dda-817">Build 16176</span></span>

<span data-ttu-id="19dda-818">一般 Windows 組建 16176 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-819">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-819">Fixed</span></span>

- [<span data-ttu-id="19dda-820">已啟用序列的支援</span><span class="sxs-lookup"><span data-stu-id="19dda-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="19dda-821">已新增的 IP 通訊端選項 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="19dda-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="19dda-822">（在檔案上傳至 nginx/PHP-FPM） 實作 pwritev 函式 [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="19dda-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="19dda-823">新增 IP 通訊端選項 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="19dda-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="19dda-824">支援的通訊端選項 IP_MULTICAST_LOOP IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="19dda-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="19dda-825">已新增適用於應用程式節點、 追蹤路由、 dig、 nslookup、 主機 IP (V6) _MTU 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="19dda-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="19dda-826">已新增的 IP 通訊端選項 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="19dda-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="19dda-827">檔案系統的增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="19dda-828">允許的 UNC 路徑的掛接</span><span class="sxs-lookup"><span data-stu-id="19dda-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="19dda-829">啟用在 drvfs CDFS 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="19dda-830">正確處理 drvfs 中的網路檔案系統權限</span><span class="sxs-lookup"><span data-stu-id="19dda-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="19dda-831">支援遠端磁碟機新增至 drvfs</span><span class="sxs-lookup"><span data-stu-id="19dda-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="19dda-832">啟用 FAT drvfs 中支援</span><span class="sxs-lookup"><span data-stu-id="19dda-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="19dda-833">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-834">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="19dda-834">LTP Results</span></span>
<span data-ttu-id="19dda-835">自 15042 後的任何變更</span><span class="sxs-lookup"><span data-stu-id="19dda-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="19dda-836">建置 16170</span><span class="sxs-lookup"><span data-stu-id="19dda-836">Build 16170</span></span>

<span data-ttu-id="19dda-837">一般 Windows 組建 16170 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="19dda-838">我們發行了新[部落格文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)討論我們努力測試 WSL。</span><span class="sxs-lookup"><span data-stu-id="19dda-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-839">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-839">Fixed</span></span>

- <span data-ttu-id="19dda-840">支援通訊端選項 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="19dda-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="19dda-841">新增對 PTRACE_OLDSETOPTIONS 支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="19dda-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="19dda-842">[GH 1692]</span></span>
- <span data-ttu-id="19dda-843">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-844">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="19dda-844">LTP Results</span></span>
<span data-ttu-id="19dda-845">自 15042 後的任何變更</span><span class="sxs-lookup"><span data-stu-id="19dda-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="19dda-846">建置 15046 到 Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="19dda-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="19dda-847">沒有更多的 WSL 修正或加入至 Windows 10 Creators Update 中的功能。</span><span class="sxs-lookup"><span data-stu-id="19dda-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="19dda-848">在未來幾週的目標設為下一個主要的 Windows 更新的新增項目中，將會繼續 WSL 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="19dda-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="19dda-849">針對一般的 Windows 上建置 15046 和未來的測試人員的資訊發行版本，請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="19dda-850">建置 15042</span><span class="sxs-lookup"><span data-stu-id="19dda-850">Build 15042</span></span>

<span data-ttu-id="19dda-851">一般 Windows 組建 15042 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-852">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-852">Fixed</span></span>

- <span data-ttu-id="19dda-853">移除路徑，在結束時，產生死結的修正"."</span><span class="sxs-lookup"><span data-stu-id="19dda-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="19dda-854">已修正的問題其中 FIONBIO 未成功 [GH 1683] 傳回 0</span><span class="sxs-lookup"><span data-stu-id="19dda-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="19dda-855">已修正的問題 inet 資料包通訊端讀取長度為零</span><span class="sxs-lookup"><span data-stu-id="19dda-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="19dda-856">修正 [drvfs inode 查閱 [GH 1675] 中的 [可能的死結，因為競爭條件</span><span class="sxs-lookup"><span data-stu-id="19dda-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="19dda-857">擴充支援 unix 通訊端的輔助資料;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514，613、 1326年]</span><span class="sxs-lookup"><span data-stu-id="19dda-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="19dda-858">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-859">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-859">LTP Results:</span></span>
<span data-ttu-id="19dda-860">通過測試數目：737</span><span class="sxs-lookup"><span data-stu-id="19dda-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="19dda-861">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="19dda-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="19dda-862">建置 15031</span><span class="sxs-lookup"><span data-stu-id="19dda-862">Build 15031</span></span>

<span data-ttu-id="19dda-863">一般 Windows 組建 15031 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-864">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-864">Fixed</span></span>

- <span data-ttu-id="19dda-865">修正了其中 time(2) 會偶發性行為異常。</span><span class="sxs-lookup"><span data-stu-id="19dda-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="19dda-866">已修正，並發出 where \* SIGPROCMASK syscall 可能會損毀訊號遮罩。</span><span class="sxs-lookup"><span data-stu-id="19dda-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="19dda-867">現在會傳回完整的命令列長度在 WSL 程序建立通知。</span><span class="sxs-lookup"><span data-stu-id="19dda-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="19dda-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="19dda-868">[GH 1632]</span></span>
- <span data-ttu-id="19dda-869">WSL 現在會報告執行緒結束時，透過 ptrace 的 GDB 停止回應。</span><span class="sxs-lookup"><span data-stu-id="19dda-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="19dda-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="19dda-870">[GH 1196]</span></span>
- <span data-ttu-id="19dda-871">已修正的 bug，其中 ptys 會停止回應之後大量 tmux IO。</span><span class="sxs-lookup"><span data-stu-id="19dda-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="19dda-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="19dda-872">[GH 1358]</span></span>
- <span data-ttu-id="19dda-873">許多系統呼叫 （futex、 semtimedop、 ppoll、 sigtimedwait、 itimer、 timer_create） 中的固定的逾時驗證</span><span class="sxs-lookup"><span data-stu-id="19dda-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="19dda-874">已新增的 eventfd EFD_SEMAPHORE 支援 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="19dda-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="19dda-875">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-876">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-876">LTP Results:</span></span>
<span data-ttu-id="19dda-877">通過測試數目：737</span><span class="sxs-lookup"><span data-stu-id="19dda-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="19dda-878">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="19dda-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="19dda-879">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="19dda-880">建置 15025</span><span class="sxs-lookup"><span data-stu-id="19dda-880">Build 15025</span></span>

<span data-ttu-id="19dda-881">一般 Windows 組建 15025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-882">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-882">Fixed</span></span>

- <span data-ttu-id="19dda-883">修正 bug，沒壞的 grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="19dda-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="19dda-884">實作的 eventfd2 syscall [GH 452] EFD_SEMAPHORE 旗標</span><span class="sxs-lookup"><span data-stu-id="19dda-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="19dda-885">實作 /proc/ [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="19dda-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="19dda-886">訊號驅動 IO 支援 unix 資料流通訊端 [GH 393，68]</span><span class="sxs-lookup"><span data-stu-id="19dda-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="19dda-887">支援 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="19dda-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="19dda-888">實作 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="19dda-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="19dda-889">已修正的 bug epoll_wait() 不正在等候 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="19dda-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="19dda-890">實作 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="19dda-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="19dda-891">Tee syscall 現在會傳回失敗，如果這兩個檔案描述元參考到相同的管道</span><span class="sxs-lookup"><span data-stu-id="19dda-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="19dda-892">實作正確的行為 SO_PEERCRED Unix 通訊端</span><span class="sxs-lookup"><span data-stu-id="19dda-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="19dda-893">固定的 tkill syscall 無效參數處理方法</span><span class="sxs-lookup"><span data-stu-id="19dda-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="19dda-894">若要增加的 drvfs preformace 的變更</span><span class="sxs-lookup"><span data-stu-id="19dda-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="19dda-895">Ruby IO 封鎖的次要修正</span><span class="sxs-lookup"><span data-stu-id="19dda-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="19dda-896">固定的 recvmsg() 傳回 EINVAL MSG_DONTWAIT 旗標的 inet 通訊端 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="19dda-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="19dda-897">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-898">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-898">LTP Results:</span></span>
<span data-ttu-id="19dda-899">通過測試數目：732</span><span class="sxs-lookup"><span data-stu-id="19dda-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="19dda-900">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="19dda-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="19dda-901">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="19dda-902">Build 15019</span><span class="sxs-lookup"><span data-stu-id="19dda-902">Build 15019</span></span>

<span data-ttu-id="19dda-903">一般 Windows build 15019 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-904">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-904">Fixed</span></span>

- <span data-ttu-id="19dda-905">已修正的 bug，正確地報告中的 CPU 使用量 procfs htop (GH 823 945、 971) 等工具</span><span class="sxs-lookup"><span data-stu-id="19dda-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="19dda-906">當呼叫 open （） 與 O_TRUNC 上的現有檔案 inotify 現在會產生之前 IN_OPEN IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="19dda-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="19dda-907">Unix 通訊端 getsockopt SO_ERROR 啟用 postgress [GH 61，1354年] 修正程式</span><span class="sxs-lookup"><span data-stu-id="19dda-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="19dda-908">實作 /proc/sys/net/core/somaxconn GO 語言</span><span class="sxs-lookup"><span data-stu-id="19dda-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="19dda-909">Apt get 封裝更新背景工作現在會隱藏執行檢視</span><span class="sxs-lookup"><span data-stu-id="19dda-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="19dda-910">清除範圍 ipv6 localhost （Spring-Framework(Java) 失敗）。</span><span class="sxs-lookup"><span data-stu-id="19dda-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="19dda-911">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-912">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-912">LTP Results:</span></span>
<span data-ttu-id="19dda-913">通過測試數目：714</span><span class="sxs-lookup"><span data-stu-id="19dda-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="19dda-914">非通過的數字 (失敗，所以已略過等等。...):249</span><span class="sxs-lookup"><span data-stu-id="19dda-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="19dda-915">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="19dda-916">建置 15014</span><span class="sxs-lookup"><span data-stu-id="19dda-916">Build 15014</span></span>

<span data-ttu-id="19dda-917">一般 Windows 組建 15014 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="19dda-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-918">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-918">Fixed</span></span>

- <span data-ttu-id="19dda-919">Ctrl + C 現在如預期般運作</span><span class="sxs-lookup"><span data-stu-id="19dda-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="19dda-920">htop 和 ps auxw 現在顯示正確的資源使用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="19dda-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="19dda-921">基本訊號的 NT 例外狀況的翻譯。</span><span class="sxs-lookup"><span data-stu-id="19dda-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="19dda-922">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="19dda-922">(GH #513)</span></span>
- <span data-ttu-id="19dda-923">fallocate 現在 ENOSPC 時發生無法用盡空間，而不是 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="19dda-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="19dda-924">已新增的 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="19dda-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="19dda-925">實作的 semop 和 semtimedop 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="19dda-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="19dda-926">固定的 nslookup 錯誤 IP_RECVTOS & IPV6_RECVTCLASS 通訊端選項 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="19dda-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="19dda-927">支援通訊端選項 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="19dda-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="19dda-928">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-929">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-929">LTP Results:</span></span>
<span data-ttu-id="19dda-930">通過測試數目：709</span><span class="sxs-lookup"><span data-stu-id="19dda-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="19dda-931">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="19dda-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="19dda-932">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="19dda-933">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="19dda-933">Syscall Summary</span></span>
<span data-ttu-id="19dda-934">總 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="19dda-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="19dda-935">實作的總計：235</span><span class="sxs-lookup"><span data-stu-id="19dda-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="19dda-936">虛設常式的總計：22</span><span class="sxs-lookup"><span data-stu-id="19dda-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="19dda-937">如果未實作的總計：127</span><span class="sxs-lookup"><span data-stu-id="19dda-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="19dda-938">詳細分解圖</span><span class="sxs-lookup"><span data-stu-id="19dda-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="19dda-939">建置 15007</span><span class="sxs-lookup"><span data-stu-id="19dda-939">Build 15007</span></span>

<span data-ttu-id="19dda-940">一般 Windows 組建 15007 的詳細資訊請造訪[Windows 部落格]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="19dda-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="19dda-941">已知的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-941">Known Issue</span></span>

- <span data-ttu-id="19dda-942">已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。</span><span class="sxs-lookup"><span data-stu-id="19dda-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="19dda-943">這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="19dda-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="19dda-944">因應措施：替代的索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="19dda-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="19dda-945">例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="19dda-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="19dda-946">此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。</span><span class="sxs-lookup"><span data-stu-id="19dda-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="19dda-947">使用者可以瀏覽的選項包含在其 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="19dda-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-948">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-948">Fixed</span></span>

- <span data-ttu-id="19dda-949">已更正此問題，其中執行 WSL 會消耗掉 100%的 CPU 核心</span><span class="sxs-lookup"><span data-stu-id="19dda-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="19dda-950">通訊端選項 IP_PKTINFO，IPV6_RECVPKTINFO 現在支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="19dda-951">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="19dda-951">(GH #851, 987)</span></span>
- <span data-ttu-id="19dda-952">截斷的 lxcore 16 個位元組到網路介面實體位址 (GH #1452 1414，1343，468，308)</span><span class="sxs-lookup"><span data-stu-id="19dda-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="19dda-953">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-954">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-954">LTP Results:</span></span>
<span data-ttu-id="19dda-955">通過測試數目：709</span><span class="sxs-lookup"><span data-stu-id="19dda-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="19dda-956">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="19dda-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="19dda-957">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="19dda-958">建置 15002</span><span class="sxs-lookup"><span data-stu-id="19dda-958">Build 15002</span></span>

<span data-ttu-id="19dda-959">一般 Windows 組建 15002 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="19dda-960">已知的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-960">Known Issue</span></span>

<span data-ttu-id="19dda-961">兩個已知的問題：</span><span class="sxs-lookup"><span data-stu-id="19dda-961">Two known issues:</span></span>
- <span data-ttu-id="19dda-962">已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。</span><span class="sxs-lookup"><span data-stu-id="19dda-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="19dda-963">這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="19dda-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="19dda-964">因應措施：替代的索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="19dda-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="19dda-965">例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="19dda-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="19dda-966">此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。</span><span class="sxs-lookup"><span data-stu-id="19dda-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="19dda-967">使用者可以瀏覽的選項包含在其 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="19dda-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="19dda-968">執行 WSL 時系統執行緒會耗用的 CPU 核心的 100%。</span><span class="sxs-lookup"><span data-stu-id="19dda-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="19dda-969">已解決的根本原因並已修正在內部。</span><span class="sxs-lookup"><span data-stu-id="19dda-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-970">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-970">Fixed</span></span>

- <span data-ttu-id="19dda-971">所有的 bash 工作階段現在必須建立在相同的權限層級。</span><span class="sxs-lookup"><span data-stu-id="19dda-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="19dda-972">嘗試啟動工作階段在不同的層級會被封鎖。</span><span class="sxs-lookup"><span data-stu-id="19dda-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="19dda-973">這表示系統管理員 」 和 「 非系統管理員主控台無法在同一時間執行。</span><span class="sxs-lookup"><span data-stu-id="19dda-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="19dda-974">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="19dda-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="19dda-975">實作下列 NETLINK_ROUTE 訊息 （需要 Windows 系統管理員）</span><span class="sxs-lookup"><span data-stu-id="19dda-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="19dda-976">RTM_NEWADDR (支援`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="19dda-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="19dda-977">RTM_NEWROUTE (支援`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="19dda-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="19dda-978">RTM_DELADDR (支援`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="19dda-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="19dda-979">RTM_DELROUTE (支援`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="19dda-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="19dda-980">在計量付費連線 (GH #1371) 上，將無法再執行套件，以更新檢查的排程的工作</span><span class="sxs-lookup"><span data-stu-id="19dda-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="19dda-981">已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="19dda-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="19dda-982">實作的 TCP_KEEPCNT 通訊端選項 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="19dda-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="19dda-983">實作的 IP_MTU_DISCOVER INET 通訊端選項 (GH #720，717，170，69)</span><span class="sxs-lookup"><span data-stu-id="19dda-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="19dda-984">移除舊版的功能，以從 NT 路徑查閱使用 init 執行 NT 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="19dda-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="19dda-985">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="19dda-985">(GH #1325)</span></span>
- <span data-ttu-id="19dda-986">修正/kmsg 允許群組 / 讀取權限 (0644) (GH #1321) 模式</span><span class="sxs-lookup"><span data-stu-id="19dda-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="19dda-987">實作的 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="19dda-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="19dda-988">修正的錯誤，處理序開始時間會顯示為 2432 年 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="19dda-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="19dda-989">切換的預設詞彙環境變數，以 xterm 256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="19dda-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="19dda-990">修改處理認可的方式計算期間處理程序分支。</span><span class="sxs-lookup"><span data-stu-id="19dda-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="19dda-991">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="19dda-991">(GH #1286)</span></span>
- <span data-ttu-id="19dda-992">實作的 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="19dda-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="19dda-993">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="19dda-993">(GH #1286)</span></span>
- <span data-ttu-id="19dda-994">實作的 /proc/net/route 檔案 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="19dda-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="19dda-995">已修正的錯誤捷徑名稱的正確當地語系化 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="19dda-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="19dda-996">已修正剖析邏輯，不正確地驗證程式的標頭的 elf 必須小於 （或等於） PATH_MAX。</span><span class="sxs-lookup"><span data-stu-id="19dda-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="19dda-997">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="19dda-997">(GH #1048)</span></span>
- <span data-ttu-id="19dda-998">實作的 statfs 回呼 procfs，sysfs、 cgroupfs，和 binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="19dda-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="19dda-999">不會關閉 (GH #1184，也在 GH # 1193年中討論) 的固定的 AptPackageIndexUpdate windows</span><span class="sxs-lookup"><span data-stu-id="19dda-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="19dda-1000">已新增的 ASLR 個性 ADDR_NO_RANDOMIZE 支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="19dda-1001">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="19dda-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="19dda-1002">改善的 PTRACE_GETSIGINFO，SIGSEGV，針對適當 gdb AV (GH #875) 期間的堆疊追蹤</span><span class="sxs-lookup"><span data-stu-id="19dda-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="19dda-1003">Elf 剖析不會再失敗 patchelf 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="19dda-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="19dda-1004">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="19dda-1004">(GH #471)</span></span>
- <span data-ttu-id="19dda-1005">VPN DNS 傳播至 /etc/resolv.conf (GH #416，1350年)</span><span class="sxs-lookup"><span data-stu-id="19dda-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="19dda-1006">改善 TCP 關閉更可靠的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="19dda-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="19dda-1007">(GH #610 616、 1025，1335年)</span><span class="sxs-lookup"><span data-stu-id="19dda-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="19dda-1008">開啟 (EMFILE) 現在會傳回正確的錯誤程式碼中，使用太多檔案時。</span><span class="sxs-lookup"><span data-stu-id="19dda-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="19dda-1009">(GH # 1126年 2090年)</span><span class="sxs-lookup"><span data-stu-id="19dda-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="19dda-1010">Windows 稽核記錄檔現在報告程序中的映像名稱建立稽核。</span><span class="sxs-lookup"><span data-stu-id="19dda-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="19dda-1011">現在依正常程序失敗時啟動 bash 視窗內從 bash.exe</span><span class="sxs-lookup"><span data-stu-id="19dda-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="19dda-1012">當 interop 新增的錯誤訊息無法存取工作目錄下 LxFs (也就是 notepad.exe.bashrc)</span><span class="sxs-lookup"><span data-stu-id="19dda-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="19dda-1013">已修正的問題已在 WSL 遭截斷 Windows 路徑</span><span class="sxs-lookup"><span data-stu-id="19dda-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="19dda-1014">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1015">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1015">LTP Results:</span></span>
<span data-ttu-id="19dda-1016">通過測試數目：690</span><span class="sxs-lookup"><span data-stu-id="19dda-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="19dda-1017">非通過的數字 (失敗，所以已略過等等。...):274</span><span class="sxs-lookup"><span data-stu-id="19dda-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="19dda-1018">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1019">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1019">Syscall Support</span></span>
<span data-ttu-id="19dda-1020">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1021">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="19dda-1022">建置 14986</span><span class="sxs-lookup"><span data-stu-id="19dda-1022">Build 14986</span></span>

<span data-ttu-id="19dda-1023">一般 Windows 組建 14986 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1024">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1024">Fixed</span></span>

- <span data-ttu-id="19dda-1025">固定的 bugchecks Netlink 與 Pty Ioctl</span><span class="sxs-lookup"><span data-stu-id="19dda-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="19dda-1026">核心版本現在會報告 4.4.0-43 與 Xenial 的一致性</span><span class="sxs-lookup"><span data-stu-id="19dda-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="19dda-1027">輸入指示時，現在會啟動 Bash.exe ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="19dda-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="19dda-1028">執行緒現在報告識別碼正確 procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="19dda-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="19dda-1029">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |現在支援 inotify_add_watch() (GH #1280) IN_ISDIR 旗標</span><span class="sxs-lookup"><span data-stu-id="19dda-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="19dda-1030">實作 timer_create 和相關的系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="19dda-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="19dda-1031">這可讓 GHC 支援 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="19dda-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="19dda-1032">已修正的問題，其中 ping 傳回 0.000ms (GH #1296) 的時間</span><span class="sxs-lookup"><span data-stu-id="19dda-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="19dda-1033">開啟太多檔案時，則傳回正確的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19dda-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="19dda-1034">已修正的問題，在 WSL 其中網路介面 data Netlink 要求會失敗並 EINVAL 如果介面的硬體位址為 32 個位元組 （例如 Teredo 介面）</span><span class="sxs-lookup"><span data-stu-id="19dda-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="19dda-1035">請注意，Linux 「 ip 」 公用程式，包含的 bug，其中這皆會損毀如果 WSL 報告 32 位元組的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="19dda-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="19dda-1036">這是 「 ip 」，不 WSL 中的 bug。</span><span class="sxs-lookup"><span data-stu-id="19dda-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="19dda-1037">「 Ip 」 公用程式硬式編碼的字串緩衝區長度用來列印的硬體位址，以及該緩衝區太小而無法列印的 32 位元組的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="19dda-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="19dda-1038">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1039">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1039">LTP Results:</span></span>
<span data-ttu-id="19dda-1040">通過測試數目：669</span><span class="sxs-lookup"><span data-stu-id="19dda-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="19dda-1041">非通過的數字 (失敗，所以已略過等等。...):258</span><span class="sxs-lookup"><span data-stu-id="19dda-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="19dda-1042">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1043">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1043">Syscall Support</span></span>
<span data-ttu-id="19dda-1044">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1045">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="19dda-1046">建置 14971</span><span class="sxs-lookup"><span data-stu-id="19dda-1046">Build 14971</span></span>

<span data-ttu-id="19dda-1047">一般 Windows 組建 14971 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1048">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1048">Fixed</span></span>

 - <span data-ttu-id="19dda-1049">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="19dda-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="19dda-1050">下一個版本時才會恢復有排定來定期更新。</span><span class="sxs-lookup"><span data-stu-id="19dda-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1051">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1051">LTP Results:</span></span>
<span data-ttu-id="19dda-1052">從 14965 以來並未變更</span><span class="sxs-lookup"><span data-stu-id="19dda-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="19dda-1053">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="19dda-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="19dda-1054">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1055">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="19dda-1056">建置 14965</span><span class="sxs-lookup"><span data-stu-id="19dda-1056">Build 14965</span></span>

<span data-ttu-id="19dda-1057">一般 Windows 組建 14965 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1058">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1058">Fixed</span></span>

- <span data-ttu-id="19dda-1059">支援 Netlink 通訊端通訊協定 NETLINK_ROUTE RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="19dda-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="19dda-1060">可讓網路列舉的 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="19dda-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="19dda-1061">詳細的資訊可在我們[WSL 網路部落格文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="19dda-1062">/sbin 現在是使用者的預設路徑</span><span class="sxs-lookup"><span data-stu-id="19dda-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="19dda-1063">現在預設 （也就是您可以現在輸入 notepad.exe 而不會增加 System32 Linux 路徑），以附加至 WSL 路徑的 NT 使用者路徑</span><span class="sxs-lookup"><span data-stu-id="19dda-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="19dda-1064">已新增的支援 /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="19dda-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="19dda-1065">NT 二進位檔可以立即從 WSL 啟動，當目前的工作目錄包含非 ansi 字元 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="19dda-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="19dda-1066">允許在已中斷連線的 unix 資料流通訊端上的關機。</span><span class="sxs-lookup"><span data-stu-id="19dda-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="19dda-1067">已新增的支援 PR_GET_PDEATHSIG。</span><span class="sxs-lookup"><span data-stu-id="19dda-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="19dda-1068">已新增的支援 CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="19dda-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="19dda-1069">已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="19dda-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="19dda-1070">若要連接到目前的終端機的控制代碼要求。</span><span class="sxs-lookup"><span data-stu-id="19dda-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="19dda-1071">標示 /proc/<pid>/oom_score_adj 為可寫入。</span><span class="sxs-lookup"><span data-stu-id="19dda-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="19dda-1072">新增 /sys/fs/cgroup 資料夾。</span><span class="sxs-lookup"><span data-stu-id="19dda-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="19dda-1073">sched_setaffinity 應傳回數目相似性位元遮罩</span><span class="sxs-lookup"><span data-stu-id="19dda-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="19dda-1074">修正未正確假設 解譯器路徑必須少於 64 個字元長 ELF 驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="19dda-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="19dda-1075">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="19dda-1075">(GH #743)</span></span>
- <span data-ttu-id="19dda-1076">開啟檔案描述元可以保留主控台視窗中開啟 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="19dda-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="19dda-1077">Fixeed 錯誤 rename （） 後面加上目標名稱 (GH #1008) 的正斜線失敗的位置</span><span class="sxs-lookup"><span data-stu-id="19dda-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="19dda-1078">實作 /proc/net/dev 檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="19dda-1079">固定的 0.000ms 偵測由於計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="19dda-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="19dda-1080">實作的 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="19dda-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="19dda-1081">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1082">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1082">LTP Results:</span></span>
<span data-ttu-id="19dda-1083">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="19dda-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="19dda-1084">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1085">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="19dda-1086">建置 14959</span><span class="sxs-lookup"><span data-stu-id="19dda-1086">Build 14959</span></span>

<span data-ttu-id="19dda-1087">一般 Windows 組建 14959 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1088">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1088">Fixed</span></span>

- <span data-ttu-id="19dda-1089">已改進的 Windows 的 Pico 程序通知。</span><span class="sxs-lookup"><span data-stu-id="19dda-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="19dda-1090">其他資訊，請參閱[WSL 部落格](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="19dda-1091">改進的穩定性與 Windows 互通性</span><span class="sxs-lookup"><span data-stu-id="19dda-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="19dda-1092">已修正的錯誤 0x80070057 啟用企業資料保護 (EDP) 時，啟動 bash.exe 時</span><span class="sxs-lookup"><span data-stu-id="19dda-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="19dda-1093">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1094">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1094">LTP Results:</span></span>
<span data-ttu-id="19dda-1095">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="19dda-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="19dda-1096">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1097">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="19dda-1098">建置 14955</span><span class="sxs-lookup"><span data-stu-id="19dda-1098">Build 14955</span></span>

<span data-ttu-id="19dda-1099">一般 Windows 組建 14955 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1100">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1100">Fixed</span></span>

 - <span data-ttu-id="19dda-1101">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="19dda-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="19dda-1102">下一個版本時才會恢復有排定來定期更新。</span><span class="sxs-lookup"><span data-stu-id="19dda-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1103">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1103">LTP Results:</span></span>
<span data-ttu-id="19dda-1104">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="19dda-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="19dda-1105">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1106">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="19dda-1107">建置 14951</span><span class="sxs-lookup"><span data-stu-id="19dda-1107">Build 14951</span></span>

<span data-ttu-id="19dda-1108">一般 Windows 組建 14951 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="19dda-1109">新功能：Windows / Ubuntu 互通性</span><span class="sxs-lookup"><span data-stu-id="19dda-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="19dda-1110">現在可以直接從 WSL 命令列叫用 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="19dda-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="19dda-1111">這可讓使用者使用他們的 Windows 環境和系統的方式一直無法互動的能力。</span><span class="sxs-lookup"><span data-stu-id="19dda-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="19dda-1112">快速的範例，就可以讓使用者執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="19dda-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="19dda-1113">詳細資訊，參閱：</span><span class="sxs-lookup"><span data-stu-id="19dda-1113">More information can be found at:</span></span>

- [<span data-ttu-id="19dda-1114">Interop 的 WSL 小組部落格</span><span class="sxs-lookup"><span data-stu-id="19dda-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="19dda-1115">MSDN Interop 文件</span><span class="sxs-lookup"><span data-stu-id="19dda-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1116">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1116">Fixed</span></span>

- <span data-ttu-id="19dda-1117">Ubuntu 16.04 (Xenial) 現在會安裝所有新的 WSL 執行個體。</span><span class="sxs-lookup"><span data-stu-id="19dda-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="19dda-1118">使用現有的 14.04 (Mible) 執行個體的使用者將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="19dda-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="19dda-1119">現在會顯示在安裝期間設定的地區設定</span><span class="sxs-lookup"><span data-stu-id="19dda-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="19dda-1120">終端機功能改良，包括的 bug，其中將 WSL 程序重新導向至檔案不一定不會運作</span><span class="sxs-lookup"><span data-stu-id="19dda-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="19dda-1121">主控台存留期應該繫結至 bash.exe 存留期</span><span class="sxs-lookup"><span data-stu-id="19dda-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="19dda-1122">主控台視窗大小應該使用可見的大小，而非緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="19dda-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="19dda-1123">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1124">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1124">LTP Results:</span></span>
<span data-ttu-id="19dda-1125">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="19dda-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="19dda-1126">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1127">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="19dda-1128">建置 14946</span><span class="sxs-lookup"><span data-stu-id="19dda-1128">Build 14946</span></span>

<span data-ttu-id="19dda-1129">一般 Windows 組建 14946 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1130">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1130">Fixed</span></span>

- <span data-ttu-id="19dda-1131">已修正的問題，導致無法建立 WSL 之使用者的使用者帳戶為 NT 使用者名稱包含空格或引號。</span><span class="sxs-lookup"><span data-stu-id="19dda-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="19dda-1132">變更 VolFs 和 DrvFs，以傳回狀態 0 代表目錄的連結計數</span><span class="sxs-lookup"><span data-stu-id="19dda-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="19dda-1133">支援 IPV6_MULTICAST_HOPS 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="19dda-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="19dda-1134">I/O 迴圈每 tty 限制為單一主控台中。</span><span class="sxs-lookup"><span data-stu-id="19dda-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="19dda-1135">範例： 可能是下列命令：</span><span class="sxs-lookup"><span data-stu-id="19dda-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="19dda-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="19dda-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="19dda-1137">空格取代為 /proc/cpuinfo (GH #1115) 中的索引標籤</span><span class="sxs-lookup"><span data-stu-id="19dda-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="19dda-1138">DrvFs 現在會出現在 mountinfo 符合掛接的 Windows 磁碟區的名稱</span><span class="sxs-lookup"><span data-stu-id="19dda-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="19dda-1139">/home 和 /root 現在會出現在 mountinfo 具有正確的名稱</span><span class="sxs-lookup"><span data-stu-id="19dda-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="19dda-1140">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1141">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1141">LTP Results:</span></span>
<span data-ttu-id="19dda-1142">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="19dda-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="19dda-1143">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1144">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="19dda-1145">建置 14942</span><span class="sxs-lookup"><span data-stu-id="19dda-1145">Build 14942</span></span>

<span data-ttu-id="19dda-1146">一般 Windows 組建 14942 的詳細資訊請造訪[Windows 部落格](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1147">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1147">Fixed</span></span>

- <span data-ttu-id="19dda-1148">數個 bugchecks 解決，包括 「 嘗試執行的 NOEXECUTE 記憶體 」 網路已封鎖 SSH 的損毀</span><span class="sxs-lookup"><span data-stu-id="19dda-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="19dda-1149">來自 DrvFs 上的 Windows 應用程式所產生之通知的 inotifiy 支援現為</span><span class="sxs-lookup"><span data-stu-id="19dda-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="19dda-1150">實作 TCP_KEEPIDLE 和 TCP_KEEPINTVL mongod。</span><span class="sxs-lookup"><span data-stu-id="19dda-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="19dda-1151">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="19dda-1151">(GH #695)</span></span>
- <span data-ttu-id="19dda-1152">實作 pivot_root 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="19dda-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="19dda-1153">實作 SO_DONTROUTE 的通訊端選項</span><span class="sxs-lookup"><span data-stu-id="19dda-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="19dda-1154">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="19dda-1155">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1155">LTP Results:</span></span>
<span data-ttu-id="19dda-1156">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="19dda-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="19dda-1157">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="19dda-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="19dda-1158">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1159">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1159">Syscall Support</span></span>
<span data-ttu-id="19dda-1160">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1161">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="19dda-1162">建置 14936</span><span class="sxs-lookup"><span data-stu-id="19dda-1162">Build 14936</span></span>

<span data-ttu-id="19dda-1163">一般 Windows 組建 14936 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="19dda-1164">注意：WSL 會安裝在即將推出的版本中的 Ubuntu 16.04 版 (Xenial) 而不是 Ubuntu 14.04 （駒）。</span><span class="sxs-lookup"><span data-stu-id="19dda-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="19dda-1165">這項變更將套用到安裝新的執行個體 （lxrun.exe /install 或 bash.exe 第一次執行） 的測試人員。</span><span class="sxs-lookup"><span data-stu-id="19dda-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="19dda-1166">具有可信賴的現有執行個體將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="19dda-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="19dda-1167">使用者可以 Xenial 使用執行版本升級 命令來升級其 Mible 映像。</span><span class="sxs-lookup"><span data-stu-id="19dda-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="19dda-1168">已知的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1168">Known Issue</span></span>
<span data-ttu-id="19dda-1169">WSL 發生某些通訊端實作的問題。</span><span class="sxs-lookup"><span data-stu-id="19dda-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="19dda-1170">檢查錯誤會造成系統呈現的損毀並出現錯誤 「 嘗試執行的 NOEXECUTE 記憶體 」。</span><span class="sxs-lookup"><span data-stu-id="19dda-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="19dda-1171">此問題最常見的現象使用 ssh 時當機。</span><span class="sxs-lookup"><span data-stu-id="19dda-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="19dda-1172">修正內部組建並將測試人員儘早推送根本原因。</span><span class="sxs-lookup"><span data-stu-id="19dda-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-1173">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1173">Fixed</span></span>

- <span data-ttu-id="19dda-1174">實作 chroot 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="19dda-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="19dda-1175">改進 inotify~~包括來自 DrvFs 上的 Windows 應用程式所產生之通知的支援~~</span><span class="sxs-lookup"><span data-stu-id="19dda-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="19dda-1176">修正：Inotify 支援來自 Windows 應用程式無法使用目前的變更。</span><span class="sxs-lookup"><span data-stu-id="19dda-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="19dda-1177">通訊端繫結的 ipv6::<port n>現在支援 IPV6_V6ONLY (GH #68、 #157、 #393、 #460、 #674、 #740、 #982、 #996)</span><span class="sxs-lookup"><span data-stu-id="19dda-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="19dda-1178">Waitid systemcall WNOWAIT 行為實作 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="19dda-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="19dda-1179">支援 IP 通訊端選項 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="19dda-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="19dda-1180">長度為零的 read （） 應該會立即傳回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="19dda-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="19dda-1181">正確處理不在.tar 檔案中包含 NULL 結束字元的檔名和檔案名稱前置詞。</span><span class="sxs-lookup"><span data-stu-id="19dda-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="19dda-1182">/dev/null 時發生 epoll 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="19dda-1183">修正 /dev/alarm 時間來源</span><span class="sxs-lookup"><span data-stu-id="19dda-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="19dda-1184">Bash-c 現在能夠重新導向至檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="19dda-1185">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1186">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1186">LTP Results:</span></span>
<span data-ttu-id="19dda-1187">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="19dda-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="19dda-1188">非通過的數字 (失敗，所以已略過等等。...):264</span><span class="sxs-lookup"><span data-stu-id="19dda-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="19dda-1189">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1190">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1190">Syscall Support</span></span>
<span data-ttu-id="19dda-1191">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1192">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="19dda-1193">建置 14931</span><span class="sxs-lookup"><span data-stu-id="19dda-1193">Build 14931</span></span>

<span data-ttu-id="19dda-1194">一般 Windows 組建 14931 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1195">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1195">Fixed</span></span>

 - <span data-ttu-id="19dda-1196">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="19dda-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="19dda-1197">下一個版本中，將會繼續定期排定的更新。</span><span class="sxs-lookup"><span data-stu-id="19dda-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="19dda-1198">建置 14926</span><span class="sxs-lookup"><span data-stu-id="19dda-1198">Build 14926</span></span>

<span data-ttu-id="19dda-1199">一般 Windows 組建 14926 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1200">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1200">Fixed</span></span>

- <span data-ttu-id="19dda-1201">Ping 現在可在主控台中確實具備系統管理員權限</span><span class="sxs-lookup"><span data-stu-id="19dda-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="19dda-1202">現在支援，也沒有管理員權限的 ping 6</span><span class="sxs-lookup"><span data-stu-id="19dda-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="19dda-1203">Inotify 支援透過 WSL 修改的檔案。</span><span class="sxs-lookup"><span data-stu-id="19dda-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="19dda-1204">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="19dda-1204">(GH #216)</span></span>
  - <span data-ttu-id="19dda-1205">支援的旗標：</span><span class="sxs-lookup"><span data-stu-id="19dda-1205">Flags supported:</span></span>
    - <span data-ttu-id="19dda-1206">inotify_init1:LX_O_CLOEXEC LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="19dda-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="19dda-1207">inotify_add_watch 事件：LX_IN_ACCESS、 LX_IN_MODIFY、 LX_IN_ATTRIB、 LX_IN_CLOSE_WRITE、 LX_IN_CLOSE_NOWRITE、 LX_IN_OPEN、 LX_IN_MOVED_FROM、 LX_IN_MOVED_TO、 LX_IN_CREATE、 LX_IN_DELETE、 LX_IN_DELETE_SELF、 LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="19dda-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="19dda-1208">inotify_add_watch 屬性：LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="19dda-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="19dda-1209">讀取輸出：LX_IN_ISDIR LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="19dda-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="19dda-1210">已知的問題：修改檔案從 Windows 應用程式不會產生任何事件</span><span class="sxs-lookup"><span data-stu-id="19dda-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="19dda-1211">Unix 通訊端現在支援 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="19dda-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="19dda-1212">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="19dda-1212">LTP Results:</span></span>
<span data-ttu-id="19dda-1213">通過測試數目：651</span><span class="sxs-lookup"><span data-stu-id="19dda-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="19dda-1214">非通過的數字 (失敗，所以已略過等等。...):258</span><span class="sxs-lookup"><span data-stu-id="19dda-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="19dda-1215">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="19dda-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="19dda-1216">建置 14915</span><span class="sxs-lookup"><span data-stu-id="19dda-1216">Build 14915</span></span>

<span data-ttu-id="19dda-1217">一般 Windows 組建 14915 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1218">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1218">Fixed</span></span>
-  <span data-ttu-id="19dda-1219">Socketpair unix 資料包通訊端 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="19dda-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="19dda-1220">SO_REUSEADDR Unix 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="19dda-1221">SO_BROADCAST (GH #568) 的 UNIX 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="19dda-1222">SOCK_SEQPACKET (GH #758，#546) 的 Unix 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="19dda-1223">新增支援 unix 資料包通訊端的傳送、 接收和關閉</span><span class="sxs-lookup"><span data-stu-id="19dda-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="19dda-1224">修正由於非固定位址的無效 mmap 參數驗證錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="19dda-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="19dda-1225">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="19dda-1225">(GH #847)</span></span>
- <span data-ttu-id="19dda-1226">支援的暫止 / 繼續的終端機的狀態</span><span class="sxs-lookup"><span data-stu-id="19dda-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="19dda-1227">若要解除封鎖 「 螢幕 」 公用程式 (GH #774) TIOCPKT ioctl 的支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="19dda-1228">已知的問題：功能鍵無法運作</span><span class="sxs-lookup"><span data-stu-id="19dda-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="19dda-1229">已更正的競爭可能會導致將釋放的成員 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814) 存取的 TimerFd</span><span class="sxs-lookup"><span data-stu-id="19dda-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="19dda-1230">啟用 futex、 輪詢和 clock_nanosleep 的可重新啟動系統呼叫支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="19dda-1231">新增繫結掛接支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1231">Added bind mount support</span></span>
- <span data-ttu-id="19dda-1232">如需掛接命名空間支援取消共用</span><span class="sxs-lookup"><span data-stu-id="19dda-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="19dda-1233">已知的問題：當建立新的掛接命名空間與`unshare(CLONE_NEWNS)`仍然指向舊的命名空間目前的工作目錄</span><span class="sxs-lookup"><span data-stu-id="19dda-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="19dda-1234">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="19dda-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="19dda-1235">建置 14905</span><span class="sxs-lookup"><span data-stu-id="19dda-1235">Build 14905</span></span>

<span data-ttu-id="19dda-1236">一般 Windows 組建 14905 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1237">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1237">Fixed</span></span>
- <span data-ttu-id="19dda-1238">可重新啟動系統呼叫現在支援 (GH #349，GH #520)</span><span class="sxs-lookup"><span data-stu-id="19dda-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="19dda-1239">結束在 / 現在操作的目錄 (GH #650) 的符號連結</span><span class="sxs-lookup"><span data-stu-id="19dda-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="19dda-1240">實作的 RNDGETENTCNT ioctl /dev/random 的</span><span class="sxs-lookup"><span data-stu-id="19dda-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="19dda-1241">實作 /proc/ [pid] / 掛接，/proc/ [pid] / mountinfo 和 /proc/ [pid] / mountstats 檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="19dda-1242">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="19dda-1243">建置 14901</span><span class="sxs-lookup"><span data-stu-id="19dda-1243">Build 14901</span></span>
<span data-ttu-id="19dda-1244">第一次的測試人員組建的 Windows 10 年度更新版的文章。</span><span class="sxs-lookup"><span data-stu-id="19dda-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="19dda-1245">一般 Windows 組建 14901 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1246">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1246">Fixed</span></span>
- <span data-ttu-id="19dda-1247">已修正的尾端斜線問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="19dda-1248">命令，例如`$ mv a/c/ a/b/`現在可運作</span><span class="sxs-lookup"><span data-stu-id="19dda-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="19dda-1249">只有當 Ubuntu 地區設定應該設為 Windows 地區設定，現在安裝提示</span><span class="sxs-lookup"><span data-stu-id="19dda-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="19dda-1250">Procfs 支援 ns 資料夾</span><span class="sxs-lookup"><span data-stu-id="19dda-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="19dda-1251">新增掛接和卸載 tmpfs procfs 和 sysfs 檔案系統</span><span class="sxs-lookup"><span data-stu-id="19dda-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="19dda-1252">修正 mknod [at] 32 位元 ABI 簽章</span><span class="sxs-lookup"><span data-stu-id="19dda-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="19dda-1253">移至分派模型的 Unix 通訊端</span><span class="sxs-lookup"><span data-stu-id="19dda-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="19dda-1254">設定使用 setsockopt INET 通訊端接收緩衝區大小應該接受</span><span class="sxs-lookup"><span data-stu-id="19dda-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="19dda-1255">實作 MSG_CMSG_CLOEXEC unix 通訊端接收訊息的旗標</span><span class="sxs-lookup"><span data-stu-id="19dda-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="19dda-1256">Linux 程序 stdin/stdout 管道重新導向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="19dda-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="19dda-1257">允許的 CMD 中的 bash-c 命令的管線</span><span class="sxs-lookup"><span data-stu-id="19dda-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="19dda-1258">範例： > dir |bash-c"grep foo"</span><span class="sxs-lookup"><span data-stu-id="19dda-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="19dda-1259">現在可以在多個分頁檔 (GH #538，#358) 的系統上安裝 bash</span><span class="sxs-lookup"><span data-stu-id="19dda-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="19dda-1260">預設 INET 通訊端緩衝區大小應該符合預設 Ubuntu 安裝程式</span><span class="sxs-lookup"><span data-stu-id="19dda-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="19dda-1261">對齊到 listxattr xattr syscall</span><span class="sxs-lookup"><span data-stu-id="19dda-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="19dda-1262">只從 SIOCGIFCONF 傳回有效的 IPv4 位址的介面</span><span class="sxs-lookup"><span data-stu-id="19dda-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="19dda-1263">修正當由 ptrace 插入的訊號的預設動作</span><span class="sxs-lookup"><span data-stu-id="19dda-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="19dda-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="19dda-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="19dda-1265">還原在 sigreturn 內容時所使用電腦內容暫存器值</span><span class="sxs-lookup"><span data-stu-id="19dda-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="19dda-1266">這個方法可以解決此問題其中的某些使用者溢出 java 和 javac</span><span class="sxs-lookup"><span data-stu-id="19dda-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="19dda-1267">實作 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="19dda-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1268">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1268">Syscall Support</span></span>
<span data-ttu-id="19dda-1269">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1270">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="19dda-1271">建置 Windows 10 年度更新版的 14388</span><span class="sxs-lookup"><span data-stu-id="19dda-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="19dda-1272">一般 Windows 組建 14388 的詳細資訊請造訪[Windows 部落格](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1273">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1273">Fixed</span></span>
- <span data-ttu-id="19dda-1274">準備適用於 Windows 10 年度更新 8/2 的修正</span><span class="sxs-lookup"><span data-stu-id="19dda-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="19dda-1275">在年度更新版的 WSL 的詳細資訊都位於我們[部落格](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="19dda-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="19dda-1276">建置 14376</span><span class="sxs-lookup"><span data-stu-id="19dda-1276">Build 14376</span></span>
<span data-ttu-id="19dda-1277">一般 Windows 組建 14376 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1278">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1278">Fixed</span></span>
- <span data-ttu-id="19dda-1279">移除某些情況下，apt get 停止回應 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="19dda-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="19dda-1280">已修正的問題，空白的掛接已無法正確處理</span><span class="sxs-lookup"><span data-stu-id="19dda-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="19dda-1281">已修正的問題其中 ramdisks 已不正確地掛載</span><span class="sxs-lookup"><span data-stu-id="19dda-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="19dda-1282">變更 unix 通訊端接受支援旗標 (部分 GH #451)</span><span class="sxs-lookup"><span data-stu-id="19dda-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="19dda-1283">已修正常見的網路相關藍色螢幕</span><span class="sxs-lookup"><span data-stu-id="19dda-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="19dda-1284">存取 /proc/ [pid] 時，已修正藍色螢幕 / 工作 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="19dda-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="19dda-1285">已修正的 CPU 使用率過高的一些 pty 案例 (GH #488，#504)</span><span class="sxs-lookup"><span data-stu-id="19dda-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="19dda-1286">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="19dda-1287">建置 14371</span><span class="sxs-lookup"><span data-stu-id="19dda-1287">Build 14371</span></span>
<span data-ttu-id="19dda-1288">一般 Windows 組建 14371 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1289">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1289">Fixed</span></span>
- <span data-ttu-id="19dda-1290">當使用 ptrace 更正 SIGCHLD 與 wait() 計時競爭</span><span class="sxs-lookup"><span data-stu-id="19dda-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="19dda-1291">當路徑有尾端時修正某些行為 / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="19dda-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="19dda-1292">取消重新命名/連結來失敗的原因是子系的開啟控制代碼已修正的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="19dda-1293">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="19dda-1294">建置 14366</span><span class="sxs-lookup"><span data-stu-id="19dda-1294">Build 14366</span></span>
<span data-ttu-id="19dda-1295">一般 Windows 組建 14366 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1296">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1296">Fixed</span></span>
- <span data-ttu-id="19dda-1297">修正透過符號連結的檔案建立時</span><span class="sxs-lookup"><span data-stu-id="19dda-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="19dda-1298">已新增的 listxattr 適用於 Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="19dda-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="19dda-1299">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1300">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1300">Syscall Support</span></span>
-   <span data-ttu-id="19dda-1301">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1302">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="19dda-1303">組建 14361 開始</span><span class="sxs-lookup"><span data-stu-id="19dda-1303">Build 14361</span></span>
<span data-ttu-id="19dda-1304">一般 Windows 組建 14361 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1305">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1305">Fixed</span></span>
- <span data-ttu-id="19dda-1306">Windows 上執行 bash on Ubuntu 時，DrvFs 現在會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="19dda-1307">使用者可能 case.txt 和案例。TXT 其 /mnt c 磁碟機</span><span class="sxs-lookup"><span data-stu-id="19dda-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="19dda-1308">在 Windows 上 Ubuntu 之 Bash 上才支援區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="19dda-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="19dda-1309">當外部 Bash NTFS 的報表檔案的正確，但未預期的行為可能會發生與從 Windows 檔案互動。</span><span class="sxs-lookup"><span data-stu-id="19dda-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="19dda-1310">每個磁碟區 (也就是 /mnt/c) 的根目錄不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="19dda-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="19dda-1311">可以找到更多有關處理 Windows 中的這些檔案[此處](https://support.microsoft.com/en-us/kb/100625)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="19dda-1312">經過大幅增強的 pty / tty 支援。</span><span class="sxs-lookup"><span data-stu-id="19dda-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="19dda-1313">應用程式，例如 TMUX 現在支援 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="19dda-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="19dda-1314">使用者帳戶不一定建立固定的安裝問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="19dda-1315">最佳化以很長的引數清單的命令列引數結構。</span><span class="sxs-lookup"><span data-stu-id="19dda-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="19dda-1316">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="19dda-1316">(GH #153)</span></span>
- <span data-ttu-id="19dda-1317">現在可以刪除並 chmod read_only 檔案從 DrvFs</span><span class="sxs-lookup"><span data-stu-id="19dda-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="19dda-1318">已修正某些情況下，終端機的停止回應，在中斷連線 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="19dda-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="19dda-1319">chmod 和 chown 現在使用 tty 裝置</span><span class="sxs-lookup"><span data-stu-id="19dda-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="19dda-1320">允許連線至 0.0.0.0 和:: 為 localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="19dda-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="19dda-1321">Sendmsg/recvmsg 現在處理的 IO 向量長度 > 1 (部分 GH #376)</span><span class="sxs-lookup"><span data-stu-id="19dda-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="19dda-1322">使用者可以立即選擇不自動產生的主機檔案 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="19dda-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="19dda-1323">自動安裝 (GH #11) 期間會符合 Linux NT 地區設定的地區設定</span><span class="sxs-lookup"><span data-stu-id="19dda-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="19dda-1324">新增 /proc/sys/vm/swappiness 檔案 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="19dda-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="19dda-1325">才能正確 strace 現在結束</span><span class="sxs-lookup"><span data-stu-id="19dda-1325">strace now exits correctly</span></span>
- <span data-ttu-id="19dda-1326">允許管道來重新開啟透過 /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="19dda-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="19dda-1327">隱藏 %LOCALAPPDATA%\lxss 從 DrvFs (GH #270) 下的目錄</span><span class="sxs-lookup"><span data-stu-id="19dda-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="19dda-1328">更妥善地處理的 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="19dda-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="19dda-1329">命令喜歡"bash ~-c ls 」 現在支援 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="19dda-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="19dda-1330">通訊端現在，當 epoll 關機 (GH #271) 期間所提供的讀取</span><span class="sxs-lookup"><span data-stu-id="19dda-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="19dda-1331">lxrun / 解除安裝的刪除的檔案和資料夾工作</span><span class="sxs-lookup"><span data-stu-id="19dda-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="19dda-1332">已更正的 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="19dda-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="19dda-1333">已改善支援 x11 xEmacs (GH #481) 之類的應用程式</span><span class="sxs-lookup"><span data-stu-id="19dda-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="19dda-1334">已更新初始執行緒堆疊大小，以符合預設 Ubuntu 設定，並正確地回報給 get_rlimit syscall (GH #172，#258) 的大小</span><span class="sxs-lookup"><span data-stu-id="19dda-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="19dda-1335">改善報告 pico 程序映像名稱 （例如，適用於稽核）</span><span class="sxs-lookup"><span data-stu-id="19dda-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="19dda-1336">實作的 /proc/mountinfo df 命令</span><span class="sxs-lookup"><span data-stu-id="19dda-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="19dda-1337">已修正子名稱的符號連結錯誤程式碼。</span><span class="sxs-lookup"><span data-stu-id="19dda-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="19dda-1338">與...</span><span class="sxs-lookup"><span data-stu-id="19dda-1338">and ..</span></span>
- <span data-ttu-id="19dda-1339">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1340">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1340">Syscall Support</span></span>
<span data-ttu-id="19dda-1341">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1342">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="19dda-1343">組建 14352</span><span class="sxs-lookup"><span data-stu-id="19dda-1343">Build 14352</span></span>
<span data-ttu-id="19dda-1344">一般 Windows 組建 14352 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1345">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1345">Fixed</span></span>
- <span data-ttu-id="19dda-1346">已修正的問題，大型檔案已下載 / 無法正確建立。</span><span class="sxs-lookup"><span data-stu-id="19dda-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="19dda-1347">這應該解除封鎖 npm 和其他案例 （GH #3，GH #313）</span><span class="sxs-lookup"><span data-stu-id="19dda-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="19dda-1348">移除某些情況下通訊端的停止回應</span><span class="sxs-lookup"><span data-stu-id="19dda-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="19dda-1349">修正一些 ptrace 錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="19dda-1350">已修正的問題，以允許檔案名稱超過 255 個字元的 WSL</span><span class="sxs-lookup"><span data-stu-id="19dda-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="19dda-1351">非英文字元的改進的支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="19dda-1352">加入目前的 Windows 時區資料，並設定為預設值</span><span class="sxs-lookup"><span data-stu-id="19dda-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="19dda-1353">唯一裝置識別碼的每個掛接點 （jre 修復 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="19dda-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="19dda-1354">包含路徑與修正問題 」。 」</span><span class="sxs-lookup"><span data-stu-id="19dda-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="19dda-1355">和"."</span><span class="sxs-lookup"><span data-stu-id="19dda-1355">and “..”</span></span>
- <span data-ttu-id="19dda-1356">已新增的 Fifo 支援 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="19dda-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="19dda-1357">更新的 resolv.conf 來比對原生的 Ubuntu 格式的格式</span><span class="sxs-lookup"><span data-stu-id="19dda-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="19dda-1358">某些 procfs 的清除工作</span><span class="sxs-lookup"><span data-stu-id="19dda-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="19dda-1359">系統管理員主控台 (GH #18) 的已啟用的 ping</span><span class="sxs-lookup"><span data-stu-id="19dda-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1360">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1360">Syscall Support</span></span>
<span data-ttu-id="19dda-1361">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1362">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="19dda-1363">建置 14342</span><span class="sxs-lookup"><span data-stu-id="19dda-1363">Build 14342</span></span>
<span data-ttu-id="19dda-1364">一般的 Windows 上的資訊建置 14342 [Windows 部落格](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="19dda-1365">可以上找到有關 VolFs 和 DriveFs [WSL 部落格](https://blogs.msdn.microsoft.com/wsl)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="19dda-1366">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1366">Fixed</span></span>
- <span data-ttu-id="19dda-1367">Windows 使用者的使用者名稱中有 Unicode 字元時，已修正安裝問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="19dda-1368">第一次執行的預設現在會提供常見問題集中的 apt get 更新 udev 因應措施</span><span class="sxs-lookup"><span data-stu-id="19dda-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="19dda-1369">啟用 DriveFs 中的符號連結 (於 /mnt/<drive>) 目錄</span><span class="sxs-lookup"><span data-stu-id="19dda-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="19dda-1370">符號連結現在可 DriveFs 和 VolFs 之間</span><span class="sxs-lookup"><span data-stu-id="19dda-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="19dda-1371">定址頂部層級路徑剖析的問題： ls。 / / 現在會如預期般運作</span><span class="sxs-lookup"><span data-stu-id="19dda-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="19dda-1372">npm 安裝上 DriveFs 和現在正設法-g 選項</span><span class="sxs-lookup"><span data-stu-id="19dda-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="19dda-1373">已修正防止 PHP 伺服器啟動的問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="19dda-1374">已更新的預設環境的值，例如更接近比對原生的 Ubuntu $PATH</span><span class="sxs-lookup"><span data-stu-id="19dda-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="19dda-1375">更新 apt 套件快取的 Windows 中加入每週的維護工作</span><span class="sxs-lookup"><span data-stu-id="19dda-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="19dda-1376">ELF 標頭驗證修正問題，WSL 現在支援所有 Melkor 選項</span><span class="sxs-lookup"><span data-stu-id="19dda-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="19dda-1377">Zsh shell 正常運作</span><span class="sxs-lookup"><span data-stu-id="19dda-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="19dda-1378">先行編譯的 Go 二進位檔現在支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="19dda-1379">在第一次執行的 Bash.exe 提示是現在正確當地語系化</span><span class="sxs-lookup"><span data-stu-id="19dda-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="19dda-1380">/proc/meminfo 現在會傳回正確的資訊</span><span class="sxs-lookup"><span data-stu-id="19dda-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="19dda-1381">VFS 現可支援的通訊端</span><span class="sxs-lookup"><span data-stu-id="19dda-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="19dda-1382">/dev 現在已掛接為 tempfs</span><span class="sxs-lookup"><span data-stu-id="19dda-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="19dda-1383">Fifo 現在支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1383">Fifo now supported</span></span>
- <span data-ttu-id="19dda-1384">多核心系統現在/proc/cpuinfo 中正確顯示</span><span class="sxs-lookup"><span data-stu-id="19dda-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="19dda-1385">其他增強功能與在第一次執行期間所下載的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="19dda-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="19dda-1386">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="19dda-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="19dda-1387">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="19dda-1388">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="19dda-1389">已知問題</span><span class="sxs-lookup"><span data-stu-id="19dda-1389">Known Issues</span></span>
- <span data-ttu-id="19dda-1390">無法解析 '.'</span><span class="sxs-lookup"><span data-stu-id="19dda-1390">Not resolving ‘..’</span></span> <span data-ttu-id="19dda-1391">在某些情況下 DriveFs 上的正確</span><span class="sxs-lookup"><span data-stu-id="19dda-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1392">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1392">Syscall Support</span></span>
<span data-ttu-id="19dda-1393">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="19dda-1394">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="19dda-1395">建置 14332</span><span class="sxs-lookup"><span data-stu-id="19dda-1395">Build 14332</span></span>

<span data-ttu-id="19dda-1396">一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="19dda-1397">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1397">Fixed</span></span>
- <span data-ttu-id="19dda-1398">改良的 resolv.conf 產生包括設定 DNS 項目優先順序</span><span class="sxs-lookup"><span data-stu-id="19dda-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="19dda-1399">移動檔案和目錄，以及非 /mnt 之間的問題-/ /mnt 磁碟機</span><span class="sxs-lookup"><span data-stu-id="19dda-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="19dda-1400">您現在可以使用符號連結建立 tar 檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="19dda-1401">在 建立執行個體上新增的預設 /run/lock 目錄</span><span class="sxs-lookup"><span data-stu-id="19dda-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="19dda-1402">若要傳回適當的狀態資訊更新 /dev/null 時發生</span><span class="sxs-lookup"><span data-stu-id="19dda-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="19dda-1403">下載期間第一次執行時的其他錯誤</span><span class="sxs-lookup"><span data-stu-id="19dda-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="19dda-1404">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="19dda-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="19dda-1405">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="19dda-1406">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1407">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1407">Syscall Support</span></span>
<span data-ttu-id="19dda-1408">以下是新 syscall WSL 中有某種實作。</span><span class="sxs-lookup"><span data-stu-id="19dda-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="19dda-1409">在這份清單 syscall 在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="19dda-1410">組建 14328</span><span class="sxs-lookup"><span data-stu-id="19dda-1410">Build 14328</span></span>

<span data-ttu-id="19dda-1411">一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="19dda-1412">新功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1412">New Features</span></span>
* <span data-ttu-id="19dda-1413">現在支援 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="19dda-1413">Now support Linux users.</span></span>  <span data-ttu-id="19dda-1414">在 Windows 上 Ubuntu 上安裝 Bash 會提示輸入建立 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="19dda-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="19dda-1415">如需詳細資訊，請瀏覽 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="19dda-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="19dda-1416">主機名稱現在已不再設定為 Windows 電腦的名稱， @localhost</span><span class="sxs-lookup"><span data-stu-id="19dda-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="19dda-1417">如需詳細資訊請組建 14328，請瀏覽： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="19dda-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="19dda-1418">固定式</span><span class="sxs-lookup"><span data-stu-id="19dda-1418">Fixed</span></span>
* <span data-ttu-id="19dda-1419">非於 /mnt/ 的符號連結改進<drive>檔案</span><span class="sxs-lookup"><span data-stu-id="19dda-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="19dda-1420">npm 安裝現在的運作方式</span><span class="sxs-lookup"><span data-stu-id="19dda-1420">npm install now works</span></span>
    * <span data-ttu-id="19dda-1421">jdk 現在可安裝的 jre 使用指示[此處](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)。</span><span class="sxs-lookup"><span data-stu-id="19dda-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="19dda-1422">已知問題： 符號連結無法運作的 Windows 掛接。</span><span class="sxs-lookup"><span data-stu-id="19dda-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="19dda-1423">功能可在更新的組建</span><span class="sxs-lookup"><span data-stu-id="19dda-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="19dda-1424">top 和 htop 現在會顯示</span><span class="sxs-lookup"><span data-stu-id="19dda-1424">top and htop now display</span></span>
* <span data-ttu-id="19dda-1425">其他錯誤訊息，某些安裝失敗</span><span class="sxs-lookup"><span data-stu-id="19dda-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="19dda-1426">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="19dda-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="19dda-1427">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="19dda-1428">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="19dda-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="19dda-1429">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="19dda-1429">Syscall Support</span></span>
<span data-ttu-id="19dda-1430">以下是 syscall 的某些實作在 WSL 的清單。</span><span class="sxs-lookup"><span data-stu-id="19dda-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="19dda-1431">Syscall 在這份清單中至少一個案例中，支援，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="19dda-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
