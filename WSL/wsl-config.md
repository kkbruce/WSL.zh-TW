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
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="c7871-104">管理和設定適用于 Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="c7871-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="c7871-105">適用于 Windows 10 秋季建立者更新和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c7871-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="c7871-106">請參閱我們已更新的[安裝指南](./install_guide.md), 以試用新的管理功能, 並從 Microsoft store 開始執行多個 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="c7871-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="c7871-107">執行 WSL 的方式</span><span class="sxs-lookup"><span data-stu-id="c7871-107">Ways to run WSL</span></span>

<span data-ttu-id="c7871-108">有許多方法可以使用適用于 Linux 的 Windows 子系統來執行 Linux。</span><span class="sxs-lookup"><span data-stu-id="c7871-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="c7871-109">`[distro]`, 例如`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="c7871-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="c7871-110">`wsl.exe` 或 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="c7871-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="c7871-111">`wsl [command]` 或 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="c7871-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="c7871-112">您應該使用哪一種方法取決於您所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="c7871-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="c7871-113">依散發套件啟動 WSL</span><span class="sxs-lookup"><span data-stu-id="c7871-113">Launch WSL by distribution</span></span>

<span data-ttu-id="c7871-114">使用它的散發版本特定應用程式執行散發, 會在其自有的主控台視窗中啟動該散發。</span><span class="sxs-lookup"><span data-stu-id="c7871-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![從 [開始] 功能表啟動 WSL](media/start-launch.png)

<span data-ttu-id="c7871-116">這與在 Microsoft store 中按一下 [啟動] 的方式相同。</span><span class="sxs-lookup"><span data-stu-id="c7871-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![從 Microsoft store 啟動 WSL](media/store-launch.png)

<span data-ttu-id="c7871-118">您也可以執行, 從命令列`[distribution].exe`執行散發。</span><span class="sxs-lookup"><span data-stu-id="c7871-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="c7871-119">以這種方式從命令列執行發佈的缺點是, 它會自動將您的工作目錄從目前目錄變更為發佈的主目錄。</span><span class="sxs-lookup"><span data-stu-id="c7871-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="c7871-120">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="c7871-121">wsl 和 wsl [命令]</span><span class="sxs-lookup"><span data-stu-id="c7871-121">wsl and wsl [command]</span></span>

