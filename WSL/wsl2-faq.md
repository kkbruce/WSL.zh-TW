---
title: WSL 2 常見問題
description: 關於適用于 Linux 的 Windows 子系統的常見問題2
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a74f5e3f5879d0af274d2e2b10aaf05e95a97a6f
ms.sourcegitcommit: e16097a3d863bbda8c4655054f154415cdd7f2f5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/05/2019
ms.locfileid: "67587146"
---
# <a name="wsl-2-faq"></a><span data-ttu-id="35b4f-104">WSL 2 常見問題</span><span class="sxs-lookup"><span data-stu-id="35b4f-104">WSL 2 FAQ</span></span>

<span data-ttu-id="35b4f-105">以下是適用于 Linux 2 之 Windows 子系統的常見問題 (FAQ) 清單。</span><span class="sxs-lookup"><span data-stu-id="35b4f-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="35b4f-106">WSL 2 是否使用 Hyper-v？</span><span class="sxs-lookup"><span data-stu-id="35b4f-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="35b4f-107">是否可在 Windows 10 家用版上使用？</span><span class="sxs-lookup"><span data-stu-id="35b4f-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="35b4f-108">WSL 2 將在 WSL 目前可用的所有 Sku 上提供, 包括 Windows 10 家用版。</span><span class="sxs-lookup"><span data-stu-id="35b4f-108">WSL 2 will be available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="35b4f-109">最新版本的 WSL 會使用 Hyper-v 架構來啟用其虛擬化。</span><span class="sxs-lookup"><span data-stu-id="35b4f-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="35b4f-110">此架構將在「虛擬機器平臺」選用元件中提供。</span><span class="sxs-lookup"><span data-stu-id="35b4f-110">This architecture will be available in the 'Virtual Machine Platform' optional component.</span></span> <span data-ttu-id="35b4f-111">此選用元件將會在所有 Sku 上提供。</span><span class="sxs-lookup"><span data-stu-id="35b4f-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="35b4f-112">當我們更接近 WSL 2 版本時, 您可以預期很快就會看到更多關於此體驗的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="35b4f-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="35b4f-113">WSL 1 會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="35b4f-113">What will happen to WSL 1?</span></span> <span data-ttu-id="35b4f-114">它會被放棄嗎？</span><span class="sxs-lookup"><span data-stu-id="35b4f-114">Will it be abandoned?</span></span>

<span data-ttu-id="35b4f-115">我們目前沒有計劃取代 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="35b4f-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="35b4f-116">您可以並存執行 WSL 1 和 WSL 2 散發版本, 並且可以隨時升級及降級任何散發版本。</span><span class="sxs-lookup"><span data-stu-id="35b4f-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="35b4f-117">將 WSL 2 新增為新的架構, 可提供更好的平臺, 讓 WSL 小組能夠提供功能, 使 WSL 成為在 Windows 中執行 Linux 環境的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="35b4f-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="35b4f-118">我是否能夠執行 WSL 2 和其他協力廠商虛擬化工具, 例如 VMware 或 VirtualBox？</span><span class="sxs-lookup"><span data-stu-id="35b4f-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="35b4f-119">當 Hyper-v 在使用中時, 有些協力廠商應用程式無法運作, 這表示在啟用 WSL 2 時將無法執行。</span><span class="sxs-lookup"><span data-stu-id="35b4f-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled.</span></span> <span data-ttu-id="35b4f-120">可惜的是, 這包括 VMware 和 VirtualBox 6 之前的 VirtualBox 版本 (2018 年12月發行的 VirtualBox 6.0.0[現在支援 hyper-v 做為 Windows 主機上的 fallback 執行核心][1]!)</span><span class="sxs-lookup"><span data-stu-id="35b4f-120">Unfortunately, this does include VMware, and versions of VirtualBox before VirtualBox 6 (VirtualBox 6.0.0 released in December 2018 [now supports Hyper-V as a fallback execution core on a Windows host][1]!)</span></span>

