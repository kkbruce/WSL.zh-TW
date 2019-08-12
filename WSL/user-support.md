---
title: Linux 使用者帳戶和許可權
說明: 適用於 Linux 的 Windows 子系統的使用者帳戶和版權管理的參考。
關鍵字: BashOnWindows、bash、wsl、windows、適用於 linux 的 windows 子系統、windowssubsystem、ubuntu、使用者帳戶
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040830"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>適用於 Linux 的 Windows 子系統的使用者帳戶和許可權

建立 Linux 使用者是在 WSL 上設定新的 Linux 散發套件的第一個步驟。 您所建立的第一個使用者帳戶會自動設定一些特殊屬性:

1. 這是您的預設使用者--它會在啟動時自動登入。
1. 預設為 Linux 系統管理員 (sudo 群組的成員)。

在適用於 Linux 的 Windows 子系統上執行的每個 Linux 散發套件都有自己的 Linux 使用者帳戶和密碼。 每當您新增散發、重新安裝或重設時, 都必須設定 Linux 使用者帳戶。 Linux 使用者帳戶不只是每個散發套件都獨立, 它們也獨立於您的 Windows 使用者帳戶。

## <a name="resetting-your-linux-password"></a>重設您的 Linux 密碼

如果您有 Linux 使用者帳戶的存取權, 並知道目前的密碼, 請使用該發佈的 Linux 密碼重設工具加以變更- `passwd`-最有可能。

如果這不是選項, 則視散發套件而定, 您可以藉由重設預設使用者來重設密碼。	

WSL 提供預設的使用者標記, 以識別當您啟動 WSL 時, 會自動登入的使用者帳戶。  由於許多發行版本都包含將預設使用者設定為 root 的命令, 以及未設定密碼的根使用者, 因此將預設使用者變更為 root 是很方便的工具, 可用於重設密碼等。

### <a name="for-creators-update-and-earlier"></a>適用於建立者更新和更早版本
如果您執行的是 Windows 10 建立者更新或更早的版本, 您可以執行下列命令來變更預設 Bash 使用者:

1. 將預設使用者變更為`root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 執行`bash.exe`以立即`root`登入:

    ```console
    C:\> bash.exe
    ```

1. 使用發佈的密碼命令重設您的密碼, 然後關閉 Linux 主控台:

    ```BASH
    $ passwd username
    $ exit
    ```

1. 從 Windows CMD, 將您的預設使用者重設回一般的 Linux 使用者帳戶:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>適用於秋季建立者更新和更新版本
若要查看哪些命令可用於特定的散發, 請`[distro.exe] /?`執行。
    
例如, 已安裝 Ubuntu:

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

使用 Ubuntu 的逐步指示:

1. 開啟 CMD
1. 將預設的 Linux 使用者設定為`root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. 啟動您的 Linux 散發`ubuntu`套件。您將會自動登入為`root`:

1. 使用命令重設您`passwd`的密碼:

    ```BASH
    $ passwd username
    ```

1. 從 Windows CMD, 將您的預設使用者重設回一般的 Linux 使用者帳戶。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permissions

在 WSL 中的許可權時, 有兩個重要的概念要謹記在心:

1. Windows 許可權模型可控制處理常式對 Windows 資源的許可權
2. Linux 許可權模型可控制處理常式對 Linux 資源的許可權

在 WSL 上執行 Linux 時, Linux 的 Windows 許可權會與啟動它的進程相同。 您可以在下列兩種許可權層級之一啟動 Linux:

* 一般 (未提高許可權):Linux 會以已登入使用者的許可權執行
* 提高許可權/系統管理員:使用提高許可權/管理 Windows 許可權執行 Linux

> 因為提高許可權的進程可以存取/修改 (因而損毀) 全系統的設定和全系統/受保護的資料, 除非您絕對需要, 否則請**避免**啟動提高許可權的進程 (不論它們是 Windows 或 Linux 應用程式/工具/)殼層!

上述 Windows 許可權與 Linux 執行個體內的許可權無關:Linux 「根許可權」只會影響使用者在 Linux 環境中的許可權 & filesystem;它們不會影響授與的 Windows 許可權。 因此, 以 root 身分執行 Linux 處理程序 (例如使用`sudo`) 只會授與該處理程序在 Linux 環境中的系統管理員許可權。

**範例：**     
具有 Windows 管理員許可權的 bash 會話可能會`cd /mnt/c/Users/Administrator`存取, 而沒有系統管理員許可權的 bash 會話會看到「許可權被拒」錯誤。

在 Linux 中, `sudo cd /mnt/c/Users/Administrator`因為 windows 中的許可權是由 windows 所管理, 所以輸入不會授與系統管理員目錄的存取權。

在 Linux 環境中, 如果使用者有以目前的 Linux 使用者為基礎的許可權, Linux 許可權模型就很重要。

**範例:**  
Sudo 群組中的使用者可能會執行`sudo apt update`。
