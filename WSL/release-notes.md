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
# <a name="release-notes-for-windows-subsystem-for-linux"></a>適用於 Linux 的 Windows 子系統的版本資訊

## <a name="build-18342"></a>建置 18342
一般 Windows 組建 18342 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。

### <a name="wsl"></a>WSL
* 我們已新增可讓使用者從 Windows 存取在 WSL 散發版本的 Linux 檔案。 這些檔案可以透過命令列，以及 Windows 應用程式，例如 [檔案總管] 中，VSCode，等等，都可以與這些檔案互動。 存取檔案，請瀏覽至\\ \\wsl$\\< distro_name >，或看到一份瀏覽至執行散發套件\\ \\wsl$
* 新增額外的 CPU 資訊標記，並修正 Cpus_allowed [清單 （_l)] 值 [GH 2234]
* 支援從非領導者執行緒 [GH 3800] exec
* 設定更新失敗視為非嚴重 [GH 3785]
* 更新 binfmt 可正確處理位移 [GH 3768]
* 計劃 9 [GH 3854] 啟用對應網路磁碟機
* 支援 Windows]-> [Linux 和 Linux]-> [繫結掛接的 Windows 路徑轉譯
* 建立唯讀的區段，對應上開啟的檔案唯讀

## <a name="build-18334"></a>建置 18334
一般 Windows 組建 18334 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。

### <a name="wsl"></a>WSL
* 重新設計 Windows 時區會對應至 Linux 時間的時區 [GH 3747] 的方式
* 修正記憶體流失並新增新的字串翻譯函式 [GH 3746]
* 在任何執行緒的 threadgroup SIGCONT 是無作業 [GH 3741] 
* 正確地顯示 /proc/self/fd 中的 通訊端與 epoll 檔案描述項

## <a name="build-18305"></a>建置 18305
一般 Windows 組建 18305 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。

### <a name="wsl"></a>WSL
* pthreads 主執行緒結束 [GH 3589] 時，遺失檔案的存取權
* TIOCSCTTY 應該略過 「 強制 」 參數，除非必要，否則 [GH 3652]
* wsl.exe 命令列改進功能和新增匯入/匯出功能。
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

## <a name="build-18277"></a>建置 18277
一般 Windows 組建 18277 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。

### <a name="wsl"></a>WSL
* 修正組建 18272 [GH 3645] 中所引進的 「 沒有這類介面支援 」 錯誤
* 忽略 umount syscall [GH 3605] MNT_FORCE 旗標
* 切換以使用官方 CreatePseudoConsole API WSL interop
* FUTEX_WAIT 重新啟動時，維護任何逾時值

## <a name="build-18272"></a>建置 18272
一般 Windows 組建 18272 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。

### <a name="wsl"></a>WSL
* **警告：** 讓 WSL 無法運作的這個組建中沒有問題。 嘗試啟動您的散發套件時，您會看到 「 沒有這類介面支援 」 錯誤。 此問題已修正，而且會在下一週的測試人員快速建置。 如果您已安裝此組建，您可以回復至先前的 Windows 組建使用 [執行回舊版的 Windows 10] 在 [設定]-> [更新與安全性]-> 復原。

## <a name="build-18267"></a>建置 18267
一般 Windows 組建 18267 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。

### <a name="wsl"></a>WSL
* 修正的問題廢止程序可能會不 reaped 而無限期保留。
* 如果錯誤訊息超過最大長度 [GH 3592] WslRegisterDistribution 停止回應
* 允許 fsync DrvFs [GH 3556] 上的唯讀檔案順利完成
* 請確定 [/bin] 和 [/sbin 目錄存在，才能建立 [GH 3584] 內的符號連結
* 新增 WSL 執行個體的執行個體終止逾時機制。 逾時是目前設定為 15 秒，這表示執行個體將會終止在最後一個 WSL 程序結束之後的 15 秒。 若要立即終止發佈，請使用：
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>建置 17763 (1809)
一般 Windows 組建 17763 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]
* 確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* 處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結
* 更妥善地處理的 threadgroup 領導者檔案描述元清除。
* 切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL
* Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]
* 修正數個 AF_UNIX 相關問題 [GH 3371]
* 修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop
* 避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲
* 新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]
* 更精確的 IPV6 範圍資訊。
* PR_SET_PTRACER 支援 [GH 3053]
* 使用管線傳送不小心清除 edge 觸發 epoll 事件 [GH 3276] 的檔案系統
* Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]
* 改善的殭屍支援 [GH 1353]
* 加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]
* 新增支援 TIOCSTI [GH 1863]
* 連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]
* 支援在掛接的 Vhd [GH 3246，3291] 上的 interop
* 修正權限檢查在根資料夾 [GH 3304] 上的問題
* TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。
* Windows UI 應用程式應該執行，即使是在背景中啟動。
* 新增 wsl-u 或--使用者選項 [GH 1203]
* 啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]
* Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]
* 非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]
* 案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]
    * 請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。
* 新增 wslconfig/終止停止執行的散發套件。
* 修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。
* 每個目錄區分大小寫做為擴充屬性公開 （expose)
* ARM64:模擬快取的維護作業。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。
* DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。
* 修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤
* WSL 絕對計時器與過去的時間不會引發 [GH 3091]
* 確定新建立的重新分析點將因此列出父目錄中。
* 以不可分割方式在 DrvFs 區分大小寫的目錄。
* 已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。 [GH 2712]
* 固定的 WSL UMCI 啟用時，啟動失敗。 [GH 3020]
* 新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。 若要使用，請按住 shift 鍵，以滑鼠右鍵按一下 [在檔案總管] 視窗中。
* 修正 Unix 通訊端非封鎖行為 [GH 2822，3100]
* 當掉 NETLINK 命令，GH 2026 中所報告的修正程式。
* 新增支援掛接傳用旗標 [GH 2911]。
* 截斷而造成不 inotify 事件 [GH 2978] 修正問題。
* 新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。
* 新增--wsl.exe 來選取特定的散發版本的散發選項。
* Dmesg 的有限的支援。 應用程式現在可以 dmesg 來記錄。 WSL 驅動程式會記錄到 dmesg 的有限的資訊。 在將來，這可以延伸到包含其他資訊/診斷的驅動程式。
    * 注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。 `syslog` 尚未支援 syscall 介面。 以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。
* 變更預設 gid 和模式比對原生 [GH 3042] 序列裝置
* DrvFs 現在支援擴充的屬性。
    * 注意：DrvFs 的擴充屬性名稱有一些限制。 某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs

## <a name="build-18252-skip-ahead"></a>建置 18252 （直接略過）
一般 Windows 組建 18252 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。

### <a name="wsl"></a>WSL
* 移動 init 和 bsdtar 二進位檔出 lxssmanager dll 並進入不同的工具資料夾
* 修正競爭周圍使用 CLONE_FILES 時關閉檔案描述元
* 翻譯 DrvFs 路徑時，處理 /proc/pid/mountinfo 中的選擇性欄位
* 允許 DrvFs mknod 不用 S_IFREG 的中繼資料支援成功
* DrvFs 上建立的唯讀檔案應該有設定 [GH 3411] 中的 readonly 屬性
* 新增處理 DrvFs 掛接 /sbin/mount.drvfs 協助程式
* 用於 DrvFs POSIX 重新命名。
* 允許在不含磁碟區 GUID 的磁碟區上的路徑轉譯。

## <a name="build-17738-fast"></a>建置 17738 (Fast)
一般 Windows 組建 17738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 權限檢查太過嚴苛的變更相同的執行緒優先順序 [GH 1838]
* 確保非偏誤插斷時間使用開機時間，來避免傳回負值 clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* 處理在 WSL binfmt 解譯器 [GH 3424] 中的符號連結
* 更妥善地處理的 threadgroup 領導者檔案描述元清除。

## <a name="build-17728-fast"></a>建置 17728 (Fast)
一般 Windows 組建 17728 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。

### <a name="wsl"></a>WSL
* 切換以 KeQueryInterruptTimePrecise 改用 KeQueryPerformanceCounter，以避免溢位 [GH 3252] WSL
* Ptrace 附加可能導致不正確的傳回值，從系統呼叫 [GH 1731]
* 修正幾個 AF_UNIX 的相關問題 [GH 3371]
* 修正問題，可能會導致失敗，如果目前的工作目錄為小於 5 個字元長 [GH 3379] WSL interop

## <a name="build-18204-skip-ahead"></a>建置 18204 （直接略過）
一般 Windows 組建 18204 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]
* Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]

## <a name="build-17723-fast"></a>建置 17723 (Fast)
一般 Windows 組建 17723 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 避免一個失敗的回送連線不存在的連接埠 [GH 3286] 的第二個延遲
* 新增 /proc/sys/fs/file-max stub 檔案 [GH 2893]
* 更精確的 IPV6 範圍資訊。
* PR_SET_PTRACER 支援 [GH 3053]
* 使用管線傳送 filesystem inadvertenly 清除 edge 觸發 epoll 事件 [GH 3276]
* Win32 可執行檔啟動 NTFS 的符號連結透過不遵循符號連結名稱 [GH 2909]

## <a name="build-17713"></a>建置 17713
一般 Windows 組建 17713 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。

