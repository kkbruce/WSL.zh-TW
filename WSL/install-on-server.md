---
title: Windows Server 上安裝 Linux 子系統
description: 在 Windows Server 上的 Linux 子系統的安裝指示。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 windows server 的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063616"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="2d3fe-104">Windows Server 安裝指南</span><span class="sxs-lookup"><span data-stu-id="2d3fe-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="2d3fe-105">適用於 Windows Server 2019 和更新版本</span><span class="sxs-lookup"><span data-stu-id="2d3fe-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="2d3fe-106">在 / / Build2017，Microsoft 宣布，將會是適用於 Linux 的 Windows 子系統[Windows Server 上可用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="2d3fe-107">這些指示會逐步執行適用於 Linux 的 Windows Server 1709 和更新版本的 Windows 子系統。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="2d3fe-108">啟用適用於 Linux (WSL) 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="2d3fe-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="2d3fe-109">您可以在 Windows 上執行的 Linux 散發版本之前，您必須啟用 「 Windows Linux 子系統 」 選擇性功能，並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="2d3fe-110">系統管理員身分開啟 PowerShell 並執行：</span><span class="sxs-lookup"><span data-stu-id="2d3fe-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="2d3fe-111">重新啟動您的電腦，當系統提示您。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-111">Restart your computer when prompted.</span></span> <span data-ttu-id="2d3fe-112">**這必須重新開機**為了確保 WSL 可以起始受信任的執行環境。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="2d3fe-113">下載 Linux 發行版本</span><span class="sxs-lookup"><span data-stu-id="2d3fe-113">Download a Linux distro</span></span>

<span data-ttu-id="2d3fe-114">請遵循[這些指示](install-manual.md)若要下載您最愛的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="2d3fe-115">解壓縮並安裝 Linux 發行版本</span><span class="sxs-lookup"><span data-stu-id="2d3fe-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="2d3fe-116">既然您已下載的散發版本，就會將其內容解壓縮，並手動安裝散發版本：</span><span class="sxs-lookup"><span data-stu-id="2d3fe-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="2d3fe-117">擷取`<distro>.appx`套件的內容，例如，使用 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="2d3fe-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="2d3fe-118">執行散發啟動器若要完成安裝，請在 [目標] 資料夾中，執行 distro 啟動器應用程式，名為`<distro>.exe`。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="2d3fe-119">例如：`ubuntu.exe`等等。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-119">For example: `ubuntu.exe`, etc.</span></span>

    ![擴充的 Windows Server 上的 Ubuntu 散發套件](media/server-appx-expand.png)

    > **<span data-ttu-id="2d3fe-121">疑難排解</span><span class="sxs-lookup"><span data-stu-id="2d3fe-121">Troubleshooting</span></span>**
    > * <span data-ttu-id="2d3fe-122">**安裝失敗，錯誤 0x8007007e**:當您的系統不支援 WSL 時，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="2d3fe-123">請確認︰</span><span class="sxs-lookup"><span data-stu-id="2d3fe-123">Make sure that:</span></span>
    >   * <span data-ttu-id="2d3fe-124">您正在執行 Windows 組建，16215 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="2d3fe-125">[請檢查您的組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="2d3fe-126">已啟用 Linux 選擇性元件的 Windows 子系統，並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="2d3fe-127">[請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="2d3fe-128">將您的散發套件路徑新增至 Windows 環境的路徑 (`C:\Users\Administrator\Ubuntu`在此範例中)，例如，使用 Powershell:</span><span class="sxs-lookup"><span data-stu-id="2d3fe-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="2d3fe-129">您現在可以啟動您的散發版本，從任何路徑輸入`<distro>.exe`。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="2d3fe-130">例如: </span><span class="sxs-lookup"><span data-stu-id="2d3fe-130">For example:</span></span> `ubuntu.exe`

<span data-ttu-id="2d3fe-131">既然您的 Linux 散發套件已安裝，您必須[初始化新的散發版本執行個體](initialize-distro.md)才能使用您的散發套件。</span><span class="sxs-lookup"><span data-stu-id="2d3fe-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
