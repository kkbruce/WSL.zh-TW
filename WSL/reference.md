---
title: 適用于 Linux 的 Windows 子系統命令參考
description: 管理適用于 Linux 的 Windows 子系統的命令清單
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307660"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="3acfc-104">適用于 Linux 的 Windows 子系統命令參考</span><span class="sxs-lookup"><span data-stu-id="3acfc-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="3acfc-105">與適用于 Linux 的 Windows 子系統互動的最佳方式是使用`wsl.exe`命令。</span><span class="sxs-lookup"><span data-stu-id="3acfc-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="3acfc-106">以下清單包含使用`wsl.exe` Windows 1903 版時的所有選項。</span><span class="sxs-lookup"><span data-stu-id="3acfc-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="3acfc-107">執行 Linux 二進位檔的引數:</span><span class="sxs-lookup"><span data-stu-id="3acfc-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="3acfc-108">如果未提供任何命令列, 則 wsl 會啟動預設的 shell。</span><span class="sxs-lookup"><span data-stu-id="3acfc-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="3acfc-109">--exec、-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="3acfc-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="3acfc-110">執行指定的命令, 而不使用預設的 Linux shell。</span><span class="sxs-lookup"><span data-stu-id="3acfc-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="3acfc-111">依情況傳遞其餘的命令列。</span><span class="sxs-lookup"><span data-stu-id="3acfc-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="3acfc-112">選項:</span><span class="sxs-lookup"><span data-stu-id="3acfc-112">Options:</span></span>
    * <span data-ttu-id="3acfc-113">--散發,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="3acfc-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="3acfc-114">執行指定的散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="3acfc-115">--user、-u<UserName></span><span class="sxs-lookup"><span data-stu-id="3acfc-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="3acfc-116">以指定的使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="3acfc-116">Run as the specified user.</span></span>

