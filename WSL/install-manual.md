---
title: 手動下載 Linux (WSL) 散發版本的 Windows 子系統
description: 如何手動下載針對 Linux 發行版本的 Windows 子系統的指示。
keywords: BashOnWindows、 bash、 wsl、 windows、 windows subsystem for linux WSL，windows 子系統、 散發版本、 ubuntu、 openSUSE、 SLES，debian，kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063566"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="67988-104">手動下載 Linux 散發套件的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="67988-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="67988-105">有幾個案例中您可能不會 （或不想） 若要安裝 WSL Linux 散發版本，透過 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="67988-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="67988-106">具體來說，您可能會執行 Windows Server 或長期維護 (LTSB/LTSC) 桌面 OS SKU 不支援 Microsoft Store，或您公司的網路原則和/或系統管理員不允許您的環境中的 Microsoft Store 使用量。</span><span class="sxs-lookup"><span data-stu-id="67988-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="67988-107">在這些情況下，而本身的 WSL 可用，如何下載及安裝 WSL 中的 Linux 散發版本，如果您無法存取存放區嗎？</span><span class="sxs-lookup"><span data-stu-id="67988-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="67988-108">注意：**命令列殼層的環境，包括 Cmd、 PowerShell 和 Linux/WSL 散發版本不允許執行 Windows 10 S 模式**。</span><span class="sxs-lookup"><span data-stu-id="67988-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="67988-109">這項限制是為了確保 S 模式提供的完整性和安全性目標：讀取[這篇文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="67988-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="67988-110">下載散發版本</span><span class="sxs-lookup"><span data-stu-id="67988-110">Downloading distros</span></span>

<span data-ttu-id="67988-111">如果找不到 Microsoft Store 應用程式，您可以下載，並按一下這些連結，手動安裝的 Linux 散發版本：</span><span class="sxs-lookup"><span data-stu-id="67988-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="67988-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="67988-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="67988-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="67988-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="67988-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="67988-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="67988-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="67988-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="67988-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="67988-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="67988-117">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="67988-117">OpenSUSE</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="67988-118">SLES</span><span class="sxs-lookup"><span data-stu-id="67988-118">SLES</span></span>](https://aka.ms/wsl-sles-12)

<span data-ttu-id="67988-119">這會導致`<distro>.appx`套件下載至您所選擇的資料夾。</span><span class="sxs-lookup"><span data-stu-id="67988-119">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="67988-120">請遵循[安裝指示](#installing-your-distro)安裝您已下載的 distro(s)。</span><span class="sxs-lookup"><span data-stu-id="67988-120">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="67988-121">下載透過命令列的散發套件</span><span class="sxs-lookup"><span data-stu-id="67988-121">Downloading distros via the command line</span></span>
<span data-ttu-id="67988-122">如果您想，您也可以下載您慣用的 distro(s) 透過命令列：</span><span class="sxs-lookup"><span data-stu-id="67988-122">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="67988-123">使用 PowerShell 下載</span><span class="sxs-lookup"><span data-stu-id="67988-123">Download using PowerShell</span></span>
 <span data-ttu-id="67988-124">若要下載使用 PowerShell 的散發版本，請使用[Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67988-124">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="67988-125">以下是範例指示，來下載 Ubuntu 16.04。</span><span class="sxs-lookup"><span data-stu-id="67988-125">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="67988-126">如果下載花費很長的時間，將進度列關閉設定 `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="67988-126">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="67988-127">使用 curl 下載</span><span class="sxs-lookup"><span data-stu-id="67988-127">Download using curl</span></span>
<span data-ttu-id="67988-128">Windows 10 Spring 2018 Update （或更新版本） 包含熱門[curl 命令列公用程式](https://curl.haxx.se/)，您可以叫用 web 要求 (也就是 HTTP GET、 POST、 PUT、 等命令) 從命令列。</span><span class="sxs-lookup"><span data-stu-id="67988-128">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="67988-129">您可以使用`curl.exe`下載上述的散發版本：</span><span class="sxs-lookup"><span data-stu-id="67988-129">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="67988-130">在上述範例中，`curl.exe`執行 (不是只`curl`) 來確保，在 PowerShell 中，實際的 curl 可執行檔是叫用，不別名的 PowerShell curl [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="67988-130">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="67988-131">注意：使用`curl`可能比較適合，如果您必須叫用/指令碼下載使用 Cmd shell 中的步驟和 （或) `.bat`  /  `.cmd`指令碼。</span><span class="sxs-lookup"><span data-stu-id="67988-131">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="67988-132">安裝您的散發套件</span><span class="sxs-lookup"><span data-stu-id="67988-132">Installing your distro</span></span>
<span data-ttu-id="67988-133">如需有關如何安裝您已下載的 distro(s) 的指示，請參閱[Windows 桌面](install-win10.md)或是[Windows Server](install-on-server.md)安裝指示。</span><span class="sxs-lookup"><span data-stu-id="67988-133">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
