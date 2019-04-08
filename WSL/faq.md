---
title: 常見問題集 (FAQ)
description: Linux 的 Windows 子系統的相關常見問題集問題。
keywords: BashOnWindows、 bash、 wsl、 windows、 windowssubsystem、 常見問題集
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063266"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>適用於 Linux 常見問題集 Windows 子系統相關的問題

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>什麼是 Windows for Linux 子系統 (WSL)？
Windows for Linux 子系統 (WSL) 是新的 Windows 10 功能，可讓您直接在 Windows 上執行原生 Linux 命令列工具，以及傳統的 Windows 桌面和現代的市集應用程式。

請參閱[頁的相關](./about.md)如需詳細資訊。

## <a name="who-is-wsl-for"></a>針對 WSL 是誰？
這是主要是針對開發人員，特別是 web 開發人員和處理上或開放原始碼專案的任何人的工具。 這可讓人希望/需要使用 Bash，常見的 Linux 工具 (`sed`，`awk`等) 和許多 Linux 第一個工具 （Ruby、 Python 等） 在 Windows 上使用其工具鏈。

## <a name="what-can-i-do-with-wsl"></a>我可以 WSL 用來做什麼？
WSL 會提供應用程式呼叫 Bash.exe，啟動時，會開啟 Windows 主控台中執行 Bash 殼層。 使用 Bash，您可以執行 Linux 的命令列工具和應用程式。 例如，輸入`lsb_release -a`並按 enter 鍵; 您會看到目前正在執行的 Linux 散發版本的詳細資料：

![散發套件詳細資料的螢幕擷取畫面](media/distro.png)

您也可以存取您的本機電腦檔案系統從 Linux Bash 殼層中，您會發現您本機的磁碟機掛接在下`/mnt`資料夾。 例如，您`C:`下有掛接的磁碟機`/mnt/c`:  

![掛接的 C 磁碟機的螢幕擷取畫面](media/ls.png)

## <a name="what-is-bash"></a>Bash 的功能？
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是常用以文字為基礎的殼層和命令語言。 它是包含在 Ubuntu 和其他 Linux 散發版本，和在 macOS 中的預設殼層。 使用者會輸入到執行指令碼及/或執行命令與工具，來完成許多工作 shell 命令。

