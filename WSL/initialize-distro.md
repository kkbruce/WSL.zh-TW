---
title: 初始化新的 WSL Linux 散發版本
description: 安裝適用于 WSL 的 Linux 散發版本之後, 請遵循下列簡單步驟來完成初始化
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499293"
---
# <a name="initializing-a-newly-installed-distro"></a>將新安裝的散發版本初始化
下載並安裝散發版本之後, 您必須完成新散發版本的初始化:

## <a name="launch-a-distro"></a>啟動散發版本
若要完成新安裝散發版本的初始化, 請啟動新的實例。 若要這麼做, 您可以按一下 Microsoft Store 應用程式中的 [啟動] 按鈕, 或從 [開始] 功能表啟動散發版本:

> 秘訣：您可能想要將最常使用的散發版本釘選到 [開始] 功能表和/或您的工作列!

![從 [開始] 功能表啟動散發版本](media/start-menu.png)

> 在 Windows Server 上, 您可以從散發版本安裝資料夾啟動`<distro>.exe`散發版本的啟動器可執行檔。

第一次執行新安裝的散發版本時, 主控台視窗將會開啟, 而且系統會要求您等候一或兩分鐘的時間來完成安裝。

> 在安裝的最後一個階段, 會將散發版本的檔案解除壓縮並儲存在您的電腦上, 以供使用。 這可能需要一分鐘或更長的時間, 視電腦的存放裝置效能而定。 只有在清除安裝散發版本時, 才需要執行此初始安裝階段-所有未來的啟動都應該不到一秒。

## <a name="setting-up-a-new-linux-user-account"></a>設定新的 Linux 使用者帳戶

安裝完成之後, 系統會提示您建立新的使用者帳戶 (及其密碼)。 

![Windows 主控台中的 Ubuntu 解壓縮](media/UbuntuInstall.png)

這個使用者帳戶是針對您在啟動散發版本時, 預設將登入的一般非系統管理員使用者。

> 您可以選擇任何您想要的使用者名稱和密碼, 而不會影響您的 Windows 使用者名稱。 

當您開啟新的散發版本實例時, 系統不會提示您輸入密碼, 但**如果您使用`sudo`** 來提高進程的許可權, 就必須輸入您的密碼, 因此請務必選擇您可以輕鬆記住的密碼! 如需詳細資訊, 請參閱[使用者支援](user-support.md)頁面。

## <a name="update--upgrade-your-distros-packages"></a>更新 & 升級散發版本的套件

大部分的散發版本都隨附空的/最小的套件目錄。 我們強烈建議您定期更新您的套件目錄, 並使用散發版本的慣用套件管理員升級已安裝的套件。 在 Debian/Ubuntu 上, 您可以使用 apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不會自動更新或升級您的 Linux 散發版本:這是 Linux 使用者偏好控制自己的工作。

大功告成！ 在 WSL 上盡情使用您的新 Linux 散發版本! 若要深入瞭解 WSL, 請參閱其他[WSL](https://aka.ms/wsldocs)檔或[WSL learning 資源頁面](https://aka.ms/learnwsl)。

![在 WSL 上享用使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑難排解

以下是相關的錯誤和建議的修正。 如需其他常見錯誤及其解決方案, 請參閱[WSL 疑難排解頁面](troubleshooting.md)。

> **安裝失敗, 發生錯誤 0x8007007e**當您的系統不支援存放區中的 Linux 時, 就會發生此錯誤。  請確認︰
> * 您正在執行 Windows 組建16215或更新版本。 [檢查您的組建](troubleshooting.md#check-your-build-number)。
> * [適用于 Linux 的 Windows 子系統] 選用元件已啟用, 且電腦已重新開機。  [請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
