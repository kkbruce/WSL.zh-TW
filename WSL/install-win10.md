---
title: 在 Windows 10 上安裝適用于 Linux 的 Windows 子系統 (WSL)
description: 適用于 Windows 10 上適用于 Linux 的 Windows 子系統的安裝指示。
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499281"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="69bed-104">適用于 Linux 的 windows 子系統安裝指南 Windows 10</span><span class="sxs-lookup"><span data-stu-id="69bed-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="69bed-105">安裝適用于 Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="69bed-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="69bed-106">在安裝任何適用于 WSL 的 Linux 散發版本之前, 您必須確定已啟用「適用于 Linux 的 Windows 子系統」選用功能:</span><span class="sxs-lookup"><span data-stu-id="69bed-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="69bed-107">以系統管理員身分開啟 PowerShell 並執行:</span><span class="sxs-lookup"><span data-stu-id="69bed-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="69bed-108">出現提示時, 重新開機您的電腦。</span><span class="sxs-lookup"><span data-stu-id="69bed-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="69bed-109">安裝您選擇的 Linux 散發套件</span><span class="sxs-lookup"><span data-stu-id="69bed-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="69bed-110">若要下載並安裝您慣用的散發版本, 您有三個選擇:</span><span class="sxs-lookup"><span data-stu-id="69bed-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="69bed-111">從 Microsoft Store 下載並安裝 (請參閱下文)</span><span class="sxs-lookup"><span data-stu-id="69bed-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="69bed-112">從命令列/腳本下載並安裝 ([閱讀手動安裝指示](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="69bed-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="69bed-113">下載並手動打開封裝並安裝 (適用于 Windows Server-[此處的指示](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="69bed-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="69bed-114">Windows 10 秋季建立者更新和更新版本:從 Microsoft Store 安裝</span><span class="sxs-lookup"><span data-stu-id="69bed-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="69bed-115">本節適用于 Windows 組建16215或更新版本。</span><span class="sxs-lookup"><span data-stu-id="69bed-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="69bed-116">請遵循下列步驟來[檢查您的組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="69bed-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="69bed-117">開啟 Microsoft Store, 然後選擇您最愛的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="69bed-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store 中的 Linux 散發版本視圖](media/store.png)

    <span data-ttu-id="69bed-119">下列連結會開啟每個散發套件的 Microsoft store 頁面:</span><span class="sxs-lookup"><span data-stu-id="69bed-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="69bed-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="69bed-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="69bed-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="69bed-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="69bed-122">OpenSUSE 閏15</span><span class="sxs-lookup"><span data-stu-id="69bed-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="69bed-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="69bed-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="69bed-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="69bed-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="69bed-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="69bed-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="69bed-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="69bed-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="69bed-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="69bed-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="69bed-128">適用于 WSL 的 Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="69bed-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="69bed-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="69bed-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="69bed-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="69bed-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="69bed-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="69bed-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="69bed-132">從散發版本的頁面中, 選取 [取得]</span><span class="sxs-lookup"><span data-stu-id="69bed-132">From the distro's page, select "Get"</span></span>

    ![Microsoft store 中的 Linux 散發版本視圖](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="69bed-134">完成散發版本的初始化</span><span class="sxs-lookup"><span data-stu-id="69bed-134">Complete initialization of your distro</span></span>
<span data-ttu-id="69bed-135">現在已安裝您的 Linux 散發版本, 您必須先[初始化新的散發版本實例](initialize-distro.md)一次, 才能使用它。</span><span class="sxs-lookup"><span data-stu-id="69bed-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="69bed-136">疑難排解：</span><span class="sxs-lookup"><span data-stu-id="69bed-136">Troubleshooting:</span></span> 

<span data-ttu-id="69bed-137">以下是相關的錯誤和建議的修正。</span><span class="sxs-lookup"><span data-stu-id="69bed-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="69bed-138">如需其他常見錯誤及其解決方案, 請參閱[WSL 疑難排解頁面](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="69bed-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="69bed-139">**安裝失敗, 發生錯誤0x80070003**</span><span class="sxs-lookup"><span data-stu-id="69bed-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="69bed-140">適用于 Linux 的 Windows 子系統只會在您的系統磁片磁碟機上執行`C:` (通常是您的磁片磁碟機)。</span><span class="sxs-lookup"><span data-stu-id="69bed-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="69bed-141">請確定散發版本儲存在您的系統磁片磁碟機上:</span><span class="sxs-lookup"><span data-stu-id="69bed-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="69bed-142">開啟 [**設定** -> ] [**儲存體** -> **] [其他存放裝置設定]:變更系統設定的新內容**儲存
     ![位置, 以在 C: 磁片磁碟機上安裝應用程式](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="69bed-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="69bed-143">**WslRegisterDistribution 失敗, 發生錯誤0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="69bed-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="69bed-144">未啟用適用于 Linux 的 Windows 子系統選用元件:</span><span class="sxs-lookup"><span data-stu-id="69bed-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="69bed-145">開啟 **控制台** ->  **程式和功能**-> \* \* 開啟或關閉 windows 功能 \* *-> 檢查\*\*適用于 Linux 的 windows 子系統,*\* 或使用本文開頭所述的 PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69bed-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
