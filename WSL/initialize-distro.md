---
title: 初始化新的 WSL Linux 散發套件
description: 之後 WSL 安裝的 Linux distro，請遵循下列簡單步驟來完成初始設定
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063606"
---
# <a name="initializing-a-newly-installed-distro"></a>初始化新安裝的散發套件
一旦下載及安裝您散發版本，您必須完成初始化新的散發版本：

## <a name="launch-a-distro"></a>啟動散發版本
若要完成初始化的新安裝的散發版本，啟動新的執行個體。 您可以藉由按一下 Windows 市集應用程式中中的 「 啟動 」 按鈕，或啟動從 [開始] 功能表的散發版本來這樣做：

> 秘訣：您可能想要釘選到 [開始]，和/或工作列所做的您最常使用的散發套件 ！

![啟動散發版本，從 [開始] 功能表](media/start-menu.png)

> 在 Windows 伺服器上，您可以啟動您的散發套件的可執行檔啟動程式`<distro>.exe`從散發套件安裝資料夾。

第一次新安裝的散發套件執行的主控台視窗隨即開啟，並需要等候幾分鐘的時間才能完成安裝。

> 在安裝此最終階段中，發行版本的檔案取消壓縮，並儲存在您的電腦，可供使用上。 這可能需要一分鐘的時間或多個根據您的電腦的存放裝置效能。 這個初始的安裝階段只是必要的散發套件為全新安裝-所有未來的啟動花費時間少於一秒。

## <a name="setting-up-a-new-linux-user-account"></a>設定新的 Linux 使用者帳戶

安裝完成之後，系統會提示您建立新的使用者帳戶 （和其密碼）。 

![打開包裝 Windows 主控台中的 Ubuntu](media/UbuntuInstall.png)

此使用者帳戶是一般的非系統管理員使用者，您將是已登入做為預設時啟動的散發版本。

> 您可以選擇任何使用者名稱和您想要的密碼-它們對您的 Windows 使用者名稱並無任何影響。 

當您開啟新的散發版本執行個體時，您將不會提示您輸入密碼，但**如果您使用提升權限處理程序`sudo`，您必須輸入密碼**，因此請確定您選擇的密碼，您可輕易記住 ！ 請參閱[使用者支援](user-support.md)如需詳細資訊 頁面。

## <a name="update--upgrade-your-distros-packages"></a>更新和升級您的散發套件

大部分的散發版本隨附的最小空白/封裝目錄中。 我們強烈建議您套件的目錄，定期進行更新和升級您已安裝的套件，使用您的散發版本首選的套件管理員。 在 Debian/Ubuntu，您使用 apt 項目：

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不會自動更新或升級 Linux distro(s):這是 Linux 使用者想要控制自己的工作。

大功告成！ 享受在 WSL 使用新的 Linux 發行版本 ！ 若要深入了解 WSL，檢閱另[WSL docs](https://aka.ms/wsldocs)，或有[WSL 學習資源頁面](https://aka.ms/learnwsl)。

![享受 WSL 上使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑難排解

以下是相關的錯誤和建議的修正。 請參閱[WSL 疑難排解頁面](troubleshooting.md)其他常見的錯誤和他們的解決方案。

> **安裝失敗，錯誤 0x8007007e**系統不支援 Linux，從存放區時，會發生此錯誤。  請確認︰
> * 您正在執行 Windows 組建，16215 或更新版本。 [請檢查您的組建](troubleshooting.md#check-your-build-number)。
> * 已啟用 Linux 選擇性元件的 Windows 子系統，並重新啟動電腦。  [請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
