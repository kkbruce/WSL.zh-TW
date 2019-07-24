---
title: 安裝 WSL 2
description: WSL 2 的安裝指示
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246872"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="8a7b9-104">WSL 2 的安裝指示</span><span class="sxs-lookup"><span data-stu-id="8a7b9-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="8a7b9-105">若要安裝並開始使用 WSL 2，請完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="8a7b9-106">啟用「虛擬機器平臺」選用元件</span><span class="sxs-lookup"><span data-stu-id="8a7b9-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="8a7b9-107">使用命令列設定 WSL 2 支援的分散式版</span><span class="sxs-lookup"><span data-stu-id="8a7b9-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="8a7b9-108">驗證分散式版本使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="8a7b9-108">Verify what versions of WSL your distros are using</span></span>

<span data-ttu-id="8a7b9-109">請注意，您必須執行 Windows 10 組建 18917 或更新版本才能使用 WSL 2，而且必須已安裝 WSL (您可以在[這裡](./install-win10.md)找到相關指示)。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-109">Please note that you'll need to be running Windows 10 build 18917 or higher to use WSL 2, and that you will need to have WSL already installed (you can find instructions to do so [here](./install-win10.md)).</span></span> 

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="8a7b9-110">啟用「虛擬機器平臺」選用元件</span><span class="sxs-lookup"><span data-stu-id="8a7b9-110">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="8a7b9-111">以系統管理員身分開啟 PowerShell 並執行：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-111">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="8a7b9-112">啟用這些變更之後，電腦需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-112">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="8a7b9-113">使用命令列設定 WSL 2 支援的分散式版</span><span class="sxs-lookup"><span data-stu-id="8a7b9-113">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="8a7b9-114">在 PowerShell 中執行：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-114">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="8a7b9-115">而且，請務必將 `<Distro>` 取代為分散式版本實際名稱。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-115">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="8a7b9-116">(您可以使用命令 `wsl -l` 來找到這些內容)。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-116">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="8a7b9-117">您可以執行與上述相同的命令，隨時變更回 WSL 1，但將「2」取代為「1」。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-117">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="8a7b9-118">此外，如果您要讓 WSL 2 成為您的預設架構，則可以使用以下命令來執行此動作：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-118">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="8a7b9-119">這會讓您安裝的任何全新分散式版本都初始化為 WSL 2 分散式版本。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-119">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="8a7b9-120">完成驗證分散式版本所使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="8a7b9-120">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="8a7b9-121">若要確認每個分散式版本使用哪個版本的 WSL，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-121">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="8a7b9-122">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="8a7b9-122">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="8a7b9-123">您於上述所選擇的分散式版本現在應該在 [版本] 欄位下顯示「2」。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-123">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="8a7b9-124">現在您已完成作業，可以隨時開始使用 WSL 2 分散式版本！</span><span class="sxs-lookup"><span data-stu-id="8a7b9-124">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="8a7b9-125">疑難排解：</span><span class="sxs-lookup"><span data-stu-id="8a7b9-125">Troubleshooting:</span></span> 

<span data-ttu-id="8a7b9-126">以下是安裝 WSL 2 時的相關錯誤和建議修正。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-126">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="8a7b9-127">有關其他一般 WSL 錯誤和其解決方案的 [WSL 疑難排解頁面](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-127">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="8a7b9-128">**安裝失敗，發生錯誤 0x80070003 或錯誤0x80370102**</span><span class="sxs-lookup"><span data-stu-id="8a7b9-128">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="8a7b9-129">請確定已在電腦的 BIOS 內啟用虛擬化。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-129">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="8a7b9-130">有關如何執行此操作的指示會因電腦而異，並且很可能與 CPU 相關。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-130">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="8a7b9-131">**嘗試升級時發生錯誤`Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="8a7b9-131">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="8a7b9-132">請確定已啟用適用於 Linux 的 Windows 子系統，且使用的是 Windows 組建 18917 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-132">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="8a7b9-133">若要啟用 WSL，請在具有系統管理員權限的 Powershell 提示中執行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-133">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="8a7b9-134">您可以在[這裡](./install-win10.md)尋找完整的 WSL 安裝指示。</span><span class="sxs-lookup"><span data-stu-id="8a7b9-134">You can find the full WSL install instructions [here](./install-win10.md).</span></span>