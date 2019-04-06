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
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063496"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="71dcc-104">管理和設定適用於 Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="71dcc-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="71dcc-105">適用於 Windows 10 Fall Creators Update 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="71dcc-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="71dcc-106">請參閱我們已更新[安裝指南](./install_guide.md)嘗試新的管理功能，並開始執行從 Windows 市集的多個 Linux 發行版本。</span><span class="sxs-lookup"><span data-stu-id="71dcc-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="71dcc-107">如何執行 WSL</span><span class="sxs-lookup"><span data-stu-id="71dcc-107">Ways to run WSL</span></span>

<span data-ttu-id="71dcc-108">有許多方法可執行 Linux 的 Windows 子系統，適用於 Linux。</span><span class="sxs-lookup"><span data-stu-id="71dcc-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. `[distro]` <span data-ttu-id="71dcc-109">ie</span><span class="sxs-lookup"><span data-stu-id="71dcc-109">ie</span></span> `ubuntu`
1. `wsl.exe` <span data-ttu-id="71dcc-110">或</span><span class="sxs-lookup"><span data-stu-id="71dcc-110">or</span></span> `bash.exe`
1. `wsl [command]` <span data-ttu-id="71dcc-111">或</span><span class="sxs-lookup"><span data-stu-id="71dcc-111">or</span></span> `bash -c [command]`

<span data-ttu-id="71dcc-112">您應該使用哪個方法取決於您的所作所為。</span><span class="sxs-lookup"><span data-stu-id="71dcc-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="71dcc-113">啟動發佈 WSL</span><span class="sxs-lookup"><span data-stu-id="71dcc-113">Launch WSL by distribution</span></span>

<span data-ttu-id="71dcc-114">執行散發套件使用的散發套件專用應用程式會啟動該發佈它本身的主控台視窗中。</span><span class="sxs-lookup"><span data-stu-id="71dcc-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![從 [開始] 功能表啟動 WSL](media/start-launch.png)

<span data-ttu-id="71dcc-116">它是不同於按一下 [啟動] 在 Windows 市集中。</span><span class="sxs-lookup"><span data-stu-id="71dcc-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![啟動從 Windows 市集的 WSL](media/store-launch.png)

<span data-ttu-id="71dcc-118">您也可以執行從命令列發佈，藉由執行`[distribution].exe`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="71dcc-119">從命令列，如此一來執行散發的缺點是，它會自動將變更您的工作目錄從目前的目錄來散發套件的主目錄。</span><span class="sxs-lookup"><span data-stu-id="71dcc-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

**<span data-ttu-id="71dcc-120">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-120">Example:</span></span>**

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="71dcc-121">wsl 和 wsl [command]</span><span class="sxs-lookup"><span data-stu-id="71dcc-121">wsl and wsl [command]</span></span>

