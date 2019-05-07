---
title: 常見問題集 (FAQ)
description: Linux 的 Windows 子系統的相關常見問題集問題。
keywords: BashOnWindows、 bash、 wsl、 windows、 windowssubsystem、 常見問題集
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063266"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="e95a8-104">適用於 Linux 常見問題集 Windows 子系統相關的問題</span><span class="sxs-lookup"><span data-stu-id="e95a8-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="e95a8-105">什麼是 Windows for Linux 子系統 (WSL)？</span><span class="sxs-lookup"><span data-stu-id="e95a8-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="e95a8-106">Windows for Linux 子系統 (WSL) 是新的 Windows 10 功能，可讓您直接在 Windows 上執行原生 Linux 命令列工具，以及傳統的 Windows 桌面和現代的市集應用程式。</span><span class="sxs-lookup"><span data-stu-id="e95a8-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="e95a8-107">請參閱[頁的相關](./about.md)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e95a8-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="e95a8-108">針對 WSL 是誰？</span><span class="sxs-lookup"><span data-stu-id="e95a8-108">Who is WSL for?</span></span>
<span data-ttu-id="e95a8-109">這是主要是針對開發人員，特別是 web 開發人員和處理上或開放原始碼專案的任何人的工具。</span><span class="sxs-lookup"><span data-stu-id="e95a8-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="e95a8-110">這可讓人希望/需要使用 Bash，常見的 Linux 工具 (`sed`，`awk`等) 和許多 Linux 第一個工具 （Ruby、 Python 等） 在 Windows 上使用其工具鏈。</span><span class="sxs-lookup"><span data-stu-id="e95a8-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="e95a8-111">我可以 WSL 用來做什麼？</span><span class="sxs-lookup"><span data-stu-id="e95a8-111">What can I do with WSL?</span></span>
<span data-ttu-id="e95a8-112">WSL 會提供應用程式呼叫 Bash.exe，啟動時，會開啟 Windows 主控台中執行 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="e95a8-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="e95a8-113">使用 Bash，您可以執行 Linux 的命令列工具和應用程式。</span><span class="sxs-lookup"><span data-stu-id="e95a8-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="e95a8-114">例如，輸入`lsb_release -a`並按 enter 鍵; 您會看到目前正在執行的 Linux 散發版本的詳細資料：</span><span class="sxs-lookup"><span data-stu-id="e95a8-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![散發套件詳細資料的螢幕擷取畫面](media/distro.png)

