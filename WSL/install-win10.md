---
title: 在 Windows 10 上安裝 Windows 子系統適用於 Linux (WSL)
description: Windows 子系統的安裝指示適用於 Windows 10 上的 Linux。
keywords: 安裝 BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063286"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Linux 安裝指南，適用於 Windows 10 的 Windows 子系統

## <a name="install-the-windows-subsystem-for-linux"></a>安裝適用於 Linux 的 Windows 子系統

之前的 WSL 安裝任何 Linux 散發版本，您必須確定 「 Windows 子系統的 Linux 」 啟用選擇性功能：

1. 系統管理員身分開啟 PowerShell 並執行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 重新啟動您的電腦，當系統提示您。

## <a name="install-your-linux-distribution-of-choice"></a>安裝您的 Linux 散發套件的選擇
若要下載並安裝您慣用的 distro(s)，您會有三種選擇：
1. 從 Windows 市集 （如下所示） 下載並安裝
1. 從命令列/指令下載並安裝 ([讀取的手動安裝指示](install-manual.md))
1. 下載手動解壓縮並安裝 (適用於 Windows Server-[這裡的指示](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 和更新版本：從 Microsoft Store 安裝

> 此區段可讓 Windows 組建 16215 或更新版本。  請遵循下列步驟[來檢查組建](troubleshooting.md#check-your-build-number)。 

1. 開啟 Microsoft Store，並選擇您最愛的 Linux 散發套件。

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/store.png)

    下列連結會開啟 [Windows 市集] 頁面的每個散發：

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. 從散發版本的頁面上，選取 "Get"

    ![在 Windows 市集中的 Linux 散發版本的檢視](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>您的散發版本的完成初始化
既然您的 Linux 散發套件已安裝，您必須[初始化新的散發版本執行個體](initialize-distro.md)一次，才能使用。

## <a name="troubleshooting"></a>疑難排解： 

以下是相關的錯誤和建議的修正。 請參閱[WSL 疑難排解頁面](troubleshooting.md)其他常見的錯誤和他們的解決方案。

* **安裝失敗，錯誤 0x80070003**
    * 適用於 Linux 的 Windows 子系統只在您的系統磁碟機上執行 (這通常是您`C:`磁碟機)。 請確定發行版本會儲存您的系統磁碟機上：  
    * 開啟**設定** -> **儲存體** -> **更多的儲存體設定：新的內容儲存的變更**
    ![系統設定的 c： 磁碟機上安裝應用程式中的圖片](media/AppStorage.png)