<span data-ttu-id="35b4f-121">我們正在調查協助解決此問題的方法。</span><span class="sxs-lookup"><span data-stu-id="35b4f-121">We are investigating ways to help resolve this issue.</span></span> <span data-ttu-id="35b4f-122">例如, 我們公開一組稱為「[虛擬機器平臺][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s. This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3]」的 api, 以及 VirtualBox 6 和更新版本, 兩者現在都與 hyper-v 相容。</span><span class="sxs-lookup"><span data-stu-id="35b4f-122">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s. This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="35b4f-123">我可以在 WSL 2 中存取 GPU 嗎？</span><span class="sxs-lookup"><span data-stu-id="35b4f-123">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="35b4f-124">是否有計劃增加硬體支援？</span><span class="sxs-lookup"><span data-stu-id="35b4f-124">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="35b4f-125">在 WSL 2 的初始版本中, 硬體存取支援將會受到限制, 例如: 您將無法存取 GPU、序列或 USBs。</span><span class="sxs-lookup"><span data-stu-id="35b4f-125">In initial releases of WSL 2 hardware access support will be limited, e.g: you will be unable to access the GPU, serial or USBs .</span></span> <span data-ttu-id="35b4f-126">不過, 在我們的待處理專案中新增更好的裝置支援會很高, 因為這會為想要與這些裝置互動的開發人員開啟更多使用案例。</span><span class="sxs-lookup"><span data-stu-id="35b4f-126">However, adding better device support is high on our backlog, as this opens many more use cases for developers that wish to interact with these devices.</span></span> <span data-ttu-id="35b4f-127">在此同時, 您可以一律使用具有序列埠和 USB 存取的 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="35b4f-127">In the meantime, you can always use WSL 1 which has serial port and USB access.</span></span> <span data-ttu-id="35b4f-128">請隨時留意此 blog, 並在 Twitter 上 WSL 小組成員, 隨時掌握有關 insider build 的最新功能, 並提供意見反應, 告訴我們您想要與之互動的裝置。</span><span class="sxs-lookup"><span data-stu-id="35b4f-128">Please stay tuned to this blog and WSL team members on Twitter to stay informed about the latest features coming to insider builds and reach out to give us feedback on what devices you’d like to interact with!</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="35b4f-129">WSL 2 是否能夠使用網路應用程式？</span><span class="sxs-lookup"><span data-stu-id="35b4f-129">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="35b4f-130">是, 在一般的網路應用程式中, 因為我們具有完整的系統呼叫相容性, 所以可以更快速且更有效率。</span><span class="sxs-lookup"><span data-stu-id="35b4f-130">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="35b4f-131">不過, 新的架構會使用虛擬化的網路元件。</span><span class="sxs-lookup"><span data-stu-id="35b4f-131">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="35b4f-132">這表示在初始預覽組建中, WSL 2 的行為會比虛擬機器更相似, 例如:WSL 2 將會有不同于主機電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="35b4f-132">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="35b4f-133">我們致力於讓 WSL 2 的風格與 WSL 1 相同, 並包含改善我們的網路功能案例。</span><span class="sxs-lookup"><span data-stu-id="35b4f-133">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> <span data-ttu-id="35b4f-134">我們希望能儘快新增改良功能, 例如使用 localhost 從 Linux 或 Windows 存取所有網路應用程式。</span><span class="sxs-lookup"><span data-stu-id="35b4f-134">We expect to add improvements as quickly as we are able to, such as accessing all networking apps from Linux or Windows using localhost.</span></span> <span data-ttu-id="35b4f-135">我們將在我們處理 WSL 2 的版本時, 公佈更多關於網路案例和改進的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="35b4f-135">We will be posting more details about our networking story and improvements as we approach the release of WSL 2.</span></span>

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="35b4f-136">我可以在虛擬機器中執行 WSL 2 嗎？</span><span class="sxs-lookup"><span data-stu-id="35b4f-136">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="35b4f-137">是的！</span><span class="sxs-lookup"><span data-stu-id="35b4f-137">Yes!</span></span> <span data-ttu-id="35b4f-138">您必須確定虛擬機器已啟用「嵌套虛擬化」。</span><span class="sxs-lookup"><span data-stu-id="35b4f-138">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="35b4f-139">這可以在 Hyper-v 中啟用, 方法是在具有系統管理員許可權的 PowerShell 視窗中執行下列命令:</span><span class="sxs-lookup"><span data-stu-id="35b4f-139">This can be enabled in Hyper-V by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="35b4f-140">請務必以您的&lt;虛擬&gt;機名稱取代 ' VMName '。</span><span class="sxs-lookup"><span data-stu-id="35b4f-140">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

## <a name="can-i-use-wslconf-in-wsl-2"></a><span data-ttu-id="35b4f-141">我可以在 WSL 2 中使用 wsl 嗎？</span><span class="sxs-lookup"><span data-stu-id="35b4f-141">Can I use wsl.conf in WSL 2?</span></span>

<span data-ttu-id="35b4f-142">WSL 2 支援 WSL 1 所使用的相同 WSL 檔案。</span><span class="sxs-lookup"><span data-stu-id="35b4f-142">WSL 2 supports the same wsl.conf file that WSL 1 uses.</span></span> <span data-ttu-id="35b4f-143">這表示您在 WSL 1 散發版本 (例如 automounting Windows 磁片磁碟機、啟用或停用 interop、變更 Windows 磁片磁碟機將裝載的目錄等) 中設定的任何設定選項, 都將在 WSL 2 中全部工作。</span><span class="sxs-lookup"><span data-stu-id="35b4f-143">This means that any configuration options that you had set in a WSL 1 distro, such as automounting Windows drives, enabling or disabling interop, changing the directory where Windows drives will be mounted, etc. will all work inside of WSL 2.</span></span> <span data-ttu-id="35b4f-144">您可以在[散發版本管理](./wsl-config.md)頁面中深入瞭解 WSL 中的設定選項。</span><span class="sxs-lookup"><span data-stu-id="35b4f-144">You can learn more about the configuration options in WSL in the [Distro Management](./wsl-config.md) page.</span></span> 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/