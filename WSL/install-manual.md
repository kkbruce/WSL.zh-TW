---
title: 手動下載 Linux (WSL) 散發版本的 Windows 子系統
description: 如何手動下載針對 Linux 發行版本的 Windows 子系統的指示。
keywords: BashOnWindows、 bash、 wsl、 windows、 windows subsystem for linux WSL，windows 子系統、 散發版本、 ubuntu、 openSUSE、 SLES，debian，kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063566"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>手動下載 Linux 散發套件的 Windows 子系統

有幾個案例中您可能不會 （或不想） 若要安裝 WSL Linux 散發版本，透過 Microsoft Store。 具體來說，您可能會執行 Windows Server 或長期維護 (LTSB/LTSC) 桌面 OS SKU 不支援 Microsoft Store，或您公司的網路原則和/或系統管理員不允許您的環境中的 Microsoft Store 使用量。

在這些情況下，而本身的 WSL 可用，如何下載及安裝 WSL 中的 Linux 散發版本，如果您無法存取存放區嗎？

> 注意：**命令列殼層的環境，包括 Cmd、 PowerShell 和 Linux/WSL 散發版本不允許執行 Windows 10 S 模式**。 這項限制是為了確保 S 模式提供的完整性和安全性目標：讀取[這篇文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)如需詳細資訊。

## <a name="downloading-distros"></a>下載散發版本

如果找不到 Microsoft Store 應用程式，您可以下載，並按一下這些連結，手動安裝的 Linux 散發版本：
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE](https://aka.ms/wsl-opensuse-42)
* [SLES](https://aka.ms/wsl-sles-12)

這會導致`<distro>.appx`套件下載至您所選擇的資料夾。 請遵循[安裝指示](#installing-your-distro)安裝您已下載的 distro(s)。

## <a name="downloading-distros-via-the-command-line"></a>下載透過命令列的散發套件
如果您想，您也可以下載您慣用的 distro(s) 透過命令列：

 ### <a name="download-using-powershell"></a>使用 PowerShell 下載
 若要下載使用 PowerShell 的散發版本，請使用[Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。 以下是範例指示，來下載 Ubuntu 16.04。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 如果下載花費很長的時間，將進度列關閉設定 `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>使用 curl 下載
Windows 10 Spring 2018 Update （或更新版本） 包含熱門[curl 命令列公用程式](https://curl.haxx.se/)，您可以叫用 web 要求 (也就是 HTTP GET、 POST、 PUT、 等命令) 從命令列。 您可以使用`curl.exe`下載上述的散發版本：

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

在上述範例中，`curl.exe`執行 (不是只`curl`) 來確保，在 PowerShell 中，實際的 curl 可執行檔是叫用，不別名的 PowerShell curl [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> 注意：使用`curl`可能比較適合，如果您必須叫用/指令碼下載使用 Cmd shell 中的步驟和 （或) `.bat`  /  `.cmd`指令碼。

## <a name="installing-your-distro"></a>安裝您的散發套件
如需有關如何安裝您已下載的 distro(s) 的指示，請參閱[Windows 桌面](install-win10.md)或是[Windows Server](install-on-server.md)安裝指示。
