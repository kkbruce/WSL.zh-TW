---
title: 手動下載適用于 Linux 的 Windows 子系統 (WSL) 散發版本
description: 如何手動下載適用于 Linux 的 Windows 子系統發行版本的指示。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、WSL、windows 子系統、散發版本、ubuntu、openSUSE、SLES、debian、kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: bf2f2e24fb8a2db49270fb77558d4fda1828dedf
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523775"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="fb45a-104">手動下載適用于 Linux 的 Windows 子系統散發版本套件</span><span class="sxs-lookup"><span data-stu-id="fb45a-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="fb45a-105">在幾種情況下, 您可能無法 (或想要) 透過 Microsoft Store 安裝 WSL Linux 散發版本。</span><span class="sxs-lookup"><span data-stu-id="fb45a-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="fb45a-106">具體而言, 您可能正在執行不支援 Microsoft Store 的 Windows Server 或長期維護 (LTSC) 桌面作業系統 SKU, 或公司網路原則及/或系統管理員不允許在您的環境中使用 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="fb45a-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="fb45a-107">在這些情況下, 雖然 WSL 本身可供使用, 如果您無法存取存放區, 如何在 WSL 中下載並安裝 Linux 散發版本？</span><span class="sxs-lookup"><span data-stu-id="fb45a-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="fb45a-108">注意:**不允許在 Windows 10 S 模式上執行命令列 shell 環境, 包括 Cmd、PowerShell 和 Linux/WSL 散發版本**。</span><span class="sxs-lookup"><span data-stu-id="fb45a-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="fb45a-109">這項限制是為了確保 S 模式所提供的完整性和安全目標:如需詳細資訊, 請閱讀[這篇文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)。</span><span class="sxs-lookup"><span data-stu-id="fb45a-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="fb45a-110">正在下載散發版本</span><span class="sxs-lookup"><span data-stu-id="fb45a-110">Downloading distros</span></span>

<span data-ttu-id="fb45a-111">如果無法使用 Microsoft Store 應用程式, 您可以按一下下列連結, 下載並手動安裝 Linux 散發版本:</span><span class="sxs-lookup"><span data-stu-id="fb45a-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="fb45a-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="fb45a-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="fb45a-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="fb45a-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="fb45a-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="fb45a-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="fb45a-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="fb45a-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="fb45a-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="fb45a-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="fb45a-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="fb45a-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="fb45a-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="fb45a-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="fb45a-119">適用于 WSL 的 Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="fb45a-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="fb45a-120">這會導致`<distro>.appx`套件下載到您選擇的資料夾。</span><span class="sxs-lookup"><span data-stu-id="fb45a-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="fb45a-121">遵循[安裝指示](#Installing-your-distro)來安裝您下載的散發版本。</span><span class="sxs-lookup"><span data-stu-id="fb45a-121">Follow the [installation instructions](#Installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="fb45a-122">透過命令列下載散發版本</span><span class="sxs-lookup"><span data-stu-id="fb45a-122">Downloading distros via the command line</span></span>
<span data-ttu-id="fb45a-123">如果您想要的話, 也可以透過命令列下載您偏好的散發版本:</span><span class="sxs-lookup"><span data-stu-id="fb45a-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="fb45a-124">使用 PowerShell 下載</span><span class="sxs-lookup"><span data-stu-id="fb45a-124">Download using PowerShell</span></span>
 <span data-ttu-id="fb45a-125">若要使用 PowerShell 下載散發版本, 請使用[WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb45a-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="fb45a-126">以下是下載 Ubuntu 16.04 的範例指示。</span><span class="sxs-lookup"><span data-stu-id="fb45a-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="fb45a-127">如果下載花費較長的時間, 請設定來關閉進度列`$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="fb45a-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="fb45a-128">使用捲曲下載</span><span class="sxs-lookup"><span data-stu-id="fb45a-128">Download using curl</span></span>
<span data-ttu-id="fb45a-129">Windows 10 春季 2018 Update (或更新版本) 包含常用的[捲曲命令列公用程式](https://curl.haxx.se/), 可讓您從命令列叫用 web 要求 (例如 HTTP GET、POST、PUT 等命令)。</span><span class="sxs-lookup"><span data-stu-id="fb45a-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="fb45a-130">您可以使用`curl.exe`下載上述散發版本:</span><span class="sxs-lookup"><span data-stu-id="fb45a-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="fb45a-131">在上述範例中, `curl.exe`會執行 (而不`curl`只是), 以確保在 PowerShell 中叫用實際的可執行檔, 而不是叫用[WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)的 powershell 捲曲別名</span><span class="sxs-lookup"><span data-stu-id="fb45a-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="fb45a-132">注意:如果`curl`您必須使用 Cmd shell 和/或`.bat`  /  `.cmd`腳本來叫用/編寫下載步驟, 則使用可能會比較理想。</span><span class="sxs-lookup"><span data-stu-id="fb45a-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="fb45a-133">安裝散發版本</span><span class="sxs-lookup"><span data-stu-id="fb45a-133">Installing your distro</span></span>
<span data-ttu-id="fb45a-134">如果您使用的是 Windows 10, 您可以使用 PowerShell 安裝散發版本。</span><span class="sxs-lookup"><span data-stu-id="fb45a-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="fb45a-135">只要流覽至包含上述散發版本所下載的資料夾, 然後在該目錄中執行下列命令, `app_name`其中是散發版本 .appx 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb45a-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="fb45a-136">如果您使用的是 Windows server, 可以在[Windows server](install-on-server.md)檔頁面上找到安裝指示。</span><span class="sxs-lookup"><span data-stu-id="fb45a-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="fb45a-137">安裝散發版本之後, 請參閱[Intilization 步驟](initialize-distro.md)頁面以初始化新的散發版本。</span><span class="sxs-lookup"><span data-stu-id="fb45a-137">Once your distro is installed please refer to the [Intilization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