<span data-ttu-id="71dcc-122">若要從命令列執行 WSL 的最佳方式使用`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

**<span data-ttu-id="71dcc-123">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-123">Example:</span></span>**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="71dcc-124">不但`wsl`就地保留目前的工作目錄，它可讓您執行單一命令，沿著端 Windows 命令。</span><span class="sxs-lookup"><span data-stu-id="71dcc-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

**<span data-ttu-id="71dcc-125">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-125">Example:</span></span>**

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

**<span data-ttu-id="71dcc-126">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-126">Example:</span></span>**

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="71dcc-127">管理多個 Linux 發行版本</span><span class="sxs-lookup"><span data-stu-id="71dcc-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="71dcc-128">1903 和更新版本的 Windows 10 版本</span><span class="sxs-lookup"><span data-stu-id="71dcc-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="71dcc-129">您可以使用`wsl.exe`來管理您散發的 Windows 子系統中的 Linux (WSL)，包括列出可用的散發套件、 設定的預設發佈，以及解除安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="71dcc-130">每個 Linux 散發套件會獨立管理它自己的組態。</span><span class="sxs-lookup"><span data-stu-id="71dcc-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="71dcc-131">若要查看特定散發的命令，請執行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="71dcc-132">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="71dcc-133">清單的散發套件</span><span class="sxs-lookup"><span data-stu-id="71dcc-133">List distributions</span></span>

`wsl -l` <span data-ttu-id="71dcc-134">、</span><span class="sxs-lookup"><span data-stu-id="71dcc-134">,</span></span> `wsl --list`  
<span data-ttu-id="71dcc-135">列出可用於 WSL 的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="71dcc-136">如果列出的散發，它會安裝，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="71dcc-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="71dcc-137">列出所有的散發套件，包括不是目前可用的。</span><span class="sxs-lookup"><span data-stu-id="71dcc-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="71dcc-138">它們可能正在安裝，解除安裝，或處於中斷狀態。</span><span class="sxs-lookup"><span data-stu-id="71dcc-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="71dcc-139">列出目前正在執行的所有分佈。</span><span class="sxs-lookup"><span data-stu-id="71dcc-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="71dcc-140">設定預設的通訊</span><span class="sxs-lookup"><span data-stu-id="71dcc-140">Set a default distribution</span></span>

<span data-ttu-id="71dcc-141">預設的 WSL 通訊是當您執行時所執行`wsl`命令列上。</span><span class="sxs-lookup"><span data-stu-id="71dcc-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wsl -s <DistributionName>`<span data-ttu-id="71dcc-142">、</span><span class="sxs-lookup"><span data-stu-id="71dcc-142">,</span></span> `wsl --setdefault <DistributionName>`

