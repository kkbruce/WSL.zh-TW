---
title: 在 Windows 10 上安裝適用於 Linux 的 Windows 子系統 (WSL)
description: 適用於 Windows 10 上適用於 Linux 的 Windows 子系統的安裝指示。
keywords: BashOnWindows, bash, wsl, windows, 適用於 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499281"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>適用於 Linux 的 windows 子系統安裝指南 Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>安裝適用於 Linux 的 Windows 子系統

在安裝任何適用於 WSL 的 Linux 散發版本之前, 您必須確定已啟用「適用於 Linux 的 Windows 子系統」選用功能:

1. 以系統管理員身分開啟 PowerShell 並執行:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出現提示時, 重新開機您的電腦。

## <a name="install-your-linux-distribution-of-choice"></a>安裝您選擇的 Linux 散發套件
若要下載並安裝您慣用的散發版本, 您有三個選擇:
1. 從 Microsoft Store 下載並安裝 (請參閱下文)
1. 從命令列/腳本下載並安裝 ([閱讀手動安裝指示](install-manual.md))
1. 下載並手動打開封裝並安裝 (適用於 Windows Server-[此處的指示](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 秋季建立者更新和更新版本:從 Microsoft Store 安裝

> 本節適用於 Windows 組建16215或更新版本。  請遵循下列步驟來[檢查您的組建](troubleshooting.md#check-your-build-number)。 

1. 開啟 Microsoft Store, 然後選擇您最愛的 Linux 散發套件。

    ![Microsoft Store 中的 Linux 散發版本視圖](media/store.png)

    下列連結會開啟每個散發套件的 Microsoft store 頁面:

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE 閏15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [適用於 WSL 的 Fedora Remix](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. 從散發版本的頁面中, 選取 [取得]

    ![Microsoft store 中的 Linux 散發版本視圖](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>完成散發版本的初始化
現在已安裝您的 Linux 散發版本, 您必須先[初始化新的散發版本實例](initialize-distro.md)一次, 才能使用它。

## <a name="troubleshooting"></a>疑難排解： 

以下是相關的錯誤和建議的修正。 如需其他常見錯誤及其解決方案, 請參閱[WSL 疑難排解頁面](troubleshooting.md)。

* **安裝失敗, 發生錯誤0x80070003**
    * 適用於 Linux 的 Windows 子系統只會在您的系統磁片磁碟機上執行`C:` (通常是您的磁片磁碟機)。 請確定散發版本儲存在您的系統磁片磁碟機上:  
    * 開啟 [**設定** -> ] [**儲存體** -> **] [其他存放裝置設定]:變更系統設定的新內容**儲存
     ![位置, 以在 C: 磁片磁碟機上安裝應用程式](media/AppStorage.png)
    
    
 * **WslRegisterDistribution 失敗, 發生錯誤0x8007019e**   
  * 未啟用適用於 Linux 的 Windows 子系統選用元件: 
   * 開啟 **控制台** ->  **程式和功能**-> * * 開啟或關閉 windows 功能 * *-> 檢查**適用於 Linux 的 windows 子系統,** 或使用本文開頭所述的 PowerShell Cmdlet。
