---
title: Windows 與 Linux 的互通性
description: 描述適用於 Linux 的 Windows 子系統上執行的 Linux 發行版本 Windows 的互通性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063246"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows 與 Linux 互通性的 Windows 子系統

> **Fall Creators update 更新。**  
如果您執行 Creators Update 或年度更新版，跳至[Creators/年度更新版 」 一節](interop.md#creators-update-and-anniversary-update)。

Windows for Linux 子系統 (WSL) 不斷致力改善 Windows 與 Linux 之間的整合。  您可以：

1. 叫用從 Linux 主控台的 Windows 二進位檔。
1. 叫用 Linux 的 Windows 主控台的二進位檔。
1. **Windows Insiders 組建 17063 +** 共用 Linux 和 Windows 之間的環境變數。

這可提供 Windows 與 WSL 之間順暢的體驗。  技術詳細資料位於[WSL 部落格](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)。

## <a name="run-linux-tools-from-a-windows-command-line"></a>從 Windows 命令列執行 Linux 工具

從 Windows 命令提示字元 （CMD 或 PowerShell） 使用執行 Linux 的二進位檔`wsl.exe <command>`。

以這種方式叫用的二進位檔：

1. 為目前的 CMD 或 PowerShell 提示字元中使用相同的工作目錄。
1. WSL 預設使用者身分執行。
1. 具有做為呼叫處理序和終端機相同的 Windows 系統管理權限。

例如: 

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Linux 命令下列`wsl.exe`處理像是在 WSL 中執行任何命令。  Sudo、 管道等檔案重新導向能正常運作。

使用 sudo 的範例：

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

混用 WSL 與 Windows 命令的範例：

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

命令傳遞至`wsl.exe`會轉送給 WSL 程序，而不需修改。  在 WSL 格式，就必須指定檔案路徑。

路徑範例：

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL 從執行 Windows 的工具

WSL 可以叫用直接從 WSL 命令列中使用的 Windows 二進位檔`[binary name].exe`。  例如， `notepad.exe` 。  若要讓 Windows 可執行檔執行的工作變得更容易，Windows 中包含 Linux `$PATH` Fall Creators Update 中。

執行這種方式的應用程式具有下列屬性：

1. 保留 WSL 命令提示字元中的工作目錄 （大部分的情況下，例外狀況會如下所述）。
1. 具有相同的權限權限，為 WSL 程序。
1. 作用中的 Windows 使用者身分執行。
1. 在 Windows 工作管理員 中顯示如同直接從命令提示字元執行。

範例：

``` BASH
$ notepad.exe
```

在 WSL 中執行的 Windows 可執行檔被處理方式類似原生 Linux 可執行檔，透過管道傳送，重新導向，以及如預期般運作，即使背景工作。

使用管道的範例：

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

使用混合的 Windows 和 WSL 命令的範例：

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 二進位檔必須包含副檔名、 檔案大小寫須相符，而且可執行檔。  包括非可執行檔的批次指令碼。  例如 CMD 原生命令`dir`您可以執行`cmd.exe /C`命令。

範例：

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

參數會傳遞至未修改 Windows 二進位。

例如，下列命令會開啟`C:\temp\foo.txt`在`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

修改檔案放在 VolFs (不會在檔案`/mnt/<x>`) 與 Windows 不支援在 WSL 的應用程式。

根據預設，WSL 會嘗試將 Windows 的工作目錄為目前的 WSL 目錄中，二進位，但是會切換回執行個體建立目錄的工作目錄是否位於 VolFs 上。

例如，`wsl.exe`最初從啟動`C:\temp`和目前的 WSL 目錄會變更使用者的首頁。  當`notepad.exe`會呼叫從使用者的主目錄時，WSL 會自動回復為`C:\temp`為 notepad.exe 工作目錄：

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>共用 WSL 與 Windows 環境變數

> 適用於 Windows 測試人員組建 17063 和更新版本。

在之前 17063，只有 Windows 環境變數，可能會存取 WSL 是`PATH`（因此您無法啟動 WSL 底下的 Win32 可執行檔）。

從開始 17063，WSL 與 Windows 共用`WSLENV`，以橋接在 WSL 上執行的 Windows 和 Linux 散發版本建立的特殊環境變數。

屬性的`WSLENV`:

* 它被共用;它存在於 Windows 和 WSL 環境。
* 它是以 Windows 和 WSL 之間共用的環境變數的清單。
* 它可以設定環境變數，以在 Windows 和 WSL 中正常運作的格式。

有四個旗標用於`WSLENV`影響轉譯該環境變數的方式。

`WSLENV` 旗標：

* `/p` -將轉譯 WSL/Linux 樣式路徑和 Win32 路徑之間的路徑。
* `/l` -表示環境變數路徑清單。
* `/u` -表示這個環境變數只應包含從 Win32 執行 WSL 時。
* `/w` -表示這個環境變數只應包含從 WSL 執行 Win32 時。

視需要可以結合旗標。

## <a name="disable-interop"></a>停用 Interop

使用者可能會停用單一 WSL 工作階段執行 Windows 二進位檔，藉由執行下列命令以 root 身分執行的能力：

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

若要重新啟用 Windows 二進位檔結束所有 WSL 工作階段和重新執行 bash.exe 或是以 root 身分執行下列命令：

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

停用 interop 不會保存 WSL 工作階段之間--interop 時才會啟用一次啟動新的工作階段。

## <a name="creators-update-and-anniversary-update"></a>Creators Update 」 和 「 年度更新版

雖然 interop 體驗前 Fall Creators Update 也是較新的 interop 體驗類似，但在 handfull 的主要差異。

總結：

* `bash.exe` 已被取代，並取代`wsl.exe`。
* `-c` 選項不需要執行單一命令`wsl.exe`。
* Windows 路徑包含在 WSL `$PATH`

停用 interop 的程序不會變更。

### <a name="invoking-wsl-from-the-windows-command-line"></a>從 Windows 命令列叫用 WSL

從 Windows 命令提示字元或 PowerShell，可以叫用 Linux 的二進位檔。  以這種方式叫用的二進位檔具有下列屬性：

1. 為 CMD 或 PowerShell 提示字元中使用相同的工作目錄。
1. WSL 預設使用者身分執行。
1. 具有做為呼叫處理序和終端機相同的 Windows 系統管理權限。

範例：

```console
C:\temp> bash -c "ls -la"
```

就像任何其他 Windows 應用程式處理這種方式呼叫的 Linux 命令。  項目，例如輸入、 管道及檔案重新導向正常運作。

範例：

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

WSL 命令傳遞至`bash -c`會轉送給 WSL 程序，而不需修改。  檔案路徑必須指定 WSL 格式，而且必須小心以逸出相關的字元。 範例：

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>叫用的 Windows 二進位檔案從 WSL

適用於 Linux 的 Windows 子系統可以叫用 Windows 二進位檔，直接從 WSL 命令列。  執行這種方式的應用程式具有下列屬性：

1. WSL 命令提示字元中除了下面所述的案例中為保留的工作目錄。
1. 具有相同的權限權限，為`bash.exe`程序。 
1. 作用中的 Windows 使用者身分執行。
1. 在 Windows 工作管理員 中顯示如同直接從命令提示字元執行。

範例：

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

在 WSL，這些可執行檔被處理類似於原生 Linux 可執行檔。  這表示將目錄新增至 Linux 路徑，並使用管線傳送之間命令運作如預期般運作。  範例：

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 二進位檔必須包含副檔名、 檔案大小寫須相符，而且可執行檔。  包括非可執行檔的批次指令碼和命令等`dir`您可以執行`/mnt/c/Windows/System32/cmd.exe /C`命令。

範例：

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

參數會傳遞至未修改 Windows 二進位。  

例如，下列命令會開啟`C:\temp\foo.txt`在`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

修改檔案放在 VolFs (不會在檔案`/mnt/<x>`) 不支援 with Windows 應用程式。  根據預設，WSL 會嘗試保留 Windows 的工作目錄為目前的 WSL 目錄中，二進位，但是會切換回執行個體建立目錄的工作目錄是否位於 VolFs 上。

例如，`bash.exe`最初從啟動`C:\temp`和目前的 WSL 目錄會變更使用者的首頁。  當`notepad.exe`會呼叫從使用者的主目錄時，WSL 會自動回復為`C:\temp`為 notepad.exe 工作目錄：

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
