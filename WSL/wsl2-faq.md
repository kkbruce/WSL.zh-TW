---
title: WSL 2 常見問題集
description: 常見問題集 Windows 子系統適用於 Linux 2
keywords: 安裝 BashOnWindows、 bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038088"
---
# <a name="wsl-2-faq"></a><span data-ttu-id="5af14-104">WSL 2 常見問題集</span><span class="sxs-lookup"><span data-stu-id="5af14-104">WSL 2 FAQ</span></span>

<span data-ttu-id="5af14-105">以下是一份常見問題 (集 FAQ) 的 Windows 子系統 Linux 2。</span><span class="sxs-lookup"><span data-stu-id="5af14-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="5af14-106">WSL 2 不會使用 HYPER-V 嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="5af14-107">它可在 Windows 10 家用版嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="5af14-108">WSL 2 會提供所有 sku WSL 目前可使用，包括 Windows 10 家用版的。</span><span class="sxs-lookup"><span data-stu-id="5af14-108">WSL 2 will be available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="5af14-109">最新版的 WSL 會使用 HYPER-V 架構，讓其虛擬化。</span><span class="sxs-lookup"><span data-stu-id="5af14-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="5af14-110">此架構可在為 HYPER-V 功能的子集的選用元件。</span><span class="sxs-lookup"><span data-stu-id="5af14-110">This architecture will be available in an optional component that is a subset of the Hyper-V feature.</span></span> <span data-ttu-id="5af14-111">此選用的元件會從所有 Sku 中取得。</span><span class="sxs-lookup"><span data-stu-id="5af14-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="5af14-112">您可以預期看到有關這項體驗的詳細資料很快就是隨著我們越來越接近 WSL 2 版本的時候。</span><span class="sxs-lookup"><span data-stu-id="5af14-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="5af14-113">WSL 1 會發生什麼情況？</span><span class="sxs-lookup"><span data-stu-id="5af14-113">What will happen to WSL 1?</span></span> <span data-ttu-id="5af14-114">則它會放棄嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-114">Will it be abandoned?</span></span>

<span data-ttu-id="5af14-115">我們目前沒有任何計劃，以取代 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="5af14-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="5af14-116">您可以執行 WSL 1 及 WSL 2 發佈並排顯示，並可以升級與降級任何散發版本在任何時間。</span><span class="sxs-lookup"><span data-stu-id="5af14-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="5af14-117">將 WSL 2 新增為新的架構提供更佳的平台，供 WSL 小組提供的功能，讓 WSL 令人讚嘆的方式，在 Windows 中執行的 Linux 環境。</span><span class="sxs-lookup"><span data-stu-id="5af14-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="5af14-118">我可以執行 WSL 2 和 VMware 或 VirtualBox 之類的其他第 3 方虛擬化工具嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="5af14-119">在使用中，這表示它們不能啟用 WSL 2 時執行 HYPER-V 時，某些第 3 個合作對象應用程式無法運作。</span><span class="sxs-lookup"><span data-stu-id="5af14-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled.</span></span> <span data-ttu-id="5af14-120">不幸的是，這包含 VMware 和 VirtualBox VirtualBox 6 之前的版本 (VirtualBox 於 2018 年 12 月發行的 6.0.0[現在支援作為後援執行核心的 Windows 主機上的 HYPER-V] [ 1]!)</span><span class="sxs-lookup"><span data-stu-id="5af14-120">Unfortunately, this does include VMware, and versions of VirtualBox before VirtualBox 6 (VirtualBox 6.0.0 released in December 2018 [now supports Hyper-V as a fallback execution core on a Windows host][1]!)</span></span>

