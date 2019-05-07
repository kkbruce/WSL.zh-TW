---
title: Windows Server 上安裝 Linux 子系統
description: 在 Windows Server 上的 Linux 子系統的安裝指示。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 windows server 的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063616"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安裝指南

> 適用於 Windows Server 2019 和更新版本

在 / / Build2017，Microsoft 宣布，將會是適用於 Linux 的 Windows 子系統[Windows Server 上可用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。  這些指示會逐步執行適用於 Linux 的 Windows Server 1709 和更新版本的 Windows 子系統。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>啟用適用於 Linux (WSL) 的 Windows 子系統

您可以在 Windows 上執行的 Linux 散發版本之前，您必須啟用 「 Windows Linux 子系統 」 選擇性功能，並重新啟動。

1. 系統管理員身分開啟 PowerShell 並執行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 重新啟動您的電腦，當系統提示您。 **這必須重新開機**為了確保 WSL 可以起始受信任的執行環境。

## <a name="download-a-linux-distro"></a>下載 Linux 發行版本

請遵循[這些指示](install-manual.md)若要下載您最愛的 Linux 散發套件。

## <a name="extract-and-install-a-linux-distro"></a>解壓縮並安裝 Linux 發行版本
既然您已下載的散發版本，就會將其內容解壓縮，並手動安裝散發版本：

1. 擷取`<distro>.appx`套件的內容，例如，使用 PowerShell:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. 執行散發啟動器若要完成安裝，請在 [目標] 資料夾中，執行 distro 啟動器應用程式，名為`<distro>.exe`。 例如：`ubuntu.exe`等等。

    ![擴充的 Windows Server 上的 Ubuntu 散發套件](media/server-appx-expand.png)

    > **疑難排解**
    > * **安裝失敗，錯誤 0x8007007e**:當您的系統不支援 WSL 時，就會發生此錯誤。 請確認︰
    >   * 您正在執行 Windows 組建，16215 或更新版本。 [請檢查您的組建](troubleshooting.md#check-your-build-number)。
    >   * 已啟用 Linux 選擇性元件的 Windows 子系統，並重新啟動電腦。  [請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 將您的散發套件路徑新增至 Windows 環境的路徑 (`C:\Users\Administrator\Ubuntu`在此範例中)，例如，使用 Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    您現在可以啟動您的散發版本，從任何路徑輸入`<distro>.exe`。 例如：`ubuntu.exe`

既然您的 Linux 散發套件已安裝，您必須[初始化新的散發版本執行個體](initialize-distro.md)才能使用您的散發套件。