<span data-ttu-id="c7871-122">從命令列執行 WSL 的最佳方式是使用`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="c7871-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="c7871-123">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="c7871-124">不僅會`wsl`將目前的工作目錄保留在原處, 還可讓您執行單一命令以及 Windows 命令。</span><span class="sxs-lookup"><span data-stu-id="c7871-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="c7871-125">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-125">**Example:**</span></span>

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

<span data-ttu-id="c7871-126">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="c7871-127">管理多個 Linux 發行版本</span><span class="sxs-lookup"><span data-stu-id="c7871-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="c7871-128">Windows 10 版本1903和更新版本</span><span class="sxs-lookup"><span data-stu-id="c7871-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="c7871-129">您可以使用`wsl.exe`在適用于 Linux 的 Windows 子系統 (WSL) 中管理您的散發套件, 包括列出可用的發行版本、設定預設發佈, 以及卸載發行版本。</span><span class="sxs-lookup"><span data-stu-id="c7871-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="c7871-130">每個 Linux 散發套件都會獨立管理自己的設定。</span><span class="sxs-lookup"><span data-stu-id="c7871-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="c7871-131">若要查看散發特定的命令, `[distro.exe] /?`請執行。</span><span class="sxs-lookup"><span data-stu-id="c7871-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="c7871-132">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="c7871-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="c7871-133">列出發行版本</span><span class="sxs-lookup"><span data-stu-id="c7871-133">List distributions</span></span>

<span data-ttu-id="c7871-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="c7871-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="c7871-135">列出可用的 Linux 散發套件, 可供 WSL。</span><span class="sxs-lookup"><span data-stu-id="c7871-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="c7871-136">如果已列出散發套件, 則會加以安裝並可供使用。</span><span class="sxs-lookup"><span data-stu-id="c7871-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="c7871-137">列出所有發行版本, 包括目前無法使用的散發套件。</span><span class="sxs-lookup"><span data-stu-id="c7871-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="c7871-138">它們可能正在安裝、卸載或處於中斷狀態。</span><span class="sxs-lookup"><span data-stu-id="c7871-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="c7871-139">列出目前正在執行的所有發行版本。</span><span class="sxs-lookup"><span data-stu-id="c7871-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="c7871-140">設定預設散發</span><span class="sxs-lookup"><span data-stu-id="c7871-140">Set a default distribution</span></span>

<span data-ttu-id="c7871-141">預設 WSL 分佈是在命令列上執行`wsl`時所執行的散發。</span><span class="sxs-lookup"><span data-stu-id="c7871-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="c7871-142">`wsl -s <DistributionName>`、 `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="c7871-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="c7871-143">將預設散發設定為`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="c7871-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="c7871-144">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-144">**Example:**</span></span>  
<span data-ttu-id="c7871-145">`wsl -s Ubuntu`會將預設散發設定為 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="c7871-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="c7871-146">現在當我執行`wsl npm init`時, 它會在 Ubuntu 中執行。</span><span class="sxs-lookup"><span data-stu-id="c7871-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="c7871-147">如果我執行`wsl`它, 就會開啟 Ubuntu 會話。</span><span class="sxs-lookup"><span data-stu-id="c7871-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="c7871-148">取消註冊並重新安裝散發套件</span><span class="sxs-lookup"><span data-stu-id="c7871-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="c7871-149">雖然 Linux 散發套件可透過 Microsoft store 安裝, 但無法透過存放區卸載。</span><span class="sxs-lookup"><span data-stu-id="c7871-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="c7871-150">WSL Config 允許取消註冊/卸載發行。</span><span class="sxs-lookup"><span data-stu-id="c7871-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="c7871-151">取消註冊也允許重新安裝發佈。</span><span class="sxs-lookup"><span data-stu-id="c7871-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="c7871-152">**注意**：一旦取消註冊, 所有與該發佈相關聯的資料、設定和軟體都會永久遺失。</span><span class="sxs-lookup"><span data-stu-id="c7871-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="c7871-153">從存放區重新安裝將會安裝一份全新的散發套件。</span><span class="sxs-lookup"><span data-stu-id="c7871-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="c7871-154">從 WSL 取消註冊散發, 使其可以重新安裝或清除。</span><span class="sxs-lookup"><span data-stu-id="c7871-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="c7871-155">例如: `wsl --unregister Ubuntu`會從 WSL 中提供的散發套件中移除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="c7871-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="c7871-156">當我執行`wsl --list`時, 將不會列出。</span><span class="sxs-lookup"><span data-stu-id="c7871-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="c7871-157">若要重新安裝, 請在 Microsoft store 中尋找發佈, 然後選取 [啟動]。</span><span class="sxs-lookup"><span data-stu-id="c7871-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="c7871-158">以特定使用者身分執行</span><span class="sxs-lookup"><span data-stu-id="c7871-158">Run as a specific user</span></span>

