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
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/26/2019
ms.locfileid: "67587146"
---
# <a name="wsl-2-faq"></a>WSL 2 常見問題

以下是適用于 Linux 2 之 Windows 子系統的常見問題 (FAQ) 清單。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 是否使用 Hyper-v？ 是否可在 Windows 10 家用版上使用？

WSL 2 將在 WSL 目前可用的所有 Sku 上提供, 包括 Windows 10 家用版。

最新版本的 WSL 會使用 Hyper-v 架構來啟用其虛擬化。 此架構將在「虛擬機器平臺」選用元件中提供。 此選用元件將會在所有 Sku 上提供。 當我們更接近 WSL 2 版本時, 您可以預期很快就會看到更多關於此體驗的詳細資料。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 會發生什麼事？ 它會被放棄嗎？

我們目前沒有計劃取代 WSL 1。 您可以並存執行 WSL 1 和 WSL 2 散發版本, 並且可以隨時升級及降級任何散發版本。 將 WSL 2 新增為新的架構, 可提供更好的平臺, 讓 WSL 小組能夠提供功能, 使 WSL 成為在 Windows 中執行 Linux 環境的絕佳方式。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>我是否能夠執行 WSL 2 和其他協力廠商虛擬化工具, 例如 VMware 或 VirtualBox？

當 Hyper-v 在使用中時, 有些協力廠商應用程式無法運作, 這表示在啟用 WSL 2 時將無法執行。 可惜的是, 這包括 VMware 和 VirtualBox 6 之前的 VirtualBox 版本 (2018 年12月發行的 VirtualBox 6.0.0[現在支援 hyper-v 做為 Windows 主機上的 fallback 執行核心][1]!)

我們正在調查協助解決此問題的方法。 例如, 我們公開一組稱為「[虛擬機器平臺][2]」的 api, 協力廠商虛擬化提供者可以使用它來使其軟體與 hyper-v 相容。 這可讓應用程式使用 Hyper-v 架構來進行模擬, 例如[Google Android Emulator][3], 而 VirtualBox 6 和更新版本現在兩者都與 hyper-v 相容。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>我可以在 WSL 2 中存取 GPU 嗎？ 是否有計劃增加硬體支援？

在 WSL 2 的初始版本中, 硬體存取支援將會受到限制, 例如: 您將無法存取 GPU、序列或 USBs。 不過, 在我們的待處理專案中新增更好的裝置支援會很高, 因為這會為想要與這些裝置互動的開發人員開啟更多使用案例。 在此同時, 您可以一律使用具有序列埠和 USB 存取的 WSL 1。 請隨時留意此 blog, 並在 Twitter 上 WSL 小組成員, 隨時掌握有關 insider build 的最新功能, 並提供意見反應, 告訴我們您想要與之互動的裝置。

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 是否能夠使用網路應用程式？

是, 在一般的網路應用程式中, 因為我們具有完整的系統呼叫相容性, 所以可以更快速且更有效率。 不過, 新的架構會使用虛擬化的網路元件。 這表示在初始預覽組建中, WSL 2 的行為會比虛擬機器更相似, 例如:WSL 2 將會有不同于主機電腦的 IP 位址。 我們致力於讓 WSL 2 的風格與 WSL 1 相同, 並包含改善我們的網路功能案例。 我們希望能儘快新增改良功能, 例如使用 localhost 從 Linux 或 Windows 存取所有網路應用程式。 我們將在我們處理 WSL 2 的版本時, 公佈更多關於網路案例和改進的詳細資料。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>我可以在虛擬機器中執行 WSL 2 嗎？

是的！ 您必須確定虛擬機器已啟用「嵌套虛擬化」。 這可以在 Hyper-v 中啟用, 方法是在具有系統管理員許可權的 PowerShell 視窗中執行下列命令:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

請務必以您的&lt;虛擬&gt;機名稱取代 ' VMName '。

## <a name="can-i-use-wslconf-in-wsl-2"></a>我可以在 WSL 2 中使用 wsl 嗎？

WSL 2 支援 WSL 1 所使用的相同 WSL 檔案。 這表示您在 WSL 1 散發版本 (例如 automounting Windows 磁片磁碟機、啟用或停用 interop、變更 Windows 磁片磁碟機將裝載的目錄等) 中設定的任何設定選項, 都將在 WSL 2 中全部工作。 您可以在[散發版本管理](./wsl-config.md)頁面中深入瞭解 WSL 中的設定選項。 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/