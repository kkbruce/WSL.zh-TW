---
title: WSL 2 常見問題
description: 關於適用於 Linux 的 Windows 子系統 2 的常見問題集
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 760ca61f77f12509224458f1b44a1329d7225600
ms.sourcegitcommit: 00e4d12bfcd0dcd53c7445ddb2f8f0d0739d20af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/09/2019
ms.locfileid: "68915553"
---
# <a name="wsl-2-faq"></a>WSL 2 常見問題

以下是適用於 WSL 2的常見問題集 (FAQ) 清單。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 是否使用 Hyper-v？ 是否可在 Windows 10 家用版上使用？

WSL 2 將在 WSL 目前可用的所有 Sku 上提供, 包括 Windows 10 家用版。

最新版本的 WSL 會使用 Hyper-v 架構來啟用其虛擬化。 此架構將在「虛擬機器平臺」選用元件中提供。 此選用元件將會在所有 Sku 上提供。 當我們更接近 WSL 2 版本時, 您可以預期很快就會看到更多關於此體驗的詳細資料。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 會發生什麼事？ 它會被放棄嗎？


我們目前沒有計劃取代 WSL 1。您可以並存執行 WSL 1 和 WSL 2 發行版本，並且可以隨時升級及降級任何發行版本。將 WSL 2 新增為新的架構可為 WSL 小組提供更好的平台M，讓他們能夠提供功能，使 WSL 成為在 Windows 中執行 Linux 環境的絕佳方式。


## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>我是否能夠執行 WSL 2 和其他協力廠商虛擬化工具, 例如 VMware 或 VirtualBox？

當 Hyper-v 在使用中時, 有些協力廠商應用程式無法運作, 這表示在啟用 WSL 2 時將無法執行。 可惜的是, 這包括 VMware 和 VirtualBox 6 之前的 VirtualBox 版本 (2018 年12月發行的 VirtualBox 6.0.0[現在支援 hyper-v 做為 Windows 主機上的 fallback 執行核心][1]!)

我們正在調查可協助解決此問題的方法。例如，我們公開一組稱為 [Hypervisor 平台][2]的 API，第三方虛擬化提供者可以使用它們來使其軟體與 Hyper-V 相容。這可讓應用程式使用 Hyper-V 架構來進行模擬，例如 [Google Android Emulator][3] 以及 VirtualBox 6 與更新版本 (這兩者現在都與 Hyper-V 相容)。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>我可以在 WSL 2 中存取 GPU 嗎？ 是否有計劃增加硬體支援？

在 WSL 2 的初始版本中，硬體存取支援將會受到限制，例如：您將無法存取 GPU、序列埠或 USB。不過，在我們的待處理專案中，新增更好的裝置支援有很高的優先順序，因為這會為想要與這些裝置互動的開發人員開啟更多使用案例。同時，您一律可以使用具有序列埠和 USB 存取的 WSL 1。請隨時留意此部落格，並關注 Twitter 上的 WSL 小組成員，隨時掌握有關即將推出之測試人員組建並搶先試用，並提供有關您要與哪種裝置互動的意見反應。

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 是否能夠使用網路應用程式？

是, 在一般的網路應用程式中, 因為我們具有完整的系統呼叫相容性, 所以可以更快速且更有效率。 不過, 新的架構會使用虛擬化的網路元件。 這表示在初始預覽組建中, WSL 2 的行為會比虛擬機器更相似, 例如:WSL 2 將會有不同于主機電腦的 IP 位址。 我們致力於讓 WSL 2 的風格與 WSL 1 相同, 並包含改善我們的網路功能案例。 我們希望能儘快新增改良功能, 例如使用 localhost 從 Linux 或 Windows 存取所有網路應用程式。 我們將在我們處理 WSL 2 的版本時, 公佈更多關於網路案例和改進的詳細資料。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>我可以在虛擬機器中執行 WSL 2 嗎？


是！您必須確定虛擬機器已啟用「巢狀虛擬化」。這可以在父 Hyper-V 主機中啟用，方式是使用系統管理員權限在 PowerShell 視窗中執行下列命令：


`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

請務必以您的虛擬機器名稱取代 &lt;VMName&gt;。

## <a name="can-i-use-wslconf-in-wsl-2"></a>我可以在 WSL 2 中使用 wsl 嗎？


WSL 2 支援 WSL 1 所使用的相同 WSL 檔案。這表示您在 WSL 1 發行版本中設定的任何設定選項 (例如，自動掛接 Windows 磁碟機、啟用或停用 Interop、變更 Windows 磁碟機將掛接的目錄等) 全部都能在 WSL 2 中運作。您可以在[發行版本管理](./wsl-config.md)頁面中深入了解 WSL 中的設定選項。	


 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
