---
title: Windows 與 Linux 的互通性
description: 描述適用於 Linux 的 Windows 子系統上執行的 Linux 發行版本 Windows 的互通性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040813"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="24c43-103">Windows 與 Linux 互通性的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="24c43-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="24c43-104">**Fall Creators update 更新。**</span><span class="sxs-lookup"><span data-stu-id="24c43-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="24c43-105">如果您執行 Creators Update 或年度更新版，跳至[Creators/年度更新版 」 一節](interop.md#creators-update-and-anniversary-update)。</span><span class="sxs-lookup"><span data-stu-id="24c43-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="24c43-106">Windows for Linux 子系統 (WSL) 不斷致力改善 Windows 與 Linux 之間的整合。</span><span class="sxs-lookup"><span data-stu-id="24c43-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="24c43-107">您可以：</span><span class="sxs-lookup"><span data-stu-id="24c43-107">You can:</span></span>

1. <span data-ttu-id="24c43-108">叫用從 Linux 主控台的 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="24c43-109">叫用 Linux 的 Windows 主控台的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="24c43-110">**Windows Insiders 組建 17063 +** 共用 Linux 和 Windows 之間的環境變數。</span><span class="sxs-lookup"><span data-stu-id="24c43-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="24c43-111">這可提供 Windows 與 WSL 之間順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="24c43-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="24c43-112">技術詳細資料位於[WSL 部落格](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)。</span><span class="sxs-lookup"><span data-stu-id="24c43-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="24c43-113">從 Windows 命令列執行 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="24c43-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="24c43-114">從 Windows 命令提示字元 （CMD 或 PowerShell） 使用執行 Linux 的二進位檔`wsl.exe <command>`。</span><span class="sxs-lookup"><span data-stu-id="24c43-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="24c43-115">以這種方式叫用的二進位檔：</span><span class="sxs-lookup"><span data-stu-id="24c43-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="24c43-116">為目前的 CMD 或 PowerShell 提示字元中使用相同的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="24c43-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="24c43-117">WSL 預設使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="24c43-118">具有做為呼叫處理序和終端機相同的 Windows 系統管理權限。</span><span class="sxs-lookup"><span data-stu-id="24c43-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="24c43-119">例如:</span><span class="sxs-lookup"><span data-stu-id="24c43-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="24c43-120">Linux 命令下列`wsl.exe`處理像是在 WSL 中執行任何命令。</span><span class="sxs-lookup"><span data-stu-id="24c43-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="24c43-121">Sudo、 管道等檔案重新導向能正常運作。</span><span class="sxs-lookup"><span data-stu-id="24c43-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="24c43-122">使用 sudo 的範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="24c43-123">混用 WSL 與 Windows 命令的範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="24c43-124">命令傳遞至`wsl.exe`會轉送給 WSL 程序，而不需修改。</span><span class="sxs-lookup"><span data-stu-id="24c43-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="24c43-125">在 WSL 格式，就必須指定檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="24c43-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="24c43-126">路徑範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="24c43-127">WSL 從執行 Windows 的工具</span><span class="sxs-lookup"><span data-stu-id="24c43-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="24c43-128">WSL 可以叫用直接從 WSL 命令列中使用的 Windows 二進位檔`[binary name].exe`。</span><span class="sxs-lookup"><span data-stu-id="24c43-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="24c43-129">例如， `notepad.exe` 。</span><span class="sxs-lookup"><span data-stu-id="24c43-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="24c43-130">若要讓 Windows 可執行檔執行的工作變得更容易，Windows 中包含 Linux `$PATH` Fall Creators Update 中。</span><span class="sxs-lookup"><span data-stu-id="24c43-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="24c43-131">執行這種方式的應用程式具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="24c43-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="24c43-132">保留 WSL 命令提示字元中的工作目錄 （大部分的情況下，例外狀況會如下所述）。</span><span class="sxs-lookup"><span data-stu-id="24c43-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="24c43-133">具有相同的權限權限，為 WSL 程序。</span><span class="sxs-lookup"><span data-stu-id="24c43-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="24c43-134">作用中的 Windows 使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="24c43-135">在 Windows 工作管理員 中顯示如同直接從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="24c43-136">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="24c43-137">在 WSL 中執行的 Windows 可執行檔被處理方式類似原生 Linux 可執行檔，透過管道傳送，重新導向，以及如預期般運作，即使背景工作。</span><span class="sxs-lookup"><span data-stu-id="24c43-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="24c43-138">使用管道的範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="24c43-139">使用混合的 Windows 和 WSL 命令的範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="24c43-140">Windows 二進位檔必須包含副檔名、 檔案大小寫須相符，而且可執行檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="24c43-141">包括非可執行檔的批次指令碼。</span><span class="sxs-lookup"><span data-stu-id="24c43-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="24c43-142">例如 CMD 原生命令`dir`您可以執行`cmd.exe /C`命令。</span><span class="sxs-lookup"><span data-stu-id="24c43-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="24c43-143">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="24c43-144">參數會傳遞至未修改 Windows 二進位。</span><span class="sxs-lookup"><span data-stu-id="24c43-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="24c43-145">例如，下列命令會開啟`C:\temp\foo.txt`在`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="24c43-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="24c43-146">修改檔案放在 VolFs (不會在檔案`/mnt/<x>`) 與 Windows 不支援在 WSL 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="24c43-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="24c43-147">根據預設，WSL 會嘗試將 Windows 的工作目錄為目前的 WSL 目錄中，二進位，但是會切換回執行個體建立目錄的工作目錄是否位於 VolFs 上。</span><span class="sxs-lookup"><span data-stu-id="24c43-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="24c43-148">例如，`wsl.exe`最初從啟動`C:\temp`和目前的 WSL 目錄會變更使用者的首頁。</span><span class="sxs-lookup"><span data-stu-id="24c43-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="24c43-149">當`notepad.exe`會呼叫從使用者的主目錄時，WSL 會自動回復為`C:\temp`為 notepad.exe 工作目錄：</span><span class="sxs-lookup"><span data-stu-id="24c43-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="24c43-150">共用 WSL 與 Windows 環境變數</span><span class="sxs-lookup"><span data-stu-id="24c43-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="24c43-151">適用於 Windows 測試人員組建 17063 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="24c43-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="24c43-152">在之前 17063，只有 Windows 環境變數，可能會存取 WSL 是`PATH`（因此您無法啟動 WSL 底下的 Win32 可執行檔）。</span><span class="sxs-lookup"><span data-stu-id="24c43-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="24c43-153">從開始 17063，WSL 與 Windows 共用`WSLENV`，以橋接在 WSL 上執行的 Windows 和 Linux 散發版本建立的特殊環境變數。</span><span class="sxs-lookup"><span data-stu-id="24c43-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="24c43-154">屬性的`WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="24c43-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="24c43-155">它被共用;它存在於 Windows 和 WSL 環境。</span><span class="sxs-lookup"><span data-stu-id="24c43-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="24c43-156">它是以 Windows 和 WSL 之間共用的環境變數的清單。</span><span class="sxs-lookup"><span data-stu-id="24c43-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="24c43-157">它可以設定環境變數，以在 Windows 和 WSL 中正常運作的格式。</span><span class="sxs-lookup"><span data-stu-id="24c43-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="24c43-158">有四個旗標用於`WSLENV`影響轉譯該環境變數的方式。</span><span class="sxs-lookup"><span data-stu-id="24c43-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="24c43-159">`WSLENV` 旗標：</span><span class="sxs-lookup"><span data-stu-id="24c43-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="24c43-160">`/p` -將轉譯 WSL/Linux 樣式路徑和 Win32 路徑之間的路徑。</span><span class="sxs-lookup"><span data-stu-id="24c43-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="24c43-161">`/l` -表示環境變數路徑清單。</span><span class="sxs-lookup"><span data-stu-id="24c43-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="24c43-162">`/u` -表示這個環境變數只應包含從 Win32 執行 WSL 時。</span><span class="sxs-lookup"><span data-stu-id="24c43-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="24c43-163">`/w` -表示這個環境變數只應包含從 WSL 執行 Win32 時。</span><span class="sxs-lookup"><span data-stu-id="24c43-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="24c43-164">視需要可以結合旗標。</span><span class="sxs-lookup"><span data-stu-id="24c43-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="24c43-165">停用 Interop</span><span class="sxs-lookup"><span data-stu-id="24c43-165">Disable Interop</span></span>

