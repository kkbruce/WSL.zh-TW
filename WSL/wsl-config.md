---
title: 管理 Linux 散發套件
description: 參考清單和設定在適用于 Linux 的 Windows 子系統上執行的多個 Linux 散發套件。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu、wsl、wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499274"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和設定適用于 Linux 的 Windows 子系統

> 適用于 Windows 10 秋季建立者更新和更新版本。  請參閱我們已更新的[安裝指南](./install_guide.md), 以試用新的管理功能, 並從 Microsoft store 開始執行多個 Linux 散發套件。

## <a name="ways-to-run-wsl"></a>執行 WSL 的方式

有許多方法可以使用適用于 Linux 的 Windows 子系統來執行 Linux。

1. `[distro]`, 例如`ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

您應該使用哪一種方法取決於您所執行的作業。

### <a name="launch-wsl-by-distribution"></a>依散發套件啟動 WSL

使用它的散發版本特定應用程式執行散發, 會在其自有的主控台視窗中啟動該散發。

![從 [開始] 功能表啟動 WSL](media/start-launch.png)

這與在 Microsoft store 中按一下 [啟動] 的方式相同。

![從 Microsoft store 啟動 WSL](media/store-launch.png)

您也可以執行, 從命令列`[distribution].exe`執行散發。

以這種方式從命令列執行發佈的缺點是, 它會自動將您的工作目錄從目前目錄變更為發佈的主目錄。

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

### <a name="wsl-and-wsl-command"></a>wsl 和 wsl [命令]

從命令列執行 WSL 的最佳方式是使用`wsl.exe`。

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

不僅會`wsl`將目前的工作目錄保留在原處, 還可讓您執行單一命令以及 Windows 命令。

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10 版本1903和更新版本

您可以使用`wsl.exe`在適用于 Linux 的 Windows 子系統 (WSL) 中管理您的散發套件, 包括列出可用的發行版本、設定預設發佈, 以及卸載發行版本。

每個 Linux 散發套件都會獨立管理自己的設定。 若要查看散發特定的命令, `[distro.exe] /?`請執行。  例如 `ubuntu /?`。

#### <a name="list-distributions"></a>列出發行版本

`wsl -l`,`wsl --list`  
列出可用的 Linux 散發套件, 可供 WSL。  如果已列出散發套件, 則會加以安裝並可供使用。

`wsl --list --all`   
列出所有發行版本, 包括目前無法使用的散發套件。  它們可能正在安裝、卸載或處於中斷狀態。  

`wsl --list --running`   
列出目前正在執行的所有發行版本。

#### <a name="set-a-default-distribution"></a>設定預設散發

預設 WSL 分佈是在命令列上執行`wsl`時所執行的散發。

`wsl -s <DistributionName>`、 `wsl --setdefault <DistributionName>`

將預設散發設定為`<DistributionName>`。

**範例:**  
`wsl -s Ubuntu`會將預設散發設定為 Ubuntu。  現在當我執行`wsl npm init`時, 它會在 Ubuntu 中執行。  如果我執行`wsl`它, 就會開啟 Ubuntu 會話。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消註冊並重新安裝散發套件

雖然 Linux 散發套件可透過 Microsoft store 安裝, 但無法透過存放區卸載。  WSL Config 允許取消註冊/卸載發行。

取消註冊也允許重新安裝發佈。

> **注意**：一旦取消註冊, 所有與該發佈相關聯的資料、設定和軟體都會永久遺失。  從存放區重新安裝將會安裝一份全新的散發套件。

`wsl --unregister <DistributionName>`  
從 WSL 取消註冊散發, 使其可以重新安裝或清除。

例如: `wsl --unregister Ubuntu`會從 WSL 中提供的散發套件中移除 Ubuntu。  當我執行`wsl --list`時, 將不會列出。

若要重新安裝, 請在 Microsoft store 中尋找發佈, 然後選取 [啟動]。

#### <a name="run-as-a-specific-user"></a>以特定使用者身分執行

`wsl -u <Username>`、 `wsl --user <Username>`

以指定的使用者身分執行 WSL。 請注意, 使用者必須存在於 WSL 散發內。

#### <a name="run-a-specific-distribution"></a>執行特定的散發套件

`wsl --d <DistributionName>`、 `wsl --distribution <DistributionName>`

執行指定的 WSL 散發, 可以用來將命令傳送至特定的散發, 而不需要變更預設值。

### <a name="versions-earlier-than-windows-10-version-1903"></a>早于 Windows 10 版本1903的版本

WSL Config (`wslconfig.exe`) 是一種命令列工具, 可用於管理在適用于 linux 的 Windows 子系統 (WSL) 上執行的 linux 發行版本。  它可讓您列出可用的發行版本、設定預設的散發, 以及卸載發行版本。

雖然 WSL Config 對於跨越或協調散發的設定很有説明, 但每個 Linux 散發套件會獨立管理自己的設定。  若要查看散發特定的命令, `[distro.exe] /?`請執行。  例如 `ubuntu /?`。

若要查看 wslconfig 的所有可用選項, 請執行:`wslconfig /?`

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

#### <a name="list-distributions"></a>列出發行版本

`wslconfig /list`  
列出可用的 Linux 散發套件, 可供 WSL。  如果已列出散發套件, 則會加以安裝並可供使用。

`wslconfig /list /all`  
列出所有發行版本, 包括目前無法使用的散發套件。  它們可能正在安裝、卸載或處於中斷狀態。  

#### <a name="set-a-default-distribution"></a>設定預設散發

預設 WSL 分佈是在命令列上執行`wsl`時所執行的散發。

`wslconfig /setdefault <DistributionName>`

將預設散發設定為`<DistributionName>`。

**範例:**  
`wslconfig /setdefault Ubuntu`會將預設散發設定為 Ubuntu。  現在當我執行`wsl npm init`時, 它會在 Ubuntu 中執行。  如果我執行`wsl`它, 就會開啟 Ubuntu 會話。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消註冊並重新安裝散發套件

雖然 Linux 散發套件可透過 Microsoft store 安裝, 但無法透過存放區卸載。  WSL Config 允許取消註冊/卸載發行。

取消註冊也允許重新安裝發佈。

> **注意**：一旦取消註冊, 所有與該發佈相關聯的資料、設定和軟體都會永久遺失。  從存放區重新安裝將會安裝一份全新的散發套件。

`wslconfig /unregister <DistributionName>`  
從 WSL 取消註冊散發, 使其可以重新安裝或清除。

例如: `wslconfig /unregister Ubuntu`會從 WSL 中提供的散發套件中移除 Ubuntu。  當我執行`wslconfig /list`時, 將不會列出。

若要重新安裝, 請在 Microsoft store 中尋找發佈, 然後選取 [啟動]。

## <a name="set-wsl-launch-settings"></a>設定 WSL 啟動設定

> **適用于 Windows 測試人員組建17093和更新版本**

會在每次使用`wsl.conf`啟動子系統時, 自動在 WSL 中設定特定功能。 

目前, 這包括自動掛接選項和網路設定。

`wsl.conf`位於中`/etc/wsl.conf`的每個 Linux 散發套件中。 如果檔案不存在, 您可以自行建立。 WSL 會偵測檔案是否存在, 並將讀取其內容。 如果檔案遺失或格式不正確 (也就是不正確的標記格式), WSL 會繼續正常啟動。

以下是您可以`wsl.conf`新增至散發版本的範例檔案:

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

### <a name="configuration-options"></a>設定選項

為了維持 .ini 慣例, 金鑰會在區段下宣告。 

WSL 支援兩個區段`automount` : `network`和。

#### <a name="automount"></a>裝載

截面`[automount]`


| key        | value                          | 預設值      | 紀錄                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`導致固定磁片磁碟機 (亦即 `C:/`或`D:/`), 以在`/mnt`底下自動裝載 DrvFs。  `false`表示磁片磁碟機不會自動掛接, 但您仍然可以手動或`fstab`透過來掛接它們。                                                                                                             |
| mountFsTab | boolean                        | true         | `true`要`/etc/fstab`在 WSL 開始時處理的集合。 /etc/fstab 是一個檔案, 您可以在其中宣告其他檔案系統, 例如 SMB 共用。 因此, 您可以在啟動時, 在 WSL 中自動掛接這些檔案系統。                                                                                                                |
| 路徑       | 字串                         | `/mnt/`      | 設定將自動掛接固定磁片磁碟機的目錄。 例如, 如果您在 WSL `/windir/`中有一個目錄, 並將它指定為根, 您應該會看到掛接于的固定磁片磁碟機`/windir/c`                                                                                              |
| 選項    | 以逗號分隔的值清單 | 空字串 | 此值會附加至預設的 DrvFs 掛接選項字串。 **只能指定 DrvFs 特有的選項。** 不支援掛接二進位檔通常會剖析成旗標的選項。 如果您想要明確指定這些選項, 必須在/etc/fstab 中包含您要執行此動作的每個磁片磁碟機 |

