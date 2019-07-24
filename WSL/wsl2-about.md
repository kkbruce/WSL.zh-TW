---
title: 關於 WSL 2
description: 關於 WSL 2 適用于 Linux 的 Windows 子系統的新架構
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: e9c1f043207193a5c00ecf6176f54f240aa48680
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499258"
---
# <a name="about-wsl-2"></a>關於 WSL 2

WSL 2 是新版本的架構, 可讓適用于 Linux 的 Windows 子系統在 Windows 上執行 ELF64 Linux 二進位檔。 其主要目標是增加檔案系統效能, 以及新增完整的系統呼叫相容性。 這個新架構會變更這些 Linux 二進位檔與 Windows 和您電腦硬體的互動方式, 但仍然提供與 WSL 1 (目前廣泛可用的版本) 相同的使用者體驗。 個別的 Linux 散發版本可以執行為 WSL 1 散發版本, 或作為 WSL 2 散發版本, 隨時都可以升級或降級, 而且您可以並存執行 WSL 1 和 WSL 2 散發版本。 WSL 2 使用全新的架構, 其使用真實的 Linux 核心。

## <a name="linux-kernel-in-wsl-2"></a>WSL 中的 Linux 核心2

WSL 2 中的 Linux 核心是根據 kernel.org 提供的來源, 從最新的穩定分支內建。此核心已特別針對 WSL 2 進行調整。 它已針對大小和效能優化, 以在 Windows 上提供絕佳的 Linux 體驗, 並透過 Windows 更新提供服務, 這表示您將獲得最新的安全性修正程式和核心改良功能, 而不需要自行管理。

此外, 此核心也會是開放原始碼。 您可以在[這裡](https://github.com/microsoft/WSL2-Linux-Kernel)找到 Linux 核心的完整原始程式碼。 如果您想要閱讀更多關於此核心的資訊, 您可以查看[這篇](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)建立的小組所撰寫的文章。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 架構的簡要總覽

WSL 2 使用最新且最棒的虛擬化技術, 在輕量公用程式虛擬機器 (VM) 內執行其 Linux 核心。 不過, WSL 2 將不會是傳統的 VM 體驗。 傳統的 VM 體驗可能會很慢而無法開機、隔離、耗用大量資源, 而且需要您的時間來管理它。 WSL 2 沒有這些屬性。 它仍然會提供 WSL 1 的優異優勢:Windows 和 Linux 之間的高層級整合、極快速的開機時間、小型的資源使用量, 而且最棒的就是不需要進行 VM 設定或管理。 雖然 WSL 2 會使用 VM, 但它會在幕後進行管理並執行, 讓您擁有與 WSL 1 相同的使用者體驗。

## <a name="increased-file-io-performance"></a>增加檔案 IO 效能

需要大量檔案的作業, 例如 git 複製、npm 安裝、apt 更新、apt 升級等等, 全都會明顯加快。 實際的速度增加將取決於您正在執行的應用程式, 以及它與檔案系統的互動方式。 相較于 WSL 1, WSL 2 的初始版本在解壓縮壓縮的 tarball 時, 執行的速度最多可20倍, 而在使用 git 複製時, npm 在各種專案上安裝和 cmake 的速度大約是2倍。

## <a name="full-system-call-compatibility"></a>完整系統呼叫相容性

Linux 二進位檔會使用系統呼叫來執行許多功能, 例如存取檔案、要求記憶體、建立進程等等。 WSL 1 使用 WSL 小組所建立的轉譯層, 而 WSL 2 則包含其本身的 Linux 核心, 並具有完整的系統呼叫相容性。 這引進了一套全新的應用程式, 您可以在 WSL 內執行, 例如 Docker 等。 此外, Linux 核心的任何更新都可以立即新增至您的電腦, 而不是等待 WSL 小組執行變更, 然後將它們新增。