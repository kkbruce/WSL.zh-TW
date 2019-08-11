---
title: 常見問題集 (FAQ)
description: 適用於 Linux 的 Windows 子系統常見問題集。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、常見問題
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237384"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>適用於 Linux 的 Windows 子系統常見問題集

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>什麼是適用於 Linux 的 Windows 子系統 (WSL)？
適用於 Linux 的 Windows 子系統 (WSL) 是新的 Windows 10 功能，可讓您直接在 Windows 上執行原生 Linux 命令列工具，以及傳統的 Windows 傳統型與新式 Store 應用程式。

如需詳細資訊, 請參閱[about 頁面](./about.md)。

## <a name="who-is-wsl-for"></a>WSL 適用於什麼人？
這主要是適用於開發人員的工具，特別是 Web 開發人員，以及那些處理或使用開放原始碼專案的人。 這可讓想要/需要使用 Bash、常見 Linux 工具 (`sed`、`awk` 等) 以及許多 Linux 優先工具 (Ruby、Python 等) 的人在 Windows 上使用其工具鏈。

## <a name="what-can-i-do-with-wsl"></a>我可以使用 WSL 來做什麼？
WSL 提供名為 Bash 的應用程式，當此應用程式啟動時，會開啟執行 Bash 殼層的 Windows 主控台。 使用 Bash，您可以執行命令列 Linux 工具和應用程式。 例如，輸入 `lsb_release -a` 並按 Enter：您將會看到目前正在執行之 Linux 發行版本的詳細資料：

![發行版本詳細資料的螢幕擷取畫面](media/distro.png)

您也可以從 Linux Bash 殼層存取您本機電腦的檔案系統 – 您將可以在 `/mnt` 資料夾下發現裝載的本機磁碟機。 例如，您的 `C:` 磁碟機裝載於 `/mnt/c` 下：  

![裝載的 C 磁片磁碟機螢幕擷取畫面](media/ls.png)

## <a name="what-is-bash"></a>什麼是 Bash？
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 是熱門的文字型殼層與命令語言。 它是包含在 Ubuntu 和其他 Linux 發行版本以及 macOS 中的預設殼層。 使用者在殼層中輸入命令來執行指令碼和/或執行命令和工具以完成許多工作。