根據預設, WSL 會將 uid 和 gid 設定為預設使用者的值 (在 Ubuntu 散發版本中, 預設使用者是以 uid = 1000, gid = 1000) 來建立。 如果使用者透過這個機碼明確指定了 gid 或 uid 選項, 將會覆寫相關聯的值。 否則, 一律會附加預設值。

**注意：** 這些選項會套用為所有自動掛接之磁片磁碟機的掛接選項。 若只要變更特定磁片磁碟機的選項, 請改用/etc/fstab。

#### <a name="network"></a>網路

區段標籤:`[network]`

| key | value | 預設值 | 紀錄|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`設定要產生`/etc/hosts`的 WSL。 `hosts`檔案包含主機名稱對應的 IP 位址的靜態對應。 |
| generateResolvConf | boolean | `true` | `true`將 WSL 設定為`/etc/resolv.conf`[產生]。 `resolv.conf`包含可以將指定的主機名稱解析為其 IP 位址的 DNS 清單。 | 

#### <a name="interop"></a>互

區段標籤:`[interop]`

這些選項可在 Insider Build 17713 和更新版本中使用。

| key | value | 預設值 | 紀錄|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 設定此索引鍵將決定 WSL 是否將支援啟動 Windows 進程。 |
| appendWindowsPath | boolean | `true` | 設定此索引鍵將決定 WSL 是否會將 Windows path 元素新增至 $PATH 環境變數。 | 