<span data-ttu-id="71dcc-143">若要設定的預設分佈`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-143">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="71dcc-144">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-144">Example:</span></span>**  
`wsl -s Ubuntu` <span data-ttu-id="71dcc-145">會將我的預設發佈設定到 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="71dcc-145">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="71dcc-146">現在，當我執行`wsl npm init`會在 Ubuntu 執行。</span><span class="sxs-lookup"><span data-stu-id="71dcc-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="71dcc-147">如果我執行`wsl`即會開啟 Ubuntu 工作階段。</span><span class="sxs-lookup"><span data-stu-id="71dcc-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="71dcc-148">取消註冊再重新安裝散發</span><span class="sxs-lookup"><span data-stu-id="71dcc-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="71dcc-149">在 Linux 散發套件可透過 Windows 安裝時儲存，它們無法透過市集解除安裝。</span><span class="sxs-lookup"><span data-stu-id="71dcc-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="71dcc-150">WSL 組態可讓要取消註冊/解除安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="71dcc-151">取消註冊時，也可讓重新安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="71dcc-152">**注意**：一旦取消註冊所有的資料、 設定以及與該發佈相關聯的軟體將會永久遺失。</span><span class="sxs-lookup"><span data-stu-id="71dcc-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="71dcc-153">從存放區重新安裝將會安裝全新的分佈。</span><span class="sxs-lookup"><span data-stu-id="71dcc-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="71dcc-154">取消註冊 WSL 散發，讓它能夠重新安裝或清除。</span><span class="sxs-lookup"><span data-stu-id="71dcc-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="71dcc-155">例如：`wsl -unregister Ubuntu`會將 Ubuntu 移除 WSL 中可用的散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="71dcc-156">當我執行`wsl --list`不會列出。</span><span class="sxs-lookup"><span data-stu-id="71dcc-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="71dcc-157">若要重新安裝，請在 Windows 市集尋找散發並選取 「 啟動 」。</span><span class="sxs-lookup"><span data-stu-id="71dcc-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="71dcc-158">以特定的使用者身分執行</span><span class="sxs-lookup"><span data-stu-id="71dcc-158">Run as a specific user</span></span>

`wsl -u <Username>`<span data-ttu-id="71dcc-159">、</span><span class="sxs-lookup"><span data-stu-id="71dcc-159">,</span></span> `wsl --user <Username>`

<span data-ttu-id="71dcc-160">執行 WSL 成為指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="71dcc-160">Run WSL as the specified user.</span></span> <span data-ttu-id="71dcc-161">請注意，使用者必須存在於 WSL 散發內。</span><span class="sxs-lookup"><span data-stu-id="71dcc-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="71dcc-162">執行特定的散發套件</span><span class="sxs-lookup"><span data-stu-id="71dcc-162">Run a specific distribution</span></span>

`wsl --d <DistributionName>`<span data-ttu-id="71dcc-163">、</span><span class="sxs-lookup"><span data-stu-id="71dcc-163">,</span></span> `wsl --distribution <DistributionName>`

<span data-ttu-id="71dcc-164">執行指定的 WSL 散發套件，可用來將命令傳送至特定的分佈，而不需要變更您的預設值。</span><span class="sxs-lookup"><span data-stu-id="71dcc-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="71dcc-165">Windows 10 版本 1903，之前的版本</span><span class="sxs-lookup"><span data-stu-id="71dcc-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="71dcc-166">WSL 組態 (`wslconfig.exe`) 是命令列工具來管理執行 Windows 子系統上的 Linux (WSL) 的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="71dcc-167">它可讓您列出可用的散發套件、 設定的預設散發，以及解除安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="71dcc-168">範圍或協調散發套件的設定很有幫助 WSL 組態時，每個 Linux 散發套件會獨立管理它自己的組態。</span><span class="sxs-lookup"><span data-stu-id="71dcc-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="71dcc-169">若要查看特定散發的命令，請執行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="71dcc-170">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="71dcc-171">若要查看所有可用的選項，如 wslconfig，請執行：</span><span class="sxs-lookup"><span data-stu-id="71dcc-171">To see all available options for wslconfig, run:</span></span>  `wslconfig /?`

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

#### <a name="list-distributions"></a><span data-ttu-id="71dcc-172">清單的散發套件</span><span class="sxs-lookup"><span data-stu-id="71dcc-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="71dcc-173">列出可用於 WSL 的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="71dcc-174">如果列出的散發，它會安裝，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="71dcc-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="71dcc-175">列出所有的散發套件，包括不是目前可用的。</span><span class="sxs-lookup"><span data-stu-id="71dcc-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="71dcc-176">它們可能正在安裝，解除安裝，或處於中斷狀態。</span><span class="sxs-lookup"><span data-stu-id="71dcc-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="71dcc-177">設定預設的通訊</span><span class="sxs-lookup"><span data-stu-id="71dcc-177">Set a default distribution</span></span>

<span data-ttu-id="71dcc-178">預設的 WSL 通訊是當您執行時所執行`wsl`命令列上。</span><span class="sxs-lookup"><span data-stu-id="71dcc-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="71dcc-179">若要設定的預設分佈`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-179">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="71dcc-180">範例：</span><span class="sxs-lookup"><span data-stu-id="71dcc-180">Example:</span></span>**  
`wslconfig /setdefault Ubuntu` <span data-ttu-id="71dcc-181">會將我的預設發佈設定到 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="71dcc-181">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="71dcc-182">現在，當我執行`wsl npm init`會在 Ubuntu 執行。</span><span class="sxs-lookup"><span data-stu-id="71dcc-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="71dcc-183">如果我執行`wsl`即會開啟 Ubuntu 工作階段。</span><span class="sxs-lookup"><span data-stu-id="71dcc-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="71dcc-184">取消註冊再重新安裝散發</span><span class="sxs-lookup"><span data-stu-id="71dcc-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="71dcc-185">在 Linux 散發套件可透過 Windows 安裝時儲存，它們無法透過市集解除安裝。</span><span class="sxs-lookup"><span data-stu-id="71dcc-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="71dcc-186">WSL 組態可讓要取消註冊/解除安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="71dcc-187">取消註冊時，也可讓重新安裝散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="71dcc-188">**注意**：一旦取消註冊所有的資料、 設定以及與該發佈相關聯的軟體將會永久遺失。</span><span class="sxs-lookup"><span data-stu-id="71dcc-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="71dcc-189">從存放區重新安裝將會安裝全新的分佈。</span><span class="sxs-lookup"><span data-stu-id="71dcc-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="71dcc-190">取消註冊 WSL 散發，讓它能夠重新安裝或清除。</span><span class="sxs-lookup"><span data-stu-id="71dcc-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="71dcc-191">例如：`wslconfig /unregister Ubuntu`會將 Ubuntu 移除 WSL 中可用的散發套件。</span><span class="sxs-lookup"><span data-stu-id="71dcc-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="71dcc-192">當我執行`wslconfig /list`不會列出。</span><span class="sxs-lookup"><span data-stu-id="71dcc-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="71dcc-193">若要重新安裝，請在 Windows 市集尋找散發並選取 「 啟動 」。</span><span class="sxs-lookup"><span data-stu-id="71dcc-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="71dcc-194">設定 WSL 啟動設定</span><span class="sxs-lookup"><span data-stu-id="71dcc-194">Set WSL launch settings</span></span>