## <a name="how-does-this-work"></a>這是如何運作？
查看我們的[blog](https://blogs.msdn.microsoft.com/wsl/) , 我們將詳細說明基礎技術。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>為什麼我會在 VM 中使用 WSL 而不是 Linux？
WSL 所需的資源 (CPU、記憶體和儲存體) 比完整虛擬機器少。 WSL 也可讓您同時執行 Linux 命令列工具和應用程式, 以及 Windows 命令列、桌面和存放區應用程式, 以及從 Linux 記憶體取您的 Windows 檔案。 這可讓您視需要在相同的檔案集合上使用 Windows 應用程式和 Linux 命令列工具。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>為什麼我會使用 Linux 上的 Ruby, 而不是 Windows 上的？
某些跨平臺工具的建立方式, 是假設它們執行的環境與 Linux 類似。 例如, 某些工具會假設它們能夠存取非常長的檔案路徑, 或特定檔案/資料夾存在。 這通常會導致 Windows 上的問題, 這通常會與 Linux 有不同的行為。

許多語言 (例如 Ruby 和 node) 通常會在 Windows 上移植並執行良好。 不過, 並非所有 Ruby Gem 或 node/NPM 程式庫擁有者都會移植其程式庫以支援 Windows, 而且許多都有 Linux 特定的相依性。 這通常會導致使用這類工具和程式庫所建立的系統, 在 Windows 上的組建和有時發生執行階段錯誤或不需要的行為。

這些只是導致許多人要求 Microsoft 改進 Windows 命令列工具的問題, 以及讓我們與標準夥伴合作, 以在 Windows 上執行原生 Bash 和 Linux 命令列工具。

## <a name="what-does-this-mean-for-powershell"></a>這對 PowerShell 有何意義？
使用 OSS 專案時, 在許多情況下, 從 PowerShell 提示字元拖放至 Bash 非常有用。 Bash 支援是互補的, 可強化 Windows 上的命令列價值, 讓 PowerShell 和 PowerShell 社區得以運用其他熱門技術。

深入瞭解 PowerShell 小組的 blog-- [適用于 Windows 的 Bash:為什麼它非常棒, 而對 PowerShell 的意義是什麼？](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>我可以在 WSL 中執行所有 Linux 應用程式嗎？
不！ WSL 是一種工具, 其目標是要讓需要他們的使用者在 Windows 上執行 Bash 和 core Linux 命令列工具。 

WSL 不是用來支援 GUI 桌上型電腦或應用程式 (例如 GNOME、KDE 等)  

此外, 即使您可以執行許多熱門的伺服器應用程式 (例如 Redis), 也不建議使用 WSL 來裝載生產服務– Microsoft 提供各種解決方案, 讓您在 Azure、Hyper-v 和 Docker 中執行生產 Linux 工作負載。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL 包含哪些 Windows Sku？
「適用於 Linux 的 Windows 子系統」可在 Windows 10 年度更新版和 Creators Update 或更新版本中的 Windows 電腦版本上找到。

從秋季建立者更新 WSL 將可在 Windows 的桌面和伺服器 Sku 上取得。

## <a name="what-processors-does-wsl-support"></a>WSL 支援哪些處理器？
WSL 支援 x64 和 ARM Cpu。

## <a name="how-do-i-access-my-c-drive"></a>如何? 存取我的 C: 磁片磁碟機嗎？
本機電腦上的硬碟掛接點會自動建立，並可讓您輕鬆存取 Windows 檔案系統。 
 
**于/mnt/\<磁碟機號 >/**
 
使用方法的範例`cd /mnt/c`是存取 c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>如何? 搭配 Linux 應用程式使用 Windows 檔案？

WSL 的其中一項優點是能夠透過 Windows 和 Linux 應用程式或工具存取您的檔案。 

WSL 會將您電腦的固定磁片磁碟機`/mnt/<drive>`掛接在 Linux 散發版本的資料夾底下。 例如, 您`C:`的磁片磁碟機裝載于`/mnt/c/` 

使用您載入的磁片磁碟機, 您可以在中編輯程式碼`C:\dev\myproj\` , 例如, 使用[Visual Studio](https://visualstudio.microsoft.com/vs/) /或[VS Code](https://code.visualstudio.com/), 然後透過存取相同`/mnt/c/dev/myproj`的檔案, 在 Linux 中建立/測試該程式碼。

> **重要注意事項**:使用 WSL 的其中一個主要限制是, 不支援使用 Windows 應用程式或工具直接存取/變更 Linux 散發版本檔案系統中的檔案。 請參閱：[不要使用 Windows 應用程式和工具變更 Linux 檔案](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux 磁片磁碟機中的檔案與裝載的 Windows 磁片磁碟機有何不同？

1. Linux 根目錄下的檔案 (亦即`/`) 是由模擬 linux 特定行為的 WSL 所控制, 包括但不限於:
   * 包含無效 Windows 檔案名字元的檔案
   * 為非系統管理員使用者建立的符號連結
   * 透過 chmod 和 chown 變更檔案屬性
   * 檔案/資料夾區分大小寫

2. 裝載的磁片磁碟機中的檔案是由 Windows 所控制, 並具有下列行為:
   * 支援區分大小寫
   * 擁有權限都設定為最佳反映 Windows 許可權

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>當我執行 apt 時, 為什麼會發生太多錯誤-取得升級？
有些套件會使用我們尚未實行的功能。 `udev`例如, 尚不支援, 而且會導致數`apt-get upgrade`個錯誤。

若要修正與相關`udev`的問題, 請遵循下列步驟:

1. 將下列`/usr/sbin/policy-rc.d`程式寫入並儲存您的變更。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 將執行許可權新增至`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 執行下列命令

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>如何? 卸載 WSL 散發套件嗎？

在 1709 (16299) 之前的組建上, 開啟命令提示字元並執行:
  ```batchfile
  lxrun /uninstall /full
  ```
  
從存放區安裝的 WSL 散發套件可以像任何其他 Windows 應用程式一樣卸載, 方法是以滑鼠右鍵按一下應用程式磚, 然後按一下 [卸載], 或透過 PowerShell 使用[ `Remove-AppxPackage` Cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。

## <a name="why-does-ping-generate-permission-denied-errors"></a>為什麼 ping 產生許可權被拒錯誤？
在 WSL 組建 < 14926 中, 透過提升許可權的主控台執行 ping 所需的 WSL。 此問題已在組建14926和更新版本中修正。

## <a name="how-do-i-run-an-openssh-server"></a>如何? 執行 OpenSSH 伺服器？
需要 Windows 中的系統管理員許可權, 才能在 WSL 中執行 OpenSSH。 若要執行 OpenSSH 伺服器, 請以系統管理員身分在 Windows 上的 Ubuntu 上執行 Bash, 或從具有系統管理員許可權的 CMD/PowerShell 提示字元執行 bash。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>為什麼會收到「錯誤:0x80040306 "當我嘗試安裝時？
WSL 不支援在舊版主控台中執行。 若要關閉舊版主控台:

1. 開啟 WSL、PowerShell 或 Cmd
1. 以滑鼠右鍵按一下標題列-> 屬性-> 取消核取 [使用舊版主控台]
1. 按一下 [確定]

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>為什麼會收到「錯誤:0x80040154 「在升級 Windows 之後執行 bash .exe 嗎？
「適用于 Linux 的 Windows 子系統」功能可能會在 Windows 更新期間停用。 如果發生這種情況, 則必須重新啟用 Windows 功能。 如需如何啟用「適用于 Linux 的 Windows 子系統」功能的指示, 請參閱[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>如何? 變更 WSL 的顯示語言？
WSL install 會嘗試自動變更 Ubuntu 地區設定, 以符合 Windows 安裝的地區設定。 如果您不想要此行為, 您可以執行此命令, 以在安裝完成後變更 Ubuntu 地區設定。 您必須重新開機 bash, 這種變更才會生效。

下列範例會將地區設定變更為 en-us:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>為什麼我無法從 WSL 存取網際網路？
某些使用者回報了在 WSL 中封鎖網際網路存取的特定防火牆應用程式問題。 回報的防火牆如下:

1. Kaspersky
1. AVG
1. Avast

在某些情況下, 關閉防火牆可讓您存取。 在某些情況下, 只安裝防火牆會顯示封鎖存取。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>如何? 從 Windows 中的 WSL 存取埠？
WSL 會共用 Windows 的 IP 位址, 因為它是在 Windows 上執行。 如此一來, 您就可以存取 localhost 上的任何埠, 例如, 如果您在埠 1234 https://localhost:1234 上有 web 內容, 您可以進入 Windows 瀏覽器。

## <a name="how-can-i-back-up-my-wsl-distros"></a>如何備份我的 WSL 散發版本？

備份散發版本的最佳方式是在 Windows 1809 版和更新版本中提供。 您可以使用`wsl --export`命令, 將整個散發匯出至 tarball。 接著, 您可以使用命令將`wsl --import`此散發版本匯回 WSL, 讓您可以備份和儲存 WSL 散發的狀態。 

請注意, 在 Appdata 資料夾 (例如 Windows Backup) 中備份檔案的傳統備份服務將不會損毀您的 Linux 檔案。 



## <a name="where-can-i-provide-feedback"></a>我可以在哪裡提供意見反應？

您可以透過多個管道來分享意見反應並提出問題:意見反應和問題應導向至:
* 我們的[GitHub 問題追蹤](https://github.com/Microsoft/BashOnWindows/issues)程式
* 我們[的命令列 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* 我們[的命令列小組 blog](https://blogs.msdn.microsoft.com/commandline/)
* 透過 Twitter。 請在[@richturn_ms](https://twitter.com/richturn_MS) Twitter 上追蹤以瞭解新聞、更新等等。
