---
title: 安裝或移除 Windows 10 年度更新版或建立者更新
description: Windows 10 年度更新版或建立者更新的舊版、Beta 散發版本的安裝和卸載指示
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10, 舊版, Beta, 安裝, 移除, 卸載, 取消安裝, 刪除, 已淘汰
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499270"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>在 Windows 10 年度更新版和建立者更新上安裝或卸載適用于 Linux 的 Windows 子系統的指南 

如果您執行的是 Windows 10 建立者更新或更新版本, 請[遵循 windows 10 安裝指示](install-win10.md)。

<strong><em><span style="color: #f28014">下列指示適用于執行 Windows 10 年度更新版或 Windows 10 建立者更新的使用者</span></em></strong>

在 Windows 10 秋季建立者更新 (版本 1709) 之前, WSL 已發行為搶鮮版 (Beta) 功能, 而且會在第一次執行「Windows 上的 Ubuntu 上的 Bash」 (或 Bash) 時, 安裝單一 Ubuntu 實例。

> 雖然您可以在先前的 Windows 10 版本上使用 WSL, 但這個 Beta 版的「舊版散發版本」現在已被視為過時。 我們強烈建議您執行最新版本的 Windows 10。 每個新的 Windows 10 版本都包含 WSL 的數百個修正和改善, 讓更多的 Linux 工具和應用程式可以在 WSL 上正確執行。

如果您無法升級至秋季建立者更新或更新版本, 請遵循下列步驟來啟用及使用 WSL:

1. 開啟開發人員模式以在 Windows 10 年度更新版或建立者更新上執行 WSL, 您必須啟用開發人員模式:

    開啟**開發人員的** **設定** -> **更新和安全性** -> 

    選取 [開發人員模式] 選項按鈕  
    ![啟用開發人員模式](media/updateAndSecurity.png)

    > [Windows 10 秋季建立者更新已移除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)啟用開發人員模式的需求

1. 開啟命令提示字元。  輸入`bash` , 然後按 enter 鍵

    當您第一次在 Windows 上的 Ubuntu 上執行 Bash 時, 系統會提示您接受標準授權。 一旦接受, WSL 會下載 Ubuntu 實例並將其安裝到您的電腦上, 並在 [開始] 功能表中新增 "Bash on Ubuntu on Windows" 快捷方式。

    ![提示安裝 Ubuntu](media/bashShellInstall.png)

    當您第一次在 Windows 上的 Ubuntu 上執行 Bash 時, 系統會提示您建立 UNIX 使用者名稱和密碼。 遵循[新的散發版本實例指示](initialize-distro.md)來完成安裝

1. 啟動新的 Ubuntu shell, 方法是:
    * `bash`從命令提示字元執行
    * 按一下 [開始] 功能表中的 [Windows 上 Ubuntu 上的 Bash] 快捷方式

    
## <a name="uninstallingremoving-the-legacy-distro"></a>卸載/移除舊版散發版本
如果您從舊版已安裝 WSL 的 Windows 10 版本升級至 Windows 10 秋季建立者更新, 現有的散發版本將維持不變。 不過, 我們強烈建議您儘快安裝新的商店提供散發版本, 並將任何必要的檔案、資料等等從您的舊版散發版本遷移到新的散發版本。

若要從您的電腦移除舊版散發版本, 請從命令列或 PowerShell 實例執行下列程式碼:

```console
wsl --unregister Legacy
```

如果您不是使用 Windows 1903 版或更新版本, 您可能需要改`wslconfig /u Legacy`為`lxrun /uninstall /full`執行或。 

### <a name="manually-deleting-the-legacy-distro"></a>手動刪除舊版散發版本
如有需要, 您可以手動刪除舊版實例。 如果您在使用`lxrun.exe`卸載舊版散發版本時遇到問題, 或是執行 Windows 10 春季 2018 Update (或更新版本), 但未隨附于`lxrun.exe`, 這可能是必要的。

若要強制刪除舊版 WSL 散發版本, 請使用`%localappdata%\lxss\` Windows 的 [檔案瀏覽器] 或命令列來刪除資料夾 (及其所有子內容):

使用 PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

使用 Cmd:
```console
DEL /S %localappdata%\lxss\
```