## <a name="how-does-this-work"></a>這是如何運作？
請查看我們[部落格](https://blogs.msdn.microsoft.com/wsl/)我們到基礎的技術詳細資料。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>為什麼我要使用 WSL，而不是 Linux VM 中？
WSL 需要比完整的虛擬機器較少的資源 （CPU、 記憶體和儲存體）。 WSL 也可讓您以執行 Linux 命令列工具和應用程式和 Windows 命令列中，桌面和市集應用程式，並存取您 Windows 中的檔案從 Linux。 這可讓您 Windows 應用程式和 Linux 命令列工具使用同一組檔案上，如果您想要。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>為什麼我要使用，比方說，而不是在 Windows 上的 Linux 上的 Ruby？
假設執行所在環境的行為類似 Linux，已建立一些跨平台工具。 比方說，某些工具會假設他們就能夠存取很長的檔案路徑或特定的檔案/資料夾存在。 這通常會導致問題在其通常運作方式的 Windows 上以不同的方式從 Linux。

諸如 Ruby 和節點的許多語言通常是移植到，，並在 Windows 上執行太棒了。 不過，並非所有的 Ruby Gem 或節點 /NPM 程式庫擁有者的連接埠他們的程式庫，以支援 Windows，且許多都有 Linux 特定的相依性。 這通常會導致系統使用這類的工具和程式庫，而組建和有時也會執行階段錯誤或不想要的行為，在 Windows 上建置。

這些只是一些造成許多人向 Microsoft 以協助改善 Windows 的命令列工具和功能驅使我們合作夥伴若要啟用原生 Bash 和 Linux 命令列工具在 Windows 上執行的 Canonical 的問題。

## <a name="what-does-this-mean-for-powershell"></a>這代表 PowerShell 的什麼？
同時使用 OSS 專案，有許多情況下，非常有用，並放入 Bash 從 PowerShell 提示字元。 Bash 支援互補，且可強化 Windows，讓 PowerShell 和 PowerShell 社群可充分利用其他受歡迎的技術的命令列的值。

閱讀的更多關於 PowerShell 小組部落格- [Bash for Windows:為何好極了，它表示適用於 PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>可以執行所有的 Linux 應用程式在 WSL 嗎？
不可能 ！ WSL 是工具，旨在讓需要它們來執行 Bash 和核心 Linux 命令列工具，在 Windows 上的使用者。 

沒有 WSL**不**目標是要支援 GUI 桌面或應用程式 （例如 Gnome，KDE 等等。）  

此外，即使您將能夠執行許多受歡迎的伺服器應用程式 (例如 Redis)，我們不建議用於裝載生產服務 WSL – Microsoft 提供各種解決方案在 Azure 中，執行 Linux 工作負載實際執行的 HYPER-V 和 Docker。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL 包含哪些 Windows Sku？
適用於 Linux 的 Windows 子系統可在桌上型電腦版本的 Windows for Windows 10 Anniversary 和 Creators update 或更新版本。

從開始 Fall Creators update WSL 會提供桌面及伺服器 Sku 的 Windows 上。

## <a name="what-processors-does-wsl-support"></a>WSL 支援哪些處理器？
WSL 支援 x64 和 ARM Cpu。

## <a name="how-do-i-access-my-c-drive"></a>如何存取我的 c： 磁碟機？
在本機電腦上的硬碟機的掛接點會自動建立和暺瘨謺髍 Windows 檔案系統。 
 
**於 /mnt/\<磁碟機代號 > /**
 
範例使用方式為`cd /mnt/c`存取 c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>如何搭配 Linux 應用程式中使用 Windows 檔案？

WSL 的好處之一能夠存取您的檔案，透過 Windows 和 Linux 應用程式或工具。 

WSL 掛接您的電腦下的固定磁碟機`/mnt/<drive>`在您的 Linux 散發版本的資料夾。 例如，您`C:`下有掛接的磁碟機 `/mnt/c/` 

使用您已掛接的磁碟機，您可以編輯程式碼中，例如`C:\dev\myproj\`使用[Visual Studio](https://visualstudio.microsoft.com/vs/) / 或[VS Code](https://code.visualstudio.com/)，以及建置/測試 Linux 中的程式碼存取相同的檔案，透過`\mnt\c\dev\myproj`。

> **重要事項**:其中一個使用 WSL 的主要限制是，不支援直接存取/變更您的 Linux 散發版本的檔案系統使用 Windows 應用程式或工具中的檔案。 請參閱：[不會變更使用 Windows 應用程式和工具的 Linux 檔案](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux 磁碟機中的檔案有不同於已掛接的 Windows 磁碟機？

1. 在 Linux 根目錄下的檔案 (也就是`/`) 所控制的 WSL 可以模擬 Linux 特定行為，包括但不是限於：
   * 檔案包含無效的 Windows 檔案名稱字元
   * 為非系統管理員使用者所建立的符號連結
   * 變更檔案屬性透過 chmod 和 chown
   * 區分大小寫的檔案/資料夾

2. 掛接的磁碟機中的檔案由 Windows 所控制，並具有下列行為：
   * 支援區分大小寫
   * 所有的權限是設為最能代表的 Windows 權限

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>為什麼有這麼多的錯誤時執行的 apt get 升級？
有些套件會使用我們尚未在尚未實作的功能。 `udev`比方說，尚未支援，而導致幾`apt-get upgrade`錯誤。

若要修正的相關問題`udev`，請遵循下列步驟：

1. 寫入下列命令以`/usr/sbin/policy-rc.d`並儲存變更。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 新增執行權限 `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 執行下列命令

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>如何解除安裝 WSL 發佈？

在建置之前 1709 (16299) 開啟命令提示字元，然後執行：
  ```batchfile
  lxrun /uninstall /full
  ```
  
應用程式磚上按一下滑鼠右鍵，然後按一下 解除安裝，或透過 PowerShell 使用，從市集安裝的 WSL 散發套件可以解除像任何其他 Windows 應用程式的安裝[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。

## <a name="why-does-ping-generate-permission-denied-errors"></a>為何要 ping 會產生權限遭拒錯誤？
在 WSL 建置 < 14926，ping 所需 WSL 透過提升權限的主控台執行。 在建置 14926 和更新版本，已修正此問題。

## <a name="how-do-i-run-an-openssh-server"></a>如何執行 OpenSSH 伺服器呢？
在 Windows 中的系統管理員權限，才能在 WSL 執行 OpenSSH。 若要執行的 OpenSSH 伺服器，在 Ubuntu 上執行 Bash，身為管理員，Windows 上，或從系統管理員權限的 CMD/PowerShell 提示字元執行 bash.exe。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>為什麼我會收到 「 錯誤：0x80040306 「 當我嘗試安裝嗎？
WSL 不支援在舊版的主控台中執行。 若要關閉舊版主控台：

1. 開啟 WSL、 PowerShell 或 Cmd
1. 以滑鼠右鍵按一下標題列]-> [屬性]-> [取消核取 [使用舊版主控台]
1. 按一下 [確定]

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>為什麼我會收到 「 錯誤：0x80040154 「 當我升級 Windows 之後，會在執行 bash.exe 時？
[Windows Linux 子系統] 功能可能會停用在 Windows 的更新。 如果發生這種情況則必須重新啟用 Windows 功能。 啟用 「 Windows Linux 子系統 」 功能的指示可在[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>如何變更顯示語言的 WSL？
WSL 安裝將會嘗試自動變更以符合您的 Windows 安裝的地區設定的 Ubuntu 地區設定。 如果不想讓此行為，您可以執行這個命令來安裝完成之後，變更 Ubuntu 地區設定。 您必須重新啟動 bash.exe 這項變更才會生效。

下列範例會變更為 EN-US 地區設定：
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>為什麼我沒有 WSL 從網際網路存取？
某些使用者有特定的防火牆應用程式封鎖網際網路存取，在 WSL 使用回報的問題。 報告在防火牆︰

1. Kaspersky
1. AVG
1. 太好了

在某些情況下關閉防火牆可供存取。 在某些情況下單純地安裝防火牆會封鎖其存取權。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>如何從 Windows 在 WSL 存取連接埠？
在 Windows 上執行時，WSL 會共用 Windows，IP 位址。 因此您可以存取在 localhost 上的任何連接埠例如如果您有 web 內容的通訊埠 1234，您可以在 https://localhost:1234到您的 Windows 瀏覽器。

## <a name="where-can-i-provide-feedback"></a>其中提供意見反應？

您可以分享意見並提出問題，透過多個管道：意見和問題應導向至：
* 我們[GitHub 問題追蹤程式](https://github.com/Microsoft/BashOnWindows/issues)
* 我們[命令列的 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* 我們[命令列的小組部落格](https://blogs.msdn.microsoft.com/commandline/)
* 透過 Twitter。 請遵循[ @richturn_ms ](https://twitter.com/richturn_MS)到 Twitter 以了解的新聞、 更新等等。