> **<span data-ttu-id="71dcc-195">可在 Windows Insider 組建 17093 及更新版本</span><span class="sxs-lookup"><span data-stu-id="71dcc-195">Available in Windows Insider Build 17093 and later</span></span>**

<span data-ttu-id="71dcc-196">自動設定在 WSL 會在每次您啟動子系統使用套用的特定功能`wsl.conf`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="71dcc-197">權限，這包括自動掛接選項和網路設定。</span><span class="sxs-lookup"><span data-stu-id="71dcc-197">Right now, this includes automount options and network configuration.</span></span>

`wsl.conf` <span data-ttu-id="71dcc-198">位於中每個 Linux 散發套件`/etc/wsl.conf`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-198">is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="71dcc-199">如果檔案不存在，您可以建立它自己。</span><span class="sxs-lookup"><span data-stu-id="71dcc-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="71dcc-200">WSL 會偵測檔案存在，並將讀取其內容。</span><span class="sxs-lookup"><span data-stu-id="71dcc-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="71dcc-201">如果檔案已遺失或格式不正確 （也就是不正確標記格式化），WSL 會繼續如往常啟動。</span><span class="sxs-lookup"><span data-stu-id="71dcc-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="71dcc-202">以下是範例`wsl.conf`您無法將它新增至您的散發套件的檔案：</span><span class="sxs-lookup"><span data-stu-id="71dcc-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="71dcc-203">組態選項</span><span class="sxs-lookup"><span data-stu-id="71dcc-203">Configuration Options</span></span>

<span data-ttu-id="71dcc-204">為了保持.ini 慣例，金鑰會宣告下一節。</span><span class="sxs-lookup"><span data-stu-id="71dcc-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="71dcc-205">WSL 支援兩個區段：`automount`和`network`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="71dcc-206">自動掛接</span><span class="sxs-lookup"><span data-stu-id="71dcc-206">automount</span></span>

<span data-ttu-id="71dcc-207">區段：</span><span class="sxs-lookup"><span data-stu-id="71dcc-207">Section:</span></span> `[automount]`


