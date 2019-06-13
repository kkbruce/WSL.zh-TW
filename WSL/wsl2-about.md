---
title: 關於 WSL 2
description: 關於 WSL 2 的新架構，適用於 Linux 的 Windows 子系統
keywords: 安裝 BashOnWindows、 bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038128"
---
WSL 2 是支援的 Windows 子系統，適用於執行 ELF64 Linux 二進位檔在 Windows 上的 Linux 架構的新版本。 其主要的目標是要增加檔案系統的效能，以及新增完整的系統呼叫相容性。 這個新架構變更這些 Linux 二進位檔與 Windows 電腦的硬體互動的方式，但仍會提供相同的使用者體驗，如 WSL 1 （目前廣泛使用的版本） 所示。 個別的 Linux 散發版本可以執行，WSL 1 的散發版本，或是 WSL 2 的散發版本，可以升級或降級任何時候，而且您可以執行 WSL 1 和 WSL 2 的散發版本並存。 WSL 2 使用全新的架構，會使用實際的 Linux 核心。

## <a name="linux-kernel-in-wsl-2"></a>在 WSL 2 中的 Linux 核心

在 WSL 2 中的 Linux 核心已內建家中從最新的穩定分支，根據在 kernel.org 中可用的來源。此核心已特別調整 WSL 2。 它已針對大小和效能，以在 Windows 上提供令人讚嘆的 Linux 體驗最佳化，並將服務透過 Windows 更新，這表示您會取得最新的安全性修正程式和核心改良功能而不需要自行管理。

此外此核心將會開放原始碼。 您可以找到完整的原始碼 Linux kernel[此處](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip)。 如果您想要深入了解您可以看看此核心[此部落格文章](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)內建的小組所撰寫。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 架構的簡要概觀

WSL 2 會使用最新及最佳虛擬化技術執行其輕量級的公用程式的虛擬機器 (VM) 內的 Linux 核心。 不過，WSL 2 不會有傳統 VM 經驗。 傳統 VM 經驗可能會慢啟動、 隔離、 耗用大量資源，和需要您的時間來管理它。 WSL 2 並沒有這些屬性。 它仍然會提供引人注目的 WSL 1 優點：任何 VM 組態或管理需要高層級的 Windows 和 Linux、 極快速的開機時間、 小型資源使用量及最棒的是之間的整合。 雖然 WSL 2 會使用 VM，它會管理並讓您利用相同的使用者體驗為 WSL 1 在幕後執行。

## <a name="increased-file-io-performance"></a>增加的檔案的 IO 效能

檔案的大量作業，例如 git 複製，npm 安裝、 apt 更新、 apt 的升級和更多功能會明顯更快。 實際的速度增加取決於哪一個應用程式上正在執行，且它與檔案系統的互動方式。 初始版本 WSL 2 執行最多 20 個 x 速度比 WSL 1，當解壓縮壓縮的 tarball，以及各種專案使用 git 複製、 npm 安裝和 cmake 時更快 2-5 倍。

## <a name="full-system-call-compatibility"></a>完整的系統呼叫相容性

Linux 的二進位檔會使用系統呼叫來執行許多功能，例如存取檔案、 要求的記憶體、 建立處理序等等。 但是 WSL 1 使用的轉譯層 WSL 小組所建置，WSL 2 會包含它自己的 Linux 核心完整的系統呼叫相容性。 這引進了一組全新的應用程式，您可以執行在 WSL，例如 Docker 和更多功能。 此外，任何 Linux 核心的更新可能立即新增到您的電腦，而不是等待 WSL 小組来實作變更，然後再加以新增。