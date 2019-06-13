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
# <a name="wsl-2-faq"></a>WSL 2 常見問題集

以下是一份常見問題 (集 FAQ) 的 Windows 子系統 Linux 2。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 不會使用 HYPER-V 嗎？ 它可在 Windows 10 家用版嗎？

WSL 2 會提供所有 sku WSL 目前可使用，包括 Windows 10 家用版的。

最新版的 WSL 會使用 HYPER-V 架構，讓其虛擬化。 此架構可在為 HYPER-V 功能的子集的選用元件。 此選用的元件會從所有 Sku 中取得。 您可以預期看到有關這項體驗的詳細資料很快就是隨著我們越來越接近 WSL 2 版本的時候。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 會發生什麼情況？ 則它會放棄嗎？

我們目前沒有任何計劃，以取代 WSL 1。 您可以執行 WSL 1 及 WSL 2 發佈並排顯示，並可以升級與降級任何散發版本在任何時間。 將 WSL 2 新增為新的架構提供更佳的平台，供 WSL 小組提供的功能，讓 WSL 令人讚嘆的方式，在 Windows 中執行的 Linux 環境。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>我可以執行 WSL 2 和 VMware 或 VirtualBox 之類的其他第 3 方虛擬化工具嗎？

在使用中，這表示它們不能啟用 WSL 2 時執行 HYPER-V 時，某些第 3 個合作對象應用程式無法運作。 不幸的是，這包含 VMware 和 VirtualBox VirtualBox 6 之前的版本 (VirtualBox 於 2018 年 12 月發行的 6.0.0[現在支援作為後援執行核心的 Windows 主機上的 HYPER-V] [ 1]!)

我們正在調查如何協助您解決此問題。 比方說，我們會公開一組 Api 呼叫[Hypervisor 平台][ 2]協力廠商虛擬化提供者可以使用，讓他們的軟體與 HYPER-V 相容 這可讓應用程式針對其模擬使用 HYPER-V 的架構，例如[Google Android 模擬器][3]，和 VirtualBox 6 和更新版本的都是現在與 HYPER-V 相容。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>我是否可以存取在 WSL 2 GPU？ 有計劃，以增加硬體支援嗎？

在 WSL 2 硬體存取權的初始版本中支援會受到限制，例如： 您將無法存取 GPU，序列或 Usb。 不過，新增更好的裝置支援是在我們的待處理項目，這會開啟許多詳細的使用案例適用於開發人員想要與這些裝置進行互動。 在此同時，您可以一律使用 WSL 1 有序列連接埠及 USB 存取。 請持續關注此部落格和 WSL 小組成員到 Twitter 以掌握最新的功能即將 insider 組建，並連線到您想要與互動哪些裝置上提供意見反應 ！

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>將 WSL 2 可以使用網路的應用程式嗎？

是，應用程式的一般網路將會比較快，更好用，因為我們有完整的系統呼叫相容性。 不過，新的架構會使用虛擬化的網路元件。 這表示在初始的預覽組建 WSL 2 會更具有類似的行為至虛擬機器，例如：WSL 2 會有不同的 IP 位址與主機電腦。 我們致力於讓 WSL 2 也有同感 WSL 1，且包含改進我們的網路功能案例。 我們預計儘快我們就能夠，例如從 Linux 或 Windows 使用 localhost 存取網路的所有應用程式新增增強功能。 我們將會張貼有關我們網路劇本和增強功能的詳細資料時接近 WSL 2 的版本。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>可以在虛擬機器中執行 WSL 2 嗎？

Yes ！ 您必須確定虛擬機器有巢狀虛擬化已啟用。 這可啟用在 HYPER-V 中的系統管理員權限的 PowerShell 視窗中執行下列命令：

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

請務必取代 '&lt;VMName&gt;' 與虛擬機器的名稱。

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/