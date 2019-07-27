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
# <a name="release-notes-for-windows-subsystem-for-linux"></a>適用于 Linux 的 Windows 子系統版本資訊


## <a name="build-18945"></a>組建18945
如需組建18945的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。

### <a name="wsl"></a>WSL
* [WSL2]允許使用 localhost: port 從主機存取 WSL2 中的接聽 tcp 通訊端
* [WSL2]修正安裝/轉換失敗和其他診斷以追蹤未來問題 [GH 4105] 
* [WSL2]改善 WSL2 網路問題的診斷
* [WSL2]將核心版本更新為4.19.55
* [WSL2]使用 docker 所需的設定選項更新核心 [GH 4165]
* [WSL2]增加指派給輕量公用程式 VM 的 Cpu 數目, 使其與主機相同 (之前在核心設定中 CONFIG_NR_CPUS 的上限為 8) [GH 4137]
* [WSL2]建立 WSL2 輕量 VM 的交換檔
* [WSL2]允許透過\\ \\wsl $\\散發版本顯示使用者裝載 (例如 sshfs) [GH 4172]
* [WSL2]改善9p 檔案系統效能
* [WSL2]確保 vhd ACL 沒有無限成長 [GH 4126]
* [WSL2]更新核心設定以支援 squashfs 和 xt_conntrack [GH 4107, 4123]
* [WSL2]修正 interop. enabled/etc/wsl.conf 選項 [GH 4140]
* [WSL2]如果檔案系統不支援 EAs, 則傳回 ENOTSUP
* [WSL2]修正具有 wsl $ \\的\\CopyFile 停止回應
* 將預設 umask 切換至 0022, 並將 filesystem. umask 設定新增至/etc/wsl.conf
* 修正 wslpath 以適當地解決符號連結, 這是回歸在 19h1 [GH 4078]
* 引進% UserProfile%\.wslconfig 檔案以調整 WSL2 設定
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

## <a name="build-18917"></a>組建18917
如需組建18917的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。

### <a name="wsl"></a>WSL
* WSL 2 現已推出! 如需詳細資訊, 請參閱[blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) 。
* 修正透過符號連結啟動 Windows 進程的回歸無法正常運作 [GH 3999]
* 將 wsl--list--verbose、wsl--list--quiet 和 wsl--import--version 選項新增至 wsl
* 新增 wsl--shutdown 選項
* 方案 9:允許開啟目錄以供寫入成功

## <a name="build-18890"></a>組建18890
如需組建18890的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。

### <a name="wsl"></a>WSL
* 非封鎖通訊端洩漏 [GH 2913]
* 對終端機的 EOF 輸入可以封鎖後續讀取 [GH 3421]
* 更新 resolv.conf 的標頭以參考 wsl [在 GH 3928 中討論]
* Epoll 刪除程式碼中的鎖死 [GH 3922]
* 處理引數中的空格--import 和– export [GH 3932]
* 擴充 mmap 的檔案無法正常運作 [GH 3939]
* 修正 ARM64 \\wsl $ access 無法正常運作的問題
* 為 wsl 新增更好的預設圖示

## <a name="build-18342"></a>組建18342
如需組建18342的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。

### <a name="wsl"></a>WSL
* 我們新增了一項功能, 讓使用者從 Windows 存取 WSL 散發版本中的 Linux 檔案。 這些檔案可透過命令列存取, 而 Windows 應用程式 (例如檔案瀏覽器、VSCode 等) 則可以與這些檔案互動。 流覽至 wsl \\$ \\ \\ \\< distro_name > 以存取您的檔案, 或流覽至\\wsl $ 來查看執行中的發行版本清單
* 新增額外的 CPU 資訊標記並修正 Cpus_allowed [_list] 值 [GH 2234]
* 從非領導者執行緒支援 exec [GH 3800]
* 將設定更新失敗視為非嚴重的 [GH 3785]
* 更新 binfmt 以適當地處理位移 [GH 3768]
* 啟用對應規劃9的網路磁碟機 [GH 3854]
* 支援 Windows > Linux 和 Linux > 適用于系結裝載的 Windows 路徑轉譯
* 在以唯讀狀態開啟的檔案上建立對應的唯讀區段

## <a name="build-18334"></a>組建18334
如需組建18334的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。

### <a name="wsl"></a>WSL
* 重新設計 Windows 時區對應到 Linux 時區的方式 [GH 3747]
* 修正記憶體流失並加入新的字串轉譯函數 [GH 3746]
* 不含執行緒的 threadgroup 上的 SIGCONT 不是「GH 3741」 
* 在/proc/self/fd 中正確顯示通訊端和 epoll 檔案描述項

## <a name="build-18305"></a>組建18305
如需組建18305的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。

### <a name="wsl"></a>WSL
* pthreads 在主要執行緒結束時遺失檔案的存取權 [GH 3589]
* TIOCSCTTY 應該忽略 "force" 參數, 除非它是必要的 [GH 3652]
* wsl 的命令列改進和匯入/匯出功能的新增。
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

## <a name="build-18277"></a>組建18277
如需組建18277的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。

### <a name="wsl"></a>WSL
* 修正組建18272中引進的「不支援這類介面」錯誤 [GH 3645]
* 忽略 umount syscall 的 MNT_FORCE 旗標 [GH 3605]
* 切換 WSL interop 以使用官方 CreatePseudoConsole API
* FUTEX_WAIT 重新開機時維持無超時值

## <a name="build-18272"></a>組建18272
如需組建18272的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。

### <a name="wsl"></a>WSL
* **WARNING**此組建中的問題導致 WSL 無法運作。 嘗試啟動您的散發套件時, 您會看到「不支援這種介面」錯誤。 已修正此問題, 並將于下一周的 Insider 快速組建中提供。 如果您已安裝此組建, 您可以使用 [設定] 中的 [回到先前的 Windows 10 版本] 復原到先前的 Windows 組建, > 更新 & 安全性 > 復原。

## <a name="build-18267"></a>組建18267
如需組建18267的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。

