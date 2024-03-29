---
title: 手動下載適用于 Linux 的 Windows 子系統 (WSL) 散發版本
description: 如何手動下載適用于 Linux 的 Windows 子系統發行版本的指示。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、WSL、windows 子系統、散發版本、ubuntu、openSUSE、SLES、debian、kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: bf2f2e24fb8a2db49270fb77558d4fda1828dedf
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523775"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>手動下載適用于 Linux 的 Windows 子系統散發版本套件

在幾種情況下, 您可能無法 (或想要) 透過 Microsoft Store 安裝 WSL Linux 散發版本。 具體而言, 您可能正在執行不支援 Microsoft Store 的 Windows Server 或長期維護 (LTSC) 桌面作業系統 SKU, 或公司網路原則及/或系統管理員不允許在您的環境中使用 Microsoft Store。

在這些情況下, 雖然 WSL 本身可供使用, 如果您無法存取存放區, 如何在 WSL 中下載並安裝 Linux 散發版本？

> 注意:**不允許在 Windows 10 S 模式上執行命令列 shell 環境, 包括 Cmd、PowerShell 和 Linux/WSL 散發版本**。 這項限制是為了確保 S 模式所提供的完整性和安全目標:如需詳細資訊, 請閱讀[這篇文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)。

## <a name="downloading-distros"></a>正在下載散發版本

如果無法使用 Microsoft Store 應用程式, 您可以按一下下列連結, 下載並手動安裝 Linux 散發版本:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [適用于 WSL 的 Fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

這會導致`<distro>.appx`套件下載到您選擇的資料夾。 遵循[安裝指示](#Installing-your-distro)來安裝您下載的散發版本。

## <a name="downloading-distros-via-the-command-line"></a>透過命令列下載散發版本
如果您想要的話, 也可以透過命令列下載您偏好的散發版本:

 ### <a name="download-using-powershell"></a>使用 PowerShell 下載
 若要使用 PowerShell 下載散發版本, 請使用[WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) Cmdlet。 以下是下載 Ubuntu 16.04 的範例指示。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 如果下載花費較長的時間, 請設定來關閉進度列`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>使用捲曲下載
Windows 10 春季 2018 Update (或更新版本) 包含常用的[捲曲命令列公用程式](https://curl.haxx.se/), 可讓您從命令列叫用 web 要求 (例如 HTTP GET、POST、PUT 等命令)。 您可以使用`curl.exe`下載上述散發版本:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

在上述範例中, `curl.exe`會執行 (而不`curl`只是), 以確保在 PowerShell 中叫用實際的可執行檔, 而不是叫用[WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)的 powershell 捲曲別名

> 注意:如果`curl`您必須使用 Cmd shell 和/或`.bat`  /  `.cmd`腳本來叫用/編寫下載步驟, 則使用可能會比較理想。

## <a name="installing-your-distro"></a>安裝散發版本
如果您使用的是 Windows 10, 您可以使用 PowerShell 安裝散發版本。 只要流覽至包含上述散發版本所下載的資料夾, 然後在該目錄中執行下列命令, `app_name`其中是散發版本 .appx 檔案的名稱。  
```Powershell
Add-AppxPackage .\app_name.appx
```

如果您使用的是 Windows server, 可以在[Windows server](install-on-server.md)檔頁面上找到安裝指示。

安裝散發版本之後, 請參閱[Intilization 步驟](initialize-distro.md)頁面以初始化新的散發版本。
