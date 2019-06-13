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
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 的安裝指示

安裝和開始使用 WSL 2 會完成下列步驟：

- 啟用 '虛擬機器平台' 選用元件
- 設定受到 WSL 2 使用命令列的散發套件
- 確認要使用的 WSL 您的散發套件的版本

## <a name="enable-the-virtual-machine-platform-optional-component"></a>啟用 '虛擬機器平台' 選用元件

系統管理員身分開啟 PowerShell 並執行：

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

啟用這些變更之後，您必須重新啟動電腦。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>設定受到 WSL 2 使用命令列的散發套件

在 PowerShell 中執行：

`wsl --set-version <Distro> 2`

並請務必取代`<Distro>`與您的散發套件的實際名稱。 (您可以找到這些命令： `wsl -l`)。 您可以變更回 WSL 1 隨時執行與上述的相同命令，但取代 '2' 與' 1'。

此外，如果您想要讓 WSL 2 預設架構則可以使用下列命令：

`wsl --set-default-version 2`

這會讓任何新安裝的散發套件會初始化為 WSL 2 發行版本。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>完成，並確認 WSL 您的散發套件的版本會使用

若要確認哪些版本的 WSL 使用每個散發套件會使用下列命令：

`wsl --list --verbose` 或 `wsl -l -v`

您已選擇上述的散發版本現在應該會顯示 '2' 的 'version' 資料行底下。 現在，您已完成放心地開始使用您的 WSL 2 發行版本 ！ 