| <span data-ttu-id="71dcc-208">索引鍵</span><span class="sxs-lookup"><span data-stu-id="71dcc-208">key</span></span>        | <span data-ttu-id="71dcc-209">value</span><span class="sxs-lookup"><span data-stu-id="71dcc-209">value</span></span>                          | <span data-ttu-id="71dcc-210">預設值</span><span class="sxs-lookup"><span data-stu-id="71dcc-210">default</span></span>      | <span data-ttu-id="71dcc-211">附註</span><span class="sxs-lookup"><span data-stu-id="71dcc-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71dcc-212">enabled</span><span class="sxs-lookup"><span data-stu-id="71dcc-212">enabled</span></span>    | <span data-ttu-id="71dcc-213">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-213">boolean</span></span>                        | <span data-ttu-id="71dcc-214">true</span><span class="sxs-lookup"><span data-stu-id="71dcc-214">true</span></span>         | `true` <span data-ttu-id="71dcc-215">固定磁碟機 （也就是原因</span><span class="sxs-lookup"><span data-stu-id="71dcc-215">causes fixed drives (i.e</span></span> `C:/` <span data-ttu-id="71dcc-216">或是`D:/`) 會自動使用 DrvFs 下掛接`/mnt`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-216">or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  `false` <span data-ttu-id="71dcc-217">表示將不會自動掛接磁碟機，但仍然無法裝載它們，以手動方式或透過`fstab`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-217">means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="71dcc-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="71dcc-218">mountFsTab</span></span> | <span data-ttu-id="71dcc-219">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-219">boolean</span></span>                        | <span data-ttu-id="71dcc-220">true</span><span class="sxs-lookup"><span data-stu-id="71dcc-220">true</span></span>         | `true` <span data-ttu-id="71dcc-221">設定`/etc/fstab`處理在 WSL 啟動。</span><span class="sxs-lookup"><span data-stu-id="71dcc-221">sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="71dcc-222">/etc/fstab 是您可以在此宣告，請在其他檔案系統，例如 SMB 共用的檔案。</span><span class="sxs-lookup"><span data-stu-id="71dcc-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="71dcc-223">因此，您可以掛接這些檔案系統在 WSL 在啟動時自動註冊。</span><span class="sxs-lookup"><span data-stu-id="71dcc-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="71dcc-224">根目錄</span><span class="sxs-lookup"><span data-stu-id="71dcc-224">root</span></span>       | <span data-ttu-id="71dcc-225">字串</span><span class="sxs-lookup"><span data-stu-id="71dcc-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="71dcc-226">設定其中的固定磁碟機將會自動掛接的目錄。</span><span class="sxs-lookup"><span data-stu-id="71dcc-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="71dcc-227">例如，如果您有一個目錄中在 WSL`/windir/`和您指定，做為根，您會預期會看見您掛接於的固定磁碟機</span><span class="sxs-lookup"><span data-stu-id="71dcc-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at</span></span> `/windir/c`                                                                                              |
| <span data-ttu-id="71dcc-228">選項</span><span class="sxs-lookup"><span data-stu-id="71dcc-228">options</span></span>    | <span data-ttu-id="71dcc-229">以逗號分隔值清單</span><span class="sxs-lookup"><span data-stu-id="71dcc-229">comma-separated list of values</span></span> | <span data-ttu-id="71dcc-230">空字串</span><span class="sxs-lookup"><span data-stu-id="71dcc-230">empty string</span></span> | <span data-ttu-id="71dcc-231">這個值會附加至預設 DrvFs 掛接選項字串。</span><span class="sxs-lookup"><span data-stu-id="71dcc-231">This value is appended to the default DrvFs mount options string.</span></span> **<span data-ttu-id="71dcc-232">可以指定只有 DrvFs 特有的選項。</span><span class="sxs-lookup"><span data-stu-id="71dcc-232">Only DrvFs-specific options can be specified.</span></span>** <span data-ttu-id="71dcc-233">不支援二進位掛接通常會剖析成旗標的選項。</span><span class="sxs-lookup"><span data-stu-id="71dcc-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="71dcc-234">如果您想要明確指定這些選項，您必須包含您要在 /etc/fstab 中這麼做的每個磁碟機。</span><span class="sxs-lookup"><span data-stu-id="71dcc-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="71dcc-235">根據預設，WSL 將 uid 與 gid 設為值的預設使用者 (在 Ubuntu 發行版本，預設的使用者會建立具有 uid = 1000，gid = 1000年)。</span><span class="sxs-lookup"><span data-stu-id="71dcc-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="71dcc-236">如果使用者指定的 gid 或 uid 選項明確地透過此機碼，相關聯的值會被覆寫。</span><span class="sxs-lookup"><span data-stu-id="71dcc-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="71dcc-237">否則將一律會附加的預設值。</span><span class="sxs-lookup"><span data-stu-id="71dcc-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="71dcc-238">**注意：** 這些選項會套用為所有的自動掛接磁碟機的掛接選項。</span><span class="sxs-lookup"><span data-stu-id="71dcc-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="71dcc-239">若要變更特定磁碟的選項，請改為使用 /etc/fstab。</span><span class="sxs-lookup"><span data-stu-id="71dcc-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="71dcc-240">網路</span><span class="sxs-lookup"><span data-stu-id="71dcc-240">network</span></span>