<span data-ttu-id="24c43-166">使用者可能會停用單一 WSL 工作階段執行 Windows 二進位檔，藉由執行下列命令以 root 身分執行的能力：</span><span class="sxs-lookup"><span data-stu-id="24c43-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="24c43-167">若要重新啟用 Windows 二進位檔結束所有 WSL 工作階段和重新執行 bash.exe 或是以 root 身分執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="24c43-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="24c43-168">停用 interop 不會保存 WSL 工作階段之間--interop 時才會啟用一次啟動新的工作階段。</span><span class="sxs-lookup"><span data-stu-id="24c43-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="24c43-169">Creators Update 」 和 「 年度更新版</span><span class="sxs-lookup"><span data-stu-id="24c43-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="24c43-170">雖然 interop 體驗前 Fall Creators Update 也是較新的 interop 體驗類似，但有少數幾個主要的差異。</span><span class="sxs-lookup"><span data-stu-id="24c43-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="24c43-171">總結：</span><span class="sxs-lookup"><span data-stu-id="24c43-171">To summarize:</span></span>

* <span data-ttu-id="24c43-172">`bash.exe` 已被取代，並取代`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="24c43-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="24c43-173">`-c` 選項不需要執行單一命令`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="24c43-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="24c43-174">Windows 路徑包含在 WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="24c43-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="24c43-175">停用 interop 的程序不會變更。</span><span class="sxs-lookup"><span data-stu-id="24c43-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="24c43-176">從 Windows 命令列叫用 WSL</span><span class="sxs-lookup"><span data-stu-id="24c43-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="24c43-177">從 Windows 命令提示字元或 PowerShell，可以叫用 Linux 的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="24c43-178">以這種方式叫用的二進位檔具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="24c43-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="24c43-179">為 CMD 或 PowerShell 提示字元中使用相同的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="24c43-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="24c43-180">WSL 預設使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="24c43-181">具有做為呼叫處理序和終端機相同的 Windows 系統管理權限。</span><span class="sxs-lookup"><span data-stu-id="24c43-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="24c43-182">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="24c43-183">就像任何其他 Windows 應用程式處理這種方式呼叫的 Linux 命令。</span><span class="sxs-lookup"><span data-stu-id="24c43-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="24c43-184">項目，例如輸入、 管道及檔案重新導向正常運作。</span><span class="sxs-lookup"><span data-stu-id="24c43-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="24c43-185">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-185">Examples:</span></span>

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