<span data-ttu-id="c7871-159">`wsl -u <Username>`、 `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="c7871-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="c7871-160">以指定的使用者身分執行 WSL。</span><span class="sxs-lookup"><span data-stu-id="c7871-160">Run WSL as the specified user.</span></span> <span data-ttu-id="c7871-161">請注意, 使用者必須存在於 WSL 散發內。</span><span class="sxs-lookup"><span data-stu-id="c7871-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="c7871-162">執行特定的散發套件</span><span class="sxs-lookup"><span data-stu-id="c7871-162">Run a specific distribution</span></span>

<span data-ttu-id="c7871-163">`wsl --d <DistributionName>`、 `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="c7871-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="c7871-164">執行指定的 WSL 散發, 可以用來將命令傳送至特定的散發, 而不需要變更預設值。</span><span class="sxs-lookup"><span data-stu-id="c7871-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="c7871-165">早于 Windows 10 版本1903的版本</span><span class="sxs-lookup"><span data-stu-id="c7871-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="c7871-166">WSL Config (`wslconfig.exe`) 是一種命令列工具, 可用於管理在適用于 linux 的 Windows 子系統 (WSL) 上執行的 linux 發行版本。</span><span class="sxs-lookup"><span data-stu-id="c7871-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="c7871-167">它可讓您列出可用的發行版本、設定預設的散發, 以及卸載發行版本。</span><span class="sxs-lookup"><span data-stu-id="c7871-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="c7871-168">雖然 WSL Config 對於跨越或協調散發的設定很有説明, 但每個 Linux 散發套件會獨立管理自己的設定。</span><span class="sxs-lookup"><span data-stu-id="c7871-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="c7871-169">若要查看散發特定的命令, `[distro.exe] /?`請執行。</span><span class="sxs-lookup"><span data-stu-id="c7871-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="c7871-170">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="c7871-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="c7871-171">若要查看 wslconfig 的所有可用選項, 請執行:`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="c7871-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="c7871-172">列出發行版本</span><span class="sxs-lookup"><span data-stu-id="c7871-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="c7871-173">列出可用的 Linux 散發套件, 可供 WSL。</span><span class="sxs-lookup"><span data-stu-id="c7871-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="c7871-174">如果已列出散發套件, 則會加以安裝並可供使用。</span><span class="sxs-lookup"><span data-stu-id="c7871-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="c7871-175">列出所有發行版本, 包括目前無法使用的散發套件。</span><span class="sxs-lookup"><span data-stu-id="c7871-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="c7871-176">它們可能正在安裝、卸載或處於中斷狀態。</span><span class="sxs-lookup"><span data-stu-id="c7871-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="c7871-177">設定預設散發</span><span class="sxs-lookup"><span data-stu-id="c7871-177">Set a default distribution</span></span>

<span data-ttu-id="c7871-178">預設 WSL 分佈是在命令列上執行`wsl`時所執行的散發。</span><span class="sxs-lookup"><span data-stu-id="c7871-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="c7871-179">將預設散發設定為`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="c7871-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="c7871-180">**範例:**</span><span class="sxs-lookup"><span data-stu-id="c7871-180">**Example:**</span></span>  
<span data-ttu-id="c7871-181">`wslconfig /setdefault Ubuntu`會將預設散發設定為 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="c7871-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="c7871-182">現在當我執行`wsl npm init`時, 它會在 Ubuntu 中執行。</span><span class="sxs-lookup"><span data-stu-id="c7871-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="c7871-183">如果我執行`wsl`它, 就會開啟 Ubuntu 會話。</span><span class="sxs-lookup"><span data-stu-id="c7871-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="c7871-184">取消註冊並重新安裝散發套件</span><span class="sxs-lookup"><span data-stu-id="c7871-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="c7871-185">雖然 Linux 散發套件可透過 Microsoft store 安裝, 但無法透過存放區卸載。</span><span class="sxs-lookup"><span data-stu-id="c7871-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="c7871-186">WSL Config 允許取消註冊/卸載發行。</span><span class="sxs-lookup"><span data-stu-id="c7871-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="c7871-187">取消註冊也允許重新安裝發佈。</span><span class="sxs-lookup"><span data-stu-id="c7871-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="c7871-188">**注意**：一旦取消註冊, 所有與該發佈相關聯的資料、設定和軟體都會永久遺失。</span><span class="sxs-lookup"><span data-stu-id="c7871-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="c7871-189">從存放區重新安裝將會安裝一份全新的散發套件。</span><span class="sxs-lookup"><span data-stu-id="c7871-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="c7871-190">從 WSL 取消註冊散發, 使其可以重新安裝或清除。</span><span class="sxs-lookup"><span data-stu-id="c7871-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="c7871-191">例如: `wslconfig /unregister Ubuntu`會從 WSL 中提供的散發套件中移除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="c7871-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="c7871-192">當我執行`wslconfig /list`時, 將不會列出。</span><span class="sxs-lookup"><span data-stu-id="c7871-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="c7871-193">若要重新安裝, 請在 Microsoft store 中尋找發佈, 然後選取 [啟動]。</span><span class="sxs-lookup"><span data-stu-id="c7871-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="c7871-194">設定 WSL 啟動設定</span><span class="sxs-lookup"><span data-stu-id="c7871-194">Set WSL launch settings</span></span>

> <span data-ttu-id="c7871-195">**適用于 Windows 測試人員組建17093和更新版本**</span><span class="sxs-lookup"><span data-stu-id="c7871-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="c7871-196">會在每次使用`wsl.conf`啟動子系統時, 自動在 WSL 中設定特定功能。</span><span class="sxs-lookup"><span data-stu-id="c7871-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="c7871-197">目前, 這包括自動掛接選項和網路設定。</span><span class="sxs-lookup"><span data-stu-id="c7871-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="c7871-198">`wsl.conf`位於中`/etc/wsl.conf`的每個 Linux 散發套件中。</span><span class="sxs-lookup"><span data-stu-id="c7871-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="c7871-199">如果檔案不存在, 您可以自行建立。</span><span class="sxs-lookup"><span data-stu-id="c7871-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="c7871-200">WSL 會偵測檔案是否存在, 並將讀取其內容。</span><span class="sxs-lookup"><span data-stu-id="c7871-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="c7871-201">如果檔案遺失或格式不正確 (也就是不正確的標記格式), WSL 會繼續正常啟動。</span><span class="sxs-lookup"><span data-stu-id="c7871-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="c7871-202">以下是您可以`wsl.conf`新增至散發版本的範例檔案:</span><span class="sxs-lookup"><span data-stu-id="c7871-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="c7871-203">設定選項</span><span class="sxs-lookup"><span data-stu-id="c7871-203">Configuration Options</span></span>

