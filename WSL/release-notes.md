---
title: 適用於 Linux 的 Windows 子系統的版本資訊
description: 適用於 Linux 的 Windows 子系統的版本資訊。  每週更新。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu 的 windows 子系統
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063626"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="5e18f-105">適用於 Linux 的 Windows 子系統的版本資訊</span><span class="sxs-lookup"><span data-stu-id="5e18f-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18342"></a><span data-ttu-id="5e18f-106">建置 18342</span><span class="sxs-lookup"><span data-stu-id="5e18f-106">Build 18342</span></span>
<span data-ttu-id="5e18f-107">一般 Windows 組建 18342 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-107">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-108">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-108">WSL</span></span>
* <span data-ttu-id="5e18f-109">我們已新增可讓使用者從 Windows 存取在 WSL 散發版本的 Linux 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-109">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="5e18f-110">這些檔案可以透過命令列，以及 Windows 應用程式，例如 [檔案總管] 中，VSCode，等等，都可以與這些檔案互動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-110">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="5e18f-111">存取檔案，請瀏覽至\\ \\wsl$\\< distro_name >，或看到一份瀏覽至執行散發套件\\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="5e18f-111">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="5e18f-112">新增額外的 CPU 資訊標記，並修正 Cpus_allowed [清單 （_l)] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="5e18f-112">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="5e18f-113">支援從非領導者執行緒 [GH 3800] exec</span><span class="sxs-lookup"><span data-stu-id="5e18f-113">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="5e18f-114">設定更新失敗視為非嚴重 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="5e18f-114">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="5e18f-115">更新 binfmt 可正確處理位移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="5e18f-115">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="5e18f-116">計劃 9 [GH 3854] 啟用對應網路磁碟機</span><span class="sxs-lookup"><span data-stu-id="5e18f-116">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="5e18f-117">支援 Windows]-> [Linux 和 Linux]-> [繫結掛接的 Windows 路徑轉譯</span><span class="sxs-lookup"><span data-stu-id="5e18f-117">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="5e18f-118">建立唯讀的區段，對應上開啟的檔案唯讀</span><span class="sxs-lookup"><span data-stu-id="5e18f-118">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="5e18f-119">建置 18334</span><span class="sxs-lookup"><span data-stu-id="5e18f-119">Build 18334</span></span>
<span data-ttu-id="5e18f-120">一般 Windows 組建 18334 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-120">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-121">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-121">WSL</span></span>
* <span data-ttu-id="5e18f-122">重新設計 Windows 時區會對應至 Linux 時間的時區 [GH 3747] 的方式</span><span class="sxs-lookup"><span data-stu-id="5e18f-122">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="5e18f-123">修正記憶體流失並新增新的字串翻譯函式 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="5e18f-123">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="5e18f-124">在任何執行緒的 threadgroup SIGCONT 是無作業 [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="5e18f-124">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="5e18f-125">正確地顯示 /proc/self/fd 中的 通訊端與 epoll 檔案描述項</span><span class="sxs-lookup"><span data-stu-id="5e18f-125">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="5e18f-126">建置 18305</span><span class="sxs-lookup"><span data-stu-id="5e18f-126">Build 18305</span></span>
<span data-ttu-id="5e18f-127">一般 Windows 組建 18305 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-127">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-128">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-128">WSL</span></span>
* <span data-ttu-id="5e18f-129">pthreads 主執行緒結束 [GH 3589] 時，遺失檔案的存取權</span><span class="sxs-lookup"><span data-stu-id="5e18f-129">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="5e18f-130">TIOCSCTTY 應該略過 「 強制 」 參數，除非必要，否則 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="5e18f-130">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="5e18f-131">wsl.exe 命令列改進功能和新增匯入/匯出功能。</span><span class="sxs-lookup"><span data-stu-id="5e18f-131">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="5e18f-132">建置 18277</span><span class="sxs-lookup"><span data-stu-id="5e18f-132">Build 18277</span></span>
<span data-ttu-id="5e18f-133">一般 Windows 組建 18277 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-133">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-134">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-134">WSL</span></span>
* <span data-ttu-id="5e18f-135">修正組建 18272 [GH 3645] 中所引進的 「 沒有這類介面支援 」 錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-135">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="5e18f-136">忽略 umount syscall [GH 3605] MNT_FORCE 旗標</span><span class="sxs-lookup"><span data-stu-id="5e18f-136">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="5e18f-137">切換以使用官方 CreatePseudoConsole API WSL interop</span><span class="sxs-lookup"><span data-stu-id="5e18f-137">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="5e18f-138">FUTEX_WAIT 重新啟動時，維護任何逾時值</span><span class="sxs-lookup"><span data-stu-id="5e18f-138">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="5e18f-139">建置 18272</span><span class="sxs-lookup"><span data-stu-id="5e18f-139">Build 18272</span></span>
<span data-ttu-id="5e18f-140">一般 Windows 組建 18272 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-140">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-141">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-141">WSL</span></span>
* <span data-ttu-id="5e18f-142">**警告：** 讓 WSL 無法運作的這個組建中沒有問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-142">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="5e18f-143">嘗試啟動您的散發套件時，您會看到 「 沒有這類介面支援 」 錯誤。</span><span class="sxs-lookup"><span data-stu-id="5e18f-143">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="5e18f-144">此問題已修正，而且會在下一週的測試人員快速建置。</span><span class="sxs-lookup"><span data-stu-id="5e18f-144">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="5e18f-145">如果您已安裝此組建，您可以回復至先前的 Windows 組建使用 [執行回舊版的 Windows 10] 在 [設定]-> [更新與安全性]-> 復原。</span><span class="sxs-lookup"><span data-stu-id="5e18f-145">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="5e18f-146">建置 18267</span><span class="sxs-lookup"><span data-stu-id="5e18f-146">Build 18267</span></span>
<span data-ttu-id="5e18f-147">一般 Windows 組建 18267 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-147">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-148">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-148">WSL</span></span>
* <span data-ttu-id="5e18f-149">修正的問題廢止程序可能會不 reaped 而無限期保留。</span><span class="sxs-lookup"><span data-stu-id="5e18f-149">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="5e18f-150">如果錯誤訊息超過最大長度 [GH 3592] WslRegisterDistribution 停止回應</span><span class="sxs-lookup"><span data-stu-id="5e18f-150">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="5e18f-151">允許 fsync DrvFs [GH 3556] 上的唯讀檔案順利完成</span><span class="sxs-lookup"><span data-stu-id="5e18f-151">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="5e18f-152">請確定 [/bin] 和 [/sbin 目錄存在，才能建立 [GH 3584] 內的符號連結</span><span class="sxs-lookup"><span data-stu-id="5e18f-152">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="5e18f-153">新增 WSL 執行個體的執行個體終止逾時機制。</span><span class="sxs-lookup"><span data-stu-id="5e18f-153">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="5e18f-154">逾時是目前設定為 15 秒，這表示執行個體將會終止在最後一個 WSL 程序結束之後的 15 秒。</span><span class="sxs-lookup"><span data-stu-id="5e18f-154">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="5e18f-155">若要立即終止發佈，請使用：</span><span class="sxs-lookup"><span data-stu-id="5e18f-155">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="5e18f-156">建置 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="5e18f-156">Build 17763 (1809)</span></span>
<span data-ttu-id="5e18f-157">一般 Windows 組建 17763 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-157">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-158">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-158">WSL</span></span>
* <span data-ttu-id="5e18f-159">Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="5e18f-159">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="5e18f-160">確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="5e18f-160">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="5e18f-161">處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結</span><span class="sxs-lookup"><span data-stu-id="5e18f-161">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="5e18f-162">更妥善地處理的 threadgroup 領導者檔案描述元清除。</span><span class="sxs-lookup"><span data-stu-id="5e18f-162">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="5e18f-163">切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-163">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="5e18f-164">Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="5e18f-164">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="5e18f-165">修正數個 AF_UNIX 相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="5e18f-165">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="5e18f-166">修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop</span><span class="sxs-lookup"><span data-stu-id="5e18f-166">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="5e18f-167">避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲</span><span class="sxs-lookup"><span data-stu-id="5e18f-167">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="5e18f-168">新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="5e18f-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="5e18f-169">更精確的 IPV6 範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-169">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="5e18f-170">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="5e18f-170">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="5e18f-171">使用管線傳送不小心清除 edge 觸發 epoll 事件 [GH 3276] 的檔案系統</span><span class="sxs-lookup"><span data-stu-id="5e18f-171">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e18f-172">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e18f-172">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="5e18f-173">改善的殭屍支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="5e18f-173">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="5e18f-174">加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目</span><span class="sxs-lookup"><span data-stu-id="5e18f-174">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="5e18f-175">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="5e18f-175">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="5e18f-176">新增支援 TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="5e18f-176">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="5e18f-177">連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="5e18f-177">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="5e18f-178">支援在掛接的 Vhd [GH 3246，3291] 上的 interop</span><span class="sxs-lookup"><span data-stu-id="5e18f-178">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="5e18f-179">修正權限檢查在根資料夾 [GH 3304] 上的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-179">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="5e18f-180">TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-180">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="5e18f-181">Windows UI 應用程式應該執行，即使是在背景中啟動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-181">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="5e18f-182">新增 wsl-u 或--使用者選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="5e18f-182">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="5e18f-183">啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="5e18f-183">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="5e18f-184">Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="5e18f-184">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="5e18f-185">非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="5e18f-185">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="5e18f-186">案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="5e18f-186">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="5e18f-187">請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-187">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="5e18f-188">新增 wslconfig/終止停止執行的散發套件。</span><span class="sxs-lookup"><span data-stu-id="5e18f-188">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="5e18f-189">修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。</span><span class="sxs-lookup"><span data-stu-id="5e18f-189">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="5e18f-190">每個目錄區分大小寫做為擴充屬性公開 （expose)</span><span class="sxs-lookup"><span data-stu-id="5e18f-190">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="5e18f-191">ARM64:模擬快取的維護作業。</span><span class="sxs-lookup"><span data-stu-id="5e18f-191">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="5e18f-192">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-192">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="5e18f-193">DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。</span><span class="sxs-lookup"><span data-stu-id="5e18f-193">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="5e18f-194">修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-194">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="5e18f-195">WSL 絕對計時器與過去的時間不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="5e18f-195">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="5e18f-196">確定新建立的重新分析點將因此列出父目錄中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-196">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="5e18f-197">以不可分割方式在 DrvFs 區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="5e18f-197">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="5e18f-198">已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="5e18f-198">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e18f-199">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e18f-199">[GH 2712]</span></span>
* <span data-ttu-id="5e18f-200">固定的 WSL UMCI 啟用時，啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="5e18f-200">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="5e18f-201">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="5e18f-201">[GH 3020]</span></span>
* <span data-ttu-id="5e18f-202">新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-202">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="5e18f-203">若要使用，請按住 shift 鍵，以滑鼠右鍵按一下 [在檔案總管] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-203">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="5e18f-204">修正 Unix 通訊端非封鎖行為 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="5e18f-204">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="5e18f-205">當掉 NETLINK 命令，GH 2026 中所報告的修正程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-205">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="5e18f-206">新增支援掛接傳用旗標 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-206">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="5e18f-207">截斷而造成不 inotify 事件 [GH 2978] 修正問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-207">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="5e18f-208">新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-208">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="5e18f-209">新增--wsl.exe 來選取特定的散發版本的散發選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-209">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="5e18f-210">Dmesg 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-210">Limited support for dmesg.</span></span> <span data-ttu-id="5e18f-211">應用程式現在可以 dmesg 來記錄。</span><span class="sxs-lookup"><span data-stu-id="5e18f-211">Applications can now log to dmesg.</span></span> <span data-ttu-id="5e18f-212">WSL 驅動程式會記錄到 dmesg 的有限的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-212">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="5e18f-213">在將來，這可以延伸到包含其他資訊/診斷的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-213">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="5e18f-214">注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-214">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="5e18f-215">尚未支援 syscall 介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-215">syscall interface is not yet supported.</span></span> <span data-ttu-id="5e18f-216">以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。</span><span class="sxs-lookup"><span data-stu-id="5e18f-216">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="5e18f-217">變更預設 gid 和模式比對原生 [GH 3042] 序列裝置</span><span class="sxs-lookup"><span data-stu-id="5e18f-217">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="5e18f-218">DrvFs 現在支援擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e18f-218">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="5e18f-219">注意：DrvFs 的擴充屬性名稱有一些限制。</span><span class="sxs-lookup"><span data-stu-id="5e18f-219">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="5e18f-220">某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="5e18f-220">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="5e18f-221">建置 18252 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-221">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-222">一般 Windows 組建 18252 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-222">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-223">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-223">WSL</span></span>
* <span data-ttu-id="5e18f-224">移動 init 和 bsdtar 二進位檔出 lxssmanager dll 並進入不同的工具資料夾</span><span class="sxs-lookup"><span data-stu-id="5e18f-224">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="5e18f-225">修正競爭周圍使用 CLONE_FILES 時關閉檔案描述元</span><span class="sxs-lookup"><span data-stu-id="5e18f-225">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="5e18f-226">翻譯 DrvFs 路徑時，處理 /proc/pid/mountinfo 中的選擇性欄位</span><span class="sxs-lookup"><span data-stu-id="5e18f-226">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="5e18f-227">允許 DrvFs mknod 不用 S_IFREG 的中繼資料支援成功</span><span class="sxs-lookup"><span data-stu-id="5e18f-227">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="5e18f-228">DrvFs 上建立的唯讀檔案應該有設定 [GH 3411] 中的 readonly 屬性</span><span class="sxs-lookup"><span data-stu-id="5e18f-228">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="5e18f-229">新增處理 DrvFs 掛接 /sbin/mount.drvfs 協助程式</span><span class="sxs-lookup"><span data-stu-id="5e18f-229">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="5e18f-230">用於 DrvFs POSIX 重新命名。</span><span class="sxs-lookup"><span data-stu-id="5e18f-230">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="5e18f-231">允許在不含磁碟區 GUID 的磁碟區上的路徑轉譯。</span><span class="sxs-lookup"><span data-stu-id="5e18f-231">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="5e18f-232">建置 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="5e18f-232">Build 17738 (Fast)</span></span>
<span data-ttu-id="5e18f-233">一般 Windows 組建 17738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-233">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-234">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-234">WSL</span></span>
* <span data-ttu-id="5e18f-235">Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="5e18f-235">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="5e18f-236">確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="5e18f-236">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="5e18f-237">處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結</span><span class="sxs-lookup"><span data-stu-id="5e18f-237">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="5e18f-238">更妥善地處理的 threadgroup 領導者檔案描述元清除。</span><span class="sxs-lookup"><span data-stu-id="5e18f-238">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="5e18f-239">建置 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="5e18f-239">Build 17728 (Fast)</span></span>
<span data-ttu-id="5e18f-240">一般 Windows 組建 17728 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-240">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-241">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-241">WSL</span></span>
* <span data-ttu-id="5e18f-242">切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-242">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="5e18f-243">Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="5e18f-243">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="5e18f-244">修正幾個 AF_UNIX 的相關問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="5e18f-244">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="5e18f-245">修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop</span><span class="sxs-lookup"><span data-stu-id="5e18f-245">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="5e18f-246">建置 18204 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-246">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-247">一般 Windows 組建 18204 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-247">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-248">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-248">WSL</span></span>
* <span data-ttu-id="5e18f-249">使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="5e18f-249">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e18f-250">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e18f-250">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="5e18f-251">建置 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="5e18f-251">Build 17723 (Fast)</span></span>
<span data-ttu-id="5e18f-252">一般 Windows 組建 17723 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-252">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-253">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-253">WSL</span></span>
* <span data-ttu-id="5e18f-254">避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲</span><span class="sxs-lookup"><span data-stu-id="5e18f-254">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="5e18f-255">新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="5e18f-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="5e18f-256">更精確的 IPV6 範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-256">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="5e18f-257">PR_SET_PTRACER 支援 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="5e18f-257">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="5e18f-258">使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="5e18f-258">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e18f-259">Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e18f-259">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="5e18f-260">建置 17713</span><span class="sxs-lookup"><span data-stu-id="5e18f-260">Build 17713</span></span>
<span data-ttu-id="5e18f-261">一般 Windows 組建 17713 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-261">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-262">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-262">WSL</span></span>
* <span data-ttu-id="5e18f-263">改善的殭屍支援 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="5e18f-263">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="5e18f-264">加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目</span><span class="sxs-lookup"><span data-stu-id="5e18f-264">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="5e18f-265">修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="5e18f-265">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="5e18f-266">新增支援 TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="5e18f-266">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="5e18f-267">連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="5e18f-267">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="5e18f-268">支援在掛接的 Vhd [GH 3246，3291] 上的 interop</span><span class="sxs-lookup"><span data-stu-id="5e18f-268">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="5e18f-269">修正權限檢查在根資料夾 [GH 3304] 上的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-269">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="5e18f-270">TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-270">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="5e18f-271">Windows UI 應用程式應該執行，即使是在背景中啟動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-271">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="5e18f-272">建置 17704</span><span class="sxs-lookup"><span data-stu-id="5e18f-272">Build 17704</span></span>
<span data-ttu-id="5e18f-273">一般 Windows 組建 17704 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-273">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-274">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-274">WSL</span></span>
* <span data-ttu-id="5e18f-275">新增 wsl-u 或--使用者選項 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="5e18f-275">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="5e18f-276">啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="5e18f-276">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="5e18f-277">Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="5e18f-277">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="5e18f-278">非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="5e18f-278">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="5e18f-279">案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="5e18f-279">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="5e18f-280">請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-280">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="5e18f-281">新增 wslconfig/終止停止執行的散發套件。</span><span class="sxs-lookup"><span data-stu-id="5e18f-281">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="5e18f-282">建置 17692</span><span class="sxs-lookup"><span data-stu-id="5e18f-282">Build 17692</span></span>
<span data-ttu-id="5e18f-283">一般 Windows 組建 17692 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-283">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-284">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-284">WSL</span></span>
* <span data-ttu-id="5e18f-285">修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。</span><span class="sxs-lookup"><span data-stu-id="5e18f-285">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="5e18f-286">每個目錄區分大小寫做為擴充屬性公開 （expose)</span><span class="sxs-lookup"><span data-stu-id="5e18f-286">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="5e18f-287">ARM64:模擬快取的維護作業。</span><span class="sxs-lookup"><span data-stu-id="5e18f-287">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="5e18f-288">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-288">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="5e18f-289">DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。</span><span class="sxs-lookup"><span data-stu-id="5e18f-289">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="5e18f-290">建置 17686</span><span class="sxs-lookup"><span data-stu-id="5e18f-290">Build 17686</span></span>
<span data-ttu-id="5e18f-291">一般 Windows 組建 17686 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-291">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-292">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-292">WSL</span></span>
* <span data-ttu-id="5e18f-293">修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-293">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="5e18f-294">WSL 絕對計時器與過去的時間不會引發 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="5e18f-294">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="5e18f-295">確定新建立的重新分析點將因此列出父目錄中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-295">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="5e18f-296">以不可分割方式在 DrvFs 區分大小寫的目錄。</span><span class="sxs-lookup"><span data-stu-id="5e18f-296">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="5e18f-297">建置 17677</span><span class="sxs-lookup"><span data-stu-id="5e18f-297">Build 17677</span></span>
<span data-ttu-id="5e18f-298">一般 Windows 組建 17677 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-298">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-299">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-299">WSL</span></span>
* <span data-ttu-id="5e18f-300">已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="5e18f-300">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e18f-301">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e18f-301">[GH 2712]</span></span>
* <span data-ttu-id="5e18f-302">固定的 WSL UMCI 啟用時，啟動失敗。</span><span class="sxs-lookup"><span data-stu-id="5e18f-302">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="5e18f-303">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="5e18f-303">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="5e18f-304">建置 17666</span><span class="sxs-lookup"><span data-stu-id="5e18f-304">Build 17666</span></span>
<span data-ttu-id="5e18f-305">一般 Windows 組建 17666 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-305">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-306">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-306">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="5e18f-307">警告：還有一些 AMD 晶片 [GH 3134] 上執行時，防止 WSL 問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-307">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="5e18f-308">修正程式是準備好讓測試人員組建分支及其方式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-308">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="5e18f-309">新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-309">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="5e18f-310">若要使用按住 shift 鍵並以滑鼠右鍵按一下在檔案總管 視窗中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-310">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="5e18f-311">修正 unix 通訊端非封鎖行為 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="5e18f-311">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="5e18f-312">當掉 NETLINK 命令，GH 2026 中所報告的修正程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-312">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="5e18f-313">新增支援掛接傳用旗標 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-313">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="5e18f-314">截斷而造成不 inotify 事件 [GH 2978] 修正問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-314">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="5e18f-315">新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-315">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="5e18f-316">新增--wsl.exe 來選取特定的散發版本的散發選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-316">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="5e18f-317">建置 17655 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-317">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-318">一般 Windows 組建 17655 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-318">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-319">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-319">WSL</span></span>
* <span data-ttu-id="5e18f-320">Dmesg 的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-320">Limited support for dmesg.</span></span> <span data-ttu-id="5e18f-321">應用程式現在可以 dmesg 來記錄。</span><span class="sxs-lookup"><span data-stu-id="5e18f-321">Applications can now log to dmesg.</span></span> <span data-ttu-id="5e18f-322">WSL 驅動程式會記錄到 dmesg 的有限的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-322">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="5e18f-323">在將來，這可以延伸到包含其他資訊/診斷的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-323">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="5e18f-324">注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-324">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="5e18f-325">尚未支援 sycall 介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-325">sycall interface is not yet supported.</span></span> <span data-ttu-id="5e18f-326">以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。</span><span class="sxs-lookup"><span data-stu-id="5e18f-326">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="5e18f-327">已修正的問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="5e18f-327">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e18f-328">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e18f-328">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="5e18f-329">建置 17639 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-329">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-330">一般 Windows 組建 17639 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-330">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-331">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-331">WSL</span></span>
* <span data-ttu-id="5e18f-332">變更預設 gid 和模式比對原生 [GH 3042] 序列裝置</span><span class="sxs-lookup"><span data-stu-id="5e18f-332">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="5e18f-333">DrvFs 現在支援擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e18f-333">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="5e18f-334">注意：DrvFs 的擴充屬性名稱有一些限制。</span><span class="sxs-lookup"><span data-stu-id="5e18f-334">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="5e18f-335">特別是，某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="5e18f-335">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="5e18f-336">建置 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="5e18f-336">Build 17133 (Fast)</span></span>
<span data-ttu-id="5e18f-337">一般 Windows 組建 17133 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-337">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-338">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-338">WSL</span></span>
* <span data-ttu-id="5e18f-339">修正在 WSL 的停止回應。</span><span class="sxs-lookup"><span data-stu-id="5e18f-339">Fix for hang in WSL.</span></span> <span data-ttu-id="5e18f-340">[GH 3039，3034]</span><span class="sxs-lookup"><span data-stu-id="5e18f-340">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="5e18f-341">建置 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="5e18f-341">Build 17128 (Fast)</span></span>
<span data-ttu-id="5e18f-342">一般 Windows 組建 17128 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-342">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-343">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-343">WSL</span></span>
* <span data-ttu-id="5e18f-344">None</span><span class="sxs-lookup"><span data-stu-id="5e18f-344">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="5e18f-345">建置 17627 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-345">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-346">一般 Windows 組建 17627 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-346">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-347">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-347">WSL</span></span>
* <span data-ttu-id="5e18f-348">新增支援 futex 感知 pi 的作業。</span><span class="sxs-lookup"><span data-stu-id="5e18f-348">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="5e18f-349">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="5e18f-349">[GH 1006]</span></span>
    * <span data-ttu-id="5e18f-350">請注意，優先順序而不是目前支援的 WSL 功能因此有一些限制，但標準使用量應該要解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="5e18f-350">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="5e18f-351">WSL 程序的 Windows 防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-351">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="5e18f-352">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="5e18f-352">[GH 1852]</span></span>
    * <span data-ttu-id="5e18f-353">比方說，若要允許 WSL python 則會接聽任何通訊埠，請使用提高權限的 Windows cmd 處理：</span><span class="sxs-lookup"><span data-stu-id="5e18f-353">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd:</span></span>
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * <span data-ttu-id="5e18f-354">如需有關如何新增防火牆規則的詳細資訊，請參閱[連結](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="5e18f-354">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="5e18f-355">使用 wsl.exe 時，請採用使用者的預設殼層。</span><span class="sxs-lookup"><span data-stu-id="5e18f-355">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="5e18f-356">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="5e18f-356">[GH 2372]</span></span>
* <span data-ttu-id="5e18f-357">報告為乙太網路的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-357">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="5e18f-358">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="5e18f-358">[GH 2996]</span></span>
* <span data-ttu-id="5e18f-359">更妥善地處理的損毀 /etc/passwd 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-359">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="5e18f-360">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="5e18f-360">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-361">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-361">Console</span></span>
* <span data-ttu-id="5e18f-362">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-362">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-363">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-363">LTP Results:</span></span>
<span data-ttu-id="5e18f-364">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-364">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="5e18f-365">建置 17618 （直接略過）</span><span class="sxs-lookup"><span data-stu-id="5e18f-365">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="5e18f-366">一般 Windows 組建 17618 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-366">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-367">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-367">WSL</span></span>
* <span data-ttu-id="5e18f-368">引入 NT interop pseudoconsole 功能 [GH 988，1366，1433年、 1542年、 2370年、 2406年]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-368">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="5e18f-369">舊版安裝機制 (lxrun.exe) 已被取代。</span><span class="sxs-lookup"><span data-stu-id="5e18f-369">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="5e18f-370">安裝散發套件支援的機制是透過 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="5e18f-370">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-371">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-371">Console</span></span>
* <span data-ttu-id="5e18f-372">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-372">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-373">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-373">LTP Results:</span></span>
<span data-ttu-id="5e18f-374">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-374">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="5e18f-375">建置 17110</span><span class="sxs-lookup"><span data-stu-id="5e18f-375">Build 17110</span></span>
<span data-ttu-id="5e18f-376">一般 Windows 組建 17110 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-376">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-377">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-377">WSL</span></span>
* <span data-ttu-id="5e18f-378">允許從 Windows [GH 2928] 終止 /init。</span><span class="sxs-lookup"><span data-stu-id="5e18f-378">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="5e18f-379">DrvFs 現在預設會使用每個目錄是否區分大小寫 (相當於"案例 = dir 」 掛接選項)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-379">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="5e18f-380">使用 「 案例 = force"（舊的行為） 需要設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5e18f-380">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="5e18f-381">執行下列命令，以啟用 「 案例 = 強制 「 如果您需要使用它： reg 新增 HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="5e18f-381">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="5e18f-382">如果您有現有的目錄建立 WSL 與 Windows 所需區分大小寫的舊版本中，會使用 fsutil.exe 來將它們標示為區分大小寫： fsutil.exe 檔案 setcasesensitiveinfo<path>啟用</span><span class="sxs-lookup"><span data-stu-id="5e18f-382">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="5e18f-383">以 NULL 結尾的 uname syscall 從傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="5e18f-383">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-384">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-384">Console</span></span>
* <span data-ttu-id="5e18f-385">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-385">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-386">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-386">LTP Results:</span></span>
<span data-ttu-id="5e18f-387">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-387">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="5e18f-388">建置 17107</span><span class="sxs-lookup"><span data-stu-id="5e18f-388">Build 17107</span></span>
<span data-ttu-id="5e18f-389">一般 Windows 組建 17107 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-389">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-390">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-390">WSL</span></span>
* <span data-ttu-id="5e18f-391">支援 TCSETSF 和 TCSETSW 主要 pty 端點 [GH 2552] 上。</span><span class="sxs-lookup"><span data-stu-id="5e18f-391">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="5e18f-392">啟動同時 interop 的程序，可能會導致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-392">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="5e18f-393">修正 PTRACE_ATTACH 在 /proc/pid/status 中顯示適當的追蹤狀態。</span><span class="sxs-lookup"><span data-stu-id="5e18f-393">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="5e18f-394">修正競爭短期處理序使用 CLEARTID 和 SETTID 旗標已複製的儲存無法結束而不清除 TID 位址。</span><span class="sxs-lookup"><span data-stu-id="5e18f-394">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="5e18f-395">移動從 pre 17093 組建時升級 Linux 檔案系統目錄時，顯示一則訊息。</span><span class="sxs-lookup"><span data-stu-id="5e18f-395">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="5e18f-396">如需 17093 檔案系統變更的詳細資訊，請參閱版本資訊[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-396">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-397">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-397">Console</span></span>
* <span data-ttu-id="5e18f-398">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-398">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-399">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-399">LTP Results:</span></span>
<span data-ttu-id="5e18f-400">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-400">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="5e18f-401">建置 17101</span><span class="sxs-lookup"><span data-stu-id="5e18f-401">Build 17101</span></span>
<span data-ttu-id="5e18f-402">一般 Windows 組建 17101 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-402">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-403">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-403">WSL</span></span>
* <span data-ttu-id="5e18f-404">Signalfd 支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-404">Support for signalfd.</span></span> <span data-ttu-id="5e18f-405">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="5e18f-405">[GH 129]</span></span>
* <span data-ttu-id="5e18f-406">支援的檔案名稱包含不合法的 NTFS 字元加以編碼為私用的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="5e18f-406">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="5e18f-407">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="5e18f-407">[GH 1514]</span></span>
* <span data-ttu-id="5e18f-408">不支援寫入時，自動掛接會將恢復為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5e18f-408">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="5e18f-409">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="5e18f-409">[GH 2603]</span></span>
* <span data-ttu-id="5e18f-410">允許貼上的 Unicode surrogate 字組 （例如 emoji 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-410">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="5e18f-411">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="5e18f-411">[GH 2765]</span></span>
* <span data-ttu-id="5e18f-412">/Proc 和 /sys 中的虛擬檔案應該會傳回讀取和寫入已準備好從 select、 投票、 epoll，要是 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="5e18f-412">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="5e18f-413">修正問題，可能會導致服務登錄已遭竄改，或已損毀時進入無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="5e18f-413">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="5e18f-414">修正使用較新版本 (4.14 上游) iproute2 netlink 訊息。</span><span class="sxs-lookup"><span data-stu-id="5e18f-414">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-415">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-415">Console</span></span>
* <span data-ttu-id="5e18f-416">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-416">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-417">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-417">LTP Results:</span></span>
<span data-ttu-id="5e18f-418">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-418">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="5e18f-419">建置 17093</span><span class="sxs-lookup"><span data-stu-id="5e18f-419">Build 17093</span></span>
<span data-ttu-id="5e18f-420">一般 Windows 組建 17093 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-420">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="5e18f-421">重要事項：</span><span class="sxs-lookup"><span data-stu-id="5e18f-421">Important:</span></span>
<span data-ttu-id="5e18f-422">當從 WSL 開始第一次升級至此組建之後，它必須執行一些工作升級 Linux 檔案系統目錄。</span><span class="sxs-lookup"><span data-stu-id="5e18f-422">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="5e18f-423">這可能需要幾分鐘的時間，因此 WSL 似乎較慢啟動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-423">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="5e18f-424">這只應該發生之後的每個散發中，您已安裝從存放區。</span><span class="sxs-lookup"><span data-stu-id="5e18f-424">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="5e18f-425">已改善 DrvFs 中的區分大小寫支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-425">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="5e18f-426">DrvFs 現在支援每個目錄區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-426">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="5e18f-427">這是新旗標，可以設定目錄，以指出在這些目錄中的所有作業應都視為區分大小寫，如此即使 Windows 應用程式正確地開啟只有大小寫不同的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-427">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="5e18f-428">DrvFs 具備新的掛接選項，控制每個目錄為基礎的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="5e18f-428">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="5e18f-429">案例 = 強制： 所有目錄都區分大小寫 （除了磁碟機根目錄中）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-429">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="5e18f-430">WSL 以建立新的目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-430">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="5e18f-431">這是除了標示新的目錄的區分大小寫的舊行為。</span><span class="sxs-lookup"><span data-stu-id="5e18f-431">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="5e18f-432">案例 = dir： 只有透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-432">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="5e18f-433">WSL 以建立新的目錄會標示為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-433">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="5e18f-434">案例 = 關閉： 只透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-434">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="5e18f-435">WSL 以建立新的目錄會標示為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-435">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="5e18f-436">注意： 在舊版中建立的 WSL 目錄沒有設定，因此將不被視為區分大小寫如果您使用這個旗標 」 案例 = dir"選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-436">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="5e18f-437">即將推出的方式，若要在現有的目錄上設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="5e18f-437">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="5e18f-438">裝載這些選項的範例 （現有的磁碟機，您必須先卸載之前，您可以掛上使用不同的選項）： sudo mount-t drvfs c: / /mnt/c o 案例 = dir</span><span class="sxs-lookup"><span data-stu-id="5e18f-438">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="5e18f-439">現在，寫 = 強制仍是預設選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-439">For now, case=force is still the default option.</span></span> <span data-ttu-id="5e18f-440">這將會變更為案例未來 = dir。</span><span class="sxs-lookup"><span data-stu-id="5e18f-440">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="5e18f-441">您現在可以使用正斜線 Windows 路徑中時，裝載 DrvFs，例如： sudo 掛接-t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="5e18f-441">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="5e18f-442">現在，WSL 會在執行個體啟動 [GH 2636] 處理 /etc/fstab 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-442">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="5e18f-443">這是之前自動掛接 DrvFs 磁碟機;任何已經 fstab 已掛接的磁碟機將不會自動重新掛接，可讓您變更特定磁碟機的掛接點。</span><span class="sxs-lookup"><span data-stu-id="5e18f-443">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="5e18f-444">此行為可以關閉使用 wsl.conf。</span><span class="sxs-lookup"><span data-stu-id="5e18f-444">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="5e18f-445">掛接、 mountinfo 和 mountstats 檔案中 /proc 正確逸出特殊字元，例如反斜線和空格 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="5e18f-445">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="5e18f-446">可以複製和移動從 Windows 建立 DrvFs WSL 符號連結，或 fifos 等通訊端啟用中繼資料時，特殊的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-446">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="5e18f-447">WSL 會與 wsl.conf 更易設定</span><span class="sxs-lookup"><span data-stu-id="5e18f-447">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="5e18f-448">我們已新增為您自動設定會套用每次您啟動子系統的 WSL 中的 特定功能的方法。</span><span class="sxs-lookup"><span data-stu-id="5e18f-448">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="5e18f-449">這包括自動掛接選項和網路設定。</span><span class="sxs-lookup"><span data-stu-id="5e18f-449">This includes automount options and network configuration.</span></span> <span data-ttu-id="5e18f-450">深入了解在我們的部落格文章，網址： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="5e18f-450">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="5e18f-451">AF_UNIX 可讓 Linux 處理序在 WSL 與 Windows 原生程序之間的通訊端連線</span><span class="sxs-lookup"><span data-stu-id="5e18f-451">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="5e18f-452">WSL 與 Windows 應用程式現在可以透過 Unix 通訊端通訊彼此。</span><span class="sxs-lookup"><span data-stu-id="5e18f-452">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="5e18f-453">假設您想要在 Windows 中執行的服務，並使其可供 Windows 和 WSL 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-453">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="5e18f-454">現在，這可能與 Unix 通訊端。</span><span class="sxs-lookup"><span data-stu-id="5e18f-454">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="5e18f-455">如需我們的部落格文章，讀取 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="5e18f-455">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-456">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-456">WSL</span></span>
* <span data-ttu-id="5e18f-457">支援使用 MAP_NORESERVE [GH 121，2784年] mmap()</span><span class="sxs-lookup"><span data-stu-id="5e18f-457">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="5e18f-458">支援 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121，2781年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-458">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="5e18f-459">處理非 SIGCHLD 終止訊號中複製 [GH 121，2781年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-459">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="5e18f-460">虛設常式 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="5e18f-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="5e18f-461">載入 ELF 二進位碼檔案包含具有非零位移 [GH 1884] 的負載標頭時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-461">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="5e18f-462">會全面清除載入影像時後, 置頁面位元組。</span><span class="sxs-lookup"><span data-stu-id="5e18f-462">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="5e18f-463">減少 execve 以無訊息方式結束處理序的情況下</span><span class="sxs-lookup"><span data-stu-id="5e18f-463">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-464">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-464">Console</span></span>
* <span data-ttu-id="5e18f-465">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-465">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-466">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-466">LTP Results:</span></span>
<span data-ttu-id="5e18f-467">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-467">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="5e18f-468">建置 17083</span><span class="sxs-lookup"><span data-stu-id="5e18f-468">Build 17083</span></span>
<span data-ttu-id="5e18f-469">一般 Windows 組建 17083 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-469">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-470">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-470">WSL</span></span>
* <span data-ttu-id="5e18f-471">固定的 epoll [GH 2798，2801，2857年] 相關的錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="5e18f-471">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="5e18f-472">固定的停止回應時關閉 ASLR [GH 1185，2870年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-472">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="5e18f-473">請確定 mmap 作業出現不可部分完成 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="5e18f-473">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-474">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-474">Console</span></span>
* <span data-ttu-id="5e18f-475">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-475">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-476">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-476">LTP Results:</span></span>
<span data-ttu-id="5e18f-477">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-477">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="5e18f-478">建置 17074</span><span class="sxs-lookup"><span data-stu-id="5e18f-478">Build 17074</span></span>
<span data-ttu-id="5e18f-479">一般 Windows 組建 17074 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-479">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-480">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-480">WSL</span></span>
* <span data-ttu-id="5e18f-481">DrvFs 中繼資料 [GH 2777] 固定的儲存體格式</span><span class="sxs-lookup"><span data-stu-id="5e18f-481">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="5e18f-482">**重要事項：** 這個組建不正確，或完全不會出現之前建立的 DrvFs 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-482">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="5e18f-483">若要修正受影響的檔案，請使用 chmod 和 chown 來重新套用中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-483">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="5e18f-484">與多個訊號可重新啟動 syscall 修正的問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-484">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-485">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-485">Console</span></span>
* <span data-ttu-id="5e18f-486">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-487">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-487">LTP Results:</span></span>
<span data-ttu-id="5e18f-488">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-488">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="5e18f-489">建置 17063</span><span class="sxs-lookup"><span data-stu-id="5e18f-489">Build 17063</span></span>
<span data-ttu-id="5e18f-490">一般 Windows 組建 17063 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-490">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e18f-491">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-491">WSL</span></span>
* <span data-ttu-id="5e18f-492">DrvFs 支援 Linux 的其他中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-492">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="5e18f-493">這可讓設定擁有者和使用 chmod/chown，以及建立特殊的檔案，例如 fifos、 unix 通訊端和裝置檔案的檔案模式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-493">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="5e18f-494">這預設會停用目前因為它是仍屬實驗性質。</span><span class="sxs-lookup"><span data-stu-id="5e18f-494">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="5e18f-495">**注意：** 我們修正了在 DrvFs 所使用的中繼資料格式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-495">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="5e18f-496">而中繼資料則適用於此組建進行實驗，未來的組建將不會正確地讀取此組建所建立的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-496">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="5e18f-497">您可能需要手動更新已修改檔案的擁有者，就必須重新建立自訂裝置識別碼的裝置。</span><span class="sxs-lookup"><span data-stu-id="5e18f-497">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="5e18f-498">若要啟用，請使用 [中繼資料] 選項掛接 DrvFs （現有的裝載上啟用此功能，您必須先取消掛接）：</span><span class="sxs-lookup"><span data-stu-id="5e18f-498">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="5e18f-499">Linux 的權限會新增為額外的中繼資料檔案，它們不會影響 Windows 權限。</span><span class="sxs-lookup"><span data-stu-id="5e18f-499">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="5e18f-500">請記住，編輯檔案，使用 Windows 編輯器可能會移除的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-500">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="5e18f-501">在此情況下，檔案將還原為其預設權限。</span><span class="sxs-lookup"><span data-stu-id="5e18f-501">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="5e18f-502">已新增的掛接選項 DrvFs 以不含中繼資料的控制檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-502">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="5e18f-503">uid： 使用的所有檔案擁有者的使用者 ID。</span><span class="sxs-lookup"><span data-stu-id="5e18f-503">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="5e18f-504">gid： 使用的所有檔案擁有者的群組 ID。</span><span class="sxs-lookup"><span data-stu-id="5e18f-504">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="5e18f-505">umask： 排除所有的檔案和目錄的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="5e18f-505">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="5e18f-506">fmask： 排除所有的一般檔案的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="5e18f-506">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="5e18f-507">dmask： 排除所有目錄的權限的八進位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="5e18f-507">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="5e18f-508">例如: </span><span class="sxs-lookup"><span data-stu-id="5e18f-508">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="5e18f-509">結合指定不含中繼資料檔案的預設權限的 [中繼資料] 選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-509">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="5e18f-510">導入新的環境變數， `WSLENV`，來設定環境變數 WSL 和 Win32 之間流動的方式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-510">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="5e18f-511">例如: </span><span class="sxs-lookup"><span data-stu-id="5e18f-511">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` <span data-ttu-id="5e18f-512">是以冒號分隔的清單時啟動 WSL 程序，從 Win32 或從 WSL 的 Win32 處理序可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="5e18f-512">is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="5e18f-513">每個變數都可以加斜線，後面接著旗標，以指定在轉譯的方式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-513">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="5e18f-514">p:值為應轉譯 WSL 路徑與 Win32 路徑之間的路徑。</span><span class="sxs-lookup"><span data-stu-id="5e18f-514">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="5e18f-515">L:值是路徑的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-515">l: The value is a list of paths.</span></span> <span data-ttu-id="5e18f-516">在 WSL，它是以冒號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-516">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="5e18f-517">在 Win32 中，它是以分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-517">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="5e18f-518">U:值只能包含時叫用從 Win32 WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-518">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="5e18f-519">寫入：值只能包含時叫用 Win32 從 WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-519">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="5e18f-520">您可以設定`WSLENV`.bashrc 或自訂的 Windows 環境，為您的使用者。</span><span class="sxs-lookup"><span data-stu-id="5e18f-520">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="5e18f-521">drvfs 掛接正確保留時間戳記的 tar 檔案解壓縮，cp-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="5e18f-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="5e18f-522">drvfs 符號連結報告正確的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="5e18f-522">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="5e18f-523">讀取/寫入適用於非常大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="5e18f-523">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="5e18f-524">waitpid 搭配處理序群組識別碼 (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="5e18f-524">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="5e18f-525">大型的保留區域，大幅改善的 mmap 效能改善 ghc 效能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="5e18f-525">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="5e18f-526">READ_IMPLIES_EXEC; 的人格支援修正行程最長和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="5e18f-526">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="5e18f-527">mprotect 支援 PROT_GROWSDOWN;修正 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="5e18f-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="5e18f-528">頁面中的錯誤修正程式過量使用模式;修正 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="5e18f-528">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="5e18f-529">複製支援多個旗標的組合</span><span class="sxs-lookup"><span data-stu-id="5e18f-529">clone supports more flags combinations</span></span>
* <span data-ttu-id="5e18f-530">支援選取/epoll 的 epoll 檔案 （之前執行任何作業）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-530">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="5e18f-531">通知未實作 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="5e18f-531">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="5e18f-532">忽略都未運作時產生 resolv.conf nameservers [GH 2694] 的介面</span><span class="sxs-lookup"><span data-stu-id="5e18f-532">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="5e18f-533">列舉沒有實體位址的網路介面。</span><span class="sxs-lookup"><span data-stu-id="5e18f-533">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="5e18f-534">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="5e18f-534">[GH 2685]</span></span>
* <span data-ttu-id="5e18f-535">其他錯誤修正和改進功能。</span><span class="sxs-lookup"><span data-stu-id="5e18f-535">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="5e18f-536">在 Windows 上的開發人員可使用的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="5e18f-536">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="5e18f-537">Windows 命令列工具鏈包含 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="5e18f-537">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="5e18f-538">讀取[這篇部落格](https://aka.ms/tarcurlwindows)深入了解這兩個新工具加入，並查看如何它們塑造在 Windows 上的開發人員體驗。</span><span class="sxs-lookup"><span data-stu-id="5e18f-538">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   `AF_UNIX` <span data-ttu-id="5e18f-539">提供 Windows Insider SDK 中 （17061 +）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-539">is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="5e18f-540">讀取[這篇部落格](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)若要深入了解`AF_UNIX`以及如何在 Windows 上的開發人員可以使用它。</span><span class="sxs-lookup"><span data-stu-id="5e18f-540">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="5e18f-541">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-541">Console</span></span>
* <span data-ttu-id="5e18f-542">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-542">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-543">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-543">LTP Results:</span></span>
<span data-ttu-id="5e18f-544">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-544">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="5e18f-545">建置 17046</span><span class="sxs-lookup"><span data-stu-id="5e18f-545">Build 17046</span></span>

<span data-ttu-id="5e18f-546">一般 Windows 組建 17046 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-546">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="5e18f-547">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-547">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-548">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-548">WSL</span></span>
- <span data-ttu-id="5e18f-549">允許在沒有使用中的終端機的情況下執行的處理序。</span><span class="sxs-lookup"><span data-stu-id="5e18f-549">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="5e18f-550">[GH 709、 1007、 1511年、 2252年 2391，et al。]</span><span class="sxs-lookup"><span data-stu-id="5e18f-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="5e18f-551">CLONE_VFORK 和 CLONE_VM 更佳的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-551">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="5e18f-552">[GH 1878，2615年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-552">[GH 1878, 2615]</span></span>
- <span data-ttu-id="5e18f-553">略過網路作業的 WSL TDI 篩選器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-553">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="5e18f-554">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="5e18f-554">[GH 1554]</span></span>
- <span data-ttu-id="5e18f-555">DrvFs 會在符合特定條件時，建立 NT 符號連結。</span><span class="sxs-lookup"><span data-stu-id="5e18f-555">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="5e18f-556">[GH 353，1475，2602年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-556">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="5e18f-557">連結目標必須是相對的不能跨越任何掛接點或符號連結，而且必須存在。</span><span class="sxs-lookup"><span data-stu-id="5e18f-557">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="5e18f-558">使用者必須擁有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE （這通常需要您啟動 wsl.exe 提升權限），除非開發人員模式下開啟。</span><span class="sxs-lookup"><span data-stu-id="5e18f-558">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="5e18f-559">在其他情況下，DrvFs 仍會建立 WSL 符號連結。</span><span class="sxs-lookup"><span data-stu-id="5e18f-559">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="5e18f-560">允許同時執行提高權限和非提高權限的 WSL 執行個體。</span><span class="sxs-lookup"><span data-stu-id="5e18f-560">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="5e18f-561">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="5e18f-561">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="5e18f-562">新增 wslpath 執行 WSL <>-Windows 路徑的轉換。</span><span class="sxs-lookup"><span data-stu-id="5e18f-562">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="5e18f-563">[GH 522，1243，1834年、 2327，et al。]</span><span class="sxs-lookup"><span data-stu-id="5e18f-563">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="5e18f-564">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-564">Console</span></span>
- <span data-ttu-id="5e18f-565">不再出現問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-565">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-566">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-566">LTP Results:</span></span>
<span data-ttu-id="5e18f-567">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-567">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="5e18f-568">建置 17040</span><span class="sxs-lookup"><span data-stu-id="5e18f-568">Build 17040</span></span>

<span data-ttu-id="5e18f-569">一般 Windows 組建 17040 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-569">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-570">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-570">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-571">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-571">WSL</span></span>
- <span data-ttu-id="5e18f-572">因為 17035 任何修正。</span><span class="sxs-lookup"><span data-stu-id="5e18f-572">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-573">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-573">Console</span></span>
- <span data-ttu-id="5e18f-574">因為 17035 任何修正。</span><span class="sxs-lookup"><span data-stu-id="5e18f-574">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-575">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-575">LTP Results:</span></span>
<span data-ttu-id="5e18f-576">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-576">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="5e18f-577">建置 17035</span><span class="sxs-lookup"><span data-stu-id="5e18f-577">Build 17035</span></span>

<span data-ttu-id="5e18f-578">一般 Windows 組建 17035 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-578">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-579">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-579">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-580">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-580">WSL</span></span>
- <span data-ttu-id="5e18f-581">偶爾會失敗，但是 EINVAL 存取 DrvFs 上的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-581">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="5e18f-582">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="5e18f-582">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-583">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-583">Console</span></span>
- <span data-ttu-id="5e18f-584">色彩遺失部分插入/刪除 VT 模式中的行時。</span><span class="sxs-lookup"><span data-stu-id="5e18f-584">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-585">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-585">LTP Results:</span></span>
<span data-ttu-id="5e18f-586">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-586">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="5e18f-587">組建 17025</span><span class="sxs-lookup"><span data-stu-id="5e18f-587">Build 17025</span></span>

<span data-ttu-id="5e18f-588">一般 Windows 組建 17025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-588">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-589">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-589">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-590">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-590">WSL</span></span>
- <span data-ttu-id="5e18f-591">在新的前景處理程序群組 [GH 1653，2510年] 開始初始程序。</span><span class="sxs-lookup"><span data-stu-id="5e18f-591">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="5e18f-592">SIGHUP 傳遞修正 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-592">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="5e18f-593">若無提供 [GH 2497]，則產生預設虛擬橋接器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e18f-593">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="5e18f-594">實作 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="5e18f-595">修正了更 interop 的 stdout/stderr 管道。</span><span class="sxs-lookup"><span data-stu-id="5e18f-595">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="5e18f-596">虛設常式 syncfs 系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-596">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-597">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-597">Console</span></span>
- <span data-ttu-id="5e18f-598">修正輸入的 VT 翻譯的協力廠商主控台 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="5e18f-598">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-599">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-599">LTP Results:</span></span>
<span data-ttu-id="5e18f-600">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-600">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="5e18f-601">建置 17017</span><span class="sxs-lookup"><span data-stu-id="5e18f-601">Build 17017</span></span>

<span data-ttu-id="5e18f-602">一般 Windows 組建 17017 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-602">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-603">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-603">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-604">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-604">WSL</span></span>
- <span data-ttu-id="5e18f-605">忽略空白 ELF 程式標頭 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-605">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="5e18f-606">允許建立非互動式使用者的 WSL 執行個體的 LxssManager (ssh 和排程的工作支援) [GH 777 1602年]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-606">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="5e18f-607">支援 WSL]-> [Win32]-> [WSL （「 開始 」） 案例 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-607">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="5e18f-608">終止透過 interop [GH 1614] 叫用的主控台應用程式的有限的支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-608">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="5e18f-609">支援掛接 devpts [GH 1948] 選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-609">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="5e18f-610">Ptrace 封鎖子啟動 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-610">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="5e18f-611">EPOLLET 遺漏某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-611">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="5e18f-612">傳回 PTRACE_GETSIGINFO 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5e18f-612">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="5e18f-613">使用 lseek Getdents 提供不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="5e18f-613">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="5e18f-614">修正一些 Win32 interop 應用程式停止回應，有沒有更多的資料管道上等候輸入。</span><span class="sxs-lookup"><span data-stu-id="5e18f-614">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="5e18f-615">O_ASYNC 支援 tty/pty 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-615">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="5e18f-616">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-616">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-617">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-617">Console</span></span>
- <span data-ttu-id="5e18f-618">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-618">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-619">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-619">LTP Results:</span></span>
<span data-ttu-id="5e18f-620">在進行測試。</span><span class="sxs-lookup"><span data-stu-id="5e18f-620">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="5e18f-621">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="5e18f-621">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="5e18f-622">建置 16288</span><span class="sxs-lookup"><span data-stu-id="5e18f-622">Build 16288</span></span>

<span data-ttu-id="5e18f-623">一般 Windows 組建 16288 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-623">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-624">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-624">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-625">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-625">WSL</span></span>
- <span data-ttu-id="5e18f-626">正確初始化，並報告 uid、 gid 和通訊端檔案描述元 [GH 2490] 模式</span><span class="sxs-lookup"><span data-stu-id="5e18f-626">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="5e18f-627">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-628">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-628">Console</span></span>
- <span data-ttu-id="5e18f-629">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-630">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-630">LTP Results:</span></span>
<span data-ttu-id="5e18f-631">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-631">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="5e18f-632">建置 16278</span><span class="sxs-lookup"><span data-stu-id="5e18f-632">Build 16278</span></span>

<span data-ttu-id="5e18f-633">一般 Windows 組建 162738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-633">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-634">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-634">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-635">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-635">WSL</span></span>
- <span data-ttu-id="5e18f-636">卸除 LX MM 狀態 [GH 2415] 時，明確地取消對應支援的檔案區段的對應的檢視</span><span class="sxs-lookup"><span data-stu-id="5e18f-636">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="5e18f-637">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-637">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-638">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-638">Console</span></span>
- <span data-ttu-id="5e18f-639">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-639">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-640">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-640">LTP Results:</span></span>
<span data-ttu-id="5e18f-641">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-641">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="5e18f-642">建置 16275</span><span class="sxs-lookup"><span data-stu-id="5e18f-642">Build 16275</span></span>

<span data-ttu-id="5e18f-643">一般 Windows 組建 162735 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-643">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-644">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-645">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-645">WSL</span></span>
- <span data-ttu-id="5e18f-646">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-646">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-647">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-647">Console</span></span>
- <span data-ttu-id="5e18f-648">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-648">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-649">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-649">LTP Results:</span></span>
<span data-ttu-id="5e18f-650">16273 後並無變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-650">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="5e18f-651">建置 16273</span><span class="sxs-lookup"><span data-stu-id="5e18f-651">Build 16273</span></span>

<span data-ttu-id="5e18f-652">一般 Windows 組建 16273 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-652">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-653">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-654">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-654">WSL</span></span>
- <span data-ttu-id="5e18f-655">已修正的問題 DrvFs 有時報告目錄 [GH 2392] 錯誤的檔案類型</span><span class="sxs-lookup"><span data-stu-id="5e18f-655">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="5e18f-656">允許建立 NETLINK_KOBJECT_UEVENT 通訊端，若要解除封鎖程式，使用 uevent [GH 1121，2293，2242年、 2295年 2235，648、 637]</span><span class="sxs-lookup"><span data-stu-id="5e18f-656">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="5e18f-657">新增支援非封鎖連線 [GH 903，1391，1584年、 1585年、 1829年、 2290年、 2314年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-657">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="5e18f-658">實作 CLONE_FS 複製系統呼叫旗標 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="5e18f-658">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="5e18f-659">修正問題不會處理索引標籤或 NT interop [GH 1625，2164年] 中正確的引號</span><span class="sxs-lookup"><span data-stu-id="5e18f-659">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="5e18f-660">解決錯誤時嘗試重新啟動 WSL 執行個體 [GH 651、 2095年] 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="5e18f-660">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="5e18f-661">實作 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 作業 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="5e18f-661">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="5e18f-662">修正各種 SysFs 檔案 [GH 2214] 的權限</span><span class="sxs-lookup"><span data-stu-id="5e18f-662">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="5e18f-663">在安裝 [GH 2290] 期間修正 Haskell 堆疊停止回應</span><span class="sxs-lookup"><span data-stu-id="5e18f-663">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="5e18f-664">實作 binfmt_misc 'C' 'o' 和 'P' 旗標 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="5e18f-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="5e18f-665">加入 /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="5e18f-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="5e18f-666">新增部分支援 ioprio_set 系統呼叫 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="5e18f-666">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="5e18f-667">虛設常式 SO_REUSEPORT & 新增支援 SO_PASSCRED netlink 通訊端 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="5e18f-667">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="5e18f-668">從 RegisterDistribuiton 傳回不同的錯誤碼，如果目前正在發佈安裝或解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5e18f-668">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="5e18f-669">允許部分安裝 WSL 散發 wslconfig.exe 透過取消的註冊</span><span class="sxs-lookup"><span data-stu-id="5e18f-669">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="5e18f-670">修正從 udp::msg_peek python 通訊端測試停止回應</span><span class="sxs-lookup"><span data-stu-id="5e18f-670">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="5e18f-671">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-671">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-672">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-672">Console</span></span>
- <span data-ttu-id="5e18f-673">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-673">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-674">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-674">LTP Results:</span></span>
<span data-ttu-id="5e18f-675">測試總計：1904</span><span class="sxs-lookup"><span data-stu-id="5e18f-675">Total Tests: 1904</span></span><br/>
<span data-ttu-id="5e18f-676">總略過測試：209</span><span class="sxs-lookup"><span data-stu-id="5e18f-676">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="5e18f-677">失敗總數：229</span><span class="sxs-lookup"><span data-stu-id="5e18f-677">Total Failures: 229</span></span><br/>
[<span data-ttu-id="5e18f-678">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-678">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="5e18f-679">建置 16257</span><span class="sxs-lookup"><span data-stu-id="5e18f-679">Build 16257</span></span>

<span data-ttu-id="5e18f-680">一般 Windows 組建 16257 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-680">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-681">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-681">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-682">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-682">WSL</span></span>
- <span data-ttu-id="5e18f-683">實作 prlimit64 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="5e18f-683">Implement prlimit64 system call</span></span>
- <span data-ttu-id="5e18f-684">新增支援 ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="5e18f-684">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="5e18f-685">虛設常式 MSG_MORE 針對 TCP 通訊端 [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="5e18f-685">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="5e18f-686">修正無效的 AT_EXECFN 輔助向量行為 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="5e18f-686">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="5e18f-687">修正主控台/tty，複製/貼上的行為並新增更好的完整緩衝處理 [GH 2204，2131年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-687">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="5e18f-688">設定使用者識別碼和設定群組識別碼程式 [GH 2031] 的輔助向量中設定 AT_SECURE</span><span class="sxs-lookup"><span data-stu-id="5e18f-688">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="5e18f-689">虛擬終端機主要端點不會處理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="5e18f-689">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="5e18f-690">修正 lseek 會更新，以倒轉 LxFs [GH 2310] 中的目錄</span><span class="sxs-lookup"><span data-stu-id="5e18f-690">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="5e18f-691">/dev/ptmx 鎖之後的繁重使用量 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="5e18f-691">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="5e18f-692">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-692">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-693">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-693">Console</span></span>
- <span data-ttu-id="5e18f-694">針對水平列/底線 Everywhere [GH 2168] 修正程式</span><span class="sxs-lookup"><span data-stu-id="5e18f-694">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="5e18f-695">修正程序順序變更並關閉 [GH 2170] 的工作變得更難的 NPM</span><span class="sxs-lookup"><span data-stu-id="5e18f-695">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="5e18f-696">加入我們新的色彩配置： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="5e18f-696">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-697">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-697">LTP Results:</span></span>
<span data-ttu-id="5e18f-698">16251 後並無變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-698">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-699">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-699">Syscall Support</span></span>
<span data-ttu-id="5e18f-700">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-700">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-701">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-701">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="5e18f-702">已知問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-702">Known Issues</span></span>
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="5e18f-703">GitHub 問題 2392年:無法辨識的 WSL Windows 資料夾...</span><span class="sxs-lookup"><span data-stu-id="5e18f-703">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="5e18f-704">在組建中 16257，WSL 有問題時列舉 Windows 檔案/資料夾透過`/mnt/c/...`。</span><span class="sxs-lookup"><span data-stu-id="5e18f-704">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="5e18f-705">已修正此問題，因此應該在發行測試人員組建開始時間 2017 年 8 月 14 日一週內。</span><span class="sxs-lookup"><span data-stu-id="5e18f-705">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="5e18f-706">建置 16251</span><span class="sxs-lookup"><span data-stu-id="5e18f-706">Build 16251</span></span>

<span data-ttu-id="5e18f-707">一般 Windows 組建 16251 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-707">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-708">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-709">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-709">WSL</span></span>
- <span data-ttu-id="5e18f-710">Beta 標記移除 WSL 選用元件，請參閱 <<c0> [ 部落格文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-710">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="5e18f-711">正確初始化儲存組 uid 與 gid exec [GH 962，1415，2072年] 上設定使用者識別碼和設定群組識別碼的二進位檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-711">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="5e18f-712">已新增的支援 ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="5e18f-712">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="5e18f-713">已新增支援 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET NT_FPREGSET [GH 555] 與</span><span class="sxs-lookup"><span data-stu-id="5e18f-713">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="5e18f-714">已修正 ptrace 若要停止忽略訊號</span><span class="sxs-lookup"><span data-stu-id="5e18f-714">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="5e18f-715">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-715">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-716">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-716">Console</span></span>
- <span data-ttu-id="5e18f-717">沒有主控台的相關變更，在此版本中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-718">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-718">LTP Results:</span></span>
<span data-ttu-id="5e18f-719">成功的測試數目：768</span><span class="sxs-lookup"><span data-stu-id="5e18f-719">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="5e18f-720">失敗的測試數目：244</span><span class="sxs-lookup"><span data-stu-id="5e18f-720">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="5e18f-721">已略過的測試數目：96</span><span class="sxs-lookup"><span data-stu-id="5e18f-721">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="5e18f-722">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-722">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="5e18f-723">建置 16241</span><span class="sxs-lookup"><span data-stu-id="5e18f-723">Build 16241</span></span>

<span data-ttu-id="5e18f-724">一般 Windows 組建 16241 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-724">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-725">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-725">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e18f-726">WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-726">WSL</span></span>
- <span data-ttu-id="5e18f-727">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-727">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="5e18f-728">Console</span><span class="sxs-lookup"><span data-stu-id="5e18f-728">Console</span></span>
- <span data-ttu-id="5e18f-729">修正錯誤的字元輸出的交叉線年 12 月原本報告[這裡](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="5e18f-729">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="5e18f-730">不修正在字碼頁 65001 (utf-8) 中顯示任何輸出文字</span><span class="sxs-lookup"><span data-stu-id="5e18f-730">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="5e18f-731">不會傳送至選取範圍變更調色盤的其他部分的一種色彩的 RGB 值所做的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-731">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="5e18f-732">這會讓主控台內容工作表頁更容易使用。</span><span class="sxs-lookup"><span data-stu-id="5e18f-732">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="5e18f-733">Ctrl + S 似乎未正確運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-733">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="5e18f-734">非粗體 /-維度沒有完全從 ANSI 逸出程式碼 [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="5e18f-734">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="5e18f-735">主控台不會正確支援 Vim 色彩佈景主題 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="5e18f-735">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="5e18f-736">無法貼上的特定字元 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="5e18f-736">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="5e18f-737">自動重排調整互動奇怪調整 bash 視窗的大小，在 [編輯] / [命令列 [GH ConEmu 1123] 上的東西時</span><span class="sxs-lookup"><span data-stu-id="5e18f-737">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="5e18f-738">Ctrl-L 離開畫面已變更 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="5e18f-738">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="5e18f-739">HDPI [GH 1907] 上顯示 VT 時，主控台轉譯 bug</span><span class="sxs-lookup"><span data-stu-id="5e18f-739">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="5e18f-740">Japansese 字元很陌生與 Unicode 字元 U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="5e18f-740">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="5e18f-741">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-741">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="5e18f-742">組建 16237</span><span class="sxs-lookup"><span data-stu-id="5e18f-742">Build 16237</span></span>

<span data-ttu-id="5e18f-743">一般 Windows 組建 16237 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-743">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-744">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-744">Fixed</span></span>
- <span data-ttu-id="5e18f-745">使用預設屬性，而不需要 EAs lxfs （根目錄、 根目錄，0000） 中的檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-745">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="5e18f-746">已新增的支援使用擴充的屬性的散發套件</span><span class="sxs-lookup"><span data-stu-id="5e18f-746">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="5e18f-747">修正填補 getdents 和 getdents64 所傳回的項目</span><span class="sxs-lookup"><span data-stu-id="5e18f-747">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="5e18f-748">修正 shmctl SHM_STAT 系統呼叫 [GH 2068] 的權限檢查</span><span class="sxs-lookup"><span data-stu-id="5e18f-748">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="5e18f-749">已修正不正確的初始 epoll tty [GH 2231] 狀態</span><span class="sxs-lookup"><span data-stu-id="5e18f-749">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="5e18f-750">修正 DrvFs readdir 不會傳回所有項目 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="5e18f-750">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="5e18f-751">修正 LxFs readdir 檔案時已取消連結 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="5e18f-751">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="5e18f-752">允許透過 procfs 重新開啟的檔案未連結的 drvfs</span><span class="sxs-lookup"><span data-stu-id="5e18f-752">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="5e18f-753">新增全域登錄金鑰覆寫停用 WSL 功能 (interop / 磁碟機掛接)</span><span class="sxs-lookup"><span data-stu-id="5e18f-753">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="5e18f-754">修正 「 狀態 」 中的不正確的區塊計數 DrvFs （以及 LxFs） [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="5e18f-754">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="5e18f-755">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-755">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="5e18f-756">建置 16232</span><span class="sxs-lookup"><span data-stu-id="5e18f-756">Build 16232</span></span>

<span data-ttu-id="5e18f-757">一般 Windows 組建 16232 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-757">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-758">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-758">Fixed</span></span>
- <span data-ttu-id="5e18f-759">沒有 WSL 相關的此版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-759">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="5e18f-760">建置 16226</span><span class="sxs-lookup"><span data-stu-id="5e18f-760">Build 16226</span></span>

<span data-ttu-id="5e18f-761">一般 Windows 組建 16226 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-761">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-762">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-762">Fixed</span></span>
- <span data-ttu-id="5e18f-763">xattr 相關 syscall 支援 （getxattr、 setxattr、 listxattr、 removexattr）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-763">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="5e18f-764">security.capablity xattr 支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-764">security.capablity xattr support.</span></span>
- <span data-ttu-id="5e18f-765">改進的相容性與特定的檔案系統篩選器，包括非 MS SMB 伺服器。</span><span class="sxs-lookup"><span data-stu-id="5e18f-765">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="5e18f-766">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="5e18f-766">[GH #1952]</span></span>
- <span data-ttu-id="5e18f-767">改善對 OneDrive 預留位置、 GVFS 預留位置和精簡的 OS 支援壓縮的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-767">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="5e18f-768">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-768">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="5e18f-769">建置 16215</span><span class="sxs-lookup"><span data-stu-id="5e18f-769">Build 16215</span></span>

<span data-ttu-id="5e18f-770">一般 Windows 組建 16215 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-770">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-771">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-771">Fixed</span></span>
- <span data-ttu-id="5e18f-772">WSL 不再需要開發人員模式。</span><span class="sxs-lookup"><span data-stu-id="5e18f-772">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="5e18f-773">支援 drvfs 目錄連接。</span><span class="sxs-lookup"><span data-stu-id="5e18f-773">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="5e18f-774">處理的 WSL 發佈 appx 套件解除安裝。</span><span class="sxs-lookup"><span data-stu-id="5e18f-774">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="5e18f-775">更新 procfs 顯示私用和共用對應。</span><span class="sxs-lookup"><span data-stu-id="5e18f-775">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="5e18f-776">新增 wslconfig.exe 清除部分安裝或解除安裝的散發套件的能力。</span><span class="sxs-lookup"><span data-stu-id="5e18f-776">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="5e18f-777">已新增的支援 IP_MTU_DISCOVER 針對 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="5e18f-777">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="5e18f-778">[GH 1639，2115，2205年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-778">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="5e18f-779">推斷 AF_INADDR 路由通訊協定家族。</span><span class="sxs-lookup"><span data-stu-id="5e18f-779">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="5e18f-780">序列裝置的功能改進 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="5e18f-780">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="5e18f-781">建置 16199</span><span class="sxs-lookup"><span data-stu-id="5e18f-781">Build 16199</span></span>

<span data-ttu-id="5e18f-782">一般 Windows 組建 16199 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-782">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-783">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-783">Fixed</span></span>
- <span data-ttu-id="5e18f-784">沒有 WSL 相關的這些版本中的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-784">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="5e18f-785">建置 16193</span><span class="sxs-lookup"><span data-stu-id="5e18f-785">Build 16193</span></span>

<span data-ttu-id="5e18f-786">一般 Windows 組建 16193 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-786">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-787">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-787">Fixed</span></span>
- <span data-ttu-id="5e18f-788">傳送 SIGCONT 以及終止 [GH 1973] threadgroup 之間的競爭情形</span><span class="sxs-lookup"><span data-stu-id="5e18f-788">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="5e18f-789">將報表而不是 [GH 1840] FILE_DEVICE_CONSOLE FILE_DEVICE_NAMED_PIPE tty 和 pty 裝置</span><span class="sxs-lookup"><span data-stu-id="5e18f-789">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="5e18f-790">SSH IP_OPTIONS 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-790">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="5e18f-791">移動 DrvFs 掛接至 init 精靈 [GH 1862，1968 年，1767年、 1933年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-791">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="5e18f-792">已新增的支援在 DrvFs 遵循 NT 符號連結。</span><span class="sxs-lookup"><span data-stu-id="5e18f-792">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="5e18f-793">建置 16184</span><span class="sxs-lookup"><span data-stu-id="5e18f-793">Build 16184</span></span>

<span data-ttu-id="5e18f-794">一般 Windows 組建 16184 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-794">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-795">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-795">Fixed</span></span>
- <span data-ttu-id="5e18f-796">已移除的 apt 套件維護工作 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="5e18f-796">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="5e18f-797">已修正未出現在從 node.js [GH 1840] 中的 Windows 處理序的輸出</span><span class="sxs-lookup"><span data-stu-id="5e18f-797">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="5e18f-798">放寬 lxcore [GH 1794] 中的對齊需求</span><span class="sxs-lookup"><span data-stu-id="5e18f-798">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="5e18f-799">已修正的數系統呼叫的 AT_EMPTY_PATH 旗標的處理。</span><span class="sxs-lookup"><span data-stu-id="5e18f-799">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="5e18f-800">已修正的問題，其中刪除 DrvFs 檔案含有開啟控制代碼，會導致檔案出現未定義的行為 [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="5e18f-800">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="5e18f-801">eg /etc/ 主機現在將會從 Windows hosts 檔案 (%windir%\system32\drivers\etc\hosts) 繼承項目 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="5e18f-801">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="5e18f-802">建置 16179</span><span class="sxs-lookup"><span data-stu-id="5e18f-802">Build 16179</span></span>

<span data-ttu-id="5e18f-803">一般 Windows 組建 16179 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-803">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-804">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-804">Fixed</span></span>
- <span data-ttu-id="5e18f-805">沒有 WSL 變更本週。</span><span class="sxs-lookup"><span data-stu-id="5e18f-805">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="5e18f-806">建置 16176</span><span class="sxs-lookup"><span data-stu-id="5e18f-806">Build 16176</span></span>

<span data-ttu-id="5e18f-807">一般 Windows 組建 16176 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-807">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-808">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-808">Fixed</span></span>

- [<span data-ttu-id="5e18f-809">已啟用序列的支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-809">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="5e18f-810">已新增的 IP 通訊端選項 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="5e18f-810">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="5e18f-811">（在檔案上傳至 nginx/PHP-FPM） 實作 pwritev 函式 [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="5e18f-811">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="5e18f-812">新增 IP 通訊端選項 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="5e18f-812">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="5e18f-813">支援的通訊端選項 IP_MULTICAST_LOOP IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="5e18f-813">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="5e18f-814">已新增適用於應用程式節點、 追蹤路由、 dig、 nslookup、 主機 IP (V6) _MTU 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="5e18f-814">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="5e18f-815">已新增的 IP 通訊端選項 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="5e18f-815">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="5e18f-816">檔案系統的增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-816">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="5e18f-817">允許的 UNC 路徑的掛接</span><span class="sxs-lookup"><span data-stu-id="5e18f-817">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="5e18f-818">啟用在 drvfs CDFS 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-818">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="5e18f-819">正確處理 drvfs 中的網路檔案系統權限</span><span class="sxs-lookup"><span data-stu-id="5e18f-819">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="5e18f-820">支援遠端磁碟機新增至 drvfs</span><span class="sxs-lookup"><span data-stu-id="5e18f-820">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="5e18f-821">啟用 FAT drvfs 中支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-821">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="5e18f-822">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-822">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-823">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="5e18f-823">LTP Results</span></span>
<span data-ttu-id="5e18f-824">自 15042 後的任何變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-824">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="5e18f-825">建置 16170</span><span class="sxs-lookup"><span data-stu-id="5e18f-825">Build 16170</span></span>

<span data-ttu-id="5e18f-826">一般 Windows 組建 16170 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-826">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="5e18f-827">我們發行了新[部落格文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)討論我們努力測試 WSL。</span><span class="sxs-lookup"><span data-stu-id="5e18f-827">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e18f-828">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-828">Fixed</span></span>

- <span data-ttu-id="5e18f-829">支援通訊端選項 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="5e18f-829">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="5e18f-830">新增對 PTRACE_OLDSETOPTIONS 支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-830">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="5e18f-831">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="5e18f-831">[GH 1692]</span></span>
- <span data-ttu-id="5e18f-832">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-832">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-833">LTP 結果</span><span class="sxs-lookup"><span data-stu-id="5e18f-833">LTP Results</span></span>
<span data-ttu-id="5e18f-834">自 15042 後的任何變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-834">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="5e18f-835">建置 15046 到 Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="5e18f-835">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="5e18f-836">沒有更多的 WSL 修正或加入至 Windows 10 Creators Update 中的功能。</span><span class="sxs-lookup"><span data-stu-id="5e18f-836">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="5e18f-837">在未來幾週的目標設為下一個主要的 Windows 更新的新增項目中，將會繼續 WSL 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="5e18f-837">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="5e18f-838">針對一般的 Windows 上建置 15046 和未來的測試人員的資訊發行版本，請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-838">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="5e18f-839">建置 15042</span><span class="sxs-lookup"><span data-stu-id="5e18f-839">Build 15042</span></span>

<span data-ttu-id="5e18f-840">一般 Windows 組建 15042 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-840">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-841">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-841">Fixed</span></span>

- <span data-ttu-id="5e18f-842">移除路徑，在結束時，產生死結的修正"."</span><span class="sxs-lookup"><span data-stu-id="5e18f-842">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="5e18f-843">已修正的問題其中 FIONBIO 未成功 [GH 1683] 傳回 0</span><span class="sxs-lookup"><span data-stu-id="5e18f-843">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="5e18f-844">已修正的問題 inet 資料包通訊端讀取長度為零</span><span class="sxs-lookup"><span data-stu-id="5e18f-844">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="5e18f-845">修正 [drvfs inode 查閱 [GH 1675] 中的 [可能的死結，因為競爭條件</span><span class="sxs-lookup"><span data-stu-id="5e18f-845">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="5e18f-846">擴充支援 unix 通訊端的輔助資料;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514，613、 1326年]</span><span class="sxs-lookup"><span data-stu-id="5e18f-846">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="5e18f-847">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-847">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-848">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-848">LTP Results:</span></span>
<span data-ttu-id="5e18f-849">通過測試數目：737</span><span class="sxs-lookup"><span data-stu-id="5e18f-849">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="5e18f-850">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="5e18f-850">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="5e18f-851">建置 15031</span><span class="sxs-lookup"><span data-stu-id="5e18f-851">Build 15031</span></span>

<span data-ttu-id="5e18f-852">一般 Windows 組建 15031 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-852">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-853">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-853">Fixed</span></span>

- <span data-ttu-id="5e18f-854">修正了其中 time(2) 會偶發性行為異常。</span><span class="sxs-lookup"><span data-stu-id="5e18f-854">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="5e18f-855">已修正，並發出 where \* SIGPROCMASK syscall 可能會損毀訊號遮罩。</span><span class="sxs-lookup"><span data-stu-id="5e18f-855">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="5e18f-856">現在會傳回完整的命令列長度在 WSL 程序建立通知。</span><span class="sxs-lookup"><span data-stu-id="5e18f-856">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="5e18f-857">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="5e18f-857">[GH 1632]</span></span>
- <span data-ttu-id="5e18f-858">WSL 現在會報告執行緒結束時，透過 ptrace 的 GDB 停止回應。</span><span class="sxs-lookup"><span data-stu-id="5e18f-858">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="5e18f-859">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="5e18f-859">[GH 1196]</span></span>
- <span data-ttu-id="5e18f-860">已修正的 bug，其中 ptys 會停止回應之後大量 tmux IO。</span><span class="sxs-lookup"><span data-stu-id="5e18f-860">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="5e18f-861">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="5e18f-861">[GH 1358]</span></span>
- <span data-ttu-id="5e18f-862">許多系統呼叫 （futex、 semtimedop、 ppoll、 sigtimedwait、 itimer、 timer_create） 中的固定的逾時驗證</span><span class="sxs-lookup"><span data-stu-id="5e18f-862">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="5e18f-863">已新增的 eventfd EFD_SEMAPHORE 支援 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="5e18f-863">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="5e18f-864">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-864">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-865">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-865">LTP Results:</span></span>
<span data-ttu-id="5e18f-866">通過測試數目：737</span><span class="sxs-lookup"><span data-stu-id="5e18f-866">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="5e18f-867">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="5e18f-867">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e18f-868">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-868">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="5e18f-869">建置 15025</span><span class="sxs-lookup"><span data-stu-id="5e18f-869">Build 15025</span></span>

<span data-ttu-id="5e18f-870">一般 Windows 組建 15025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-870">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-871">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-871">Fixed</span></span>

- <span data-ttu-id="5e18f-872">修正 bug，沒壞的 grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="5e18f-872">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="5e18f-873">實作的 eventfd2 syscall [GH 452] EFD_SEMAPHORE 旗標</span><span class="sxs-lookup"><span data-stu-id="5e18f-873">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="5e18f-874">實作 /proc/ [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="5e18f-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="5e18f-875">訊號驅動 IO 支援 unix 資料流通訊端 [GH 393，68]</span><span class="sxs-lookup"><span data-stu-id="5e18f-875">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="5e18f-876">支援 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="5e18f-876">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="5e18f-877">實作 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="5e18f-877">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="5e18f-878">已修正的 bug epoll_wait() 不正在等候 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="5e18f-878">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="5e18f-879">實作 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="5e18f-879">Implement /proc/version_signature</span></span>
- <span data-ttu-id="5e18f-880">Tee syscall 現在會傳回失敗，如果這兩個檔案描述元參考到相同的管道</span><span class="sxs-lookup"><span data-stu-id="5e18f-880">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="5e18f-881">實作正確的行為 SO_PEERCRED Unix 通訊端</span><span class="sxs-lookup"><span data-stu-id="5e18f-881">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="5e18f-882">固定的 tkill syscall 無效參數處理方法</span><span class="sxs-lookup"><span data-stu-id="5e18f-882">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="5e18f-883">若要增加的 drvfs preformace 的變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-883">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="5e18f-884">Ruby IO 封鎖的次要修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-884">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="5e18f-885">固定的 recvmsg() 傳回 EINVAL MSG_DONTWAIT 旗標的 inet 通訊端 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="5e18f-885">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="5e18f-886">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-886">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-887">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-887">LTP Results:</span></span>
<span data-ttu-id="5e18f-888">通過測試數目：732</span><span class="sxs-lookup"><span data-stu-id="5e18f-888">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="5e18f-889">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="5e18f-889">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e18f-890">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-890">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="5e18f-891">Build 15019</span><span class="sxs-lookup"><span data-stu-id="5e18f-891">Build 15019</span></span>

<span data-ttu-id="5e18f-892">一般 Windows build 15019 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-892">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-893">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-893">Fixed</span></span>

- <span data-ttu-id="5e18f-894">已修正的 bug，正確地報告中的 CPU 使用量 procfs htop (GH 823 945、 971) 等工具</span><span class="sxs-lookup"><span data-stu-id="5e18f-894">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="5e18f-895">當呼叫 open （） 與 O_TRUNC 上的現有檔案 inotify 現在會產生之前 IN_OPEN IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5e18f-895">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="5e18f-896">Unix 通訊端 getsockopt SO_ERROR 啟用 postgress [GH 61，1354年] 修正程式</span><span class="sxs-lookup"><span data-stu-id="5e18f-896">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="5e18f-897">實作 /proc/sys/net/core/somaxconn GO 語言</span><span class="sxs-lookup"><span data-stu-id="5e18f-897">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="5e18f-898">Apt get 封裝更新背景工作現在會隱藏執行檢視</span><span class="sxs-lookup"><span data-stu-id="5e18f-898">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="5e18f-899">清除範圍 ipv6 localhost （Spring-Framework(Java) 失敗）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-899">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="5e18f-900">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-900">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-901">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-901">LTP Results:</span></span>
<span data-ttu-id="5e18f-902">通過測試數目：714</span><span class="sxs-lookup"><span data-stu-id="5e18f-902">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="5e18f-903">非通過的數字 (失敗，所以已略過等等。...):249</span><span class="sxs-lookup"><span data-stu-id="5e18f-903">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="5e18f-904">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-904">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="5e18f-905">建置 15014</span><span class="sxs-lookup"><span data-stu-id="5e18f-905">Build 15014</span></span>

<span data-ttu-id="5e18f-906">一般 Windows 組建 15014 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-906">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-907">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-907">Fixed</span></span>

- <span data-ttu-id="5e18f-908">Ctrl + C 現在如預期般運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-908">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="5e18f-909">htop 和 ps auxw 現在顯示正確的資源使用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="5e18f-909">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="5e18f-910">基本訊號的 NT 例外狀況的翻譯。</span><span class="sxs-lookup"><span data-stu-id="5e18f-910">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="5e18f-911">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="5e18f-911">(GH #513)</span></span>
- <span data-ttu-id="5e18f-912">fallocate 現在 ENOSPC 時發生無法用盡空間，而不是 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="5e18f-912">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="5e18f-913">已新增的 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="5e18f-913">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="5e18f-914">實作的 semop 和 semtimedop 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="5e18f-914">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="5e18f-915">固定的 nslookup 錯誤 IP_RECVTOS & IPV6_RECVTCLASS 通訊端選項 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="5e18f-915">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="5e18f-916">支援通訊端選項 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="5e18f-916">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="5e18f-917">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-917">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-918">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-918">LTP Results:</span></span>
<span data-ttu-id="5e18f-919">通過測試數目：709</span><span class="sxs-lookup"><span data-stu-id="5e18f-919">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="5e18f-920">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="5e18f-920">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e18f-921">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-921">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="5e18f-922">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="5e18f-922">Syscall Summary</span></span>
<span data-ttu-id="5e18f-923">總 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="5e18f-923">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="5e18f-924">實作的總計：235</span><span class="sxs-lookup"><span data-stu-id="5e18f-924">Total Implemented: 235</span></span> </br>
<span data-ttu-id="5e18f-925">虛設常式的總計：22</span><span class="sxs-lookup"><span data-stu-id="5e18f-925">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="5e18f-926">如果未實作的總計：127</span><span class="sxs-lookup"><span data-stu-id="5e18f-926">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="5e18f-927">詳細分解圖</span><span class="sxs-lookup"><span data-stu-id="5e18f-927">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="5e18f-928">建置 15007</span><span class="sxs-lookup"><span data-stu-id="5e18f-928">Build 15007</span></span>

<span data-ttu-id="5e18f-929">一般 Windows 組建 15007 的詳細資訊請造訪[Windows 部落格]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-929">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="5e18f-930">已知的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-930">Known Issue</span></span>

- <span data-ttu-id="5e18f-931">已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。</span><span class="sxs-lookup"><span data-stu-id="5e18f-931">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="5e18f-932">這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="5e18f-932">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="5e18f-933">因應措施：替代的索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="5e18f-933">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="5e18f-934">例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="5e18f-934">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="5e18f-935">此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-935">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="5e18f-936">使用者可以瀏覽的選項包含在其</span><span class="sxs-lookup"><span data-stu-id="5e18f-936">Users can explore the option to include this in their</span></span> `.bashrc`

### <a name="fixed"></a><span data-ttu-id="5e18f-937">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-937">Fixed</span></span>

- <span data-ttu-id="5e18f-938">已更正此問題，其中執行 WSL 會消耗掉 100%的 CPU 核心</span><span class="sxs-lookup"><span data-stu-id="5e18f-938">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="5e18f-939">通訊端選項 IP_PKTINFO，IPV6_RECVPKTINFO 現在支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-939">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="5e18f-940">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="5e18f-940">(GH #851, 987)</span></span>
- <span data-ttu-id="5e18f-941">截斷的 lxcore 16 個位元組到網路介面實體位址 (GH #1452 1414，1343，468，308)</span><span class="sxs-lookup"><span data-stu-id="5e18f-941">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="5e18f-942">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-942">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-943">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-943">LTP Results:</span></span>
<span data-ttu-id="5e18f-944">通過測試數目：709</span><span class="sxs-lookup"><span data-stu-id="5e18f-944">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="5e18f-945">非通過的數字 (失敗，所以已略過等等。...):255</span><span class="sxs-lookup"><span data-stu-id="5e18f-945">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e18f-946">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-946">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="5e18f-947">建置 15002</span><span class="sxs-lookup"><span data-stu-id="5e18f-947">Build 15002</span></span>

<span data-ttu-id="5e18f-948">一般 Windows 組建 15002 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-948">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="5e18f-949">已知的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-949">Known Issue</span></span>

<span data-ttu-id="5e18f-950">兩個已知的問題：</span><span class="sxs-lookup"><span data-stu-id="5e18f-950">Two known issues:</span></span>
- <span data-ttu-id="5e18f-951">已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。</span><span class="sxs-lookup"><span data-stu-id="5e18f-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="5e18f-952">這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="5e18f-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="5e18f-953">因應措施：替代的索引鍵對應至 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="5e18f-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="5e18f-954">例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="5e18f-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="5e18f-955">此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="5e18f-956">使用者可以瀏覽的選項包含在其</span><span class="sxs-lookup"><span data-stu-id="5e18f-956">Users can explore the option to include this in their</span></span> `.bashrc`

- <span data-ttu-id="5e18f-957">執行 WSL 時系統執行緒會耗用的 CPU 核心的 100%。</span><span class="sxs-lookup"><span data-stu-id="5e18f-957">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="5e18f-958">已解決的根本原因並已修正在內部。</span><span class="sxs-lookup"><span data-stu-id="5e18f-958">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e18f-959">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-959">Fixed</span></span>

- <span data-ttu-id="5e18f-960">所有的 bash 工作階段現在必須建立在相同的權限層級。</span><span class="sxs-lookup"><span data-stu-id="5e18f-960">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="5e18f-961">嘗試啟動工作階段在不同的層級會被封鎖。</span><span class="sxs-lookup"><span data-stu-id="5e18f-961">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="5e18f-962">這表示系統管理員 」 和 「 非系統管理員主控台無法在同一時間執行。</span><span class="sxs-lookup"><span data-stu-id="5e18f-962">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="5e18f-963">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="5e18f-963">(GH #626)</span></span>
<br/>
- <span data-ttu-id="5e18f-964">實作下列 NETLINK_ROUTE 訊息 （需要 Windows 系統管理員）</span><span class="sxs-lookup"><span data-stu-id="5e18f-964">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="5e18f-965">RTM_NEWADDR (支援`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="5e18f-965">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="5e18f-966">RTM_NEWROUTE (支援`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="5e18f-966">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="5e18f-967">RTM_DELADDR (支援`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="5e18f-967">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="5e18f-968">RTM_DELROUTE (支援`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="5e18f-968">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="5e18f-969">在計量付費連線 (GH #1371) 上，將無法再執行套件，以更新檢查的排程的工作</span><span class="sxs-lookup"><span data-stu-id="5e18f-969">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="5e18f-970">已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="5e18f-970">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="5e18f-971">實作的 TCP_KEEPCNT 通訊端選項 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="5e18f-971">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="5e18f-972">實作的 IP_MTU_DISCOVER INET 通訊端選項 (GH #720，717，170，69)</span><span class="sxs-lookup"><span data-stu-id="5e18f-972">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="5e18f-973">移除舊版的功能，以從 NT 路徑查閱使用 init 執行 NT 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="5e18f-973">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="5e18f-974">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="5e18f-974">(GH #1325)</span></span>
- <span data-ttu-id="5e18f-975">修正/kmsg 允許群組 / 讀取權限 (0644) (GH #1321) 模式</span><span class="sxs-lookup"><span data-stu-id="5e18f-975">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="5e18f-976">實作的 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="5e18f-976">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="5e18f-977">修正的錯誤，處理序開始時間會顯示為 2432 年 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="5e18f-977">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="5e18f-978">切換的預設詞彙環境變數，以 xterm 256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="5e18f-978">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="5e18f-979">修改處理認可的方式計算期間處理程序分支。</span><span class="sxs-lookup"><span data-stu-id="5e18f-979">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="5e18f-980">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="5e18f-980">(GH #1286)</span></span>
- <span data-ttu-id="5e18f-981">實作的 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="5e18f-981">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="5e18f-982">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="5e18f-982">(GH #1286)</span></span>
- <span data-ttu-id="5e18f-983">實作的 /proc/net/route 檔案 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="5e18f-983">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="5e18f-984">已修正的錯誤捷徑名稱的正確當地語系化 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="5e18f-984">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="5e18f-985">已修正剖析邏輯，不正確地驗證程式的標頭的 elf 必須小於 （或等於） PATH_MAX。</span><span class="sxs-lookup"><span data-stu-id="5e18f-985">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="5e18f-986">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="5e18f-986">(GH #1048)</span></span>
- <span data-ttu-id="5e18f-987">實作的 statfs 回呼 procfs，sysfs、 cgroupfs，和 binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="5e18f-987">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="5e18f-988">不會關閉 (GH #1184，也在 GH # 1193年中討論) 的固定的 AptPackageIndexUpdate windows</span><span class="sxs-lookup"><span data-stu-id="5e18f-988">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="5e18f-989">已新增的 ASLR 個性 ADDR_NO_RANDOMIZE 支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-989">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="5e18f-990">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="5e18f-990">(GH #1148, 1128)</span></span>
- <span data-ttu-id="5e18f-991">改善的 PTRACE_GETSIGINFO，SIGSEGV，針對適當 gdb AV (GH #875) 期間的堆疊追蹤</span><span class="sxs-lookup"><span data-stu-id="5e18f-991">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="5e18f-992">Elf 剖析不會再失敗 patchelf 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="5e18f-992">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="5e18f-993">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="5e18f-993">(GH #471)</span></span>
- <span data-ttu-id="5e18f-994">VPN DNS 傳播至 /etc/resolv.conf (GH #416，1350年)</span><span class="sxs-lookup"><span data-stu-id="5e18f-994">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="5e18f-995">改善 TCP 關閉更可靠的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="5e18f-995">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="5e18f-996">(GH #610 616、 1025，1335年)</span><span class="sxs-lookup"><span data-stu-id="5e18f-996">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="5e18f-997">開啟 (EMFILE) 現在會傳回正確的錯誤程式碼中，使用太多檔案時。</span><span class="sxs-lookup"><span data-stu-id="5e18f-997">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="5e18f-998">(GH # 1126年 2090年)</span><span class="sxs-lookup"><span data-stu-id="5e18f-998">(GH #1126, 2090)</span></span>
- <span data-ttu-id="5e18f-999">Windows 稽核記錄檔現在報告程序中的映像名稱建立稽核。</span><span class="sxs-lookup"><span data-stu-id="5e18f-999">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="5e18f-1000">現在依正常程序失敗時啟動 bash 視窗內從 bash.exe</span><span class="sxs-lookup"><span data-stu-id="5e18f-1000">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="5e18f-1001">當 interop 新增的錯誤訊息無法存取工作目錄下 LxFs (也就是 notepad.exe.bashrc)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1001">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="5e18f-1002">已修正的問題已在 WSL 遭截斷 Windows 路徑</span><span class="sxs-lookup"><span data-stu-id="5e18f-1002">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="5e18f-1003">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1003">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1004">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1004">LTP Results:</span></span>
<span data-ttu-id="5e18f-1005">通過測試數目：690</span><span class="sxs-lookup"><span data-stu-id="5e18f-1005">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="5e18f-1006">非通過的數字 (失敗，所以已略過等等。...):274</span><span class="sxs-lookup"><span data-stu-id="5e18f-1006">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="5e18f-1007">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1007">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1008">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1008">Syscall Support</span></span>
<span data-ttu-id="5e18f-1009">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1009">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1010">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1010">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="5e18f-1011">建置 14986</span><span class="sxs-lookup"><span data-stu-id="5e18f-1011">Build 14986</span></span>

<span data-ttu-id="5e18f-1012">一般 Windows 組建 14986 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1012">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1013">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1013">Fixed</span></span>

- <span data-ttu-id="5e18f-1014">固定的 bugchecks Netlink 與 Pty Ioctl</span><span class="sxs-lookup"><span data-stu-id="5e18f-1014">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="5e18f-1015">核心版本現在會報告 4.4.0-43 與 Xenial 的一致性</span><span class="sxs-lookup"><span data-stu-id="5e18f-1015">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="5e18f-1016">輸入指示時，現在會啟動 Bash.exe ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1016">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="5e18f-1017">執行緒現在報告識別碼正確 procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1017">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="5e18f-1018">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |現在支援 inotify_add_watch() (GH #1280) IN_ISDIR 旗標</span><span class="sxs-lookup"><span data-stu-id="5e18f-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="5e18f-1019">實作 timer_create 和相關的系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1019">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="5e18f-1020">這可讓 GHC 支援 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1020">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="5e18f-1021">已修正的問題，其中 ping 傳回 0.000ms (GH #1296) 的時間</span><span class="sxs-lookup"><span data-stu-id="5e18f-1021">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="5e18f-1022">開啟太多檔案時，則傳回正確的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1022">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="5e18f-1023">已修正的問題，在 WSL 其中網路介面 data Netlink 要求會失敗並 EINVAL 如果介面的硬體位址為 32 個位元組 （例如 Teredo 介面）</span><span class="sxs-lookup"><span data-stu-id="5e18f-1023">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="5e18f-1024">請注意，Linux 「 ip 」 公用程式，包含的 bug，其中這皆會損毀如果 WSL 報告 32 位元組的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1024">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="5e18f-1025">這是 「 ip 」，不 WSL 中的 bug。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1025">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="5e18f-1026">「 Ip 」 公用程式硬式編碼的字串緩衝區長度用來列印的硬體位址，以及該緩衝區太小而無法列印的 32 位元組的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1026">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="5e18f-1027">其他修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1027">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1028">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1028">LTP Results:</span></span>
<span data-ttu-id="5e18f-1029">通過測試數目：669</span><span class="sxs-lookup"><span data-stu-id="5e18f-1029">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="5e18f-1030">非通過的數字 (失敗，所以已略過等等。...):258</span><span class="sxs-lookup"><span data-stu-id="5e18f-1030">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="5e18f-1031">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1031">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1032">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1032">Syscall Support</span></span>
<span data-ttu-id="5e18f-1033">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1033">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1034">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1034">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="5e18f-1035">建置 14971</span><span class="sxs-lookup"><span data-stu-id="5e18f-1035">Build 14971</span></span>

<span data-ttu-id="5e18f-1036">一般 Windows 組建 14971 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1036">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1037">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1037">Fixed</span></span>

 - <span data-ttu-id="5e18f-1038">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1038">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e18f-1039">下一個版本時才會恢復有排定來定期更新。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1039">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1040">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1040">LTP Results:</span></span>
<span data-ttu-id="5e18f-1041">從 14965 以來並未變更</span><span class="sxs-lookup"><span data-stu-id="5e18f-1041">Unchanged from 14965</span></span> </br>
<span data-ttu-id="5e18f-1042">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="5e18f-1042">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e18f-1043">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1043">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1044">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="5e18f-1045">建置 14965</span><span class="sxs-lookup"><span data-stu-id="5e18f-1045">Build 14965</span></span>

<span data-ttu-id="5e18f-1046">一般 Windows 組建 14965 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1046">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1047">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1047">Fixed</span></span>

- <span data-ttu-id="5e18f-1048">支援 Netlink 通訊端通訊協定 NETLINK_ROUTE RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1048">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="5e18f-1049">可讓網路列舉的 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="5e18f-1049">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="5e18f-1050">詳細的資訊可在我們[WSL 網路部落格文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1050">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="5e18f-1051">/sbin 現在是使用者的預設路徑</span><span class="sxs-lookup"><span data-stu-id="5e18f-1051">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="5e18f-1052">現在預設 （也就是您可以現在輸入 notepad.exe 而不會增加 System32 Linux 路徑），以附加至 WSL 路徑的 NT 使用者路徑</span><span class="sxs-lookup"><span data-stu-id="5e18f-1052">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="5e18f-1053">已新增的支援 /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="5e18f-1053">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="5e18f-1054">NT 二進位檔可以立即從 WSL 啟動，當目前的工作目錄包含非 ansi 字元 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1054">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="5e18f-1055">允許在已中斷連線的 unix 資料流通訊端上的關機。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1055">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="5e18f-1056">已新增的支援 PR_GET_PDEATHSIG。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1056">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="5e18f-1057">已新增的支援 CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="5e18f-1057">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="5e18f-1058">已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1058">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="5e18f-1059">若要連接到目前的終端機的控制代碼要求。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1059">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="5e18f-1060">標示 /proc/<pid>/oom_score_adj 為可寫入。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1060">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="5e18f-1061">新增 /sys/fs/cgroup 資料夾。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1061">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="5e18f-1062">sched_setaffinity 應傳回數目相似性位元遮罩</span><span class="sxs-lookup"><span data-stu-id="5e18f-1062">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="5e18f-1063">修正未正確假設 解譯器路徑必須少於 64 個字元長 ELF 驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1063">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="5e18f-1064">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1064">(GH #743)</span></span>
- <span data-ttu-id="5e18f-1065">開啟檔案描述元可以保留主控台視窗中開啟 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1065">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="5e18f-1066">Fixeed 錯誤 rename （） 後面加上目標名稱 (GH #1008) 的正斜線失敗的位置</span><span class="sxs-lookup"><span data-stu-id="5e18f-1066">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="5e18f-1067">實作 /proc/net/dev 檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-1067">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="5e18f-1068">固定的 0.000ms 偵測由於計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1068">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="5e18f-1069">實作的 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1069">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="5e18f-1070">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1070">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1071">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1071">LTP Results:</span></span>
<span data-ttu-id="5e18f-1072">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="5e18f-1072">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e18f-1073">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1073">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1074">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1074">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="5e18f-1075">建置 14959</span><span class="sxs-lookup"><span data-stu-id="5e18f-1075">Build 14959</span></span>

<span data-ttu-id="5e18f-1076">一般 Windows 組建 14959 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1076">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1077">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1077">Fixed</span></span>

- <span data-ttu-id="5e18f-1078">已改進的 Windows 的 Pico 程序通知。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1078">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="5e18f-1079">其他資訊，請參閱[WSL 部落格](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1079">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="5e18f-1080">改進的穩定性與 Windows 互通性</span><span class="sxs-lookup"><span data-stu-id="5e18f-1080">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="5e18f-1081">已修正的錯誤 0x80070057 啟用企業資料保護 (EDP) 時，啟動 bash.exe 時</span><span class="sxs-lookup"><span data-stu-id="5e18f-1081">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="5e18f-1082">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1082">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1083">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1083">LTP Results:</span></span>
<span data-ttu-id="5e18f-1084">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="5e18f-1084">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e18f-1085">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1085">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1086">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1086">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="5e18f-1087">建置 14955</span><span class="sxs-lookup"><span data-stu-id="5e18f-1087">Build 14955</span></span>

<span data-ttu-id="5e18f-1088">一般 Windows 組建 14955 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1088">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1089">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1089">Fixed</span></span>

 - <span data-ttu-id="5e18f-1090">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1090">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e18f-1091">下一個版本時才會恢復有排定來定期更新。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1091">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1092">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1092">LTP Results:</span></span>
<span data-ttu-id="5e18f-1093">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="5e18f-1093">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e18f-1094">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1094">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1095">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1095">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="5e18f-1096">建置 14951</span><span class="sxs-lookup"><span data-stu-id="5e18f-1096">Build 14951</span></span>

<span data-ttu-id="5e18f-1097">一般 Windows 組建 14951 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1097">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="5e18f-1098">新功能：Windows / Ubuntu 互通性</span><span class="sxs-lookup"><span data-stu-id="5e18f-1098">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="5e18f-1099">現在可以直接從 WSL 命令列叫用 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1099">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="5e18f-1100">這可讓使用者使用他們的 Windows 環境和系統的方式一直無法互動的能力。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1100">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="5e18f-1101">快速的範例，就可以讓使用者執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1101">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="5e18f-1102">詳細資訊，參閱：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1102">More information can be found at:</span></span>

- [<span data-ttu-id="5e18f-1103">Interop 的 WSL 小組部落格</span><span class="sxs-lookup"><span data-stu-id="5e18f-1103">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="5e18f-1104">MSDN Interop 文件</span><span class="sxs-lookup"><span data-stu-id="5e18f-1104">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1105">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1105">Fixed</span></span>

- <span data-ttu-id="5e18f-1106">Ubuntu 16.04 (Xenial) 現在會安裝所有新的 WSL 執行個體。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1106">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="5e18f-1107">使用現有的 14.04 (Mible) 執行個體的使用者將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1107">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="5e18f-1108">現在會顯示在安裝期間設定的地區設定</span><span class="sxs-lookup"><span data-stu-id="5e18f-1108">Locale set during install is now displayed</span></span>
- <span data-ttu-id="5e18f-1109">終端機功能改良，包括的 bug，其中將 WSL 程序重新導向至檔案不一定不會運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1109">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="5e18f-1110">主控台存留期應該繫結至 bash.exe 存留期</span><span class="sxs-lookup"><span data-stu-id="5e18f-1110">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="5e18f-1111">主控台視窗大小應該使用可見的大小，而非緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="5e18f-1111">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="5e18f-1112">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1112">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1113">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1113">LTP Results:</span></span>
<span data-ttu-id="5e18f-1114">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="5e18f-1114">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e18f-1115">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1115">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1116">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="5e18f-1117">建置 14946</span><span class="sxs-lookup"><span data-stu-id="5e18f-1117">Build 14946</span></span>

<span data-ttu-id="5e18f-1118">一般 Windows 組建 14946 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1118">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1119">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1119">Fixed</span></span>

- <span data-ttu-id="5e18f-1120">已修正的問題，導致無法建立 WSL 之使用者的使用者帳戶為 NT 使用者名稱包含空格或引號。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1120">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="5e18f-1121">變更 VolFs 和 DrvFs，以傳回狀態 0 代表目錄的連結計數</span><span class="sxs-lookup"><span data-stu-id="5e18f-1121">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="5e18f-1122">支援 IPV6_MULTICAST_HOPS 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1122">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="5e18f-1123">I/O 迴圈每 tty 限制為單一主控台中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1123">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="5e18f-1124">範例： 可能是下列命令：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1124">Example: the following command is possible:</span></span>
  - <span data-ttu-id="5e18f-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="5e18f-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="5e18f-1126">空格取代為 /proc/cpuinfo (GH #1115) 中的索引標籤</span><span class="sxs-lookup"><span data-stu-id="5e18f-1126">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="5e18f-1127">DrvFs 現在會出現在 mountinfo 符合掛接的 Windows 磁碟區的名稱</span><span class="sxs-lookup"><span data-stu-id="5e18f-1127">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="5e18f-1128">/home 和 /root 現在會出現在 mountinfo 具有正確的名稱</span><span class="sxs-lookup"><span data-stu-id="5e18f-1128">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="5e18f-1129">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1129">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1130">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1130">LTP Results:</span></span>
<span data-ttu-id="5e18f-1131">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="5e18f-1131">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e18f-1132">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1133">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="5e18f-1134">建置 14942</span><span class="sxs-lookup"><span data-stu-id="5e18f-1134">Build 14942</span></span>

<span data-ttu-id="5e18f-1135">一般 Windows 組建 14942 的詳細資訊請造訪[Windows 部落格](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1135">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1136">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1136">Fixed</span></span>

- <span data-ttu-id="5e18f-1137">數個 bugchecks 解決，包括 「 嘗試執行的 NOEXECUTE 記憶體 」 網路已封鎖 SSH 的損毀</span><span class="sxs-lookup"><span data-stu-id="5e18f-1137">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="5e18f-1138">來自 DrvFs 上的 Windows 應用程式所產生之通知的 inotifiy 支援現為</span><span class="sxs-lookup"><span data-stu-id="5e18f-1138">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="5e18f-1139">實作 TCP_KEEPIDLE 和 TCP_KEEPINTVL mongod。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1139">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="5e18f-1140">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1140">(GH #695)</span></span>
- <span data-ttu-id="5e18f-1141">實作 pivot_root 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="5e18f-1141">Implement the pivot_root system call</span></span>
- <span data-ttu-id="5e18f-1142">實作 SO_DONTROUTE 的通訊端選項</span><span class="sxs-lookup"><span data-stu-id="5e18f-1142">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="5e18f-1143">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1143">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="5e18f-1144">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1144">LTP Results:</span></span>
<span data-ttu-id="5e18f-1145">通過測試數目：665</span><span class="sxs-lookup"><span data-stu-id="5e18f-1145">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e18f-1146">非通過的數字 (失敗，所以已略過等等。...):263</span><span class="sxs-lookup"><span data-stu-id="5e18f-1146">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e18f-1147">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1147">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1148">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1148">Syscall Support</span></span>
<span data-ttu-id="5e18f-1149">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1149">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1150">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1150">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="5e18f-1151">建置 14936</span><span class="sxs-lookup"><span data-stu-id="5e18f-1151">Build 14936</span></span>

<span data-ttu-id="5e18f-1152">一般 Windows 組建 14936 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1152">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="5e18f-1153">注意：WSL 會安裝在即將推出的版本中的 Ubuntu 16.04 版 (Xenial) 而不是 Ubuntu 14.04 （駒）。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1153">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="5e18f-1154">這項變更將套用到安裝新的執行個體 （lxrun.exe /install 或 bash.exe 第一次執行） 的測試人員。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1154">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="5e18f-1155">具有可信賴的現有執行個體將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1155">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="5e18f-1156">使用者可以 Xenial 使用執行版本升級 命令來升級其 Mible 映像。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1156">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="5e18f-1157">已知的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1157">Known Issue</span></span>
<span data-ttu-id="5e18f-1158">WSL 發生某些通訊端實作的問題。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1158">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="5e18f-1159">檢查錯誤會造成系統呈現的損毀並出現錯誤 「 嘗試執行的 NOEXECUTE 記憶體 」。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1159">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="5e18f-1160">此問題最常見的現象使用 ssh 時當機。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1160">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="5e18f-1161">修正內部組建並將測試人員儘早推送根本原因。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1161">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e18f-1162">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1162">Fixed</span></span>

- <span data-ttu-id="5e18f-1163">實作 chroot 系統呼叫</span><span class="sxs-lookup"><span data-stu-id="5e18f-1163">Implemented the chroot system call</span></span>
- <span data-ttu-id="5e18f-1164">改進 inotify~~包括來自 DrvFs 上的 Windows 應用程式所產生之通知的支援~~</span><span class="sxs-lookup"><span data-stu-id="5e18f-1164">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="5e18f-1165">修正：Inotify 支援來自 Windows 應用程式無法使用目前的變更。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1165">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="5e18f-1166">通訊端繫結的 ipv6::<port n>現在支援 IPV6_V6ONLY (GH #68、 #157、 #393、 #460、 #674、 #740、 #982、 #996)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1166">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="5e18f-1167">Waitid systemcall WNOWAIT 行為實作 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1167">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="5e18f-1168">支援 IP 通訊端選項 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="5e18f-1168">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="5e18f-1169">長度為零的 read （） 應該會立即傳回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1169">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="5e18f-1170">正確處理不在.tar 檔案中包含 NULL 結束字元的檔名和檔案名稱前置詞。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1170">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="5e18f-1171">/dev/null 時發生 epoll 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1171">epoll support for /dev/null</span></span>
- <span data-ttu-id="5e18f-1172">修正 /dev/alarm 時間來源</span><span class="sxs-lookup"><span data-stu-id="5e18f-1172">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="5e18f-1173">Bash-c 現在能夠重新導向至檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-1173">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="5e18f-1174">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1174">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1175">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1175">LTP Results:</span></span>
<span data-ttu-id="5e18f-1176">通過測試數目：664</span><span class="sxs-lookup"><span data-stu-id="5e18f-1176">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e18f-1177">非通過的數字 (失敗，所以已略過等等。...):264</span><span class="sxs-lookup"><span data-stu-id="5e18f-1177">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="5e18f-1178">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1178">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1179">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1179">Syscall Support</span></span>
<span data-ttu-id="5e18f-1180">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1180">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1181">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1181">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="5e18f-1182">建置 14931</span><span class="sxs-lookup"><span data-stu-id="5e18f-1182">Build 14931</span></span>

<span data-ttu-id="5e18f-1183">一般 Windows 組建 14931 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1183">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1184">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1184">Fixed</span></span>

 - <span data-ttu-id="5e18f-1185">由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1185">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e18f-1186">下一個版本中，將會繼續定期排定的更新。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1186">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="5e18f-1187">建置 14926</span><span class="sxs-lookup"><span data-stu-id="5e18f-1187">Build 14926</span></span>

<span data-ttu-id="5e18f-1188">一般 Windows 組建 14926 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1188">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1189">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1189">Fixed</span></span>

- <span data-ttu-id="5e18f-1190">Ping 現在可在主控台中確實具備系統管理員權限</span><span class="sxs-lookup"><span data-stu-id="5e18f-1190">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="5e18f-1191">現在支援，也沒有管理員權限的 ping 6</span><span class="sxs-lookup"><span data-stu-id="5e18f-1191">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="5e18f-1192">Inotify 支援透過 WSL 修改的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1192">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="5e18f-1193">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1193">(GH #216)</span></span>
  - <span data-ttu-id="5e18f-1194">支援的旗標：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1194">Flags supported:</span></span>
    - <span data-ttu-id="5e18f-1195">inotify_init1:LX_O_CLOEXEC LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="5e18f-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="5e18f-1196">inotify_add_watch 事件：LX_IN_ACCESS、 LX_IN_MODIFY、 LX_IN_ATTRIB、 LX_IN_CLOSE_WRITE、 LX_IN_CLOSE_NOWRITE、 LX_IN_OPEN、 LX_IN_MOVED_FROM、 LX_IN_MOVED_TO、 LX_IN_CREATE、 LX_IN_DELETE、 LX_IN_DELETE_SELF、 LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="5e18f-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="5e18f-1197">inotify_add_watch 屬性：LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="5e18f-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="5e18f-1198">讀取輸出：LX_IN_ISDIR LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="5e18f-1198">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="5e18f-1199">已知的問題：修改檔案從 Windows 應用程式不會產生任何事件</span><span class="sxs-lookup"><span data-stu-id="5e18f-1199">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="5e18f-1200">Unix 通訊端現在支援 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="5e18f-1200">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e18f-1201">LTP 結果：</span><span class="sxs-lookup"><span data-stu-id="5e18f-1201">LTP Results:</span></span>
<span data-ttu-id="5e18f-1202">通過測試數目：651</span><span class="sxs-lookup"><span data-stu-id="5e18f-1202">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="5e18f-1203">非通過的數字 (失敗，所以已略過等等。...):258</span><span class="sxs-lookup"><span data-stu-id="5e18f-1203">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="5e18f-1204">LTP 測試回合記錄檔</span><span class="sxs-lookup"><span data-stu-id="5e18f-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="5e18f-1205">建置 14915</span><span class="sxs-lookup"><span data-stu-id="5e18f-1205">Build 14915</span></span>

<span data-ttu-id="5e18f-1206">一般 Windows 組建 14915 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1206">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1207">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1207">Fixed</span></span>
-  <span data-ttu-id="5e18f-1208">Socketpair unix 資料包通訊端 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1208">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="5e18f-1209">SO_REUSEADDR Unix 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1209">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="5e18f-1210">SO_BROADCAST (GH #568) 的 UNIX 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1210">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="5e18f-1211">SOCK_SEQPACKET (GH #758，#546) 的 Unix 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1211">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="5e18f-1212">新增支援 unix 資料包通訊端的傳送、 接收和關閉</span><span class="sxs-lookup"><span data-stu-id="5e18f-1212">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="5e18f-1213">修正由於非固定位址的無效 mmap 參數驗證錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1213">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="5e18f-1214">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1214">(GH #847)</span></span>
- <span data-ttu-id="5e18f-1215">支援的暫止 / 繼續的終端機的狀態</span><span class="sxs-lookup"><span data-stu-id="5e18f-1215">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="5e18f-1216">若要解除封鎖 「 螢幕 」 公用程式 (GH #774) TIOCPKT ioctl 的支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1216">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="5e18f-1217">已知的問題：功能鍵無法運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1217">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="5e18f-1218">已更正的競爭可能會導致將釋放的成員 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814) 存取的 TimerFd</span><span class="sxs-lookup"><span data-stu-id="5e18f-1218">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="5e18f-1219">啟用 futex、 輪詢和 clock_nanosleep 的可重新啟動系統呼叫支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1219">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="5e18f-1220">新增繫結掛接支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1220">Added bind mount support</span></span>
- <span data-ttu-id="5e18f-1221">如需掛接命名空間支援取消共用</span><span class="sxs-lookup"><span data-stu-id="5e18f-1221">unshare for mount namespace support</span></span>
    - <span data-ttu-id="5e18f-1222">已知的問題：當建立新的掛接命名空間與`unshare(CLONE_NEWNS)`仍然指向舊的命名空間目前的工作目錄</span><span class="sxs-lookup"><span data-stu-id="5e18f-1222">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="5e18f-1223">其他改進和 bug 修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-1223">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="5e18f-1224">建置 14905</span><span class="sxs-lookup"><span data-stu-id="5e18f-1224">Build 14905</span></span>

<span data-ttu-id="5e18f-1225">一般 Windows 組建 14905 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1225">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1226">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1226">Fixed</span></span>
- <span data-ttu-id="5e18f-1227">可重新啟動系統呼叫現在支援 (GH #349，GH #520)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1227">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="5e18f-1228">結束在 / 現在操作的目錄 (GH #650) 的符號連結</span><span class="sxs-lookup"><span data-stu-id="5e18f-1228">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="5e18f-1229">實作的 RNDGETENTCNT ioctl /dev/random 的</span><span class="sxs-lookup"><span data-stu-id="5e18f-1229">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="5e18f-1230">實作 /proc/ [pid] / 掛接，/proc/ [pid] / mountinfo 和 /proc/ [pid] / mountstats 檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-1230">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="5e18f-1231">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1231">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="5e18f-1232">建置 14901</span><span class="sxs-lookup"><span data-stu-id="5e18f-1232">Build 14901</span></span>
<span data-ttu-id="5e18f-1233">第一次的測試人員組建的 Windows 10 年度更新版的文章。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1233">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="5e18f-1234">一般 Windows 組建 14901 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1234">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1235">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1235">Fixed</span></span>
- <span data-ttu-id="5e18f-1236">已修正的尾端斜線問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1236">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="5e18f-1237">命令，例如`$ mv a/c/ a/b/`現在可運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1237">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="5e18f-1238">只有當 Ubuntu 地區設定應該設為 Windows 地區設定，現在安裝提示</span><span class="sxs-lookup"><span data-stu-id="5e18f-1238">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="5e18f-1239">Procfs 支援 ns 資料夾</span><span class="sxs-lookup"><span data-stu-id="5e18f-1239">Procfs support for ns folder</span></span>
- <span data-ttu-id="5e18f-1240">新增掛接和卸載 tmpfs procfs 和 sysfs 檔案系統</span><span class="sxs-lookup"><span data-stu-id="5e18f-1240">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="5e18f-1241">修正 mknod [at] 32 位元 ABI 簽章</span><span class="sxs-lookup"><span data-stu-id="5e18f-1241">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="5e18f-1242">移至分派模型的 Unix 通訊端</span><span class="sxs-lookup"><span data-stu-id="5e18f-1242">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="5e18f-1243">設定使用 setsockopt INET 通訊端接收緩衝區大小應該接受</span><span class="sxs-lookup"><span data-stu-id="5e18f-1243">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="5e18f-1244">實作 MSG_CMSG_CLOEXEC unix 通訊端接收訊息的旗標</span><span class="sxs-lookup"><span data-stu-id="5e18f-1244">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="5e18f-1245">Linux 程序 stdin/stdout 管道重新導向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1245">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="5e18f-1246">允許的 CMD 中的 bash-c 命令的管線</span><span class="sxs-lookup"><span data-stu-id="5e18f-1246">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="5e18f-1247">範例： > dir |bash-c"grep foo"</span><span class="sxs-lookup"><span data-stu-id="5e18f-1247">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="5e18f-1248">現在可以在多個分頁檔 (GH #538，#358) 的系統上安裝 bash</span><span class="sxs-lookup"><span data-stu-id="5e18f-1248">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="5e18f-1249">預設 INET 通訊端緩衝區大小應該符合預設 Ubuntu 安裝程式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1249">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="5e18f-1250">對齊到 listxattr xattr syscall</span><span class="sxs-lookup"><span data-stu-id="5e18f-1250">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="5e18f-1251">只從 SIOCGIFCONF 傳回有效的 IPv4 位址的介面</span><span class="sxs-lookup"><span data-stu-id="5e18f-1251">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="5e18f-1252">修正當由 ptrace 插入的訊號的預設動作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1252">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="5e18f-1253">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="5e18f-1253">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="5e18f-1254">還原在 sigreturn 內容時所使用電腦內容暫存器值</span><span class="sxs-lookup"><span data-stu-id="5e18f-1254">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="5e18f-1255">這個方法可以解決此問題其中的某些使用者溢出 java 和 javac</span><span class="sxs-lookup"><span data-stu-id="5e18f-1255">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="5e18f-1256">實作 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="5e18f-1256">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1257">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1257">Syscall Support</span></span>
<span data-ttu-id="5e18f-1258">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1259">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="5e18f-1260">建置 Windows 10 年度更新版的 14388</span><span class="sxs-lookup"><span data-stu-id="5e18f-1260">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="5e18f-1261">一般 Windows 組建 14388 的詳細資訊請造訪[Windows 部落格](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1261">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1262">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1262">Fixed</span></span>
- <span data-ttu-id="5e18f-1263">準備適用於 Windows 10 年度更新 8/2 的修正</span><span class="sxs-lookup"><span data-stu-id="5e18f-1263">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="5e18f-1264">在年度更新版的 WSL 的詳細資訊都位於我們[部落格](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1264">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="5e18f-1265">建置 14376</span><span class="sxs-lookup"><span data-stu-id="5e18f-1265">Build 14376</span></span>
<span data-ttu-id="5e18f-1266">一般 Windows 組建 14376 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1266">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1267">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1267">Fixed</span></span>
- <span data-ttu-id="5e18f-1268">移除某些情況下，apt get 停止回應 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1268">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="5e18f-1269">已修正的問題，空白的掛接已無法正確處理</span><span class="sxs-lookup"><span data-stu-id="5e18f-1269">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="5e18f-1270">已修正的問題其中 ramdisks 已不正確地掛載</span><span class="sxs-lookup"><span data-stu-id="5e18f-1270">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="5e18f-1271">變更 unix 通訊端接受支援旗標 (部分 GH #451)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1271">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="5e18f-1272">已修正常見的網路相關藍色螢幕</span><span class="sxs-lookup"><span data-stu-id="5e18f-1272">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="5e18f-1273">存取 /proc/ [pid] 時，已修正藍色螢幕 / 工作 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1273">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="5e18f-1274">已修正的 CPU 使用率過高的一些 pty 案例 (GH #488，#504)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1274">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="5e18f-1275">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1275">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="5e18f-1276">建置 14371</span><span class="sxs-lookup"><span data-stu-id="5e18f-1276">Build 14371</span></span>
<span data-ttu-id="5e18f-1277">一般 Windows 組建 14371 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1277">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1278">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1278">Fixed</span></span>
- <span data-ttu-id="5e18f-1279">當使用 ptrace 更正 SIGCHLD 與 wait() 計時競爭</span><span class="sxs-lookup"><span data-stu-id="5e18f-1279">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="5e18f-1280">當路徑有尾端時修正某些行為 / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1280">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="5e18f-1281">取消重新命名/連結來失敗的原因是子系的開啟控制代碼已修正的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1281">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="5e18f-1282">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1282">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="5e18f-1283">建置 14366</span><span class="sxs-lookup"><span data-stu-id="5e18f-1283">Build 14366</span></span>
<span data-ttu-id="5e18f-1284">一般 Windows 組建 14366 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1284">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1285">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1285">Fixed</span></span>
- <span data-ttu-id="5e18f-1286">修正透過符號連結的檔案建立時</span><span class="sxs-lookup"><span data-stu-id="5e18f-1286">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="5e18f-1287">已新增的 listxattr 適用於 Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1287">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="5e18f-1288">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1288">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1289">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1289">Syscall Support</span></span>
-   <span data-ttu-id="5e18f-1290">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1290">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1291">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1291">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="5e18f-1292">組建 14361 開始</span><span class="sxs-lookup"><span data-stu-id="5e18f-1292">Build 14361</span></span>
<span data-ttu-id="5e18f-1293">一般 Windows 組建 14361 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1293">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1294">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1294">Fixed</span></span>
- <span data-ttu-id="5e18f-1295">Windows 上執行 bash on Ubuntu 時，DrvFs 現在會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1295">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="5e18f-1296">使用者可能 case.txt 和案例。TXT 其 /mnt c 磁碟機</span><span class="sxs-lookup"><span data-stu-id="5e18f-1296">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="5e18f-1297">在 Windows 上 Ubuntu 之 Bash 上才支援區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1297">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="5e18f-1298">當外部 Bash NTFS 的報表檔案的正確，但未預期的行為可能會發生與從 Windows 檔案互動。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1298">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="5e18f-1299">每個磁碟區 (也就是 /mnt/c) 的根目錄不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="5e18f-1299">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="5e18f-1300">可以找到更多有關處理 Windows 中的這些檔案[此處](https://support.microsoft.com/en-us/kb/100625)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1300">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="5e18f-1301">經過大幅增強的 pty / tty 支援。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1301">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="5e18f-1302">應用程式，例如 TMUX 現在支援 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1302">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="5e18f-1303">使用者帳戶不一定建立固定的安裝問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1303">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="5e18f-1304">最佳化以很長的引數清單的命令列引數結構。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1304">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="5e18f-1305">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1305">(GH #153)</span></span>
- <span data-ttu-id="5e18f-1306">現在可以刪除並 chmod read_only 檔案從 DrvFs</span><span class="sxs-lookup"><span data-stu-id="5e18f-1306">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="5e18f-1307">已修正某些情況下，終端機的停止回應，在中斷連線 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1307">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="5e18f-1308">chmod 和 chown 現在使用 tty 裝置</span><span class="sxs-lookup"><span data-stu-id="5e18f-1308">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="5e18f-1309">允許連線至 0.0.0.0 和:: 為 localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1309">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="5e18f-1310">Sendmsg/recvmsg 現在處理的 IO 向量長度 > 1 (部分 GH #376)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1310">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="5e18f-1311">使用者可以立即選擇不自動產生的主機檔案 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1311">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="5e18f-1312">自動安裝 (GH #11) 期間會符合 Linux NT 地區設定的地區設定</span><span class="sxs-lookup"><span data-stu-id="5e18f-1312">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="5e18f-1313">新增 /proc/sys/vm/swappiness 檔案 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1313">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="5e18f-1314">才能正確 strace 現在結束</span><span class="sxs-lookup"><span data-stu-id="5e18f-1314">strace now exits correctly</span></span>
- <span data-ttu-id="5e18f-1315">允許管道來重新開啟透過 /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1315">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="5e18f-1316">隱藏 %LOCALAPPDATA%\lxss 從 DrvFs (GH #270) 下的目錄</span><span class="sxs-lookup"><span data-stu-id="5e18f-1316">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="5e18f-1317">更妥善地處理的 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1317">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="5e18f-1318">命令喜歡"bash ~-c ls 」 現在支援 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1318">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="5e18f-1319">通訊端現在，當 epoll 關機 (GH #271) 期間所提供的讀取</span><span class="sxs-lookup"><span data-stu-id="5e18f-1319">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="5e18f-1320">lxrun / 解除安裝的刪除的檔案和資料夾工作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1320">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="5e18f-1321">已更正的 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1321">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="5e18f-1322">已改善支援 x11 xEmacs (GH #481) 之類的應用程式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1322">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="5e18f-1323">已更新初始執行緒堆疊大小，以符合預設 Ubuntu 設定，並正確地回報給 get_rlimit syscall (GH #172，#258) 的大小</span><span class="sxs-lookup"><span data-stu-id="5e18f-1323">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="5e18f-1324">改善報告 pico 程序映像名稱 （例如，適用於稽核）</span><span class="sxs-lookup"><span data-stu-id="5e18f-1324">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="5e18f-1325">實作的 /proc/mountinfo df 命令</span><span class="sxs-lookup"><span data-stu-id="5e18f-1325">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="5e18f-1326">已修正子名稱的符號連結錯誤程式碼。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1326">Fixed symlink error code for child name .</span></span> <span data-ttu-id="5e18f-1327">與...</span><span class="sxs-lookup"><span data-stu-id="5e18f-1327">and ..</span></span>
- <span data-ttu-id="5e18f-1328">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1328">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1329">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1329">Syscall Support</span></span>
<span data-ttu-id="5e18f-1330">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1331">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="5e18f-1332">組建 14352</span><span class="sxs-lookup"><span data-stu-id="5e18f-1332">Build 14352</span></span>
<span data-ttu-id="5e18f-1333">一般 Windows 組建 14352 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1333">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1334">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1334">Fixed</span></span>
- <span data-ttu-id="5e18f-1335">已修正的問題，大型檔案已下載 / 無法正確建立。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1335">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="5e18f-1336">這應該解除封鎖 npm 和其他案例 （GH #3，GH #313）</span><span class="sxs-lookup"><span data-stu-id="5e18f-1336">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="5e18f-1337">移除某些情況下通訊端的停止回應</span><span class="sxs-lookup"><span data-stu-id="5e18f-1337">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="5e18f-1338">修正一些 ptrace 錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-1338">Corrected some ptrace errors</span></span>
- <span data-ttu-id="5e18f-1339">已修正的問題，以允許檔案名稱超過 255 個字元的 WSL</span><span class="sxs-lookup"><span data-stu-id="5e18f-1339">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="5e18f-1340">非英文字元的改進的支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1340">Improved support for non-English characters</span></span>
- <span data-ttu-id="5e18f-1341">加入目前的 Windows 時區資料，並設定為預設值</span><span class="sxs-lookup"><span data-stu-id="5e18f-1341">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="5e18f-1342">唯一裝置識別碼的每個掛接點 （jre 修復 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="5e18f-1342">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="5e18f-1343">包含路徑與修正問題 」。 」</span><span class="sxs-lookup"><span data-stu-id="5e18f-1343">Correct issue with paths containing “.”</span></span> <span data-ttu-id="5e18f-1344">和"."</span><span class="sxs-lookup"><span data-stu-id="5e18f-1344">and “..”</span></span>
- <span data-ttu-id="5e18f-1345">已新增的 Fifo 支援 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="5e18f-1345">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="5e18f-1346">更新的 resolv.conf 來比對原生的 Ubuntu 格式的格式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1346">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="5e18f-1347">某些 procfs 的清除工作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1347">Some procfs cleanup</span></span>
- <span data-ttu-id="5e18f-1348">系統管理員主控台 (GH #18) 的已啟用的 ping</span><span class="sxs-lookup"><span data-stu-id="5e18f-1348">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1349">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1349">Syscall Support</span></span>
<span data-ttu-id="5e18f-1350">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1351">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="5e18f-1352">建置 14342</span><span class="sxs-lookup"><span data-stu-id="5e18f-1352">Build 14342</span></span>
<span data-ttu-id="5e18f-1353">一般的 Windows 上的資訊建置 14342 [Windows 部落格](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1353">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="5e18f-1354">可以上找到有關 VolFs 和 DriveFs [WSL 部落格](https://blogs.msdn.microsoft.com/wsl)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1354">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e18f-1355">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1355">Fixed</span></span>
- <span data-ttu-id="5e18f-1356">Windows 使用者的使用者名稱中有 Unicode 字元時，已修正安裝問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1356">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="5e18f-1357">第一次執行的預設現在會提供常見問題集中的 apt get 更新 udev 因應措施</span><span class="sxs-lookup"><span data-stu-id="5e18f-1357">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="5e18f-1358">啟用 DriveFs 中的符號連結 (於 /mnt/<drive>) 目錄</span><span class="sxs-lookup"><span data-stu-id="5e18f-1358">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="5e18f-1359">符號連結現在可 DriveFs 和 VolFs 之間</span><span class="sxs-lookup"><span data-stu-id="5e18f-1359">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="5e18f-1360">定址頂部層級路徑剖析的問題： ls。 / / 現在會如預期般運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1360">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="5e18f-1361">npm 安裝上 DriveFs 和現在正設法-g 選項</span><span class="sxs-lookup"><span data-stu-id="5e18f-1361">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="5e18f-1362">已修正防止 PHP 伺服器啟動的問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1362">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="5e18f-1363">已更新的預設環境的值，例如更接近比對原生的 Ubuntu $PATH</span><span class="sxs-lookup"><span data-stu-id="5e18f-1363">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="5e18f-1364">更新 apt 套件快取的 Windows 中加入每週的維護工作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1364">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="5e18f-1365">ELF 標頭驗證修正問題，WSL 現在支援所有 Melkor 選項</span><span class="sxs-lookup"><span data-stu-id="5e18f-1365">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="5e18f-1366">Zsh shell 正常運作</span><span class="sxs-lookup"><span data-stu-id="5e18f-1366">Zsh shell is functional</span></span>
- <span data-ttu-id="5e18f-1367">先行編譯的 Go 二進位檔現在支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1367">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="5e18f-1368">在第一次執行的 Bash.exe 提示是現在正確當地語系化</span><span class="sxs-lookup"><span data-stu-id="5e18f-1368">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="5e18f-1369">/proc/meminfo 現在會傳回正確的資訊</span><span class="sxs-lookup"><span data-stu-id="5e18f-1369">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="5e18f-1370">VFS 現可支援的通訊端</span><span class="sxs-lookup"><span data-stu-id="5e18f-1370">Sockets now supported in VFS</span></span>
- <span data-ttu-id="5e18f-1371">/dev 現在已掛接為 tempfs</span><span class="sxs-lookup"><span data-stu-id="5e18f-1371">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="5e18f-1372">Fifo 現在支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1372">Fifo now supported</span></span>
- <span data-ttu-id="5e18f-1373">多核心系統現在/proc/cpuinfo 中正確顯示</span><span class="sxs-lookup"><span data-stu-id="5e18f-1373">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="5e18f-1374">其他增強功能與在第一次執行期間所下載的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5e18f-1374">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="5e18f-1375">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1375">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="5e18f-1376">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1376">Supported syscall list below.</span></span>
- <span data-ttu-id="5e18f-1377">其他錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1377">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="5e18f-1378">已知問題</span><span class="sxs-lookup"><span data-stu-id="5e18f-1378">Known Issues</span></span>
- <span data-ttu-id="5e18f-1379">無法解析 '.'</span><span class="sxs-lookup"><span data-stu-id="5e18f-1379">Not resolving ‘..’</span></span> <span data-ttu-id="5e18f-1380">在某些情況下 DriveFs 上的正確</span><span class="sxs-lookup"><span data-stu-id="5e18f-1380">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1381">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1381">Syscall Support</span></span>
<span data-ttu-id="5e18f-1382">以下是某些實作在 WSL 的全新或加強 syscall 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1382">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1383">在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1383">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="5e18f-1384">建置 14332</span><span class="sxs-lookup"><span data-stu-id="5e18f-1384">Build 14332</span></span>

<span data-ttu-id="5e18f-1385">一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1385">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="5e18f-1386">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1386">Fixed</span></span>
- <span data-ttu-id="5e18f-1387">改良的 resolv.conf 產生包括設定 DNS 項目優先順序</span><span class="sxs-lookup"><span data-stu-id="5e18f-1387">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="5e18f-1388">移動檔案和目錄，以及非 /mnt 之間的問題-/ /mnt 磁碟機</span><span class="sxs-lookup"><span data-stu-id="5e18f-1388">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="5e18f-1389">您現在可以使用符號連結建立 tar 檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-1389">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="5e18f-1390">在 建立執行個體上新增的預設 /run/lock 目錄</span><span class="sxs-lookup"><span data-stu-id="5e18f-1390">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="5e18f-1391">若要傳回適當的狀態資訊更新 /dev/null 時發生</span><span class="sxs-lookup"><span data-stu-id="5e18f-1391">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="5e18f-1392">下載期間第一次執行時的其他錯誤</span><span class="sxs-lookup"><span data-stu-id="5e18f-1392">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="5e18f-1393">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1393">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="5e18f-1394">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1394">Supported syscall list below.</span></span>
- <span data-ttu-id="5e18f-1395">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1395">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1396">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1396">Syscall Support</span></span>
<span data-ttu-id="5e18f-1397">以下是新 syscall WSL 中有某種實作。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1397">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="5e18f-1398">在這份清單 syscall 在至少一個案例中，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1398">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="5e18f-1399">組建 14328</span><span class="sxs-lookup"><span data-stu-id="5e18f-1399">Build 14328</span></span>

<span data-ttu-id="5e18f-1400">一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1400">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="5e18f-1401">新功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1401">New Features</span></span>
* <span data-ttu-id="5e18f-1402">現在支援 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1402">Now support Linux users.</span></span>  <span data-ttu-id="5e18f-1403">在 Windows 上 Ubuntu 上安裝 Bash 會提示輸入建立 Linux 使用者。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1403">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="5e18f-1404">如需詳細資訊，請瀏覽 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="5e18f-1404">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="5e18f-1405">主機名稱現在已不再設定為 Windows 電腦的名稱， @localhost</span><span class="sxs-lookup"><span data-stu-id="5e18f-1405">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="5e18f-1406">如需詳細資訊請組建 14328，請瀏覽： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="5e18f-1406">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="5e18f-1407">固定式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1407">Fixed</span></span>
* <span data-ttu-id="5e18f-1408">非於 /mnt/ 的符號連結改進<drive>檔案</span><span class="sxs-lookup"><span data-stu-id="5e18f-1408">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="5e18f-1409">npm 安裝現在的運作方式</span><span class="sxs-lookup"><span data-stu-id="5e18f-1409">npm install now works</span></span>
    * <span data-ttu-id="5e18f-1410">jdk 現在可安裝的 jre 使用指示[此處](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1410">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="5e18f-1411">已知問題： 符號連結無法運作的 Windows 掛接。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1411">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="5e18f-1412">功能可在更新的組建</span><span class="sxs-lookup"><span data-stu-id="5e18f-1412">Functionality will be available in a later build</span></span>
* <span data-ttu-id="5e18f-1413">top 和 htop 現在會顯示</span><span class="sxs-lookup"><span data-stu-id="5e18f-1413">top and htop now display</span></span>
* <span data-ttu-id="5e18f-1414">其他錯誤訊息，某些安裝失敗</span><span class="sxs-lookup"><span data-stu-id="5e18f-1414">Additional error messages for some install failures</span></span>
* <span data-ttu-id="5e18f-1415">Syscall 改進和錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1415">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="5e18f-1416">支援的 syscall 下方的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1416">Supported syscall list below.</span></span>
* <span data-ttu-id="5e18f-1417">其他改進錯誤修正和增強功能</span><span class="sxs-lookup"><span data-stu-id="5e18f-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e18f-1418">Syscall 支援</span><span class="sxs-lookup"><span data-stu-id="5e18f-1418">Syscall Support</span></span>
<span data-ttu-id="5e18f-1419">以下是 syscall 的某些實作在 WSL 的清單。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1419">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="5e18f-1420">Syscall 在這份清單中至少一個案例中，支援，但可能不具有所有參數都支援這一次。</span><span class="sxs-lookup"><span data-stu-id="5e18f-1420">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
