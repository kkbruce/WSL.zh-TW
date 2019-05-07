---
title: 建置自訂的 Linux Distro WSL
description: 了解如何建立自訂的 Linux 散發套件的 Windows 子系統，適用於 Linux。
keywords: BashOnWindows，bash，wsl、 windows、 windows 子系統、 散發版本，自訂
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063256"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>建立自訂的 Linux Distro WSL

為 Microsoft Store 建置 WSL 散發套件，及/或建立自訂的側載功能的 Linux 散發套件，請使用我們的開放原始碼 WSL 範例。 您可以找到[distro 啟動器存放庫](https://github.com/Microsoft/WSL-DistroLauncher)GitHub 上。

此專案可讓：
* 若要封裝並送出為 appx 在 WSL 上執行的 Linux 散發套件的 Linux 發行版本維護者
* 開發人員建立自訂的 Linux 散發套件可以側載至其開發電腦

## <a name="background"></a>背景
我們將散發的 Linux 散發版本 WSL 為 UWP 應用程式可以透過 Microsoft Store。 您可以安裝在 WSL-在 Windows 核心中的子系統便會執行這些應用程式。 這個傳遞機制有許多優點，先前的部落格文章中所述。

## <a name="sideloading-a-custom-linux-distro-package"></a>側載自訂的 Linux 散發套件
在您的個人電腦上，您可以為要側載應用程式建立自訂的 Linux 散發套件。 請注意，自訂套件將無法散發透過 Microsoft Store 除非您為發佈維護程式送出。
若要設定您的電腦，側載應用程式，您必須在 「 適用於開發人員 」 下的系統設定中啟用。  請務必要有開發人員模式或選取的側載應用程式

## <a name="for-linux-distro-maintainers"></a>針對 Linux 散發套件維護人員
若要提交至市集，您必須與我們配合以接收發行的核准。 如果您想要將您的散發套件新增至 Microsoft Store 的 Linux 發佈擁有者，請連絡wslpartners@microsoft.com。

## <a name="getting-started"></a>開始使用
遵循上的指示[Distro 啟動器 GitHub 存放庫](https://github.com/Microsoft/WSL-DistroLauncher)來建立自訂的 Linux 散發套件。

 
## <a name="team-blogs"></a>小組部落格
*  [開啟來源 WSL 範例 Linux 發行版本維護者和側載自訂的 Linux 散發套件](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [命令列的部落格](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>提供意見反應
* [散發套件在啟動器 Github 存放庫](https://github.com/Microsoft/WSL-DistroLauncher)
* [WSL 的 GitHub 問題追蹤器](https://github.com/Microsoft/BashOnWindows/issues)
* [命令列的 UserVoice 入口網站](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