<span data-ttu-id="c7871-204">為了維持 .ini 慣例, 金鑰會在區段下宣告。</span><span class="sxs-lookup"><span data-stu-id="c7871-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="c7871-205">WSL 支援兩個區段`automount` : `network`和。</span><span class="sxs-lookup"><span data-stu-id="c7871-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="c7871-206">裝載</span><span class="sxs-lookup"><span data-stu-id="c7871-206">automount</span></span>

<span data-ttu-id="c7871-207">截面`[automount]`</span><span class="sxs-lookup"><span data-stu-id="c7871-207">Section: `[automount]`</span></span>


| <span data-ttu-id="c7871-208">key</span><span class="sxs-lookup"><span data-stu-id="c7871-208">key</span></span>        | <span data-ttu-id="c7871-209">value</span><span class="sxs-lookup"><span data-stu-id="c7871-209">value</span></span>                          | <span data-ttu-id="c7871-210">預設值</span><span class="sxs-lookup"><span data-stu-id="c7871-210">default</span></span>      | <span data-ttu-id="c7871-211">紀錄</span><span class="sxs-lookup"><span data-stu-id="c7871-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7871-212">enabled</span><span class="sxs-lookup"><span data-stu-id="c7871-212">enabled</span></span>    | <span data-ttu-id="c7871-213">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-213">boolean</span></span>                        | <span data-ttu-id="c7871-214">true</span><span class="sxs-lookup"><span data-stu-id="c7871-214">true</span></span>         | <span data-ttu-id="c7871-215">`true`導致固定磁片磁碟機 (亦即</span><span class="sxs-lookup"><span data-stu-id="c7871-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="c7871-216">`C:/`或`D:/`), 以在`/mnt`底下自動裝載 DrvFs。</span><span class="sxs-lookup"><span data-stu-id="c7871-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="c7871-217">`false`表示磁片磁碟機不會自動掛接, 但您仍然可以手動或`fstab`透過來掛接它們。</span><span class="sxs-lookup"><span data-stu-id="c7871-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="c7871-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="c7871-218">mountFsTab</span></span> | <span data-ttu-id="c7871-219">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-219">boolean</span></span>                        | <span data-ttu-id="c7871-220">true</span><span class="sxs-lookup"><span data-stu-id="c7871-220">true</span></span>         | <span data-ttu-id="c7871-221">`true`要`/etc/fstab`在 WSL 開始時處理的集合。</span><span class="sxs-lookup"><span data-stu-id="c7871-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="c7871-222">/etc/fstab 是一個檔案, 您可以在其中宣告其他檔案系統, 例如 SMB 共用。</span><span class="sxs-lookup"><span data-stu-id="c7871-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="c7871-223">因此, 您可以在啟動時, 在 WSL 中自動掛接這些檔案系統。</span><span class="sxs-lookup"><span data-stu-id="c7871-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="c7871-224">路徑</span><span class="sxs-lookup"><span data-stu-id="c7871-224">root</span></span>       | <span data-ttu-id="c7871-225">字串</span><span class="sxs-lookup"><span data-stu-id="c7871-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="c7871-226">設定將自動掛接固定磁片磁碟機的目錄。</span><span class="sxs-lookup"><span data-stu-id="c7871-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="c7871-227">例如, 如果您在 WSL `/windir/`中有一個目錄, 並將它指定為根, 您應該會看到掛接于的固定磁片磁碟機`/windir/c`</span><span class="sxs-lookup"><span data-stu-id="c7871-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="c7871-228">選項</span><span class="sxs-lookup"><span data-stu-id="c7871-228">options</span></span>    | <span data-ttu-id="c7871-229">以逗號分隔的值清單</span><span class="sxs-lookup"><span data-stu-id="c7871-229">comma-separated list of values</span></span> | <span data-ttu-id="c7871-230">空字串</span><span class="sxs-lookup"><span data-stu-id="c7871-230">empty string</span></span> | <span data-ttu-id="c7871-231">此值會附加至預設的 DrvFs 掛接選項字串。</span><span class="sxs-lookup"><span data-stu-id="c7871-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="c7871-232">**只能指定 DrvFs 特有的選項。**</span><span class="sxs-lookup"><span data-stu-id="c7871-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="c7871-233">不支援掛接二進位檔通常會剖析成旗標的選項。</span><span class="sxs-lookup"><span data-stu-id="c7871-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="c7871-234">如果您想要明確指定這些選項, 必須在/etc/fstab 中包含您要執行此動作的每個磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="c7871-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="c7871-235">根據預設, WSL 會將 uid 和 gid 設定為預設使用者的值 (在 Ubuntu 散發版本中, 預設使用者是以 uid = 1000, gid = 1000) 來建立。</span><span class="sxs-lookup"><span data-stu-id="c7871-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="c7871-236">如果使用者透過這個機碼明確指定了 gid 或 uid 選項, 將會覆寫相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="c7871-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="c7871-237">否則, 一律會附加預設值。</span><span class="sxs-lookup"><span data-stu-id="c7871-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="c7871-238">**注意：** 這些選項會套用為所有自動掛接之磁片磁碟機的掛接選項。</span><span class="sxs-lookup"><span data-stu-id="c7871-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="c7871-239">若只要變更特定磁片磁碟機的選項, 請改用/etc/fstab。</span><span class="sxs-lookup"><span data-stu-id="c7871-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="c7871-240">網路</span><span class="sxs-lookup"><span data-stu-id="c7871-240">network</span></span>