<span data-ttu-id="e95a8-116">您也可以存取您的本機電腦檔案系統從 Linux Bash 殼層中，您會發現您本機的磁碟機掛接在下`/mnt`資料夾。</span><span class="sxs-lookup"><span data-stu-id="e95a8-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="e95a8-117">例如，您`C:`下有掛接的磁碟機`/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="e95a8-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![掛接的 C 磁碟機的螢幕擷取畫面](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="e95a8-119">Bash 的功能？</span><span class="sxs-lookup"><span data-stu-id="e95a8-119">What is Bash?</span></span>
<span data-ttu-id="e95a8-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是常用以文字為基礎的殼層和命令語言。</span><span class="sxs-lookup"><span data-stu-id="e95a8-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="e95a8-121">它是包含在 Ubuntu 和其他 Linux 散發版本，和在 macOS 中的預設殼層。</span><span class="sxs-lookup"><span data-stu-id="e95a8-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="e95a8-122">使用者會輸入到執行指令碼及/或執行命令與工具，來完成許多工作 shell 命令。</span><span class="sxs-lookup"><span data-stu-id="e95a8-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="e95a8-123">這是如何運作？</span><span class="sxs-lookup"><span data-stu-id="e95a8-123">How does this work?</span></span>
<span data-ttu-id="e95a8-124">請查看我們[部落格](https://blogs.msdn.microsoft.com/wsl/)我們到基礎的技術詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e95a8-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="e95a8-125">為什麼我要使用 WSL，而不是 Linux VM 中？</span><span class="sxs-lookup"><span data-stu-id="e95a8-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="e95a8-126">WSL 需要比完整的虛擬機器較少的資源 （CPU、 記憶體和儲存體）。</span><span class="sxs-lookup"><span data-stu-id="e95a8-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="e95a8-127">WSL 也可讓您以執行 Linux 命令列工具和應用程式和 Windows 命令列中，桌面和市集應用程式，並存取您 Windows 中的檔案從 Linux。</span><span class="sxs-lookup"><span data-stu-id="e95a8-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="e95a8-128">這可讓您 Windows 應用程式和 Linux 命令列工具使用同一組檔案上，如果您想要。</span><span class="sxs-lookup"><span data-stu-id="e95a8-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="e95a8-129">為什麼我要使用，比方說，而不是在 Windows 上的 Linux 上的 Ruby？</span><span class="sxs-lookup"><span data-stu-id="e95a8-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="e95a8-130">假設執行所在環境的行為類似 Linux，已建立一些跨平台工具。</span><span class="sxs-lookup"><span data-stu-id="e95a8-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="e95a8-131">比方說，某些工具會假設他們就能夠存取很長的檔案路徑或特定的檔案/資料夾存在。</span><span class="sxs-lookup"><span data-stu-id="e95a8-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="e95a8-132">這通常會導致問題在其通常運作方式的 Windows 上以不同的方式從 Linux。</span><span class="sxs-lookup"><span data-stu-id="e95a8-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="e95a8-133">諸如 Ruby 和節點的許多語言通常是移植到，，並在 Windows 上執行太棒了。</span><span class="sxs-lookup"><span data-stu-id="e95a8-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="e95a8-134">不過，並非所有的 Ruby Gem 或節點 /NPM 程式庫擁有者的連接埠他們的程式庫，以支援 Windows，且許多都有 Linux 特定的相依性。</span><span class="sxs-lookup"><span data-stu-id="e95a8-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="e95a8-135">這通常會導致系統使用這類的工具和程式庫，而組建和有時也會執行階段錯誤或不想要的行為，在 Windows 上建置。</span><span class="sxs-lookup"><span data-stu-id="e95a8-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="e95a8-136">這些只是一些造成許多人向 Microsoft 以協助改善 Windows 的命令列工具和功能驅使我們合作夥伴若要啟用原生 Bash 和 Linux 命令列工具在 Windows 上執行的 Canonical 的問題。</span><span class="sxs-lookup"><span data-stu-id="e95a8-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="e95a8-137">這代表 PowerShell 的什麼？</span><span class="sxs-lookup"><span data-stu-id="e95a8-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="e95a8-138">同時使用 OSS 專案，有許多情況下，非常有用，並放入 Bash 從 PowerShell 提示字元。</span><span class="sxs-lookup"><span data-stu-id="e95a8-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="e95a8-139">Bash 支援互補，且可強化 Windows，讓 PowerShell 和 PowerShell 社群可充分利用其他受歡迎的技術的命令列的值。</span><span class="sxs-lookup"><span data-stu-id="e95a8-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="e95a8-140">閱讀的更多關於 PowerShell 小組部落格- [Bash for Windows:為何好極了，它表示適用於 PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="e95a8-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="e95a8-141">可以執行所有的 Linux 應用程式在 WSL 嗎？</span><span class="sxs-lookup"><span data-stu-id="e95a8-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="e95a8-142">不可能 ！</span><span class="sxs-lookup"><span data-stu-id="e95a8-142">No!</span></span> <span data-ttu-id="e95a8-143">WSL 是工具，旨在讓需要它們來執行 Bash 和核心 Linux 命令列工具，在 Windows 上的使用者。</span><span class="sxs-lookup"><span data-stu-id="e95a8-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="e95a8-144">沒有 WSL**不**目標是要支援 GUI 桌面或應用程式 （例如 Gnome，KDE 等等。）</span><span class="sxs-lookup"><span data-stu-id="e95a8-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="e95a8-145">此外，即使您將能夠執行許多受歡迎的伺服器應用程式 (例如 Redis)，我們不建議用於裝載生產服務 WSL – Microsoft 提供各種解決方案在 Azure 中，執行 Linux 工作負載實際執行的 HYPER-V 和 Docker。</span><span class="sxs-lookup"><span data-stu-id="e95a8-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="e95a8-146">WSL 包含哪些 Windows Sku？</span><span class="sxs-lookup"><span data-stu-id="e95a8-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="e95a8-147">適用於 Linux 的 Windows 子系統可在桌上型電腦版本的 Windows for Windows 10 Anniversary 和 Creators update 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e95a8-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="e95a8-148">從開始 Fall Creators update WSL 會提供桌面及伺服器 Sku 的 Windows 上。</span><span class="sxs-lookup"><span data-stu-id="e95a8-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="e95a8-149">WSL 支援哪些處理器？</span><span class="sxs-lookup"><span data-stu-id="e95a8-149">What processors does WSL support?</span></span>
<span data-ttu-id="e95a8-150">WSL 支援 x64 和 ARM Cpu。</span><span class="sxs-lookup"><span data-stu-id="e95a8-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="e95a8-151">如何存取我的 c： 磁碟機？</span><span class="sxs-lookup"><span data-stu-id="e95a8-151">How do I access my C: drive?</span></span>
<span data-ttu-id="e95a8-152">在本機電腦上的硬碟機的掛接點會自動建立和暺瘨謺髍 Windows 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="e95a8-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="e95a8-153">**於 /mnt/\<磁碟機代號 > /**</span><span class="sxs-lookup"><span data-stu-id="e95a8-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="e95a8-154">範例使用方式為`cd /mnt/c`存取 c:\\</span><span class="sxs-lookup"><span data-stu-id="e95a8-154">Example usage would be `cd /mnt/c` to access c:\\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="e95a8-155">如何搭配 Linux 應用程式中使用 Windows 檔案？</span><span class="sxs-lookup"><span data-stu-id="e95a8-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="e95a8-156">WSL 的好處之一能夠存取您的檔案，透過 Windows 和 Linux 應用程式或工具。</span><span class="sxs-lookup"><span data-stu-id="e95a8-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="e95a8-157">WSL 掛接您的電腦下的固定磁碟機`/mnt/<drive>`在您的 Linux 散發版本的資料夾。</span><span class="sxs-lookup"><span data-stu-id="e95a8-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="e95a8-158">例如，您`C:`下有掛接的磁碟機 `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="e95a8-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="e95a8-159">使用您已掛接的磁碟機，您可以編輯程式碼中，例如`C:\dev\myproj\`使用[Visual Studio](https://visualstudio.microsoft.com/vs/) / 或[VS Code](https://code.visualstudio.com/)，以及建置/測試 Linux 中的程式碼存取相同的檔案，透過`\mnt\c\dev\myproj`。</span><span class="sxs-lookup"><span data-stu-id="e95a8-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `\mnt\c\dev\myproj`.</span></span>

> <span data-ttu-id="e95a8-160">**重要事項**:其中一個使用 WSL 的主要限制是，不支援直接存取/變更您的 Linux 散發版本的檔案系統使用 Windows 應用程式或工具中的檔案。</span><span class="sxs-lookup"><span data-stu-id="e95a8-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="e95a8-161">請參閱：[不會變更使用 Windows 應用程式和工具的 Linux 檔案](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="e95a8-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="e95a8-162">Linux 磁碟機中的檔案有不同於已掛接的 Windows 磁碟機？</span><span class="sxs-lookup"><span data-stu-id="e95a8-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="e95a8-163">在 Linux 根目錄下的檔案 (也就是`/`) 所控制的 WSL 可以模擬 Linux 特定行為，包括但不是限於：</span><span class="sxs-lookup"><span data-stu-id="e95a8-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="e95a8-164">檔案包含無效的 Windows 檔案名稱字元</span><span class="sxs-lookup"><span data-stu-id="e95a8-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="e95a8-165">為非系統管理員使用者所建立的符號連結</span><span class="sxs-lookup"><span data-stu-id="e95a8-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="e95a8-166">變更檔案屬性透過 chmod 和 chown</span><span class="sxs-lookup"><span data-stu-id="e95a8-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="e95a8-167">區分大小寫的檔案/資料夾</span><span class="sxs-lookup"><span data-stu-id="e95a8-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="e95a8-168">掛接的磁碟機中的檔案由 Windows 所控制，並具有下列行為：</span><span class="sxs-lookup"><span data-stu-id="e95a8-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="e95a8-169">支援區分大小寫</span><span class="sxs-lookup"><span data-stu-id="e95a8-169">Support case sensitivity</span></span>
   * <span data-ttu-id="e95a8-170">所有的權限是設為最能代表的 Windows 權限</span><span class="sxs-lookup"><span data-stu-id="e95a8-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="e95a8-171">為什麼有這麼多的錯誤時執行的 apt get 升級？</span><span class="sxs-lookup"><span data-stu-id="e95a8-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="e95a8-172">有些套件會使用我們尚未在尚未實作的功能。</span><span class="sxs-lookup"><span data-stu-id="e95a8-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="e95a8-173">`udev`比方說，尚未支援，而導致幾`apt-get upgrade`錯誤。</span><span class="sxs-lookup"><span data-stu-id="e95a8-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="e95a8-174">若要修正的相關問題`udev`，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="e95a8-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="e95a8-175">寫入下列命令以`/usr/sbin/policy-rc.d`並儲存變更。</span><span class="sxs-lookup"><span data-stu-id="e95a8-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="e95a8-176">新增執行權限 `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="e95a8-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="e95a8-177">執行下列命令</span><span class="sxs-lookup"><span data-stu-id="e95a8-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="e95a8-178">如何解除安裝 WSL 發佈？</span><span class="sxs-lookup"><span data-stu-id="e95a8-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="e95a8-179">在建置之前 1709 (16299) 開啟命令提示字元，然後執行：</span><span class="sxs-lookup"><span data-stu-id="e95a8-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="e95a8-180">應用程式磚上按一下滑鼠右鍵，然後按一下 解除安裝，或透過 PowerShell 使用，從市集安裝的 WSL 散發套件可以解除像任何其他 Windows 應用程式的安裝[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e95a8-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="e95a8-181">為何要 ping 會產生權限遭拒錯誤？</span><span class="sxs-lookup"><span data-stu-id="e95a8-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="e95a8-182">在 WSL 建置 < 14926，ping 所需 WSL 透過提升權限的主控台執行。</span><span class="sxs-lookup"><span data-stu-id="e95a8-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="e95a8-183">在建置 14926 和更新版本，已修正此問題。</span><span class="sxs-lookup"><span data-stu-id="e95a8-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="e95a8-184">如何執行 OpenSSH 伺服器呢？</span><span class="sxs-lookup"><span data-stu-id="e95a8-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="e95a8-185">在 Windows 中的系統管理員權限，才能在 WSL 執行 OpenSSH。</span><span class="sxs-lookup"><span data-stu-id="e95a8-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="e95a8-186">若要執行的 OpenSSH 伺服器，在 Ubuntu 上執行 Bash，身為管理員，Windows 上，或從系統管理員權限的 CMD/PowerShell 提示字元執行 bash.exe。</span><span class="sxs-lookup"><span data-stu-id="e95a8-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="e95a8-187">為什麼我會收到 「 錯誤：0x80040306 「 當我嘗試安裝嗎？</span><span class="sxs-lookup"><span data-stu-id="e95a8-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="e95a8-188">WSL 不支援在舊版的主控台中執行。</span><span class="sxs-lookup"><span data-stu-id="e95a8-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="e95a8-189">若要關閉舊版主控台：</span><span class="sxs-lookup"><span data-stu-id="e95a8-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="e95a8-190">開啟 WSL、 PowerShell 或 Cmd</span><span class="sxs-lookup"><span data-stu-id="e95a8-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="e95a8-191">以滑鼠右鍵按一下標題列]-> [屬性]-> [取消核取 [使用舊版主控台]</span><span class="sxs-lookup"><span data-stu-id="e95a8-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="e95a8-192">按一下 [確定]</span><span class="sxs-lookup"><span data-stu-id="e95a8-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="e95a8-193">為什麼我會收到 「 錯誤：0x80040154 「 當我升級 Windows 之後，會在執行 bash.exe 時？</span><span class="sxs-lookup"><span data-stu-id="e95a8-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="e95a8-194">[Windows Linux 子系統] 功能可能會停用在 Windows 的更新。</span><span class="sxs-lookup"><span data-stu-id="e95a8-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="e95a8-195">如果發生這種情況則必須重新啟用 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="e95a8-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="e95a8-196">啟用 「 Windows Linux 子系統 」 功能的指示可在[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。</span><span class="sxs-lookup"><span data-stu-id="e95a8-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="e95a8-197">如何變更顯示語言的 WSL？</span><span class="sxs-lookup"><span data-stu-id="e95a8-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="e95a8-198">WSL 安裝將會嘗試自動變更以符合您的 Windows 安裝的地區設定的 Ubuntu 地區設定。</span><span class="sxs-lookup"><span data-stu-id="e95a8-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="e95a8-199">如果不想讓此行為，您可以執行這個命令來安裝完成之後，變更 Ubuntu 地區設定。</span><span class="sxs-lookup"><span data-stu-id="e95a8-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="e95a8-200">您必須重新啟動 bash.exe 這項變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="e95a8-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="e95a8-201">下列範例會變更為 EN-US 地區設定：</span><span class="sxs-lookup"><span data-stu-id="e95a8-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="e95a8-202">為什麼我沒有 WSL 從網際網路存取？</span><span class="sxs-lookup"><span data-stu-id="e95a8-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="e95a8-203">某些使用者有特定的防火牆應用程式封鎖網際網路存取，在 WSL 使用回報的問題。</span><span class="sxs-lookup"><span data-stu-id="e95a8-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="e95a8-204">報告在防火牆︰</span><span class="sxs-lookup"><span data-stu-id="e95a8-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="e95a8-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="e95a8-205">Kaspersky</span></span>
1. <span data-ttu-id="e95a8-206">AVG</span><span class="sxs-lookup"><span data-stu-id="e95a8-206">AVG</span></span>
1. <span data-ttu-id="e95a8-207">太好了</span><span class="sxs-lookup"><span data-stu-id="e95a8-207">Avast</span></span>

<span data-ttu-id="e95a8-208">在某些情況下關閉防火牆可供存取。</span><span class="sxs-lookup"><span data-stu-id="e95a8-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="e95a8-209">在某些情況下單純地安裝防火牆會封鎖其存取權。</span><span class="sxs-lookup"><span data-stu-id="e95a8-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="e95a8-210">如何從 Windows 在 WSL 存取連接埠？</span><span class="sxs-lookup"><span data-stu-id="e95a8-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="e95a8-211">在 Windows 上執行時，WSL 會共用 Windows，IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e95a8-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="e95a8-212">因此您可以存取在 localhost 上的任何連接埠例如如果您有 web 內容的通訊埠 1234，您可以在 https://localhost:1234到您的 Windows 瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="e95a8-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="e95a8-213">其中提供意見反應？</span><span class="sxs-lookup"><span data-stu-id="e95a8-213">Where can I provide feedback?</span></span>

<span data-ttu-id="e95a8-214">您可以分享意見並提出問題，透過多個管道：意見和問題應導向至：</span><span class="sxs-lookup"><span data-stu-id="e95a8-214">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="e95a8-215">我們[GitHub 問題追蹤程式](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="e95a8-215">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="e95a8-216">我們[命令列的 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="e95a8-216">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="e95a8-217">我們[命令列的小組部落格](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="e95a8-217">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="e95a8-218">透過 Twitter。</span><span class="sxs-lookup"><span data-stu-id="e95a8-218">Via Twitter.</span></span> <span data-ttu-id="e95a8-219">請遵循[ @richturn_ms ](https://twitter.com/richturn_MS)到 Twitter 以了解的新聞、 更新等等。</span><span class="sxs-lookup"><span data-stu-id="e95a8-219">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
