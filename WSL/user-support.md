---
title: Linux 使用者帳戶和權限
description: 使用者帳戶和權限管理適用於 Linux 的 Windows 子系統的參考。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 使用者帳戶的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063596"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>使用者帳戶和適用於 Linux 的 Windows 子系統的權限

建立您的 Linux 使用者是新的 Linux 散發套件在 WSL 上所設定的第一個步驟。  您所建立的第一個使用者帳戶會自動設定使用幾個特殊的屬性：

1. 是您預設的使用者--它登入時自動啟動。
1. 它是預設的 Linux 系統管理員 （sudo 群組的成員）。

適用於 Linux 的 Windows 子系統上執行的每個 Linux 散發套件都有自己的 Linux 使用者帳戶和密碼。  您必須設定的 Linux 使用者帳戶新增通訊群組、 重新安裝，或重設的任何時間。  Linux 使用者帳戶不是只有獨立每個散發，它們也是獨立於您的 Windows 使用者帳戶。

## <a name="resetting-your-linux-password"></a>重設 Linux 密碼

如果您可以存取您的 Linux 使用者帳戶，而且知道您目前的密碼，將它變更 linux 密碼重設工具，該分佈，最可能的`passwd`。

如果不是可行，根據散發套件，您可以藉由重設預設的使用者重設密碼。

WSL 會提供預設的使用者標記，來識別哪一個使用者帳戶自動登入，當您啟動 WSL。  由於許多散發套件包含根，也是以根使用者設定預設的使用者，且不需要密碼設定的命令，變更至根目錄的預設使用者是一個便利的工具，針對密碼重設等。

### <a name="for-creators-update-and-earlier"></a>Creators Update 及更早版本
如果您執行 Windows 10 Creators update 或更早版本，您可以變更預設 Bash 使用者執行下列命令：

1. 變更預設使用者`root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 執行`bash.exe`立即登入成`root`:

    ```console
    C:\> bash.exe
    ```

1. 重設密碼使用散發套件的 密碼 命令，並關閉 Linux 主控台：

    ```BASH
    $ passwd username
    $ exit
    ```

1. 從 Windows CMD 重設為一般 Linux 使用者帳戶的預設使用者：

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update 和更新版本
若要查看哪些命令可供特定的分佈，請執行`[distro.exe] /?`。
    
例如，使用 Ubuntu 安裝：

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

使用 Ubuntu 的逐步指示的步驟：

1. 開啟 CMD
1. 若要設定預設的 Linux 使用者`root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. 啟動您的 Linux 散發套件 (`ubuntu`)。  您會自動登入為`root`:

1. 重設您的密碼使用`passwd`命令：

    ```BASH
    $ passwd username
    ```

1. 從 Windows CMD 重設為一般 Linux 使用者帳戶的預設使用者。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permissions

有兩個重要的概念，要牢記在心，就在 WSL 的權限：

1. Windows 權限模型會控管 Windows 資源的處理序的權限
2. Linux 的權限模型控制 Linux 資源的處理序的權限

當 Linux 在 WSL 上執行，Linux 會有相同的 Windows 權限，其啟動的程序。 可以在其中兩個權限等級中啟動 Linux:

* 一般 （非提高權限）：Linux 執行的登入的使用者權限
* 提高權限/系統管理：以提高權限/系統管理員的 Windows 權限執行的 Linux

> 因為，提高權限處理程序可以變更/損毀的全系統設定和資料，和可存取/修改受保護的檔案和資料夾，**避免**啟動提高程序，除非絕對需要的時候-不論它們是 Windows 或Linux 應用程式/tools/殼層 ！

上述的 Windows 權限是獨立的中的 Linux 執行個體的權限：Linux 「 根權限 」 只會影響使用者的權限中的 Linux 環境與檔案系統;它們會將不會影響對授與 Windows 權限。 因此，以 root 身分執行 Linux 處理序 (例如，透過`sudo`) 只會處理在 Linux 環境中的系統管理員權限授與。

**範例：**    
Windows 系統管理員權限的 Bash 工作階段可以存取`cd /mnt/c/Users/Administrator`沒有系統管理員權限就會看到 「 拒絕的權限 」 的錯誤時的 Bash 工作階段。

在 Linux 中，輸入`sudo cd /mnt/c/Users/Administrator`由於 Windows 內的權限由 Windows，將會授與系統管理員的目錄的存取權。

Linux 的權限模型是很重要時，使用者已根據目前的 Linux 使用者的權限的 Linux 環境內。

**範例:**  
Sudo 群組中的使用者可以執行`sudo apt update`。