<span data-ttu-id="24c43-186">WSL 命令傳遞至`bash -c`會轉送給 WSL 程序，而不需修改。</span><span class="sxs-lookup"><span data-stu-id="24c43-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="24c43-187">檔案路徑必須指定 WSL 格式，而且必須小心以逸出相關的字元。</span><span class="sxs-lookup"><span data-stu-id="24c43-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="24c43-188">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="24c43-189">叫用的 Windows 二進位檔案從 WSL</span><span class="sxs-lookup"><span data-stu-id="24c43-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="24c43-190">適用於 Linux 的 Windows 子系統可以叫用 Windows 二進位檔，直接從 WSL 命令列。</span><span class="sxs-lookup"><span data-stu-id="24c43-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="24c43-191">執行這種方式的應用程式具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="24c43-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="24c43-192">WSL 命令提示字元中除了下面所述的案例中為保留的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="24c43-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="24c43-193">具有相同的權限權限，為`bash.exe`程序。</span><span class="sxs-lookup"><span data-stu-id="24c43-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="24c43-194">作用中的 Windows 使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="24c43-195">在 Windows 工作管理員 中顯示如同直接從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="24c43-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="24c43-196">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="24c43-197">在 WSL，這些可執行檔被處理類似於原生 Linux 可執行檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="24c43-198">這表示將目錄新增至 Linux 路徑，並使用管線傳送之間命令運作如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="24c43-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="24c43-199">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="24c43-200">Windows 二進位檔必須包含副檔名、 檔案大小寫須相符，而且可執行檔。</span><span class="sxs-lookup"><span data-stu-id="24c43-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="24c43-201">包括非可執行檔的批次指令碼和命令等`dir`您可以執行`/mnt/c/Windows/System32/cmd.exe /C`命令。</span><span class="sxs-lookup"><span data-stu-id="24c43-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="24c43-202">範例：</span><span class="sxs-lookup"><span data-stu-id="24c43-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="24c43-203">參數會傳遞至未修改 Windows 二進位。</span><span class="sxs-lookup"><span data-stu-id="24c43-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="24c43-204">例如，下列命令會開啟`C:\temp\foo.txt`在`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="24c43-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="24c43-205">修改檔案放在 VolFs (不會在檔案`/mnt/<x>`) 不支援 with Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="24c43-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="24c43-206">根據預設，WSL 會嘗試保留 Windows 的工作目錄為目前的 WSL 目錄中，二進位，但是會切換回執行個體建立目錄的工作目錄是否位於 VolFs 上。</span><span class="sxs-lookup"><span data-stu-id="24c43-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="24c43-207">例如，`bash.exe`最初從啟動`C:\temp`和目前的 WSL 目錄會變更使用者的首頁。</span><span class="sxs-lookup"><span data-stu-id="24c43-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="24c43-208">當`notepad.exe`會呼叫從使用者的主目錄時，WSL 會自動回復為`C:\temp`為 notepad.exe 工作目錄：</span><span class="sxs-lookup"><span data-stu-id="24c43-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
