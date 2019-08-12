---
title: 建立適用於 WSL 的自訂 Linux 發行版本
description: 了解如何為適用於 Linux 的 Windows 子系統建立自訂 Linux 發行套件。

keywords: BashOnWindows, bash, wsl, windows, windows 子系統, 發行版本, 自訂

author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040781"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>建立適用於 WSL 的自訂 Linux 發行版本


使用我們的開放原始碼 WSL 範例來建置適用於 Microsoft Store 和/或建立用於側載的 Linux 發行版本套件。您可以在 GitHub 上找到[發行版本啟動器存放庫](https://github.com/Microsoft/WSL-DistroLauncher)。


此專案會啟用:
* Linux 發行版本維護人員封裝並提交 Linux 發行版本，作為在 WSL 上執行的 appx
* 開發人員建立可側載至其開發電腦的自訂 Linux 發行版本

## <a name="background"></a>背景

我們會透過 Microsoft Store 將 WSL 的 Linux 發行版本作為 UWP 應用程式發行。您可以安裝將在 WSL 上執行的那些應用程式，也就是位於 Windows 核心的子系統。此傳遞機制有許多優點，如[先前的部落格文章](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)中所述。

## <a name="sideloading-a-custom-linux-distro-package"></a>側載自訂 Linux 發行版本套件
您可以建立自訂 Linux 發行版本套件作為應用程式，以在您的個人電腦上側載。請注意，除非您以發行維護程式形式提交，否則您的自訂套件不會透過 Microsoft Store 發行。
若要設定您的電腦以側載應用程式，您必須在 [適用於開發人員] 底下的 [系統設定] 中啟用此功能。請確定已選取開發人員模式，或選取側載應用程式


## <a name="for-linux-distro-maintainers"></a>適用於 Linux 發行版本維護人員
若要提交到商店，您必須與我們合作以接收發行核准。如果您是想要將發行版本新增至 Microsoft Store 的 Linux 發行版本擁有者，請透過 wslpartners@microsoft.com 與我們連絡。
## <a name="getting-started"></a>開始使用
依照[發行版本啟動器 GitHub 存放庫](https://github.com/Microsoft/WSL-DistroLauncher)中的指示建立自訂 Linux 發行版本套件。

## <a name="team-blogs"></a>小組 Blog
* [將適用於 Linux 發行版本維護人員的 WSL 變更為開放原始碼及側載自訂 Linux 發行版本](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)

* [命令列的 blog](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>提供意見反應
* [發行版本啟動器 GitHub 存放庫](https://github.com/Microsoft/WSL-DistroLauncher)
* [適用於 WSL 的 GitHub 問題追蹤器](https://github.com/Microsoft/BashOnWindows/issues)
* [命令列 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
