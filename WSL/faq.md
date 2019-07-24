---
title: 常見問題集 (FAQ)
description: 適用于 Linux 的 Windows 子系統常見問題。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、常見問題
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237384"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="98d12-104">適用于 Linux 的 Windows 子系統常見問題</span><span class="sxs-lookup"><span data-stu-id="98d12-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="98d12-105">什麼是適用于 Linux 的 Windows 子系統 (WSL)？</span><span class="sxs-lookup"><span data-stu-id="98d12-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="98d12-106">適用于 Linux 的 Windows 子系統 (WSL) 是新的 Windows 10 功能, 可讓您直接在 Windows 上執行原生 Linux 命令列工具, 以及傳統的 Windows 桌面和新式存放區應用程式。</span><span class="sxs-lookup"><span data-stu-id="98d12-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="98d12-107">如需詳細資訊, 請參閱[about 頁面](./about.md)。</span><span class="sxs-lookup"><span data-stu-id="98d12-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="98d12-108">誰 WSL？</span><span class="sxs-lookup"><span data-stu-id="98d12-108">Who is WSL for?</span></span>
<span data-ttu-id="98d12-109">這主要是適用于開發人員的工具, 特別是 網頁程式開發人員, 也是使用開放原始碼專案的使用者。</span><span class="sxs-lookup"><span data-stu-id="98d12-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="98d12-110">這可讓想要/需要使用 Bash、通用 Linux 工具 (`sed`、 `awk`等) 的使用者, 以及許多 Linux 優先工具 (Ruby、Python 等) 使用其在 Windows 上的工具鏈。</span><span class="sxs-lookup"><span data-stu-id="98d12-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="98d12-111">我可以使用 WSL 來做什麼？</span><span class="sxs-lookup"><span data-stu-id="98d12-111">What can I do with WSL?</span></span>
<span data-ttu-id="98d12-112">WSL 會提供名為 Bash 的應用程式, 啟動時, 會開啟執行 Bash shell 的 Windows 主控台。</span><span class="sxs-lookup"><span data-stu-id="98d12-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="98d12-113">使用 Bash, 您可以執行命令列 Linux 工具和應用程式。</span><span class="sxs-lookup"><span data-stu-id="98d12-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="98d12-114">例如, `lsb_release -a`輸入並按 enter 鍵, 您會看到目前正在執行之 Linux 散發版本的詳細資料:</span><span class="sxs-lookup"><span data-stu-id="98d12-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![散發版本詳細資料的螢幕擷取畫面](media/distro.png)

