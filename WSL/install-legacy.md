---
title: 安裝或移除在 Windows 10 年度更新版 」 或 「 建立者更新
description: 安裝和解除安裝舊版，Windows 10 年度更新版或 Creators Update 上的 beta 版散發套件的指示
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10，舊版、 beta 版的 windows 子系統安裝、 移除、 解除安裝，請解除安裝，delete，已被取代
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063586"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="08de1-104">若要安裝或解除安裝適用於 Windows 10 年度更新版和 Creators Update 上 Linux 的 Windows 子系統的指南</span><span class="sxs-lookup"><span data-stu-id="08de1-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="08de1-105">如果您執行 Windows 10 Creators Update 或更新版本中，請[遵循 Windows 10 安裝指示](install-win10.md)。</span><span class="sxs-lookup"><span data-stu-id="08de1-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<strong><em><span style="color: #f28014"><span data-ttu-id="08de1-106">下列指示是提供給執行 Windows 10 年度更新版或 Windows 10 Creators Update 的使用者</span><span class="sxs-lookup"><span data-stu-id="08de1-106">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></span></span></em></strong>

<span data-ttu-id="08de1-107">之前 Windows 10 Fall Creators Update （1709年版），WSL 會發行為 beta 功能，並 「 Bash 在 Ubuntu 上 Windows 」 （或 Bash.exe） 第一次執行時，安裝單一的 Ubuntu 執行個體。</span><span class="sxs-lookup"><span data-stu-id="08de1-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="08de1-108">雖然您可以使用 WSL 有關較早的 Windows 10 版本，此 beta 版的 「 舊版 distro"會被視為淘汰。</span><span class="sxs-lookup"><span data-stu-id="08de1-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="08de1-109">我們強烈建議您執行可用的 Windows 10 最新版本。</span><span class="sxs-lookup"><span data-stu-id="08de1-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="08de1-110">每個新的 Windows 10 版本包含數以百計的修正和改善在 WSL，允許更多 Linux 工具和應用程式，以在 WSL 上正常執行。</span><span class="sxs-lookup"><span data-stu-id="08de1-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="08de1-111">如果您無法升級至 Fall Creators Update 或更新版本，請遵循下列步驟來啟用及使用 WSL:</span><span class="sxs-lookup"><span data-stu-id="08de1-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="08de1-112">開啟 開發人員模式來執行 WSL Windows 10 年度更新版或 Creators Update 上，您必須啟用開發人員模式：</span><span class="sxs-lookup"><span data-stu-id="08de1-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="08de1-113">開啟**設定** -> **更新與安全性** -> **適用於開發人員**</span><span class="sxs-lookup"><span data-stu-id="08de1-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="08de1-114">選取 [開發人員模式] 選項按鈕</span><span class="sxs-lookup"><span data-stu-id="08de1-114">Select the Developer Mode radio button</span></span>  
    ![啟用開發人員模式](media/updateAndSecurity.png)

    > <span data-ttu-id="08de1-116">若要啟用開發人員模式需求是[在 Windows 10 Fall Creators Update 中移除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="08de1-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="08de1-117">開啟命令提示字元。</span><span class="sxs-lookup"><span data-stu-id="08de1-117">Open a command prompt.</span></span>  <span data-ttu-id="08de1-118">型別`bash`然後按 enter 鍵</span><span class="sxs-lookup"><span data-stu-id="08de1-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="08de1-119">您第一次在 Ubuntu 執行 Bash Windows，系統會提示您接受 Canonical 的授權。</span><span class="sxs-lookup"><span data-stu-id="08de1-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="08de1-120">一旦 accpted，WSL 會下載並安裝到您的電腦上的 Ubuntu 執行個體，"Bash 在 Ubuntu 上 Windows 「 快顯會新增至 [開始] 功能表。</span><span class="sxs-lookup"><span data-stu-id="08de1-120">Once accpted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![若要安裝 Ubuntu 的提示字元](media/bashShellInstall.png)

    <span data-ttu-id="08de1-122">您第一次在 Ubuntu 執行 Bash Windows，系統會提示您建立的 UNIX 使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="08de1-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="08de1-123">請遵循[散發版本的新執行個體指示](initialize-distro.md)完成您的安裝</span><span class="sxs-lookup"><span data-stu-id="08de1-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="08de1-124">透過下列方式啟動新的 Ubuntu 殼層：</span><span class="sxs-lookup"><span data-stu-id="08de1-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="08de1-125">執行`bash`從命令提示字元</span><span class="sxs-lookup"><span data-stu-id="08de1-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="08de1-126">按一下 [開始] 功能表"Bash 在 Ubuntu 上 Windows 「 捷徑</span><span class="sxs-lookup"><span data-stu-id="08de1-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="08de1-127">解除安裝/移除舊版的散發套件</span><span class="sxs-lookup"><span data-stu-id="08de1-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="08de1-128">如果您從您安裝 WSL 先前的 Windows 10 版本升級至 Windows 10 Fall Creators Update，您現有的散發套件會維持不變。</span><span class="sxs-lookup"><span data-stu-id="08de1-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="08de1-129">不過，我們強烈建議您安裝新的存放區提供散發版本儘速，，並從舊版的散發的任何必要的檔案、 資料等移轉至新的散發。</span><span class="sxs-lookup"><span data-stu-id="08de1-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="08de1-130">若要從您的電腦中移除舊版的散發版本，執行下列命令從命令列或 PowerShell 執行個體：</span><span class="sxs-lookup"><span data-stu-id="08de1-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="08de1-131">手動刪除舊版的散發套件</span><span class="sxs-lookup"><span data-stu-id="08de1-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="08de1-132">如果您想，您可以手動刪除舊版執行個體。</span><span class="sxs-lookup"><span data-stu-id="08de1-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="08de1-133">如果您遇到問題，解除安裝舊版的發行版本使用可能會需要`lxrun.exe`，或正在執行 Windows 10 Spring 2018 Update （或更新版本） 這並未隨附`lxrun.exe`。</span><span class="sxs-lookup"><span data-stu-id="08de1-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="08de1-134">若要強制刪除舊版的 WSL 散發版本，請刪除`%localappdata%\lxss\`資料夾 (和所有的子內容) 使用 Windows 的 [檔案總管] 中，或在命令列：</span><span class="sxs-lookup"><span data-stu-id="08de1-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="08de1-135">使用 PowerShell</span><span class="sxs-lookup"><span data-stu-id="08de1-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="08de1-136">使用命令提示字元：</span><span class="sxs-lookup"><span data-stu-id="08de1-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