<span data-ttu-id="5af14-121">我們正在調查如何協助您解決此問題。</span><span class="sxs-lookup"><span data-stu-id="5af14-121">We are investigating ways to help resolve this issue.</span></span> <span data-ttu-id="5af14-122">比方說，我們會公開一組 Api 呼叫[Hypervisor 平台][ 2]協力廠商虛擬化提供者可以使用，讓他們的軟體與 HYPER-V 相容</span><span class="sxs-lookup"><span data-stu-id="5af14-122">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s.</span></span> <span data-ttu-id="5af14-123">這可讓應用程式針對其模擬使用 HYPER-V 的架構，例如[Google Android 模擬器][3]，和 VirtualBox 6 和更新版本的都是現在與 HYPER-V 相容。</span><span class="sxs-lookup"><span data-stu-id="5af14-123">This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="5af14-124">我是否可以存取在 WSL 2 GPU？</span><span class="sxs-lookup"><span data-stu-id="5af14-124">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="5af14-125">有計劃，以增加硬體支援嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-125">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="5af14-126">在 WSL 2 硬體存取權的初始版本中支援會受到限制，例如： 您將無法存取 GPU，序列或 Usb。</span><span class="sxs-lookup"><span data-stu-id="5af14-126">In initial releases of WSL 2 hardware access support will be limited, e.g: you will be unable to access the GPU, serial or USBs .</span></span> <span data-ttu-id="5af14-127">不過，新增更好的裝置支援是在我們的待處理項目，這會開啟許多詳細的使用案例適用於開發人員想要與這些裝置進行互動。</span><span class="sxs-lookup"><span data-stu-id="5af14-127">However, adding better device support is high on our backlog, as this opens many more use cases for developers that wish to interact with these devices.</span></span> <span data-ttu-id="5af14-128">在此同時，您可以一律使用 WSL 1 有序列連接埠及 USB 存取。</span><span class="sxs-lookup"><span data-stu-id="5af14-128">In the meantime, you can always use WSL 1 which has serial port and USB access.</span></span> <span data-ttu-id="5af14-129">請持續關注此部落格和 WSL 小組成員到 Twitter 以掌握最新的功能即將 insider 組建，並連線到您想要與互動哪些裝置上提供意見反應 ！</span><span class="sxs-lookup"><span data-stu-id="5af14-129">Please stay tuned to this blog and WSL team members on Twitter to stay informed about the latest features coming to insider builds and reach out to give us feedback on what devices you’d like to interact with!</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="5af14-130">將 WSL 2 可以使用網路的應用程式嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-130">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="5af14-131">是，應用程式的一般網路將會比較快，更好用，因為我們有完整的系統呼叫相容性。</span><span class="sxs-lookup"><span data-stu-id="5af14-131">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="5af14-132">不過，新的架構會使用虛擬化的網路元件。</span><span class="sxs-lookup"><span data-stu-id="5af14-132">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="5af14-133">這表示在初始的預覽組建 WSL 2 會更具有類似的行為至虛擬機器，例如：WSL 2 會有不同的 IP 位址與主機電腦。</span><span class="sxs-lookup"><span data-stu-id="5af14-133">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="5af14-134">我們致力於讓 WSL 2 也有同感 WSL 1，且包含改進我們的網路功能案例。</span><span class="sxs-lookup"><span data-stu-id="5af14-134">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> <span data-ttu-id="5af14-135">我們預計儘快我們就能夠，例如從 Linux 或 Windows 使用 localhost 存取網路的所有應用程式新增增強功能。</span><span class="sxs-lookup"><span data-stu-id="5af14-135">We expect to add improvements as quickly as we are able to, such as accessing all networking apps from Linux or Windows using localhost.</span></span> <span data-ttu-id="5af14-136">我們將會張貼有關我們網路劇本和增強功能的詳細資料時接近 WSL 2 的版本。</span><span class="sxs-lookup"><span data-stu-id="5af14-136">We will be posting more details about our networking story and improvements as we approach the release of WSL 2.</span></span>

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="5af14-137">可以在虛擬機器中執行 WSL 2 嗎？</span><span class="sxs-lookup"><span data-stu-id="5af14-137">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="5af14-138">Yes ！</span><span class="sxs-lookup"><span data-stu-id="5af14-138">Yes!</span></span> <span data-ttu-id="5af14-139">您必須確定虛擬機器有巢狀虛擬化已啟用。</span><span class="sxs-lookup"><span data-stu-id="5af14-139">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="5af14-140">這可啟用在 HYPER-V 中的系統管理員權限的 PowerShell 視窗中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="5af14-140">This can be enabled in Hyper-V by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="5af14-141">請務必取代 '&lt;VMName&gt;' 與虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af14-141">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/