* <span data-ttu-id="3acfc-117">用於管理適用于 Linux 的 Windows 子系統的引數:</span><span class="sxs-lookup"><span data-stu-id="3acfc-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="3acfc-118">--export <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="3acfc-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="3acfc-119">將散發匯出至 tar 檔案。</span><span class="sxs-lookup"><span data-stu-id="3acfc-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="3acfc-120">標準輸出的檔案名可以是-。</span><span class="sxs-lookup"><span data-stu-id="3acfc-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="3acfc-121">--import <Distro> <InstallLocation>[Options <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="3acfc-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="3acfc-122">匯入指定的 tar 檔案做為新的散發套件。</span><span class="sxs-lookup"><span data-stu-id="3acfc-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="3acfc-123">檔案名可以是-用於標準輸入。</span><span class="sxs-lookup"><span data-stu-id="3acfc-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="3acfc-124">選項:</span><span class="sxs-lookup"><span data-stu-id="3acfc-124">Options:</span></span>
            * <span data-ttu-id="3acfc-125">--version <Version>指定要用於新散發的版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="3acfc-126">--list、-l [Options]</span><span class="sxs-lookup"><span data-stu-id="3acfc-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="3acfc-127">列出發行版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-127">Lists distributions.</span></span>

        * <span data-ttu-id="3acfc-128">選項:</span><span class="sxs-lookup"><span data-stu-id="3acfc-128">Options:</span></span>
            * <span data-ttu-id="3acfc-129">--全部</span><span class="sxs-lookup"><span data-stu-id="3acfc-129">--all</span></span>
                * <span data-ttu-id="3acfc-130">列出所有散發套件, 包括目前正在安裝或卸載的發行版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="3acfc-131">--正在執行</span><span class="sxs-lookup"><span data-stu-id="3acfc-131">--running</span></span>
                * <span data-ttu-id="3acfc-132">僅列出目前正在執行的散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="3acfc-133">--set-default、-s<Distro></span><span class="sxs-lookup"><span data-stu-id="3acfc-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="3acfc-134">將散發設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="3acfc-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="3acfc-135">--設定-預設版本<Version></span><span class="sxs-lookup"><span data-stu-id="3acfc-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="3acfc-136">變更新發行版本的預設安裝版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="3acfc-137">--設定版本<Distro><Version></span><span class="sxs-lookup"><span data-stu-id="3acfc-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="3acfc-138">變更指定之散發套件的版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="3acfc-139">--terminate、-t<Distro></span><span class="sxs-lookup"><span data-stu-id="3acfc-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="3acfc-140">終止指定的散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="3acfc-141">--取消註冊<Distro></span><span class="sxs-lookup"><span data-stu-id="3acfc-141">--unregister <Distro></span></span>
        * <span data-ttu-id="3acfc-142">取消註冊散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="3acfc-143">--help</span><span class="sxs-lookup"><span data-stu-id="3acfc-143">--help</span></span>
        * <span data-ttu-id="3acfc-144">顯示使用方式資訊。</span><span class="sxs-lookup"><span data-stu-id="3acfc-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="3acfc-145">其他命令</span><span class="sxs-lookup"><span data-stu-id="3acfc-145">Additional Commands</span></span>

<span data-ttu-id="3acfc-146">還有與適用于 Linux 的 Windows 子系統互動的歷史命令。</span><span class="sxs-lookup"><span data-stu-id="3acfc-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="3acfc-147">其功能包含在中`wsl.exe`, 但仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="3acfc-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="3acfc-148">此命令可讓您設定 WSL 分佈。</span><span class="sxs-lookup"><span data-stu-id="3acfc-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="3acfc-149">以下是其選項的清單。</span><span class="sxs-lookup"><span data-stu-id="3acfc-149">Below is a list of its options.</span></span>

* <span data-ttu-id="3acfc-150">/l,/list [選項]</span><span class="sxs-lookup"><span data-stu-id="3acfc-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="3acfc-151">列出已註冊的發行版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="3acfc-152">/all-選擇性地列出所有散發套件, 包括目前正在安裝或卸載的發行版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="3acfc-153">/running-僅列出目前正在執行的散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="3acfc-154">/s、/setdefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="3acfc-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="3acfc-155">將散發設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="3acfc-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="3acfc-156">/t、/terminate<DistributionName></span><span class="sxs-lookup"><span data-stu-id="3acfc-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="3acfc-157">終止散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-157">Terminates the distribution.</span></span>

* <span data-ttu-id="3acfc-158">/u、/unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="3acfc-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="3acfc-159">取消註冊散發。</span><span class="sxs-lookup"><span data-stu-id="3acfc-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="3acfc-160">此命令可用來啟動 bash shell。</span><span class="sxs-lookup"><span data-stu-id="3acfc-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="3acfc-161">以下是您可以搭配此命令使用的選項。</span><span class="sxs-lookup"><span data-stu-id="3acfc-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="3acfc-162">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="3acfc-162">No Option given</span></span>
    * <span data-ttu-id="3acfc-163">在目前目錄中啟動 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="3acfc-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="3acfc-164">如果未安裝 Bash shell, 則會自動執行`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="3acfc-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="3acfc-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="3acfc-165">bash ~</span></span>
    * <span data-ttu-id="3acfc-166">在使用者的主目錄中啟動 bash shell。</span><span class="sxs-lookup"><span data-stu-id="3acfc-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="3acfc-167">類似于正在`cd ~`執行。</span><span class="sxs-lookup"><span data-stu-id="3acfc-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="3acfc-168">bash-c "&lt;command&gt;"</span><span class="sxs-lookup"><span data-stu-id="3acfc-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="3acfc-169">執行命令, 列印輸出並結束 Windows 命令提示字元。</span><span class="sxs-lookup"><span data-stu-id="3acfc-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="3acfc-170">實例`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="3acfc-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="3acfc-171">已淘汰的命令</span><span class="sxs-lookup"><span data-stu-id="3acfc-171">Deprecated Commands</span></span>

<span data-ttu-id="3acfc-172">`lxrun.exe`是用來安裝和管理適用于 Linux 的 Windows 子系統的第一個命令。</span><span class="sxs-lookup"><span data-stu-id="3acfc-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="3acfc-173">它已被取代為 Windows 10 1803 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3acfc-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="3acfc-174">命令`lxrun.exe`可以用來直接與[適用于 Linux 的 Windows 子系統 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)互動。</span><span class="sxs-lookup"><span data-stu-id="3acfc-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="3acfc-175">這些命令會安裝到`\Windows\System32`目錄中, 而且可以在 Windows 命令提示字元或 PowerShell 中執行。</span><span class="sxs-lookup"><span data-stu-id="3acfc-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="3acfc-176">命令</span><span class="sxs-lookup"><span data-stu-id="3acfc-176">Command</span></span>                     | <span data-ttu-id="3acfc-177">描述</span><span class="sxs-lookup"><span data-stu-id="3acfc-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="3acfc-178">Lxrun 命令是用來管理 WSL 實例。</span><span class="sxs-lookup"><span data-stu-id="3acfc-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="3acfc-179">開始下載和安裝程式。</span><span class="sxs-lookup"><span data-stu-id="3acfc-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="3acfc-180">可能會加入 **/y**以略過所有提示。</span><span class="sxs-lookup"><span data-stu-id="3acfc-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="3acfc-181">系統會自動接受確認提示, 並將預設使用者設定為 [根]。</span><span class="sxs-lookup"><span data-stu-id="3acfc-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="3acfc-182">卸載並刪除 Ubuntu 映射。</span><span class="sxs-lookup"><span data-stu-id="3acfc-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="3acfc-183">根據預設, 這不會移除使用者的 Ubuntu 主目錄。</span><span class="sxs-lookup"><span data-stu-id="3acfc-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="3acfc-184">可能會新增 **/y**以自動接受確認提示</span><span class="sxs-lookup"><span data-stu-id="3acfc-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="3acfc-185">**/full**卸載並刪除使用者的 Ubuntu 主目錄</span><span class="sxs-lookup"><span data-stu-id="3acfc-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="3acfc-186">設定 Ubuntu 使用者的預設 Bash。</span><span class="sxs-lookup"><span data-stu-id="3acfc-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="3acfc-187">如果指定的使用者不存在, 則會提示您輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="3acfc-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="3acfc-188">如需詳細資訊, https://aka.ms/wslusers 請造訪:。</span><span class="sxs-lookup"><span data-stu-id="3acfc-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="3acfc-189">**/y**略過密碼的 promping。</span><span class="sxs-lookup"><span data-stu-id="3acfc-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="3acfc-190">將建立不含密碼的使用者。</span><span class="sxs-lookup"><span data-stu-id="3acfc-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="3acfc-191">更新子系統的套件索引</span><span class="sxs-lookup"><span data-stu-id="3acfc-191">Updates the subsystem's package index</span></span>          |
