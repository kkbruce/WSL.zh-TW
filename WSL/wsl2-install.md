---
title: 安裝 WSL 2
description: WSL 2 的安裝指示
keywords: 安裝 BashOnWindows、 bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038078"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="56eca-104">WSL 2 的安裝指示</span><span class="sxs-lookup"><span data-stu-id="56eca-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="56eca-105">安裝和開始使用 WSL 2 會完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="56eca-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="56eca-106">啟用 '虛擬機器平台' 選用元件</span><span class="sxs-lookup"><span data-stu-id="56eca-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="56eca-107">設定受到 WSL 2 使用命令列的散發套件</span><span class="sxs-lookup"><span data-stu-id="56eca-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="56eca-108">確認要使用的 WSL 您的散發套件的版本</span><span class="sxs-lookup"><span data-stu-id="56eca-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="56eca-109">啟用 '虛擬機器平台' 選用元件</span><span class="sxs-lookup"><span data-stu-id="56eca-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="56eca-110">系統管理員身分開啟 PowerShell 並執行：</span><span class="sxs-lookup"><span data-stu-id="56eca-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="56eca-111">啟用這些變更之後，您必須重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="56eca-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="56eca-112">設定受到 WSL 2 使用命令列的散發套件</span><span class="sxs-lookup"><span data-stu-id="56eca-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="56eca-113">在 PowerShell 中執行：</span><span class="sxs-lookup"><span data-stu-id="56eca-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="56eca-114">並請務必取代`<Distro>`與您的散發套件的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="56eca-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="56eca-115">(您可以找到這些命令： `wsl -l`)。</span><span class="sxs-lookup"><span data-stu-id="56eca-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="56eca-116">您可以變更回 WSL 1 隨時執行與上述的相同命令，但取代 '2' 與' 1'。</span><span class="sxs-lookup"><span data-stu-id="56eca-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="56eca-117">此外，如果您想要讓 WSL 2 預設架構則可以使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="56eca-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="56eca-118">這會讓任何新安裝的散發套件會初始化為 WSL 2 發行版本。</span><span class="sxs-lookup"><span data-stu-id="56eca-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="56eca-119">完成，並確認 WSL 您的散發套件的版本會使用</span><span class="sxs-lookup"><span data-stu-id="56eca-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="56eca-120">若要確認哪些版本的 WSL 使用每個散發套件會使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="56eca-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="56eca-121">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="56eca-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="56eca-122">您已選擇上述的散發版本現在應該會顯示 '2' 的 'version' 資料行底下。</span><span class="sxs-lookup"><span data-stu-id="56eca-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="56eca-123">現在，您已完成放心地開始使用您的 WSL 2 發行版本 ！</span><span class="sxs-lookup"><span data-stu-id="56eca-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 