### <a name="wsl"></a>WSL
* 改善的殭屍支援 [GH 1353]
* 加入用於控制 Windows interop 行為 [GH 1493] wsl.conf 項目
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修正 getsockname 不一定會傳回 UNIX 通訊端系列類型 [GH 1774]
* 新增支援 TIOCSTI [GH 1863]
* 連接的過程中的非封鎖通訊端應該傳回 EAGAIN 寫入嘗試 [GH 2846]
* 支援在掛接的 Vhd [GH 3246，3291] 上的 interop
* 修正權限檢查在根資料夾 [GH 3304] 上的問題
* TTY 鍵盤 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支援。
* Windows UI 應用程式應該執行，即使是在背景中啟動。

## <a name="build-17704"></a>建置 17704
一般 Windows 組建 17704 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。

### <a name="wsl"></a>WSL
* 新增 wsl-u 或--使用者選項 [GH 1203]
* 啟用快速啟動時，修正 WSL 啟動問題 [GH 2576]
* Unix 通訊端需要保留已中斷連線的對等認證 [GH 3183]
* 非封鎖式 Unix 通訊端失敗，無限期地發生 EAGAIN [GH 3191]
* 案例 = off 是新的預設 drvfs 掛接類型 [GH 2937，3212，3328]
    * 請參閱[部落格](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)如需詳細資訊。
* 新增 wslconfig/終止停止執行的散發套件。

## <a name="build-17692"></a>建置 17692
一般 Windows 組建 17692 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。

### <a name="wsl"></a>WSL
* 修正問題與 WSL 殼層內容功能表項目無法正確處理具有空格的路徑。
* 每個目錄區分大小寫做為擴充屬性公開 （expose)
* ARM64:模擬快取的維護作業。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)。
* DrvFs： 只有 unescape 私用範圍內對應的字元逸出字元。

## <a name="build-17686"></a>建置 17686
一般 Windows 組建 17686 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。

### <a name="wsl"></a>WSL
* 修正 ELF 剖析器解譯器長度驗證 [GH 3154] 中關閉一個錯誤
* WSL 絕對計時器與過去的時間不會引發 [GH 3091]
* 確定新建立的重新分析點將因此列出父目錄中。
* 以不可分割方式在 DrvFs 區分大小寫的目錄。

## <a name="build-17677"></a>建置 17677
一般 Windows 組建 17677 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。

### <a name="wsl"></a>WSL
* 已修正的其他問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。 [GH 2712]
* 固定的 WSL UMCI 啟用時，啟動失敗。 [GH 3020]

## <a name="build-17666"></a>建置 17666
一般 Windows 組建 17666 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告：還有一些 AMD 晶片 [GH 3134] 上執行時，防止 WSL 問題。 修正程式是準備好讓測試人員組建分支及其方式。
* 新增 [檔案總管] 內容功能表來啟動 WSL [GH 437，603、 1836年]。 若要使用按住 shift 鍵並以滑鼠右鍵按一下在檔案總管 視窗中。
* 修正 unix 通訊端非封鎖行為 [GH 2822，3100]
* 當掉 NETLINK 命令，GH 2026 中所報告的修正程式。
* 新增支援掛接傳用旗標 [GH 2911]。
* 截斷而造成不 inotify 事件 [GH 2978] 修正問題。
* 新增--exec wsl.exe 叫用單一的二進位檔，而不需要殼層的選項。
* 新增--wsl.exe 來選取特定的散發版本的散發選項。

## <a name="build-17655-skip-ahead"></a>建置 17655 （直接略過）
一般 Windows 組建 17655 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* Dmesg 的有限的支援。 應用程式現在可以 dmesg 來記錄。 WSL 驅動程式會記錄到 dmesg 的有限的資訊。 在將來，這可以延伸到包含其他資訊/診斷的驅動程式。
    * 注意： 透過目前支援 dmesg`/dev/kmsg`裝置介面。 `syslog` 尚未支援 sycall 介面。 以及，因此，一些`dmesg`命令列選項，例如`-S`，`-C`無法運作。
* 已修正的問題，多執行緒的作業可能會傳回 ENOENT 即使檔案已存在。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>建置 17639 （直接略過）
一般 Windows 組建 17639 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 變更預設 gid 和模式比對原生 [GH 3042] 序列裝置
* DrvFs 現在支援擴充的屬性。
    * 注意：DrvFs 的擴充屬性名稱有一些限制。 特別是，某些字元 (例如 '/'、 ':' 和 '\*') 不允許，以及擴充屬性名稱不區分大小寫上 DrvFs

## <a name="build-17133-fast"></a>建置 17133 (Fast)
一般 Windows 組建 17133 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。

### <a name="wsl"></a>WSL
* 修正在 WSL 的停止回應。 [GH 3039，3034]

## <a name="build-17128-fast"></a>建置 17128 (Fast)
一般 Windows 組建 17128 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。

### <a name="wsl"></a>WSL
* None

## <a name="build-17627-skip-ahead"></a>建置 17627 （直接略過）
一般 Windows 組建 17627 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 新增支援 futex 感知 pi 的作業。 [GH 1006]
    * 請注意，優先順序而不是目前支援的 WSL 功能因此有一些限制，但標準使用量應該要解除封鎖。
