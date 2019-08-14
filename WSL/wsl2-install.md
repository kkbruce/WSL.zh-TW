---
title: 安裝 WSL 2
description: WSL 2 的安裝指示
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246872"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 的安裝指示

若要安裝並開始使用 WSL 2，請完成下列步驟：

- 啟用「虛擬機器平臺」選用元件
- 使用命令列設定 WSL 2 支援的發行版本
- 驗證發行版本本使用的 WSL 版本

請注意，您必須執行 Windows 10 組建 18917 或更新版本才能使用 WSL 2，而且必須已安裝 WSL (您可以在[這裡](./install-win10.md)找到相關指示)。 

## <a name="enable-the-virtual-machine-platform-optional-component"></a>啟用「虛擬機器平臺」選用元件

以系統管理員身分開啟 PowerShell 並執行：

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

啟用這些變更之後，電腦需要重新開機。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>使用命令列設定 WSL 2 支援的發行版本

在 PowerShell 中執行：

`wsl --set-version <Distro> 2`

而且，請務必將 `<Distro>` 取代為您的實際發行版本名稱。 (您可以使用命令 `wsl -l` 來找到這些名稱)。 您可以隨時執行與上面相同的命令，但將 '2' 取代為 '1'，以變更回 WSL 1。

此外，如果您要讓 WSL 2 成為您的預設架構，則可以使用以下命令來執行此動作：

`wsl --set-default-version 2`

這會讓您安裝的任何全新發行版本都初始化為 WSL 2 發行版本。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>完成驗證發行版本所使用的 WSL 版本

若要確認每個發行版本使用的 WSL 版本，請使用下列命令：

`wsl --list --verbose` 或 `wsl -l -v`

您在上面所選擇的發行版本現在應該在 [版本] 欄位下顯示 '2'。 現在您已完成作業，可以隨時開始使用 WSL 2 發行版本！ 

## <a name="troubleshooting"></a>疑難排解： 

以下是安裝 WSL 2 時的相關錯誤和建議修正。 有關其他一般 WSL 錯誤和其解決方案的 [WSL 疑難排解頁面](troubleshooting.md)。

* **安裝失敗，發生錯誤 0x80070003 或錯誤0x80370102**
    * 請確定已在電腦的 BIOS 內啟用虛擬化。 有關如何執行此操作的指示會因電腦而異，並且很可能與 CPU 相關。
   
* **嘗試升級時發生錯誤`Invalid command line option: wsl --set-version Ubuntu 2`**
    * 請確定已啟用適用於 Linux 的 Windows 子系統，且使用的是 Windows 組建 18917 或更高版本。 若要啟用 WSL，請在具有系統管理員權限的 Powershell 提示中執行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 您可以在[這裡](./install-win10.md)尋找完整的 WSL 安裝指示。