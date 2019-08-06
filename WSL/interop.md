---
title: Windows 與 Linux 的互通性
description: 說明在適用於 Linux 的 Windows 子系統上執行的 Linux 發行版本的 Windows 互通性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040813"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>適用於 Linux 的 windows 子系統與 Windows 的互通性

> **已針對秋季建立者更新進行更新。**  
如果您執行的是「建立者更新」或「年度更新」, 請跳至 [建立者/年度更新區段](interop.md#creators-update-and-anniversary-update)。

適用於 Linux 的 Windows 子系統 (WSL) 會持續改善 Windows 和 Linux 之間的整合。  您可以：

1. 從 Linux 主控台叫用 Windows 二進位檔。
1. 從 Windows 主控台叫用 Linux 二進位檔。
1. **Windows 測試人員組建 17063 +** 在 Linux 和 Windows 之間共用環境變數。

這可在 Windows 和 WSL 之間提供順暢的體驗。  [WSL 的 blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)上有技術詳細資料。

## <a name="run-linux-tools-from-a-windows-command-line"></a>從 Windows 命令列執行 Linux 工具

使用`wsl.exe <command>`, 從 Windows 命令提示字元 (CMD 或 PowerShell) 執行 Linux 二進位檔。

以這種方式叫用的二進位檔:

1. 使用與目前的 CMD 或 PowerShell 提示相同的工作目錄。
1. 以 WSL 預設使用者身分執行。
1. 具有與呼叫程序和終端機相同的 Windows 系統管理許可權。

例如:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

下列`wsl.exe`的 Linux 命令會如同在 WSL 中執行的任何命令一樣處理。  Sudo、管線和檔案重新導向等專案會運作。

使用 sudo 的範例:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

混合 WSL 和 Windows 命令的範例:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

傳入的命令`wsl.exe`會轉送至 WSL 程序, 而不會進行修改。  檔案路徑必須以 WSL 格式指定。

具有路徑的範例:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>從 WSL 執行 Windows 工具

WSL 可以直接從 WSL 命令列`[binary name].exe`呼叫Windows 二進位檔。  例如： `notepad.exe` 。  為了讓 windows 可執行檔更容易執行, windows 路徑會包含在`$PATH` Linux 的秋季建立者更新中。

以這種方式執行的應用程式具有下列屬性:

1. 將工作目錄保留為 WSL 命令提示字元 (大部分的例外狀況, 如下所述)。
1. 具有與 WSL 流程相同的許可權。
1. 以作用中的 Windows 使用者身分執行。
1. 會顯示在 Windows 工作管理員中, 如同直接從命令提示字元執行一樣。

範例：

``` BASH
$ notepad.exe
```

在 WSL 中執行的 Windows 可執行檔的處理方式類似于原生 Linux 可執行檔--管線、重新導向, 甚至是背景處理如預期般運作。

使用管道的範例:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

使用混合的 Windows 和 WSL 命令的範例:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 二進位檔必須包含副檔名、符合檔案大小寫, 而且必須是可執行檔。  無法執行像是包括批次腳本等。  CMD 原生命令`dir` (例如) 可以`cmd.exe /C`使用命令來執行。

範例：

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

參數會傳遞至未修改的 Windows 二進位檔。

例如, 下列命令會在中`C:\temp\foo.txt` `notepad.exe`開啟:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支援使用 WSL 中的 Windows 應用程式修改位於 VolFs (檔案不位於`/mnt/<x>`) 的檔案。

根據預設, WSL 會嘗試將 Windows 二進位檔的工作目錄保留為目前的 WSL 目錄, 但是如果工作目錄是在 VolFs 上, 則會在實例上建立目錄上回複。

例如,最初是從`C:\temp`啟動, 而目前的 WSL 目錄變更為使用者的首頁。 `wsl.exe`  從`notepad.exe`使用者的主目錄呼叫時, WSL 會自動還原為`C:\temp` notepad.exe 工作目錄:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>在 Windows 和 WSL 之間共用環境變數

> 適用於 Windows 測試人員組建17063和更新版本。

在17063之前, 只有 WSL 可以存取的 Windows 環境變數 `PATH` (因此您可以從 WSL 下啟動 Win32 可執行檔)。

從17063、WSL 和 Windows share `WSLENV`開始, 這是為了橋接在 WSL 上執行的 Windows 和 Linux 發行版本而建立的特殊環境變數。

`WSLENV`的屬性:

* 它是共用的;它存在於 Windows 和 WSL 環境中。
* 這是要在 Windows 和 WSL 之間共用的環境變數清單。
* 它可以將環境變數格式化, 以便在 Windows 和 WSL 中順利運作。

`WSLENV`中有四個可用的旗標, 以影響該環境變數的轉譯方式。

`WSLENV`旗標

* `/p`-轉譯 WSL/Linux 樣式路徑和 Win32 路徑之間的路徑。
* `/l`-指出環境變數是路徑的清單。
* `/u`-表示在從 Win32 執行 WSL 時, 應該只包含此環境變數。
* `/w`-指出只有從 WSL 執行 Win32 時, 才應包含這個環境變數。

旗標可以視需要結合。

## <a name="disable-interop"></a>停用 Interop

使用者可以藉由以 root 身分執行下列命令, 停用對單一 WSL 會話執行 Windows 二進位檔的功能:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

若要重新啟用 Windows 二進位檔, 請結束所有 WSL 會話, 然後重新執行 bash, 或以 root 身分執行下列命令:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

停用 interop 不會在 WSL 會話之間保存, 當新的會話啟動時, 將會再次啟用 interop。

## <a name="creators-update-and-anniversary-update"></a>建立者更新和周年年度更新

雖然互通性體驗的「建立者」建立者更新與最近的 interop 體驗類似, 但有幾個主要差異。

總結:

* `bash.exe`已被取代, 並取代為`wsl.exe`。
* `-c`不需要`wsl.exe`執行單一命令的選項。
* Windows 路徑包含在 WSL 中`$PATH`

停用 interop 的程序不變。

### <a name="invoking-wsl-from-the-windows-command-line"></a>從 Windows 命令列叫用 WSL

您可以從 Windows 命令提示字元或 PowerShell 叫用 Linux 二進位檔。  以這種方式叫用的二進位檔具有下列屬性:

1. 使用與 CMD 或 PowerShell 提示相同的工作目錄。
1. 以 WSL 預設使用者身分執行。
1. 具有與呼叫程序和終端機相同的 Windows 系統管理許可權。

範例：

```console
C:\temp> bash -c "ls -la"
```

以這種方式呼叫的 Linux 命令會如同任何其他 Windows 應用程式般處理。  輸入、管道和檔案重新導向等專案會如預期般運作。

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

傳入的 WSL 命令`bash -c`會轉送至 WSL 程序, 而不會進行修改。  檔案路徑必須以 WSL 格式指定, 而且必須小心地將相關字元換成。 範例：

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>從 WSL 叫用 Windows 二進位檔

適用於 Linux 的 Windows 子系統可以直接從 WSL 命令列叫用 Windows 二進位檔。  以這種方式執行的應用程式具有下列屬性:

1. 保留工作目錄作為 WSL 命令提示字元, 但下列案例所述除外。
1. 具有與`bash.exe`程序相同的許可權。 
1. 以作用中的 Windows 使用者身分執行。
1. 會顯示在 Windows 工作管理員中, 如同直接從命令提示字元執行一樣。

範例：

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

在 WSL 中, 這些可執行檔的處理方式類似于原生 Linux 可執行檔。  這表示將目錄新增至 Linux 路徑, 而命令之間的管道則會如預期般運作。  範例：

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 二進位檔必須包含副檔名、符合檔案大小寫, 而且可以是可執行檔。  無法執行檔, 包括批次腳本和`dir`命令 (例如) `/mnt/c/Windows/System32/cmd.exe /C`可以使用命令來執行。

範例：

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

參數會傳遞至未修改的 Windows 二進位檔。  

例如, 下列命令會在中`C:\temp\foo.txt` `notepad.exe`開啟:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支援使用 Windows 應用程式修改位於 VolFs (檔案不位於`/mnt/<x>`) 的檔案。  根據預設, WSL 會嘗試將 Windows 二進位檔的工作目錄保留為目前的 WSL 目錄, 但是如果工作目錄是在 VolFs 上, 則會在實例上建立目錄上回複。

例如,最初是從`C:\temp`啟動, 而目前的 WSL 目錄變更為使用者的首頁。 `bash.exe`  從`notepad.exe`使用者的主目錄呼叫時, WSL 會自動還原為`C:\temp` notepad.exe 工作目錄:

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
