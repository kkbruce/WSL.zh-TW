---
title: Windows 與 Linux 的互通性
description: 說明在適用于 Linux 的 Windows 子系統上執行的 Linux 發行版本的 Windows 互通性。
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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="ab0bf-103">適用于 Linux 的 windows 子系統與 Windows 的互通性</span><span class="sxs-lookup"><span data-stu-id="ab0bf-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="ab0bf-104">**已針對秋季建立者更新進行更新。**</span><span class="sxs-lookup"><span data-stu-id="ab0bf-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="ab0bf-105">如果您執行的是「建立者更新」或「年度更新」, 請跳至 [建立[者/年度更新] 區段](interop.md#creators-update-and-anniversary-update)。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="ab0bf-106">適用于 Linux 的 Windows 子系統 (WSL) 會持續改善 Windows 和 Linux 之間的整合。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="ab0bf-107">您可以：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-107">You can:</span></span>

1. <span data-ttu-id="ab0bf-108">從 Linux 主控台叫用 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="ab0bf-109">從 Windows 主控台叫用 Linux 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="ab0bf-110">**Windows 測試人員組建 17063 +** 在 Linux 和 Windows 之間共用環境變數。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="ab0bf-111">這可在 Windows 和 WSL 之間提供順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="ab0bf-112">[WSL 的 blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)上有技術詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="ab0bf-113">從 Windows 命令列執行 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="ab0bf-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="ab0bf-114">使用`wsl.exe <command>`, 從 Windows 命令提示字元 (CMD 或 PowerShell) 執行 Linux 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="ab0bf-115">以這種方式叫用的二進位檔:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="ab0bf-116">使用與目前的 CMD 或 PowerShell 提示相同的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="ab0bf-117">以 WSL 預設使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="ab0bf-118">具有與呼叫進程和終端機相同的 Windows 系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="ab0bf-119">例如:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="ab0bf-120">下列`wsl.exe`的 Linux 命令會如同在 WSL 中執行的任何命令一樣處理。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="ab0bf-121">Sudo、管線和檔案重新導向等專案會運作。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="ab0bf-122">使用 sudo 的範例:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="ab0bf-123">混合 WSL 和 Windows 命令的範例:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="ab0bf-124">傳入的命令`wsl.exe`會轉送至 WSL 進程, 而不會進行修改。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="ab0bf-125">檔案路徑必須以 WSL 格式指定。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="ab0bf-126">具有路徑的範例:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="ab0bf-127">從 WSL 執行 Windows 工具</span><span class="sxs-lookup"><span data-stu-id="ab0bf-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="ab0bf-128">WSL 可以使用, 直接從 WSL 命令列叫用`[binary name].exe`Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="ab0bf-129">例如： `notepad.exe` 。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="ab0bf-130">為了讓 windows 可執行檔更容易執行, windows 路徑會包含在`$PATH` Linux 的秋季建立者更新中。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="ab0bf-131">以這種方式執行的應用程式具有下列屬性:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="ab0bf-132">將工作目錄保留為 WSL 命令提示字元 (大部分的例外狀況, 如下所述)。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="ab0bf-133">具有與 WSL 流程相同的許可權。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="ab0bf-134">以作用中的 Windows 使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="ab0bf-135">會顯示在 Windows 工作管理員中, 如同直接從命令提示字元執行一樣。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="ab0bf-136">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="ab0bf-137">在 WSL 中執行的 Windows 可執行檔的處理方式類似于原生 Linux 可執行檔--管線、重新導向, 甚至是背景處理如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="ab0bf-138">使用管道的範例:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="ab0bf-139">使用混合的 Windows 和 WSL 命令的範例:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="ab0bf-140">Windows 二進位檔必須包含副檔名、符合檔案大小寫, 而且必須是可執行檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="ab0bf-141">無法執行檔, 包括批次腳本。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="ab0bf-142">CMD 原生命令`dir` (例如) 可以`cmd.exe /C`使用命令來執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="ab0bf-143">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="ab0bf-144">參數會傳遞至未修改的 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="ab0bf-145">例如, 下列命令會在中`C:\temp\foo.txt` `notepad.exe`開啟:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="ab0bf-146">不支援使用 WSL 中的 Windows 應用程式`/mnt/<x>`修改位於 VolFs (不在下) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="ab0bf-147">根據預設, WSL 會嘗試將 Windows 二進位檔的工作目錄保留為目前的 WSL 目錄, 但是如果工作目錄是在 VolFs 上, 則會在實例建立目錄上回複。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="ab0bf-148">例如,最初是從`C:\temp`啟動, 而目前的 WSL 目錄變更為使用者的首頁。 `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="ab0bf-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="ab0bf-149">從`notepad.exe`使用者的主目錄呼叫時, WSL 會自動還原為`C:\temp` notepad.exe 工作目錄:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="ab0bf-150">在 Windows 和 WSL 之間共用環境變數</span><span class="sxs-lookup"><span data-stu-id="ab0bf-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="ab0bf-151">適用于 Windows 測試人員組建17063和更新版本。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="ab0bf-152">在17063之前, 只有 WSL 可以存取的 Windows 環境變數 was `PATH` (因此您可以從 WSL 下啟動 Win32 可執行檔)。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="ab0bf-153">從17063、WSL 和 Windows share `WSLENV`開始, 這是為了橋接在 WSL 上執行的 Windows 和 Linux 散發版本而建立的特殊環境變數。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="ab0bf-154">的`WSLENV`屬性:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="ab0bf-155">它是共用的;它存在於 Windows 和 WSL 環境中。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="ab0bf-156">這是要在 Windows 和 WSL 之間共用的環境變數清單。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="ab0bf-157">它可以將環境變數格式化, 以便在 Windows 和 WSL 中順利運作。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="ab0bf-158">中`WSLENV`有四個可用的旗標, 以影響該環境變數的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="ab0bf-159">`WSLENV`旗幟</span><span class="sxs-lookup"><span data-stu-id="ab0bf-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="ab0bf-160">`/p`-轉譯 WSL/Linux 樣式路徑和 Win32 路徑之間的路徑。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="ab0bf-161">`/l`-指出環境變數是路徑的清單。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="ab0bf-162">`/u`-表示在從 Win32 執行 WSL 時, 應該只包含此環境變數。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="ab0bf-163">`/w`-指出只有從 WSL 執行 Win32 時, 才應包含這個環境變數。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="ab0bf-164">旗標可以視需要結合。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="ab0bf-165">停用 Interop</span><span class="sxs-lookup"><span data-stu-id="ab0bf-165">Disable Interop</span></span>

<span data-ttu-id="ab0bf-166">使用者可以藉由以 root 身分執行下列命令, 停用對單一 WSL 會話執行 Windows 二進位檔的功能:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="ab0bf-167">若要重新啟用 Windows 二進位檔, 請結束所有 WSL 會話, 然後重新執行 bash, 或以 root 身分執行下列命令:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="ab0bf-168">停用 interop 不會在 WSL 會話之間保存, 當新的會話啟動時, 將會再次啟用 interop。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="ab0bf-169">建立者更新和周年年度更新</span><span class="sxs-lookup"><span data-stu-id="ab0bf-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="ab0bf-170">雖然互通性體驗的「建立者」建立者更新與最近的 interop 體驗類似, 但有幾個主要差異。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="ab0bf-171">總結:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-171">To summarize:</span></span>

* <span data-ttu-id="ab0bf-172">`bash.exe`已被取代, 並取代`wsl.exe`為。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="ab0bf-173">`-c`不需要`wsl.exe`執行單一命令的選項。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="ab0bf-174">Windows 路徑包含在 WSL 中`$PATH`</span><span class="sxs-lookup"><span data-stu-id="ab0bf-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="ab0bf-175">停用 interop 的進程不變。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="ab0bf-176">從 Windows 命令列叫用 WSL</span><span class="sxs-lookup"><span data-stu-id="ab0bf-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="ab0bf-177">您可以從 Windows 命令提示字元或 PowerShell 叫用 Linux 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="ab0bf-178">以這種方式叫用的二進位檔具有下列屬性:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="ab0bf-179">使用與 CMD 或 PowerShell 提示相同的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="ab0bf-180">以 WSL 預設使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="ab0bf-181">具有與呼叫進程和終端機相同的 Windows 系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="ab0bf-182">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="ab0bf-183">以這種方式呼叫的 Linux 命令會如同任何其他 Windows 應用程式般處理。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="ab0bf-184">輸入、管道和檔案重新導向等專案會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="ab0bf-185">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-185">Examples:</span></span>

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

<span data-ttu-id="ab0bf-186">傳入的 WSL 命令`bash -c`會轉送至 WSL 進程, 而不會進行修改。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="ab0bf-187">檔案路徑必須以 WSL 格式指定, 而且必須小心地將相關字元換成。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="ab0bf-188">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="ab0bf-189">從 WSL 叫用 Windows 二進位檔</span><span class="sxs-lookup"><span data-stu-id="ab0bf-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="ab0bf-190">適用于 Linux 的 Windows 子系統可以直接從 WSL 命令列叫用 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="ab0bf-191">以這種方式執行的應用程式具有下列屬性:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="ab0bf-192">保留工作目錄作為 WSL 命令提示字元, 但下列案例所述除外。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="ab0bf-193">具有與`bash.exe`進程相同的許可權。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="ab0bf-194">以作用中的 Windows 使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="ab0bf-195">會顯示在 Windows 工作管理員中, 如同直接從命令提示字元執行一樣。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="ab0bf-196">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="ab0bf-197">在 WSL 中, 這些可執行檔的處理方式類似于原生 Linux 可執行檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="ab0bf-198">這表示將目錄新增至 Linux 路徑, 而命令之間的管道則會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="ab0bf-199">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="ab0bf-200">Windows 二進位檔必須包含副檔名、符合檔案大小寫, 而且可以是可執行檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="ab0bf-201">無法執行檔, 包括批次腳本和`dir`命令 (例如) `/mnt/c/Windows/System32/cmd.exe /C`可以使用命令來執行。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="ab0bf-202">範例：</span><span class="sxs-lookup"><span data-stu-id="ab0bf-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="ab0bf-203">參數會傳遞至未修改的 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="ab0bf-204">例如, 下列命令會在中`C:\temp\foo.txt` `notepad.exe`開啟:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="ab0bf-205">不支援使用 Windows 應用程式修改位於 VolFs `/mnt/<x>`(不在下) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="ab0bf-206">根據預設, WSL 會嘗試將 Windows 二進位檔的工作目錄保留為目前的 WSL 目錄, 但是如果工作目錄是在 VolFs 上, 則會在實例建立目錄上回複。</span><span class="sxs-lookup"><span data-stu-id="ab0bf-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="ab0bf-207">例如,最初是從`C:\temp`啟動, 而目前的 WSL 目錄變更為使用者的首頁。 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="ab0bf-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="ab0bf-208">從`notepad.exe`使用者的主目錄呼叫時, WSL 會自動還原為`C:\temp` notepad.exe 工作目錄:</span><span class="sxs-lookup"><span data-stu-id="ab0bf-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
