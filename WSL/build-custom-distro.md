---
title: 建置自訂的 Linux Distro WSL
description: 了解如何建立自訂的 Linux 散發套件的 Windows 子系統，適用於 Linux。
keywords: BashOnWindows，bash，wsl、 windows、 windows 子系統、 散發版本，自訂
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040781"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="9a1fa-104">建立自訂的 Linux Distro WSL</span><span class="sxs-lookup"><span data-stu-id="9a1fa-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="9a1fa-105">為 Microsoft Store 建置 WSL 散發套件，及/或建立自訂的側載功能的 Linux 散發套件，請使用我們的開放原始碼 WSL 範例。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="9a1fa-106">您可以找到[distro 啟動器存放庫](https://github.com/Microsoft/WSL-DistroLauncher)GitHub 上。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="9a1fa-107">此專案可讓：</span><span class="sxs-lookup"><span data-stu-id="9a1fa-107">This project enables:</span></span>
* <span data-ttu-id="9a1fa-108">若要封裝並送出為 appx 在 WSL 上執行的 Linux 散發套件的 Linux 發行版本維護者</span><span class="sxs-lookup"><span data-stu-id="9a1fa-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="9a1fa-109">開發人員建立自訂的 Linux 散發套件可以側載至其開發電腦</span><span class="sxs-lookup"><span data-stu-id="9a1fa-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="9a1fa-110">背景</span><span class="sxs-lookup"><span data-stu-id="9a1fa-110">Background</span></span>
<span data-ttu-id="9a1fa-111">我們將散發的 Linux 散發版本 WSL 為 UWP 應用程式可以透過 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="9a1fa-112">您可以安裝在 WSL-在 Windows 核心中的子系統便會執行這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="9a1fa-113">這個傳遞機制中所述，有許多優點[較早的部落格文章](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="9a1fa-114">側載自訂的 Linux 散發套件</span><span class="sxs-lookup"><span data-stu-id="9a1fa-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="9a1fa-115">在您的個人電腦上，您可以為要側載應用程式建立自訂的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="9a1fa-116">請注意，自訂套件將無法散發透過 Microsoft Store 除非您為發佈維護程式送出。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="9a1fa-117">若要設定您的電腦，側載應用程式，您必須在 「 適用於開發人員 」 下的系統設定中啟用。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="9a1fa-118">請務必要有開發人員模式或選取的側載應用程式</span><span class="sxs-lookup"><span data-stu-id="9a1fa-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="9a1fa-119">針對 Linux 散發套件維護人員</span><span class="sxs-lookup"><span data-stu-id="9a1fa-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="9a1fa-120">若要提交至市集，您必須與我們配合以接收發行的核准。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="9a1fa-121">如果您想要將您的散發套件新增至 Microsoft Store 的 Linux 發佈擁有者，請連絡wslpartners@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="9a1fa-122">開始使用</span><span class="sxs-lookup"><span data-stu-id="9a1fa-122">Getting Started</span></span>
<span data-ttu-id="9a1fa-123">遵循上的指示[Distro 啟動器 GitHub 存放庫](https://github.com/Microsoft/WSL-DistroLauncher)來建立自訂的 Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="9a1fa-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="9a1fa-124">小組部落格</span><span class="sxs-lookup"><span data-stu-id="9a1fa-124">Team Blogs</span></span>
*  [<span data-ttu-id="9a1fa-125">開啟來源 WSL 範例 Linux 發行版本維護者和側載自訂的 Linux 散發套件</span><span class="sxs-lookup"><span data-stu-id="9a1fa-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="9a1fa-126">命令列的部落格</span><span class="sxs-lookup"><span data-stu-id="9a1fa-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="9a1fa-127">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="9a1fa-127">Provide Feedback</span></span>
* [<span data-ttu-id="9a1fa-128">Distro 啟動器 GitHub 存放庫</span><span class="sxs-lookup"><span data-stu-id="9a1fa-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="9a1fa-129">WSL 的 GitHub 問題追蹤器</span><span class="sxs-lookup"><span data-stu-id="9a1fa-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="9a1fa-130">命令列的 UserVoice 入口網站</span><span class="sxs-lookup"><span data-stu-id="9a1fa-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
