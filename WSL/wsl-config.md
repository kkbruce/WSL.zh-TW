---
title: 管理 Linux 散發套件
description: 列出和設定適用於 Linux 的 Windows 子系統上執行的多個 Linux 發行版本的參考。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 wsl.conf、 wslconfig 的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063496"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和設定適用於 Linux 的 Windows 子系統

> 適用於 Windows 10 Fall Creators Update 和更新版本。  請參閱我們已更新[安裝指南](./install_guide.md)嘗試新的管理功能，並開始執行從 Windows 市集的多個 Linux 發行版本。

## <a name="ways-to-run-wsl"></a>如何執行 WSL

有許多方法可執行 Linux 的 Windows 子系統，適用於 Linux。

1. `[distro]` 亦即 `ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

您應該使用哪個方法取決於您的所作所為。

### <a name="launch-wsl-by-distribution"></a>啟動發佈 WSL

執行散發套件使用的散發套件專用應用程式會啟動該發佈它本身的主控台視窗中。

![從 [開始] 功能表啟動 WSL](media/start-launch.png)

它是不同於按一下 [啟動] 在 Windows 市集中。

![啟動從 Windows 市集的 WSL](media/store-launch.png)

您也可以執行從命令列發佈，藉由執行`[distribution].exe`。

從命令列，如此一來執行散發的缺點是，它會自動將變更您的工作目錄從目前的目錄來散發套件的主目錄。

**範例:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl 和 wsl [command]

若要從命令列執行 WSL 的最佳方式使用`wsl.exe`。

**範例:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

不但`wsl`就地保留目前的工作目錄，它可讓您執行單一命令，沿著端 Windows 命令。

**範例:**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**範例:**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>管理多個 Linux 發行版本

### <a name="windows-10-version-1903-and-later"></a>1903 和更新版本的 Windows 10 版本

您可以使用`wsl.exe`來管理您散發的 Windows 子系統中的 Linux (WSL)，包括列出可用的散發套件、 設定的預設發佈，以及解除安裝散發套件。

每個 Linux 散發套件會獨立管理它自己的組態。 若要查看特定散發的命令，請執行`[distro.exe] /?`。  例如 `ubuntu /?`。

#### <a name="list-distributions"></a>清單的散發套件

`wsl -l` , `wsl --list`  
列出可用於 WSL 的 Linux 散發套件。  如果列出的散發，它會安裝，且可供使用。

`wsl --list --all`   
列出所有的散發套件，包括不是目前可用的。  它們可能正在安裝，解除安裝，或處於中斷狀態。  

`wsl --list --running`   
列出目前正在執行的所有分佈。

#### <a name="set-a-default-distribution"></a>設定預設的通訊

預設的 WSL 通訊是當您執行時所執行`wsl`命令列上。

`wsl -s <DistributionName>`、 `wsl --setdefault <DistributionName>`

若要設定的預設分佈`<DistributionName>`。

**範例:**  
`wsl -s Ubuntu` 會將我的預設發佈設定到 Ubuntu。  現在，當我執行`wsl npm init`會在 Ubuntu 執行。  如果我執行`wsl`即會開啟 Ubuntu 工作階段。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消註冊再重新安裝散發

在 Linux 散發套件可透過 Windows 安裝時儲存，它們無法透過市集解除安裝。  WSL 組態可讓要取消註冊/解除安裝散發套件。

取消註冊時，也可讓重新安裝散發套件。

> **注意**：一旦取消註冊所有的資料、 設定以及與該發佈相關聯的軟體將會永久遺失。  從存放區重新安裝將會安裝全新的分佈。

`wsl --unregister <DistributionName>`  
取消註冊 WSL 散發，讓它能夠重新安裝或清除。

例如：`wsl -unregister Ubuntu`會將 Ubuntu 移除 WSL 中可用的散發套件。  當我執行`wsl --list`不會列出。

若要重新安裝，請在 Windows 市集尋找散發並選取 「 啟動 」。

#### <a name="run-as-a-specific-user"></a>以特定的使用者身分執行

`wsl -u <Username>`、 `wsl --user <Username>`

執行 WSL 成為指定的使用者。 請注意，使用者必須存在於 WSL 散發內。

#### <a name="run-a-specific-distribution"></a>執行特定的散發套件

`wsl --d <DistributionName>`、 `wsl --distribution <DistributionName>`

執行指定的 WSL 散發套件，可用來將命令傳送至特定的分佈，而不需要變更您的預設值。

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 版本 1903，之前的版本

WSL 組態 (`wslconfig.exe`) 是命令列工具來管理執行 Windows 子系統上的 Linux (WSL) 的 Linux 散發套件。  它可讓您列出可用的散發套件、 設定的預設散發，以及解除安裝散發套件。

範圍或協調散發套件的設定很有幫助 WSL 組態時，每個 Linux 散發套件會獨立管理它自己的組態。  若要查看特定散發的命令，請執行`[distro.exe] /?`。  例如 `ubuntu /?`。

若要查看所有可用的選項，如 wslconfig，請執行：  `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>清單的散發套件

`wslconfig /list`  
列出可用於 WSL 的 Linux 散發套件。  如果列出的散發，它會安裝，且可供使用。

