---
title: 安裝適用於 Windows 10 上的 Linux (WSL) 的 Windows 子系統
description: Windows 子系統的安裝指示適用於 Windows 10 上的 Linux。
keywords: 安裝 BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035058"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="61518-104">Linux 安裝指南，適用於 Windows 10 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="61518-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="61518-105">安裝適用於 Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="61518-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="61518-106">之前的 WSL 安裝任何 Linux 散發版本，您必須確定 「 Windows 子系統的 Linux 」 啟用選擇性功能：</span><span class="sxs-lookup"><span data-stu-id="61518-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="61518-107">系統管理員身分開啟 PowerShell 並執行：</span><span class="sxs-lookup"><span data-stu-id="61518-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="61518-108">重新啟動您的電腦，當系統提示您。</span><span class="sxs-lookup"><span data-stu-id="61518-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="61518-109">安裝您的 Linux 散發套件的選擇</span><span class="sxs-lookup"><span data-stu-id="61518-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="61518-110">若要下載並安裝您慣用的 distro(s)，您會有三種選擇：</span><span class="sxs-lookup"><span data-stu-id="61518-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="61518-111">從 Windows 市集 （如下所示） 下載並安裝</span><span class="sxs-lookup"><span data-stu-id="61518-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="61518-112">從命令列/指令下載並安裝 ([讀取的手動安裝指示](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="61518-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="61518-113">下載手動解壓縮並安裝 (適用於 Windows Server-[這裡的指示](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="61518-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="61518-114">Windows 10 Fall Creators Update 和更新版本：從 Microsoft Store 安裝</span><span class="sxs-lookup"><span data-stu-id="61518-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="61518-115">此區段可讓 Windows 組建 16215 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="61518-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="61518-116">請遵循下列步驟[來檢查組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="61518-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="61518-117">開啟 Microsoft Store，並選擇您最愛的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="61518-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/store.png)

    <span data-ttu-id="61518-119">下列連結會開啟 [Windows 市集] 頁面的每個散發：</span><span class="sxs-lookup"><span data-stu-id="61518-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="61518-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="61518-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="61518-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="61518-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="61518-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="61518-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="61518-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="61518-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="61518-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="61518-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="61518-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="61518-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="61518-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="61518-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="61518-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="61518-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="61518-128">Fedora Remix 的 WSL</span><span class="sxs-lookup"><span data-stu-id="61518-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="61518-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="61518-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="61518-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="61518-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="61518-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="61518-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="61518-132">從散發版本的頁面上，選取 "Get"</span><span class="sxs-lookup"><span data-stu-id="61518-132">From the distro's page, select "Get"</span></span>

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="61518-134">您的散發版本的完成初始化</span><span class="sxs-lookup"><span data-stu-id="61518-134">Complete initialization of your distro</span></span>
<span data-ttu-id="61518-135">既然您的 Linux 散發套件已安裝，您必須[初始化新的散發版本執行個體](initialize-distro.md)一次，才能使用。</span><span class="sxs-lookup"><span data-stu-id="61518-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="61518-136">疑難排解：</span><span class="sxs-lookup"><span data-stu-id="61518-136">Troubleshooting:</span></span> 

<span data-ttu-id="61518-137">以下是相關的錯誤和建議的修正。</span><span class="sxs-lookup"><span data-stu-id="61518-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="61518-138">請參閱[WSL 疑難排解頁面](troubleshooting.md)其他常見的錯誤和他們的解決方案。</span><span class="sxs-lookup"><span data-stu-id="61518-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="61518-139">**安裝失敗，錯誤 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="61518-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="61518-140">適用於 Linux 的 Windows 子系統只在您的系統磁碟機上執行 (這通常是您`C:`磁碟機)。</span><span class="sxs-lookup"><span data-stu-id="61518-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="61518-141">請確定發行版本會儲存您的系統磁碟機上：</span><span class="sxs-lookup"><span data-stu-id="61518-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="61518-142">開啟**設定** -> **儲存體** -> **更多的儲存體設定：新的內容儲存的變更**
    ![系統設定的 c： 磁碟機上安裝應用程式中的圖片](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="61518-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="61518-143">**失敗，錯誤 0x8007019e WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="61518-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="61518-144">適用於 Linux 的選用元件未啟用 Windows 子系統：</span><span class="sxs-lookup"><span data-stu-id="61518-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="61518-145">開啟**控制台中** -> **程式和功能**-> \* \* 開啟或關閉 Windows 功能-> 核取**適用於 Linux 的 Windows 子系統**或使用在本文開頭所述的 PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61518-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
