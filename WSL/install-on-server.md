---
title: 在 Windows Server 上安裝 Linux 子系統
description: Windows Server 上 Linux 子系統的安裝指示。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu、windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308794"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安裝指南

> 適用于 Windows Server 2019 和更新版本

在//Build2017, Microsoft 宣佈 windows Server 上適用于 Linux 的 Windows 子系統將可[供使用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。  這些指示會逐步解說如何在 Windows Server 1709 和更新版本上執行適用于 Linux 的 Windows 子系統。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>啟用適用于 Linux 的 Windows 子系統 (WSL)

您必須先啟用「適用于 Linux 的 Windows 子系統」選用功能並重新啟動, 才可以在 Windows 上執行 Linux 散發版本。

1. 以系統管理員身分開啟 PowerShell 並執行:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出現提示時, 重新開機您的電腦。 **這是必要的重新開機**, 以便確保 WSL 可以起始受信任的執行環境。

## <a name="download-a-linux-distro"></a>下載 Linux 散發版本

請遵循[這些指示](install-manual.md)來下載您最愛的 Linux 散發套件。

## <a name="extract-and-install-a-linux-distro"></a>解壓縮並安裝 Linux 散發版本
既然您已下載散發版本, 請將其內容解壓縮並手動安裝散發版本:

1. `<distro>.appx`解壓縮套件的內容, 例如使用 PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. 執行散發版本啟動器以完成安裝, 在名為`<distro>.exe`的目的檔案夾中執行散發版本啟動器應用程式。 例如: `ubuntu.exe`、等等。

    ![Windows Server 上擴充的 Ubuntu 散發版本](media/server-appx-expand.png)

    > **疑難排解**
    > * **安裝失敗, 發生錯誤 0x8007007e**:當您的系統不支援 WSL 時, 就會發生此錯誤。 請確認︰
    >   * 您正在執行 Windows 組建16215或更新版本。 [檢查您的組建](troubleshooting.md#check-your-build-number)。
    >   * [適用于 Linux 的 Windows 子系統] 選用元件已啟用, 且電腦已重新開機。  [請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 將您的散發版本路徑新增至 Windows 環境路徑`C:\Users\Administrator\Ubuntu` (在此範例中為), 例如使用 Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    您現在可以輸入`<distro>.exe`, 從任何路徑啟動散發版本。 例如：`ubuntu.exe`

現在已安裝您的 Linux 散發版本, 您必須先[初始化新的散發版本實例](initialize-distro.md), 然後再使用散發版本。