`wslconfig /list /all`  
列出所有的散發套件，包括不是目前可用的。  它們可能正在安裝，解除安裝，或處於中斷狀態。  

#### <a name="set-a-default-distribution"></a>設定預設的通訊

預設的 WSL 通訊是當您執行時所執行`wsl`命令列上。

`wslconfig /setdefault <DistributionName>`

若要設定的預設分佈`<DistributionName>`。

**範例:**  
`wslconfig /setdefault Ubuntu` 會將我的預設發佈設定到 Ubuntu。  現在，當我執行`wsl npm init`會在 Ubuntu 執行。  如果我執行`wsl`即會開啟 Ubuntu 工作階段。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消註冊再重新安裝散發

在 Linux 散發套件可透過 Windows 安裝時儲存，它們無法透過市集解除安裝。  WSL 組態可讓要取消註冊/解除安裝散發套件。

取消註冊時，也可讓重新安裝散發套件。

> **注意**：一旦取消註冊所有的資料、 設定以及與該發佈相關聯的軟體將會永久遺失。  從存放區重新安裝將會安裝全新的分佈。

`wslconfig /unregister <DistributionName>`  
取消註冊 WSL 散發，讓它能夠重新安裝或清除。

例如：`wslconfig /unregister Ubuntu`會將 Ubuntu 移除 WSL 中可用的散發套件。  當我執行`wslconfig /list`不會列出。

若要重新安裝，請在 Windows 市集尋找散發並選取 「 啟動 」。

## <a name="set-wsl-launch-settings"></a>設定 WSL 啟動設定

> **可在 Windows Insider 組建 17093 及更新版本**

自動設定在 WSL 會在每次您啟動子系統使用套用的特定功能`wsl.conf`。 

權限，這包括自動掛接選項和網路設定。

`wsl.conf` 位於中每個 Linux 散發套件`/etc/wsl.conf`。 如果檔案不存在，您可以建立它自己。 WSL 會偵測檔案存在，並將讀取其內容。 如果檔案已遺失或格式不正確 （也就是不正確標記格式化），WSL 會繼續如往常啟動。

以下是範例`wsl.conf`您無法將它新增至您的散發套件的檔案：

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>組態選項

為了保持.ini 慣例，金鑰會宣告下一節。 

WSL 支援兩個區段：`automount`和`network`。

#### <a name="automount"></a>自動掛接

區段： `[automount]`


| key        | value                          | 預設值      | 附註                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` 固定磁碟機 （也就是原因 `C:/` 或是`D:/`) 會自動使用 DrvFs 下掛接`/mnt`。  `false` 表示將不會自動掛接磁碟機，但仍然無法裝載它們，以手動方式或透過`fstab`。                                                                                                             |
| mountFsTab | boolean                        | true         | `true` 設定`/etc/fstab`處理在 WSL 啟動。 /etc/fstab 是您可以在此宣告，請在其他檔案系統，例如 SMB 共用的檔案。 因此，您可以掛接這些檔案系統在 WSL 在啟動時自動註冊。                                                                                                                |
| 根目錄       | 字串                         | `/mnt/`      | 設定其中的固定磁碟機將會自動掛接的目錄。 例如，如果您有一個目錄中在 WSL`/windir/`和您指定，做為根，您會預期會看見您掛接於的固定磁碟機 `/windir/c`                                                                                              |
| 選項    | 以逗號分隔值清單 | 空字串 | 這個值會附加至預設 DrvFs 掛接選項字串。 **可以指定只有 DrvFs 特有的選項。** 不支援二進位掛接通常會剖析成旗標的選項。 如果您想要明確指定這些選項，您必須包含您要在 /etc/fstab 中這麼做的每個磁碟機。 |

根據預設，WSL 將 uid 與 gid 設為值的預設使用者 (在 Ubuntu 發行版本，預設的使用者會建立具有 uid = 1000，gid = 1000年)。 如果使用者指定的 gid 或 uid 選項明確地透過此機碼，相關聯的值會被覆寫。 否則將一律會附加的預設值。

**注意：** 這些選項會套用為所有的自動掛接磁碟機的掛接選項。 若要變更特定磁碟的選項，請改為使用 /etc/fstab。

#### <a name="network"></a>網路

區段標籤： `[network]`

| key | value | 預設值 | 附註|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` 設定產生 WSL `/etc/hosts`。 `hosts`檔案包含主機名稱對應的 IP 位址的靜態對應。 |
| generateResolvConf | boolean | `true` | `true` 設定產生 WSL `/etc/resolv.conf`。 `resolv.conf`包含 DNS 清單所能指定的主機名稱解析為其 IP 位址。 | 

#### <a name="interop"></a>Interop

區段標籤： `[interop]`

這些選項是用於測試人員組建 17713 和更新版本。

| key | value | 預設值 | 附註|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 此索引鍵的設定會決定是否支援 WSL 啟動 Windows 處理程序。 |
| appendWindowsPath | boolean | `true` | 此索引鍵的設定會判定 WSL 是否會將 Windows 路徑項目加入至 $PATH 環境變數。 | 
