---
title: 在 Windows 10 上安裝 Windows 子系統適用於 Linux (WSL)
description: Windows 子系統的安裝指示適用於 Windows 10 上的 Linux。
keywords: 安裝 BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063286"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="d055a-104">Linux 安裝指南，適用於 Windows 10 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="d055a-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="d055a-105">安裝適用於 Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="d055a-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="d055a-106">之前的 WSL 安裝任何 Linux 散發版本，您必須確定 「 Windows 子系統的 Linux 」 啟用選擇性功能：</span><span class="sxs-lookup"><span data-stu-id="d055a-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="d055a-107">系統管理員身分開啟 PowerShell 並執行：</span><span class="sxs-lookup"><span data-stu-id="d055a-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="d055a-108">重新啟動您的電腦，當系統提示您。</span><span class="sxs-lookup"><span data-stu-id="d055a-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="d055a-109">安裝您的 Linux 散發套件的選擇</span><span class="sxs-lookup"><span data-stu-id="d055a-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="d055a-110">若要下載並安裝您慣用的 distro(s)，您會有三種選擇：</span><span class="sxs-lookup"><span data-stu-id="d055a-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="d055a-111">從 Windows 市集 （如下所示） 下載並安裝</span><span class="sxs-lookup"><span data-stu-id="d055a-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="d055a-112">從命令列/指令下載並安裝 ([讀取的手動安裝指示](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="d055a-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="d055a-113">下載手動解壓縮並安裝 (適用於 Windows Server-[這裡的指示](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="d055a-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="d055a-114">Windows 10 Fall Creators Update 和更新版本：從 Microsoft Store 安裝</span><span class="sxs-lookup"><span data-stu-id="d055a-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="d055a-115">此區段可讓 Windows 組建 16215 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d055a-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="d055a-116">請遵循下列步驟[來檢查組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="d055a-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="d055a-117">開啟 Microsoft Store，並選擇您最愛的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="d055a-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/store.png)

    <span data-ttu-id="d055a-119">下列連結會開啟 [Windows 市集] 頁面的每個散發：</span><span class="sxs-lookup"><span data-stu-id="d055a-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="d055a-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="d055a-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="d055a-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="d055a-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="d055a-122">SLES</span><span class="sxs-lookup"><span data-stu-id="d055a-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="d055a-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="d055a-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="d055a-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="d055a-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="d055a-125">從散發版本的頁面上，選取 "Get"</span><span class="sxs-lookup"><span data-stu-id="d055a-125">From the distro's page, select "Get"</span></span>

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="d055a-127">您的散發版本的完成初始化</span><span class="sxs-lookup"><span data-stu-id="d055a-127">Complete initialization of your distro</span></span>
<span data-ttu-id="d055a-128">既然您的 Linux 散發套件已安裝，您必須[初始化新的散發版本執行個體](initialize-distro.md)一次，才能使用。</span><span class="sxs-lookup"><span data-stu-id="d055a-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d055a-129">疑難排解：</span><span class="sxs-lookup"><span data-stu-id="d055a-129">Troubleshooting:</span></span> 

<span data-ttu-id="d055a-130">以下是相關的錯誤和建議的修正。</span><span class="sxs-lookup"><span data-stu-id="d055a-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="d055a-131">請參閱[WSL 疑難排解頁面](troubleshooting.md)其他常見的錯誤和他們的解決方案。</span><span class="sxs-lookup"><span data-stu-id="d055a-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* **<span data-ttu-id="d055a-132">安裝失敗，錯誤 0x80070003</span><span class="sxs-lookup"><span data-stu-id="d055a-132">Installation failed with error 0x80070003</span></span>**
    * <span data-ttu-id="d055a-133">適用於 Linux 的 Windows 子系統只在您的系統磁碟機上執行 (這通常是您`C:`磁碟機)。</span><span class="sxs-lookup"><span data-stu-id="d055a-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="d055a-134">請確定發行版本會儲存您的系統磁碟機上：</span><span class="sxs-lookup"><span data-stu-id="d055a-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="d055a-135">開啟**設定** -> **儲存體** -> **更多的儲存體設定：新的內容儲存的變更**
    ![系統設定的 c： 磁碟機上安裝應用程式中的圖片](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="d055a-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
