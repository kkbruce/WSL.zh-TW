---
title: 在 Windows Server 上安裝 Linux 子系統
description: Windows Server 上 Linux 子系統的安裝指示。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu、windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308794"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="6c0aa-104">Windows Server 安裝指南</span><span class="sxs-lookup"><span data-stu-id="6c0aa-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="6c0aa-105">適用于 Windows Server 2019 和更新版本</span><span class="sxs-lookup"><span data-stu-id="6c0aa-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="6c0aa-106">在//Build2017, Microsoft 宣佈 windows Server 上適用于 Linux 的 Windows 子系統將可[供使用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="6c0aa-107">這些指示會逐步解說如何在 Windows Server 1709 和更新版本上執行適用于 Linux 的 Windows 子系統。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="6c0aa-108">啟用適用于 Linux 的 Windows 子系統 (WSL)</span><span class="sxs-lookup"><span data-stu-id="6c0aa-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="6c0aa-109">您必須先啟用「適用于 Linux 的 Windows 子系統」選用功能並重新啟動, 才可以在 Windows 上執行 Linux 散發版本。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="6c0aa-110">以系統管理員身分開啟 PowerShell 並執行:</span><span class="sxs-lookup"><span data-stu-id="6c0aa-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="6c0aa-111">出現提示時, 重新開機您的電腦。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-111">Restart your computer when prompted.</span></span> <span data-ttu-id="6c0aa-112">**這是必要的重新開機**, 以便確保 WSL 可以起始受信任的執行環境。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="6c0aa-113">下載 Linux 散發版本</span><span class="sxs-lookup"><span data-stu-id="6c0aa-113">Download a Linux distro</span></span>

<span data-ttu-id="6c0aa-114">請遵循[這些指示](install-manual.md)來下載您最愛的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="6c0aa-115">解壓縮並安裝 Linux 散發版本</span><span class="sxs-lookup"><span data-stu-id="6c0aa-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="6c0aa-116">既然您已下載散發版本, 請將其內容解壓縮並手動安裝散發版本:</span><span class="sxs-lookup"><span data-stu-id="6c0aa-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="6c0aa-117">`<distro>.appx`解壓縮套件的內容, 例如使用 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6c0aa-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="6c0aa-118">執行散發版本啟動器以完成安裝, 在名為`<distro>.exe`的目的檔案夾中執行散發版本啟動器應用程式。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="6c0aa-119">例如: `ubuntu.exe`、等等。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上擴充的 Ubuntu 散發版本](media/server-appx-expand.png)

    > <span data-ttu-id="6c0aa-121">**疑難排解**</span><span class="sxs-lookup"><span data-stu-id="6c0aa-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="6c0aa-122">**安裝失敗, 發生錯誤 0x8007007e**:當您的系統不支援 WSL 時, 就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="6c0aa-123">請確認︰</span><span class="sxs-lookup"><span data-stu-id="6c0aa-123">Make sure that:</span></span>
    >   * <span data-ttu-id="6c0aa-124">您正在執行 Windows 組建16215或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="6c0aa-125">[檢查您的組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="6c0aa-126">[適用于 Linux 的 Windows 子系統] 選用元件已啟用, 且電腦已重新開機。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="6c0aa-127">[請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="6c0aa-128">將您的散發版本路徑新增至 Windows 環境路徑`C:\Users\Administrator\Ubuntu` (在此範例中為), 例如使用 Powershell:</span><span class="sxs-lookup"><span data-stu-id="6c0aa-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="6c0aa-129">您現在可以輸入`<distro>.exe`, 從任何路徑啟動散發版本。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="6c0aa-130">例如：`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="6c0aa-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="6c0aa-131">現在已安裝您的 Linux 散發版本, 您必須先[初始化新的散發版本實例](initialize-distro.md), 然後再使用散發版本。</span><span class="sxs-lookup"><span data-stu-id="6c0aa-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