### <a name="wsl"></a>WSL
* 修正無法 reaped 或無限期地維持廢止進程的問題。
* 如果錯誤訊息超過最大長度 [GH 3592], WslRegisterDistribution 就會停止回應
* 允許 fsync 在 DrvFs 上成功執行唯讀檔案 [GH 3556]
* 在 [GH 3584] 內建立符號連結之前, 請先確認/bin 和/sbin 目錄是否存在
* 已新增 WSL 實例的實例終止超時機制。 Timeout 目前設定為15秒, 表示實例會在最後一個 WSL 進程結束後的15秒後終止。 若要立即終止散發, 請使用:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>組建 17763 (1809)
如需組建17763的一般 Windows 資訊, 請造訪[windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 許可權檢查太嚴格, 無法變更相同的執行緒優先順序 [GH 1838]
* 確保開機時間使用非偏誤停機時間, 以避免傳回 clock_gettime (CLOCK_BOOTTIME) [GH 3434] 的負值
* 在 WSL binfmt 解譯器中處理符號連結 [GH 3424]
* 較佳的 threadgroup 領導者檔案描述項清除處理。
* 將 WSL 切換為使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter, 以避免溢位 [GH 3252]
* Ptrace attach 可能會造成系統呼叫的錯誤傳回值 [GH 1731]
* 修正數個 AF_UNIX 相關問題 [GH 3371]
* 修正當目前的工作目錄長度少於5個字元時, 可能導致 WSL interop 失敗的問題 [GH 3379]
* 避免一秒延遲失敗的回送連線到不存在的埠 [GH 3286]
* 新增/proc/sys/fs/file-max stub 檔案 [GH 2893]
* 更精確的 IPV6 領域資訊。
* PR_SET_PTRACER 支援 [GH 3053]
* 管道檔案系統不小心清除邊緣觸發的 epoll 事件 [GH 3276]
* 透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]
* 改良的僵支援 [GH 1353]
* 新增用於控制 Windows interop 行為的 wsl 專案 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]
* 新增對 TIOCSTI 的支援 [GH 1863]
* 連接過程中的非封鎖通訊端應該會傳回 EAGAIN 進行寫入嘗試 [GH 2846]
* 支援掛接的 Vhd 上的 interop [GH 3246, 3291]
* 修正根資料夾 [GH 3304] 的許可權檢查問題
* 對 TTY 鍵盤 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的支援有限。
* 即使是在背景中啟動, Windows UI 應用程式也應該執行。
* 新增 wsl-u 或--user 選項 [GH 1203]
* 修正啟用快速啟動時的 WSL 啟動問題 [GH 2576]
* Unix 通訊端需要保留中斷連線的對等認證 [GH 3183]
* 非封鎖的 Unix 通訊端使用 EAGAIN 無限期失敗 [GH 3191]
* case = off 是新的預設 drvfs 掛接類型 [GH 2937, 3212, 3328]
    * 如需詳細資訊, 請參閱[blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 。
* 新增 wslconfig/terminate 以停止執行散發套件。
* 修正未正確處理具有空格之路徑的 WSL shell 內容功能表項目問題。
* 以擴充屬性的形式公開每個目錄的區分大小寫
* ARM64模擬快取維護作業。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。
* DrvFs: 僅 unescape 與逸出字元對應之私用範圍中的字元。
* 修正 ELF parser 解譯器長度驗證中的逐一錯誤 [GH 3154]
* WSL 過去時間的絕對計時器不會引發 [GH 3091]
* 確保新建立的重新分析點在上層目錄中列為。
* 以原子方式在 DrvFs 中建立區分大小寫的目錄。
* 已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的其他問題。 [GH 2712]
* 已修正啟用 UMCI 時的 WSL 啟動失敗。 [GH 3020]
* [新增 explorer] 操作功能表以啟動 WSL [GH 437, 603, 1836]。 若要使用, 請按住 shift 鍵, 並在 explorer 視窗中按一下滑鼠右鍵。
* 修正 Unix 通訊端未封鎖的行為 [GH 2822, 3100]
* 修正 GH 2026 中所報告的懸掛 NETLINK 命令。
* 新增對掛接傳播旗標的支援 [GH 2911]。
* 修正不會造成 inotifypropertychanged 事件的截斷問題 [GH 2978]。
* Add--wsl 的 exec 選項, 可在不使用 shell 的情況下叫用單一二進位檔。
* 新增--wsl 的散發選項, 以選取特定的散發版本。
* 有限的 dmesg 支援。 應用程式現在可以登入 dmesg。 WSL 驅動程式會將有限的資訊記錄到 dmesg。 未來, 您可以擴充此功能, 以從驅動程式中攜帶其他資訊/診斷。
    * 注意: 目前透過`/dev/kmsg`裝置介面支援 dmesg。 `syslog`尚不支援 syscall 介面。 因此, 某些`dmesg`命令列選項`-S`(例如) `-C`無法使用。
* 變更序列裝置的預設 gid 和模式以符合原生 [GH 3042]
* DrvFs 現在支援擴充屬性。
    * 注意:DrvFs 在擴充屬性的名稱上有一些限制。 不允許某些字元 (例如 '/'、': '\*和 ' '), 而且擴充屬性名稱在 DrvFs 上不區分大小寫

## <a name="build-18252-skip-ahead"></a>組建 18252 (向前跳過)
如需組建18252的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。

### <a name="wsl"></a>WSL
* 將 init 和 bsdtar 二進位檔從 lxssmanager dll 移到另一個工具資料夾
* 修正使用 CLONE_FILES 時有關關閉檔案描述項的競爭
* 轉換 DrvFs 路徑時, 處理/proc/pid/mountinfo 中的選擇性欄位
* 允許 DrvFs mknod 成功, 但不支援 S_IFREG 的中繼資料
* 在 DrvFs 上建立的 readonly 檔案應具有 readonly 屬性集 [GH 3411]
* 新增/sbin/mount.drvfs helper 以處理 DrvFs 裝載
* 在 DrvFs 中使用 POSIX rename。
* 允許磁片區上沒有磁片區 GUID 的路徑轉譯。

## <a name="build-17738-fast"></a>組建 17738 (快速)
如需組建17738的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 許可權檢查太嚴格, 無法變更相同的執行緒優先順序 [GH 1838]
* 確保開機時間使用非偏誤停機時間, 以避免傳回 clock_gettime (CLOCK_BOOTTIME) [GH 3434] 的負值
* 在 WSL binfmt 解譯器中處理符號連結 [GH 3424]
* 較佳的 threadgroup 領導者檔案描述項清除處理。

## <a name="build-17728-fast"></a>組建 17728 (快速)
如需組建17728的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。

### <a name="wsl"></a>WSL
* 將 WSL 切換為使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter, 以避免溢位 [GH 3252]
* Ptrace attach 可能會造成系統呼叫的錯誤傳回值 [GH 1731]
* 修正一些 AF_UNIX 相關問題 [GH 3371]
* 修正當目前的工作目錄長度少於5個字元時, 可能導致 WSL interop 失敗的問題 [GH 3379]

## <a name="build-18204-skip-ahead"></a>組建 18204 (向前跳過)
如需組建18204的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 管道檔案系統 inadvertenly 清除邊緣觸發的 epoll 事件 [GH 3276]
* 透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]

## <a name="build-17723-fast"></a>組建 17723 (快速)
如需組建17723的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 避免一秒延遲失敗的回送連線到不存在的埠 [GH 3286]
* 新增/proc/sys/fs/file-max stub 檔案 [GH 2893]
* 更精確的 IPV6 領域資訊。
* PR_SET_PTRACER 支援 [GH 3053]
* 管道檔案系統 inadvertenly 清除邊緣觸發的 epoll 事件 [GH 3276]
* 透過 NTFS 符號啟動的 Win32 可執行檔不遵守符號名稱 [GH 2909]

## <a name="build-17713"></a>組建17713
如需組建17713的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。

### <a name="wsl"></a>WSL
* 改良的僵支援 [GH 1353]
* 新增用於控制 Windows interop 行為的 wsl 專案 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]
* 新增對 TIOCSTI 的支援 [GH 1863]
* 連接過程中的非封鎖通訊端應該會傳回 EAGAIN 進行寫入嘗試 [GH 2846]
* 支援掛接的 Vhd 上的 interop [GH 3246, 3291]
* 修正根資料夾 [GH 3304] 的許可權檢查問題
* 對 TTY 鍵盤 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的支援有限。
* 即使是在背景中啟動, Windows UI 應用程式也應該執行。

## <a name="build-17704"></a>組建17704
如需組建17704的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。

### <a name="wsl"></a>WSL
* 新增 wsl-u 或--user 選項 [GH 1203]
* 修正啟用快速啟動時的 WSL 啟動問題 [GH 2576]
* Unix 通訊端需要保留中斷連線的對等認證 [GH 3183]
* 非封鎖的 Unix 通訊端使用 EAGAIN 無限期失敗 [GH 3191]
* case = off 是新的預設 drvfs 掛接類型 [GH 2937, 3212, 3328]
    * 如需詳細資訊, 請參閱[blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) 。
* 新增 wslconfig/terminate 以停止執行散發套件。

## <a name="build-17692"></a>組建 17692
如需組建17692的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。

### <a name="wsl"></a>WSL
* 修正未正確處理具有空格之路徑的 WSL shell 內容功能表項目問題。
* 以擴充屬性的形式公開每個目錄的區分大小寫
* ARM64模擬快取維護作業。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。
* DrvFs: 僅 unescape 與逸出字元對應之私用範圍中的字元。

## <a name="build-17686"></a>組建 17686
如需組建17686的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。

### <a name="wsl"></a>WSL
* 修正 ELF parser 解譯器長度驗證中的逐一錯誤 [GH 3154]
* WSL 過去時間的絕對計時器不會引發 [GH 3091]
* 確保新建立的重新分析點在上層目錄中列為。
* 以原子方式在 DrvFs 中建立區分大小寫的目錄。

## <a name="build-17677"></a>組建17677
如需組建17677的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。

### <a name="wsl"></a>WSL
* 已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的其他問題。 [GH 2712]
* 已修正啟用 UMCI 時的 WSL 啟動失敗。 [GH 3020]

## <a name="build-17666"></a>組建17666
如需組建17666的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告：有一個問題導致 WSL 無法在某些 AMD 晶片組上執行 [GH 3134]。 修正已準備就緒, 可對 Insider Build 分支進行。
* [新增 explorer] 操作功能表以啟動 WSL [GH 437, 603, 1836]。 在 explorer 視窗中, 使用按住 shift 並以滑鼠右鍵按一下。
* 修正 unix 通訊端未封鎖的行為 [GH 2822, 3100]
* 修正 GH 2026 中所報告的懸掛 NETLINK 命令。
* 新增對掛接傳播旗標的支援 [GH 2911]。
* 修正不會造成 inotifypropertychanged 事件的截斷問題 [GH 2978]。
* Add--wsl 的 exec 選項, 可在不使用 shell 的情況下叫用單一二進位檔。
* 新增--wsl 的散發選項, 以選取特定的散發版本。

## <a name="build-17655-skip-ahead"></a>組建 17655 (向前跳過)
如需組建17655的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 有限的 dmesg 支援。 應用程式現在可以登入 dmesg。 WSL 驅動程式會將有限的資訊記錄到 dmesg。 未來, 您可以擴充此功能, 以從驅動程式中攜帶其他資訊/診斷。
    * 注意: 目前透過`/dev/kmsg`裝置介面支援 dmesg。 `syslog`尚不支援 sycall 介面。 因此, 某些`dmesg`命令列選項`-S`(例如) `-C`無法使用。
* 已修正即使檔案存在, 多執行緒作業還是會傳回 ENOENT 的問題。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>組建 17639 (向前跳過)
如需組建17639的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 變更序列裝置的預設 gid 和模式以符合原生 [GH 3042]
* DrvFs 現在支援擴充屬性。
    * 注意:DrvFs 在擴充屬性的名稱上有一些限制。 特別的是, 不允許某些字元 (例如 '/'、':\*' 和 ' '), 而且擴充屬性名稱在 DrvFs 上不區分大小寫。

## <a name="build-17133-fast"></a>組建 17133 (快速)
如需組建17133的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。

### <a name="wsl"></a>WSL
* 修正 WSL 中的停止回應。 [GH 3039, 3034]

## <a name="build-17128-fast"></a>組建 17128 (快速)
如需組建17128的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。

### <a name="wsl"></a>WSL
* None

## <a name="build-17627-skip-ahead"></a>組建 17627 (向前跳過)
如需組建17627的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 新增對 futex pi 感知作業的支援。 [GH 1006]
    * 請注意, 優先順序目前不是支援的 WSL 功能, 因此有一些限制, 但應該解除封鎖標準使用方式。
