---
title: 安裝或移除 Windows 10 年度更新版或建立者更新
description: Windows 10 年度更新版或建立者更新的舊版、Beta 散發版本的安裝和卸載指示
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10, 舊版, Beta, 安裝, 移除, 卸載, 取消安裝, 刪除, 已淘汰
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499270"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="1ed99-104">在 Windows 10 年度更新版和建立者更新上安裝或卸載適用于 Linux 的 Windows 子系統的指南</span><span class="sxs-lookup"><span data-stu-id="1ed99-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="1ed99-105">如果您執行的是 Windows 10 建立者更新或更新版本, 請[遵循 windows 10 安裝指示](install-win10.md)。</span><span class="sxs-lookup"><span data-stu-id="1ed99-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="1ed99-106"><strong><em><span style="color: #f28014">下列指示適用于執行 Windows 10 年度更新版或 Windows 10 建立者更新的使用者</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="1ed99-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="1ed99-107">在 Windows 10 秋季建立者更新 (版本 1709) 之前, WSL 已發行為搶鮮版 (Beta) 功能, 而且會在第一次執行「Windows 上的 Ubuntu 上的 Bash」 (或 Bash) 時, 安裝單一 Ubuntu 實例。</span><span class="sxs-lookup"><span data-stu-id="1ed99-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="1ed99-108">雖然您可以在先前的 Windows 10 版本上使用 WSL, 但這個 Beta 版的「舊版散發版本」現在已被視為過時。</span><span class="sxs-lookup"><span data-stu-id="1ed99-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="1ed99-109">我們強烈建議您執行最新版本的 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="1ed99-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="1ed99-110">每個新的 Windows 10 版本都包含 WSL 的數百個修正和改善, 讓更多的 Linux 工具和應用程式可以在 WSL 上正確執行。</span><span class="sxs-lookup"><span data-stu-id="1ed99-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="1ed99-111">如果您無法升級至秋季建立者更新或更新版本, 請遵循下列步驟來啟用及使用 WSL:</span><span class="sxs-lookup"><span data-stu-id="1ed99-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="1ed99-112">開啟開發人員模式以在 Windows 10 年度更新版或建立者更新上執行 WSL, 您必須啟用開發人員模式:</span><span class="sxs-lookup"><span data-stu-id="1ed99-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="1ed99-113">開啟**開發人員的** **設定** -> **更新和安全性** -> </span><span class="sxs-lookup"><span data-stu-id="1ed99-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="1ed99-114">選取 [開發人員模式] 選項按鈕</span><span class="sxs-lookup"><span data-stu-id="1ed99-114">Select the Developer Mode radio button</span></span>  
    ![啟用開發人員模式](media/updateAndSecurity.png)

    > <span data-ttu-id="1ed99-116">[Windows 10 秋季建立者更新已移除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)啟用開發人員模式的需求</span><span class="sxs-lookup"><span data-stu-id="1ed99-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="1ed99-117">開啟命令提示字元。</span><span class="sxs-lookup"><span data-stu-id="1ed99-117">Open a command prompt.</span></span>  <span data-ttu-id="1ed99-118">輸入`bash` , 然後按 enter 鍵</span><span class="sxs-lookup"><span data-stu-id="1ed99-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="1ed99-119">當您第一次在 Windows 上的 Ubuntu 上執行 Bash 時, 系統會提示您接受標準授權。</span><span class="sxs-lookup"><span data-stu-id="1ed99-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="1ed99-120">一旦接受, WSL 會下載 Ubuntu 實例並將其安裝到您的電腦上, 並在 [開始] 功能表中新增 "Bash on Ubuntu on Windows" 快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1ed99-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![提示安裝 Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="1ed99-122">當您第一次在 Windows 上的 Ubuntu 上執行 Bash 時, 系統會提示您建立 UNIX 使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="1ed99-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="1ed99-123">遵循[新的散發版本實例指示](initialize-distro.md)來完成安裝</span><span class="sxs-lookup"><span data-stu-id="1ed99-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="1ed99-124">啟動新的 Ubuntu shell, 方法是:</span><span class="sxs-lookup"><span data-stu-id="1ed99-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="1ed99-125">`bash`從命令提示字元執行</span><span class="sxs-lookup"><span data-stu-id="1ed99-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="1ed99-126">按一下 [開始] 功能表中的 [Windows 上 Ubuntu 上的 Bash] 快捷方式</span><span class="sxs-lookup"><span data-stu-id="1ed99-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="1ed99-127">卸載/移除舊版散發版本</span><span class="sxs-lookup"><span data-stu-id="1ed99-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="1ed99-128">如果您從舊版已安裝 WSL 的 Windows 10 版本升級至 Windows 10 秋季建立者更新, 現有的散發版本將維持不變。</span><span class="sxs-lookup"><span data-stu-id="1ed99-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="1ed99-129">不過, 我們強烈建議您儘快安裝新的商店提供散發版本, 並將任何必要的檔案、資料等等從您的舊版散發版本遷移到新的散發版本。</span><span class="sxs-lookup"><span data-stu-id="1ed99-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="1ed99-130">若要從您的電腦移除舊版散發版本, 請從命令列或 PowerShell 實例執行下列程式碼:</span><span class="sxs-lookup"><span data-stu-id="1ed99-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="1ed99-131">如果您不是使用 Windows 1903 版或更新版本, 您可能需要改`wslconfig /u Legacy`為`lxrun /uninstall /full`執行或。</span><span class="sxs-lookup"><span data-stu-id="1ed99-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="1ed99-132">手動刪除舊版散發版本</span><span class="sxs-lookup"><span data-stu-id="1ed99-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="1ed99-133">如有需要, 您可以手動刪除舊版實例。</span><span class="sxs-lookup"><span data-stu-id="1ed99-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="1ed99-134">如果您在使用`lxrun.exe`卸載舊版散發版本時遇到問題, 或是執行 Windows 10 春季 2018 Update (或更新版本), 但未隨附于`lxrun.exe`, 這可能是必要的。</span><span class="sxs-lookup"><span data-stu-id="1ed99-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="1ed99-135">若要強制刪除舊版 WSL 散發版本, 請使用`%localappdata%\lxss\` Windows 的 [檔案瀏覽器] 或命令列來刪除資料夾 (及其所有子內容):</span><span class="sxs-lookup"><span data-stu-id="1ed99-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="1ed99-136">使用 PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ed99-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="1ed99-137">使用 Cmd:</span><span class="sxs-lookup"><span data-stu-id="1ed99-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