<span data-ttu-id="c7871-241">區段標籤:`[network]`</span><span class="sxs-lookup"><span data-stu-id="c7871-241">Section label: `[network]`</span></span>

| <span data-ttu-id="c7871-242">key</span><span class="sxs-lookup"><span data-stu-id="c7871-242">key</span></span> | <span data-ttu-id="c7871-243">value</span><span class="sxs-lookup"><span data-stu-id="c7871-243">value</span></span> | <span data-ttu-id="c7871-244">預設值</span><span class="sxs-lookup"><span data-stu-id="c7871-244">default</span></span> | <span data-ttu-id="c7871-245">紀錄</span><span class="sxs-lookup"><span data-stu-id="c7871-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="c7871-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="c7871-246">generateHosts</span></span> | <span data-ttu-id="c7871-247">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-247">boolean</span></span> | `true` | <span data-ttu-id="c7871-248">`true`設定要產生`/etc/hosts`的 WSL。</span><span class="sxs-lookup"><span data-stu-id="c7871-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="c7871-249">`hosts`檔案包含主機名稱對應的 IP 位址的靜態對應。</span><span class="sxs-lookup"><span data-stu-id="c7871-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="c7871-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="c7871-250">generateResolvConf</span></span> | <span data-ttu-id="c7871-251">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-251">boolean</span></span> | `true` | <span data-ttu-id="c7871-252">`true`將 WSL 設定為`/etc/resolv.conf`[產生]。</span><span class="sxs-lookup"><span data-stu-id="c7871-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="c7871-253">`resolv.conf`包含可以將指定的主機名稱解析為其 IP 位址的 DNS 清單。</span><span class="sxs-lookup"><span data-stu-id="c7871-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="c7871-254">互</span><span class="sxs-lookup"><span data-stu-id="c7871-254">interop</span></span>

<span data-ttu-id="c7871-255">區段標籤:`[interop]`</span><span class="sxs-lookup"><span data-stu-id="c7871-255">Section label: `[interop]`</span></span>

<span data-ttu-id="c7871-256">這些選項可在 Insider Build 17713 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="c7871-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="c7871-257">key</span><span class="sxs-lookup"><span data-stu-id="c7871-257">key</span></span> | <span data-ttu-id="c7871-258">value</span><span class="sxs-lookup"><span data-stu-id="c7871-258">value</span></span> | <span data-ttu-id="c7871-259">預設值</span><span class="sxs-lookup"><span data-stu-id="c7871-259">default</span></span> | <span data-ttu-id="c7871-260">紀錄</span><span class="sxs-lookup"><span data-stu-id="c7871-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="c7871-261">enabled</span><span class="sxs-lookup"><span data-stu-id="c7871-261">enabled</span></span> | <span data-ttu-id="c7871-262">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-262">boolean</span></span> | `true` | <span data-ttu-id="c7871-263">設定此索引鍵將決定 WSL 是否將支援啟動 Windows 進程。</span><span class="sxs-lookup"><span data-stu-id="c7871-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="c7871-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="c7871-264">appendWindowsPath</span></span> | <span data-ttu-id="c7871-265">boolean</span><span class="sxs-lookup"><span data-stu-id="c7871-265">boolean</span></span> | `true` | <span data-ttu-id="c7871-266">設定此索引鍵將決定 WSL 是否會將 Windows path 元素新增至 $PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="c7871-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