* 適用于 WSL 進程的 Windows 防火牆支援。 [GH 1852]
    * 例如, 若要允許 WSL python 進程在任何埠上接聽, 請使用提升許可權的 Windows cmd:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 如需如何新增防火牆規則的其他詳細資料, 請參閱[連結](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* 使用 wsl 時, 請遵循使用者的預設 shell。 [GH 2372]
* 將所有網路介面報告為 ethernet。 [GH 2996]
* 更好的處理損毀的/etc/passwd 檔案。 [GH 3001]

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17618-skip-ahead"></a>組建 17618 (向前跳過)
如需組建17618的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。

### <a name="wsl"></a>WSL
* 引進 NT interop 的 pseudoconsole 功能 [GH 988、1366、1433、1542、2370、2406]。
* 舊版安裝機制 (lxrun) 已被取代。 安裝發行版本的支援機制是透過 Microsoft Store。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17110"></a>組建 17110
如需組建17110的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。

### <a name="wsl"></a>WSL
* 允許從 Windows 終止/init [GH 2928]。
* 根據預設, DrvFs 現在會使用每個目錄的區分大小寫 (相當於 "case = dir" 掛接選項)。
    * 使用 "case = force" (舊行為) 需要設定登錄機碼。 執行下列命令, 以在您需要使用「案例 = 強制」時啟用它: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * 如果您在舊版 Windows 中使用 WSL 建立的現有目錄需要區分大小寫, 請使用 fsutil 將它們標示為區分大小寫: fsutil file setcasesensitiveinfo <path> enable
* 從 uname syscall 傳回的 Null 終止字串。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17107"></a>組建17107
如需組建17107的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。

### <a name="wsl"></a>WSL
* 支援主要 pty 端點上的 TCSETSF 和 TCSETSW [GH 2552]。
* 啟動同步 interop 進程可能會導致 EINVAL [GH 2813]。
* 修正 PTRACE_ATTACH 以在/proc/pid/status. 中顯示適當的追蹤狀態
* 修正使用 CLEARTID 和 SETTID 旗標複製短期進程的競爭情形, 而不需要清除 TID 位址即可結束。
* 從17093前版本的組建進行升級時, 顯示一則訊息。 如需17093檔案系統變更的詳細資料, 請參閱[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)版的版本資訊。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17101"></a>組建17101
如需組建17101的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。

### <a name="wsl"></a>WSL
* 支援 signalfd。 [GH 129]
* 支援包含不合法 NTFS 字元的檔案名, 方法是將它們編碼為私用 Unicode 字元。 [GH 1514]
* 當不支援寫入時, 自動掛接將會回復為唯讀。 [GH 2603]
* 允許貼上 Unicode 代理配對 (如表情字元)。 [GH 2765]
* /Proc 和/sys 中的虛擬檔案應該會從 select、輪詢、epoll、et al 傳回讀取和寫入準備就緒。 [GH 2838]
* 修正可能導致服務在登錄遭篡改或損毀時進入無限迴圈的問題。
* 修正 netlink 訊息, 以使用較新的 (上游 4.14) 版本的 iproute2。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17093"></a>組建17093
如需組建17093的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。

#### <a name="important"></a>重要事項：
升級至這個組建之後, 第一次啟動 WSL 時, 它需要執行一些工作來升級 Linux 檔案系統目錄。 這可能需要幾分鐘的時間, 因此 WSL 的啟動速度可能會變慢。 這應該只會針對您從存放區安裝的每個發佈執行一次。
* 改善 DrvFs 中的區分大小寫支援。
    * DrvFs 現在支援每個目錄區分大小寫。 這是可以在目錄上設定的新旗標, 以指出這些目錄中的所有作業都應該視為區分大小寫, 這可讓 Windows 應用程式能夠正確開啟只有大小寫不同的檔案。
    * DrvFs 有新的掛接選項, 可控制以每個目錄為基礎的區分大小寫
        * case = force: 將所有目錄視為區分大小寫 (磁片磁碟機根目錄除外)。 使用 WSL 建立的新目錄會標示為區分大小寫。 這是舊版的行為, 但會將新的目錄標記為區分大小寫。
        * case = dir: 只有具有每個目錄的區分大小寫旗標的目錄會被視為區分大小寫;其他目錄則不區分大小寫。 使用 WSL 建立的新目錄會標示為區分大小寫。
        * 案例 = 關閉: 只有具有每個目錄區分大小寫旗標的目錄會被視為區分大小寫;其他目錄則不區分大小寫。 使用 WSL 建立的新目錄會標示為不區分大小寫。
    * 注意: 在舊版中, WSL 所建立的目錄並不會設定此旗標, 因此如果您使用 "case = dir" 選項, 則不會將其視為區分大小寫。 即將推出在現有目錄上設定此旗標的方法。
    * 使用這些選項掛接的範例 (針對現有的磁片磁碟機, 您必須先卸載, 才可以使用不同的選項進行掛接): sudo mount-t drvfs C:/mnt/c-o case = dir
    * 目前, case = force 仍然是預設選項。 未來將會變更為案例 = dir。
* 在裝載 DrvFs 時, 您現在可以在 Windows 路徑中使用正斜線, 例如: sudo mount-t DrvFs//server/share/mnt/share
* WSL 現在會在實例開始 [GH 2636] 期間處理/etc/fstab 檔案。
    * 這會在自動掛接 DrvFs 磁片磁碟機之前完成。fstab 已掛接的任何磁片磁碟機將不會自動重新掛接, 可讓您變更特定磁片磁碟機的掛接點。
    * 您可以使用 wsl 來關閉此行為。
* /Proc 中的 mount、mountinfo 和 mountstats 檔案會適當地轉義特殊字元, 例如反斜線和空格 [GH 2799]
* 在啟用中繼資料時, 使用 DrvFs 建立的特殊檔案 (例如 WSL 符號連結, 或 fifos 和通訊端), 現在可以從 Windows 複製和移動。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL 可透過 WSL 更容易設定
我們新增了一種方法, 讓您在每次啟動子系統時, 自動設定 WSL 中的特定功能。 這包括自動掛接選項和網路設定。 在我們的 blog 文章中深入瞭解它, 網址為: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX 允許 WSL 和 Windows 原生進程上 Linux 進程之間的通訊端連線
WSL 和 Windows 應用程式現在可以透過 Unix 通訊端彼此通訊。 假設您想要在 Windows 中執行服務, 並讓 Windows 和 WSL 應用程式都能使用它。 現在, 您可以使用 Unix 通訊端來做到這一點。 在我們的 blog 文章中閱讀更多資訊, 網址為 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* 支援 mmap () 與 MAP_NORESERVE [GH 121, 2784]
* 支援 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121, 2781]
* 處理複製中的非 SIGCHLD 終止信號 [GH 121, 2781]
* Stub/proc/sys/fs/inotify/max_user_instances 和/proc/sys/fs/inotify/max_user_watches [GH 1705]
* 載入包含具有非零位移之載入標頭的 ELF 二進位檔時發生錯誤 [GH 1884]
* 載入影像時, 有零的尾端分頁位元組。
* 減少 execve 以無訊息方式終止進程的情況

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17083"></a>組建 17083
如需組建17083的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。

### <a name="wsl"></a>WSL
* 已修正與 epoll 相關的錯誤檢查 [GH 2798, 2801, 2857]
* 已修正關閉 ASLR 時的停止回應 [GH 1185, 2870]
* 確保 mmap 作業看起來不可部分完成 [GH 2732]

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17074"></a>組建17074
如需組建17074的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。

### <a name="wsl"></a>WSL
* 已修正 DrvFs 中繼資料的儲存格式 [GH 2777] </br>
**重要事項：** 在此組建之前建立的 DrvFs 中繼資料將不會正確地顯示, 或根本不會出現。 若要修正受影響的檔案, 請使用 chmod 和 chown 來重新套用中繼資料。
* 已修正多個信號和可重新開機 syscalls 的問題。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17063"></a>組建17063
如需組建17063的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。

### <a name="wsl"></a>WSL
* DrvFs 支援其他 Linux 中繼資料。 這可讓您使用 chmod/chown 來設定檔案的擁有者和模式, 以及建立特殊檔案 (例如 fifos、unix 通訊端和裝置檔案)。 預設會停用這項功能, 因為它仍然是實驗性。
**注意：** 我們已修正 DrvFs 所使用之元資料格式的 bug。 雖然中繼資料適用于實驗的此組建, 但未來的組建將無法正確讀取此組建所建立的中繼資料。  您可能需要手動更新已修改檔案的擁有者, 而且必須重新建立具有自訂裝置識別碼的裝置。

  若要啟用, 請使用中繼資料選項掛接 DrvFs (若要在現有的掛接上啟用, 您必須先將它卸載):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 許可權會當做額外的中繼資料新增至檔案;它們不會影響 Windows 許可權。  請記住, 使用 Windows 編輯器編輯檔案可能會移除中繼資料。 在此情況下, 檔案將會還原為其預設許可權。

* 已將掛接選項新增至 DrvFs, 以控制沒有中繼資料的檔案。
  * uid: 用於所有檔案之擁有者的使用者識別碼。
  * gid: 用於所有檔案之擁有者的群組識別碼。
  * umask: 要針對所有檔案和目錄排除的八進位遮罩許可權。
  * fmask: 要針對所有一般檔案排除的八進位遮罩許可權。
  * dmask: 要針對所有目錄排除的八進位遮罩許可權。

  例如:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  結合中繼資料選項來指定沒有中繼資料之檔案的預設許可權。