<span data-ttu-id="71dcc-241">區段標籤：</span><span class="sxs-lookup"><span data-stu-id="71dcc-241">Section label:</span></span> `[network]`

| <span data-ttu-id="71dcc-242">索引鍵</span><span class="sxs-lookup"><span data-stu-id="71dcc-242">key</span></span> | <span data-ttu-id="71dcc-243">value</span><span class="sxs-lookup"><span data-stu-id="71dcc-243">value</span></span> | <span data-ttu-id="71dcc-244">預設值</span><span class="sxs-lookup"><span data-stu-id="71dcc-244">default</span></span> | <span data-ttu-id="71dcc-245">附註</span><span class="sxs-lookup"><span data-stu-id="71dcc-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="71dcc-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="71dcc-246">generateHosts</span></span> | <span data-ttu-id="71dcc-247">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-247">boolean</span></span> | `true` | `true` <span data-ttu-id="71dcc-248">設定產生 WSL `/etc/hosts`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-248">sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="71dcc-249">`hosts`檔案包含主機名稱對應的 IP 位址的靜態對應。</span><span class="sxs-lookup"><span data-stu-id="71dcc-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="71dcc-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="71dcc-250">generateResolvConf</span></span> | <span data-ttu-id="71dcc-251">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-251">boolean</span></span> | `true` | `true` <span data-ttu-id="71dcc-252">設定產生 WSL `/etc/resolv.conf`。</span><span class="sxs-lookup"><span data-stu-id="71dcc-252">set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="71dcc-253">`resolv.conf`包含 DNS 清單所能指定的主機名稱解析為其 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="71dcc-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="71dcc-254">Interop</span><span class="sxs-lookup"><span data-stu-id="71dcc-254">interop</span></span>

<span data-ttu-id="71dcc-255">區段標籤：</span><span class="sxs-lookup"><span data-stu-id="71dcc-255">Section label:</span></span> `[interop]`

<span data-ttu-id="71dcc-256">這些選項是用於測試人員組建 17713 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="71dcc-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="71dcc-257">索引鍵</span><span class="sxs-lookup"><span data-stu-id="71dcc-257">key</span></span> | <span data-ttu-id="71dcc-258">value</span><span class="sxs-lookup"><span data-stu-id="71dcc-258">value</span></span> | <span data-ttu-id="71dcc-259">預設值</span><span class="sxs-lookup"><span data-stu-id="71dcc-259">default</span></span> | <span data-ttu-id="71dcc-260">附註</span><span class="sxs-lookup"><span data-stu-id="71dcc-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="71dcc-261">enabled</span><span class="sxs-lookup"><span data-stu-id="71dcc-261">enabled</span></span> | <span data-ttu-id="71dcc-262">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-262">boolean</span></span> | `true` | <span data-ttu-id="71dcc-263">此索引鍵的設定會決定是否支援 WSL 啟動 Windows 處理程序。</span><span class="sxs-lookup"><span data-stu-id="71dcc-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="71dcc-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="71dcc-264">appendWindowsPath</span></span> | <span data-ttu-id="71dcc-265">布林值</span><span class="sxs-lookup"><span data-stu-id="71dcc-265">boolean</span></span> | `true` | <span data-ttu-id="71dcc-266">此索引鍵的設定會判定 WSL 是否會將 Windows 路徑項目加入至 $PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="71dcc-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
