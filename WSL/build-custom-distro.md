---
title: 建立適用于 WSL 的自訂 Linux 散發版本
description: 瞭解如何為適用于 Linux 的 Windows 子系統建立自訂 Linux 散發套件。
keywords: BashOnWindows、bash、wsl、windows、windows 子系統、散發版本、custom
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040781"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="42e2b-104">建立適用于 WSL 的自訂 Linux 散發版本</span><span class="sxs-lookup"><span data-stu-id="42e2b-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="42e2b-105">使用我們的開放原始碼 WSL 範例來建立適用于 Microsoft Store 和/或的 WSL 散發版本套件, 以建立用於側載的自訂 Linux 散發版本套件。</span><span class="sxs-lookup"><span data-stu-id="42e2b-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="42e2b-106">您可以在 GitHub 上找到[散發版本啟動器](https://github.com/Microsoft/WSL-DistroLauncher)存放庫。</span><span class="sxs-lookup"><span data-stu-id="42e2b-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="42e2b-107">此專案會啟用:</span><span class="sxs-lookup"><span data-stu-id="42e2b-107">This project enables:</span></span>
* <span data-ttu-id="42e2b-108">Linux 散發套件維護人員, 可封裝並提交 Linux 發行版本, 做為在 WSL 上執行的 appx</span><span class="sxs-lookup"><span data-stu-id="42e2b-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="42e2b-109">開發人員建立可側載至其開發電腦的自訂 Linux 發行版本</span><span class="sxs-lookup"><span data-stu-id="42e2b-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="42e2b-110">背景</span><span class="sxs-lookup"><span data-stu-id="42e2b-110">Background</span></span>
<span data-ttu-id="42e2b-111">我們會透過 Microsoft Store, 將 WSL 的 Linux 散發版本作為 UWP 應用程式散發。</span><span class="sxs-lookup"><span data-stu-id="42e2b-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="42e2b-112">您可以安裝將在 WSL 上執行的應用程式, 也就是位於 Windows 核心的子系統。</span><span class="sxs-lookup"><span data-stu-id="42e2b-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="42e2b-113">這項傳遞機制有許多優點, 如[先前的 blog 文章](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)中所述。</span><span class="sxs-lookup"><span data-stu-id="42e2b-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="42e2b-114">側載自訂 Linux 散發版本套件</span><span class="sxs-lookup"><span data-stu-id="42e2b-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="42e2b-115">您可以建立自訂的 Linux 散發版本套件作為應用程式, 以在您的個人電腦上側載。</span><span class="sxs-lookup"><span data-stu-id="42e2b-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="42e2b-116">請注意, 除非您以散發維護程式形式提交, 否則您的自訂套件不會透過 Microsoft Store 散發。</span><span class="sxs-lookup"><span data-stu-id="42e2b-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="42e2b-117">若要設定您的電腦以側載應用程式, 您必須在 [適用于開發人員] 底下的 [系統設定] 中啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="42e2b-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="42e2b-118">請確定已選取 [開發人員模式] 或 [側載應用程式]</span><span class="sxs-lookup"><span data-stu-id="42e2b-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="42e2b-119">針對 Linux 散發版本維護人員</span><span class="sxs-lookup"><span data-stu-id="42e2b-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="42e2b-120">若要提交到商店, 您必須與我們合作以接收發行核准。</span><span class="sxs-lookup"><span data-stu-id="42e2b-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="42e2b-121">如果您是想要將散發新增至 Microsoft Store 的 Linux 散發擁有者, 請洽詢wslpartners@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="42e2b-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="42e2b-122">開始使用</span><span class="sxs-lookup"><span data-stu-id="42e2b-122">Getting Started</span></span>
<span data-ttu-id="42e2b-123">依照[散發版本啟動器 GitHub](https://github.com/Microsoft/WSL-DistroLauncher)存放庫中的指示, 建立自訂的 Linux 散發版本套件。</span><span class="sxs-lookup"><span data-stu-id="42e2b-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="42e2b-124">小組 Blog</span><span class="sxs-lookup"><span data-stu-id="42e2b-124">Team Blogs</span></span>
*  [<span data-ttu-id="42e2b-125">開放採購 Linux 散發維護人員和側載自訂 Linux 發行版本的 WSL 範例</span><span class="sxs-lookup"><span data-stu-id="42e2b-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="42e2b-126">命令列的 blog</span><span class="sxs-lookup"><span data-stu-id="42e2b-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="42e2b-127">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="42e2b-127">Provide Feedback</span></span>
* [<span data-ttu-id="42e2b-128">散發版本啟動器 GitHub 存放庫</span><span class="sxs-lookup"><span data-stu-id="42e2b-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="42e2b-129">適用于 WSL 的 GitHub 問題追蹤器</span><span class="sxs-lookup"><span data-stu-id="42e2b-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="42e2b-130">命令列 UserVoice 入口網站</span><span class="sxs-lookup"><span data-stu-id="42e2b-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