* WSL 程序的 Windows 防火牆支援。 [GH 1852]
    * 比方說，若要允許 WSL python 則會接聽任何通訊埠，請使用提高權限的 Windows cmd 處理：
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 如需有關如何新增防火牆規則的詳細資訊，請參閱[連結](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* 使用 wsl.exe 時，請採用使用者的預設殼層。 [GH 2372]
* 報告為乙太網路的所有網路介面。 [GH 2996]
* 更妥善地處理的損毀 /etc/passwd 檔案。 [GH 3001]

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17618-skip-ahead"></a>建置 17618 （直接略過）
一般 Windows 組建 17618 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。

### <a name="wsl"></a>WSL
* 引入 NT interop pseudoconsole 功能 [GH 988，1366，1433年、 1542年、 2370年、 2406年]。
* 舊版安裝機制 (lxrun.exe) 已被取代。 安裝散發套件支援的機制是透過 Microsoft Store。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17110"></a>建置 17110
一般 Windows 組建 17110 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。

### <a name="wsl"></a>WSL
* 允許從 Windows [GH 2928] 終止 /init。
* DrvFs 現在預設會使用每個目錄是否區分大小寫 (相當於"案例 = dir 」 掛接選項)。
    * 使用 「 案例 = force"（舊的行為） 需要設定登錄機碼。 執行下列命令，以啟用 「 案例 = 強制 「 如果您需要使用它： reg 新增 HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * 如果您有現有的目錄建立 WSL 與 Windows 所需區分大小寫的舊版本中，會使用 fsutil.exe 來將它們標示為區分大小寫： fsutil.exe 檔案 setcasesensitiveinfo<path>啟用
* 以 NULL 結尾的 uname syscall 從傳回的字串。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17107"></a>建置 17107
一般 Windows 組建 17107 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。

### <a name="wsl"></a>WSL
* 支援 TCSETSF 和 TCSETSW 主要 pty 端點 [GH 2552] 上。
* 啟動同時 interop 的程序，可能會導致 EINVAL [GH 2813]。
* 修正 PTRACE_ATTACH 在 /proc/pid/status 中顯示適當的追蹤狀態。
* 修正競爭短期處理序使用 CLEARTID 和 SETTID 旗標已複製的儲存無法結束而不清除 TID 位址。
* 移動從 pre 17093 組建時升級 Linux 檔案系統目錄時，顯示一則訊息。 如需 17093 檔案系統變更的詳細資訊，請參閱版本資訊[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17101"></a>建置 17101
一般 Windows 組建 17101 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。

### <a name="wsl"></a>WSL
* Signalfd 支援。 [GH 129]
* 支援的檔案名稱包含不合法的 NTFS 字元加以編碼為私用的 Unicode 字元。 [GH 1514]
* 不支援寫入時，自動掛接會將恢復為唯讀。 [GH 2603]
* 允許貼上的 Unicode surrogate 字組 （例如 emoji 字元為單位）。 [GH 2765]
* /Proc 和 /sys 中的虛擬檔案應該會傳回讀取和寫入已準備好從 select、 投票、 epoll，要是 [GH 2838]
* 修正問題，可能會導致服務登錄已遭竄改，或已損毀時進入無限迴圈。
* 修正使用較新版本 (4.14 上游) iproute2 netlink 訊息。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17093"></a>建置 17093
一般 Windows 組建 17093 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。

#### <a name="important"></a>重要事項：
當從 WSL 開始第一次升級至此組建之後，它必須執行一些工作升級 Linux 檔案系統目錄。 這可能需要幾分鐘的時間，因此 WSL 似乎較慢啟動。 這只應該發生之後的每個散發中，您已安裝從存放區。
* 已改善 DrvFs 中的區分大小寫支援。
    * DrvFs 現在支援每個目錄區分大小寫。 這是新旗標，可以設定目錄，以指出在這些目錄中的所有作業應都視為區分大小寫，如此即使 Windows 應用程式正確地開啟只有大小寫不同的檔案。
    * DrvFs 具備新的掛接選項，控制每個目錄為基礎的區分大小寫
        * 案例 = 強制： 所有目錄都區分大小寫 （除了磁碟機根目錄中）。 WSL 以建立新的目錄會標示為區分大小寫。 這是除了標示新的目錄的區分大小寫的舊行為。
        * 案例 = dir： 只有透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。 WSL 以建立新的目錄會標示為區分大小寫。
        * 案例 = 關閉： 只透過每個目錄是否區分大小寫的旗標的目錄會區分大小寫;其他目錄不區分大小寫。 WSL 以建立新的目錄會標示為不區分大小寫。
    * 注意： 在舊版中建立的 WSL 目錄沒有設定，因此將不被視為區分大小寫如果您使用這個旗標 」 案例 = dir"選項。 即將推出的方式，若要在現有的目錄上設定此旗標。
    * 裝載這些選項的範例 （現有的磁碟機，您必須先卸載之前，您可以掛上使用不同的選項）： sudo mount-t drvfs c: / /mnt/c o 案例 = dir
    * 現在，寫 = 強制仍是預設選項。 這將會變更為案例未來 = dir。
* 您現在可以使用正斜線 Windows 路徑中時，裝載 DrvFs，例如： sudo 掛接-t drvfs //server/share /mnt/share
* 現在，WSL 會在執行個體啟動 [GH 2636] 處理 /etc/fstab 檔案。
    * 這是之前自動掛接 DrvFs 磁碟機;任何已經 fstab 已掛接的磁碟機將不會自動重新掛接，可讓您變更特定磁碟機的掛接點。
    * 此行為可以關閉使用 wsl.conf。
* 掛接、 mountinfo 和 mountstats 檔案中 /proc 正確逸出特殊字元，例如反斜線和空格 [GH 2799]
* 可以複製和移動從 Windows 建立 DrvFs WSL 符號連結，或 fifos 等通訊端啟用中繼資料時，特殊的檔案。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL 會與 wsl.conf 更易設定
我們已新增為您自動設定會套用每次您啟動子系統的 WSL 中的 特定功能的方法。 這包括自動掛接選項和網路設定。 深入了解在我們的部落格文章，網址： https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX 可讓 Linux 處理序在 WSL 與 Windows 原生程序之間的通訊端連線
WSL 與 Windows 應用程式現在可以透過 Unix 通訊端通訊彼此。 假設您想要在 Windows 中執行的服務，並使其可供 Windows 和 WSL 應用程式。 現在，這可能與 Unix 通訊端。 如需我們的部落格文章，讀取 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* 支援使用 MAP_NORESERVE [GH 121，2784年] mmap()
* 支援 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121，2781年]
* 處理非 SIGCHLD 終止訊號中複製 [GH 121，2781年]
* 虛設常式 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]
* 載入 ELF 二進位碼檔案包含具有非零位移 [GH 1884] 的負載標頭時發生錯誤
* 會全面清除載入影像時後, 置頁面位元組。
* 減少 execve 以無訊息方式結束處理序的情況下

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17083"></a>建置 17083
一般 Windows 組建 17083 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。

### <a name="wsl"></a>WSL
* 固定的 epoll [GH 2798，2801，2857年] 相關的錯誤檢查
* 固定的停止回應時關閉 ASLR [GH 1185，2870年]
* 請確定 mmap 作業出現不可部分完成 [GH 2732]

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17074"></a>建置 17074
一般 Windows 組建 17074 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。

### <a name="wsl"></a>WSL
* DrvFs 中繼資料 [GH 2777] 固定的儲存體格式 </br>
**重要事項：** 這個組建不正確，或完全不會出現之前建立的 DrvFs 中繼資料。 若要修正受影響的檔案，請使用 chmod 和 chown 來重新套用中繼資料。
* 與多個訊號可重新啟動 syscall 修正的問題。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17063"></a>建置 17063
一般 Windows 組建 17063 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。

### <a name="wsl"></a>WSL
* DrvFs 支援 Linux 的其他中繼資料。 這可讓設定擁有者和使用 chmod/chown，以及建立特殊的檔案，例如 fifos、 unix 通訊端和裝置檔案的檔案模式。 這預設會停用目前因為它是仍屬實驗性質。
**注意：** 我們修正了在 DrvFs 所使用的中繼資料格式。 而中繼資料則適用於此組建進行實驗，未來的組建將不會正確地讀取此組建所建立的中繼資料。  您可能需要手動更新已修改檔案的擁有者，就必須重新建立自訂裝置識別碼的裝置。

  若要啟用，請使用 [中繼資料] 選項掛接 DrvFs （現有的裝載上啟用此功能，您必須先取消掛接）：

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 的權限會新增為額外的中繼資料檔案，它們不會影響 Windows 權限。  請記住，編輯檔案，使用 Windows 編輯器可能會移除的中繼資料。 在此情況下，檔案將還原為其預設權限。

* 已新增的掛接選項 DrvFs 以不含中繼資料的控制檔案。
  * uid： 使用的所有檔案擁有者的使用者 ID。
  * gid： 使用的所有檔案擁有者的群組 ID。
  * umask： 排除所有的檔案和目錄的權限的八進位的遮罩。
  * fmask： 排除所有的一般檔案的權限的八進位的遮罩。
  * dmask： 排除所有目錄的權限的八進位的遮罩。

  例如: 
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  結合指定不含中繼資料檔案的預設權限的 [中繼資料] 選項。

* 導入新的環境變數， `WSLENV`，來設定環境變數 WSL 和 Win32 之間流動的方式。

  例如: 

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` 是以冒號分隔的清單時啟動 WSL 程序，從 Win32 或從 WSL 的 Win32 處理序可以包含環境變數。  每個變數都可以加斜線，後面接著旗標，以指定在轉譯的方式。
  * p:值為應轉譯 WSL 路徑與 Win32 路徑之間的路徑。
  * L:值是路徑的清單。 在 WSL，它是以冒號分隔的清單。 在 Win32 中，它是以分號分隔清單。
  * U:值只能包含時叫用從 Win32 WSL
  * 寫入：值只能包含時叫用 Win32 從 WSL

  您可以設定`WSLENV`.bashrc 或自訂的 Windows 環境，為您的使用者。

* drvfs 掛接正確保留時間戳記的 tar 檔案解壓縮，cp-p (GH 1939)
* drvfs 符號連結報告正確的大小 (GH 2641)
* 讀取/寫入適用於非常大的 IO 大小 (GH 2653)
* waitpid 搭配處理序群組識別碼 (GH 2534)
* 大型的保留區域，大幅改善的 mmap 效能改善 ghc 效能 (GH 1671)
* READ_IMPLIES_EXEC; 的人格支援修正行程最長和 clisp (GH 1185)
* mprotect 支援 PROT_GROWSDOWN;修正 clisp (GH 1128)
* 頁面中的錯誤修正程式過量使用模式;修正 sbcl (GH 1128)
* 複製支援多個旗標的組合
* 支援選取/epoll 的 epoll 檔案 （之前執行任何作業）。
* 通知未實作 syscall 的 ptrace。
* 忽略都未運作時產生 resolv.conf nameservers [GH 2694] 的介面
* 列舉沒有實體位址的網路介面。 [GH 2685]
* 其他錯誤修正和改進功能。

### <a name="linux-tools-available-to-developers-on-windows"></a>在 Windows 上的開發人員可使用的 Linux 工具

* Windows 命令列工具鏈包含 bsdtar (tar) 和 curl。
  讀取[這篇部落格](https://aka.ms/tarcurlwindows)深入了解這兩個新工具加入，並查看如何它們塑造在 Windows 上的開發人員體驗。

*   `AF_UNIX` 提供 Windows Insider SDK 中 （17061 +）。
  讀取[這篇部落格](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)若要深入了解`AF_UNIX`以及如何在 Windows 上的開發人員可以使用它。

### <a name="console"></a>Console
* 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。


## <a name="build-17046"></a>建置 17046

一般 Windows 組建 17046 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。

### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 允許在沒有使用中的終端機的情況下執行的處理序。 [GH 709、 1007、 1511年、 2252年 2391，et al。]
- CLONE_VFORK 和 CLONE_VM 更佳的支援。 [GH 1878，2615年]
- 略過網路作業的 WSL TDI 篩選器驅動程式。 [GH 1554]
- DrvFs 會在符合特定條件時，建立 NT 符號連結。 [GH 353，1475，2602年]
    - 連結目標必須是相對的不能跨越任何掛接點或符號連結，而且必須存在。
    - 使用者必須擁有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE （這通常需要您啟動 wsl.exe 提升權限），除非開發人員模式下開啟。
    - 在其他情況下，DrvFs 仍會建立 WSL 符號連結。
- 允許同時執行提高權限和非提高權限的 WSL 執行個體。
- Support /proc/sys/kernel/yama/ptrace_scope
- 新增 wslpath 執行 WSL <>-Windows 路徑的轉換。 [GH 522，1243，1834年、 2327，et al。]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- 不再出現問題。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。


## <a name="build-17040"></a>建置 17040

一般 Windows 組建 17040 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 因為 17035 任何修正。

#### <a name="console"></a>Console
- 因為 17035 任何修正。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17035"></a>建置 17035

一般 Windows 組建 17035 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 偶爾會失敗，但是 EINVAL 存取 DrvFs 上的檔案。 [GH 2448]

#### <a name="console"></a>Console
- 色彩遺失部分插入/刪除 VT 模式中的行時。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17025"></a>組建 17025

一般 Windows 組建 17025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 在新的前景處理程序群組 [GH 1653，2510年] 開始初始程序。
- SIGHUP 傳遞修正 [GH 2496]。
- 若無提供 [GH 2497]，則產生預設虛擬橋接器的名稱。
- 實作 /proc/sys/kernel/random/boot_id [GH 2518]。
- 修正了更 interop 的 stdout/stderr 管道。
- 虛設常式 syncfs 系統呼叫。

#### <a name="console"></a>Console
- 修正輸入的 VT 翻譯的協力廠商主控台 [GH 111]

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="build-17017"></a>建置 17017

一般 Windows 組建 17017 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 忽略空白 ELF 程式標頭 [GH 330]。
- 允許建立非互動式使用者的 WSL 執行個體的 LxssManager (ssh 和排程的工作支援) [GH 777 1602年]。
- 支援 WSL]-> [Win32]-> [WSL （「 開始 」） 案例 [GH 1228]。
- 終止透過 interop [GH 1614] 叫用的主控台應用程式的有限的支援。
- 支援掛接 devpts [GH 1948] 選項。
- Ptrace 封鎖子啟動 [GH 2333]。
- EPOLLET 遺漏某些事件 [GH 2462]。
- 傳回 PTRACE_GETSIGINFO 詳細資料。
- 使用 lseek Getdents 提供不正確的結果。
- 修正一些 Win32 interop 應用程式停止回應，有沒有更多的資料管道上等候輸入。
- O_ASYNC 支援 tty/pty 檔案。
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
在進行測試。

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>建置 16288

一般 Windows 組建 16288 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 正確初始化，並報告 uid、 gid 和通訊端檔案描述元 [GH 2490] 模式
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
16273 後並無變更

## <a name="build-16278"></a>建置 16278

一般 Windows 組建 162738 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 卸除 LX MM 狀態 [GH 2415] 時，明確地取消對應支援的檔案區段的對應的檢視
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
16273 後並無變更

## <a name="build-16275"></a>建置 16275

一般 Windows 組建 162735 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 沒有 WSL 相關的此版本中的變更。

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
16273 後並無變更

## <a name="build-16273"></a>建置 16273

一般 Windows 組建 16273 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 已修正的問題 DrvFs 有時報告目錄 [GH 2392] 錯誤的檔案類型
- 允許建立 NETLINK_KOBJECT_UEVENT 通訊端，若要解除封鎖程式，使用 uevent [GH 1121，2293，2242年、 2295年 2235，648、 637]
- 新增支援非封鎖連線 [GH 903，1391，1584年、 1585年、 1829年、 2290年、 2314年]
- 實作 CLONE_FS 複製系統呼叫旗標 [GH 2242]
- 修正問題不會處理索引標籤或 NT interop [GH 1625，2164年] 中正確的引號
- 解決錯誤時嘗試重新啟動 WSL 執行個體 [GH 651、 2095年] 拒絕存取
- 實作 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 作業 [GH 2242]
- 修正各種 SysFs 檔案 [GH 2214] 的權限
- 在安裝 [GH 2290] 期間修正 Haskell 堆疊停止回應
- 實作 binfmt_misc 'C' 'o' 和 'P' 旗標 [GH 2103]
- 加入 /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- 新增部分支援 ioprio_set 系統呼叫 [GH 498]
- 虛設常式 SO_REUSEPORT & 新增支援 SO_PASSCRED netlink 通訊端 [GH 69]
- 從 RegisterDistribuiton 傳回不同的錯誤碼，如果目前正在發佈安裝或解除安裝。
- 允許部分安裝 WSL 散發 wslconfig.exe 透過取消的註冊
- 修正從 udp::msg_peek python 通訊端測試停止回應
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
測試總計：1904<br/>
總略過測試：209<br/>
失敗總數：229<br/>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>建置 16257

一般 Windows 組建 16257 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 實作 prlimit64 系統呼叫
- 新增支援 ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]
- 虛設常式 MSG_MORE 針對 TCP 通訊端 [GH 2351]
- 修正無效的 AT_EXECFN 輔助向量行為 [GH 2133]
- 修正主控台/tty，複製/貼上的行為並新增更好的完整緩衝處理 [GH 2204，2131年]
- 設定使用者識別碼和設定群組識別碼程式 [GH 2031] 的輔助向量中設定 AT_SECURE
- 虛擬終端機主要端點不會處理 TIOCPGRP [GH 1063]
- 修正 lseek 會更新，以倒轉 LxFs [GH 2310] 中的目錄
- /dev/ptmx 鎖之後的繁重使用量 [GH 1882]
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 針對水平列/底線 Everywhere [GH 2168] 修正程式
- 修正程序順序變更並關閉 [GH 2170] 的工作變得更難的 NPM
- 加入我們新的色彩配置： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 結果：
16251 後並無變更

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`prlimit64`<br/>

### <a name="known-issues"></a>已知問題
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>GitHub 問題 2392年:無法辨識的 WSL Windows 資料夾...](https://github.com/Microsoft/BashOnWindows/issues/2392)
在組建中 16257，WSL 有問題時列舉 Windows 檔案/資料夾透過`/mnt/c/...`。
已修正此問題，因此應該在發行測試人員組建開始時間 2017 年 8 月 14 日一週內。

<br/>

## <a name="build-16251"></a>建置 16251

一般 Windows 組建 16251 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- Beta 標記移除 WSL 選用元件，請參閱 <<c0> [ 部落格文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)如需詳細資訊。
- 正確初始化儲存組 uid 與 gid exec [GH 962，1415，2072年] 上設定使用者識別碼和設定群組識別碼的二進位檔
- 已新增的支援 ptrace PTRACE_O_TRACEEXIT [GH 555]
- 已新增支援 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET NT_FPREGSET [GH 555] 與
- 已修正 ptrace 若要停止忽略訊號
- 其他改進和 bug 修正

#### <a name="console"></a>Console
- 沒有主控台的相關變更，在此版本中。

### <a name="ltp-results"></a>LTP 結果：
成功的測試數目：768</br>
失敗的測試數目：244</br>
已略過的測試數目：96</br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>建置 16241

一般 Windows 組建 16241 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。<br/>


### <a name="fixed"></a>固定式
#### <a name="wsl"></a>WSL
- 沒有 WSL 相關的此版本中的變更。

#### <a name="console"></a>Console
- 修正錯誤的字元輸出的交叉線年 12 月原本報告[這裡](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- 不修正在字碼頁 65001 (utf-8) 中顯示任何輸出文字
- 不會傳送至選取範圍變更調色盤的其他部分的一種色彩的 RGB 值所做的變更。 這會讓主控台內容工作表頁更容易使用。
- Ctrl + S 似乎未正確運作
- 非粗體 /-維度沒有完全從 ANSI 逸出程式碼 [GH 2174]
- 主控台不會正確支援 Vim 色彩佈景主題 [GH 1706]
- 無法貼上的特定字元 [GH 2149]
- 自動重排調整互動奇怪調整 bash 視窗的大小，在 [編輯] / [命令列 [GH ConEmu 1123] 上的東西時
- Ctrl-L 離開畫面已變更 [GH 1978]
- HDPI [GH 1907] 上顯示 VT 時，主控台轉譯 bug
- Japansese 字元很陌生與 Unicode 字元 U + 30FB [GH 2146]
- 其他改進和 bug 修正

</br>

## <a name="build-16237"></a>組建 16237

一般 Windows 組建 16237 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。<br/>


### <a name="fixed"></a>固定式
- 使用預設屬性，而不需要 EAs lxfs （根目錄、 根目錄，0000） 中的檔案
- 已新增的支援使用擴充的屬性的散發套件
- 修正填補 getdents 和 getdents64 所傳回的項目
- 修正 shmctl SHM_STAT 系統呼叫 [GH 2068] 的權限檢查
- 已修正不正確的初始 epoll tty [GH 2231] 狀態
- 修正 DrvFs readdir 不會傳回所有項目 [GH 2077]
- 修正 LxFs readdir 檔案時已取消連結 [GH 2077]
- 允許透過 procfs 重新開啟的檔案未連結的 drvfs
- 新增全域登錄金鑰覆寫停用 WSL 功能 (interop / 磁碟機掛接)
- 修正 「 狀態 」 中的不正確的區塊計數 DrvFs （以及 LxFs） [GH 1894]
- 其他改進和 bug 修正

</br>

## <a name="build-16232"></a>建置 16232

一般 Windows 組建 16232 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 沒有 WSL 相關的此版本中的變更。

</br>

## <a name="build-16226"></a>建置 16226

一般 Windows 組建 16226 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。<br/>


### <a name="fixed"></a>固定式
- xattr 相關 syscall 支援 （getxattr、 setxattr、 listxattr、 removexattr）。
- security.capablity xattr 支援。
- 改進的相容性與特定的檔案系統篩選器，包括非 MS SMB 伺服器。 [GH #1952]
- 改善對 OneDrive 預留位置、 GVFS 預留位置和精簡的 OS 支援壓縮的檔案。
- 其他改進和 bug 修正

</br>

## <a name="build-16215"></a>建置 16215

一般 Windows 組建 16215 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。<br/>


### <a name="fixed"></a>固定式
- WSL 不再需要開發人員模式。
- 支援 drvfs 目錄連接。
- 處理的 WSL 發佈 appx 套件解除安裝。
- 更新 procfs 顯示私用和共用對應。
- 新增 wslconfig.exe 清除部分安裝或解除安裝的散發套件的能力。
- 已新增的支援 IP_MTU_DISCOVER 針對 TCP 通訊端。 [GH 1639，2115，2205年]
- 推斷 AF_INADDR 路由通訊協定家族。
- 序列裝置的功能改進 [GH 1929]。

</br>

## <a name="build-16199"></a>建置 16199

一般 Windows 組建 16199 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 沒有 WSL 相關的這些版本中的變更。

</br>

## <a name="build-16193"></a>建置 16193

一般 Windows 組建 16193 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 傳送 SIGCONT 以及終止 [GH 1973] threadgroup 之間的競爭情形
- 將報表而不是 [GH 1840] FILE_DEVICE_CONSOLE FILE_DEVICE_NAMED_PIPE tty 和 pty 裝置
- SSH IP_OPTIONS 修正
- 移動 DrvFs 掛接至 init 精靈 [GH 1862，1968 年，1767年、 1933年]
- 已新增的支援在 DrvFs 遵循 NT 符號連結。

</br>

## <a name="build-16184"></a>建置 16184

一般 Windows 組建 16184 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 已移除的 apt 套件維護工作 (lxrun.exe /update)
- 已修正未出現在從 node.js [GH 1840] 中的 Windows 處理序的輸出
- 放寬 lxcore [GH 1794] 中的對齊需求
- 已修正的數系統呼叫的 AT_EMPTY_PATH 旗標的處理。
- 已修正的問題，其中刪除 DrvFs 檔案含有開啟控制代碼，會導致檔案出現未定義的行為 [GH 544,966,1357,1535,1615]
- eg /etc/ 主機現在將會從 Windows hosts 檔案 (%windir%\system32\drivers\etc\hosts) 繼承項目 [GH 1495]

</br>

## <a name="build-16179"></a>建置 16179

一般 Windows 組建 16179 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 沒有 WSL 變更本週。

</br>

## <a name="build-16176"></a>建置 16176

一般 Windows 組建 16176 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。<br/>


### <a name="fixed"></a>固定式

- [已啟用序列的支援](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 已新增的 IP 通訊端選項 IP_OPTIONS [GH 1116]
- （在檔案上傳至 nginx/PHP-FPM） 實作 pwritev 函式 [GH 1506]
- 新增 IP 通訊端選項 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- 支援的通訊端選項 IP_MULTICAST_LOOP IPV6_MULTICAST_LOOP [GH 1678]
- 已新增適用於應用程式節點、 追蹤路由、 dig、 nslookup、 主機 IP (V6) _MTU 通訊端選項
- 已新增的 IP 通訊端選項 IPV6_UNICAST_HOPS
- [檔案系統的增強功能](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * 允許的 UNC 路徑的掛接
    * 啟用在 drvfs CDFS 支援
    * 正確處理 drvfs 中的網路檔案系統權限
    * 支援遠端磁碟機新增至 drvfs
    * 啟用 FAT drvfs 中支援
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果
自 15042 後的任何變更

</br>

## <a name="build-16170"></a>建置 16170

一般 Windows 組建 16170 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。<br/>

我們發行了新[部落格文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)討論我們努力測試 WSL。

### <a name="fixed"></a>固定式

- 支援通訊端選項 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- 新增對 PTRACE_OLDSETOPTIONS 支援。 [GH 1692]
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果
自 15042 後的任何變更

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>建置 15046 到 Windows 10 Creators Update
沒有更多的 WSL 修正或加入至 Windows 10 Creators Update 中的功能。 在未來幾週的目標設為下一個主要的 Windows 更新的新增項目中，將會繼續 WSL 的版本資訊。 針對一般的 Windows 上建置 15046 和未來的測試人員的資訊發行版本，請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。 <br/><br/>
 <br/>

## <a name="build-15042"></a>建置 15042

一般 Windows 組建 15042 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。<br/>


### <a name="fixed"></a>固定式

- 移除路徑，在結束時，產生死結的修正"."
- 已修正的問題其中 FIONBIO 未成功 [GH 1683] 傳回 0
- 已修正的問題 inet 資料包通訊端讀取長度為零
- 修正 [drvfs inode 查閱 [GH 1675] 中的 [可能的死結，因為競爭條件
- 擴充支援 unix 通訊端的輔助資料;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514，613、 1326年]
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：737</br>
非通過的數字 (失敗，所以已略過等等。...):255

</br>

## <a name="build-15031"></a>建置 15031

一般 Windows 組建 15031 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。<br/>


### <a name="fixed"></a>固定式

- 修正了其中 time(2) 會偶發性行為異常。
- 已修正，並發出 where * SIGPROCMASK syscall 可能會損毀訊號遮罩。
- 現在會傳回完整的命令列長度在 WSL 程序建立通知。 [GH 1632]
- WSL 現在會報告執行緒結束時，透過 ptrace 的 GDB 停止回應。 [GH 1196]
- 已修正的 bug，其中 ptys 會停止回應之後大量 tmux IO。 [GH 1358]
- 許多系統呼叫 （futex、 semtimedop、 ppoll、 sigtimedwait、 itimer、 timer_create） 中的固定的逾時驗證
- 已新增的 eventfd EFD_SEMAPHORE 支援 [GH 452]
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：737</br>
非通過的數字 (失敗，所以已略過等等。...):255 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>建置 15025

一般 Windows 組建 15025 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。<br/>


### <a name="fixed"></a>固定式

- 修正 bug，沒壞的 grep 2.27 [GH 1578]
- 實作的 eventfd2 syscall [GH 452] EFD_SEMAPHORE 旗標
- 實作 /proc/ [pid] / net/ipv6_route [GH 1608]
- 訊號驅動 IO 支援 unix 資料流通訊端 [GH 393，68]
- 支援 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]
- 實作 recvmmsg() syscall [GH 1531]
- 已修正的 bug epoll_wait() 不正在等候 [GH 1609]
- 實作 /proc/version_signature
- Tee syscall 現在會傳回失敗，如果這兩個檔案描述元參考到相同的管道
- 實作正確的行為 SO_PEERCRED Unix 通訊端
- 固定的 tkill syscall 無效參數處理方法
- 若要增加的 drvfs preformace 的變更
- Ruby IO 封鎖的次要修正
- 固定的 recvmsg() 傳回 EINVAL MSG_DONTWAIT 旗標的 inet 通訊端 [GH 1296]
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：732</br>
非通過的數字 (失敗，所以已略過等等。...):255 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

一般 Windows build 15019 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。<br/>


### <a name="fixed"></a>固定式

- 已修正的 bug，正確地報告中的 CPU 使用量 procfs htop (GH 823 945、 971) 等工具
- 當呼叫 open （） 與 O_TRUNC 上的現有檔案 inotify 現在會產生之前 IN_OPEN IN_MODIFY
- Unix 通訊端 getsockopt SO_ERROR 啟用 postgress [GH 61，1354年] 修正程式
- 實作 /proc/sys/net/core/somaxconn GO 語言
- Apt get 封裝更新背景工作現在會隱藏執行檢視
- 清除範圍 ipv6 localhost （Spring-Framework(Java) 失敗）。
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：714 </br>
非通過的數字 (失敗，所以已略過等等。...):249 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>建置 15014

一般 Windows 組建 15014 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定式

- Ctrl + C 現在如預期般運作
- htop 和 ps auxw 現在顯示正確的資源使用率 (GH #516)
- 基本訊號的 NT 例外狀況的翻譯。 (GH #513)
- fallocate 現在 ENOSPC 時發生無法用盡空間，而不是 EINVAL (GH #1571)
- 已新增的 /proc/sys/kernel/sem。
- 實作的 semop 和 semtimedop 系統呼叫
- 固定的 nslookup 錯誤 IP_RECVTOS & IPV6_RECVTCLASS 通訊端選項 (GH 69)
- 支援通訊端選項 IP_RECVTTL 和 IPV6_RECVHOPLIMIT
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：709 </br>
非通過的數字 (失敗，所以已略過等等。...):255 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 摘要
總 Syscall:384 </br>
實作的總計：235 </br>
虛設常式的總計：22 </br>
如果未實作的總計：127 </br>
[詳細分解圖](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>建置 15007

一般 Windows 組建 15007 的詳細資訊請造訪[Windows 部落格]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。<br/>


### <a name="known-issue"></a>已知的問題

- 已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。  這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。

  - 因應措施：替代的索引鍵對應至 Ctrl + C。 例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。  此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。 使用者可以瀏覽的選項包含在其 `.bashrc`

### <a name="fixed"></a>固定式

- 已更正此問題，其中執行 WSL 會消耗掉 100%的 CPU 核心
- 通訊端選項 IP_PKTINFO，IPV6_RECVPKTINFO 現在支援。 (GH #851, 987)
- 截斷的 lxcore 16 個位元組到網路介面實體位址 (GH #1452 1414，1343，468，308)
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：709 </br>
非通過的數字 (失敗，所以已略過等等。...):255 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>建置 15002

一般 Windows 組建 15002 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。<br/>


### <a name="known-issue"></a>已知的問題

兩個已知的問題：
- 已知錯誤，主控台不會辨識某些 Ctrl +<key>輸入。  這包括將做為一般 'c' 按鍵動作的 ctrl + c 命令。

  - 因應措施：替代的索引鍵對應至 Ctrl + C。 例如，若要對應 Ctrl + K Ctrl + C 來執行： `stty intr \^k`。  此對應是在每個終端機，而且必須完成*每個*時間 bash 會啟動。 使用者可以瀏覽的選項包含在其 `.bashrc`

- 執行 WSL 時系統執行緒會耗用的 CPU 核心的 100%。  已解決的根本原因並已修正在內部。

### <a name="fixed"></a>固定式

- 所有的 bash 工作階段現在必須建立在相同的權限層級。  嘗試啟動工作階段在不同的層級會被封鎖。  這表示系統管理員 」 和 「 非系統管理員主控台無法在同一時間執行。 (GH #626)
<br/>
- 實作下列 NETLINK_ROUTE 訊息 （需要 Windows 系統管理員）
     - RTM_NEWADDR (支援`ip addr add`)
     - RTM_NEWROUTE (支援`ip route add`)
     - RTM_DELADDR (支援`ip addr del`)
     - RTM_DELROUTE (支援`ip route del`)
- 在計量付費連線 (GH #1371) 上，將無法再執行套件，以更新檢查的排程的工作
- 已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)
- 實作的 TCP_KEEPCNT 通訊端選項 (GH #843)
- 實作的 IP_MTU_DISCOVER INET 通訊端選項 (GH #720，717，170，69)
- 移除舊版的功能，以從 NT 路徑查閱使用 init 執行 NT 二進位檔。 (GH #1325)
- 修正/kmsg 允許群組 / 讀取權限 (0644) (GH #1321) 模式
- 實作的 /proc/sys/kernel/random/uuid (GH #1092)
- 修正的錯誤，處理序開始時間會顯示為 2432 年 (GH #974)
- 切換的預設詞彙環境變數，以 xterm 256color (GH #1446)
- 修改處理認可的方式計算期間處理程序分支。 (GH #1286)
- 實作的 /proc/sys/vm/overcommit_memory。 (GH #1286)
- 實作的 /proc/net/route 檔案 (GH #69)
- 已修正的錯誤捷徑名稱的正確當地語系化 (GH #696)
- 已修正剖析邏輯，不正確地驗證程式的標頭的 elf 必須小於 （或等於） PATH_MAX。 (GH #1048)
- 實作的 statfs 回呼 procfs，sysfs、 cgroupfs，和 binfmtfs (GH #1378)
- 不會關閉 (GH #1184，也在 GH # 1193年中討論) 的固定的 AptPackageIndexUpdate windows
- 已新增的 ASLR 個性 ADDR_NO_RANDOMIZE 支援。 (GH #1148, 1128)
- 改善的 PTRACE_GETSIGINFO，SIGSEGV，針對適當 gdb AV (GH #875) 期間的堆疊追蹤
- Elf 剖析不會再失敗 patchelf 二進位檔。 (GH #471)
- VPN DNS 傳播至 /etc/resolv.conf (GH #416，1350年)
- 改善 TCP 關閉更可靠的資料傳輸。 (GH #610 616、 1025，1335年)
- 開啟 (EMFILE) 現在會傳回正確的錯誤程式碼中，使用太多檔案時。 (GH # 1126年 2090年)
- Windows 稽核記錄檔現在報告程序中的映像名稱建立稽核。
- 現在依正常程序失敗時啟動 bash 視窗內從 bash.exe
- 當 interop 新增的錯誤訊息無法存取工作目錄下 LxFs (也就是 notepad.exe.bashrc)
- 已修正的問題已在 WSL 遭截斷 Windows 路徑
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：690 </br>
非通過的數字 (失敗，所以已略過等等。...):274 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>建置 14986

一般 Windows 組建 14986 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。<br/>


### <a name="fixed"></a>固定式

- 固定的 bugchecks Netlink 與 Pty Ioctl
- 核心版本現在會報告 4.4.0-43 與 Xenial 的一致性
- 輸入指示時，現在會啟動 Bash.exe ' nul:' (GH #1259)
- 執行緒現在報告識別碼正確 procfs (GH #967)
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |現在支援 inotify_add_watch() (GH #1280) IN_ISDIR 旗標
- 實作 timer_create 和相關的系統呼叫。  這可讓 GHC 支援 (GH #307)
- 已修正的問題，其中 ping 傳回 0.000ms (GH #1296) 的時間
- 開啟太多檔案時，則傳回正確的錯誤碼。
- 已修正的問題，在 WSL 其中網路介面 data Netlink 要求會失敗並 EINVAL 如果介面的硬體位址為 32 個位元組 （例如 Teredo 介面）
   - 請注意，Linux 「 ip 」 公用程式，包含的 bug，其中這皆會損毀如果 WSL 報告 32 位元組的硬體位址。 這是 「 ip 」，不 WSL 中的 bug。 「 Ip 」 公用程式硬式編碼的字串緩衝區長度用來列印的硬體位址，以及該緩衝區太小而無法列印的 32 位元組的硬體位址。
- 其他修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：669 </br>
非通過的數字 (失敗，所以已略過等等。...):258 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>建置 14971

一般 Windows 組建 14971 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。<br/>


### <a name="fixed"></a>固定式

 - 由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。  下一個版本時才會恢復有排定來定期更新。

### <a name="ltp-results"></a>LTP 結果：
從 14965 以來並未變更 </br>
通過測試數目：664 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>建置 14965

一般 Windows 組建 14965 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。<br/>


### <a name="fixed"></a>固定式

- 支援 Netlink 通訊端通訊協定 NETLINK_ROUTE RTM_GETLINK 和 RTM_GETADDR (GH #468)
  - 可讓網路列舉的 ifconfig 和 ip 命令
  - 詳細的資訊可在我們[WSL 網路部落格文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。

- /sbin 現在是使用者的預設路徑
- 現在預設 （也就是您可以現在輸入 notepad.exe 而不會增加 System32 Linux 路徑），以附加至 WSL 路徑的 NT 使用者路徑
- 已新增的支援 /proc/sys/kernel/cap_last_cap
- NT 二進位檔可以立即從 WSL 啟動，當目前的工作目錄包含非 ansi 字元 (GH #1254)
- 允許在已中斷連線的 unix 資料流通訊端上的關機。
- 已新增的支援 PR_GET_PDEATHSIG。
- 已新增的支援 CLONE_PARENT
- 已修正錯誤，管線取得卡也就是 bash-c"ls alR /"|bash-c"cat"(GH #1214)
- 若要連接到目前的終端機的控制代碼要求。
- 標示 /proc/<pid>/oom_score_adj 為可寫入。
- 新增 /sys/fs/cgroup 資料夾。
- sched_setaffinity 應傳回數目相似性位元遮罩
- 修正未正確假設 解譯器路徑必須少於 64 個字元長 ELF 驗證邏輯。 (GH #743)
- 開啟檔案描述元可以保留主控台視窗中開啟 (GH #1187)
- Fixeed 錯誤 rename （） 後面加上目標名稱 (GH #1008) 的正斜線失敗的位置
- 實作 /proc/net/dev 檔案
- 固定的 0.000ms 偵測由於計時器解析度。
- 實作的 /proc/self/environ (GH #730)
- 其他錯誤修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：664 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>建置 14959

一般 Windows 組建 14959 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。<br/>


### <a name="fixed"></a>固定式

- 已改進的 Windows 的 Pico 程序通知。  其他資訊，請參閱[WSL 部落格](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)。
- 改進的穩定性與 Windows 互通性
- 已修正的錯誤 0x80070057 啟用企業資料保護 (EDP) 時，啟動 bash.exe 時
- 其他錯誤修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：665 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>建置 14955

一般 Windows 組建 14955 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。<br/>


### <a name="fixed"></a>固定式

 - 由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。  下一個版本時才會恢復有排定來定期更新。

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：665 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>建置 14951

一般 Windows 組建 14951 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新功能：Windows / Ubuntu 互通性
現在可以直接從 WSL 命令列叫用 Windows 二進位檔。  這可讓使用者使用他們的 Windows 環境和系統的方式一直無法互動的能力。  快速的範例，就可以讓使用者執行下列命令：

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

詳細資訊，參閱：

- [Interop 的 WSL 小組部落格](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop 文件](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定式

- Ubuntu 16.04 (Xenial) 現在會安裝所有新的 WSL 執行個體。  使用現有的 14.04 (Mible) 執行個體的使用者將不會自動升級。
- 現在會顯示在安裝期間設定的地區設定
- 終端機功能改良，包括的 bug，其中將 WSL 程序重新導向至檔案不一定不會運作
- 主控台存留期應該繫結至 bash.exe 存留期
- 主控台視窗大小應該使用可見的大小，而非緩衝區大小
- 其他錯誤修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：665 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>建置 14946

一般 Windows 組建 14946 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。<br/>


### <a name="fixed"></a>固定式

- 已修正的問題，導致無法建立 WSL 之使用者的使用者帳戶為 NT 使用者名稱包含空格或引號。 
- 變更 VolFs 和 DrvFs，以傳回狀態 0 代表目錄的連結計數
- 支援 IPV6_MULTICAST_HOPS 通訊端選項。
- I/O 迴圈每 tty 限制為單一主控台中。 範例： 可能是下列命令：
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- 空格取代為 /proc/cpuinfo (GH #1115) 中的索引標籤
- DrvFs 現在會出現在 mountinfo 符合掛接的 Windows 磁碟區的名稱
- /home 和 /root 現在會出現在 mountinfo 具有正確的名稱
- 其他錯誤修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：665 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>建置 14942

一般 Windows 組建 14942 的詳細資訊請造訪[Windows 部落格](https://aka.ms/onefourninefourtwoooooo)。<br/>


### <a name="fixed"></a>固定式

- 數個 bugchecks 解決，包括 「 嘗試執行的 NOEXECUTE 記憶體 」 網路已封鎖 SSH 的損毀
- 來自 DrvFs 上的 Windows 應用程式所產生之通知的 inotifiy 支援現為
- 實作 TCP_KEEPIDLE 和 TCP_KEEPINTVL mongod。 (GH #695)
- 實作 pivot_root 系統呼叫
- 實作 SO_DONTROUTE 的通訊端選項
- 其他錯誤修正和增強功能


### <a name="ltp-results"></a>LTP 結果：
通過測試數目：665 </br>
非通過的數字 (失敗，所以已略過等等。...):263 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>建置 14936

一般 Windows 組建 14936 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。<br/>


注意：WSL 會安裝在即將推出的版本中的 Ubuntu 16.04 版 (Xenial) 而不是 Ubuntu 14.04 （駒）。  這項變更將套用到安裝新的執行個體 （lxrun.exe /install 或 bash.exe 第一次執行） 的測試人員。  具有可信賴的現有執行個體將不會自動升級。 使用者可以 Xenial 使用執行版本升級 命令來升級其 Mible 映像。

### <a name="known-issue"></a>已知的問題
WSL 發生某些通訊端實作的問題。  檢查錯誤會造成系統呈現的損毀並出現錯誤 「 嘗試執行的 NOEXECUTE 記憶體 」。  此問題最常見的現象使用 ssh 時當機。  修正內部組建並將測試人員儘早推送根本原因。

### <a name="fixed"></a>固定式

- 實作 chroot 系統呼叫
- 改進 inotify~~包括來自 DrvFs 上的 Windows 應用程式所產生之通知的支援~~
  - 修正：Inotify 支援來自 Windows 應用程式無法使用目前的變更。
- 通訊端繫結的 ipv6::<port n>現在支援 IPV6_V6ONLY (GH #68、 #157、 #393、 #460、 #674、 #740、 #982、 #996)
- Waitid systemcall WNOWAIT 行為實作 (GH #638)
- 支援 IP 通訊端選項 IP_HDRINCL 和 IP_TTL
- 長度為零的 read （） 應該會立即傳回 (GH #975)
- 正確處理不在.tar 檔案中包含 NULL 結束字元的檔名和檔案名稱前置詞。
- /dev/null 時發生 epoll 支援
- 修正 /dev/alarm 時間來源
- Bash-c 現在能夠重新導向至檔案
- 其他錯誤修正和增強功能

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：664 </br>
非通過的數字 (失敗，所以已略過等等。...):264 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>建置 14931

一般 Windows 組建 14931 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。<br/>


### <a name="fixed"></a>固定式

 - 由於我們控制的情況下沒有任何更新適用於 Linux 的 Windows 子系統的這個組建中。  下一個版本中，將會繼續定期排定的更新。

<br/>

## <a name="build-14926"></a>建置 14926

一般 Windows 組建 14926 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。<br/>


### <a name="fixed"></a>固定式

- Ping 現在可在主控台中確實具備系統管理員權限
- 現在支援，也沒有管理員權限的 ping 6
- Inotify 支援透過 WSL 修改的檔案。 (GH #216)
  - 支援的旗標：
    - inotify_init1:LX_O_CLOEXEC LX_O_NONBLOCK
    - inotify_add_watch 事件：LX_IN_ACCESS、 LX_IN_MODIFY、 LX_IN_ATTRIB、 LX_IN_CLOSE_WRITE、 LX_IN_CLOSE_NOWRITE、 LX_IN_OPEN、 LX_IN_MOVED_FROM、 LX_IN_MOVED_TO、 LX_IN_CREATE、 LX_IN_DELETE、 LX_IN_DELETE_SELF、 LX_IN_MOVE_SELF
    - inotify_add_watch 屬性：LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 讀取輸出：LX_IN_ISDIR LX_IN_IGNORED
  - 已知的問題：修改檔案從 Windows 應用程式不會產生任何事件
- Unix 通訊端現在支援 SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP 結果：
通過測試數目：651 </br>
非通過的數字 (失敗，所以已略過等等。...):258 </br>
[LTP 測試回合記錄檔](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>建置 14915

一般 Windows 組建 14915 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定式
-  Socketpair unix 資料包通訊端 (GH #262)
- SO_REUSEADDR Unix 通訊端支援
- SO_BROADCAST (GH #568) 的 UNIX 通訊端支援
- SOCK_SEQPACKET (GH #758，#546) 的 Unix 通訊端支援
- 新增支援 unix 資料包通訊端的傳送、 接收和關閉
- 修正由於非固定位址的無效 mmap 參數驗證錯誤檢查。 (GH #847)
- 支援的暫止 / 繼續的終端機的狀態
- 若要解除封鎖 「 螢幕 」 公用程式 (GH #774) TIOCPKT ioctl 的支援
    - 已知的問題：功能鍵無法運作
- 已更正的競爭可能會導致將釋放的成員 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814) 存取的 TimerFd
- 啟用 futex、 輪詢和 clock_nanosleep 的可重新啟動系統呼叫支援
- 新增繫結掛接支援
- 如需掛接命名空間支援取消共用
    - 已知的問題：當建立新的掛接命名空間與`unshare(CLONE_NEWNS)`仍然指向舊的命名空間目前的工作目錄
- 其他改進和 bug 修正

<br/>

## <a name="build-14905"></a>建置 14905

一般 Windows 組建 14905 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。<br/>


### <a name="fixed"></a>固定式
- 可重新啟動系統呼叫現在支援 (GH #349，GH #520)
- 結束在 / 現在操作的目錄 (GH #650) 的符號連結
- 實作的 RNDGETENTCNT ioctl /dev/random 的
- 實作 /proc/ [pid] / 掛接，/proc/ [pid] / mountinfo 和 /proc/ [pid] / mountstats 檔案
- 其他錯誤修正和增強功能

</br>

## <a name="build-14901"></a>建置 14901
第一次的測試人員組建的 Windows 10 年度更新版的文章。

一般 Windows 組建 14901 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。<br/>


### <a name="fixed"></a>固定式
- 已修正的尾端斜線問題
    - 命令，例如`$ mv a/c/ a/b/`現在可運作
- 只有當 Ubuntu 地區設定應該設為 Windows 地區設定，現在安裝提示
- Procfs 支援 ns 資料夾
- 新增掛接和卸載 tmpfs procfs 和 sysfs 檔案系統
- 修正 mknod [at] 32 位元 ABI 簽章
- 移至分派模型的 Unix 通訊端
- 設定使用 setsockopt INET 通訊端接收緩衝區大小應該接受
- 實作 MSG_CMSG_CLOEXEC unix 通訊端接收訊息的旗標
- Linux 程序 stdin/stdout 管道重新導向 (GH #2)
    - 允許的 CMD 中的 bash-c 命令的管線  範例： > dir |bash-c"grep foo"
- 現在可以在多個分頁檔 (GH #538，#358) 的系統上安裝 bash
- 預設 INET 通訊端緩衝區大小應該符合預設 Ubuntu 安裝程式
- 對齊到 listxattr xattr syscall
- 只從 SIOCGIFCONF 傳回有效的 IPv4 位址的介面
- 修正當由 ptrace 插入的訊號的預設動作
- implement /proc/sys/vm/min_free_kbytes
- 還原在 sigreturn 內容時所使用電腦內容暫存器值
    - 這個方法可以解決此問題其中的某些使用者溢出 java 和 javac
- 實作 /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>建置 Windows 10 年度更新版的 14388
一般 Windows 組建 14388 的詳細資訊請造訪[Windows 部落格](https://aka.ms/14388wip)。 <br/>

### <a name="fixed"></a>固定式
- 準備適用於 Windows 10 年度更新 8/2 的修正
  - 在年度更新版的 WSL 的詳細資訊都位於我們[部落格](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>建置 14376
一般 Windows 組建 14376 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。 <br/>

### <a name="fixed"></a>固定式
- 移除某些情況下，apt get 停止回應 (GH #493)
- 已修正的問題，空白的掛接已無法正確處理
- 已修正的問題其中 ramdisks 已不正確地掛載
- 變更 unix 通訊端接受支援旗標 (部分 GH #451)
- 已修正常見的網路相關藍色螢幕
- 存取 /proc/ [pid] 時，已修正藍色螢幕 / 工作 (GH #523)
- 已修正的 CPU 使用率過高的一些 pty 案例 (GH #488，#504)
- 其他錯誤修正和增強功能

<br/>

## <a name="build-14371"></a>建置 14371
一般 Windows 組建 14371 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。 <br/>

### <a name="fixed"></a>固定式
- 當使用 ptrace 更正 SIGCHLD 與 wait() 計時競爭
- 當路徑有尾端時修正某些行為 / (GH #432)
- 取消重新命名/連結來失敗的原因是子系的開啟控制代碼已修正的問題
- 其他錯誤修正和增強功能

<br/>

## <a name="build-14366"></a>建置 14366
一般 Windows 組建 14366 的詳細資訊請造訪[Windows 部落格](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。 <br/>

### <a name="fixed"></a>固定式
- 修正透過符號連結的檔案建立時
-   已新增的 listxattr 適用於 Python (GH 385)
-   其他錯誤修正和增強功能

### <a name="syscall-support"></a>Syscall 支援
-   以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>組建 14361 開始
一般 Windows 組建 14361 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14361)。 <br/>

### <a name="fixed"></a>固定式
- Windows 上執行 bash on Ubuntu 時，DrvFs 現在會區分大小寫。
  - 使用者可能 case.txt 和案例。TXT 其 /mnt c 磁碟機
  - 在 Windows 上 Ubuntu 之 Bash 上才支援區分大小寫。 當外部 Bash NTFS 的報表檔案的正確，但未預期的行為可能會發生與從 Windows 檔案互動。
  - 每個磁碟區 (也就是 /mnt/c) 的根目錄不區分大小寫
  - 可以找到更多有關處理 Windows 中的這些檔案[此處](https://support.microsoft.com/en-us/kb/100625)。
- 經過大幅增強的 pty / tty 支援。  應用程式，例如 TMUX 現在支援 (GH #40)
- 使用者帳戶不一定建立固定的安裝問題
- 最佳化以很長的引數清單的命令列引數結構。 (GH #153)
- 現在可以刪除並 chmod read_only 檔案從 DrvFs
- 已修正某些情況下，終端機的停止回應，在中斷連線 (GH #43)
- chmod 和 chown 現在使用 tty 裝置
- 允許連線至 0.0.0.0 和:: 為 localhost (GH #388)
- Sendmsg/recvmsg 現在處理的 IO 向量長度 > 1 (部分 GH #376)
- 使用者可以立即選擇不自動產生的主機檔案 (GH #398)
- 自動安裝 (GH #11) 期間會符合 Linux NT 地區設定的地區設定
- 新增 /proc/sys/vm/swappiness 檔案 (GH #306)
- 才能正確 strace 現在結束
- 允許管道來重新開啟透過 /proc/self/fd (GH #222)
- 隱藏 %LOCALAPPDATA%\lxss 從 DrvFs (GH #270) 下的目錄
- 更妥善地處理的 bash.exe ~。  命令喜歡"bash ~-c ls 」 現在支援 (GH #467)
- 通訊端現在，當 epoll 關機 (GH #271) 期間所提供的讀取
- lxrun / 解除安裝的刪除的檔案和資料夾工作
- 已更正的 ps-f (GH #246)
- 已改善支援 x11 xEmacs (GH #481) 之類的應用程式
- 已更新初始執行緒堆疊大小，以符合預設 Ubuntu 設定，並正確地回報給 get_rlimit syscall (GH #172，#258) 的大小
- 改善報告 pico 程序映像名稱 （例如，適用於稽核）
- 實作的 /proc/mountinfo df 命令
- 已修正子名稱的符號連結錯誤程式碼。 與...
- 其他改進錯誤修正和增強功能

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>組建 14352
一般 Windows 組建 14352 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14352)。<br/>


### <a name="fixed"></a>固定式
- 已修正的問題，大型檔案已下載 / 無法正確建立。  這應該解除封鎖 npm 和其他案例 （GH #3，GH #313）
- 移除某些情況下通訊端的停止回應
- 修正一些 ptrace 錯誤
- 已修正的問題，以允許檔案名稱超過 255 個字元的 WSL
- 非英文字元的改進的支援
- 加入目前的 Windows 時區資料，並設定為預設值
- 唯一裝置識別碼的每個掛接點 （jre 修復 – GH #49）
- 包含路徑與修正問題 」。 」 和"."
- 已新增的 Fifo 支援 (GH #71)
- 更新的 resolv.conf 來比對原生的 Ubuntu 格式的格式
- 某些 procfs 的清除工作
- 系統管理員主控台 (GH #18) 的已啟用的 ping

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>建置 14342
一般的 Windows 上的資訊建置 14342 [Windows 部落格](https://aka.ms/wip14342)。 <br/>

可以上找到有關 VolFs 和 DriveFs [WSL 部落格](https://blogs.msdn.microsoft.com/wsl)。 <br/>

### <a name="fixed"></a>固定式
- Windows 使用者的使用者名稱中有 Unicode 字元時，已修正安裝問題
- 第一次執行的預設現在會提供常見問題集中的 apt get 更新 udev 因應措施
- 啟用 DriveFs 中的符號連結 (於 /mnt/<drive>) 目錄
- 符號連結現在可 DriveFs 和 VolFs 之間
- 定址頂部層級路徑剖析的問題： ls。 / / 現在會如預期般運作
- npm 安裝上 DriveFs 和現在正設法-g 選項
- 已修正防止 PHP 伺服器啟動的問題
- 已更新的預設環境的值，例如更接近比對原生的 Ubuntu $PATH
- 更新 apt 套件快取的 Windows 中加入每週的維護工作
- ELF 標頭驗證修正問題，WSL 現在支援所有 Melkor 選項
- Zsh shell 正常運作
- 先行編譯的 Go 二進位檔現在支援
- 在第一次執行的 Bash.exe 提示是現在正確當地語系化
- /proc/meminfo 現在會傳回正確的資訊
- VFS 現可支援的通訊端
- /dev 現在已掛接為 tempfs
- Fifo 現在支援
- 多核心系統現在/proc/cpuinfo 中正確顯示
- 其他增強功能與在第一次執行期間所下載的錯誤訊息
- Syscall 改進和錯誤修正。 支援的 syscall 下方的清單。
- 其他錯誤修正和增強功能

### <a name="known-issues"></a>已知問題
- 無法解析 '.' 在某些情況下 DriveFs 上的正確

### <a name="syscall-support"></a>Syscall 支援
以下是某些實作在 WSL 的全新或加強 syscall 的清單。 在這份清單 syscall 支援在至少一個案例中，但可能不具有所有參數都支援這一次。

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

## <a name="build-14332"></a>建置 14332

一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14332)。 <br/>


### <a name="fixed"></a>固定式
- 改良的 resolv.conf 產生包括設定 DNS 項目優先順序
- 移動檔案和目錄，以及非 /mnt 之間的問題-/ /mnt 磁碟機
- 您現在可以使用符號連結建立 tar 檔案
- 在 建立執行個體上新增的預設 /run/lock 目錄
- 若要傳回適當的狀態資訊更新 /dev/null 時發生
- 下載期間第一次執行時的其他錯誤
- Syscall 改進和錯誤修正。 支援的 syscall 下方的清單。
- 其他改進錯誤修正和增強功能

### <a name="syscall-support"></a>Syscall 支援
以下是新 syscall WSL 中有某種實作。 在這份清單 syscall 在至少一個案例中，但可能不具有所有參數都支援這一次。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>組建 14328

一般 Windows 組建 14332 的詳細資訊請造訪[Windows 部落格](https://aka.ms/wip14328)。 <br/>


### <a name="new-features"></a>新功能
* 現在支援 Linux 使用者。  在 Windows 上 Ubuntu 上安裝 Bash 會提示輸入建立 Linux 使用者。  如需詳細資訊，請瀏覽 https://aka.ms/wslusers
* 主機名稱現在已不再設定為 Windows 電腦的名稱， @localhost
* 如需詳細資訊請組建 14328，請瀏覽： https://aka.ms/wip14328

### <a name="fixed"></a>固定式
* 非於 /mnt/ 的符號連結改進<drive>檔案
    * npm 安裝現在的運作方式
    * jdk 現在可安裝的 jre 使用指示[此處](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)。
    * 已知問題： 符號連結無法運作的 Windows 掛接。  功能可在更新的組建
* top 和 htop 現在會顯示
* 其他錯誤訊息，某些安裝失敗
* Syscall 改進和錯誤修正。  支援的 syscall 下方的清單。
* 其他改進錯誤修正和增強功能

### <a name="syscall-support"></a>Syscall 支援
以下是 syscall 的某些實作在 WSL 的清單。  Syscall 在這份清單中至少一個案例中，支援，但可能不具有所有參數都支援這一次。

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