<span data-ttu-id="98d12-116">您也可以從 Linux Bash shell 記憶體取本機電腦的檔案系統–您會在`/mnt`資料夾下找到掛接的本機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="98d12-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="98d12-117">例如, 您的`C:`磁片磁碟機`/mnt/c`裝載于:</span><span class="sxs-lookup"><span data-stu-id="98d12-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![裝載的 C 磁片磁碟機螢幕擷取畫面](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="98d12-119">什麼是 Bash？</span><span class="sxs-lookup"><span data-stu-id="98d12-119">What is Bash?</span></span>
<span data-ttu-id="98d12-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是常用的文字型命令介面和命令語言。</span><span class="sxs-lookup"><span data-stu-id="98d12-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="98d12-121">這是包含在 Ubuntu 和其他 Linux 散發版本中的預設 shell, 也是在 macOS 中。</span><span class="sxs-lookup"><span data-stu-id="98d12-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="98d12-122">使用者在 shell 中輸入命令來執行腳本及/或執行命令和工具, 以完成許多工具。</span><span class="sxs-lookup"><span data-stu-id="98d12-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="98d12-123">這是如何運作？</span><span class="sxs-lookup"><span data-stu-id="98d12-123">How does this work?</span></span>
<span data-ttu-id="98d12-124">查看我們的[blog](https://blogs.msdn.microsoft.com/wsl/) , 我們將詳細說明基礎技術。</span><span class="sxs-lookup"><span data-stu-id="98d12-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="98d12-125">為什麼我會在 VM 中使用 WSL 而不是 Linux？</span><span class="sxs-lookup"><span data-stu-id="98d12-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="98d12-126">WSL 所需的資源 (CPU、記憶體和儲存體) 比完整虛擬機器少。</span><span class="sxs-lookup"><span data-stu-id="98d12-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="98d12-127">WSL 也可讓您同時執行 Linux 命令列工具和應用程式, 以及 Windows 命令列、桌面和存放區應用程式, 以及從 Linux 記憶體取您的 Windows 檔案。</span><span class="sxs-lookup"><span data-stu-id="98d12-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="98d12-128">這可讓您視需要在相同的檔案集合上使用 Windows 應用程式和 Linux 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="98d12-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="98d12-129">為什麼我會使用 Linux 上的 Ruby, 而不是 Windows 上的？</span><span class="sxs-lookup"><span data-stu-id="98d12-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="98d12-130">某些跨平臺工具的建立方式, 是假設它們執行的環境與 Linux 類似。</span><span class="sxs-lookup"><span data-stu-id="98d12-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="98d12-131">例如, 某些工具會假設它們能夠存取非常長的檔案路徑, 或特定檔案/資料夾存在。</span><span class="sxs-lookup"><span data-stu-id="98d12-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="98d12-132">這通常會導致 Windows 上的問題, 這通常會與 Linux 有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="98d12-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="98d12-133">許多語言 (例如 Ruby 和 node) 通常會在 Windows 上移植並執行良好。</span><span class="sxs-lookup"><span data-stu-id="98d12-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="98d12-134">不過, 並非所有 Ruby Gem 或 node/NPM 程式庫擁有者都會移植其程式庫以支援 Windows, 而且許多都有 Linux 特定的相依性。</span><span class="sxs-lookup"><span data-stu-id="98d12-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="98d12-135">這通常會導致使用這類工具和程式庫所建立的系統, 在 Windows 上的組建和有時發生執行階段錯誤或不需要的行為。</span><span class="sxs-lookup"><span data-stu-id="98d12-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="98d12-136">這些只是導致許多人要求 Microsoft 改進 Windows 命令列工具的問題, 以及讓我們與標準夥伴合作, 以在 Windows 上執行原生 Bash 和 Linux 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="98d12-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="98d12-137">這對 PowerShell 有何意義？</span><span class="sxs-lookup"><span data-stu-id="98d12-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="98d12-138">使用 OSS 專案時, 在許多情況下, 從 PowerShell 提示字元拖放至 Bash 非常有用。</span><span class="sxs-lookup"><span data-stu-id="98d12-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="98d12-139">Bash 支援是互補的, 可強化 Windows 上的命令列價值, 讓 PowerShell 和 PowerShell 社區得以運用其他熱門技術。</span><span class="sxs-lookup"><span data-stu-id="98d12-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="98d12-140">深入瞭解 PowerShell 小組的 blog-- [適用于 Windows 的 Bash:為什麼它非常棒, 而對 PowerShell 的意義是什麼？](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="98d12-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="98d12-141">我可以在 WSL 中執行所有 Linux 應用程式嗎？</span><span class="sxs-lookup"><span data-stu-id="98d12-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="98d12-142">不！</span><span class="sxs-lookup"><span data-stu-id="98d12-142">No!</span></span> <span data-ttu-id="98d12-143">WSL 是一種工具, 其目標是要讓需要他們的使用者在 Windows 上執行 Bash 和 core Linux 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="98d12-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="98d12-144">WSL 不是用來支援 GUI 桌上型電腦或應用程式 (例如 GNOME、KDE 等)</span><span class="sxs-lookup"><span data-stu-id="98d12-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="98d12-145">此外, 即使您可以執行許多熱門的伺服器應用程式 (例如 Redis), 也不建議使用 WSL 來裝載生產服務– Microsoft 提供各種解決方案, 讓您在 Azure、Hyper-v 和 Docker 中執行生產 Linux 工作負載。</span><span class="sxs-lookup"><span data-stu-id="98d12-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="98d12-146">WSL 包含哪些 Windows Sku？</span><span class="sxs-lookup"><span data-stu-id="98d12-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="98d12-147">適用于 Linux 的 windows 子系統可在 windows 10 年度版和建立者更新或更新版本的 Windows 桌上出版本上取得。</span><span class="sxs-lookup"><span data-stu-id="98d12-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="98d12-148">從秋季建立者更新 WSL 將可在 Windows 的桌面和伺服器 Sku 上取得。</span><span class="sxs-lookup"><span data-stu-id="98d12-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="98d12-149">WSL 支援哪些處理器？</span><span class="sxs-lookup"><span data-stu-id="98d12-149">What processors does WSL support?</span></span>
<span data-ttu-id="98d12-150">WSL 支援 x64 和 ARM Cpu。</span><span class="sxs-lookup"><span data-stu-id="98d12-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="98d12-151">如何? 存取我的 C: 磁片磁碟機嗎？</span><span class="sxs-lookup"><span data-stu-id="98d12-151">How do I access my C: drive?</span></span>
<span data-ttu-id="98d12-152">本機電腦上的硬碟掛接點會自動建立, 並可讓您輕鬆存取 Windows 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="98d12-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="98d12-153">**于/mnt/\<磁碟機號 >/**</span><span class="sxs-lookup"><span data-stu-id="98d12-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="98d12-154">使用方法的範例`cd /mnt/c`是存取 c:</span><span class="sxs-lookup"><span data-stu-id="98d12-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="98d12-155">如何? 搭配 Linux 應用程式使用 Windows 檔案？</span><span class="sxs-lookup"><span data-stu-id="98d12-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="98d12-156">WSL 的其中一項優點是能夠透過 Windows 和 Linux 應用程式或工具存取您的檔案。</span><span class="sxs-lookup"><span data-stu-id="98d12-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="98d12-157">WSL 會將您電腦的固定磁片磁碟機`/mnt/<drive>`掛接在 Linux 散發版本的資料夾底下。</span><span class="sxs-lookup"><span data-stu-id="98d12-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="98d12-158">例如, 您`C:`的磁片磁碟機裝載于`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="98d12-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="98d12-159">使用您載入的磁片磁碟機, 您可以在中編輯程式碼`C:\dev\myproj\` , 例如, 使用[Visual Studio](https://visualstudio.microsoft.com/vs/) /或[VS Code](https://code.visualstudio.com/), 然後透過存取相同`/mnt/c/dev/myproj`的檔案, 在 Linux 中建立/測試該程式碼。</span><span class="sxs-lookup"><span data-stu-id="98d12-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="98d12-160">**重要注意事項**:使用 WSL 的其中一個主要限制是, 不支援使用 Windows 應用程式或工具直接存取/變更 Linux 散發版本檔案系統中的檔案。</span><span class="sxs-lookup"><span data-stu-id="98d12-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="98d12-161">請參閱：[不要使用 Windows 應用程式和工具變更 Linux 檔案](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="98d12-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="98d12-162">Linux 磁片磁碟機中的檔案與裝載的 Windows 磁片磁碟機有何不同？</span><span class="sxs-lookup"><span data-stu-id="98d12-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="98d12-163">Linux 根目錄下的檔案 (亦即`/`) 是由模擬 linux 特定行為的 WSL 所控制, 包括但不限於:</span><span class="sxs-lookup"><span data-stu-id="98d12-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="98d12-164">包含無效 Windows 檔案名字元的檔案</span><span class="sxs-lookup"><span data-stu-id="98d12-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="98d12-165">為非系統管理員使用者建立的符號連結</span><span class="sxs-lookup"><span data-stu-id="98d12-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="98d12-166">透過 chmod 和 chown 變更檔案屬性</span><span class="sxs-lookup"><span data-stu-id="98d12-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="98d12-167">檔案/資料夾區分大小寫</span><span class="sxs-lookup"><span data-stu-id="98d12-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="98d12-168">裝載的磁片磁碟機中的檔案是由 Windows 所控制, 並具有下列行為:</span><span class="sxs-lookup"><span data-stu-id="98d12-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="98d12-169">支援區分大小寫</span><span class="sxs-lookup"><span data-stu-id="98d12-169">Support case sensitivity</span></span>
   * <span data-ttu-id="98d12-170">擁有權限都設定為最佳反映 Windows 許可權</span><span class="sxs-lookup"><span data-stu-id="98d12-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="98d12-171">當我執行 apt 時, 為什麼會發生太多錯誤-取得升級？</span><span class="sxs-lookup"><span data-stu-id="98d12-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="98d12-172">有些套件會使用我們尚未實行的功能。</span><span class="sxs-lookup"><span data-stu-id="98d12-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="98d12-173">`udev`例如, 尚不支援, 而且會導致數`apt-get upgrade`個錯誤。</span><span class="sxs-lookup"><span data-stu-id="98d12-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="98d12-174">若要修正與相關`udev`的問題, 請遵循下列步驟:</span><span class="sxs-lookup"><span data-stu-id="98d12-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="98d12-175">將下列`/usr/sbin/policy-rc.d`程式寫入並儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="98d12-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="98d12-176">將執行許可權新增至`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="98d12-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="98d12-177">執行下列命令</span><span class="sxs-lookup"><span data-stu-id="98d12-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="98d12-178">如何? 卸載 WSL 散發套件嗎？</span><span class="sxs-lookup"><span data-stu-id="98d12-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="98d12-179">在 1709 (16299) 之前的組建上, 開啟命令提示字元並執行:</span><span class="sxs-lookup"><span data-stu-id="98d12-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="98d12-180">從存放區安裝的 WSL 散發套件可以像任何其他 Windows 應用程式一樣卸載, 方法是以滑鼠右鍵按一下應用程式磚, 然後按一下 [卸載], 或透過 PowerShell 使用[ `Remove-AppxPackage` Cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。</span><span class="sxs-lookup"><span data-stu-id="98d12-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="98d12-181">為什麼 ping 產生許可權被拒錯誤？</span><span class="sxs-lookup"><span data-stu-id="98d12-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="98d12-182">在 WSL 組建 < 14926 中, 透過提升許可權的主控台執行 ping 所需的 WSL。</span><span class="sxs-lookup"><span data-stu-id="98d12-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="98d12-183">此問題已在組建14926和更新版本中修正。</span><span class="sxs-lookup"><span data-stu-id="98d12-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="98d12-184">如何? 執行 OpenSSH 伺服器？</span><span class="sxs-lookup"><span data-stu-id="98d12-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="98d12-185">需要 Windows 中的系統管理員許可權, 才能在 WSL 中執行 OpenSSH。</span><span class="sxs-lookup"><span data-stu-id="98d12-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="98d12-186">若要執行 OpenSSH 伺服器, 請以系統管理員身分在 Windows 上的 Ubuntu 上執行 Bash, 或從具有系統管理員許可權的 CMD/PowerShell 提示字元執行 bash。</span><span class="sxs-lookup"><span data-stu-id="98d12-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="98d12-187">為什麼會收到「錯誤:0x80040306 "當我嘗試安裝時？</span><span class="sxs-lookup"><span data-stu-id="98d12-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="98d12-188">WSL 不支援在舊版主控台中執行。</span><span class="sxs-lookup"><span data-stu-id="98d12-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="98d12-189">若要關閉舊版主控台:</span><span class="sxs-lookup"><span data-stu-id="98d12-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="98d12-190">開啟 WSL、PowerShell 或 Cmd</span><span class="sxs-lookup"><span data-stu-id="98d12-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="98d12-191">以滑鼠右鍵按一下標題列-> 屬性-> 取消核取 [使用舊版主控台]</span><span class="sxs-lookup"><span data-stu-id="98d12-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="98d12-192">按一下 [確定]</span><span class="sxs-lookup"><span data-stu-id="98d12-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="98d12-193">為什麼會收到「錯誤:0x80040154 「在升級 Windows 之後執行 bash .exe 嗎？</span><span class="sxs-lookup"><span data-stu-id="98d12-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="98d12-194">「適用于 Linux 的 Windows 子系統」功能可能會在 Windows 更新期間停用。</span><span class="sxs-lookup"><span data-stu-id="98d12-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="98d12-195">如果發生這種情況, 則必須重新啟用 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="98d12-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="98d12-196">如需如何啟用「適用于 Linux 的 Windows 子系統」功能的指示, 請參閱[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。</span><span class="sxs-lookup"><span data-stu-id="98d12-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="98d12-197">如何? 變更 WSL 的顯示語言？</span><span class="sxs-lookup"><span data-stu-id="98d12-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="98d12-198">WSL install 會嘗試自動變更 Ubuntu 地區設定, 以符合 Windows 安裝的地區設定。</span><span class="sxs-lookup"><span data-stu-id="98d12-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="98d12-199">如果您不想要此行為, 您可以執行此命令, 以在安裝完成後變更 Ubuntu 地區設定。</span><span class="sxs-lookup"><span data-stu-id="98d12-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="98d12-200">您必須重新開機 bash, 這種變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="98d12-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="98d12-201">下列範例會將地區設定變更為 en-us:</span><span class="sxs-lookup"><span data-stu-id="98d12-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="98d12-202">為什麼我無法從 WSL 存取網際網路？</span><span class="sxs-lookup"><span data-stu-id="98d12-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="98d12-203">某些使用者回報了在 WSL 中封鎖網際網路存取的特定防火牆應用程式問題。</span><span class="sxs-lookup"><span data-stu-id="98d12-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="98d12-204">回報的防火牆如下:</span><span class="sxs-lookup"><span data-stu-id="98d12-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="98d12-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="98d12-205">Kaspersky</span></span>
1. <span data-ttu-id="98d12-206">AVG</span><span class="sxs-lookup"><span data-stu-id="98d12-206">AVG</span></span>
1. <span data-ttu-id="98d12-207">Avast</span><span class="sxs-lookup"><span data-stu-id="98d12-207">Avast</span></span>

<span data-ttu-id="98d12-208">在某些情況下, 關閉防火牆可讓您存取。</span><span class="sxs-lookup"><span data-stu-id="98d12-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="98d12-209">在某些情況下, 只安裝防火牆會顯示封鎖存取。</span><span class="sxs-lookup"><span data-stu-id="98d12-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="98d12-210">如何? 從 Windows 中的 WSL 存取埠？</span><span class="sxs-lookup"><span data-stu-id="98d12-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="98d12-211">WSL 會共用 Windows 的 IP 位址, 因為它是在 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="98d12-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="98d12-212">如此一來, 您就可以存取 localhost 上的任何埠, 例如, 如果您在埠 1234 https://localhost:1234 上有 web 內容, 您可以進入 Windows 瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="98d12-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="98d12-213">如何備份我的 WSL 散發版本？</span><span class="sxs-lookup"><span data-stu-id="98d12-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="98d12-214">備份散發版本的最佳方式是在 Windows 1809 版和更新版本中提供。</span><span class="sxs-lookup"><span data-stu-id="98d12-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="98d12-215">您可以使用`wsl --export`命令, 將整個散發匯出至 tarball。</span><span class="sxs-lookup"><span data-stu-id="98d12-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="98d12-216">接著, 您可以使用命令將`wsl --import`此散發版本匯回 WSL, 讓您可以備份和儲存 WSL 散發的狀態。</span><span class="sxs-lookup"><span data-stu-id="98d12-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="98d12-217">請注意, 在 Appdata 資料夾 (例如 Windows Backup) 中備份檔案的傳統備份服務將不會損毀您的 Linux 檔案。</span><span class="sxs-lookup"><span data-stu-id="98d12-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="98d12-218">我可以在哪裡提供意見反應？</span><span class="sxs-lookup"><span data-stu-id="98d12-218">Where can I provide feedback?</span></span>

<span data-ttu-id="98d12-219">您可以透過多個管道來分享意見反應並提出問題:意見反應和問題應導向至:</span><span class="sxs-lookup"><span data-stu-id="98d12-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="98d12-220">我們的[GitHub 問題追蹤](https://github.com/Microsoft/BashOnWindows/issues)程式</span><span class="sxs-lookup"><span data-stu-id="98d12-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="98d12-221">我們[的命令列 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="98d12-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="98d12-222">我們[的命令列小組 blog](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="98d12-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="98d12-223">透過 Twitter。</span><span class="sxs-lookup"><span data-stu-id="98d12-223">Via Twitter.</span></span> <span data-ttu-id="98d12-224">請在[@richturn_ms](https://twitter.com/richturn_MS) Twitter 上追蹤以瞭解新聞、更新等等。</span><span class="sxs-lookup"><span data-stu-id="98d12-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
