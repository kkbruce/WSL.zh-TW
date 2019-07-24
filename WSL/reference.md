---
title: 適用于 Linux 的 Windows 子系統命令參考
description: 管理適用于 Linux 的 Windows 子系統的命令清單
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307660"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>適用于 Linux 的 Windows 子系統命令參考

與適用于 Linux 的 Windows 子系統互動的最佳方式是使用`wsl.exe`命令。 

## `wsl.exe` 

以下清單包含使用`wsl.exe` Windows 1903 版時的所有選項。

* 執行 Linux 二進位檔的引數:

    * 如果未提供任何命令列, 則 wsl 會啟動預設的 shell。

    * --exec、-e<CommandLine>
        * 執行指定的命令, 而不使用預設的 Linux shell。

    * --
        * 依情況傳遞其餘的命令列。

* 選項:
    * --散發,-d<Distro>
        * 執行指定的散發。

    * --user、-u<UserName>
        * 以指定的使用者身分執行。

* 用於管理適用于 Linux 的 Windows 子系統的引數:

    * --export <Distro><FileName>
        * 將散發匯出至 tar 檔案。
        標準輸出的檔案名可以是-。

    * --import <Distro> <InstallLocation>[Options <FileName> ]
        * 匯入指定的 tar 檔案做為新的散發套件。
        檔案名可以是-用於標準輸入。

        * 選項:
            * --version <Version>指定要用於新散發的版本。

    * --list、-l [Options]
        * 列出發行版本。

        * 選項:
            * --全部
                * 列出所有散發套件, 包括目前正在安裝或卸載的發行版本。

            * --正在執行
                * 僅列出目前正在執行的散發。

    * --set-default、-s<Distro>
        * 將散發設定為預設值。

    * --設定-預設版本<Version>
        * 變更新發行版本的預設安裝版本。

    * --設定版本<Distro><Version>
        * 變更指定之散發套件的版本。

    * --terminate、-t<Distro>
        * 終止指定的散發。

    * --取消註冊<Distro>
        * 取消註冊散發。

    * --help
        * 顯示使用方式資訊。

## <a name="additional-commands"></a>其他命令

還有與適用于 Linux 的 Windows 子系統互動的歷史命令。 其功能包含在中`wsl.exe`, 但仍可供使用。 

### `wslconfig.exe`

此命令可讓您設定 WSL 分佈。 以下是其選項的清單。

* /l,/list [選項]
    * 列出已註冊的發行版本。
        * /all-選擇性地列出所有散發套件, 包括目前正在安裝或卸載的發行版本。

        * /running-僅列出目前正在執行的散發。

* /s、/setdefault<DistributionName>
    * 將散發設定為預設值。

* /t、/terminate<DistributionName>
    * 終止散發。

* /u、/unregister<DistributionName>
    * 取消註冊散發。

### `bash.exe`

此命令可用來啟動 bash shell。 以下是您可以搭配此命令使用的選項。

* 未指定任何選項
    * 在目前目錄中啟動 Bash shell。 如果未安裝 Bash shell, 則會自動執行`lxrun /install`

* bash ~
    * 在使用者的主目錄中啟動 bash shell。  類似于正在`cd ~`執行。

* bash-c "&lt;command&gt;"
    * 執行命令, 列印輸出並結束 Windows 命令提示字元。 <br/> <br/> 實例`bash -c "ls"`

## <a name="deprecated-commands"></a>已淘汰的命令

`lxrun.exe`是用來安裝和管理適用于 Linux 的 Windows 子系統的第一個命令。 它已被取代為 Windows 10 1803 和更新版本。

命令`lxrun.exe`可以用來直接與[適用于 Linux 的 Windows 子系統 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)互動。  這些命令會安裝到`\Windows\System32`目錄中, 而且可以在 Windows 命令提示字元或 PowerShell 中執行。

| 命令                     | 描述                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 命令是用來管理 WSL 實例。 |
| `lxrun /install`            | 開始下載和安裝程式。 <br/> 可能會加入 **/y**以略過所有提示。  系統會自動接受確認提示, 並將預設使用者設定為 [根]。          |
| `lxrun /uninstall`          | 卸載並刪除 Ubuntu 映射。  根據預設, 這不會移除使用者的 Ubuntu 主目錄。 <br/> 可能會新增 **/y**以自動接受確認提示 <br/>**/full**卸載並刪除使用者的 Ubuntu 主目錄         |
| `lxrun /setdefaultuser <userName>`     | 設定 Ubuntu 使用者的預設 Bash。 如果指定的使用者不存在, 則會提示您輸入密碼。  如需詳細資訊, https://aka.ms/wslusers 請造訪:。 <br/> **/y**略過密碼的 promping。  將建立不含密碼的使用者。|
| `lxrun /update`            | 更新子系統的套件索引          |