* 引進新的環境變數, `WSLENV`以設定環境變數在 WSL 與 Win32 之間的流動方式。

  例如:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`這是以冒號分隔的環境變數清單, 可在從 WSL 啟動 Win32 或 Win32 進程中的 WSL 進程時包含。  每個變數都可以加上斜線, 後面接著旗標, 以指定翻譯的方式。
  * p&id此值是應該在 WSL 路徑和 Win32 路徑之間轉譯的路徑。
  * l值是路徑的清單。 在 WSL 中, 它是以冒號分隔的清單。 在 Win32 中, 它是以分號分隔的清單。
  * 那麼從 Win32 叫用 WSL 時, 應該只包含此值
  * 寬從 WSL 叫用 Win32 時, 應該只包含此值

  您可以在`WSLENV` .bashrc 或在自訂 Windows 環境中, 為您的使用者設定。

* drvfs 裝載會正確保留 tar、cp-p 的時間戳記 (GH 1939)
* drvfs 符號連結報告正確的大小 (GH 2641)
* 讀取/寫入適用于非常大的 IO 大小 (GH 2653)
* waitpid 適用于進程群組識別碼 (GH 2534)
* 大幅改善大型保留區域的 mmap 效能;改善 ghc 效能 (GH 1671)
* 特性支援 READ_IMPLIES_EXEC;修正 maxima 和 clisp (GH 1185)
* mprotect 支援 PROT_GROWSDOWN;修正 clisp (GH 1128)
* 過量使用模式中的分頁錯誤修正;修正 sbcl (GH 1128)
* 複製支援更多旗標組合
* 支援 epoll 檔案的 select/epoll (先前為無 op)。
* 通知 ptrace 未實現的 syscalls。
* 忽略產生 resolv.conf 時未啟動的介面 [GH 2694]
* 列舉沒有實體位址的網路介面。 [GH 2685]
* 其他錯誤修正和改善。

### <a name="linux-tools-available-to-developers-on-windows"></a>適用于 Windows 開發人員的 Linux 工具

* Windows 命令列工具鏈包括 bsdtar (tar) 和捲曲。
  閱讀[這篇 blog](https://aka.ms/tarcurlwindows)以深入瞭解如何新增這兩項新工具, 並查看其如何塑造 Windows 上的開發人員經驗。

*   `AF_UNIX`可在 Windows 測試人員 SDK (17061 +) 中取得。
  閱讀[這篇 blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)以深入瞭解`AF_UNIX` , 以及 Windows 上的開發人員可以如何使用它。

### <a name="console"></a>Console
* 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。


## <a name="build-17046"></a>組建17046

如需組建17046的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。

### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 允許進程在沒有使用中的終端機的情況下執行。 [GH 709, 1007, 1511, 2252, 2391, et al。]
- 更好的 CLONE_VFORK 和 CLONE_VM 支援。 [GH 1878, 2615]
- 略過 WSL 網路作業的 TDI 篩選器驅動程式。 [GH 1554]
- DrvFs 會在符合特定條件時建立 NT 符號連結。 [GH 353, 1475, 2602]
    - 連結目標必須是相對的, 而且不能跨越任何掛接點或符號連結, 而且必須存在。
    - 除非已開啟開發人員模式, 否則使用者必須具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (這通常會要求您啟動 wsl 提升許可權)。
    - 在所有其他情況下, DrvFs 仍然會建立 WSL 符號連結。
- 允許同時執行提高許可權和未提高許可權的 WSL 實例。
- 支援/proc/sys/kernel/yama/ptrace_scope
- 新增 wslpath 以執行 WSL <-> Windows 路徑轉換。 [GH 522、1243、1834、2327、et al。]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- 沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。


## <a name="build-17040"></a>組建17040

如需組建17040的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 17035之後沒有任何修正。

#### <a name="console"></a>Console
- 17035之後沒有任何修正。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17035"></a>組建17035

如需組建17035的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 在 DrvFs 上存取檔案時, 偶爾會發生 EINVAL 失敗。 [GH 2448]

#### <a name="console"></a>Console
- 在 VT 模式下插入/刪除線條時, 某些色彩會遺失。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17025"></a>組建17025

如需組建17025的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 在新的前景進程群組中啟動初始進程 [GH 1653, 2510]。
- SIGHUP 傳遞修正 [GH 2496]。
- 如果未提供 [GH 2497], 則產生預設虛擬橋接器名稱。
- 執行/proc/sys/kernel/random/boot_id [GH 2518]。
- 更多 interop stdout/stderr 管線修正。
- 存根 syncfs 系統呼叫。

#### <a name="console"></a>Console
- 修正協力廠商主控台的輸入 VT 轉譯 [GH 111]

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="build-17017"></a>組建17017

如需組建17017的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 忽略空的 ELF 程式標頭 [GH 330]。
- 允許 LxssManager 建立非互動式使用者的 WSL 實例 (ssh 和排程的工作支援) [GH 777, 1602]。
- 支援 WSL-> Win32 > WSL (「開始」) 案例 [GH 1228]。
- 限制終止透過 interop [GH 1614] 叫用的主控台應用程式。
- 支援 devpts 的掛接選項 [GH 1948]。
- Ptrace 封鎖子啟動 [GH 2333]。
- EPOLLET 遺漏某些事件 [GH 2462]。
- 傳回 PTRACE_GETSIGINFO 的更多資料。
- 具有 lseek 的 Getdents 會提供不正確的結果。
- 修正某些 Win32 interop 應用程式當機, 等候沒有其他資料的管道上的輸入。
- O_ASYNC 對 tty/pty 檔案的支援。
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
正在進行測試。

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>組建16288

如需組建16288的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 正確初始化和報告通訊端檔案描述項的 uid、gid 和模式 [GH 2490]
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
自16273開始沒有任何變更

## <a name="build-16278"></a>組建16278

如需組建162738的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 卸載 LX MM 狀態時, 明確取消對應檔案支援區段的對應視圖 [GH 2415]
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
自16273開始沒有任何變更

## <a name="build-16275"></a>組建16275

如需組建162735的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 此版本中沒有任何 WSL 相關的變更。

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
自16273開始沒有任何變更

## <a name="build-16273"></a>組建16273

如需組建16273的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 已修正 DrvFs 有時會回報錯誤的目錄檔案類型 [GH 2392] 的問題
- 允許建立 NETLINK_KOBJECT_UEVENT 通訊端來解除封鎖使用 UEVENT 的程式 [GH 1121、2293、2242、2295、2235、648、637]
- 新增對非封鎖型連接的支援 [GH 903、1391、1584、1585、1829、2290、2314]
- 執行 CLONE_FS 複製系統呼叫旗標 [GH 2242]
- 修正不會在 NT interop 中正確處理索引標籤或引號的問題 [GH 1625, 2164]
- 解決嘗試重新開機 WSL 實例時發生的拒絕存取錯誤 [GH 651, 2095]
- 執行 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 作業 [GH 2242]
- 修正各種 SysFs 檔案的許可權 [GH 2214]
- 修正安裝期間的 Haskell 堆疊停止回應 [GH 2290]
- 執行 binfmt_misc ' C ' ' O ' 與 ' P ' 旗標 [GH 2103]
- 新增/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]
- 新增 ioprio_set 系統呼叫的部分支援 [GH 498]
- 存根 SO_REUSEPORT & 新增 netlink 通訊端的 SO_PASSCRED 支援 [GH 69]
- 如果目前正在安裝或卸載散發, 則會從 RegisterDistribuiton 傳回不同的錯誤碼。
- 允許透過 wslconfig 取消註冊部分安裝的 WSL 散發套件
- 從 udp:: msg_peek 修正 python 通訊端測試停止回應
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
測試總計:1904<br/>
已略過的測試總數:209<br/>
失敗總計:229<br/>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>組建 16257

如需組建16257的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 執行 prlimit64 系統呼叫
- 新增對 ulimit 的支援-n (setrlimit RLIMIT_NOFILE) [GH 1688]
- TCP 通訊端的存根 MSG_MORE [GH 2351]
- 修正不正確 AT_EXECFN 輔助向量行為 [GH 2133]
- 修正主控台/tty 的複製/貼上行為, 並新增更好的完整緩衝區處理 [GH 2204, 2131]
- 設定 AT_SECURE 在輔助向量中用於設定使用者識別碼和設定群組識別碼程式 [GH 2031]
- 虛擬-終端機主要端點未處理 TIOCPGRP [GH 1063]
- 修正 lseek 在 LxFs 中倒轉目錄 [GH 2310]
- /dev/ptmx 在高使用量之後鎖定 [GH 1882]
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 修正所有位置的水平線/底線 [GH 2168]
- 修正程式順序變更, 使 NPM 難以關閉 [GH 2170]
- 已新增新的色彩配置: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 結果:
自16251開始沒有任何變更

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`prlimit64`<br/>

### <a name="known-issues"></a>已知問題
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub 問題 2392:WSL 無法辨識的 Windows 資料夾 .。。](https://github.com/Microsoft/BashOnWindows/issues/2392)
在組建16257中, WSL 在透過列舉 Windows 檔案/資料夾`/mnt/c/...`時發生問題。
此問題已獲得修正, 應在一周開始8/14/2017 期間, 于內部人員組建中發行。

<br/>

## <a name="build-16251"></a>組建16251

如需組建16251的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 從 WSL 選用元件移除 Beta 標記, 如需詳細資訊, 請參閱[blog 文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。
- 在 exec [GH 962, 1415, 2072] 上正確初始化已儲存集的 uid 和 gid, 用於設定使用者識別碼和集合群組識別碼二進位檔
- 已新增對 ptrace PTRACE_O_TRACEEXIT 的支援 [GH 555]
- 已新增使用 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支援 [GH 555]
- 已修正 ptrace 以停止忽略的信號
- 其他改良功能和 bug 修正

#### <a name="console"></a>Console
- 此版本中沒有任何與主控台相關的變更。

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:768</br>
失敗的測試數目:244</br>
略過的測試數目:96</br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>組建16241

如需組建16241的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 此版本中沒有任何 WSL 相關的變更。

#### <a name="console"></a>Console
- 修正輸出中的跨行不正確的字元, 原先在[此](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)報告
- 修正字碼頁 65001 (utf8) 中沒有顯示的輸出文字
- 在選取範圍變更時, 請勿將對某個色彩的 RGB 值所做的變更傳送到調色板的其他部分。 這會讓主控台屬性工作表的使用變得更容易。
- Ctrl + S 似乎無法正常運作
- ANSI 轉義碼中的非粗體/-Dim 完全不存在 [GH 2174]
- 主控台未正確支援 Vim 色彩主題 [GH 1706]
- 無法貼上特定字元 [GH 2149]
- 重新調整大小會互動奇怪, 並在編輯/命令列上有內容時調整 bash 視窗的大小 [GH ConEmu 1123]
- Ctrl-L 讓螢幕保持不變 [GH 1978]
- 在 HDPI 上顯示 VT 時的主控台呈現錯誤 [GH 1907]
- Unicode 字元 U + 30FB 的 Japansese 字元看起來很奇怪 [GH 2146]
- 其他改良功能和 bug 修正

</br>

## <a name="build-16237"></a>組建 16237

如需組建16237的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。<br/>


### <a name="fixed"></a>固定式
- 在 lxfs 中使用不含 EAs 的檔案的預設屬性 (root、root、0000)
- 已新增使用擴充屬性之散發的支援
- 修正 getdents 和 getdents64 所傳回之專案的填補
- 修正 shmctl SHM_STAT 系統呼叫的許可權檢查 [GH 2068]
- 已修正 ttys 的初始 epoll 狀態不正確 [GH 2231]
- 修正 DrvFs readdir 未傳回所有專案 [GH 2077]
- 修正檔案未連結時的 LxFs readdir [GH 2077]
- 允許透過 procfs 重新開啟未連結的 drvfs 檔案
- 已新增用來停用 WSL 功能的全域登錄機碼覆寫 (interop/磁片磁碟機裝載)
- 針對 DrvFs (和 LxFs) 的 "stat" 修正不正確的區塊計數 [GH 1894]
- 其他改良功能和 bug 修正

</br>

## <a name="build-16232"></a>組建16232

如需組建16232的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 此版本中沒有任何 WSL 相關的變更。

</br>

## <a name="build-16226"></a>組建16226

如需組建16226的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。<br/>


### <a name="fixed"></a>固定式
- xattr 相關的 syscalls 支援 (getxattr、setxattr、listxattr、removexattr)。
- capablity xattr 支援。
- 改善與特定檔案系統和篩選器的相容性, 包括非 MS SMB 伺服器。 [GH #1952]
- 改善對 OneDrive 預留位置、GVFS 預留位置和 Compact OS 壓縮檔的支援。
- 其他改良功能和 bug 修正

</br>

## <a name="build-16215"></a>組建16215

如需組建16215的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。<br/>


### <a name="fixed"></a>固定式
- WSL 不再需要開發人員模式。
- 支援 drvfs 中的目錄聯接。
- 處理 WSL 散發 appx 套件的卸載。
- 更新 procfs 以顯示私用和共用對應。
- 新增 wslconfig 的功能, 以清除部分安裝或卸載的散發套件。
- 已針對 TCP 通訊端新增 IP_MTU_DISCOVER 的支援。 [GH 1639, 2115, 2205]
- 推斷通訊協定系列以取得 AF_INADDR 的路由。
- 序列裝置改善 [GH 1929]。

</br>

## <a name="build-16199"></a>組建16199

如需組建16199的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 這些版本中沒有任何 WSL 相關的變更。

</br>

## <a name="build-16193"></a>組建16193

如需組建16193的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 傳送 SIGCONT 與 threadgroup 終止之間的競爭條件 [GH 1973]
- 將 tty 和 pty 裝置變更為報告 FILE_DEVICE_NAMED_PIPE, 而不是 FILE_DEVICE_CONSOLE [GH 1840]
- IP_OPTIONS 的 SSH 修正
- 已將 DrvFs 裝載移至 init daemon [GH 1862, 1968, 1767, 1933]
- 已在 DrvFs 中新增下列 NT 符號連結的支援。

</br>

## <a name="build-16184"></a>組建16184

如需組建16184的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 已移除 apt 套件維護工作 (lxrun .exe/update)
- 已修正的輸出不會顯示在 node.js 中的 Windows 進程 [GH 1840]
- 放寬 lxcore 中的對齊需求 [GH 1794]
- 已修正系統呼叫推中的 AT_EMPTY_PATH 旗標處理。
- 已修正使用開啟的控制碼刪除 DrvFs 檔案將導致檔案出現未定義的行為 [GH 544、966、1357、1535、1615] 的問題
- /etc/hosts 現在會繼承 Windows hosts 檔案中的專案 (%windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>組建16179

如需組建16179的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 本周沒有任何 WSL 變更。

</br>

## <a name="build-16176"></a>組建16176

如需組建16176的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。<br/>


### <a name="fixed"></a>固定式

- [啟用的序列支援](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 已新增 IP 通訊端選項 IP_OPTIONS [GH 1116]
- 實 pwritev 函式 (在上傳檔案至 nginx/PHP-FPM) [GH 1506]
- 已新增 IP 通訊端選項 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- 支援通訊端選項 IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- 已新增適用于應用程式節點、追蹤路由、發掘、nslookup、主機的 IP (V6) _MTU 通訊端選項
- 已新增 IP 通訊端選項 IPV6_UNICAST_HOPS
- [檔案系統改良功能](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * 允許裝載 UNC 路徑
    * 在 drvfs 中啟用 CDFS.SYS 支援
    * 在 drvfs 中正確處理網路檔案系統的許可權
    * 將遠端磁片磁碟機的支援新增至 drvfs
    * 在 drvfs 中啟用 FAT 支援
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果
自15042開始沒有任何變更

</br>

## <a name="build-16170"></a>組建16170

如需組建16170的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。<br/>

我們發行了新的[blog 文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), 討論我們對測試 WSL 的努力。

### <a name="fixed"></a>固定式

- 支援通訊端選項 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- 新增對 PTRACE_OLDSETOPTIONS 的支援。 [GH 1692]
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果
自15042開始沒有任何變更

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>組建15046至 Windows 10 建立者更新
尚未規劃要加入 Windows 10 的建立者更新中的 WSL 修正或功能。 WSL 的版本資訊將會在接下來的幾周內繼續, 以供下一個主要 Windows Update 的新增目標。 如需組建15046和未來 Insider 版本的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。 <br/><br/>
 <br/>

## <a name="build-15042"></a>組建15042

如需組建15042的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。<br/>


### <a name="fixed"></a>固定式

- 修正移除結尾為 "..." 的路徑時的鎖死
- 已修正 FIONBIO 未在成功時傳回0的問題 [GH 1683]
- 已修正長度為零的 inet 資料包通訊端讀取的問題
- 修正因 drvfs inode 查閱中的競爭條件而造成的可能鎖死 [GH 1675]
- 擴充對 unix 通訊端輔助資料的支援;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514, 613, 1326]
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:737</br>
非通過的數字 (失敗，所以已略過等等...):255

</br>

## <a name="build-15031"></a>組建15031

如需組建15031的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。<br/>


### <a name="fixed"></a>固定式

- 已修正時間 (2) 偶爾會行為失常的錯誤。
- 已修正併發出 * SIGPROCMASK syscalls 可能會損毀信號遮罩的問題。
- 現在, 在 WSL 進程建立通知中傳回完整的命令列長度。 [GH 1632]
- WSL 現在會透過 ptrace 來報告執行緒結束, 以 GDB 停止回應。 [GH 1196]
- 已修正 ptys 在大量 tmux IO 後停止回應的 bug。 [GH 1358]
- 已修正許多系統呼叫中的超時驗證 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)
- 已新增 eventfd EFD_SEMAPHORE 支援 [GH 452]
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:737</br>
非通過的數字 (失敗，所以已略過等等...):255 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>組建15025

如需組建15025的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。<br/>


### <a name="fixed"></a>固定式

- 修正中斷 grep 2.27 [GH 1578] 的 bug
- Eventfd2 syscall 的實 EFD_SEMAPHORE 旗標 [GH 452]
- 實/proc/[pid]/net/ipv6_route [GH 1608]
- Unix 串流通訊端的信號驅動 IO 支援 [GH 393, 68]
- 支援 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]
- 執行 recvmmsg () syscall [GH 1531]
- 已修正 epoll_wait () 未等候的錯誤 [GH 1609]
- 執行/proc/version_signature
- 如果兩個檔案描述元都參考相同的管道, 則 t a syscall 現在會傳回失敗
- 已為 Unix 通訊端的 SO_PEERCRED 實作為正確行為
- 已修正 tkill syscall 不正確參數處理
- 增加 drvfs preformace 的變更
- Ruby IO 封鎖的次要修正
- 已修正 recvmsg () 針對 inet 通訊端的 MSG_DONTWAIT 旗標傳回 EINVAL [GH 1296]
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:732</br>
非通過的數字 (失敗，所以已略過等等...):255 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>組建15019

如需組建15019的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。<br/>


### <a name="fixed"></a>固定式

- 已修正不正確回報 procfs for htop (GH 823, 945, 971) 等工具的 CPU 使用量錯誤
- 在現有檔案上以 O_TRUNC 呼叫 open () 時, inotifypropertychanged 現在會在 IN_OPEN 之前產生 IN_MODIFY
- 修正 unix 通訊端 getsockopt SO_ERROR 以啟用 postgress [GH 61, 1354]
- 執行 GO 語言的/proc/sys/net/core/somaxconn
- Apt-取得套件更新背景工作現在會從 view 隱藏執行
- 清除 ipv6 localhost (春季 (JAVA) 失敗) 的範圍。
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:714 </br>
非通過的數字 (失敗，所以已略過等等...):249 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>組建15014

如需組建15014的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定式

- Ctrl + C 現在可如預期運作
- htop 和 ps auxw 現在會顯示正確的資源使用率 (GH #516)
- NT 例外狀況與信號的基本轉譯。 (GH #513)
- fallocate 現在會在空間用盡 (而非 EINVAL (GH #1571) 時失敗, 並出現 ENOSPC
- 已新增/proc/sys/kernel/sem。
- 執行 semop 和 semtimedop 系統呼叫
- 已修正使用 IP_RECVTOS & IPV6_RECVTCLASS 通訊端選項 (GH 69) 的 nslookup 錯誤
- 支援通訊端選項 IP_RECVTTL 和 IPV6_RECVHOPLIMIT
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:709 </br>
非通過的數字 (失敗，所以已略過等等...):255 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 摘要
總 Syscalls:384 </br>
已實行總數:235 </br>
總 Stub:22 </br>
未實現的總計:127 </br>
[詳細細目](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>組建15007

如需組建15007的一般 Windows 資訊, 請造訪[Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。<br/>


### <a name="known-issue"></a>已知問題

- 有一個已知的錯誤, 主控台無法辨識某些 Ctrl + <key>輸入。  這包括將做為一般 ' c ' 按鍵動作的 ctrl-c 命令。

  - 因應措施：將其他索引鍵對應至 Ctrl + C。 例如, 若要將 Ctrl + K 對應到 Ctrl + C, `stty intr \^k`請執行:。  這是每個終端機的對應, 必須在*每*次啟動 bash 時完成。 使用者可以流覽選項, 將此包含在其`.bashrc`

### <a name="fixed"></a>固定式

- 已更正執行 WSL 耗用 100% CPU 核心的問題
- 通訊端選項 IP_PKTINFO, 現在支援 IPV6_RECVPKTINFO。 (GH #851, 987)
- 在 lxcore 中截斷網路介面實體位址為16個位元組 (GH #1452、1414、1343、468、308)
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:709 </br>
非通過的數字 (失敗，所以已略過等等...):255 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>組建15002

如需組建15002的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。<br/>


### <a name="known-issue"></a>已知問題

兩個已知問題:
- 有一個已知的錯誤, 主控台無法辨識某些 Ctrl + <key>輸入。  這包括將做為一般 ' c ' 按鍵動作的 ctrl-c 命令。

  - 因應措施：將其他索引鍵對應至 Ctrl + C。 例如, 若要將 Ctrl + K 對應到 Ctrl + C, `stty intr \^k`請執行:。  這是每個終端機的對應, 必須在*每*次啟動 bash 時完成。 使用者可以流覽選項, 將此包含在其`.bashrc`

- 當 WSL 正在執行時, 系統執行緒會耗用 100% 的 CPU 核心。  根本原因已于內部解決和修正。

### <a name="fixed"></a>固定式

- 所有 bash 會話現在都必須在相同的許可權層級建立。  嘗試在不同層級啟動會話將會遭到封鎖。  這表示系統管理員和非系統管理員的主控台無法同時執行。 (GH #626)
<br/>
- 已執行下列 NETLINK_ROUTE 訊息 (需要 Windows 系統管理員)
     - RTM_NEWADDR (支援`ip addr add`)
     - RTM_NEWROUTE (支援`ip route add`)
     - RTM_DELADDR (支援`ip addr del`)
     - RTM_DELROUTE (支援`ip route del`)
- 針對要更新的套件, 已排程的工作檢查將不再于計量付費連線上執行 (GH #1371)
- 已修正管道停滯的錯誤, 亦即 bash-c "ls-alR/" |bash-c 「cat」 (GH #1214)
- 已執行 TCP_KEEPCNT 通訊端選項 (GH #843)
- 已實 IP_MTU_DISCOVER INET 通訊端選項 (GH #720、717、170、69)
- 已移除舊版功能, 以使用 NT 路徑查閱從 init 執行 NT 二進位檔。 (GH #1325)
- /Dev/kmsg 的修正模式, 允許群組/其他讀取權限 (0644) (GH #1321)
- 實/proc/sys/kernel/random/uuid (GH #1092)
- 已更正處理開始時間顯示為年2432的錯誤 (GH #974)
- 已將預設詞彙環境變數切換為 xterm-256color (GH #1446)
- 修改處理常式分叉期間計算進程認可的方式。 (GH #1286)
- 實/proc/sys/vm/overcommit_memory。 (GH #1286)
- 已執行的/proc/net/route 檔案 (GH #69)
- 已修正快捷方式名稱未正確當地語系化的錯誤 (GH #696)
- 已修正不正確地驗證程式標頭的 elf 剖析邏輯必須小於 (或等於) PATH_MAX。 (GH #1048)
- 已針對 procfs、sysfs、cgroupfs 和 binfmtfs 實 statfs 回呼 (GH #1378)
- 已修正不會關閉的 AptPackageIndexUpdate 視窗 (GH #1184 也會在 GH #1193 中討論)
- 已新增 ASLR 個性 ADDR_NO_RANDOMIZE 支援。 (GH #1148, 1128)
- 改善 PTRACE_GETSIGINFO (SIGSEGV), 以在 AV 期間適當的 gdb 堆疊追蹤 (GH #875)
- Patchelf 二進位檔的 Elf 剖析不會再失敗。 (GH #471)
- VPN DNS 已傳播至/etc/resolv.conf (GH #416, 1350)
- 已改善 TCP 關閉以提供更可靠的資料傳輸。 (GH #610、616、1025、1335)
- 當開啟太多檔案時, 現在會傳回正確的錯誤碼 (EMFILE)。 (GH #1126, 2090)
- Windows Audit 記錄現在會報告進程建立 Audit 中的映射名稱。
- 現在, 從 bash 視窗內啟動 bash 時, 正常地失敗
- 當 interop 無法存取 LxFs 下的工作目錄 (亦即 notepad.exe. .bashrc) 時, 新增錯誤訊息
- 已修正在 WSL 中截斷 Windows 路徑的問題
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:690 </br>
非通過的數字 (失敗，所以已略過等等...):274 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>組建14986

如需組建14986的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。<br/>


### <a name="fixed"></a>固定式

- 已修正 Netlink 和 Pty Ioctl 的錯誤檢查
- 核心版本現在會報告 4.4.0-43, 以與 Xenial 一致
- 當輸入導向 ' nul: ' (GH #1259) 時, Bash 現在會啟動
- 執行緒識別碼現在在 procfs 中正確地回報 (GH #967)
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |Inotify_add_watch () 中現在支援 IN_ISDIR 旗標 () (GH #1280)
- 執行 timer_create 和相關的系統呼叫。  這會啟用 GHC 支援 (GH #307)
- 已修正 ping 傳回 0.000 ms 時間的問題 (GH #1296)
- 開啟太多檔案時, 傳回正確的錯誤碼。
- 已修正 WSL 中的問題, 其中如果介面的硬體位址為 32-位元組 (例如 Teredo 介面), 則網路介面資料的 Netlink 要求會失敗, 並 EINVAL
   - 請注意, Linux 「ip」公用程式包含一個 bug, 如果 WSL 報告32位元組的硬體位址, 它會損毀。 這是「ip」中的錯誤 (bug), 而不是 WSL。 「Ip」公用程式用來硬式編碼用來列印硬體位址的字串緩衝區長度, 而該緩衝區太小, 無法列印32位元組的硬體位址。
- 其他修正和改善

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:669 </br>
非通過的數字 (失敗，所以已略過等等...):258 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>組建14971

如需組建14971的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。<br/>


### <a name="fixed"></a>固定式

 - 由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。  定期排程的更新將會在下一版中繼續。

### <a name="ltp-results"></a>LTP 結果:
不變更自14965 </br>
通過測試的數目:664 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>組建14965

如需組建14965的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。<br/>


### <a name="fixed"></a>固定式

- 支援 Netlink 通訊端 NETLINK_ROUTE 通訊協定的 RTM_GETLINK 和 RTM_GETADDR (GH #468)
  - 啟用網路列舉的 ifconfig 和 ip 命令
  - 如需詳細資訊, 請參閱我們的[WSL 網路功能 blog 文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。

- 根據預設,/sbin 現在位於使用者的路徑中
- NT 使用者路徑預設會附加至 WSL 路徑 (也就是您現在可以輸入 notepad.exe, 而不需要將 System32 新增至 Linux 路徑)
- 已新增對/proc/sys/kernel/cap_last_cap 的支援
- 當目前的工作目錄包含非 ansi 字元 (GH #1254) 時, 現在可以從 WSL 啟動 NT 二進位檔
- 允許在中斷連線的 unix 資料流程通訊端上關機。
- 已新增對 PR_GET_PDEATHSIG 的支援。
- 已新增對 CLONE_PARENT 的支援
- 已修正管道停滯的錯誤, 亦即 bash-c "ls-alR/" |bash-c 「cat」 (GH #1214)
- 處理要求以連接到目前的終端機。
- 將/proc/<pid>/oom_score_adj 標記為可寫入。
- 新增形式/sys/fs/cgroup 掛接資料夾。
- sched_setaffinity 應該傳回相似性位元遮罩的數目
- 修正不正確假設解譯器路徑長度不能超過64個字元的 ELF 驗證邏輯。 (GH #743)
- 開啟檔案描述元可以保持主控台視窗開啟 (GH #1187)
- Fixeed 錯誤, 其中在目標名稱上以尾端斜線結尾的重新命名 () 失敗 (GH #1008)
- 執行/proc/net/dev 檔案
- 已修正 0.000 ms ping, 因為計時器解析度。
- 實/proc/self/environ (GH #730)
- 其他錯誤修正與改良功能

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:664 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>組建14959

如需組建14959的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。<br/>


### <a name="fixed"></a>固定式

- 改善 Windows 的 Pico 流程通知。  在[WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)上找到的其他資訊。
- 改善 Windows 互通性的穩定性
- 已修正在啟用企業資料保護 (EDP) 時啟動 bash 時的錯誤0x80070057
- 其他錯誤修正與改良功能

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:665 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>組建14955

如需組建14955的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。<br/>


### <a name="fixed"></a>固定式

 - 由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。  定期排程的更新將會在下一版中繼續。

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:665 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>組建14951

如需組建14951的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新功能:Windows/Ubuntu 互通性
現在可以直接從 WSL 命令列叫用 Windows 二進位檔。  這讓使用者能夠以不可行的方式與其 Windows 環境和系統互動。  作為快速範例, 使用者現在可以執行下列命令:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

如需詳細資訊, 請參閱:

- [WSL 適用于 Interop 的小組 Blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop 檔](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定式

- 現在已針對所有新的 WSL 實例安裝 Ubuntu 16.04 (Xenial)。  將不會自動升級具有現有 14.04 (Trusty) 實例的使用者。
- 現在會顯示在安裝期間設定的地區設定
- 終端機改善, 包括將 WSL 程式重新導向至檔案的 bug, 不一定都能運作
- 主控台存留期應該系結至 bash 存留期
- 主控台視窗大小應使用可見大小, 而不是緩衝區大小
- 其他錯誤修正與改良功能

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:665 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>組建14946

如需組建14946的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。<br/>


### <a name="fixed"></a>固定式

- 已修正無法為包含空格或引號的 NT 使用者名稱建立 WSL 使用者帳戶的問題。 
- 變更 VolFs 和 DrvFs, 使其在 stat 中針對目錄的連結計數傳回0
- 支援 IPV6_MULTICAST_HOPS 通訊端選項。
- 限制每個 tty 的單一主控台 i/o 迴圈。 範例: 以下是可能的命令:
  - bash-c "echo data" |bash-c "ssh user@example.com ' cat > foo .txt '"

- 以/proc/cpuinfo 中的索引標籤取代空格 (GH #1115)
- DrvFs 現在會出現在 mountinfo 中, 名稱符合已掛接的 Windows 磁片區
- /home 和/root 現在會以正確的名稱出現在 mountinfo 中
- 其他錯誤修正與改良功能

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:665 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>組建14942

如需組建14942的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/onefourninefourtwoooooo)。<br/>


### <a name="fixed"></a>固定式

- 有一些錯誤的錯誤處理, 包括「嘗試執行 NOEXECUTE 記憶體」網路損毀, 但封鎖了 SSH
- DrvFs 上 Windows 應用程式所產生之通知的 inotifiy 支援現已推出
- 執行 mongod.exe 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。 (GH #695)
- 執行 pivot_root 系統呼叫
- SO_DONTROUTE 的執行通訊端選項
- 其他錯誤修正與改良功能


### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:665 </br>
非通過的數字 (失敗，所以已略過等等...):263 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>組建14936

如需組建14936的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。<br/>


注意:WSL 將會在即將推出的版本中安裝 Ubuntu 版本 16.04 (Xenial), 而不是 Ubuntu 14.04 (Trusty)。  這項變更將適用于安裝新實例 (lxrun/install 或第一次執行 bash) 的內部人員。  具有 Trusty 的現有實例將不會自動升級。 使用者可以使用 [發行-升級] 命令, 將其 Trusty 映射升級至 Xenial。

### <a name="known-issue"></a>已知問題
WSL 遇到一些通訊端執行問題。  檢查錯誤會將本身視為損毀, 並出現「嘗試執行 NOEXECUTE 記憶體」錯誤。  此問題最常見的表現是使用 ssh 時的損毀。  內部組建已修正根本原因, 並會以最早的機會將其推送給內部人員。

### <a name="fixed"></a>固定式

- 執行 chroot 系統呼叫
- Inotifypropertychanged 的改良功能~~, 包括支援 DrvFs 上的 Windows 應用程式所產生的通知~~
  - 更正Inotifypropertychanged 對於源自 Windows 應用程式的變更, 目前不提供支援。
- 通訊端系結至 IPV6<port n> :: 現在支援 IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996)
- 已實 WNOWAIT waitid systemcall 的行為 (GH #638)
- 支援 IP 通訊端選項 IP_HDRINCL 和 IP_TTL
- 長度為零的讀取 () 應立即傳回 (GH #975)
- 正確處理檔案名和檔案名前置詞, 這些前置詞不會在. tar 檔案中包含 Null 結束字元。
- /dev/null 的 epoll 支援
- 修正/dev/alarm 時間來源
- Bash-c 現在可以重新導向至檔案
- 其他錯誤修正與改良功能

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:664 </br>
非通過的數字 (失敗，所以已略過等等...):264 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>組建14931

如需組建14931的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。<br/>


### <a name="fixed"></a>固定式

 - 由於不在我們的控制範圍內, 適用于 Linux 的 Windows 子系統的此組建中不會有任何更新。  定期排程的更新將會在下一版中繼續。

<br/>

## <a name="build-14926"></a>組建14926

如需組建14926的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。<br/>


### <a name="fixed"></a>固定式

- Ping 現在適用于沒有系統管理員許可權的主控台
- 現在也支援 Ping6, 而且沒有系統管理員許可權
- Inotifypropertychanged 支援透過 WSL 修改的檔案。 (GH #216)
  - 支援的旗標:
    - inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch 事件:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 屬性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 讀取輸出:LX_IN_ISDIR, LX_IN_IGNORED
  - 已知問題:從 Windows 應用程式修改檔案並不會產生任何事件
- Unix 通訊端現在支援 SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP 結果:
通過測試的數目:651 </br>
非通過的數字 (失敗，所以已略過等等...):258 </br>
[LTP 測試回合記錄](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>組建14915

如需組建14915的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定式
-  Socketpair for unix 資料包通訊端 (GH #262)
- 適用于 SO_REUSEADDR 的 Unix 通訊端支援
- 適用于 SO_BROADCAST 的 UNIX 通訊端支援 (GH #568)
- 適用于 SOCK_SEQPACKET 的 Unix 通訊端支援 (GH #758, #546)
- 新增對 unix 資料包通訊端傳送、接收和關閉的支援
- 修正錯誤檢查, 因為非固定位址的 mmap 參數驗證無效。 (GH #847)
- 支援終止/繼續終端機狀態
- 支援 TIOCPKT ioctl 來解除封鎖螢幕公用程式 (GH #774)
    - 已知問題:功能鍵無法運作
- 已更正 TimerFd 中可能造成 LxpTimerFdWorkerRoutine (GH #814) 存取已釋放成員 ' ReaderReady ' 的競爭
- 啟用 futex、輪詢和 clock_nanosleep 的可重新開機系統呼叫支援
- 已新增 bind 掛接支援
- 掛接命名空間支援的取消共用
    - 已知問題:使用`unshare(CLONE_NEWNS)`目前的工作目錄建立新的掛接命名空間時, 將會繼續指向舊的命名空間
- 其他改良功能和 bug 修正

<br/>

## <a name="build-14905"></a>組建14905

如需組建14905的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 現在支援可重新開機的系統呼叫 (GH #349、GH #520)
- 符號連結至結尾為/現在可運作的目錄 (GH #650)
- 已針對/dev/random 執行 RNDGETENTCNT ioctl
- 執行/proc/[pid]/mounts,/proc/[pid]/mountinfo 和/proc/[pid]/mountstats 檔案
- 其他錯誤修正與改良功能

</br>

## <a name="build-14901"></a>組建14901
Windows 10 年度更新版文章的第一個 Insider 組建。

如需組建14901的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。<br/>


### <a name="fixed"></a>固定式
- 已修正結尾斜線問題
    - 現在可以使用`$ mv a/c/ a/b/`的命令
- 如果 Ubuntu 地區設定應設為 Windows locale, 現在安裝會提示
- Ns 資料夾的 Procfs 支援
- 新增 tmpfs、procfs 和 sysfs 檔案系統的掛接和卸載
- 修正 mknod [at] 32 位 ABI 簽名
- Unix 通訊端已移至分派模型
- 應接受使用 setsockopt 設定的 INET 通訊端接收緩衝區大小
- 執行 MSG_CMSG_CLOEXEC unix 通訊端接收訊息旗標
- Linux 進程 stdin/stdout 管道重新導向 (GH #2)
    - 允許在 CMD 中進行 bash-c 命令的管線。  範例: > dir |bash-c "grep foo"
- Bash 現在可以安裝在具有多個頁面的系統上 (GH #538、#358)
- 預設 INET 通訊端緩衝區大小應符合預設 Ubuntu 安裝程式
- 將 xattr syscalls 對齊 listxattr
- 僅從 SIOCGIFCONF 傳回具有有效 IPv4 位址的介面
- 修正 ptrace 插入時的信號預設動作
- 執行/proc/sys/vm/min_free_kbytes
- 還原 sigreturn 中的內容時使用機器內容暫存器值
    - 這可解決某些使用者的 java 和 javac 已懸掛的問題
- 執行/proc/sys/kernel/hostname

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>組建14388至 Windows 10 年度更新版
如需組建14388的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/14388wip)。 <br/>

### <a name="fixed"></a>固定式
- 修正在8/2 上準備 Windows 10 年度更新版
  - 如需有關 WSL 的詳細資訊, 請參閱我們的[blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>組建14376
如需組建14376的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。 <br/>

### <a name="fixed"></a>固定式
- 移除某些 apt-get 停止回應的實例 (GH #493)
- 已修正未正確處理空白裝載的問題
- 已修正未正確裝載 ramdisks 的問題
- 變更 unix 通訊端接受以支援旗標 (部分 GH #451)
- 已修正一般網路相關的藍屏
- 已修正存取/proc/[pid]/task (GH #523) 時的藍屏
- 已針對某些 pty 案例 (GH #488、#504) 修正高 CPU 使用率
- 其他錯誤修正與改良功能

<br/>

## <a name="build-14371"></a>組建14371
如需組建14371的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。 <br/>

### <a name="fixed"></a>固定式
- 使用 ptrace 時, 以 SIGCHLD 和 wait () 更正計時競賽
- 已更正路徑具有尾端/(GH #432) 時的部分行為
- 已修正因為開啟子系的控制碼而導致重新命名/取消連結失敗的問題
- 其他錯誤修正與改良功能

<br/>

## <a name="build-14366"></a>組建14366
如需組建14366的一般 Windows 資訊, 請造訪[Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。 <br/>

### <a name="fixed"></a>固定式
- 透過符號連結在檔案建立時修正
-   已新增 Python 的 listxattr (GH 385)
-   其他錯誤修正與改良功能

### <a name="syscall-support"></a>Syscall 支援
-   以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>組建14361
如需組建14361的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14361)。 <br/>

### <a name="fixed"></a>固定式
- 在 Windows 上 Ubuntu 的 Bash 中執行時, DrvFs 現在會區分大小寫。
  - 使用者可能會有 .txt 和大小寫。/Mnt/c 磁片磁碟機上的 TXT
  - 只有在 Windows 上 Ubuntu 的 Bash 中才支援區分大小寫。 在 Bash NTFS 以外的地方, 會正確地報告檔案, 但是可能會發生非預期的行為, 與 Windows 中的檔案互動。
  - 每個磁片區的根目錄 (亦即/mnt/c) 不區分大小寫
  - 如需如何在 Windows 中處理這些檔案的詳細資訊, 請參閱[這裡](https://support.microsoft.com/en-us/kb/100625)。
- 大幅增強的 pty/tty 支援。  現在支援 TMUX 之類的應用程式 (GH #40)
- 已修正不一定會建立使用者帳戶的安裝問題
- 優化的命令列 arg 結構, 允許非常長的引數清單。 (GH #153)
- 現在可以從 DrvFs 刪除和 chmod read_only 檔案
- 已修正終端機在中斷連線時停止回應的某些實例 (GH #43)
- chmod 和 chown 現在可以在 tty 裝置上執行
- 允許連接到0.0.0.0 和:: 作為 localhost (GH #388)
- Sendmsg/recvmsg 現在會處理 > 1 的 IO 向量長度 (部分 GH #376)
- 使用者現在可以退出宣告自動產生的主機檔案 (GH #398)
- 在安裝期間, 自動將 Linux 地區設定與 NT 地區設定進行比對 (GH #11)
- 已新增/proc/sys/vm/swappiness 檔案 (GH #306)
- strace 現在已正確結束
- 允許透過/proc/self/fd 重新開啟管道 (GH #222)
- 隱藏%LOCALAPPDATA%\lxss from DrvFs 下的目錄 (GH #270)
- 更好的 bash 處理。  現在支援 "bash ~-c ls" 之類的命令 (GH #467)
- 通訊端現在會在關機期間通知 epoll 讀取可用 (GH #271)
- lxrun/uninstall 有更好的工作刪除檔案和資料夾
- 已更正 ps-f (GH #246)
- 改良的 x11 應用程式支援, 例如 xEmacs (GH #481)
- 已更新初始執行緒堆疊大小以符合預設 Ubuntu 設定, 並將大小正確地報告給 get_rlimit syscall (GH #172, #258)
- 已改善 pico 進程映射名稱的報告 (例如, 用於審核)
- 已針對 df 命令執行/proc/mountinfo
- 已修正子系名稱的符號式錯誤碼。 和。
- 其他改良功能的錯誤修正和改進

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>組建14352
如需組建14352的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14352)。<br/>


### <a name="fixed"></a>固定式
- 已修正未正確下載/建立大型檔案的問題。  這應該會解除封鎖 npm 和其他案例 (GH #3, GH #313)
- 移除通訊端停止回應的部分實例
- 已更正某些 ptrace 錯誤
- 已修正 WSL 允許檔案名長度超過255個字元的問題
- 改善非英文字元的支援
- 新增目前的 Windows 時區資料並設定為預設值
- 每個掛接點的唯一裝置識別碼 (jre 修正程式– GH #49)
- 更正包含 "." 之路徑的問題 和 "..."
- 已新增 Fifo 支援 (GH #71)
- 已更新 resolv.conf 格式以符合原生 Ubuntu 格式
- 某些 procfs 清除
- 已啟用系統管理員主控台的 ping (GH #18)

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>組建14342
如需組建14342的一般 Windows 資訊, 請查看[Windows Blog](https://aka.ms/wip14342)。 <br/>

如需 VolFs 和 DriveFs 的資訊, 請參閱[WSL Blog](https://blogs.msdn.microsoft.com/wsl)。 <br/>

### <a name="fixed"></a>固定式
- 已修正 Windows 使用者在使用者名稱中具有 Unicode 字元時的安裝問題
- 常見問題中的 apt-get update udev 因應措施現在預設會在第一次執行時提供
- 已在 DriveFs (于/mnt/<drive>) 目錄中啟用符號連結
- 符號連結現在可在 DriveFs 和 VolFs 之間工作
- 已解決最上層路徑剖析問題: ls.//現在會如預期般運作
- DriveFs 上的 npm install 和-g 選項現在正在運作
- 已修正導致 PHP 伺服器無法啟動的問題
- 已更新預設的環境值, 例如 $PATH 更接近原生 Ubuntu
- 在 Windows 中新增每週維護工作以更新 apt 套件快取
- 已修正 ELF 標頭驗證的問題, WSL 現在支援所有 Melkor 選項
- Zsh shell 功能正常
- 現在支援先行編譯的 Go 二進位檔
- 在 Bash 第一次執行時提示現在已正確當地語系化
- /proc/meminfo 現在會傳回正確的資訊
- VFS 現在支援的通訊端
- /dev 現在掛接為 tempfs
- 現在支援 Fifo
- 多核心系統現在已正確地顯示在/proc/cpuinfo 中
- 第一次執行期間下載的其他改良功能和錯誤訊息
- Syscall 改良功能與錯誤修正。 支援的 syscall 清單如下。
- 其他錯誤修正與改良功能

### <a name="known-issues"></a>已知問題
- 未解析 ' ... ' 在某些情況下, 于 DriveFs 上正確運作

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些執行的新或增強型 syscalls 清單。 這份清單上的 syscalls 在至少一個案例中受到支援, 但目前可能不支援所有參數。

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

## <a name="build-14332"></a>組建14332

如需組建14332的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14332)。 <br/>


### <a name="fixed"></a>固定式
- 更好的 resolv.conf, 包括排列 DNS 專案的優先順序
- 在/mnt 與非/mnt 磁片磁碟機之間移動檔案和目錄的問題
- 現在可以使用符號連結來建立 Tar 檔案
- 已在建立實例時新增預設/run/lock 目錄
- 更新/dev/null 以傳回適當的 stat 資訊
- 第一次執行時下載的其他錯誤
- Syscall 改良功能與錯誤修正。 支援的 syscall 清單如下。
- 其他改良功能的錯誤修正和改進

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些實作為的新 syscall。 至少有一個案例支援此清單上的 syscall, 但目前不支援所有參數。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>組建14328

如需組建14332的一般 Windows 資訊, 請造訪[Windows Blog](https://aka.ms/wip14328)。 <br/>


### <a name="new-features"></a>新功能
* 現在支援 Linux 使用者。  在 Windows 上的 Ubuntu 上安裝 Bash 時, 將會提示您建立 Linux 使用者。  如需詳細資訊, 請造訪 https://aka.ms/wslusers
* 主機名稱現在已設定為 Windows 電腦名稱稱, 不再有@localhost
* 如需組建14328的詳細資訊, 請造訪: https://aka.ms/wip14328

### <a name="fixed"></a>固定式
* 非于/mnt/<drive>檔案的符號的增強功能
    * npm install now works
    * jdk/jre 現在可使用[這裡](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)找到的指示來安裝。
    * 已知問題: 符號連結不適用於 Windows 裝載。  功能將在稍後的組建中提供
* 頂端和 htop 現在顯示
* 某些安裝失敗的其他錯誤訊息
* Syscall 改良功能與錯誤修正。  支援的 syscall 清單如下。
* 其他改良功能的錯誤修正和改進

### <a name="syscall-support"></a>Syscall 支援
以下是在 WSL 中有一些實作為 syscalls 的清單。  至少有一個案例支援此清單上的 Syscalls, 但目前可能不支援所有參數。

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
