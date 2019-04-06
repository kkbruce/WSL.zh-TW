---
title: 安裝或移除在 Windows 10 年度更新版 」 或 「 建立者更新
description: 安裝和解除安裝舊版，Windows 10 年度更新版或 Creators Update 上的 beta 版散發套件的指示
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10，舊版、 beta 版的 windows 子系統安裝、 移除、 解除安裝，請解除安裝，delete，已被取代
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063586"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>若要安裝或解除安裝適用於 Windows 10 年度更新版和 Creators Update 上 Linux 的 Windows 子系統的指南 

如果您執行 Windows 10 Creators Update 或更新版本中，請[遵循 Windows 10 安裝指示](install-win10.md)。

<strong><em><span style="color: #f28014">下列指示是提供給執行 Windows 10 年度更新版或 Windows 10 Creators Update 的使用者</span></em></strong>

之前 Windows 10 Fall Creators Update （1709年版），WSL 會發行為 beta 功能，並 「 Bash 在 Ubuntu 上 Windows 」 （或 Bash.exe） 第一次執行時，安裝單一的 Ubuntu 執行個體。

> 雖然您可以使用 WSL 有關較早的 Windows 10 版本，此 beta 版的 「 舊版 distro"會被視為淘汰。 我們強烈建議您執行可用的 Windows 10 最新版本。 每個新的 Windows 10 版本包含數以百計的修正和改善在 WSL，允許更多 Linux 工具和應用程式，以在 WSL 上正常執行。

如果您無法升級至 Fall Creators Update 或更新版本，請遵循下列步驟來啟用及使用 WSL:

1. 開啟 開發人員模式來執行 WSL Windows 10 年度更新版或 Creators Update 上，您必須啟用開發人員模式：

    開啟**設定** -> **更新與安全性** -> **適用於開發人員**

    選取 [開發人員模式] 選項按鈕  
    ![啟用開發人員模式](media/updateAndSecurity.png)

    > 若要啟用開發人員模式需求是[在 Windows 10 Fall Creators Update 中移除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. 開啟命令提示字元。  型別`bash`然後按 enter 鍵

    您第一次在 Ubuntu 執行 Bash Windows，系統會提示您接受 Canonical 的授權。 一旦 accpted，WSL 會下載並安裝到您的電腦上的 Ubuntu 執行個體，"Bash 在 Ubuntu 上 Windows 「 快顯會新增至 [開始] 功能表。

    ![若要安裝 Ubuntu 的提示字元](media/bashShellInstall.png)

    您第一次在 Ubuntu 執行 Bash Windows，系統會提示您建立的 UNIX 使用者名稱和密碼。 請遵循[散發版本的新執行個體指示](initialize-distro.md)完成您的安裝

1. 透過下列方式啟動新的 Ubuntu 殼層：
    * 執行`bash`從命令提示字元
    * 按一下 [開始] 功能表"Bash 在 Ubuntu 上 Windows 「 捷徑

    
## <a name="uninstallingremoving-the-legacy-distro"></a>解除安裝/移除舊版的散發套件
如果您從您安裝 WSL 先前的 Windows 10 版本升級至 Windows 10 Fall Creators Update，您現有的散發套件會維持不變。 不過，我們強烈建議您安裝新的存放區提供散發版本儘速，，並從舊版的散發的任何必要的檔案、 資料等移轉至新的散發。

若要從您的電腦中移除舊版的散發版本，執行下列命令從命令列或 PowerShell 執行個體：

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>手動刪除舊版的散發套件
如果您想，您可以手動刪除舊版執行個體。 如果您遇到問題，解除安裝舊版的發行版本使用可能會需要`lxrun.exe`，或正在執行 Windows 10 Spring 2018 Update （或更新版本） 這並未隨附`lxrun.exe`。

若要強制刪除舊版的 WSL 散發版本，請刪除`%localappdata%\lxss\`資料夾 (和所有的子內容) 使用 Windows 的 [檔案總管] 中，或在命令列：

使用 PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

使用命令提示字元：
```console
DEL /S %localappdata%\lxss\
```
